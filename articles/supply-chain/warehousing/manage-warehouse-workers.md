---
title: "Laotöötajate haldamine"
description: "Selles artiklis kirjeldatakse, kuidas saate kasutada Dynamics 365 for Finance and Operationsit nii, et see aitab kontrollida ja jälgida ladude töötajate tehtavat tööd."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmWorker, InventLocation, WHSLaborStandards, WHSWorker, WHSWorkTable, WHSWorkTableListPage
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 72891
ms.assetid: feaa6f15-49d2-41f5-9b87-453463c52e4e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 97f70bf2f122ee06900a1a9b930d29aab5ce4b25
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="manage-warehouse-workers"></a><span data-ttu-id="f6876-103">Laotöötajate haldamine</span><span class="sxs-lookup"><span data-stu-id="f6876-103">Manage warehouse workers</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f6876-104">Selles artiklis kirjeldatakse, kuidas saate kasutada Microsoft Dynamics 365 for Finance and Operations, Enterprise editionit nii, et see aitab kontrollida ja jälgida ladude töötajate tehtavat tööd.</span><span class="sxs-lookup"><span data-stu-id="f6876-104">This article describes how you can use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to help control and monitor the work that's carried out by employees in your warehouses.</span></span>

<span data-ttu-id="f6876-105">Kui kasutate funktsiooni jaotises Laohaldus, viidatakse kõikidele laotöötaja toimingutele sõnaga *töö*.</span><span class="sxs-lookup"><span data-stu-id="f6876-105">If you're using the functionality in Warehouse management, all warehouse worker operations are referred to as *work*.</span></span> <span data-ttu-id="f6876-106">Töö, nagu komplekteerimine, teisaldamine ja vabade laovarude inventuur, salvestatakse mobiilse seadmega.</span><span class="sxs-lookup"><span data-stu-id="f6876-106">Work such as picking, moving, and counting on-hand inventory is recorded by using mobile devices.</span></span> <span data-ttu-id="f6876-107">Enne kui laotöötaja saab tööd teha, peab ta olema jaotises Inimressursid töötajaga seostatud.</span><span class="sxs-lookup"><span data-stu-id="f6876-107">Before a warehouse worker can perform work, he or she must be associated with a worker in Human resources.</span></span> <span data-ttu-id="f6876-108">Iga kontoga **Töötaja** võib olla seostatud mitu laotöö kasutajat.</span><span class="sxs-lookup"><span data-stu-id="f6876-108">Each **Worker** account can have multiple warehouse work users associated with it.</span></span> <span data-ttu-id="f6876-109">Need töökasutajad võivad töötada erinevates ladudes ja neil võib olla erinevatele mobiilse seadme menüüdele erinev juurdepääsutase.</span><span class="sxs-lookup"><span data-stu-id="f6876-109">Those work users can work in different warehouses and can have different levels of access to the various mobile device menus.</span></span> <span data-ttu-id="f6876-110">Laotöö kasutajatest võib mõelda kui valitud töötaja mitmest logimisnimest.</span><span class="sxs-lookup"><span data-stu-id="f6876-110">You can think of the warehouse work users as multiple logons for the selected worker.</span></span> <span data-ttu-id="f6876-111">Igal töö kasutajal on vaikeladu ja selle töö kasutajale saadaolevate menüü-üksused kasutavad konkreetseid töövooge.</span><span class="sxs-lookup"><span data-stu-id="f6876-111">Each work user has a default warehouse, and specific workflows are exposed by the menus items that are available to that work user.</span></span> 

