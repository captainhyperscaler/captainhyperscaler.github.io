---
title: What I have learned about Serverless and Lambda on AWS
categories:
- 'Amazon-Web-Services'
feature_image: "https://picsum.photos/2560/600?image=873"
aside: true
---

This is the twelfth and final post of content for preparing yourself for becoming an AWS Solutions Architect Associate.

![](images/../../images/Wordpress-Images/awscerts.png)

In this post, we are going to focus on serverless and Lambda features within AWS.

As I have done previously let's look at the similarities and differences to the closest equivalent in Azure.  As I go through this section, I will point out some of the similar platforms.

**Lambda**

- Similar to Azure Functions
- Alexa is using Lambda for the detect and response.
- AWS Lambda is a service where you upload your code and run functions to run the code.
- Event driven compute service with a trigger.
- Run code in response to a HTTP request using Amazon API Gateway or API calls.
- Lambda functions called will trigger in a separate function to scale infinitely.
- Languages supported are Node.js, Java, Python, C#, Go, and PowerShell.
- Priced on Number of requests and duration of function run time. Very inexpensive: $.20 per 1 million requests.
- No Servers
- Continuous scaling (Out not Up)
- Super cheap
- AWS X-ray allows you to debug serverless applications
- Lambda works globally and can be backed up to S3 buckets in other regions.


**Serverless Application Model (SAM)**

- CloudFormation extension optimized for serverless applications
- functions, APIs, and tables
- Run serverless locally using Docker
- Package and deploy using CodeDeploy



**Elastic Container Service (ECS)**

- Similar to Azure Container Services
- Container is a software package that includes applications, libraries, runtime and tools.
- Docker is a container engine to run the container.
- Containers have less overhead through isolation for faster starts than VMs.
- Containerized applications are portable and offer a consistent environment that does not rely on the compute OS and infrastructure.
- ECS is a managed container orchestration service.
    - Create clusters to manage fleets of container deployments
    - ECS manages ECS or Fargate instances.
    - Schedules containers for optimal placement.
    - Defines rules for CPU and memory requirements.
    - Monitors resource utilization.
    - ECS is Free. EC2 instances and Fargate compute resources are the only cost
    - CloudTrail and CloudWatch integrated.
- Components:
    - Cluster - compute
    - Task Definition
    - Container definition
    - Task - single running copy of container
    - Service - defines min and max
    - Registry - image repository
- Fargate is a serverless compute engine. Works with ECS and EKS (Kubernetes). Isolation and security. 

**EKS (Elastic Kubernetes Service)**

- Containers are grouped in pods
- K8s is open source and can be used on-premises and in the cloud.

**ECR**

- Managed Docker container registry
- Works with ECS, EKS, and on-premises
- Integrated with IAM

**ECS Security**

- EC2 Instance Role
- Task Role - more granular control based on tasks rather than instance. Least privilege approach.



This is the final post in the preparation for the AWS Solution Architect Associate exam.  This has been helpful in preparing me to comprehend AWS services for the exam.  I hope that you find it to do the same.  Thank you very much.

**Reference links**:

What I've Learned about IAM on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/03/20/aws-iam> 

What I've Learned about S3 on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/03/20/aws-s3> 

What I've Learned about EC2 on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/03/22/aws-ec2> 

What I've Learned about EBS on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/03/22/aws-ebs> 

What I've Learned about Cloudwatch on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/03/22/aws-cloudwatch>

What I've Learned about RDS on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/03/22/aws-rds>

What I've Learned about Route 53 on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/04/01/aws-dns>

What I've Learned about VPC on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/04/01/aws-vpc>

What I've Learned about High Availability on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/05/01/aws-ha>

What I've Learned about Applications on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/05/02/aws-apps>

What I've Learned about Security on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/05/03/aws-security>

What I've Learned about Lambda and serverless on AWS

<https://captainhyperscaler.github.io/amazon-web-services/2022/05/04/aws-serverless>


