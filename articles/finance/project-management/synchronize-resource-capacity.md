---
title: Ressursi võimsuse sünkroonimine
description: See teema annab teavet ressursi võimsuse sünkroonimise kohta kalendrite ja projektide vahel.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760522"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="e27e7-103">Ressursi võimsuse sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="e27e7-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e27e7-104">Ressursi sünkroonimise protsessid aitavad tagada, et kalendri ja aluskalendri teave arvestab projekti ressursiplaanimisega.</span><span class="sxs-lookup"><span data-stu-id="e27e7-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="e27e7-105">Kalendri muutmisel teevad protsessid projektiressursside plaanimises vajalikud värskendused.</span><span class="sxs-lookup"><span data-stu-id="e27e7-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="e27e7-106">Protsessid aitavad ka jõudlust parandada, kuna kalendriressursi teave sünkroonitakse eelnevalt.</span><span class="sxs-lookup"><span data-stu-id="e27e7-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="e27e7-107">Seetõttu toimub ressursiplaanimise teabe uuendamine kiiremini.</span><span class="sxs-lookup"><span data-stu-id="e27e7-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="e27e7-108">Soovitame plaanida protsessid ühekordsete asemel partiina.</span><span class="sxs-lookup"><span data-stu-id="e27e7-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="e27e7-109">Vastasel korral on olemas oht, et keegi unustab hõlmavad kuupäevad, millal teavet viimati sünkrooniti.</span><span class="sxs-lookup"><span data-stu-id="e27e7-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="e27e7-110">Kui hõlmavaid kuupäevi ei kasutata, võivad kuupäevade sünkroonimisel tekkida vahed.</span><span class="sxs-lookup"><span data-stu-id="e27e7-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendri sünkroonimine](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="e27e7-112">Ressursi võimsuse kokkuvõtete sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="e27e7-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="e27e7-113">Sünkroonimisprotsess on mõeldud kogu ressursikalendri teabe sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="e27e7-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="e27e7-114">See teave sisaldab peamist kalendriteavet kõigi muudatuste kohta projekti ressursikalendri võimsuse tabelis.</span><span class="sxs-lookup"><span data-stu-id="e27e7-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="e27e7-115">Kui projektile lisatakse uusi ressursse, aitab sünkroonimine tagada, et värskendatud kalendriteave oleks saadaval.</span><span class="sxs-lookup"><span data-stu-id="e27e7-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="e27e7-116">See sünkroonimine võib toimuda igal ajal.</span><span class="sxs-lookup"><span data-stu-id="e27e7-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="e27e7-117">Soovitame kasutada partiid.</span><span class="sxs-lookup"><span data-stu-id="e27e7-117">We recommend that you use a batch.</span></span> <span data-ttu-id="e27e7-118">Need valikud on võimsuse reserveerimiste sünkroonimisel saadaval.</span><span class="sxs-lookup"><span data-stu-id="e27e7-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="e27e7-119">Valige **Projektihaldus ja raamatupidamine** &gt; **Perioodiline** &gt; **Võimsuse sünkroonimine** &gt; **Ressursside võimsuse kokkuvõtete sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="e27e7-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="e27e7-120">Määrake valikud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="e27e7-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="e27e7-121">Suvand</span><span class="sxs-lookup"><span data-stu-id="e27e7-121">Option</span></span>      | <span data-ttu-id="e27e7-122">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e27e7-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="e27e7-123">Perioodi kood</span><span class="sxs-lookup"><span data-stu-id="e27e7-123">Period code</span></span> | <span data-ttu-id="e27e7-124">Soovi korral võite valida pearaamatu kuupäevavahemiku koodi ressursi võimsuse kokkuvõtete sünkroonimisprotsessi alguse ja lõpu kuupäevade määramiseks.</span><span class="sxs-lookup"><span data-stu-id="e27e7-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="e27e7-125">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="e27e7-125">Start date</span></span>  | <span data-ttu-id="e27e7-126">Sisestage ressursi võimsuse kokkuvõtete sünkroonimisprotsessi alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="e27e7-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="e27e7-127">Lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="e27e7-127">End date</span></span>    | <span data-ttu-id="e27e7-128">Sisestage ressursi võimsuse kokkuvõtete sünkroonimisprotsessi lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="e27e7-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="e27e7-129">[![Sünkroonimisprotsess](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="e27e7-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
