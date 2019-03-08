---
title: Arve põhiandmed ostureskontro süsteemi arvete kausta abil
description: See ülesande juhend näitab teile, kuidas kasutada arvete loomiseks arveregistrit.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b4e9a52a383d4acc0bf2adc669fd88c0c0f7402
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "357446"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="ecc68-103">Arve põhiandmed ostureskontro süsteemi arvete kausta abil</span><span class="sxs-lookup"><span data-stu-id="ecc68-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ecc68-104">See ülesande juhend näitab teile, kuidas kasutada arvete loomiseks arveregistrit.</span><span class="sxs-lookup"><span data-stu-id="ecc68-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="ecc68-105">Seejärel kasutage arve sobitamiseks ostutellimusega arvete kausta ja lõpetage kulu hankija arve lehel.</span><span class="sxs-lookup"><span data-stu-id="ecc68-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="ecc68-106">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="ecc68-106">Create a purchase order</span></span>
1. <span data-ttu-id="ecc68-107">Avage Ostureskonto > Ostutellimused > Ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="ecc68-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="ecc68-108">Klõpsake ostutellimuse loomiseks suvandit Uus.</span><span class="sxs-lookup"><span data-stu-id="ecc68-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="ecc68-109">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ecc68-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="ecc68-110">Valige hankija loendist.</span><span class="sxs-lookup"><span data-stu-id="ecc68-110">Select the vendor from the list.</span></span> <span data-ttu-id="ecc68-111">Näiteks hankija 1001.</span><span class="sxs-lookup"><span data-stu-id="ecc68-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="ecc68-112">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ecc68-112">Click OK.</span></span>
6. <span data-ttu-id="ecc68-113">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ecc68-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="ecc68-114">Leidke loendist teenuste kaubakood.</span><span class="sxs-lookup"><span data-stu-id="ecc68-114">Find the services item number in the list.</span></span> <span data-ttu-id="ecc68-115">Valige näiteks S0001.</span><span class="sxs-lookup"><span data-stu-id="ecc68-115">For example, select S0001.</span></span>
8. <span data-ttu-id="ecc68-116">Klõpsake kaubakoodil ja valige see.</span><span class="sxs-lookup"><span data-stu-id="ecc68-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="ecc68-117">Netosumma on 75,00.</span><span class="sxs-lookup"><span data-stu-id="ecc68-117">The net amount is 75.00.</span></span>  <span data-ttu-id="ecc68-118">See on summa, mida arvele eeldame.</span><span class="sxs-lookup"><span data-stu-id="ecc68-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="ecc68-119">Klõpsake tegumiribal valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="ecc68-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="ecc68-120">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="ecc68-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="ecc68-121">Arve loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="ecc68-121">Create and post and invoice</span></span>
1. <span data-ttu-id="ecc68-122">Avage Ostureskontro > Arved > Arveregister.</span><span class="sxs-lookup"><span data-stu-id="ecc68-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="ecc68-123">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ecc68-123">Click New.</span></span>
3. <span data-ttu-id="ecc68-124">Avage otsing, et valida arveregistri nimi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="ecc68-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="ecc68-125">Valige selle arveregistri nimi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="ecc68-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="ecc68-126">Registri avamiseks ja kuluridade sisestamiseks klõpsake nuppu Read.</span><span class="sxs-lookup"><span data-stu-id="ecc68-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="ecc68-127">Valige otsingus hankija.</span><span class="sxs-lookup"><span data-stu-id="ecc68-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="ecc68-128">Näiteks klõpsake hankijat 1001.</span><span class="sxs-lookup"><span data-stu-id="ecc68-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="ecc68-129">Sisestage arve number väljale Arve.</span><span class="sxs-lookup"><span data-stu-id="ecc68-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="ecc68-130">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="ecc68-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="ecc68-131">Sisestage arv väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="ecc68-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="ecc68-132">Klõpsake väljal Ostutellimus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ecc68-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="ecc68-133">Valige varem loodud ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="ecc68-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="ecc68-134">Klõpsake väljal Kinnitaja otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ecc68-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="ecc68-135">Tõstke kinnitaja esile ja klõpsake nuppu Vali, et see kinnitaja valida.</span><span class="sxs-lookup"><span data-stu-id="ecc68-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="ecc68-136">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="ecc68-136">Click Post.</span></span>
15. <span data-ttu-id="ecc68-137">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="ecc68-137">Close the form.</span></span>
16. <span data-ttu-id="ecc68-138">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="ecc68-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="ecc68-139">Arve avamine kaustast ja selle vastendamine ostutellimusega arve protsessi lõpetamiseks</span><span class="sxs-lookup"><span data-stu-id="ecc68-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="ecc68-140">Avage Ostureskontro > Arved > Arvete kaust.</span><span class="sxs-lookup"><span data-stu-id="ecc68-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="ecc68-141">Klõpsake suvandit Ostutellimus, et luua kaustas olevast arvest hankija arve.</span><span class="sxs-lookup"><span data-stu-id="ecc68-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="ecc68-142">Valige arve, mida soovite vaadata.</span><span class="sxs-lookup"><span data-stu-id="ecc68-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="ecc68-143">Vastendamise lõpetamiseks klõpsake suvandit Värskenda vastendamise olek.</span><span class="sxs-lookup"><span data-stu-id="ecc68-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="ecc68-144">Klõpsake tegumiribal valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="ecc68-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="ecc68-145">Klõpsake suvandit Muuda vaadet.</span><span class="sxs-lookup"><span data-stu-id="ecc68-145">Click Change view.</span></span>
7. <span data-ttu-id="ecc68-146">Klõpsake suvandit Ruudustikuvaade.</span><span class="sxs-lookup"><span data-stu-id="ecc68-146">Click Grid view.</span></span>
8. <span data-ttu-id="ecc68-147">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="ecc68-147">Click Post.</span></span>
9. <span data-ttu-id="ecc68-148">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="ecc68-148">Close the form.</span></span>
10. <span data-ttu-id="ecc68-149">Avage Ostureskonto > Hankijad > Hankijad.</span><span class="sxs-lookup"><span data-stu-id="ecc68-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="ecc68-150">Valige ostutellimusel olnud hankija.</span><span class="sxs-lookup"><span data-stu-id="ecc68-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="ecc68-151">Valige näiteks hankija 1001.</span><span class="sxs-lookup"><span data-stu-id="ecc68-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="ecc68-152">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ecc68-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="ecc68-153">Klõpsake tegumiribal valikut Hankija.</span><span class="sxs-lookup"><span data-stu-id="ecc68-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="ecc68-154">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="ecc68-154">Click Transactions.</span></span>
15. <span data-ttu-id="ecc68-155">Valige loodud arve.</span><span class="sxs-lookup"><span data-stu-id="ecc68-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="ecc68-156">Arve registri juurdekasv tühistati ja sisestati asjakohasele kulu kontole.</span><span class="sxs-lookup"><span data-stu-id="ecc68-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

