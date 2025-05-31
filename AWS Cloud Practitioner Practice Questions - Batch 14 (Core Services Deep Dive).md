# AWS Cloud Practitioner Practice Questions - Batch 14 (Core Services Deep Dive)

526. An application requires compute capacity that can handle sudden, unpredictable spikes in traffic. The workload is fault-tolerant and can be interrupted. Which EC2 purchasing option offers the potentially lowest cost for this scenario?
    - A. On-Demand Instances
    - B. Reserved Instances (Standard)
    - C. Spot Instances
    - D. Dedicated Hosts

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Spot Instances offer significant discounts on spare EC2 capacity. They are ideal for fault-tolerant, flexible workloads that can withstand interruptions, making them cost-effective for handling unpredictable spikes if the application is designed accordingly.
    </details>

527. You need to run a critical database on EC2 that requires a consistent level of compute resources for the next three years. Which purchasing option provides the best discount for this long-term, predictable workload?
    - A. On-Demand Instances
    - B. Spot Instances
    - C. Savings Plans or Standard Reserved Instances
    - D. Dedicated Instances

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Both Savings Plans and Standard Reserved Instances offer significant discounts (up to 72-75%) over On-Demand pricing in exchange for a 1-year or 3-year commitment to a certain level of usage. They are ideal for stable, predictable workloads like databases.
    </details>

528. What is the primary difference between EC2 Dedicated Instances and Dedicated Hosts?
    - A. Dedicated Instances run on shared hardware, while Dedicated Hosts provide dedicated physical servers.
    - B. Dedicated Instances provide visibility into the underlying physical server (sockets, cores), while Dedicated Hosts do not.
    - C. Dedicated Hosts provide dedicated physical servers for your use, offering additional visibility and control needed for certain software licenses, while Dedicated Instances run on hardware dedicated to a single customer but may share the physical server.
    - D. Dedicated Hosts are cheaper than Dedicated Instances.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Both provide dedicated hardware at some level, but Dedicated Hosts give you an entire physical server, which is often necessary for Bring Your Own License (BYOL) scenarios requiring specific hardware affinity or visibility. Dedicated Instances ensure your instances run on hardware used only by your account but don\t guarantee a whole physical server.
    </details>

529. Which Elastic Load Balancing (ELB) type operates at the application layer (Layer 7) and is best suited for routing HTTP/S traffic based on content like hostnames or paths?
    - A. Classic Load Balancer (CLB)
    - B. Network Load Balancer (NLB)
    - C. Gateway Load Balancer (GWLB)
    - D. Application Load Balancer (ALB)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: ALBs are designed for modern microservices and container-based applications, offering advanced request routing features based on HTTP/S headers, methods, query parameters, hostnames, and paths.
    </details>

530. Which Elastic Load Balancing (ELB) type operates at the transport layer (Layer 4) and is capable of handling millions of requests per second with ultra-low latency, often used for TCP/UDP traffic?
    - A. Application Load Balancer (ALB)
    - B. Classic Load Balancer (CLB)
    - C. Network Load Balancer (NLB)
    - D. Gateway Load Balancer (GWLB)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: NLBs operate at the connection level, providing high throughput and low latency. They preserve the client-side source IP address and are ideal for TCP/UDP traffic, including gaming, IoT, and high-performance applications.
    </details>

531. Which Elastic Load Balancing (ELB) type makes it easy to deploy, scale, and manage third-party virtual network appliances like firewalls, intrusion detection/prevention systems, etc.?
    - A. Application Load Balancer (ALB)
    - B. Network Load Balancer (NLB)
    - C. Classic Load Balancer (CLB)
    - D. Gateway Load Balancer (GWLB)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: GWLB operates at Layer 3 (IP) and acts as a transparent bump-in-the-wire, distributing traffic to a fleet of virtual appliances while maintaining source/destination IP addresses. It simplifies inserting security or inspection appliances into the network path.
    </details>

532. What is the primary purpose of an Auto Scaling Group (ASG) Launch Configuration or Launch Template?
    - A. To define the health checks for instances in the ASG.
    - B. To specify the template (AMI, instance type, key pair, security groups, etc.) used to launch new EC2 instances within the ASG.
    - C. To configure the load balancer attached to the ASG.
    - D. To set the desired capacity of the ASG.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: A Launch Configuration (older) or Launch Template (newer, recommended) defines all the parameters needed to launch a new EC2 instance when the ASG needs to scale out.
    </details>

533. Which Auto Scaling policy adjusts the number of instances based on a specific metric (like average CPU utilization) exceeding a threshold?
    - A. Simple Scaling Policy
    - B. Step Scaling Policy
    - C. Target Tracking Scaling Policy
    - D. Scheduled Scaling Action

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Target Tracking is generally the easiest and recommended policy type. You set a target value for a metric (e.g., 50% average CPU utilization), and the ASG automatically adjusts capacity to keep the metric at or near the target.
    </details>

534. Which Auto Scaling policy allows you to define different scaling adjustments based on the size of the alarm breach (e.g., scale out by 1 instance if CPU is 60-70%, scale out by 3 instances if CPU is >70%)?
    - A. Simple Scaling Policy
    - B. Step Scaling Policy
    - C. Target Tracking Scaling Policy
    - D. Predictive Scaling Policy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Step Scaling policies provide more granular control than Simple Scaling by allowing you to define steps that vary the scaling magnitude based on how far the metric is from the threshold.
    </details>

535. Which Auto Scaling feature uses machine learning to predict future traffic patterns and provision the right number of EC2 instances in advance?
    - A. Scheduled Scaling
    - B. Target Tracking Scaling
    - C. Step Scaling
    - D. Predictive Scaling

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Predictive Scaling analyzes historical workload patterns and forecasts future demand, proactively adjusting capacity to handle expected changes, often combined with dynamic scaling policies.
    </details>

