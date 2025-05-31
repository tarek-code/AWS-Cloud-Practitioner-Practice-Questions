# AWS Cloud Practitioner Practice Questions - Batch 13 (Advanced Identity & Other Services)

451. Which AWS service provides user sign-up, sign-in, and access control for web and mobile applications?
    - A. AWS IAM (Identity and Access Management)
    - B. AWS Directory Service
    - C. Amazon Cognito
    - D. AWS IAM Identity Center (AWS SSO)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Cognito provides identity management for customer-facing applications, handling user registration, authentication, and authorization, including federation with social and enterprise identity providers.
    </details>

452. What are the two main components of Amazon Cognito?
    - A. Identity Pools and User Directories
    - B. User Pools and Identity Pools (Federated Identities)
    - C. Managed AD and Simple AD
    - D. SAML Providers and OpenID Connect Providers

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Cognito User Pools are user directories for managing sign-up/sign-in. Cognito Identity Pools provide temporary AWS credentials to grant users (authenticated via User Pools, social logins, SAML, etc.) access to AWS resources.
    </details>

453. Which AWS service provides managed directory services, such as Managed Microsoft AD, Simple AD, and AD Connector?
    - A. Amazon Cognito
    - B. AWS IAM
    - C. AWS Directory Service
    - D. AWS Organizations

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Directory Service offers various options for using managed directories in the cloud, integrating with existing on-premises AD or providing standalone directories.
    </details>

454. What is the primary use case for AWS Directory Service AD Connector?
    - A. To create a new, standalone Active Directory in the cloud.
    - B. To synchronize users between Cognito User Pools and Active Directory.
    - C. To redirect directory requests from AWS applications (like WorkSpaces or EC2 instances) to an existing on-premises Microsoft Active Directory without caching information in the cloud.
    - D. To manage DNS for Active Directory.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AD Connector acts as a directory proxy, allowing AWS services to authenticate users against your existing on-premises AD without requiring complex network setups or directory synchronization.
    </details>

455. Which AWS service simplifies managing Single Sign-On (SSO) access to multiple AWS accounts and business applications?
    - A. Amazon Cognito
    - B. AWS Directory Service
    - C. AWS IAM Identity Center (successor to AWS Single Sign-On)
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS IAM Identity Center provides a central place to manage users and their SSO access across all accounts in an AWS Organization and integrates with various third-party applications.
    </details>

456. What identity sources can be used with AWS IAM Identity Center?
    - A. Only the built-in IAM Identity Center directory.
    - B. Only external identity providers like Okta or Azure AD.
    - C. The built-in directory, an existing Active Directory (via AWS Directory Service), or an external identity provider (via SAML 2.0).
    - D. Only Amazon Cognito User Pools.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: IAM Identity Center offers flexibility by allowing you to use its own identity store, connect to your existing AD infrastructure, or federate with external SAML 2.0 compliant identity providers.
    </details>

457. Which AWS service allows you to securely share specified AWS resources with other AWS accounts or within your AWS Organization?
    - A. AWS Organizations
    - B. AWS Service Catalog
    - C. AWS Resource Access Manager (RAM)
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS RAM enables resource sharing across accounts, eliminating the need to duplicate resources in each account. Shared resources include Transit Gateways, Subnets, License Manager configurations, Route 53 Resolver rules, and more.
    </details>

458. What is a primary benefit of using AWS Resource Access Manager (RAM)?
    - A. It reduces costs by allowing resources (like subnets or Transit Gateways) to be shared instead of duplicated in multiple accounts.
    - B. It provides enhanced security monitoring.
    - C. It automates application deployment.
    - D. It manages user identities.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: RAM promotes resource efficiency and reduces operational overhead by enabling secure sharing of network infrastructure and other supported resources across accounts within an Organization or with specific external accounts.
    </details>

