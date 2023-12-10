# AWS: Understanding S3 and Lambda

## Amazon S3

### What is Amazon S3? 
Amazon Simple Storage Service (Amazon S3) is a robust cloud storage solution from AWS. It offers industry-leading scalability, data availability, security, and performance. S3 caters to various needs, from basic file storage to complex applications, supporting data storage for websites, mobile apps, backup and restore, archives, enterprise applications, and data analytics. Its key features include high durability, availability, and scalability, making it an effective and secure data management solution in the cloud.

### Use Cases for Amazon S3
- Building data lakes for storing structured and unstructured data.
- Running big data analytics, AI, machine learning, and high-performance computing applications.
- Backup and restoration of critical data with robust replication features.
- Archiving data cost-effectively using Glacier storage classes.
- Providing scalable, high-performance storage for cloud-native, mobile, and web apps.

### Benefits of Amazon S3
- Scalability and data durability with cost-effective storage classes.
- Robust security features, compliance, and audit capabilities.
- Comprehensive data management with access controls, replication tools, and organizational visibility.

## AWS Lambda: Basics

### What is AWS Lambda? 
AWS Lambda is a serverless computing service by AWS, allowing code execution without server management. It automates the execution and scaling of code written as functions. Lambda can perform tasks like data processing, AWS service integration, and web app powering. It simplifies infrastructure management, supporting various programming languages and offering a cost-effective, usage-based billing model.

### Use Cases for AWS Lambda
- Building scalable APIs with automatic scaling.
- Event-driven data processing, reacting to AWS service data changes.
- Automating tasks like database updates, log cleanups, or backups.
- Integrating AWS services for complex workflows and data processing without dedicated servers.

### Describe 'serverless' to a non-technical friend
Imagine hiring a catering service for a party, where they handle food preparation, setup, and cleanup. In this analogy, the party is like running an application, and the catering service represents 'serverless' computing. With serverless computing, you provide the software (plan the menu) but don’t worry about the servers (kitchen and equipment). AWS, like the caterers, manages the technical aspects, allowing you to focus on your software.

## Content Delivery Network (CDN)

### What is a CDN?
A Content Delivery Network (CDN) is a globally distributed network of servers enhancing the delivery of internet content. It caches web content like HTML pages, javascript files, stylesheets, images, and videos to deliver them efficiently. The CDN's goal is to boost speed and performance by reducing the distance between the server and the user, improving website and web application user experience.

### How does a CDN work with relation to the website visitors? 
When a user requests a CDN-served webpage, the request is redirected to the closest CDN server. This server, having cached the content, responds swiftly, reducing webpage load time. If the content isn't cached, the CDN retrieves it from the original server or a closer node, ensuring quick delivery even for uncached content.

### What are the benefits of employing a CDN? 
- Faster web content delivery, enhancing user experience.
- Improved handling of high traffic and quicker page load times.
- Enhanced security, including DDoS attack protection, by distributing load across multiple servers.
- Reduced bandwidth costs as much of the content is served from the CDN's cache.

#### References
- [Amazon S3 - Cloud Object Storage](https://aws.amazon.com/s3/)
- [AWS Lambda: The Ultimate Guide - Serverless](https://www.serverless.com/aws-lambda)
- [Content Delivery Network (CDN) - CyberHoot](https://cyberhoot.com/cybrary/content-delivery-network-cdn/)
