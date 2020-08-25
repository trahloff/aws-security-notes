# AWS Certified Security Specialist



## Active Directory

- OnPrem access to EC2-hosted AD: NACLs + SGs
- MFA for Monitor and Notify on AWS Account Root User Activity: enable directly at service level
- Transport encryption: LDAP over SSL
- Managed MS AD: lock out user after number of failed logons: password policy in directory service


## Cloudwatch

-  Monitor and Notify on AWS Account Root User Activity -> CloudWatch Rule + SNS


## Kinesis

- KCL 
  - Permissions: "your
    policy must include permissions for Amazon **DynamoDB** and Amazon **CloudWatch**; the KCL
    uses DynamoDB to
    track state information for the application, and CloudWatch to send KCL metrics to
    CloudWatch" https://docs.aws.amazon.com/streams/latest/dev/controlling-access.html
- Monitoring
  - Basic -> Stream-Level
  - Enhanced -> Shard-Level
- Encryption
  - Send data to S3 w/ KMS -> kms:Decrypt + kms:GenerateDataKey
- Access Kinesis w/o internet: VPC Endpoint **Interface**
- Kinesis Data Streams + Lambda: 
  1. Service role of the type AWS **Lambda**
  2. AWSLambdaKinesisExecutionRole


## KMS

- Simply encrypt file via CLI
  1. Create new CMK
  2. Use AWS encryption CLI to encrypt file with CMK
- IAM Permissions needed for use of CMK:
  1. kms:Encrypt
  2. kms:Decrypt
  3. kms:ReEncrypt*
  4. kms:GenerateDataKey*
- DynamoDB "enable encryption" automatically encrypts keys, indices, etc


## IAM

- 


## WAF

- ALB + CloudFront
- Logs: S3+ Kinesis Firehose