459. Which AWS service manages the provisioning, management, and deployment of SSL/TLS certificates for use with AWS services?
    - A. AWS Secrets Manager
    - B. AWS Key Management Service (KMS)
    - C. AWS Certificate Manager (ACM)
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: ACM simplifies obtaining, managing, and deploying public and private SSL/TLS certificates, including handling automatic renewals for public certificates.
    </details>

460. Can AWS Certificate Manager (ACM) be used to issue certificates for internal, non-public facing servers?
    - A. No, ACM only issues public certificates.
    - B. Yes, using ACM Private Certificate Authority (PCA).
    - C. Yes, but only if integrated with AWS Directory Service.
    - D. No, certificates must be obtained from a third-party CA.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: ACM Private CA allows you to create and manage your own private certificate authority within AWS, enabling you to issue private SSL/TLS certificates for internal resources.
    </details>

461. Which AWS service provides a cloud-based virtual desktop infrastructure (VDI) solution?
    - A. Amazon EC2
    - B. Amazon AppStream 2.0
    - C. Amazon WorkSpaces
    - D. AWS Lambda

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon WorkSpaces is a managed Desktop-as-a-Service (DaaS) solution that allows you to provision Windows or Linux virtual desktops for users.
    </details>

462. Which AWS service allows you to stream desktop applications securely to any device via a web browser, without needing to rewrite them?
    - A. Amazon WorkSpaces
    - B. Amazon AppStream 2.0
    - C. AWS Lambda
    - D. Amazon EC2

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Amazon AppStream 2.0 is a fully managed application streaming service that allows you to centrally manage desktop applications and securely deliver them to users on demand.
    </details>

463. Which AWS service provides a fully managed service for deploying, operating, and scaling containers using Kubernetes?
    - A. Amazon EC2
    - B. Amazon Elastic Container Service (ECS)
    - C. Amazon Elastic Kubernetes Service (EKS)
    - D. AWS Fargate

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EKS is the managed Kubernetes service on AWS, simplifying the process of running Kubernetes clusters without needing to manage the control plane.
    </details>

464. Which AWS service provides a highly scalable, fully managed container orchestration service that supports Docker containers?
    - A. Amazon Elastic Kubernetes Service (EKS)
    - B. Amazon Elastic Container Service (ECS)
    - C. AWS Lambda
    - D. Amazon EC2

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: ECS is AWS\s native container orchestration service, deeply integrated with other AWS services, offering choices for launch types (EC2 or Fargate).
    </details>

465. What is AWS Fargate?
    - A. A managed Kubernetes service.
    - B. A serverless compute engine for containers that works with both ECS and EKS, removing the need to manage underlying EC2 instances.
    - C. A service for building container images.
    - D. A container registry.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Fargate allows you to run containers without managing servers or clusters. You define your application, specify resources, and Fargate launches and scales the compute capacity needed.
    </details>

466. Which AWS service provides a fully managed Docker container registry for storing, managing, and deploying container images?
    - A. Amazon Elastic Container Service (ECS)
    - B. Amazon Elastic Kubernetes Service (EKS)
    - C. Amazon Elastic Container Registry (ECR)
    - D. AWS CodeBuild

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: ECR is a secure, scalable, and reliable AWS-managed container image registry service integrated with ECS, EKS, and IAM.
    </details>

467. Which AWS service provides a cloud-based integrated development environment (IDE) for writing, running, and debugging code?
    - A. AWS CodeCommit
    - B. AWS CodeBuild
    - C. AWS Cloud9
    - D. AWS CodeDeploy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Cloud9 provides an IDE accessible via a web browser, pre-packaged with essential tools for popular programming languages and direct terminal access to an underlying EC2 instance.
    </details>

468. Which AWS service provides a fully managed source control service that hosts secure Git-based repositories?
    - A. AWS CodePipeline
    - B. AWS CodeBuild
    - C. AWS CodeCommit
    - D. AWS CodeDeploy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CodeCommit is a secure, highly scalable, managed source control service similar to GitHub or Bitbucket, but hosted within AWS.
    </details>

