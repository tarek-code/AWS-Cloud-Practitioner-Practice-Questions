# AWS Cloud Practitioner Practice Questions - Batch 4 (EC2)

76. What does EC2 stand for in AWS?
    - A. Elastic Compute Cache
    - B. Elastic Container Cloud
    - C. Elastic Compute Cloud
    - D. Encrypted Compute Cloud

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EC2 stands for Elastic Compute Cloud. It provides scalable virtual servers (instances) in the AWS cloud.
    </details>

77. Which AWS service category does Amazon EC2 primarily fall under?
    - A. Software as a Service (SaaS)
    - B. Platform as a Service (PaaS)
    - C. Infrastructure as a Service (IaaS)
    - D. Function as a Service (FaaS)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon EC2 provides fundamental compute infrastructure (virtual machines, storage, networking) and is a core example of IaaS, giving users control over the operating system and compute environment.
    </details>

78. What components do you typically configure when launching an EC2 instance? (Choose THREE)
    - A. Amazon Machine Image (AMI)
    - B. Instance Type (CPU, RAM)
    - C. Security Group (Firewall rules)
    - D. Database Schema
    - E. S3 Bucket Policy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A, B, C
      Explanation: Key configuration options when launching an EC2 instance include selecting an AMI (operating system and pre-installed software), choosing an Instance Type (determining CPU, memory, storage, and network capacity), and assigning Security Groups (defining firewall rules).
    </details>

79. What is an Amazon Machine Image (AMI)?
    - A. A snapshot of an EBS volume.
    - B. A template containing the software configuration (OS, application server, applications) required to launch an EC2 instance.
    - C. A type of network interface.
    - D. A container image format.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: An AMI provides the information required to launch an instance. It includes a template for the root volume (e.g., OS, application server), launch permissions, and block device mappings.
    </details>

80. What determines the CPU, memory, storage, and networking capacity of an EC2 instance?
    - A. The selected AMI.
    - B. The Security Group rules.
    - C. The Instance Type.
    - D. The EC2 User Data script.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Instance Type (e.g., t2.micro, m5.large, c5.2xlarge) defines the hardware specifications allocated to the virtual server, including vCPUs, memory, storage type/size (for instance store), and network performance.
    </details>

81. What is the purpose of EC2 User Data?
    - A. To store persistent application data.
    - B. To define firewall rules for the instance.
    - C. To provide a script that runs automatically when an instance is first launched, typically for bootstrapping (installing software, updates, etc.).
    - D. To assign an IAM role to the instance.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EC2 User Data allows you to pass a script (e.g., shell script, cloud-init directives) to an instance at launch time. This script runs automatically on the first boot and is commonly used for initial configuration and software installation.
    </details>

82. Which EC2 instance family is optimized for compute-intensive workloads requiring high-performance processors?
    - A. General Purpose (e.g., M5, T3)
    - B. Memory Optimized (e.g., R5, X1)
    - C. Storage Optimized (e.g., I3, D2)
    - D. Compute Optimized (e.g., C5, C6g)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Compute Optimized instances (like the C family) are designed for applications that benefit from high compute power, such as batch processing, media transcoding, high-performance web servers, and scientific modeling.
    </details>

83. A company needs to run a large in-memory database on EC2. Which instance family would be most suitable?
    - A. Compute Optimized (C family)
    - B. General Purpose (T family)
    - C. Memory Optimized (R, X, or z1d families)
    - D. Storage Optimized (I family)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Memory Optimized instances are designed to deliver fast performance for workloads that process large datasets in memory, making them ideal for relational/non-relational databases, in-memory caches, and real-time big data analytics.
    </details>

84. What is the function of a Security Group in the context of EC2?
    - A. It defines IAM permissions for the instance.
    - B. It acts as a virtual firewall, controlling inbound and outbound traffic to the EC2 instance.
    - C. It specifies the physical location of the instance.
    - D. It encrypts the instance's root volume.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Security Groups act as stateful firewalls at the instance level. They control traffic based on protocol, port number, and source/destination IP address (or other security groups).
    </details>

