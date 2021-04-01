---
title: Laovaru tasemete lähtestamine laos
description: See protseduur näitab, kuidas värskendada vabu kaubavarusid käsitsi, kasutades varude liikumise töölehte.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2c1e5ca96919acde7e850292a73ebd00185f1f7a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244470"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="656ee-103">Laovaru tasemete lähtestamine laos</span><span class="sxs-lookup"><span data-stu-id="656ee-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="656ee-104">See protseduur näitab, kuidas värskendada vabu kaubavarusid käsitsi, kasutades varude liikumise töölehte.</span><span class="sxs-lookup"><span data-stu-id="656ee-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="656ee-105">(Vabu kaubavarusid saab värskendada ka kannete importimisega andmeüksustes.) Saate käitada seda juhendit demoettevõttes USMF, kus kõik eeltingimused, nagu töölehe nimi, kaubaseadistus, sisestusprofiilid ja kontod,on saadaval.</span><span class="sxs-lookup"><span data-stu-id="656ee-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="656ee-106">Juhend soovitab kindlaid väärtusi kasutatavale kaubale ja dimensioonidele.</span><span class="sxs-lookup"><span data-stu-id="656ee-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="656ee-107">Teise kauba valimisel peate võib-olla sisestama väärtused teiste dimensioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="656ee-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="656ee-108">Minge jaotisse Varude haldus > Töölehe sisestused > Kaubad > Liikumine.</span><span class="sxs-lookup"><span data-stu-id="656ee-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="656ee-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="656ee-109">Click New.</span></span>
3. <span data-ttu-id="656ee-110">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="656ee-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="656ee-111">Valige suvand IMov.</span><span class="sxs-lookup"><span data-stu-id="656ee-111">Select IMov.</span></span>
    * <span data-ttu-id="656ee-112">Soovitatav on kasutada erinevate äritegevuste jaoks erinevaid töölehtede nimemalle.</span><span class="sxs-lookup"><span data-stu-id="656ee-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="656ee-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="656ee-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="656ee-114">Määrake väljal vastaskonto väärtus 140 200.</span><span class="sxs-lookup"><span data-stu-id="656ee-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="656ee-115">See on vastaskonto, mis on töölehe ridade vaikekonto.</span><span class="sxs-lookup"><span data-stu-id="656ee-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="656ee-116">Vaikekonto saab tühistada, et määrata igale reale erinevad vastaskontod.</span><span class="sxs-lookup"><span data-stu-id="656ee-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="656ee-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="656ee-117">Click OK.</span></span>
8. <span data-ttu-id="656ee-118">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="656ee-118">Click New.</span></span>
9. <span data-ttu-id="656ee-119">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="656ee-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="656ee-120">Valige kaup A0001.</span><span class="sxs-lookup"><span data-stu-id="656ee-120">Select item A0001.</span></span>
11. <span data-ttu-id="656ee-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="656ee-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="656ee-122">Klõpsake vahekaarti Varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="656ee-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="656ee-123">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="656ee-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="656ee-124">Valige tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="656ee-124">Select site 1.</span></span>
15. <span data-ttu-id="656ee-125">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="656ee-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="656ee-126">Valige ladu 13.</span><span class="sxs-lookup"><span data-stu-id="656ee-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="656ee-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="656ee-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="656ee-128">Klõpsake väljal Asukoht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="656ee-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="656ee-129">Valige asukoht 13.</span><span class="sxs-lookup"><span data-stu-id="656ee-129">Select location 13.</span></span>
20. <span data-ttu-id="656ee-130">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="656ee-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="656ee-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="656ee-131">Click Save.</span></span>
22. <span data-ttu-id="656ee-132">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="656ee-132">Click Post.</span></span>
23. <span data-ttu-id="656ee-133">Märkige või tühjendage ruut Kanna kõik sisestusvead üle uuele töölehele.</span><span class="sxs-lookup"><span data-stu-id="656ee-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="656ee-134">Selle suvandi lubamisel kopeeritakse kõik read, mille sisestamine ei õnnestu, uuele töölehele.</span><span class="sxs-lookup"><span data-stu-id="656ee-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="656ee-135">Logiteabe abil saate probleemid lahendada ja seejärel read uuesti sisestada.</span><span class="sxs-lookup"><span data-stu-id="656ee-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="656ee-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="656ee-136">Click OK.</span></span>
25. <span data-ttu-id="656ee-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="656ee-137">Close the page.</span></span>
26. <span data-ttu-id="656ee-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="656ee-138">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]