---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# Chrono Genesis Game

## Turn-based trading card web game built on Serverless architecture on the AWS platform

### 1. Executive Summary

The project is Chrono Genesis Game, a turn-based trading card web game built on a Serverless Real-time Architecture on the AWS platform.

The entire game uses WebSocket to synchronize data in real-time. Match operations are processed by multiple specialized AWS Lambdas. The system exclusively uses Amazon DynamoDB as a comprehensive data center, fulfilling two roles: storing the match state (Game State) with millisecond-level latency in real-time, while securely storing long-term data (User, Deck, Match History, Logs) and optimizing costs.

### 2. Problem Statement

*Current Problems*

- Traditional real-time game systems require continuous server maintenance costs even when there are no players.
- Network latency negatively impacts the experience of a game that requires continuous tactical calculations.

*Solution*  
Deploy a Serverless Real-time Architecture via Amazon API Gateway (WebSocket API) and AWS Lambda functions to create independent processing flows. Consolidate into a single Game Engine flow that interacts directly with Amazon DynamoDB to update the state, ensuring low latency and cost savings.

### 3. Solution Architecture

The platform applies AWS Serverless architecture to operate a real-time trading card web game application, capable of automatically scaling to accommodate thousands of concurrent players. The user interface is distributed via AWS Amplify and Route 53, secured and authenticated by Amazon Cognito.

Two-way real-time connections (Real-time WebSocket) are routed through Amazon API Gateway to directly interact with a set of AWS Lambda functions (Start Match, Process Game Engine, Save Deck, Handle Timeout, End Match) to centrally process the entire game logic.

Game data and connection information are stored in Amazon DynamoDB. In addition, after the match ends, events are pushed to Amazon SQS for a Lambda function (Post Match Worker) to asynchronously process tasks such as updating Rank, EXP, and saving match history, ensuring the system achieves high performance and ultra-low latency.

![Chrono Genesis TCG Game Architecture](/images/2-Proposal/ar.jpg)

*AWS Services Used*

- *AWS Amplify*: Host and distribute the web game interface (React/TypeScript), automate CI/CD.

- *AWS Lambda*: Process data and trigger Glue jobs (2 functions).

- *Amazon Route 53*: Communicate with the web application.

- *Amazon S3*: Manage domain names and route player traffic to the application.

- *Amazon Cognito*: Authenticate player identities, manage login sessions, and issue JWT Tokens.

- *Amazon API Gateway (WebSocket API)*: Manage two-way real-time connections between Client and Server.

- *AWS Lambda*: Centrally process game logic and computational tasks.

- *Amazon SQS*: Asynchronous queue to receive data from the Lambda Engine and process it.

- *Amazon DynamoDB*: NoSQL database to store match states, connections, and user data.

- *Security & Monitoring (IAM, KMS, Secrets Manager, CloudWatch, X-Ray)*: Secure permissions, manage keys, track logs, and monitor system performance.

*Component Design*

- *Real-time Routing*: Amazon API Gateway combined with Route 53 manages two-way WebSocket connections between players and the system.

- *Game Logic Processing*: A collection of AWS Lambda functions acting as a centralized Game Engine.

- *Asynchronous Processing*: Amazon SQS receives end-of-match events for the Lambda worker to automatically calculate Rank, EXP, and save history.

- *Data Processing*: Amazon DynamoDB stores the board state, connection information, and player profiles.

- *Web Interface*: Built with React / TypeScript, packaged and distributed via AWS Amplify's CDN network.

- *User Management*: Use Amazon Cognito User Pool to manage the entire account lifecycle (registration, authentication, password reset, and session revocation).

### 4. Technical Implementation

*Implementation Phases*

1. Infrastructure Initialization: Deploy the environment, domain name, and set up CI/CD via AWS Amplify.

2. Connection & Authentication: Configure Amazon Cognito for users and set up the WebSocket connection flow via API Gateway.

3. Game Engine Development: Program core Lambda functions (Start Match, Process Action, End Match) to handle card logic.

4. Post-Match Processing: Configure the SQS queue and Lambda Worker to process Rank points and history without bottlenecking the system.

5. Testing & Optimization: Monitor with X-Ray and CloudWatch, optimize security with WAF/IAM, and conduct load testing (Stress Test).

