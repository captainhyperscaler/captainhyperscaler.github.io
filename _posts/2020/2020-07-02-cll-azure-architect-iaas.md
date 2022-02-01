---
layout: post
title: So You want to be an Azure Solutions Architect Expert…the blog series...IaaS

---

<!-- wp:image {"align":"center","id":689,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2020/06/cll-azure-solution-architect-poster.jpg?w=1024" alt="" class="wp-image-689"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Welcome to this installment of the "So You want to be an Azure Solutions Architect Expert" series.  This is the second accompanying article, and it will focus on some key objectives that are part of the AZ-303 and AZ-304 exams.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To attend the session on Monday, July 6, 2020, please access the link for the <a rel="noreferrer noopener" href="https://www.cloudlunchlearn.com/" target="_blank">Cloud Lunch and Learn website</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>These sessions are also being recorded and posted on the <a rel="noreferrer noopener" href="https://www.youtube.com/channel/UCHZeZzSlTtmfgPozIq8J2Kw" target="_blank">Cloud Lunch and Learn YouTube channel</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In this session and article, I will be focusing on IaaS in Azure.  Infrastructure as a Service (IaaS) primarily focuses on the virtual machine ecosystem and how we create, configure, and manage these within Azure.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The key topics that I will be covering are potentially heavily tested topics within the exams, so the goal is that this information will provide you with a strong foundation of information that you can build upon as you prepare for the exams.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>These topics are: operating systems, virtual machine sizes, managed storage for VMs, encryption, VM baselines, high availability, scalability, backup, replication, and recovery.  It is important to note that these sessions bring together the objectives of both exams to assist you in preparation.  This discussion speaks to Azure Site Recovery which is a heavy objective topic on the AZ-304 exam and not on the AZ-303 exam.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a href="https://docs.microsoft.com/en-us/azure/virtual-machines/windows/overview" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/virtual-machines/windows/overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Operation systems and sizing for Virtual Machines within Azure</strong>: When preparing for these exams, it is important to understand the operating system and sizing options for virtual machines, along with the ability to choose the correct sized virtual machine for a workload.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There are currently four (4) Windows options and six (6) Linux options for operating systems when creating a virtual machine in Azure.  These are the operating systems that would be fully licensed as part of the virtual machine cost.  Microsoft also provides the option to "Bring your own license (BYOL)" for older Windows operating systems that are within an organizations Enterprise Agreement (EA) with Software Assurance (SA).  An example of this is Windows Server 2008, which reach its EOL date on January 14, 2020.  However, organizations with an EA on this license that includes SA, can install this license on an Azure VM and continue to receive security updates, ONLY in Azure, for three additional years. The supported operating systems that can be licensed within an Azure virtual machine image are for Windows: Server 2016 Datacenter, Server 2019 Datacenter, Server 2012 R2 Datacenter, and Windows 10 Pro. For Linux: Ubuntu Server 18.04 or 16.04, Red Hat Enterprise 8.1, SUSE Enterprise 15, CentOS 8.1, and Debian 10 “Buster”.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>There are many different virtual machine sizing options to consider within Azure.  The best option for determining the server series to use would be to follow the Azure guidelines based on the grouping types.  These can be found within Azure docs here:  <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes" target="_blank">https://docs.microsoft.com/en-us/azure/virtual-machines/windows/sizes</a>.  There are six types of servers.  They are general purpose, compute optimized, memory optimized, storage optimized, GPU, and high performance compute. Knowing the series of VM that falls into each of these categories should be understood before taking either exam.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Storage, encryptions, and virtual machine baselines</strong>: These objectives are being grouped together as part of this session mainly because they are important to understand conceptually for these exams, but the services themselves are covered in much more detail if you are preparing for the Azure Security Engineer Associate exam (AZ-500).  The keys points for storage are that a virtual machine should utilize managed disks for file storage, and for most of the VM sizes, there is the option for Standard HDD (spinning disks), and Standard or Premium SSD (solid state).  Some high performance or memory optimized types also have Ultra SSD available.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The important part of virtual machine encryption is to understand that all storage within Azure has encryption at rest configured by default.  However, in order for a virtual machine to have both the OS and disk encrypted, Azure Disk Encryption must be enabled on the virtual machine.  <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/security/azure-security-disk-encryption#overview" target="_blank">https://docs.microsoft.com/en-us/azure/security/azure-security-disk-encryption#overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The final topic within this section is creating a virtual machine baseline with <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/virtual-machines/extensions/dsc-overview#:~:text=%20Introduction%20to%20the%20Azure%20Desired%20State%20Configuration,extension%20uses%20the%20Azure%20VM%20Agent...%20More%20" target="_blank">Desired State Configuration</a>.  This service within Azure allows an organization to create an automated deployment of virtual machines based on a corporate standard that includes required extensions and software required for these virtual machines.  DSC is a very helpful automation option within Azure to maintain a security standard for virtual machines.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>High availability and scalability</strong>:  I tend to spend a bit of time when training students on the differences of availability and scalability within Azure.  Though they are understandably different concepts within the cloud ecosystem, when discussing how an availability set or scale set function and are billed within Azure, it causes some confusion.  I went into this within some detail in a recent <a href="https://youtu.be/MJSfpfs--UA" target="_blank" rel="noreferrer noopener">Skylines Summer Session video</a>.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Virtual Machine Availability sets create an infrastructure that avoids an application from going off-line due to a single virtual machine failure.  Within Azure, this is accomplished through increasing the number of virtual machines that are deployed and assigning them to different update domains, fault domains, and/or availability zones.  Fault domains can be equated to separate racks to avoid an off-schedule failure of a PDU or switch on a rack, for example.  Update domains would be putting servers on different hypervisor stacks to avoid downtime from updates on the hypervisor host.  Availability zones are placing these fault and update domains within different physical datacenter buildings.  When configuring an availability set, understand that the number of virtual machines within that set are "always on" virtual machines and you are paying for the compute on each.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Virtual Machine Scale Sets take advantage of the elasticity of the cloud.  In contrast to an availability set with maintains that an application does not go down due to a failure, an availability set allows for applications demand is met by increasing or decreasing compute resources based on that demand and the capacity requirements.  Automated conditions, or triggers, are created that enforce an action to scale out or scale in virtual machines, meaning adding or decreasing the number of virtual machines that are running that application.  The costs of these virtual machines is much more dynamic than with an availability set.  You only pay for the compute on the virtual machines that are turned on and once these virtual machines scale in, the costs decrease.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Whether you are utilizing availability sets or scale sets, you should utilize a load balancer for directing traffic equally to virtual machines and avoid the need for public IP address on the virtual machines.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Replication, Backup, and Site Recovery</strong>: The final area that I will cover in this session is around replication, backup, and site recovery.  Each of these areas assist in the business continuity and disaster recovery planning of an organization.  Each one of these service areas are an important component to maintaining an available infrastructure that maintains its data and application integrity.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Storage replication is an intrinsic part of all storage accounts within Azure.  When a storage account is created, replication of blobs and files is included, with the number of replicas being determined by the level that you select.  The three primary levels are Local-redundant storage (LRS), Zone-redundant storage (ZRS), and Global-redundant storage (GRS).  LRS and ZRS both provide three (3) replicas of any object/file within the storage account, and GRS provides six (6).  These replicas protect your storage from becoming unavailable in the case of Azure having a failure in the storage array within a data center, and ZRS spreads the objects across the datacenter buildings within a region.  GRS goes a step further to protect against an entire Azure region failure.  This replication does not protect an organization from a object or file becoming corrupt or accidentally deleted.  Enabling "soft delete" does protect against accidental deletion by sending deleted files to a recycle bin for up to a year.  If one copy is corrupt, they all become corrupt.  To protect further from file corruption, Azure Backup should be used.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Backup can protect against corrupt files and virtual machine images within Azure and on-premises through saving snapshots of VMs and disks that are kept based on organization defined retention policies.  If a virtual machine image were to become corrupt, the last confirmed snapshot can be used to create a new virtual machine and get back online relatively quickly.  This is not an automated process of recovery.  If automated recovery is required, Azure Site Recovery could be utilized.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Site Recovery is the component within this section that can assist in automated recovery and decreased RTO (recovery time objective) to a failure in virtual machine workloads or an entire data center.  If maintaining business continuity and having disaster recovery in place is important to your organization, Azure Site Recovery provides a very cost effective and efficient solution without the need to invest in expensive hardware and software.  Azure Site Recovery has the ability to replicate and recover servers that are in on-premises and Azure datacenters.  It is also an effective tool that can be utilized for migrating workload to Azure.</p>
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