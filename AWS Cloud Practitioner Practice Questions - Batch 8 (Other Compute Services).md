# AWS Cloud Practitioner Practice Questions - Batch 8 (Other Compute Services)

176. Which AWS compute service allows you to run code without provisioning or managing servers (serverless compute)?
    - A. Amazon EC2
    - B. AWS Lambda
    - C. Amazon Lightsail
    - D. AWS Elastic Beanstalk

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Lambda is a serverless compute service that lets you run code in response to events without needing to provision or manage servers. You pay only for the compute time consumed.
    </details>

177. Which AWS service provides an easy way to deploy and manage applications in the AWS Cloud without worrying about the underlying infrastructure (servers, load balancers, scaling)?
    - A. AWS Lambda
    - B. Amazon EC2
    - C. AWS Elastic Beanstalk
    - D. Amazon S3

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Elastic Beanstalk is a PaaS (Platform as a Service) offering that handles the deployment details of capacity provisioning, load balancing, auto-scaling, and application health monitoring for web applications and services.
    </details>

178. Which AWS service is designed to be the easiest way to launch and manage a virtual private server (VPS) with a simple management interface, bundling compute, storage, and networking into a low, predictable monthly price?
    - A. Amazon EC2
    - B. AWS Elastic Beanstalk
    - C. AWS Lambda
    - D. Amazon Lightsail

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Amazon Lightsail provides easy-to-use virtual private server (VPS) instances, containers, storage, databases, and more at a cost-effective monthly price. It simplifies getting started on AWS.
    </details>

179. What are the typical triggers for an AWS Lambda function? (Choose TWO)
    - A. Changes in an S3 bucket (e.g., object creation).
    - B. Scheduled events (e.g., run every hour via CloudWatch Events/EventBridge).
    - C. Manually starting an EC2 instance.
    - D. Attaching an EBS volume.
    - E. Creating a new VPC.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A, B
      Explanation: Lambda functions can be triggered by various AWS service events (like S3 object uploads, DynamoDB table updates, API Gateway requests), scheduled events, or direct invocations via the SDK/CLI.
    </details>

180. What is the pricing model for AWS Lambda?
    - A. Per hour of server uptime.
    - B. Based on the number of EC2 instances managed.
    - C. Based on the number of requests served and the duration (compute time) your code runs.
    - D. Fixed monthly fee per function.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Lambda pricing is based on the number of requests for your functions and the duration (measured in milliseconds) it takes for your code to execute. There is a generous free tier.
    </details>

181. Which programming languages are supported by AWS Lambda?
    - A. Only Python and Node.js
    - B. Only Java and C#
    - C. A wide variety of languages including Node.js, Python, Java, Ruby, C#, Go, PowerShell, and custom runtimes.
    - D. Only low-level assembly languages.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Lambda supports numerous popular programming languages through managed runtimes and also allows bringing custom runtimes for other languages.
    </details>

182. What does Elastic Beanstalk manage on your behalf? (Choose THREE)
    - A. Application code deployment.
    - B. Infrastructure provisioning (EC2 instances, Load Balancers).
    - C. Auto Scaling configuration.
    - D. Database schema design.
    - E. Writing application code.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A, B, C
      Explanation: Elastic Beanstalk automates the setup and management of the environment for your application, including deploying your code, provisioning EC2 instances, setting up load balancing and auto scaling, and monitoring application health.
    </details>

183. Which service is generally more suitable if you need full control over the underlying EC2 instances, operating system, and software stack for your web application?
    - A. AWS Lambda
    - B. AWS Elastic Beanstalk (using default configurations)
    - C. Amazon EC2
    - D. Amazon Lightsail

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon EC2 (IaaS) provides the highest level of control over the compute environment, including OS choice, patching, software installation, and instance configuration. Elastic Beanstalk abstracts much of this, while Lambda abstracts it completely.
    </details>

184. Amazon Lightsail bundles resources like a VPS, SSD-based storage, data transfer, DNS management, and a static IP. What is the primary advantage of this approach?
    - A. Maximum flexibility and customization.
    - B. Suitability for complex, large-scale enterprise applications.
    - C. Simplicity and predictable low monthly pricing for getting started quickly.
    - D. Integration with advanced AWS networking features like Transit Gateway.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Lightsail is designed for simplicity, offering pre-configured bundles with predictable pricing, making it easy for developers, small businesses, or students to launch simple web applications or websites without deep AWS expertise.
    </details>

185. Can you run containerized applications using AWS compute services other than EC2?
    - A. No, containers can only run on EC2 instances.
    - B. Yes, services like AWS Fargate, Amazon ECS, Amazon EKS, AWS Lambda (container images), and Elastic Beanstalk (Docker platform) support containers.
    - C. Yes, but only using Amazon Lightsail containers.
    - D. No, containers are not supported on AWS.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS offers multiple ways to run containers, including serverless options (Fargate, Lambda), orchestration services (ECS, EKS), and platform services (Elastic Beanstalk), in addition to running them directly on EC2.
    </details>