536. What is the purpose of Auto Scaling Group lifecycle hooks?
    - A. To perform custom actions (like installing software or downloading data) on an instance before it is put into service (during scale-out) or before it is terminated (during scale-in).
    - B. To trigger scaling actions based on a schedule.
    - C. To define the health check type for the ASG.
    - D. To attach a load balancer to the ASG.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: Lifecycle hooks pause the instance launch or termination process, allowing you to run custom scripts or processes at specific points in the instance lifecycle within an ASG.
    </details>

537. Which S3 storage class is designed for frequently accessed data requiring low latency and high throughput, suitable for dynamic websites, content distribution, and mobile/gaming applications?
    - A. S3 Glacier Deep Archive
    - B. S3 Standard-Infrequent Access (S3 Standard-IA)
    - C. S3 Standard
    - D. S3 One Zone-Infrequent Access (S3 One Zone-IA)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Standard is the default storage class, offering high durability, availability, and performance for frequently accessed data.
    </details>

538. Which S3 storage class offers the high durability and availability of S3 Standard but with a lower storage price and a per-GB retrieval fee, suitable for long-lived, less frequently accessed data like backups or disaster recovery files?
    - A. S3 Standard
    - B. S3 Intelligent-Tiering
    - C. S3 Standard-Infrequent Access (S3 Standard-IA)
    - D. S3 One Zone-Infrequent Access (S3 One Zone-IA)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Standard-IA provides the same high durability (99.999999999%) and availability (99.9%) as S3 Standard by storing data across multiple AZs, but optimizes for cost savings on storage when data is accessed less often.
    </details>

539. Which S3 storage class provides the lowest storage cost but stores data in only a single Availability Zone, making it suitable for easily reproducible, infrequently accessed data where lower availability is acceptable?
    - A. S3 Standard
    - B. S3 Standard-IA
    - C. S3 Glacier Flexible Retrieval
    - D. S3 One Zone-Infrequent Access (S3 One Zone-IA)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: S3 One Zone-IA sacrifices the multi-AZ resilience of other S3 classes for even lower storage costs. It\s appropriate for secondary backups or data that can be easily recreated if the AZ fails.
    </details>

540. Which S3 storage class automatically moves data between two access tiers (frequent and infrequent) based on changing access patterns, optimizing costs without performance impact or operational overhead?
    - A. S3 Standard
    - B. S3 Intelligent-Tiering
    - C. S3 Standard-IA
    - D. S3 Lifecycle Policies

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: S3 Intelligent-Tiering monitors access patterns and automatically moves objects that haven\t been accessed to the lower-cost infrequent access tier. If accessed later, the object moves back to the frequent access tier. It can also optionally archive data to Glacier tiers.
    </details>

541. Which S3 storage class is designed for long-term data archiving with retrieval times ranging from minutes to hours, offering a balance between cost and retrieval speed?
    - A. S3 Standard-IA
    - B. S3 Glacier Instant Retrieval
    - C. S3 Glacier Flexible Retrieval
    - D. S3 Glacier Deep Archive

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Glacier Flexible Retrieval (formerly S3 Glacier) is suitable for archives where occasional retrieval is needed, offering expedited (minutes), standard (hours), or bulk (longer) retrieval options.
    </details>

542. Which S3 storage class provides the absolute lowest storage cost in AWS, designed for long-term retention (years) of data that is rarely accessed, with retrieval times typically within 12 hours?
    - A. S3 Glacier Instant Retrieval
    - B. S3 Glacier Flexible Retrieval
    - C. S3 One Zone-IA
    - D. S3 Glacier Deep Archive

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: S3 Glacier Deep Archive offers the cheapest S3 storage, ideal for compliance archives or data preservation where long retrieval times are acceptable.
    </details>

543. Which S3 storage class is designed for archiving data that needs immediate, millisecond access when retrieved, but is accessed infrequently?
    - A. S3 Standard-IA
    - B. S3 Glacier Instant Retrieval
    - C. S3 Glacier Flexible Retrieval
    - D. S3 Intelligent-Tiering (Archive Access Tiers)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: S3 Glacier Instant Retrieval offers the low latency and high throughput of S3 Standard but with storage costs comparable to S3 Standard-IA, suitable for archives needing rapid access when requested.
    </details>

544. What is the purpose of S3 Versioning?
    - A. To automatically move objects between storage classes.
    - B. To keep multiple variants of an object in the same bucket, protecting against accidental overwrites or deletions.
    - C. To replicate objects to another Region.
    - D. To encrypt objects at rest.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: When versioning is enabled, S3 preserves existing objects whenever they are overwritten or deleted. This allows you to retrieve previous versions or recover from unintended actions.
    </details>

545. Which S3 feature allows you to automatically replicate objects from a source bucket to one or more destination buckets in the same or different AWS Regions?
    - A. S3 Versioning
    - B. S3 Lifecycle Policies
    - C. S3 Cross-Region Replication (CRR) / Same-Region Replication (SRR)
    - D. S3 Transfer Acceleration

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Replication copies objects asynchronously to destination buckets, useful for compliance, disaster recovery, minimizing latency, or creating shared datasets across Regions.
    </details>

546. Which S3 feature enables faster, easier, and more secure transfers of files over long distances between your client and an S3 bucket?
    - A. S3 Replication
    - B. S3 Multipart Upload
    - C. S3 Transfer Acceleration
    - D. S3 Pre-signed URLs

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Transfer Acceleration uses CloudFront\s globally distributed edge locations to accelerate uploads/downloads to S3 by routing traffic over an optimized network path.
    </details>

547. What is an S3 Pre-signed URL?
    - A. A URL that automatically redirects to the nearest S3 edge location.
    - B. A URL that grants temporary access (based on the creator\s credentials) to a specific S3 object for a limited time, without requiring AWS credentials.
    - C. A URL used for S3 website endpoints.
    - D. A URL for accessing S3 Glacier archives.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Pre-signed URLs provide a secure way to grant time-limited download or upload access to objects, useful for sharing specific files with users who don\t have AWS accounts or permissions.
    </details>

