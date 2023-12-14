# AWS: Events

## AWS SQS vs SNS: 

- **What is the difference between SQS and SNS?**

SQS (Simple Queue Service) and SNS (Simple Notification Service) are both messaging services in AWS, but they serve different purposes. SQS is a message queuing service that enables the storage of messages in a queue, allowing applications to process and respond to them asynchronously. It's designed for decoupling components of a cloud application, ensuring that if one component fails, the messages are not lost. On the other hand, SNS is a publish-subscribe messaging service. It enables sending messages to a large number of subscribers, including systems, users, or mobile devices, simultaneously. While SQS is about storing and then processing messages, SNS is about immediately broadcasting messages to multiple subscribers.

- **What are some use cases for both SNS and SQS?**

Use Cases for SNS (Simple Notification Service):

- Triggering Notifications: Ideal for sending real-time alerts via email or SMS, such as system failures or transaction alerts.
- Message Distribution to Multiple Subscribers: Efficient for broadcasting messages to a wide range of subscribers for parallel processing.
- Integration with AWS Lambda: Useful for triggering serverless functions in response to events, enabling scalable, event-driven architectures.
- Real-Time Data Streaming: Facilitates the streaming of data to various endpoints, ensuring timely data delivery for processing and analysis.

Use Cases for SQS (Simple Queue Service):

- Decoupling System Components: Helps in separating different parts of a system to ensure that if one part fails, it doesn’t impact the others.
- Handling Sporadic Data Flows: Effective in managing messages or tasks that arrive unpredictably, ensuring smooth system operation.
- Load Leveling: Useful for absorbing bursts of requests by a service or application, preventing system overload during peak times.
- Asynchronous Processing: Enables background processing of tasks by queuing them up for later execution, optimizing resource usage and performance.

## AWS SNS and SQS

- **Describe how to use SQS and SNS in a “fanout” pattern.**

  The "fanout" pattern in AWS involves using SNS (Simple Notification Service) in conjunction with multiple SQS (Simple Queue Service) queues to distribute a message to various recipients simultaneously. Here's how it works:

  - **Create an SNS Topic:** First, you set up an SNS topic. This topic acts as a central point for publishing messages.
  
  - **Set Up SQS Queues:** Next, you create multiple SQS queues, each intended for different recipients or services that need to process the message.
  
  - **Subscribe Queues to the SNS Topic:** Each SQS queue is then subscribed to the SNS topic. This means that when a message is published to the SNS topic, it is automatically sent to all subscribed SQS queues.
  
  - **Publish Messages to SNS Topic:** When an event occurs that needs to be processed by multiple services, a message is published to the SNS topic.
  
  - **Message Distribution:** The SNS service then "fans out" the message to all the subscribed SQS queues simultaneously.
  
  - **Independent Processing:** Each SQS queue receives the message independently. The services or applications polling these queues can then process the messages at their own pace without affecting each other.

- **Explain how “push notifications” work, using SNS.**

  Push notifications using Amazon SNS (Simple Notification Service) work by sending a direct message to users' devices or to other services. Here's the process:

  - **Set Up SNS Topic:** You start by creating an SNS topic, which is a channel for sending messages.
  
  - **Register Subscribers:** Subscribers, which can be mobile devices, email addresses, or other services, are registered to the SNS topic. In the case of mobile devices, they need to be registered with a device token or identifier.
  
  - **Publish Messages:** When you want to send a notification, you publish a message to the SNS topic. This message contains the content of the notification.
  
  - **Message Delivery:** SNS then pushes this message to all registered subscribers. For mobile devices, SNS communicates with Apple APNS (Apple Push Notification Service), Google FCM (Firebase Cloud Messaging), or other similar services to deliver the message.
  
  - **Notification Receipt:** The end devices (like smartphones) receive the notification as a push alert, while other services like email endpoints receive it as an email message.

  This mechanism allows for real-time, scalable distribution of notifications to a large number of recipients, making it ideal for alerts, reminders, or any communication that requires immediate attention.


## SQS and SNS Basics

- **How might a large scale, distributed application make use of a Queue system like SQS?**

A large-scale, distributed application can leverage Amazon SQS in several ways to enhance scalability, reliability, and efficiency. Here are some key use cases:

- **Decoupling System Components:** SQS can be used to decouple various components of an application. By using queues, components can operate independently, without being directly connected. This means that if one component fails or is slow, it doesn't directly impact other components.

- **Load Balancing:** SQS can distribute tasks evenly across multiple nodes. When a component of the application generates a task, it sends a message to an SQS queue. Other components then pull tasks from the queue at their own pace, which helps in balancing the load and managing traffic spikes.

- **Asynchronous Processing:** SQS enables asynchronous processing by allowing tasks to be queued and processed later. This is particularly useful for tasks that are not time-sensitive or for operations that can be delayed, improving the application's overall responsiveness and efficiency.

- **Integrating with Other AWS Services:** SQS can be integrated with other AWS services like AWS Lambda, Amazon S3, and Amazon DynamoDB for various workflows, such as triggering a Lambda function to process data when a new message is added to the queue.


## Reflection

My goal is to gain a basic understanding of AWS's inter-app messaging services, SNS and SQS. I aim to comprehend the unique use cases for each service, with a particular focus on the concept of FIFO (First-In-First-Out) queues. Additionally, I am keen on developing the skills necessary to proficiently publish messages using SNS and to effectively manage SQS queues within a Node.js environment. This knowledge will not only enhance my technical expertise but also enable me to design and implement more efficient, scalable messaging solutions in cloud-based applications. 

#### Citations

*AWS - Difference between SQS and SNS*. Medium. Retrieved from [https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)

*SNS vs SQS Comparison? Whats the difference? | Learn with a practical example*. YouTube. Retrieved from [https://www.youtube.com/watch?v=mXk0MNjlO7A](https://www.youtube.com/watch?v=mXk0MNjlO7A)

*Decouple and Scale Applications Using Amazon SQS and Amazon SNS - 2017 AWS Online Tech Talks*. YouTube. Retrieved from [https://www.youtube.com/watch?v=UesxWuZMZqI](https://www.youtube.com/watch?v=UesxWuZMZqI)
