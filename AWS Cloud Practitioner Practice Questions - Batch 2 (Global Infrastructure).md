# AWS Cloud Practitioner Practice Questions - Batch 2 (Global Infrastructure)

26. What is an AWS Region?
    - A. A single, large data center.
    - B. A collection of Edge Locations within a specific city.
    - C. A physical location in the world composed of multiple, isolated Availability Zones.
    - D. A virtual network dedicated to a single AWS account.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: An AWS Region is a distinct geographic area. Each Region consists of multiple, isolated, and physically separate Availability Zones (AZs).
    </details>

27. What is an Availability Zone (AZ)?
    - A. A specific server rack within a data center.
    - B. One or more discrete data centers with redundant power, networking, and connectivity within an AWS Region.
    - C. A global content delivery network endpoint.
    - D. A billing and account management boundary.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: An Availability Zone (AZ) consists of one or more discrete data centers, each with redundant power, networking, and connectivity, housed in separate facilities within a Region. They are designed to be isolated from failures in other AZs.
    </details>

28. What is the minimum number of Availability Zones recommended and typically found in most AWS Regions?
    - A. 1
    - B. 2
    - C. 3
    - D. 6

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: While the minimum is technically 2, most AWS Regions are composed of three or more Availability Zones to provide high availability and fault tolerance for customer applications.
    </details>

29. Which factors should influence your decision when selecting an AWS Region for deploying an application? (Choose THREE)
    - A. The Region with the lowest number of Availability Zones.
    - B. Proximity to your end-users to minimize latency.
    - C. Data sovereignty and compliance requirements.
    - D. Availability of specific AWS services needed by the application.
    - E. The alphabetical order of the Region name.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B, C, D
      Explanation: Key factors include latency to end-users, data governance/compliance needs, the availability of required AWS services (as not all services are in all Regions), and cost (pricing can vary by Region).
    </details>

30. What is the primary purpose of AWS Edge Locations?
    - A. To run core compute services like EC2.
    - B. To host relational databases like RDS.
    - C. To cache content closer to users and reduce latency for services like Amazon CloudFront.
    - D. To manage user identities via IAM.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Edge Locations are part of the AWS global network, primarily used by Amazon CloudFront (CDN) and Route 53 to cache data and DNS responses closer to end-users, thereby reducing latency and improving performance.
    </details>

31. Which AWS services are considered global rather than regional? (Choose TWO)
    - A. Amazon S3
    - B. Amazon EC2
    - C. AWS Identity and Access Management (IAM)
    - D. Amazon VPC
    - E. Amazon Route 53

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C, E
      Explanation: IAM and Route 53 are global services. IAM entities (users, groups, roles, policies) are global, and Route 53 is a global DNS service. EC2 and VPC are regional. S3 buckets are created in a specific region, although bucket names are globally unique.
    </details>

32. A company wants to deploy a highly available web application on AWS. Which architectural practice best supports this goal?
    - A. Deploying all instances within a single Availability Zone.
    - B. Deploying instances across multiple Availability Zones within a Region.
    - C. Deploying instances across multiple Edge Locations.
    - D. Deploying instances only in the us-east-1 Region.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Deploying application resources across multiple Availability Zones within a Region is a fundamental best practice for achieving high availability, as it protects the application from failures within a single data center.
    </details>

33. Can an EBS volume created in Availability Zone `us-east-1a` be directly attached to an EC2 instance running in `us-east-1b`?
    - A. Yes, EBS volumes are regional resources.
    - B. Yes, but only if the instance and volume are in the same VPC.
    - C. No, EBS volumes are specific to the Availability Zone in which they are created.
    - D. No, EBS volumes can only be attached to instances in the same data center rack.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: EBS volumes are zonal resources. A volume created in one AZ cannot be directly attached to an instance in a different AZ. To move data, you would typically create a snapshot and restore it to a new volume in the target AZ.
    </details>

34. As of early 2025, AWS announced plans for new Regions in which locations? (Choose TWO based on recent announcements)
    - A. Antarctica
    - B. New Zealand
    - C. The Moon
    - D. Kingdom of Saudi Arabia
    - E. Atlantis

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B, D
      Explanation: Based on recent announcements (around late 2024/early 2025), AWS has plans for new regions including New Zealand, Kingdom of Saudi Arabia, Taiwan, and the AWS European Sovereign Cloud.
    </details>

35. What is the benefit of the physical separation and isolation of Availability Zones within an AWS Region?
    - A. It increases network latency between AZs.
    - B. It reduces the number of services available in the Region.
    - C. It isolates AZs from failures in other AZs, improving fault tolerance.
    - D. It makes it harder to manage resources across AZs.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The physical separation and independent infrastructure (power, cooling, networking) of AZs ensure that a failure impacting one AZ is unlikely to affect others, which is crucial for building fault-tolerant applications.
    </details>

36. Which AWS service uses the global network of Edge Locations to deliver content with low latency?
    - A. Amazon S3 Transfer Acceleration
    - B. Amazon CloudFront
    - C. AWS Direct Connect
    - D. Amazon VPC Peering

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Amazon CloudFront is AWS's Content Delivery Network (CDN) service that utilizes the global network of Edge Locations to cache and deliver content (like web pages, videos, APIs) to users with low latency.
    </details>

37. If a company has strict data residency requirements mandating that customer data must remain within a specific country (e.g., Germany), how does the AWS Global Infrastructure help meet this?
    - A. By automatically replicating data across all Regions.
    - B. By allowing the company to select a specific AWS Region located within that country (e.g., eu-central-1 Frankfurt).
    - C. By using Edge Locations within that country.
    - D. By encrypting all data globally.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Customers retain control over the Region(s) in which their data is stored. By choosing a Region located within the required country/jurisdiction, companies can meet data residency requirements. Data is not moved outside a chosen Region without explicit customer action.
    </details>