548. Which EBS volume type provides the highest performance SSD storage, designed for latency-sensitive transactional workloads like large relational or NoSQL databases?
    - A. General Purpose SSD (gp3 / gp2)
    - B. Provisioned IOPS SSD (io2 Block Express / io1)
    - C. Throughput Optimized HDD (st1)
    - D. Cold HDD (sc1)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Provisioned IOPS SSD volumes (especially io2 Block Express) are engineered for I/O-intensive workloads requiring consistent, high IOPS performance and low latency.
    </details>

549. Which EBS volume type offers a balance of price and performance using SSDs, suitable for a wide variety of transactional workloads like boot volumes, virtual desktops, and development/test environments?
    - A. Provisioned IOPS SSD (io1/io2)
    - B. Throughput Optimized HDD (st1)
    - C. General Purpose SSD (gp3 / gp2)
    - D. Cold HDD (sc1)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: General Purpose SSD volumes (gp3 is the latest generation, offering better baseline performance and independent scaling of IOPS/throughput) provide cost-effective SSD performance suitable for most common workloads.
    </details>

550. Which EBS volume type uses Hard Disk Drives (HDDs) and is optimized for frequently accessed, throughput-intensive workloads with large datasets and large I/O sizes, such as big data analytics, data warehousing, and log processing?
    - A. General Purpose SSD (gp3 / gp2)
    - B. Provisioned IOPS SSD (io1/io2)
    - C. Cold HDD (sc1)
    - D. Throughput Optimized HDD (st1)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: st1 volumes provide low-cost magnetic storage focused on delivering high sequential throughput (MB/s) rather than high IOPS, making them ideal for large, sequential read/write operations.
    </details>

551. Which EBS volume type provides the lowest cost HDD storage per GB, designed for less frequently accessed workloads requiring large, cold data storage?
    - A. Throughput Optimized HDD (st1)
    - B. General Purpose SSD (gp3 / gp2)
    - C. Provisioned IOPS SSD (io1/io2)
    - D. Cold HDD (sc1)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: sc1 volumes offer the cheapest EBS storage, optimized for cost savings on large volumes of infrequently accessed data where throughput and IOPS are less critical.
    </details>

552. What is an EBS Snapshot?
    - A. A real-time replica of an EBS volume in another AZ.
    - B. A point-in-time backup copy of an EBS volume stored durably in Amazon S3.
    - C. A performance baseline measurement for an EBS volume.
    - D. An encrypted version of an EBS volume.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: EBS Snapshots are incremental backups stored in S3. They can be used to create new EBS volumes, restore existing volumes, or copy volumes across AZs or Regions.
    </details>

553. Are EBS Snapshots incremental?
    - A. No, each snapshot is a full copy of the volume.
    - B. Yes, only the blocks that have changed since the last snapshot are saved, although you only need the latest snapshot to restore the full volume.
    - C. Only if you enable versioning on the snapshot.
    - D. Only for SSD volumes, not HDD volumes.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: EBS snapshots are incremental, meaning subsequent snapshots only store the changed blocks, saving on storage costs and reducing backup time. However, the snapshot process presents a simple, complete point-in-time view for restoration.
    </details>

554. Can you create an EBS volume from a snapshot in a different Availability Zone or Region than the original volume?
    - A. Only in a different AZ within the same Region.
    - B. Only in a different Region, not a different AZ.
    - C. Yes, snapshots can be used to create volumes in any AZ within the same Region, and snapshots can be copied to other Regions to create volumes there.
    - D. No, volumes can only be created in the same AZ as the original snapshot.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Snapshots are stored regionally but are AZ-independent within that Region. You can create a volume from a snapshot in any AZ in its Region. To create a volume in a different Region, you must first copy the snapshot to that target Region.
    </details>

555. What is the purpose of Amazon Data Lifecycle Manager (DLM)?
    - A. To automatically move S3 objects between storage classes.
    - B. To automate the creation, retention, and deletion of EBS snapshots and EBS-backed AMIs.
    - C. To manage the lifecycle of IAM users.
    - D. To replicate EBS volumes across Regions.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: DLM allows you to define policies to manage the lifecycle of EBS snapshots and AMIs based on schedules or tags, simplifying backup management and ensuring compliance with retention requirements.
    </details>

556. Which VPC component controls traffic flow between subnets and to/from gateways (like IGW, VGW)?
    - A. Security Group
    - B. Network Access Control List (NACL)
    - C. Route Table
    - D. VPC Endpoint

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Route tables contain rules (routes) that determine where network traffic originating from associated subnets is directed based on its destination IP address.
    </details>

557. What is the difference in scope between Security Groups and Network ACLs (NACLs)?
    - A. Security Groups operate at the VPC level, NACLs at the subnet level.
    - B. Security Groups operate at the instance level, NACLs operate at the subnet level.
    - C. Security Groups operate at the subnet level, NACLs at the instance level.
    - D. Both operate at the instance level.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Security Groups act as a stateful firewall associated directly with network interfaces (and thus instances). NACLs act as a stateless firewall associated with one or more subnets, controlling traffic entering or leaving those subnets.
    </details>

558. Which VPC feature allows instances in a private subnet to access the internet for updates without allowing inbound connections from the internet?
    - A. Internet Gateway (IGW)
    - B. Virtual Private Gateway (VGW)
    - C. NAT Gateway or NAT Instance
    - D. VPC Peering

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: A NAT (Network Address Translation) device (either the managed NAT Gateway service or a self-managed NAT Instance on EC2) performs address translation, allowing private instances to initiate outbound connections while masking their private IPs.
    </details>

559. What is the purpose of a VPC Endpoint?
    - A. To connect a VPC to an on-premises network.
    - B. To connect two VPCs together.
    - C. To enable private connectivity from a VPC to supported AWS services (like S3, DynamoDB, API Gateway) or endpoint services without traversing the public internet.
    - D. To provide DNS resolution within a VPC.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: VPC Endpoints keep traffic between your VPC and supported services on the AWS private network, enhancing security and potentially reducing data transfer costs.
    </details>

