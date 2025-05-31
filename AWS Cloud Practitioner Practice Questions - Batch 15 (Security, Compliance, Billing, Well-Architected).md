# AWS Cloud Practitioner Practice Questions - Batch 15 (Security, Compliance, Billing, Well-Architected)

651. Which AWS service provides managed DDoS protection for applications hosted on AWS?
    - A. AWS WAF
    - B. AWS Shield
    - C. Amazon GuardDuty
    - D. AWS Firewall Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Shield Standard (automatically enabled) and Shield Advanced provide protection against Distributed Denial of Service attacks.
    </details>

652. What is the difference between AWS Shield Standard and AWS Shield Advanced?
    - A. Shield Standard protects against Layer 3/4 attacks; Shield Advanced protects against Layer 7 attacks.
    - B. Shield Standard is free and provides basic protection; Shield Advanced is a paid service offering enhanced protection, visibility, and DDoS cost protection.
    - C. Shield Standard requires AWS WAF; Shield Advanced does not.
    - D. Shield Standard is managed by the customer; Shield Advanced is managed by AWS.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Shield Standard offers automatic protection against common network and transport layer DDoS attacks at no extra charge. Shield Advanced provides more sophisticated detection, mitigation, near real-time visibility, access to the AWS DDoS Response Team (DRT), and cost protection against DDoS-related usage spikes.
    </details>

653. Which AWS service helps protect web applications from common web exploits like SQL injection and cross-site scripting (XSS)?
    - A. AWS Shield
    - B. AWS WAF
    - C. Amazon Inspector
    - D. Network ACLs

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS WAF is a web application firewall that filters traffic based on rules you define, targeting common application-layer attacks.
    </details>

654. Where can AWS WAF be deployed?
    - A. Only on EC2 instances.
    - B. Only with Elastic Load Balancers.
    - C. With Amazon CloudFront, Application Load Balancer (ALB), API Gateway, and AWS AppSync.
    - D. Only with Amazon Route 53.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: WAF integrates with these front-end services to inspect incoming web requests before they reach your application.
    </details>

655. Which AWS service provides intelligent threat detection by continuously monitoring for malicious activity and unauthorized behavior using logs like CloudTrail, VPC Flow Logs, and DNS logs?
    - A. AWS Security Hub
    - B. Amazon Inspector
    - C. Amazon GuardDuty
    - D. AWS WAF

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: GuardDuty uses machine learning and threat intelligence to identify potential threats like compromised instances, reconnaissance, or unusual API activity.
    </details>

656. Which AWS service performs automated security assessments to identify vulnerabilities and deviations from best practices in EC2 instances and container images?
    - A. Amazon GuardDuty
    - B. Amazon Macie
    - C. Amazon Inspector
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Inspector scans for software vulnerabilities (CVEs) and unintended network accessibility.
    </details>

657. Which AWS service uses machine learning to discover, classify, and protect sensitive data (like PII or financial data) stored in Amazon S3?
    - A. Amazon GuardDuty
    - B. Amazon Inspector
    - C. Amazon Macie
    - D. AWS Secrets Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Macie provides visibility into data security risks within S3 buckets.
    </details>

658. Which AWS service provides a centralized view of security alerts and compliance status from various AWS services (like GuardDuty, Inspector, Macie) and partner solutions?
    - A. AWS Trusted Advisor
    - B. Amazon CloudWatch
    - C. AWS Security Hub
    - D. AWS Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Security Hub aggregates security findings and provides automated compliance checks against standards like CIS AWS Foundations Benchmark.
    </details>

659. Which AWS service allows central management of firewall rules (WAF, Security Group, Network Firewall) across multiple accounts in an AWS Organization?
    - A. AWS Security Hub
    - B. AWS Control Tower
    - C. AWS Firewall Manager
    - D. Amazon GuardDuty

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Firewall Manager simplifies the administration and maintenance of firewall rules across your organization.
    </details>

660. What is the primary function of AWS Key Management Service (KMS)?
    - A. To store application secrets.
    - B. To manage SSL/TLS certificates.
    - C. To create, manage, and control the use of cryptographic keys for encryption.
    - D. To provide dedicated hardware security modules.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: KMS is the core service for managing encryption keys used by many AWS services and customer applications.
    </details>

661. What is the difference between AWS KMS Customer Master Keys (CMKs) and data keys?
    - A. CMKs encrypt data directly; data keys encrypt CMKs.
    - B. CMKs are managed by AWS; data keys are managed by the customer.
    - C. CMKs are used to encrypt/decrypt small amounts of data (up to 4KB) or generate data keys; data keys are used to encrypt larger amounts of data outside of KMS (envelope encryption).
    - D. CMKs are stored in CloudHSM; data keys are stored in Secrets Manager.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The common pattern (envelope encryption) involves using a CMK within KMS to generate and encrypt a unique data key. This data key is then used outside KMS to encrypt the actual application data. The encrypted data key is stored alongside the encrypted data.
    </details>

662. Which AWS service provides dedicated, single-tenant hardware security modules (HSMs) for high-security key management?
    - A. AWS KMS
    - B. AWS Secrets Manager
    - C. AWS CloudHSM
    - D. AWS Certificate Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudHSM provides HSMs that you control, meeting stringent compliance requirements like FIPS 140-2 Level 3.
    </details>

663. Which AWS service is specifically designed for securely storing, managing, and automatically rotating secrets like database credentials, API keys, and passwords?
    - A. AWS KMS
    - B. AWS Systems Manager Parameter Store
    - C. AWS Secrets Manager
    - D. AWS Certificate Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Secrets Manager offers features like automated rotation integration with services like RDS, which Parameter Store does not.
    </details>

