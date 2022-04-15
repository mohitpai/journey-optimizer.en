---
title: Get Started with Datasets
description: Learn how to use Adobe Experience Platform Datasets in Adobe Journey Optimizer
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
---
# Get Started with Datasets {#datasets-gs}

All data that is ingested into Adobe Experience Platform is persisted within the Data Lake as datasets. A dataset is a storage and management construct for a collection of data, typically a table, that contains a schema (columns) and fields (rows).

## Access datasets{#access-datasets}

The **Datasets** workspace in [!DNL Adobe Journey Optimizer] user interface allows you to explore data and create datasets. 

Select **Datasets** in the left-navigation to open the Datasets dashboard.

![](assets/datasets-home.png)

Adding data to Adobe Experience Platform is the foundation to building a Profile. You will then be able to leverage profiles in [!DNL Adobe Journey Optimizer]. First define schemas, use ETL tools to prepare and standardize your data, then create datasets based on your schemas.

Select the **Browse** tab to display the list of all available datasets for your organization. Details are displayed for each listed dataset, including its name, the schema the dataset adheres to, and status of the most recent ingestion run.

By default, only the datasets that you have ingested into are shown. If you want to see the system-generated datasets, enable the **Show system datasets** toggle from the filter.

![](assets/ajo-system-datasets.png)

Select the name of a dataset to access its Dataset activity screen and see details of the dataset you selected. The activity tab includes a graph visualizing the rate of messages being consumed as well as a list of successful and failed batches.

## Create datasets{#create-datasets}

To create a new dataset, start by selecting **Create dataset** in the Datasets dashboard.

You can:

* Create dataset from schema. [Learn more in this documentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target="_blank"}
* Create dataset from CSV file. [Learn more in this documentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html){target="_blank"}


Watch this video to learn how to create a dataset, map it to a schema, add data to it, and confirm that the data has been ingested.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)


Learn how to create a schema, a dataset and ingest data to add Test profiles in Adobe Journey Optimizer in [this end-to-end sample](../segment/creating-test-profiles.md)

Learn more about dataset creation in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target="_blank"}.

Learn how to use Datasets UI in the [Data Ingestion overview documentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target="_blank"}.


**See also**

* [Create a schema, a dataset and ingest data to add Test profiles in Journey Optimizer](../segment/creating-test-profiles.md)
* [Streaming ingestion overview](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html){target="_blank"}
* [Ingest data into Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target="_blank"}
