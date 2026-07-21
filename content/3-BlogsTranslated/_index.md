---
title: "Published Blogs"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

During the internship at FCAJ, my **Lacrimosa** team and I have published 3 blogs according to FCAJ's regulations. The representative of the team is **Tuong Vi**, who is responsible for posting the blogs on behalf of the team. These blogs include:

### [Blog 1 - OPTIMIZING LAKEHOUSE ARCHITECTURE WITH AMAZON SAGEMAKER](3.1-Blog1/)

This blog introduces the Lakehouse Architecture with Amazon SageMaker. The Lakehouse Architecture with Amazon SageMaker provides a unified solution for organizations, combining the flexibility of a Data Lake with the performance of a Data Warehouse on an open platform. The system is built on four core components: flexible storage, centralized technical catalog (AWS Glue), fine-grained access control (AWS Lake Formation), and an open API framework based on Apache Iceberg. Enterprises can choose from three data integration methods—traditional ETL, automated Zero-ETL, or Data Federation without data movement—along with optimal storage options (S3 + Iceberg, S3 Tables, or Redshift Managed Storage) depending on latency and performance requirements. This approach allows organizations to build highly scalable, AI/ML-ready data systems without compromising between flexibility and cost optimization.

### [Blog 2 - BUILDING A CONTEXTUAL CHATBOT APPLICATION USING AMAZON BEDROCK KNOWLEDGE BASES](3.2-Blog2/)

This blog discusses building a smart chatbot by combining LLMs with the RAG (Retrieval Augmented Generation) architecture to provide answers based on an organization's proprietary data. Instead of building a complex RAG system from scratch (which requires managing vector embeddings, databases, semantic search, etc.), Amazon Bedrock Knowledge Bases offers a serverless solution that automates the entire process: from data ingestion (StartIngestionJob splits documents, creates embeddings using Amazon Titan, saves to OpenSearch Serverless) to querying and generating responses (RetrieveAndGenerate combines Titan embeddings with Claude Instant 1.2). The architecture uses S3 as the data source, Lambda to automate the workflow, API Gateway for the user interface, and Infrastructure as Code (AWS CDK) for easy deployment and scaling—helping the technical team focus on business value rather than complex operations.

### [Blog 3 - BUILDING A MULTIPLAYER GAME WITH AWS SERVERLESS ARCHITECTURE](3.3-Blog3/)

This blog covers building a multiplayer web game using AWS Serverless architecture to optimize development time, costs, and automatic scaling capabilities. The Simple Trivia Service project demonstrates how serverless services (Lambda, API Gateway, DynamoDB, SNS) combine with supporting tools (Cognito, ElastiCache, AWS IoT) to build a complete game featuring both single-player and multiplayer modes. Depending on the requirements of each game mode: the single-player mode uses HTTP API + SNS to update scores asynchronously; the multiplayer mode typically utilizes API Gateway WebSockets with state managed from the client side; while the live leaderboard mode (requiring ultra-low latency) uses AWS IoT + ElastiCache for Redis to store backend states and provide real-time updates for all players. This architecture not only saves operational costs but also frees the development team from the burden of server configuration, allowing them to focus on content creation and player experience.