85. By default, what traffic is allowed by a newly created Security Group?
    - A. All inbound traffic is allowed, all outbound traffic is denied.
    - B. All inbound traffic is denied, all outbound traffic is allowed.
    - C. All inbound and outbound traffic is allowed.
    - D. All inbound and outbound traffic is denied.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: By default, a new security group denies all inbound traffic and allows all outbound traffic. You must explicitly add inbound rules to allow traffic to reach your instance.
    </details>

86. Which port number needs to be allowed in a Security Group to connect to a Linux EC2 instance using SSH?
    - A. 80 (HTTP)
    - B. 443 (HTTPS)
    - C. 3389 (RDP)
    - D. 22 (SSH)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Secure Shell (SSH) protocol, used for command-line access to Linux instances, typically operates on TCP port 22.
    </details>

87. Which port number is typically used for accessing Windows EC2 instances via Remote Desktop Protocol (RDP)?
    - A. 22 (SSH)
    - B. 80 (HTTP)
    - C. 443 (HTTPS)
    - D. 3389 (RDP)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Remote Desktop Protocol (RDP), used for graphical remote access to Windows instances, typically operates on TCP port 3389.
    </details>

88. Which EC2 purchasing option offers the most significant potential discount (up to 90%) but comes with the risk that instances can be terminated by AWS with short notice?
    - A. On-Demand Instances
    - B. Reserved Instances
    - C. Spot Instances
    - D. Dedicated Hosts

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Spot Instances leverage unused EC2 capacity and offer the largest discounts. However, they can be interrupted by AWS if the capacity is needed elsewhere or if the Spot price exceeds your maximum bid.
    </details>

89. A company has a predictable, long-term workload running on EC2 and wants to achieve significant cost savings compared to On-Demand pricing by committing to 1 or 3 years of usage. Which purchasing options should they consider? (Choose TWO)
    - A. Spot Instances
    - B. Reserved Instances (Standard or Convertible)
    - C. On-Demand Instances
    - D. Savings Plans (EC2 Instance or Compute)
    - E. Dedicated Instances

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B, D
      Explanation: Both Reserved Instances (RIs) and Savings Plans offer significant discounts (up to 72%) over On-Demand pricing in exchange for a 1-year or 3-year usage commitment. They are ideal for steady-state workloads.
    </details>

90. What is the key difference between Standard Reserved Instances and Convertible Reserved Instances?
    - A. Standard RIs offer a larger discount than Convertible RIs.
    - B. Convertible RIs allow changing instance attributes (like family, OS, tenancy) during the term, while Standard RIs do not.
    - C. Standard RIs can be sold on the RI Marketplace, while Convertible RIs cannot.
    - D. Convertible RIs require an All Upfront payment, while Standard RIs offer flexible payment options.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Convertible RIs provide flexibility to change instance attributes during the term, albeit with a slightly lower discount compared to Standard RIs which lock you into specific attributes.
    </details>

91. Which EC2 purchasing option provides a physical server fully dedicated to your use, often for compliance or licensing reasons?
    - A. Spot Instances
    - B. Dedicated Instances
    - C. Dedicated Hosts
    - D. Reserved Instances

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Dedicated Hosts provide you with physical servers dedicated for your use, giving you the most control over instance placement and visibility into the underlying hardware, often required for specific licensing (BYOL) or compliance needs.
    </details>

92. What is the difference between Dedicated Instances and Dedicated Hosts?
    - A. Dedicated Instances run on hardware dedicated to a single customer account, while Dedicated Hosts provide an entire physical server.
    - B. Dedicated Hosts are cheaper than Dedicated Instances.
    - C. Dedicated Instances offer per-second billing, while Dedicated Hosts offer per-hour billing.
    - D. There is no difference; the terms are interchangeable.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: Dedicated Instances run on hardware dedicated to your account, but you don't control instance placement and might share the hardware with other instances from your account. Dedicated Hosts give you an entire physical server and control over instance placement.
    </details>

