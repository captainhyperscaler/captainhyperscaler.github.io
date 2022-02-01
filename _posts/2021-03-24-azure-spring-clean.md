---
layout: post
title: AzureSpringClean - Using Azure Policy and Security Center for Organizational Governance. https://www.azurespringclean.com/

---

<!-- wp:paragraph -->
<p>This is my 2021 #AzureSpringClean contribution.  Special thanks to Joe Carlyle (@<a rel="noreferrer noopener" href="https://twitter.com/wedoazure" target="_blank">wedoazure</a>) and Thomas Thornton (@<a rel="noreferrer noopener" href="https://twitter.com/tamstar1234" target="_blank">tamstar1234</a>) for putting together this event for another year.  All of the posts for this year's event can be found at <a rel="noreferrer noopener" href="https://www.azurespringclean.com/" target="_blank">Azure Spring Clean</a>. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>This post covers how to use the tools of Azure Policy and Azure Security Center to govern your resources in Azure, as well as on hybrid infrastructures.  The topics that will be covered in this article are:</p>
<!-- /wp:paragraph -->

<!-- wp:list {"ordered":true} -->
<ol><li>What is Azure Policy and initiatives?</li><li>How can they be utilized for organizational governance?</li><li>What can Azure Security Center provide to manage policy and compliance?</li><li>How can GitHub Actions be used for Policy governance?</li><li>How can you monitor and maintain policy compliance</li></ol>
<!-- /wp:list -->

