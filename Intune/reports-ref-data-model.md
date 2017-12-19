---
# required metadata
title: Data Warehouse data model | Microsoft Docs 
description: The Intune Data Warehouse samples data daily to provide a historical view of your continually changing mobile environment.
keywords: Intune Data Warehouse
author: mattbriggs
ms.author: mabrigg
manager: angrobe
ms.date: 11/14/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: 4D04D3D9-4B6C-41CD-AAF8-466AF8FA6032

# optional metadata
#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: jeffgilb
ms.suite: ems
#ms.tgt_pltfrm:
ms.custom: intune-classic
---

# Data Warehouse data model

The Intune Data Warehouse samples data daily to provide a historical view of your continually changing environment of mobile devices. The view is composed of related things in time.

## Things: Entity sets

The warehouse exposes data in the following high-level areas:

  -  App protection enabled apps and usage
  -  Enrolled devices, properties, and inventory
  -  Apps and software inventory
  -  Device configuration and compliance policies

These areas contain the entities, or things, that are meaningful to your Intune environment. You find details about the entity sets in the following topics:

  -  [Application](reports-ref-application.md)
  -  [Date](reports-ref-date.md)
  -  [Devices](reports-ref-devices.md)
  -  [Intune Management Extension](reports-ref-intunemanagementextension.md)
  -  [Policy](reports-ref-policy.md)
  -  [Mobile App Management (MAM)](reports-ref-mobile-app-management.md)
  -  [User](reports-ref-user.md)
  -  [Current User](reports-ref-current-user.md)
  -  [User Device Associations](reports-ref-user-device.md)

## Relationships: Star-schema model

The warehouse organizes the entities in relationships that are meaningful to the type of questions you want to ask. For example, you can review the number of installations of an in-house developed Android application. The structure of the data warehouse enables you to gain insight into your mobile environment. In turn, analytics tools, such as Microsoft Power BI, can use the Data Warehouse data model to create visualizations and dynamic dashboards.

The entities and relationships use a star-schema model. A star-schema correlates facts over the dimension of time. A *fact* in the context of the model is a quantitative measurement such as the number of devices, number of apps, or time of enrollment. Fact tables store a lot of data. They can get very large, and so they typically limit information to 30 days. A *dimension* provides context to the facts. Where the fact measures what happened, the dimensions indicate to whom it happened. Dimension tables, such as the like the **User** table are smaller and can retrain data for longer periods of time= than fact tables. 

A star-schema model is optimized for flexibility and data analysis so that you can create the reports needed to understand your evolving mobile environment.

## Time: Daily snapshots

The warehouse is downstream from your Intune data. Intune takes a daily snapshot at Midnight UTC and stores the snapshot in the warehouse. The duration of held snapshots vary from fact table to fact table. Some may hold seven days, others 30 days, and some even longer durations.

## Next steps

 - To learn more more about how the data warehouse tracks a user's lifetime in Intune, see [User lifetime representation in the Intune Data Warehouse](reports-ref-user-timeline.md).
 - To learn more more about working with data warehouses in the [Create First Data WareHouse](https://www.codeproject.com/Articles/652108/Create-First-Data-WareHouse).
 - To learn more about working with Power BI and a data warehouse in [Create a new Power BI report by importing a dataset](https://powerbi.microsoft.com/documentation/powerbi-service-create-a-new-report/). 
