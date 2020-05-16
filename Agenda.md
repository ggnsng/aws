# AWS-SAA

## Day01

- Basics of Cloud Computing 
- [The NIST definition of cloud computing](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-145.pdf)
- [Introduction and History of AWS](https://techcrunch.com/2016/07/02/andy-jassys-brief-history-of-the-genesis-of-aws/)
- [Certification Roadmap](https://aws.amazon.com/certification/)
- [AWS Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/)
- [Regions, Availability Zones, Local Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html) and [Edge Network Locations](https://aws.amazon.com/about-aws/global-infrastructure/regional-product-services/#AWS_Edge_Network_Locations)
- [Free tier account creation](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/) and [coverage](https://aws.amazon.com/free/)
- Exploring the AWS Management Console
- [Setting up free tier billing alerts](https://docs.aws.amazon.com/awsaccountbilling/latest/aboutv2/tracking-free-tier-usage.html)
- [AWS Documentation](https://docs.aws.amazon.com/index.html)
- [Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/) (to be revisited)

### [AWS Identity and Access Management](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)

<details>
  <summary>Owner's account AKA The root user</summary>
  
[The AWS Account Root User](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_root-user.html) and [only when to use it](https://docs.aws.amazon.com/general/latest/gr/aws_tasks-that-require-root.html)
</details>

<details>
  <summary>IAM Users</summary>
  
An AWS IAM user is an entity that you create in AWS to represent the person or service that uses it to interact with AWS. IAM Users have a set of permanent credentials such as an Access Key and/or Console ID-Password. You attach permission policies to the IAM user that determine what the user can and cannot do in AWS.
The console ID-password is used to access the services in the AWS account through the browser interface.
Access keys are a combination of an access key ID and a secret access key that are assigned to a user. These can be used to make programmatic calls to AWS when using the API in program code or at a command prompt when using the AWS CLI.
</details>

<details>
  <summary>IAM Groups</summary>
  
  If you find that you'll have several users who need similar permissions, you can define an IAM Group and associate your users to the group.
  
</details>

<details>
  <summary>IAM Policies (AWS Managed, Customer managed, Inline)</summary>
  
  By default, all permissions are denied unless explicitly granted. You may select predefined permissions from the list of AWS Managed Policies or define your own custom IAM policies.
  AWS Managed policies are common across all AWS customers. We can only use them but cannot modify/delete them. Customer-managed policies provide more precise control over your policies than AWS managed policies.
</details>

<details>
  <summary>IAM Roles (to be revisited)</summary>
  IAM Roles are used to provide temporary security credentials to any principal. One common case is allowing the EC2 service to distribute credentials to your application code running on an EC2 instance. Roles can also enable other scenarios in the enterprise such as cross-account access and identity federation.
  

</details>

<details>
  <summary>MFA</summary>
  
NA
</details>

### Network

- VPC
  - IGW
  - Subnets
  - RouteTables
  - NAT Gateway, NAT Instance; Comparison
  - NACL (Stateless)
  - Security Groups (Stateful)
  - NACL vs SG
  - Elastic IP

[Lab01](https://github.com/ashydv/aws-labs/blob/master/SAA-Lab01.md)

### Compute

- EC2
  - Creation Modification, Deletion
  - [Userdata, Metadata (Comparison)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html)
  - [EC2 purchasing Options](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-purchasing-options.html), [Tenancy](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/dedicated-instance.html)
  - Auto Scaling and Loadbalancing

## Day 02

- VPC Peering, Transit Gateway
- VPN Options
- DirectConnect
- VPC Endpoints (to be revisited)

### Storage

- EBS  
  - Types  
    - Creation, Modification, Snapshots, Deletion, Movement
- S3
  - Pricing
  - Versioning
  - Static Website Hosting
  - Pre-signed url
  - ACL and Bucket Policy
  - S3 tiers
  - CRR, Transfer Acceleration
  - Life Cycle Policy
- Glacier
- CLI and Roles Lab
- CloudFront
- EFS
- Storage Gateway
- Snow family

### Automation

- CloudFormation
- Elastic Beanstalk
- OpsWorks

### Application Integration/Decoupling

- SQS
- SNS
- SWF
- SES


[Lab02](https://github.com/ashydv/aws-labs/blob/master/SAA-Lab02.md)

## Day 03

### Databases

- RDS
  - Supported engines
    - Creation, modification and deletion
- ElastiCache
- DynamoDB
- RedShift

### Others

- Kinesis
- Route 53
- CloudWatch
- CloudTrail
- Trusted Advisor
- HSM
- ECS, ECR, EKS
- Lambda

[SAA-Lab03](https://github.com/ashydv/aws-labs/blob/master/SAA-Lab03.md)

### Wrap up

- [Simple Monthly Calculator](https://calculator.s3.amazonaws.com/index.html), [AWS TCO Calculator](https://awstcocalculator.com/)
- [AWS Services quotas](https://docs.aws.amazon.com/general/latest/gr/aws_service_limits.html)
- Scope of service e.g. Global, Regional and AZ resources
- Well-Architected Framework
- reInvent, breakout sessions, aws.training, whitepapers, customer use cases, this is my architecture
- AWS Blog, AWS Online Tech Talks
