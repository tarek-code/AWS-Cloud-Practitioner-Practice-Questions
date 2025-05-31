# AWS Cloud Practitioner Practice Questions - Batch 5 (EC2 Storage, ELB, ASG)

101. What is Amazon Elastic Block Store (EBS)?
    - A. A file storage service accessible via NFS.
    - B. An object storage service for the internet.
    - C. A network-attached block storage volume that can be attached to EC2 instances.
    - D. A temporary storage volume physically attached to the host computer.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EBS provides persistent block-level storage volumes for use with Amazon EC2 instances. They are network-attached and persist independently from the life of an instance.
    </details>

102. Which statement accurately describes the relationship between EBS volumes and Availability Zones (AZs)?
    - A. EBS volumes are global resources, accessible from any AZ.
    - B. EBS volumes are regional resources, accessible from any AZ within the Region.
    - C. EBS volumes are created within a specific AZ and can only be attached to instances in that same AZ.
    - D. EBS volumes can be attached to instances across multiple AZs simultaneously.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EBS volumes are zonal resources. They are created in a specific Availability Zone and can only be attached to EC2 instances running within that same AZ.
    </details>

103. What is the primary use case for EC2 Instance Store compared to EBS?
    - A. Long-term persistent data storage.
    - B. Storing operating system boot volumes.
    - C. High-performance temporary storage for caches, buffers, or scratch data.
    - D. Shared file storage accessible by multiple instances.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EC2 Instance Store provides high I/O performance, temporary block-level storage located on disks physically attached to the host computer. It is ideal for temporary data that requires very low latency, but the data is lost if the instance stops or terminates.
    </details>

104. What feature allows you to create backups of EBS volumes?
    - A. EBS Replication
    - B. EBS Snapshots
    - C. EBS Archiving
    - D. EBS Mirroring

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: EBS Snapshots are point-in-time backups of EBS volumes stored durably in Amazon S3. They can be used to restore volumes or create new volumes.
    </details>

105. Can you create an AMI (Amazon Machine Image) directly from an EBS Snapshot?
    - A. No, AMIs can only be created from running instances.
    - B. No, AMIs are independent of EBS snapshots.
    - C. Yes, you can register an EBS snapshot as a new AMI.
    - D. Yes, but only for Linux instances.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: You can create an AMI from an EBS snapshot, typically a snapshot of a root device volume. This allows you to launch new EC2 instances based on that snapshot.
    </details>

106. What is the default behavior of the root EBS volume when its associated EC2 instance is terminated?
    - A. The volume is detached and becomes available for attachment to another instance.
    - B. The volume is automatically snapshotted before deletion.
    - C. The volume is deleted.
    - D. The volume persists indefinitely unless manually deleted.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: By default, the "Delete on Termination" attribute is enabled for the root EBS volume, meaning it will be deleted when the instance terminates. This behavior can be changed at launch or later.
    </details>

107. What is Elastic Load Balancing (ELB)?
    - A. A service that automatically adjusts EC2 instance capacity.
    - B. A service that distributes incoming application traffic across multiple targets, such as EC2 instances.
    - C. A service that provides dedicated network connections.
    - D. A service that manages DNS records.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Elastic Load Balancing automatically distributes incoming application traffic across multiple targets (like EC2 instances, containers, IP addresses) in one or more Availability Zones, increasing application fault tolerance and availability.
    </details>

108. Which type of Elastic Load Balancer is best suited for load balancing HTTP and HTTPS traffic at the request level (Layer 7)?
    - A. Network Load Balancer (NLB)
    - B. Classic Load Balancer (CLB)
    - C. Gateway Load Balancer (GWLB)
    - D. Application Load Balancer (ALB)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Application Load Balancer operates at the request level (Layer 7), routing traffic based on content like host headers or URL paths, making it ideal for modern microservices and container-based applications handling HTTP/HTTPS traffic.
    </details>

109. Which type of Elastic Load Balancer operates at the connection level (Layer 4) and is capable of handling millions of requests per second with ultra-low latency?
    - A. Application Load Balancer (ALB)
    - B. Network Load Balancer (NLB)
    - C. Classic Load Balancer (CLB)
    - D. Gateway Load Balancer (GWLB)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Network Load Balancer operates at the connection level (Layer 4), routing TCP, UDP, and TLS traffic. It offers high performance, static IP addresses per AZ, and is optimized for volatile traffic patterns.
    </details>

