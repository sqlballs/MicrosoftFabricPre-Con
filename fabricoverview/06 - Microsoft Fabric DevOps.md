![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop from Azure Data and the Fasttrack Team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>06 - Designing, Operating, and Controlling a Microsoft Fabric Deployment</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" target="_blank">Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module on Fabric DevOps:

<dl>

  <dt><a href="#6.1" target="_blank">6.1 - Designing and sizing a Fabric solution</a></dt>
  <dt><a href="#6.2" target="_blank">6.2 - Discover and Govern Data in your Deployment</a></dt>
  <dt><a href="#6.3" target="_blank">6.3 - Source Control integration with Microsoft Fabric</a></dt>
  <dt><a href="#6.4" target="_blank">6.4 - Monitoring and Managing a Fabric solution</a></dt>

</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="6.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">6.1 Designing and sizing a Fabric solution</h2>

The first step in implementing a Microsoft Fabric solution is to thoroughly understand the business opportunities from your organization, and then understand the various solutions within the Microsoft Fabric platform, so that you can choose the proper elements, sizing and pricing for your organization. Throughout this Workshop, you have learned more about the services and solutions within Microsoft Fabric, and in this section, you'll put that information to use to design a solution. 

Designing a data solution for a large organization can be a complex process that requires careful planning and execution. Here are some steps that can be taken to design a data solution for a large organization:

- Determine the goal of the data solution
- Choose the data sources
- Determine the data ingestion strategy.
- Design the data processing plan
- Set up storage for the output of the pipeline
- Plan the data workflow
- Implement a data monitoring and governance framework
- Plan the data consumption layer

>*These steps are not necessarily linear and may require iteration and refinement as you go along.*

In a large organization, a BI solution architecture can consist of:

1. Data sources
2. Data ingestion
3. Big data / data preparation
4. Data warehouse
5. BI semantic models
6. Reports

The design of such a complex structure requires an engineering mindset, though it can be one of the most creative and rewarding IT architecture efforts. [You can find a comprehensive general guide for creating a Data Architecture here.](https://learn.microsoft.com/en-us/azure/architecture/data-guide/)

There are a few decisions to make as you bring your solution design. 

- One of your first steps is to enable Microsoft Fabric for your Tenant. [You can find the process for that here.](https://learn.microsoft.com/en-us/fabric/admin/fabric-switch)
- Next, you need to understand the licensing model for using the solution. [You can find more information on that here.](https://learn.microsoft.com/en-us/fabric/enterprise/licenses)
- You can then review the [Microsoft Fabric decision guide: data warehouse or lakehouse at this reference](https://learn.microsoft.com/en-us/fabric/get-started/decision-guide-warehouse-lakehouse)
- After reviewing that material, you can check the [Microsoft Fabric decision guide: copy activity, dataflow, or Spark at this reference](https://learn.microsoft.com/en-us/fabric/get-started/decision-guide-pipeline-dataflow-spark)

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: Locate and Create a Design Decision Document for a real-world Analytics solution</b></p>

In this activity, you will determine a real-world opportunity at your organization for an Advanced Analytics solution, and create a design document you can use as a template for when you return to work. 

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- Open any document or note-taking implement you like
- Create a "solution statement" for Advanced Analytics that your organization, explaining the opportunity and the benefits of creating a solution.
- Using the references above or others that you find by a web search, create a document that has the primary elements you need to decide with their factors. For instance, you can [find some interesting decision vectors at this reference](https://www.cdw.com/content/cdw/en/articles/dataanalytics/how-the-modern-data-platform-fuels-success.html). You may also [craft a prompt at Bing Chat](https://www.bing.com/search?q=Bing+AI&showconv=1) or another GPT to create a starting point. 
- Be ready to discuss your decision guide in class.

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="6.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">6.2 - Discover and Govern Data in your Deployment</h2>

Data Governance is the set of processes and tools for locating, defining, documenting and tracking data from source systems as it moves throughout the processing cycle to analytics. Microsoft Purview is a unified data-governance service that helps you manage and govern your on-premises, in-multicloud, and any software-as-a-service (SaaS) data. You can use it to create a current and past map of your data landscape with using an automated data discovery system, sensitive data classifications, and end-to-end data lineage. You can then expose this map to your users so that they can quickly find authoritative data for analysis. 


Microsoft Purview is designed to help enterprises get the most value from their existing information assets. With this cloud-based service, you can register your data sources to help you discover and manage them. Your data sources remain in place, but a copy of the metadata for the source is added to Microsoft Purview. You can register a wide range of sources in Azure and across your multicloud data estate in Microsoft Purview. These sources include Azure Data Lake Storage, AWS, Azure SQL Database on-premises and in the cloud, and many more.


 <img src="https://learn.microsoft.com/en-us/training/modules/intro-to-microsoft-purview/media/data-map-sources.png" height = 400> 


Microsoft Purview Consists of three main systems: a **Microsoft Purview Data Map**, which provides a structure for your data estate in Microsoft Purview, where you can map your existing data stores into groups and hierarchies; the **Microsoft Purview Data Catalog**, which allows your users to browse the metadata stored in the data map so that they can find reliable data and understand its context; and **Microsoft Purview Data Estate Insights**, covering a high-level view into your data catalog, covering Data stewardship, Catalog adoption, Asset insights, Scan insights, Glossary insights, Classification insights, and Sensitivity insights. 

[You can find the complete list of Microsoft Purview learning and reference resources at this location.](https://learn.microsoft.com/en-us/training/purview/)

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: Work through the Data Catalog Tutorial</b></p>

In this activity, you will follow the basic training tutorial for Microsfot Azure Purview.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open the following reference, and follow all of the steps you see there.](https://learn.microsoft.com/en-us/training/modules/intro-to-microsoft-purview/) 


<p style="border-bottom: 1px solid lightgrey;"></p>


<h2 id="6.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">6.3 Source Control integration with Microsoft Fabric</h2>

The primary integration method for working with Microsoft Fabric in a Source Control system is the git program. If you are new to git, [there is a free Workshop you can take here - ensure you understand the material there before continuing](https://learn.microsoft.com/en-us/training/modules/intro-to-git/) since this section will assume knowledge from that Workshop. 

When you begin work on a project, you can version the solution at the  workspace level. This way, you can keep track of what you have done and undo any changes if you need to. You can also see what other people working on the same project have done in the same workspace. Using git provides the following advantages:

- Backup and version your work
- Revert to previous stages
- Collaborate with others or work alone using Git branches

To begin working with git and Microsoft Fabric, there are a few pre-requisites. Before you start, you will need to set up:

- An active Azure account registered to the same user that is using the Fabric workspace
- Access to an existing repository
- A Power BI Premium license. Your Power BI premium license still works for all Power BI features
- A Fabric capacity is required to use all supported Fabric items
- Your organization’s administrator has to [enable the Fabric switch](https://learn.microsoft.com/en-us/fabric/admin/fabric-switch)

With all that set up, you need to ensure the permissions are correct for the DevOps team. You can find a complete [definition of the permissions you need for each DevOps task at this reference](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/git-integration-process#permissions). 

After you complete those steps, you will connect a workspace to an *Azure repo*.  This is done in the Power BI tenant where you can find the workspace you want to enable, and then set the options for the repo, organization, and branches you want to enable. You can [find that process at this reference](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/git-get-started?tabs=commit-to-git#connect-a-workspace-to-an-azure-repo).

Next, you can start committing changes to git. 

Once your changes are made, you can update the workspace from git. To commit your changes to the git branch, follow these steps:

- Go to the workspace.
- Select the Source control icon. This icon shows the number of uncommitted changes. 
- Select the Changes tab of the Source control pane. A list appears with all the items you changed, and an icon indicating if the item is *new*, *modified*, *conflict*, or *deleted*.
- Select the items you want to commit. To select all items, check the top box.
- Add a comment in the box. If you don't add a comment, a default message is added automatically.
- Select Commit.

After the changes are committed, the items that were committed are removed from the list, and the workspace will point to the new commit that it's synced to. Then when the commit is completed successfully, the status of the selected items changes from *Uncommitted* to *Synced*.

If you are done with the repo and you no longer wish to track it with git, you can disconnect a workspace from git. You'll need to have *admin* permissions to do that, but the process is simple: 

- In the Workspace settings, Select *Git integration*
- Select *Disconnect workspace*
- Select *Disconnect again* to confirm

There are some considerations to keep in mind when working with git and Microsoft Fabric. Open this reference to see [the latest updates that you need to keep in mind](https://learn.microsoft.com/en-us/fabric/cicd/git-integration/git-get-started?tabs=commit-to-git#considerations-and-limitations).

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="6.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">6.4 Monitoring and Managing a Fabric solution</h2>

Managing a Microsoft Fabric solution involves multiple tools, processes, and procedures. Since there are multiple products involved, you'll often take an "outside-in" approach, where you start the administration and monitoring at the outermost level and drill in to the specific area of focus. This outside in approach should involve getting as many components under one view as possible. The Microsoft Fabric platform has various tools and features to help you administer the solution from as broad a perspective as possible, and you may also augment these views with administration processes and tools of your own. 

<h3>Administration</h3>
Your primary tasks in administration are in recovery, capacity management, object security, and user management, along with Governance and Compliance. Most of these are at done at the *workspace* level, although there are individual management tools that deal with other aspects of the solution. These interfaces include: 

- [Microsoft Fabric admin portal](https://learn.microsoft.com/en-us/fabric/admin/admin-center): Acquire and work with capacities, Ensure quality of service, Manage workspaces, Publish visuals, Verify codes used to embed Microsoft Fabric in other applications, Troubleshoot data access and other issues

<img src = "https://learn.microsoft.com/en-us/power-bi/admin/media/service-admin-portal/power-bi-settings-menu.png" height = 400>
  
- [Microsoft 365 admin portal](https://admin.microsoft.com/): Manage users and groups, Purchase and assign licenses, Block users from accessing Microsoft Fabric

 <img src="https://th.bing.com/th/id/R.0bba966c93c501a25699e7fdff90a36f?rik=C4zRsPtLjGSeog&pid=ImgRaw&r=0" height = 400> 
  
- [Microsoft 365 Security & Microsoft Purview compliance portal](https://admin.microsoft.com/): Review and manage auditing, Data classification and tracking, Data loss prevention policies, Microsoft Purview Data Lifecycle Management

 <img src="https://th.bing.com/th/id/R.0bba966c93c501a25699e7fdff90a36f?rik=C4zRsPtLjGSeog&pid=ImgRaw&r=0" height = 400> 
  
- [Azure Active Directory in the Azure portal](https://aad.portal.azure.com/): Configure conditional access to Microsoft Fabric resources

<img src="https://learn.microsoft.com/pt-br/azure/active-directory/fundamentals/media/add-users-azure-active-directory/add-user-in-users-all-users.png" height = 400>

- [PowerShell cmdlets](https://learn.microsoft.com/en-us/powershell/power-bi/overview): Manage workspaces and other aspects of Microsoft Fabric using scripts

<img src="https://learn.microsoft.com/en-us/azure/active-directory/reports-monitoring/media/reference-powershell-reporting/get-azureadauditsigninlogs.png" height = 400>

- [Administrative APIs and SDK](https://learn.microsoft.com/en-us/power-bi/developer/visuals/create-r-based-power-bi-desktop): Build custom admin tools.

<img src="https://reviewsapp.org/uploads/visual-studio-code-a-powerful-tool-for-all-developers.png" height = 400>

<h3>Monitoring</h3>
Depending on your solution, you'll develop a custom set of monitoring tools, processes and techniques that give you the most insight into the status, trends, issues and alerts for your deployment. It's best to start with an "outside-in" approach for these monitoring elements, since that will help you narrow down any actions you need to take quickly. You can use the tools provided within the system for this approach, but you will likely need to combine some of them with other tools and perhaps integrate your monitoring into your organization's current tool set. 

The first tool you can use for your monitoring is the *Monitoring Hub*. The Monitoring hub enables users to monitor various Microsoft Fabric activities, such as dataset refresh and Spark Job runs and many others, from a central location. 

![Monitoring Hub Panel](https://learn.microsoft.com/en-us/fabric/admin/media/monitoring-hub/admin-monitoring-hub-02.png)

The first seven columns in the list of items are shared across all Monitoring hub views. The columns after the first seven are specific to the viewing context, such as Power BI. When you select an item from the list, Monitoring hub displays detailed information about that item.

When you hover over an item's name, any available quick actions for the item type are displayed, such as stop, start, re-run, or other quick actions. You can also open a detail pane for the item itself when you hover, for example, View run history for datasets that are in Monitoring hub, to display their refresh activities.

Another important concept in monitoring your solution is to understand how each component uses its own internal logging system or transmits that information to the Microsoft Azure Logging system. [This reference provides a guide to the various ingestion mechanisms for Azure Logs](https://learn.microsoft.com/en-us/azure/azure-monitor/essentials/platform-logs-overview). 

To analyze the logs, you have several options. Log analysis is based on the Azure Data Explorer, and uses the Kusto Query Language (KQL) to navigate, along with a graphical Interface. [You can learn more about analyzing logs at this reference](https://learn.microsoft.com/en-us/azure/azure-monitor/logs/log-query-overview). [There's an excellent resource to learn more about Kusto here.](https://detective.kusto.io/)


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: Review the Monitoring and Management Tools for Microsoft Fabric</b></p>

In this Activity you will navigate the primary interfaces for monitoring and managing your solution. You can augment this activity with a discussion of your current monitoring and management tools and processes, and how you can integrate these into your process.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

Open each of the following tools and navigate the various actions and properties they provide. If you do not have a full deployment yet, you can open the document pages from the links for each tool. 

- [Admin Center](https://learn.microsoft.com/en-us/fabric/admin/admin-center) 
- [Capacity management](https://learn.microsoft.com/en-us/fabric/enterprise/pause-resume)
- [Using the Monitoring Hub](https://learn.microsoft.com/en-us/fabric/admin/monitoring-hub) 
- [Using the Metrics app](https://learn.microsoft.com/en-us/fabric/enterprise/metrics-app)

> If you only reviewed the documentation in this Activity, ensure you bookmark each of these references and then perform the Activity in full once you do have your deployment. 

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: Learn basic Log Navigation</b></p>

In this Activity you will navigate the primary interfaces for navigating the Azure Log Monitoring system. 

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open this reference and follow the steps you see there](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/tutorials/learn-common-operators?pivots=azuremonitor) 

<p style="border-bottom: 1px solid lightgrey;"></p>

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
  <li><a href="https://learn.microsoft.com/en-us/fabric/release-plan/">Microsoft Fabric release plan documentation</a></li>
  <li><a href="https://data-ascend.com/2023/10/11/how-do-you-set-up-your-data-governance-in-microsoft-fabric/">Microsoft MVP Marthe Moengen has an excellent article on Data Governance in Microsoft Fabric that you can reference here.</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/admin/" target="_blank">Microsoft Fabric Administrator Portal</a></li>
  <li><a href="https://www.kevinrchant.com/2023/08/09/prepare-azure-devops-for-microsoft-fabric-git-integration/" target="_blank">Kevin Chant's tutorial on git integration with Fabric</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/whats-new" target="_blank">As always, this is a fast-changing technology, so ensure you check this reference to find the latest improvements.</a></li>
</ul>

Congratulations! You have completed this workshop on *Microsoft Fabric for the Data Professional*. You now have the tools, assets, and processes you need to extrapolate this information into other applications.
