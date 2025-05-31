# AWS Cloud Practitioner Practice Questions - Batch 11 (Security & Compliance)

301. What is the AWS Shared Responsibility Model?
    - A. A model where AWS manages all aspects of security.
    - B. A model where the customer manages all aspects of security.
    - C. A framework outlining the security responsibilities of AWS (security OF the cloud) and the customer (security IN the cloud).
    - D. A billing model for security services.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Shared Responsibility Model defines that AWS is responsible for securing the underlying infrastructure (hardware, software, networking, facilities), while the customer is responsible for securing their data, applications, operating systems, network configurations (like firewalls), and identity/access management within the cloud.
    </details>

302. Under the Shared Responsibility Model, which of the following is typically the customer's responsibility? (Choose TWO)
    - A. Securing AWS global infrastructure (Regions, AZs, Edge Locations).
    - B. Patching the guest operating system on EC2 instances.
    - C. Managing physical access to data centers.
    - D. Configuring Security Groups and Network ACLs.
    - E. Managing the hypervisor for EC2.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B, D
      Explanation: Customers are responsible for security measures within their control, such as patching their guest OS, configuring firewalls (Security Groups, NACLs), managing user access (IAM), and encrypting their data.
    </details>

303. Under the Shared Responsibility Model, which of the following is typically AWS's responsibility?
    - A. Encrypting customer data stored in S3.
    - B. Managing IAM user passwords.
    - C. Ensuring the physical security of AWS data centers.
    - D. Installing customer applications on EC2 instances.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS is responsible for the security OF the cloud, which includes protecting the hardware, software, networking, and facilities that run AWS services, including physical data center security.
    </details>

304. Which AWS service helps protect web applications from common web exploits like SQL injection and cross-site scripting (XSS)?
    - A. AWS Shield
    - B. Amazon GuardDuty
    - C. AWS WAF (Web Application Firewall)
    - D. Amazon Inspector

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS WAF is a web application firewall that monitors HTTP/S requests forwarded to services like CloudFront, Application Load Balancer, or API Gateway, allowing you to configure rules to block malicious traffic patterns.
    </details>

305. Which AWS service provides managed Distributed Denial of Service (DDoS) protection?
    - A. AWS WAF
    - B. AWS Shield (Standard and Advanced)
    - C. Amazon GuardDuty
    - D. AWS Firewall Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Shield provides protection against DDoS attacks. Shield Standard is automatically enabled for all AWS customers at no additional cost, while Shield Advanced offers more comprehensive protection for specific resources.
    </details>

306. What is the difference between AWS Shield Standard and AWS Shield Advanced?
    - A. Shield Standard protects against web application exploits, while Shield Advanced protects against DDoS.
    - B. Shield Standard is a paid service, while Shield Advanced is free.
    - C. Shield Advanced provides enhanced detection, mitigation for larger attacks, near real-time visibility, and access to the AWS DDoS Response Team (DRT), which are not included in Shield Standard.
    - D. Shield Standard only protects EC2 instances, while Shield Advanced protects CloudFront and ELB.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Shield Standard offers basic, automatic protection against common network and transport layer DDoS attacks. Shield Advanced provides more sophisticated protection, visibility, specialized support (DRT), and cost protection against DDoS-related usage spikes for protected resources.
    </details>

307. Which AWS service continuously monitors for malicious activity and unauthorized behavior by analyzing CloudTrail logs, VPC Flow Logs, and DNS logs?
    - A. Amazon Inspector
    - B. AWS Security Hub
    - C. Amazon GuardDuty
    - D. AWS WAF

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon GuardDuty is an intelligent threat detection service that uses machine learning and anomaly detection to identify potential threats like compromised instances, reconnaissance, or unusual API activity.
    </details>

308. Which AWS service is used to assess EC2 instances and container images for software vulnerabilities and unintended network exposure?
    - A. Amazon GuardDuty
    - B. Amazon Macie
    - C. Amazon Inspector
    - D. AWS Shield

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Inspector is an automated vulnerability management service that scans workloads for known software vulnerabilities (CVEs) and checks network reachability against best practices.
    </details>

