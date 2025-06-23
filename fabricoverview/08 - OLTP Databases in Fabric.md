![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2> 08 - OLTP Databases In Microsoft Fabric </h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.


(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" >Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.) 

In this section you will learn about Fabric SQL Database & Cosmos DB in Microsoft Fabric 



You'll cover these topics in this Module on OLTP Databases in Microsoft Fabric:

<dl>

  <dt><a href="#8-1" >8.1 - Fabric SQL Database (preview)</a></dt>
  <dt><a href="#8-2" >8.2 - Cosmos DB in Microsoft Fabric (preview)</a></dt>



</dl>


<h2 id="8.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">8.1 Fabric SQL Database (preview)</h2>

The Fabric SQL Database is a core component of Microsoft Fabric that provides a fully managed, scalable, and performant SQL engine for analytics workloads. It enables users to query structured data using familiar T-SQL syntax while integrating seamlessly with other Fabric components like Lakehouse, Pipelines, and Power BI.


<img src="https://data-mozart.com/wp-content/uploads/2024/11/image-7-1024x501.png">


## Key Concepts

| Concept | Description |
|--------|-------------|
| **SQL Endpoint** | A TDS-compatible endpoint that allows external tools to connect via the SQL engine to the Fabric SQL Database. Fabric SQL database requires the endpoint connection and a specific database name|
| **SQL Analytics Endpoint** | A TDS-compatible endpoint that allows external tools to connect via the Polaris Engine to Fabric Warehouses, Lakehouses, and Database Mirrors. |
| **Fabric SQL database Mirror** | A mirrored replicated copy stored in delta lake accessable via the SQL Analytics Endpoint, automatically created when a Fabric SQL Database is created. |
| **Direct Lake Mode** | Enables Power BI to query Fabric SQL Database directly without data movement. |
| **Security** | Supports role-based access control, row-level security, and integration with Microsoft Entra ID. |

### Why use SQL database in Fabric?

SQL database in Fabric is part of the Database workload, and the data is accessible from other items in Fabric. Your SQL database data is also kept up-to-date in a queryable format in OneLake, so you can use all the different services in Fabric, such as running analytics with Spark, executing notebooks, data engineering, visualizing through Power BI Reports, and more.


<img src="https://learn.microsoft.com/en-us/fabric/database/sql/media/mirroring-overview/sql-database-in-fabric-mirroring.svg">

### Regional Availability
| Americas             | Europe                 | Middle East | Africa              | Asia Pacific         |
|----------------------|------------------------|-------------|---------------------|----------------------|
| Brazil South         | North Europe          | UAE North   | South Africa North  | Australia East       |
| Canada Central       | West Europe            |             |                     | Australia Southeast  |
| Canada East         | France Central         |             |                     | Central India        |
| Central US           | Germany West Central   |             |                     | East Asia            |
| East US              | Italy North           |             |                     | Japan East          |
| East US 2            | Norway East            |             |                     | Japan West          |
| North Central US     | Poland Central        |             |                     | Southeast Asia       |
| South Central US   | Sweden Central         |             |                     | South India          |
| West US              | Switzerland North      |             |                     | Korea Central        |
| West US 2            | Switzerland West      |             |                     |                      |
| West US 3           | UK South               |             |                     |                      |
|                      | UK West¹               |             |                     |                      |

¹ Fabric SQL database isn't available in this region  





### Connecting to Fabric SQL Database

In Microsoft Fabric, the SQL analytics endpoint and SQL database are accessible through a Tabular Data Stream, or TDS endpoint, familiar to all modern web applications that interact with a SQL Server TDS endpoint. This is referred to as the SQL connection string within the Microsoft Fabric user interface.

The connection string of the SQL database is similar to the connection string of Azure SQL Database, <server-unique-identifer>.database.windows.net. The SQL analytics endpoint connection string looks like <server-unique-identifier>.<tenant>.fabric.microsoft.com.

To find the SQL connection string for your Fabric SQL database:

- Go to the settings of your SQL database item.
- Or, in the item list, select the ... menu. Select Settings then Connection strings. Fabric provides complete connection strings for providers including ADO.NET, JDBC, ODBC, PHP, and Go.
- Or, select the Open in button and SQL Server Management Studio. The server connection information is displayed.

To find the SQL connection string for the SQL analytics endpoint of your Fabric SQL database:

- Go to the settings of your SQL database item, then select SQL endpoint.
- Or, select the ... menu, then select Copy SQL connection string.

You can easy connect to your SQL database with the Open in button in the Fabric portal query editor. Choose SQL Server Management Studio or the mssql extension with Visual Studio Code.

<img src="https://learn.microsoft.com/en-us/fabric/database/sql/media/connect/open-in-connect-button.png#lightbox">

***Connect with SQL Server Management Studio manually***
<img src="https://learn.microsoft.com/en-us/fabric/database/sql/media/connect/sql-server-management-studio-settings.png#lightbox">

In SQL Server Management Studio (SSMS):

1. From your workspace area in the Database workload of Fabric, select the ... next to your SQL database.
2. Select Settings.
3. Select Connection strings. Look for the connection string to your SQL database, including the Data Source=. For example, tcp:<servername>.database.fabric.microsoft.com,1433. The Initial Catalog= is the database name.
4. In SSMS, open a New connection.
5. From the Fabric dialog box, copy and paste the value from Server Name into the Server name.
6. Choose Authentication type: Microsoft Entra ID - Universal with MFA support.
7. Select Options<<.
8. Copy and paste the value from Database Name into the Connect to database text box.
9. Select Connect.
10. Sign in using Microsoft Entra ID - Universal with MFA support.

For more detailed information on connecting or migrating data to Fabric SQL Database view:

<a href="https://www.youtube.com/watch?v=aJ_ekT42WWs"><img src="https://img.youtube.com/vi/aJ_ekT42WWs/0.jpg" height = 200></a>

<p>

<a href="https://www.youtube.com/watch?v=Ae77yoGqqnM"><img src="https://img.youtube.com/vi/Ae77yoGqqnM/0.jpg" height = 200></a>


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: Work through the Data Catalog Tutorial</b></p>

In this activity, you will follow the basic training tutorial for a full life cycle tutorial for Fabric SQL Database.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

<p>

<img src="https://learn.microsoft.com/en-us/fabric/database/sql/media/tutorial-introduction/architecture-diagram.png">

- [Open the following reference, and follow all of the steps you see there.](https://learn.microsoft.com/en-us/fabric/database/sql/tutorial-create-database) 


<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="8-2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">8.2 - Cosmos DB in Microsoft Fabric (preview)</h2>

Cosmos DB in Microsoft Fabric is now in preview. Cosmos DB in Fabric makes it easy to build agentic AI apps, offering an AI-optimized database that is automatically configured to meet your application’s needs. It’s built on the high availability, dynamic scaling, and AI-ready capabilities of Azure Cosmos DB.

Building on the momentum from the launch of SQL database in Fabric, we are expanding databases workload in Fabric with this new addition. You can now store semi-structured NoSQL data in Cosmos DB in Fabric, alongside your relational data in SQL databases, enabling a unified data platform for your applications. This further positions Fabric as a complete data platform to handle all your organizational needs, from operational to analytics and BI.

<img src="https://dataplatformblogwebfd-d3h9cbawf0h8ecgf.b01.azurefd.net/wp-content/uploads/2025/05/image-of-cosmos-db-in-fabric-item.png">

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
  <li><a href="https://learn.microsoft.com/en-us/fabric/database/sql/overview">SQL database in Microsoft Fabric (Preview)</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/database/sql/faq">Frequently asked questions for SQL database in Microsoft Fabric (preview)</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/database/sql/feature-comparison-sql-database-fabric" >Features comparison: Azure SQL Database and SQL database in Microsoft Fabric (preview)</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/database/sql/decision-guide" >Microsoft Fabric decision guide: choose a SQL database</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/fundamentals/decision-guide-data-store?toc=%2Ffabric%2Fdatabase%2Ftoc.json&bc=%2Ffabric%2Fdatabase%2Ftoc.json" >Microsoft Fabric decision guide: choose a data store</a></li>
  <li><a href="https://blog.fabric.microsoft.com/en-us/blog/22987?ft=All" >Announcing Cosmos DB in Microsoft Fabric (Preview)</a></li>
</ul>

<p style="border-bottom: 1px solid lightgrey;"></p>


Congratulations! You have completed this workshop on *Microsoft Fabric for the Data Professional*. You now have the tools, assets, and processes you need to extrapolate this information into other applications.