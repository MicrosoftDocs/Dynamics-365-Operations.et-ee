---
title: Kindlatele toodetele hankijate kinnitamine
description: Selles protseduuris selgitatakse, kuidas kinnitada hankijaid kindlate toodete puhul.
author: RichardLuan
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, PdsApprovedVendorList, VendTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d08791caba34908903ce330df0f91e44fbdfcaea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237271"
---
# <a name="approve-vendors-for-specific-products"></a><span data-ttu-id="88fbc-103">Kindlatele toodetele hankijate kinnitamine</span><span class="sxs-lookup"><span data-stu-id="88fbc-103">Approve vendors for specific products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88fbc-104">Selles protseduuris selgitatakse, kuidas kinnitada hankijaid kindlate toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="88fbc-104">This procedure shows you how to approve vendors for specific products.</span></span> <span data-ttu-id="88fbc-105">See võimaldab teil juhtida, milliseid hankijaid saab kasutada, kui toode ostutellimusse lisatakse.</span><span class="sxs-lookup"><span data-stu-id="88fbc-105">This allows you to control which vendors can be used when the product is added to a purchase order.</span></span> <span data-ttu-id="88fbc-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="88fbc-106">You can use this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="88fbc-107">Seda ülesannet täidab tavaliselt Ostujuht.</span><span class="sxs-lookup"><span data-stu-id="88fbc-107">This task would typically be carried out by a Purchasing manager.</span></span>

