---
title: Architecting a Zero Trust Framework in Azure
categories:
- 'Community'
feature_image: "https://picsum.photos/2560/600?image=873"
aside: true
---

## Azure Spring Clean 2023 ##

# Architecting a Zero Trust Framework in Azure #

#AzureSpringClean, #AzureFamily, #CloudFamily, #AZOps

![](images/../../images/Bit23.png)

In this article, you will be provided with guidance toward architecting a Zero Trust Framework within your Azure infrastructure. This will include areas of focus for identity, networking, devices, applications, and data for a defense in depth security design. This article will close with a case study example of how to evaluate and consult for a Zero Trust Framework within your company or customer.

### **What is Zero Trust?** ###

At its core, Zero Trust is an integrated approach to securing access with adaptive controls and continuous verification across your entire digital estate.

Everything from the user’s identity to the application’s hosting environment is used to verify the request and prevent breach. And to limit the impact of potential breaches, we apply segmentation policies, employ the principle of least privilege access, and use analytics to help detect and respond quickly.

Zero Trust is a security strategy. It is not a product or a service, but an approach in designing, adopting, and implementing defined, verified security principles.

Simplified, Zero Trust can be boiled down to three basic tenets:

- **Verify explicitly**: In other words, always authenticate and authorize based on all available data points, including user identity, location, device health, service or workload, data classification, and anomalies.

- **Use least privileged access**: For example, limit user access with Just-in-Time and Just Enough Access (JIT/JEA), to protect both data and productivity.

- **Assume breach**: Minimize blast radius for breaches and employ security strategies to prevent lateral movement

Instead of assuming everything behind the corporate firewall is safe, the Zero Trust model assumes every request is a potential breach. As such, every request must be verified as though it originates from an open network. Regardless of where the request originates or what resource it accesses, Zero Trust teaches us to “never trust, always verify.” Every access request is fully authenticated, authorized, and encrypted before granting access. Micro segmentation and least privileged access principles are applied to minimize lateral movement. Rich intelligence and analytics are used to detect and respond to anomalies in real time.

**Why Zero Trust?**

One of the obvious benefits of designing and implementing a Zero Trust strategy is developing a more secure, more compliant environment. But there’s even more opportunities for expanding the Zero Trust methodology within your company.

According to a Forrester total economic impact study from December 2021, costs, flexibility, and risks are all positively impacted by a Zero Trust approach.

The old way of security does not provide business agility, user experiences, and protections needed for a rapidly evolving digital estate. Many organizations are implementing Zero Trust to alleviate these challenges and enable the new normal of working anywhere, with anyone, at any time. The expanded ecosystem of remote users with multiple devices creates more attack surfaces to be exploited. This

leads to the potential for an attacker to gain information on a user or device to gain access. Zero Trust methods assist in the mitigation of these threats before they become active attacks.

Zero Trust is a key survival skill for digital transformation and can help unlock a 92% return on investment.

Let's take a deeper look at how to implement zero trust with the pillars of coverage. Approaching each of these areas with a focus on zero trust will provide a strong defense in depth strategy to protecting sensitive information and mitigating a potential breach within your environment.

### **Pillars of the Zero Trust Framework**

Zero Trust has six coverage areas that are like a defense in depth strategy. Addressing each of these pillars will provide an approach that will protect personal information and data from a potential breach. These areas of coverage include the following:

**Identity**

Identity is a key pillar in zero trust. User and device access through the identity providers requires the use of rules-based access, such as IAM policies and Conditional access policies that determine the potential risk of a user or login request.

Properly planning for roles and permissions are key to successfully implementing zero trust for identity.  Authorization to resources should be based on principles of least privilege and administrative access should be time-based with proper approvals and auditing.  When users need access to sensitive information, they should be evaluated for the level of risk that user or that sign-in creates for the company based on the conditions of the user location, devices, and user integrity.  The level of risk will then determine the additional verification that may be needed, and whether to allow or deny access to the application or data.

**Infrastructure**

Infrastructure protection within the cloud and on-premises through providing limited access and permission through management ports of virtual machines and containers.

