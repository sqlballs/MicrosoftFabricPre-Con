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

Using Copilot in Power BI leverages the power of large language models into Power BI at every layer to help users get more done and create more value from their data. Using Copilot, you can simply describe the visuals and insights you’re looking for, and Copilot will do the rest.  

Users can create and tailor reports in seconds, generate and edit DAX calculations, create narrative summaries, and ask questions about their data, all in conversational language. With the ability to easily tailor the tone, scope, and style of narratives and add them seamlessly within reports, Power BI can also deliver data insights even more impactfully through easy-to-understand text summaries.

<a href="https://www.microsoft.com/en-us/videoplayer/embed/RW13t3E">Click here for a demo of the Fabric CoPilot</a>

Microsoft has released *quick measure* suggestions for DAX capability that helps analysts quickly create the code they need. 

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.2 Using SQL Server Management Studio</h2>

You can use  to SQL Server Management Studio (SSMS) to start at the Microsoft Fabric workspace and connect to a warehouse. First, you'll need your connection string. Navigate to your workspace, select the Warehouse, and select More options. Select Copy SQL connection string to copy the connection string to your clipboard.

![Connection String](https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/warehouse-copy-sql-connection-string.png#lightbox)

When you open SSMS, the Connect to Server window appears. If already open, you can connect manually by selecting Object Explorer > Connect > Database Engine.

![SSMS](https://learn.microsoft.com/en-us/fabric/data-warehouse/media/connectivity/connect-server-window.png#lightbox)

Once the Connect to Server window is open, paste the connection string copied from the previous section of this article into the Server name box. Select Connect and proceed with the appropriate credentials for authentication. Remember that only Azure Active Directory - MFA authentication is supported.

Once that  connection is established, Object Explorer displays the connected warehouse from the workspace and its respective tables and views, all of which are ready to be queried.

When connecting via SSMS (or Azure Data Studio), you see both a SQL Endpoint and Warehouse listed as warehouses, and it's difficult to differentiate between the two item types and their functionality. For this reason, we strongly encourage you to adopt a naming convention that allows you to easily distinguish between the two item types when you work in tools outside of the Microsoft Fabric portal experience.

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.3 Using Visual Studio Code</h2>

The Synapse VS Code extension supports a pro-developer experience for exploring Microsoft Fabric lakehouses, and authoring Fabric notebooks and Spark job definitions. Visual Studio Code is a one of the most popular lightweight source code editors; it runs on your desktop and is available for Windows, macOS, and Linux. By installing the Synapse VS Code extension, you can author, run, and debug your notebook and Spark job definition locally in VS Code. You can also post the code to the remote Spark compute in your Fabric workspace to run or debug. The extension also allows you to browse your lakehouse data, including tables and raw files, in VS Code.

**Prerequisites**

The prerequisites for the Synapse VS Code extension are:

- Java 1.8
- Conda
- Jupyter extension for VS Code

After you have installed the required software, you must update the operating system properties to referene the new packages.

*Windows*

- Add JAVA_HOME to the environment variables and point it to the directory where java 1.8 is installed.
- Add both %JAVA_HOME%/bin and the condabin subfolder of the Conda installation to the system path directory.

*macOS*
Run the conda.sh in the terminal:

- Open the terminal window, change the directory to the folder where conda is installed, then change to the subdirectory etc/profile.d. The subdirectory should contain a file named conda.sh.
- Execute source conda.sh.
- In the same terminal window, run sudo conda init.
- Type in Java --version. The version should be Java 1.8.

No you can install the extension and prepare your environment. In VS Code, search for Synapse VS Code in the VS Code extension marketplace and install the extension. (The extension is still under preview, so you need to select the prerelease version to install.)

After the extension installation is complete, restart VS Code. The icon for the extension is listed at the VS Code activity bar.

**Setting a local working directory**

To edit a notebook, you must have a local copy of the notebook content. The local working directory of the extension serves as the local root folder for all downloaded notebooks, even notebooks from different workspaces. By invoking the command Synapse:Set Local Work Folder, you can specify a folder as the local working directory for the extension. These are the steps:

- Sign in and out of your account
- From the VS Code command palette, enter the Synapse:Sign in command to sign in to the extension. A separate browser sign-in page appears.
- Enter your username and password.
- After you successfully sign in, your username will be displayed in the VS Code status bar to indicate that you're signed in.
- To sign out of the extension, enter the command Synapse: Sign off.

**Choose a workspace to work with**

To select a Fabric workspace, you must have a workspace created. If you don't have one, you can create one in the Fabric portal. Once you have a workspace, choose it by selecting the Select Workspace option. A list appears of all workspaces that you have access to; select the one you want from the list.

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

- [Click this reference, and follow all steps you see there](https://learn.microsoft.com/en-us/fabric/data-engineering/author-notebook-with-vs-code)

<h2 id="4.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.4 Using Command Line Tools</h2>

There are two CLI utilities used to interact with Service Fabric. Azure CLI is used to manage Azure resources, such as an Azure-hosted Service Fabric cluster. Service Fabric CLI is used to directly connect to the Service Fabric cluster (regardless of where it's hosted) and manage the cluster, applications, and services.

The Azure Service Fabric command-line interface (CLI) is a command-line utility for interacting with and managing Service Fabric entities. The Service Fabric CLI can be used with either Windows or Linux clusters. The Service Fabric CLI runs on any platform where Python is supported. 

**Prerequisites**

Prior to installation, make sure your environment has both Python and pip installed. The CLI supports Python versions 2.7 and 3.6+, with Python 3.x recommended.

**Select a cluster** 

Before you perform any operations, you must select a cluster to connect to. For example, to select and connect to the cluster with the name testcluster.com, run the following command:

````sfctl cluster select --endpoint http://testcluster.com:19080````

> **Warning**: Do not use unsecured Service Fabric clusters in a production environment.

The cluster endpoint must be prefixed by http or https. It must include the port for the HTTP gateway. The port and address are the same as the Service Fabric Explorer URL. For clusters that are secured with a certificate, you can specify a PEM-encoded certificate. The certificate can be specified as a single file or as a cert and a key pair. If it is a self-signed certificate that is not CA signed, you can pass the ````--no-verify option```` to bypass CA verification.

````sfctl cluster select --endpoint https://testsecurecluster.com:19080 --pem ./client.pem --no-verify````

**Basic operations** 

Cluster connection information persists across multiple Service Fabric CLI sessions. After you select a Service Fabric cluster, you can run any Service Fabric command on the cluster. For example, to get the Service Fabric cluster health state, use the following command:

````sfctl cluster health````

The command results in the following output:

````
{
  "aggregatedHealthState": "Ok",
  "applicationHealthStates": [
    {
      "aggregatedHealthState": "Ok",
      "name": "fabric:/System"
    }
  ],
  "healthEvents": [],
  "nodeHealthStates": [
    {
      "aggregatedHealthState": "Ok",
      "id": {
        "id": "66aa824a642124089ee474b398d06a57"
      },
      "name": "_Test_0"
    }
  ],
  "unhealthyEvaluations": []
}
````

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: TODO: Activity Name</b></p>

TODO: Activity Description and tasks

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>

TODO: Enter activity steps description with checkbox<p style="border-bottom: 1px solid lightgrey;"></p>

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