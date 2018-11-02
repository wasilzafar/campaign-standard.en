---
title: Exporting logs
seo-title: Exporting logs
description: Exporting logs
seo-description: Log data, whether they are related to deliveries or to subscriptions, can be exported through a simple workflow.
uuid: 994d5bb0-572a-4955-a63b-358aceb24a33
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/exporting-logs
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-25T09 29 59.434-0400
cq-lastreplicated: 2018-07-23T05 57 55.338-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: importing-and-exporting-data
cq-template: /apps/help/templates/article-3
discoiquuid: 38684da9-c561-49dd-84ee-f36af1837565
firstPublishExternalDate: 2018-07-23T05:57:55.259-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 00.687-0400
jcr-createdby: admin
jcr-description: Exporting logs
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:57:55.259-0400
lochandoffdate: 2018-07-25T09 29 59.434-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Exporting logs
publishexternaldate: 2018-07-23T05 57 55.259-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/exporting-logs.html
sha1: 5193dcb376aa8bb7dc54ea7f7f261ce22d12efa1
topicBrowsingSortDate: 2018-07-23T05:57:55.259-0400
index: y
internal: n
snippet: y
---

# Exporting logs

Exporting logs

Log data, whether they are related to deliveries or to subscriptions, can be exported through a simple workflow. It enables you to analyze the results of your campaigns in your own reporting or BI tool.

By using an **Incremental query** that only retrieves new logs every time the workflow is executed and a simple **Extract file** activity to define the output columns, you can get a file with the format and all the data you need. Then use a **Transfer file** activity to retrieve the final file. Each workflow execution is planned by a **Scheduler**.

The export logs operation can be carried out by standard users. Private resources such as: broadlogs, tracking logs, exclusion logs subscription logs and subscription history logs on **Profiles** can only be managed by functional administrator.

1. Create a new workflow as detailed in [this section](../../automating/using/building-a-workflow.md#creating-a-workflow).
1. Add a **Scheduler** activity and set it according to your needs. Below is an example of a monthly execution.

   ![](assets/export_logs_scheduler.png)

1. Add an **Incremental query** activity and configure it so that it selects the logs you need. For example, to select all new or updated broadlogs (profile delivery logs):

    * In the **Properties** tab, change the target resource to **Delivery logs** (broadLogRcp).
    
      ![](assets/export_logs_query_properties.png)

    * In the **Target** tab, set a condition to retrieve all delivery logs that correspond to deliveries sent in 2016 or after. For more information, refer to the [Editing queries](../../automating/using/editing-queries.md#creating-queries) section.
    
      ![](assets/export_logs_query_target.png)

    * In the **Processed data** tab, select **Use a date field** and choose the **lastModified** field. On the next executions of the workflow, only logs that will have been modified or created after the last execution will be retrieved.
    
      ![](assets/export_logs_query_processeddata.png)    
    
      After the first execution of the workflow, you can see in this tab the last execution date that will be used for the next execution. It is automatically updated every time the workflow is executed. You still have the possibility to override this value by manually entering a new one so that it fits your needs.

1. Add an **Extract file** activity that will export the queried data in a file:

    * In the **Extraction** tab, specify the name of the file. This name will be automatically completed with the date of the export to ensure all extracted files are unique.

      Select the columns that you want to export in your file. You can select here data coming from related resources such as delivery or profile information. To organize the final file, you can apply a sort. For example on the log date, as shown in the example below.
    
      ![](assets/export_logs_extractfile_extraction.png)

      >[!NOTE]
      >
      >It is not possible to export unique identifiers (primary keys) of log resources.

    * In the **File structure** tab, define the format of the output file to match your needs.

      Check the **Export labels instead of internal values of enumerations** option in case you export enumeration values. This option allows to retrieve shorter labels that are easy to understand instead of IDs.

1. Add a **Transfer file** activity and configure it to transfer the newly created file from the Adobe Campaign server to another location where you can access it, such as a SFTP server.

    * In the **General** tab, select **File upload** as the purpose is to send the file from Adobe Campaign to another server.
    * In the **Protocol** tab, specify the transfer parameters and select the [external account](../../administration/using/external-accounts.md#creating-an-external-account) to use.

1. Add an **End** activity to make sure it properly ends and save your workflow.

   ![](assets/export_logs_example_workflow.png)

You can now execute the workflow and retrieve the output file on your external server.

**Related topic:**

[Workflows](../../automating/using/discovering-workflows.md)