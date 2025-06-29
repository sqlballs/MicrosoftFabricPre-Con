![](../graphics/microsoftlogo.png)

# Workshop: Microsoft Fabric Overview for the Data Professional

#### <i>A Microsoft Workshop</i>

<p style="border-bottom: 1px solid lightgrey;"></p>

<img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/textbubble.png"> <h2>04 - The Lakehouse</h2>

In this workshop you'll cover using The Microsoft Fabric Platform to implement a complete Analytics solution using the Microsoft Fabric platform.

In each module you'll get more references, which you should follow up on to learn more. Also watch for links within the text - click on each one to explore that topic.

(<a href="https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/00%20-%20Pre-Requisites.md" >Make sure you check out the <b>Pre-Requisites</b> page before you start</a>. You'll need all of the items loaded there before you can proceed with the workshop.)

You'll cover these topics in this Module:

<dl>
  <dt><a href="#4.1" >4.1 - Understanding a Microsoft Fabric Lakehouse</a></dt>
  <dt><a href="#4.2" >4.2 - Loading Data & Shortcuts</a></dt>
  <dt><a href="#4.3" >4.3 - Using Spark to create new data sets in the Lakehouse</a></dt>
  <dt><a href="#4.4" >4.4 - How to accelerate data prep with Data Wrangler in Microsoft Fabric</a></dt>
  <dt><a href="#4.5" >4.5 - Transform and enrich data seamlessly with AI functions</a></dt>
</dl>

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.1"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.1 Understanding a Microsoft Fabric Lakehouse</h2>

Microsoft Fabric Lakehouse is a data architecture platform for storing, managing, and analyzing structured and unstructured data in a single location. It is a flexible and scalable solution that allows organizations to handle large volumes of data using a variety of tools and frameworks to process and analyze that data. It integrates with other data management and analytics tools to provide a comprehensive solution for data engineering and analytics. 

<p><img src="https://learn.microsoft.com/en-us/fabric/data-engineering/media/lakehouse-overview/lakehouse-overview.gif" height=400>

The Lakehouse creates a serving layer by auto-generating an SQL endpoint and a default dataset during creation. This new see-through functionality allows user to work directly on top of the delta tables in the lake to provide a frictionless and performant experience all the way from data ingestion to reporting.

An important distinction between the warehouse is that it's a read-only experience and doesn't support the full T-SQL surface area of a transactional data warehouse. It is important to note that only the tables in Delta format are available in the SQL Endpoint. Parquet, CSV, and other formats can't be queried using the SQL Endpoint. If you don't see your table, convert it to Delta format.

**Interacting with the Lakehouse item**

A data engineer can interact with the lakehouse and the data within the lakehouse in several ways:

- The Lakehouse explorer: The explorer is the main Lakehouse interaction page. You can load data in your Lakehouse, explore data in the Lakehouse using the object explorer, set MIP labels & various other things. Learn more about the explorer experience: Navigating the Lakehouse explorer.
- Notebooks: Data engineers can use the notebook to write code to read, transform and write directly to Lakehouse as tables and/or folders. You can learn more about how to leverage notebooks for Lakehouse: Explore the data in your Lakehouse with a notebook and How to use a notebook to load data into your Lakehouse.
- Pipelines: Data engineers can use data integration tools such as pipeline copy tool to pull data from other sources and land into the Lakehouse. Find more information on how to use the copy activity: How to copy data using copy activity.
- Apache Spark job definitions: Data engineers can develop robust applications and orchestrate the execution of compiled Spark jobs in Java, Scala, and Python. Learn more about Spark jobs: What is an Apache Spark job definition?.
- Dataflows Gen 2: Data engineers can leverage Dataflows Gen 2 to ingest and prepare their data. Find more information on load data using dataflows: Create your first dataflow to get and transform data.

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.2"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.2 - Loading Data & Shortcuts</h2>

In Microsoft Fabric, there are a few ways you can get data into a lakehouse.

### Considerations when choosing approach to load data

| Use Case                                | Recommendation                                                                 |
|-----------------------------------------|---------------------------------------------------------------------------------|
| Small file upload from local machine    | Use **Local file upload**                                                      |
| Small data or specific connector        | Use **Dataflows**                                                              |
| Large data source                       | Use **Copy tool in pipelines**                                                 |
| Complex data transformations            | Use **Notebook code**                                                          |
| Streaming data                          | Use **Eventstream** to stream data into **Eventhouse**; enable **OneLake availability** and create a shortcut from **Lakehouse** |
| Time-series data                        | Get data from **Eventhouse**                                                   |


<p><img  src="https://learn.microsoft.com/en-us/fabric/data-warehouse/media/tutorial-analyze-data-notebook/lakehouse-load-data-new-shortcut.png" height=200>

You will see examples of many of these processes throughout the Workshop. You can also use a link of sorts to data - called a *shortcut*.

*Shortcuts* in a lakehouse allow users to reference data without copying it. It unifies data from different lakehouses, workspaces, or external storage, such as ADLS Gen2 or AWS S3. You can quickly make large amounts of data available in your lakehouse locally without the latency of copying data from the source.

**Setting up a shortcut**

To create a shortcut, open *Lakehouse Explorer* and select where to place the shortcut under *Tables* or *Files*. Creating a shortcut to Delta formatted table under Tables in Lakehouse Explorer will automatically register it as a table, enabling data access through Spark, SQL endpoint, and default dataset. Spark can access shortcuts in Files for data science projects or for transformation into structured data.

**Access Control for shortcuts**

Shortcuts to Microsoft Fabric internal sources will use the calling user identity. External shortcuts will use connectivity details, including security details specified when the shortcut is created.


**Stream real-time events with Eventstream**

With Eventstream, you can get, process, and route high volumes real-time events from a wide variety of sources.

<img src="https://learn.microsoft.com/en-us/fabric/data-engineering/media/load-data-lakehouse/get-data-eventstream.png">

To see how to add lakehouse as a destination for Eventstream, see <a href="https://learn.microsoft.com/en-us/fabric/real-time-intelligence/event-streams/get-data-from-eventstream-in-multiple-fabric-items#get-data-from-eventstream-in-a-lakehouse">Get data from Eventstream in a lakehouse</a>.

For optimal streaming performance, you can stream data from Eventstream into an Eventhouse and then enable OneLake availability.


**Get data from Eventhouse**

When you enable OneLake availability on data in an Eventhouse, a Delta table is created in OneLake. This Delta table can be accessed by a lakehouse using a shortcut. 

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Ingest Data & Create a shortcut</b></p>

In this activity you will follow  the Data warehouse tutorial introduction.

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/checkmark.png">

- Open the following reference in another tab, [Tutorial: Analyze data with a notebook](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-analyze-data-notebook)
- Follow Tutorial 10 Tutorial: Analyze data in a notebook
- - In Step 10 Remember to use the Lakehouse we created in Module 2

<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.3"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.3 - Using Spark to create new data sets in the Lakehouse</h2>

Microsoft Fabric Data Engineering and Data Science experiences operate on a fully managed Spark compute platform. This platform is designed to deliver unparalleled speed and efficiency. With starter pools, you can expect rapid Spark session initialization, typically within 5 to 10 seconds, and no need for manual setup. 

<p><img  src="https://learn.microsoft.com/en-us/fabric/data-warehouse/media/tutorial-analyze-data-notebook/drop-dim-customer-notebook.png" height=300>

**Load Data with Spark**

In this section you'll see how to read/write data into your lakehouse with a notebook. Spark API and Pandas API are supported to achieve this goal.

*Load data with a Juypter Notebook*

It is simple to load data into a notebook using Microsoft Fabric.  Any table in your Lakehouse can easily be added to a new or existing notebook by simply clicking on the table, selecting Load Data, and then selecting Spark.  This will add a PySpark command to your notebook loading the top 1000 rows into a data frame and displaying them.

*Load data with an Apache Spark API*

In the code cell of the notebook, you can read data from the source and load it into Files, Tables, or both sections of your lakehouse.

To specify the location to read from, you can use the relative path if the data is from the default lakehouse of current notebook, or you can use the absolute ABFS path if the data is from other lakehouse. you can copy this path from the context menu of the data explorer.

<p><img  src="https://learn.microsoft.com/en-us/fabric/data-engineering/media/lakehouse-notebook-explore/load-data-menu.png" height=400>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Activity: Create Cross Database Queries for Reporting</b></p>

In this activity we will be following with the Data warehouse tutorial introduction

<b>Steps:</b>

- Open the following reference in another tab, [Tutorial: Create a cross-warehouse query in a warehouse](https://learn.microsoft.com/en-us/fabric/data-warehouse/tutorial-sql-cross-warehouse-query-editor)


<p style="border-bottom: 1px solid lightgrey;"></p>

<h2 id="4.4"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.4 - How to accelerate data prep with Data Wrangler in Microsoft Fabric</h2>

<p><img  src="https://learn.microsoft.com/en-us/fabric/data-science/media/data-wrangler/view-summary-panel.png" height=400>

Data Wrangler is a notebook-based tool that provides users with an immersive experience to conduct exploratory data analysis. The feature combines a grid-like data display with dynamic summary statistics, built-in visualizations, and a library of common data-cleaning operations. Each operation can be applied in a matter of clicks, updating the data display in real time and generating code that can be saved back to the notebook as a reusable function.

### Launch Data Wrangler

Users can launch Data Wrangler directly from a Microsoft Fabric notebook to explore and transform any Pandas DataFrame. 

<p><img  src="https://learn.microsoft.com/en-us/fabric/data-science/media/data-wrangler/launch-data-wrangler.png" height=400>

### Viewing summary statistics

When Data Wrangler launches, it generates a descriptive overview of the displayed DataFrame in the Summary panel. This overview includes information about the DataFrame's dimensions, missing values, and more. Selecting any column in the Data Wrangler grid prompts the Summary panel to update and display descriptive statistics about that specific column. Quick insights about every column are also available in its header.

<p><img  src="https://learn.microsoft.com/en-us/fabric/data-science/media/data-wrangler/view-summary-panel.png" height=400>

<p><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/point1.png"><b>Self-Guided Activity: How to accelerate data prep with Data Wrangler in Microsoft Fabric</b></p>

In this Self-Guided activity you will follow  the Data warehouse tutorial introduction

<b>Steps:</b>

- Open the following reference in another tab: [How to accelerate data prep with Data Wrangler in Microsoft Fabric](https://learn.microsoft.com/en-us/fabric/data-science/data-wrangler)
  - Follow the steps on the page to utilize Data Wrangler

You can also right-click this link to open it in another tab and review this video that introduces you to these concepts:

<p><a href="https://www.youtube.com/watch?v=uwsCFJR3rmk"><img src="https://img.youtube.com/vi/uwsCFJR3rmk/0.jpg" height = 200></a> 

<p style="border-bottom: 1px solid lightgrey;"></p>



<h2 id="4.5"><img style="float: left; margin: 0px 15px 15px 0px;" src="../graphics/pencil2.png">4.5 - Transform and enrich data seamlessly with AI functions</h2>

<p><img  src="https://learn.microsoft.com/en-us/fabric/data-science/media/data-wrangler/view-summary-panel.png" height=400>

Currently in preview with Microsoft Fabric, all business professionals—from developers to analysts—can derive more value from their enterprise data through Generative AI, using experiences like Copilot and Fabric data agents. Thanks to a new set of AI functions for data engineering, Fabric users can now harness the power of industry-leading large language models (LLMs) to transform and enrich data seamlessly.

AI functions harness the power of GenAI for summarization, classification, text generation, and so much more—all with a single line of code:

Calculate similarity with ai.similarity: 
<p>

- <a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-functions/overview?tabs=pandas#calculate-similarity-with-aisimilarity">Calculate similarity with ai.similarity:</a> Compare the meaning of input text with a single common text value, or with corresponding text values in another column.
- <a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-functions/overview?tabs=pandas#categorize-text-with-aiclassify">Categorize text with ai.classify:</a> Classify input text values according to labels you choose.
- <a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-functions/overview?tabs=pandas#detect-sentiment-with-aianalyze_sentiment">Detect sentiment with ai.analyze_sentiment:</a> Identify the emotional state expressed by input text.
- <a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-functions/overview?tabs=pandas#extract-entities-with-aiextract">Extract entities with ai.extract:</a> Find and extract specific types of information from input text, for example locations or names.
- <a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-functions/overview?tabs=pandas#fix-grammar-with-aifix_grammar">Fix grammar with ai.fix_grammar:</a> Correct the spelling, grammar, and punctuation of input text.
- <a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-functions/overview?tabs=pandas#summarize-text-with-aisummarize">Summarize text with ai.summarize:</a> Get summaries of input text.
- <a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-functions/overview?tabs=pandas#translate-text-with-aitranslate">Translate text with ai.translate:</a> Translate input text into another language.
- <a href="https://learn.microsoft.com/en-us/fabric/data-science/ai-functions/overview?tabs=pandas#answer-custom-user-prompts-with-aigenerate_response">Answer custom user prompts with ai.generate_response:</a> Generate responses based on your own instructions.
<p>

It's seamless to incorporate these functions as part of data-science and data-engineering workflows, whether you're working with pandas or Spark. There is no detailed configuration, no complex infrastructure management, and no specific technical expertise needed.


You can also right-click this link to open it in another tab and review this video to see a demonstration of AI Functions.

<p><a href="https://www.youtube.com/watch?v=rfvCgPS3ie0"><img src="https://img.youtube.com/vi/rfvCgPS3ie0/0.jpg" height = 200></a> 

<p style="border-bottom: 1px solid lightgrey;"></p>

<p><img style="margin: 0px 15px 15px 0px;" src="../graphics/owl.png"><b>For Further Study</b></p>
<ul>
 <li><a href="https://learn.microsoft.com/en-us/fabric/release-plan/">Microsoft Fabric release plan documentation</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/spark-compute" >What is Spark compute in Microsoft Fabric?</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/runtime" >Apache Spark Runtime in Fabric</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/create-custom-spark-pools" >How to create custom Spark pools in Microsoft Fabric</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/high-concurrency-overview" >High Concurrency mode in Fabric Spark</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/autotune?tabs=sparksql" >What is autotune for Apache Spark configurations in Fabric and how to enable and disable it?</a></li>
    <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/spark-job-concurrency-and-queueing" >Concurrency limits and queueing in Microsoft Fabric Spark</a></li>
        <li><a href="https://learn.microsoft.com/en-us/fabric/data-engineering/lakehouse-schemas" >What are lakehouse schemas (Preview)?</a></li>
</ul>

Congratulations! You have completed this Module. If you understand the concepts here and have completed all of the Activities, you can [proceed to the next Module](https://github.com/sqlballs/MicrosoftFabricPre-Con/blob/main/fabricoverview/05%20-%20Introduction%20to%20Mirroring%20in%20Fabric.md).
