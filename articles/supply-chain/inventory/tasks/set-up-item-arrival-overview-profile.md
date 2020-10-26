---
title: Kauba saabumise ülevaateprofiili seadistamine
description: Selles teemas keskendutakse saabumise ülevaate profiilile.
author: ShylaThompson
manager: tfehr
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69389dd3a53ffec11116e16512bd038b45eda4d4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979688"
---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="f0ede-103">Kauba saabumise ülevaateprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="f0ede-103">Set up an item arrival overview profile</span></span>

<span data-ttu-id="f0ede-104">[!include [banner](../../includes/banner.md)]]</span><span class="sxs-lookup"><span data-stu-id="f0ede-104">[!include [banner](../../includes/banner.md)]]</span></span>

<span data-ttu-id="f0ede-105">Selles teemas keskendutakse saabumise ülevaate profiilile.</span><span class="sxs-lookup"><span data-stu-id="f0ede-105">This topic focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="f0ede-106">Saabumisülevaate profiil on kogumik reegleid, mida rakendatakse, kui kasutaja avaneb lehe Saabumisülevaade.</span><span class="sxs-lookup"><span data-stu-id="f0ede-106">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="f0ede-107">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="f0ede-107">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="f0ede-108">Seda protseduuri viib tavaliselt läbi vastuvõtuametnik.</span><span class="sxs-lookup"><span data-stu-id="f0ede-108">This procedure would typically be carried out by a receiving clerk.</span></span>

1. <span data-ttu-id="f0ede-109">Navigeerimispaanil avage **Moodulid > Varude haldus > Seadistus > Jaotus > Saabumise ülevaate profiilid**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-109">In the navigation pane, go to **Modules > Inventory management > Setup > Distribution > Arrival overview profiles**.</span></span>
2. <span data-ttu-id="f0ede-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-110">Select **New**.</span></span> <span data-ttu-id="f0ede-111">Kuna töötate täis veokikoormate mahalaadimisel peaaegu alati samas laos, peaksite looma saabuvate kaupade registreerimise lihtsustamiseks saabumisülevaate profiili.</span><span class="sxs-lookup"><span data-stu-id="f0ede-111">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="f0ede-112">Trükkige väärtus väljale **Saabumise ülevaate profiili nimi**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-112">In the **Arrival overview profile name** field, type a value.</span></span>
4. <span data-ttu-id="f0ede-113">Valige suvand väljal **Näita ridu**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-113">In the **Show lines** field, select an option.</span></span> <span data-ttu-id="f0ede-114">Valige milliseid ridu näidata kviitungitel.</span><span class="sxs-lookup"><span data-stu-id="f0ede-114">Select which lines to show for the receipts:</span></span>  

    - <span data-ttu-id="f0ede-115">**Kõik** – näitab kõiki ridu, olenemata olekust.</span><span class="sxs-lookup"><span data-stu-id="f0ede-115">**All** – Show all lines, regardless of status.</span></span>   
    - <span data-ttu-id="f0ede-116">**Töötluses** – näitab kviitungitel kõiki ridu, millel on töötlemine kas lõpetatud või osaline.</span><span class="sxs-lookup"><span data-stu-id="f0ede-116">**In progress** – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="f0ede-117">See tähendab, et iga rea puhul on saabumistöölehele registreeritud täielik või osaline kogus.</span><span class="sxs-lookup"><span data-stu-id="f0ede-117">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   
    - <span data-ttu-id="f0ede-118">**Lõpetamata** – näitab kviitungitel kõiki ridu, millel on töötlemine kas puudu või osaline.</span><span class="sxs-lookup"><span data-stu-id="f0ede-118">**Not complete** – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="f0ede-119">See tähendab, et iga rea puhul on saabumistöölehele registreeritud mitte midagi või ainult osa kogusest.</span><span class="sxs-lookup"><span data-stu-id="f0ede-119">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  

5. <span data-ttu-id="f0ede-120">Jaotise **Saabumise suvandid** laiendamine või ahendamine.</span><span class="sxs-lookup"><span data-stu-id="f0ede-120">Expand or collapse the **Arrival options** section.</span></span>
6. <span data-ttu-id="f0ede-121">Sisestage väärtus väljale **Päevi edasi**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-121">In the **Days forward** field, type a value.</span></span> <span data-ttu-id="f0ede-122">See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse järgmise paari päeva jooksul (olenevalt teie määratud numbrist).</span><span class="sxs-lookup"><span data-stu-id="f0ede-122">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="f0ede-123">Sisestage väärtus väljale **Päevi tagasi**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-123">In the **Days back** field, type a value.</span></span> <span data-ttu-id="f0ede-124">See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse arv päevi enne tänast.</span><span class="sxs-lookup"><span data-stu-id="f0ede-124">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="f0ede-125">Sisestage väärtus väljale **Laod**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-125">In the **Warehouses** field, type a value.</span></span> <span data-ttu-id="f0ede-126">Saate filtreerida ühe või mitme lao alusel.</span><span class="sxs-lookup"><span data-stu-id="f0ede-126">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="f0ede-127">Valige väärtus väljal **Tarneviis**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-127">In the **Mode of delivery** field, select a value.</span></span> <span data-ttu-id="f0ede-128">See määrab filtri kuvama ainult selle tarneviisiga sissetulekuread.</span><span class="sxs-lookup"><span data-stu-id="f0ede-128">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="f0ede-129">Valige WHS väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-129">In the **Name** field, select WHS.</span></span>
11. <span data-ttu-id="f0ede-130">Valige ladu 24 väljal **Ladu**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-130">In the **Warehouse** field, select warehouse 24.</span></span> <span data-ttu-id="f0ede-131">See on vaikeladu, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.</span><span class="sxs-lookup"><span data-stu-id="f0ede-131">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="f0ede-132">Valige väljal **Asukoht** suvand **Baydoor**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-132">In the **Location** field, select **Baydoor**.</span></span> <span data-ttu-id="f0ede-133">See on vaikeasukoht, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.</span><span class="sxs-lookup"><span data-stu-id="f0ede-133">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="f0ede-134">Jaotise **Saabumise päringu üksikasjad** laiendamine või ahendamine.</span><span class="sxs-lookup"><span data-stu-id="f0ede-134">Expand or collapse the **Arrival query details** section.</span></span>
14. <span data-ttu-id="f0ede-135">Valige koht 2 väljal **Piira kohaga**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-135">In the **Restrict to site** field, select site 2.</span></span> <span data-ttu-id="f0ede-136">See määrab filtri kuvama ainult selle tegevuskohaga sissetulekuread.</span><span class="sxs-lookup"><span data-stu-id="f0ede-136">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="f0ede-137">Määrake suvandi **Ostutellimused** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-137">Set the **Purchase orders** option to **Yes**.</span></span> <span data-ttu-id="f0ede-138">Saate valida sissetulekuridu ostutellimustest.</span><span class="sxs-lookup"><span data-stu-id="f0ede-138">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="f0ede-139">Määrake suvandi tellimuste **Edastus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-139">Set the **Transfer** orders option to **Yes**.</span></span> <span data-ttu-id="f0ede-140">Saate valida sissetulekuridu üleviimistellimustest.</span><span class="sxs-lookup"><span data-stu-id="f0ede-140">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="f0ede-141">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f0ede-141">Select **Save**.</span></span>
18. <span data-ttu-id="f0ede-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f0ede-142">Close the page.</span></span>