664. Which AWS service provides access to AWS compliance reports (e.g., SOC, PCI, ISO) and allows management of certain agreements?
    - A. AWS Config
    - B. AWS Trusted Advisor
    - C. AWS Artifact
    - D. AWS Security Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Artifact is the central resource for compliance-related documentation.
    </details>

665. According to the AWS Shared Responsibility Model, which of the following is AWS responsible for?
    - A. Patching the guest operating system on EC2 instances.
    - B. Configuring security groups and NACLs.
    - C. Managing the physical infrastructure (hardware, software, networking) that runs AWS services.
    - D. Encrypting customer data stored in S3.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS manages the security OF the cloud, which includes the global infrastructure. Customer responsibilities include security IN the cloud, such as OS patching, firewall configuration, and data encryption choices.
    </details>

666. According to the AWS Shared Responsibility Model, which of the following is the customer responsible for?
    - A. Managing edge locations.
    - B. Securing the physical data center facilities.
    - C. Patching the hypervisor.
    - D. Configuring IAM users, groups, roles, and policies.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Identity and access management configuration is a key customer responsibility for security IN the cloud.
    </details>

667. For a managed service like Amazon RDS, how does the Shared Responsibility Model differ from EC2?
    - A. AWS takes on more responsibility, managing the underlying OS, database patching, and backups.
    - B. The customer takes on more responsibility, managing the database engine.
    - C. There is no difference in responsibility.
    - D. AWS manages network configuration, but the customer manages patching.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: With managed services like RDS, AWS handles many operational tasks (OS patching, DB patching, backups) that the customer would manage on EC2. The customer remains responsible for network controls (security groups) and managing data within the database (including encryption options).
    </details>

668. Which AWS service provides recommendations to help optimize your AWS environment across cost, performance, security, fault tolerance, and service limits?
    - A. AWS Config
    - B. Amazon CloudWatch
    - C. AWS Trusted Advisor
    - D. AWS Well-Architected Tool

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Trusted Advisor scans your environment and provides actionable recommendations based on AWS best practices.
    </details>

669. Which AWS tool helps you review your application architectures against AWS best practices using a structured framework?
    - A. AWS Trusted Advisor
    - B. AWS Cost Explorer
    - C. AWS Well-Architected Tool
    - D. AWS Personal Health Dashboard

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Well-Architected Tool provides a questionnaire based on the pillars of the Well-Architected Framework to help identify potential risks and improvements.
    </details>

670. What are the pillars of the AWS Well-Architected Framework? (Choose FIVE)
    - A. Cost Optimization
    - B. Performance Efficiency
    - C. Security
    - D. Scalability
    - E. Reliability
    - F. Operational Excellence
    - G. Availability

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A, B, C, E, F
      Explanation: The six pillars are Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, and Sustainability (Sustainability was added more recently, but the core five often tested are the first five listed here).
    </details>

671. Which pillar of the AWS Well-Architected Framework focuses on running and monitoring systems to deliver business value and continually improving processes and procedures?
    - A. Security
    - B. Reliability
    - C. Performance Efficiency
    - D. Operational Excellence

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Operational Excellence covers aspects like automation, responding to events, and refining operational procedures.
    </details>

672. Which pillar of the AWS Well-Architected Framework focuses on protecting information, systems, and assets while delivering business value through risk assessments and mitigation strategies?
    - A. Operational Excellence
    - B. Security
    - C. Reliability
    - D. Cost Optimization

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Security covers identity management, detective controls, infrastructure protection, data protection, and incident response.
    </details>

673. Which pillar of the AWS Well-Architected Framework focuses on the ability of a system to recover from infrastructure or service disruptions, dynamically acquire computing resources, and mitigate disruptions?
    - A. Performance Efficiency
    - B. Cost Optimization
    - C. Reliability
    - D. Operational Excellence

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Reliability encompasses foundations, change management, and failure management to ensure workloads perform correctly and consistently.
    </details>

674. Which pillar of the AWS Well-Architected Framework focuses on using computing resources efficiently to meet system requirements and maintaining that efficiency as demand changes and technologies evolve?
    - A. Reliability
    - B. Security
    - C. Performance Efficiency
    - D. Cost Optimization

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Performance Efficiency includes selecting the right resource types, monitoring performance, and making informed decisions to maintain efficiency.
    </details>

675. Which pillar of the AWS Well-Architected Framework focuses on avoiding unnecessary costs?
    - A. Operational Excellence
    - B. Performance Efficiency
    - C. Reliability
    - D. Cost Optimization

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Cost Optimization involves understanding spending, controlling costs, selecting appropriate pricing models, and optimizing resource usage over time.
    </details>

676. Which AWS service allows you to visualize, understand, and manage your AWS costs and usage over time?
    - A. AWS Budgets
    - B. AWS Cost Explorer
    - C. AWS Cost and Usage Report (CUR)
    - D. AWS Pricing Calculator

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Cost Explorer provides interactive graphs and reports to analyze cost trends and usage patterns.
    </details>

677. Which AWS service enables you to set custom cost and usage thresholds and receive alerts when they are breached?
    - A. AWS Cost Explorer
    - B. AWS Budgets
    - C. AWS Trusted Advisor
    - D. Amazon CloudWatch Alarms

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Budgets is the primary tool for setting spending limits and receiving notifications.
    </details>

