# Amazon s3

`1 - You have a 25 GB file that you are trying to upload to S3 but you're getting errors. What's a possible solution for this?`

Use multi-part upload when uploading files larger than 5 GB. Multipart upload is recommended as soon as the file is over 100 MB.

`2 - We're getting it hurts while trying to create a new S3 bucket named “dev”. You are using a new AWS account with no S3 buckets created before. What is a possible cause for this?`

s3 bucket names must be globally unique and “dev is already taken.

`3 - You have enabled versioning in your S3 bucket which contains a lot of files. Which version will the existing files have?`

null

`4 - You have updated a nasty bucket policy to allow IAM users to read or write files in the S3 buckets, but one of the users complained that he can't perform a PutObject API call. What's the possible cause for this?`

The IAM user must have an explicit DENY in the attached Iam policy. Explicit DENY in an IAM policy will take precedence over an S3 bucket policy.

`5 - You want the contents of an s3 bucket to be fully available in different AWS regions. That will help your team perform data analysis at the lowest latency and cost possible. What s3 feature should you use?`

S3 replication. S3 replication allows you to replicate data from an S3 bucket to another in the same or different AWS region.

`5 - You have three S3 buckets. one Sears bucket a and two destination buckets B and C in different AWS regions. You want to replicate objects from bucket A to both bucket B and C. How would you achieve this?`

Configure application from buckets a to bucket B, then from bucket a to bucket C.

`6 - Which of the following is not a Glacier Deep archive Retrieval mode?`

`Expedited (1 - 5 minutes)

`7 - Which of the following is not a Glacier Flexible Retrieval mode?`

`Instant (1 - 5 minutes)
