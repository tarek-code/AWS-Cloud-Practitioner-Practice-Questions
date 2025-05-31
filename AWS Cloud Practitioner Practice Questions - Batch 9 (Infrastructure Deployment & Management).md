# AWS Cloud Practitioner Practice Questions - Batch 9 (Infrastructure Deployment & Management)

201. Which AWS service allows you to model and provision your AWS infrastructure resources using templates (Infrastructure as Code)?
    - A. AWS Systems Manager
    - B. AWS Config
    - C. AWS CloudFormation
    - D. AWS Elastic Beanstalk

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS CloudFormation provides a common language (using JSON or YAML templates) to describe and provision all the infrastructure resources in your cloud environment safely and predictably.
    </details>

202. What is the primary benefit of using Infrastructure as Code (IaC) with services like CloudFormation?
    - A. It eliminates the need for monitoring.
    - B. It allows infrastructure to be managed programmatically, enabling automation, version control, and repeatability.
    - C. It provides free compute resources.
    - D. It automatically optimizes application performance.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: IaC treats infrastructure provisioning and management like software development, bringing benefits like automation, consistency, versioning via source control, and reduced manual errors.
    </details>

203. What is a CloudFormation Stack?
    - A. A template file written in JSON or YAML.
    - B. A collection of AWS resources that you manage as a single unit, created from a CloudFormation template.
    - C. A visualization of resource dependencies.
    - D. A service for monitoring resource configurations.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: When you use a CloudFormation template to create resources, they are managed together as a single unit called a stack. You can create, update, or delete a collection of resources by managing the stack.
    </details>

204. What is AWS Systems Manager?
    - A. A service for provisioning infrastructure using templates.
    - B. A unified interface that provides operational visibility and control over your AWS infrastructure.
    - C. A relational database service.
    - D. A content delivery network.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Systems Manager gives you visibility and control of your infrastructure on AWS. It provides a unified user interface so you can view operational data from multiple AWS services and allows you to automate operational tasks across your AWS resources.
    </details>

205. Which Systems Manager capability allows you to automate operational tasks like patching, software installation, or configuration updates across a fleet of instances?
    - A. Systems Manager Parameter Store
    - B. Systems Manager OpsCenter
    - C. Systems Manager Automation (Runbooks)
    - D. Systems Manager Inventory

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Systems Manager Automation simplifies common maintenance and deployment tasks using pre-defined or custom runbooks. These runbooks can perform tasks like creating AMIs, patching instances, or running scripts.
    </details>

206. Which Systems Manager capability provides secure storage for configuration data and secrets (like passwords or API keys)?
    - A. Systems Manager Session Manager
    - B. Systems Manager Patch Manager
    - C. Systems Manager Parameter Store
    - D. Systems Manager Distributor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Parameter Store provides secure, hierarchical storage for configuration data management and secrets management. You can store data such as passwords, database strings, and license codes as parameter values.
    </details>

207. Which Systems Manager capability allows you to securely connect to your EC2 instances (Linux or Windows) via a browser-based shell or CLI without needing SSH keys or bastion hosts?
    - A. Systems Manager Automation
    - B. Systems Manager Run Command
    - C. Systems Manager Session Manager
    - D. Systems Manager Patch Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Session Manager provides secure and auditable instance management without the need to open inbound ports, manage SSH keys, or use bastion hosts. Access is controlled via IAM policies.
    </details>

208. Which Systems Manager capability allows you to remotely execute commands or scripts on a set of managed instances?
    - A. Systems Manager Session Manager
    - B. Systems Manager Run Command
    - C. Systems Manager Inventory
    - D. Systems Manager OpsCenter

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Run Command lets you remotely and securely manage the configuration of your managed instances at scale. You can use it to execute commands or scripts on demand.
    </details>

209. Which Systems Manager capability helps automate the process of patching managed instances for both operating system and application updates?
    - A. Systems Manager Parameter Store
    - B. Systems Manager Patch Manager
    - C. Systems Manager State Manager
    - D. Systems Manager Automation

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Patch Manager automates the process of patching fleets of managed nodes (EC2 instances, on-premises servers, VMs) with both security-related and other types of updates.
    </details>

210. What is the purpose of Systems Manager State Manager?
    - A. To store configuration secrets.
    - B. To provide secure remote access to instances.
    - C. To ensure that your instances and infrastructure are in a defined, consistent state (e.g., specific software installed, security settings configured).
    - D. To collect software inventory from instances.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: State Manager helps maintain infrastructure consistency by defining desired state configurations (e.g., ensuring antivirus software is installed and running) and automatically applying them to managed nodes at specified intervals.
    </details>

211. What is required for an EC2 instance to be managed by AWS Systems Manager?
    - A. The instance must have a public IP address.
    - B. The instance must be running a specific Linux distribution.
    - C. The SSM Agent must be installed and running on the instance, and the instance must have appropriate IAM permissions.
    - D. The instance must be part of an Auto Scaling group.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Instances need the SSM Agent installed and configured, network connectivity to the Systems Manager service endpoints, and an IAM instance profile granting necessary permissions to communicate with the service.
    </details>

212. Can AWS Systems Manager be used to manage servers located outside of AWS (on-premises or in other clouds)?
    - A. No, Systems Manager only works with EC2 instances.
    - B. Yes, by installing the SSM Agent and registering them as managed instances (hybrid activations).
    - C. Only if they are connected via AWS Direct Connect.
    - D. Only for Windows servers.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Systems Manager supports hybrid environments. You can install the SSM Agent on on-premises servers or VMs in other clouds and register them with Systems Manager to manage them alongside your EC2 instances.
    </details>

