---
title: AzureSpringClean - Using Azure Policy and Security Center for Organizational Governance. https://www.azurespringclean.com/
categories:
- 'Community'
feature_image: "https://twentysixteendemo.files.wordpress.com/2015/11/post.png"
aside: true
---


This is my 2021 #AzureSpringClean contribution.  Special thanks to Joe Carlyle (@<a rel="noreferrer noopener" href="https://twitter.com/wedoazure" target="_blank">wedoazure</a>) and Thomas Thornton (@<a rel="noreferrer noopener" href="https://twitter.com/tamstar1234" target="_blank">tamstar1234</a>) for putting together this event for another year.  All of the posts for this year's event can be found at <a rel="noreferrer noopener" href="https://www.azurespringclean.com/" target="_blank">Azure Spring Clean</a>. 

This post covers how to use the tools of Azure Policy and Azure Security Center to govern your resources in Azure, as well as on hybrid infrastructures.  The topics that will be covered in this article are:

- What is Azure Policy and initiatives?

- How can they be utilized for organizational governance?

- What can Azure Security Center provide to manage policy and compliance?

- How can GitHub Actions be used for Policy governance?

- How can you monitor and maintain policy compliance

<strong>What is Azure Policy and initiatives?</strong>

Before we discuss how it can help, it is important to understand Azure Policy.  Azure Policy can be used to govern cost, security, and jurisdiction for your organization’s infrastructure.

Azure has hundreds of pre-built policies based on best practices that can be assigned to monitor and manage subscriptions and resources.

Initiatives are made up of a group of policies. Pre-built initiatives within Azure provide the ability to easily configure your subscription or resource groups for regulatory governance. Assigning initiatives to resources will audit those resources for compliance, and then provide the ability to remediate those resources for compliance.


<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image.png?w=697" alt="" class="wp-image-1192"/></figure></div>


Microsoft Azure holds many cloud attestations for their buildings and infrastructure. Some of the popular ones are on this slide and a full list can be found at the link provided.

It is important to understand what these attestations mean to an organization that is moving their workloads into Azure. If your organization requires a regulatory compliance, Azure definitely assists in putting you on the path to adhering to the requirements. However, compliance goes beyond the attestations held by Azure or other cloud providers. There are processes, procedures, and controls that are all part of the audit guidelines. The benefit of Azure attestations is that utilizing their infrastructure decreases the amount of architecture investment required to build out a compliant environment.

As with any hosted environment, there is a partnership of shared responsibility that needs to be understood.  These attestations can get you on the first steps to regulatory compliance, but you are responsible to enable many of the controls necessary for full compliance and to pass an audit.  Azure Policy can assist in identifying these and provide recommendations to get you to where you need to be.


<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-1.png?w=816" alt="" class="wp-image-1194"/></figure></div>


<strong>How can they be utilized for organizational governance?</strong>

Azure Policy is a very helpful service within Azure, and it can assist in many ways.  We will discuss the role that Azure Policy can be used for organizational, financial, security, and business governance.

<span style="text-decoration:underline;">Organizational governance</span>: Challenges arise within a cloud environment when resources can be created that may affect, cost, security, or regulatory jurisdictions. Governing your environment for financial, business, and security will be discussed further in the following sections, but it is important to understand the role that Azure can play in assisting you in monitoring and management.

Azure policies are created, assigned, and utilized to govern the resources within your Azure subscription. Policies can be assigned using the built-in policies within Azure, of which there are hundreds, or custom policies can be created that may be necessary for your specific organizational needs.  A list of these policies can be found at the link on the slide

Policies should be assigned at the beginning of building your environment in Azure but they can also be retroactively created, and existing resources can be audited against these policies. Determining the policies to put in place should be based a business, security, and financial discussion. <a href="https://docs.microsoft.com/en-us/azure/governance/policy/samples/built-in-policies" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/governance/policy/samples/built-in-policies</a>

