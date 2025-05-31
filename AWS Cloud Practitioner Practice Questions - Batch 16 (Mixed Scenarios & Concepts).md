# AWS Cloud Practitioner Practice Questions - Batch 16 (Mixed Scenarios & Concepts)

776. A company is migrating its on-premises application to AWS. They want to ensure their architecture follows AWS best practices for security, reliability, and cost-effectiveness from the start. Which AWS resource provides guidance based on pillars like Operational Excellence, Security, Reliability, Performance Efficiency, and Cost Optimization?
    - A. AWS Trusted Advisor
    - B. AWS Well-Architected Framework
    - C. AWS Service Catalog
    - D. AWS Personal Health Dashboard

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: The AWS Well-Architected Framework provides architectural best practices across its pillars to help customers build secure, high-performing, resilient, and efficient infrastructure for their applications.
    </details>

777. Which AWS service allows you to provision a logically isolated section of the AWS Cloud where you can launch AWS resources in a virtual network that you define?
    - A. Amazon Route 53
    - B. Amazon EC2
    - C. Amazon S3
    - D. Amazon Virtual Private Cloud (VPC)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Amazon VPC lets you define your own virtual network, including selecting your IP address range, creating subnets, and configuring route tables and network gateways.
    </details>

778. A user needs to launch a new EC2 instance. What information is required at a minimum to launch the instance?
    - A. Instance Type and Security Group
    - B. Amazon Machine Image (AMI) and Instance Type
    - C. Key Pair and Subnet ID
    - D. AMI and VPC ID

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: An AMI provides the operating system and initial software configuration, while the Instance Type defines the hardware resources (CPU, memory, storage, networking) for the instance. These are the fundamental choices for launching an EC2 instance.
    </details>

779. Which component of AWS global infrastructure consists of one or more discrete data centers, each with redundant power, networking, and connectivity, housed in separate facilities?
    - A. AWS Region
    - B. Availability Zone (AZ)
    - C. Edge Location
    - D. Local Zone

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Availability Zones are the distinct physical locations within an AWS Region designed for fault isolation.
    </details>

780. What is the primary benefit of deploying an application across multiple Availability Zones?
    - A. Reduced network latency for global users.
    - B. Increased fault tolerance and high availability.
    - C. Lower data transfer costs.
    - D. Access to a wider range of EC2 instance types.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: If one AZ fails, the application can continue running from the other AZs, enhancing reliability and availability.
    </details>

781. Which AWS service is used to distribute incoming application traffic across multiple targets, such as EC2 instances, containers, and IP addresses?
    - A. Amazon Route 53
    - B. Elastic Load Balancing (ELB)
    - C. Amazon CloudFront
    - D. AWS Auto Scaling

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: ELB automatically distributes traffic to improve application availability and fault tolerance.
    </details>

782. A company wants to ensure their application can automatically adjust compute capacity to maintain steady, predictable performance at the lowest possible cost. Which AWS service helps achieve this?
    - A. Elastic Load Balancing
    - B. AWS Auto Scaling
    - C. Amazon CloudWatch
    - D. AWS Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Auto Scaling monitors applications and automatically adjusts capacity (e.g., adding or removing EC2 instances) based on defined policies to meet demand.
    </details>

783. Which AWS service provides object storage suitable for storing backups, archives, and static website assets?
    - A. Amazon EBS
    - B. Amazon EFS
    - C. Amazon S3
    - D. Amazon RDS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon S3 is designed for durable, scalable, and secure object storage for a wide variety of use cases.
    </details>

784. Which AWS service provides persistent block storage volumes for use with Amazon EC2 instances?
    - A. Amazon S3
    - B. Amazon EFS
    - C. Amazon EBS
    - D. Amazon Glacier

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EBS volumes function like virtual hard drives attached to EC2 instances, suitable for boot volumes and application data requiring block storage.
    </details>

785. Which AWS service provides a scalable file storage system accessible via the NFS protocol, primarily for Linux-based workloads?
    - A. Amazon S3
    - B. Amazon EBS
    - C. Amazon EFS
    - D. Amazon FSx for Windows File Server

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EFS offers shared, elastic file storage that can be mounted by multiple Linux instances concurrently.
    </details>

786. A company needs to run a Microsoft SQL Server database on AWS with high availability. Which AWS service is most suitable for this?
    - A. Amazon DynamoDB
    - B. Amazon Redshift
    - C. Amazon RDS for SQL Server (using Multi-AZ deployment)
    - D. Running SQL Server on EC2 instances without RDS.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon RDS provides managed relational database services, including SQL Server. Enabling the Multi-AZ option provides high availability by maintaining a synchronous standby replica in a different AZ.
    </details>

