![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft workshop from the SQL Server team</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>04 - The Fabric Developer Experience</h2>

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
  <dt><a href="#46-using-visual-studio-code" target="_blank">4.6 - Using Visual Studio Code</a></dt>
  <dt><a href="#47-using-power-bi" target="_blank">4.7 - Using Power BI</a></dt>

</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.1 Using Co-Pilot</h2>

Copilot is a new feature in Power BI that harnesses the power of large language models to help users create value from their data using natural language. Users can simply describe their desired visuals and insights, and Copilot will generate them automatically, without requiring any manual input.

Copilot also enables users to easily and quickly create and customize reports, write and edit DAX formulas, produce narrative summaries, and query their data in a conversational way. Users can tailor the tone, scope, and style of the narratives and integrate them into their reports for more effective data communication through clear and concise text.

![Connection String](https://powerbiblogscdn.azureedge.net/wp-content/uploads/2023/05/AZ_Trident-PBi-D365-Blog-Hero-1200x628.png")


Microsoft has released *quick measure* suggestions for DAX capability that helps analysts quickly create the code they need. 

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png">
<b>Activity: Learn more about how Copilot works with Power BI </b></p>

To learn more about how Copilot works with Power BI, please select the link below. This link will take you to a video demonstration of Copilot in action, as well as a tutorial on how to get started with Copilot & Power BI. 

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Open the following reference in another tab](https://www.microsoft.com/en-us/videoplayer/embed/RW13t3E), to watch video demonstration of Copilot and Power BI in action. 

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.2 Using SQL Server Management Studio</h2>

SSMS (SQL Server Management Studio) is a graphical tool that allows you to manage and query data from SQL Server databases. Fabric is a cloud-based data platform that enables you to create and manage data warehouses and lakehouses. A lakehouse is a hybrid of a data warehouse and a data lake, which combines the best features of both. SSMS can connect to Fabric lakehouse SQL endpoints, which are interfaces that allow you to run SQL queries on the data stored in Fabric.

The following paragraphs describe how to use SQL Server Management Studio (SSMS) to connect to a warehouse from the Microsoft Fabric workspace.

 First, you need to obtain your connection string, which is a sequence of characters that specifies how to connect to the warehouse. To do this, go to your workspace, select the Warehouse, and click on More options. Then, choose Copy SQL connection string and paste it somewhere convenient.

[//]: #(https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/warehouse-copy-sql-connection-string.png#lightbox)

Next, you need to launch SSMS and enter the connection string in the Connect to Server dialog box. Click on Connect to establish the connection. After that, you can query and manage your warehouse data using SSMS. This is a simple and efficient way to access your warehouse data from the Microsoft Fabric workspace.

[//]: #(https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/object-explorer-connect-menu.png#lightbox)

In the Connect to Server dialog box, paste the SQL connection string from the Fabric user interface into the Server name box. The connection string should look something like this: fabric://<fabric-name>.sql.<region>.azure.com:1433/<database-name>.

Once the Connect to Server window is open, paste the connection string copied from the previous section of this article into the Server name box. Select Connect and proceed with the appropriate credentials for authentication. Remember that only Azure Active Directory - MFA authentication is supported.

![SSMS](https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/connect-server-window.png#lightbox)

Once that  connection is established, Object Explorer displays the connected warehouse from the workspace and its respective tables and views, all of which are ready to be queried.

![SSMS](https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/object-explorer-example.png#lightbox)

When connecting via SSMS (or Azure Data Studio), you see both a SQL Endpoint and Warehouse listed as warehouses, and it's difficult to differentiate between the two item types and their functionality. For this reason, we strongly encourage you to adopt a naming convention that allows you to easily distinguish between the two item types when you work in tools outside of the Microsoft Fabric portal experience.


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Connecting to your Fabric Workspace using SSMS.</b></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

To learn how to connect SSMS to Microsoft Fabric, please select the link below. This link will take you to a tutorial that explains how to retrieve the SQL connection string from your Microsoft Fabric workspace, and how to use it to establish a connection in SSMS. You will also see how to explore and query the data objects in your Microsoft Fabric environment using SSMS.

- <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity">Click here for a demo on how to connect to Microsoft Fabric with SSMS.</a>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://youtu.be/iDLTj-tCLdY?si=tv0t9MO7ptx0W_Ud" target="_blank"> Connect to Microsoft Fabric with 5 Tools</a></li>
</ul>

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/iDLTj-tCLdY/0.jpg)](https://www.youtube.com/watch?v=iDLTj-tCLdY)

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.3 Using Azure Data Studio</h2>

<h2 id="4.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.4 Using Microsoft Excel</h2>

<h2 id="4.5"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.5 Using OneLake File Explorer</h2>

<h2 id="4.6"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.6 Using Visual Studio Code</h2>

Using Visual Studio Code with Microsoft Fabric is a great way to develop and deploy applications for the cloud. Visual Studio Code is a free, open source, and cross-platform code editor that supports multiple languages and runtimes, such as C#, Java, Python, and .NET. Microsoft Fabric is an all-in-one analytics solution for enterprises that covers everything from data movement to data science, real-time analytics, and business intelligence. It offers a comprehensive suite of services, including data lake, data engineering, and data integration, all in one place.

The Synapse VS Code extension enables a seamless and productive developer experience for exploring Microsoft Fabric lakehouses, and creating Fabric notebooks and Spark job definitions

Visual Studio Code is a widely used and lightweight source code editor that runs on your desktop and supports Windows, macOS, and Linux platforms. With the Synapse VS Code extension, you can create, execute, and debug your notebook and Spark job definition locally in VS Code. You can also submit the code to the remote Spark compute in your Fabric workspace for running or debugging. Moreover, the extension enables you to browse your lakehouse data, including tables and raw files, in VS Code.

**Prerequisites**

The prerequisites for the Synapse VS Code extension are:

- Java 1.8
- Conda
- Jupyter extension for VS Code

After you have installed the required software, you must update the operating system properties to reference the new packages.

**Windows**

1. Add JAVA_HOME to the environment variables and point it to the directory where java 1.8 is installed.

2. Add both %JAVA_HOME%/bin and the condabin subfolder of the Conda installation to the system path directory.

**macOS**
Run the conda.sh in the terminal:

1. Open the terminal window, change the directory to the folder where conda is installed, then change to the subdirectory etc/profile.d. The subdirectory should contain a file named conda.sh.
2. Execute source conda.sh.
3. In the same terminal window, run sudo conda init.
4. Type in Java --version. The version should be Java 1.8.

**Install the extension and prepare your environment**

1. In VS Code, search for Synapse VS Code in the VS Code extension marketplace and install the extension. (The extension is still under preview, so you need to select the prerelease version to install.)
2. After the extension installation is complete, restart VS Code. The icon for the extension is listed at the VS Code activity bar.

**Setting a local working directory**

To edit a notebook, you must have a local copy of the notebook content. The local working directory of the extension serves as the local root folder for all downloaded notebooks, even notebooks from different workspaces. By invoking the command Synapse:Set Local Work Folder, you can specify a folder as the local working directory for the extension. These are the steps:

- Sign in and out of your account
- From the VS Code command palette, enter the Synapse:Sign in command to sign in to the extension. A separate browser sign-in page appears.
- Enter your username and password.
- After you successfully sign in, your username will be displayed in the VS Code status bar to indicate that you're signed in.
![vscsignin](https://learn.microsoft.com/en-us/fabric/data-engineering/media/vscode/signin-status.png)
- To sign out of the extension, enter the command Synapse: Sign off.

**Choose a workspace to work with**

To select a Fabric workspace, you must have a workspace created. If you don't have one, you can create one in the Fabric portal. Once you have a workspace, choose it by selecting the Select Workspace option. A list appears of all workspaces that you have access to; select the one you want from the list.
 
**Considerations and limitations**
- SQL Authentication is not supported.
- Multiple Active Result Sets (MARS) is unsupported for Microsoft Fabric Warehouse. MARS is disabled by default, however if MultipleActiveResultSets is included in the connection string, it should be removed or set to false.
- On connection to a warehouse, you may receive an error that "The token size exceeded the maximum allowed payload size". This may be due to having a large number of warehouses within the workspace or being a member of a large number of Azure AD groups. For most users, the error typically would not occur until approaching beyond 80 warehouses in the workspace. In event of this error, work with the Workspace admin to clean up unused Warehouses and retry the connection, or contact support if the problem persists.

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Connect to Microsoft Fabric using Visual Studio Code</b></p>

To learn how to connect VS Code to Microsoft Fabric, please select the link below.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>
- <a href="https://learn.microsoft.com/en-us/fabric/data-engineering/setup-vs-code-extension">What is the Synapse Visual Studio Code extension.</a>

<p></p>

The following video shows us how to connect Visual Studio Code to our Microsoft Fabric Workspace and then how to interact with an existing Notebook so we can interface with our Lakehouse & Spark:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/0tODoHLXhMc/0.jpg)](https://www.youtube.com/watch?v=0tODoHLXhMc&ab)

<b></b>
<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/author-notebook-with-vs-code" target="_blank">Microsoft Fabric notebook experience in VS Code</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/author-notebook-resource-with-vs-code" target="_blank">Microsoft Fabric notebook resource in VS Code</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/author-sjd-with-vs-code" target="_blank">Spark job definition experience in VS Code</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/explore-lakehouse-with-vs-code" target="_blank">Explore Microsoft Fabric lakehouses in VS Code</a></li>

</ul>

<p style="border-bottom: 1px solid lightgrey;"></p>



<h2 id="4.7"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.7 Using Power BI</h2>

Power BI natively and fully supports a Warehouse or Lakehouse SQL Endpoint as a data source, eliminating the need for the SQL Connection string. The Data Hub provides direct access to all of the warehouses that you have permissions for.

![pbimf](https://learn.microsoft.com/en-us/power-bi/fundamentals/media/fabric-get-started/configure-connection.png)


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Connect to Fabric with Power BI users</b></p>

In this tutorial, you learn how to use Dataflows Gen2 and Pipelines to ingest data into a Lakehouse and create a dimensional model. You also learn how to generate a beautiful report automatically to display the latest sales figures from start to finish in just 45 minutes.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

Select the link below for a tutorial on getting started with Power BI in Fabric. 

- <a href="https://learn.microsoft.com/en-us/power-bi/fundamentals/fabric-get-started">Connecting to Microsoft Fabric with Power BI.</a>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://learn.microsoft.com/en-us/fabric/cicd/cicd-tutorial" target="_blank">End to end lifecycle management tutorial</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/cicd/git-integration/git-get-started?tabs=commit-to-git" target="_blank">Get started with git integration</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/cicd/deployment-pipelines/get-started-with-deployment-pipelines" target="_blank">Get started with deployment pipelines</a></li>
</ul>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/05%20-%20The%20Fabric%20User%20Experience.md).
