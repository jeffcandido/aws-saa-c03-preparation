# CloudFront & AWS Global Accelerator

`1 - You have a cloud front distribution that serves your website hosted on a fleet of ec2 instances behind an application load balancer. All your clients are from the United States but you found that some malicious requests are coming from other countries. What should you do to only allow users from the US and block other countries?`

Use cloud from Geo restriction

`2 - A WordPress website is hosted in a set of EC2 instances in an EC2 Auto Scaling Group and fronted by a CloudFront Distribution which is configured to cache the content for 3 day. You have released a new version of the website and want to release it immediately to production without waiting for three days for the cached content to expire. What's the easiest and most efficient way to solve this?`

Clothes front cache Invalidation

`3 - A company is deploying a media sharing website to AWS. They're going to use cloud front to deliver the content with low latency to their customers where they are located in both US and Europe only. After a while there is a huge cost for cloudfront. Which Cloud front feature allows you to decrease costs by targeting only us and Europe?`

CloudFront Price Classes

`4 - A company is migrating a web application to AWS cloud and they're going to use a set of EC2 instances in an EC2 Auto scaling group. The web application is made of multiple components so they will need a host-based routing feature to Route the specific web application components. This web application is used by many customers and therefore the web application must have a static IP address so it can be white listed by the customer's firewalls as the customers are distributed around the world the web application must also provide low latency to our customer. Which AWS service can help you to assign a static IP address and provide low latency across the globe?`

AWS Global accelerator + application load balancer
