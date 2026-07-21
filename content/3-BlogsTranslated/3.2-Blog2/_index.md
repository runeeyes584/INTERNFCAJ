---
title: "Blog 2"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
---

# BUILDING A CONTEXTUAL CHATBOT APPLICATION USING KNOWLEDGE BASES FOR AMAZON BEDROCK

## INTRODUCTION

Modern chatbots provide 24/7 customer support services with the capability to process multiple queries simultaneously in various languages. Although Large Language Models (LLMs) bring natural understanding and response capabilities, if a chatbot can only answer basic questions, its overall utility remains limited.
To make a chatbot more reliable, we need to connect it with internal information systems and databases. Integrating this proprietary data allows the chatbot to personalize responses and tailor its language to match the user's expertise.

## RETRIEVAL AUGMENTED GENERATION (RAG) ARCHITECTURE

The most common way to bring context to LLMs is by using Retrieval Augmented Generation (RAG) architecture. This method combines the text generation power of LLMs with the ability to search and extract factual information from a database.

The RAG workflow consists of two main streams:

- Data Ingestion: Uses an LLM to generate vector embeddings representing the meaning of documents. Documents are split into chunks and stored as indexes in a vector database.
- Text Generation: Converts user questions into vectors, retrieves the most similar document chunks from the database to supplement context, and then prompts the LLM to generate an answer based on that context.

Building a RAG system manually is complex because it requires high-level engineering skills to manage dependencies across databases, search mechanisms, prompt engineering, and generative models. It can take weeks for an engineering team just to set up and optimize.

## AMAZON BEDROCK KNOWLEDGE BASES - THE OPTIMAL SERVERLESS SOLUTION

To reduce engineering overhead, Amazon Bedrock Knowledge Bases provides a serverless RAG system that automatically manages both the data ingestion and text generation workflows.

- The `StartIngestionJob` API automates document chunking, vector embedding creation, and storage.
- The `RetrieveAndGenerate` API automatically retrieves relevant information and generates accurate responses.

## CHATBOT SOLUTION ARCHITECTURE OVERVIEW

The architecture design workflow includes the following steps:

1. Users upload datasets to Amazon S3 (acting as the data source).
2. Amazon S3 invokes an AWS Lambda function to sync the data source with the knowledge base via `StartIngestionJob`.
3. The system chunks the documents, uses the Amazon Titan model to generate embeddings, and stores them in an Amazon OpenSearch Serverless vector store.
4. On the user interface, users ask questions in natural language.
5. The query is sent via Amazon API Gateway to another Lambda function, which calls the `RetrieveAndGenerate` API.
6. Bedrock uses the Titan model to search for similar text and then sends this context along with the question to the Anthropic Claude Instant 1.2 LLM to generate a response. Claude Instant 1.2 was selected due to its fast speed, cost efficiency, and strong conversational handling.
7. Finally, users receive an answer with specific citations.

## PREREQUISITES

To set up this solution, you need to:
- Request access to the Amazon Titan Embeddings G1 – Text and Claude Instant 1.2 models in Amazon Bedrock.
- Select an AWS Region supported by Amazon Bedrock.
- For local deployment, install and configure AWS CLI, AWS CDK, Node.js 20.x, and Docker.

## SOLUTION DEPLOYMENT

The solution is available in the GitHub repository: https://github.com/aws-samples/amazon-bedrock-rag

Complete the following steps to deploy the solution:

1. From the command line, navigate to the backend directory: `cd backend`
2. Install the necessary dependencies: `npm install`
3. Use AWS CDK to deploy the backend of the chatbot application: `cdk deploy --context allowedip="xxx.xxx.xxx.xxx/32"`

## CONCLUSION

Through its built-in RAG architecture, Amazon Bedrock Knowledge Bases thoroughly addresses the operational complexities of information retrieval systems. The result is a superior Chatbot application capable of querying proprietary company data, providing highly personalized answers while maintaining transparency regarding information sources. Furthermore, the entire infrastructure of this project is packaged as Infrastructure as Code via AWS CDK, making it easy to deploy, customize, and scale on the AWS environment.

![Blog2](/images/3-Blog/blog2.png)

[Link to published blog post](https://www.facebook.com/groups/awsstudygroupfcj/posts/2208429953255298/?locale=en_US)

[Link to reference material](https://aws.amazon.com/blogs/machine-learning/build-a-contextual-chatbot-application-using-knowledge-bases-for-amazon-bedrock/)
