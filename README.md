![](graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop</i>


### https://aka.ms/fabricdata

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="https://raw.githubusercontent.com/microsoft/sqlworkshops/master/graphics/textbubble.png"> <h2>About this Workshop</h2>

Welcome to this Microsoft solutions workshop on Microsoft Fabric for the Data Professional. Microsoft Fabric is an end-to-end analytics solution with full-service capabilities including data movement, data lakes, data engineering, data integration, data science, real-time analytics, and business intelligence—all backed by a shared platform providing robust data security, governance, and compliance.

In this workshop, you'll learn what the Microsoft Fabric platform is, the various services and components it contains, how to create, use and manage a deployment, from the point of view of the data professional.

The focus of this workshop is to understand how to use Microsoft Fabric in a solution, focusing on the data aspects of the platform. 

You'll start with an introduction to Microsoft Fabric, move on to understanding Workspaces, user security, and data governance. From there you'll learn about the Data Lakehouse, and then understand the developer and user experience of Microsoft Fabric. You'll end with a section on the DevOps of a Microsoft Fabric solution, with a focus on how to extrapolate what you have learned to create other solutions for your organization.

This github README.MD file explains how the workshop is laid out, what you will learn, and the technologies you will use in this solution. To download this Lab to your local computer, click the **Clone or Download** button you see at the top right side of this page. [More about that process is here](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository). 

You can view all of the [Workshops and other workshops our team has created at this link - open in a new tab to find out more.](https://microsoft.github.io/sqlworkshops/)

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="https://raw.githubusercontent.com/microsoft/sqlworkshops/master/graphics/checkmark.png"> <h3>Learning Objectives</h3>

In this workshop you'll cover these topics:

- Introduction and Overview:	Introduction of the Workshop, Basic Concepts, Services, Roles, Benchmarks. Verification of pre-requisites
- Data Warehouse and Data Integration:	Understanding and creating Workspaces, creating a Data Warehouse, connecting and managing, ingesting data with pipelines and data flows
- The Data Lakehouse:	Creating a Lakehouse, Linking data, using Spark to create new data sets in the Lakehouse
- The Fabric Developer Experience:	Using Co-Pilot, SSMS, VS Code, and development best-practices
- Real-Time Analytics with Microsoft Fabric: Working with Azure Data Explorer in Microsoft Fabric, Working with Fabric and Streaming / Event Data, and Working with Fabric and the Kusto Query Language (KQL)
- Microsoft Fabric DevOps: Design, Sizing, Monitoring and Management, Source Control, and the EXPLAIN command.

The goal of this workshop is to train the data professional to get an overview on how to determine when to implement a Microsoft Fabric solution, how to design the solution, implement it, use it, and manage, monitor and maintain it.

In each *Module*, you will find *Sections* that have topics, concepts and technologies that you will cover throughout the Workshop. You will also find various *Activities* where you willwork through hands-on steps to learn the material. You will also see *Self-Guided Activities* that you should complete after an in-person experience, or along the way if you are taking this Workshop directly from this GitHub repository. 

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="https://raw.githubusercontent.com/microsoft/sqlworkshops/master/graphics/listcheck.png"> <h2>Technologies used in this Workshop</h2>

The solution includes the following technologies - although you are not limited to these, they form the basis of the workshop. At the end of the workshop you will learn how to extrapolate these components into other solutions. You will cover these at an overview level, with references to much deeper training provided.

 <table style="tr:nth-child(even) {background-color: #f2f2f2;}; text-align: left; display: table; border-collapse: collapse; border-spacing: 2px; border-color: gray;">

  <tr><th style="background-color: #1b20a1; color: white;">Technology</th> <th style="background-color: #1b20a1; color: white;">Description</th></tr>

  <tr><td>OneLake</td><td>Serves as the foundation storage layer for all other services, and as a Data Lake.</td></tr>
  <tr><td>Data Factory</td><td>A fully scheduled cloud service for data pipelines.</td></tr>
  <tr><td>Synapse</td><td>The primary Data Lake, Data Warehouse, Data Science, and Data Analytics distributed processing system for the platform.</td></tr>
  <tr><td>Microsoft Power BI</td><td>Closest-to-user interface for data analysis.</td></tr>

</table>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="https://raw.githubusercontent.com/microsoft/sqlworkshops/master/graphics/owl.png"> <h2>Before Taking this Workshop</h2>

You'll need a local system that you are able to install software on. The workshop demonstrations use Microsoft Windows as an operating system and all examples use Windows for the workshop. Optionally, you can use a Microsoft Azure Virtual Machine (VM) to install the software on and work with the solution.

- You must have a Microsoft Azure account with the ability to create assets.
- You will need a laptop to work through the examples, access the workshop materials, and take notes.

This workshop expects that you understand data architectures, working with large data sets, data security, data analysis, and data pipelines.

If you are new to these, here are a few references you can complete prior to class:

-  [Big Data Architectures](https://learn.microsoft.com/en-us/azure/architecture/data-guide/big-data/)
-  [Pipelines](https://learn.microsoft.com/en-us/azure/architecture/data-guide/technology-choices/pipeline-orchestration-data-movement)
-  [Data Security](https://learn.microsoft.com/en-us/azure/architecture/data-guide/scenarios/securing-data-solutions)
-  [Data Analysis](https://learn.microsoft.com/en-us/azure/architecture/solution-ideas/articles/analytics-start-here)

<img style="float: left; margin: 0px 15px 15px 0px;" src="https://raw.githubusercontent.com/microsoft/sqlworkshops/master/graphics/bulletlist.png"> <h3>Setup</h3>

<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" >A full pre-requisites document is located here</a>. These instructions should be completed before the workshop starts, since you will not have time to cover these in class. <i>Remember to turn off any Virtual Machines from the Azure Portal when not taking the class so that you do incur charges (shutting down the machine in the VM itself is not sufficient)</i>.

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="https://raw.githubusercontent.com/microsoft/sqlworkshops/master/graphics/pinmap.png"> <h2>Related Workshops</h2>

 - [You can find a full Learning Path on Microsoft Fabric from Microsoft Learn at this reference](https://learn.microsoft.com/en-us/training/paths/get-started-fabric/?WT.mc_id=DP-MVP-5004032)

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="https://raw.githubusercontent.com/microsoft/sqlworkshops/master/graphics/bookpencil.png"> <h2>Workshop Modules</h2>

This is a modular workshop, and in each section, you'll learn concepts, technologies and processes to help you complete the solution.

<table style="tr:nth-child(even) {background-color: #f2f2f2;}; text-align: left; display: table; border-collapse: collapse; border-spacing: 5px; border-color: gray;">

  <tr><td style="background-color: AliceBlue; color: black;"><b>Module</b></td><td style="background-color: AliceBlue; color: black;"><b>Topics</b></td></tr>

  <tr><td><a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/01%20-%20Introduction%20and%20Overview.md" >01 - Introduction and Overview </a></td><td> Introduction of the Workshop, Basic Concepts, Services, Roles, Benchmarks. Verification of prerequisites.</td></tr>
  
  <tr><td style="background-color: AliceBlue; color: black;"><a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/02%20-%20Desktop%20Tools%20to%20use%20with%20Microsoft%20Fabric.md" >02 - Desktop Tools to use with Microsoft Fabric</a> </td><td td style="background-color: AliceBlue; color: black;"> Understanding what desktop tools interface with Microsoft Fabric and how to use them.</td></tr>
  

   <tr><td><a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/03%20-%20Data%20Warehouse%20and%20Data%20Integration.md" >03 - Data Warehouse and Data Integration </a></td><td>  Understanding and creating Workspaces, creating a Data Warehouse, connecting and managing, ingesting data with pipelines and data flows</td></tr>

  <tr><td><a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/04%20-%20The%20Lakehouse.md" >04 - The Lakehouse </a></td><td>  Creating a Lakehouse, Linking data, using Spark to create new data sets in the Lakehouse</td></tr>

  <tr><td><a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/05%20-%20Introduction%20to%20Mirroring%20in%20Fabric.md" >05 - Database Mirroring </a></td><td> Introduction to Mirroring in Microsoft Fabric and how to utilize Mirroring as a Data Integration tool</td></tr>
   
  <tr><td><a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/06%20-%20Real-Time%20Intelligence.md" >06 - Real-Time Analytics with Microsoft Fabric </a></td><td> Azure Data Explorer, Fabric and Streaming / Event Data, the Kusto Query Language (KQL)</td></tr>
  
  <tr><td style="background-color: AliceBlue; color: black;"><a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/07%20-%20CoPilots%20%26%20AI%20Skills.md" >07 - Copilots & AI Skills</a> </td><td td style="background-color: AliceBlue; color: black;"> Microsoft Fabric integrates AI and LLM capabilities to assist you in creating your data workloads.  Additionally you can use AI Skills to create RAG patterns off of your data to produce additional insights.</td></tr>

  <tr><td style="background-color: AliceBlue; color: black;"><a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/08%20-%20OLTP%20Databases%20in%20Fabric.md" >08 - OLTP Databases In Microsoft Fabric</a> </td><td td style="background-color: AliceBlue; color: black;"> Microsoft Fabric integrates SQL database and Cosmos DB into your Fabric environment to provide a full end to end development OLTP to Analytics driven scenarios.</td></tr>



</table>

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="https://raw.githubusercontent.com/microsoft/sqlworkshops/master/graphics/geopin.png"><b>Next Steps</b></p>

Next, Continue to <a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" ><i> Pre-Requisites</i></a>

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

# Legal Notices

### License
Microsoft and any contributors grant you a license to the Microsoft documentation and other content in this repository under the [Creative Commons Attribution 4.0 International Public License](https://creativecommons.org/licenses/by/4.0/legalcode), and grant you a license to any code in the repository under [the MIT License](https://opensource.org/licenses/MIT).

Microsoft, Windows, Microsoft Azure and/or other Microsoft products and services referenced in the documentation
may be either trademarks or registered trademarks of Microsoft in the United States and/or other countries.
The licenses for this project do not grant you rights to use any Microsoft names, logos, or trademarks.
Microsoft's general trademark guidelines can be found at http://go.microsoft.com/fwlink/?LinkID=254653.

Privacy information can be found at https://privacy.microsoft.com/en-us/

Microsoft and any contributors reserve all other rights, whether under their respective copyrights, patents,
or trademarks, whether by implication, estoppel or otherwise.
