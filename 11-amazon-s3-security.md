# Amazon s3 Security

`1 - Your client wants to make sure that file encryption is happening in s3, but he wants to fully manage the encryption keys and never store them in AWS. You recommend him to use . . .`

SSE-C. With SSE-C the encryption happens in AWS and you have full control over the encryption keys.

`2 - A company You're working for once their data is starting S3 to be encrypted. They don't mind the encryption Keys stored in managed by AWS, but they want to maintain control over the rotation policy of the encryption key. You recommend them to use . . .`

SSE-KMS. With SSE-KMS the encryption happens in AWS, and the encryption keys are managed by AWS but you have full control of the rotation policy of the encryption key. Encryption Keys stored in AWS.

`3 - Your company does not dress AWS for the future process and wanted to happen on the application. You recommend them to use . . .`

Client side encryption. With client side encryption you have to do the encryption yourself and you have full control over the encryption keys. You performed the encryption yourself and send encrypted data to AWS. AWS does not know your encryption keys and cannot decrypt your data.

`4 - You have a website that loads files from an s3 bucket. When you try the URL of the files directly in your Chrome browser it works but, when a website with a different domain tries to load these files it doesn't. What's the problem?`

CORS is wrong. Cross origin resource sharing (CORS) defines a way for client web applications that are load in one domain to interact with the resources in a different domain.

`5 - An e-ommerce company has its customers and orders data stored in s3 bucket. The company CEO wants to generate a report to show the list of customers and the revenue for each customer. Customer data is stored in files on the S3 bucket has sesitive information that we don't want to expose in the report. How do you recommend the reports can be created without exposing sensitive information?`

Use S3 object lambda to change the objects before they are retrieved by the report generator application.

`6 - You suspect that some of your employees try to access files in an S3 bucket that they don't have access to. How can you verify this is indeed the case without them noticing?`

Enable S3 access logs and analyze them using Athena. S3 Access logs log all the requests made to S3 bucket and Amazon Athena can be used to run serverless analytics on top of the log files.

`7 - You're looking to provide temporary URLs to a growing list of Federated users to allow them to perform a file upload on your S3 bucket to a specific location. What should you use?`

S3 Pre-Signed URL. S3 Pre-signed URLs are temporary URLs that you generate to Grant time-limited access to some actions in your S3 bucket.

`8 - For compliance reasons your company has a policy mandate the database backups must be retained for 4 years. It shouldn't be possible to erase them. What do you recommend?`

Glacier vaults with vault lock policies

`9 - You would like all your files in an s3 bucket to be encrypted by default. What's the optimal way of achieving this?`

Do nothing, Amazon S3 automatically encrypts new objects using server-side encryption with S3 managed keys (SSE-S3).

`10 - You have enabled versioning and want to be extra careful when it comes to deleting files on an s3 bucket. what should you enable to prevent accidental permanent deletions?`

Enable MFA delete. MFA delete forces users to use MFA codes before deleting S3 objects. It's an extra level of security to prevent accidental deletions.

`11 - A company has its data and files stored on some S3 buckets. Some of these files need to be kept for a predefined period of time and protected from being overwritten and deleted according to company compliance policy. Which S3 feature helps you in doing this?`

S3 object `lock - retention compliance mode

`12 - Which of the following S3 objects to lock configuration allows you to prevent an object or its versions from being overwritten or deleted indefinitely and gives you the ability to remove it manually?`

Legal Hold