787. Which AWS service allows you to manage users, groups, and permissions centrally for accessing AWS resources?
    - A. Amazon Cognito
    - B. AWS Directory Service
    - C. AWS IAM (Identity and Access Management)
    - D. AWS Organizations

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: IAM is the core service for managing access control to AWS services and resources.
    </details>

788. What is the most secure way to manage AWS access keys for an IAM user?
    - A. Embed the keys directly in application code.
    - B. Store the keys in a public S3 bucket.
    - C. Rotate the access keys regularly and avoid sharing them.
    - D. Use the root account access keys instead.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Regular rotation minimizes the window of opportunity if keys are compromised. Keys should never be shared or embedded in code. Using the root keys for regular tasks is strongly discouraged.
    </details>

789. Which AWS service provides a managed firewall at the EC2 instance level?
    - A. Network Access Control List (NACL)
    - B. AWS WAF
    - C. Security Group
    - D. AWS Shield

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Security Groups act as stateful firewalls associated with instance network interfaces.
    </details>

790. Which AWS service provides a firewall at the subnet level?
    - A. Security Group
    - B. AWS WAF
    - C. Network Access Control List (NACL)
    - D. AWS Firewall Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: NACLs are associated with subnets and control traffic entering or leaving the subnet.
    </details>

791. A company wants to ensure that certain sensitive API actions are never allowed in specific AWS accounts within their Organization, regardless of IAM permissions. Which AWS feature should they use?
    - A. IAM Permission Boundaries
    - B. AWS Config Rules
    - C. Service Control Policies (SCPs)
    - D. AWS CloudTrail

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SCPs, applied via AWS Organizations, act as guardrails that restrict the maximum permissions available within member accounts.
    </details>

792. Which AWS service helps protect web applications from common exploits like SQL injection and cross-site scripting?
    - A. AWS Shield
    - B. AWS WAF
    - C. Amazon GuardDuty
    - D. Security Groups

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS WAF inspects web traffic at the application layer to block malicious requests.
    </details>

793. Which AWS service provides managed protection against Distributed Denial of Service (DDoS) attacks?
    - A. AWS WAF
    - B. AWS Shield
    - C. Amazon Inspector
    - D. AWS Firewall Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Shield (Standard and Advanced) is specifically designed for DDoS mitigation.
    </details>

794. Which AWS service provides continuous threat detection by analyzing logs like CloudTrail, VPC Flow Logs, and DNS logs?
    - A. Amazon Inspector
    - B. Amazon Macie
    - C. Amazon GuardDuty
    - D. AWS Security Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: GuardDuty uses intelligent threat detection to identify potential security issues.
    </details>

795. Which AWS service helps assess EC2 instances for vulnerabilities and deviations from security best practices?
    - A. Amazon GuardDuty
    - B. Amazon Inspector
    - C. AWS Config
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Inspector performs automated security assessments against known vulnerabilities and network configuration issues.
    </details>

796. Which AWS service helps discover, classify, and protect sensitive data stored in Amazon S3?
    - A. Amazon GuardDuty
    - B. Amazon Inspector
    - C. Amazon Macie
    - D. AWS KMS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Macie focuses on data security and privacy within S3.
    </details>

797. Which AWS service provides a unified view of security alerts and compliance status across your AWS environment?
    - A. Amazon CloudWatch
    - B. AWS Security Hub
    - C. AWS Trusted Advisor
    - D. AWS Control Tower

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Security Hub aggregates findings from various AWS security services and partner tools.
    </details>

798. Which AWS service is used to create and manage encryption keys for protecting data?
    - A. AWS Secrets Manager
    - B. AWS Certificate Manager
    - C. AWS Key Management Service (KMS)
    - D. AWS CloudHSM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: KMS provides managed key generation, storage, usage, and auditing capabilities.
    </details>

799. Which AWS service is used to securely store and manage secrets like database passwords and API keys, including automated rotation?
    - A. AWS KMS
    - B. AWS Systems Manager Parameter Store
    - C. AWS Secrets Manager
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Secrets Manager is specifically designed for managing the lifecycle of secrets.
    </details>

800. Which AWS service provides access to AWS compliance reports like SOC 2 and PCI DSS?
    - A. AWS Config
    - B. AWS Trusted Advisor
    - C. AWS Artifact
    - D. AWS Security Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Artifact is the central repository for AWS compliance documentation.
    </details>

