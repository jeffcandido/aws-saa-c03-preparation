# Disaster Recovery and Migration

`1 - As part of your Disaster Recovery plan, you would like to have only the critical infrastructure up and running in AWS. You don't mind a longer Recovery Time Objective (RTO). Which DR strategy do you recommend?`

Pilot Light. If you're interested, read more about Disaster Recovery options in AWS here: <https://docs.aws.amazon.com/whitepapers/latest/disaster-recovery-workloads-on-aws/disaster-recovery-options-in-the-cloud.html>

`2 - You would like to get the Disaster Recovery strategy with the lowest Recovery Time Objective (RTO) and Recovery Point Objective (RPO), regardless of the cost. Which DR should you choose?`

Multi-site (active/active)

`3 - Which of the following Disaster Recovery strategies has a potentially high Recovery Point Objective (RPO) and Recovery Time Objective (RTO)?`

Backup and Restore.

`4 - You want to make a Disaster Recovery plan where you have a scaled-down version of your system up and running, and when a disaster happens, it scales up quickly. Which DR strategy should you choose?`

Warm Standby.

`5 - You have an on-premises Oracle database that you want to migrate to AWS, specifically to Amazon Aurora. How would you do the migration?`

Use AWS Schema Conversion Tool (AWS SCT) to convert the database schema, then use AWS Database Migration Service (AWS DMS) to migrate the data.

`6 - AWS DataSync supports the following locations, EXCEPT ....................`

Amazon EBS.

`7 - You are running many resources in AWS such as EC2 instances, EBS volumes, DynamoDB tables... You want an easy way to manage backups across all these AWS services from a single place. Which AWS offering makes this process easy?`

AWS Backup enables you to centralize and automate data protection across AWS services. It helps you support your regulatory compliance or business policies for data protection.

`8 - A company planning to migrate its existing websites, applications, servers, virtual machines, and data to AWS. They want to do a lift-and-shift migration with minimum downtime and reduced costs. Which AWS service can help in this scenario?`

AWS Application Migration Service.

`9 - A company is using VMware on its on-premises data center to manage its infrastructure. There is a requirement to extend their data center and infrastructure to AWS but keep using the technology stack they are using which is VMware. Which AWS service can they use?`

VMWare Cloud on AWS.

`10 - A company is using RDS for MySQL as their main database but, lately they have been facing issues in managing the database, performance issues, and the scalability. And they have decided to use Aurora for MySQL instead for better performance, less complexity and less administrative tasks required. What is the best way and most cost-effective way to migrate from RDS for MySQL to Aurora for MySQL?`

Create a Snapshot from RDS for MySQL and restore it to Aurora for MySQL.

`11 - Which AWS service can you use to automate the backup across different AWS services such as RDS, DynamoDB, Aurora, and EFS file systems, and EBS volumes?`

AWS Backup.
