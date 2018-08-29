--- 
title: "Süsteemi konfigureerimine kasutajatele töövooga seotud meili saatmiseks"
description: "Saate konfigureerida süsteemi saatma kasutajatele meilisõnumeid töövooga seotud sündmuste esinemisel."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 04d90c9ded1ba7fb1ceac4ff1d54f54f6c43f9e9
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="configure-the-system-to-send-workflow-related-email-to-users"></a><span data-ttu-id="0539d-103">Süsteemi konfigureerimine kasutajatele töövooga seotud meili saatmiseks</span><span class="sxs-lookup"><span data-stu-id="0539d-103">Configure the system to send workflow-related email to users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0539d-104">Saate konfigureerida süsteemi saatma kasutajatele meilisõnumeid töövooga seotud sündmuste esinemisel.</span><span class="sxs-lookup"><span data-stu-id="0539d-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="0539d-105">Näiteks e-kirju saab saata kasutajatele kui dokumendid on neile määratud kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="0539d-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="0539d-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="0539d-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="0539d-107">Minge jaotisse Süsteemihaldus > Kasutajad > Kasutajad.</span><span class="sxs-lookup"><span data-stu-id="0539d-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="0539d-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="0539d-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0539d-109">Klõpsake suvandit Kasutaja suvandid.</span><span class="sxs-lookup"><span data-stu-id="0539d-109">Click User options.</span></span>
4. <span data-ttu-id="0539d-110">Klõpsake vahekaarti Töövoog.</span><span class="sxs-lookup"><span data-stu-id="0539d-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="0539d-111">Veenduge, et jaotis Teatised on laiendatud.</span><span class="sxs-lookup"><span data-stu-id="0539d-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="0539d-112">Teatiste jaotises saate määrata, kuidas soovite, et kasutajat teavitatakse töövooga seotud sündmustest.</span><span class="sxs-lookup"><span data-stu-id="0539d-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="0539d-113">Valige suvand väljal Rea kauba töövoo teavitustüüp.</span><span class="sxs-lookup"><span data-stu-id="0539d-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="0539d-114">Grupeeritud – reakaupade teatised grupeeritakse üheks meilisõnumiks.</span><span class="sxs-lookup"><span data-stu-id="0539d-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="0539d-115">Üksik – meilisõnum saadetakse iga rea kauba puhul.</span><span class="sxs-lookup"><span data-stu-id="0539d-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="0539d-116">Kui soovite, et kasutaja saaks klientrakenduses teatisi, märkige ruut Teatiste saatmine meiliga.</span><span class="sxs-lookup"><span data-stu-id="0539d-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="0539d-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0539d-117">Click Save.</span></span>
7. <span data-ttu-id="0539d-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0539d-118">Close the page.</span></span>


