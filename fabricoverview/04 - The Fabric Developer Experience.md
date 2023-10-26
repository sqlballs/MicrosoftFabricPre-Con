![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft workshop from the SQL Server team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>04 - The Fabric Developer Experience</h2>
<br></br>
In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution using the Microsoft Fabric platform.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" target="_blank">Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module on the Developer Experience:

<dl>

  <dt><a href="#41-using-co-pilot" target="_blank">4.1 - Using Co-Pilot</a></dt>
  <dt><a href="#42-using-sql-server-management-studio" target="_blank">4.2 - Using SQL Server Management Studio</a></dt>
  <dt><a href="#43-using-azure-data-studio" target="_blank">4.3 - Using Azure Data Studio</a></dt>
  <dt><a href="#44-using-microsoft-excel" target="_blank">4.4 - Using Microsoft Excel</a></dt>
  <dt><a href="#45-using-onelake-file-explorer" target="_blank">4.5 - Using OneLake File Explorer</a></dt>
  <dt><a href="#46-using-kusto-explorer" target="_blank">4.6 - Using Kusto Explorer</a></dt>
  <dt><a href="#47-using-visual-studio-code" target="_blank">4.7 - Using Visual Studio Code</a></dt>
  <dt><a href="#48-using-power-bi" target="_blank">4.8 - Using Power BI</a></dt>

</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.1 Using Co-Pilot</h2>
<br></br>
Copilot is a new feature in Power BI that harnesses the power of large language models to help users create value from their data using natural language. Users can simply describe their desired visuals and insights, and Copilot will generate them automatically, without requiring any manual input.


Copilot also enables users to easily and quickly create and customize reports, write and edit DAX formulas, produce narrative summaries, and query their data in a conversational way. Users can tailor the tone, scope, and style of the narratives and integrate them into their reports for more effective data communication through clear and concise text.

<img src="https://powerbiblogscdn.azureedge.net/wp-content/uploads/2023/05/AZ_Trident-PBi-D365-Blog-Hero-1200x628.png" height = 400> 


Microsoft has released *quick measure* suggestions for DAX capability that helps analysts quickly create the code they need. 

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png">
<b>Self-Guided Activity: Learn more about how Copilot works with Power BI </b></p>
<br>
</br>To learn more about how Copilot works with Power BI, please select the link below. This link will take you to a video demonstration of Copilot in action, as well as a tutorial on how to get started with Copilot & Power BI. 
</br>
</br>
<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><br><b>Steps</b></br></p>

- Open this reference to see how to access Copilot in Power BI Desktop

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/4fJq8qessuM/0.jpg)](https://www.youtube.com/watch?v=4fJq8qessuM)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.2 Using SQL Server Management Studio</h2>
<br></br>

SSMS (SQL Server Management Studio) is a graphical tool that allows you to manage and query data from SQL Server databases. Fabric is a cloud-based data platform that enables you to create and manage data warehouses and lakehouses. A lakehouse is a hybrid of a data warehouse and a data lake, which combines the best features of both. SSMS can connect to Fabric lakehouse SQL endpoints, which are interfaces that allow you to run SQL queries on the data stored in Fabric.

The following paragraphs describe how to use SQL Server Management Studio (SSMS) to connect to a warehouse from the Microsoft Fabric workspace.

 First, you need to obtain your connection string, which is a sequence of characters that specifies how to connect to the warehouse. To do this, go to your workspace, select the Warehouse, and click on More options. Then, choose Copy SQL connection string and paste it somewhere convenient.

<img src="https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/warehouse-copy-sql-connection-string.png#lightbox" height = 400> 


Next, you need to launch SSMS and enter the connection string in the Connect to Server dialog box. Click on Connect to establish the connection. After that, you can query and manage your warehouse data using SSMS. This is a simple and efficient way to access your warehouse data from the Microsoft Fabric workspace.

[//]: #(https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/object-explorer-connect-menu.png#lightbox)

In the Connect to Server dialog box, paste the SQL connection string from the Fabric user interface into the Server name box. The connection string should look something like this: fabric://<fabric-name>.sql.<region>.azure.com:1433/<database-name>.

Once the Connect to Server window is open, paste the connection string copied from the previous section of this article into the Server name box. Select Connect and proceed with the appropriate credentials for authentication. Remember that only Azure Active Directory - MFA authentication is supported.

<img src="https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/connect-server-window.png#lightbox" height = 400> 

Once that  connection is established, Object Explorer displays the connected warehouse from the workspace and its respective tables and views, all of which are ready to be queried.

<img src="https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/object-explorer-example.png#lightbox" height = 400> 

When connecting via SSMS (or Azure Data Studio), you see both a SQL Endpoint and Warehouse listed as warehouses, and it's difficult to differentiate between the two item types and their functionality. For this reason, we strongly encourage you to adopt a naming convention that allows you to easily distinguish between the two item types when you work in tools outside of the Microsoft Fabric portal experience.

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png">
<b>Self-Guided Activity: Connecting to your Fabric Workspace using SSMS.</b></p>
<br>
</br>Learn how to get SQL connection string from workspace and connect SSMS. Learn how to query and explore data objects in Microsoft Fabric with SSMS. 
</br>
</br>
<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><br><b>Steps</b></br></p>

- [Open this reference and follow the steps you see there](https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity#get-started-with-sql-server-management-studio-ssms)
-  Open this reference to see an example of how to connect to Microsoft Fabric with SSMS click the following link.

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/iDLTj-tCLdY/0.jpg)](https://www.youtube.com/watch?v=iDLTj-tCLdY&t=63s)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.3 Using Azure Data Studio</h2>
<br></br>

Azure Data Studio is a versatile tool for working with data from various sources, such as SQL Server, Azure SQL Database, Azure Synapse, Microsoft Fabric, and more. It enables you to query, design, and manage your databases and data warehouses on-premises or in the cloud. Azure Data Studio is free, open-source, and cross-platform, so you can run it on Windows, macOS, or Linux. It also supports multiple languages, such as SQL, PowerShell, Python, KQL, Apache Spark, and PySpark. Azure Data Studio has a modern and intuitive interface that features a query editor, native Jupyter Notebooks, an integrated terminal, and built-in Git support. You can also enhance your environment with extensions that offer new features and services for Azure Data Studio. Some of the popular extensions are Database Projects, GitHub Copilot, Oracle to Azure SQL Migration Assistant, PostgreSQL Migration Assistant, and more. You can explore more extensions in the extension library or create your own. Azure Data Studio is designed to simplify the data landscape and provide a unified tooling experience for data professionals.

<img src="https://learn.microsoft.com/en-us/azure-data-studio/media/quickstart-sql-database/new-connection-icon.png" height = 400> 

Prerequisites: Before you can set up a connection, the following prerequisites are required:
- A Microsoft Fabric tenant account with an active subscription.
- A Microsoft Fabric enabled Workspace.

Retrieve the SQL connection string: Navigate to your workspace, select the Warehouse, and select More options. Select Copy SQL connection string to copy the connection string to your clipboard.

<img src="https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/warehouse-copy-sql-connection-string.png#lightbox" height = 400> 

Open Azure Data Studio. If already open, you can connect manually by selecting Object Explorer > Connect > Database Engine. Once the Connect to Server window is open, paste the connection string copied from the previous step into the Server name box. Select Connect and proceed with the appropriate credentials for authentication.

<img src="https://learn.microsoft.com/en-us/azure-data-studio/media/azure-view/azure-connection-configuration.png" height = 400> 

**_note_** For the server you will be using the SQL connection string copied to the clipboard. It will look similair to the following : xxxxxxxxxx-xxxxxxxxxx.xxxx-datawarehouse.pbidedicated.windows.net


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png">
<b>Self-Guided Activity: Using Azure Data Studio to access Microsoft Fabric.</b></p>
<br>
</br>Using Azure Data Studio to Explore and manage Azure SQL resources.
</br>
</br>
<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><br><b>Steps</b></br></p>

-  Open this reference to see an example of how to connect to Microsoft Fabric with Azure Data Studio click the following link.

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/iDLTj-tCLdY/0.jpg)](https://www.youtube.com/watch?v=iDLTj-tCLdY&t=127s)

</br>
<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.4 Using Microsoft Excel</h2>
<br></br>

Microsoft Excel is a software program that allows you to create, edit, and analyze spreadsheets and data. It is part of the Microsoft 365 suite of productivity tools, or it can be purchased separately. You can use Excel to organize your data in rows and columns, perform calculations with formulas and functions, create charts and graphs to visualize your data, and share your work with others. Excel also supports various languages and data types, such as SQL, Python, KQL, and Power BI.

In the menu bar at the top of the page, select the Data tab, select Get Data, select From Azure, and then select From Azure SQL Database.

<img src="https://learn.microsoft.com/en-us/azure/azure-sql/database/media/connect-excel/excel_data_source.png?view=azuresql" height = 400> 

In the SQL Server database dialog box, type the Server name you want to connect to in the form xxxxxxxxxx-xxxxxxxxxx.xxxx-datawarehouse.pbidedicated.windows.net. Enter in the name of your data warehouse. Select OK to open the credentials window.

<img src="https://learn.microsoft.com/en-us/azure/azure-sql/database/media/connect-excel/server-name.png?view=azuresql" height = 400> 

In the SQL Server database dialog box, select Microsoft Account on the left side, and then login with your Microsoft Credentials which have access to Microsoft Fabric. Select Connect to open the Navigator.


<img src="https://learn.microsoft.com/en-us/azure/azure-sql/database/media/connect-excel/connect-to-server.png?view=azuresql" height = 400> 

<br></br>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png">
<b>Self-Guided Activity: Using Microsoft Excel to access Microsoft Fabric.</b></p>
<br>
</br>Using Microsoft Excel to access Microsoft Fabric. 

</br>
</br>
<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><br><b>Steps</b></br></p>

- Open this reference and follow the steps you see there
For an example of how to connect to Microsoft Fabric with Microsoft Excel click the following link.

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/iDLTj-tCLdY/0.jpg)](https://www.youtube.com/watch?v=iDLTj-tCLdY&t=279s)


<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.5"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.5 Using OneLake File Explorer</h2> 
<br></br>
  
The OneLake file explorer application enables a seamless integration of OneLake with Windows File Explorer. It synchronizes all OneLake items that you have access to in Windows File Explorer automatically. Synchronization means updating the metadata of files and folders to reflect the latest changes, and uploading the local modifications to the OneLake service.

- To stop OneLake from launching on Windows startup, go to Task Manager > Startup apps, right-click OneLake and choose Disable
- To launch OneLake manually, use Windows search (Windows+S) and click on OneLake. The app will refresh your synced folders automatically.
- To exit OneLake, right-click the OneLake icon on the taskbar, and choose Exit. The sync will pause, and you won't be able to access placeholders. You will still see the blue cloud icon for placeholders that were not downloaded.

<img src="https://learn.microsoft.com/en-us/fabric/onelake/media/onelake-file-explorer/onelake-file-explorer-screen-v-2.png#lightbox" height = 400> 

When you create, update, or delete a file via Windows File Explorer, it automatically syncs the changes to OneLake service. Updates to your item made outside of your File Explorer aren't automatically synced. To pull these updates, you need to right-click on the item or subfolder in Windows File Explorer and select Sync from OneLake.

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png">
<b>Self-Guided Activity: Use OneLake file explorer to access Fabrc data.</b></p>
<br>
</br>Using OneLake file explorer to access, edit, and upload to Fabric data.
</br>
</br>
<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><br><b>Steps</b></br></p>

- [Open this reference and follow the steps you see there](https://learn.microsoft.com/en-us/fabric/onelake/onelake-file-explorer)
- For an example of how to install and use OneLake Explorer watch the following video

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/4NbuG1JBq60/0.jpg)](https://www.youtube.com/watch?v=4NbuG1JBq60)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.6"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.6 Using Kusto Explorer</h2>
<br></br>

A Desktop Application for Data Exploration with Kusto Query Language. Kusto.Explorer is a robust Windows desktop application that empowers users to delve into their data using the Kusto Query Language, all within an intuitive and user-friendly interface.

-   Use search mode to quickly find data in your tables and visualize the results.
-   Use query mode to write and execute complex queries using the Kusto Query Language syntax and features.
-   Share your queries with others by copying or exporting them as files or URLs.
-   Manage your clusters, databases, and tables by viewing their properties, creating new ones, or deleting existing ones.

<img src="https://learn.microsoft.com/en-us/azure/data-explorer/kusto/tools/images/kusto-explorer/ke-start.png" height = 400> 

The Connections pane shows all the configured cluster connections. For each cluster the databases, tables, and attributes (columns) that they store are shown. Select items (which sets an implicit context for the search/query in the main panel), or double-click items to copy the name to the search/query panel.

<img src="https://learn.microsoft.com/en-us/azure/data-explorer/kusto/tools/images/kusto-explorer/connections-panel.png" height = 400> 

</br>
<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png">
<b>Self-Guided Activity: Installation and using Kusto.Explorer.</b></p>
<br>
</br>Installation and Usage of Kusto.Explorer Desktop Application.
</br>
</br>
<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><br><b>Steps</b></br></p>

- [Open this reference and follow the steps you see there](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/tools/kusto-explorer#connections-panel) 
- [Open this reference and follow the steps you see there](https://learn.microsoft.com/en-us/azure/data-explorer/kusto/tools/kusto-explorer-using) 
- For an example of how to use Kutso Explorer to connect to Microsoft Fabric watch the following video

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/iDLTj-tCLdY/0.jpg)](https://youtu.be/iDLTj-tCLdY?t=186)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.7"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.7 Using Visual Studio Code</h2>
<br></br>

Using Visual Studio Code with Microsoft Fabric is a great way to develop and deploy applications for the cloud. Visual Studio Code is a free, open source, and cross-platform code editor that supports multiple languages and runtimes, such as C#, Java, Python, and .NET. Microsoft Fabric is an all-in-one analytics solution for enterprises that covers everything from data movement to data science, real-time analytics, and business intelligence. It offers a comprehensive suite of services, including data lake, data engineering, and data integration, all in one place.

The Synapse VS Code extension enables a seamless and productive developer experience for exploring Microsoft Fabric lakehouses, and creating Fabric notebooks and Spark job definitions

Visual Studio Code is a widely used and lightweight source code editor that runs on your desktop and supports Windows, macOS, and Linux platforms. With the Synapse VS Code extension, you can create, execute, and debug your notebook and Spark job definition locally in VS Code. You can also submit the code to the remote Spark compute in your Fabric workspace for running or debugging. Moreover, the extension enables you to browse your lakehouse data, including tables and raw files, in VS Code.

<img src="https://learn.microsoft.com/en-us/fabric/data-engineering/media/vscode/list-notebook.png" height = 400> 

**Considerations and limitations**
- SQL Authentication is not supported.
- Multiple Active Result Sets (MARS) is unsupported for Microsoft Fabric Warehouse. MARS is disabled by default, however if MultipleActiveResultSets is included in the connection string, it should be removed or set to false.
- On connection to a warehouse, you may receive an error that "The token size exceeded the maximum allowed payload size". This may be due to having a large number of warehouses within the workspace or being a member of a large number of Azure AD groups. For most users, the error typically would not occur until approaching beyond 80 warehouses in the workspace. In event of this error, work with the Workspace admin to clean up unused Warehouses and retry the connection, or contact support if the problem persists.

</br>
<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png">
<b>Self-Guided Activity: Connect to Microsoft Fabric using Visual Studio Code.</b></p>
<br>
</br>Learn how to connect VS Code to Microsoft Fabric.
</br>
</br>
<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><br><b>Steps</b></br></p>

- [Open this reference and follow the steps you see there](https://learn.microsoft.com/en-us/fabric/data-engineering/setup-vs-code-extension) 

- Open this reference to see how to access Microsoft Fabric with Visual Studio Code

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/0tODoHLXhMc/0.jpg)](https://www.youtube.com/watch?v=0tODoHLXhMc&ab)


<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.8"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.8 Using Power BI</h2>
<br></br>

Microsoft Fabric lets you create reusable and default Power BI datasets to create reports in various ways in Power BI. This article describes the various ways you can use your Warehouse or SQL Endpoint, and their default Power BI datasets, to create reports.

For example, you can establish a live connection to a shared dataset in the Power BI service and create many different reports from the same dataset. You can create a data model in Power BI Desktop and publish to the Power BI service. Then, you and others can create multiple reports in separate .pbix files from that common data model and save them to different workspaces.

Advanced users can build reports from a warehouse using a composite model or using the SQL connection string.

Power BI natively and fully supports a Warehouse or Lakehouse SQL Endpoint as a data source, eliminating the need for the SQL Connection string. The Data Hub provides direct access to all of the warehouses that you have permissions for.

<img src="https://learn.microsoft.com/en-us/power-bi/fundamentals/media/fabric-get-started/configure-connection.png" height = 400> 


</br>
<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png">
<b>Self-Guided Activity: Create reports using Power BI Desktop.</b></p>
<br>
</br>You can build reports from datasets with Power BI Desktop using a Live connection to the default dataset. For information on how to make the connection, see connect to datasets from Power BI Desktop.
</br>
</br>
<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><br><b>Steps</b></br></p>

- [Open this reference and follow the steps you see there](https://learn.microsoft.com/en-us/fabric/data-warehouse/create-reports#create-reports-using-power-bi-desktop) 
- For an example of how to use Power BI to connect to Microsoft Fabric watch the following video

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/iDLTj-tCLdY/0.jpg)](https://www.youtube.com/watch?v=iDLTj-tCLdY&t=329s)

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><br><b>For Further Study</b></br></p>
<ul>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/author-notebook-with-vs-code" target="_blank">Microsoft Fabric notebook experience in VS Code</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/author-notebook-resource-with-vs-code" target="_blank">Microsoft Fabric notebook resource in VS Code</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/author-sjd-with-vs-code" target="_blank">Spark job definition experience in VS Code</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/explore-lakehouse-with-vs-code" target="_blank">Explore Microsoft Fabric lakehouses in VS Code</a></li>



   
   <li><a href="https://www.youtube.com/watch?v=0tODoHLXhMc&ab" target="_blank"> Microsoft Fabric, VS Code, Notebooks, & Spark! Set it up, connect to a Workspace, EDIT, & Upload!! </a></li>


</ul>

<b></b>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/05%20-%20The%20Fabric%20User%20Experience.md).
