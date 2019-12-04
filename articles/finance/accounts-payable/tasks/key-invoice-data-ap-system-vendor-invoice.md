---
title: Arve põhiandmed AP-süsteemis, kasutades hankija arvet
description: Selle tegevusejuhise abil saate ostutellimuse põhjal luua hankija arve ja vaadata ostutellimuse, sissetuleku ja arve (kolmesuunaline vastavusseviimine) vastavusseviimise tulemusi.
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7abae6d680d899a0294ad3c298a4b0264ba01d0b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189426"
---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="8fea0-103">Arve põhiandmed AP-süsteemis, kasutades hankija arvet</span><span class="sxs-lookup"><span data-stu-id="8fea0-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8fea0-104">Selle tegevusejuhise abil saate ostutellimuse põhjal luua hankija arve ja vaadata ostutellimuse, sissetuleku ja arve (kolmesuunaline vastavusseviimine) vastavusseviimise tulemusi.</span><span class="sxs-lookup"><span data-stu-id="8fea0-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="8fea0-105">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="8fea0-105">Create a purchase order</span></span>
1. <span data-ttu-id="8fea0-106">Avage navigeerimispaanil **Moodulid > Arved > Ostutellimused > Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="8fea0-107">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-107">Click **New**.</span></span>
3. <span data-ttu-id="8fea0-108">Klõpsake väljal **Hankija konto** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8fea0-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8fea0-109">Leidke valitav hankija.</span><span class="sxs-lookup"><span data-stu-id="8fea0-109">Find a vendor to select.</span></span> <span data-ttu-id="8fea0-110">Kerige näiteks alla suvandini US-104.</span><span class="sxs-lookup"><span data-stu-id="8fea0-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="8fea0-111">Valige hankija US-104.</span><span class="sxs-lookup"><span data-stu-id="8fea0-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="8fea0-112">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-112">Click **OK**.</span></span>
7. <span data-ttu-id="8fea0-113">Klõpsake väljal **Kaubakood otsingu** avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8fea0-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="8fea0-114">Valige laokaup.</span><span class="sxs-lookup"><span data-stu-id="8fea0-114">Select an inventory item.</span></span> <span data-ttu-id="8fea0-115">Valige näiteks kauba number 1000.</span><span class="sxs-lookup"><span data-stu-id="8fea0-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="8fea0-116">Laiendage kiirkaarti **Rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="8fea0-117">Klõpsake vahekaarti **Seadistamine**. Teil on võimalik alistada vastavusseviimise poliitika ja kasutada vastavusseviimise puudumist, kahesuunalist vastavusseviimist või kolmesuunalist vastavusseviimist.</span><span class="sxs-lookup"><span data-stu-id="8fea0-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="8fea0-118">Klõpsake toimingupaanil valikut **Ost**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="8fea0-119">Klõpsake käsku **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="8fea0-120">Toodete vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="8fea0-120">Receive the products</span></span>
1. <span data-ttu-id="8fea0-121">Klõpsake toimingupaanil valikut **Vastuvõtt**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="8fea0-122">Klõpsake valikut **Toote sissetulek**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="8fea0-123">Sisestage väljale **Toote sissetulek** tootesissetuleku number.</span><span class="sxs-lookup"><span data-stu-id="8fea0-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="8fea0-124">Sisestage näiteks PR123.</span><span class="sxs-lookup"><span data-stu-id="8fea0-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="8fea0-125">Klõpsake tootesissetuleku sisestamiseks nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="8fea0-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8fea0-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="8fea0-127">Hankijaarve koostamine</span><span class="sxs-lookup"><span data-stu-id="8fea0-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="8fea0-128">Minge navigeerimispaanil jaotisse **Moodulid > Maksmisele kuuluvad kontod > Ostutellimused> Saadud, kuid arveta ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="8fea0-129">Valige loodud ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="8fea0-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="8fea0-130">Klõpsake toimingupaanil valikut **Arve**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="8fea0-131">Klõpsake **Arve**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="8fea0-132">Sisestage väljale **Number** arve number.</span><span class="sxs-lookup"><span data-stu-id="8fea0-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="8fea0-133">Sisestage väljale **Arve kirjeldus** soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="8fea0-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="8fea0-134">Sisestage kuupäev väljale **Arve kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="8fea0-135">Sisestage 1200 väljale **Ühiku hind**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="8fea0-136">Klõpsake käsku **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-136">Click **Add line**.</span></span>
10. <span data-ttu-id="8fea0-137">Klõpsake väljal **Kaubakood otsingu** avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8fea0-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="8fea0-138">Leidke loendist installimistasu kaubakood.</span><span class="sxs-lookup"><span data-stu-id="8fea0-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="8fea0-139">Näiteks S0001</span><span class="sxs-lookup"><span data-stu-id="8fea0-139">For example, S0001</span></span>
12. <span data-ttu-id="8fea0-140">Valige installimistasu kaubakood.</span><span class="sxs-lookup"><span data-stu-id="8fea0-140">Select the installation charge item number.</span></span> <span data-ttu-id="8fea0-141">Võtke arvesse, et vastavusseviimist pole pärast muudatuste tegemist toimunud.</span><span class="sxs-lookup"><span data-stu-id="8fea0-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="8fea0-142">**Klõpsake suvandit Värskenda vastendamise olek.**</span><span class="sxs-lookup"><span data-stu-id="8fea0-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="8fea0-143">Klõpsake toimingupaanil valikut **Vaata üle**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="8fea0-144">Klõpsake valikut **Vastanduvad üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-144">Click **Matching details**.</span></span> <span data-ttu-id="8fea0-145">Uus teenuste rida ei pea olema vastavusse viidud, nii et olekuks jääb Täitmata.</span><span class="sxs-lookup"><span data-stu-id="8fea0-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="8fea0-146">Valige saadud laokauba toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="8fea0-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="8fea0-147">Tootesissetuleku rida on vastavusse viidud, kuid kogus või hind ei sobi, nii et see nurjub.</span><span class="sxs-lookup"><span data-stu-id="8fea0-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="8fea0-148">Sisestage arv väljale **Ühiku hind**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="8fea0-149">Nüüd, kui ühiku hind on vastavuses, värskendatakse olekut, ja uueks oleks seatakse Arvestatud.</span><span class="sxs-lookup"><span data-stu-id="8fea0-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="8fea0-150">Kui teie poliitika lubab lahknevusi või kui vastavusseviimine on ainult hoiatus, saate arve siiski sisestada.</span><span class="sxs-lookup"><span data-stu-id="8fea0-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="8fea0-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8fea0-151">Close the page.</span></span>
19. <span data-ttu-id="8fea0-152">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="8fea0-152">Click **Post**.</span></span>
20. <span data-ttu-id="8fea0-153">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="8fea0-153">Close the form.</span></span> <span data-ttu-id="8fea0-154">Võtke arvesse, et ostutellimus pole loendis enam „vastu võetud“, vaid „arveldamata“.</span><span class="sxs-lookup"><span data-stu-id="8fea0-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  
