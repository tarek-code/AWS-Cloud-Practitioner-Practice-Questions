# AWS Cloud Practitioner Practice Questions - Batch 3 (IAM)

51. What is AWS Identity and Access Management (IAM)?
    - A. A service for managing domain names.
    - B. A global service that allows you to manage access to AWS services and resources securely.
    - C. A regional service for provisioning virtual servers.
    - D. A tool for monitoring application performance.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: IAM is a global AWS service that enables you to manage users, groups, roles, and their permissions to AWS resources securely.
    </details>

52. What is the recommended best practice for the AWS account root user?
    - A. Use the root user for daily administrative tasks.
    - B. Share the root user credentials with the entire team.
    - C. Avoid using the root user for everyday tasks; secure it with a strong password and MFA.
    - D. Delete the root user account after creating IAM users.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The root user has unrestricted access. Best practice is to secure it (strong password, MFA) and use it only for tasks that specifically require it (like initial account setup or closing the account). Create IAM users for daily tasks.
    </details>

53. In IAM, what is the primary purpose of creating Groups?
    - A. To assign permissions directly to multiple EC2 instances.
    - B. To organize users and easily manage permissions for multiple users at once.
    - C. To define network access control lists.
    - D. To monitor AWS resource usage.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: IAM Groups are collections of IAM users. You can attach permission policies to a group, and all users within that group inherit those permissions, simplifying access management.
    </details>

54. Can an IAM Group contain other IAM Groups?
    - A. Yes, groups can be nested for complex hierarchies.
    - B. No, IAM Groups can only contain IAM Users.
    - C. Yes, but only up to two levels deep.
    - D. Only if the groups are in the same Availability Zone.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: IAM Groups cannot be nested; they can only contain IAM users.
    </details>

55. How are permissions defined and assigned in IAM?
    - A. Through configuration files stored on EC2 instances.
    - B. Using JSON documents called Policies, which are attached to users, groups, or roles.
    - C. By assigning users to specific Availability Zones.
    - D. Through network routing tables.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Permissions in AWS are defined using IAM Policies, which are JSON documents specifying allowed or denied actions on specific resources. These policies are attached to IAM identities (users, groups, roles).
    </details>

56. What is the principle of least privilege in the context of IAM?
    - A. Granting all users administrator access by default.
    - B. Granting only the minimum permissions necessary for a user or service to perform its required tasks.
    - C. Assigning permissions based on the user's physical location.
    - D. Allowing users to define their own permissions.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: The principle of least privilege is a security best practice that dictates granting only the permissions required to perform a specific task and no more.
    </details>

57. What is Multi-Factor Authentication (MFA) in AWS?
    - A. A method for encrypting data at rest.
    - B. A way to share access keys securely.
    - C. An additional layer of security requiring users to provide a second form of authentication besides their password.
    - D. A tool for analyzing AWS costs.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: MFA adds an extra layer of security by requiring users to provide something they know (password) plus something they have (e.g., a code from a virtual or hardware MFA device) to log in.
    </details>

58. Which of the following are valid MFA options supported by AWS IAM? (Choose TWO)
    - A. Email confirmation codes.
    - B. Virtual MFA devices (e.g., Google Authenticator, Authy).
    - C. SMS text messages.
    - D. U2F / FIDO Security Keys (e.g., YubiKey).
    - E. Handwritten notes.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B, D
      Explanation: AWS supports virtual MFA devices (authenticator apps), U2F/FIDO hardware security keys, and hardware key fob MFA devices. SMS is not recommended or typically used for standard IAM user MFA.
    </details>

59. What are AWS Access Keys used for?
    - A. Logging into the AWS Management Console.
    - B. Encrypting EBS volumes.
    - C. Authenticating programmatic access to AWS services (via CLI, SDK, API).
    - D. Connecting to EC2 instances via SSH.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Access Keys (composed of an Access Key ID and a Secret Access Key) are credentials used to authenticate requests made programmatically via the AWS CLI, SDKs, or direct API calls.
    </details>

60. What is an IAM Role?
    - A. A collection of IAM users.
    - B. A set of permissions that can be assumed by trusted entities (like EC2 instances, AWS services, or users from another account).
    - C. A type of security group.
    - D. A billing construct for grouping costs.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: An IAM Role is an identity with permission policies that determine what the identity can and cannot do in AWS. Roles do not have standard long-term credentials like passwords or access keys. Instead, when an entity assumes a role, it gets temporary security credentials.
    </details>

61. Why is it generally more secure to use IAM Roles for applications running on EC2 instances instead of storing Access Keys directly on the instance?
    - A. Roles provide permanent credentials that never expire.
    - B. Roles automatically rotate credentials, eliminating the need to manage long-term keys on the instance.
    - C. Roles grant broader permissions than Access Keys.
    - D. Access Keys are easier to guess than Role names.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: IAM Roles provide temporary security credentials to the EC2 instance automatically. This avoids the risk associated with storing long-term Access Keys directly on the instance, which could be compromised.
    </details>

62. Which IAM tool provides a report listing all users in your account and the status of their credentials (password, access keys, MFA)?
    - A. IAM Access Advisor
    - B. AWS Config
    - C. IAM Credentials Report
    - D. AWS Trusted Advisor

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The IAM Credentials Report is an account-level report that lists all IAM users and the status of their various credentials, including password age, access key age, and MFA status.
    </details>

63. Which IAM tool helps you review permissions by showing the services a user has permissions for and when those services were last accessed?
    - A. IAM Credentials Report
    - B. IAM Access Advisor
    - C. AWS CloudTrail
    - D. Amazon Inspector

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: The IAM Access Advisor shows the service permissions granted to a user, group, or role and when those services were last accessed, helping identify unused permissions that can potentially be removed (following the least privilege principle).
    </details>

