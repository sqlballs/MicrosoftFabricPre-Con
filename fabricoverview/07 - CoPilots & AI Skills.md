![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2> 07 - Copilots & Data Agents </h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" >Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.) *Note in this section you will need an F2 and higher or a P-SKU in order to test or access Copilot or Data Agents, formerly known in preview as AI Skills.

In this section you will learn about Copilots and Data Agents in Microsoft Fabric.  



You'll cover these topics in this Module on CoPilots & Data Agents:

<dl>

  <dt><a href="#7-1" >7.1 - Understanding Copilots & Data Agents, the Differences & Requirements</a></dt>
  <dt><a href="#7-2" >7.2 - Copilots in Microsoft Fabric</a></dt>
  <dt><a href="#7-3" >7.3 - Microsoft Fabric Data Agents</a></dt>


</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

# 07.1 - Understanding Copilots & Data Agents in Microsoft Fabric

In this section, we will explore the **Copilot** and **Data Agents** features within Microsoft Fabric, highlighting their differences, use cases, and how they can enhance your data workflows.  At the time of the publishing of this course, both **Copilot** and **Data Agents** require an F64 capacity in order to utilize their functionality.

## What is Copilot?

**Copilot** acts as an intelligent assistant designed to streamline various tasks within Microsoft Fabric. It provides real-time support for data professionals by:

- **Generating SQL Queries**: Copilot can help you write SQL code quickly and efficiently, making it easier to interact with your data.
- **Code Completion**: It offers contextual suggestions as you type, reducing the time spent on routine coding tasks.
- **Troubleshooting and Documentation**: Copilot assists in debugging and provides documentation references to help you understand complex processes.



## What is Data Agents?

**Data Agents** is a tool that allows users to configure a generative AI assistant tailored to their specific data needs. Key features include:

- **Natural Language Processing**: Users can ask questions in plain language, and Data Agents generates the corresponding SQL queries.
- **Customization**: You can configure Data Agents to include business context, making it adaptable to your organization’s requirements.
- **Accessibility**: Data Agents enables non-technical users to interact with data without needing SQL knowledge, fostering a self-service data culture.

For more information, visit the Data Agents creation guide (https://learn.microsoft.com/en-us/fabric/get-started/copilot-fabric-overview).

## Difference between an Data Agents and a copilot
The technology behind the Data Agents and the Fabric copilots is similar. They both use generative AI to reason over data. They also have some key differences:

- Configuration: With an Data Agents, you can configure the AI to behave the way you need. You can provide it with instructions and examples that tune it to your specific use case. A Fabric copilot doesn't offer this configuration flexibility.

- Use case: A copilot can help you do your work on Fabric. It can help you generate notebook code or data warehouse queries. In contrast, the Data Agents operates independently. You can eventually connect it to Microsoft Teams and other areas outside of Fabric.


<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="7-2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">7.2 - Copilots in Microsoft Fabric</h2>

Copilot and other generative AI features in preview bring new ways to transform and analyze data, generate insights, and create visualizations and reports in Microsoft Fabric and Power BI.

## Enable Copilot
Before your business can start using Copilot capabilities in Microsoft Fabric, you need to enable Copilot.  To understand how to enable Copilot right click on this link to open in another window, <a href="https://learn.microsoft.com/en-us/fabric/get-started/copilot-enable-fabric">Enable Copilot in Fabric</a>.

Read on for answers to your questions about how it works in the different workloads, how it keeps your business data secure and adheres to privacy requirements, and how to use generative AI responsibly.

Copilot is available in the following services: 

### Copilot for Data Science and Data Engineering
Copilot for Data Engineering and Data Science is an AI-enhanced toolset tailored to support data professionals in their workflow. It provides intelligent code completion, automates routine tasks, and supplies industry-standard code templates to facilitate building robust data pipelines and crafting complex analytical models. Utilizing advanced machine learning algorithms, Copilot offers contextual code suggestions that adapt to the specific task at hand, helping you code more effectively and with greater ease. From data preparation to insight generation, Microsoft Fabric Copilot acts as an interactive aide, lightening the load on engineers and scientists and expediting the journey from raw data to meaningful conclusions.

<p><a href="https://www.youtube.com/watch?v=GOq5gOdKEVs"><img src="https://img.youtube.com/vi/GOq5gOdKEVs/0.jpg" height = 200></a> 

### Copilot for Data Factory
Copilot for Data Factory is an AI-enhanced toolset that supports both citizen and professional data wranglers in streamlining their workflow. It provides intelligent code generation to transform data with ease and generates code explanations to help you better understand complex tasks.

<p><a href="https://www.youtube.com/watch?v=ckw6tZPzP7Y"><img src="https://img.youtube.com/vi/ckw6tZPzP7Y/0.jpg" height = 200></a> 

### Copilot for Data Warehouse
Microsoft Copilot for Synapse Data Warehouse is an AI assistant designed to streamline your data warehousing tasks. Key features of Copilot for Warehouse include Natural Language to SQL, code completion, quick actions, and intelligent insights. For more information, see <a href="https://learn.microsoft.com/en-us/fabric/data-warehouse/copilot">Copilot for Data Warehouse</a>.

<p><a href="https://www.youtube.com/watch?v=WC-mxioPp_8"><img src="https://img.youtube.com/vi/WC-mxioPp_8/0.jpg" height = 200></a> 

### Copilot for Power BI
Power BI has introduced generative AI that allows you to create reports automatically by selecting the topic for a report or by prompting Copilot for Power BI on a particular topic. You can use Copilot for Power BI to generate a summary for the report page that you just created, and generate synonyms for better Q&A capabilities.

For more information on the features and how to use Copilot for Power BI, see <a href="https://learn.microsoft.com/en-us/power-bi/create-reports/copilot-introduction">Overview of Copilot for Power BI</a>.

<p><a href="https://www.youtube.com/watch?v=iTI2HUWLvVI"><img src="https://img.youtube.com/vi/iTI2HUWLvVI/0.jpg" height = 200></a> 

### Copilot for Real-Time Intelligence
Copilot for Real-Time Intelligence is an advanced AI tool designed to help you explore your data and extract valuable insights. You can input questions about your data, which are then automatically translated into Kusto Query Language (KQL) queries. Copilot streamlines the process of analyzing data for both experienced KQL users and citizen data scientists.

For more information, see <a href="https://learn.microsoft.com/en-us/fabric/get-started/copilot-real-time-intelligence">Copilot for Real-Time Intelligence overview</a>.

<p><a href="https://www.youtube.com/watch?v=WC-mxioPp_8"><img src="https://img.youtube.com/vi/WC-mxioPp_8/0.jpg" height = 200></a> 

### Create your own AI solution accelerators
Build your own copilots
Using the client advisor AI accelerator tool, you can build custom copilot with your enterprise data. The client advisor AI accelerator uses Azure OpenAI Service, Azure AI Search, and Microsoft Fabric to create custom Copilot solutions. This all-in-one custom copilot empowers client advisors to use generative AI across structured and unstructured data optimizing daily tasks and fostering better interactions with clients. To learn more, see the GitHub repo.

<p><a href="https://www.youtube.com/watch?v=0jOEUeOykzQ"><img src="https://img.youtube.com/vi/0jOEUeOykzQ/0.jpg" height = 200></a> 

<p><a href="https://www.youtube.com/watch?v=8da4smSAoEk"><img src="https://img.youtube.com/vi/8da4smSAoEk/0.jpg" height = 200></a> 

For more details, check out the [Overview of Copilot in Fabric](https://learn.microsoft.com/en-us/fabric/get-started/copilot-fabric-overview) (https://blog.fabric.microsoft.com/en-us/blog/data-warehouse-copilot-ai-skill/).

[You can find the complete list of Microsoft Purview learning and reference resources at this location.](https://learn.microsoft.com/en-us/training/purview/)

<br>
<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Configure Fabric Mirrored Database</b></p>

<p><img src="https://learn.microsoft.com/en-us/fabric/database/mirrored-database/media/azure-sql-database/fabric-mirroring-sql-database.svg" height = 400></p>

In this activity, you will learn how Copilot in Power BI supports enterprise developers, self-service users, and business users and provides information on integration points and the different experiences designed for creating and consuming content using Copilot.

Open the following reference and complete the steps you see there:

- Open the following Link in another tab follow the instructions to obtain Revenue Opportunities.pbix file <a href="https://learn.microsoft.com/en-us/power-bi/create-reports/tutorial-copilot-power-bi-get-started"> Copilot in Power BI tutorial: Get started</a>
- Open the following Link in another tab follow the instructions <a href="https://learn.microsoft.com/en-us/power-bi/create-reports/tutorial-copilot-power-bi-prepare-model">Prepare semantic model for AI</a>
- Open the following Link in another tab follow the instructions <a href="https://learn.microsoft.com/en-us/power-bi/create-reports/tutorial-copilot-power-bi-discover-data">Discover data and ask questions</a>
- Open the following Link in another tab follow the instructions <a href="https://learn.microsoft.com/en-us/power-bi/create-reports/tutorial-copilot-power-bi-explore-data">Explore data and get more insights</a>


<p style="border-bottom: 1px solid lightgrey;"></p>


<h2 id="7-3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">7.3 Microsoft Fabric Data Agents</h2>

With the Microsoft Fabric Data Agents, you can make data more accessible to your colleagues. You can configure a generative AI system to generate queries that answer questions about your data. After you configure the Data Agents, you can share it with your colleagues, who can then ask their questions in plain English. Based on their questions, the AI generates queries over your data that answer those questions.

## How the Data Agents works
The Data Agents relies on generative AI, specifically, large language models (LLMs). These LLMs can generate queries, for example, T-SQL queries, based on a specific schema and a question. The system sends a question in the Data Agents, information about the selected data (including the table and column names, and the data types found in the tables) to the LLM. Next, it requests generation of a T-SQL query that answers the question. Parse the generated query to first ensure that it doesn't change the data in any way. Then execute that query. Finally, show the query execution results. An Data Agents is intended to access specific database resources, and then generate and execute relevant T-SQL queries.

## Data Agents configuration
Think of the Data Agents as you might think about Power BI reports. You first build the report, and then you share the report with your colleagues who can consume it to get their data insights. The Data Agents works in a similar way. You need to first create and configure the Data Agents. Then, you can share it with your colleagues.

You should expect to handle some necessary configuration steps before the Data Agents works properly. An Data Agents can often provide out-of-the-box answers to reasonable questions, but it could provide incorrect answers for your specific situation. Incorrect answers typically occur because the AI is missing context about your company, setup, or definition of key terms. To solve the problem, provide the AI with instructions and example question-query pairs. You can use these powerful techniques to guide the AI to the right answers.

Microsoft Fabric: Data Agents Preview! Build RAG Patterns Simple and Easy!


<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided or in Class Activity: Create an Data Agents</b></p>

In this Activity you will execute code from the following exercises to create  AdventureWorks tables in a Microsoft Fabric Lakehouse.  You will then provision an Data Agents and follow the steps in the tutorial to publish the skill and access it in a Microsoft Fabric Notebook.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png"><b>Steps</b></p>


- [Data Agents example with the AdventureWorks dataset](https://learn.microsoft.com/en-us/fabric/data-science/ai-skill-scenario) 


> If you only reviewed the documentation in this Activity, ensure you bookmark each of these references and then perform the Activity in full once you do have your deployment. 

<a href="https://www.youtube.com/watch?v=5ivA4zdnDtE"><img src="https://img.youtube.com/vi/5ivA4zdnDtE/0.jpg" height = 200></a> 

<p><a href="https://www.youtube.com/watch?v=cuF00-iV_YA"><img src="https://img.youtube.com/vi/cuF00-iV_YA/0.jpg" height = 200></a> 

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
  <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/copilot-privacy-security">Privacy, security, and responsible use of Copilot in Fabric</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/copilot-fabric-consumption">Copilot in Fabric consumption</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/copilot-faq-fabric" >Copilot for Microsoft Fabric and Power BI: FAQ</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-skill-tenant-switch" >Data Agents tenant settings</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-skill-sharing" >Data Agents sharing and permission management</a></li>
  <li><a href="https://learn.microsoft.com/en-us/fabric/get-started/whats-new" >As always, this is a fast-changing technology, so ensure you check this reference to find the latest improvements.</a></li>
</ul>

<p style="border-bottom: 1px solid lightgrey;"></p>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/08%20-%20OLTP%20Databases%20in%20Fabric.md).



