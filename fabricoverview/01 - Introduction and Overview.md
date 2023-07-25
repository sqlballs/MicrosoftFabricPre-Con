![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft workshop from the SQL Server team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>01 - Introduction and Overview</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution using the Microsoft Fabric platform.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/frabricoverview/00%20-%20Pre-Requisites.md" target="_blank">Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items mentioned there to be completed before you can proceed with the workshop.)

You'll cover these topics in this module:
<dl>

  <dt><a href="#1.1" target="_blank">1.1 - Introduction of the course</a><dt>
  <dt><a href="#1.2" target="_blank">1.2 - Basic Concepts in Microsoft Fabric</a><dt>
  <dt><a href="#1.3" target="_blank">1.3 - Microsoft Fabric Services</a><dt>
  <dt><a href="#1.4" target="_blank">1.4 - Microsoft Fabric Roles</a><dt>
  <dt><a href="#1.5" target="_blank">1.5 - Understanding Microsoft Fabric Benchmarks</a><dt>
  <dt><a href="#1.6" target="_blank">1.6 - Verification of pre-requisites for the Activities</a><dt>

</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.1 Introduction of the Course</h2>

Microsoft Fabric is an all-in-one analytics solution for enterprises that covers everything from data movement to data science, Real-Time Analytics, and business intelligence. It offers a comprehensive suite of services, including data lake, data engineering, data integration, data science, data warehouse, real-time analytics, and Power BI. It is built on a foundation of Software as a Service (SaaS), which simplifies, integrates, and secures the analytics needs of organizations. Microsoft Fabric is in preview and brings together new and existing components from Power BI, Azure Synapse, and Azure Data Factory into a single integrated environment. These components are then presented in various customized user experiences, such as Data Engineering, Data Factory, Data Science, Data Warehouse, Real-Time Analytics, and Power BI. Fabric also provides a unified data lake that allows users to retain, access, and share data across different experiences and clouds. Users can also create their own workspaces and lakehouses within OneLake, the data lake, and mount existing PaaS storage accounts into OneLake with the Shortcut feature. This way, users can enjoy a highly integrated, end-to-end, and easy-to-use product that is designed to turn large and complex data repositories into actionable workloads and analytics.

In this Course, you will TODO

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

![Fabric Diagram](https://learn.microsoft.com/en-us/fabric/get-started/media/microsoft-fabric-overview/saas-foundation.png)


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Review Exercise for this Course</b></p>

In this exercise, you will review the exercise we will use throughout the course. You will read over these steps only, in a future activity you will complete each step. 

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open the following reference in another tab](https://learn.microsoft.com/en-us/fabric/data-engineering/tutorial-lakehouse-introduction), and read over the steps you see there. We will refer back to this exercise throughout the course. 

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.3 - Microsoft Fabric Services</h2>

Microsoft Fabric is an end-to-end analytics solution with full-service capabilities including data movement, data lakes, data engineering, data integration, data science, real-time analytics, and business intelligence—all backed by a shared platform providing robust data security, governance, and compliance. It powers core Azure infrastructure as well as other Microsoft services such as Skype for Business, Intune, Azure Event Hubs, Azure Data Factory, Azure Cosmos DB, Azure SQL Database, Dynamics 365, and other services. It is an all-in-one analytics solution for enterprises that covers everything from data movement to data science. It offers a comprehensive suite of services including data lake, data engineering and data integration.

A graphical list of these services are shown here:

![](https://learn.microsoft.com/en-us/fabric/get-started/media/microsoft-fabric-overview/workloads-access-data.png)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.4 - Microsoft Fabric Roles</h2>

Microsoft Fabric has different admin roles such as Microsoft 365 admin roles, Power Platform and Power BI admin roles, and Capacity admin roles. 

Workspace roles define what user can do with Microsoft Fabric items. Roles can be assigned to individuals or security groups from workspace view. Workspace roles in Microsoft Fabric extend the Power BI workspace roles by associating new Microsoft Fabric capabilities such as data integration and data exploration with existing workspace roles. 

To be a Microsoft Fabric admin for your organization, you must be in one of the following roles: Global administrator, Power Platform administrator, Fabric administrator.

- [Administration Roles are described here](https://learn.microsoft.com/en-us/fabric/admin/microsoft-fabric-admin)
- [Learn more about Microsoft Fabric admin roles](https://learn.microsoft.com/en-us/fabric/admin/roles)
- [Roles in workspaces are described here](https://learn.microsoft.com/en-us/fabric/get-started/roles-workspaces)
- [Understand more about Workspace roles and permissions in lakehouse](https://learn.microsoft.com/en-us/fabric/data-engineering/workspace-roles-lakehouse)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.5"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.5 - Understanding Microsoft Fabric Benchmarks</h2>

Microsoft Fabric Capacity Metrics app is designed to provide monitoring capabilities for Power BI Premium capacities. Capacity metrics in Fabric is a governance feature for admins to monitor the performance of workloads and their usage compared to purchased capacity. 

The Azure security baseline for Service Fabric is also available. [You can learn more about the capacity metrics in Microsoft Fabric here.](https://blog.fabric.microsoft.com/en-us/blog/capacity-metrics-in-microsoft-fabric)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.6"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.6 - Verification of pre-requisites for the Activities</h2>

TODO

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/microsoft-fabric-overview " target="_blank">The primary page for documentation on Microsoft Fabric is here</a></li>
    <li><a href="https://learn.microsoft.com/en-us/training/paths/get-started-fabric/?WT.mc_id=DP-MVP-5004032">Microsoft Learn Pathway on Fabric</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-install">Installing the Fabric Metrics app</a></li>
</ul>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/02%20-%20Workspaces%2C%20User%20Security%2C%20Data%20Governance%2C%20and%20Data%20Integration.md).