678. Which AWS report provides the most comprehensive and granular data about your AWS costs and usage, often used for detailed analysis with BI tools?
    - A. AWS Cost Explorer Reports
    - B. AWS Budgets Reports
    - C. AWS Cost and Usage Report (CUR)
    - D. Billing Console PDF Invoice

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The CUR contains detailed hourly or daily line items for all usage, delivered to an S3 bucket.
    </details>

679. How can you track AWS costs associated with specific projects, departments, or environments within your account?
    - A. By creating separate AWS accounts for each.
    - B. By using AWS Organizations Organizational Units (OUs).
    - C. By applying Cost Allocation Tags to resources and activating them in the Billing console.
    - D. By analyzing CloudTrail logs.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Cost Allocation Tags allow you to assign metadata to resources, which can then be used to filter and group costs in billing reports and Cost Explorer.
    </details>

680. Which AWS service allows you to centrally manage multiple AWS accounts, apply policies, and get consolidated billing?
    - A. AWS IAM
    - B. AWS Control Tower
    - C. AWS Organizations
    - D. AWS Service Catalog

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Organizations provides the foundational capabilities for multi-account management.
    </details>

681. What is the primary benefit of Consolidated Billing in AWS Organizations?
    - A. It applies security policies across all accounts.
    - B. It allows volume pricing discounts (tiering) to be aggregated across all member accounts, potentially lowering overall costs.
    - C. It simplifies user management.
    - D. It provides detailed resource monitoring.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Usage from all accounts is combined, allowing the organization to reach higher usage tiers for services with volume discounts sooner than individual accounts might.
    </details>

682. What type of policy within AWS Organizations can restrict the maximum permissions available to IAM users and roles in member accounts?
    - A. Identity-based Policies
    - B. Resource-based Policies
    - C. Service Control Policies (SCPs)
    - D. Session Policies

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SCPs act as guardrails, defining the boundaries of what actions can be performed within an account or OU, even if IAM policies grant broader permissions.
    </details>

683. Which AWS Support plan offers access to the full set of Trusted Advisor checks?
    - A. Basic
    - B. Developer
    - C. Business
    - D. Enterprise

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C, D (and Enterprise On-Ramp)
      Explanation: While Basic provides core checks, Developer adds some more, but Business, Enterprise On-Ramp, and Enterprise plans provide access to all Trusted Advisor checks across all categories.
    </details>

684. A company needs 24x7 support via phone, email, and chat with a < 1 hour response time for production system down issues. They do not require a dedicated Technical Account Manager (TAM). Which is the minimum AWS Support plan they should choose?
    - A. Basic
    - B. Developer
    - C. Business
    - D. Enterprise

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Business plan meets these requirements, offering 24x7 access and the specified SLA for critical issues, without the added cost and features (like a TAM) of the Enterprise plan.
    </details>

685. Which AWS service provides a personalized view of AWS service health events and scheduled changes that might impact your specific AWS resources?
    - A. AWS Service Health Dashboard (public status page)
    - B. AWS Personal Health Dashboard
    - C. Amazon CloudWatch Events
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: The Personal Health Dashboard is specific to your account and the resources you are using.
    </details>

686. Which AWS pricing principle states that you pay only for the individual services you consume, for as long as you use them, without long-term contracts or complex licensing?
    - A. Pay less when you reserve.
    - B. Pay less by using more.
    - C. Pay as you go.
    - D. Pay less as AWS grows.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Pay-as-you-go is a fundamental AWS pricing model, allowing flexibility and avoiding upfront costs.
    </details>

687. Which AWS pricing principle allows you to get lower prices per GB for services like S3 or data transfer as your usage increases?
    - A. Pay as you go.
    - B. Pay less when you reserve.
    - C. Pay less by using more (volume discounts).
    - D. Pay less as AWS grows.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Many AWS services have tiered pricing, where the unit cost decreases as usage volume increases.
    </details>

688. Which AWS pricing principle applies when you commit to using services like EC2 or RDS for a 1 or 3-year term using Reserved Instances or Savings Plans?
    - A. Pay as you go.
    - B. Pay less when you reserve.
    - C. Pay less by using more.
    - D. Pay less as AWS grows.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Committing to usage allows AWS to offer significant discounts compared to on-demand pricing.
    </details>

689. Which AWS tool helps you estimate the costs for a specific solution architecture you plan to deploy on AWS?
    - A. AWS Cost Explorer
    - B. AWS Budgets
    - C. AWS Pricing Calculator
    - D. AWS Total Cost of Ownership (TCO) Calculator

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Pricing Calculator is designed for estimating costs of specific AWS configurations.
    </details>

690. Which AWS tool helps compare the cost of running your applications in an on-premises data center versus on AWS?
    - A. AWS Pricing Calculator
    - B. AWS Cost Explorer
    - C. AWS Budgets
    - D. AWS Total Cost of Ownership (TCO) Calculator

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: The TCO Calculator is designed to help potential customers estimate the savings they might achieve by migrating to AWS.
    </details>

691. What does the AWS Free Tier typically provide for new accounts?
    - A. Unlimited access to all services for 12 months.
    - B. A fixed monthly credit for 12 months.
    - C. Specific amounts of certain services free for 12 months, plus some services with an always-free tier.
    - D. Free Enterprise Support for 3 months.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Free Tier includes a mix of 12-month free offers (up to limits), always-free offers (up to limits), and short-term trials.
    </details>

692. A company wants to ensure that developers in a specific OU within AWS Organizations cannot launch EC2 instances larger than t3.medium. Which service should they use?
    - A. IAM Policies
    - B. AWS Config Rules
    - C. Service Control Policies (SCPs)
    - D. AWS Budgets Actions

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SCPs can enforce restrictions like limiting allowable instance types at the OU or account level, acting as a guardrail.
    </details>