64. What feature allows you to enforce password complexity requirements and rotation policies for IAM users?
    - A. Security Groups
    - B. IAM Roles
    - C. IAM Password Policy
    - D. AWS WAF

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The account-level IAM Password Policy allows administrators to set requirements like minimum length, character types, password expiration, and prevention of password reuse for IAM user passwords.
    </details>

65. Under the Shared Responsibility Model for IAM, what is AWS responsible for?
    - A. Creating and managing IAM users and groups.
    - B. Defining and managing IAM policies.
    - C. Securing the underlying infrastructure that runs the IAM service.
    - D. Enabling MFA for all users.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS is responsible for the security OF the cloud, which includes the infrastructure, hardware, software, networking, and facilities that run AWS services like IAM. The customer is responsible for managing users, groups, roles, policies, and enabling security best practices like MFA (security IN the cloud).
    </details>

66. What are the components of an AWS Access Key? (Choose TWO)
    - A. User Name
    - B. Access Key ID
    - C. Password
    - D. Secret Access Key
    - E. MFA Code

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B, D
      Explanation: An AWS Access Key consists of two parts: an Access Key ID (like a username) and a Secret Access Key (like a password). Both are required for programmatic authentication.
    </details>

67. Which IAM entity is best suited for granting temporary access to AWS resources for users federated from a corporate directory?
    - A. IAM User with long-term Access Keys.
    - B. IAM Group.
    - C. IAM Role.
    - D. Root Account.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: IAM Roles are designed to be assumed by trusted entities. For federated users (e.g., via SAML 2.0 or OpenID Connect), they authenticate with their corporate identity provider and then assume an IAM Role to receive temporary AWS credentials.
    </details>

68. What is the recommended way to grant permissions to an application running on an AWS Lambda function?
    - A. Create an IAM user and embed its access keys in the Lambda code.
    - B. Assign an IAM Role (Execution Role) to the Lambda function.
    - C. Store root account credentials in Lambda environment variables.
    - D. Configure a security group for the Lambda function.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: Similar to EC2 instances, the best practice for Lambda functions is to assign an IAM Execution Role. The function automatically assumes this role and receives temporary credentials to interact with other AWS services based on the role's permissions.
    </details>

69. You need to provide a third-party auditor with read-only access to your AWS environment configuration. Which approach follows best practices?
    - A. Give them the root user credentials.
    - B. Create an IAM user for the auditor with the `AdministratorAccess` managed policy.
    - C. Create an IAM user for the auditor with a custom policy granting only necessary read-only permissions (least privilege).
    - D. Create an IAM role with read-only access and allow the auditor's AWS account to assume it.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: D
      Explanation: Creating a cross-account IAM role with specific read-only permissions is the most secure method. It allows the auditor to use their own AWS account credentials to assume the role in your account, granting temporary, limited access without needing to manage IAM users or keys for them.
    </details>

70. What does an IAM policy statement with `"Effect": "Deny"` do?
    - A. It explicitly allows the specified actions on the specified resources.
    - B. It has no effect if an `Allow` statement exists for the same action.
    - C. It explicitly prohibits the specified actions on the specified resources, overriding any `Allow` statements.
    - D. It grants permissions only if certain conditions are met.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: An explicit `Deny` in an IAM policy always overrides any `Allow` statements. This is a key mechanism for restricting access even if broader permissions are granted elsewhere.
    </details>

71. Where are IAM users, groups, roles, and policies managed?
    - A. Within a specific AWS Region.
    - B. Globally, across all AWS Regions.
    - C. Within a specific Availability Zone.
    - D. Within a specific VPC.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: B
      Explanation: IAM is a global service. Identities (users, groups, roles) and policies created in IAM are available across all AWS Regions.
    </details>

72. What is the purpose of the `Principal` element in an IAM policy (especially resource-based policies)?
    - A. To specify the actions that are allowed or denied.
    - B. To specify the resources the policy applies to.
    - C. To specify the user, account, service, or other entity that is allowed or denied access.
    - D. To specify conditions under which the policy is effective.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The `Principal` element identifies the IAM user, IAM role, AWS account, AWS service, or other principal entity that is allowed or denied access to a resource in a resource-based policy (like an S3 bucket policy or a role trust policy).
    </details>

73. Which AWS CLI command is used to configure your credentials for programmatic access?
    - A. `aws login`
    - B. `aws iam create-user`
    - C. `aws configure`
    - D. `aws sts assume-role`

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: The `aws configure` command is used to set up your AWS access key ID, secret access key, default region name, and default output format for the AWS CLI.
    </details>

74. A developer needs to allow their EC2 instance to upload files to an S3 bucket. What is the most secure way to grant these permissions?
    - A. Hardcode AWS root user credentials in the application.
    - B. Create an IAM user with S3 write permissions and store its access keys on the EC2 instance.
    - C. Create an IAM role with S3 write permissions and attach it to the EC2 instance profile.
    - D. Configure the S3 bucket to allow public write access.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: Using an IAM role attached to the EC2 instance profile allows the instance to obtain temporary credentials automatically, avoiding the need to store long-term keys on the instance. This is the recommended best practice.
    </details>

75. What is the primary function of the AWS SDKs (Software Development Kits)?
    - A. To provide a command-line interface for managing AWS resources.
    - B. To offer pre-configured virtual machine images.
    - C. To simplify using AWS services from within applications using popular programming languages.
    - D. To manage network security rules.

    <details markdown=1><summary markdown=\"span\">Answer</summary>
      Correct answer: C
      Explanation: AWS SDKs provide language-specific APIs (libraries) that make it easier for developers to integrate AWS service functionalities into their applications without needing to handle the low-level API calls directly.
    </details>

