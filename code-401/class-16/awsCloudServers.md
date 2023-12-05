# AWS: Cloud Servers

## AWS EC2

### What is an EC2 Instance?

An EC2 Instance is a virtual server in Amazon's Elastic Compute Cloud (EC2) for running applications on the Amazon Web Services (AWS) infrastructure. It provides scalable computing capacity in the AWS cloud, allowing users to use virtual machines of varied configurations, manage storage, and scale computing resources as needed.

### 2 Use Cases for EC2

1. **Web Hosting**: EC2 instances can be used for hosting websites, ranging from simple static web pages to complex dynamic web applications. They offer the flexibility to choose the required computing resources and scale up or down based on traffic demands.

2. **High-Performance Computing (HPC)**: EC2 provides the necessary computational power for high-performance computing tasks. This includes scientific simulations, financial modeling, and data analysis that require processing large volumes of data quickly.

### 1 Reason to Use ECS Instead of Services like Heroku, Digital Ocean, or Render.com

- **Control and Customization**: Amazon ECS (Elastic Container Service) offers greater control over the underlying infrastructure compared to platform-as-a-service (PaaS) providers like Heroku, Digital Ocean, or Render.com. This includes detailed configuration options for networking, security, and instance types, which is crucial for applications with specific compliance, performance, or security requirements.

## EC2 For Humans

### Where Can We Find EC2 on the AWS Console?

EC2 can be found in the AWS Console under the "Compute" section. To access it, you would typically log in to your AWS Console, navigate to the "Services" menu at the top of the page, and then select "EC2" from the list of services under the "Compute" category. This will take you to the EC2 dashboard where you can manage your EC2 instances, storage, security groups, and other related settings.

### General Difference Between T2 Micro and XL

The T2 Micro and XL instances in AWS EC2 are different types of virtual servers that cater to varying computing needs. Here's a general comparison:

- **T2 Micro**:
  - **Purpose**: Designed for small-scale, low-traffic applications or development environments.
  - **Resources**: Offers limited CPU and memory resources, suitable for handling low to moderate workloads.
  - **Cost**: Generally more cost-effective, making it a popular choice for small applications or for users in the AWS Free Tier.

- **XL (e.g., m5.xlarge)**:
  - **Purpose**: Intended for larger-scale, high-performance applications that require more robust computing resources.
  - **Resources**: Provides significantly more CPU and memory compared to T2 Micro, enabling it to handle high workloads and more demanding applications.
  - **Cost**: More expensive due to its enhanced capabilities, suitable for businesses or applications with higher resource requirements.

### Explaining a "Compute Cycle" to a Non-Technical Friend

Imagine you're at a coffee shop. Each time you order a coffee, the barista performs a series of steps: taking your order, making the coffee, and serving it to you. This whole process can be thought of as a "coffee-making cycle."

Similarly, in the world of computers, a "compute cycle" is like the process of making coffee. It's a series of steps that a computer takes to receive an instruction, process it (like making the coffee), and then produce a result (serving the coffee). Just as different coffee orders (like an espresso vs. a latte) require different amounts of effort and time from the barista, different tasks require varying amounts of compute cycles from a computer, depending on their complexity.

## Elastic Beanstalk

### What is Elastic Beanstalk?

AWS Elastic Beanstalk is a service provided by Amazon Web Services (AWS) that simplifies the process of deploying and scaling web applications and services. It automates the deployment process, from capacity provisioning and load balancing to auto-scaling and application health monitoring. Elastic Beanstalk supports various programming platforms such as Java, .NET, PHP, Node.js, Python, Ruby, and Docker.

### Relationship Between EC2 and Elastic Beanstalk

- **EC2 as the Foundation**: Elastic Beanstalk uses Amazon EC2 (Elastic Compute Cloud) instances to run the applications it deploys. EC2 provides the scalable computing capacity which forms the backbone of Elastic Beanstalk's infrastructure.
- **Managed EC2 Instances**: While EC2 offers flexibility and control over individual server instances, Elastic Beanstalk abstracts and manages these EC2 instances for the user. It automatically handles the deployment of applications to EC2 instances, including configuration, scaling, and health monitoring.
- **Complementary Services**: Elastic Beanstalk integrates with other AWS services like Amazon S3, Elastic Load Balancing, and Auto Scaling, which are often used in conjunction with EC2. This integration provides a more comprehensive and managed cloud service experience.

### Benefits of Using Elastic Beanstalk

1. **Simplified Deployment**: Elastic Beanstalk automates the process of deploying applications to the cloud, making it easier for developers to deploy and manage their applications without worrying about the underlying infrastructure.
2. **Automatic Scaling**: It automatically scales the application up or down based on the demand, ensuring optimal resource utilization and performance.
3. **Health Monitoring and Management**: Elastic Beanstalk continuously monitors the health of applications, providing alerts and detailed reports on application performance.
4. **Developer Focus**: By managing the infrastructure, Elastic Beanstalk allows developers to focus on writing code and developing their applications, rather than spending time on system administration.
5. **Customization and Control**: While it provides a managed environment, Elastic Beanstalk also offers customization options for developers who need more control over their application's environment.
6. **Cost-Effective**: There is no extra charge for Elastic Beanstalk; users only pay for the AWS resources (like EC2 instances) used to store and run their applications.

## Things I want to know more about
I'm excited to learn about AWS Cloud Servers and understanding how "The Cloud" powers so many aspects of modern internet apps. My primary learning goal is understanding cloud concepts like containers, and virtual service instances. I especially look forward to deploying a Node.js server using Elastic Beanstalk on an EC2 instance, which seems like a crucial skill going forward as a developer. 

#### Citations
Cloud Compute Capacity - Amazon EC2. https://aws.amazon.com/ec2/
Amazon Web Services BASICS. YouTube. https://www.youtube.com/watch?v=lZMkgOMYYIg
AmIntroduction to AWS Elastic Beanstalk. YouTube. https://www.youtube.com/watch?v=SrwxAScdyT0