38. What connects Availability Zones within an AWS Region?
    - A. Public internet connections.
    - B. High-bandwidth, low-latency private networking.
    - C. Satellite links.
    - D. Dedicated carrier pigeons.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Availability Zones within a Region are interconnected with high-bandwidth, low-latency networking, allowing for fast and reliable communication between resources deployed across different AZs for high availability.
    </details>

39. Which component of the AWS Global Infrastructure would you use to establish a dedicated private connection from your on-premises data center to AWS?
    - A. AWS VPN
    - B. AWS Direct Connect
    - C. Amazon CloudFront
    - D. AWS Availability Zone

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Direct Connect provides a dedicated, private network connection between a customer's premises and AWS, bypassing the public internet.
    </details>

40. What is the primary difference between an AWS Region and an AWS Local Zone?
    - A. Regions have multiple AZs, while Local Zones are single data centers.
    - B. Local Zones are extensions of a Region designed to place compute, storage, and other select services closer to end-users or specific population centers.
    - C. Local Zones offer all AWS services, while Regions offer only a subset.
    - D. Regions are free to use, while Local Zones incur additional charges.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Local Zones are extensions of an AWS Region that bring select AWS services closer to specific geographic areas or population centers, primarily to support applications requiring single-digit millisecond latency to end-users.
    </details>

41. How does AWS ensure the physical security of its data centers?
    - A. By publishing the exact addresses of all data centers.
    - B. By allowing public tours of the facilities.
    - C. Through strict access controls, surveillance, and environmental security measures managed by AWS.
    - D. By relying solely on local law enforcement.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS manages the physical security of its data centers (part of security OF the cloud) using multiple layers of controls, including access authorization, surveillance, environmental protections, and operational expertise.
    </details>

42. Which AWS offering allows customers to operate AWS infrastructure on-premises for a consistent hybrid experience?
    - A. AWS Outposts
    - B. AWS Local Zones
    - C. AWS Wavelength
    - D. AWS Regions

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: AWS Outposts bring native AWS services, infrastructure, and operating models to virtually any data center, co-location space, or on-premises facility for a truly consistent hybrid experience.
    </details>

43. What is the main goal of designing applications across multiple Availability Zones?
    - A. To reduce costs.
    - B. To achieve high availability and fault tolerance.
    - C. To simplify application architecture.
    - D. To increase network latency.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Spreading application components across multiple AZs ensures that if one AZ becomes unavailable due to a power outage, flood, or other disaster, the application can continue running using resources in the other AZs.
    </details>

44. Which AWS global infrastructure component is specifically designed to deliver applications with ultra-low latency to mobile devices and end-users over 5G networks?
    - A. AWS Regions
    - B. AWS Availability Zones
    - C. AWS Local Zones
    - D. AWS Wavelength

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: AWS Wavelength embeds AWS compute and storage services within telecommunications providers’ 5G networks, enabling developers to build applications that require ultra-low latency to mobile devices and end-users.
    </details>

45. As of early 2025, approximately how many AWS Regions are operational globally?
    - A. Around 10
    - B. Around 20
    - C. Around 35-40
    - D. Over 100

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Based on information from late 2024/early 2025, AWS operates around 36 geographic Regions globally, with plans for more.
    </details>

46. Which statement accurately describes the relationship between AWS Global Infrastructure and compliance?
    - A. Using AWS automatically makes an application compliant with all regulations.
    - B. AWS provides compliance certifications for its infrastructure, and customers can build compliant applications on top.
    - C. Compliance is solely the customer's responsibility, regardless of AWS infrastructure.
    - D. AWS Regions do not impact compliance considerations.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS infrastructure is compliant with numerous global standards (e.g., ISO 27001, SOC 1/2/3, PCI DSS). Customers inherit these controls and can leverage AWS services and guidance to build applications that meet their specific compliance requirements, often tied to data location (Regions).
    </details>

47. What is the term for the AWS infrastructure designed to support workloads requiring specific sovereignty controls, like the planned AWS European Sovereign Cloud?
    - A. Standard Regions
    - B. Local Zones
    - C. Sovereign Clouds/Regions
    - D. Edge Locations

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS is developing specific Sovereign Cloud regions (like the planned European Sovereign Cloud) designed to meet stringent data residency, operational control, and sovereignty requirements for customers in specific jurisdictions.
    </details>

48. Can customers choose the specific data center within an Availability Zone where their resources are deployed?
    - A. Yes, by specifying the data center ID.
    - B. Yes, but only for Dedicated Hosts.
    - C. No, AWS manages the placement of resources within an AZ for customers.
    - D. No, resources are randomly assigned across all AZs in a Region.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: While an AZ consists of one or more data centers, customers deploy resources to an AZ, and AWS handles the specific placement within the data center(s) comprising that AZ. Customers do not select individual data centers.
    </details>

49. What is a key benefit of using AWS Regions located closer to your users?
    - A. Higher data transfer costs.
    - B. Increased application latency.
    - C. Lower application latency.
    - D. Fewer available AWS services.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Deploying applications in AWS Regions geographically closer to the majority of end-users reduces the physical distance data must travel, resulting in lower network latency and a better user experience.
    </details>

50. Which part of the AWS Global Infrastructure map represents the highest level of geographic distribution?
    - A. Availability Zones
    - B. Edge Locations
    - C. Regions
    - D. Data Centers

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Regions represent the largest geographic footprint, encompassing multiple Availability Zones spread across a distinct geographical area (like North America, Europe, Asia Pacific).
    </details>

