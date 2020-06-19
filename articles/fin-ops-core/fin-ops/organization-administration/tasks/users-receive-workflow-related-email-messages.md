---
title: Luba kasutajatel töövooga seotud e-kirju vastu võtta
description: Saate konfigureerida süsteemi saatma kasutajatele meilisõnumeid töövooga seotud sündmuste esinemisel.
author: jasongre
manager: AnnBe
ms.date: 06/01/2020
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
ms.openlocfilehash: 40ad380c7bfb2b3fc518b0278286ae03532668ed
ms.sourcegitcommit: 4db8c30c2f26af1896938dd3ece3756577374ecb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/01/2020
ms.locfileid: "3416549"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="538bb-103">Luba kasutajatel töövooga seotud e-kirju vastu võtta</span><span class="sxs-lookup"><span data-stu-id="538bb-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="538bb-104">Saate konfigureerida süsteemi saatma kasutajatele meilisõnumeid töövooga seotud sündmuste esinemisel.</span><span class="sxs-lookup"><span data-stu-id="538bb-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="538bb-105">Näiteks e-kirju saab saata kasutajatele kui dokumendid on neile määratud kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="538bb-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="538bb-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="538bb-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="538bb-107">Avage **Navigeerimispaan > Moodulid > Süsteemiadministraator > Kasutajad > Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="538bb-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="538bb-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="538bb-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="538bb-109">Klõpsake **Toimingupaneelil** valikut **Kasutajavalikud**.</span><span class="sxs-lookup"><span data-stu-id="538bb-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="538bb-110">Klõpsake vahekaarti **Töövoog** . Veenduge, et jaotis **Teatised** on laiendatud.</span><span class="sxs-lookup"><span data-stu-id="538bb-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="538bb-111">Jaotises **Teatisted** saate määrata, kuidas soovite, et kasutajat teavitatakse töövooga seotud sündmustest.</span><span class="sxs-lookup"><span data-stu-id="538bb-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="538bb-112">Valige suvand väljal **Rea kauba töövoo teavitustüüp**.</span><span class="sxs-lookup"><span data-stu-id="538bb-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="538bb-113">Grupeeritud – reakaupade teatised grupeeritakse üheks meilisõnumiks.</span><span class="sxs-lookup"><span data-stu-id="538bb-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="538bb-114">Üksik – meilisõnum saadetakse iga rea kauba puhul.</span><span class="sxs-lookup"><span data-stu-id="538bb-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="538bb-115">Kui soovite, et kasutaja saaks klientrakenduses teatisi, märkige ruut **Teatiste saatmine meiliga**.</span><span class="sxs-lookup"><span data-stu-id="538bb-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="538bb-116">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="538bb-116">Click **Save**.</span></span>
7. <span data-ttu-id="538bb-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="538bb-117">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="538bb-118">Töövoo meilimallid hangitakse süsteemi meilimallidest või organisatsiooni meilimallidest, sõltuvalt sellest, kas tegemist on süsteemitasandi (mitte ettevõttepõhise) või organisatsioonitasandi (ettevõttepõhise) töövooga.</span><span class="sxs-lookup"><span data-stu-id="538bb-118">The workflow email templates will be sourced from either system email templates or organization email templates depending on whether the workflow is a system-level (not company specific) or organization-level (company specific) workflow.</span></span>
