# AWS Workshop: Serverless Web Game Architecture (Chrono Genesis TCG)

Welcome to the documentation repository for building the **Chrono Genesis Game** – a fully Serverless Real-time Architecture web game on AWS!

## Overview
This workshop guides you through designing, configuring, and deploying a real-time multiplayer card game entirely on the AWS Serverless platform. 

## Key Technologies & Services
- **Amazon API Gateway (WebSocket API) & Amazon Cognito**: Maintain real-time connections and authenticate users securely using JWT.
- **AWS Lambda & Amazon SQS**: Process complex business logic, handle background workers for EXP/Rank calculation asynchronously.
- **Amazon DynamoDB**: Provide a robust NoSQL database to store game states and player statistics in real-time.
- **AWS Amplify Hosting**: Globally distribute and host the React/TypeScript frontend with automated CI/CD.

## Structure
The site is built using the [Hugo](https://gohugo.io/) static site generator with a documentation theme. It contains multiple chapters covering:
1. Preparation & Prerequisites (IAM, Cognito)
2. Backend Infrastructure (DynamoDB, Lambda, API Gateway)
3. Event-Driven workflows (SQS, EventBridge)
4. Frontend Deployment & Cleanup

## How to run locally
1. Install [Hugo](https://gohugo.io/installation/) (Extended version recommended).
2. Clone this repository.
3. Run `hugo server -D` in the root directory.
4. Open `http://localhost:1313` in your browser.

## Team Lacrimosa
This workshop documentation and the Chrono Genesis TCG game are proudly created by the Lacrimosa team.

> Check out the live demo of our game: [TCG Chrono Genesis](https://dev.d3oenyc702mfnb.amplifyapp.com/)
