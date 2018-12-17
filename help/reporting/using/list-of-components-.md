---
title: List of components 
seo-title: List of components 
description: List of components 
seo-description: Find here the list of every components available in Dynamic reports as well as their definitions.
page-status-flag: never-activated
uuid: 0aebb00f-da02-496d-b725-77a058cb9f8d
contentOwner: sauviat
products: SG_CAMPAIGN/STANDARD
audience: reporting
content-type: reference
topic-tags: about-reporting
discoiquuid: 75479206-1b9f-4d58-be22-d38ce91030bd
isreadyforlocalization: true
index: y
internal: n
snippet: y
---

# List of components {#list-of-components}

List of components

## Dimensions {#dimensions}

The table below gives you the list of dimensions used in reports and their definitions.

<table> 
 <thead> 
  <tr> 
   <th> Dimension<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Browser<br /> </td> 
   <td> Browser from which the message was opened or clicked on.<br /> </td> 
  </tr> 
  <tr> 
   <td> Campaign<br /> </td> 
   <td> Label and ID of your campaign.<br /> </td> 
  </tr> 
  <tr> 
   <td> City<br /> </td> 
   <td> City registered in the recipient's profile.<br /> </td> 
  </tr> 
  <tr> 
   <td> Country<br /> </td> 
   <td> Country registered in the recipient's profile.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivery<br /> </td> 
   <td> Label and ID of the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Device<br /> </td> 
   <td> Device from which the message was opened or clicked on.<br /> </td> 
  </tr> 
  <tr> 
   <td> Gender<br /> </td> 
   <td> Recipient's gender such as male or female. If the gender field is empty in the recipient's profile, the value will be none.<br /> </td> 
  </tr> 
  <tr> 
   <td> Message type<br /> </td> 
   <td> Channel used for the delivery, such as email, SMS or push notification.<br /> </td> 
  </tr> 
  <tr> 
   <td> Platform<br /> </td> 
   <td> Platform of the device from which the message was opened or clicked on.<br /> </td> 
  </tr> 
  <tr> 
   <td> Profiles<br /> </td> 
   <td> Regroups out-of-the-box and custom profile fields created during the profile resource extension, for more on this refer to this <a href="../../developing/using/key-steps.md">page</a> or this <a href="../../reporting/using/creating-a-custom-profile-dimension.md">example</a>.<br /> Note that data for this dimension is retrieved as soon as the custom resource linked to the profile field is published.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push notification Mobile App<br /> </td> 
   <td> Mobile app ID of the push notification.<br /> </td> 
  </tr> 
  <tr> 
   <td> Push platform<br /> </td> 
   <td> Platform of the device from which the push notification was opened, such as iOS or Android.<br /> </td> 
  </tr> 
  <tr> 
   <td> Recipient domain<br /> </td> 
   <td> Domain used to open the email.<br /> </td> 
  </tr> 
  <tr> 
   <td> Recurring delivery<br /> </td> 
   <td> Label and ID of the recurring delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Sender domain<br /> </td> 
   <td> Domain used to send the email.<br /> </td> 
  </tr> 
  <tr> 
   <td> Sender IP<br /> </td> 
   <td> IP used to send the email.<br /> </td> 
  </tr> 
  <tr> 
   <td> State<br /> </td> 
   <td> State registered in the recipient's profile.<br /> </td> 
  </tr> 
  <tr> 
   <td> Tracking URL<br /> </td> 
   <td> URL that was clicked on by the user from the message.<br /> </td> 
  </tr> 
  <tr> 
   <td> Tracking URL category<br /> </td> 
   <td> Category assigned to the tracking URL.<br /> </td> 
  </tr> 
  <tr> 
   <td> Tracking URL label<br /> </td> 
   <td> Label given to the URL, such as mirror page, contact us or open.<br /> </td> 
  </tr> 
  <tr> 
   <td> Transactional delivery<br /> </td> 
   <td> Label and ID of the transactional delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Variant<br /> </td> 
   <td> Variant of the email in case of A/B testing.<br /> </td> 
  </tr> 
  <tr> 
   <td> Zip code<br /> </td> 
   <td> Zip code registered in the recipient's profile.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Metrics {#metrics}

The table below gives you the list of metrics used in reports and their definitions.

