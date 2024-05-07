# EC2 Data Management

`1 -  You have just terminated an EC2 instance in us-east-1a, and its attached EBS volume is now available. Your teammate tries to attach it to an EC2 instance in us-east-1b but he can't. What is a possible cause for this?`

EBS Volumes are created for a specific Availability Zone. It is possible to migrate them between different AZs using EBS Snapshots.

`2 -  You have launched an EC2 instance with two EBS volumes, Root volume type and the other EBS volume type to store the data. A month later you are planning to terminate the EC2 instance. What's the default behavior that will happen to each EBS volume?`

By default, the Root volume type will be deleted as its "Delete On Termination" attribute checked by default. Any other EBS volume types will not be deleted as its "Delete On Termination" attribute disabled by default.

`3 -  You can use an AMI in N.Virginia Region us-east-1 to launch an EC2 instance in any AWS Region.`

AMIs are built for a specific AWS Region, ther're unique for each AWS Region. You can't launch an EC2 instance using an AMI in another AWS Region, but you can copy the AMI to the target AWS Region and then use it to create your EC2 instances.

`4 - Which of the following EBS volume types can be used as boot volumes when you create EC2 instances?`

gp2, gp3, io1, io2

`5 - What is EBS Multi-Attach?`

Using EBS Multi-Attach, you can attach the same EBS volume to multiple EC2 instances in the same AZ. Each EC2 instance has full read/write permissions.

`6 - You would like to encrypt an unencrypted EBS volume attached to your EC2 instance. What should you do?`

Create an EBS Snapshot of your EBS volume. Copy the snapshot and tick the option to encrypt the copied snapshot. Then, use the encrypted snapshot to create a new EBS volume.

`7 - You have a fleet of EC2 instances distributes across AZs that process a large data set. What do you recommend to make the same data to be accessible as an NFS drive to all of your EC2 instances?`

EFS is a network file system (NFS) that allows you to mount the same file system on EC2 instances that are in different AZs.


`8 - You would like to have a high-performance local cache for your application hosted on an EC2 instance. You don't mind losing the cache upon the termination of your EC2 instance. Which storage mechanism do you recommend as a Solutions Architect?`

EC2 Instance Store provides the best disk I/O performance.

`9 - You are running a high-performance database that requires an IOPS of 310,000 for its underlying storage. What do you recommend?`

You can run a database on an EC2 instance that uses an Intance Store, but you'll have a problem that the data will be lost if the EC2 instance is stopped (it can be restarted without problems). One solution is that you can set up a replication mechanism on another EC2 instance with an Instance Store to have a standby copy. Another solution is to set up backup mechanisms for your data. It's all up to you how you want to set up your architecture to validate your requirements. In this use case, it's around IOPS, so we have to choose an EC2 Instance Store.