93. Which EC2 purchasing option allows you to reserve capacity in a specific Availability Zone for any duration without receiving a discount, ensuring you can launch On-Demand instances when needed?
    - A. Zonal Reserved Instances
    - B. EC2 Capacity Reservations
    - C. Regional Reserved Instances
    - D. Spot Fleet

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: EC2 Capacity Reservations allow you to reserve compute capacity for your EC2 instances in a specific AZ for any duration. You pay the On-Demand rate whether you run instances or not, but it guarantees capacity availability.
    </details>

94. Under the Shared Responsibility Model for EC2, what is the customer responsible for? (Choose TWO)
    - A. Managing the physical hardware hosting the EC2 instances.
    - B. Patching the guest operating system and installing applications on the instance.
    - C. Configuring Security Groups and Network ACLs.
    - D. Maintaining the virtualization infrastructure (hypervisor).
    - E. Ensuring power and cooling in the data center.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B, C
      Explanation: The customer is responsible for security IN the cloud, which for EC2 includes managing the guest OS (patching, updates), applications installed, configuring firewalls (Security Groups, NACLs), and managing data security and IAM permissions.
    </details>

95. What is EC2 Instance Connect?
    - A. A way to establish a dedicated network connection to AWS.
    - B. A method to connect securely to your Linux instances via SSH directly from the AWS Management Console or CLI without managing SSH keys.
    - C. A tool for monitoring EC2 instance performance.
    - D. A type of load balancer.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: EC2 Instance Connect provides a simple and secure way to connect to your Linux instances using SSH. It uses IAM policies for access control and pushes a temporary SSH key to the instance, removing the need for users to manage their own keys.
    </details>

96. If you stop and then start an EC2 instance, what might change?
    - A. The Availability Zone it is running in.
    - B. The underlying physical host it is running on.
    - C. The data stored on its attached EBS volumes.
    - D. The instance ID.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: When you stop and start an instance (unless it's on a Dedicated Host), it may be migrated to different underlying physical hardware. The instance ID, EBS volume data, and Availability Zone remain the same. The public IPv4 address will likely change unless an Elastic IP is used.
    </details>

97. What happens to data stored on an EC2 Instance Store volume if the instance is stopped or terminated?
    - A. The data is automatically backed up to S3.
    - B. The data persists until the volume is manually deleted.
    - C. The data is lost.
    - D. The data is moved to an EBS volume.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EC2 Instance Store provides temporary, block-level storage located on disks physically attached to the host computer. Data on instance store volumes is ephemeral and is lost if the instance is stopped, hibernated, or terminated.
    </details>

98. Which AWS service allows you to automate the creation, maintenance, validation, and testing of EC2 AMIs?
    - A. AWS CloudFormation
    - B. AWS Systems Manager
    - C. EC2 Image Builder
    - D. AWS CodeDeploy

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EC2 Image Builder simplifies the building, testing, and deployment of Virtual Machine and container images for use with AWS or on-premises environments.
    </details>

99. You need to launch a Windows Server instance on EC2. Which AMI source would you typically use?
    - A. An AMI you created from a Linux instance.
    - B. A public AMI provided by AWS specifically for Windows Server.
    - C. An AWS Marketplace AMI for a specialized Linux distribution.
    - D. An AMI from a different AWS Region.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS provides official, public AMIs for various operating systems, including different versions of Windows Server, which are the standard starting point for launching Windows instances.
    </details>

100. As of February 2024, what change did AWS implement regarding public IPv4 addresses for EC2 instances?
    - A. Public IPv4 addresses became free for all instances.
    - B. AWS stopped assigning public IPv4 addresses.
    - C. AWS started charging for all public IPv4 addresses associated with instances (with a free tier for new accounts).
    - D. Public IPv4 addresses were replaced entirely by IPv6.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Starting February 1, 2024, AWS began charging for all public IPv4 addresses, whether attached to a service or idle. There is a free tier allocation for EC2 public IPv4 usage for the first 12 months for new AWS accounts.
    </details>