469. Which AWS service provides a fully managed continuous integration service that compiles source code, runs tests, and produces software packages?
    - A. AWS CodeCommit
    - B. AWS CodePipeline
    - C. AWS CodeDeploy
    - D. AWS CodeBuild

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: CodeBuild is a build service that scales automatically and charges per minute, eliminating the need to manage build servers.
    </details>

470. Which AWS service automates software deployments to various compute services such as EC2, Fargate, Lambda, and on-premises servers?
    - A. AWS CodeBuild
    - B. AWS CodePipeline
    - C. AWS CodeDeploy
    - D. AWS CloudFormation

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CodeDeploy handles the complexity of updating applications, managing deployment health, and rolling back changes if necessary.
    </details>

471. Which AWS service provides a fully managed continuous delivery service that helps automate release pipelines for fast and reliable application and infrastructure updates?
    - A. AWS CodeDeploy
    - B. AWS CodeBuild
    - C. AWS CodeCommit
    - D. AWS CodePipeline

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: CodePipeline orchestrates the different stages of a software release process (e.g., build, test, deploy), integrating with services like CodeCommit, CodeBuild, CodeDeploy, and third-party tools.
    </details>

472. Which AWS service helps analyze and debug production, distributed applications, providing insights into performance bottlenecks and errors?
    - A. Amazon CloudWatch
    - B. AWS CloudTrail
    - C. AWS X-Ray
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS X-Ray collects data about requests served by your application, providing tools to visualize components, identify performance issues, and trace requests as they travel through different services.
    </details>

473. Which AWS service provides a managed message broker service supporting protocols like MQTT, AMQP, STOMP, etc., often used for migrating existing applications using these protocols?
    - A. Amazon SQS
    - B. Amazon SNS
    - C. Amazon MQ
    - D. Amazon Kinesis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon MQ provides managed Apache ActiveMQ and RabbitMQ brokers, making it easier to migrate applications relying on these specific broker types and protocols.
    </details>

474. Which AWS service provides a way to coordinate multiple AWS services into serverless workflows using visual diagrams?
    - A. AWS Lambda
    - B. AWS Step Functions
    - C. AWS SWF (Simple Workflow Service)
    - D. AWS Batch

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Step Functions allows you to define workflows as state machines, coordinating components like Lambda functions, ECS tasks, and API Gateway endpoints into robust applications.
    </details>

475. Which AWS service provides a petabyte-scale data warehousing solution?
    - A. Amazon RDS
    - B. Amazon DynamoDB
    - C. Amazon Redshift
    - D. Amazon S3

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Redshift is a fast, fully managed data warehouse optimized for analyzing large datasets using standard SQL and existing BI tools.
    </details>

476. Which AWS service allows you to easily process large amounts of data using frameworks like Apache Spark and Hadoop?
    - A. Amazon Redshift
    - B. Amazon Kinesis
    - C. Amazon EMR (Elastic MapReduce)
    - D. AWS Glue

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EMR provides managed clusters specifically designed for running big data processing frameworks efficiently.
    </details>

477. Which AWS service provides a fully managed extract, transform, and load (ETL) service?
    - A. Amazon EMR
    - B. AWS Data Pipeline
    - C. AWS Glue
    - D. Amazon Kinesis Data Analytics

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Glue is a serverless data integration service that includes a data catalog, ETL capabilities, and job scheduling for preparing data for analytics.
    </details>

478. Which AWS service makes it easy to collect, process, and analyze real-time streaming data?
    - A. Amazon SQS
    - B. Amazon Kinesis
    - C. AWS Glue
    - D. Amazon EMR

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: The Amazon Kinesis family (including Data Streams, Data Firehose, Data Analytics) provides services specifically designed for ingesting, processing, and analyzing streaming data at scale.
    </details>