801. What is the AWS Shared Responsibility Model?
    - A. AWS manages all security aspects.
    - B. The customer manages all security aspects.
    - C. AWS manages security OF the cloud; the customer manages security IN the cloud.
    - D. Security is outsourced to a third party.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: This model defines the distinct security responsibilities of AWS (infrastructure) and the customer (data, applications, configuration).
    </details>

802. Under the Shared Responsibility Model, who is responsible for patching the operating system on an Amazon RDS instance?
    - A. The Customer
    - B. AWS
    - C. Both AWS and the Customer
    - D. The database vendor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: For managed services like RDS, AWS handles the underlying OS and database engine patching as part of the service.
    </details>

803. Which AWS service provides recommendations based on best practices for cost optimization, performance, security, fault tolerance, and service limits?
    - A. AWS Config
    - B. AWS Well-Architected Tool
    - C. AWS Trusted Advisor
    - D. Amazon CloudWatch

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Trusted Advisor automatically scans your environment and provides actionable recommendations.
    </details>

804. Which AWS tool helps you review your architecture against the principles of the Well-Architected Framework?
    - A. AWS Trusted Advisor
    - B. AWS Cost Explorer
    - C. AWS Well-Architected Tool
    - D. AWS CloudFormation

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Well-Architected Tool provides a structured way to assess workloads against best practices.
    </details>

805. Which pillar of the Well-Architected Framework focuses on the ability to run workloads effectively, gain insights into their operations, and continuously improve supporting processes?
    - A. Security
    - B. Reliability
    - C. Performance Efficiency
    - D. Operational Excellence

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Operational Excellence covers automation, monitoring, and refining procedures.
    </details>

806. Which pillar of the Well-Architected Framework focuses on ensuring a workload performs its intended function correctly and consistently when expected?
    - A. Operational Excellence
    - B. Security
    - C. Reliability
    - D. Cost Optimization

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Reliability involves designing for failure and ensuring systems recover automatically.
    </details>

807. Which AWS service helps you visualize and analyze your AWS costs and usage?
    - A. AWS Budgets
    - B. AWS Cost Explorer
    - C. AWS Cost and Usage Report
    - D. AWS Pricing Calculator

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Cost Explorer provides graphical tools for cost analysis and forecasting.
    </details>

808. Which AWS service allows you to set custom cost thresholds and receive alerts?
    - A. AWS Cost Explorer
    - B. AWS Budgets
    - C. AWS Trusted Advisor
    - D. Amazon CloudWatch

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Budgets is the primary tool for cost alerting and monitoring against limits.
    </details>

809. What is the main benefit of using Cost Allocation Tags?
    - A. To improve application performance.
    - B. To enforce security policies.
    - C. To categorize and track AWS costs by project, department, or other criteria.
    - D. To automate resource deployment.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Tags enable granular cost tracking when activated for cost allocation.
    </details>

810. Which AWS service allows you to manage multiple AWS accounts centrally?
    - A. AWS IAM
    - B. AWS Control Tower
    - C. AWS Organizations
    - D. AWS Service Catalog

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Organizations provides the framework for multi-account management, consolidated billing, and policy application.
    </details>

811. What is Consolidated Billing in AWS Organizations?
    - A. A way to apply security policies.
    - B. A single bill for all accounts in the organization, often allowing for aggregated volume discounts.
    - C. A tool for estimating costs.
    - D. A method for managing IAM users.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: It simplifies billing and can lead to cost savings through combined usage tiers.
    </details>

812. Which AWS Support plan offers the fastest response times (typically < 15 minutes) for business-critical system down issues and includes a designated Technical Account Manager (TAM)?
    - A. Basic
    - B. Developer
    - C. Business
    - D. Enterprise

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: The Enterprise plan provides the highest level of support, including the fastest SLAs and a dedicated TAM.
    </details>

813. Which AWS tool helps estimate the cost of running a specific workload on AWS before deployment?
    - A. AWS Cost Explorer
    - B. AWS TCO Calculator
    - C. AWS Pricing Calculator
    - D. AWS Budgets

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Pricing Calculator is used for estimating costs of planned architectures.
    </details>

814. Which AWS tool helps compare the costs of running infrastructure on-premises versus on AWS?
    - A. AWS Pricing Calculator
    - B. AWS Cost Explorer
    - C. AWS TCO Calculator
    - D. AWS Well-Architected Tool

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The TCO Calculator focuses on the comparison between on-premises and AWS costs.
    </details>

