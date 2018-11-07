---
title: AND-join
seo-title: AND-join
description: AND-join
seo-description: The AND-join activity allows you to synchronize multiple execution branches of a workflow.
uuid: 9880cbfe-4940-40bd-8ca4-08ca7123f916
content-encoding: ISO-8859-1
aemsrcnodepath: /content/help/en/campaign/standard/automating/using/and-join
contentOwner: sauviat
cq-designpath: /etc/designs/help
cq-lastmodified: 2018-09-10T07 26 20.696-0400
cq-lastreplicated: 2018-09-07T14 59 38.416-0400
cq-lastreplicatedby: sauviat
cq-lastreplicationaction: Activate
products: SG_CAMPAIGN/STANDARD
audience: automating
content-type: reference
topic-tags: execution-activities
cq-template: /apps/help/templates/article-3
discoiquuid: 89683efe-92ea-4e1e-9d26-bb84db0e3e13
firstPublishExternalDate: 2018-09-07T14:59:34.681-0400
herogradient: light
isreadyforlocalization: false
jcr-created: 2018-03-15T09 02 21.420-0400
jcr-createdby: admin
jcr-description: AND-join
jcr-ischeckedout: true
jcr-language: en_us
lastPublishExternalDate: 2018-09-07T14:59:34.681-0400
lochandoffdate: 2018-09-10T07 26 20.695-0400
loclangtag: locales fr;locales de;locales ja
lr-lastreplicatedby: sauviat@adobe.com
navTitle: AND-join
publishexternaldate: 2018-09-07T14 59 34.681-0400
publishExternalURL: https://helpx.adobe.com/campaign/standard/automating/using/and-join.html
sha1: 28f36a7820a9f9d642f7b221a71d88927a8d829a
topicBrowsingSortDate: 2018-09-07T14:59:34.681-0400
index: y
internal: n
snippet: y
---

# AND-join

AND-join

## Description

![](assets/and_join.png)

The **AND-join** activity allows you to synchronize multiple execution branches of a workflow.

## Context of use

The **AND-join** activity only triggers its outbound transition once all the inbound transitions are activated, in other words, once all of the preceding activities have finished.

## Configuration

1. Drop multiple activities such as queries into your workflow to form at least two different execution branches.
1. Drag and drop an **AND-join** activity into your workflow.
1. Connect it after the two different branches that you would like to synchronize.
1. Select the activity, then open it using the  ![](assets/edit_darkgrey-24px.png)

   button from the quick actions that appear.
1. Select the main set to be kept in the outbound transition. If you do not select any set, a random population will be sent from the activity.
1. Confirm the configuration of your activity and save your workflow.

## Example

The following example shows two workflow branches before they are joined with the **AND-join** activity. File extraction can only take place when the three inbound transitions of the **AND-join** activity are enabled.

![](assets/wkf_and-join_example.png)