560. What are the two types of VPC Endpoints?
    - A. Public Endpoints and Private Endpoints
    - B. Gateway Endpoints and Interface Endpoints
    - C. Service Endpoints and Client Endpoints
    - D. Regional Endpoints and Zonal Endpoints

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Gateway Endpoints are used for S3 and DynamoDB and modify route tables. Interface Endpoints (powered by AWS PrivateLink) use an Elastic Network Interface (ENI) with a private IP address to access many other AWS services and custom endpoint services.
    </details>

561. Which Route 53 routing policy would you use to distribute traffic across multiple resources based on the proportion you define (e.g., 80% to server A, 20% to server B)?
    - A. Simple Routing
    - B. Failover Routing
    - C. Weighted Routing
    - D. Latency Routing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Weighted routing allows you to assign weights to different resource record sets for the same domain name, controlling the percentage of traffic directed to each corresponding resource.
    </details>

562. Which Route 53 routing policy directs users to the endpoint that provides the lowest network latency from their location?
    - A. Geolocation Routing
    - B. Weighted Routing
    - C. Latency Routing
    - D. Failover Routing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Latency-based routing uses AWS\s network latency measurements to route users to the AWS Region or endpoint that will give them the fastest response time.
    </details>

563. Which Route 53 routing policy routes traffic based on the user\s geographic location (e.g., country or continent)?
    - A. Latency Routing
    - B. Geolocation Routing
    - C. Weighted Routing
    - D. Geoproximity Routing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Geolocation routing allows you to serve content or direct users based on their physical location, often used for localization or content distribution rights management.
    </details>

564. Which Route 53 routing policy is used primarily for active-passive disaster recovery, directing traffic to a secondary resource only if the primary resource fails health checks?
    - A. Weighted Routing
    - B. Latency Routing
    - C. Multivalue Answer Routing
    - D. Failover Routing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Failover routing requires Route 53 health checks. Traffic goes to the primary resource when healthy; if it fails the health check, traffic is automatically diverted to the designated secondary (failover) resource.
    </details>

565. Which Route 53 feature allows you to monitor the health of your endpoints (like web servers or ELBs) and influence routing decisions (e.g., in Failover routing)?
    - A. Alias Records
    - B. Private Hosted Zones
    - C. Route 53 Health Checks
    - D. Traffic Flow

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Route 53 Health Checks monitor specified endpoints (via HTTP, HTTPS, TCP) and report their status, which can then be used by routing policies like Failover or in CloudWatch alarms.
    </details>

566. What is an Amazon Route 53 Alias record?
    - A. A standard CNAME record.
    - B. A Route 53 specific record type that lets you map your domain name (e.g., example.com) to AWS resources like CloudFront distributions, ELBs, S3 website endpoints, or other Route 53 records in the same hosted zone.
    - C. A record used for email validation (MX record).
    - D. A record that routes traffic based on latency.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Alias records provide CNAME-like functionality but can be used at the zone apex (e.g., example.com, where CNAMEs are not allowed) and often offer benefits like no charge for Alias queries to AWS resources.
    </details>

567. Can you use an EC2 instance\s public IP address directly in a Route 53 record set?
    - A. Yes, using an A record.
    - B. Yes, using an Alias record.
    - C. No, you should use an Elastic IP address associated with the instance and create an A record for the EIP.
    - D. No, you must put the instance behind an ELB and use an Alias record for the ELB.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Standard public IP addresses assigned to EC2 instances can change if the instance is stopped/started. For a stable DNS entry pointing to an instance, you should associate an Elastic IP (a static public IP) with it and create an A record pointing to that EIP.
    </details>

568. What is the purpose of a Private Hosted Zone in Route 53?
    - A. To manage DNS for public domains.
    - B. To manage internal DNS names (e.g., internal.example.com) for resources within one or more specified VPCs, not resolvable on the public internet.
    - C. To host website content privately.
    - D. To configure health checks for internal resources.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Private Hosted Zones allow you to use custom domain names for your internal applications within your VPCs without exposing that DNS information publicly.
    </details>

569. Which AWS service provides managed hardware security modules (HSMs) in the cloud?
    - A. AWS KMS
    - B. AWS Secrets Manager
    - C. AWS CloudHSM
    - D. AWS Certificate Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudHSM provides dedicated, single-tenant HSM appliances compliant with standards like FIPS 140-2 Level 3, offering high levels of security and control over cryptographic keys.
    </details>

570. Which AWS service is designed to protect web applications from common exploits like SQL injection and cross-site scripting?
    - A. AWS Shield
    - B. AWS WAF (Web Application Firewall)
    - C. Amazon GuardDuty
    - D. Network ACLs

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS WAF operates at the application layer (Layer 7) to inspect web requests and block malicious patterns based on configured rules.
    </details>

571. Which AWS service provides threat detection by continuously monitoring logs like CloudTrail, VPC Flow Logs, and DNS logs for malicious or unauthorized activity?
    - A. Amazon Inspector
    - B. AWS Security Hub
    - C. Amazon GuardDuty
    - D. AWS WAF

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: GuardDuty uses machine learning, anomaly detection, and integrated threat intelligence to identify potential security threats across your AWS accounts and workloads.
    </details>

572. Which AWS service helps you assess applications for vulnerabilities and deviations from security best practices, focusing on EC2 instances and container images?
    - A. Amazon GuardDuty
    - B. Amazon Macie
    - C. Amazon Inspector
    - D. AWS Shield

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Inspector performs automated security assessments, checking for software vulnerabilities (CVEs) and unintended network exposure.
    </details>

573. Which AWS service uses machine learning to discover, classify, and protect sensitive data (like PII) stored in Amazon S3?
    - A. Amazon GuardDuty
    - B. Amazon Inspector
    - C. Amazon Macie
    - D. AWS Secrets Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Macie focuses specifically on data security and privacy within S3, identifying sensitive data types and alerting on potential risks like publicly accessible buckets containing sensitive data.
    </details>

574. Which AWS service provides a central view of security alerts and compliance status from various AWS services and partner tools?
    - A. AWS Trusted Advisor
    - B. Amazon GuardDuty
    - C. AWS Security Hub
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Security Hub aggregates findings, runs automated compliance checks against security standards, and provides a unified dashboard for managing security posture.
    </details>

