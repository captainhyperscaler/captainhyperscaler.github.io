---
title: What I have learned about Security on AWS
categories:
- 'Amazon-Web-Services'
feature_image: "https://picsum.photos/2560/600?image=873"
aside: true
---

This is the eleventh post of content for preparing yourself for becoming an AWS Solutions Architect Associate.

![](images/../../images/Wordpress-Images/awscerts.png)

In this post, we are going to focus on security features within AWS.

As I have done previously let's look at the similarities and differences to the closest equivalent in Azure.  As I go through this section, I will point out some of the similar platforms.

**Reducing Security Threats**

- Bad actors - automated processes, content scrapers, bad bots
- Network Access Control lists (NACL) - create inbound rules to block known IPs from bad actors.
- Host-based firewalls - cannot be used with an Application Load Balancer. Connection from the bad actor will terminate at the ALB, not the EC2 instance.
- WAF attached to the LB can monitor web requests and protect against malicious attacks from bad actors.
    - Layer 7 and can protect against common exploits.
    - WAF can be used with CloudFront and ALB.
- NACL works at Layer 4.


**Key Management Service**

- Same as Azure Key Vault
- Create and control the encryption keys
- Manages Customer Managed Keys (CMK)
- Pay per API call
- Integrated with most AWS services
- Audited with CloudTrail
- FIPS 140-2 Level 2
- Level 3 is supported with CloudHSM
- Types of CMK:
    - AWS Managed CMK - Free - used by a specific service.
    - Customer Managed CMK - allows key rotation and is controlled by key policies.
    - AWS owned CMK - used by AWS on a shared basis across accounts, typically not seen. Not in your AWS account, but AWS can use for account access/support.

- Symmetric CMK is used by AWS services
    - AES-256
    - Same key is used for encryption and decryption

- Asymmetric CMK
    - RSA and ECC encryption
    - Used outside of AWS where they cannot call KMS CMKs

- Default Key Policy - root user is given full access to the CMK

**CloudHSM**

- Similar to Premium Azure Key Vault, but rather than third party HSM, AWS provides this service.
- Using own encryption keys
- Dedicated hardware security module that uses FIPS 140-2 **Level 3**.
- KMS is level 2 compliant. Multi-tenant
- Manage your own keys.
- Single tenant, dedicated hardware, multi-AZ cluster.
- Strict regulatory requirements is a primary use case.


**System Manager Parameter Store**

- Securely manages configuration and secrets to resources.
- Component of AWS Systems Manager (SSM).
- Secrets and application code securely stored.
- Secure serverless storage for configuration and secrets, including:
    - Passwords
    - Database connection strings
    - License codes
    - API keys

- KMS keys or plaintext
- Separate from source control
- Store parameters in hierarchies
- Track versions
- Set time to live for staging and production
- No additional charges but a max of 10,000 API calls.

**Secrets Manager**
- Automatically rotate keys with RDS
- Charge per secret stored and per 10,000 API calls.
- Apply new key/password in RDS for you.
- Generates random secrets.

**Note**: There are elements in KMS, CloudHSM, System Manager Parameter Store, and Secrets Manager that are found within Azure Key Vault and App Configuration, which both work together in the Azure architecture.

**AWS Shield**

- Protects against DDoS attacks.
- Same as Microsoft DDoS Protection.
- Two tiers:
    - Standard - Included with WAF. Protects against Layer 3 and 4 attacks (SYN/UDP floods, Reflection attacks). 
    - Advanced - $3,000 per month, per organization. Enhanced protection for EC2, ELB, CloudFront, Global Accelerator, and Route 53.  Includes Business and Enterprise support with a Dedicated Response Team.

**Web Application Firewall**

- Works with ALB and CloudFront
- Layer 7 solution that protects against common threats. <www.owasp.org/Top10>
- HTTP(s) requests monitored for CloudFront, ALB, or API Gateway.
- Control access and configure filtering rules:
    - IP addresses
    - Query string parameters
    - SQL query injection attacks

- Allow all requests, except ones that are specified.
- Block all requests, except ones that are specified.
- Count the requests with specific properties.
    - Request properties:
        - Originating IP address
        - Originating country
        - Request size
        - Value in request headers
        - Strings in request matching regular expressions (regex) patterns
        - SQL code (injection)
        - Cross site scripting (XSS)

**AWS Firewall Manager**

- Security management services to configure and manage firewall rules across the AWS organization.
    - WAF rules for:
        - ALB
        - API Gateway
        - CloudFront distribution
    - AWS Shield Advanced protections:
        - ALB
        - ELB Classic
        - EIP
        - CloudFront distributions
    - Enable security groups for EC2 and ENI




I hope that you are enjoying this information so far.  It is helping me to continue to comprehend these services as I prepare for the exam myself.  Thank you very much.

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