110. What is the primary function of an Auto Scaling Group (ASG)?
    - A. To distribute traffic evenly across instances.
    - B. To automatically adjust the number of EC2 instances in a group based on demand or a schedule.
    - C. To provide persistent block storage for instances.
    - D. To manage firewall rules for a group of instances.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: An Auto Scaling Group helps ensure you have the correct number of EC2 instances available to handle the load for your application. It allows you to scale out (add instances) or scale in (remove instances) automatically based on defined conditions (scaling policies) or on a schedule.
    </details>

111. What components are typically defined within an Auto Scaling Group configuration? (Choose THREE)
    - A. Launch Template or Launch Configuration (specifying instance details like AMI, instance type).
    - B. Minimum, Maximum, and Desired number of instances.
    - C. Scaling Policies (how to scale in/out).
    - D. IAM User credentials.
    - E. S3 Bucket name for logs.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A, B, C
      Explanation: Key components of an ASG include a Launch Template/Configuration (defining what instances to launch), size parameters (Min/Max/Desired capacity), and Scaling Policies (defining when and how to adjust the number of instances).
    </details>

112. How does Elastic Load Balancing contribute to high availability?
    - A. By automatically patching the operating systems of instances.
    - B. By distributing traffic across instances in multiple Availability Zones.
    - C. By encrypting data stored on EBS volumes.
    - D. By providing static IP addresses.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: ELB enhances availability by routing traffic away from unhealthy instances and distributing the load across healthy instances spread across multiple Availability Zones. If one AZ fails, traffic is directed to instances in other AZs.
    </details>

113. What mechanism does ELB use to determine if a registered target (e.g., EC2 instance) is available to handle requests?
    - A. IAM Policies
    - B. Security Group rules
    - C. Health Checks
    - D. CloudWatch Alarms

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Load balancers periodically send requests (health checks) to their registered targets to test their status. If a target fails consecutive health checks, the load balancer stops sending traffic to it.
    </details>

114. Which scaling policy type for an Auto Scaling Group adjusts the capacity based on a CloudWatch alarm?
    - A. Scheduled Scaling
    - B. Manual Scaling
    - C. Dynamic Scaling (e.g., Target Tracking, Step Scaling)
    - D. Predictive Scaling

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Dynamic Scaling policies adjust the number of instances in response to changing demand, typically triggered by CloudWatch metrics exceeding a defined threshold (e.g., average CPU utilization).
    </details>

115. What is the benefit of using a Launch Template compared to a Launch Configuration with Auto Scaling Groups?
    - A. Launch Configurations support more instance types.
    - B. Launch Templates allow versioning and support newer EC2 features (like Spot allocation strategies, T2/T3 Unlimited).
    - C. Launch Configurations are required for Application Load Balancers.
    - D. Launch Templates are automatically deleted when the ASG is deleted.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Launch Templates are recommended over Launch Configurations as they provide versioning capabilities, allow modification after creation, and support a wider range of newer EC2 features and purchasing options.
    </details>

116. Can an EBS volume be detached from one EC2 instance and attached to another?
    - A. No, EBS volumes are permanently tied to the instance they were launched with.
    - B. Yes, but only if both instances are in the same Region.
    - C. Yes, but only if both instances are in the same Availability Zone.
    - D. Yes, but only after creating a snapshot and restoring it.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: An EBS volume can be detached from one instance and attached to another, provided both instances reside within the same Availability Zone.
    </details>

117. What is the purpose of the "Desired Capacity" setting in an Auto Scaling Group?
    - A. The maximum number of instances the ASG can launch.
    - B. The minimum number of instances the ASG must maintain.
    - C. The number of instances the ASG attempts to maintain at all times.
    - D. The number of instances currently passing health checks.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Desired Capacity is the number of instances the Auto Scaling group tries to maintain. It will launch or terminate instances to reach and maintain this number, staying within the Min and Max size limits.
    </details>

