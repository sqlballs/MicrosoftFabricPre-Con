![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop from Azure Data and the Fasttrack Team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="02"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png">02 - Data Warehouse and Data Integration</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution using the Microsoft Fabric platform.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" >Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module:

<dl>
  <dt><a href="#2.1">2.1 - Data Warehouse</a></dt>
  <dt><a href="#2.2">2.2 - Ingesting data with pipelines</a></dt>
  <dt><a href="#2.3>2.3 - SQL Experience</a></dt>
  <dt><a href="#2.4">2.4 - Ingesting data with pipelines and data flows</a></dt>
</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="2.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">2.1 Data Warehouse</h2>

Microsoft Fabric introduces a lake centric data warehouse built on an enterprise grade distributed processing engine that enables industry leading performance at scale while eliminating the need for configuration and management. Through an easy to use SaaS experience that is tightly integrated with Power BI for easy analysis and reporting, Warehouse in Microsoft Fabric converges the world of data lakes and warehouses with a goal of greatly simplifying an organizations investment in their analytics estate. Data warehousing workloads benefit from the rich capabilities of the SQL engine over an open data format, enabling customers to focus on data preparation, analysis and reporting over a single copy of their data stored in their OneLake.

The Warehouse is built for any skill level - from the citizen developer through to the professional developer, DBA or data engineer. The rich set of experiences built into Microsoft Fabric workspace enables customers to reduce their time to insights by having an easily consumable, always connected dataset that is integrated with Power BI in DirectLake mode. This enables second-to-none industry leading performance that ensures a customer's report always has the most recent data for analysis and reporting. Cross-database querying can be leveraged to quickly and seamlessly leverage multiple data sources that span multiple databases for fast insights and zero data duplication.  

<p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/761b96fa-4e30-43d1-8ffe-d34650599be2" height = 400>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity:Creating your first Warehouse</b></p>

- Open the following reference in another tab, [Tutorial: Analyze data with a notebook](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-create-warehouse)
- - Follow Step 2
 
 You can also right-click this link to open it in another tab and review this video that introduces you to these concepts:

 <p><a href="https://www.youtube.com/watch?v=StIBBb69wDw"><img src="https://img.youtube.com/vi/StIBBb69wDw/0.jpg" height = 200></a> 

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="2.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">2.2 Ingesting data with pipelines</h2>

In the previous module, you learned about the main storage concept, OneLake. To move data into and out of OneLake, you will use the Microsoft Fabric experience of *Data Factory*.

Data Factory provides a data integration tool to ingest, prepare and transform data from a rich set of data sources (for example, databases, data warehouse, Lakehouse, real-time data, and more). Using the Data Factory, you can transform the data with intelligent transformations and leverage a rich set of activities. Microsoft Fabric uses Data Factory to  bring fast copy (data movement) capabilities to both *dataflows* and *data pipelines*. With Fast Copy, you can move data quickly, and it enables you to bring data to your Lakehouse and Data Warehouse in Microsoft Fabric for analytics.

There are two primary concepts to understand about using Azure Data Factory with Microsoft Fabric: 

- Dataflows
- Data pipelines

 <h3>Data Factory Pipelines</h3>

Data pipelines enable powerful workflow capabilities at cloud-scale. With data pipelines, you can build complex workflows that can refresh your dataflow, move PB-size data, and define sophisticated control flow pipelines. You use data pipelines to build complex ETL and data factory workflows that can perform many different tasks at scale. Control flow capabilities are built into data pipelines that allow you to build workflow logic, which provides loops and conditionals.

You can add a configuration-driven copy activity together with your low-code dataflow refresh in a single pipeline for an end-to-end ETL data pipeline. You can even add code-first activities for Spark Notebooks, SQL scripts, stored procs, and more.

Data pipelines offer an alternative to using the COPY command through a graphical user interface. A data pipeline is a logical grouping of activities that together perform a data ingestion task. Pipelines allow you to manage extract, transform, and load (ETL) activities instead of managing each one individually.

In this tutorial, you'll create a new pipeline that loads sample data into a Warehouse in Microsoft Fabric.

<p><img src="https://learn.microsoft.com/en-us/fabric/data-factory/media/data-factory-overview/data-pipelines.png" height = 300></p>

<br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity:Ingest data into warehouse</b></p>

- Open the following reference in another tab, [Tutorial: Analyze data with a notebook](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-ingest-data)
- - Follow Step 3

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="2.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">2.3 SQL Experience</h2>

Since Data Warehousing is closely related to the SQL experience persona, you can leverage many of the features that you may be accustomed to using in SQL Server, such as:

- <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-create-tables" >Create Tables</a>

   Creating a table in Fabric is a remarkably similar process to creating a table in SQL Server. You can initiate a new query within the Fabric editor or SQL Server Management Studio (SSMS) and execute the 'create table' script, which will result in the table's creation within Microsoft Fabric.

  <p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/11f9beaa-6d57-4538-b2db-89f1470c7e56" height = 100>


- <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-load-data" >Load data using T-SQL</a>

Loading data into your newly created table is a straightforward process. You can achieve this with ease by utilizing the COPY INTO T-SQL statement. This statement allows you to efficiently load data into your tables.

<p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/717e6430-b66d-4fd1-bda5-7ef97e1e4d0f" height = 200>

- <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-clone-table" >Clone a table using T-SQL</a>

Microsoft Fabric offers the capability to create near-instantaneous zero-copy clones with minimal storage costs.

- Table clones facilitate development and testing processes by creating copies of tables in lower environments.
- Table clones provide consistent reporting and zero-copy duplication of datasets for analytical workloads and machine learning modeling and testing.
- Table clones provide the capability of data recovery in the event of a failed release or data corruption by retaining the previous state of data.

<p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/a05bc1b4-5033-4056-9a81-8c52a3c80a73" height = 150>

You can also right-click this link to open it in another tab and review this video that introduces you to these concepts:

<p><a href="https://www.youtube.com/watch?v=2rETPwBLnnY"><img src="https://img.youtube.com/vi/2rETPwBLnnY/0.jpg" height=200>

- <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-transform-data" >Transform data using stored procedure</a>

For SQL users, the availability of stored procedures is a valuable feature, and Microsoft Fabric supports them in a way that aligns with your familiarity. Writing stored procedures in Fabric follows the same approach as you would in SQL Server, making it convenient for users to leverage this important SQL functionality. The data can be transformed using Stored procedures.

<p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/dac19efe-a5ec-4c38-8315-12bc6990d48e" height = 700>

- <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-visual-query" >Create a query with the visual query builder</a>

Microsoft Fabric is designed with user-friendliness in mind, catering to individuals who may not be proficient in writing SQL queries. You have the option to utilize the Visual Query Builder, a graphical interface that simplifies the process of building queries. By merely dragging and dropping fields, the query builder will seamlessly generate the necessary SQL query in the background. This feature makes data retrieval and manipulation more accessible for a broader range of users.

<p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/d39a994d-815b-44c3-bef5-4a24d5ab0ab6" height = 60>

<br> 

<p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/5b87b205-64c8-4293-b063-9bbcb49ecc24" height = 400>

<br> 

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity:SQL Experience</b></p>

- Open the following reference in another tab, [Tutorial: SQL Experience](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-create-tables)
- - Follow Steps 4 - 8

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="2.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">2.4 Ingesting Data using pipelines with Data flow Gen2</h2>

<h3>Data Factory Dataflows</h3>

Dataflows provide a low-code interface for ingesting data from hundreds of data sources, transforming your data using 300+ data transformations. You can then load the resulting data into multiple destinations, such as Azure SQL databases and more. Dataflows can be run repeatedly using manual or scheduled refresh, or as part of a data pipeline orchestration.

Dataflows are built using Power Query in Microsoft products and services such as Excel, Power BI, Power Platform, Dynamics 365 Insights applications, and more, using Power Query to perform data ingestion and data transformations across the data estate. You can also create joins, aggregations, data cleansing, custom transformations, and much more all from a highly visual, low-code UI.

<p><img src="https://learn.microsoft.com/en-us/fabric/data-factory/media/data-factory-overview/dataflow-experience.png#lightbox" height = 400>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: Work through the Ingesting Data using pipelines with Data flow Gen2</b></p>

In this activity, you will follow the basic training tutorial for Microsfot Azure Purview.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- Right-click this link to open it in another tab and review this video that introduces you to these concepts:

<p><a href="https://www.youtube.com/watch?v=mlxlPhJ5ovc"><img src="https://img.youtube.com/vi/mlxlPhJ5ovc/0.jpg" height = 200></a> 

<br>

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
 <li><a href="https://learn.microsoft.com/en-us/fabric/release-plan/">Microsoft Fabric release plan documentation</a></li>
 <li><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/security/">Data Warehouse Security</a></li>
 <li><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity">Data Warehouse Connectivity</a></li>
 <li><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/guidelines-warehouse-performance">Data Warehouse Performance Guidelines</a></li>
 <li><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/data-types">Data Warehouse Data Types</a></li>
 <li><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/table-constraints">Data Warehouse Table Constraints</a></li>
 <li><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/statistics">Data Warehouse Statistics</a></li>
 <li><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/usage-reporting">Data Warehouse Usage Monitoring</a></li>
 <li><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/compute-capacity-smoothing-throttling">Data Warehouse Smoothing & Throttling</a></li>
 <li><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/monitor-using-dmv">Data Warehouse Monitoring using DMVs</a></li>
</ul>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/03%20-%20The%20Data%20Lakehouse.md).