1. <span data-ttu-id="88fbc-108">Avage navigeerimispaanil **Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-108">In Navigation Pane, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="88fbc-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="88fbc-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="88fbc-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="88fbc-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="88fbc-111">Suurendage vahekaarti **Osta**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-111">Expand the **Purchase** fastTab.</span></span> <span data-ttu-id="88fbc-112">Kui väljal **Hankija** kuvatakse esmane hankija, siis peate järgmistes etappides lisama selle hankija kinnitatud hankijana.</span><span class="sxs-lookup"><span data-stu-id="88fbc-112">If there is a primary vendor shown in the **Vendor** field, then you need to add this vendor as an approved vendor in the following steps.</span></span> <span data-ttu-id="88fbc-113">Märkige üles hankija kood, kui see kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="88fbc-113">Make a note of the vendor number, if one is shown.</span></span>  
5. <span data-ttu-id="88fbc-114">Klõpsake toimingupaanil valikut **Ost**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-114">On the Action Pane, click **Purchase**.</span></span>
6. <span data-ttu-id="88fbc-115">Klõpsake **Häälestus**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-115">Click **Setup**.</span></span>
7. <span data-ttu-id="88fbc-116">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-116">Click **Add**.</span></span>
8. <span data-ttu-id="88fbc-117">Sisestage või valige väärtus väljal Hankija.</span><span class="sxs-lookup"><span data-stu-id="88fbc-117">In the Vendor field, enter or select a value.</span></span> <span data-ttu-id="88fbc-118">Valige kinnitatud hankija.</span><span class="sxs-lookup"><span data-stu-id="88fbc-118">Select the approved vendor.</span></span> <span data-ttu-id="88fbc-119">Vähemalt üks ridadest peab olema esmane hankija, kui toote kirjes oli hankija.</span><span class="sxs-lookup"><span data-stu-id="88fbc-119">At least one of the lines has to be the primary vendor if there was one in the product record.</span></span> <span data-ttu-id="88fbc-120">Kui tegite hankijakoodi varem märkuse, valige see siin.</span><span class="sxs-lookup"><span data-stu-id="88fbc-120">If you made a note of the vendor number earlier, select it here.</span></span>  
9. <span data-ttu-id="88fbc-121">Sisestage kuupäev väljale **Aegumine**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-121">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="88fbc-122">Valige kuupäev, mis on mõned kuud hiljem.</span><span class="sxs-lookup"><span data-stu-id="88fbc-122">Choose a date a that is a few months ahead.</span></span>  
10. <span data-ttu-id="88fbc-123">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-123">Click **Add**.</span></span>
11. <span data-ttu-id="88fbc-124">Sisestage või valige väärtus väljal **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-124">In the **Vendor** field, enter or select a value.</span></span>
12. <span data-ttu-id="88fbc-125">Sisestage kuupäev väljale **Aegumine**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-125">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="88fbc-126">Valige kuupäev, mis erineb eelmisest aegumiskuupäevast.</span><span class="sxs-lookup"><span data-stu-id="88fbc-126">Choose a date that is different than the previous expiration date.</span></span>  
13. <span data-ttu-id="88fbc-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88fbc-127">Close the page.</span></span>
14. <span data-ttu-id="88fbc-128">Klõpsake toimingupaanil valikut **Kinnitatud hankijad**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-128">On the Action Pane, click **Approved vendors**.</span></span>
15. <span data-ttu-id="88fbc-129">Sisestage kuupäev väljale **Aegumine**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-129">In the **Expiration** field, enter a date.</span></span> <span data-ttu-id="88fbc-130">See kuupäev toimib filtrina, nii et saate teatud kuupäevani vaadata, kes on kinnitatud hankijaid.</span><span class="sxs-lookup"><span data-stu-id="88fbc-130">This date acts as a filter so you can see who the approved vendors are, up to a certain date.</span></span>  
16. <span data-ttu-id="88fbc-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88fbc-131">Close the page.</span></span>
17. <span data-ttu-id="88fbc-132">Klõpsake toimingupaanil valikut **Kehtiv periood**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-132">On the Action Pane, click **Effective period**.</span></span>
18. <span data-ttu-id="88fbc-133">Sisestage kuupäev väljale **Kuva hankijad, kes on aegunud kuupäevaks**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-133">In the **Show vendors expired by** field, enter a date.</span></span> <span data-ttu-id="88fbc-134">Selle lehe abil saate tuvastada tarnijaid, kui kinnitamisolek aegub pärast kindlat kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="88fbc-134">You can use this page to identify vendors where the approval status will expire after a certain date.</span></span>  
19. <span data-ttu-id="88fbc-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88fbc-135">Close the page.</span></span>
20. <span data-ttu-id="88fbc-136">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-136">Click **Edit**.</span></span>
21. <span data-ttu-id="88fbc-137">Valige suvand väljal **Kinnitatud hankija tšeki meetod**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-137">In the **Approved vendor check method** field, select an option.</span></span> <span data-ttu-id="88fbc-138">Sellel väljal saate valida poliitika selle kohta, mis peaks juhtuma siis, kui toode lisatakse ostutellimuse reale, kus hankija pole kinnitatud hankija.</span><span class="sxs-lookup"><span data-stu-id="88fbc-138">This field allows you to select the policy for what should happen if the product is added to a purchase order line where the vendor is not an approved vendor.</span></span>  
22. <span data-ttu-id="88fbc-139">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-139">Click **Save**.</span></span>
23. <span data-ttu-id="88fbc-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88fbc-140">Close the page.</span></span>
24. <span data-ttu-id="88fbc-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88fbc-141">Close the page.</span></span>
25. <span data-ttu-id="88fbc-142">Avage navigeerimispaneelil **Moodulid > Hanked > Hankijad > Hankija/kauba seosed > Kinnitatud hankija loend kauba alusel**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-142">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > Vendor/item relations > Approved vendor list by item**.</span></span> <span data-ttu-id="88fbc-143">Sellel lehel antakse ülevaade kõikide toodete ja kinnitatud hankijate kohta.</span><span class="sxs-lookup"><span data-stu-id="88fbc-143">This page gives you an overview of all products and the approved vendors.</span></span>  
26. <span data-ttu-id="88fbc-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88fbc-144">Close the page.</span></span>
27. <span data-ttu-id="88fbc-145">Avage navigeerimispaanil **Moodulid > Hanked > Hankijad > Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-145">In Navigation Pane, go to **Modules > Procurement and sourcing > Vendors > All vendors**.</span></span> <span data-ttu-id="88fbc-146">Samuti saate alustada hankijast ja avada seejärel selle hankija konto kinnitatud toodete loendi.</span><span class="sxs-lookup"><span data-stu-id="88fbc-146">You can also start from a vendor and then go to the list of approved products for that vendor account.</span></span>  
28. <span data-ttu-id="88fbc-147">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="88fbc-147">In the list, find and select the desired record.</span></span>
29. <span data-ttu-id="88fbc-148">Klõpsake toimingupaanil suvandit **Hange**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-148">On the Action Pane, click **Procurement**.</span></span>
30. <span data-ttu-id="88fbc-149">Klõpsake suvandit **Kinnitatud hankijaloend hankija alusel**.</span><span class="sxs-lookup"><span data-stu-id="88fbc-149">Click **Approved vendor list by vendor**.</span></span>
31. <span data-ttu-id="88fbc-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88fbc-150">Close the page.</span></span>
32. <span data-ttu-id="88fbc-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="88fbc-151">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]