<span data-ttu-id="f6876-112">Uue töö kasutaja loomiseks klõpsake lehe **Töötajad** vahekaardi **Üldine** jaotises **Laod** suvandit **Töötaja**.</span><span class="sxs-lookup"><span data-stu-id="f6876-112">To create a new work user, on the **Workers** page, on the **General** tab, in the **Warehouses** section, click **Worker**.</span></span> <span data-ttu-id="f6876-113">Peate määrama kasutaja ID, kasutajanime, vaikelao ja menüü nime.</span><span class="sxs-lookup"><span data-stu-id="f6876-113">You must specify a user ID, a user name, a default warehouse, and a menu name.</span></span> <span data-ttu-id="f6876-114">See menüü laaditakse, kui kasutaja logib sisse lao mobiilsete seadmete portaali ja laseb teil määratleda, millistele menüü-üksustele kasutajal juurdepääs on.</span><span class="sxs-lookup"><span data-stu-id="f6876-114">This menu is loaded when the user signs in to the Warehouse Mobile Device Portal, and lets you define which menu items the user has access to.</span></span> 

<span data-ttu-id="f6876-115">Iga töö kasutaja seadistuse osana saate määratleda ka konkreetsed protsessi töövood.</span><span class="sxs-lookup"><span data-stu-id="f6876-115">As part of the setup for each work user, you can also define specific process workflows.</span></span> <span data-ttu-id="f6876-116">Näiteks saate kasutada välja **On tsüklilise inventuuri ülevaataja** määramaks, kas kasutaja saab korrigeerimisi töödela inventuuri ajal inventuuri lahknemiste tsükli kaupa läbimisel või kas need korrigeerimised tuleb enne teise isiku poolt üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="f6876-116">For example, you can use the **Is a cycle count supervisor** field to specify whether the user can process adjustments to cycle counting discrepancies during a counting operation, or whether these adjustments must first be reviewed by another person.</span></span>

## <a name="defining-labor-standards"></a><span data-ttu-id="f6876-117">Tööstandardite määratlemine</span><span class="sxs-lookup"><span data-stu-id="f6876-117">Defining labor standards</span></span>
<span data-ttu-id="f6876-118">Leht **Tööstandardid** võimaldab teil määratleda arvutamismeetodid, mida süsteem kasutab kindlat tüüpi töö jaoks vajaminema hinnangulise aja arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="f6876-118">The **Labor standards** page lets you define the calculation methods that the system uses to calculate the estimated time that a particular type of work should require.</span></span> <span data-ttu-id="f6876-119">Selle määratluse saab seada üldisele või konkreetsele tasemele.</span><span class="sxs-lookup"><span data-stu-id="f6876-119">This definition can be set on a generic level or on a specific level.</span></span> <span data-ttu-id="f6876-120">Näiteks saate määratleda aja, mis on vajalik müügitellimuse komplekteerimise töötlemiseks kaalu järgi kindla üksuse määratlusele, kui kasutatakse kindlat komplekteerimisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="f6876-120">For example, you can define the time that should be required in order to process a sales order pick per weight for a specific unit definition when a specific picking process is used.</span></span> <span data-ttu-id="f6876-121">Samal ajal saate salvestada aja muu arvutamisviisi alusel komplekteeritud vaba kaubavaruga asetamistoimingu puhul.</span><span class="sxs-lookup"><span data-stu-id="f6876-121">At the same time, you can record the time, based on another calculation method, for the put operation of the on-hand inventory that is picked.</span></span> 

<span data-ttu-id="f6876-122">Enda määratletud tööstandardite lubamiseks peate valima suvandi **Luba tööstandardid** igale laole, kus tööstandardeid kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="f6876-122">To enable the labor standards that you've defined, you must select the **Allow labor standards** option for each warehouse where labor standards will be used.</span></span>

