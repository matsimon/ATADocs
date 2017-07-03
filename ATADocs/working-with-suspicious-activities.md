---
# required metadata

title: Working with suspicious activities in Advanced Threat Analytics | Microsoft Docs
description: Describes how to review suspicious activities identified by ATA
keywords:
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 06/23/2017
ms.topic: article
ms.prod:
ms.service: advanced-threat-analytics
ms.technology:
ms.assetid: 44d7c899-816c-4f7f-91d3-84a09d291a24

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: bennyl
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

*Applies to: Advanced Threat Analytics version 1.8*



# Working with Suspicious Activities
This topic explains the basics of how to work with Advanced Threat Analytics.

## Review suspicious activities on the attack time line
After logging in to the ATA Console, you are automatically taken to the open **Suspicious Activities Time Line**. Suspicious activities are listed in chronological order with the newest suspicious activities on the top of the time line.
Each suspicious activity has the following information:

-   Entities involved, including users, computers, servers, domain controllers, and resources.

-   Times and time frame of the suspicious activities.

-   Severity of the suspicious activity, High, Medium, or Low.

-   Status: Open, closed, or suppressed.

-   Ability to

    -   Share the suspicious activity with other people in your organization via email.

    -   Export the suspicious activity to Excel.

    -   Add a note to the suspicious activity.

    -   Provide input on the suspicious activity.

-   Provides recommendations for how to respond to the suspicious activity.

> [!NOTE]
> -   When you hover your mouse over a user or computer, an entity mini-profile is displayed that provides additional information about the entity and includes the number of suspicious activities that the entity is linked to.
> -   If you click on an entity, it will take you to the entity profile of the user or computer.

![ATA suspicious activities timeline image](media/ATA-Suspicious-Activity-Timeline.JPG)

## Filter suspicious activities list
To filter the suspicious activities list:

1.  In the **Filter by** pane on the left side of the screen, select one of the following: **All**, **Open**, **Resolved**, or **Dismissed**.

2.  To further filter the list, select **High**, **Medium** or **Low**.

**Suspicious activity severity**

-   **Low**

    Indicates suspicious activities that can lead to attacks designed for malicious users or software to gain access to organizational data.

-   **Medium**

    Indicates suspicious activities that can put specific identities at risk for more severe attacks that could result in identity theft or privileged escalation

-   **High**

    Indicates suspicious activities that can lead to identity theft, privilege escalation or other high-impact attacks




## Remediating suspicious activities
You can change the status of a suspicious activity by clicking the current status of the suspicious activity and selecting one of the following **Open**, **Suppressed**, **Closed** or **Deleted**.
To do this, click the three dots at the top right corner of a specific suspicious activity to reveal the list of available actions.

![ATA Actions for suspicious activities](./media/sa-actions.png)

**Suspicious activity status**

-   **Open**: All new suspicious activities appear in this list.

-   **Close**: Is used to track suspicious activities which you identified, researched and fixed for mitigated.

    > [!NOTE]
    > ATA may reopen a resolved activity if it the same activity is detected again within a short period of time.

-   **Suppress**: Suppressing an activity means you want to ignore it for now, and only be alerted again if there's a new instance. This means that if there's a similar alert ATA won't reopen it. But if the alert stops for 7 days, and is then seen again, you will be alerted again.

- **Delete**: If you Delete an alert, it will be deleted from the system, from the database and you will NOT be able to restore it. After you click delete, you'll be able to delete all suspicious activities of the same type.

- **Exclude**: The ability to exclude an entity from raising more of a certain type of alerts. For example, you can set ATA to exclude a specific entity (user or computer) from alerting again for a certain type of suspicious activity, such as a specific admin who runs remote code or a security scanner that does DNS reconnaissance. In addition to being able to add exclusions directly on the Suspicious activity as it is detected in the time line, you can also go to the Configuration page to **Exclusions**, and for each suspicious activity you can manually add and remove excluded entities or subnets (for example for Pass-the-Ticket). 
> [!NOTE]
> The configuration pages can only be modified by ATA admins.


## See Also
- [Check out the ATA forum!](https://social.technet.microsoft.com/Forums/security/home?forum=mata)
- [Working with ATA detection settings](working-with-detection-settings.md)
- [Modifying ATA configuration](modifying-ata-center-configuration.md)