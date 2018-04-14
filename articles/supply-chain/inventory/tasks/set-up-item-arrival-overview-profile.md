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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5f9df0afe90bcb619304c39b53165e3fe2970ec3
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="02019-103">Kauba saabumise ülevaateprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="02019-103">Set up an item arrival overview profile</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="02019-104">See ülesanne keskendub saabumisülevaate profiili seadistusele.</span><span class="sxs-lookup"><span data-stu-id="02019-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="02019-105">Saabumisülevaate profiil on kogumik reegleid, mida rakendatakse, kui kasutaja avaneb lehe Saabumisülevaade.</span><span class="sxs-lookup"><span data-stu-id="02019-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="02019-106">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="02019-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="02019-107">Seda protseduuri viib tavaliselt läbi vastuvõtuametnik.</span><span class="sxs-lookup"><span data-stu-id="02019-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="02019-108">Avage Varude haldus > Seadistus > Jaotus > Saabumisülevaate profiilid.</span><span class="sxs-lookup"><span data-stu-id="02019-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="02019-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="02019-109">Click New.</span></span>
    * <span data-ttu-id="02019-110">Kuna töötate täis veokikoormate mahalaadimisel peaaegu alati samas laos, peaksite looma saabuvate kaupade registreerimise lihtsustamiseks saabumisülevaate profiili.</span><span class="sxs-lookup"><span data-stu-id="02019-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="02019-111">Sisestage väärtus väljale Saabumisülevaate profiili nimi.</span><span class="sxs-lookup"><span data-stu-id="02019-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="02019-112">Valige suvand väljal Kuva read.</span><span class="sxs-lookup"><span data-stu-id="02019-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="02019-113">Valige, milliseid ridu sissetulekute puhul kuvada: kõik – saate kuvada kõik read olenemata olekust.</span><span class="sxs-lookup"><span data-stu-id="02019-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="02019-114">Pooleli – kuvatakse read sissetulekute puhul, mil edenemise olekuks on Lõpetatud või Pooleli.</span><span class="sxs-lookup"><span data-stu-id="02019-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="02019-115">See tähendab, et iga rea puhul on saabumistöölehele registreeritud täielik või osaline kogus.</span><span class="sxs-lookup"><span data-stu-id="02019-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="02019-116">Lõpetamata – kuvatakse read sissetulekute puhul, mil edenemise olekuks on Puudub või Pooleli.</span><span class="sxs-lookup"><span data-stu-id="02019-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="02019-117">See tähendab, et iga rea puhul on saabumistöölehele registreeritud mitte midagi või ainult osa kogusest.</span><span class="sxs-lookup"><span data-stu-id="02019-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="02019-118">Laiendage või ahendage jaotist Saabumisvalikud.</span><span class="sxs-lookup"><span data-stu-id="02019-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="02019-119">Sisestage väärtus väljale Päevi edasi.</span><span class="sxs-lookup"><span data-stu-id="02019-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="02019-120">See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse järgmise paari päeva jooksul (olenevalt teie määratud numbrist).</span><span class="sxs-lookup"><span data-stu-id="02019-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="02019-121">Sisestage väärtus väljale Päevi tagasi.</span><span class="sxs-lookup"><span data-stu-id="02019-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="02019-122">See seadistab filtri kuvama sissetuleku ridu, mille saabumist eeldatakse arv päevi enne tänast.</span><span class="sxs-lookup"><span data-stu-id="02019-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="02019-123">Sisestage väärtus väljale Laod.</span><span class="sxs-lookup"><span data-stu-id="02019-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="02019-124">Saate filtreerida ühe või mitme lao alusel.</span><span class="sxs-lookup"><span data-stu-id="02019-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="02019-125">Valige väärtus väljalt Tarneviis.</span><span class="sxs-lookup"><span data-stu-id="02019-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="02019-126">See määrab filtri kuvama ainult selle tarneviisiga sissetulekuread.</span><span class="sxs-lookup"><span data-stu-id="02019-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="02019-127">Valige väljalt Nimi väärtus WHS.</span><span class="sxs-lookup"><span data-stu-id="02019-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="02019-128">Valige väljalt Ladu ladu 24.</span><span class="sxs-lookup"><span data-stu-id="02019-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="02019-129">See on vaikeladu, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.</span><span class="sxs-lookup"><span data-stu-id="02019-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="02019-130">Valige Baydoor väljalt Asukoht.</span><span class="sxs-lookup"><span data-stu-id="02019-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="02019-131">See on vaikeasukoht, mida kasutatakse seda profiili kasutavate registreeritud sissetuleku ridadega.</span><span class="sxs-lookup"><span data-stu-id="02019-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="02019-132">Laiendage või ahendage jaotist Saabumispäringu üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="02019-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="02019-133">Väljal Piira tegevuskohaga valige tegevuskoht 2.</span><span class="sxs-lookup"><span data-stu-id="02019-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="02019-134">See määrab filtri kuvama ainult selle tegevuskohaga sissetulekuread.</span><span class="sxs-lookup"><span data-stu-id="02019-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="02019-135">Määrake valiku Ostutellimused väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="02019-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="02019-136">Saate valida sissetulekuridu ostutellimustest.</span><span class="sxs-lookup"><span data-stu-id="02019-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="02019-137">Määrake valiku Üleviimistellimused väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="02019-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="02019-138">Saate valida sissetulekuridu üleviimistellimustest.</span><span class="sxs-lookup"><span data-stu-id="02019-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="02019-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="02019-139">Click Save.</span></span>
18. <span data-ttu-id="02019-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="02019-140">Close the page.</span></span>