575. Which AWS service allows you to centrally manage firewall rules (WAF, Security Group, Network Firewall) across multiple accounts in an AWS Organization?
    - A. AWS Shield
    - B. AWS Security Hub
    - C. AWS Firewall Manager
    - D. Amazon GuardDuty

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Firewall Manager simplifies the administration of firewall rules across your organization, ensuring consistent policy application.
    </details>

576. What is the primary purpose of AWS Key Management Service (KMS)?
    - A. To manage SSL/TLS certificates.
    - B. To store application secrets like database passwords.
    - C. To create and control the cryptographic keys used to encrypt data across AWS services.
    - D. To provide dedicated HSM hardware.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: KMS provides a secure and highly available managed service for creating, managing, and auditing the use of encryption keys (CMKs) integrated with numerous AWS services.
    </details>

577. Which AWS service helps you securely store, manage, and automatically rotate secrets like database credentials and API keys?
    - A. AWS KMS
    - B. AWS Systems Manager Parameter Store
    - C. AWS Secrets Manager
    - D. AWS Certificate Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Secrets Manager is specifically designed for the lifecycle management of secrets, including automated rotation capabilities for supported services.
    </details>

578. Which AWS service provides managed DDoS protection?
    - A. AWS WAF
    - B. AWS Shield
    - C. Amazon GuardDuty
    - D. AWS Firewall Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Shield (Standard and Advanced) is the service dedicated to protecting AWS resources against Distributed Denial of Service attacks.
    </details>

579. Which AWS service provides on-demand access to AWS compliance reports like SOC 2, PCI DSS, and ISO certifications?
    - A. AWS Trusted Advisor
    - B. AWS Artifact
    - C. AWS Config
    - D. AWS Security Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Artifact is the central portal for accessing AWS compliance documentation and managing certain agreements.
    </details>

580. Which AWS service provides recommendations based on best practices across cost optimization, performance, security, fault tolerance, and service limits?
    - A. AWS Config
    - B. AWS CloudTrail
    - C. AWS Trusted Advisor
    - D. AWS Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Trusted Advisor acts as a cloud optimization expert, analyzing your environment and providing actionable recommendations.
    </details>

581. What is the AWS Shared Responsibility Model?
    - A. AWS is responsible for all security.
    - B. The customer is responsible for all security.
    - C. AWS is responsible for security OF the cloud (infrastructure), while the customer is responsible for security IN the cloud (data, applications, configuration).
    - D. Security responsibilities are equally shared for all aspects.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: This model clearly defines the division of security tasks. AWS secures the underlying global infrastructure, and the customer secures everything they put on that infrastructure.
    </details>

582. Under the Shared Responsibility Model, who is responsible for patching the operating system on an EC2 instance?
    - A. AWS
    - B. The Customer
    - C. Both AWS and the Customer
    - D. Neither, patching is not required.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: For IaaS services like EC2, the customer is responsible for managing and patching the guest operating system, applications, and configuring security controls like firewalls.
    </details>

583. Under the Shared Responsibility Model, who is responsible for the security of the physical AWS data centers?
    - A. The Customer
    - B. AWS
    - C. A third-party security firm
    - D. The local government

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Physical security of the data centers housing the AWS infrastructure is part of AWS\s responsibility for security OF the cloud.
    </details>

584. Which AWS service allows you to visualize, understand, and manage your AWS costs and usage?
    - A. AWS Budgets
    - B. AWS Cost Explorer
    - C. AWS Cost and Usage Report (CUR)
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Cost Explorer provides graphical tools and reports for analyzing spending patterns and identifying cost drivers.
    </details>

585. Which AWS service allows you to set custom spending thresholds and receive alerts when costs exceed those thresholds?
    - A. AWS Cost Explorer
    - B. AWS Budgets
    - C. AWS Organizations
    - D. AWS Pricing Calculator

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Budgets is the primary tool for monitoring costs against defined limits and triggering notifications or actions.
    </details>

586. Which AWS report provides the most granular cost and usage data, suitable for detailed analysis?
    - A. AWS Cost Explorer daily report
    - B. AWS Budgets monthly report
    - C. AWS Cost and Usage Report (CUR)
    - D. AWS Trusted Advisor cost report

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The CUR contains detailed line items for usage and costs, typically delivered to S3 for analysis with tools like Athena or QuickSight.
    </details>

587. What is the primary benefit of using Cost Allocation Tags?
    - A. To enforce security policies.
    - B. To automate resource deployment.
    - C. To categorize and track AWS costs based on business needs (e.g., project, department).
    - D. To improve resource performance.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Tags allow you to assign metadata to resources, and activating them for cost allocation enables cost tracking based on these tags in billing reports.
    </details>

588. Which AWS service helps you manage multiple AWS accounts centrally, including consolidated billing and policy application?
    - A. AWS IAM
    - B. AWS Control Tower
    - C. AWS Organizations
    - D. AWS Service Catalog

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Organizations provides the framework for managing a collection of accounts, enabling features like consolidated billing and Service Control Policies (SCPs).
    </details>

589. What is the function of Service Control Policies (SCPs) in AWS Organizations?
    - A. To grant permissions to users.
    - B. To define the maximum allowable permissions (guardrails) for accounts within an OU.
    - C. To monitor costs across accounts.
    - D. To automate operational tasks.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SCPs restrict what actions IAM users and roles in member accounts can perform, acting as organizational boundaries.
    </details>

590. Which AWS Support plan is included at no additional cost with every AWS account?
    - A. Developer
    - B. Business
    - C. Enterprise
    - D. Basic

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Basic Support provides fundamental support resources like documentation, forums, and core Trusted Advisor checks.
    </details>

591. Which AWS Support plan provides access to a designated Technical Account Manager (TAM)?
    - A. Basic
    - B. Developer
    - C. Business
    - D. Enterprise

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: A TAM is a key feature of the Enterprise Support plan, offering proactive guidance and advocacy.
    </details>