<span style="text-decoration:underline;">Financial governance</span>:  Most of the financial and cost governance can be monitored and managed through the cost and billing services and Azure Advisor, with spending limits and controls being put in place for the subscription and resources. 

There are also policies that can be put in place for controlling costs and performance compliance by assigning specific SKUs that are allowed within storage accounts, virtual machines (VMs), and VPN gateways. 

Assigning these policies, especially as they pertain to virtual machines, assist in controlling costs associated with deploying compute resources that are beyond what is necessary. 

<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-8.png?w=1024" alt="" class="wp-image-1218"/></figure></div>


<span style="text-decoration:underline;">Security governance</span>:  Securing and protecting resources within the environment is extremely important. 

Azure has many built-in policies for security available. These policies provide guidance for configuration policies of virtual machine guests, SQL databases, networking, monitoring, and Security Center. 

We will discuss this on the next slide, but enabling compliance controls and policies can audit resources for specific regulatory requirements that include a number of security controls. Reviewing these initiatives, you may find that auditing against one of the policies, such as NIST SP 800-53, could provide you with a strong security baseline for controls within your environment.   

When searching on the term security, you will find some helpful initiatives, such as auditing VMs for security baseline settings and auditing VMs with insecure password settings. Both initiatives protect exposure of resources and allow an administrator to be proactive to potential vulnerabilities. The Policy service dashboard provides an overview of compliance. 

If resources are non-compliant, they are identified and can be remediated directly from within the Policy service. 

Azure Security Center can also be used as a central source for monitoring controls for data, network, identity, and threat protection


<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-10.png?w=1024" alt="" class="wp-image-1221"/></figure></div>


When an organization is building a security program, they must take into account the two primary threats, internal and external. 

Internal threats are from inside of the organization while external threats are bad actors that are attempting to access something from outside of the organization.

Improperly identifying and addressing internal and external threats can leave organizational data at risk.  This can lead to data being exposed, compromised, and even lost, having negative affects on the organization both financially, and in the case of public companies, regulatory and reputational damage.

As with building a house, there are layers of protection to take into account within a technology infrastructure.  This is known as “defense in depth”.  There are typically seven layers to build a security program and protect organizational data. 


<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-3.png?w=688" alt="" class="wp-image-1199"/></figure></div>


These layers are:

1. Physical security which includes building security, such as exterior fences, concrete barriers, and doors.  In an Azure or public cloud ecosystem, the cloud provider is responsible for this. 

2. Identity and Access is properly designing user, group, and resource access that makes sure that access provided is only to what is needed to get the job done. 


3. Perimeter security layer includes the firewall with port rules and access control lists that protects what transmits inbound and outbound. 

4. Network security builds upon the perimeter security by segmenting your network with multiple virtual networks.  

5. Compute security includes hardening of the host or hypervisor, which is the responsibility of the cloud provider in a public hosting scenario, and operating system hardening and building a secure virtual machine baseline. 

6. At the application layer, it is important to make sure that proper security is in place for APIs and that there are no developer “backdoors” left open before an application is put into production.  If an application is accessing a database, that connection should be configured with proper roles and only allow internal connections.

7. At the center of it all is the data, which is ultimately what we are trying to protect as an organization.  The last line of defense here is to make sure that all data is encrypted at rest and in transit, that data is properly classified for role-based access, and that all encryption keys are protected and accessible when needed.

All of these layers should be continuously monitored for best practices and effectiveness.
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-2.png?w=1024" alt="" class="wp-image-1198"/></figure></div>


Shared responsibility within cloud environments is extremely important to understand.  Shared responsibility provides the guidelines of where Microsoft Azure responsibility ends and an organization's responsibility begins.  This responsibility is different among the cloud delivery models. 

Looking at the graphic, organizational responsibility and infrastructure control are a direct correlation when moving from infrastructure, platform, or software as a service models.

Even though the graphic shows organizational responsibility, it does not mean that Azure does not have the ability to provide services for an organization to maintain security and compliance.  In many cases, there are services available that need intervention to turn on and configure.

