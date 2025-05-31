# AWS Cloud Practitioner Practice Questions - Batch 6 (S3)

126. What type of storage does Amazon S3 provide?
    - A. Block storage
    - B. File storage (NFS/SMB)
    - C. Object storage
    - D. In-memory cache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon S3 (Simple Storage Service) is a scalable object storage service designed for durability, availability, and performance. Data is stored as objects within containers called buckets.
    </details>

127. What is the fundamental storage unit in Amazon S3?
    - A. Volume
    - B. File System
    - C. Bucket
    - D. Object

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Data in S3 is stored as objects. An object consists of data (the file itself), metadata (descriptive information), and a globally unique key (name).
    </details>

128. What is an S3 Bucket?
    - A. A virtual server for storing objects.
    - B. A container for storing objects in S3.
    - C. A type of database table.
    - D. A network drive attached to an EC2 instance.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: An S3 bucket is a container used to store objects. Bucket names must be globally unique across all AWS accounts.
    </details>

129. What is the maximum size of a single object that can be uploaded to S3?
    - A. 1 GB
    - B. 100 GB
    - C. 1 TB
    - D. 5 TB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: The total volume of data and number of objects you can store are unlimited, but the maximum size for a single S3 object is 5 Terabytes (TB).
    </details>

130. Which S3 storage class is designed for frequently accessed data requiring low latency and high throughput?
    - A. S3 Standard-Infrequent Access (S3 Standard-IA)
    - B. S3 One Zone-Infrequent Access (S3 One Zone-IA)
    - C. S3 Standard
    - D. S3 Glacier Flexible Retrieval

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Standard is the default storage class, offering high durability, availability, and performance object storage for frequently accessed data. It delivers low latency and high throughput.
    </details>

131. Which S3 storage class offers the high durability of S3 Standard but with a lower storage price and a retrieval fee, suitable for long-lived, less frequently accessed data?
    - A. S3 Standard
    - B. S3 Standard-Infrequent Access (S3 Standard-IA)
    - C. S3 One Zone-Infrequent Access (S3 One Zone-IA)
    - D. S3 Glacier Instant Retrieval

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: S3 Standard-IA is optimized for data that is accessed less frequently but requires rapid access when needed. It offers the same high durability and low latency as S3 Standard but with a lower per-GB storage price and a per-GB retrieval fee.
    </details>

132. Which S3 storage class is similar to S3 Standard-IA but stores data in only a single Availability Zone, offering lower cost but less resilience?
    - A. S3 Standard
    - B. S3 Standard-Infrequent Access (S3 Standard-IA)
    - C. S3 One Zone-Infrequent Access (S3 One Zone-IA)
    - D. S3 Intelligent-Tiering

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 One Zone-IA stores data in a single AZ and is ideal for less frequently accessed data that does not require the multi-AZ resilience of S3 Standard or S3 Standard-IA, offering a lower storage cost than S3 Standard-IA.
    </details>

133. Which S3 storage class automatically moves data between frequent and infrequent access tiers based on changing access patterns, optimizing costs without performance impact?
    - A. S3 Standard
    - B. S3 Standard-IA
    - C. S3 Intelligent-Tiering
    - D. S3 Glacier Deep Archive

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Intelligent-Tiering is designed for data with unknown or changing access patterns. It automatically moves objects between a frequent access tier and an infrequent access tier (and optional archive tiers) to optimize storage costs.
    </details>

134. Which S3 storage classes are designed for long-term data archiving? (Choose TWO)
    - A. S3 Standard
    - B. S3 Glacier Flexible Retrieval
    - C. S3 One Zone-IA
    - D. S3 Glacier Deep Archive
    - E. S3 Intelligent-Tiering (Frequent Access Tier)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B, D
      Explanation: S3 Glacier Flexible Retrieval (formerly S3 Glacier) and S3 Glacier Deep Archive are secure, durable, and low-cost storage classes designed for data archiving. Deep Archive offers the lowest cost but with longer retrieval times (hours).
    </details>