592. Which AWS Support plans offer response times of less than 1 hour for production system down cases? (Choose TWO)
    - A. Basic
    - B. Developer
    - C. Business
    - D. Enterprise
    - E. Enterprise On-Ramp

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C, D, E
      Explanation: Business, Enterprise On-Ramp, and Enterprise plans all provide < 1 hour response time SLAs for critical production issues. (Note: The question asks for two, but three fit. Typically Business and Enterprise are the main tiers considered after Developer).
    </details>

593. Which AWS service provides a personalized view of AWS service health events that may impact your specific resources?
    - A. AWS Service Health Dashboard
    - B. AWS Personal Health Dashboard
    - C. Amazon CloudWatch
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: The Personal Health Dashboard filters events based on your account\s resources and configuration.
    </details>

594. Which EC2 pricing model offers the largest potential discount but carries the risk of instances being terminated with short notice?
    - A. On-Demand
    - B. Reserved Instances
    - C. Savings Plans
    - D. Spot Instances

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Spot Instances utilize spare capacity and offer deep discounts, but AWS can reclaim the capacity when needed.
    </details>

595. Which AWS pricing model provides discounts for committing to a consistent amount of compute usage ($/hour) over a 1 or 3-year term, offering flexibility across instance families and Regions?
    - A. Spot Instances
    - B. Reserved Instances (Standard)
    - C. Savings Plans
    - D. On-Demand Instances

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Savings Plans offer commitment-based discounts similar to RIs but provide more flexibility in how that commitment is applied across different compute services or instance types.
    </details>

596. Which AWS tool allows you to estimate the cost of a planned AWS solution before deploying it?
    - A. AWS Cost Explorer
    - B. AWS Budgets
    - C. AWS Pricing Calculator
    - D. AWS Cost and Usage Report

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Pricing Calculator is designed for modeling architectures and estimating their costs based on selected services and configurations.
    </details>

597. What does the AWS Free Tier typically offer?
    - A. Permanent free access to all AWS services.
    - B. Limited-time free trials or limited quantities of services free indefinitely.
    - C. Discounts on Reserved Instances.
    - D. Access to the Enterprise Support plan.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: The Free Tier includes offers like 12 months free for certain services up to limits, always-free tiers for some services, and short-term trials.
    </details>

598. Which AWS service provides a fully managed platform for building, training, and deploying machine learning models?
    - A. Amazon Rekognition
    - B. Amazon Comprehend
    - C. Amazon SageMaker
    - D. Amazon Lex

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SageMaker is the comprehensive AWS service covering the entire ML lifecycle.
    </details>

599. Which AWS service provides pre-trained AI models for tasks like image analysis, text-to-speech, and translation via APIs?
    - A. Amazon SageMaker
    - B. AWS AI Services (e.g., Rekognition, Polly, Translate)
    - C. Amazon EMR
    - D. AWS Glue

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Services like Rekognition, Polly, Translate, Comprehend, Lex, etc., offer specialized AI capabilities without requiring users to build their own models.
    </details>

600. Which AWS service simplifies setting up a secure, multi-account AWS environment following best practices (landing zone)?
    - A. AWS Organizations
    - B. AWS Control Tower
    - C. AWS Service Catalog
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Control Tower automates the creation of a well-architected landing zone using multiple underlying AWS services.
    </details>

601. Which S3 feature helps protect against accidental object deletion or overwrites?
    - A. S3 Lifecycle Policies
    - B. S3 Replication
    - C. S3 Versioning
    - D. S3 Intelligent-Tiering

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Versioning keeps all versions of an object, allowing recovery of previous states.
    </details>

602. Which EBS volume type is recommended for the boot volume of most general-purpose EC2 instances?
    - A. Provisioned IOPS SSD (io1/io2)
    - B. Throughput Optimized HDD (st1)
    - C. General Purpose SSD (gp3/gp2)
    - D. Cold HDD (sc1)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: General Purpose SSDs offer a good balance of cost and performance suitable for boot volumes and many common application needs.
    </details>

603. What is the function of an Internet Gateway (IGW) in a VPC?
    - A. To connect the VPC to an on-premises network via VPN.
    - B. To allow communication between the VPC and the public internet.
    - C. To enable private communication between VPCs.
    - D. To provide NAT services for private subnets.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: An IGW is attached to a VPC and serves as a target in route tables for internet-bound traffic.
    </details>

604. Which AWS service provides managed DNS resolution?
    - A. Amazon VPC
    - B. Amazon CloudFront
    - C. Amazon Route 53
    - D. Elastic Load Balancing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Route 53 is AWS\s scalable and highly available Domain Name System service.
    </details>

605. Which type of Elastic Load Balancer is best suited for handling extreme performance TCP traffic?
    - A. Application Load Balancer (ALB)
    - B. Network Load Balancer (NLB)
    - C. Classic Load Balancer (CLB)
    - D. Gateway Load Balancer (GWLB)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: NLBs operate at Layer 4 and are designed for high throughput, low latency TCP/UDP load balancing.
    </details>

606. Which Auto Scaling policy maintains a specified average metric (like CPU utilization) across all instances in the group?
    - A. Simple Scaling
    - B. Step Scaling
    - C. Target Tracking Scaling
    - D. Scheduled Scaling

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Target Tracking automatically calculates the scaling adjustments needed to keep the chosen metric at the desired target value.
    </details>

607. Which S3 storage class automatically optimizes costs by moving data between frequent and infrequent access tiers?
    - A. S3 Standard
    - B. S3 Standard-IA
    - C. S3 Intelligent-Tiering
    - D. S3 One Zone-IA

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Intelligent-Tiering monitors access patterns and moves objects automatically to the most cost-effective tier without performance impact.
    </details>

608. What is the primary purpose of an EBS Snapshot?
    - A. To increase volume performance.
    - B. To provide a point-in-time backup of an EBS volume stored in S3.
    - C. To encrypt an EBS volume.
    - D. To share a volume across multiple EC2 instances.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Snapshots are the mechanism for backing up EBS volumes and enabling volume restoration or creation.
    </details>

609. Which VPC component acts as a firewall at the subnet level?
    - A. Security Group
    - B. Route Table
    - C. Network Access Control List (NACL)
    - D. Internet Gateway

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: NACLs are associated with subnets and control inbound/outbound traffic for the entire subnet based on ordered rules.
    </details>

