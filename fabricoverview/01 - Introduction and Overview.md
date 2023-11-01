![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Course from Azure Data and the Fasttrack Team</i>


<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>01 - Introduction and Overview</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution using the Microsoft Fabric platform.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" target="_blank">Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items mentioned there to be completed before you can proceed with the workshop.)

You'll cover these topics in this Module:
<dl>

  <dt><a href="#11-introduction-of-the-course" target="_blank">1.1 - Introduction of the course</a><dt>
  <dt><a href="#12-basic-concepts-in-microsoft-fabric" target="_blank">1.2 - Basic Concepts in Microsoft Fabric</a><dt>
  <dt><a href="#13-onelake--microsoft-fabric-architecture" target="_blank">1.3 - 1.3 OneLake & Microsoft Fabric Architecture</a><dt>
  <dt><a href="#14---microsoft-fabric-services" target="_blank">1.4 - Microsoft Fabric Services</a><dt>
  <dt><a href="#15---microsoft-fabric-roles" target="_blank">1.5 - Microsoft Fabric Roles</a><dt>
  <dt><a href="#16---understanding-microsoft-fabric-benchmarks" target="_blank">1.6 - Understanding Microsoft Fabric Benchmarks</a><dt>
  <dt><a href="#17---verification-of-pre-requisites-for-the-activities" target="_blank">1.7 - Verification of pre-requisites for the Activities</a><dt>

</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1-1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.1 Introduction of the Course</h2>

Data is a valuable asset for many organizations that want to make better business decisions. Microsoft Fabric is a Service that enables data collection, storage, processing, analysis, and visualization in one place. It offers a secure, flexible, and user-friendly solution for data management and transformation. Microsoft Fabric is a new solution that allows doing everything with data, from ingesting it to deriving insights from it. It provides different services for different purposes.

Microsoft Fabric leverages cloud technology, which eliminates the need for setting up or managing any infrastructure. It also integrates and secures data across different experiences and clouds, enabling seamless data workflows. Microsoft Fabric is currently in preview, which means it is under development and improvement. It combines new and existing features from Power BI, Azure Synapse, and Azure Data Factory into one environment. These features can be accessed through different user interfaces, depending on the data task.

Microsoft Fabric introduces OneLake, the OneDrive of the Data world. OneLake is not only a storage place for data, but also a logical layer that organizes and governs data.

OneLake allows creating workspaces and lakehouses, which are similar to folders or projects for data. It also offers the Shortcut feature to access data from other workspaces or tenants, or from other cloud services like Azure Storage. This way, it ensures one copy of data for consistent and reliable insights.

Microsoft Fabric is designed to help turn large and complex data into actionable workloads and analytics. It is a powerful and easy-to-use tool that can help achieve business goals and growth.

In this Course, you will understand:
- The <b>basic</b> concepts, services, roles, and benchmarks of Microsoft Fabric
- <b>How to create and manage</b> workspaces, data warehouses, and data integration pipelines and data flows
- <b>How to Secure and govern</b> your data with distributed ownership and collaboration
- <b>How to different analytical engines</b> can be used to run T-SQL, Python, or KQL queries in order to load, transform, query, and visualize your data
- <b>How to use various developer tools</b>, such as Co-Pilot, SSMS, VS Code, and command-line tools, to develop and test your data applications
- <b>How</b> Microsoft Fabric integrates with DevOps

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.2 Basic Concepts in Microsoft Fabric</h2>

Actionable intelligence requires data integration from diverse sources and environments. This involves various data professionals across the organization using different data sources, tools, and processes. Microsoft Fabric unifies these experiences into a single platform that provides the industry’s most comprehensive big data analytics solution.

Microsoft Fabric enables organizations and individuals to turn large and complex data repositories into actionable workloads and analytics, and is an implementation of a *[data mesh](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/cloud-scale-analytics/architectures/what-is-data-mesh)* architecture. It provides various systems with associated tools and aspects to the data professionals in their day-to-day work:

- *Data Engineering* - Microsoft Fabric provides a Spark platform with a simplified but powerful authoring experiences, enabling data engineers to perform large scale data transformation and democratize data through the lakehouse. Microsoft Fabric Spark's integration with *Data Factory* enables notebooks and spark jobs to be scheduled and orchestrated. 

- *Data Pipelines* - *Fabric Data Factory* combines the simplicity of *Power Query* with the scale and power of [Azure Data Factory](https://learn.microsoft.com/en-us/azure/data-factory/introduction). You can use more than 200 native connectors to connect to data sources on-premises and in the cloud.

- *Data Science* - Various tools for Data Science in Microsoft Fabric enables you to build, deploy, and operationalize machine learning models. It integrates with [Azure Machine Learning](https://learn.microsoft.com/en-us/azure/machine-learning/overview-what-is-azure-machine-learning?view=azureml-api-2) to provide built-in experiment creation, tracking and model registry. Data scientists can enrich organizational data with predictions and allow business analysts to integrate those predictions into their BI reports. Microsoft Fabric allows you to work from descriptive to predictive insights. 

- *Data Warehouse* - Microsoft Fabric provides a [Data Warehouse using SQL](https://learn.microsoft.com/en-us/azure/architecture/data-guide/relational-data/data-warehousing), with high performance and scale. It fully separates compute from storage, enabling independent scaling of both the components. Additionally, it natively stores data in the open Delta Lake format. 

- *Real-Time Analytics* - Observational data, which is collected from various sources such as apps, IoT devices, human interactions, and so many more. It's currently the fastest growing data category. This data is often semi-structured in formats like JSON or Text. It comes in at high volume, with shifting schemas. These characteristics make it hard for traditional data warehousing platforms to work with. [Azure Synapse](https://learn.microsoft.com/en-us/azure/architecture/solution-ideas/articles/real-time-analytics) is best in class engine for observational data analytics. 

- Power BI - [*Power BI*](https://powerbi.microsoft.com/en-us/getting-started-with-power-bi/) is the world's leading Business Intelligence platform. It ensures that business owners can access all the data in Fabric quickly and intuitively to make better decisions with data. 

- OneLake - [*OneLake*](https://learn.microsoft.com/en-us/fabric/onelake/onelake-overview)  is a single, unified, logical data lake for the whole organization. Like OneDrive, OneLake comes automatically with every Microsoft Fabric tenant and is designed to be the single place for all your analytics data. 

<p><img src="https://learn.microsoft.com/en-us/fabric/get-started/media/microsoft-fabric-overview/saas-foundation.png" height = 400>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Review Exercise for this Course</b></p>

In this exercise, you will review the exercise we will use throughout the course. You will read over these steps only, in a future activity you will complete each step. 

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open the following reference in another tab](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-introduction), and read over the steps you see there. This is an example of the different tutorials that you will experience in this class. 

You can also right-click this link to open it in another tab and review this video that introduces you to Microsoft Fabric and shows the results of the tutorial you will use in the Workshop:

<p><a href="https://www.youtube.com/watch?v=TSTeoeCNh7c"><img src="https://img.youtube.com/vi/TSTeoeCNh7c/0.jpg" height = 300></a> 

<h3>Microsoft OneLake</h3>

Microsoft OneLake is a SaaS service that provides a single, unified, logical data lake for the entire organization. 

<p><img src="https://learn.microsoft.com/en-us/fabric/onelake/media/onelake-overview/onelake-foundation-for-fabric.png" height = 400>

OneLake is the foundation of Microsoft Fabric, a cloud-native data platform that enables customers to build and manage data solutions at scale. OneLake simplifies data storage, access, security, governance, and discovery by offering the following features:
<p>

- One data lake for the entire organization: OneLake comes automatically with every Microsoft Fabric tenant and is designed to be the single place for all your analytics data. You don’t need to set up or manage any infrastructure or resources to use OneLake.
- One copy of data for use with multiple analytical engines: OneLake stores all tabular data in delta parquet format, which is compatible with various analytical engines such as Spark, SQL, and Synapse. You can use different data items such as lakehouses, warehouses, and cubes to access and analyze the same data in OneLake without creating redundant copies.
- One security model living natively with the data in the lake (coming soon): OneLake will support a unified security model that lives with the data in the lake, enabling fine-grained access control and encryption at rest and in transit. You will be able to manage security policies at the tenant, workspace, or data item level.
- A centralized OneLake data hub for data discovery and management: OneLake provides a data hub where you can discover, browse, and manage all the data items in your tenant. You can also use the data hub to create new data items, import or export data, monitor usage and performance, and troubleshoot issues.

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.4 - Microsoft Fabric Services</h2>

Microsoft Fabric is an end-to-end analytics solution with full-service capabilities including data movement, data lakes, data engineering, data integration, data science, real-time analytics, and business intelligence—all backed by a shared platform providing robust data security, governance, and compliance. It powers core Azure infrastructure as well as other Microsoft services such as Skype for Business, Intune, Azure Event Hubs, Azure Data Factory, Azure Cosmos DB, Azure SQL Database, Dynamics 365, and other services. It is an all-in-one analytics solution for enterprises that covers everything from data movement to data science. It offers a comprehensive suite of services including data lake, data engineering and data integration.

A graphical list of these services are shown in this diagram:

<p><img src="https://learn.microsoft.com/en-us/fabric/get-started/media/microsoft-fabric-overview/workloads-access-data.png" height = 400>

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

You can also right-click this link to open it in another tab and review this video that introduces you to these concepts:

<p><a href="https://www.youtube.com/watch?v=Z4_yY8axMsc"><img src="https://img.youtube.com/vi/Z4_yY8axMsc/0.jpg" height = 300></a> 

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.6"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.6 - Understanding Microsoft Fabric Benchmarks</h2>

There are several basic concepts in setting up the benchmarks for your Microsoft Fabric deployments.

## What are Capacities?
Microsoft Fabric is a unified data platform that offers shared experiences, architecture, governance, compliance, and billing. Capacities provide the computing power that drives all of these experiences. They offer a simple and unified way to scale resources to meet customer demand and can be easily increased with a SKU upgrade.

<p><img src="https://dataplatformblogcdn.azureedge.net/wp-content/uploads/2023/09/Fabric-Utilization-DW-static-caption-1024x575.png" height = 400>

<p>

### Bursting & Smoothing

Bursting allows you to consume extra compute resources beyond what have been purchased to speed the execution of a workload. For example, instead of running a job on 64 CU and completing in 60 seconds, bursting could use 256 CUs to complete the job in 15 seconds.

- Bursting is a SaaS feature and requires no user management. Behind the scenes, the capacity platform is pre-provisioning Microsoft managed virtualized compute resources to optimize for maximum performance.
- Compute spikes generated from bursting will not cause throttling due to smoothing policies outlined in the next section.

<p><img src="https://dataplatformblogcdn.azureedge.net/wp-content/uploads/2023/09/FabricBurstingSmoothing5.gif" height = 400>

<p>

When a capacity is running multiple jobs, a sudden spike in compute demand may be generated that exceeds the limits of a purchased capacity. Smoothing simplifies capacity management here by spreading the evaluation of compute to ensure that your jobs run smoothly and efficiently. Two places to expect to see this in place is:

<p>

- <b>For interactive jobs run by users:</b> capacity demand is typically smoothed over 5 minutes to reduce short-term temporal spikes.  
- <B>For scheduled, or background jobs:</b> capacity demand is spread over 24 hours, eliminating the concern of job scheduling or contention.

<p>
Smoothing will not impact execution time, that is always at peak performance! Smoothing simply also allows you to size your capacity based on average, not peak usage.

### OneLake Storage Reporting in Capacity Metrics

With this new feature, you can easily analyze your storage consumption by selecting your Capacity, choosing the date range, and viewing usage by workspace. This will provide you with valuable insights into your overall storage spend and enable you to monitor daily or hourly trends with usage of drill-through. 

<p><img src="https://dataplatformblogcdn.azureedge.net/wp-content/uploads/2023/09/onelake-demo-ux.png" height = 400>

<p>

### Capacity Long Running Workloads


Fabric contains a new optimization for long-running jobs. Historically, if a job’s reported usage exceeded capacity limits, the following jobs would be throttled. Now, if a job’s reported usage exceeds capacity limits, throttling will not be immediately applied to following jobs. Instead, any overage will be automatically balanced against future capacity when the system has unutilized capacity. This feature to “borrow from the future” is in addition to smoothing and is also seamless to customers and supported by the following new analytics experience in Capacity Metrics.
<p>

<p><img src="https://dataplatformblogcdn.azureedge.net/wp-content/uploads/2023/09/Throttling-cumulative-burndown.png" height = 400>

After the October 1st platform update, capacity throttling policies will now be based on the amount of future capacity consumption that resulted from smoothing policies, this offers increased Overage protection for when future use is less than 10 minutes and richer queue management features to prevent excessive overload when usage exceeds an hour. The 4 new policies are outlined in Table 1

<p>

<table style="height: 327px" width="1110">
<tbody>
<tr>
<td><strong>Future Smoothed Consumption – Policy Limits</strong></td>
<td>
<p><strong>Platform Policy</strong></p>
</td>
<td>
<p><strong>Experience Impact</strong></p>
</td>
</tr>
<tr>
<td>Usage &lt;= 10 minutes</td>
<td>
<p>Overage protection</p>
</td>
<td>
<p>Jobs can consume 10 minutes of future capacity use without throttling.</p>
</td>
</tr>
<tr>
<td>
<p>10 minutes &lt; Usage &lt;= 60 minutes</p>
</td>
<td>
<p>Interactive Delay</p>
</td>
<td>
<p>User requested interactive type jobs will be throttled.</p>
</td>
</tr>
<tr>
<td>
<p>60 minutes &lt; Usage &lt;= 24 hours</p>
</td>
<td>
<p>Interactive Rejection</p>
</td>
<td>
<p>User requested interactive type jobs will be rejected.</p>
</td>
</tr>
<tr>
<td>
<p>Usage &gt; 24 hours</p>
</td>
<td>
<p>Background Rejection</p>
</td>
<td>
<p>User Scheduled background jobs will be rejected from execution.</p>
</td>
</tr>
</tbody>
</table>
<p>
To help you monitor and analyze the new policies, Microsoft Fabric has added a new throttling tab in the utilization section of the Capacity Metrics. You can now easily observe future usage as a percentage of each limit, and even drill down to specific workloads that contributed to an overage.

<p><img src="https://dataplatformblogcdn.azureedge.net/wp-content/uploads/2023/09/Throttling-policy-analaytics.png" height = 400>

### Power BI & Microsoft Fabric - One Capacity Model
Capacity Units offer more granularity than the previously used v-cores and let us offer smaller sized capacities to Fabric customers with a very low entry point for pricing. Starting on 10/1, we will be updating all Power BI premium SKU’s (EM, P and A) to report in capacity units. Key takeaways for this change:
<p>

- This update will not result in any change to the throughput of a capacity.
- Power BI Premium SKU’s EM / A and P will now report usage using CUs.
- There will be one version of the Capacity Metrics app that supports all Power BI and Fabric capacity SKUs

<p><img src="https://dataplatformblogcdn.azureedge.net/wp-content/uploads/2023/09/a-screenshot-of-a-test-description-automatically.png" height = 400>

<p>
For more information about the Microsoft Fabric Capacity app see the following documentation:

-  [Capacity metrics in Microsoft Fabric Announcement](https://blog.fabric.microsoft.com/en-us/blog/capacity-metrics-in-microsoft-fabric)
-  [Understand the metrics app OneLake page](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-onelake-page)
-  [Fabric Capacities – Everything you need to know about what’s new and what’s coming](https://blog.fabric.microsoft.com/en-us/blog/fabric-capacities-everything-you-need-to-know-about-whats-new-and-whats-coming?ft=All)
-  [What is the utilization and metrics app?](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app)
-  [Install the Microsoft Fabric capacity metrics app](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-install?tabs=1st)
-  [Understand the metrics app overview page](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-overview-page)
-  [Understand the metrics app timepoint page](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-timepoint-page)

You can also right-click this link to open it in another tab and review this video that introduces you to these concepts:

<p><a href="https://www.youtube.com/watch?v=TZnZob8B_Xk&?t=2196"><img src="https://img.youtube.com/vi/TZnZob8B_Xk/0.jpg" height = 300></a> 

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="1.7"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">1.7 Understanding and creating Workspaces</h2>

Microsoft Fabric is a comprehensive platform that offers a variety of tools designed for the creation and administration of data pipelines. Within Microsoft Fabric, a Workspace serves as a fundamental element, facilitating collaboration among users on different projects, including dashboards, reports, and various other content. Each individual using Microsoft Fabric is allocated a personal workspace called *My workspace*, providing them with a dedicated area to work on their own content and projects.

<p><img src="https://learn.microsoft.com/en-us/fabric/enterprise/media/licenses/tenants-capacities.png#lightbox" height = 400>

#### Microsoft Fabric components

This section describes tenants, capacities, and workspaces, which are the main building blocks of a Microsoft Fabric subscription.

### Tenant
The foundation of a Microsoft Fabric subscription is the tenant. Each tenant is tied to a specific Domain Name System (DNS). Your tenant is created when you buy a capacity, and after it's created, you can add more capacities. Usually, an organization has one tenant. In such cases, the tenant is synonymous with the organization. Some companies may want to have several tenants, each with their own capacities.

### Capacity
A Microsoft Fabric capacity resides on a tenant. Each capacity that sits under a specific tenant is a distinct pool of resources allocated to Microsoft Fabric. The size of the capacity determines the amount of computation power your organization gets. Before you purchase Microsoft Fabric, review the capacity and SKUs section, to establish which capacity is right for your organization.

### Workspace
Workspaces reside within capacities and are used as containers for Microsoft Fabric items. Each Microsoft Fabric user has a personal workspace known as *My Workspace*. More workspaces can be created to enable collaboration. By default, workspaces are created in your organization's shared capacity. When your organization has other capacities, workspaces - including My Workspaces - can be assigned to any capacity in your organization.

<br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity:Creating your first Workspace</b></p>

<b>

- Validate that you have created a Workspace from the previous module
- - If not, execute the following steps.

</b>

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

- Navigate to [Tutorial: Create a Microsoft Fabric workspace](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-create-workspace)
- Navigate to your Microsoft Fabric enabled workspace
- Click +New
- Click Show all
- Ask an Instructor to validate that you have a Microsoft Fabric Enabled Workspace

<p>

If you cannot complete these steps open and follow the  [Pre-Requisites](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md).

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
 <li><a href="https://learn.microsoft.com/en-us/fabric/release-plan/">Microsoft Fabric release plan documentation</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/onelake/onelake-overview">OneLake, the OneDrive for data</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/microsoft-fabric-overview " target="_blank">The primary page for documentation on Microsoft Fabric is here</a></li>
    <li><a href="https://learn.microsoft.com/en-us/training/paths/get-started-fabric/?WT.mc_id=DP-MVP-5004032">Microsoft Learn Pathway on Fabric</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app-install">Installing the Fabric Metrics app</a></li>
  <li><a href="https://erwindekreuk.com/microsoft-fabric-content-hub/">Microsoft Fabric Content Hub from Erwin de Kreuk</a></li>

</ul>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/02%20-%20Workspaces%2C%20User%20Security%2C%20Data%20Governance%2C%20and%20Data%20Integration.md).