186. What is AWS Fargate?
    - A. A physical server dedicated to a single customer.
    - B. A serverless compute engine for containers that works with both Amazon ECS and EKS.
    - C. A service for managing relational databases.
    - D. A tool for building machine learning models.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Fargate allows you to run containers without managing the underlying EC2 instances (serverless). You define your application containers, and Fargate launches and scales the compute required.
    </details>

187. Which AWS service would be most appropriate for running a batch processing job that needs to execute periodically based on a schedule?
    - A. AWS Elastic Beanstalk
    - B. AWS Lambda triggered by CloudWatch Events/EventBridge
    - C. Amazon EC2 instances running continuously
    - D. Amazon Lightsail

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Lambda is well-suited for event-driven or scheduled tasks. Using CloudWatch Events (or EventBridge) to trigger a Lambda function on a schedule is a cost-effective and serverless way to run periodic batch jobs.
    </details>

188. If you deploy an application using Elastic Beanstalk, do you still have access to the underlying EC2 instances?
    - A. No, Elastic Beanstalk completely hides the underlying infrastructure.
    - B. Yes, you retain full control and can SSH into the EC2 instances managed by Elastic Beanstalk.
    - C. Only if you use the Docker platform.
    - D. Only read-only access is provided.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: While Elastic Beanstalk automates management, it runs on standard AWS resources like EC2 instances. You still have the option to access these underlying resources (e.g., via SSH) if needed, although direct modifications can interfere with Beanstalk management.
    </details>

189. What is the maximum execution duration for a single AWS Lambda function invocation?
    - A. 60 seconds
    - B. 5 minutes
    - C. 15 minutes
    - D. 1 hour

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The maximum timeout value for an AWS Lambda function is 900 seconds (15 minutes).
    </details>

190. Which service provides a simpler alternative to EC2 for users who just need a basic virtual server, perhaps for hosting a WordPress site or a simple web application?
    - A. AWS Lambda
    - B. Amazon EKS
    - C. Amazon Lightsail
    - D. AWS Batch

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Lightsail offers pre-configured blueprints (including WordPress) and bundles compute, storage, and networking into easy-to-understand plans, making it ideal for simpler use cases compared to the flexibility (and complexity) of EC2.
    </details>

191. You have developed a web application packaged as a Docker container. Which AWS service provides a simple way to deploy and scale this containerized application without managing servers?
    - A. Amazon EC2 with Docker installed manually.
    - B. AWS Fargate with Amazon ECS or EKS.
    - C. AWS Lambda (using function code directly).
    - D. Amazon S3 static website hosting.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Fargate is the serverless compute engine for containers. Used with an orchestrator like ECS (Elastic Container Service) or EKS (Elastic Kubernetes Service), it allows you to run Docker containers without managing the underlying EC2 instances.
    </details>

192. Which AWS compute service bills based on provisioned resources (like instance hours) rather than actual execution time?
    - A. AWS Lambda
    - B. AWS Fargate
    - C. Amazon EC2
    - D. Both A and B

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon EC2 instances are typically billed based on the time they are running (per second or per hour, depending on OS), regardless of whether the CPU is idle or busy. Lambda and Fargate bill based on resource consumption during execution.
    </details>

193. What is AWS Batch?
    - A. A serverless compute service for event-driven code.
    - B. A service that enables developers and scientists to easily and efficiently run batch computing jobs on AWS.
    - C. A platform for deploying web applications.
    - D. A virtual private server service.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Batch dynamically provisions the optimal quantity and type of compute resources (e.g., CPU or memory-optimized instances) based on the volume and specific resource requirements of the batch jobs submitted.
    </details>

194. If cost is a primary concern and you need a simple VPS for a low-traffic website, which service often provides the most predictable and lowest monthly cost?
    - A. A large EC2 instance
    - B. AWS Lambda
    - C. AWS Elastic Beanstalk
    - D. Amazon Lightsail

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Lightsail offers bundled plans with fixed monthly pricing, making costs highly predictable and often lower for simple, low-resource use cases compared to the pay-as-you-go flexibility of EC2 or Lambda.
    </details>

195. Which service automatically handles capacity provisioning, load balancing, scaling, and application health monitoring for your deployed code?
    - A. Amazon EC2
    - B. AWS Lambda
    - C. AWS Elastic Beanstalk
    - D. AWS Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Elastic Beanstalk is designed as a PaaS to abstract away the operational burden of managing infrastructure, automatically handling these common deployment and management tasks.
    </details>

196. Can AWS Lambda functions access resources within a VPC?
    - A. No, Lambda functions run outside of VPCs.
    - B. Yes, Lambda functions can be configured to access resources within a specified VPC.
    - C. Only if the VPC is peered with the Lambda service VPC.
    - D. Only for functions written in Python.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: You can configure a Lambda function to connect to private subnets in a virtual private cloud (VPC) in your AWS account, allowing it to access private resources like databases or internal services.
    </details>

197. What is the concept of 
