---
title: Configuring Triggers in Experience Cloud
seo-title: Configuring Triggers in Experience Cloud
description: Configuring Triggers in Experience Cloud
seo-description: Learn how to configure the Adobe Experience Cloud Triggers integration to start sending personalized deliveries to your customers based on their previous behaviors. 
uuid: a2a8da1d-6e5d-450e-b3e9-94a20efc4e91
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/integrating/using/configuring-triggers-in-experience-cloud
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-27T03 27 20.801-0400
cq-lastreplicated: 2018-07-23T05 59 48.352-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: integrating
content-type: reference
topic-tags: working-with-campaign-and-triggers
cq-template: /apps/help/templates/article-3
discoiquuid: f94500ac-0d3a-4106-8db6-5bdc8622a238
firstPublishExternalDate: 2018-07-23T05:59:48.311-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-06-15T07 29 56.227-0400
jcr-createdby: admin
jcr-description: Configuring Triggers in Experience Cloud
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T05:59:48.311-0400
lochandoffdate: 2018-07-27T03 27 20.800-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Configuring Triggers in Experience Cloud
publishexternaldate: 2018-07-23T05 59 48.311-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/integrating/using/configuring-triggers-in-experience-cloud.html
sha1: b93cc13d96716c6f89fd44600d873843ecdb8c98
topicBrowsingSortDate: 2018-07-23T05:59:48.311-0400
index: y
internal: n
snippet: y
---

# Configuring Triggers in Experience Cloud

Configuring Triggers in Experience Cloud

## Activating the functionality

The functionality must be activated in Adobe Campaign by Adobe. Please contact your Adobe account executive or professional services partner.

The Adobe team will need the following information to activate triggers:

* Marketing Cloud Company Name
* IMS ORG ID
* Analytics Login Company (can be the same as the Marketing Cloud Company Name)

## Configuring solutions and services

In order to use this feature, you need to have access to the following solutions/core services:

* Adobe Campaign
* Adobe Analytics Ultimate, Premium, Foundation, OD, Select, Prime, Mobile Apps, Select, or Standard.
* Experience Cloud Triggers Core Service

  ![](assets/trigger_uc_prereq_1.png)

* Experience Cloud DTM Core Service

  ![](assets/trigger_uc_prereq_2.png)

* Experience Cloud Visitor ID and Experience Cloud People Core Service

  ![](assets/trigger_uc_prereq_3.png)

You also need to have a working website.

![](assets/trigger_uc_prereq_4.png)

>[!CAUTION]
>
>Sub-domain delegation is a deliverability key element. Make sure that the Adobe Campaign emails are sent from the same domain as the one used by the website.

You need to configure [Experience Cloud DTM Core Service](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-experience-cloud-dtm-core-service), [Experience Cloud People Core Service](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-experience-cloud-people-core-service) and [Campaign](../../integrating/using/configuring-triggers-in-experience-cloud.md#configuring-triggers-and-aliases-in-campaign) to run these use cases.

### Configuring Experience Cloud DTM Core Service

1. In Experience Cloud DTM Core Service (Dynamic Tag Management), activate Experience Cloud ID and Adobe Analytics for your website pages.

   ![](assets/trigger_uc_conf_1.png)

1. ID reconciliation between the website, Adobe Analytics and Adobe Campaign requires to use aliasing. Create an alias, "visitorid" for example.

   ![](assets/trigger_uc_conf_2.png)

### Configuring Experience Cloud People Core Service

The alias previously referenced in DTM needs to be created in the Experience Cloud People Core Service through a Customer Attribute. Make sure you create a new one and reference the same DTM alias in the integration code (for example "visitorid").

![](assets/trigger_uc_conf_3.png)

>[!NOTE]
>
>We are going to use this Customer Attribute in the Data source in Adobe Campaign (next step).

### Configuring triggers and aliases in Campaign

1. Make sure you have **Experience Cloud triggers** visible on your Adobe Campaign Standard instance. If you don't, contact the Adobe Campaign administrators.

   ![](assets/remarketing_1.png)

1. Aliases enable a contact in Analytics to be reconciled with a profile in Campaign. You need to match the aliases defined in the Experience Cloud ID service with a Shared Data Source in Campaign. You need to configure the aliases resolution in Adobe Campaign via a Data source (**Administration** > **Application Settings** > **Shared Data Sources**). Make sure you choose the correct data source in the **Data Source/Alias** drop-down menu, which is mapped with the same Customer Attribute data source created in previous step.

   ![](assets/trigger_uc_conf_5.png)

   >[!NOTE]
   >
   >You can reconcile your triggers for both anonymous and logged in users. For anonymous users, the profile should exist in Adobe Campaign and an email has been sent to the user before. For this, Visitor ID configuration is sufficient. However, if you want to reconcile triggers for logged in users, you need to setup Declared ID Data Source. For more on this, refer to [Data Source configuration](../../integrating/using/provisioning-and-configuring-integration-with-audience-manager-or-people-core-service.md#step-2--configure-the-data-sources).

## Creating a trigger in the Experience Cloud interface

An Adobe Experience Cloud trigger needs to be created so that you can use it in Campaign.

Create a new trigger in Experience Cloud and make sure you select the report suite used on your website. Make sure you choose the right dimension so that the trigger will fire.

Refer to the [Adobe Experience Cloud documentation](https://marketing.adobe.com/resources/help/en_US/mcloud/triggers.html) and watch this [video](https://helpx.adobe.com/marketing-cloud/how-to/email-marketing.html#step-two) .

## Triggers best practices and limitations

Here is a list of best practices and limitations for the use of the Campaign - Triggers integration:

* If you have multiple instances of Campaign Standard, then triggers can be received by all instances as long as they are in the same IMS org ID. Analytics also needs to be on same IMS org ID.
* You cannot create a trigger in the Trigger Core Service using events from two different report suites.
* Triggers are based on transactional messages. Transactional messages are used whenever you have to send a message very quickly. You cannot queue transactional messages and then loop them in batch.
* Triggers are not deterministic in nature. When a trigger is generated, it sends all aliases associated with the cookie, so in case of shared browsers such as in retail kiosks, libraries, cyber cafes, or shared devices at home (husband and wife logging in from the same device), it is not possible to map to the right ID. All IDs used to login with the browser are sent to Campaign which sends out a message on the basis of the first reconciliation. If there are multiple "email IDs" eligible for reconciliation, then Campaign does not send an email. There is no way for Campaign to know what the right email ID is unless it is captured and sent by Analytics.
* You cannot store contents of payload in Campaign. Triggers cannot be used to update a profile's data.
* Customer Attributes are not supported in Triggers (meaning, only report suite data can be used to define Triggers business rules).
* Collection of collections are not supported in Campaign.

>[!CAUTION]
>
>Your website must be running on the same domain as the Adobe Campaign server. If not, you cannot use visitor id to reconcile and reach out to users visiting the website anonymously.
