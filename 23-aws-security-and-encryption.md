# AWS Security and Encryption

`1 - To enable In-flight Encryption (In-Transit Encryption), we need to have ........................`

a HTTPS endpoint with an SSL certificate. In-flight Encryption = HTTPS, and HTTPS can not be enabled without an SSL certificate.

`2 - Server-Side Encryption means that the data is sent encrypted to the server.`

False. Server-Side Encryption means the server will encrypt the data for us. We don't need to encrypt it beforehand.

`3 - In Server-Side Encryption, where do the encryption and decryption happen?`

Both encryption and decryption happen on the server. In Server-Side Encryption, we can't do encryption/decryption ourselves as we don't have access to the corresponding encryption key.

`4 - In Client-Side Encryption, the server must know our encryption scheme before we can upload the data.`

False. With Client-Side Encryption, the server doesn't need to know any information about the encryption scheme being used, as the server will not perform any encryption or decryption operations.

`5 - You need to create KMS Keys in AWS KMS before you are able to use the encryption features for EBS, S3, RDS ...`

False. You can use the AWS Managed Service keys in KMS, therefore we don't need to create our own KMS keys.

`6 - AWS KMS supports both symmetric and asymmetric KMS keys.`

True. KMS keys can be symmetric or asymmetric. A symmetric KMS key represents a 256-bit key used for encryption and decryption. An asymmetric KMS key represents an RSA key pair used for encryption and decryption or signing and verification, but not both. Or it represents an elliptic curve (ECC) key pair used for signing and verification.

`7 - When you enable Automatic Rotation on your KMS Key, the backing key is rotated every .................`

1 year.

`8 - You have an AMI that has an encrypted EBS snapshot using KMS CMK. You want to share this AMI with another AWS account. You have shared the AMI with the desired AWS account, but the other AWS account still can't use it. How would you solve this problem?`

You need to share the KMS CMK used to encrypt the AMI with the other AWS account

`9 - You have created a Customer-managed CMK in KMS that you use to encrypt both S3 buckets and EBS snapshots. Your company policy mandates that your encryption keys be rotated every 3 months. What should you do?`

Rotate the KMS CMK manually. Create a new KMS CMK and use Key Aliases to reference the new KMS CMK. Keep the old KMS CMK so you can decrypt the old data.

`10 - What should you use to control access to your KMS CMKs?`

KMS Key Policies.

`11 - You have a Lambda function used to process some data in the database. You would like to give your Lambda function access to the database password. Which of the following options is the most secure?`

Have it as an encrypted environment variable and decrypt it at runtime

`12 - You have a secret value that you use for encryption purposes, and you want to store and track the values of this secret over time. Which AWS service should you use?`

SSM Parameter Store. SSM Parameters Store can be used to store secrets and has built-in version tracking capability. Each time you edit the value of a parameter, SSM Parameter Store creates a new version of the parameter and retains the previous versions. You can view the details, including the values, of all versions in a parameter's history.

`13 - Your user-facing website is a high-risk target for DDoS attacks and you would like to get 24/7 support in case they happen and AWS bill reimbursement for the incurred costs during the attack. What AWS service should you use?`

AWS Shield Advanced.

`14 - You would like to externally maintain the configuration values of your main database, to be picked up at runtime by your application. What's the best place to store them to maintain control and version history?`

SSM Parameter Store.

`15 - AWS GuardDuty scans the following data sources, EXCEPT ................`

CloudWatch logs.

`16 - You have a website hosted on a fleet of EC2 instances fronted by an Application Load Balancer. What should you use to protect your website from common web application attacks (e.g., SQL Injection)?`

AWS WAF.

`17 - You would like to analyze OS vulnerabilities from within EC2 instances. You need these analyses to occur weekly and provide you with concrete recommendations in case vulnerabilities are found. Which AWS service should you use?`

Amazon Inspector.

`18 - What is the most suitable AWS service for storing RDS DB passwords which also provides you automatic rotation?`

AWS Secrets Manager.

`19 - Which AWS service allows you to centrally manage EC2 Security Groups and AWS Shield Advanced across all AWS accounts in your AWS Organization?`

AWS Firewall Manager. AWS Firewall Manager is a security management service that allows you to centrally configure and manage firewall rules across your accounts and applications in AWS Organizations. It is integrated with AWS Organizations so you can enable AWS WAF rules, AWS Shield Advanced protection, security groups, AWS Network Firewall rules, and Amazon Route 53 Resolver DNS Firewall rules.

`20 - Which AWS service helps you protect your sensitive data stored in S3 buckets?`

Amazon Macie. Amazon Macie is a fully managed data security service that uses Machine Learning to discover and protect your sensitive data stored in S3 buckets. It automatically provides an inventory of S3 buckets including a list of unencrypted buckets, publicly accessible buckets, and buckets shared with other AWS accounts. It allows you to identify and alert you to sensitive data, such as Personally Identifiable Information (PII).

`21 - An online-payment company is using AWS to host its infrastructure. The frontend is created using VueJS and is hosted on an S3 bucket and the backend is developed using PHP and is hosted on EC2 instances in an Auto Scaling Group. As their customers are worldwide, they use both CloudFront and Aurora Global database to implement multi-region deployments to provide the lowest latency and provide availability, and resiliency. A new feature required which gives customers the ability to store data encrypted on the database and this data must not be disclosed even by the company admins. The data should be encrypted on the client side and stored in an encrypted format. What do you recommend to implement this?`

Using Aurora Client-Side Encryption and KMS Multi-region Keys.

`22 - You have an S3 bucket that is encrypted with SSE-KMS. You have been tasked to replicate the objects to a target bucket in the same AWS region but with a different KMS Key. You have configured the S3 replication, the target bucket, and the target KMS key and it is still not working. What is missing to make the S3 replication work?`

You have to configure permissions for both Source KMS Key `kms:Decrypt` and Target KMS Key `kms:Encrypt` to be used by the S3 Replication Service.

`23 - You have generated a public certificate using LetsEncrypt and uploaded it to the ACM so you can use and attach to an Application Load Balancer that forwards traffic to EC2 instances. As this certificate is generated outside of AWS, it does not support the automatic renewal feature. How would you be notified 30 days before this certificate expires so you can manually generate a new one?`

Configure EventBridge for Daily Expiration Events from ACM to invoke SNS notifications to your email.

`24 - You have created the main Edge-Optimized API Gateway in us-west-2 AWS region. This main Edge-Optimized API Gateway forwards traffic to the second level API Gateway in ap-southeast-1. You want to secure the main API Gateway by attaching an ACM certificate to it. Which AWS region are you going to create the ACM certificate in?`

As the Edge-Optimized API Gateway is using a custom AWS managed CloudFront distribution behind the scene to route requests across the globe through CloudFront Edge locations, the ACM certificate must be created in us-east-1.

`25 - You are managing an AWS Organization with multiple AWS accounts. Each account has a separate application with different resources. You want an easy way to manage Security Groups and WAF Rules across those accounts as there was a security incident the last week and you want to tighten up your resources. Which AWS service can help you to do so?`

AWS Firewal Manager.
