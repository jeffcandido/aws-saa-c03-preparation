# Classic Solutions Architect discussion

`1 - Your website trianglesunglasses.com is hosted on the fleet of ec2 instances managed by an Auto scaling group and fronted by an application load balancer. You're Auto scaling group has been configured to scale on-demand based on the traffic going to your website. To reduce costs you have configured the outer scaling group to Scale based on the traffic going through the application load balancer.  to make this solution highly available you have updated your outer scaling group and set the minimum capacity to 2. How can you further a reduce the costs while respecting the requirements?`

Reserve 2 EC2 instances. This is the way to save further costs as we will run two EC2 instances no matter what.

`2 -  which of the following will not help us while designing a stateless application tier?`

Star session data on EBS volumes. EBS volumes are created in a specific Availability Zone and can only be attached to one EC2 instance at a time.

`3 - You want to install software updates on hundreds of Linux ec2 instances that you manage. You want to store these updates on shared storage which should be dynamically loaded on the EC2 instances and shouldn't require heavy operations. What do you suggest?`

Store the software updates on EFS and mount EFS as a network drive at startup. EFS is a network file system (NFS) that allows you to mount the same file system to hundreds of ec2 instances. Storing software updates on an EFS allows each EC2 instance to access them.

`4 - As a Solutions Architect, you're planning to migrate a complex ERP software suite to AWS cloud.  You're planning to host the software on a set of Linux ec2 instances managed by an Auto Scaling group. The software traditionally takes over an hour to set up on a Linux machine.  How do you recommend you speed up the installation process when there's a scale out event?`

Use a golden AMI. Golden AMI is an image that contains all your software installed and configured so that future EC2 instances can boot up quickly from that AMI.

`5 - You're developing an application and would like to deploy it to Elastic Beanstalk with minimal cost. You should run it in . . .`

Single instance mode. The question mentions that you're still in the development stage and you want to reduce costs. Single instance mode will create one EC2 instance and one elastic IP.

`6 - You're deploying your application to an elastic beanstalk environment but you notice that the deployment process is painfully slow.  After reviewing the logs you found that your dependencies are resolved on each EC2 instance each time you deploy. How can you speed up the deployment process with minimal impact?`

Create a golden AMI that contains the dependencies and use that image to launch the ec2 instances. Golden AMI is an image that contains all your software dependencies and configurations so that future EC2 instances can boot up quickly from that AMI.
