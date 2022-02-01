---
layout: post
title: Demystifying Cloud Platform Services

---


<!-- wp:image {"align":"center","id":233,"width":579,"height":190,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large is-resized"><img src="https://captainhyperscaler.files.wordpress.com/2020/01/img_0852.jpg?w=462" alt="" class="wp-image-233" width="579" height="190"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p><strong><em>Kubernetes, Containers, WebApps, App Services, Docker, DevOps, CI/CD, NoSQL, Cognitive Services, Bot Services, Micro-Services, Serverless computing, etc</em></strong>.  The list goes on and on and on when it comes to the number of platform-based services that are available in Azure and other public cloud providers.  In this article, I am going to attempt to provide everyone a base understanding of what some of this means within the IT ecosystem, and when you have completed this article, have a better understanding of how to potentially utilize these services.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Author's Note</strong>:  this is not a technical "how to" article.  I will provide some links at the end of where you can find more information for some of these services. What you should walk away from with this article is a foundational understanding of an approach to platform services, potential workloads that are suited for these services, and some of the security and cost considerations.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Defining Platform Services</strong>.  Let's set the table on what is being referenced in terms of platform services.  By definition, a platform service is when the cloud provider is providing and managing all aspects of the virtual infrastructure.  This includes all of the operating systems and patching of the environment, and the hardware (see diagram below).  From a developer's perspective, this is extremely helpful because all they have to be concerned with is the application code, data, and APIs, to simplify.  For this article's context, think about container services and app services being the primary reference.</p>
<!-- /wp:paragraph -->

<!-- wp:image {"align":"center","id":242,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2020/01/xaas.png?w=553" alt="" class="wp-image-242"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p> <strong>Break it down</strong>.  As Dilbert points out in the comic, just because containers, kubernetes, and AI are techy words that we hear and see daily in articles, key note speeches, and commercials, doesn't mean that it is going to solve your problems.  There may be an opportunity within your environment to re-architect or "transform" your applications to utilize these services, but that is not a process that happens with a flick of a switch.  Not all applications can be re-written to be cloud native.  In addition, there may be other applications or databases within the environment that are inter-dependent on that application.  Therefore, it is extremely important to have a sound understanding of how your applications and workloads behave prior to making significant changes to your environment.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Not all applications fit into platform services</strong>.  There has been a continued push to move applications to the various platform services.  Organizations believe that being able to do this will decrease management overhead and lower infrastructure costs.  This is true when an application is already in a "cloud native" format, that is, it runs as code.  The best example that I can provide for readers that do not typically develop applications would be a website.  The back end of a website is all code for commands that present the website and images for that website.  The website code does not rely on a packaged .exe file to run on the server and, therefore, administrative access to an operating system is not going to be required to execute and run the application.  </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>An opposing example may be an off-the-shelf accounting software the runs on Windows.  In order to make this software "cloud native" where it no longer relies on the Windows Operating System, it would need to be taken apart and re-written to run in a native code.  Many applications over the years have been made to run in this manner when you think of web browser-based versions of Microsoft Office suite, Outlook, Google Apps, and many others.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Consumption is key and a potential concern</strong>. Know the triggers. Most platform services have both a consumption-based or performance-based subscription. Using consumption-based is the best way to start and many platform services have a free tier, which is great for development and testing. However, production applications and databases would rarely fit into the free tiers. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Whether you determine and choose consumption or performance subscriptions, understanding the costs are important. For consumption-based subscriptions, there is flexibility for dynamic platforms. Your workloads will scale in and out as needed, within the limits and levels of that subscription. When traffic is low, costs will be lower and vise versa. For workloads that have more predictable traffic levels, a performance-based subscription should be the best route to take. You can select the level of performance and have a more predictable monthly cost. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Whichever option you choose, cost and performance control is important. The cost triggers of traffic, compute, and storage are just as important to monitor in platform services as they are within an infrastructure service. Understanding where these costs are incurred are the key to proper budgeting. Examples of these fee structures can be found here: <a rel="noreferrer noopener" aria-label="https://docs.microsoft.com/en-us/azure/app-service/overview-hosting-plans (opens in a new tab)" href="https://docs.microsoft.com/en-us/azure/app-service/overview-hosting-plans" target="_blank">https://docs.microsoft.com/en-us/azure/app-service/overview-hosting-plans</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Security</strong>. APIs, not patches become one of the primary security concerns for platform services. Now that the cloud provider is responsible for the operating system and middleware, the provider will now execute any host and operating system security patches. Proper testing of security for network port connections and APIs on applications during all stages of development, staging, and production will help to decrease the likelihood of a breach in your organization.  Azure and cloud providers have best practice policies that provide a good foundation to build upon. There is, however, a burden on developers to determine and test security of applications to organizational standards and regulatory requirements prior to deploying to production. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Take advantage of DevOps tools</strong>. Cloud native tools such as Azure DevOps and Azure App Services allow the ability to test, stage, and deploy workflows for your applications in a continuous integration/continuous deployment (CI/CD) manner. As stated in the previous section, this helps to verify how an application will act upon deployment. A formal CI/CD process creates a standardized workflow for validation, approvals, and staging applications throughout development. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>As you can see, there are numerous considerations when taking the step from just a cloud migration to a cloud transformation.  It requires a developer's skillset to move down this path, and, in most cases, requires assistance from the application owner to be successful.  If you are looking to take advantage of platform-based services on a short-term basis, my recommendation is to first look at whether you are hosting your corporate websites in a private infrastructure.  The fact that these are public facing and require scalable, elastic infrastructure make them a perfect candidate to run as a cloud native service.  A great example article around running and deploying a web page can be found in the Azure Advent Calendar wrap up from Microsoft MVP Gregor Suttie (@gregor_suttie): <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://gregorsuttie.com/2020/01/03/azure-advent-calendar-wrap-up/" target="_blank">https://gregorsuttie.com/2020/01/03/azure-advent-calendar-wrap-up/</a>.  As mentioned at the beginning of this article, I am providing some links to various platform services below for you to reference in your cloud transformation journey and education.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Additional Links to docs and blogs that you may found helpful are below. </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>HPE and Docker Containers for Dummies: <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://www.qcmtech.com/wp-content/uploads/2017/09/HPE-pub-10010-Containers-for-Dummies.pdf" target="_blank">https://www.qcmtech.com/wp-content/uploads/2017/09/HPE-pub-10010-Containers-for-Dummies.pdf</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Skylines Academy: <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://www.skylinesacademy.com/" target="_blank">https://www.skylinesacademy.com/</a>.  Courses and blogs for training, including Terraform and HashiCorp development tools.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Web Apps: <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://azure.microsoft.com/en-us/services/app-service/web/" target="_blank">https://azure.microsoft.com/en-us/services/app-service/web/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Kubernetes: <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://azure.microsoft.com/en-us/services/kubernetes-service/" target="_blank">https://azure.microsoft.com/en-us/services/kubernetes-service/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Container Services: <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://azure.microsoft.com/en-us/product-categories/containers/" target="_blank">https://azure.microsoft.com/en-us/product-categories/containers/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure DevOps: <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://azure.microsoft.com/en-us/product-categories/devops/" target="_blank">https://azure.microsoft.com/en-us/product-categories/devops/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure AI and Machine Learning: <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://azure.microsoft.com/en-us/overview/ai-platform/" target="_blank">https://azure.microsoft.com/en-us/overview/ai-platform/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><a rel="noreferrer noopener" aria-label="Red Gate Introduction to DevOps (opens in a new tab)" href="https://www.red-gate.com/simple-talk/sysadmin/devops/introduction-to-devops-the-evolving-world-of-application-delivery/amp/" target="_blank">Red Gate Introduction to DevOps</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>#AzureFriday AKS video with @DonovanBrown <a rel="noreferrer noopener" aria-label="https://youtu.be/E9YWmbUb9Ps (opens in a new tab)" href="https://youtu.be/E9YWmbUb9Ps" target="_blank">https://youtu.be/E9YWmbUb9Ps</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Secure DevOps kit for Azure <a href="https://azure.microsoft.com/en-us/resources/videos/azure-friday-getting-started-with-the-secure-devops-kit-for-azure-azsk/" target="_blank" rel="noreferrer noopener" aria-label="https://azure.microsoft.com/en-us/resources/videos/azure-friday-getting-started-with-the-secure-devops-kit-for-azure-azsk/ (opens in a new tab)">https://azure.microsoft.com/en-us/resources/videos/azure-friday-getting-started-with-the-secure-devops-kit-for-azure-azsk/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Many Azure blogs contain other information and tips for developing applications in the cloud. Here is a ranked list that is helpful: <a rel="noreferrer noopener" aria-label=" (opens in a new tab)" href="https://blog.feedspot.com/microsoft_azure_blogs/" target="_blank">https://blog.feedspot.com/microsoft_azure_blogs/</a>.  The ranked list include some great contributors to the community, including @gregor_suttie, @skylinesacademy, and @pixel_robots, among many others that I follow.</p>
<!-- /wp:paragraph -->