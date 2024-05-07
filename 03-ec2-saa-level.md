# EC2 Solutions Architect Associate Level

`1 - You have launched an EC2 instance that will host a NodeJS application. After installing all the required software and configured your application, you noted down the EC2 instance public IPv4 so you can access it. Then, you stopped and then started your EC2 instance to complete the application configuration. After restart, you can't access the EC2 instance, and you found that the EC2 instance public IPv4 has been changed. What should you do to assign a fixed public IPv4 to your EC2 instance?`

Elastic IP is a public IPv4 that yo own as long as you want and you can attach it to one EC2 instance at a time.

`2 - You have an application performing big data analysis hosted on a fleet of EC2 instances. You want to ensure your EC2 instances have the highest networking performance while communicating with each other. Which EC2 Placement Group should you choose?`

Cluster Placement Groups places your EC2 instances next to each other which gives you high-performance.

`3 - You have a critical application hosted on a fleet of EC2 instances in which you want to achieve maximum availability when there's an AZ failure. Which EC2 Placement Group should you choose?`

Spread Placement Groups places your EC2 instances on different physical hardware across different AZs.

`4 - Elastic Network Interface (ENI) can be attached to EC2 instances in another AZ.`

False. Elastic Network Interfaces (ENIs) are bounded to a specific AZ. You can not attach an ENI to an EC2 instance in a different AZ.

`5 - EC2 Instance Root Volume must be an Intance Store Volume.`

To enable EC2 Hibernate, the EC2 Instance Root Volume type must be an EBS volume and must be encrypted to ensure the protection of sensitive content.