610. Which Route 53 routing policy would you use to route users to different endpoints based on their continent or country?
    - A. Latency Routing
    - B. Weighted Routing
    - C. Geolocation Routing
    - D. Failover Routing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Geolocation routing uses the geographic origin of the DNS query to determine the appropriate endpoint.
    </details>

611. Which AWS service provides a fully managed container orchestration service compatible with Kubernetes?
    - A. Amazon ECS
    - B. Amazon EKS
    - C. AWS Fargate
    - D. Amazon ECR

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: EKS is the AWS managed service for running Kubernetes.
    </details>

612. Which AWS service provides a serverless compute engine for containers, eliminating the need to manage EC2 instances?
    - A. Amazon ECS (EC2 Launch Type)
    - B. Amazon EKS (Managed Node Groups)
    - C. AWS Fargate
    - D. AWS Lambda

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Fargate allows you to run ECS or EKS containers without managing the underlying server infrastructure.
    </details>

613. Which AWS service provides a managed source control repository using Git?
    - A. AWS CodeBuild
    - B. AWS CodeDeploy
    - C. AWS CodeCommit
    - D. AWS CodePipeline

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CodeCommit is AWS\s managed Git repository service.
    </details>

614. Which AWS service orchestrates the build, test, and deploy phases of a software release process?
    - A. AWS CodeCommit
    - B. AWS CodeBuild
    - C. AWS CodeDeploy
    - D. AWS CodePipeline

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: CodePipeline models and automates the workflow of your release process.
    </details>

615. Which AWS service provides a fully managed message queuing service?
    - A. Amazon SNS
    - B. Amazon SQS
    - C. Amazon MQ
    - D. Amazon Kinesis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SQS is a highly scalable, managed queue service for decoupling application components.
    </details>

616. Which AWS service provides a managed publish/subscribe (pub/sub) messaging service?
    - A. Amazon SQS
    - B. Amazon SNS
    - C. Amazon MQ
    - D. AWS Step Functions

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SNS allows applications to send messages to multiple subscribers (like SQS queues, Lambda functions, HTTP endpoints) through topics.
    </details>

617. Which AWS service provides monitoring for AWS resources and applications, collecting metrics, logs, and events?
    - A. AWS CloudTrail
    - B. AWS Config
    - C. Amazon CloudWatch
    - D. AWS X-Ray

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudWatch is the central monitoring and observability service in AWS.
    </details>

618. Which AWS service records API calls made within your AWS account for auditing and compliance?
    - A. Amazon CloudWatch
    - B. AWS Config
    - C. AWS CloudTrail
    - D. Amazon GuardDuty

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudTrail logs user activity and API usage across AWS services.
    </details>

619. Which AWS service allows you to assess, audit, and evaluate the configurations of your AWS resources?
    - A. AWS CloudTrail
    - B. AWS Config
    - C. Amazon Inspector
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Config continuously monitors resource configurations and can evaluate them against desired rules.
    </details>

620. Which AWS service provides a global content delivery network (CDN)?
    - A. Amazon Route 53
    - B. AWS Global Accelerator
    - C. Amazon CloudFront
    - D. Elastic Load Balancing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudFront caches content at edge locations worldwide to reduce latency for end-users.
    </details>

621. Which AWS service helps migrate databases to AWS with minimal downtime?
    - A. AWS Schema Conversion Tool (SCT)
    - B. AWS Server Migration Service (SMS)
    - C. AWS Database Migration Service (DMS)
    - D. AWS Migration Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: DMS facilitates the replication and migration of databases to AWS.
    </details>

622. Which AWS service provides managed relational databases like MySQL, PostgreSQL, etc.?
    - A. Amazon DynamoDB
    - B. Amazon Redshift
    - C. Amazon RDS
    - D. Amazon ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: RDS simplifies the management of common relational database engines in the cloud.
    </details>

623. Which AWS service provides a managed NoSQL key-value database?
    - A. Amazon RDS
    - B. Amazon Aurora
    - C. Amazon DynamoDB
    - D. Amazon DocumentDB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: DynamoDB is AWS\s highly scalable, serverless NoSQL key-value and document database.
    </details>

624. Which AWS service provides a managed data warehouse solution?
    - A. Amazon RDS
    - B. Amazon DynamoDB
    - C. Amazon Redshift
    - D. Amazon EMR

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Redshift is optimized for large-scale data warehousing and analytics.
    </details>

625. Which AWS service provides managed in-memory caching using Redis or Memcached?
    - A. Amazon RDS
    - B. Amazon DynamoDB Accelerator (DAX)
    - C. Amazon ElastiCache
    - D. Amazon MemoryDB for Redis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: ElastiCache provides managed Redis and Memcached clusters for caching purposes.
    </details>

626. Which AWS service allows you to run code without provisioning servers, triggered by events?
    - A. Amazon EC2
    - B. AWS Fargate
    - C. AWS Lambda
    - D. Amazon ECS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Lambda is the core serverless compute service in AWS.
    </details>

627. Which AWS service acts as an API front-end for backend services like Lambda?
    - A. Elastic Load Balancing
    - B. Amazon CloudFront
    - C. Amazon API Gateway
    - D. AWS AppSync

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: API Gateway manages API creation, security, monitoring, and routing to backend resources.
    </details>

628. Which AWS service provides a simple way to deploy containerized web applications from source code or images?
    - A. AWS Elastic Beanstalk
    - B. AWS App Runner
    - C. Amazon ECS
    - D. Amazon EKS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: App Runner offers a highly simplified experience for deploying and running containerized web apps.
    </details>

629. Which AWS service provides a platform-as-a-service (PaaS) environment for deploying and scaling web applications and services developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker?
    - A. AWS Lambda
    - B. AWS App Runner
    - C. AWS Elastic Beanstalk
    - D. Amazon EC2

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Elastic Beanstalk automates the deployment, capacity provisioning, load balancing, auto-scaling, and health monitoring of applications.
    </details>