<!-- wp:paragraph -->
<p><strong>What is Azure Policy and initiatives?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Before we discuss how it can help, it is important to understand Azure Policy.  Azure Policy can be used to govern cost, security, and jurisdiction for your organization’s infrastructure.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure has hundreds of pre-built policies based on best practices that can be assigned to monitor and manage subscriptions and resources.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Initiatives are made up of a group of policies.&nbsp; Pre-built initiatives within Azure provide the ability to easily configure your subscription or resource groups for regulatory governance.&nbsp; Assigning initiatives to resources will audit those resources for compliance, and then provide the ability to remediate those resources for compliance.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1192,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image.png?w=697" alt="" class="wp-image-1192"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Microsoft Azure holds many cloud attestations for their buildings and infrastructure.&nbsp; Some of the popular ones are on this slide and a full list can be found at the link provided.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>It is important to understand what these attestations mean to an organization that is moving their workloads into Azure.&nbsp; If your organization requires a regulatory compliance, Azure definitely assists in putting you on the path to adhering to the requirements.&nbsp; However, compliance goes beyond the attestations held by Azure or other cloud providers.&nbsp; There are processes, procedures, and controls that are all part of the audit guidelines.&nbsp; The benefit of Azure attestations is that utilizing their infrastructure decreases the amount of architecture investment required to build out a compliant environment.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>As with any hosted environment, there is a partnership of shared responsibility that needs to be understood.  These attestations can get you on the first steps to regulatory compliance, but you are responsible to enable many of the controls necessary for full compliance and to pass an audit.  Azure Policy can assist in identifying these and provide recommendations to get you to where you need to be.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1194,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-1.png?w=816" alt="" class="wp-image-1194"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><strong>How can they be utilized for organizational governance?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Policy is a very helpful service within Azure, and it can assist in many ways.  We will discuss the role that Azure Policy can be used for organizational, financial, security, and business governance.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><span style="text-decoration:underline;">Organizational governance</span>: Challenges arise within&nbsp;a cloud environment when resources&nbsp;can&nbsp;be created that may affect, cost, security, or regulatory jurisdictions.&nbsp;Governing your environment for financial, business, and security&nbsp;will&nbsp;be&nbsp;discussed&nbsp;further&nbsp;in the following&nbsp;sections, but it is important to understand the role that Azure can play in assisting you in monitoring and management.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure policies&nbsp;are created, assigned, and utilized to govern the resources within your Azure subscription.&nbsp;Policies can be assigned using the&nbsp;built-in&nbsp;policies within Azure, of which&nbsp;there are hundreds, or custom policies can be created that&nbsp;may be necessary for your specific organizational needs.&nbsp; A list of these policies can be found at the link on the slide</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Policies should be&nbsp;assigned at the beginning of building your environment in&nbsp;Azure&nbsp;but they can also be retroactively&nbsp;created,&nbsp;and existing resources can be audited against these policies.&nbsp;Determining the policies&nbsp;to put&nbsp;in place&nbsp;should be&nbsp;based a business, security, and financial&nbsp;discussion.&nbsp;<a href="https://docs.microsoft.com/en-us/azure/governance/policy/samples/built-in-policies" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/governance/policy/samples/built-in-policies</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><span style="text-decoration:underline;">Financial governance</span>:  Most of the&nbsp;financial and cost governance can be&nbsp;monitored and managed through the cost and billing services&nbsp;and&nbsp;Azure Advisor, with spending limits and controls being put in place for the subscription and resources.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There are&nbsp;also policies that can be put in place for controlling costs and&nbsp;performance compliance by assigning specific SKUs&nbsp;that are allowed within storage accounts, virtual machines&nbsp;(VMs), and VPN gateways.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Assigning these policies, especially as they pertain to&nbsp;virtual machines, assist in controlling costs&nbsp;associated with deploying compute resources that are beyond what is necessary.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1218,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-8.png?w=1024" alt="" class="wp-image-1218"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><span style="text-decoration:underline;">Security governance</span>:  Securing and protecting resources within&nbsp;the environment is extremely important.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure has many&nbsp;built-in policies for security&nbsp;available.&nbsp;These&nbsp;policies provide guidance for configuration policies of virtual machine guests, SQL databases,&nbsp;networking, monitoring, and Security Center.&nbsp;&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>We will discuss this on the next slide, but enabling compliance controls and policies&nbsp;can audit resources for specific regulatory requirements that include a number of security controls.&nbsp;Reviewing these initiatives, you may find that auditing against one of the policies, such as NIST SP 800-53,&nbsp;could provide you with a strong security baseline for controls within your environment.&nbsp; &nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>When searching&nbsp;on the term security, you will find some helpful initiatives, such as auditing VMs for&nbsp;security baseline settings and auditing VMs with insecure password settings.&nbsp;Both initiatives&nbsp;protect exposure of resources and allow an administrator to be proactive to potential vulnerabilities.&nbsp;The Policy service dashboard&nbsp;provides an overview of compliance.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If resources are non-compliant, they are identified and can be remediated directly from within the Policy&nbsp;service.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Security Center can also be used as a central source for monitoring controls for data, network, identity, and threat protection</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1221,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-10.png?w=1024" alt="" class="wp-image-1221"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>When an organization is building a security program, they must take into account the two primary threats, internal and external.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Internal threats are from inside of the organization while external threats are bad actors that are attempting to access something from outside of the organization.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Improperly identifying and addressing internal and external threats can leave organizational data at risk.&nbsp; This can lead to data being exposed, compromised, and even lost, having negative affects on the organization both financially, and in the case of public companies, regulatory and reputational damage.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>As with building a house, there are layers of protection to take into account within a technology infrastructure.&nbsp; This is known as “defense in depth”.&nbsp; There are typically seven layers to build a security program and protect organizational data.&nbsp; </p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1199,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-3.png?w=688" alt="" class="wp-image-1199"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>These layers are: </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>1.Physical security which includes building security, such as exterior fences, concrete barriers, and doors.&nbsp; In an Azure or public cloud ecosystem, the cloud provider is responsible for this. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>2.Identity and Access is properly designing user, group, and resource access that makes sure that access provided is only to what is needed to get the job done. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>3.Perimeter security layer includes the firewall with port rules and access control lists that protects what transmits inbound and outbound. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>4.Network security builds upon the perimeter security by segmenting your network with multiple virtual networks.&nbsp; </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>5.Compute security includes hardening of the host or hypervisor, which is the responsibility of the cloud provider in a public hosting scenario, and operating system hardening and building a secure virtual machine baseline. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>6.At the application layer, it is important to make sure that proper security is in place for APIs and that there are no developer “backdoors” left open before an application is put into production.&nbsp; If an application is accessing a database, that connection should be configured with proper roles and only allow internal connections. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>7.At the center of it all is the data, which is ultimately what we are trying to protect as an organization.&nbsp; The last line of defense here is to make sure that all data is encrypted at rest and in transit, that data is properly classified for role-based access, and that all encryption keys are protected and accessible when needed.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>All of these layers should be continuously monitored for best practices and effectiveness.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1198,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-2.png?w=1024" alt="" class="wp-image-1198"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Shared responsibility within cloud environments is extremely important to understand.&nbsp; Shared responsibility provides the guidelines of where Microsoft Azure responsibility ends and an organization's responsibility begins.&nbsp; This responsibility is different among the cloud delivery models.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Looking at the graphic, organizational responsibility and infrastructure control are a direct correlation when moving from infrastructure, platform, or software as a service models.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Even though the graphic shows organizational responsibility, it does not mean that Azure does not have the ability to provide services for an organization to maintain security and compliance.&nbsp; In many cases, there are services available that need intervention to turn on and configure.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>For example, data responsibility is considered an organization's responsibility across all cloud models.&nbsp; However, Azure provides encryption at rest by default for storage accounts, and encryption options for databases.&nbsp; For encryption in transit, the organization is required to configure https-only to transmit using TLS.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Another example of Azure services that assist in security and compliance is usage of Azure Policy services.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><span style="text-decoration:underline;">Business governance</span>: The business and security governance&nbsp;areas are somewhat related.&nbsp;Both are focused on protecting&nbsp;the continued operation of the business.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In terms of&nbsp;business governance, policies can be assigned to&nbsp;ensure that resources are created&nbsp;without violating any regulatory restrictions, such as GDPR.&nbsp;Azure has&nbsp;built-in policies&nbsp;for allowed locations&nbsp;that can be created for the entire subscription or can be assigned by resource group to segment jurisdiction&nbsp;as needed.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Within the definitions, the&nbsp;parameters for&nbsp;data center locations are selected&nbsp;for where resources will be allowed to be created.&nbsp;If you are architecting the resource groups based on jurisdiction, the parameters can be&nbsp;assigned to only specific resource groups for segmentation.&nbsp;The ability to govern and audit where resources&nbsp;are created&nbsp;helps the business maintain compliance of where their data, backups,&nbsp;and&nbsp;sensitive information is held.&nbsp;In the event of an audit or legal&nbsp;seizure, proper&nbsp;jurisdictions can be&nbsp;verified and followed.&nbsp;&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1224,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-11.png?w=1024" alt="" class="wp-image-1224"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Within the built-in policies, there are&nbsp;over a dozen&nbsp;initiatives&nbsp;specific to the category of&nbsp;<strong>regulatory compliance</strong>.&nbsp;Initiatives are made up of a group of policies.&nbsp;This includes&nbsp;ISO27001,&nbsp;PCI, NIST, FedRAMP, HITRUST/HIPAA, UK NHS,&nbsp;and Canada PBMM.&nbsp; These are initiatives&nbsp;can be assigned to audit for these regulatory compliances.&nbsp;There are&nbsp;several&nbsp;policies within each of these&nbsp;audit&nbsp;initiatives.&nbsp; If you find that an initiative does not fully suite the requirements for your organization, these initiatives can be cloned and adjusted to create a custom initiative for your organization.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Built-in regulatory compliance initiatives can be found at the link on the slide.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>When you select an&nbsp;initiative, you&nbsp;can&nbsp;view the&nbsp;policies that are assigned.&nbsp;The NIST audit&nbsp;initiative&nbsp;itself has 798 policies&nbsp;that make up the audit.&nbsp;The ability to perform these audits are extremely helpful to a business&nbsp;since third party audits can be disruptive, time-consuming, and costly.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>It is important to note that not all policies are restricted to Azure resources.&nbsp;Azure&nbsp;Monitor services can be used for Azure and external resources, and the information&nbsp;fed&nbsp;into Azure monitor and Azure Security Center.&nbsp;Azure Policies are gathering&nbsp;the information for these audits through the same activity and diagnostic logging.&nbsp; This enables an organization to have a central policy that audits&nbsp;a hybrid architecture for regulatory compliance.&nbsp; <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/governance/policy/samples/built-in-initiatives#regulatory-compliance." target="_blank">https://docs.microsoft.com/en-us/azure/governance/policy/samples/built-in-initiatives#regulatory-compliance.</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>What can Azure Security Center provide to manage policy and compliance?</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure policy governs resource creation as well as audits existing resource compliance.&nbsp; Azure Security Center is a central point review compliance and identify resources that are non-compliant.&nbsp; When a resource is non-compliant, it is important to identify and resolve this issue through remediation.&nbsp; Under remediations within the policy dashboard, a list of policies that need to be remediated is provided along with remediation tasks to become compliant.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1202,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-4.png?w=885" alt="" class="wp-image-1202"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Much of the data collected from the activity logs, service logs, and policies are fed into the Azure Security Center dashboard, such as MFA, updates, policy compliance, and RBAC roles.&nbsp; The security center dashboard can be used as a central source for policy and compliance of security controls.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>As stated previously, Azure Security Center provides a central location for monitoring and managing your security posture.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Security Center provides a number of graphics and tools based on best practices that can assist you with: •Review policy and compliance to regulatory controls •Monitor resources to best practice security controls •Review network topology and traffic for potential external threats •Monitor and alert using advanced threat analysis and global threat intelligence maps</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1204,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-5.png?w=747" alt="" class="wp-image-1204"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Compliance to policies and initiatives&nbsp;all feed into Azure Security Center&nbsp;and acts a guide to assigning policies&nbsp;and controls through recommendations that are based on regulatory controls or industry best practices.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>When enabling Azure Security Center for the standard subscription, four regulatory standards are enabled.&nbsp; These are Azure CIS, PCI DSS, ISO 27001, and SOC TSP.&nbsp; If your organization requires other standards to be enabled, those can be initiated through the Regulatory compliance menu of Security Center.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Within the Policy service definitions, there is a specific category&nbsp;for Security Center policies that can be assigned&nbsp;to allow data to be provided to the Security Center dashboard for an accurate&nbsp;Overall Secure Score for your subscription.&nbsp;&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Security Center is a central source for&nbsp;the overall security health of your organization’s environment, from a business and security governance perspective.&nbsp;From this central dashboard, there is the ability to drill down and access areas of policy non-compliance and remediate resources to maintain a strong security posture.&nbsp;</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Additional information and a tutorial on utilizing security policy within Security Center can be found at the link <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/security-center/tutorial-security-policy" target="_blank">https://docs.microsoft.com/en-us/azure/security-center/tutorial-security-policy</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Security Center regulatory compliance: </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Security Center provides a number of benefits when enabling the Azure Defender subscription for regulatory compliance.  These include: </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Self-audit regularly for compliance to standards: Security Center's Regulatory compliance auditing capabilities provide you with a detailed list of all of the controls for that particular standard, and will show you whether you are red or green in that area.  If that control does not apply to your environment, it is grayed out.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1226,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-12.png?w=764" alt="" class="wp-image-1226"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Being able to self-audit prepares you for the full compliance audits.  Using Azure Security Center's recommendations and remediating the areas of non-compliance will have you prepared when a regulatory audit takes place.  Avoiding potential costly fines for non-compliance and the need for additional reviews when rectifying missing controls.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Many organizations hire third party consultants to review their environments and provide reports on controls that are missing prior to their full audits.  Azure Security Center helps to save on these consulting fees because these reports are provided for you.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1206,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-6.png?w=591" alt="" class="wp-image-1206"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Azure Security Center works very closed with Azure policy for regulatory compliance.  When enabling the Azure Defender subscription on your resources in Azure Security Center, there are default policies that are enabled for regulatory compliance.  These default policy assignments may not pertain to your organization.  You can leave them enabled or you can disable these policies and replace them with others.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":1207,"sizeSlug":"large","linkDestination":"none"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2021/03/image-7.png?w=682" alt="" class="wp-image-1207"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>The screen capture above shows where you have the ability to disable the "out of the box" initiatives and adjust regulatory standards policy assignments by using the "Add more standards" selection.  This customizes your Regulatory compliance dashboard for those standards taht pertain to your organization.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Using GitHub Actions with Azure Policy</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>For IT professionals that use GitHub Actions for their CI/CD pipelines, you can now integrate GitHub Actions with Azure Policy to export policy definitions and assignments to GitHub, push policy objects updated in GitHub to Azure, and trigger a compliance scan from the GitHub action. More information on this topic can be found here: <a rel="noreferrer noopener" href="https://github.com/marketplace/actions/azure-policy-compliance-scan#:~:text=%20GitHub%20Action%20for%20Azure%20Policy%20Compliance%20Scan,welcomes%20contributions%20and%20suggestions.%20Most%20contributions...%20More" target="_blank">Azure Policy Compliance Scan · Actions · GitHub Marketplace · GitHub</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>As you have read, Azure Policy and Azure Security Center are two extremely helpful tools for assisting you in controlling various areas of governance for your resources within Azure.  You can find additional information within Microsoft Docs at the following links: </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/governance/policy/overview#:~:text=Overview%201%20Understand%20evaluation%20outcomes.%20Resources%20are%20evaluated,Remediate%20non-compliant%20resources.%20...%204%20Video%20overview." target="_blank">Overview of Azure Policy - Azure Policy | Microsoft Docs</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/security-center/" target="_blank">Azure Security Center documentation | Microsoft Docs</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>View all of the posts for #AzureSpringClean for some excellent topics and information that will help you in managing and governing resources with Azure and in hybrid infrastructures.  <a href="https://www.azurespringclean.com/" target="_blank" rel="noreferrer noopener">Azure Spring Clean</a></p>
<!-- /wp:paragraph -->