For example, data responsibility is considered an organization's responsibility across all cloud models.  However, Azure provides encryption at rest by default for storage accounts, and encryption options for databases.  For encryption in transit, the organization is required to configure https-only to transmit using TLS.

Another example of Azure services that assist in security and compliance is usage of Azure Policy services. 

<span style="text-decoration:underline;">Business governance</span>: The business and security governance areas are somewhat related. Both are focused on protecting the continued operation of the business. 

In terms of business governance, policies can be assigned to ensure that resources are created without violating any regulatory restrictions, such as GDPR. Azure has built-in policies for allowed locations that can be created for the entire subscription or can be assigned by resource group to segment jurisdiction as needed. 

Within the definitions, the parameters for data center locations are selected for where resources will be allowed to be created. If you are architecting the resource groups based on jurisdiction, the parameters can be assigned to only specific resource groups for segmentation. The ability to govern and audit where resources are created helps the business maintain compliance of where their data, backups, and sensitive information is held. In the event of an audit or legal seizure, proper jurisdictions can be verified and followed.  

<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-11.png?w=1024" alt="" class="wp-image-1224"/></figure></div>


Within the built-in policies, there are over a dozen initiatives specific to the category of <strong>regulatory compliance</strong>. Initiatives are made up of a group of policies. This includes ISO27001, PCI, NIST, FedRAMP, HITRUST/HIPAA, UK NHS, and Canada PBMM.  These are initiatives can be assigned to audit for these regulatory compliances. There are several policies within each of these audit initiatives.  If you find that an initiative does not fully suite the requirements for your organization, these initiatives can be cloned and adjusted to create a custom initiative for your organization.

Built-in regulatory compliance initiatives can be found at the link on the slide.

When you select an initiative, you can view the policies that are assigned. The NIST audit initiative itself has 798 policies that make up the audit. The ability to perform these audits are extremely helpful to a business since third party audits can be disruptive, time-consuming, and costly. 

It is important to note that not all policies are restricted to Azure resources. Azure Monitor services can be used for Azure and external resources, and the information fed into Azure monitor and Azure Security Center. Azure Policies are gathering the information for these audits through the same activity and diagnostic logging.  This enables an organization to have a central policy that audits a hybrid architecture for regulatory compliance.  <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/governance/policy/samples/built-in-initiatives#regulatory-compliance." target="_blank">https://docs.microsoft.com/en-us/azure/governance/policy/samples/built-in-initiatives#regulatory-compliance.</a>

<strong>What can Azure Security Center provide to manage policy and compliance?</strong>

Azure policy governs resource creation as well as audits existing resource compliance.  Azure Security Center is a central point review compliance and identify resources that are non-compliant.  When a resource is non-compliant, it is important to identify and resolve this issue through remediation.  Under remediations within the policy dashboard, a list of policies that need to be remediated is provided along with remediation tasks to become compliant.

<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-4.png?w=885" alt="" class="wp-image-1202"/></figure></div>


Much of the data collected from the activity logs, service logs, and policies are fed into the Azure Security Center dashboard, such as MFA, updates, policy compliance, and RBAC roles.  The security center dashboard can be used as a central source for policy and compliance of security controls.

As stated previously, Azure Security Center provides a central location for monitoring and managing your security posture.

Security Center provides a number of graphics and tools based on best practices that can assist you with: •Review policy and compliance to regulatory controls •Monitor resources to best practice security controls •Review network topology and traffic for potential external threats •Monitor and alert using advanced threat analysis and global threat intelligence maps


<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-5.png?w=747" alt="" class="wp-image-1204"/></figure></div>


Compliance to policies and initiatives all feed into Azure Security Center and acts a guide to assigning policies and controls through recommendations that are based on regulatory controls or industry best practices.