630. Which AWS service provides scalable, elastic file storage for use with Linux-based workloads (EC2, ECS, EKS)?
    - A. Amazon S3
    - B. Amazon EBS
    - C. Amazon EFS
    - D. Amazon FSx for Windows File Server

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EFS provides a standard NFS interface and can be mounted by multiple instances concurrently.
    </details>

631. Which AWS service provides block storage volumes attachable to EC2 instances?
    - A. Amazon S3
    - B. Amazon EFS
    - C. Amazon EBS
    - D. Amazon Glacier

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EBS provides persistent block storage analogous to local hard drives for EC2 instances.
    </details>

632. Which AWS service provides low-cost, durable object storage for data archiving?
    - A. Amazon S3 Standard
    - B. Amazon EBS
    - C. Amazon EFS
    - D. Amazon S3 Glacier storage classes

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: S3 Glacier, Glacier Flexible Retrieval, and Glacier Deep Archive are designed for long-term, low-cost archival storage.
    </details>

633. Which AWS service provides a managed graph database?
    - A. Amazon RDS
    - B. Amazon DynamoDB
    - C. Amazon Neptune
    - D. Amazon DocumentDB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Neptune is optimized for querying highly connected datasets typical of graph use cases.
    </details>

634. Which AWS service provides a managed document database with MongoDB compatibility?
    - A. Amazon DynamoDB
    - B. Amazon RDS
    - C. Amazon Neptune
    - D. Amazon DocumentDB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: DocumentDB offers MongoDB compatibility with the benefits of a managed AWS service.
    </details>

635. Which AWS service provides a managed ledger database with an immutable, verifiable transaction log?
    - A. Amazon Neptune
    - B. Amazon Managed Blockchain
    - C. Amazon QLDB
    - D. Amazon Timestream

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: QLDB is designed for systems of record requiring verifiable data lineage.
    </details>

636. Which AWS service provides a managed time-series database?
    - A. Amazon QLDB
    - B. Amazon Neptune
    - C. Amazon Timestream
    - D. Amazon DynamoDB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Timestream is optimized for ingesting and querying time-stamped data like IoT or log data.
    </details>

637. Which AWS service provides user sign-up, sign-in, and access control for web/mobile apps?
    - A. AWS IAM
    - B. AWS Directory Service
    - C. Amazon Cognito
    - D. AWS IAM Identity Center

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Cognito is the AWS service for customer identity and access management (CIAM).
    </details>

638. Which AWS service provides managed Active Directory services in the cloud?
    - A. Amazon Cognito
    - B. AWS IAM
    - C. AWS Directory Service
    - D. AWS Organizations

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Directory Service offers options like Managed Microsoft AD and AD Connector.
    </details>

639. Which AWS service simplifies SSO access to multiple AWS accounts and business applications?
    - A. Amazon Cognito
    - B. AWS Directory Service
    - C. AWS IAM Identity Center
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: IAM Identity Center (formerly AWS SSO) provides a central portal for managing user access across accounts and applications.
    </details>

640. Which AWS service allows secure sharing of resources (like subnets) across AWS accounts?
    - A. AWS Organizations
    - B. VPC Peering
    - C. AWS Resource Access Manager (RAM)
    - D. AWS Service Catalog

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: RAM facilitates controlled resource sharing, reducing duplication and operational overhead.
    </details>

641. Which AWS service manages SSL/TLS certificates for use with services like ELB and CloudFront?
    - A. AWS Secrets Manager
    - B. AWS KMS
    - C. AWS Certificate Manager (ACM)
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: ACM handles the provisioning, management, and deployment of certificates, including auto-renewal for public certs.
    </details>

642. Which AWS service provides managed virtual desktops (DaaS)?
    - A. Amazon AppStream 2.0
    - B. Amazon WorkSpaces
    - C. Amazon EC2
    - D. AWS Lambda

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: WorkSpaces provides persistent cloud-based desktops.
    </details>

643. Which AWS service streams desktop applications to users via a browser?
    - A. Amazon WorkSpaces
    - B. Amazon AppStream 2.0
    - C. AWS Client VPN
    - D. Amazon EC2

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AppStream 2.0 allows users to access desktop applications from any device without installation.
    </details>

644. Which AWS service provides a managed container registry?
    - A. Amazon ECS
    - B. Amazon EKS
    - C. Amazon ECR
    - D. Docker Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: ECR is AWS\s managed Docker container image registry.
    </details>

645. Which AWS service provides a cloud-based IDE?
    - A. AWS CodeCommit
    - B. AWS CodeBuild
    - C. AWS Cloud9
    - D. AWS CloudShell

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Cloud9 offers a development environment accessible through a web browser.
    </details>

646. Which AWS service helps trace and debug distributed applications?
    - A. Amazon CloudWatch
    - B. AWS CloudTrail
    - C. AWS X-Ray
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: X-Ray provides request tracing and service map visualization for identifying performance bottlenecks.
    </details>

647. Which AWS service provides a managed message broker for ActiveMQ or RabbitMQ?
    - A. Amazon SQS
    - B. Amazon SNS
    - C. Amazon MQ
    - D. Amazon Kinesis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: MQ is designed for migrating applications using standard messaging protocols like JMS, AMQP, etc.
    </details>

648. Which AWS service helps coordinate components of distributed applications using visual workflows?
    - A. AWS Lambda
    - B. AWS Step Functions
    - C. AWS SWF
    - D. AWS Batch

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Step Functions allows you to build state machines to orchestrate serverless workflows.
    </details>

649. Which AWS service provides a serverless interactive query service for data in S3?
    - A. Amazon Redshift
    - B. Amazon EMR
    - C. Amazon Athena
    - D. Amazon QuickSight

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Athena allows querying S3 data directly using standard SQL without managing infrastructure.
    </details>

650. Which AWS service provides a cloud-powered Business Intelligence (BI) service?
    - A. Amazon Athena
    - B. Amazon Redshift
    - C. Amazon QuickSight
    - D. AWS Glue

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: QuickSight enables creation and sharing of interactive dashboards and visualizations.
    </details>

