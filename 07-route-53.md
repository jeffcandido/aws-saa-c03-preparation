# Route 53

`1 - You have purchased mycompany.com on Amazon Route 53 Registrar and would like the domain to point to your elastic load balancer. Which Route 53 record type must you use here?`

Alias

`2 - You have deployed a new Elastic Beanstalk environment and would like to direct 5% of your production traffic so this new environment. This allows you to monitor for cloudwatch metrics and ensuring that there's no bugs exist with your new environment. Which Route 53 record type allows you to do so?`

Weighted. Weighted Routing Policy allows you to redirect part of the traffic based on weight (e.g., percentage). It's a common use case to send part of the traffic to a new version of your application.

`3 - You have updated a halt 53 records myapp.mydomain.com value to point to a new elastic load balancer, But it looks like users are still directed to the old elb. What  is a possible cause for this behavior?`

Because of the TTL. Each DNS record has a TTL ( time to live ) Which orders clients for how long to cash these values and not overload the DNS resolver with DNS requests. The TTL valve should be set to strike a balance between how long the value should be cached versus how many requests should go to the DNS resolver.

`4 - You have an application that's hosted in two different AWS region us-west-1 and eu-west-2. You want your users to get the best possible user experience by minimizing the response time from application servers to your users.  Which Route 53 routing policy should you choose?`

Latency. latency voting policy will evaluate the latency between your users and AWS regions and help them get the DNS response that will minimize their latency (eg. response time).

`5 - You have a legal requirement that people in any country but friends should not be able to access your website.  Which Route 53 routing policy helps you in achieving this?`

Geolocation

`6 - You have purchased a domain on GoDaddy and would like to use Route 53 as the DNS service provider. What should you do to make this work?`

Create a public hosted Zone and update the 3rd party Registrar and NS records. Public hosted zones are meant to be used for people requesting your website through the internet. finally NS records must be updated on the 3rd party Registrar.

`7 - Which of the following are not valid Route 53 health checks?`

Health check that monitor SQS queues