693. Which security control operates at the instance level and is stateful?
    - A. Network Access Control List (NACL)
    - B. Security Group
    - C. AWS WAF Rule
    - D. Service Control Policy (SCP)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Security Groups are associated with ENIs/instances and automatically allow return traffic for allowed outbound connections (stateful).
    </details>

694. Which security control operates at the subnet level and is stateless?
    - A. Security Group
    - B. AWS WAF Rule
    - C. Network Access Control List (NACL)
    - D. IAM Policy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: NACLs are associated with subnets and require explicit allow rules for both inbound and outbound traffic, including return traffic (stateless).
    </details>

695. You need to provide temporary AWS credentials to an application running on an EC2 instance so it can access S3, without storing long-term access keys on the instance. What is the most secure method?
    - A. Embed access keys directly in the application code.
    - B. Store access keys in a configuration file on the instance.
    - C. Create an IAM Role for EC2, attach the necessary S3 permissions policy, and associate the role with the EC2 instance.
    - D. Generate pre-signed URLs for every S3 operation.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Using IAM Roles for EC2 is the standard best practice. The instance automatically retrieves temporary credentials via its metadata service, eliminating the need to manage access keys on the instance.
    </details>

696. Which AWS service helps automate the deployment of infrastructure using code templates (JSON or YAML)?
    - A. AWS Elastic Beanstalk
    - B. AWS OpsWorks
    - C. AWS CloudFormation
    - D. AWS CodeDeploy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudFormation is AWS\s primary Infrastructure as Code (IaC) service, allowing you to define and provision AWS resources predictably and repeatedly.
    </details>

697. What is a CloudFormation Stack?
    - A. A collection of related AWS resources provisioned and managed together based on a CloudFormation template.
    - B. A version control system for templates.
    - C. A security policy for CloudFormation.
    - D. A monitoring dashboard for provisioned resources.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: A stack is the unit of deployment in CloudFormation, representing the set of resources created from a single template.
    </details>

698. Which AWS service provides a managed configuration management service using Chef or Puppet?
    - A. AWS CloudFormation
    - B. AWS Systems Manager
    - C. AWS OpsWorks (Stacks / for Chef Automate / for Puppet Enterprise)
    - D. AWS Elastic Beanstalk

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: OpsWorks provides managed environments for running Chef and Puppet to automate server configuration.
    </details>

699. Which AWS service provides operational insights and allows you to automate operational tasks across your AWS resources?
    - A. AWS CloudTrail
    - B. Amazon CloudWatch
    - C. AWS Systems Manager
    - D. AWS OpsWorks

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Systems Manager offers a suite of tools for resource grouping, patching (Patch Manager), parameter storage (Parameter Store), automation (Automation documents), remote access (Session Manager), and more.
    </details>

700. Which feature of AWS Systems Manager allows you to securely connect to EC2 instances (Linux or Windows) via a browser-based shell or CLI without needing SSH keys or bastion hosts?
    - A. Patch Manager
    - B. Run Command
    - C. Session Manager
    - D. Parameter Store

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Session Manager provides secure, audited instance access through the AWS console or CLI, improving security posture by removing the need for open inbound ports.
    </details>

701. Which AWS service provides a curated catalog of IT services approved for use on AWS, helping organizations achieve consistent governance?
    - A. AWS Marketplace
    - B. AWS Service Catalog
    - C. AWS Control Tower
    - D. AWS Organizations

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Service Catalog allows administrators to create portfolios of approved products (like CloudFormation templates for specific EC2 setups) that end-users can then launch.
    </details>

702. Which AWS service provides a digital catalog of thousands of software listings from independent software vendors (ISVs) that make it easy to find, test, buy, and deploy software that runs on AWS?
    - A. AWS Service Catalog
    - B. AWS Partner Network (APN)
    - C. AWS Marketplace
    - D. AWS Quick Starts

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Marketplace is the online store for third-party software and services deployable on AWS.
    </details>

703. A company wants to implement a hybrid cloud storage solution where frequently accessed data remains on-premises, while infrequently accessed data is tiered to low-cost cloud storage. Which AWS service facilitates this?
    - A. AWS Snowball
    - B. AWS DataSync
    - C. AWS Storage Gateway (specifically File Gateway or Volume Gateway)
    - D. Amazon S3 Intelligent-Tiering

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Storage Gateway provides on-premises appliances (virtual or hardware) that connect to AWS storage, offering modes like File Gateway (NFS/SMB access backed by S3) and Volume Gateway (iSCSI volumes backed by S3/EBS snapshots) that can cache data locally.
    </details>

704. Which AWS service provides a fully managed service for transferring large amounts of online data between on-premises storage and AWS storage services like S3 or EFS?
    - A. AWS Storage Gateway
    - B. AWS Snow Family
    - C. AWS DataSync
    - D. S3 Transfer Acceleration

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: DataSync is designed for large-scale online data transfers, automating and accelerating the process over the network.
    </details>

705. When would you typically choose an AWS Snow Family device (like Snowball Edge) over AWS DataSync for data transfer?
    - A. When transferring small amounts of data frequently.
    - B. When network bandwidth is limited, unreliable, or transferring the data online would take too long (weeks or months).
    - C. When you need real-time data replication.
    - D. When transferring data between AWS Regions.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Snow Family devices are used for offline data transfer when online methods are impractical due to network constraints or the sheer volume of data.
    </details>