*Technical Requirements*

- *System Infrastructure*: AWS Amplify (Hosting & CI/CD), GitHub, Route 53 (domain name), IAM, and VPC to deploy, manage, and secure the system.

- *Game Platform*: Amazon Cognito (JWT authentication), API Gateway (WebSocket), AWS Lambda (game logic processing), DynamoDB (store player data, matches, decks), Amazon SQS (post-match task processing), CloudWatch and X-Ray (monitoring), AWS WAF (security). Frontend uses React connected via WebSocket to synchronize match states in real-time.

### 5. Timeline & Milestones

- *Pre-internship (Month 0)*: 1 month of planning.
  - Month 1: Learn about AWS services, practice Labs to consolidate knowledge.
  - Month 2: Design and adjust architecture.
  - Month 3: Deploy, test, and put into use.
- *Post-deployment*: Research and develop additional new features.

### 6. Budget Estimation

*Infrastructure Costs*

- AWS Amplify: $0.00 - $0.02/month (~500 MB hosting, a few CI/CD deployments, within the 12-month Free Tier).

- Amazon Route 53: $0.50/month (01 Hosted Zone, domain name fee not included).

- Amazon Cognito: $0.00/month (≤ 10 users, within the MAU Free Tier).

- Amazon API Gateway (WebSocket): $0.00 - $0.02/month (~20,000 WebSocket messages and low connection time, within Free Tier).

- AWS Lambda: $0.00/month (~50,000 requests, 512 MB, under the 1 million requests and 400,000 GB-s Free Tier).

- Amazon DynamoDB: $0.00/month (≈1 GB of data, choose Provisioned mode 25 WCU/RCU to achieve $0 within Free Tier).

- Amazon SQS: $0.00/month (~10,000 messages, under Free Tier).

- Amazon CloudWatch: $0.00/month (≈1 GB log storage, under the 5 GB free/month threshold).

- AWS X-Ray: $0.00/month (low trace volume, within Free Tier).

- AWS KMS: $0.00/month (uses AWS managed keys).

- AWS Systems Manager Parameter Store: $0.00/month (Replaces Secrets Manager to store 01 Secret completely free).

- Internet Data Transfer: $0.00/month (~1 GB Data Transfer Out, under the 100 GB free/month threshold).

- AWS WAF: $0.00/month (if temporarily disabled) / ≥ $5.00/month (if 01 Web ACL is enabled to filter malicious requests).

*Total Cost*:

- MVP Infrastructure Cost (Excluding WAF): approx. $0.54/month (~$6.50/year).

- MVP Infrastructure Cost (Including WAF): approx. $5.54/month (~$66.50/year).

### 7. Risk Assessment

*Risk Matrix*

- Lambda Cold Start causing lag in the first turn: Medium probability, medium impact.

- WebSocket network disconnection from the player's side: High probability, high impact.

- Reaching AWS Quota limits: Low probability, very high impact.

*Mitigation Strategies*

- Mitigate Lambda Cold Start: Optimize startup time by reducing package size, reusing connections, and only configuring Provisioned Concurrency for real-time processing Lambdas (Process Game Engine) when the system experiences high traffic. This solution significantly reduces latency on the first turn while optimizing operational costs.

- Mitigate WebSocket Disconnection: Build an Auto-Reconnect mechanism on the Frontend combined with sending periodic alerts to detect disconnections. When a player reconnects, API Gateway and Lambda update the new Connection ID into DynamoDB, then resynchronize the current Game State so the player can continue the match without creating a new session.

- Mitigate Reaching AWS Quota Limits: Set up CloudWatch Metrics and CloudWatch Alarms to monitor the number of WebSocket connections, Lambda Invocations, and critical resources. When resources reach about 70–80% of the limit, the system sends an email alert so administrators can proactively request a quota increase before it affects users.

*Contingency Plans*

- Resource Expansion: When AWS resources approach the Service Quota, the administrator requests a quota increase and temporarily limits the creation of new matches, prioritizing resources for ongoing matches to ensure system stability.

### 8. Expected Outcomes

- *Technical Improvements*: Successfully build a Game Engine flow entirely on a Serverless platform, replacing continuously maintained servers to save costs.

- *Long-term Value*: A data platform used for game development, reusable for future projects.