479. Which AWS service provides a fast, scalable, serverless query service that makes it easy to analyze data directly in Amazon S3 using standard SQL?
    - A. Amazon Redshift Spectrum
    - B. Amazon EMR
    - C. Amazon Athena
    - D. Amazon QuickSight

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Athena allows you to query data stored in S3 without needing to load it into a database or data warehouse, paying only for the queries you run.
    </details>

480. Which AWS service provides a fast, cloud-powered business intelligence (BI) service for creating visualizations and dashboards?
    - A. Amazon Athena
    - B. Amazon Redshift
    - C. Amazon QuickSight
    - D. AWS Glue DataBrew

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: QuickSight allows users to connect to various data sources (including S3, Redshift, RDS, Athena) and build interactive BI dashboards accessible via browsers or mobile devices.
    </details>

481. Which AWS service provides a secure way to connect your on-premises network to your AWS VPC over the public internet using encrypted tunnels?
    - A. AWS Direct Connect
    - B. AWS VPN (Site-to-Site VPN)
    - C. VPC Peering
    - D. AWS Transit Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Site-to-Site VPN establishes secure IPsec tunnels between your customer gateway (on-premises) and a virtual private gateway or transit gateway (AWS side).
    </details>

482. Which AWS service provides a dedicated, private physical network connection between your premises and AWS?
    - A. AWS VPN
    - B. AWS Direct Connect
    - C. VPC Endpoint
    - D. Internet Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Direct Connect offers a private, high-bandwidth, low-latency connection bypassing the public internet, suitable for consistent network performance requirements.
    </details>

483. Which AWS service acts as a central cloud router to simplify network connectivity between multiple VPCs and on-premises networks?
    - A. VPC Peering
    - B. AWS Direct Connect Gateway
    - C. AWS Transit Gateway
    - D. Virtual Private Gateway (VGW)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Transit Gateway uses a hub-and-spoke model, allowing VPCs and VPN/Direct Connect attachments to connect to the central gateway, simplifying routing and management compared to numerous peering connections.
    </details>

484. Which AWS service provides a global content delivery network (CDN) service that securely delivers data, videos, applications, and APIs with low latency and high transfer speeds?
    - A. Amazon S3 Transfer Acceleration
    - B. AWS Global Accelerator
    - C. Amazon CloudFront
    - D. Elastic Load Balancing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudFront caches content at edge locations worldwide, closer to end-users, reducing latency and improving performance for delivering web assets and streaming media.
    </details>

485. Which AWS service improves the availability and performance of global applications by directing traffic to optimal endpoints over the AWS global network?
    - A. Amazon CloudFront
    - B. Elastic Load Balancing
    - C. AWS Global Accelerator
    - D. Amazon Route 53

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Global Accelerator provides static IP addresses acting as a fixed entry point and uses the AWS network to route traffic to the nearest healthy application endpoint (e.g., ELB, EC2 instance, EIP) across Regions.
    </details>

486. Which AWS service provides a managed Domain Name System (DNS) web service?
    - A. Amazon VPC
    - B. Amazon CloudFront
    - C. Amazon Route 53
    - D. AWS Direct Connect

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Route 53 provides highly available and scalable DNS services, including domain registration, DNS routing (with various policies like latency, geo, failover), and health checking.
    </details>

487. Which AWS service helps you migrate databases to AWS easily and securely, supporting homogeneous and heterogeneous migrations?
    - A. AWS Schema Conversion Tool (SCT)
    - B. AWS Database Migration Service (DMS)
    - C. AWS Server Migration Service (SMS)
    - D. AWS Application Discovery Service

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: DMS helps migrate databases with minimal downtime. For heterogeneous migrations (different database engines), it\s often used with SCT to convert the database schema.
    </details>

488. Which AWS tool helps assess and convert source database schemas and code objects to a format compatible with a target database during heterogeneous migrations?
    - A. AWS Database Migration Service (DMS)
    - B. AWS Application Discovery Service
    - C. AWS Schema Conversion Tool (SCT)
    - D. AWS Migration Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SCT analyzes the source schema and automatically converts it to be compatible with the target database engine (e.g., Oracle to PostgreSQL), highlighting any items needing manual conversion.
    </details>

