# AWS: API, Dynamo and Lambda

## AWS API Gateway Overview

- **What is Amazon API Gateway?**

A managed service provided by AWS that enables developers to create, publish, maintain, monitor, and secure APIs at any scale. It allows the definition of HTTP endpoints for REST or WebSocket APIs and connects these ends points to the corresponding backend business logic. API Gateway handles various aspects of the API lifecycle, including authentication, access control, monitorning, and tracing API requests. It serves as a critical component in serverless architectures, replacing traditional API servers with a managed serverless solution, thereby streamlining the process of API management and deployment. 

- **What is Amazon API Gateway an important part of the Serverless ecosystem?**

Amazon API Gateway plays an important role in the serverless ecosystem due to its ability to seamlessly connect HTTP requests to serverless functions, such as AWS Lambda. This integration is key to enabling a truly serverless architecture for web apps, as it allows the execution of serverless functions in direct response to HTTP requests. By doing so, API Gateway facilitates the creation of scalable, low-maintenance web apps without the need for managing servers. This integration not only enhances the efficiency of deploying serverless apps but also leverages the full potential of serverless computing in terms of scalability and cost-effectiveness. 

- **How does API Gateway integrate with other AWS services?**

API Gateway integrates extensively with a range of AWS services, enhancing its capabilities and flexibility. It works closely with AWS Lambda, allowing Lambda functions to be triggered by API calls and to generate HTTP API responses. Integration with Amazon Simple Notification Service enables the publication of notifications upon API endpoint access. For authentication and authorization, it integrates with Amazon Cognito, providing secure access to HTTP APIs. Additionally, API Gateway supports direct integrations for invoking Lambda functions, making HTTP calls to AWS service APIs, and generating mock responses. These integrations enable developers to build robust, scalable, and secure apps by leveraging the comprehensive suite of AWS services in conjunction with API Gateway. 

## AWS API Gateway 

- **What are some benefits of using Amazon API Gateway?**

1. Efficient API Development: It enables the running of multiple API versions concurrently, facilitating rapid development, and testing of APIs

2. Scalability and Performance: API Gateway ensures low latency for API requests and responses and is capable of handling a high volume of concurrent API calls. This is further enhanced by its integration with Amazon CloudFront, which distributes traffic across a global network of edge locations. 

3. Cost-Effectiveness: The service allows a tiered pricing model, which becomes more economical with increased API usage. Additionally, the AWS Free Tier includes plenty of API calls per month for the first 12 months, reducing initial costs for new users. 

- **What two API types might you choose from?**

1. RESTful APIs: These are optimized for serverless workloads and HTTP backends. They are ideal for apps that require API proxy functionality. RESTful APIs in API Gateway can be further categorized into HTTP APIs, which are more streamlined and cost-effective for most use cases, and REST APIs, which offer more comprehensive API management features. 

2. WebSocket APIs: These are designed for building real-time, two-way communication apps such as chat apps or streaming dashboards. WebSocket APIs maintain a persistent connection between the backend service and the clients, facilitating an ongoing exchange of messages. 

## AWS DynamoDB Guide

- **What is DynamoDB?**

A fully managed NoSQL database provided by AWS. It is designed to offer fast and predictable performance with seamless scalability. DynamoDB allows users to store and retrieve any amount of data and serve any level of request traffic. It supports key-value and document data structures, making it versatile for a wide range of apps. 

- **Under what circumstances would you recommend DynamoDB over MongoDB?**

1. Serverless Architecture: For applications built on AWS, especially serverless architectures using AWS Lambda, DynamoDB is a natural choice due to its tight integration with AWS services, including IAM for security.

2. Predictable Performance at Scale: If an application requires consistent, low-latency performance at any scale, DynamoDB is preferable. It is designed to handle large-scale, high-traffic applications with predictable performance.

3. Fully Managed Service: For teams that prefer a fully managed database without the need to handle server maintenance, patching, or setup, DynamoDB offers a hassle-free solution compared to self-managed MongoDB instances.

## AWS DynamoDB

- **Explain to a non-technical friend how DynamoDB works**

DynamoDB is like a filing cabinet where you store various documents in different drawers and folders. DynamoDB lets you store all sorts of info in a structured way. It is fast and can grow with your needs. You don't have to worry about maintaining it either; AWS takes care of all the technical stuff like security and making backups. 

##

- **What is Dynamoose?**

Dynamoose is a modeling tool specifically designed for Amazon's DynamoDB, tailored for use in JavaScript environments. Dynamoose simplifies the process of working with DynamoDB by providing a high-level API and a user-friendly syntax, making it easier to interact with DynamoDB in a JavaScript application. It abstracts the complexities of direct database interactions, allowing developers to focus more on application logic rather than the intricacies of database operations.


- **What are some key features of Dynamoose?**

1. Strict Data Modeling: The tool includes features for data validation, setting required attributes, and more, ensuring the integrity and consistency of the data.

2. Type Safety: It ensures consistent use of data types, which helps in reducing errors and improving the reliability of the code.

3. High-Level API: The API provided by Dynamoose abstracts the complexities of DynamoDB, making it more accessible and simpler for developers to use.

4. Easy-to-Use Syntax: Inspired by Mongoose, Dynamoose's syntax is designed to be intuitive and straightforward, facilitating quicker development and easier code maintenance.

## Reflection

My goal is to understand how to set up a serverless, CRUD-enabling API, mirroring what we've previously achieved with Express. I aim to grasp the nuances of AWS API Gateway, particularly how to trigger Lambda functions in response to API requests and the differences between HTTP and REST APIs within AWS. Another key learning objective is to differentiate between DynamoDB and MongoDB, understanding their unique features and use cases.

### Citation
- [Amazon API Gateway Guide](https://www.serverless.com/guides/amazon-api-gateway)
- [Amazon API Gateway - AWS](https://aws.amazon.com/api-gateway/)
- [What is DynamoDB? - DynamoDB Guide](https://www.dynamodbguide.com/what-is-dynamo-db/)
- [Amazon DynamoDB - AWS](https://aws.amazon.com/dynamodb/)
- [Dynamoose - DynamoDB Client and SDK [JavaScript]](https://dynamoosejs.com/getting_started/Introduction)
