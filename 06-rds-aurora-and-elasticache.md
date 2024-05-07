# RDS, Aurora and Elasticache

`1 - Amazon RDS supports the following databases, EXCEPT:`

MongoDB. RDS supports MySQL, PostgreSQL, MariaDB, Oracle, MS SQL Server, and Amazon Aurora.

`2 - You're planning for a new solution that requires a MySQL database that must be available even in case of a disaster in one of the Availability Zones. What should you use?`

Multi-AZ helps when you plan a disaster recovery for an entire AZ going down. If you plan against an entire AWS Region going down, you should use backups and replication across AWS Regions.

`3 - We have an RDS database that struggles to keep up with the demand of requests from our website. Our million users mostly read news, and we don't post news very often. Which solution is NOT adapted to this problem?`

RDS Multi-AZ. Be very careful with the way you read questions at the exam. Here the question is asking which solution is NOT adapted to this problem. ElastiCache and RDS Read Replicas do indeend help with scaling reads.

`4 - You have set up read replicas on your RDS database, but users are complaining that upon updating their social media posts, they do not see their updated posts right away. What is a possible cause for this?`

Read Replicas have Asynchronous Replication, therefore it's likely your users will only read Eventual Consistency.

`5 - Which RDS (NOT Aurora) feature when used does not require you to change the SQL connection string?`

Multi-AZ. Multi-AZ keeps the same connection string regardless of which database is up.

`6 - Your application running on a fleet of EC2 instances managed by an Auto Scaling Group behind an Application Load Balancer. Users have to constantly log back in and you don't want to enable Sticky Sessions on your ALB as you fear it will overload some EC2 instances. What should you do?`

Store Session data in ElastiCache. Storing Session Data in ElastiCache is a common pattern to ensuring different EC2 instances can retrieve your user's state if needed.

`7 - An analytics application is currently performing its queries against your main production RDS database. These queries run at any time of the day and slow down the RDS database which impacts your users' experience. What should you do to improve the users' experience?`

Setup a Read Replica. Read Replicas will help as your analytics application can now perform queries against it, and these queries won't impact the main production RDS database.

`8 - You would like to ensure you have a replica of your database available in another AWS Region if a disaster happens to your main AWS Region. Which database do you recommend to implement this easily?`

`9 - You would like to ensure you have a replica of your database available in another AWS Region if a disaster happens to your main AWS Region. Which database do you recommend to implement this easily?`

Aurora Global Databases allows you to have an Aurora Replica in another AWS Region, with up to 5 secondary regions.

`10 - How can you enhance the security of your ElastiCache Redis Cluster by allowing users to access your ElastiCache Redis Cluster using their IAM Identities (e.g., Users, Roles)?`

Using IAM Authentication

`11 - Your company has a production Node.js application that is using RDS MySQL 5.6 as its database. A new application programmed in Java will perform some heavy analytics workload to create a dashboard on a regular hourly basis. What is the most cost-effective solution you can implement to minimize disruption for the main application?`

Create a Read Replica in a different AZ and run the analytics workload on the replica database

`11 - You would like to create a disaster recovery strategy for your RDS PostgreSQL database so that in case of a regional outage the database can be quickly made available for both read and write workloads in another AWS Region. The DR database must be highly available. What do you recommend?`

Create a Read Replica in a different region and enable Multi-AZ on the Read Replica

`12 - You have migrated the MySQL database from on-premises to RDS. You have a lot of applications and developers interacting with your database. Each developer has an IAM user in the company's AWS account. What's a suitable approach to give access to developers to the MySQL RDS DB instance instead of creating a DB user for each one?`

Enable IAM database Authentication

`13 - Which of the following statements is true regarding replication in both RDS read replicas and Multi-AZ?`

Read replica uses a synchronous replication in multi-AZ use synchronous replication

`14 - How do you encrypt an encrypted RDS DB instance?`

Create a snapshot of the unencrypted RDS DB instance, copy the snapshot and tick “Enable encryption”, then restore the RDS DB instance from the encrypted snapshot.

`15 - For your RDS database you can have up to 15 Read replicas.`

`16 - Which RDS database technology does not support IAM database Authentication.`

Oracle

`17 - You have an unencrypted RDS DB instance and you want to create Read Replicas. Can you configure the RDS Read Replicas to be encrypted?`

No. You cannot create encrypted read replicas from an unencrypted RDS DB instance.

`18 - An application running prediction is using an aurora cluster as its  database. Your development team would like to run a version of the application in a scale-down application with the ability to perform some heavy workload on a need-basis. Most of the time the application will be unused.  Your CIO has tested you with helping the team to achieve these wild minimizing costs. What do you suggest?`

Use Aurora serverless

`19 - How many Aurora Read Replicas can you have in a single Aurora DB cluster?`

15

`20 - Amazon Aurora supports both MySQL in PostgreSQL databases.`

`21 - You work as a Solutions architect for a gaming company. One of the games mandates that players are ranked in real-time based on  their score. Your boss asked you to design and then Implement an effective and highly available solution to create a gaming leaderboard.  What should you use?`

Use the last cash for Redis sorted sets

`22 - You need full customization of an Oracle database on AWS.  You would like to benefit from using AWS services. What do you recommend?`

RDS custom for Oracle.

`23 - You need to store long-term backups for your Aurora database for disaster  recovery and audit purposes.  What do you recommend?`

Perform On Demand Backups.

`24 - Your development team would like to perform a suite of read and write tests against your production Aurora database because they need access to production data as soon as possible. What do you advise?`

Use the Aurora cloning feature.

`25 - You have 100  EC2 instances connected to your RDS database and you see that upon maintenance of the database, all your applications take a lot of time to reconnect to RDS, due to poor application logic. How do you improve this?`

Using RDS proxy. This reduces the failover time by up to 66% and keeps connection actives for your applications.