815. What is a primary benefit of cloud computing related to expenditure?
    - A. Increased capital expenditure (CapEx).
    - B. Trading capital expenditure (CapEx) for variable operational expenditure (OpEx).
    - C. Fixed monthly costs regardless of usage.
    - D. Elimination of all operational expenditure (OpEx).

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Instead of investing heavily in data centers and servers upfront (CapEx), cloud computing allows you to pay for resources as you consume them (OpEx).
    </details>

816. Which benefit of cloud computing refers to the ability to acquire resources as needed and release them when no longer required?
    - A. Fault Tolerance
    - B. Elasticity
    - C. High Availability
    - D. Global Reach

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Elasticity allows systems to scale compute capacity up or down easily based on demand.
    </details>

817. Which cloud computing deployment model involves running infrastructure exclusively on AWS?
    - A. Hybrid Cloud
    - B. Private Cloud
    - C. Public Cloud (All-in Cloud)
    - D. On-Premises

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Running entirely within a public cloud provider like AWS is the public cloud model.
    </details>

818. Which cloud computing deployment model connects on-premises infrastructure with cloud resources?
    - A. Public Cloud
    - B. Private Cloud
    - C. Hybrid Cloud
    - D. Multi-Cloud

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Hybrid cloud integrates on-premises infrastructure with public cloud services.
    </details>

819. Which AWS service provides Infrastructure as Code capabilities?
    - A. AWS Elastic Beanstalk
    - B. AWS CloudFormation
    - C. AWS CodeDeploy
    - D. AWS Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: CloudFormation allows you to define and provision infrastructure using code templates.
    </details>

820. Which AWS service provides a Platform as a Service (PaaS) environment for deploying web applications?
    - A. Amazon EC2
    - B. AWS Lambda
    - C. AWS Elastic Beanstalk
    - D. AWS Fargate

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Elastic Beanstalk abstracts the underlying infrastructure, allowing developers to focus on deploying code.
    </details>

821. Which AWS service provides Function as a Service (FaaS) or serverless compute?
    - A. Amazon EC2
    - B. AWS Elastic Beanstalk
    - C. AWS Lambda
    - D. Amazon ECS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Lambda allows you to run code without managing servers, triggered by events.
    </details>

822. A company needs to store frequently accessed data with low latency requirements. Which S3 storage class is most appropriate?
    - A. S3 Glacier Deep Archive
    - B. S3 Standard-IA
    - C. S3 Standard
    - D. S3 One Zone-IA

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Standard is designed for frequently accessed data requiring low latency and high throughput.
    </details>

823. A company needs to archive data for 10 years at the lowest possible cost. Data retrieval time is flexible (within 12-48 hours). Which S3 storage class should they use?
    - A. S3 Standard-IA
    - B. S3 Glacier Flexible Retrieval
    - C. S3 Glacier Deep Archive
    - D. S3 Intelligent-Tiering Archive Access

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Glacier Deep Archive offers the lowest storage cost for long-term archival where infrequent, slow retrieval is acceptable.
    </details>

824. Which EBS volume type is best suited for I/O-intensive database workloads requiring high, consistent IOPS?
    - A. General Purpose SSD (gp3)
    - B. Provisioned IOPS SSD (io1/io2)
    - C. Throughput Optimized HDD (st1)
    - D. Cold HDD (sc1)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Provisioned IOPS SSD volumes are designed for workloads needing guaranteed high IOPS performance.
    </details>

825. Which EBS volume type is recommended as a cost-effective boot volume for general-purpose EC2 instances?
    - A. Provisioned IOPS SSD (io1/io2)
    - B. General Purpose SSD (gp3/gp2)
    - C. Throughput Optimized HDD (st1)
    - D. Cold HDD (sc1)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: General Purpose SSDs provide a good balance of price and performance for boot volumes and common workloads.
    </details>

826. What is the purpose of an EC2 Auto Scaling group?
    - A. To manually launch EC2 instances.
    - B. To automatically adjust the number of EC2 instances based on demand or schedule.
    - C. To distribute traffic across EC2 instances.
    - D. To provide static IP addresses for EC2 instances.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Auto Scaling groups maintain application availability by scaling the number of instances up or down automatically.
    </details>

827. Which type of Elastic Load Balancer operates at Layer 7 (Application Layer) and supports path-based routing?
    - A. Classic Load Balancer (CLB)
    - B. Network Load Balancer (NLB)
    - C. Application Load Balancer (ALB)
    - D. Gateway Load Balancer (GWLB)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: ALBs provide advanced request routing features based on HTTP/S information, including paths and hostnames.
    </details>

