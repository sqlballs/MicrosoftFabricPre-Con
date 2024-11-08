![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop from Azure Data and the Fasttrack Team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>05 -  Mirroring in Fabric</h2>
<br></br>
In this module we will explore various data replication techniques using Mirroring in Fabric, which offers efficient and low-latency solutions. They will explore the process of integrating diverse data sources, such as Azure SQL Database, Azure Cosmos DB, and Snowflake, into a unified analytics platform, OneLake.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" >Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module on the User Experience:

<dl>
  <dt><a href="#5.1" >5.1 - What is Mirroing in Fabric?</a></dt>
  <dt><a href="#5.2" >5.2 - When to use Mirroing in Fabric</a></dt>
  <dt><a href="#5.3" >5.3 - Configure Microsoft Fabric mirrored databases from Azure SQL Database</a></dt>
  <dt><a href="#5.4" >5.4 - Furture of Mirroring in Fabric</a></dt>
  <dt><a href="#5.5" >5.5 - Trouble shoot Fabric mirrored database</a></dt>
</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.1 What is Mirroing in Fabric?</h2>
<br></br>

Mirroring in Fabric offers a low-cost and low-latency data replication solution, enabling seamless integration of data from various systems into a single analytics platform, OneLake. You can continuously replicate data from sources like Azure SQL Database, Azure Cosmos DB, Azure Databricks, and Snowflake.

Once the data is in OneLake, it becomes accessible in a queryable format, allowing the use of Fabric's diverse services, such as Spark analytics, notebook execution, data engineering, and Power BI Reports visualization. This solution offers an integrated, end-to-end product designed to simplify analytics and foster openness and collaboration, supporting the open-source Delta Lake table format.

Mirroring in Fabric accelerates the data integration process, providing a turnkey solution for creating data replicas in OneLake to meet all analytical needs.

</br>

<h2 id="5.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.2 - When to use Mirroing in Fabric</h2>
<br></br>

Today, many organizations face challenges with mission-critical operational or analytical data being isolated in silos, requiring complex ETL pipelines and business processes to access and work with this data. This situation leads to restricted access to important, constantly changing data, friction between people, processes, and technology, long wait times to create necessary data pipelines, and a lack of freedom to use preferred tools for analysis and sharing insights. Additionally, there is often no proper foundation for data collaboration and no common, open data formats for various analytical scenarios such as BI, AI, Integration, Engineering, and Apps.

Mirroring in Fabric addresses these challenges by providing a seamless experience that accelerates the time-to-value for insights and decisions, and breaks down data silos between technology solutions. It offers near real-time replication of data into a SaaS data lake, with built-in analytics for BI and AI.

The Microsoft Fabric platform, built on a foundation of SaaS, simplifies and integrates data processes to a new level. Mirroring in Fabric creates three essential items in your Fabric workspace:
1. **Data replication management**: Manages the replication of data into OneLake and converts it to Parquet in an analytics-ready format, enabling further data engineering and data science scenarios.
2. **SQL analytics endpoint**: Provides a SQL endpoint for querying and analyzing data.
3. **Default semantic model**: Establishes a semantic model for easier data interpretation.

Furthermore, it supports a broad ecosystem of tools, including SQL Server Management Studio, Azure Data Studio, and GitHub Copilot. Sharing capabilities ensure ease of access control and secure decision-making across the organization.

Currently, the following external databases are available:

| Platform | Near real-time replication | End-to-end tutorial |
|:--|:--|:--|
| [Microsoft Fabric mirrored databases from Azure Cosmos DB (preview)](azure-cosmos-db.md) | Yes | [Tutorial: Azure Cosmos DB](azure-cosmos-db-tutorial.md) |
| [Microsoft Fabric mirrored databases from Azure Databricks (preview)](azure-databricks.md) | Yes |[Tutorial: Azure Databricks](azure-databricks-tutorial.md) |
| [Microsoft Fabric mirrored databases from Azure SQL Database (preview)](azure-sql-database.md) | Yes | [Tutorial: Azure SQL Database](azure-sql-database-tutorial.md) |
| [Microsoft Fabric mirrored databases from Snowflake](snowflake.md) | Yes |[Tutorial: Snowflake](snowflake-tutorial.md) |


<<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: Enabling Mirroring in your tenant</b></p>

In this activity you will learn how to enable Mirroring within your tenant.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- Follow the steps within the provided link. 
<a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/overview#how-do-i-enable-mirroring-in-my-tenant">How do I enable Mirroring in my tenant?</a>


<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.3 Configure Microsoft Fabric mirrored databases from Azure SQL Database</h2>
<br></br>
In this tutorial, you will learn about Mirroring in Fabric, an enterprise, cloud-based, zero-ETL, SaaS technology. Specifically, you will learn how to create a mirrored Azure SQL Database, which results in a read-only, continuously replicated copy of your Azure SQL Database data in OneLake.

<br><br>
<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Configure Fabric Mirrored Database</b></p>

<p><img src="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/media/azure-sql-database/fabric-mirroring-sql-database.svg" height = 400></p>

In this activity, you will learn how to Configure Microsoft Fabric mirrored databases from Azure SQL Database.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

Open the following reference and complete the steps you see there:

<a href="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/azure-sql-database-tutorial"> Tutorial: Configure Microsoft Fabric mirrored databases from Azure SQL Database</a>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.4 Furture of Mirroring in Fabric</h2>

Need to determine what information we want to place here when it comes to the future of Mirroring in Fabric 

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="5.5"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">5.5 Trouble shoot Fabric mirrored database</h2>

Add information and link to Brads Trouble Shooting video as a self guided 

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
  <li><a href="https://learn.microsoft.com/en-us/azure/data-explorer/kusto/query/?context=/fabric/context/context-rta&pivots=fabric" >Kusto Query Overview</a></li>
</ul>

<p style="border-bottom: 1px solid lightgrey;"></p>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/06%20-%20Microsoft%20Fabric%20DevOps.md).