<table> 
 <thead> 
  <tr> 
   <th> Metric<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Blacklisted<br /> </td> 
   <td> Number of recipients who have declared an email as spam or junk.<br /> </td> 
  </tr> 
  <tr> 
   <td> Blacklisted rate<br /> </td> 
   <td> Percentage of deliveries marked as blacklisted.<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounces + Errors<br /> </td> 
   <td> Total of errors cumulated during delivery and automatic return processing in relation to the total number of sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Bounce + Error rate<br /> </td> 
   <td> Percentage of emails that bounced compared to email sent.<br /> </td> 
  </tr> 
  <tr> 
   <td> Click<br /> </td> 
   <td> Number of times a content was clicked in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Click through rate<br /> </td> 
   <td> Percentage of clicks in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered<br /> </td> 
   <td> Number of messages successfully sent, in relation to the total number of sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Delivered rate<br /> </td> 
   <td> Percentage of messages successfully sent.<br /> </td> 
  </tr> 
  <tr> 
   <td> Hard bounce<br /> </td> 
   <td> Total number of permanent errors, such as a wrong email address.<br /> </td> 
  </tr> 
  <tr> 
   <td> Hard bounce rate<br /> </td> 
   <td> Percentage of deliveries that failed due to permanent errors.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mirror page<br /> </td> 
   <td> Number of recipients who clicked on the mirror page link.<br /> </td> 
  </tr> 
  <tr> 
   <td> Mirror page rate<br /> </td> 
   <td> Percentage of clicks on the mirror page link compared to the total delivery messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Open<br /> </td> 
   <td> Number of times a message was opened in a delivery<br /> </td> 
  </tr> 
  <tr> 
   <td> Open rate<br /> </td> 
   <td> Percentage of opened messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Quarantine<br /> </td> 
   <td> Number of messages that bounced and resulted in the quarantine of the address.<br /> </td> 
  </tr> 
  <tr> 
   <td> Quarantine rate<br /> </td> 
   <td> Percentage of quarantines compared to sent messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Rejected<br /> </td> 
   <td> Number of messages classified as spam by the SMTP servers.<br /> </td> 
  </tr> 
  <tr> 
   <td> Rejected rate<br /> </td> 
   <td> Percentage of messages marked as rejected.<br /> </td> 
  </tr> 
  <tr> 
   <td> Sent<br /> </td> 
   <td> Total number of sends for the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Soft bounce<br /> </td> 
   <td> Total number of temporary errors, such as a full inbox.<br /> </td> 
  </tr> 
  <tr> 
   <td> Soft bounce rate<br /> </td> 
   <td> Percentage of deliveries that failed due to temporary reason.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique Clicks<br /> </td> 
   <td> Number of recipients who clicked on a content in a delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unique Opens<br /> </td> 
   <td> Number of recipients who opened the delivery.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unsubscribe rate<br /> </td> 
   <td> Percentage of unsubscriptions by recipient compared to the delivered messages.<br /> </td> 
  </tr> 
  <tr> 
   <td> Unsubscribed<br /> </td> 
   <td> Number of clicks on the unsubscription link.<br /> </td> 
  </tr> 
 </tbody> 
</table>

## Segments {#segments}

The table below gives you the list of segments used in reports and their definitions.

<table> 
 <thead> 
  <tr> 
   <th> Segment<br /> </th> 
   <th> Definition<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td> Age: Boomers 1<br /> </td> 
   <td> Recipients born from 1946 to 1954.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Boomers 2<br /> </td> 
   <td> Recipients born from 1955 to 1965.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: From 18 to 25<br /> </td> 
   <td> Recipients from 18 to 25 years old.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: From 26 to 30<br /> </td> 
   <td> Recipients from 26 to 30 years old.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: From 31 to 40<br /> </td> 
   <td> Recipients from 31 to 40 years old.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: From 41 to 50<br /> </td> 
   <td> Recipients from 41 to 50 years old.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Generation X<br /> </td> 
   <td> Recipients born from 1966 to 1976.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Generation Y (Millennials)<br /> </td> 
   <td> Recipients born from 1977 to 1994.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Generation Z<br /> </td> 
   <td> Recipients born from 1995 to today.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Greater than 50<br /> </td> 
   <td> Recipients whose age is greater than 50.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Less than 25<br /> </td> 
   <td> Recipients whose age is less than 25.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Less than 30<br /> </td> 
   <td> Recipients whose age is less than 30.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Less than 40<br /> </td> 
   <td> Recipients whose age is less than 40.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Less than 50<br /> </td> 
   <td> Recipients whose age is less than 50.<br /> </td> 
  </tr> 
  <tr> 
   <td> Age: Silent Generation<br /> </td> 
   <td> Recipients born in 1945 or before.<br /> </td> 
  </tr> 
  <tr> 
   <td> All visits<br /> </td> 
   <td> Every recipient<br /> </td> 
  </tr> 
 </tbody> 
</table>