135. What is the typical use case for S3 Glacier Deep Archive?
    - A. Hosting static websites.
    - B. Storing frequently accessed application logs.
    - C. Long-term retention (7-10+ years) of data that is rarely accessed, such as compliance archives or digital media preservation.
    - D. Caching frequently accessed data.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Glacier Deep Archive provides the lowest-cost object storage for long-term retention of data that might be accessed once or twice a year. It is suitable for highly regulated industry archives (financial, healthcare) or data that needs preservation but not frequent access.
    </details>

136. What feature allows you to automatically transition S3 objects between different storage classes based on age or other criteria?
    - A. S3 Versioning
    - B. S3 Bucket Policies
    - C. S3 Lifecycle Policies
    - D. S3 Cross-Region Replication

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Lifecycle policies allow you to define rules to automatically transition objects to other storage classes (e.g., move from Standard to Standard-IA after 30 days) or expire (delete) objects after a certain period.
    </details>

137. What is S3 Versioning?
    - A. A way to encrypt objects in S3.
    - B. A feature that keeps multiple variants of an object in the same bucket, protecting against accidental overwrites or deletions.
    - C. A method for distributing content globally.
    - D. A tool for analyzing S3 access patterns.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: S3 Versioning automatically keeps multiple versions of an object when it is overwritten or deleted. This allows you to retrieve previous versions and recover from unintended user actions or application failures.
    </details>

138. How can you control access to S3 buckets and objects? (Choose TWO)
    - A. Security Groups
    - B. Network ACLs
    - C. IAM Policies (User/Group/Role-based)
    - D. S3 Bucket Policies (Resource-based)
    - E. EC2 Key Pairs

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C, D
      Explanation: Access to S3 resources can be controlled using identity-based policies (IAM policies attached to users, groups, or roles) and resource-based policies (Bucket Policies attached directly to the bucket, and Access Control Lists - ACLs - on buckets/objects).
    </details>

139. What is the purpose of S3 Cross-Region Replication (CRR)?
    - A. To reduce storage costs.
    - B. To automatically copy objects from a bucket in one AWS Region to a bucket in a different Region.
    - C. To encrypt objects automatically.
    - D. To provide temporary storage for EC2 instances.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: CRR enables automatic, asynchronous copying of objects across buckets in different AWS Regions. It is often used for compliance, lower-latency access in different geographies, or as part of a disaster recovery strategy.
    </details>

140. Which S3 feature allows you to host a static website directly from an S3 bucket?
    - A. S3 Lifecycle Policies
    - B. S3 Static Website Hosting
    - C. S3 Versioning
    - D. S3 Transfer Acceleration

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: You can configure an S3 bucket to function as a web server for static content (HTML, CSS, JavaScript, images). This provides a low-cost, scalable solution for hosting static websites.
    </details>

141. What type of encryption does S3 offer to protect data at rest? (Choose TWO)
    - A. Client-Side Encryption (CSE)
    - B. Network-Level Encryption (IPsec)
    - C. Server-Side Encryption (SSE - S3, KMS, C)
    - D. Transport Layer Security (TLS/SSL)
    - E. File System Encryption (EFS Encryption)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A, C
      Explanation: S3 supports encrypting data before sending it (Client-Side Encryption) or having S3 encrypt it upon receipt (Server-Side Encryption). SSE has options managed by S3 (SSE-S3), managed by KMS (SSE-KMS), or using customer-provided keys (SSE-C).
    </details>

142. What is the primary benefit of using S3 Transfer Acceleration?
    - A. It reduces S3 storage costs.
    - B. It encrypts data in transit automatically.
    - C. It enables faster, easier, and more secure transfers of files over long distances between clients and an S3 bucket by using CloudFront Edge Locations.
    - D. It provides block-level storage access.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Transfer Acceleration leverages the globally distributed AWS Edge Locations (CloudFront network) to accelerate uploads and downloads to/from S3 buckets, especially beneficial for users geographically distant from the bucket's Region.
    </details>

