---
title: Data model concepts
seo-title: Data model concepts
description: Data model concepts
seo-description: 
uuid: 57445df2-d65a-4819-9156-84ccf7780581
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/developing/using/data-model-concepts
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T02 18 29.762-0400
cq-lastreplicated: 2018-09-07T14 48 15.019-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: developing
content-type: reference
topic-tags: about-custom-resources
cq-template: /apps/help/templates/article-3
discoiquuid: dac98177-b1a5-44eb-b2e5-be6377c42025
firstPublishExternalDate: 2018-09-07T14:48:12.669-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 20.817-0400
jcr-createdby: admin
jcr-description: Data model concepts
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:48:12.669-0400
lochandoffdate: 2018-09-10T02 18 29.761-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Data model concepts
publishexternaldate: 2018-09-07T14 48 12.669-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/developing/using/data-model-concepts.html
sha1: 8b6db07c565e08061ac72a2c00df58a28e4947f7
topicBrowsingSortDate: 2018-09-07T14:48:12.669-0400
index: y
internal: n
snippet: y
---

# Data model concepts

Data model concepts

Adobe Campaign comes with a pre-defined data model. This data model can be modified by administrators with new resources or extensions to existing resources.

The **Administration** > **Development** menu, accessed via the Adobe Campaign logo, allows you to manage your **custom resources**, **publish** them, and **access the diagnostic tools**.

The data used by Adobe Campaign is defined through different resources.

You can **enrich the data template** that is provided by creating your own custom resources, such as purchase or product tables.

Out-of-the-box resources (such as campaigns, emails, or audiences) cannot be modified. However, custom resources can be extended to add new fields.

>[!NOTE]
>
>You can find a datamodel representation for the out-of-the-box resources [here](https://docs.campaign.adobe.com/doc/standard/en/datamodel/datamodel.html).

You can also **configure the navigation** in the screens corresponding to the resource created.

Extension fields are generated with a prefix so that they never conflict with the out-of-the-box fields.