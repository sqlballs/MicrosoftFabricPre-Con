![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>05 -  Mirroring in Fabric</h2>
<br></br>
In this module we will explore various data replication techniques using Mirroring in Fabric, which offers efficient and low-latency solutions. They will explore the process of integrating diverse data sources.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" >Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module on the User Experience:

<dl>
  <dt><a href="#5.1" >5.1 - What is Mirroing in Fabric?</a></dt>
  <dt><a href="#5.2" >5.2 - When to use Mirroing in Fabric</a></dt>
  <dt><a href="#5.3" >5.3 - Monitor Fabric mirrored database replication </a></dt>
  <dt><a href="#5.4" >5.4 - Trouble shoot Fabric mirrored database</a></dt>
</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.1 What is Mirroing in Fabric?</h2>
<br></br>

Mirroring in Fabric is a low-cost and low-latency solution to bring data from various systems together into a single analytics platform. You can continuously replicate your existing data estate directly into Fabric's OneLake from a variety of Azure databases and external data sources.

With the most up-to-date data in a queryable format in OneLake, you can now use all the different services in Fabric, such as running analytics with Spark, executing notebooks, data engineering, visualizing through Power BI Reports, and more.

Mirroring in Fabric allows users to enjoy a highly integrated, end-to-end, and easy-to-use product that is designed to simplify your analytics needs. Built for openness and collaboration between Microsoft, and technology solutions that can read the open-source Delta Lake table format.

Mirroring in Fabric accelerates the data integration process, providing a turnkey solution for creating data replicas in OneLake to meet all analytical needs.

</br>

<h2 id="5.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.2 - When to use Mirroing in Fabric</h2>
<br></br>

Today, many organizations face challenges with mission-critical operational or analytical data being isolated in silos, requiring complex ETL pipelines and business processes to access and work with this data. This situation leads to restricted access to important, constantly changing data, friction between people, processes, and technology, long wait times to create necessary data pipelines, and a lack of freedom to use preferred tools for analysis and sharing insights. Additionally, there is often no proper foundation for data collaboration and no common, open data formats for various analytical scenarios such as BI, AI, Integration, Engineering, and Apps.

Mirroring in Fabric addresses these challenges by providing a seamless experience that accelerates the time-to-value for insights and decisions, and breaks down data silos between technology solutions. It offers near real-time replication of data into a SaaS data lake, with built-in analytics for BI and AI.

The Microsoft Fabric platform, built on a foundation of SaaS, simplifies and integrates data processes to a new level. Mirroring in Fabric creates three essential items in your Fabric workspace:
<p>

- Restricted and limited access to important, ever changing, data
- Friction between people, process, and technology
- Long wait times to create data pipelines and processes to critically important data
- No freedom to use the tools you need to analyze and share insights comfortably
- Lack of a proper foundation for folks to share and collaborate on data
- No common, open data formats for all analytical scenarios - BI, AI, Integration, Engineering, and even Apps

Furthermore, it supports a broad ecosystem of tools, including SQL Server Management Studio, Azure Data Studio, and GitHub Copilot. Sharing capabilities ensure ease of access control and secure decision-making across the organization.

Fabric offers three different approaches in bringing data into OneLake through mirroring.

- Database mirroring – Database mirroring in Microsoft Fabric allows replication of entire databases and tables, allowing you to bring data from various systems together into a single analytics platform.
- Metadata mirroring – Metadata mirroring in Fabric synchronizes metadata (such as catalog names, schemas, and tables) instead of physically moving the data. This approach leverages shortcuts, ensuring the data remains in its source while still being easily accessible within Fabric.
- Open mirroring – Open mirroring in Fabric is designed to extend mirroring based on open Delta Lake table format. This capability enables any developer to write their application's change data directly into a mirrored database item in Microsoft Fabric, based on the open mirroring approach and public APIs.

### Currently Available External Databases for Mirroring in Microsoft Fabric

| Platform                                                                 | Near Real-Time Replication | Type of Mirroring     | Tutorial                                                                 |
|--------------------------------------------------------------------------|-----------------------------|------------------------|--------------------------------------------------------------------------|
| Microsoft Fabric mirrored databases from Azure Cosmos DB (preview)      | Yes                         | Database mirroring     | <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/mirroring-azure-cosmos-db">Tutorial: Azure Cosmos DB</a> |
| Microsoft Fabric mirrored databases from Azure Databricks (preview)     | Yes                         | Metadata mirroring     | <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/mirroring-azure-databricks">Tutorial Azure Databricks</a> |
| Microsoft Fabric mirrored databases from Azure Database for PostgreSQL flexible server (preview) | Yes                         | Database mirroring     | <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-database-postgresql-tutorial">Tutorial: Azure Database for PostgrSQL flexible server</a> |
| Microsoft Fabric mirrored databases from Azure SQL Database             | Yes                         | Database mirroring     | <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/mirroring-azureric">Tutorial: Azure SQL Database</a> mirrored databases from Azure SQL Managed Instance (preview) | Yes                         | Database mirroring     | <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/mirroring-azure-sql-managed-instance">Tutorial Azure SQL Managed Instance</a> |
| Microsoft Fabric mirrored databases from Snowflake                      | Yes                         | Database mirroring     | <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/mirroring-snowflake">Tutorial: Snowflake</a> |
| Microsoft Fabric mirrored databases from SQL Server (preview)           | Yes                         | Database mirroring     | <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/sql-server-tutorial?tabs=sql201622">Tutorial: SQL Server</a>
| Open mirrored databases                                                 | Yes                         | Open mirroring         | <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/mirroring-open">Tutorial Open mirroring</a> |
| Microsoft Fabric mirrored databases from Fabric SQL database (preview)  | Yes                         | Database mirroring     | Automatically configured                                                |


<p style="border-bottom: 1px solid lightgrey;"></p>


## How does the near real time replication of database mirroring work?

Mirroring is enabled by creating a secure connection to your operational data source. You choose whether to replicate an entire database or individual tables and Mirroring will automatically keep your data in sync. Once set up, data will continuously replicate into the OneLake for analytics consumption.

The following are core tenets of Mirroring:

- Enabling Mirroring in Fabric is simple and intuitive, without having the need to create complex ETL pipelines, allocate other compute resources, and manage data movement.

- Mirroring in Fabric is a fully managed service, so you don't have to worry about hosting, maintaining, or managing replication of the mirrored connection.

- For a comprehensive introduction to troubleshooting mirroring concepts, please view the following video.:

     <p><a href="https://www.youtube.com/watch?v=I09E-0RlgNc"><img src="https://img.youtube.com/vi/I09E-0RlgNc/0.jpg"></a> 
     <p><a href="https://www.youtube.com/watch?v=YMWySj-x660"><img src="https://img.youtube.com/vi/YMWySj-x660/0.jpg"></a> 
     <p><a href="https://www.youtube.com/watch?v=wW6eLVnzO78"><img src="https://img.youtube.com/vi/wW6eLVnzO78/0.jpg"></a> 
    <p><a href="https://www.youtube.com/watch?v=K8xIVBMKfrc"><img src="https://img.youtube.com/vi/K8xIVBMKfrc/0.jpg"></a> 


## How does metadata mirroring work?

Mirroring not only enables data replication but can also be achieved through shortcuts or metadata mirroring rather than full data replication, allowing data to be available without physically moving or duplicating it. Mirroring in this context refers to replicating only metadata—such as catalog names, schemas, and tables—rather than the actual data itself. This approach enables Fabric to make data from different sources accessible without duplicating it, simplifying data management and minimizing storage needs.

For example, when accessing data registered in Unity Catalog, Fabric mirrors only the catalog structure from Azure Databricks, allowing the underlying data to be accessed through shortcuts. This method ensures that any changes in the source data are instantly reflected in Fabric without requiring data movement, maintaining real-time synchronization and enhancing efficiency in accessing up-to-date information.





## How does open mirroring work?

In addition to mirroring enabling data replication by creating a secure connection to your data source, you can also select an existing data provider or write your own application to land data into mirrored database. Once you create an open mirrored database via public API or via the Fabric portal, you will be able to obtain a landing zone URL in OneLake, where you can land change data per open mirroring specification.

Once data is in the landing zone with the proper format, replication will start running and manage the complexity of merging the changes with updates, insert, and delete to be reflected into delta tables. This method ensures that any data written into the landing zone will be immediately and keeping the data in Fabric up-to-date.

- For a comprehensive introduction to troubleshooting mirroring concepts, please view the following video:

<p><a href="https://www.youtube.com/watch?v=81M93gBYrlw"><img src="https://img.youtube.com/vi/81M93gBYrlw/0.jpg"></a> 

<p>

### Cost of mirroring

For database mirroring and open mirroring, the Fabric compute and OneLake storage are free up to a capacity-based limit.

- Storage for replicas is free up to a limit based on the capacity size. Mirroring offers a free terabyte of mirroring storage for every capacity unit (CU) you have purchased. For example, if you purchase an F64 capacity, you get 64 free terabytes worth of storage, exclusively used for mirroring. OneLake storage is billed if free Mirroring storage limit is exceeded, or when the capacity is paused. For more information, see Microsoft Fabric Pricing.

- Background Fabric compute used to replicate your data into Fabric OneLake is free and does not consume capacity. Requests directly to the OneLake for mirrored data consume capacity as normal OneLake compute consumption. The compute for querying data using SQL, Power BI, or Spark is charged at regular rates.

- A running Fabric capacity is required only for the initial setup of Mirroring.



<br>
<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Configure Fabric Mirrored Database</b></p>

<p><img src="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/media/azure-sql-database/fabric-mirroring-sql-database.svg" height = 400></p>

In this activity, you will learn how to Configure Microsoft Fabric mirrored databases from Azure SQL Database.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

Open the following reference and complete the steps you see there:

<a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-sql-database-tutorial"> Tutorial: Configure Microsoft Fabric mirrored databases from Azure SQL Database</a>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.3 Monitor Fabric mirrored database replication</h2>
<br></br>
Once the mirrored database is configured, you can monitor the current state of replication. The Monitor replication section shows you the database level status, and a list of tables under replication along with the corresponding status, total rows replicated, and the last completed time to refresh mirrored table from source.

<p>

<img src="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/media/monitor/monitor-mirrored-database.png#lightbox">

### Possible Replication Statuses

#### Database Level

| Status               | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| Running              | Replication is currently running, bringing snapshot and change data into OneLake. |
| Running with warning | Replication is running, but with transient errors.                          |
| Stopping/Stopped     | Replication has stopped.                                                    |
| Error                | Fatal error in replication that can't be recovered.                         |

#### Table Level

| Status               | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| Running              | Data is replicating.                                                        |
| Running with warning | Warning of nonfatal error with replication of the data from the table.      |
| Stopping/Stopped     | Replication has stopped.                                                    |
| Error                | Fatal error in replication for that table.                                  |


### Workspace monitoring

<a href="https://learn.microsoft.com/en-us/fabric/fundamentals/workspace-monitoring-overview">Workspace monitoring</a>, currently in preview, is an observability feature in Microsoft Fabric that enables developers and admins to access detailed logs and performance metrics of their workspaces.

Mirroring in Fabric supports operation logs in workspace monitoring to provide a more comprehensive monitoring experience for your mirrored databases. You can use these logs to monitor execution and performance of your mirrored database, including data replication, table changes, mirroring status, failures, and replication latency.

To get started, <a href="https://learn.microsoft.com/en-us/fabric/fundamentals/enable-workspace-monitoring">enable monitoring</a> in your workspace. Once the monitoring of your workspace is enabled, the mirrored database execution logs are automatically ingested into the MirroredDatabaseTableExecution table in the monitoring KQL database. To learn more about the available logs and the structure see <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/monitor-logs">Mirrored database operation logs</a>.

<p>
<img src="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/media/monitor/enable-workspace-monitoring.png#lightbox">
<p>
Then you have full access to an advanced monitoring experience for mirrored database:

Derive insights on-demand: Query the granular operation logs directly using KQL in the monitoring database to get instant access to the information you need.
<p>
<img src="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/media/monitor/monitor-query-mirrored-database-logs.png#lightbox">

<p style="border-bottom: 1px solid lightgrey;"></p>


<h2 id="5.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.4 Trouble shoot Fabric Mirrored database</h2>

<br></br>
As with any service, it is crucial to understand troubleshooting methods for anticipated issues. For detailed guidance on troubleshooting Mirroring services.
<p>

| Data Source                                             | Troubleshooting Link                                                                                      | FAQ Link                                                                                                 |
|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Azure SQL Database                                      | <a href="https://learn.microsoft.com/en-us/fabric/database/troubleshoot-mirroring-azure-sql-database">Troubleshoot Mirroring Azure SQL Database</a> | <a href="https://learn.microsoft.com/en-us/fabric/database/faq-azure-sql-database">FAQ about Mirroring Azure SQL Database</a> |
| Azure SQL Managed Instance                              | <a href="https://learn.microsoft.com/en-us/fabric/database/troubleshoot-mirroring-azure-sql-managed-instance">Troubleshoot Mirroring Azure SQL Managed Instance</a> | <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-sql-managed-instance-faq">FAQ about Mirroring Azure SQL Managed Instance</a>|
|Azure Database for PostgreSQL flexible server          | <a href="https://learn.microsoft.com/en-us/fabric/database/troubleshoot-mirroring-postgresql">Troubleshoot Mirroring Azure Database for PostgreSQL flexible server</a> | <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-database-postgresql-mirroring-faq">FAQ Mirroring Azure Database for PostgreSQL flexible server|
| Azure Cosmos DB                                         | <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-cosmos-db-troubleshooting">Troubleshoot Mirroring Azure Cosmos DB</a>| <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-cosmos-db-faq">FAQ Mirroring Azure Cosmos DB</a> |
| Snowflake                                               | <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/snowflake-mirroring-faq#troubleshoot-mirroring-snowflake-in-microsoft-fabric">Troubleshoot Mirroring Snowflake</a> |                            | 
|Azure Databricks | n/a | <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-databricks-faq">FAQ Mirroring Azure Databricks</a|
| Fabric SQL database (preview)                           | <a href="https://learn.microsoft.com/en-us/fabric/database/sql/mirroring-troubleshooting">Troubleshoot Mirroring Fabric SQL database</a> | <a href="https://learn.microsoft.com/en-us/fabric/database/sql/mirroring-faq">FAQ Mirroring Fabric SQL database(preview)</a>|
| SQL Server                                              | <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/sql-server-troubleshoot">Troubleshoot Fabric mirrored databases from SQL Server</a> | <a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/sql-server-faq">FAQ for Mirroring SQL Server in Microsoft Fabric</a> |



<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: Examine insights into common mirroring challenges</b></p>

<br></br>
The following video will discuss 5 errors that could prevent the use of technology for forklifting, locating changes, and migrating those changes from your OLTP database into Microsoft Fabric.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- For a comprehensive introduction to troubleshooting mirroring concepts, please view the following video.:

     <p><a href="https://www.youtube.com/watch?v=eID9cbAsdk0"><img src="https://img.youtube.com/vi/eID9cbAsdk0/0.jpg" height = 200></a> 

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
  <li><a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/explore" >Explore data in your mirrored database using Microsoft Fabric</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-cosmos-db" >Mirroring Azure Cosmos DB (Preview)</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-databricks" >Mirroring Azure Databricks Unity Catalog (Preview)</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/snowflake" >Mirroring Snowflake</a></li>
</ul>

<p style="border-bottom: 1px solid lightgrey;"></p>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/06%20-%20Real-Time%20Intelligence.md).
