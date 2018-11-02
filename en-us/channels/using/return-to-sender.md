---
title: Return to sender
seo-title: Return to sender
description: Return to sender
seo-description: Learn how to be notified of an incorrect address and exclude it from future communications.
uuid: c75e1208-523d-4c7f-aba3-3efeed4d1b05
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/channels/using/return-to-sender
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-07-30T04 53 59.722-0400
cq-lastreplicated: 2018-07-23T06 02 55.160-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: channels
content-type: reference
topic-tags: direct-mail
cq-template: /apps/help/templates/article-3
discoiquuid: 933d0095-534e-46c4-b811-f5827bf444d9
firstPublishExternalDate: 2018-07-23T06:02:55.130-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 09.919-0400
jcr-createdby: admin
jcr-description: Return to sender
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-07-23T06:02:55.130-0400
lochandoffdate: 2018-07-30T04 53 59.722-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: Return to sender
publishexternaldate: 2018-07-23T06 02 55.130-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/channels/using/return-to-sender.html
sha1: 48b310eebfaa2d242a3959bfc78774bad4d6354a
topicBrowsingSortDate: 2018-07-23T06:02:55.130-0400
index: y
internal: n
snippet: y
---

# Return to sender

Return to sender

Flat file exchanges with Direct Mail providers incorporating Return to Sender information are supported. This allows corresponding postal addresses to be excluded from future communications. This also allows you to be notified of an incorrect address and engage with the customer through other channels or to encourage him to update his postal address.

For example, a contact has moved to a new place and did not provide you with his new postal address. The provider retrieves the list of erroneous addresses and sends this information to Adobe Campaign which automatically blacklists the erroneous addresses.

In order for this functionality to work, the direct mail default delivery template includes, in the content, the delivery log ID. Thus, Adobe Campaign will be able to synchronize the profile and delivery data with the information returned by the provider.

![](assets/direct_mail_return_sender_1.png)

An import template is available under **Adobe Campaign > Resources > Templates > Import templates > Update Direct Mail quarantines and delivery logs**. Duplicate this template to create your own. For more on using import templates, refer to [Using import templates](../../automating/using/defining-import-templates.md).

![](assets/direct_mail_return_sender_2.png)

When the import is done, Adobe Campaign automatically performs the following actions:

* Incorrect addresses are blacklisted at the profile level
* The delivery main indicators (KPIs) are updated
* The delivery logs are updated
