--- 
title: Kindlatele toodetele hankijate kinnitamine
description: Selles protseduuris selgitatakse, kuidas kinnitada hankijaid kindlate toodete puhul.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a6db8ab41ab393cc92b4fea0435608eff110d58b
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="55a75-103">Kindlatele toodetele hankijate kinnitamine</span><span class="sxs-lookup"><span data-stu-id="55a75-103">Approve vendors for specific products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="55a75-104">Selles protseduuris selgitatakse, kuidas kinnitada hankijaid kindlate toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="55a75-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="55a75-105">See võimaldab teil juhtida, milliseid hankijaid saab kasutada, kui toode ostutellimusse lisatakse.</span><span class="sxs-lookup"><span data-stu-id="55a75-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="55a75-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="55a75-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="55a75-107">Seda ülesannet täidab tavaliselt Ostujuht.</span><span class="sxs-lookup"><span data-stu-id="55a75-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="55a75-108">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="55a75-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="55a75-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="55a75-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="55a75-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="55a75-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="55a75-111">Laiendage jaotist Ost.</span><span class="sxs-lookup"><span data-stu-id="55a75-111">Expand the Purchase section.</span></span>
    * <span data-ttu-id="55a75-112">Kui väljal Hankija kuvatakse esmane hankija, siis peate järgmistes etappides lisama selle hankija kinnitatud hankijana.</span><span class="sxs-lookup"><span data-stu-id="55a75-112">If there is a primary vendor shown in the Vendor field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="55a75-113">Märkige üles hankija kood, kui see kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="55a75-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="55a75-114">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="55a75-114">On the Action Pane, click Purchase.</span></span>
6. <span data-ttu-id="55a75-115">Klõpsake valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="55a75-115">Click Setup.</span></span>
7. <span data-ttu-id="55a75-116">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="55a75-116">Click Add.</span></span>
8. <span data-ttu-id="55a75-117">Sisestage või valige väärtus väljal Hankija.</span><span class="sxs-lookup"><span data-stu-id="55a75-117">In the Vendor field, enter or select a value.</span></span>
    * <span data-ttu-id="55a75-118">Valige kinnitatud hankija.</span><span class="sxs-lookup"><span data-stu-id="55a75-118">Select the approved vendor.</span></span> <span data-ttu-id="55a75-119">Vähemalt üks ridadest peab olema esmane hankija, kui toote kirjes oli hankija.</span><span class="sxs-lookup"><span data-stu-id="55a75-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="55a75-120">Kui tegite hankijakoodi varem märkuse, valige see siin.</span><span class="sxs-lookup"><span data-stu-id="55a75-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="55a75-121">Sisestage kuupäev väljale Aegumine.</span><span class="sxs-lookup"><span data-stu-id="55a75-121">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="55a75-122">Valige kuupäev, mis on mõned kuud hiljem.</span><span class="sxs-lookup"><span data-stu-id="55a75-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="55a75-123">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="55a75-123">Click Add.</span></span>
11. <span data-ttu-id="55a75-124">Sisestage või valige väärtus väljal Hankija.</span><span class="sxs-lookup"><span data-stu-id="55a75-124">In the Vendor field, enter or select a value.</span></span>
12. <span data-ttu-id="55a75-125">Sisestage kuupäev väljale Aegumine.</span><span class="sxs-lookup"><span data-stu-id="55a75-125">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="55a75-126">Valige kuupäev, mis erineb eelmisest aegumiskuupäevast.</span><span class="sxs-lookup"><span data-stu-id="55a75-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="55a75-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="55a75-127">Close the page.</span></span>
14. <span data-ttu-id="55a75-128">Klõpsake suvandit Kinnitatud hankijad.</span><span class="sxs-lookup"><span data-stu-id="55a75-128">Click Approved vendors.</span></span>
15. <span data-ttu-id="55a75-129">Sisestage kuupäev väljale Aegumine.</span><span class="sxs-lookup"><span data-stu-id="55a75-129">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="55a75-130">See kuupäev toimib filtrina, nii et saate teatud kuupäevani vaadata, kes on kinnitatud hankijaid.</span><span class="sxs-lookup"><span data-stu-id="55a75-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="55a75-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="55a75-131">Close the page.</span></span>
17. <span data-ttu-id="55a75-132">Klõpsake suvandit Kehtivusperiood.</span><span class="sxs-lookup"><span data-stu-id="55a75-132">Click Effective period.</span></span>
18. <span data-ttu-id="55a75-133">Sisestage kuupäev väljale Kuva hankijad, kes on aegunud kuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="55a75-133">In the Show vendors expired by field, enter a date.</span></span>
    * <span data-ttu-id="55a75-134">Selle lehe abil saate tuvastada tarnijaid, kui kinnitamisolek aegub pärast kindlat kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="55a75-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="55a75-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="55a75-135">Close the page.</span></span>
20. <span data-ttu-id="55a75-136">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="55a75-136">Click Edit.</span></span>
21. <span data-ttu-id="55a75-137">Valige suvand väljal Kinnitatud hankija tšeki meetod.</span><span class="sxs-lookup"><span data-stu-id="55a75-137">In the Approved vendor check method field, select an option.</span></span>
    * <span data-ttu-id="55a75-138">Sellel väljal saate valida poliitika selle kohta, mis peaks juhtuma siis, kui toode lisatakse ostutellimuse reale, kus hankija pole kinnitatud hankija.</span><span class="sxs-lookup"><span data-stu-id="55a75-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="55a75-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="55a75-139">Click Save.</span></span>
23. <span data-ttu-id="55a75-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="55a75-140">Close the page.</span></span>
24. <span data-ttu-id="55a75-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="55a75-141">Close the page.</span></span>
25. <span data-ttu-id="55a75-142">Avage Hanked > Hankijad > Hankija/kauba seosed > Kinnitatud hankijaloend kauba alusel.</span><span class="sxs-lookup"><span data-stu-id="55a75-142">Go to Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item.</span></span>
    * <span data-ttu-id="55a75-143">Sellel lehel antakse ülevaade kõikide toodete ja kinnitatud hankijate kohta.</span><span class="sxs-lookup"><span data-stu-id="55a75-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="55a75-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="55a75-144">Close the page.</span></span>
27. <span data-ttu-id="55a75-145">Tehke valik Hanked > Hankijad > Kõik hankijad.</span><span class="sxs-lookup"><span data-stu-id="55a75-145">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
    * <span data-ttu-id="55a75-146">Samuti saate alustada hankijast ja avada seejärel selle hankija konto kinnitatud toodete loendi.</span><span class="sxs-lookup"><span data-stu-id="55a75-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="55a75-147">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="55a75-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="55a75-148">Klõpsake toimingupaanil suvandit Hange.</span><span class="sxs-lookup"><span data-stu-id="55a75-148">On the Action Pane, click Procurement.</span></span>
30. <span data-ttu-id="55a75-149">Klõpsake suvandit Kinnitatud hankijaloend hankija alusel.</span><span class="sxs-lookup"><span data-stu-id="55a75-149">Click Approved vendor list by vendor.</span></span>
31. <span data-ttu-id="55a75-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="55a75-150">Close the page.</span></span>
32. <span data-ttu-id="55a75-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="55a75-151">Close the page.</span></span>