489. Which AWS service provides a central location to track the progress of application migrations across multiple AWS and partner solutions?
    - A. AWS Application Discovery Service
    - B. AWS Server Migration Service (SMS)
    - C. AWS Migration Hub
    - D. AWS Control Tower

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Migration Hub provides a single dashboard to discover existing servers, plan migrations, and track the status of migrations using various tools like SMS, DMS, CloudEndure Migration, etc.
    </details>

490. Which family of AWS services provides physical devices for transferring large amounts of data into and out of AWS when network transfer is impractical?
    - A. AWS Direct Connect
    - B. AWS Storage Gateway
    - C. AWS Snow Family (Snowcone, Snowball, Snowmobile)
    - D. Amazon S3 Transfer Acceleration

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Snow Family offers secure, rugged devices of varying capacities (from terabytes with Snowcone to petabytes with Snowball Edge and exabytes with Snowmobile) for offline data transfer.
    </details>

491. Which AWS service provides a hybrid cloud storage service that enables on-premises applications to seamlessly use AWS cloud storage?
    - A. Amazon S3
    - B. Amazon EBS
    - C. AWS Storage Gateway
    - D. AWS Backup

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Storage Gateway offers different gateway types (File Gateway, Volume Gateway, Tape Gateway) that connect on-premises environments to cloud storage for backup, archiving, disaster recovery, and tiered storage.
    </details>

492. Which AWS service provides a centralized, policy-based backup service for various AWS resources (like EBS, RDS, DynamoDB, EFS) and on-premises data (via Storage Gateway)?
    - A. Amazon S3 Lifecycle Policies
    - B. EBS Snapshots
    - C. AWS Backup
    - D. AWS DataSync

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Backup simplifies backup management by allowing you to define backup plans, set retention policies, and monitor backup activity across supported services from a central console.
    </details>

493. Which AWS service provides fast, automated data transfer between on-premises storage systems and AWS storage services like S3 or EFS?
    - A. AWS Snowball
    - B. AWS DataSync
    - C. AWS Storage Gateway
    - D. Amazon S3 Transfer Acceleration

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: DataSync is an online data transfer service that accelerates moving large amounts of data over the network, handling tasks like scheduling, monitoring, encryption, and data integrity validation.
    </details>

494. Which AWS service provides a managed NoSQL key-value and document database?
    - A. Amazon RDS
    - B. Amazon Redshift
    - C. Amazon DynamoDB
    - D. Amazon Aurora

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: DynamoDB is a fully managed, serverless NoSQL database known for its high scalability, performance, and availability.
    </details>

495. Which AWS service provides a managed relational database service supporting engines like MySQL, PostgreSQL, MariaDB, Oracle, and SQL Server?
    - A. Amazon DynamoDB
    - B. Amazon Redshift
    - C. Amazon RDS (Relational Database Service)
    - D. Amazon ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: RDS simplifies setting up, operating, and scaling relational databases in the cloud by automating tasks like patching, backups, and failover.
    </details>

496. Which AWS service provides a MySQL and PostgreSQL-compatible relational database built for the cloud, offering higher performance and availability than standard MySQL/PostgreSQL?
    - A. Amazon RDS
    - B. Amazon DynamoDB
    - C. Amazon Aurora
    - D. Amazon Redshift

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Aurora is part of RDS but features a cloud-native architecture with enhanced performance, scalability, and durability, while maintaining compatibility.
    </details>

497. Which AWS service provides a managed in-memory data store or cache service, supporting engines like Redis or Memcached?
    - A. Amazon RDS
    - B. Amazon DynamoDB Accelerator (DAX)
    - C. Amazon ElastiCache
    - D. Amazon MemoryDB for Redis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: ElastiCache helps improve application performance by retrieving data from fast, managed in-memory caches instead of relying solely on slower disk-based databases.
    </details>