828. Which type of Elastic Load Balancer operates at Layer 4 (Transport Layer) and offers ultra-low latency?
    - A. Classic Load Balancer (CLB)
    - B. Network Load Balancer (NLB)
    - C. Application Load Balancer (ALB)
    - D. Gateway Load Balancer (GWLB)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: NLBs are optimized for high-performance TCP/UDP traffic handling.
    </details>

829. Which AWS networking service allows you to create a logically isolated virtual network?
    - A. Amazon Route 53
    - B. AWS Direct Connect
    - C. Amazon VPC
    - D. Elastic Load Balancing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: VPC provides the foundation for networking within AWS.
    </details>

830. Which VPC component controls inbound and outbound traffic at the subnet level?
    - A. Security Group
    - B. Route Table
    - C. Network Access Control List (NACL)
    - D. Internet Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: NACLs act as stateless firewalls for subnets.
    </details>

831. Which VPC component controls inbound and outbound traffic at the instance level?
    - A. Security Group
    - B. Route Table
    - C. Network Access Control List (NACL)
    - D. NAT Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: Security Groups act as stateful firewalls for instances (ENIs).
    </details>

832. How can instances in a private subnet access the internet for software updates without being directly reachable from the internet?
    - A. By using an Internet Gateway directly.
    - B. By using a NAT Gateway or NAT Instance in a public subnet.
    - C. By using a VPC Endpoint for S3.
    - D. By using VPC Peering.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: A NAT device allows outbound internet connectivity while preventing inbound connections initiated from the internet.
    </details>

833. Which AWS service provides a managed DNS service?
    - A. Amazon VPC
    - B. Amazon CloudFront
    - C. Amazon Route 53
    - D. AWS Direct Connect

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Route 53 handles domain registration, DNS resolution, and health checks.
    </details>

834. Which Route 53 routing policy directs users to the endpoint with the lowest network latency?
    - A. Simple
    - B. Weighted
    - C. Latency
    - D. Geolocation

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Latency routing optimizes for the fastest response time based on network conditions.
    </details>

835. Which Route 53 routing policy distributes traffic based on the user\s geographic location?
    - A. Simple
    - B. Weighted
    - C. Latency
    - D. Geolocation

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Geolocation routing directs users based on their country, continent, or state.
    </details>

836. Which AWS service provides a dedicated private network connection from on-premises to AWS?
    - A. AWS VPN
    - B. AWS Direct Connect
    - C. VPC Peering
    - D. AWS Transit Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Direct Connect offers a dedicated physical link.
    </details>

837. Which AWS service acts as a central hub for connecting multiple VPCs and on-premises networks?
    - A. AWS VPN
    - B. AWS Direct Connect
    - C. VPC Peering
    - D. AWS Transit Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Transit Gateway simplifies network topology using a hub-and-spoke model.
    </details>

838. Which AWS service provides a global content delivery network (CDN)?
    - A. Amazon S3 Transfer Acceleration
    - B. AWS Global Accelerator
    - C. Amazon CloudFront
    - D. Elastic Load Balancing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudFront caches content at edge locations worldwide.
    </details>

839. Which AWS service improves the availability and performance of global applications using the AWS network backbone and static IP addresses?
    - A. Amazon CloudFront
    - B. AWS Global Accelerator
    - C. Amazon Route 53
    - D. Elastic Load Balancing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Global Accelerator optimizes the network path for application traffic.
    </details>

840. Which AWS service provides managed relational database instances?
    - A. DynamoDB
    - B. Redshift
    - C. RDS
    - D. ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: RDS manages popular relational database engines.
    </details>

841. Which AWS service provides a managed NoSQL key-value database?
    - A. RDS
    - B. Redshift
    - C. DynamoDB
    - D. Aurora

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: DynamoDB is AWS\s scalable NoSQL key-value and document database.
    </details>

842. Which AWS service provides a managed data warehouse?
    - A. RDS
    - B. DynamoDB
    - C. Redshift
    - D. EMR

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Redshift is optimized for large-scale analytics and data warehousing.
    </details>

843. Which AWS service provides managed in-memory caching?
    - A. RDS
    - B. DynamoDB
    - C. Redshift
    - D. ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: ElastiCache manages Redis or Memcached for caching.
    </details>

