![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop from Azure Data and the Fasttrack Team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="03"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png">03 - Data Warehouse and Data Integration</h2>

In this workshop we will cover using Microsoft Fabric to implement a complete Analytics solution.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" >Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this module:

<dl>
  <dt><a href="#3.1">3.1 - Creating a Data Warehouse</a></dt>
  <dt><a href="#3.2">3.2 - Ingest and Transform Data with Fabric Data Factory</a></dt>
  <dt><a href="#3.3">3.3 - Data Engineering with Fabric Data Warehouse</a></dt>
</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="3.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">3.1 Creating a Data Warehouse</h2>

Microsoft Fabric is a next-generation data warehousing solution within Microsoft Fabric.

The lake-centric warehouse is built on an enterprise grade distributed processing engine that enables industry leading performance at scale while minimizing the need for configuration and management. Living in the data lake and designed to natively support open data formats, Fabric data warehouse enables seamless collaboration between data engineers and business users without compromising security or governance.

The easy-to-use SaaS experience is also tightly integrated with Power BI for easy analysis and reporting, converging the world of data lakes and warehouses and greatly simplifying an organizations investment in their analytics estate.

Data warehouse customers benefit from:
- Data stored in Delta-parquet format enables ACID transactions and interoperability with other Fabric workloads means you don't need multiple copies of data.
- Cross database queries can use multiple data sources for fast insights with zero data duplication.
- Easily ingest, load and transform data at scale through Pipelines, Dataflows, cross database query or the COPY INTO command.
- Autonomous workload management with industry-leading distributed query processing engine means no knobs to turn to achieve best in class performance.
- Scale near instantaneously to meet business demands. Storage and compute are separated.
- Reduced time to insights with an easily consumable, always connected semantic model that is integrated with Power BI in Direct Lake mode. Reports always have the most recent data for analysis and reporting.
- Built for any skill level, from the citizen developer to DBA or data engineer.

<p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/761b96fa-4e30-43d1-8ffe-d34650599be2" height = 400>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Creating your first data warehouse</b></p>

In this activity, you will follow the data warehouse tutorial to create a data warehouse in your workspace.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- Open the following reference in another tab, [Tutorial: Create a Warehouse in Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-create-warehouse)
  - Complete all steps on this page of the the tutorial.
 
 You can also right-click this link to open it in another tab and review this video that introduces you to these concepts:

 <p><a href="https://www.youtube.com/watch?v=StIBBb69wDw"><img src="https://img.youtube.com/vi/StIBBb69wDw/0.jpg" height = 200></a> 

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="3.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">3.2 Ingest and Transform Data with Fabric Data Factory</h2>

Data Factory empowers you with a modern data integration experience to ingest, prepare and transform data from a rich set of data sources (for example, databases, data warehouse, Lakehouse, real-time data, and more). Whether you are a citizen or professional developer, you will be able to transform the data with intelligent transformations and leverage a rich set of activities. We can create pipelines to execute one or more activities, access data sources or services through linked services, and after creating a pipeline, we can add triggers to automatically run our processes at specific times or in response to changing scenarios. With Data Factory in Microsoft Fabric, we are bringing fast copy (data movement) capabilities to both dataflows and data pipelines. With Fast Copy, you can move data between your favorite data stores blazing fast. Most importantly, Fast Copy enables you to bring data to your Lakehouse and Data Warehouse in Microsoft Fabric for analytics.

There are two primary high-level features Data Factory implements: dataflows and pipelines.

<h3>Data Pipelines</h3>

Data pipelines enable powerful workflow capabilities at cloud-scale. With data pipelines, you can build complex workflows that can refresh your dataflow, move PB-size data, and define sophisticated control flow pipelines.

Use data pipelines to build complex ETL and data factory workflows that can perform many different tasks at scale. Control flow capabilities are built into data pipelines that allow you to build workflow logic, which provides loops and conditionals.

Add a configuration-driven copy activity together with your low-code dataflow refresh in a single pipeline for an end-to-end ETL data pipeline. You can even add code-first activities for Spark Notebooks, SQL scripts, stored procs, and more.

<p><img src="https://learn.microsoft.com/en-us/fabric/data-factory/media/data-factory-overview/data-pipelines.png" height = 300></p>

<br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Ingest data into the data warehouse</b></p>

In this activity, you will follow the data warehouse tutorial to load a data warehouse using a pipeline copy activity.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- In Microsoft Fabric, navigate to the workspace view then open the following reference in another tab, [Tutorial: Ingest data into a Warehouse in Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-ingest-data)
  - Complete steps 2 through 25.

<p style="border-bottom: 1px solid lightgrey;"></p>

<h3>Dataflows</h3>

Dataflows provide a low-code interface for ingesting data from hundreds of data sources, transforming your data using 300+ data transformations. You can then load the resulting data into multiple destinations, such as Azure SQL databases and more. Dataflows can be run repeatedly using manual or scheduled refresh, or as part of a data pipeline orchestration.

Dataflows are built using the familiar Power Query experience that's available today across several Microsoft products and services such as Excel, Power BI, Power Platform, Dynamics 365 Insights applications, and more. Power Query empowers all users, from citizen to professional data integrators, to perform data ingestion and data transformations across their data estate. Perform joins, aggregations, data cleansing, custom transformations, and much more all from an easy-to-use, highly visual, low-code UI.

<p><img src="https://learn.microsoft.com/en-us/fabric/data-factory/media/data-factory-overview/dataflow-experience.png" height = 300></p>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: Create your first dataflow to get and transform data</b></p>

In this activity, you will follow the basic training tutorial for ingestingd data using Dataflows Gen2.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- Open the following reference in another tab and complete all steps, [Quickstart: Create your first dataflow to get and transform data](https://learn.microsoft.com/en-us/fabric/data-factory/create-first-dataflow-gen2)
- Right-click this link to open it in another tab and review this video that introduces you to these concepts:

<p><a href="https://www.youtube.com/watch?v=0jSTd2P20pk"><img src="https://img.youtube.com/vi/0jSTd2P20pk/0.jpg" height = 200></a> 


<h2 id="3.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">3.3 Data Engineering with Fabric Data Warehouse</h2>

Data Warehousing in Microsoft Fabric is a T-SQL based experience which means you can leverage many of the features that you may be accustomed to using in SQL Server, such as:

<h3><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/tables" >Create Tables</a></h3>

   Creating a table in Fabric is a remarkably similar process to creating a table in SQL Server. You can initiate a new query within the Fabric editor or SQL Server Management Studio (SSMS) and execute the 'create table' script, which will result in the table's creation within Microsoft Fabric.

```sql
DROP TABLE IF EXISTS [dbo].[dimension_city];
CREATE TABLE [dbo].[dimension_city]
    (
        [CityKey] [int] NULL,
        [WWICityID] [int] NULL,
        [City] [varchar](8000) NULL,
        [StateProvince] [varchar](8000) NULL,
        [Country] [varchar](8000) NULL,
        [Continent] [varchar](8000) NULL,
        [SalesTerritory] [varchar](8000) NULL,
        [Region] [varchar](8000) NULL,
        [Subregion] [varchar](8000) NULL,
        [Location] [varchar](8000) NULL,
        [LatestRecordedPopulation] [bigint] NULL,
        [ValidFrom] [datetime2](6) NULL,
        [ValidTo] [datetime2](6) NULL,
        [LineageKey] [int] NULL
    );
```

<h3><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/ingest-data-copy" >Load data using T-SQL</a></h3>

Loading data into your newly created table is a straightforward process. You can achieve this with ease by utilizing the COPY INTO T-SQL statement. This statement allows you to efficiently load data into your tables.

```sql
COPY INTO [dbo].[dimension_city]
FROM 'https://fabrictutorialdata.blob.core.windows.net/sampledata/WideWorldImportersDW/tables/dimension_city.parquet'
WITH (FILE_TYPE = 'PARQUET');
```

<h3><a href="https://learn.microsoft.com/en-us/sql/t-sql/statements/create-table-as-clone-of-transact-sql" >Clone a table using T-SQL</a></h3>

Microsoft Fabric offers the capability to create near-instantaneous zero-copy clones with minimal storage costs.

- Table clones facilitate development and testing processes by creating copies of tables in lower environments.
- Table clones provide consistent reporting and zero-copy duplication of datasets for analytical workloads and machine learning modeling and testing.
- Table clones provide the capability of data recovery in the event of a failed release or data corruption by retaining the previous state of data.

```sql
-- Create a clone of the dbo.dimension_city table.
CREATE TABLE [dbo].[dimension_city1] AS CLONE OF [dbo].[dimension_city];

-- Create a clone of the dbo.fact_sale table.
CREATE TABLE [dbo].[fact_sale1] AS CLONE OF [dbo].[fact_sale];
```

You can also right-click this link to open it in another tab and review this video that introduces you to these concepts:

<p><a href="https://www.youtube.com/watch?v=-VXiEEIS2wc"><img src="https://img.youtube.com/vi/-VXiEEIS2wc/0.jpg" height=200>

<h3><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-transform-data" >Transform data using stored procedure</a></h3>

For SQL users, the availability of stored procedures is a valuable feature, and Microsoft Fabric supports them in a way that aligns with your familiarity. Writing stored procedures in Fabric follows the same approach as you would in SQL Server, making it convenient for users to leverage this important SQL functionality. The data can be transformed using Stored procedures.

```sql
-- Drop the stored procedure if it already exists.
DROP PROCEDURE IF EXISTS [dbo].[populate_aggregate_sale_by_city]
GO

-- Create the populate_aggregate_sale_by_city stored procedure.
CREATE PROCEDURE [dbo].[populate_aggregate_sale_by_city]
AS
BEGIN
    -- If the aggregate table already exists, drop it. Then create the table.
    DROP TABLE IF EXISTS [dbo].[aggregate_sale_by_date_city];
    CREATE TABLE [dbo].[aggregate_sale_by_date_city]
        (
            [Date] [DATETIME2](6),
            [City] [VARCHAR](8000),
            [StateProvince] [VARCHAR](8000),
            [SalesTerritory] [VARCHAR](8000),
            [SumOfTotalExcludingTax] [DECIMAL](38,2),
            [SumOfTaxAmount] [DECIMAL](38,6),
            [SumOfTotalIncludingTax] [DECIMAL](38,6),
            [SumOfProfit] [DECIMAL](38,2)
        );

    -- Reload the aggregated dataset to the table.
    INSERT INTO [dbo].[aggregate_sale_by_date_city]
    SELECT
        FS.[InvoiceDateKey] AS [Date], 
        DC.[City], 
        DC.[StateProvince], 
        DC.[SalesTerritory], 
        SUM(FS.[TotalExcludingTax]) AS [SumOfTotalExcludingTax], 
        SUM(FS.[TaxAmount]) AS [SumOfTaxAmount], 
        SUM(FS.[TotalIncludingTax]) AS [SumOfTotalIncludingTax], 
        SUM(FS.[Profit]) AS [SumOfProfit]
    FROM [dbo].[fact_sale] AS FS
    INNER JOIN [dbo].[dimension_city] AS DC
        ON FS.[CityKey] = DC.[CityKey]
    GROUP BY
        FS.[InvoiceDateKey],
        DC.[City], 
        DC.[StateProvince], 
        DC.[SalesTerritory]
    ORDER BY 
        FS.[InvoiceDateKey], 
        DC.[StateProvince], 
        DC.[City];
END

-- Execute the stored procedure to create the aggregate table.
EXEC [dbo].[populate_aggregate_sale_by_city];
```

<h3><a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-visual-query" >Create a query with the visual query builder</a></h3>

Microsoft Fabric is designed with user-friendliness in mind, catering to individuals who may not be proficient in writing SQL queries. You have the option to utilize the Visual Query Builder, a graphical interface that simplifies the process of building queries. By merely dragging and dropping fields, the query builder will seamlessly generate the necessary SQL query in the background. This feature makes data retrieval and manipulation more accessible for a broader range of users.

<p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/d39a994d-815b-44c3-bef5-4a24d5ab0ab6" height = 60>

<br> 

<p><img src="https://github.com/sqlballs/MicrosoftFabricPre-Con/assets/45181391/5b87b205-64c8-4293-b063-9bbcb49ecc24" height = 400>

<br> 

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: SQL Experience</b></p>

In this activity, you will follow the data warehouse tutorial to create and load tables and transform data using T-SQL.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- Open the data warehouse created in section 3.1 then open the following reference in another tab, [Tutorial: Create tables in a data warehouse](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-create-tables)
  - Follow steps 4 through 11.
- Open the data warehouse created in section 3.1 then open the following reference in another tab, [Tutorial: Load data using T-SQL](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-load-data)
  - Follow steps 1 through 8.
- Open the data warehouse created in section 3.1 then open the following reference in another tab, [Tutorial: Transform data using a stored procedure](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-transform-data)
  - Follow steps 1 through 16.
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

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/Final-Branch/fabricoverview/04%20-%20The%20Lakehouse.md).