## <a name="monitoring-and-controlling-warehouse-work"></a><span data-ttu-id="f6876-123">Laotöö seire ja kontrollimine</span><span class="sxs-lookup"><span data-stu-id="f6876-123">Monitoring and controlling warehouse work</span></span>
<span data-ttu-id="f6876-124">Leht **Kogu töö** võimaldab teil kogu plaanitud, töös olevat ja lõpetatud tööd jälgida ja säilitada.</span><span class="sxs-lookup"><span data-stu-id="f6876-124">The **All work** page lets you monitor and maintain all work that is planned, in progress, and completed.</span></span> <span data-ttu-id="f6876-125">Sellel lehel saate värskendada erinevaid protsesse, nagu laotöö kasutaja määramised ja töö prioriteet.</span><span class="sxs-lookup"><span data-stu-id="f6876-125">From this page, you can update various processes, such as warehouse work user assignments and work priority.</span></span> <span data-ttu-id="f6876-126">Samuti saate süveneda töö päise ja töö ridadega seotud üksikasjadesse, et mõista eeldatavast või lõpetatud tööprotsessidest.</span><span class="sxs-lookup"><span data-stu-id="f6876-126">You can also drill down into the details that are related to the work header and work lines to gain an understanding of the expected or completed work processes.</span></span> 

<span data-ttu-id="f6876-127">Kui lubate suvandi **Tööstandardid**, näete töö arvutatud hinnangulist aega.</span><span class="sxs-lookup"><span data-stu-id="f6876-127">If you enable the **Labor standards** option, you can see the calculated estimated time for the work.</span></span> <span data-ttu-id="f6876-128">Kui tööd tehakse, kuvatakse iga töötoimingu puhul ka tegelik aeg.</span><span class="sxs-lookup"><span data-stu-id="f6876-128">Then, when the work is processed, the actual time will also be shown for each work operation.</span></span> <span data-ttu-id="f6876-129">Nii saate võrrelda hinnangulist ajaarvutust tegeliku ajaga estimated.</span><span class="sxs-lookup"><span data-stu-id="f6876-129">In this way, you can compare the estimated time calculations to the actual time.</span></span> 

<span data-ttu-id="f6876-130">Lisaks saate kasutada hinnangulist aega töö loomisel töö automaatse jagamise reeglites.</span><span class="sxs-lookup"><span data-stu-id="f6876-130">Additionally, you can use the estimated time in the rules for automatically splitting work during work creation.</span></span> <span data-ttu-id="f6876-131">Nii saate laadida taskaalustatud töö hinnagulise ülesannete täitmiseks kuluva aja alusel.</span><span class="sxs-lookup"><span data-stu-id="f6876-131">In this way, you can load balance work, based on the expected time to complete the tasks.</span></span> 

<span data-ttu-id="f6876-132">Tööüksuste töötlemiseks kasutatav aja analüüs aitab täiustada laotöötaja tõhusust.</span><span class="sxs-lookup"><span data-stu-id="f6876-132">Analysis of the time that is used to process work items can help drive improvements in the warehouse workers’ efficiency.</span></span> <span data-ttu-id="f6876-133">Analüüsi aitavad teostada järgmised saadaolevad aruanded.</span><span class="sxs-lookup"><span data-stu-id="f6876-133">The following reports are available to help with this analysis:</span></span>

-   <span data-ttu-id="f6876-134">**Töö kasutaja alusel** – see aruanne näitab töötaja tootlikkust eeldatud aja ja tegeliku aja võrdluse alusel.</span><span class="sxs-lookup"><span data-stu-id="f6876-134">**Labor by user** – This report shows worker productivity, based on actual times against expected times.</span></span>
-   <span data-ttu-id="f6876-135">**Töö tehingu tüübi alusel** – kasutage seda aruannet kindlate laoprotsesside puudujääkide uurimiseks.</span><span class="sxs-lookup"><span data-stu-id="f6876-135">**Labor by work transaction type** – You can use this report to investigate inefficiencies in specific warehouse processes.</span></span> <span data-ttu-id="f6876-136">Näiteks märkate, et üleviimistellimuste komplekteerimised võtavad sel nädalal kauem aega kui eelmisel nädalal.</span><span class="sxs-lookup"><span data-stu-id="f6876-136">For example, you notice that picks for transfer orders are taking longer this week than in previous weeks.</span></span> <span data-ttu-id="f6876-137">Seda teavet saate kasutada edasiseks uurimiseks.</span><span class="sxs-lookup"><span data-stu-id="f6876-137">You can then use this information for further investigation.</span></span>





