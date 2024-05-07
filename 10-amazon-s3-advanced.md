# Amazon s3 Advanced

`1 - You have an s3 bucket that has S3 versioning enabled. This s3 bucket Has a lot of objects and you would like to remove old object versions to reduce costs. What's the approach to automate the deletion of these old object versions?`

S3 lifecycle rules - expiration actions

`2 - How can you automate the transition of s3 objects between their different tiers ?`

S3 lifecycle rules

`3 - While you’re uploading large files to an s3 bucket using multi-part upload, there are a lot of Unfinished Parts stored in the S3 bucket due to network issues. You are not using these unfinished parts and they cost you money. What's the best approach to remove these unfinished parts?`

Use an s3 lifecycle policy to automate old or unfinished parts deletion.

`4 - You are looking to get recommendations for S3 lifecycle rules. How can you analyze the optimal number of days to move objects between different storage tiers?`

S3 Analytics

`5 - You're looking to build an index of your files in history using Amazon RDS PostgreSQL.To build this index it's necessary to reach the first to 250 bytes of each object in s3, which contains some metadata about the content of the file itself. They're over 100,000 files in your S3 bucket amounting to 50 terabytes of data. How can you build this index efficiently?`

Create an application that will traverse the S3 bucket, issue a byte range fetch for the first 250 bytes and store that information in RDS.

`6 - You have a large data set storage in Francis that you want to upload to the S3 bucket. the data set is divided into 10 GB files. You have good bandwidth but your internet connection isn't stable. What's the best way to upload this data sets to S3 and then sure that the process is fast and avoid any problems with the internet connection?`

Use S3 multi-part upload and S3 transfer acceleration.

`7 - You would like to retrieve a subset of your data set stored in the street with the .csv format. You would like to retrieve a month of data and only three columns out of 10, to minimize computer network costs. What should you use?`

S3 Select

`8 - A company is preparing for compliance and Regulatory review on its infrastructure on AWS. Currently, they have their files start on the street buckets that are not encrypted which must be encrypted as required for compliance and Regulatory review. Which s3 feature allows them to encrypt all files in their S3 buckets in the most efficient and cost effective way?`

S3 Batch Operations

`9 - You have a 25 GB file that you are trying to upload to S3 but you're getting a errors. What's a possible solution for this?`

Use multi-part upload when not loading files larger than 5 GB. multi-part upload is recommended as soon as the file is over 100 MB.
