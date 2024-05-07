# Containers on AWS

`1 - You have multiple Docker-based applications hosted on-premises that you want to migrate to AWS. You don't want to provision or manage any infrastructure; you just want to run your containers on AWS. Which AWS service should you choose?`

AWS Fargate on ECS. AWS Fargate allows you to run your containers on AWS without managing any servers.

`2 - Amazon Elastic Container Service (ECS) has two Launch Types: .................. and ..................`

Amazon EC2 Launch Type and Fargate Launch Type.

`3 - You have an application hosted on an ECS Cluster (EC2 Launch Type) where you want your ECS tasks to upload files to an S3 bucket. Which IAM Role for your ECS Tasks should you modify?`

ECS Task Role is the IAM Role used by the ECS task itself. Use when your container wants to call other AWS services like S3, SQS, etc.

`4 - You're planning to migrate a WordPress website running on Docker containers from on-premises to AWS. You have decided to run the application in an ECS Cluster, but you want your docker containers to access the same WordPress website content such as website files, images, videos, etc. What do you recommend to achieve this?`

Mount and EFS Volume. EFS volume can be shared between different EC2 instances and different ECS Tasks. It can be used as a persistent multi-AZ shared storage for your containers.

`5 - You are deploying an application on an ECS Cluster made of EC2 instances. Currently, the cluster is hosting one application that is issuing API calls to DynamoDB successfully. Upon adding a second application, which issues API calls to S3, you are getting authorization issues. What should you do to resolve the problem and ensure proper security?`

Create an IAM Task Role for the new application.

`6 - You are migrating your on-premises Docker-based applications to Amazon ECS. You were using Docker Hub Container Image Library as your container image repository. Which is an alternative AWS service which is fully integrated with Amazon ECS?`

Elastic Container Registry. Amazon ECR is a fully managed container registry that makes it easy to store, manage, share, and deploy your container images. ECR is fully integrated with Amazon ECS, allowing easy retrieval of container images from ECR while managing and running containers using ECS.

`7 - Amazon EKS supports the following node types. . .`

Managed Node Groups, Self-Managed Nodes and AWS Fargate.

`8 - A developer has a running website and APIs on his local machine using containers and he wants to deploy both of them on AWS. The developer is new to AWS and doesn’t know much about different AWS services. Which of the following AWS services allows the developer to build and deploy the website and the APIs in the easiest way according to AWS best practices?`

AWS App Runner.