844. Which AWS service provides a MySQL and PostgreSQL-compatible database with enhanced performance?
    - A. RDS for MySQL/PostgreSQL
    - B. DynamoDB
    - C. Aurora
    - D. Redshift

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Aurora is AWS\s cloud-optimized relational database engine.
    </details>

845. Which AWS service allows you to manage users and permissions for accessing AWS resources?
    - A. Cognito
    - B. IAM
    - C. Directory Service
    - D. Organizations

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: IAM is the core service for AWS access management.
    </details>

846. What is the best practice for securing the AWS root account?
    - A. Share the root credentials with administrators.
    - B. Use the root account for daily administrative tasks.
    - C. Enable Multi-Factor Authentication (MFA) and use the root account only for tasks that require it.
    - D. Delete the root account after creating IAM users.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The root account has unrestricted access and should be secured with MFA and used sparingly.
    </details>

847. Which IAM entity allows you to group users and apply policies to the group?
    - A. IAM Role
    - B. IAM Policy
    - C. IAM Group
    - D. IAM User

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Groups simplify permission management for multiple users with similar access needs.
    </details>

848. Which IAM entity is used to grant temporary permissions, typically assumed by users or services?
    - A. IAM Role
    - B. IAM Policy
    - C. IAM Group
    - D. IAM User

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: Roles provide temporary credentials, which is more secure than using long-term user keys.
    </details>

849. What defines the permissions in AWS IAM?
    - A. IAM Role
    - B. IAM Policy
    - C. IAM Group
    - D. IAM User

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: IAM Policies are JSON documents that explicitly state permissions (allow or deny actions on resources).
    </details>

850. Which AWS service provides a managed container orchestration service?
    - A. ECR
    - B. ECS / EKS
    - C. Fargate
    - D. Lambda

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: ECS (AWS-native) and EKS (Kubernetes) are the primary container orchestration services.
    </details>

851. Which AWS service provides a serverless compute engine for containers?
    - A. ECR
    - B. ECS / EKS
    - C. Fargate
    - D. Lambda

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Fargate removes the need to manage underlying EC2 instances for containers.
    </details>

852. Which AWS service provides a managed container registry?
    - A. ECR
    - B. ECS / EKS
    - C. Fargate
    - D. Docker Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: ECR stores, manages, and deploys container images.
    </details>

853. Which AWS service provides serverless function execution?
    - A. EC2
    - B. Fargate
    - C. Lambda
    - D. ECS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Lambda runs code in response to events without server management.
    </details>

854. Which AWS service provides Infrastructure as Code using templates?
    - A. CodeDeploy
    - B. Elastic Beanstalk
    - C. CloudFormation
    - D. Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudFormation defines infrastructure in code.
    </details>

855. Which AWS service provides a PaaS environment for web applications?
    - A. CloudFormation
    - B. Elastic Beanstalk
    - C. Lambda
    - D. EC2

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Elastic Beanstalk simplifies deployment and management.
    </details>

856. Which AWS service provides managed message queues?
    - A. SNS
    - B. SQS
    - C. MQ
    - D. Kinesis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SQS is for decoupling applications using queues.
    </details>

857. Which AWS service provides managed publish/subscribe messaging?
    - A. SNS
    - B. SQS
    - C. MQ
    - D. Step Functions

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: SNS uses topics for pub/sub messaging.
    </details>

858. Which AWS service provides workflow orchestration for serverless applications?
    - A. SNS
    - B. SQS
    - C. Lambda
    - D. Step Functions

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Step Functions coordinates multiple services using state machines.
    </details>

859. Which AWS service provides monitoring via metrics, logs, and alarms?
    - A. CloudTrail
    - B. Config
    - C. CloudWatch
    - D. X-Ray

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudWatch is the central monitoring service.
    </details>

860. Which AWS service logs API activity in your account?
    - A. CloudWatch
    - B. Config
    - C. CloudTrail
    - D. GuardDuty

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudTrail records API calls for auditing.
    </details>

861. Which AWS service tracks resource configuration changes?
    - A. CloudWatch
    - B. Config
    - C. CloudTrail
    - D. Inspector

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Config records configuration history and evaluates compliance.
    </details>

862. Which AWS service provides a global CDN?
    - A. Route 53
    - B. Global Accelerator
    - C. CloudFront
    - D. ELB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudFront caches content globally.
    </details>

863. Which AWS service provides managed relational databases?
    - A. DynamoDB
    - B. RDS
    - C. Redshift
    - D. ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: RDS manages relational database engines.
    </details>