706. Which AWS service provides a centralized service to automate backup management across various AWS services (like EBS, RDS, EFS, DynamoDB) and on-premises data via Storage Gateway?
    - A. EBS Snapshots + DLM
    - B. AWS Backup
    - C. Amazon S3 Lifecycle Policies
    - D. AWS DataSync

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Backup provides a unified interface and policy engine for managing backups across multiple supported services.
    </details>

707. Which AWS service provides a way to connect your on-premises network directly to AWS using a dedicated, private network connection?
    - A. AWS Site-to-Site VPN
    - B. AWS Client VPN
    - C. AWS Direct Connect
    - D. VPC Peering

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Direct Connect offers a private, high-bandwidth connection bypassing the public internet, suitable for consistent performance needs.
    </details>

708. Which AWS service provides a secure connection between user devices and AWS or on-premises networks (managed client-based VPN)?
    - A. AWS Site-to-Site VPN
    - B. AWS Direct Connect
    - C. AWS Client VPN
    - D. AWS Transit Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Client VPN allows individual users to establish secure connections to resources from their devices.
    </details>

709. Which AWS service acts as a cloud router, simplifying network connectivity between multiple VPCs and on-premises networks using a hub-and-spoke model?
    - A. VPC Peering
    - B. Virtual Private Gateway (VGW)
    - C. AWS Transit Gateway
    - D. Internet Gateway (IGW)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Transit Gateway avoids complex peering meshes and centralizes connectivity management.
    </details>

710. Which AWS service improves the availability and performance of global applications by routing user traffic through the AWS global network to the optimal application endpoint?
    - A. Amazon CloudFront
    - B. Elastic Load Balancing
    - C. AWS Global Accelerator
    - D. Amazon Route 53 Latency Routing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Global Accelerator provides static IP entry points and leverages the AWS backbone network for optimized routing, distinct from CloudFront\s content caching.
    </details>

711. A company needs to ensure data stored in S3 remains unchanged for a 7-year retention period for compliance reasons. Which S3 feature should they use?
    - A. S3 Versioning
    - B. S3 Replication
    - C. S3 Object Lock (in Compliance mode)
    - D. S3 Lifecycle Policy to Glacier Deep Archive

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Object Lock provides Write-Once-Read-Many (WORM) protection. Compliance mode prevents deletion or modification by any user, including the root account, for the duration of the retention period.
    </details>

712. Which IAM entity is best suited for granting temporary access to AWS resources for applications running on EC2 or Lambda?
    - A. IAM User
    - B. IAM Group
    - C. IAM Role
    - D. IAM Policy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: IAM Roles are designed to be assumed by services or users to obtain temporary security credentials.
    </details>

713. What is the principle of least privilege in IAM?
    - A. Granting all users administrator access.
    - B. Granting only the minimum permissions necessary to perform a specific task.
    - C. Using only IAM roles, never IAM users.
    - D. Sharing root account credentials.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: This fundamental security principle minimizes the potential impact if credentials are compromised or misused.
    </details>

714. Which AWS service would you use to centrally manage software licenses (like Windows Server or SQL Server) for use with EC2 instances?
    - A. AWS Systems Manager
    - B. AWS License Manager
    - C. AWS Service Catalog
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: License Manager helps track license usage and enforce licensing rules to maintain compliance and control costs.
    </details>

715. Which design principle of the Well-Architected Framework encourages using services like Auto Scaling and Elastic Load Balancing?
    - A. Stop guessing capacity.
    - B. Automate everything.
    - C. Use serverless architectures.
    - D. Design for failure.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: Cloud elasticity allows you to automatically scale resources up or down based on actual demand, avoiding the need to provision for peak load upfront.
    </details>

716. Which design principle of the Well-Architected Framework is supported by deploying your application across multiple Availability Zones?
    - A. Use serverless architectures.
    - B. Design for failure (Reliability pillar).
    - C. Optimize costs.
    - D. Improve performance efficiency.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Deploying across multiple AZs builds fault tolerance, ensuring the application remains available even if one AZ experiences an outage.
    </details>

717. A company wants to analyze VPC network traffic patterns for security analysis or troubleshooting. Which AWS feature provides logs of IP traffic going to and from network interfaces in the VPC?
    - A. AWS CloudTrail Logs
    - B. VPC Flow Logs
    - C. ELB Access Logs
    - D. CloudFront Access Logs

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: VPC Flow Logs capture metadata about IP traffic (source/destination IP, ports, protocol, action) for network interfaces, subnets, or entire VPCs.
    </details>

718. Which AWS service provides a managed environment to easily set up a secure, resilient, multi-account AWS environment based on best practices (a landing zone)?
    - A. AWS Organizations
    - B. AWS CloudFormation
    - C. AWS Control Tower
    - D. AWS Service Catalog

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Control Tower orchestrates multiple services (Organizations, SSO, Config, CloudTrail, etc.) to build and govern a landing zone.
    </details>

719. What is the most cost-effective S3 storage class for data that is accessed less than once per month but requires millisecond retrieval when needed?
    - A. S3 Standard-IA
    - B. S3 One Zone-IA
    - C. S3 Glacier Instant Retrieval
    - D. S3 Glacier Flexible Retrieval

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Glacier Instant Retrieval is specifically designed for archive data needing immediate access, offering low storage costs with retrieval performance similar to S3 Standard.
    </details>

720. Which AWS service should be used to record user login activity and API calls made within an AWS account for auditing purposes?
    - A. Amazon CloudWatch
    - B. AWS Config
    - C. AWS CloudTrail
    - D. Amazon GuardDuty

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudTrail provides the event history of your AWS account activity.
    </details>

