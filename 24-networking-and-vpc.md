# Networking and VPC

`1 - What does this CIDR 10.0.4.0/28 correspond to?`

`10.0.4.0` to `10.0.4.15`. /28 means 16 IPs (=2^(32-28) = 2^4), means only the last digit can change.

`2 - You have a corporate network of size 10.0.0.0/8 and a satellite office of size 192.168.0.0/16. Which CIDR is acceptable for your AWS VPC if you plan on connecting your networks later on?`

`172.16.0.0/16`. CIDR not should overlap, and the max CIDR size in AWS is /16.

`3 - You plan on creating a subnet and want it to have at least capacity for 28 EC2 instances. What's the minimum size you need to have for your subnet?`

/26. (=2^(32-26) = 2^6) because AWS reserves 5 IPs.

`4 - Security Groups operate at the ................. level while NACLs operate at the ................. level.`

EC2 Instance, Subnet.

`5 - You have attached an Internet Gateway to your VPC, but your EC2 instances still don't have access to the internet. What is NOT a possible issue?`

The Security Group does not allow traffic in. Security groups are stateful and if traffic can go out, then it can go back in.

`6 - You would like to provide Internet access to your EC2 instances in private subnets with IPv4 while making sure this solution requires the least amount of administration and scales seamlessly. What should you use?`

NAT Gateway.

`7 - VPC Peering has been enabled between VPC A and VPC B, and the route tables have been updated for VPC A. But, the EC2 instances cannot communicate. What is the likely issue?`

Check the Route Table in VPC B. Route tables must be updated in both VPCs that are peered.

`8 - You have set up a Direct Connect connection between your corporate data center and your VPC A in your AWS account. You need to access VPC B in another AWS region from your corporate datacenter as well. What should you do?`

Use Direct Connect Gateway. This is the main use case of Direct Connect Gateways.

`9 - When using VPC Endpoints, what are the only two AWS services that have a Gateway Endpoint available?`

Amazon S3 & DynamoDB. These two services have a VPC Gateway Endpoint (remember it), all the other ones have an Interface endpoint (powered by Private Link - means a private IP).

`10 - AWS reserves 5 IP addresses each time you create a new subnet in a VPC. When you create a subnet with CIDR 10.0.0.0/24, the following IP addresses are reserved, EXCEPT ....................`

10.0.0.4

`11 - You have 3 VPCs A, B, and C. You want to establish a VPC Peering connection between all the 3 VPCs. What should you do?`

Estabilish 3 VPC Peering connections (A-B,A-C,B-C)

`12 - How can you capture information about IP traffic inside your VPCs?`

Enable VPC Flow Logs. VPC Flow Logs is a VPC feature that enables you to capture information about the IP traffic going to and from network interfaces in your VPC.

`13 - If you want a 500 Mbps Direct Connect connection between your corporate datacenter to AWS, you would choose a .................. connection.`

Hosted Direct Connect connection supports 50Mbps, 500Mbps, up to 10Gbps.

`14 - When you set up an AWS Site-to-Site VPN connection between your corporate on-premises datacenter and VPCs in AWS Cloud, what are the two major components you want to configure for this connection?`

Virtual Private Gateway and Customer Gateway.

`15 - Your company has several on-premises sites across the USA. These sites are currently linked using private connections, but your private connections provider has been recently quite unstable, making your IT architecture partially offline. You would like to create a backup connection that will use the public Internet to link your on-premises sites, that you can failover in case of issues with your provider. What do you recommend?`

AWS VPN CloudHub allows you to securely communicate with multiple sites using AWS VPN. It operates on a simple hub-and-spoke model that you can use with or without a VPC.

`16 - You need to set up a dedicated connection between your on-premises corporate datacenter and AWS Cloud. This connection must be private, consistent, and traffic must not travel through the Internet. Which AWS service should you use?`

AWS Direct Connect.

`17 - Using a Direct Connect connection, you can access both public and private AWS resources.`

True.

`18 - You want to scale up an AWS Site-to-Site VPN connection throughput, established between your on-premises data and AWS Cloud, beyond a single IPsec tunnel's maximum limit of 1.25 Gbps. What should you do?`

Use Transit Gateway.

`19 - You have a VPC in your AWS account that runs in a dual-stack mode. You are continuously trying to launch an EC2 instance, but it fails. After further investigation, you have found that you are no longer have IPv4 addresses available. What should you do?`

Add an additional IPv4 CIDR to your VPC.

`20 - A web application backend is hosted on EC2 instances in private subnets fronted by an Application Load Balancer in public subnets. There is a requirement to give some of the developers access to the backend EC2 instances but without exposing the backend EC2 instances to the Internet. You have created a bastion host EC2 instance in the public subnet and configured the backend EC2 instances Security Group to allow traffic from the bastion host. Which of the following is the best configuration for bastion host Security Group to make it secure?`

Allow traffic only on port 22 from the company's public CIDR.

`21 - A company has set up a Direct Connect connection between their corporate data center to AWS. There is a requirement to prepare a cost-effective secure backup connection in case there are issues with this Direct Connect connection. What is the most cost effective and secure solution you recommend?`

Setup a Site-to-Site VPN connection as a backup.

`22 - Which AWS service allows you to protect and control traffic in your VPC from layer 3 to layer 7?`

AWS Network Firewall.

`23 - A web application hosted on a fleet of EC2 instances managed by an Auto Scaling Group. You are exposing this application through an Application Load Balancer. Both the EC2 instances and the ALB are deployed on a VPC with the following CIDR 192.168.0.0/18. How do you configure the EC2 instances' security group to ensure only the ALB can access them on port 80?`

Add an Inbound Rule with port `80` and ALB's Security Group as the source. This is the most secure way of ensuring only the ALB can access the EC2 instances. Referencing by security groups in rules is an extremely powerful rule and many questions at the exam rely on it. Make sure you fully master the concepts behind it!
