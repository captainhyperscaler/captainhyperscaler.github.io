---
layout: post
title: So You want to be an Azure Solutions Architect Expert…the blog series...Security and Identity

---

<!-- wp:image {"align":"center","id":689,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2020/06/cll-azure-solution-architect-poster.jpg?w=1024" alt="" class="wp-image-689"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Welcome to this installment of the "So You want to be an Azure Solutions Architect Expert" series.  This is the fourth accompanying article, and it will focus on some key objectives that are part of the AZ-303 and AZ-304 exams.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To attend the session on Friday, July 17, 2020, please access the link for the <a rel="noreferrer noopener" href="https://www.cloudlunchlearn.com/" target="_blank">Cloud Lunch and Learn website</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>These sessions are also being recorded and posted on the <a rel="noreferrer noopener" href="https://www.youtube.com/channel/UCHZeZzSlTtmfgPozIq8J2Kw" target="_blank">Cloud Lunch and Learn YouTube channel</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In this session and article, I will be focusing on Security and Identity Management in Azure.  Building a strong security posture is an important foundation to the overall health and well-being of your organization.  This includes not only how you protect networks and infrastructure, but also how you architect and assign users and resources a secure identity to access services without exposing sensitive information to those that should not have access.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The key topics that I will be covering are potentially heavily tested topics within the exams, so the goal is that this information will provide you with a strong foundation of information that you can build upon as you prepare for the exams.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The topics that I will discuss on Friday include the following:  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Building a strong security posture through a defense in depth strategy</strong>: Before you begin to create resources with Azure, or any network infrastructure, it is important to understand the risks, vulnerabilities, and threats that you may face as an organization.  In addition, knowing the various privacy and regulatory requirements of the various countries that you may maintain resources and store data is also important.  Your network infrastructure is similar to building a house.  You don't build a house without choosing a location, creating an architectural blueprint of where your walls and doors are located, and what types of materials will be used for your doors to make your house secure.  All of this analysis is behind building a defense in depth security posture.  I spoke about this in a video created for the Global Azure Virtual event in April 2020.  You can find that video here: <a href="https://youtu.be/Dtwek-Kwb6s" target="_blank" rel="noreferrer noopener">https://youtu.be/Dtwek-Kwb6s</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure Active Directory, Identity and Access Management, and Conditional Access</strong>:  As more and more organizations begin their journey to Azure or other cloud technologies, how Identity and Access Management becomes extremely important.  When organizations had their own private networks and servers that were inside their own building walls, less diligence was placed on having strong passwords, separation of duties, or role-based access controls.  Much less complexity was placed on the creation of user profiles, but as the infrastructure footprint has expanded to organizations using co-location and now cloud technologies such as Azure, the role of identity and access management has come to the forefront.  No longer is it enough to protect your organization with strong perimeter security because the location of that perimeter has blurred.  Therefore, building a strong and thought out structure for user, group, and resource roles is necessary to protect from data exposure.  As an Azure Solutions Architect, understanding how to organize and structure these roles and configure conditional access for users and devices is a necessity.  Within the Microsoft ecosystem, Azure Active Directory becomes the source of cloud identity management.  More information on this topic can be found here in Microsoft docs: <a href="https://docs.microsoft.com/en-us/azure/active-directory/" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/active-directory/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Virtual Networks, Network Security Groups, and Azure Firewall</strong>: Even though I stated in the previous section that perimeter security has become blurred within cloud services, that does not make it unimportant.  When building a defense in depth security posture, all security layers are important to decreasing the attack surfaces and making it more difficult for bad actors to navigate their way to sensitive data.  Azure has various services to assist in the protection of this perimeter which include Virtual Networks (VNETs), Network Security Groups (NSGs), and Azure Firewall.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>VNETs </strong>are the foundational network components for your Azure resources.  A VNET is the address space and subnet that you will be deploying resources.  Multiple VNETs can be used to segment different workloads that may allow only certain users within your organization access, therefore, creating some barriers around different applications.  The concept of a VNET is very similar to how you would configure VLANs on switches to direct traffic and protect various services within an on-premises network.  VNETs in Azure can be connected together through peering to allow traffic to flow between VNETs, and these "peers" can be configured to block the flow of gateway traffic for added protection.  <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview" target="_blank">https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>NSGs are tied to the network interfaces of resources and allow rules to be created that control the flow of traffic.  These rules are inbound and outbound, and can be configured at the IP address, port, or resource level to further decrease the attack surface of your organization.  NSG rules are much like the rules that you would place on a router, gateway, or firewall device for your on-premises network.  This is a built in security service that is created by default within the Azure environment when deploying resources.  As an Azure Solutions Architect, you should understand how to design and create these rules to protect resources while maintaining access to resources for the organization.  <a href="https://docs.microsoft.com/en-us/azure/virtual-network/security-overview" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/virtual-network/security-overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure Load Balancer, Application Gateway, and Traffic Manager</strong>: Load balancers, Application gateways, and Traffic managers all perform a similar function within Azure.  That role is to direct traffic to resources.  As they direct traffic, they also have the ability to balance that traffic between resources, such as a set of virtual machines running a single application.  From a security standpoint, these services act as another layer of perimeter security to avoid exposure of virtual machines, databases, and containers to public IP addresses.  Since these resources are only routing devices, they do not have any data or sensitive information that can be exposed if hacked, therefore, increasing the strength of your security posture by again decreasing the attack surface.  More information on these resources can be found here:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Load balancer: <a href="https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/load-balancer/load-balancer-overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Application gateway: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/application-gateway/overview" target="_blank">https://docs.microsoft.com/en-us/azure/application-gateway/overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Traffic manager: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-overview" target="_blank">https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Front Door: <a href="https://azure.microsoft.com/en-us/services/frontdoor/">https://azure.microsoft.com/en-us/services/</a><a rel="noreferrer noopener" href="https://azure.microsoft.com/en-us/services/frontdoor/" target="_blank">frontdoor</a><a href="https://azure.microsoft.com/en-us/services/frontdoor/">/</a>.  This service provides a Web Application Firewall (WAF) and DDoS protection and global load balancing to your infrastructure.  This provides an extra layer of protection and works similar to a Traffic Manager, and can be used when you require TLS level encryption in transit and resiliency against a complete region failure. <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/frontdoor/front-door-overview" target="_blank">https://docs.microsoft.com/en-us/azure/frontdoor/front-door-overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure Key Vault and Recovery Services Vault</strong>: Azure Key Vault and Recovery Services Vault are mentioned here because they do add additional security to your organization.  We discussed Recovery Services Vault briefly in the IaaS session (<a rel="noreferrer noopener" href="https://captainhyperscaler.com/2020/07/02/so-you-want-to-be-an-azure-solutions-architect-expertthe-blog-series-iaas/" target="_blank">https://captainhyperscaler.com/2020/07/02/so-you-want-to-be-an-azure-solutions-architect-expertthe-blog-series-iaas/</a>).  Recovery Services Vault is the foundation of Azure Backup and Azure Site Recovery.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Key Vault differs from the Recovery Services Vault, as this is a service for organizations that want to manage and protect their encryption keys, certificates, and secrets within one location.  By default in the Azure environment, when data at rest is encrypted, it is assigned two Azure managed keys.  Some organizations require a segregation of duties within their cloud providers to not have the cloud provider manage the keys.  Azure Key Vault is a service that can meet that requirement by providing an area where a customer can manage their keys.  <a href="https://docs.microsoft.com/en-us/azure/key-vault/general/overview" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/key-vault/general/overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure Policy</strong>: Azure policy can be used to govern your Azure environment and resources, as well as resources outside of Azure.  Azure has hundreds of built-in policies that can be assigned and groups of policies known as initiatives that can assist an organization in auditing and managing regulatory requirements and controls.  I have written some articles in the past on this topic that can be found here: <a rel="noreferrer noopener" href="https://www.skylinesacademy.com/blog/2020/3/3/azure-security-part-2-understanding-azure-policies" target="_blank">https://www.skylinesacademy.com/blog/2020/3/3/azure-security-part-2-understanding-azure-policies</a> and a video for the Global Azure Virtual event here: <a rel="noreferrer noopener" href="https://youtu.be/2LmX3S-MQvM" target="_blank">https://youtu.be/2LmX3S-MQvM</a>.  More information can be found on Microsoft docs: <a href="https://docs.microsoft.com/en-us/azure/governance/policy/overview" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/governance/policy/overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure Monitor, Log Analytics, and Application Insights</strong>: The user of activity logs, boot diagnostics, and diagnostic logs are important to the security of an organization.  Without having these services enabled, there would be no manner in which to monitor, track, and investigate potentially suspicious activity within your environment.  As an Azure Solutions Architect, you must understand the use and role of each of these services in order to design how this will be deployed within the entire organizations infrastructure, both in Azure and external organizational virtual machines and networks. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Monitor: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/azure-monitor/overview" target="_blank">https://docs.microsoft.com/en-us/azure/azure-monitor/overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Log Analytics: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/azure-monitor/platform/log-analytics-agent" target="_blank">https://docs.microsoft.com/en-us/azure/azure-monitor/platform/log-analytics-agent</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Application Insights: <a href="https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure Security Center and Azure Sentinel</strong>:  The final topic of this article and this Cloud Lunch and Learn session are Azure Security Center and Azure Sentinel.  These two services bring together many of the services that were discussed earlier and provide central locations for monitoring and managing policies, best practices, and security controls (Azure Security Center), and monitor, alert, and investigate suspicious activity (Azure Sentinel).  I have talked about Azure Security Center as part of the Global Azure Virtual event videos that I posted earlier in this article.  I have also authored courses on both of these that are available at SkillMeUp.com.  <a rel="noreferrer noopener" href="https://skillmeup.com/course/bypath/implementing-azure-security" target="_blank">https://skillmeup.com/course/bypath/implementing-azure-security</a>  It is important to build in Azure Security Center for additional governance and visibility within your organization's security architecture.  <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/security-center/security-center-intro" target="_blank">https://docs.microsoft.com/en-us/azure/security-center/security-center-intro</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Sentinel is Microsoft's cloud-native SIEM solution.  If you are not utilizing a SIEM within your organization, Azure Sentinel can help to fill this security gap in a much shorter timeline than a typical on-premises SIEM solution.  <a href="https://docs.microsoft.com/en-us/azure/sentinel/overview" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/sentinel/overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>At a high level, these topics will be covered in my Cloud Lunch and Learn session on Friday, July 17, 2020. The recording will be located on the <a rel="noreferrer noopener" href="https://www.youtube.com/channel/UCHZeZzSlTtmfgPozIq8J2Kw" target="_blank">Cloud Lunch and Learn YouTube channel</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Additional links to assist in initial preparation include:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Cloud Lunch and Learn <a rel="noreferrer noopener" href="https://github.com/Cloud-Lunch-and-Learn/Cloud-Lunch-and-Learn-Sessions" target="_blank">github</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Build5Nines self-assessment tools: <a href="https://build5nines.com/free-oss-exam-self-assessment-tool/" target="_blank" rel="noreferrer noopener">https://build5nines.com/free-oss-exam-self-assessment-tool/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Microsoft Learn: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/learn/certifications/exams/az-300?wt.mc_id=learningredirect_certs-web-wwl" target="_blank">AZ-300</a> and <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/learn/certifications/exams/az-301?wt.mc_id=learningredirect_certs-web-wwl" target="_blank">AZ-301</a> on-demand training</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Greg posts Microsoft Docs links for every exam objective here: <a rel="noreferrer noopener" href="https://github.com/gsuttie/AzureResources/tree/master/Exams" target="_blank">Gregor Suttie github</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Pixel Robots is a helpful source of information, especially for AKS: <a href="https://pixelrobots.co.uk/" target="_blank" rel="noreferrer noopener">https://pixelrobots.co.uk/</a></p>
<!-- /wp:paragraph -->