498. Which AWS service provides an in-memory cache specifically designed to accelerate read performance for Amazon DynamoDB?
    - A. Amazon ElastiCache for Redis
    - B. Amazon ElastiCache for Memcached
    - C. Amazon DynamoDB Accelerator (DAX)
    - D. Amazon MemoryDB for Redis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: DAX is a fully managed, highly available, in-memory cache for DynamoDB that delivers microsecond response times for read-heavy workloads.
    </details>

499. Which AWS service provides a durable, Redis-compatible, in-memory database service built for microservices architectures requiring ultra-fast performance?
    - A. Amazon ElastiCache for Redis
    - B. Amazon DynamoDB Accelerator (DAX)
    - C. Amazon MemoryDB for Redis
    - D. Amazon RDS for Redis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: MemoryDB provides Redis compatibility with added durability via a Multi-AZ transactional log, making it suitable as a primary database for applications needing both speed and data persistence.
    </details>

500. Which AWS service provides a managed graph database service?
    - A. Amazon RDS
    - B. Amazon DynamoDB
    - C. Amazon Neptune
    - D. Amazon DocumentDB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Neptune is optimized for storing and querying highly connected datasets, suitable for applications like social networking, recommendation engines, and fraud detection.
    </details>

501. Which AWS service provides a managed document database service that is compatible with MongoDB?
    - A. Amazon DynamoDB
    - B. Amazon RDS
    - C. Amazon Neptune
    - D. Amazon DocumentDB (with MongoDB compatibility)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: DocumentDB is designed for workloads that use the MongoDB API but require the scalability, availability, and manageability of a cloud-native AWS service.
    </details>

502. Which AWS service provides a managed ledger database service providing a transparent, immutable, and cryptographically verifiable transaction log?
    - A. Amazon Neptune
    - B. Amazon Timestream
    - C. Amazon Quantum Ledger Database (QLDB)
    - D. Amazon Managed Blockchain

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: QLDB is designed for systems of record where data integrity and verifiability are paramount, maintaining a complete history of all changes.
    </details>

503. Which AWS service provides a managed time series database service?
    - A. Amazon QLDB
    - B. Amazon Neptune
    - C. Amazon Timestream
    - D. Amazon DynamoDB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Timestream is optimized for storing and analyzing time-stamped data, such as IoT sensor data, application logs, and industrial telemetry.
    </details>

504. Which AWS service allows you to create and manage blockchain networks using popular open-source frameworks like Hyperledger Fabric and Ethereum?
    - A. Amazon QLDB
    - B. Amazon Managed Blockchain
    - C. Amazon Neptune
    - D. AWS Step Functions

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Managed Blockchain simplifies setting up and managing scalable blockchain networks, allowing multiple parties to transact securely without a central authority.
    </details>

505. Which AWS service provides a platform for building applications where multiple parties can transact without needing a central trusted authority, using a verifiable ledger?
    - A. Amazon QLDB
    - B. Amazon Managed Blockchain
    - C. Both A and B can be used depending on whether a centralized or decentralized trust model is needed.
    - D. Amazon Neptune

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: QLDB provides a centralized, immutable ledger owned by a single entity. Managed Blockchain provides decentralized networks using frameworks like Hyperledger Fabric or Ethereum where trust is distributed among members.
    </details>

506. Which AWS service provides a visual interface to build, train, and deploy machine learning models with little to no code?
    - A. Amazon SageMaker Studio
    - B. Amazon SageMaker Canvas
    - C. Amazon SageMaker Autopilot
    - D. Amazon SageMaker Data Wrangler

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SageMaker Canvas is designed for business analysts, providing a no-code visual interface to generate ML predictions without writing code or having ML expertise.
    </details>

507. Which AWS service automates the process of building, training, and tuning machine learning models based on your data, while providing full visibility?
    - A. Amazon SageMaker Studio
    - B. Amazon SageMaker Canvas
    - C. Amazon SageMaker Autopilot
    - D. Amazon SageMaker Ground Truth

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SageMaker Autopilot automatically explores different algorithms and parameters to find the best model for your classification or regression problem based on the data you provide.
    </details>

