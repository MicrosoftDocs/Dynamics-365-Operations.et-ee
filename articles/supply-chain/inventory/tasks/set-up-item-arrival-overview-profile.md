---
title: Kauba saabumise ülevaateprofiili seadistamine
description: Selles teemas keskendutakse saabumise ülevaate profiilile.
author: ShylaThompson
manager: AnnBe
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1c6bcbb71f52e0ec5f979f8d79c896d10689a1b
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867220"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="b59f8-103">Kauba saabumise ülevaateprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="b59f8-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b59f8-104">Selles teemas keskendutakse saabumise ülevaate profiilile.</span><span class="sxs-lookup"><span data-stu-id="b59f8-104">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="b59f8-105">Saabumisülevaate profiil on kogumik reegleid, mida rakendatakse, kui kasutaja avaneb lehe Saabumisülevaade.</span><span class="sxs-lookup"><span data-stu-id="b59f8-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="b59f8-106">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="b59f8-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="b59f8-107">Seda protseduuri viib tavaliselt läbi vastuvõtuametnik.</span><span class="sxs-lookup"><span data-stu-id="b59f8-107">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="b59f8-108">Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Jaotus > Saabumise ülevaate profiilid**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-108">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="b59f8-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-109">Select **New**.</span></span> <span data-ttu-id="b59f8-110">Kuna töötate täis veokikoormate mahalaadimisel peaaegu alati samas laos, peaksite looma saabuvate kaupade registreerimise lihtsustamiseks saabumisülevaate profiili.</span><span class="sxs-lookup"><span data-stu-id="b59f8-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="b59f8-111">Trükkige väärtus väljale **Saabumise ülevaate profiili nimi**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-111">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="b59f8-112">Valige suvand väljal **Näita ridu**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-112">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="b59f8-113">Valige milliseid ridu näidata kviitungitel.</span><span class="sxs-lookup"><span data-stu-id="b59f8-113">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="b59f8-114">**Kõik** – näitab kõiki ridu, olenemata olekust.</span><span class="sxs-lookup"><span data-stu-id="b59f8-114">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="b59f8-115">**Töötluses** – näitab kviitungitel kõiki ridu, millel on töötlemine kas lõpetatud või osaline.</span><span class="sxs-lookup"><span data-stu-id="b59f8-115">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="b59f8-116">See tähendab, et iga rea puhul on saabumistöölehele registreeritud täielik või osaline kogus.</span><span class="sxs-lookup"><span data-stu-id="b59f8-116">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="b59f8-117">**Lõpetamata** – näitab kviitungitel kõiki ridu, millel on töötlemine kas puudu või osaline.</span><span class="sxs-lookup"><span data-stu-id="b59f8-117">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="b59f8-118">See tähendab, et iga rea puhul on saabumistöölehele registreeritud mitte midagi või ainult osa kogusest.</span><span class="sxs-lookup"><span data-stu-id="b59f8-118">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="b59f8-119">Jaotise **Saabumise suvandid** laiendamine või ahendamine.</span><span class="sxs-lookup"><span data-stu-id="b59f8-119">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="b59f8-120">Sisestage väärtus väljale **Päevi edasi**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-120">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="b59f8-121">See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse järgmise paari päeva jooksul (olenevalt teie määratud numbrist).</span><span class="sxs-lookup"><span data-stu-id="b59f8-121">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="b59f8-122">Sisestage väärtus väljale **Päevi tagasi**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-122">In the **Days back** field, type a value.</span></span> <span data-ttu-id="b59f8-123">See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse arv päevi enne tänast.</span><span class="sxs-lookup"><span data-stu-id="b59f8-123">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="b59f8-124">Sisestage väärtus väljale **Laod**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-124">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="b59f8-125">Saate filtreerida ühe või mitme lao alusel.</span><span class="sxs-lookup"><span data-stu-id="b59f8-125">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="b59f8-126">Valige väärtus väljal **Tarneviis**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-126">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="b59f8-127">See määrab filtri kuvama ainult selle tarneviisiga sissetulekuread.</span><span class="sxs-lookup"><span data-stu-id="b59f8-127">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="b59f8-128">Valige WHS väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-128">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="b59f8-129">Valige ladu 24 väljal **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-129">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="b59f8-130">See on vaikeladu, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.</span><span class="sxs-lookup"><span data-stu-id="b59f8-130">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="b59f8-131">Valige väljal **Asukoht** suvand **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-131">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="b59f8-132">See on vaikeasukoht, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.</span><span class="sxs-lookup"><span data-stu-id="b59f8-132">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="b59f8-133">Jaotise **Saabumise päringu üksikasjad** laiendamine või ahendamine.</span><span class="sxs-lookup"><span data-stu-id="b59f8-133">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="b59f8-134">Valige koht 2 väljal **Piira kohaga**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-134">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="b59f8-135">See määrab filtri kuvama ainult selle tegevuskohaga sissetulekuread.</span><span class="sxs-lookup"><span data-stu-id="b59f8-135">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="b59f8-136">Määrake suvandi **Ostutellimused** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-136">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="b59f8-137">Saate valida sissetulekuridu ostutellimustest.</span><span class="sxs-lookup"><span data-stu-id="b59f8-137">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="b59f8-138">Määrake suvandi tellimuste **Edastus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-138">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="b59f8-139">Saate valida sissetulekuridu üleviimistellimustest.</span><span class="sxs-lookup"><span data-stu-id="b59f8-139">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="b59f8-140">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b59f8-140">Select **Save**.</span></span>
18. <span data-ttu-id="b59f8-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b59f8-141">Close the page.</span></span>