Administrative access to infrastructure resources should be time-bound and auditable.  No users or resources should have privileged access 24x7.  Administrators do not need this full-time access. All full-time administrator authorization does is increase the ability for a successful attack to gain access and laterally move through the infrastructure.  Therefore, when a user requires access to perform administrative tasks, they should request access, have it approved and logged, and have that access for a limited time. Once that time expires, the authorization will need to be requested and approved again.

**Network Access**

Network access through zero trust includes the isolation and segmentation between public and private networks. Providing proper permissions to the private networks will allow for availability to resources that users require while blocking potential attacks.

Creating this separation within an on-premises network can be done through physical isolation of networks or virtual isolation with VLANs.  The VLAN principle can be applied within the cloud with virtual networks (VNETs) in Azure or virtual private clouds (VPCs) in AWS.  This virtual segmentation can be used to avoid public access to networks to leak into the private networks.  

Network access to through the infrastructure can be controlled with network access control lists, network security groups, and access policies.  

**Applications**

Applications and how they are accessed through web and Internet entry points become particularly challenging within the cloud. Protecting the access to public facing applications and private access to backend databases through zero trust access is important.

Enforcing zero trust for applications are challenging since applications are going to be the public facing aspect of the company.  A company should understand the information that they want accessed publicly and protect the private information from leaking.  

In addition, the company should utilize a cloud access security broker (CASB) to govern and manage access to cloud applications and avoid shadow IT being utilized by users.

**Endpoints**

Endpoints and devices are the manner that users access devices, networks, and data. Decreasing the attack surface on these devices utilizing security controls and tools to avoid access to sensitive information.

Whether an endpoint is a virtual server, windows device, or smartphone, the company should have a level of endpoint protection and governance over those devices to enforce zero trust.  

For company owned devices, mobile device management (MDM) can manage the windows, android, and apple operating systems to enforce configuration and compliance policies for protecting and decreasing the attack surface.  Policies can be put in place to deny access to applications and data on devices that are not managed with MDM.  

For personal devices, the same management can be provided with mobile application management (MAM) without taking over full control of the device. MAM creates virtual separation from personal and business applications and data to protect against data being over shared.

**Data**

Data is the center of the zero trust approach. Utilizing proper encryption and key management to avoid data to be readable in plain text will assist in enforcing zero trust. This also maintains the confidentiality and integrity of the data.

The protection of personal identifiable information (PII), personal health information (PHI), sensitive data, and confidential data is the focus of many of the zero trust pillars.  

The key to protecting your data is to understand what data you have and where it is located.  Once you have identified where the sensitive and confidential data is located, you can then put policies in place and zero trust security and governance controls to protect against data loss.

Let's look at how to apply these pillars within Azure and Microsoft 365.

## **Applying Zero Trust to Azure**

Each of the pillars can be addressed within Azure and Microsoft 365 by using their cloud native security and compliance tools. Let's take a look using an example.

**Case study**
Company ABC has concerns across their Azure, on-premises, and SaaS applications architecture.  They have come to you for assistance in addressing their security concerns.  They want you to provide suggestions on how they can use the security capabilities within Azure, Azure AD, and Microsoft 365 to enforce Zero-trust methodologies across the company’s technology infrastructure. 

The areas of concern and requirements include:
- Utilization of strong modern authentication techniques for all users, including cloud-native and on-premises directory users.  
- Guest users should be only allowed to access resources that are assigned to them, and they should be regularly reviewed.
- Administrative users should have just-in-time access to privileged resources and all access should be justified and audited.
- When accessing applications that contain sensitive information, users should be required to verify their identity.
- All user identities should be protected from common attacks.
- Users that are accessing company resources from potentially dangerous locations should be forced to re-authenticate.
- Devices should be verified with proper security patches before accessing company resources.
- Users should be analyzed for anomalous behavior and potential threats to identities.
- Network resources with sensitive information should not be accessible through publicly available connections.
- All activity and event data should be logged and can be reviewed.
- Reports can be generated for executive reviews and incident handling.

**Address Requirements with for Zero Trust Framework with Azure and Microsoft 365 solutions**

