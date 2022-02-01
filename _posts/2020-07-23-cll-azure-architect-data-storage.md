---
layout: post
title: So You want to be an Azure Solutions Architect Expert…the blog series...Data and Storage

---

<!-- wp:image {"align":"center","id":689,"sizeSlug":"large"} -->
<div class="wp-block-image"><figure class="aligncenter size-large"><img src="https://captainhyperscaler.files.wordpress.com/2020/06/cll-azure-solution-architect-poster.jpg?w=1024" alt="" class="wp-image-689"/></figure></div>
<!-- /wp:image -->

<!-- wp:paragraph -->
<p>Welcome to this installment of the "So You want to be an Azure Solutions Architect Expert" series. This is the fifth accompanying article, and it will focus on some key objectives that are part of the AZ-303 and AZ-304 exams.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>To attend the session on Friday, July 24, 2020, please access the link for the <a rel="noreferrer noopener" href="https://www.cloudlunchlearn.com/" target="_blank">Cloud Lunch and Learn website</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>These sessions are also being recorded and posted on the <a rel="noreferrer noopener" href="https://www.youtube.com/channel/UCHZeZzSlTtmfgPozIq8J2Kw" target="_blank">Cloud Lunch and Learn YouTube channel</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>In this session and article, I will be focusing on Data and Storage in Azure. There are three fundamental components that make up the cloud infrastructure (or any infrastructure) and they are compute, networking, and storage.  The previous sessions have covered compute (both IaaS and PaaS), and networking (included in the security session).  This article and session will focus on the Storage services and the various ways store and access your data.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The key topics that I will be covering are potentially heavily tested topics within the exams, so the goal is that this information will provide you with a strong foundation of information that you can build upon as you prepare for the exams.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>The topics that I will discuss on Friday include the following:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Data evolution and types of data</strong>: Before you begin to create resources with Azure, or any network infrastructure, it is important to understand how data is going to be stored and utilized.  As more and more devices become connected, the amount of data that is created grows exponentially. The concept of <a rel="noreferrer noopener" href="https://en.wikipedia.org/wiki/Moore%27s_law" target="_blank">Moore's law</a> has been accelerated and organizations are finding ways to utilize cloud services for expanding their compute capabilities to process the larges amounts of data.  If you are a Data Engineer or DBA, this is becoming a highly sought after role in the industry and I recommend looking into the Data Engineer Associate certification path, which takes a much deeper look at the use of data.  From the Azure Solutions Architect Expert scope, you will need to understand the types of data, and the various storage options and uses within Azure.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Storage types</strong>: Understanding the different storage types and where you would store this data in Azure services is important to understand.  Storage can be placed in three categories: structured, unstructured, and semi-structured.  When talking about structured and semi-structured data, we are usually storing this data within a SQL (structured) or no-SQL (CosmosDB) database.  Unstructured data are in the object storage category that utilizes Blob storage.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Azure Storage</strong>: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/?product=storage" target="_blank">https://docs.microsoft.com/en-us/azure/?product=storage</a> The foundation of storage within Azure is the Azure Storage account.  Within a General Purpose v2 (Azure default recommended option) storage account, there are four types of storage: Containers (Blobs), File Shares, Tables, and Queues.  As you prepare for the Solutions Architect exams, it is important to understand the uses of each of these, with a particular emphasis on Blobs and Files. <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/storage/common/storage-introduction?toc=%2fazure%2fstorage%2fblobs%2ftoc.json" target="_blank">https://docs.microsoft.com/en-us/azure/storage/common/storage-introduction?toc=%2fazure%2fstorage%2fblobs%2ftoc.json</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>We will also discuss during the session how to enable and use Replication, Soft-delete, and Data Lifecycle Management to protect from data loss and adhere to retention requirements.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Relational and Non-Relational Databases</strong>: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/?product=databases" target="_blank">https://docs.microsoft.com/en-us/azure/?product=databases</a> In the PaaS session on July 10, 2020, we discussed two of the key database services that should be a focus of your preparation, SQL database and Cosmos DB. A tip here would be to understand the different options for deploying a SQL database within Azure.  Each of these options can be found at the link provided above and here: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/azure-sql/" target="_blank">https://docs.microsoft.com/en-us/azure/azure-sql/</a>.  There are also scenarios where Cosmos DB can be utilized with a SQL API to provide a global database distribution, and this is key.  Know the different APIs and consistency levels that can be used with Cosmos DB. <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/cosmos-db/" target="_blank">https://docs.microsoft.com/en-us/azure/cosmos-db/</a>.  As you move to the AZ-301/304 exam, you will want to understand how and when to use Azur Database Migration service as well.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Big Data Options</strong>: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/?product=analytics" target="_blank">https://docs.microsoft.com/en-us/azure/?product=analytics</a>  There are many other options within Azure services for the ingestion and transformation of large datasets.  Understanding these at a high level, and how and where these may be used can help you on the exam.  The exams do not go deep into these but you may find some questions on some of these services, particularly Data Lake or SQL Data Warehouse (Azure Synapse Analytics).  I have provided links to the documentation for these big data services below:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Data Lake Storage: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction" target="_blank">https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-introduction</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Synapse Analytics (formerly SQL Data Warehouse): <a href="https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Databricks: <a href="https://docs.microsoft.com/en-us/azure/databricks/" target="_blank" rel="noreferrer noopener">https://docs.microsoft.com/en-us/azure/databricks/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>Choosing a Data storage option</strong>: Once you are comfortable with the various data storage options within Azure, you need to choose the best option for the environment and workloads that you are deploying.  What are the characteristics and key features that you are requiring? How are you going to be ingesting the data, how are you using it, and how are you querying the data?  Finally, what are you doing to secure your data? </p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Asking these questions will guide you on the path to choosing the proper storage option and service within Azure.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>At a high level, these topics will be covered in my Cloud Lunch and Learn session on Friday, July 24, 2020. The recording will be located on the <a rel="noreferrer noopener" href="https://www.youtube.com/channel/UCHZeZzSlTtmfgPozIq8J2Kw" target="_blank">Cloud Lunch and Learn YouTube channel</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Additional links to assist in initial preparation include:</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Cloud Lunch and Learn <a rel="noreferrer noopener" href="https://github.com/Cloud-Lunch-and-Learn/Cloud-Lunch-and-Learn-Sessions" target="_blank">github</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Build5Nines self-assessment tools: <a rel="noreferrer noopener" href="https://build5nines.com/free-oss-exam-self-assessment-tool/" target="_blank">https://build5nines.com/free-oss-exam-self-assessment-tool/</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Microsoft Learn: <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/learn/certifications/exams/az-300?wt.mc_id=learningredirect_certs-web-wwl" target="_blank">AZ-300</a> and <a rel="noreferrer noopener" href="https://docs.microsoft.com/en-us/learn/certifications/exams/az-301?wt.mc_id=learningredirect_certs-web-wwl" target="_blank">AZ-301</a> on-demand training</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Azure Greg posts Microsoft Docs links for every exam objective here: <a rel="noreferrer noopener" href="https://github.com/gsuttie/AzureResources/tree/master/Exams" target="_blank">Gregor Suttie github</a></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Pixel Robots is a helpful source of information, especially for AKS: <a rel="noreferrer noopener" href="https://pixelrobots.co.uk/" target="_blank">https://pixelrobots.co.uk/</a></p>
<!-- /wp:paragraph -->