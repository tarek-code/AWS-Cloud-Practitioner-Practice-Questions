# AWS Cloud Practitioner Practice Questions - Batch 7 (Databases & Analytics)

151. Which AWS service provides managed relational databases, simplifying setup, operation, and scaling?
    - A. Amazon DynamoDB
    - B. Amazon Redshift
    - C. Amazon RDS (Relational Database Service)
    - D. Amazon ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon RDS is a managed service that makes it easier to set up, operate, and scale relational databases like MySQL, PostgreSQL, MariaDB, Oracle, and SQL Server in the cloud.
    </details>

152. Which AWS database service is a fully managed NoSQL key-value and document database known for single-digit millisecond performance at any scale?
    - A. Amazon RDS
    - B. Amazon Redshift
    - C. Amazon DynamoDB
    - D. Amazon Aurora

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon DynamoDB is a fully managed, serverless, key-value NoSQL database designed for high performance, scalability, and availability, suitable for applications needing consistent, low-latency data access.
    </details>

153. Which AWS service is a fast, fully managed, petabyte-scale data warehouse service designed for analytics?
    - A. Amazon RDS
    - B. Amazon DynamoDB
    - C. Amazon Redshift
    - D. Amazon EMR

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Redshift is a cloud data warehouse service optimized for large-scale data analysis and business intelligence workloads using standard SQL.
    </details>

154. What is Amazon Aurora?
    - A. A NoSQL database service.
    - B. A data warehousing service.
    - C. A MySQL and PostgreSQL-compatible relational database built for the cloud, offering higher performance and availability than standard MySQL/PostgreSQL on RDS.
    - D. An in-memory caching service.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Aurora is a relational database engine compatible with MySQL and PostgreSQL, available through RDS. It provides significantly higher performance, scalability, and availability compared to standard implementations.
    </details>

155. Which AWS service helps you process large amounts of data using popular big data frameworks like Apache Spark, Hadoop, Hive, and Presto?
    - A. Amazon Redshift
    - B. Amazon EMR (Elastic MapReduce)
    - C. Amazon RDS
    - D. Amazon Kinesis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Amazon EMR is a managed cluster platform that simplifies running big data frameworks to process and analyze vast amounts of data.
    </details>

156. What is a primary benefit of using Amazon RDS compared to managing your own database on an EC2 instance?
    - A. RDS provides root access to the underlying operating system.
    - B. RDS automates time-consuming administration tasks like patching, backups, and scaling.
    - C. RDS is significantly cheaper for all database sizes.
    - D. RDS supports only proprietary database engines.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: RDS simplifies database management by handling tasks such as hardware provisioning, database setup, patching, and backups, allowing users to focus on application development.
    </details>

157. Which RDS feature automatically creates a standby copy of your database in a different Availability Zone for high availability?
    - A. Read Replicas
    - B. Multi-AZ Deployment
    - C. Database Snapshots
    - D. Performance Insights

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: RDS Multi-AZ deployments enhance database availability by synchronously replicating data to a standby instance in a different AZ. RDS automatically fails over to the standby in case of primary instance failure or AZ disruption.
    </details>

158. What is the main purpose of RDS Read Replicas?
    - A. To provide automatic failover for the primary database.
    - B. To improve database durability through backups.
    - C. To scale read traffic by creating read-only copies of the primary database.
    - D. To encrypt database connections.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Read Replicas are asynchronous copies of the primary database instance used to offload read workloads, thereby increasing aggregate read throughput for read-heavy applications.
    </details>

159. Which AWS service provides a fully managed in-memory data store or cache service, compatible with Redis or Memcached?
    - A. Amazon DynamoDB Accelerator (DAX)
    - B. Amazon RDS
    - C. Amazon ElastiCache
    - D. Amazon S3

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon ElastiCache makes it easy to deploy, operate, and scale popular open-source compatible in-memory data stores like Redis and Memcached, often used for caching database queries or session state.
    </details>

160. What is Amazon DynamoDB Accelerator (DAX)?
    - A. A data warehousing service.
    - B. A fully managed, highly available, in-memory cache specifically for DynamoDB.
    - C. A tool for migrating databases to DynamoDB.
    - D. A relational database engine.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: DAX is an in-memory cache for DynamoDB that delivers microsecond response times for accessing eventually consistent data, significantly speeding up reads from DynamoDB tables.
    </details>

161. Which AWS analytics service allows you to query data directly in S3 using standard SQL without loading it into a database?
    - A. Amazon Redshift Spectrum
    - B. Amazon EMR
    - C. Amazon Athena
    - D. Amazon QuickSight

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Athena is an interactive query service that makes it easy to analyze data directly in Amazon S3 using standard SQL. It is serverless, so there is no infrastructure to manage.
    </details>

162. Which AWS service is a fast, cloud-powered business intelligence (BI) service that makes it easy to build visualizations, perform ad hoc analysis, and get business insights from data?
    - A. Amazon Athena
    - B. Amazon QuickSight
    - C. Amazon Redshift
    - D. AWS Glue

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Amazon QuickSight is a scalable, serverless, embeddable, machine learning-powered BI service built for the cloud. It allows users to create and publish interactive dashboards.
    </details>

163. What is AWS Glue?
    - A. A relational database service.
    - B. A business intelligence dashboarding tool.
    - C. A fully managed extract, transform, and load (ETL) service.
    - D. A NoSQL database service.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Glue is a serverless data integration service that makes it easy to discover, prepare, and combine data for analytics, machine learning, and application development. It includes a Data Catalog and ETL capabilities.
    </details>

