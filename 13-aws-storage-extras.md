# AWS Storage Extras

`1 - You need to move hundreds of terabytes into Amazon S3, then process the data using a fleet of ec2 instances. You have a 1 GB per second broadband. You would like to move the data faster and possibly process it while in transit. What do you recommend?`

Use Snowball Edge. Snowball Edge is the right answer as it comes with Computing capabilities and allows you to preprocess the data while it's being moved into a snowball.

`2 - You want to expose virtually infinite storage for your tape backups. You want to keep the same software you're using and want an iSCSI compatible interface. What do you use?`

AWS Storage Gateway - Tape Gateway

`3 - You have a large data set stored in S3 that you want to access from on-premises service using the NFS or SMB protocol. Also, you want to authenticate access to these files through on premises Microsoft AD. What would you use?`

AWS Storage Gateway - S3 file Gateway

`4 - You're planning to migrate your company's infrastructure from on-premises to AWS cloud. You have an on-premises Microsoft Windows file server that you want to migrate to. What's the most suitable AWS Services you can use?`

Amazon FSX for Windows (File server)

`5 - You would like to have a distributed POSIX compliant file system that will allow you to maximize the IOPS in order to perform some High-performance Computing (HPC) and genomics computational research. This file system has to easily scale to millions of IOPS. What do you recommend?`

Amazon FSX for Lustre

`6 - Which deployment option in the FSX file system provides you with a long-term strategy that's replicated within the availability Zone?`

Persistent file system. Provides long-term storage where data is replicated within the same AZ. Failed files were replaced within minutes.

`7 - Which of the following protocols is not supported by AWS transfer family?`

Transport layer security (TLS). AWS transfer family is a managed service for file transfers into and out of S3 or EFS using the FTP protocol this TLS is not supported.

`8 - A company uses a lot of files and data which is stored in an FSX for Windows file server stored on AWS. Those files are currently used by the resources hosted on AWS. There's a requirement for those files to be accessed on premises with low latency. Which AWS Service can help you achieve this?`

FSx File Gateway

`11 - A Solutions Architect is working on planning the migration of a startup company from on-premises to AWS. Currently, their infrastructure consists of many servers and 30 TB of data hosted on a shared NFS storage. He has decided to use Amazon S3 to host the data. Which AWS service can efficiently migrate the data from on-premises to S3?`

AWS DataSync

`12 - Which AWS service is best suited to migrate a large amount of data from an S3 bucket to an EFS file system?`

AWS DataSync

`13 - A Machine Learning company is working on a set of datasets that are hosted on S3 buckets. The company decided to release those datasets to the public to be useful for others in their research, but they don’t want to configure the S3 bucket to be public. And those datasets should be exposed over the FTP protocol. What can they do to do the requirement efficiently and with the least effort?`

Use AWS Transfer Family

`14 - Amazon FSx for NetApp ONTAP is compatible with the following protocols, EXCEPt . . .`

FTP

`15 - Which AWS service is best suited when migrating from an on-premises ZFS file system to AWS?`

Amazon FSx for OpeZFS

`16 - A company is running Amazon S3 File Gateway to host their data on S3 buckets and is able to mount them on-premises using SMB. The data currently is hosted on S3 Standard storage class and there is a requirement to reduce the costs for S3. So, they have decided to migrate some of those data to S3 Glacier. What is the most efficient way they can use to move the data to S3 Glacier automatically?`

Use S3 Lifecycle Policy

`17 - You have on-premises sensitive files and documents that you want to regularly synchronize to AWS to keep another copy. Which AWS service can help you with that?`

AWS DataSync
