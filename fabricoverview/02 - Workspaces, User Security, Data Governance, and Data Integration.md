![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft workshop from the SQL Server team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>02 - Workspaces, User Security, Data Governance, and Data Integration</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution using the Microsoft Fabric platform.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" target="_blank">Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module:

<dl>
  <dt><a href="#01">2.1 - Understanding and creating Workspaces</a></dt>
  <dt><a href="#02">2.2 - Connecting to and managing the Workspace</a></dt>
  <dt><a href="#03">2.3 - Ingesting data with pipielines and data flows</a></dt>
  <dt><a href="#04">2.4 - Security concepts</a></dt>
</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="01"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">2.1 Understanding and creating Workspaces</h2>

Microsoft Fabric is a comprehensive platform that offers a variety of tools designed for the creation and administration of data pipelines. Within Microsoft Fabric, a Workspace serves as a fundamental element, facilitating collaboration among users on different projects, including dashboards, reports, and various other content1. Each individual using Microsoft Fabric is allocated a personal workspace called My workspace, providing them with a dedicated area to work on their own content and projects.

![](https://learn.microsoft.com/pt-br/fabric/onelake/media/onelake-overview/onelake-foundation-for-fabric.png)

#### <i>Microsoft Fabric components</i>

This section describes tenants, capacities, and workspaces, which are the main building blocks of a Microsoft Fabric subscription.

#### <i>Tenant</i>
The foundation of a Microsoft Fabric subscription is the tenant. Each tenant is tied to a specific Domain Name System (DNS). Your tenant is created when you buy a capacity, and after it's created, you can add more capacities. Usually, an organization has one tenant. In such cases, the tenant is synonymous with the organization. Some companies may want to have several tenants, each with their own capacities.

#### <i>Capacity</i>
A Microsoft Fabric capacity resides on a tenant. Each capacity that sits under a specific tenant is a distinct pool of resources allocated to Microsoft Fabric. The size of the capacity determines the amount of computation power your organization gets. Before you purchase Microsoft Fabric, review the capacity and SKUs section, to establish which capacity is right for your organization.

#### <i>Workspace</i>
Workspaces reside within capacities and are used as containers for Microsoft Fabric items. Each Microsoft Fabric user has a personal workspace known as My Workspace. More workspaces can be created to enable collaboration. By default, workspaces are created in your organization's shared capacity. When your organization has other capacities, workspaces - including My Workspaces - can be assigned to any capacity in your organization.


<br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity:Creating your first Workspace</b></p>

In this activity you will create a basic Workspace in Fabric.

Microsoft Fabric admins can use the Create workspaces setting to designate which users in the organization can create workspaces.

To create a Microsoft Fabric workspace, you need to:

        Sign in to Power BI.
        
        Select Workspaces > New workspace.
        
        Fill out the Create a workspace form by giving the workspace a unique name (mandatory), providing a description of the workspace (optional), and assigning the workspace to a domain (optional).
        
        Expand the Advanced section.
        
        Choose Fabric capacity or Trial in the License mode section.
        
        Choose a premium capacity you have access to.
        
        Select Apply. The workspace is created and opened.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open this reference, and complete the steps you see there.](https://learn.microsoft.com/en-us/fabric/get-started/create-workspaces)

<p style="border-bottom: 1px solid lightgrey;"></p>


<h2 id="02"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">2.2 Connecting to and managing the Workspace</h2>

To work with your Microsoft Fabric Workspace, you need to connect to it. 

![Fabric Workspace view](https://learn.microsoft.com/en-us/fabric/get-started/media/workspaces/fabric-workspace-page.png#lightbox)

Workspaces are places to collaborate with colleagues to create collections of items such as lakehouses, warehouses, and reports.To connect to a Microsoft Fabric Workspace, you can follow these steps1:

- Go to *Manage gateways* to create connection.
- From the page header in *Data Integration service*, select *Settings > Manage connections and gateways*.
- Select *New* at the top of the ribbon to add a new data source.
- The *New connection* pane is displayed on the left side of the page.

To manage your Workspace, you can follow these steps:

- Go to the workspace you want to manage.
- Select the workspace *settings* icon.
- In the *Settings* pane, you can manage the following settings:
  - General settings
  - Security settings
  - Data integration settings
  - Advanced settings

<br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Create a Workspace</b></p>

TODO:-[Create a workspace.]([https://learn.microsoft.com/en-us/fabric/get-started/create-workspaces](https://learn.microsoft.com/en-us/fabric/get-started/create-workspaces)


<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="03"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">2.3 Ingesting data with pipielines and data flows</h2>

In the previous module, you learned about the main storage concept, OneLake. To move data into and out of OneLake, you will use the Microsoft Fabric experience of *Microsoft Azure Data Factory*.

Data Factory provides a data integration tool to ingest, prepare and transform data from a rich set of data sources (for example, databases, data warehouse, Lakehouse, real-time data, and more). Using the Data Factory, you can transform the data with intelligent transformations and leverage a rich set of activities. Microsoft Fabric uses Data FFactory to  bring fast copy (data movement) capabilities to both *dataflows* and *data pipelines*. With Fast Copy, you can move data quickly, and it enables you to bring data to your Lakehouse and Data Warehouse in Microsoft Fabric for analytics.


There are two primary concepts to understand about using Azure Data Factory with Microsoft Fabric: 

- Dataflows
- Data pipelines

<h3>Microsoft Azure Data Factory Dataflows</h3>

Dataflows provide a low-code interface for ingesting data from hundreds of data sources, transforming your data using 300+ data transformations. You can then load the resulting data into multiple destinations, such as Azure SQL databases and more. Dataflows can be run repeatedly using manual or scheduled refresh, or as part of a data pipeline orchestration.

Dataflows are built using Power Query in Microsoft products and services such as Excel, Power BI, Power Platform, Dynamics 365 Insights applications, and more, using Power Query to perform data ingestion and data transformations across the data estate. You can also create joins, aggregations, data cleansing, custom transformations, and much more all from a highly visual, low-code UI.

![Dataflows](https://learn.microsoft.com/en-us/fabric/data-factory/media/data-factory-overview/dataflow-experience.png#lightbox)

<h3>Microsoft Azure Data Factory Pipelines</h3>

Data pipelines enable powerful workflow capabilities at cloud-scale. With data pipelines, you can build complex workflows that can refresh your dataflow, move PB-size data, and define sophisticated control flow pipelines. You use data pipelines to build complex ETL and data factory workflows that can perform many different tasks at scale. Control flow capabilities are built into data pipelines that allow you to build workflow logic, which provides loops and conditionals.

Add a configuration-driven copy activity together with your low-code dataflow refresh in a single pipeline for an end-to-end ETL data pipeline. You can even add code-first activities for Spark Notebooks, SQL scripts, stored procs, and more.

![Data Pipeline](https://learn.microsoft.com/en-us/fabric/data-factory/media/data-factory-overview/data-pipelines.png#lightbox)

<br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Create a Data Flow and a Data Pipeline</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="04"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">2.4 Security concepts</h2>

Security and reliability are key foundational features for every organization. In Microsoft Fabric, as you bring your data to the cloud and use it with various analytics experiences such as Power BI, Data Factory, and the next generation of Synapse, Microsoft ensures that built-in security and reliability features secure your data at rest and transit.

There are three important Security features to understand: 

- Conditional access - Secure your apps using Azure Active Directory (Azure AD).
- Service tags - Enable an Azure SQL Managed Instance (MI) to allow incoming connections from Microsoft Fabric.
- Lockbox - Control how Microsoft engineers access your data.

<h3>Conditional Access</h3>

The Conditional Access feature in Azure Active Directory (Azure Entra) offers a number of ways enterprise customers can secure apps in their tenants, including:

- Multi-factor authentication
- Allowing only Intune enrolled devices to access specific services
- Restricting user locations and IP ranges

<h3>Service Tags</h3>

You can use Azure service tags with Microsoft Fabric to enable an Azure SQL Managed Instance (MI) to allow incoming connections from the Microsoft Fabric. In Azure, a service tag is a defined group of IP addresses that you can configure to be automatically managed, as a group, to minimize the complexity of updates or changes to network security rules. By using service tags with Microsoft Fabric, you can enable a SQL Managed Instance to allow incoming connections from the Microsoft Fabric service.

<h3>Lockbox</h3>

Use Customer Lockbox for Microsoft Azure to control how Microsoft engineers access your data in an audited way. Typically, Customer Lockbox is used to help Microsoft engineers troubleshoot a Microsoft Fabric service support request. Customer Lockbox can also be used when Microsoft identifies a problem, and a Microsoft-initiated event is opened to investigate the issue.

To enable Customer Lockbox for Microsoft Fabric, you must be an Azure AD Global Administrator. To assign roles in Azure AD, see Assign Azure AD roles to users.

- Open the Azure portal.
- Go to Customer Lockbox for Microsoft Azure.
- In the Administration tab, select Enabled.


In cases where the Microsoft engineer can't troubleshoot your issue by using standard tools, elevated permissions are requested using the Just-In-Time (JIT) access service. The request can come from the original support engineer, or from a different engineer. After the access request is submitted, the JIT service evaluates the request, considering factors such as:

- The scope of the resource
- Whether the requester is an isolated identity or using multi-factor authentication
- Permissions levels

Based on the JIT role, the request may also include an approval from internal Microsoft approvers. For example, the approver might be the customer support lead or the DevOps Manager.When the request requires direct access to customer data, a Customer Lockbox request is initiated. For example, in cases where remote desktop access to a customer's virtual machine is needed. Once the Customer Lockbox request is made, it awaits customer's approval before access is granted.

![Lockbox](https://learn.microsoft.com/en-us/fabric/security/media/security-lockbox/email-example.png#lightbox)

<h3>Resiliency</h3>

Resiliency is another concept that deals with the security of your data, by ensuring it is available when you need it.  The primary functions that provide resliency are *Resource Zones* and *Business Continuity and Disaster Recovery*. Microsoft Fabric also relies on the the availability concepts in [Azure Reliability](https://learn.microsoft.com/en-us/azure/architecture/framework/resiliency/overview).

Azure availability zones are at least three physically separate groups of datacenters within each Azure region. Datacenters within each zone are equipped with independent power, cooling, and networking infrastructure. In the case of a local zone failure, availability zones are designed so that if the one zone is affected, regional services, capacity, and high availability are supported by the remaining two zones. Failures can range from software and hardware failures to events such as earthquakes, floods, and fires. Tolerance to failures is achieved with redundancy and logical isolation of Azure services. For more detailed information on availability zones in Azure, see Regions and availability zones.

Azure availability zone-enabled services are designed to provide the right level of reliability and flexibility. They can be configured in two ways. They can be either zone redundant, with automatic replication across zones, or zonal, with instances pinned to a specific zone. You can also combine these approaches. For more information on zonal vs. zone-redundant architecture, see Build solutions with availability zones.

Availability zones allow Fabric customers to run critical applications with higher availability and fault tolerance in the event of datacenter failures. Fabric supports zone-redundant availability zones, such that resources replicate across zones automatically, without any customer intervention.

Business Continuity and Disaster Recovery (BCDR) is supported in Fabric for for Power BI Fabric items, such as datasets, reports, etc.

> Note: Non-Power BI Fabric items, such as Notebooks, KQL Databases, or for data stored in OneLake are not covered under BCDR


<br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="" target="_blank">TODO: Enter courses, books, posts, whatever the student needs to extend their study</a></li>
</ul>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/03%20-%20The%20Data%20Lakehouse.md).