The customer requirements can be address using a zero trust framework with the following tools:
- Utilization of strong modern authentication techniques for all users, including cloud-native and on-premises directory users.  

    - You should develop a plan to migrate users to Azure AD as a cloud-native identity provider.  For users to remain on Windows Active Directory, you can utilize Azure AD Connect with either password hash or pass-through synchronization with password write-back.  This will allow modern authentication to new applications and the ability to utilize Azure AD MFA and Conditional Access policies.

    - Applications that support modern authentication can be registered in Azure AD to use cloud-native identities for authentication and authorization.

- Guest users should be only allowed to access resources that are assigned to them, and they should be regularly reviewed.

    - This can be accomplished utilizing Entitlement Management within Microsoft Entra Identity Governance.

    - Regular access reviews can be created with Company ABC project managers or supervisors as the reviewers.

- Administrative users should have just-in-time access to privileged resources and all access should be justified and audited.

    - Microsoft Entra Identity Governance with Privileged Identity Management (PIM) provides the JIT access.  All enabled privileged access requires a justification and is audited.  

    - Migrating users to Azure AD as a cloud-native identity provider will allow this governance to be used across all users within the company.

- When accessing applications that contain sensitive information, users should be required to verify their identity.

    - Planning, development, and use of Conditional Access policies to protect sensitive business applications will be used here.  Applications and additional verification requirements for compliant devices and user required MFA can be used for access and authorization.

- All user identities should be protected from common attacks.

    - Azure AD Identity Protection will monitor user and sign-in risks.  The risks include common attack vectors such as brute force identity attacks.

    - Azure AD Password protection can be used to protect against brute force attacks by setting parameters for login frequency to block these attacks.  Password strength can be enforced by creating a dictionary of blocked passwords.	

- Users that are accessing company resources from potentially dangerous locations should be forced to re-authenticate.

    - Additional Conditional Access policies can be created that identify trusted and untrusted locations that can force change in password and/or MFA verification.  Untrusted locations can also be blocked from allowing users to authenticate.

- Devices should be verified with proper security patches before accessing company resources.

    - All devices that are accessing company resources should be managed with Microsoft Intune MDM or MAM.

    - Conditional Access policies can be created to verify that devices follow Microsoft Intune policies prior to accessing applications.

- Users should be analyzed for anomalous behavior and potential threats to identities.

    - Azure AD Identity Protection will monitor user and sign-in risks.  This solution will monitor for potential threats and anomalous user behavior.

- Network resources with sensitive information should not be accessible through publicly available connections.

    - Network infrastructure and resources should be designed with VNet segmentation.  Resources containing sensitive information should be on their own dedicated VNet.  Access through the network should be protected in a more secure manner than VNet peering.  Network and Application Security Groups should have rules for how traffic goes between VNet segments and subnets to the private VNets.

    - Data on applications should also be identified, classified, and protected utilizing sensitivity labels.

- All activity and event data should be logged and can be reviewed.

    - Azure Monitor should be turned on for all Azure resources.

    - Azure Arc can extend the monitoring to non-Azure resources.

    - Microsoft 365 monitors and logs SaaS activity.

    - Log Analytics and Microsoft Sentinel can be used to connect all data sources and provide a single location for monitoring and reviewing events and activities for malicious activity.

- Reports can be generated for executive reviews and incident handling.
    
    - Taking the above steps for monitoring activity and events allows the creation of reports for reviews.  This information can also be used in custom dashboards, workbooks, and Power BI.

**Summary**

Implementing a zero trust framework to your cloud security architecture takes time and planning.  Cloud providers have tools that can assist you in this journey. Understanding how the pillars of zero trust will operate and interact across the environment will be a key to your success.  

**Resources**

[Zero Trust implementation guidance | Microsoft Learn](https://learn.microsoft.com/en-us/security/zero-trust/zero-trust-overview)

[Zero Trust Model - Modern Security Architecture | Microsoft Security](https://www.microsoft.com/en-us/security/business/zero-trust/?ef_id=_k_353a143435bc1ff6a92877c82a78eb57_k_&OCID=AIDcmmdamuj0pc_SEM_k_353a143435bc1ff6a92877c82a78eb57_k_&msclkid=353a143435bc1ff6a92877c82a78eb57)