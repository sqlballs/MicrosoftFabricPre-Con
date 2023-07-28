![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft workshop from the SQL Server team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>05 - The Fabric User Experience</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution using the Microsoft Fabric platform.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" target="_blank">Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module on the User Experience:

<dl>

  <dt><a href="#5.1" target="_blank">5.1 - Working with Fabric using Power BI</a></dt>
  <dt><a href="#5.2" target="_blank">5.2 - Working with Fabric and the Kusto Query Language (KQL)</a></dt>
  <dt><a href="#5.3" target="_blank">5.3 - Working with Fabric and Streaming / Event Data</a></dt>
  
</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.1 Working with Fabric using Power BI</h2>

Working with Power BI and Microsoft Fabric uses the features and functionality already present in Power BI. Power BI Premium customers can simply turn on the Fabric tenant setting in the admin portal. With Fabric’s unified capacity model, Power BI Premium capacity can be utilized by any of the new workloads. Read this documentation for more information on Fabric’s single capacity model. Power BI Pro customers can access this functionality through capacity trials. There are also several Power BI Premium only features designed to transform how you analyze and visualize your data.

As you saw in a previous Module, Copilot in Power BI leverages the power of large language models into Power BI at every layer to help users get more done and create more value from their data. Using Copilot, you can simply describe the visuals and insights you’re looking for, and Copilot will do the rest. Users can create and tailor reports in seconds, generate and edit DAX calculations, create narrative summaries, and ask questions about their data, all in conversational language. With the ability to easily tailor the tone, scope, and style of narratives and add them seamlessly within reports, Power BI can also deliver data insights even more impactfully through easy-to-understand text summaries. Microsoft has also released the quick measure suggestions for DAX capability that helps analysts quickly create the code they need. 

**Unified data foundation with OneLake and Direct Lake mode**

Power BI is standardizing on open data formats by adopting Delta Lake and Parquet as its native storage format to help you avoid vendor lock-in and reduce data duplication and management. Direct Lake mode unlocks incredible performance directly against OneLake, with no data movement. Combining this with the ability for the other analytical engines to read and write data directly in the lake, Fabric will reshape how business users consume big data. Power BI datasets in Direct Lake mode enjoy query performance on a par with import mode, with the real-time nature of DirectQuery. And the data never leaves the lake, so there is no need to manage refreshes.

To try Direct Lake from your Lakehouse or Warehouse in Fabric, click on New Power BI Dataset, select the tables you want to include, and click Confirm. Open the data model to create measures and relationships as you would for any other Power BI dataset. Lastly, click new report and create beautiful Power BI reports. Note the integrated experience from data in the lake through to report creation without leaving the browser or performing a refresh.

**Enterprise-grade collaboration with Git integration for Power BI datasets and reports**

We are also enabling more seamless collaboration with your development team on Power BI content with Git integration. You can now easily connect your workspace to Azure DevOps repositories to track changes, revert to previous versions, and merge updates from multiple team members into a single source of truth that will be synced into the workspace with a single click.

As a developer, you can use this integration to:

- Use Power BI Desktop to author report and dataset metadata files in source-control friendly formats.
- Save as a Power BI project (.PBIP) to a folder instead of to a .PBIX file.
- Enable multiple developer collaboration, source control integration to track version history, compare different revisions (diff), and revert to previous versions.
- Use continuous integration and continuous delivery (CI/CD) to enforce quality gates prior to reaching production environments.
- Enable code reviews, automated testing, and automated build to validate the integrity of a deployment.
- Users can leverage Git integration and deployment pipelines for an end-to-end application lifecycle management of their work by developing through Git integration and deploying their Power BI content across dev, test, and production workspaces. Developers can use the user interface (UI) experience or automate the process through other tools, such as Azure Pipelines.

[Review this video to learn more about Power BI and Fabric](https://youtu.be/fvuL8Nk_gxU)

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open this reference and follow all the steps you see there](https://learn.microsoft.com/en-us/power-bi/fundamentals/fabric-get-started)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.2 Working with Fabric and the Kusto Query Language (KQL)</h2>

Real-Time Analytics deals with working on data as it occurs, as quickly as possible to the source generation of the data. If any one of these questions describes your data needs, Real-Time Analytics is the right solution for you:

- Do I need high freshness from data ingestion to query?
- Do I want to transform streaming data?
- Do I have a service that needs to access data with low query latency (in a matter of seconds)?
- Does I need to search or access data in different formats, like structured data, semi-structured data (including complicated data such as JSON or other arrays), or unstructured data (for example, free text)?
- Do I want the ability to query large amounts of data?
- Does my data have a time component that can benefit from the time series-optimized database structure?
- Do I want the ability to create ad-hoc queries on any field or row without prior optimization?

The types of industries that benefit from data analysis in Real-Time Analytics is varied. For example: finance, transportation and logistics, smart cities, smart buildings, manufacturing operations, automotive, and oil and gas.

For Microsoft Fabric, the main items available in Real-Time Analytics include:

- Eventstream for capturing, transforming, and routing real-time events to various destinations with a no-code experience.
- A KQL database for data storage and management. Data loaded into a KQL database can be accessed in OneLake and is exposed to other Fabric experiences.
- A KQL queryset to run queries, view, and customize query results on data. The KQL queryset allows you to save queries for future use, export and share queries with others, and includes the option to generate a Power BI report.

The KQL Queryset is the item used to run queries, view, and customize query results on data from a KQL database. Each tab in the KQL queryset can be associated with a different KQL database, and lets your save queries for later use or share with others to collaborate on data exploration. You can also change the KQL database associated with any tab, allowing you to run the same query on data in different states.

The KQL Queryset uses the Kusto Query language for creating queries, and also supports many SQL functions. For more information about the query language, see [Kusto Query Language overview](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/index?context=/fabric/context/context).

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open this reference and follow the steps you see there](https://learn.microsoft.com/en-us/fabric/real-time-analytics/tutorial-introduction)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.3 Working with Fabric and Streaming / Event Data</h2>

The *Event streams* feature in Microsoft Fabric is a centralized place in the Fabric platform to capture, transform, and route real-time events to various destinations with a no-code experience. It's part of the Real-time analytics experience. The Eventstream item you create in the portal is an instance of Fabric event streams (also called an *eventstream*). You add event data sources, routing destinations, and the event processor when the transformation is needed, to the eventstream.

Everything in Fabric event streams is designed for event data. Capturing, transforming, and routing event data are the essential capabilities of Fabric event streams. It has a scalable infrastructure that the Fabric platform manages on behalf of you.

The event streams feature provides you with various source connectors to fetch the event data from diverse sources, such as Sample data and Azure Event Hubs. It also offers Custom App, the connection endpoint that enables you to develop your own applications to push event data into your eventstreams.

A Drag-and-drop experience gives you an intuitive and easy way to create your event data processing, transforming, and routing logic without writing any code. An end-to-end data flow diagram in an eventstream can provide you with a comprehensive understanding of the data flow and organization.

The Fabric event streams feature supports sending data to diverse destinations, such as Lakehouse, KQL database, and Custom App. You can have multiple destinations in an eventstream that can be attached simultaneously to receive event data from your eventstreams without interfering with each other.

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open this reference and follow the steps you see there](https://learn.microsoft.com/en-us/fabric/real-time-analytics/event-streams/create-manage-an-eventstream)

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://www.myonlinetraininghub.com/category/power-query" target="_blank">Power Query Hub by Mynda Treacy</a></li>
</ul>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/06%20-%20Microsoft%20Fabric%20DevOps.md.