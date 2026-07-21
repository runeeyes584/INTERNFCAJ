---
title: "Blog 3"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.3. </b> "
---
# BUILDING A MULTIPLAYER GAME WITH AWS SERVERLESS ARCHITECTURE

## INTRODUCTION

Game development is a highly iterative process with rapidly changing requirements. Many game developers want to optimize feature building time and reduce time spent on server configuration, infrastructure management, and scaling. Adopting an AWS Serverless architecture brings 4 core benefits: accelerating time-to-market, saving costs, automatically scaling with the number of players, and built-in service integration.
To demonstrate this, below is a web game project based on a serverless-first architecture, possessing fully functional real-world features such as single/multiplayer modes, registration, messaging, leaderboards, and content creation.

## OVERVIEW OF SIMPLE TRIVIA SERVICE – A SIMPLE TRIVIA GAME

### User Interface (Front-end)

The game's interface is built as a Single Page Application (SPA) using Vue.js, connecting to backend services via HTTPS and WebSockets. This frontend is built, deployed, and hosted using AWS Amplify without needing server management.

### Backend Architecture and Services Used

The backend is defined via AWS Serverless Application Model (AWS SAM) templates. The architecture uses a combination of various diverse services:

- Core Serverless services: AWS Lambda (runs microservices code), Amazon API Gateway and AWS IoT (provides endpoints for HTTP and WebSockets), Amazon DynamoDB (stores data), and Amazon SNS (pub/sub messaging).
- Other supporting services: Amazon Cognito for login management, Athena/Kinesis/S3 for data analysis, and Amazon ElastiCache for Redis (non-serverless) placed in a VPC to meet ultra-low latency requirements.

### Security and Communication

Players need to register and log in via Amazon Cognito; after authentication, the system returns a JWT token for API Gateway to authorize requests sent to Lambda. For IoT connections, security is further enhanced through AWS IAM policies.

### Gameplay Architecture Models of Simple Trivia Service

Depending on the game mode, the game applies different backend architectures:

- Single Player Mode: Uses API Gateway (HTTP API) for one-way communication from the player to the system. Lambda functions handle game logic and scoring. Specifically, the player's score and progress are asynchronously updated via Amazon SNS, allowing players to receive immediate results without waiting for the system to write to the database.
- Multiplayer Mode - Casual and Competitive: This mode requires continuous two-way communication, thus using API Gateway WebSockets. The game's state is managed directly by the room host's client. The system uses DynamoDB to track which players are connected and which room they joined.
- Multiplayer Mode - Live Leaderboard: This structure is more complex, using AWS IoT (WebSockets over MQTT) as the primary transport method. The biggest difference is that the game state is shifted from the client to being stored at the backend using ElastiCache for Redis to ensure millisecond-level response times, helping the entire player leaderboard update in real-time.

## CONCLUSION

Through the practical Simple Trivia Service project, it has been proven that a complete AWS ecosystem can smoothly and flexibly handle even the most demanding requirements of the gaming industry. Serverless architecture is not merely a cost-optimization solution, but it is truly reshaping the design and operational mindset of game developers. By completely removing the burden of server configuration and infrastructure management, the "serverless-first" approach empowers development teams to pour all their dedication into the most core aspects: content creation, enhancing player experience, and maximizing time-to-market reduction.

![Blog3](/images/3-BlogsPosted/Blog3.png)

[Link to published blog post](https://www.facebook.com/groups/awsstudygroupfcj/posts/2209312269833733?locale=en_US)

[Link to reference material](https://aws.amazon.com/blogs/compute/building-a-serverless-multiplayer-game-that-scales/)
