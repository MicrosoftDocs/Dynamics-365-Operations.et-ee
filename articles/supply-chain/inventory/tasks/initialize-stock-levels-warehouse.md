---
title: "Laovaru tasemete lähtestamine laos"
description: "See protseduur näitab, kuidas värskendada vabu kaubavarusid käsitsi, kasutades varude liikumise töölehte."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 74ab2bf22bd1dd64d3cc902052a2de9cd7c5a147
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="58d76-103">Laovaru tasemete lähtestamine laos</span><span class="sxs-lookup"><span data-stu-id="58d76-103">Initialize stock levels in the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="58d76-104">See protseduur näitab, kuidas värskendada vabu kaubavarusid käsitsi, kasutades varude liikumise töölehte.</span><span class="sxs-lookup"><span data-stu-id="58d76-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="58d76-105">(Vabu kaubavarusid saab värskendada ka kannete importimisega andmeüksustes.) Saate käitada seda juhendit demoettevõttes USMF, kus kõik eeltingimused, nagu töölehe nimi, kaubaseadistus, sisestusprofiilid ja kontod,on saadaval.</span><span class="sxs-lookup"><span data-stu-id="58d76-105">(It’s also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="58d76-106">Juhend soovitab kindlaid väärtusi kasutatavale kaubale ja dimensioonidele.</span><span class="sxs-lookup"><span data-stu-id="58d76-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="58d76-107">Teise kauba valimisel peate võib-olla sisestama väärtused teiste dimensioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="58d76-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="58d76-108">Minge jaotisse Varude haldus > Töölehe sisestused > Kaubad > Liikumine.</span><span class="sxs-lookup"><span data-stu-id="58d76-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="58d76-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="58d76-109">Click New.</span></span>
3. <span data-ttu-id="58d76-110">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="58d76-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="58d76-111">Valige suvand IMov.</span><span class="sxs-lookup"><span data-stu-id="58d76-111">Select IMov.</span></span>
    * <span data-ttu-id="58d76-112">Soovitatav on kasutada erinevate äritegevuste jaoks erinevaid töölehtede nimemalle.</span><span class="sxs-lookup"><span data-stu-id="58d76-112">It’s a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="58d76-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="58d76-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="58d76-114">Määrake väljal vastaskonto väärtus 140 200.</span><span class="sxs-lookup"><span data-stu-id="58d76-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="58d76-115">See on vastaskonto, mis on töölehe ridade vaikekonto.</span><span class="sxs-lookup"><span data-stu-id="58d76-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="58d76-116">Vaikekonto saab tühistada, et määrata igale reale erinevad vastaskontod.</span><span class="sxs-lookup"><span data-stu-id="58d76-116">It’s possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="58d76-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="58d76-117">Click OK.</span></span>
8. <span data-ttu-id="58d76-118">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="58d76-118">Click New.</span></span>
9. <span data-ttu-id="58d76-119">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="58d76-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="58d76-120">Valige kaup A0001.</span><span class="sxs-lookup"><span data-stu-id="58d76-120">Select item A0001.</span></span>
11. <span data-ttu-id="58d76-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="58d76-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="58d76-122">Klõpsake vahekaarti Varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="58d76-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="58d76-123">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="58d76-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="58d76-124">Valige tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="58d76-124">Select site 1.</span></span>
15. <span data-ttu-id="58d76-125">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="58d76-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="58d76-126">Valige ladu 13.</span><span class="sxs-lookup"><span data-stu-id="58d76-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="58d76-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="58d76-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="58d76-128">Klõpsake väljal Asukoht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="58d76-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="58d76-129">Valige asukoht 13.</span><span class="sxs-lookup"><span data-stu-id="58d76-129">Select location 13.</span></span>
20. <span data-ttu-id="58d76-130">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="58d76-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="58d76-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="58d76-131">Click Save.</span></span>
22. <span data-ttu-id="58d76-132">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="58d76-132">Click Post.</span></span>
23. <span data-ttu-id="58d76-133">Märkige või tühjendage ruut Kanna kõik sisestusvead üle uuele töölehele.</span><span class="sxs-lookup"><span data-stu-id="58d76-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="58d76-134">Selle suvandi lubamisel kopeeritakse kõik read, mille sisestamine ei õnnestu, uuele töölehele.</span><span class="sxs-lookup"><span data-stu-id="58d76-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="58d76-135">Logiteabe abil saate probleemid lahendada ja seejärel read uuesti sisestada.</span><span class="sxs-lookup"><span data-stu-id="58d76-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="58d76-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="58d76-136">Click OK.</span></span>
25. <span data-ttu-id="58d76-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="58d76-137">Close the page.</span></span>
26. <span data-ttu-id="58d76-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="58d76-138">Close the page.</span></span>

