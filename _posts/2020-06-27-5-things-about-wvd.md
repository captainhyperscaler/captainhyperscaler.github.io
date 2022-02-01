---
layout: post
title: 5 Things that I learned about a Windows Virtual Desktop deployment in Azure

---

<!-- wp:image {"align":"center","id":713,"width":383,"height":377,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><img src="https://captainhyperscaler.files.wordpress.com/2020/06/img_0433.jpg?w=1024" alt="" class="wp-image-713" width="383" height="377"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Back in April, I attended a presentation that explained the architecture. I thought that the ability to leverage your M365 subscription along with the Azure infrastructure was interesting, but the deployment did not, at the time, differentiate itself from a more mature Citrix VDI architecture.  This perspective changed this month as I had the opportunity to build a workshop and lab for a Windows Virtual Desktop (WVD) infrastructure in Azure.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Here are some things that I learned while configuring the infrastructure for WVD. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>1. Make sure that you have the proper Microsoft 365 licensing for your users. Windows 10 multi-user and ProPlus download is required. Deploying Windows virtual desktops in Azure has some excellent advantages over other Windows VDI deployment options (i.e. Citrix or VMware Horizon). The most important of these is no longer needing to have remote desktop SPLA and VDA licensing when assigning users the proper Microsoft 365 subscription that supports multi-session Windows 10 licensing.  These licenses are included with Microsoft 365 Business Premium for SMB organizations (under 300 users), and M365 E3 and E5 for Enterprise organizations. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>2. Active Directory Domain Services with Azure AD Connect to Azure Active Directory is a must.  At the time of this article creation, architecting a Windows Virtual Desktop infrastructure requires a hybrid join to Azure Active Directory. This means that if you are not currently utilizing an on-premises Active Directory domain, though most organizations likely still have this in place, you would be required to deploy Active Directory Domain Services (ADDS) on a virtual machine in Azure. Once that virtual machine is created and configured for ADDS, you will then install Azure AD Connect to synchronize using either Password Hash Sync or Pass Through Authentication. Since Windows Virtual Desktop is utilizing the M365 subscription, this Azure AD Connect hybrid architecture is necessary. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>3. Create your standard image with Office 365 ProPlus downloaded and installed.  The subscriptions that support the Windows 10 multi-session deployment are also ones that include the Office 365 ProPlus download. This is helpful for having the proper licensing in place to configure your standard desktop image for users. When preparing the image, it is important to download and install Office 365 ProPlus on that image including Microsoft Teams for proper collaboration, meeting, and chat functionality. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>4. Azure portal can be used to deploy the infrastructure.  Microsoft just recently updated the Azure Resource Manager (i.e. Azure Portal) with the ability to deploy the Windows Virtual Desktop virtual machine host pools. This makes the creation of these scales sets much easier four those that are not fully comfortable with PowerShell or CLI commands. Before this update, using deployment code commands had been the only option for creating this infrastructure, providing little advantage over completing products. The ability to quickly deploy this host pool helps to get the Windows Virtual Desktop infrastructure ready on short notice, making it a great option when initiating a business continuity plan. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>5. WVD is a great option for managing secure remote workers. The last point that I'm going to make regarding Windows Virtual Desktop brings together the previous four. That is that the advantages that Microsoft has put in place to minimize additional licensing while leveraging many of the M365 subscriptions that enterprises are utilizing today, has made this an excellent option for an organization's IT department to centrally monitor and manage the user desktop experience. WVD enables business continuity without sacrificing security and compliance as more organizations move to a remote worker environment. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>If you are interested in understanding more about Windows Virtual Desktop, I recommend that you review the information available on Microsoft at the links provided below. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Overview and Tutorials: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/virtual-desktop/overview" target="_blank">https://docs.microsoft.com/en-us/azure/virtual-desktop/overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Microsoft Learn modules: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/learn/browse/?terms=Windows%20Virtual%20Desktop" target="_blank">https://docs.microsoft.com/en-us/learn/browse/?terms=Windows%20Virtual%20Desktop</a></p>
<!-- /wp:paragraph -->