864. Which AWS service provides a managed NoSQL database?
    - A. RDS
    - B. DynamoDB
    - C. Redshift
    - D. Aurora

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: DynamoDB is the primary NoSQL service.
    </details>

865. Which AWS service provides a managed data warehouse?
    - A. RDS
    - B. DynamoDB
    - C. Redshift
    - D. ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Redshift is for analytics and data warehousing.
    </details>

866. Which AWS service provides managed in-memory caching?
    - A. RDS
    - B. DynamoDB
    - C. Redshift
    - D. ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: ElastiCache manages Redis/Memcached.
    </details>

867. Which AWS service provides a platform for the ML lifecycle?
    - A. Rekognition
    - B. SageMaker
    - C. Comprehend
    - D. Lex

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SageMaker covers building, training, and deploying ML models.
    </details>

868. Which AWS service provides pre-trained AI models via API?
    - A. SageMaker
    - B. AI Services (Rekognition, Polly, etc.)
    - C. EMR
    - D. Glue

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Services like Rekognition offer ready-to-use AI capabilities.
    </details>

869. Which AWS service manages multiple AWS accounts?
    - A. IAM
    - B. Organizations
    - C. Control Tower
    - D. Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Organizations provides the framework for multi-account management.
    </details>

870. Which AWS service provides best practice recommendations?
    - A. Config
    - B. CloudTrail
    - C. Trusted Advisor
    - D. Inspector

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Trusted Advisor scans for optimizations.
    </details>

871. Which AWS service provides managed DDoS protection?
    - A. WAF
    - B. Shield
    - C. GuardDuty
    - D. Firewall Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Shield mitigates DDoS attacks.
    </details>

872. Which AWS service provides a web application firewall?
    - A. Shield
    - B. WAF
    - C. NACL
    - D. Security Group

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: WAF filters web traffic based on rules.
    </details>

873. Which AWS service provides intelligent threat detection?
    - A. Inspector
    - B. Security Hub
    - C. GuardDuty
    - D. Macie

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: GuardDuty analyzes logs for malicious activity.
    </details>

874. Which AWS service assesses applications for vulnerabilities?
    - A. GuardDuty
    - B. Macie
    - C. Inspector
    - D. WAF

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Inspector scans EC2 and containers for vulnerabilities.
    </details>

875. Which AWS service protects sensitive data in S3?
    - A. GuardDuty
    - B. Inspector
    - C. Macie
    - D. KMS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Macie discovers and classifies sensitive data in S3.
    </details>

876. Which AWS service manages encryption keys?
    - A. Secrets Manager
    - B. CloudHSM
    - C. KMS
    - D. Certificate Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: KMS manages cryptographic keys.
    </details>

877. Which AWS service provides dedicated HSMs?
    - A. KMS
    - B. Secrets Manager
    - C. CloudHSM
    - D. Shield

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudHSM offers dedicated hardware security modules.
    </details>

878. Which AWS service manages application secrets?
    - A. KMS
    - B. Parameter Store
    - C. Secrets Manager
    - D. IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Secrets Manager handles secret storage and rotation.
    </details>

879. Which AWS service provides compliance reports?
    - A. Trusted Advisor
    - B. Config
    - C. Artifact
    - D. Security Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Artifact is the portal for compliance documents.
    </details>

880. Which AWS tool estimates migration savings?
    - A. Pricing Calculator
    - B. Cost Explorer
    - C. TCO Calculator
    - D. Budgets

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: TCO Calculator compares on-premises vs. AWS costs.
    </details>

881. Which AWS tool estimates costs for specific architectures?
    - A. TCO Calculator
    - B. Cost Explorer
    - C. Pricing Calculator
    - D. Budgets

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Pricing Calculator models specific service costs.
    </details>

882. Which AWS service sets cost alerts?
    - A. Cost Explorer
    - B. CUR
    - C. Budgets
    - D. Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Budgets monitors costs against thresholds.
    </details>

883. Which AWS report provides the most detailed usage data?
    - A. Cost Explorer
    - B. Budgets reports
    - C. CUR
    - D. Billing summary

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CUR offers granular line-item data.
    </details>

884. What feature helps track costs by project?
    - A. Budgets
    - B. Consolidated Billing
    - C. Cost Allocation Tags
    - D. SCPs

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Tags enable cost categorization.
    </details>

885. Which Support plan includes a TAM?
    - A. Basic
    - B. Developer
    - C. Business
    - D. Enterprise

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Only Enterprise Support includes a Technical Account Manager.
    </details>