721. You need to host a static website (HTML, CSS, JavaScript files) with high availability and low latency globally. Which combination of AWS services is most suitable and cost-effective?
    - A. EC2 instances with an Application Load Balancer.
    - B. Amazon S3 website hosting with Amazon CloudFront.
    - C. AWS Lambda with Amazon API Gateway.
    - D. AWS Elastic Beanstalk.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: S3 provides durable, inexpensive storage suitable for static files, and enabling website hosting is simple. CloudFront provides the global CDN for low latency delivery and caching.
    </details>

722. Which AWS database service is a fully managed NoSQL key-value and document database known for single-digit millisecond performance at any scale?
    - A. Amazon RDS
    - B. Amazon Redshift
    - C. Amazon DynamoDB
    - D. Amazon Aurora

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: DynamoDB is designed for high scalability and performance for NoSQL workloads.
    </details>

723. Which AWS service provides a MySQL and PostgreSQL-compatible relational database built for the cloud, offering enhanced performance and availability?
    - A. Amazon RDS (standard engines)
    - B. Amazon DynamoDB
    - C. Amazon Aurora
    - D. Amazon Redshift

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Aurora is AWS\s cloud-optimized relational database engine, compatible with MySQL and PostgreSQL.
    </details>

724. A developer needs to run a containerized application but wants to avoid managing the underlying EC2 instances. Which AWS compute service allows this?
    - A. Amazon EC2
    - B. AWS Lambda
    - C. AWS Fargate (with ECS or EKS)
    - D. AWS Batch

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Fargate is the serverless compute engine for containers on both ECS and EKS.
    </details>

725. Which AWS service provides recommendations based on the 5 pillars of the Well-Architected Framework?
    - A. AWS Config
    - B. AWS Trusted Advisor
    - C. Amazon Inspector
    - D. AWS Well-Architected Tool

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Trusted Advisor checks your environment against best practices defined by the Well-Architected Framework pillars.
    </details>

726. What is the purpose of Availability Zones (AZs) within an AWS Region?
    - A. To provide content caching closer to users.
    - B. To offer lower pricing for specific services.
    - C. To provide isolated locations within a Region, allowing for high availability and fault tolerance.
    - D. To connect different AWS Regions together.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AZs are distinct data centers with redundant power, networking, and connectivity within a Region. Deploying across multiple AZs protects applications from single data center failures.
    </details>

727. Which AWS service provides a way to manage infrastructure as code using JSON or YAML templates?
    - A. AWS Systems Manager
    - B. AWS CloudFormation
    - C. AWS OpsWorks
    - D. AWS CodeDeploy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: CloudFormation is the primary AWS service for Infrastructure as Code (IaC).
    </details>

728. Which AWS service would you use to create a private network connection between your on-premises data center and your AWS VPC that bypasses the public internet?
    - A. AWS Site-to-Site VPN
    - B. AWS Direct Connect
    - C. VPC Peering
    - D. AWS Transit Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Direct Connect provides a dedicated physical connection for consistent performance and potentially lower data transfer costs.
    </details>

729. Which AWS service provides a managed Domain Name System (DNS) web service?
    - A. Amazon VPC
    - B. Amazon CloudFront
    - C. Amazon Route 53
    - D. AWS Certificate Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Route 53 handles domain registration, DNS routing, and health checking.
    </details>

730. Which AWS service allows you to run code in response to events (like an S3 object upload or an API Gateway request) without managing any servers?
    - A. Amazon EC2
    - B. AWS Fargate
    - C. AWS Lambda
    - D. AWS Elastic Beanstalk

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Lambda is the core function-as-a-service (FaaS) offering in AWS, enabling event-driven serverless architectures.
    </details>

731. Which AWS billing tool allows you to forecast future costs based on historical usage?
    - A. AWS Budgets
    - B. AWS Cost and Usage Report
    - C. AWS Cost Explorer
    - D. AWS Pricing Calculator

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Cost Explorer includes forecasting capabilities based on your past spending patterns.
    </details>

732. Which AWS service provides a central location to view and manage security alerts and automate compliance checks?
    - A. Amazon GuardDuty
    - B. AWS Security Hub
    - C. Amazon Inspector
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Security Hub aggregates findings from various security services and runs compliance checks.
    </details>

733. What is the most secure way to grant an EC2 instance permission to access an S3 bucket?
    - A. Store AWS access keys in a file on the instance.
    - B. Pass access keys as user data when launching the instance.
    - C. Assign an IAM Role with the necessary S3 permissions to the instance profile.
    - D. Hardcode access keys in the application running on the instance.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Using IAM Roles for EC2 instances avoids storing long-term credentials on the instance.
    </details>

734. Which AWS service helps you migrate petabyte-scale datasets to AWS using physical appliances?
    - A. AWS DataSync
    - B. AWS Storage Gateway
    - C. AWS Snow Family (Snowball, Snowmobile)
    - D. AWS Direct Connect

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Snow Family is designed for large-scale offline data transfer.
    </details>

735. Which pillar of the AWS Well-Architected Framework emphasizes selecting the right resource types and sizes for your workload and monitoring performance?
    - A. Operational Excellence
    - B. Security
    - C. Reliability
    - D. Performance Efficiency

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Performance Efficiency focuses on using resources effectively to meet performance requirements.
    </details>

