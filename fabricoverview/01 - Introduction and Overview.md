![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft workshop from the SQL Server team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>01 - Introduction and Overview</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution using the Microsoft Fabric platform.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/frabricoverview/00%20-%20Pre-Requisites.md" target="_blank">Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items mentioned there to be completed before you can proceed with the workshop.)

You'll cover these topics in this Module:
<dl>

  <dt><a href="#1.1" target="_blank">1.1 - Introduction of the course</a><dt>
  <dt><a href="#1.2" target="_blank">1.2 - Basic Concepts in Microsoft Fabric</a><dt>
  <dt><a href="#1.3" target="_blank">1.3 - 1.3 OneLake & Microsoft Fabric Architecture</a><dt>
  <dt><a href="#1.4" target="_blank">1.4 - Microsoft Fabric Services</a><dt>
  <dt><a href="#1.5" target="_blank">1.5 - Microsoft Fabric Roles</a><dt>
  <dt><a href="#1.6" target="_blank">1.6 - Understanding Microsoft Fabric Benchmarks</a><dt>
  <dt><a href="#1.7" target="_blank">1.7 - Verification of pre-requisites for the Activities</a><dt>

</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.1 Introduction of the Course</h2>

Imagine you have a lot of data from different sources and you want to use it to make better decisions for your business. You need a tool that can help you collect, store, process, analyze, and visualize your data in one place. You also want a tool that is easy to use, secure, and flexible. That’s what Microsoft Fabric is all about.

<p>

Microsoft Fabric is a new solution that lets you do everything with your data, from moving it to making sense of it. It has different services that you can use for different purposes.
<p>


Microsoft Fabric is based on cloud technology, which means you don’t have to worry about setting up or managing any infrastructure. It also integrates and secures your data across different experiences and clouds, so you can work with it seamlessly. Microsoft Fabric is currently in preview, which means it is still being developed and improved. It combines new and existing features from Power BI, Azure Synapse, and Azure Data Factory into one environment. You can use these features through different user interfaces, depending on what you want to do with your data.
<p>
One of the best things about Microsoft Fabric is OneLake, the OneDrive of the Data world. OneLake is not just a storage place for your data, but also a logical layer that organizes and governs your data. 
<p>
You can create your own workspaces and lakehouses within OneLake, which are like folders or projects for your data. You can also use the Shortcut feature to access data from other workspaces or tenants, or from other cloud services like Azure Storage. This way, you can have one copy of your data for consistent and reliable insights.
<p>
Microsoft Fabric is designed to help you turn your large and complex data into actionable workloads and analytics. It is a powerful and easy-to-use tool that can help you grow your business and achieve your goals.

In this Course, you will understand:
- the basic concepts, services, roles, and benchmarks of Microsoft Fabric
- how to create and manage workspaces, data warehouses, and data integration pipelines and data flows
- how to Secure and govern your data with distributed ownership and collaboration
- how to different analytical engines can be used to run T-SQL, Python, or KQL queries in order to load, transform, query, and visualize your data
- how to use various developer tools, such as Co-Pilot, SSMS, VS Code, and command-line tools, to develop and test your data applications
- how Microsoft Fabric integrates with DevOps

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.2 Basic Concepts in Microsoft Fabric</h2>

Organizations are faced with multiple challenges in bringing together all data from their environment for actionable intelligence. There are many data professionals involved across the organization working with various data sources, tools, and processes. Microsoft Fabric brings together all these experiences into a unified platform to offer the most comprehensive big data analytics platform in the industry. 

Microsoft Fabric enables organizations and individuals to turn large and complex data repositories into actionable workloads and analytics, and is an implementation of a *[data mesh](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/cloud-scale-analytics/architectures/what-is-data-mesh)* architecture. It provides various systems with associated tools and aspects to the data professionals in their day-to-day work:

- *Data Engineering* - Microsoft Fabric provides a Spark platform with a simplified but powerful authoring experiences, enabling data engineers to perform large scale data transformation and democratize data through the lakehouse. Microsoft Fabric Spark's integration with *Data Factory* enables notebooks and spark jobs to be scheduled and orchestrated. 

- *Data Pipelines* - *Fabric Data Factory* combines the simplicity of *Power Query* with the scale and power of [Azure Data Factory](https://learn.microsoft.com/en-us/azure/data-factory/introduction). You can use more than 200 native connectors to connect to data sources on-premises and in the cloud.

- *Data Science* - Various tools for Data Science in Mmicrosoft Fabric enables you to build, deploy, and operationalize machine learning models. It integrates with [Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/overview-what-is-azure-machine-learning?view=azureml-api-2) to provide built-in experiment creation, tracking and model registry. Data scientists can enrich organizational data with predictions and allow business analysts to integrate those predictions into their BI reports. Microsoft Fabric allows you to work from descriptive to predictive insights. 

- *Data Warehouse* - Microsoft Fabric provides a [Data Warehouse using SQL](https://learn.microsoft.com/en-us/azure/architecture/data-guide/relational-data/data-warehousing), with high performance and scale. It fully separates compute from storage, enabling independent scaling of both the components. Additionally, it natively stores data in the open Delta Lake format. 

- *Real-Time Analytics* - Observational data, which is collected from various sources such as apps, IoT devices, human interactions, and so many more. It's currently the fastest growing data category. This data is often semi-structured in formats like JSON or Text. It comes in at high volume, with shifting schemas. These characteristics make it hard for traditional data warehousing platforms to work with. [Azure Synapse](https://learn.microsoft.com/en-us/azure/architecture/solution-ideas/articles/real-time-analytics) is best in class engine for observational data analytics. 

- Power BI - [*Power BI*](https://powerbi.microsoft.com/en-us/getting-started-with-power-bi/) is the world's leading Business Intelligence platform. It ensures that business owners can access all the data in Fabric quickly and intuitively to make better decisions with data. 

- OneLake - [*OneLake*](https://learn.microsoft.com/en-us/fabric/onelake/onelake-overview)  is a single, unified, logical data lake for the whole organization. Like OneDrive, OneLake comes automatically with every Microsoft Fabric tenant and is designed to be the single place for all your analytics data. 

![Fabric Diagram](https://learn.microsoft.com/en-us/fabric/get-started/media/microsoft-fabric-overview/saas-foundation.png)


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Review Exercise for this Course</b></p>

In this exercise, you will review the exercise we will use throughout the course. You will read over these steps only, in a future activity you will complete each step. 

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open the following reference in another tab](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-introduction), and read over the steps you see there. We will refer back to this exercise throughout the course. 

<p>
On your own time or if there is time in the class here is a video that introduces you to Microsoft Fabric and shows the results of the tutorial we will be refering to in the class:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/TSTeoeCNh7c/0.jpg)](https://www.youtube.com/watch?v=TSTeoeCNh7c)
<p style="border-bottom: 1px solid lightgrey;"></p>



<h2 id="1.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.3 OneLake & Microsoft Fabric Architecture</h2>

![OneLake Diagram](https://learn.microsoft.com/en-us/fabric/onelake/media/onelake-overview/onelake-foundation-for-fabric.png)



Microsoft OneLake is a SaaS service that provides a single, unified, logical data lake for the entire organization. It is the foundation of Microsoft Fabric, a cloud-native data platform that enables customers to build and manage data solutions at scale. OneLake simplifies data storage, access, security, governance, and discovery by offering the following features:
<p>

- One data lake for the entire organization: OneLake comes automatically with every Microsoft Fabric tenant and is designed to be the single place for all your analytics data. You don’t need to set up or manage any infrastructure or resources to use OneLake.
- One copy of data for use with multiple analytical engines: OneLake stores all tabular data in delta parquet format, which is compatible with various analytical engines such as Spark, SQL, and Synapse. You can use different data items such as lakehouses, warehouses, and cubes to access and analyze the same data in OneLake without creating redundant copies.
- One security model living natively with the data in the lake (coming soon): OneLake will support a unified security model that lives with the data in the lake, enabling fine-grained access control and encryption at rest and in transit. You will be able to manage security policies at the tenant, workspace, or data item level.
- A centralized OneLake data hub for data discovery and management: OneLake provides a data hub where you can discover, browse, and manage all the data items in your tenant. You can also use the data hub to create new data items, import or export data, monitor usage and performance, and troubleshoot issues.

<p>

<p style="border-bottom: 1px solid lightgrey;"></p>





<h2 id="1.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.4 - Microsoft Fabric Services</h2>

Microsoft Fabric is an end-to-end analytics solution with full-service capabilities including data movement, data lakes, data engineering, data integration, data science, real-time analytics, and business intelligence—all backed by a shared platform providing robust data security, governance, and compliance. It powers core Azure infrastructure as well as other Microsoft services such as Skype for Business, Intune, Azure Event Hubs, Azure Data Factory, Azure Cosmos DB, Azure SQL Database, Dynamics 365, and other services. It is an all-in-one analytics solution for enterprises that covers everything from data movement to data science. It offers a comprehensive suite of services including data lake, data engineering and data integration.

A graphical list of these services are shown here:

![](https://learn.microsoft.com/en-us/fabric/get-started/media/microsoft-fabric-overview/workloads-access-data.png)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.5"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.5 - Microsoft Fabric Roles</h2>

Microsoft Fabric has different admin roles such as Microsoft 365 admin roles, Power Platform and Power BI admin roles, and Capacity admin roles. 

Workspace roles define what user can do with Microsoft Fabric items. Roles can be assigned to individuals or security groups from workspace view. Workspace roles in Microsoft Fabric extend the Power BI workspace roles by associating new Microsoft Fabric capabilities such as data integration and data exploration with existing workspace roles. 

To be a Microsoft Fabric admin for your organization, you must be in one of the following roles: Global administrator, Power Platform administrator, Fabric administrator.

- [Administration Roles are described here](https://learn.microsoft.com/en-us/fabric/admin/microsoft-fabric-admin)
- [Learn more about Microsoft Fabric admin roles](https://learn.microsoft.com/en-us/fabric/admin/roles)
- [Roles in workspaces are described here](https://learn.microsoft.com/en-us/fabric/get-started/roles-workspaces)
- [Understand more about Workspace roles and permissions in lakehouse](https://learn.microsoft.com/en-us/fabric/data-engineering/workspace-roles-lakehouse)

<p>
Data sharing is essential to fostering a data-driven culture within an organization. Sharing a Warehouse allows you to provide read access to enable downstream users within the organization to consume this data to make data-driven decisions, without having to make copies of data.
<p>
An Admin or Member within a workspace can share a Warehouse with another recipient (AAD user or AAD groups) within your organization. You can also grant these permissions using the “Manage permissions” experience.
<p>
To understand more about Data Sharing see these links:

- [Data Warehouse sharing](https://learn.microsoft.com/en-us/fabric/admin/microsoft-fabric-admin)
- [Share your warehouse and manage permissions](https://learn.microsoft.com/en-us/fabric/data-warehouse/share-warehouse-manage-permissions)
<p>
For a brief video overview of Data Sharing see this video:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/Z4_yY8axMsc/0.jpg)](https://www.youtube.com/watch?v=Z4_yY8axMsc)
<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.6"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.6 - Understanding Microsoft Fabric Benchmarks</h2>

![](https://dataplatformblogcdn.azureedge.net/wp-content/uploads/2023/06/image_mihir-1024x661.gif)


Microsoft Fabric Capacity Metrics app is designed to provide monitoring capabilities for Power BI Premium capacities. Capacity metrics in Fabric is a governance feature for admins to monitor the performance of workloads and their usage compared to purchased capacity. 

The Azure security baseline for Service Fabric is also available. 
<p>
For more information about the Microsoft Fabric Capacity app see the following documentation:

-  [Capacity metrics in Microsoft Fabric Announcement](https://blog.fabric.microsoft.com/en-us/blog/capacity-metrics-in-microsoft-fabric)

-  [What is the utilization and metrics app?](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app)
-  [Install the Microsoft Fabric capacity metrics app](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-install?tabs=1st)
-  [Understand the metrics app overview page](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-overview-page)
-  [Understand the metrics app timepoint page](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-timepoint-page)
<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.7"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.7 - Verification of pre-requisites for the Activities</h2>

In order to complete any exercises required in this class you should have followed the [Pre-Requisites](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md) outlined in the Read.me file. 

Validate that you have a Microsoft Fabric Enabled Workspace:
- Navigate to [Power BI.com](https://www.powerbi.com)
- Click on Workspaces
- Navigate to your Microsoft Fabric enabled workspace
- Click +New
- Click Show all
- Ask an Instructor to validate that you have a Microsoft Fabric Enabled Workspace

<p>
If have a Power BI License, a Microsoft Fabric Capacity, but have not created a workspace:

- Navigate to [Lakehouse tutorial: Create a Fabric workspace](https://learn.microsoft.com/en-us/fabric/data-engineering/tutorial-lakehouse-get-started)
- Navigate to your Microsoft Fabric enabled workspace
- Click +New
- Click Show all
- Ask an Instructor to validate that you have a Microsoft Fabric Enabled Workspace

<p>

If you cannot complete these steps open and follow the  [Pre-Requisites](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md).
<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://learn.microsoft.com/en-us/fabric/onelake/onelake-overview">OneLake, the OneDrive for data</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/microsoft-fabric-overview " target="_blank">The primary page for documentation on Microsoft Fabric is here</a></li>
    <li><a href="https://learn.microsoft.com/en-us/training/paths/get-started-fabric/?WT.mc_id=DP-MVP-5004032">Microsoft Learn Pathway on Fabric</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-install">Installing the Fabric Metrics app</a></li>
  <li><a href="https://erwindekreuk.com/microsoft-fabric-content-hub/">Microsoft Fabric Content Hub from Erwin de Kreuk</a></li>

</ul>


Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/02%20-%20Workspaces%2C%20User%20Security%2C%20Data%20Governance%2C%20and%20Data%20Integration.md).

