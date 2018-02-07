---
title: "Kauba saabumise ülevaateprofiili seadistamine"
description: "See ülesanne keskendub saabumisülevaate profiili seadistusele."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 5ddc491d73bbb6ac02e37a9c9b9d93545f6f9556
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="fc055-103">Kauba saabumise ülevaateprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="fc055-103">Set up an item arrival overview profile</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc055-104">See ülesanne keskendub saabumisülevaate profiili seadistusele.</span><span class="sxs-lookup"><span data-stu-id="fc055-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="fc055-105">Saabumisülevaate profiil on kogumik reegleid, mida rakendatakse, kui kasutaja avaneb lehe Saabumisülevaade.</span><span class="sxs-lookup"><span data-stu-id="fc055-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="fc055-106">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="fc055-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="fc055-107">Seda protseduuri viib tavaliselt läbi vastuvõtuametnik.</span><span class="sxs-lookup"><span data-stu-id="fc055-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="fc055-108">Avage Varude haldus > Seadistus > Jaotus > Saabumisülevaate profiilid.</span><span class="sxs-lookup"><span data-stu-id="fc055-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="fc055-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fc055-109">Click New.</span></span>
    * <span data-ttu-id="fc055-110">Kuna töötate täis veokikoormate mahalaadimisel peaaegu alati samas laos, peaksite looma saabuvate kaupade registreerimise lihtsustamiseks saabumisülevaate profiili.</span><span class="sxs-lookup"><span data-stu-id="fc055-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="fc055-111">Sisestage väärtus väljale Saabumisülevaate profiili nimi.</span><span class="sxs-lookup"><span data-stu-id="fc055-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="fc055-112">Valige suvand väljal Kuva read.</span><span class="sxs-lookup"><span data-stu-id="fc055-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="fc055-113">Valige, milliseid ridu sissetulekute puhul kuvada: kõik – saate kuvada kõik read olenemata olekust.</span><span class="sxs-lookup"><span data-stu-id="fc055-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="fc055-114">Pooleli – kuvatakse read sissetulekute puhul, mil edenemise olekuks on Lõpetatud või Pooleli.</span><span class="sxs-lookup"><span data-stu-id="fc055-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="fc055-115">See tähendab, et iga rea puhul on saabumistöölehele registreeritud täielik või osaline kogus.</span><span class="sxs-lookup"><span data-stu-id="fc055-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="fc055-116">Lõpetamata – kuvatakse read sissetulekute puhul, mil edenemise olekuks on Puudub või Pooleli.</span><span class="sxs-lookup"><span data-stu-id="fc055-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="fc055-117">See tähendab, et iga rea puhul on saabumistöölehele registreeritud mitte midagi või ainult osa kogusest.</span><span class="sxs-lookup"><span data-stu-id="fc055-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="fc055-118">Laiendage või ahendage jaotist Saabumisvalikud.</span><span class="sxs-lookup"><span data-stu-id="fc055-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="fc055-119">Sisestage väärtus väljale Päevi edasi.</span><span class="sxs-lookup"><span data-stu-id="fc055-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="fc055-120">See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse järgmise paari päeva jooksul (olenevalt teie määratud numbrist).</span><span class="sxs-lookup"><span data-stu-id="fc055-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="fc055-121">Sisestage väärtus väljale Päevi tagasi.</span><span class="sxs-lookup"><span data-stu-id="fc055-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="fc055-122">See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse arv päevi enne tänast.</span><span class="sxs-lookup"><span data-stu-id="fc055-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="fc055-123">Sisestage väärtus väljale Laod.</span><span class="sxs-lookup"><span data-stu-id="fc055-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="fc055-124">Saate filtreerida ühe või mitme lao alusel.</span><span class="sxs-lookup"><span data-stu-id="fc055-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="fc055-125">Valige väärtus väljalt Tarneviis.</span><span class="sxs-lookup"><span data-stu-id="fc055-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="fc055-126">See määrab filtri kuvama ainult selle tarneviisiga sissetulekuread.</span><span class="sxs-lookup"><span data-stu-id="fc055-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="fc055-127">Valige väljalt Nimi väärtus WHS.</span><span class="sxs-lookup"><span data-stu-id="fc055-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="fc055-128">Valige väljalt Ladu ladu 24.</span><span class="sxs-lookup"><span data-stu-id="fc055-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="fc055-129">See on vaikeladu, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.</span><span class="sxs-lookup"><span data-stu-id="fc055-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="fc055-130">Valige Baydoor väljalt Asukoht.</span><span class="sxs-lookup"><span data-stu-id="fc055-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="fc055-131">See on vaikeasukoht, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.</span><span class="sxs-lookup"><span data-stu-id="fc055-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="fc055-132">Laiendage või ahendage jaotist Saabumispäringu üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="fc055-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="fc055-133">Väljal Piira tegevuskohaga valige tegevuskoht 2.</span><span class="sxs-lookup"><span data-stu-id="fc055-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="fc055-134">See määrab filtri kuvama ainult selle tegevuskohaga sissetulekuread.</span><span class="sxs-lookup"><span data-stu-id="fc055-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="fc055-135">Määrake valiku Ostutellimused väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="fc055-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="fc055-136">Saate valida sissetulekuridu ostutellimustest.</span><span class="sxs-lookup"><span data-stu-id="fc055-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="fc055-137">Määrake valiku Üleviimistellimused väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="fc055-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="fc055-138">Saate valida sissetulekuridu üleviimistellimustest.</span><span class="sxs-lookup"><span data-stu-id="fc055-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="fc055-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="fc055-139">Click Save.</span></span>
18. <span data-ttu-id="fc055-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fc055-140">Close the page.</span></span>

