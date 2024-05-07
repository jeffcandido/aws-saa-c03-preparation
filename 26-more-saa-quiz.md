# More Solutions Architect Quiz

`1 - You are working on a Serverless application where you want to process objects uploaded to an S3 bucket. You have configured S3 Events on your S3 bucket to invoke a Lambda function every time an object has been uploaded. You want to ensure that events that can't be processed are sent to a Dead Letter Queue (DLQ) for further processing. Which AWS service should you use to set up the DLQ?`

Lambda Function. The Lambda function's invocation is "asynchronous", so the DLQ has to be set on the Lambda function side.

`2 - As a Solutions Architect, you have created an architecture for a company that includes the following AWS services: CloudFront, Web Application Firewall (AWS WAF), AWS Shield, Application Load Balancer, and EC2 instances managed by an Auto Scaling Group. Sometimes the company receives malicious requests and wants to block these IP addresses. According to your architecture, Where should you do it?`

AWS WAF.

`3 - Your EC2 instances are deployed in Cluster Placement Group in order to perform High-Performance Computing (HPC). You would like to maximize network performance between your EC2 instances. What should you use?`

Elastic Fabric Adapter.