736. Which AWS service provides a managed platform-as-a-service (PaaS) offering that simplifies deploying and scaling web applications in various languages?
    - A. Amazon EC2
    - B. AWS Lambda
    - C. AWS Elastic Beanstalk
    - D. AWS CloudFormation

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Elastic Beanstalk automates infrastructure provisioning and application deployment.
    </details>

737. Which AWS service provides block-level storage volumes for use with EC2 instances?
    - A. Amazon S3
    - B. Amazon EFS
    - C. Amazon EBS
    - D. AWS Storage Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EBS provides persistent block storage for EC2.
    </details>

738. Which AWS service provides scalable object storage?
    - A. Amazon EBS
    - B. Amazon EFS
    - C. Amazon S3
    - D. Amazon RDS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 is designed for durable, highly available object storage.
    </details>

739. Which AWS service provides scalable file storage accessible via the NFS protocol, suitable for Linux workloads?
    - A. Amazon EBS
    - B. Amazon S3
    - C. Amazon EFS
    - D. Amazon FSx for Windows File Server

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EFS provides shared, elastic file storage for Linux-based instances.
    </details>

740. Which AWS service provides managed file storage accessible via the SMB protocol, suitable for Windows workloads?
    - A. Amazon EBS
    - B. Amazon S3
    - C. Amazon EFS
    - D. Amazon FSx for Windows File Server

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: FSx for Windows provides native Windows file system compatibility.
    </details>

741. Which AWS service provides a managed data warehouse service optimized for analytics?
    - A. Amazon RDS
    - B. Amazon DynamoDB
    - C. Amazon Redshift
    - D. Amazon ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Redshift is AWS\s petabyte-scale data warehousing solution.
    </details>

742. Which AWS service provides managed in-memory caching using Redis or Memcached?
    - A. Amazon RDS
    - B. Amazon DynamoDB
    - C. Amazon Redshift
    - D. Amazon ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: ElastiCache improves application performance by providing fast, in-memory data stores.
    </details>

743. Which AWS service provides a managed Kubernetes service?
    - A. Amazon ECS
    - B. Amazon EKS
    - C. AWS Fargate
    - D. AWS Lambda

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: EKS simplifies running Kubernetes on AWS.
    </details>

744. Which AWS service provides a managed container orchestration service (AWS-native)?
    - A. Amazon ECS
    - B. Amazon EKS
    - C. AWS Fargate
    - D. AWS Lambda

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: ECS is AWS\s proprietary container orchestration service.
    </details>

745. Which AWS service provides a managed build service that compiles source code, runs tests, and produces deployable artifacts?
    - A. AWS CodeCommit
    - B. AWS CodeBuild
    - C. AWS CodeDeploy
    - D. AWS CodePipeline

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: CodeBuild is the CI build service in the AWS developer tools suite.
    </details>

746. Which AWS service automates the deployment of applications to services like EC2, Lambda, or ECS?
    - A. AWS CodeCommit
    - B. AWS CodeBuild
    - C. AWS CodeDeploy
    - D. AWS CodePipeline

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CodeDeploy handles the process of deploying application revisions to compute environments.
    </details>

747. Which AWS service helps model and automate the steps involved in a software release process?
    - A. AWS CodeCommit
    - B. AWS CodeBuild
    - C. AWS CodeDeploy
    - D. AWS CodePipeline

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: CodePipeline orchestrates the end-to-end CI/CD workflow.
    </details>

748. Which AWS service provides a managed message queue service for decoupling microservices?
    - A. Amazon SNS
    - B. Amazon SQS
    - C. Amazon MQ
    - D. AWS Step Functions

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SQS provides durable, scalable queues for asynchronous communication.
    </details>

749. Which AWS service provides a managed publish/subscribe messaging service?
    - A. Amazon SQS
    - B. Amazon SNS
    - C. Amazon MQ
    - D. Kinesis Data Streams

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SNS allows message broadcasting to multiple subscribers via topics.
    </details>

750. Which AWS service allows you to coordinate multiple AWS services into serverless workflows using state machines?
    - A. Amazon SQS
    - B. Amazon SNS
    - C. AWS Lambda
    - D. AWS Step Functions

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Step Functions provides visual workflow orchestration for distributed applications.
    </details>

751. Which AWS service provides monitoring and observability through metrics, logs, and alarms?
    - A. AWS CloudTrail
    - B. AWS Config
    - C. Amazon CloudWatch
    - D. AWS X-Ray

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudWatch is the central monitoring service for AWS resources and applications.
    </details>

752. Which AWS service provides a log of API calls made within your AWS account?
    - A. Amazon CloudWatch Logs
    - B. VPC Flow Logs
    - C. AWS CloudTrail
    - D. AWS Config History

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudTrail records API activity for governance, compliance, and auditing.
    </details>

753. Which AWS service helps you track resource configuration changes and evaluate compliance?
    - A. AWS CloudTrail
    - B. AWS Config
    - C. Amazon Inspector
    - D. AWS Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Config provides resource inventory, configuration history, and configuration change notifications.
    </details>

754. Which AWS service provides a global Content Delivery Network (CDN) to accelerate website and API delivery?
    - A. AWS Global Accelerator
    - B. Amazon Route 53
    - C. Amazon CloudFront
    - D. Elastic Load Balancing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudFront caches content at edge locations globally.
    </details>

755. Which AWS service provides managed relational database instances?
    - A. Amazon DynamoDB
    - B. Amazon Redshift
    - C. Amazon RDS
    - D. Amazon DocumentDB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: RDS manages common relational database engines like MySQL, PostgreSQL, etc.
    </details>