118. Which AWS service provides a managed Network File System (NFS) that can be mounted concurrently by multiple EC2 instances across different Availability Zones within a Region?
    - A. Amazon EBS
    - B. Amazon S3
    - C. Amazon EFS (Elastic File System)
    - D. EC2 Instance Store

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon EFS provides scalable, elastic, cloud-native NFS file storage designed for Linux-based workloads. It can be accessed concurrently by thousands of EC2 instances within a Region, across multiple AZs.
    </details>

119. If an Auto Scaling Group is configured with a Minimum size of 2, a Maximum size of 6, and a Desired Capacity of 3, what happens if one of the three running instances fails its health check?
    - A. The ASG terminates the unhealthy instance and launches a new one to maintain the Desired Capacity of 3.
    - B. The ASG terminates the unhealthy instance, reducing the count to 2 (the Minimum size).
    - C. The ASG launches three new instances to reach the Maximum size of 6.
    - D. The ASG does nothing until manually intervened.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: The ASG automatically detects the unhealthy instance (often via ELB health checks or EC2 status checks), terminates it, and launches a replacement instance to return to the Desired Capacity of 3.
    </details>

120. What is the primary benefit of using EBS Snapshots for disaster recovery?
    - A. Snapshots automatically encrypt data.
    - B. Snapshots can be copied to other AWS Regions, allowing you to restore volumes and launch instances in a different Region if needed.
    - C. Snapshots reduce the cost of EBS volumes.
    - D. Snapshots improve the performance of EBS volumes.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: EBS snapshots can be copied across Regions. This enables disaster recovery strategies where you can recreate your EBS volumes (and the instances they attach to) in a different geographical location if your primary Region becomes unavailable.
    </details>

121. Which Elastic Load Balancer type should you use if you need to expose a fleet of third-party security virtual appliances (e.g., firewalls, IDS/IPS) for inspection of VPC traffic?
    - A. Application Load Balancer (ALB)
    - B. Network Load Balancer (NLB)
    - C. Classic Load Balancer (CLB)
    - D. Gateway Load Balancer (GWLB)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Gateway Load Balancer is designed specifically to deploy, scale, and manage third-party virtual network appliances. It acts as a transparent bump-in-the-wire, routing traffic through the appliances for inspection.
    </details>

122. What happens to data on an EBS volume when the attached EC2 instance is terminated, assuming the "Delete on Termination" flag is NOT set for that volume?
    - A. The EBS volume is automatically deleted.
    - B. The data on the EBS volume is lost.
    - C. The EBS volume persists and can be attached to another EC2 instance later.
    - D. The EBS volume is converted into an Instance Store volume.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: If the "Delete on Termination" flag is disabled (which is the default for non-root volumes), the EBS volume persists even after the instance it was attached to is terminated. It remains available in the AZ and can be attached to a new instance.
    </details>

123. An Auto Scaling group needs to increase capacity every Friday evening at 6 PM and decrease capacity every Monday morning at 8 AM. Which type of scaling policy is most appropriate?
    - A. Target Tracking Scaling
    - B. Step Scaling
    - C. Simple Scaling
    - D. Scheduled Scaling

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Scheduled Scaling allows you to configure specific times and dates for the Auto Scaling group to automatically increase or decrease the number of instances, which is ideal for predictable load changes based on time.
    </details>

124. What is the key difference between EBS (Elastic Block Store) and EFS (Elastic File System)?
    - A. EBS provides object storage, while EFS provides block storage.
    - B. EBS volumes can only be attached to one instance at a time (in an AZ), while EFS file systems can be mounted by many instances concurrently (across AZs).
    - C. EFS is cheaper than EBS for all use cases.
    - D. EBS is designed for Linux only, while EFS supports Windows and Linux.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: EBS provides block storage attached to a single EC2 instance within a specific AZ. EFS provides a shared NFS file system that can be accessed concurrently by thousands of Linux instances across multiple AZs within a Region.
    </details>

125. How can combining Elastic Load Balancing and Auto Scaling Groups improve application architecture?
    - A. By eliminating the need for security groups.
    - B. By providing a highly available, fault-tolerant, and scalable application deployment.
    - C. By reducing the cost of EBS snapshots.
    - D. By simplifying IAM policy management.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: ELB distributes traffic across healthy instances in multiple AZs (providing availability and fault tolerance), while ASG automatically adjusts the number of instances based on load (providing scalability and elasticity). Together, they form the foundation for robust web application architectures on AWS.
    </details>

