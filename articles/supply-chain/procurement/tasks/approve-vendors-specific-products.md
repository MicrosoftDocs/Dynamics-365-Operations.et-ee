---
title: Kindlatele toodetele hankijate kinnitamine
description: Selles protseduuris selgitatakse, kuidas kinnitada hankijaid kindlate toodete puhul.
author: mkirknel
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fafa2f7da5575206d452f31bb297790874369dfd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426204"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="dc772-103">Kindlatele toodetele hankijate kinnitamine</span><span class="sxs-lookup"><span data-stu-id="dc772-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc772-104">Selles protseduuris selgitatakse, kuidas kinnitada hankijaid kindlate toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="dc772-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="dc772-105">See võimaldab teil juhtida, milliseid hankijaid saab kasutada, kui toode ostutellimusse lisatakse.</span><span class="sxs-lookup"><span data-stu-id="dc772-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="dc772-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="dc772-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="dc772-107">Seda ülesannet täidab tavaliselt Ostujuht.</span><span class="sxs-lookup"><span data-stu-id="dc772-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="dc772-108">Avage navigeerimispaanil **Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="dc772-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="dc772-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="dc772-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="dc772-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dc772-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="dc772-111">Suurendage vahekaarti **Osta**.</span><span class="sxs-lookup"><span data-stu-id="dc772-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="dc772-112">Kui väljal **Hankija** kuvatakse esmane hankija, siis peate järgmistes etappides lisama selle hankija kinnitatud hankijana.</span><span class="sxs-lookup"><span data-stu-id="dc772-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="dc772-113">Märkige üles hankija kood, kui see kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="dc772-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="dc772-114">Klõpsake toimingupaanil valikut **Ost**.</span><span class="sxs-lookup"><span data-stu-id="dc772-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="dc772-115">Klõpsake **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="dc772-115">Click **Setup**.</span></span>
7. <span data-ttu-id="dc772-116">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dc772-116">Click **Add**.</span></span>
8. <span data-ttu-id="dc772-117">Sisestage või valige väärtus väljal Hankija.</span><span class="sxs-lookup"><span data-stu-id="dc772-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="dc772-118">Valige kinnitatud hankija.</span><span class="sxs-lookup"><span data-stu-id="dc772-118">Select the approved vendor.</span></span> <span data-ttu-id="dc772-119">Vähemalt üks ridadest peab olema esmane hankija, kui toote kirjes oli hankija.</span><span class="sxs-lookup"><span data-stu-id="dc772-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="dc772-120">Kui tegite hankijakoodi varem märkuse, valige see siin.</span><span class="sxs-lookup"><span data-stu-id="dc772-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="dc772-121">Sisestage kuupäev väljale **Aegumine**.</span><span class="sxs-lookup"><span data-stu-id="dc772-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="dc772-122">Valige kuupäev, mis on mõned kuud hiljem.</span><span class="sxs-lookup"><span data-stu-id="dc772-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="dc772-123">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="dc772-123">Click **Add**.</span></span>
11. <span data-ttu-id="dc772-124">Sisestage või valige väärtus väljal **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="dc772-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="dc772-125">Sisestage kuupäev väljale **Aegumine**.</span><span class="sxs-lookup"><span data-stu-id="dc772-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="dc772-126">Valige kuupäev, mis erineb eelmisest aegumiskuupäevast.</span><span class="sxs-lookup"><span data-stu-id="dc772-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="dc772-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc772-127">Close the page.</span></span>
14. <span data-ttu-id="dc772-128">Klõpsake toimingupaanil valikut **Kinnitatud hankijad**.</span><span class="sxs-lookup"><span data-stu-id="dc772-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="dc772-129">Sisestage kuupäev väljale **Aegumine**.</span><span class="sxs-lookup"><span data-stu-id="dc772-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="dc772-130">See kuupäev toimib filtrina, nii et saate teatud kuupäevani vaadata, kes on kinnitatud hankijaid.</span><span class="sxs-lookup"><span data-stu-id="dc772-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="dc772-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc772-131">Close the page.</span></span>
17. <span data-ttu-id="dc772-132">Klõpsake toimingupaanil valikut **Kehtiv periood**.</span><span class="sxs-lookup"><span data-stu-id="dc772-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="dc772-133">Sisestage kuupäev väljale **Kuva hankijad, kes on aegunud kuupäevaks**.</span><span class="sxs-lookup"><span data-stu-id="dc772-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="dc772-134">Selle lehe abil saate tuvastada tarnijaid, kui kinnitamisolek aegub pärast kindlat kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="dc772-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="dc772-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc772-135">Close the page.</span></span>
20. <span data-ttu-id="dc772-136">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dc772-136">Click **Edit**.</span></span>
21. <span data-ttu-id="dc772-137">Valige suvand väljal **Kinnitatud hankija tšeki meetod**.</span><span class="sxs-lookup"><span data-stu-id="dc772-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="dc772-138">Sellel väljal saate valida poliitika selle kohta, mis peaks juhtuma siis, kui toode lisatakse ostutellimuse reale, kus hankija pole kinnitatud hankija.</span><span class="sxs-lookup"><span data-stu-id="dc772-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="dc772-139">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc772-139">Click **Save**.</span></span>
23. <span data-ttu-id="dc772-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc772-140">Close the page.</span></span>
24. <span data-ttu-id="dc772-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc772-141">Close the page.</span></span>
25. <span data-ttu-id="dc772-142">Avage navigeerimispaneelil **Moodulid > Hanked > Hankijad > Hankija/kauba seosed > Kinnitatud hankija loend kauba alusel**.</span><span class="sxs-lookup"><span data-stu-id="dc772-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="dc772-143">Sellel lehel antakse ülevaade kõikide toodete ja kinnitatud hankijate kohta.</span><span class="sxs-lookup"><span data-stu-id="dc772-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="dc772-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc772-144">Close the page.</span></span>
27. <span data-ttu-id="dc772-145">Avage navigeerimispaanil **Moodulid > Hanked > Hankijad > Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="dc772-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="dc772-146">Samuti saate alustada hankijast ja avada seejärel selle hankija konto kinnitatud toodete loendi.</span><span class="sxs-lookup"><span data-stu-id="dc772-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="dc772-147">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="dc772-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="dc772-148">Klõpsake toimingupaanil suvandit **Hange**.</span><span class="sxs-lookup"><span data-stu-id="dc772-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="dc772-149">Klõpsake suvandit **Kinnitatud hankijaloend hankija alusel**.</span><span class="sxs-lookup"><span data-stu-id="dc772-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="dc772-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc772-150">Close the page.</span></span>
32. <span data-ttu-id="dc772-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dc772-151">Close the page.</span></span>