508. Which AWS service helps you build highly accurate training datasets for machine learning quickly using human annotators?
    - A. Amazon SageMaker Data Wrangler
    - B. Amazon SageMaker Feature Store
    - C. Amazon SageMaker Ground Truth
    - D. AWS Glue DataBrew

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SageMaker Ground Truth provides data labeling services, offering options to use automated labeling or human workforces (via Amazon Mechanical Turk, third-party vendors, or your own private workforce).
    </details>

509. Which AWS service provides a dedicated feature store for machine learning, making it easier to store, share, and manage ML features?
    - A. Amazon S3
    - B. Amazon SageMaker Data Wrangler
    - C. Amazon SageMaker Feature Store
    - D. AWS Glue Data Catalog

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SageMaker Feature Store provides a centralized repository for standardized ML features, facilitating discovery, sharing, and reuse across different ML models and teams.
    </details>

510. Which AWS service helps prepare data for machine learning faster by providing a visual interface for data selection, cleaning, transformation, and visualization?
    - A. AWS Glue Studio
    - B. Amazon SageMaker Data Wrangler
    - C. AWS Glue DataBrew
    - D. Amazon QuickSight

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SageMaker Data Wrangler is integrated into SageMaker Studio and provides tools specifically for aggregating and preparing data for ML model training with minimal coding.
    </details>

511. Which AWS service provides a visual data preparation tool for cleaning and normalizing data without writing code, often used for analytics and ML?
    - A. Amazon SageMaker Data Wrangler
    - B. AWS Glue Studio
    - C. AWS Glue DataBrew
    - D. Amazon Athena

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Glue DataBrew offers a visual interface with over 250 pre-built transformations, designed for data analysts and data scientists to easily prepare data stored in S3, Redshift, RDS, etc.
    </details>

512. Which AWS service provides a managed environment for running Apache Airflow workflows for orchestrating ETL pipelines and data workflows?
    - A. AWS Step Functions
    - B. AWS Glue Workflows
    - C. Amazon Managed Workflows for Apache Airflow (MWAA)
    - D. AWS Data Pipeline

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: MWAA provides a managed service for Apache Airflow, handling the provisioning, scaling, and maintenance of the Airflow infrastructure.
    </details>

513. Which AWS service provides a managed environment for running Jupyter notebooks, often used for data exploration and analysis?
    - A. AWS Cloud9
    - B. Amazon SageMaker Studio Notebooks (or Notebook Instances)
    - C. Amazon EMR Notebooks
    - D. All of the above can provide managed Jupyter environments.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: SageMaker provides managed notebooks integrated with its ML platform. EMR provides notebooks connected to EMR clusters for big data analysis. Cloud9 can also be configured to run Jupyter.
    </details>

514. Which AWS service provides a fully managed file storage service built on NetApp ONTAP, offering familiar file system features and data management capabilities?
    - A. Amazon EFS (Elastic File System)
    - B. Amazon FSx for Windows File Server
    - C. Amazon FSx for Lustre
    - D. Amazon FSx for NetApp ONTAP

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: FSx for NetApp ONTAP provides high-performance file storage with features like snapshots, cloning, replication, and tiering, familiar to users of NetApp systems.
    </details>

515. Which AWS service provides a fully managed, high-performance file system optimized for compute-intensive workloads like HPC, machine learning, and media processing?
    - A. Amazon EFS
    - B. Amazon FSx for Windows File Server
    - C. Amazon FSx for Lustre
    - D. Amazon S3

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: FSx for Lustre is based on the Lustre parallel file system, designed for high throughput and low latency access needed by demanding compute workloads.
    </details>

