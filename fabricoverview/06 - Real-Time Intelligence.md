![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop from Azure Data and the Fasttrack Team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>05 - Real-Time Intelligence with Microsoft Fabric</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" >Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module on the User Experience:

<dl>
  <dt><a href="#5.1" >5.1 - Working with Real-Time Intelligence in Microsoft Fabric</a></dt>
  <dt><a href="#5.2" >5.2 - Working with Fabric and Streaming / Event Data</a></dt>
  <dt><a href="#5.3" >5.3 - Working with Fabric and the Kusto Query Language (KQL)</a></dt>
  <dt><a href="#5.4" >5.4 - Eventhouse vs. KQL Database</a></dt>
  <dt><a href="#5.5" >5.5 - KQL Dashboard</a></dt>
  <dt><a href="#5.6" >5.6 - Data Activator</a></dt>
</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.1 Working with Real-Time Intelligence in Microsoft Fabric</h2>

Azure Data Explorer is a fully managed, high-performance, big data analytics platform that makes it easy to analyze high volumes of data in near real time. The Azure Data Explorer toolbox gives you an end-to-end solution for data ingestion, query, visualization, and management.

<p><img src="https://learn.microsoft.com/en-us/fabric/real-time-intelligence/media/overview/overview-schematic.png#lightbox" height = 400>

Synapse Real-Time Intelligence is a fully managed big data analytics platform optimized for streaming, and time-series data. It utilizes a query language and engine with exceptional performance for searching structured, semi-structured, and unstructured data. Real-Time Intelligence is fully integrated with the entire suite of Fabric products, for both data loading, data transformation, and advanced visualization scenarios.

Real-Time Intelligence is a data analytics SaaS experience in the Microsoft Fabric offering. Azure Data Explorer is a PaaS service in Azure. Kusto(the data engine) in Real-Time Intelligence (KQL Database and KQL Queryset) and Azure Data Explorer share the same core engine with the identical core capabilities, but different management behavior.

<h3>Kusto Engine</h3>

By analyzing structured, semi-structured, and unstructured data across time series, and by using Machine Learning, Kusto makes it simple to extract key insights, spot patterns and trends, and create forecasting models. The Kusto engine uses a traditional relational model, organizing data into tables with strongly-typed schemas. Tables are stored within databases, and a cluster can manage multiple databases. It is scalable, secure, robust, and enterprise-ready, and is useful for log analytics, time series analytics, IoT, and general-purpose exploratory analytics.

The Kusto engine exhibits several distinctive features that enhance its performance and functionality.

<h4>Velocity, Variety, and Volume</h4>
You can ingest terabytes of data in minutes in batch or streaming mode. You can query petabytes of data, with results returned within milliseconds to seconds. The Kusto engine provides high velocity (millions of events per second), low latency (seconds), and linear scale ingestion of raw data. Ingest your data in different formats and structures, flowing from various pipelines and sources.

<h4>User-friendly Query Language</h4>

Real-Time Intelligence uses the [Kusto Query Language (KQL)](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/), an open-source language initially invented by the Kusto engine team. The language is simple to understand and learn, and highly productive. You can use simple operators and advanced analytics. Real-Time Intelligence also supports [T-SQL](https://learn.microsoft.com/en-us/azure/data-explorer/t-sql).

</br>
<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.2 Working with Fabric and Streaming / Event Data</h2>

The _Event streams_ feature in Microsoft Fabric is a centralized place in the Fabric platform to capture, transform, and route real-time events to various destinations with a no-code experience. It's part of the Real-time intelligence experience. The Eventstream item you create in the portal is an instance of Fabric event streams (also called an _eventstream_). You add event data sources, routing destinations, and the event processor when the transformation is needed, to the eventstream.

The _Real-Time hub_ serves as a centralized catalog within your organization. It facilitates easy access, addition, exploration, and data sharing. By expanding the range of data sources, it enables broader insights and visual clarity across various domains. Importantly, this hub ensures that data is not only available but also accessible to all, promoting quick decision-making and informed action. The sharing of streaming data from diverse sources unlocks the potential to build comprehensive business intelligence across your organization.

Everything in Fabric event streams is designed for event data. Capturing, transforming, and routing event data are the essential capabilities of Fabric event streams. It has a scalable infrastructure that the Fabric platform manages on behalf of you.

The event streams feature provides you with various source connectors to fetch the event data from diverse sources, such as Sample data and Azure Event Hubs. It also offers Custom App, the connection endpoint that enables you to develop your own applications to push event data into your eventstreams.

A Drag-and-drop experience gives you an intuitive and easy way to create your event data processing, transforming, and routing logic without writing any code. An end-to-end data flow diagram in an eventstream can provide you with a comprehensive understanding of the data flow and organization.

The Fabric event streams feature supports sending data to diverse destinations, such as Lakehouse, KQL database, and Custom App. You can have multiple destinations in an eventstream that can be attached simultaneously to receive event data from your eventstreams without interfering with each other.

</br>
<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.3 Working with Fabric and the Kusto Query Language (KQL)</h2>

Real-Time Intelligence deals with working on data as it occurs, as quickly as possible to the source generation of the data.

If any one of these questions describes your data needs, Real-Time Intelligence is the right solution for you:

- Do I need high freshness from data ingestion to query?
- Do I want to transform streaming data?
- Do I have a service that needs to access data with low query latency (in a matter of seconds)?
- Does I need to search or access data in different formats, like structured data, semi-structured data (including complicated data such as JSON or other arrays), or unstructured data (for example, free text)?
- Do I want the ability to query large amounts of data?
- Does my data have a time component that can benefit from the time series-optimized database structure?
- Do I want the ability to create ad-hoc queries on any field or row without prior optimization?

The types of industries that benefit from data analysis in Real-Time Analytics is varied. For example: finance, transportation and logistics, smart cities, smart buildings, manufacturing operations, automotive, and oil and gas.

For Microsoft Fabric, the main items available in Real-Time Intelligence include:

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

You can also right-click this link to open it in another tab and review this video that demonstrates how to use Copilot in Real-Time Intelligence:

<a href="https://www.youtube.com/watch?v=P5YBjkB4x3g"><img src="https://img.youtube.com/vi/P5YBjkB4x3g/0.jpg" height = 200></a>

</br>
<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.4 Event House vs. KQLDB</h2>

Those new to Real-Time Intelligence may wonder about the differences between Event House and KQLDB. The following sections cover exactly what and Event House and a KQL Database are and their use case. The main difference that we will cover is similar to the constructs that organizations faced with running SQL Server on servers in their on-premises environment. Eventhouse would be analogous to the SQL Server with KQL Databases being analagous to the databases on the SQL Server

<h3>Eventhouse</h3>

Eventhouses provide a solution for handling and analyzing large volumes of data, particularly in scenarios requiring real-time analytics and exploration. They're designed to handle real-time data streams efficiently, which lets organizations ingest, process, and analyze data in near real-time. These aspects make eventhouses useful for scenarios where timely insights are crucial. Eventhouses provide a scalable infrastructure that allows organizations to handle growing volumes of data, ensuring optimal performance and resource use. Eventhouses are the preferred engine for semistructured and free text analysis. An eventhouse is a workspace of databases, which might be shared across a certain project. It allows you to manage multiple databases at once, sharing capacity and resources to optimize performance and cost. Eventhouses provide unified monitoring and management across all databases and per database.

Eventhouses are tailored to time-based, streaming events with structured, semistructured, and unstructured data. You can get data from multiple sources, in multiple pipelines (For example, Eventstream, SDKs, Kafka, Logstash, data flows, and more) and multiple data formats. This data is automatically indexed and partitioned based on ingestion time. An eventhouse would be used for any scenario that includes event-based data, for example, telemetry and log data, time series and IoT data, security and compliance logs, or financial records.

Your eventhouse is designed to optimize cost by suspending the service when not in use. When reactivating the service, you might encounter a latency of a few seconds. If you have highly time-sensitive systems that can't tolerate this latency, use Minimum consumption. This setting enables the service to be always available, but at a selected minimum level. You pay for the minimum compute level you select, or your actual consumption when your compute level is above the minimum set. The specified compute is available to all the databases within the eventhouse.

<h3>KQL Database</h3>

Databases are named entities that hold tables and stored functions. Kusto follows a relation model of storing the data where the upper-level entity is a database.

A single cluster can host several databases, in which each database hosts its own collection of tables, stored functions, and external tables. Each database has its own set of permissions that follow the Role Based Access Control (RBAC) model.

KQL Database limitations of note:

- The maximum limit of databases per cluster is 10,000.
- Database names must follow Identifier naming rules with the exception of case-sensitivity rule. Database names are case-insensitive.
- Both queries combining data from multiple tables in the same database and queries combining data from multiple databases in the same cluster have comparable performance.
- A database hosts its own collection of tables, stored functions, and external tables. Each database has its own set of permissions that follow the Role Based Access Control (RBAC) model.



</br>
<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.5"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.5 KQL Dashboard</h2>

A dashboard is a collection of tiles, optionally organized in pages, where each tile has an underlying query and a visual representation. You can natively export Kusto Query Language (KQL) queries to a dashboard as visuals and later modify their underlying queries and visual formatting as needed. In addition to ease of data exploration, this fully integrated dashboard experience provides improved query and visualization performance. As of the delivery of this course in November of 2024, Real-Time Dashboards is a feature in Public Preview and needs to be enabled in the Fabric Admin Portal. Please see the following graphic:

</br>

<p><img src="https://learn.microsoft.com/en-us/fabric/real-time-intelligence/media/real-time-dashboard/enable-tenant-settings.png" height = 400>

Similar to a PowerBI Dashboard, Real-Time Dashboards give you the opportunity to bring data together from multiple queries and querysets through interactive visuals. More features and capabilities of Real-Time Dashboards will be covered in the tutorial at the end of this module.
</br>

<p style="border-bottom: 1px solid lightgrey;"></p>
<h2 id="5.6"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.6 Data Activator</h2>

Data Activator is a no-code experience in Microsoft Fabric for automatically taking actions when patterns or conditions are detected in changing data. It monitors data in Power BI reports and Eventstreams items, for when the data hits certain thresholds or matches other patterns. It then automatically takes appropriate action such as alerting users or kicking off Power Automate workflows.

Data Activator allows users to build a digital nervous system that acts across all their data, at scale and in a timely manner. Business users can describe business conditions in a no-code experience to launch actions such as email, Teams notifications, Power Automate flows, and call into third party action systems. Business users can self-serve their needs and reduce their reliance on internal IT and developer teams, either of which is often costly and hinders agility. Customer organizations don’t need a developer team to manage and maintain custom in-house monitoring or alerting solutions.

<h3>Data Activator Core Concepts</h3>
The following concepts are used to build and trigger automated actions and responses in Data Activator.

<h4>Events</h4>
Data Activator considers all data sources to be streams of events. An event is an observation about the state of an object, with some identifier for the object itself, a timestamp, and the values for fields you’re monitoring. Eventstreams vary in frequency from many times per second for IoT sensors, to more sporadic streams such as packages being scanned in and out of shipping locations.

Data being observed from Power BI is also treated as an eventstream. In this case, events are observations made of the data on a regular schedule that typically matches the refresh frequency of your Power BI semantic model (previously known as a dataset). These observations might only happen once a day, or even once a week – it’s just a slowly changing event stream.

<h4>Objects</h4>
The business objects that you want to monitor could be physical objects like freezers, vehicles, packages, and users. The business object can also be less tangible concepts like advertising campaigns, accounts, and user sessions. In your reflex item, you model the object by connecting one or more eventstreams, choosing a column foxr the object ID, and specifying the fields you want to make properties of the object.

The term object instance refers to a specific freezer/vehicle/package etc. where object is typically used for the definition or class of object. We use population to refer to all of the object instances.

<h4>Triggers</h4>
Triggers define the conditions you want to detect on your objects, and the actions that you want to take when those conditions are met. When a trigger activates, it's always for a specific object instance. A trigger on a freezer object might detect the freezer being too warm, and send an email to the relevant technician.

<h4>Properties</h4>
Properties are useful when you want to reuse logic across multiple triggers. You might define a property on a Freezer object that smooths out the temperature readings over a one-hour period. You could then use that smoothed value in many triggers.

</br>
<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Real-Time Intelligence Introduction and Tutorial</b></p>

The following tutorial is based on sample streaming data called New York Yellow Taxi trip data. The dataset contains trip records of New York's yellow taxis, with fields capturing pick-up and drop-off dates/times, pick-up and drop-off locations, trip distances, itemized fares, rate types, payment types, and driver-reported passenger counts. This data doesn't contain latitude and longitude data, which will be loaded from a blob container and joined together with the streaming data in a later step.

You'll use the streaming and query capabilities of Real-Time Intelligence to answer key questions about the trip statistics, taxi demand in the boroughs of New York and related insights, and build reporting and automation using tools like Real-Time Dashboards and Data Activator.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

Open the following tutorial and complete steps 1-6(7 is a clean-up step and can be done when you are done with the tutorial), and complete the steps you see there:

- [Tutorial - Introduction](https://learn.microsoft.com/en-us/fabric/real-time-intelligence/tutorial-introduction)

You can also right-click the following video link to open it in another tab and review a video that demonstrates these concepts:

<a href="https://www.youtube.com/watch?v=iWepPEUUO_4"><img src="https://img.youtube.com/vi/iWepPEUUO_4/0.jpg" height = 200></a>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
  <li><a href="https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/?context=/fabric/context/context-rta&pivots=fabric" >Kusto Query Overview</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/real-time-intelligence/realtime-intelligence-compare" > Comparing Real-Time Intelligence and comparable Azure solutions</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/release-plan/">Microsoft Fabric release plan documentation</a></li>
  <li><a href="https://radacad.com/fabric-real-time-analytics">Microsoft MVP Reza Rad walks through a demo he built, including a custom streaming application, to demonstrate using Real-time Intelligence.</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/real-time-intelligence/overview" >What is Real-Time Intelligence in Microsoft Fabric</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/whats-new#real-time-intelligence-in-microsoft-fabric" >What's new in Real-Time Intelligence in Microsoft Fabric</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/release-plan/real-time-intelligence" >What's new and planned for Real-Time Intelligence in Microsoft Fabric</a></li>
</ul>

<p style="border-bottom: 1px solid lightgrey;"></p>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/06%20-%20Microsoft%20Fabric%20DevOps.md).