164. Which AWS service makes it easy to collect, process, and analyze real-time streaming data?
    - A. Amazon SQS
    - B. Amazon Kinesis
    - C. AWS Batch
    - D. Amazon EMR

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Amazon Kinesis provides services (like Kinesis Data Streams, Kinesis Data Firehose, Kinesis Data Analytics) to easily collect, process, and analyze video and data streams in real time.
    </details>

165. You need a database solution for an application with simple key-value lookups requiring extremely high read/write throughput and low latency. Which AWS service is the best fit?
    - A. Amazon RDS for MySQL
    - B. Amazon Redshift
    - C. Amazon DynamoDB
    - D. Amazon EFS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: DynamoDB is specifically designed for high-scale NoSQL workloads demanding low-latency key-value access patterns, making it ideal for applications like gaming leaderboards, session stores, or IoT data ingestion.
    </details>

166. Which AWS database service would you choose for running a traditional Online Transaction Processing (OLTP) workload using a standard PostgreSQL database?
    - A. Amazon DynamoDB
    - B. Amazon Redshift
    - C. Amazon RDS for PostgreSQL or Amazon Aurora (PostgreSQL compatible)
    - D. Amazon ElastiCache for Redis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: For standard relational OLTP workloads, Amazon RDS (offering managed PostgreSQL) or Amazon Aurora (offering a higher-performance PostgreSQL-compatible engine) are the appropriate choices.
    </details>

167. What is the primary difference in scaling between Amazon RDS and Amazon DynamoDB?
    - A. RDS scales automatically based on traffic, while DynamoDB requires manual scaling.
    - B. DynamoDB scales horizontally almost limitlessly by partitioning data, while RDS typically scales vertically (instance size) or horizontally via Read Replicas.
    - C. RDS scales storage automatically, while DynamoDB has fixed storage limits.
    - D. DynamoDB scaling only applies to read operations, while RDS scales both reads and writes.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: DynamoDB is designed for massive horizontal scalability for both reads and writes by partitioning data across multiple servers. RDS scaling involves increasing instance size (vertical) or adding Read Replicas (horizontal scaling for reads).
    </details>

168. Which AWS service helps you migrate databases to AWS easily and securely, supporting migrations between different database engines (heterogeneous) or like-for-like (homogeneous)?
    - A. AWS Schema Conversion Tool (SCT)
    - B. AWS Database Migration Service (DMS)
    - C. AWS Glue
    - D. Amazon EMR

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Database Migration Service (DMS) helps migrate databases to AWS quickly and securely. It supports homogeneous migrations (e.g., Oracle to Oracle on RDS) and heterogeneous migrations (e.g., Oracle to Aurora PostgreSQL) often used in conjunction with SCT.
    </details>

169. What is the role of the AWS Schema Conversion Tool (SCT) in database migrations?
    - A. It physically moves the data from the source to the target database.
    - B. It automatically converts the source database schema and code objects to a format compatible with the target database, especially in heterogeneous migrations.
    - C. It monitors the performance of the migrated database.
    - D. It provides a managed database service.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: SCT is used alongside DMS, primarily for heterogeneous migrations. It analyzes the source schema and automatically converts most of it to be compatible with the target database engine, highlighting any objects needing manual conversion.
    </details>

170. Which AWS service provides a managed graph database?
    - A. Amazon DocumentDB
    - B. Amazon Neptune
    - C. Amazon Timestream
    - D. Amazon QLDB

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Amazon Neptune is a fast, reliable, fully managed graph database service that makes it easy to build and run applications working with highly connected datasets.
    </details>

171. Which AWS service provides a managed document database compatible with MongoDB?
    - A. Amazon Neptune
    - B. Amazon DynamoDB
    - C. Amazon DocumentDB (with MongoDB compatibility)
    - D. Amazon RDS

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon DocumentDB is a scalable, highly available, and fully managed document database service that supports MongoDB workloads.
    </details>

172. You need to store and analyze time-series data, such as IoT sensor readings or application performance metrics. Which purpose-built AWS database service is designed for this?
    - A. Amazon QLDB
    - B. Amazon Neptune
    - C. Amazon Timestream
    - D. Amazon ElastiCache

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Timestream is a fast, scalable, and serverless time series database service for IoT and operational applications that makes it easy to store and analyze trillions of events per day.
    </details>

173. Which AWS service provides a fully managed ledger database that maintains an immutable, cryptographically verifiable transaction log?
    - A. Amazon Timestream
    - B. Amazon Neptune
    - C. Amazon QLDB (Quantum Ledger Database)
    - D. Amazon Blockchain

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon QLDB is a fully managed ledger database that provides a transparent, immutable, and cryptographically verifiable transaction log ‎owned by a central trusted authority.
    </details>

174. Under the Shared Responsibility Model for Amazon RDS, what is AWS responsible for?
    - A. Managing database schema design.
    - B. Optimizing SQL queries.
    - C. Patching the database engine and underlying operating system.
    - D. Configuring security groups for the database instance.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: For RDS, AWS manages the infrastructure, operating system, and database engine patching (security OF the cloud). The customer is responsible for schema design, query optimization, application integration, and configuring network access controls like security groups (security IN the cloud).
    </details>

175. Which feature of Amazon Redshift allows you to query data directly in your Amazon S3 data lake without loading it into Redshift tables?
    - A. Redshift Concurrency Scaling
    - B. Redshift AQUA (Advanced Query Accelerator)
    - C. Redshift Spectrum
    - D. Redshift Data Sharing

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Redshift Spectrum enables you to run SQL queries against exabytes of unstructured data in Amazon S3 without needing to load or transform the data, extending Redshift queries to your data lake.
    </details>