516. Which AWS service provides a simple, scalable, fully managed elastic file system for use with AWS cloud services and on-premises resources (via Direct Connect or VPN)?
    - A. Amazon EBS (Elastic Block Store)
    - B. Amazon S3 (Simple Storage Service)
    - C. Amazon EFS (Elastic File System)
    - D. Amazon FSx for Windows File Server

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EFS provides a standard file system interface (NFS) that can be mounted by multiple EC2 instances concurrently and automatically scales storage capacity up or down.
    </details>

517. Which AWS service provides fully managed file storage built on Windows Server, accessible via the SMB protocol?
    - A. Amazon EFS
    - B. Amazon FSx for Windows File Server
    - C. Amazon FSx for Lustre
    - D. Amazon S3

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: FSx for Windows File Server provides native Windows file systems with full SMB support, Active Directory integration, and other Windows features.
    </details>

518. Which AWS service provides block-level storage volumes for use with EC2 instances?
    - A. Amazon S3
    - B. Amazon EFS
    - C. Amazon EBS (Elastic Block Store)
    - D. Amazon Glacier

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EBS volumes behave like raw, unformatted block devices attached to a single EC2 instance, suitable for boot volumes and persistent storage requiring low latency access.
    </details>

519. Which AWS service provides secure, durable, and low-cost object storage suitable for data archiving and long-term backup?
    - A. Amazon S3 Standard
    - B. Amazon EBS
    - C. Amazon S3 Glacier (including Instant Retrieval, Flexible Retrieval, Deep Archive)
    - D. Amazon EFS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The S3 Glacier storage classes are specifically designed for archiving data that is accessed infrequently, offering different retrieval time options at very low storage costs.
    </details>

520. Which AWS service provides a way to run code in response to events without provisioning or managing servers?
    - A. Amazon EC2
    - B. Amazon ECS
    - C. AWS Lambda
    - D. AWS Batch

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Lambda is a serverless compute service that executes your code based on triggers (like API Gateway requests, S3 events, DynamoDB updates) and automatically scales based on demand.
    </details>

521. Which AWS service allows you to build and run applications without thinking about servers, often involving services like Lambda, API Gateway, S3, and DynamoDB?
    - A. Containerization
    - B. Virtualization
    - C. Serverless Computing
    - D. Infrastructure as Code

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Serverless computing is an architectural approach where the cloud provider manages the underlying infrastructure, allowing developers to focus solely on application code and configuration.
    </details>

522. Which AWS service acts as a front door for applications to access data, business logic, or functionality from backend services, often used with Lambda?
    - A. Elastic Load Balancing
    - B. Amazon API Gateway
    - C. Amazon CloudFront
    - D. AWS AppSync

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: API Gateway allows you to create, publish, maintain, monitor, and secure REST, HTTP, and WebSocket APIs at any scale, often routing requests to Lambda functions or other backend services.
    </details>

523. Which AWS service provides a managed GraphQL API service, making it easy to build data-driven applications?
    - A. Amazon API Gateway
    - B. AWS AppSync
    - C. AWS Step Functions
    - D. AWS Amplify

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AppSync simplifies developing GraphQL APIs by handling the connection to data sources like DynamoDB, Lambda, RDS, and others, enabling real-time updates and offline data synchronization.
    </details>

524. Which AWS service provides a development platform with a set of tools and services for building secure, scalable full-stack web and mobile applications?
    - A. AWS CodeStar
    - B. AWS Amplify
    - C. AWS Cloud9
    - D. AWS App Runner

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Amplify provides libraries, UI components, and a CLI/console experience to configure backends (like authentication, APIs, storage) and connect them to frontend web/mobile applications.
    </details>

525. Which AWS service makes it easy for developers to quickly deploy containerized web applications and APIs, scaling automatically with traffic?
    - A. Amazon ECS
    - B. Amazon EKS
    - C. AWS App Runner
    - D. AWS Elastic Beanstalk

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: App Runner provides a simple way to build and run containerized applications starting from source code or a container image, handling infrastructure, scaling, load balancing, and deployment pipelines.
    </details>