886. What is a key benefit of elasticity in the cloud?
    - A. Paying a fixed monthly cost.
    - B. Automatically adjusting capacity to match demand.
    - C. Deploying resources globally.
    - D. Increased capital expenditure.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Elasticity allows scaling resources up or down as needed, optimizing cost and performance.
    </details>

887. Which AWS service provides block storage that persists independently of EC2 instance lifecycle?
    - A. Instance Store
    - B. Amazon S3
    - C. Amazon EBS
    - D. Amazon EFS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EBS volumes provide persistent block storage that can be detached and reattached to instances.
    </details>

888. Which AWS service would you use to host a relational database like PostgreSQL?
    - A. DynamoDB
    - B. ElastiCache
    - C. RDS
    - D. S3

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: RDS provides managed services for various relational database engines.
    </details>

889. A company needs to grant temporary, limited permissions to a mobile application user to access specific AWS resources. Which service is best suited for this?
    - A. AWS IAM User Access Keys
    - B. Amazon Cognito Identity Pools
    - C. AWS Directory Service
    - D. EC2 Instance Roles

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Cognito Identity Pools are designed to provide temporary AWS credentials to application users (authenticated or unauthenticated) to access backend resources securely.
    </details>

890. Which AWS service provides a way to centrally manage and automate operational tasks like patching and software installation across a fleet of EC2 instances?
    - A. AWS CloudFormation
    - B. AWS OpsWorks
    - C. AWS Systems Manager
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Systems Manager offers a suite of tools (including Patch Manager, Run Command, State Manager) for managing instances at scale.
    </details>

891. What is the primary function of AWS CloudTrail?
    - A. To monitor resource performance metrics.
    - B. To log API calls made within an AWS account.
    - C. To assess resources against security best practices.
    - D. To deploy infrastructure as code.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: CloudTrail records API activity for auditing, governance, and compliance.
    </details>

892. Which AWS service provides a fully managed extract, transform, and load (ETL) service?
    - A. Amazon EMR
    - B. AWS Data Pipeline
    - C. AWS Glue
    - D. Amazon Kinesis Data Analytics

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Glue is a serverless data integration service that simplifies ETL processes.
    </details>

893. Which AWS service allows you to query data directly in Amazon S3 using standard SQL?
    - A. Amazon Redshift
    - B. Amazon EMR
    - C. Amazon Athena
    - D. Amazon QuickSight

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Athena provides serverless, interactive querying capabilities for data stored in S3.
    </details>

894. Which AWS service provides a fast, cloud-powered business intelligence (BI) service?
    - A. Amazon Athena
    - B. Amazon Redshift
    - C. Amazon QuickSight
    - D. AWS Glue

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: QuickSight enables the creation and sharing of interactive dashboards and visualizations.
    </details>

895. Which AWS service helps you migrate databases to AWS easily and securely?
    - A. AWS Schema Conversion Tool (SCT)
    - B. AWS Database Migration Service (DMS)
    - C. AWS Server Migration Service (SMS)
    - D. AWS Application Discovery Service

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: DMS facilitates the actual migration process, often used alongside SCT for schema conversion.
    </details>

896. Which AWS service provides a central location to track the progress of application migrations?
    - A. AWS Application Discovery Service
    - B. AWS Server Migration Service (SMS)
    - C. AWS Migration Hub
    - D. AWS Control Tower

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Migration Hub provides a single dashboard for monitoring migration tasks across various tools.
    </details>

897. Which AWS service provides a hybrid cloud storage solution connecting on-premises applications to AWS storage?
    - A. AWS Snowball
    - B. AWS DataSync
    - C. AWS Storage Gateway
    - D. Amazon S3

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Storage Gateway bridges on-premises environments with cloud storage.
    </details>

898. Which AWS service provides centralized, policy-based backup management?
    - A. EBS Snapshots
    - B. AWS Backup
    - C. S3 Lifecycle Policies
    - D. AWS DataSync

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Backup simplifies and centralizes backup operations across supported services.
    </details>

899. Which AWS service provides a managed service for running Apache Spark or Hadoop clusters?
    - A. Amazon Redshift
    - B. Amazon Kinesis
    - C. Amazon EMR (Elastic MapReduce)
    - D. AWS Glue

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EMR simplifies running big data frameworks like Spark and Hadoop.
    </details>

900. Which AWS service provides a fully managed source control service hosting Git repositories?
    - A. AWS CodePipeline
    - B. AWS CodeBuild
    - C. AWS CodeCommit
    - D. AWS CodeDeploy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CodeCommit is AWS\s managed Git service.
    </details>

