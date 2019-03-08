---
title: Arve põhiandmed AP-süsteemis, kasutades hankija arvet
description: Selle tegevusejuhise abil saate ostutellimuse põhjal luua hankija arve ja vaadata ostutellimuse, sissetuleku ja arve (kolmesuunaline vastavusseviimine) vastavusseviimise tulemusi.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "359102"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="332ab-103">Arve põhiandmed AP-süsteemis, kasutades hankija arvet</span><span class="sxs-lookup"><span data-stu-id="332ab-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="332ab-104">Selle tegevusejuhise abil saate ostutellimuse põhjal luua hankija arve ja vaadata ostutellimuse, sissetuleku ja arve (kolmesuunaline vastavusseviimine) vastavusseviimise tulemusi.</span><span class="sxs-lookup"><span data-stu-id="332ab-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="332ab-105">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="332ab-105">Create a purchase order</span></span>
1. <span data-ttu-id="332ab-106">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="332ab-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="332ab-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="332ab-107">Click New.</span></span>
3. <span data-ttu-id="332ab-108">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="332ab-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="332ab-109">Leidke valitav hankija.</span><span class="sxs-lookup"><span data-stu-id="332ab-109">Find a vendor to select.</span></span> <span data-ttu-id="332ab-110">Kerige näiteks alla suvandini US-104.</span><span class="sxs-lookup"><span data-stu-id="332ab-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="332ab-111">Valige hankija US-104.</span><span class="sxs-lookup"><span data-stu-id="332ab-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="332ab-112">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="332ab-112">Click OK.</span></span>
7. <span data-ttu-id="332ab-113">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="332ab-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="332ab-114">Valige laokaup.</span><span class="sxs-lookup"><span data-stu-id="332ab-114">Select an inventory item.</span></span> <span data-ttu-id="332ab-115">Valige näiteks kauba number 1000.</span><span class="sxs-lookup"><span data-stu-id="332ab-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="332ab-116">Laiendage või ahendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="332ab-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="332ab-117">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="332ab-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="332ab-118">Teil on võimalik alistada vastavusseviimise poliitika ja kasutada vastavusseviimise puudumist, kahesuunalist vastavusseviimist või kolmesuunalist vastavusseviimist.</span><span class="sxs-lookup"><span data-stu-id="332ab-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="332ab-119">Laiendage või ahendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="332ab-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="332ab-120">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="332ab-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="332ab-121">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="332ab-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="332ab-122">Toodete vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="332ab-122">Receive the products</span></span>
1. <span data-ttu-id="332ab-123">Klõpsake toimingupaanil valikut Vastuvõtt.</span><span class="sxs-lookup"><span data-stu-id="332ab-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="332ab-124">Klõpsake valikut Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="332ab-124">Click Product receipt.</span></span>
3. <span data-ttu-id="332ab-125">Sisestage väljale Toote sissetulek tootesissetuleku number.</span><span class="sxs-lookup"><span data-stu-id="332ab-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="332ab-126">Sisestage näiteks PR123.</span><span class="sxs-lookup"><span data-stu-id="332ab-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="332ab-127">Klõpsake tootesissetuleku sisestamiseks nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="332ab-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="332ab-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="332ab-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="332ab-129">Hankijaarve koostamine</span><span class="sxs-lookup"><span data-stu-id="332ab-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="332ab-130">Avage Ostureskontro > Ostutellimused > Saadud, kuid arveldamata ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="332ab-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="332ab-131">Valige loodud ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="332ab-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="332ab-132">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="332ab-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="332ab-133">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="332ab-133">Click Invoice.</span></span>
5. <span data-ttu-id="332ab-134">Sisestage väljale Number arve number.</span><span class="sxs-lookup"><span data-stu-id="332ab-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="332ab-135">Sisestage väljale Arve kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="332ab-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="332ab-136">Sisestage kuupäev väljale Arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="332ab-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="332ab-137">Sisestage 1200 väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="332ab-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="332ab-138">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="332ab-138">Click Add line.</span></span>
10. <span data-ttu-id="332ab-139">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="332ab-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="332ab-140">Leidke loendist installimistasu kaubakood.</span><span class="sxs-lookup"><span data-stu-id="332ab-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="332ab-141">Näiteks S0001</span><span class="sxs-lookup"><span data-stu-id="332ab-141">For example, S0001</span></span>
12. <span data-ttu-id="332ab-142">Valige installimistasu kaubakood.</span><span class="sxs-lookup"><span data-stu-id="332ab-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="332ab-143">Võtke arvesse, et vastavusseviimist pole pärast muudatuste tegemist toimunud.</span><span class="sxs-lookup"><span data-stu-id="332ab-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="332ab-144">Klõpsake valikut Värskenda vastandamise olek.</span><span class="sxs-lookup"><span data-stu-id="332ab-144">Click Update match status.</span></span>
14. <span data-ttu-id="332ab-145">Klõpsake toimingupaanil valikut Vaata üle.</span><span class="sxs-lookup"><span data-stu-id="332ab-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="332ab-146">Klõpsake valikut Vastanduvad üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="332ab-146">Click Matching details.</span></span>
    * <span data-ttu-id="332ab-147">Uus teenuste rida ei pea olema vastavusse viidud, nii et olekuks jääb Täitmata.</span><span class="sxs-lookup"><span data-stu-id="332ab-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="332ab-148">Valige saadud laokauba toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="332ab-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="332ab-149">Tootesissetuleku rida on vastavusse viidud, kuid kogus või hind ei sobi, nii et see nurjub.</span><span class="sxs-lookup"><span data-stu-id="332ab-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="332ab-150">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="332ab-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="332ab-151">Nüüd, kui ühiku hind on vastavuses, värskendatakse olekut, ja uueks oleks seatakse Arvestatud.</span><span class="sxs-lookup"><span data-stu-id="332ab-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="332ab-152">Kui teie poliitika lubab lahknevusi või kui vastavusseviimine on ainult hoiatus, saate arve siiski sisestada.</span><span class="sxs-lookup"><span data-stu-id="332ab-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="332ab-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="332ab-153">Close the page.</span></span>
19. <span data-ttu-id="332ab-154">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="332ab-154">Click Post.</span></span>
20. <span data-ttu-id="332ab-155">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="332ab-155">Close the form.</span></span>
    * <span data-ttu-id="332ab-156">Võtke arvesse, et ostutellimus pole loendis enam „vastu võetud“, vaid „arveldamata“.</span><span class="sxs-lookup"><span data-stu-id="332ab-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