309. Which AWS service uses machine learning to discover, classify, and protect sensitive data (like PII or financial information) stored in Amazon S3?
    - A. Amazon GuardDuty
    - B. Amazon Inspector
    - C. Amazon Macie
    - D. AWS Secrets Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Macie is a fully managed data security and data privacy service that uses machine learning and pattern matching to discover and protect sensitive data in S3 buckets.
    </details>

310. Which AWS service provides recommendations to help you follow AWS best practices, optimize your environment for cost, performance, security, fault tolerance, and service limits?
    - A. AWS Config
    - B. AWS CloudTrail
    - C. AWS Trusted Advisor
    - D. AWS Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Trusted Advisor acts like a personalized cloud expert, analyzing your AWS environment and providing real-time guidance based on best practices across its five check categories.
    </details>

311. Which AWS service provides on-demand access to AWS compliance reports, such as SOC reports, ISO certifications, and PCI DSS compliance packages?
    - A. AWS Trusted Advisor
    - B. AWS Artifact
    - C. AWS Config
    - D. AWS Security Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Artifact is a central resource for compliance-related information. It provides access to AWS security and compliance reports and select online agreements.
    </details>

312. Which AWS service allows you to create and manage cryptographic keys used to encrypt data across various AWS services?
    - A. AWS Secrets Manager
    - B. AWS Certificate Manager (ACM)
    - C. AWS Key Management Service (KMS)
    - D. AWS CloudHSM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS KMS is a managed service for creating and controlling Customer Master Keys (CMKs), which are used to encrypt and decrypt data. It integrates with many AWS services for easy encryption.
    </details>

313. What is the primary difference between AWS KMS and AWS CloudHSM?
    - A. KMS is for managing SSL certificates, CloudHSM is for encryption keys.
    - B. KMS is a multi-tenant managed service, while CloudHSM provides dedicated, single-tenant Hardware Security Modules (HSMs).
    - C. KMS keys can be exported, CloudHSM keys cannot.
    - D. CloudHSM is cheaper than KMS.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: KMS offers a shared, managed environment for key management suitable for most use cases. CloudHSM provides dedicated HSM hardware for scenarios requiring higher levels of security, compliance (like FIPS 140-2 Level 3), or exclusive control over the HSM environment.
    </details>

314. Which AWS service helps you securely store, manage, and rotate secrets like database credentials, API keys, and OAuth tokens?
    - A. AWS Key Management Service (KMS)
    - B. AWS Systems Manager Parameter Store
    - C. AWS Secrets Manager
    - D. AWS Certificate Manager (ACM)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Secrets Manager is specifically designed for managing the lifecycle of secrets, including automatic rotation capabilities for services like RDS databases, Redshift, and DocumentDB.
    </details>

315. Which AWS service simplifies the provisioning, management, and deployment of public and private SSL/TLS certificates?
    - A. AWS Secrets Manager
    - B. AWS Key Management Service (KMS)
    - C. AWS Certificate Manager (ACM)
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: ACM handles the creation, storage, and renewal of SSL/TLS certificates used with AWS services like Elastic Load Balancing and CloudFront.
    </details>

316. Which AWS service allows you to centrally configure and manage firewall rules (like WAF rules, Security Groups, Network Firewall policies) across multiple accounts and resources within an AWS Organization?
    - A. AWS Shield
    - B. AWS Security Hub
    - C. AWS Firewall Manager
    - D. Amazon GuardDuty

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Firewall Manager simplifies the administration and maintenance of firewall rules across your organization, ensuring consistent policy enforcement.
    </details>

317. Which AWS service provides a comprehensive view of your security alerts and compliance status across multiple AWS accounts?
    - A. AWS Trusted Advisor
    - B. Amazon GuardDuty
    - C. AWS Security Hub
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Security Hub aggregates, organizes, and prioritizes security findings from various AWS services (like GuardDuty, Inspector, Macie) and partner solutions, providing a single pane of glass for security posture management.
    </details>

