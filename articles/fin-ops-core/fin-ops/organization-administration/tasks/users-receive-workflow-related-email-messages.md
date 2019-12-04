---
title: Luba kasutajatel töövooga seotud e-kirju vastu võtta
description: Saate konfigureerida süsteemi saatma kasutajatele meilisõnumeid töövooga seotud sündmuste esinemisel.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189840"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="4613a-103">Luba kasutajatel töövooga seotud e-kirju vastu võtta</span><span class="sxs-lookup"><span data-stu-id="4613a-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4613a-104">Saate konfigureerida süsteemi saatma kasutajatele meilisõnumeid töövooga seotud sündmuste esinemisel.</span><span class="sxs-lookup"><span data-stu-id="4613a-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="4613a-105">Näiteks e-kirju saab saata kasutajatele kui dokumendid on neile määratud kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="4613a-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="4613a-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="4613a-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="4613a-107">Avage **Navigeerimispaan > Moodulid > Süsteemiadministraator > Kasutajad > Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="4613a-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="4613a-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="4613a-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4613a-109">Klõpsake **Toimingupaneelil** valikut **Kasutajavalikud**.</span><span class="sxs-lookup"><span data-stu-id="4613a-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="4613a-110">Klõpsake vahekaarti **Töövoog** . Veenduge, et jaotis **Teatised** on laiendatud.</span><span class="sxs-lookup"><span data-stu-id="4613a-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="4613a-111">Jaotises **Teatisted** saate määrata, kuidas soovite, et kasutajat teavitatakse töövooga seotud sündmustest.</span><span class="sxs-lookup"><span data-stu-id="4613a-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="4613a-112">Valige suvand väljal **Rea kauba töövoo teavitustüüp**.</span><span class="sxs-lookup"><span data-stu-id="4613a-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="4613a-113">Grupeeritud – reakaupade teatised grupeeritakse üheks meilisõnumiks.</span><span class="sxs-lookup"><span data-stu-id="4613a-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="4613a-114">Üksik – meilisõnum saadetakse iga rea kauba puhul.</span><span class="sxs-lookup"><span data-stu-id="4613a-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="4613a-115">Kui soovite, et kasutaja saaks klientrakenduses teatisi, märkige ruut **Teatiste saatmine meiliga**.</span><span class="sxs-lookup"><span data-stu-id="4613a-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="4613a-116">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4613a-116">Click **Save**.</span></span>
7. <span data-ttu-id="4613a-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4613a-117">Close the page.</span></span>