213. What is a CloudFormation Change Set?
    - A. A log of all changes made to a stack.
    - B. A preview of the changes CloudFormation will make to your stack resources before you execute them.
    - C. A way to roll back a stack to a previous state.
    - D. A template snippet that can be reused.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Change Sets allow you to preview how proposed changes to a stack might impact your running resources before implementing them. This helps catch potential issues before updating the stack.
    </details>

214. What happens if a resource fails to create during a CloudFormation stack launch?
    - A. CloudFormation stops and waits for manual intervention.
    - B. CloudFormation skips the failed resource and continues creating others.
    - C. By default, CloudFormation rolls back the entire stack, deleting any resources it successfully created.
    - D. CloudFormation automatically retries creating the resource indefinitely.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The default behavior upon failure is to roll back the stack creation process, deleting all resources created so far to return the environment to its previous state (usually empty).
    </details>

215. Which AWS service provides managed Chef and Puppet configuration management platforms?
    - A. AWS CloudFormation
    - B. AWS Systems Manager
    - C. AWS OpsWorks (for Chef Automate / for Puppet Enterprise)
    - D. AWS Elastic Beanstalk

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS OpsWorks provides managed instances of Chef Automate and Puppet Enterprise, helping automate how servers are configured, deployed, and managed across EC2 instances or on-premises compute environments.
    </details>

216. Which CloudFormation feature allows you to manage stacks across multiple AWS accounts and Regions from a central administrator account?
    - A. CloudFormation Change Sets
    - B. CloudFormation StackSets
    - C. CloudFormation Drift Detection
    - D. CloudFormation Nested Stacks

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: StackSets extend the functionality of stacks by enabling you to create, update, or delete stacks across multiple accounts and Regions with a single operation.
    </details>

217. What does CloudFormation Drift Detection help you identify?
    - A. Differences between the expected template configuration and the actual configuration of stack resources.
    - B. Cost overruns in your stack resources.
    - C. Performance bottlenecks in your application.
    - D. Security vulnerabilities in your template.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: A
      Explanation: Drift detection helps identify resources within a stack whose actual configuration differs from the configuration defined in the CloudFormation template (e.g., if someone manually changed a security group rule outside of CloudFormation).
    </details>

218. Which Systems Manager capability provides a central place to view, investigate, and resolve operational issues (OpsItems) impacting AWS resources?
    - A. Systems Manager Explorer
    - B. Systems Manager OpsCenter
    - C. Systems Manager Distributor
    - D. Systems Manager Maintenance Windows

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: OpsCenter aggregates operational issues (OpsItems) from various sources (like CloudWatch alarms, EventBridge events) and provides tools and runbooks to investigate and remediate them.
    </details>

219. Which Systems Manager capability allows you to define recurring windows of time to perform potentially disruptive actions like patching or updates?
    - A. Systems Manager State Manager
    - B. Systems Manager Maintenance Windows
    - C. Systems Manager Automation
    - D. Systems Manager Patch Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Maintenance Windows let you define schedules for running administrative and maintenance tasks across your instances, helping minimize impact on service availability.
    </details>

220. How are CloudFormation templates typically written?
    - A. In binary format.
    - B. Using proprietary AWS scripting language.
    - C. Using declarative JSON or YAML format.
    - D. As executable scripts (Bash, PowerShell).

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: CloudFormation templates are text files written in either JSON or YAML format, describing the AWS resources to be provisioned.
    </details>

221. Which section of a CloudFormation template is mandatory?
    - A. Parameters
    - B. Mappings
    - C. Resources
    - D. Outputs

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The `Resources` section is the only mandatory section in a CloudFormation template. It declares the AWS resources you want to include in the stack, such as EC2 instances, S3 buckets, or IAM roles.
    </details>

222. What is the purpose of the `Parameters` section in a CloudFormation template?
    - A. To define the AWS resources to be created.
    - B. To allow input values to be passed into the template when the stack is created or updated.
    - C. To declare output values that can be viewed after stack creation.
    - D. To define conditional logic for resource creation.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Parameters enable you to customize your templates by passing in values (e.g., instance type, database password) at runtime, making templates more reusable.
    </details>

223. Which Systems Manager feature allows you to securely distribute and install software packages (e.g., SSM Agent updates, custom software) to your managed instances?
    - A. Systems Manager Run Command
    - B. Systems Manager Distributor
    - C. Systems Manager Inventory
    - D. Systems Manager Parameter Store

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Distributor helps you package your own software—or find AWS-provided agent software packages—and distribute them to managed instances.
    </details>

224. Which AWS service provides a visual interface to design application architectures and provision them using CloudFormation or other tools?
    - A. AWS CloudShell
    - B. AWS Application Composer
    - C. AWS CodeStar
    - D. AWS Systems Manager Application Manager

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: AWS Application Composer helps developers simplify and accelerate architecting, configuring, and building serverless applications. You can drag, drop, and connect AWS services, and it generates CloudFormation or SAM templates.
    </details>

225. You need to ensure that a specific security agent is always installed and running on all your EC2 instances. Which Systems Manager capability is best suited for enforcing this configuration state?
    - A. Patch Manager
    - B. Session Manager
    - C. State Manager
    - D. Run Command

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: State Manager is designed to define and maintain consistent configuration states across your fleet. You can create an association that checks for the agent and installs/starts it if necessary on a defined schedule.
    </details>

