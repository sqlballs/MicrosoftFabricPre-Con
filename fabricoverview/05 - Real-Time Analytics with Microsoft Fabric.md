![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop from Azure Data and the Fasttrack Team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>05 - Real-Time Analytics with Microsoft Fabric</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution using the Microsoft Fabric platform.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" target="_blank">Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module on the User Experience:

<dl>
  <dt><a href="#5.1" target="_blank">5.1 - Working with Azure Data Explorer in Microsoft Fabric</a></dt>
  <dt><a href="#5.2" target="_blank">5.2 - Working with Fabric and Streaming / Event Data</a></dt>
  <dt><a href="#5.3" target="_blank">5.3 - Working with Fabric and the Kusto Query Language (KQL)</a></dt>
</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.1 Working with Azure Data Explorer in Microsoft Fabric</h2>

Azure Data Explorer is a fully managed, high-performance, big data analytics platform that makes it easy to analyze high volumes of data in near real time. The Azure Data Explorer toolbox gives you an end-to-end solution for data ingestion, query, visualization, and management.

<p><img src="https://learn.microsoft.com/en-us/fabric/real-time-analytics/media/sample-gallery/use-sample.png" height = 400>

Real-Time Analytics is a fully managed big data analytics platform optimized for streaming, and time-series data. It utilizes a query language and engine with exceptional performance for searching structured, semi-structured, and unstructured data. Real-Time Analytics is fully integrated with the entire suite of Fabric products, for both data loading, data transformation, and advanced visualization scenarios.

Real-Time Analytics is a data analytics SaaS experience in the Microsoft Fabric offering. Azure Data Explorer is a PaaS service in Azure. Kusto(the data engine) in Real-Time Analytics (KQL Database and KQL Queryset) and Azure Data Explorer share the same core engine with the identical core capabilities, but different management behavior. 

<h3>Kusto Engine</h3>

By analyzing structured, semi-structured, and unstructured data across time series, and by using Machine Learning, Kusto makes it simple to extract key insights, spot patterns and trends, and create forecasting models. The Kusto engine uses a traditional relational model, organizing data into tables with strongly-typed schemas. Tables are stored within databases, and a cluster can manage multiple databases. It is scalable, secure, robust, and enterprise-ready, and is useful for log analytics, time series analytics, IoT, and general-purpose exploratory analytics.

The Kusto engine exhibits several distinctive features that enhance its performance and functionality.

<h4>Velocity, Variety, and Volume</h4>
You can ingest terabytes of data in minutes in batch or streaming mode. You can query petabytes of data, with results returned within milliseconds to seconds. The Kusto engine provides high velocity (millions of events per second), low latency (seconds), and linear scale ingestion of raw data. Ingest your data in different formats and structures, flowing from various pipelines and sources.

<h4>User-friendly Query Language</h4>

Real-Time Analytics uses the [Kusto Query Language (KQL)](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/), an open-source language initially invented by the Kusto engine team. The language is simple to understand and learn, and highly productive. You can use simple operators and advanced analytics. Real-Time Analytics also supports [T-SQL](https://learn.microsoft.com/en-us/azure/data-explorer/t-sql).

You can find references for the [Kusto Query Language (KQL)](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/) and for [T-SQL](https://learn.microsoft.com/en-us/azure/data-explorer/t-sql) here.

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.2 Working with Fabric and Streaming / Event Data</h2>

The *Event streams* feature in Microsoft Fabric is a centralized place in the Fabric platform to capture, transform, and route real-time events to various destinations with a no-code experience. It's part of the Real-time analytics experience. The Eventstream item you create in the portal is an instance of Fabric event streams (also called an *eventstream*). You add event data sources, routing destinations, and the event processor when the transformation is needed, to the eventstream.

<p><img src="https://learn.microsoft.com/en-us/fabric/real-time-analytics/media/real-time-analytics-overview/schematic-architecture.png" height = 400>

Everything in Fabric event streams is designed for event data. Capturing, transforming, and routing event data are the essential capabilities of Fabric event streams. It has a scalable infrastructure that the Fabric platform manages on behalf of you.

The event streams feature provides you with various source connectors to fetch the event data from diverse sources, such as Sample data and Azure Event Hubs. It also offers Custom App, the connection endpoint that enables you to develop your own applications to push event data into your eventstreams.

A Drag-and-drop experience gives you an intuitive and easy way to create your event data processing, transforming, and routing logic without writing any code. An end-to-end data flow diagram in an eventstream can provide you with a comprehensive understanding of the data flow and organization.

The Fabric event streams feature supports sending data to diverse destinations, such as Lakehouse, KQL database, and Custom App. You can have multiple destinations in an eventstream that can be attached simultaneously to receive event data from your eventstreams without interfering with each other.

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Real-Time Analytics Introduction and Tutorial</b></p>

This tutorial is based on sample streaming data called New York Yellow Taxi trip data. The dataset contains trip records of New York's yellow taxis, with fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts. This data doesn't contain latitude and longitude data, which will be loaded from a blob container and joined together with the streaming data in a later step.

You'll use the streaming and query capabilities of Real-Time Analytics to answer key questions about the trip statistics, taxi demand in the boroughs of New York and related insights, and build Power BI reports.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

Open each of the following references, and complete the steps you see there:

- [Tutorial - Introduction](https://learn.microsoft.com/en-us/fabric/real-time-analytics/tutorial-introduction)
- [Create resources](https://learn.microsoft.com/en-us/fabric/real-time-analytics/tutorial-1-resources)
- [Get data with Eventstream](https://learn.microsoft.com/en-us/fabric/real-time-analytics/tutorial-2-event-streams)
- [Get historical data](https://learn.microsoft.com/en-us/fabric/real-time-analytics/tutorial-3-get-historical-data)

You can also right-click the following video links to open them in another tab and review videos that demonstrate these concepts:

<ul>
  <li><a href="https://www.youtube.com/watch?v=-HhU7yLyuUU"><img src="https://img.youtube.com/vi/-HhU7yLyuUU/0.jpg" height = 200></a></li> 
  <li><a href="https://www.youtube.com/watch?v=_RFvcPBNiOk"><img src="https://img.youtube.com/vi/_RFvcPBNiOk/0.jpg" height = 200></a></li> 
</ul>

<h3>Real-Time Analytics</h3>

Real-Time Analytics deals with working on data as it occurs, as quickly as possible to the source generation of the data. 

<p><img src="https://learn.microsoft.com/en-us/fabric/real-time-analytics/media/real-time-analytics-overview/product-view.png" height = 400>

If any one of these questions describes your data needs, Real-Time Analytics is the right solution for you:

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

The KQL Queryset uses the Kusto Query language for creating queries, and also supports many SQL functions. For more information about the query language, see [this reference](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/index?context=/fabric/context/context).

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Create and Query a KQL Database</b></p>
</br>

In Real-Time Analytics, you interact with your data in the context of databases. A single workspace can hold multiple databases, and each database can hold multiple tables.
</br>

The KQL Queryset is the item used to run queries, view, and customize query results on data from a KQL database. Each tab in the KQL queryset can be associated with a different KQL database, and lets your save queries for later use or share with others to collaborate on data exploration. You can also change the KQL database associated with any tab, allowing you to run the same query on data in different states. The KQL Queryset uses the Kusto Query language for creating queries, and also supports many SQL functions. 

<p><img src="https://learn.microsoft.com/en-us/azure/data-explorer/media/data-explorer-overview/workflow.png" height = 400></p>

In this activity, you will learn how to query your data using Kusto Query Language in a KQL queryset.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

Open the following references and complete the steps you see there:

- [Explore data with KQL and SQL](https://learn.microsoft.com/en-us/fabric/real-time-analytics/tutorial-4-explore)
- [Use advanced KQL queries](https://learn.microsoft.com/en-us/fabric/real-time-analytics/tutorial-5-advanced-kql-query)
- [Build a Power BI report](https://learn.microsoft.com/en-us/fabric/real-time-analytics/tutorial-6-build-report)
- [Clean up resources](https://learn.microsoft.com/en-us/fabric/real-time-analytics/tutorial-7-clean-up-resources)

You can also right-click this link to open it in another tab and review this video that demonstrates this topic:

<li><a href="https://www.youtube.com/watch?v=ZVrvP20ezYk"><img src="https://img.youtube.com/vi/ZVrvP20ezYk/0.jpg" height = 200></a></li> 


<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/?context=/fabric/context/context-rta&pivots=fabric" target="_blank">Kusto Query Overview</a></li>
    <li><a href="https://learn.microsoft.com/en-us/power-bi/developer/projects/projects-overview" target="_blank">PowerBI Desktop Projects</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/real-time-analytics/realtime-analytics-compare" target="_blank"> Comparing Real-Time Analytics and Azure Data Explorer</a></li>
    <li>Please bookmark and review the following video:</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/release-plan/">Microsoft Fabric release plan documentation</a></li>
  <li><a href="https://radacad.com/fabric-real-time-analytics">Microsoft MVP Reza Rad walks through a demo he built, including a custom streaming application, to demonstrate using Real-time Analytics.</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/real-time-analytics/overview" target="_blank">What is Real-Time Analytics in Microsoft Fabric</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/whats-new#synapse-real-time-analytics-in-microsoft-fabric" target="_blank">What's new in Real-Time Analytics in Microsoft Fabric</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/release-plan/real-time-analytics" target="_blank">What's new and planned for Synapse Real-Time Analytics in Microsoft Fabric</a></li>
</ul>




<h2 id="5.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.3 Working with Fabric and the Kusto Query Language (KQL)</h2>

<p style="border-bottom: 1px solid lightgrey;"></p>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/06%20-%20Microsoft%20Fabric%20DevOps.md).