318. What type of encryption protects data while it is traveling between systems (e.g., between a user's browser and a web server)?
    - A. Encryption at Rest
    - B. Encryption in Transit
    - C. Client-Side Encryption
    - D. Server-Side Encryption

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Encryption in transit, typically using protocols like TLS/SSL, protects data from eavesdropping as it moves across networks.
    </details>

319. What type of encryption protects data while it is stored on disk or other storage media?
    - A. Encryption in Transit
    - B. Encryption at Rest
    - C. Network Encryption
    - D. Transport Layer Security (TLS)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Encryption at rest protects data from unauthorized access if the physical storage media is compromised. AWS services like S3, EBS, and RDS offer various options for encryption at rest.
    </details>

320. Which AWS compliance program relates to the security of credit cardholder data?
    - A. SOC 2 (System and Organization Controls 2)
    - B. ISO 27001
    - C. HIPAA (Health Insurance Portability and Accountability Act)
    - D. PCI DSS (Payment Card Industry Data Security Standard)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: PCI DSS is a global standard for organizations that handle branded credit cards from major card schemes. AWS provides resources and services to help customers build PCI DSS compliant environments.
    </details>

321. Which AWS compliance framework is relevant for organizations handling Protected Health Information (PHI) in the United States?
    - A. GDPR (General Data Protection Regulation)
    - B. PCI DSS
    - C. HIPAA
    - D. SOC 1

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: HIPAA establishes requirements for the use, disclosure, and safeguarding of PHI. AWS offers a HIPAA compliance program and enables customers to build HIPAA-compliant applications.
    </details>

322. Which AWS Trusted Advisor check category specifically helps identify security vulnerabilities or deviations from security best practices?
    - A. Cost Optimization
    - B. Performance
    - C. Security
    - D. Fault Tolerance

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Security category in Trusted Advisor includes checks for things like unrestricted S3 bucket access, MFA on root account, exposed access keys, and specific port access in security groups.
    </details>

323. You need to ensure that only encrypted connections (HTTPS) are allowed to your Application Load Balancer. Where would you configure this requirement?
    - A. In the Network ACLs.
    - B. In the Security Groups attached to the EC2 instances.
    - C. In the Application Load Balancer listener configuration.
    - D. In AWS WAF rules.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: ALB listeners define the protocol and port for frontend connections. You would configure an HTTPS listener (typically on port 443) and potentially redirect HTTP traffic to HTTPS.
    </details>

324. Which service helps you understand the potential blast radius of security events by visualizing resource relationships and historical activity?
    - A. Amazon Inspector
    - B. Amazon Detective
    - C. AWS Security Hub
    - D. Amazon GuardDuty

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Amazon Detective automatically collects log data from your AWS resources and uses machine learning, statistical analysis, and graph theory to build interactive visualizations that help you conduct faster and more efficient security investigations.
    </details>

325. What is the purpose of AWS Config Rules?
    - A. To automatically remediate non-compliant resources.
    - B. To define desired configuration settings for resources and check for compliance against those settings.
    - C. To log API calls for auditing.
    - D. To provide DDoS protection.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Config Rules represent your desired configuration settings. AWS Config continuously evaluates your resource configurations against these rules and flags resources as non-compliant if they deviate.
    </details>

326. Which AWS service provides a managed Network Firewall service for VPCs?
    - A. Security Groups
    - B. Network ACLs
    - C. AWS Network Firewall
    - D. AWS WAF

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Network Firewall is a stateful, managed network firewall and intrusion detection/prevention service for VPCs, offering more granular control than Security Groups or NACLs.
    </details>

327. You want to prevent sensitive data like access keys from being accidentally embedded in code pushed to AWS CodeCommit. Which service can help detect this?
    - A. Amazon Inspector
    - B. Amazon CodeGuru Reviewer
    - C. AWS Secrets Manager
    - D. Amazon GuardDuty

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Amazon CodeGuru Reviewer uses machine learning to analyze code repositories (including CodeCommit) and identify critical issues, security vulnerabilities, and deviations from AWS best practices, including hardcoded secrets.
    </details>

328. Which principle is fundamental to securing AWS accounts, especially the root user?
    - A. Principle of Maximum Privilege
    - B. Principle of Least Privilege
    - C. Principle of Shared Credentials
    - D. Principle of Open Access

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: The principle of least privilege dictates granting only the minimum permissions necessary to perform a task. This applies strongly to the root user (which should rarely be used) and all IAM users/roles.
    </details>

329. What is a common use case for AWS CloudHSM?
    - A. Storing application logs.
    - B. Meeting strict compliance requirements that mandate key management in dedicated, validated hardware.
    - C. Managing SSL/TLS certificates for websites.
    - D. Providing DDoS protection.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: CloudHSM is often used when regulatory or compliance mandates (like FIPS 140-2 Level 3) require the use of dedicated HSMs for cryptographic operations and key storage.
    </details>

330. Which AWS service provides a unified view of compliance status against controls based on various frameworks (e.g., PCI DSS, HIPAA)?
    - A. AWS Artifact
    - B. AWS Audit Manager
    - C. AWS Config
    - D. AWS Security Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Audit Manager helps you continuously audit your AWS usage to simplify how you assess risk and compliance with regulations and industry standards. It automates evidence collection and provides prebuilt frameworks.
    </details>

331. How does AWS WAF help protect against common attacks?
    - A. By encrypting data at rest.
    - B. By detecting malware on EC2 instances.
    - C. By filtering incoming web requests based on rules that identify patterns like SQL injection or cross-site scripting.
    - D. By providing secure key storage.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: WAF inspects HTTP/S requests and applies rules (either AWS Managed Rules or custom rules) to block or allow traffic based on request characteristics, helping mitigate common web application vulnerabilities.
    </details>

332. What is a primary benefit of using AWS KMS for encryption?
    - A. It provides dedicated HSM hardware.
    - B. It simplifies key management and integrates seamlessly with many AWS services for encryption.
    - C. It automatically rotates database passwords.
    - D. It manages SSL/TLS certificates.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: KMS abstracts the complexity of key management, providing centralized control, auditing (via CloudTrail), and easy integration for encrypting data in services like S3, EBS, RDS, etc.
    </details>

333. Which Trusted Advisor check falls under the Fault Tolerance category?
    - A. Checking for exposed access keys.
    - B. Checking for S3 bucket permissions.
    - C. Checking for EBS snapshots or RDS backup status.
    - D. Checking for EC2 instances with high utilization.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The Fault Tolerance category focuses on redundancy and recoverability. Checks include verifying EBS snapshot age, RDS backup status, Auto Scaling group health, and Availability Zone balance.
    </details>

334. You need to provide evidence to auditors that your AWS environment meets specific compliance standards. Which service is the primary source for official AWS compliance reports?
    - A. AWS Trusted Advisor
    - B. AWS Config
    - C. AWS Audit Manager
    - D. AWS Artifact

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: AWS Artifact is the go-to service for downloading AWS's own compliance reports (SOC, PCI, ISO, etc.) and managing certain agreements with AWS.
    </details>

335. Which security service operates at the edge of the AWS network, often integrated with CloudFront?
    - A. Amazon GuardDuty
    - B. Amazon Inspector
    - C. AWS WAF and AWS Shield
    - D. AWS Security Hub

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS WAF and AWS Shield are commonly deployed at the edge, integrated with services like CloudFront distributions or Application Load Balancers, to filter malicious traffic and mitigate DDoS attacks before they reach backend resources.
    </details>

336. What is the purpose of enabling MFA (Multi-Factor Authentication) on the AWS account root user?
    - A. To reduce AWS costs.
    - B. To improve the performance of EC2 instances.
    - C. To add an extra layer of security, requiring more than just a password to access the highly privileged root account.
    - D. To enable cross-account access.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Enabling MFA is a critical security best practice for the root user (and all IAM users) as it significantly reduces the risk of account compromise due to stolen or weak passwords.
    </details>

337. Which AWS service helps you manage security findings and take action on them from a centralized dashboard?
    - A. AWS CloudTrail
    - B. AWS Config
    - C. AWS Security Hub
    - D. AWS Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Security Hub aggregates findings from multiple AWS security services and partner products, prioritizes them, and enables automated response actions.
    </details>

338. If you need to encrypt data using keys that you fully control within dedicated hardware, which service should you use?
    - A. AWS KMS with customer-provided keys (CMKs)
    - B. AWS Secrets Manager
    - C. AWS CloudHSM
    - D. AWS Certificate Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudHSM provides dedicated HSMs where you have exclusive control over the keys and cryptographic operations, meeting specific compliance or security requirements.
    </details>

339. Which service automatically detects sensitive data like Personally Identifiable Information (PII) in S3 buckets?
    - A. Amazon GuardDuty
    - B. Amazon Inspector
    - C. Amazon Macie
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Macie uses machine learning and pattern matching to identify and classify sensitive data stored in S3, helping with data privacy and security.
    </details>

340. What is a key difference between AWS Systems Manager Parameter Store and AWS Secrets Manager?
    - A. Parameter Store can only store plain text, while Secrets Manager stores encrypted secrets.
    - B. Secrets Manager offers automatic rotation capabilities for secrets like database credentials, which Parameter Store does not natively provide.
    - C. Parameter Store is more expensive than Secrets Manager.
    - D. Secrets Manager integrates with CloudFormation, while Parameter Store does not.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: While both can store secrets securely (Parameter Store has Standard and Advanced tiers, with Advanced supporting higher limits and policies), Secrets Manager provides built-in, automated rotation features for supported services, which is a major differentiator.
    </details>

341. Which AWS service would you use to investigate the root cause of a security finding generated by GuardDuty by exploring related resources and activities?
    - A. AWS Security Hub
    - B. Amazon Detective
    - C. AWS CloudTrail
    - D. Amazon Inspector

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Amazon Detective is designed specifically for security investigations, automatically processing logs and using graph models to help visualize context and connections related to security findings.
    </details>

342. You need to ensure all S3 buckets created in your account enforce encryption at rest. Which service can help you monitor and enforce this configuration policy?
    - A. Amazon Macie
    - B. AWS Trusted Advisor
    - C. AWS Config (using Config Rules)
    - D. Amazon GuardDuty

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Config can track S3 bucket configurations, and you can implement Config Rules (either managed or custom) to check if buckets have server-side encryption enabled and flag non-compliant buckets.
    </details>

343. Which AWS service provides a managed threat intelligence feed used by services like GuardDuty?
    - A. AWS Security Hub
    - B. Amazon Detective
    - C. AWS Trusted Advisor
    - D. GuardDuty uses its own integrated threat intelligence feeds from AWS Security and third parties.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: GuardDuty integrates threat intelligence feeds (lists of known malicious IP addresses or domains) from AWS Security and reputable third-party providers as part of its threat detection process.
    </details>

344. What is the primary purpose of AWS Firewall Manager security policies?
    - A. To define IAM user permissions.
    - B. To specify which firewall rules (WAF, Security Group, etc.) should be deployed across accounts/resources in an AWS Organization.
    - C. To configure DDoS protection levels.
    - D. To store encryption keys.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Firewall Manager policies define the rule sets (e.g., a specific WAF rule group, a baseline set of security group rules) and the scope (which accounts/resources) they should apply to, ensuring consistent enforcement.
    </details>

345. Which AWS service helps ensure that the principle of least privilege is applied by analyzing access logs and identifying unused permissions?
    - A. AWS Config
    - B. AWS CloudTrail
    - C. IAM Access Advisor
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: IAM Access Advisor shows the service permissions granted to a user, group, or role and when those services were last accessed, helping you identify and remove unnecessary permissions.
    </details>

346. Which AWS service provides visibility into user activity and API usage across your AWS infrastructure?
    - A. Amazon CloudWatch
    - B. AWS CloudTrail
    - C. AWS X-Ray
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: CloudTrail records actions taken by users, roles, or AWS services as events, providing a detailed audit trail for operational troubleshooting and security analysis.
    </details>

347. Which AWS service allows you to define and enforce security and compliance controls across your AWS accounts using pre-built or custom frameworks?
    - A. AWS Artifact
    - B. AWS Audit Manager
    - C. AWS Security Hub
    - D. AWS Control Tower

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Audit Manager helps automate evidence collection for audits based on various compliance frameworks, simplifying risk assessment and compliance reporting.
    </details>

348. What is a primary security benefit of using IAM Roles for EC2 instances instead of Access Keys?
    - A. Roles provide higher performance.
    - B. Roles allow access from any AWS Region.
    - C. Roles provide temporary credentials that are automatically rotated, eliminating the need to store long-term keys on the instance.
    - D. Roles are free, while Access Keys incur costs.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Using IAM Roles for EC2 (and other services like Lambda) is a security best practice because it avoids storing static, long-term credentials (Access Keys) which could be compromised. The service automatically retrieves temporary credentials via the instance metadata service.
    </details>

349. Which AWS service should be used to centrally manage and automate patching for EC2 instances and on-premises servers?
    - A. AWS Config
    - B. Amazon Inspector
    - C. AWS Systems Manager Patch Manager
    - D. AWS CloudFormation

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Systems Manager Patch Manager provides features to scan instances for missing patches, define patching baselines, schedule patching operations during maintenance windows, and report on patch compliance.
    </details>

350. Which AWS service provides a dashboard with checks and recommendations across cost optimization, performance, security, fault tolerance, and service limits?
    - A. AWS Security Hub
    - B. AWS Well-Architected Tool
    - C. AWS Trusted Advisor
    - D. AWS Cost Explorer

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Trusted Advisor analyzes your AWS environment against best practices in these five categories and provides actionable recommendations to improve your posture.
    </details>

351. You need to store database credentials securely and allow your application running on EC2 to retrieve them without hardcoding. The credentials also need to be rotated automatically every 30 days. Which service is best suited for this?
    - A. AWS Systems Manager Parameter Store (Standard Tier)
    - B. AWS Secrets Manager
    - C. AWS KMS
    - D. Storing them in an encrypted S3 bucket.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Secrets Manager is designed for this exact use case, offering secure storage, IAM-controlled retrieval, and built-in automatic rotation capabilities for supported database services.
    </details>

352. Which service helps you detect if configuration changes made to your AWS resources deviate from your defined policies?
    - A. AWS CloudTrail
    - B. Amazon GuardDuty
    - C. AWS Config
    - D. Amazon Inspector

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Config continuously monitors resource configurations and uses Config Rules to evaluate whether these configurations comply with your desired policies, flagging non-compliant resources.
    </details>

353. What is the primary function of AWS Security Hub?
    - A. To perform vulnerability scans on EC2 instances.
    - B. To provide DDoS protection.
    - C. To aggregate, organize, and prioritize security findings from various AWS services and partner tools.
    - D. To manage encryption keys.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Security Hub acts as a central console for managing security posture, consolidating findings from services like GuardDuty, Inspector, Macie, Firewall Manager, and others.
    </details>

354. Which AWS service would you use to obtain AWS's SOC 2 compliance report?
    - A. AWS Trusted Advisor
    - B. AWS Config
    - C. AWS Artifact
    - D. AWS Audit Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Artifact is the central repository where customers can download AWS compliance reports, such as SOC, PCI DSS, ISO, and HIPAA reports.
    </details>

355. What layer of the OSI model does AWS WAF primarily operate at?
    - A. Layer 2 (Data Link)
    - B. Layer 3 (Network)
    - C. Layer 4 (Transport)
    - D. Layer 7 (Application)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: AWS WAF inspects HTTP/S requests at the application layer, allowing filtering based on request content like headers, body, URI, query strings, etc.
    </details>

356. Which AWS service provides foundational protection against common network and transport layer DDoS attacks for all AWS customers automatically?
    - A. AWS WAF
    - B. AWS Shield Standard
    - C. AWS Shield Advanced
    - D. AWS Firewall Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Shield Standard is enabled by default at no extra cost and provides automatic protection against the most common types of DDoS attacks.
    </details>

357. You suspect an EC2 instance has been compromised and is scanning ports on other instances in your VPC. Which service is most likely to detect and alert on this behavior?
    - A. Amazon Inspector
    - B. AWS WAF
    - C. Amazon GuardDuty
    - D. AWS Shield

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: GuardDuty analyzes VPC Flow Logs and uses threat intelligence and anomaly detection to identify suspicious activities like port scanning originating from instances within your environment.
    </details>

358. Which service focuses on identifying software vulnerabilities (like outdated packages with known CVEs) within your EC2 instances?
    - A. Amazon GuardDuty
    - B. Amazon Macie
    - C. Amazon Inspector
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Inspector's primary function is vulnerability management, scanning operating systems and software packages for known vulnerabilities.
    </details>

359. What is the key benefit of using AWS Certificate Manager (ACM) for SSL/TLS certificates used with ELB or CloudFront?
    - A. It allows using self-signed certificates.
    - B. It provides free public certificates and handles automatic renewal.
    - C. It stores certificates in dedicated HSMs.
    - D. It encrypts the certificates using KMS.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: ACM can provision public SSL/TLS certificates at no cost for use with integrated AWS services, and it automatically manages the renewal process, simplifying certificate lifecycle management.
    </details>

360. Which AWS service provides a managed directory service compatible with Microsoft Active Directory?
    - A. Amazon Cognito
    - B. AWS IAM Identity Center
    - C. AWS Directory Service (specifically Managed Microsoft AD)
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS Directory Service offers several directory options, including AWS Managed Microsoft AD, which provides a fully managed Active Directory hosted on AWS.
    </details>

361. Which AWS service is specifically designed to help you investigate the root cause of security issues or suspicious activities by analyzing logs and visualizing relationships?
    - A. AWS Security Hub
    - B. Amazon GuardDuty
    - C. Amazon Detective
    - D. AWS CloudTrail Lake

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Amazon Detective automatically processes log data (CloudTrail, VPC Flow Logs, GuardDuty findings) and uses graph models to help security analysts quickly conduct investigations and understand the scope of potential security issues.
    </details>

362. What is the main purpose of AWS Key Management Service (KMS) Customer Master Keys (CMKs)?
    - A. To authenticate users.
    - B. To act as the root key for encrypting and decrypting other keys (Data Keys) which are used to encrypt actual data.
    - C. To store SSL/TLS private keys.
    - D. To manage application secrets.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: KMS uses envelope encryption. CMKs are used to encrypt/decrypt Data Keys. These Data Keys are then used outside of KMS to encrypt/decrypt application data. The CMK itself never leaves KMS.
    </details>

363. Which AWS service would you use if you need to ensure that objects stored in S3 cannot be deleted or overwritten for a specific retention period (WORM - Write Once Read Many)?
    - A. S3 Versioning
    - B. S3 Lifecycle Policies
    - C. S3 Object Lock
    - D. S3 Replication

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: S3 Object Lock provides WORM capabilities, allowing you to set retention modes (Governance or Compliance) and periods to prevent object modification or deletion, often used for regulatory compliance.
    </details>

364. Which AWS service provides a simplified way to set up a secure, multi-account AWS environment based on best practices, often used as a starting point for new AWS deployments?
    - A. AWS Organizations
    - B. AWS Control Tower
    - C. AWS Landing Zone (solution)
    - D. AWS Service Catalog

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Control Tower automates the setup of a baseline environment (a landing zone) using AWS Organizations, Service Control Policies (SCPs), AWS Config, CloudTrail, and IAM Identity Center according to AWS best practices.
    </details>

365. What type of policies can be used within AWS Organizations to restrict the permissions that IAM users and roles can have in member accounts, regardless of their IAM policies?
    - A. IAM Policies
    - B. Bucket Policies
    - C. Service Control Policies (SCPs)
    - D. Session Policies

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SCPs are applied at the Organization Unit (OU) or account level within AWS Organizations. They act as guardrails, defining the maximum available permissions for accounts within their scope; they do not grant permissions themselves but can restrict what IAM policies allow.
    </details>

366. Which AWS service provides security and operational best practice checks for your AWS account and resources?
    - A. Amazon Inspector
    - B. AWS Trusted Advisor
    - C. Amazon GuardDuty
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Trusted Advisor analyzes your AWS environment against best practices across multiple pillars (Cost Optimization, Performance, Security, Fault Tolerance, Service Limits) and provides recommendations.
    </details>

367. You need to ensure that developers cannot launch unapproved EC2 instance types within specific AWS accounts managed by AWS Organizations. Which service should you use to enforce this restriction?
    - A. IAM Policies
    - B. AWS Config Rules
    - C. Service Control Policies (SCPs)
    - D. AWS Systems Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: SCPs are the appropriate mechanism within AWS Organizations to set broad guardrails that restrict actions, such as denying the ability to launch specific EC2 instance types, across multiple accounts.
    </details>

368. Which AWS service helps protect against volumetric DDoS attacks by absorbing malicious traffic?
    - A. AWS WAF
    - B. AWS Shield
    - C. Amazon GuardDuty
    - D. Network ACLs

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Shield (both Standard and Advanced) is specifically designed to mitigate DDoS attacks, including large-scale volumetric attacks targeting network and transport layers.
    </details>

369. What is the primary focus of Amazon Macie?
    - A. Detecting network intrusions.
    - B. Scanning EC2 instances for vulnerabilities.
    - C. Discovering and protecting sensitive data stored in Amazon S3.
    - D. Managing firewall rules.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Macie is a data security and privacy service focused on identifying sensitive data (PII, financial data) within S3 buckets and alerting on potential security risks related to that data.
    </details>

370. Which service provides a single place to view and manage security alerts and compliance status across your AWS accounts?
    - A. AWS Trusted Advisor
    - B. AWS Security Hub
    - C. AWS CloudTrail
    - D. AWS Config

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Security Hub acts as a central aggregation point for findings from various AWS security services (GuardDuty, Inspector, Macie, etc.) and partner tools, providing a unified dashboard for security posture management.
    </details>

371. Which AWS service is essential for auditing who did what, when, and from where within your AWS account?
    - A. Amazon CloudWatch
    - B. AWS Config
    - C. AWS CloudTrail
    - D. AWS IAM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudTrail logs API calls made within your account, providing a detailed audit trail crucial for security analysis, compliance, and operational troubleshooting.
    </details>

372. What is the recommended security practice regarding the AWS account root user credentials after initial account setup?
    - A. Share them with the primary administrator.
    - B. Use them for daily administrative tasks.
    - C. Secure them with a strong password and MFA, and avoid using them for routine tasks.
    - D. Delete the root user.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The root user has unrestricted access. Best practice dictates securing it strongly (MFA is critical) and locking the credentials away, using IAM users/roles with appropriate permissions for all regular activities.
    </details>

373. Which AWS service helps automate the process of assessing risk and simplifying compliance against regulations and standards?
    - A. AWS Artifact
    - B. AWS Audit Manager
    - C. AWS Config
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Audit Manager automates the collection of evidence related to compliance controls for various frameworks (like PCI DSS, HIPAA, GDPR), mapping AWS resource usage to control requirements.
    </details>

374. Which AWS service allows you to centrally manage encryption keys and control their use across various AWS services?
    - A. AWS Secrets Manager
    - B. AWS Certificate Manager (ACM)
    - C. AWS Key Management Service (KMS)
    - D. AWS CloudHSM

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: KMS provides a managed service for creating, managing, and auditing the use of cryptographic keys used for encryption within AWS.
    </details>

375. Which AWS service provides managed hardware security modules (HSMs) for enhanced key security and compliance?
    - A. AWS Key Management Service (KMS)
    - B. AWS Secrets Manager
    - C. AWS CloudHSM
    - D. AWS Certificate Manager (ACM)

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudHSM offers dedicated, single-tenant HSM appliances in the cloud, meeting higher security and compliance standards like FIPS 140-2 Level 3.
    </details>