When enabling Azure Security Center for the standard subscription, four regulatory standards are enabled.  These are Azure CIS, PCI DSS, ISO 27001, and SOC TSP.  If your organization requires other standards to be enabled, those can be initiated through the Regulatory compliance menu of Security Center.

Within the Policy service definitions, there is a specific category for Security Center policies that can be assigned to allow data to be provided to the Security Center dashboard for an accurate Overall Secure Score for your subscription.  

Azure Security Center is a central source for the overall security health of your organization’s environment, from a business and security governance perspective. From this central dashboard, there is the ability to drill down and access areas of policy non-compliance and remediate resources to maintain a strong security posture. 

Additional information and a tutorial on utilizing security policy within Security Center can be found at the link <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/security-center/tutorial-security-policy" target="_blank">https://docs.microsoft.com/en-us/azure/security-center/tutorial-security-policy</a>.


Security Center regulatory compliance: 

Azure Security Center provides a number of benefits when enabling the Azure Defender subscription for regulatory compliance.  These include: 

Self-audit regularly for compliance to standards: Security Center's Regulatory compliance auditing capabilities provide you with a detailed list of all of the controls for that particular standard, and will show you whether you are red or green in that area.  If that control does not apply to your environment, it is grayed out.

<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-12.png?w=764" alt="" class="wp-image-1226"/></figure></div>


Being able to self-audit prepares you for the full compliance audits.  Using Azure Security Center's recommendations and remediating the areas of non-compliance will have you prepared when a regulatory audit takes place.  Avoiding potential costly fines for non-compliance and the need for additional reviews when rectifying missing controls.

Many organizations hire third party consultants to review their environments and provide reports on controls that are missing prior to their full audits.  Azure Security Center helps to save on these consulting fees because these reports are provided for you.

<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-6.png?w=591" alt="" class="wp-image-1206"/></figure></div>


Azure Security Center works very closed with Azure policy for regulatory compliance.  When enabling the Azure Defender subscription on your resources in Azure Security Center, there are default policies that are enabled for regulatory compliance.  These default policy assignments may not pertain to your organization.  You can leave them enabled or you can disable these policies and replace them with others.

<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-7.png?w=682" alt="" class="wp-image-1207"/></figure></div>

The screen capture above shows where you have the ability to disable the "out of the box" initiatives and adjust regulatory standards policy assignments by using the "Add more standards" selection.  This customizes your Regulatory compliance dashboard for those standards taht pertain to your organization. 

<strong>Using GitHub Actions with Azure Policy</strong>

For IT professionals that use GitHub Actions for their CI/CD pipelines, you can now integrate GitHub Actions with Azure Policy to export policy definitions and assignments to GitHub, push policy objects updated in GitHub to Azure, and trigger a compliance scan from the GitHub action. More information on this topic can be found here: <a rel="noreferrer noopener" href="https://github.com/marketplace/actions/azure-policy-compliance-scan#:~:text=%20GitHub%20Action%20for%20Azure%20Policy%20Compliance%20Scan,welcomes%20contributions%20and%20suggestions.%20Most%20contributions...%20More" target="_blank">Azure Policy Compliance Scan · Actions · GitHub Marketplace · GitHub</a>

As you have read, Azure Policy and Azure Security Center are two extremely helpful tools for assisting you in controlling various areas of governance for your resources within Azure.  You can find additional information within Microsoft Docs at the following links: 

<a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/governance/policy/overview#:~:text=Overview%201%20Understand%20evaluation%20outcomes.%20Resources%20are%20evaluated,Remediate%20non-compliant%20resources.%20...%204%20Video%20overview." target="_blank">Overview of Azure Policy - Azure Policy | Microsoft Docs</a>

<a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/security-center/" target="_blank">Azure Security Center documentation | Microsoft Docs</a>

View all of the posts for #AzureSpringClean for some excellent topics and information that will help you in managing and governing resources with Azure and in hybrid infrastructures.  <a href="https://www.azurespringclean.com/" target="_blank" rel="noreferrer noopener">Azure Spring Clean</a>

