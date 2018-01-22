---
# required metadata

title: Intune mobile device management migration guide
description: This guide walks you through the various details involved in migrating from a third-party MDM provider to Microsoft Intune.
keywords:
author: andredm7
ms.author: andredm
manager: angrobe
ms.date: 07/11/2017
ms.topic: article
ms.prod:
ms.service: microsoft-intune
ms.technology:
ms.assetid: dcfc21f9-1bcd-4371-a46d-f2e18154ec50

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: dagerrit
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Intune migration guide

![Intune MDM migration guide art](./media/MDM-migration-guide-art.PNG)

A successful migration to Intune starts with a solid plan that factors in your current mobile device management (MDM) environment, business goals, and technical requirements. Additionally, you need to have the key stakeholders whose will support and collaborate with your migration plan.

This guide walks you through the various details involved in migrating from a third-party MDM provider to Intune.

## What’s included in this guide?

This guide breaks down the migration into two phases, both of which include tasks, strategies, and tactical guidance that will help you step through the end-to-end process of migrating to Intune MDM.

-   [Phase 1: Prepare Intune for mobile device management](migration-guide-prepare.md)

    -   [Assess your MDM migration requirements](migration-guide-prepare.md#assess-mdm-requirements)

    -   [Basic setup](migration-guide-setup.md)

    -   [Configure device and app management policies](migration-guide-configure-policies.md)

    -   [Configure app protection policies](migration-guide-app-protection-policies.md)

    -   [Special migration considerations](migration-guide-considerations.md)

-   [Phase 2: Migration campaign](migration-guide-campaign.md)

    -   [Communication plan](migration-guide-communication-plan.md)

    -   [Drive end-user adoption with conditional access](migration-guide-drive-adoption.md)

    -   [Typical migration cycle](migration-guide-cycle.md)
        -   [Monitoring migration](migration-guide-cycle.md#monitoring-migration)
        -   [Post migration](migration-guide-cycle.md#post-migration)

## Assumptions

-   You've already evaluated Intune in a proof of concept (PoC) environment, and have decided to use it as the MDM solution in your organization.

-   You are already familiar with Intune and its features.

## Before you begin

It's important to recognize that your new Intune deployment might be different from your old MDM deployment. Unlike traditional MDM services, Intune centers on identity-driven access control, and so does not require a network proxy appliance to control access to corporate data from mobile devices outside the organization's network perimeter. Microsoft offers solutions to secure data services within the cloud itself through a suite of tightly integrated cloud services, collectively referred to as the Enterprise Client + Security offering.

-   Review the [common ways to use Intune](common-scenarios.md).

## Next steps

[Phase 1: Prepare Intune for mobile device management](migration-guide-prepare.md)
