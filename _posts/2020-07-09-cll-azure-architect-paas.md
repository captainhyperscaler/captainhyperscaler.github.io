---
layout: post
title: So You want to be an Azure Solutions Architect Expert…the blog series...PaaS

---

<!-- wp:image {"align":"center","id":689,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2020/06/cll-azure-solution-architect-poster.jpg?w=1024" alt="" class="wp-image-689"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Welcome to this installment of the "So You want to be an Azure Solutions Architect Expert" series.  This is the third accompanying article, and it will focus on some key objectives that are part of the AZ-303 and AZ-304 exams.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To attend the session on Monday, July 6, 2020, please access the link for the <a rel="noreferrer noopener" href="https://www.cloudlunchlearn.com/" target="_blank">Cloud Lunch and Learn website</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>These sessions are also being recorded and posted on the <a rel="noreferrer noopener" href="https://www.youtube.com/channel/UCHZeZzSlTtmfgPozIq8J2Kw" target="_blank">Cloud Lunch and Learn YouTube channel</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In this session and article, I will be focusing on PaaS in Azure.  Platform as a Service (PaaS) focuses on those services that Azure provides the entire OS and infrastructure, including the updates and upgrades.  Allowing you to focus on your applications and code.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The key topics that I will be covering are potentially heavily tested topics within the exams, so the goal is that this information will provide you with a strong foundation of information that you can build upon as you prepare for the exams.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>These topics are: Azure App Services, Logic Apps, Azure Functions, Azure Kubernetes and Azure Container Instances, Cosmos DB, Azure SQL Database, and other serverless services within Azure that are touch on, such as Event Grid, Event Hub, Service Bus, and Cognitive Services.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure App Services</strong>: When preparing for these exams, it is important to have a strong understanding of App Services.  The various use cases and capabilities of each of the App Services subscription tiers will definitely be seen on these exams.  Selection of the proper service tier and what features may require you to "scale up" your subscription will be something that you should know before going into the exam.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Additional information can be found here: <a href="https://docs.microsoft.com/en-us/azure/app-service/" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/app-service/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Logic Apps</strong>: Great to for creating a workflow within Azure.  Utilizes a graphical designer to orchestrate and automate tasks based on triggered conditions.  This service also has the ability to integrate with services inside and outside of the Microsoft ecosystem.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Additional information on Logic Apps can be found here: <a href="https://docs.microsoft.com/en-us/azure/logic-apps/" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/logic-apps/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure Functions</strong>:  Another service that can initiate a workflow within Azure.  Unlike Logic Apps that utilize a graphical designer to create your workflow.  Azure Functions utilize pieces of code that are executed on a triggered event.  These triggered events come from a variety of services, including Event Grid and Event Hub, among others.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Function information can be found here:  <a href="https://docs.microsoft.com/en-us/azure/azure-functions/functions-overview" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/azure-functions/functions-overview</a> </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure Kubernetes Service (AKS) vs. Azure Container Instances</strong> (ACI): For this exam, it is important to have a foundational understanding on how containers work and how they are used within App services.  In addition, being able to determine the differences between AKS and ACI are important for architecting an application platform.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>More can be found on both of these services at these links:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>AKS: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/aks/intro-kubernetes" target="_blank">https://docs.microsoft.com/en-us/azure/aks/intro-kubernetes</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>ACI: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/container-instances/container-instances-overview" target="_blank">https://docs.microsoft.com/en-us/azure/container-instances/container-instances-overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Databases</strong>: Understanding databases is new variable including in the Architect Expert exams that is not found in exams such as the Azure Administrator Associate exam.  I mentioned in the introduction session that the AZ-300/303 exam is about 80-85% the same as the AZ-104.  Databases is the majority of that delta of new material.  The objectives for databases cover mainly Azure SQL database and Cosmos DB.  It is important to understand the selection of one or the other, as well as the other options for running a SQL Server within Azure: SQL Virtual Machine and Managed SQL Instance.  For Cosmos DB, knowing the consistency level options and how they affect latency and availability are also important.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>More information on both can be found in Microsoft docs:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure SQL: <a href="https://docs.microsoft.com/en-us/azure/azure-sql/database/sql-database-paas-overview" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/azure-sql/database/sql-database-paas-overview</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Cosmos DB: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/cosmos-db/introduction" target="_blank">https://docs.microsoft.com/en-us/azure/cosmos-db/introduction</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Cosmos DB consistency levels: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/cosmos-db/consistency-levels" target="_blank">https://docs.microsoft.com/en-us/azure/cosmos-db/consistency-levels</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The remainder of the PaaS options within Azure that are covered in the Azure Solutions Architect Expert exam are around Event Grid, Event Hub, IoT Hub, Service Bus, and Cognitive Services.  Many of these services are covered in deeper depth on other exams, but a mid-level understanding of how these services work and when you would use them is definitely important.  <a href="https://docs.microsoft.com/en-us/azure/architecture/microservices/" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/architecture/microservices/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>At a high level, these topics will be covered in my Cloud Lunch and Learn session on Friday, July 10, 2020. The recording will be located on the <a href="https://www.youtube.com/channel/UCHZeZzSlTtmfgPozIq8J2Kw" target="_blank" rel="noreferrer noopener">Cloud Lunch and Learn YouTube channel</a></p>
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