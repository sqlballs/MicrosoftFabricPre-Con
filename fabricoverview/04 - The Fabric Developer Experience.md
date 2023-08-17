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

  <dt><a href="#4.1" target="_blank">4.1 - Using Co-Pilot</a></dt>
  <dt><a href="#4.2" target="_blank">4.2 - Using SQL Server Management Studio</a></dt>
  <dt><a href="#4.3" target="_blank">4.3 - Using Visual Studio Code</a></dt>
  <dt><a href="#4.4" target="_blank">4.4 - Using Command Line Tools</a></dt>
  <dt><a href="#4.5" target="_blank">4.5 - Development Best Practices</a></dt>

</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.1 Using Co-Pilot</h2>

Copilot is a new feature in Power BI that harnesses the power of large language models to help users create value from their data using natural language. Users can simply describe their desired visuals and insights, and Copilot will generate them automatically, without requiring any manual input.

Copilot also enables users to easily and quickly create and customize reports, write and edit DAX formulas, produce narrative summaries, and query their data in a conversational way. Users can tailor the tone, scope, and style of the narratives and integrate them into their reports for more effective data communication through clear and concise text.

![Connection String](https://powerbiblogscdn.azureedge.net/wp-content/uploads/2023/05/AZ_Trident-PBi-D365-Blog-Hero-1200x628.png")


Microsoft has released *quick measure* suggestions for DAX capability that helps analysts quickly create the code they need. 

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Integrating Co-pilot with Power BI </b></p>

TODO: Select the link below to see the how Microsoft has integrated Copilot into Power BI.


<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox
- [ ] <a href="https://www.microsoft.com/en-us/videoplayer/embed/RW13t3E">Click here for a demo of the Fabric CoPilot</a>

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


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Connecting to your Fabric Workspace using SSMS.  

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Follow instructions in the TODO link provided to connect SSMS to Farbic Workspace with SSMS. 
- [ ] <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/connectivity">Click here for a demo on how to connect to Microsoft Fabric with SSMS.</a>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://www.youtube.com/@Tales-from-the-Field" target="_blank"> "Insert Brads TFTF Video Here on ways to connect"</a></li>
</ul>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.3 Using Visual Studio Code</h2>

Using Visual Studio Code with Microsoft Fabric is a great way to develop and deploy applications for the cloud. Visual Studio Code is a free, open source, and cross-platform code editor that supports multiple languages and runtimes, such as C#, Java, Python, and .NET. Microsoft Fabric is an all-in-one analytics solution for enterprises that covers everything from data movement to data science, real-time analytics, and business intelligence. It offers a comprehensive suite of services, including data lake, data engineering, and data integration, all in one place.

The Synapse VS Code extension enables a seamless and productive developer experience for exploring Microsoft Fabric lakehouses, and creating Fabric notebooks and Spark job definitions

Visual Studio Code is a widely used and lightweight source code editor that runs on your desktop and supports Windows, macOS, and Linux platforms. With the Synapse VS Code extension, you can create, execute, and debug your notebook and Spark job definition locally in VS Code. You can also submit the code to the remote Spark compute in your Fabric workspace for running or debugging. Moreover, the extension enables you to browse your lakehouse data, including tables and raw files, in VS Code.

**Prerequisites**

The prerequisites for the Synapse VS Code extension are:

- Java 1.8
- Conda
- Jupyter extension for VS Code

After you have installed the required software, you must update the operating system properties to referene the new packages.

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

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Connect to Microsoft Fabric using Visual Studio Code</b></p>

TODO:  Follow instructions in the TODO link provided for Visual Studio Code connection overview.
- [ ] <a href="https://learn.microsoft.com/en-us/fabric/data-engineering/setup-vs-code-extension">What is the Synapse Visual Studio Code extension.</a>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/author-notebook-with-vs-code" target="_blank">"Microsoft Fabric notebook experience in VS Code"</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/author-notebook-resource-with-vs-code" target="_blank">"Microsoft Fabric notebook resource in VS Code</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/author-sjd-with-vs-code" target="_blank">"Spark job definition experience in VS Code</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/explore-lakehouse-with-vs-code" target="_blank">"Explore Microsoft Fabric lakehouses in VS Code</a></li>

</ul>

<p style="border-bottom: 1px solid lightgrey;"></p>



<h2 id="4.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.4 Connecting with Power BI</h2>

Power BI natively and fully supports a Warehouse or Lakehouse SQL Endpoint as a data source, eliminating the need for the SQL Connection string. The Data Hub provides direct access to all of the warehouses that you have permissions for.

![pbimf](https://learn.microsoft.com/en-us/power-bi/fundamentals/media/fabric-get-started/configure-connection.png)


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Fabric for Power BI users</b></p>

TODO: In this tutorial, you learn how to use Dataflows Gen2 and Pipelines to ingest data into a Lakehouse and create a dimensional model.
 You also learn how to generate a beautiful report automatically to display the latest sales figures from start to finish in just 45 minutes.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Follow instructions in the TODO link to learn how to connect Power BI to Microsoft Fabric.<p style="border-bottom: 1px solid lightgrey;"></p>

- [ ] <a href="https://learn.microsoft.com/en-us/power-bi/fundamentals/fabric-get-started">Connecting to Microsoft Fabric with Power BI.</a>

<h2 id="4.5"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.5 Development Best Practices</h2>

Apart from standard developer best-practices, there are some additional considerations for the Microsoft Fabric developer. You can use this section as a template, and add or alter best practices as you learn more and as your organization's requirements dictate. This is not an exhaustive list, so the exercise that follows will explore more suggestions in a team setting. 

**Back up your work into a git repository**

With git integration, any developer can back up their work by committing it into git. To do this properly in Fabric, here are some basic rules:

- Make sure you have an isolated environment to work in, so others don’t override your work before it gets committed. This means working in a Desktop tool (such as VSCode, Power BI Desktop or others), or in a separate workspace that other users can’t access.
- Commit to a branch that you created and no other developer is using. If you’re using a workspace as an authoring environment, read about working with branches.
- Commit together changes that must be deployed together. This advice applies for a single item, or multiple items that are related to the same change. Committing all related changes together can help you later when deploying to other stages, creating pull requests, or reverting changes back.
- Big commits might hit a max commit size limit. Be mindful of the number of items you commit together, or the general size of an item. For example, reports can grow large when adding large images. It’s bad practice to store large-size items in source control systems, even if it works. Consider ways to reduce the size of your items if they have lots of static resources, like images.

**Rolling back changes**

After backing up your work, there might be cases where you want to revert to a previous version and restore it in the workspace. There are a few options for this:

- Undo button: The Undo operation is an easy and fast way to revert the immediate changes you made, as long as they are not committed yet. You can also undo each item separately. Read more about the undo operation.
- Reverting to older commits: There’s no direct way to go back to a previous commit in the UI. The best option is to promote an older commit to be the HEAD using git revert or git reset. Doing this will show that there’s an update in the source control pane, and you can update the workspace with that new commit.

As data isn’t stored in git, consider that reverting a data item to an older version might break the existing data and could possible require you to drop the data or the operation might fail. Check this in advance before reverting changes back.

**Working with a private workspace**

When you want to work in isolation, use a separate workspace as an isolated environment. Read more about this in working with branches. For an optimal workflow for you and the team, consider the following:

- Setting up the workspace: Before you start, make sure you can create a new workspace (if you don’t already have one), that you can assign it to a Fabric capacity, and that you have access to data to work in your workspace.
- Creating a new branch: Create a new branch from the main branch, so you’ll have the most up-to-date version of your content. Also make sure you connect to the correct folder in the branch, so you can pull the right content into the workspace.
- Small, frequent changes: It's a git best practice to make small incremental changes that are easy to merge and less likely to get into conflicts. If that’s not possible, make sure to update your branch from main so you can resolve conflicts on your own first.
- Configuration changes: If necessary, change the configurations in your workspace to help you work more productively. Some changes can include connection between items, or to different data sources or changes to parameters on a given item. Just remember that anything you commit will be part of the commit and can accidentally be merged into the main branch.

**Use Client tools to edit your work**

For items and tools that support it, it might be easier to work with client tools for authoring, such as Power BI Desktop for datasets and reports, VSCode for Notebooks etc. These tools can be your local development environment. After you complete your work, push the changes into the remote repo, and sync the workspace to upload the changes. Just make sure you are working with the supported structure of the item you are authoring. If you’re not sure, first clone a repo with content already synced to a workspace, then start authoring from there, where the structure is already in place.

**Managing workspaces and branches**

Since a workspace can only be connected to a single branch at a time, it is recommended to treat this as a 1:1 mapping. However, to reduce the amount of workspace it entails, consider these options:

- If a developer set up a private workspace with all required configurations, they can continue to use that workspace for any future branch they create. When a sprint is over, your changes are merged and you are starting a fresh new task, just switch the connection to a new branch on the same workspace. You can also do this if you suddenly need to fix a bug in the middle of a sprint. Think of it as a working directory on the web.
- Developers using a client tool (such as VSCode, Power BI Desktop or others), don’t necessarily need a workspace. They can create branches and commit changes to that branch locally, push those to the remote repo and create a pull request to the main branch, all without a workspace. A workspace is needed only as a testing environment to check that everything works in a real-life scenario. It's up to you to decide when that should happen.

**Test**

This section provides guidance for working with a deployment pipelines test stage.

*Simulate your production environment*

It’s important to see how your change will impact the production stage. A deployment pipelines test stage allows you to simulate a real production environment for testing purposes. Alternatively, you can simulate this by connecting git to an additional workspace.

Make sure that these three factors are addressed in your test environment:

- Data volume
- Usage volume
- A similar capacity as in production

When testing, you can use the same capacity as the production stage. However, using the same capacity can make production unstable during load testing. To avoid unstable production, test using a different capacity similar in resources to the production capacity. To avoid extra costs, use a capacity where you can pay only for the testing time.

*Use deployment rules with a real-life data source*

If you're using the test stage to simulate real life data usage, it's recommended to separate the development and test data sources. The development database should be relatively small, and the test database should be as similar as possible to the production database. Use data source rules to switch data sources in the test stage or parameterize the connection if not working through deployment pipelines.

*Check related items*

Changes you make can also affect the dependent items. During testing, verify that your changes don’t affect or break the performance of existing items, which can be dependent on the updated ones. You can easily find the related items by using impact analysis.

*Updating data items*

Data items are items that store data. The item’s definition in git defines how the data is stored. When updating an item in the workspace, we are importing its definition into the workspace and applying it on the existing data. The operation of updating data items is the same for git and deployment pipelines.

As different items have different capabilities when it comes to retaining data when changes to the definition are applied, be mindful when applying the changes. Some practices that can help you apply the changes in the safest way:

- Know in advance what the changes are and what their impact might be on the existing data. Use commit messages to describe the changes made.
- Upload the changes first to a dev or test environment, to see how that item handles the change with test data.
- If everything goes well, it’s recommended to also check it on a staging environment, with real-life data (or as close to it as possible), to minimize the unexpected behaviors in production.
- Consider the best timing when updating the Prod environment to minimize the damage that any errors might cause to your business users who consume the data.
- After deployment, post-deployment tests in Prod to verify that everything is working as expected.

Some changes will always be considered breaking changes. Hopefully, the preceding steps will help you track them before production. Build a plan for how to apply the changes in Prod and recover the data to get back to normal state and minimize downtime for business users.

*Test your app*

If you're distributing content to your customers through an app, review the app's new version before it's in production. Since each deployment pipeline stage has its own workspace, you can easily publish and update apps for development and test stages. Publishing and updating apps allows you to test the app from an end user's point of view.

> **Important:** The deployment process doesn't include updating the app content or settings. To apply changes to content or settings, manually update the app in the required pipeline stage.

**Production**

This section provides guidance to the deployment pipelines production stage.

*Manage who can deploy to production*

Because deploying to production should be handled carefully, it's good practice to let only specific people manage this sensitive operation. However, you probably want all BI creators for a specific workspace to have access to the pipeline. Use production workspace permissions to manage access permissions. Other users can have a production workspace viewer role to see content in the workspace but not make changes from git or deployment pipelines.

In addition, limit access to the repo or pipeline by only enabling permissions to users that are part of the content creation process.

*Set rules to ensure production stage availability*

Deployment rules are a powerful way to ensure the data in production is always connected and available to users. With deployment rules applied, deployments can run while you have the assurance that customers can see the relevant information without disturbance. Make sure that you set production deployment rules for data sources and parameters defined in the dataset.

*Update the production app*

Deployment in a pipeline updates the workspace content, but it can also update the associated app through the deployment pipelines API. It's not possible to update the app through the UI. You need to update the app manually. If you use an app for content distribution, don’t forget to update the app after deploying to production so that end users are immediately able to use the latest version.

*Deploying into production using git branches*

As the repo serves as the ‘single-source-of-truth’, some teams might want to deploy updates into different stages directly from git. This is possible with git integration, with a few considerations:

- It’s recommended to use release branches. You will be required to continuously change the connection of workspace to the new release branches before every deployment.
- If your build or release pipeline requires you to change the source code, or run scripts in a build environment before deployment to the workspace, then connecting the workspace to git won't help you.
- After deploying to each stage, make sure to change all the configuration specific to that stage.

*Quick fixes to content*

Sometimes there are issues in production that require a quick fix. Deploying a fix without testing it first is bad practice. Therefore, always implement the fix in the development stage and push it to the rest of the deployment pipeline stages. Deploying to the development stage allows you to check that the fix works before deploying it to production. Deploying across the pipeline takes only a few minutes.

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

Team discussion of further best practices.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox
<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
    <li><a href="https://learn.microsoft.com/en-us/azure/service-fabric/service-fabric-develop-csharp-applications-with-vs-code" target="_blank">Develop C# Service Fabric applications with Visual Studio Code</a></li>
</ul>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/05%20-%20The%20Fabric%20User%20Experience.md).