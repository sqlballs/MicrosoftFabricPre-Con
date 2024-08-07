![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop from Azure Data and the Fasttrack Team</i>


<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>00 Pre-Requisites</h2>

The "Microsoft Fabric Overview for the Data Professional" workshop is taught using the following components, which you will install and configure in the sections that follow. 

**In Order to Commplete the Activities in this Workshop, you mush have a Power BI License and a Microsoft Fabric-Enabled Workspace. The steps for these requirements are explained below.**


- For this workshop, you will be required to execute workloads using Microsoft Fabric.  In order to do this you must first sign up for, or currently have, an M365 account with the proper permissions.  If you do not have an M365 account with the proper permissions you can sign up for a 90 day free trial of M365.
- Next you must have a Power BI Pro license.  If you do not have a Power BI license you can sign up for one for free 60 day trial.
- You will also require a Microsoft Fabric Capacity or a Free trial Microsoft Fabic Capacity which will run for 60 days.  
- Signing up for M365, Power BI, and Microsoft Fabric is free and does not require a credit card.
- Your Power BI Tenent must have Fabric Capacity enabled in order to create a Microsoft Fabric Workspace.  Please review, [Enable for your tenant](https://github.dev/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md) and [Enable for a capacity](https://learn.microsoft.com/en-us/fabric/admin/fabric-switch#enable-for-a-capacity) for instructions in how to do this. 

> You can also create a free Azure Subscription for 1 year with a $200 credit, and then provision a Microsoft Fabric Capacity and attach it to a Power BI Workspace.

## Required Permissions

In order to be a Microsoft Fabric Admin for your orginization, you must be in one of the following roles

- Global administrator
- Power Platform administrator
- Microsoft Fabric administrator

<p>

These roles are assigned in the Microsoft 365 Administration portal.  Microsoft 365 user admins assign users to the Fabric administrator or Power Platform administrator roles in the Microsoft 365 admin portal.
<p>

The other requirements are:

- **A M365 Subscription or orginizational account with the proper rights** - This will allow you to create a "domain" account which can be used to sign up for Power BI.
- **A Power BI License** - You must have a Power BI License in order to utilize Microsoft Fabric.
- **A Microsoft Fabric Capacity** - This could be a free trial or a provisioned Azure Capacity.
- **A Computer with an Internet Browser** - To participate in the activities in this Workshop you must have a computer and an internet browser.
- **A Working Internet Connection** - Microsoft Fabric is a SaaS, Software as a Service, platform hosted on the Internet.  You must have internet connectivity to access Microsoft Fabric.
- **Potentially: A Microsoft Azure Account**: This is only required if you do not have a free trial Microsoft Fabric Capacity. This workshop uses the Microsoft Fabric which  platform to host the Microsoft Fabric Capacity, and optionally you can deploy a Microsoft Fabric Capacity. You can use a free Azure account, an MSDN Account, your own account, or potentially one provided for you, as long as you can create about $200.00 (U.S.) worth of assets. 

*Note that all following activities must be completed prior to class - there will not be time to perform these operations during the workshop.*

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Set up M365 account, Power BI License, Microsoft Fabric Capacity, Validate you have a computer, and Internet</b></p>

<p>

Open this link in a seperate tab or window and follow all of the instructions, [Accessing Microsoft Fabric for developers, startups and enterprises!](https://blog.fabric.microsoft.com/en-us/blog/accessing-microsoft-fabric-for-developers-startups-and-enterprises/)




<h2 id="2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">Verification of pre-requisites for the Activities</h2>

In order to complete any exercises required in this class you should have followed the [Pre-Requisites](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md) outlined in the Read.me file. 

Validate that you have a Microsoft Fabric Enabled Workspace:
- Navigate to [Tutorial: Create a Microsoft Fabric workspace](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-create-workspace)
- Navigate to your Microsoft Fabric enabled workspace
- Click +New
- Click Show all
- Validate that you see the options available to you to create Microsoft Fabric objects such as a Lakehouse, a Data Warehouse, Pipelines, KQL Database, or an EventStream