756. Which AWS service provides a managed NoSQL database service?
    - A. Amazon RDS
    - B. Amazon Redshift
    - C. Amazon DynamoDB
    - D. Amazon Aurora

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: DynamoDB is AWS\s primary managed NoSQL offering.
    </details>

757. Which AWS service provides a platform for building, training, and deploying machine learning models at scale?
    - A. Amazon Rekognition
    - B. Amazon Lex
    - C. Amazon SageMaker
    - D. Amazon Comprehend

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SageMaker provides a comprehensive suite of tools for the entire ML lifecycle.
    </details>

758. Which AWS service provides pre-trained AI services for tasks like image analysis or natural language processing?
    - A. Amazon SageMaker
    - B. AWS AI Services (e.g., Rekognition, Comprehend, Polly)
    - C. Amazon EMR
    - D. AWS Glue

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Services like Rekognition (image/video), Comprehend (NLP), Polly (text-to-speech) offer AI capabilities via APIs.
    </details>

759. Which AWS service helps you centrally manage multiple AWS accounts and apply governance policies?
    - A. AWS IAM
    - B. AWS Control Tower
    - C. AWS Organizations
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Organizations is the service for managing multiple accounts, including consolidated billing and SCPs.
    </details>

760. Which AWS service provides automated checks and recommendations based on AWS best practices?
    - A. AWS Config
    - B. AWS CloudTrail
    - C. AWS Trusted Advisor
    - D. Amazon Inspector

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Trusted Advisor scans your environment for potential cost savings, performance improvements, security gaps, etc.
    </details>

761. Which AWS service provides managed DDoS protection?
    - A. AWS WAF
    - B. AWS Shield
    - C. Amazon GuardDuty
    - D. AWS Firewall Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Shield Standard and Advanced are dedicated to DDoS mitigation.
    </details>

762. Which AWS service acts as a web application firewall?
    - A. AWS Shield
    - B. AWS WAF
    - C. Network ACL
    - D. Security Group

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: WAF protects against common web exploits at the application layer.
    </details>

763. Which AWS service provides intelligent threat detection by analyzing logs like CloudTrail and VPC Flow Logs?
    - A. Amazon Inspector
    - B. AWS Security Hub
    - C. Amazon GuardDuty
    - D. Amazon Macie

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: GuardDuty continuously monitors for malicious or unauthorized activity.
    </details>

764. Which AWS service helps identify security vulnerabilities in EC2 instances and container images?
    - A. Amazon GuardDuty
    - B. Amazon Macie
    - C. Amazon Inspector
    - D. AWS WAF

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Inspector performs automated security assessments against known vulnerabilities.
    </details>

765. Which AWS service helps discover and protect sensitive data stored in S3?
    - A. Amazon GuardDuty
    - B. Amazon Inspector
    - C. Amazon Macie
    - D. AWS KMS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Macie focuses on data security and privacy within S3.
    </details>

766. Which AWS service provides managed creation and control of encryption keys?
    - A. AWS Secrets Manager
    - B. AWS CloudHSM
    - C. AWS Key Management Service (KMS)
    - D. AWS Certificate Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: KMS is the primary service for managing cryptographic keys integrated with AWS services.
    </details>

767. Which AWS service provides dedicated hardware security modules?
    - A. AWS KMS
    - B. AWS Secrets Manager
    - C. AWS CloudHSM
    - D. AWS Shield

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudHSM offers single-tenant, customer-controlled HSMs.
    </details>

768. Which AWS service helps manage and rotate secrets like database credentials?
    - A. AWS KMS
    - B. AWS Systems Manager Parameter Store
    - C. AWS Secrets Manager
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Secrets Manager is specifically designed for the lifecycle management of secrets, including rotation.
    </details>

769. Which AWS service provides access to AWS compliance reports?
    - A. AWS Trusted Advisor
    - B. AWS Config
    - C. AWS Artifact
    - D. AWS Security Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Artifact is the portal for downloading compliance documents.
    </details>

770. Which AWS tool helps estimate the cost savings of migrating to AWS?
    - A. AWS Pricing Calculator
    - B. AWS Cost Explorer
    - C. AWS Total Cost of Ownership (TCO) Calculator
    - D. AWS Budgets

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The TCO Calculator compares on-premises costs to estimated AWS costs.
    </details>

771. Which AWS tool helps estimate the cost of a specific planned AWS architecture?
    - A. AWS TCO Calculator
    - B. AWS Cost Explorer
    - C. AWS Pricing Calculator
    - D. AWS Budgets

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Pricing Calculator allows modeling specific service configurations.
    </details>

772. Which AWS service allows you to set spending limits and receive alerts?
    - A. AWS Cost Explorer
    - B. AWS Cost and Usage Report
    - C. AWS Budgets
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Budgets is used for cost monitoring and alerting against thresholds.
    </details>

773. Which AWS service provides the most detailed cost and usage data?
    - A. AWS Cost Explorer
    - B. AWS Budgets reports
    - C. AWS Cost and Usage Report (CUR)
    - D. Billing console summary

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The CUR provides granular, hourly/daily line-item data.
    </details>

774. What feature allows you to group costs based on tags assigned to resources?
    - A. AWS Budgets
    - B. Consolidated Billing
    - C. Cost Allocation Tags
    - D. Service Control Policies

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Activating tags for cost allocation enables cost tracking by project, department, etc.
    </details>

775. Which AWS Support plan provides access to a Technical Account Manager (TAM)?
    - A. Basic
    - B. Developer
    - C. Business
    - D. Enterprise

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: A TAM is a key feature included only with the Enterprise Support plan.
    </details>