143. Which S3 feature allows you to perform SQL-like queries directly on data stored in S3 objects (e.g., CSV, JSON, Parquet) without needing to load it into a database?
    - A. S3 Batch Operations
    - B. S3 Select / Glacier Select
    - C. S3 Inventory
    - D. S3 Analytics

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: S3 Select (and Glacier Select for archived objects) allows you to retrieve only a subset of data from an object using simple SQL expressions, significantly improving query performance and reducing data transfer costs compared to retrieving the entire object.
    </details>

144. What is the durability level designed for the S3 Standard storage class?
    - A. 99% (2 nines)
    - B. 99.9% (3 nines)
    - C. 99.99% (4 nines)
    - D. 99.999999999% (11 nines)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: S3 Standard, Standard-IA, One Zone-IA, Intelligent-Tiering, and Glacier storage classes are all designed for 99.999999999% (11 nines) of durability of objects over a given year. This means extremely low risk of data loss.
    </details>

145. You need to store data that is critical and frequently accessed, but you want to save costs compared to S3 Standard. The data can tolerate the loss of availability in a single Availability Zone. Which storage class is the most cost-effective choice?
    - A. S3 Standard
    - B. S3 Standard-IA
    - C. S3 One Zone-IA
    - D. S3 Glacier Flexible Retrieval

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 One Zone-IA offers a lower storage cost than S3 Standard-IA because it stores data in only one AZ. It's suitable for data that is regenerable or doesn't require the highest level of availability, but still needs frequent access performance when retrieved.
    </details>

146. What is the purpose of S3 Object Lock?
    - A. To encrypt objects using customer-provided keys.
    - B. To prevent objects from being deleted or overwritten for a fixed amount of time or indefinitely (Write-Once-Read-Many - WORM model).
    - C. To automatically move objects to cheaper storage tiers.
    - D. To accelerate object uploads.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: S3 Object Lock provides WORM storage capabilities, helping meet regulatory requirements for data retention or adding a layer of protection against accidental/malicious object changes or deletions.
    </details>

147. Which AWS service can be used in conjunction with S3 to serve static and dynamic content with low latency globally?
    - A. AWS Direct Connect
    - B. Amazon Route 53
    - C. Amazon CloudFront
    - D. Elastic Load Balancing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon CloudFront is AWS's Content Delivery Network (CDN). It can cache content from an S3 origin (and other origins) at Edge Locations worldwide, delivering it to users with low latency and high transfer speeds.
    </details>

148. By default, are newly created S3 buckets public or private?
    - A. Publicly readable
    - B. Publicly writable
    - C. Private (only accessible by the account owner/creator)
    - D. Accessible only by EC2 instances in the same Region

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: By default, all S3 buckets and objects are private. Only the resource owner (the AWS account that created the bucket) has access. Access must be explicitly granted via IAM policies, bucket policies, or ACLs.
    </details>

149. What S3 feature provides visibility into storage usage, access patterns, and helps identify data that could be moved to lower-cost storage classes?
    - A. S3 Versioning
    - B. S3 Storage Lens
    - C. S3 Replication Time Control (RTC)
    - D. S3 Object Lock

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: S3 Storage Lens provides organization-wide visibility into object storage usage and activity trends. It delivers interactive dashboards and metrics to help understand, analyze, and optimize S3 storage costs and apply data protection best practices.
    </details>

150. Which retrieval option for S3 Glacier Flexible Retrieval typically takes 3-5 hours?
    - A. Expedited
    - B. Standard
    - C. Bulk
    - D. Instant

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: S3 Glacier Flexible Retrieval offers three retrieval options: Expedited (1-5 minutes, higher cost), Standard (3-5 hours), and Bulk (5-12 hours, lowest cost). S3 Glacier Instant Retrieval provides millisecond access.
    </details>

