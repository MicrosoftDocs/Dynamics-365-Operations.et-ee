---
title: Arve põhiandmed ostureskontro süsteemi arvete kausta abil
description: See teema kirjeldab, kuidas kasutada arvete loomiseks arveregistrit.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b9c54f610e45d288ed58fd209d290d73bfe1ff2f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820661"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="535fd-103">Arve põhiandmed ostureskontro süsteemi arvete kausta abil</span><span class="sxs-lookup"><span data-stu-id="535fd-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="535fd-104">See teema kirjeldab, kuidas kasutada arvete loomiseks arveregistrit.</span><span class="sxs-lookup"><span data-stu-id="535fd-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="535fd-105">Seejärel kasutage arve sobitamiseks ostutellimusega arvete kausta ja lõpetage kulu hankija arve lehel.</span><span class="sxs-lookup"><span data-stu-id="535fd-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="535fd-106">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="535fd-106">Create a purchase order</span></span>
1. <span data-ttu-id="535fd-107">Avage navigeerimispaanil **Moodulid > Ostureskontro > Ostutellimused > Ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="535fd-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="535fd-108">Ostutellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="535fd-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="535fd-109">Väljal **Tarnija konto** valige ripploendist tarnija.</span><span class="sxs-lookup"><span data-stu-id="535fd-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="535fd-110">Näiteks valige tarnija **1001**.</span><span class="sxs-lookup"><span data-stu-id="535fd-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="535fd-111">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="535fd-111">Select **OK**.</span></span>
5. <span data-ttu-id="535fd-112">Väljal **Üksuse number** valige ripploendist teenuse üksuse number.</span><span class="sxs-lookup"><span data-stu-id="535fd-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="535fd-113">Näiteks, valige **S0001**.</span><span class="sxs-lookup"><span data-stu-id="535fd-113">For example, select **S0001**.</span></span> <span data-ttu-id="535fd-114">Netosumma on 75,00.</span><span class="sxs-lookup"><span data-stu-id="535fd-114">The net amount is 75.00.</span></span>  <span data-ttu-id="535fd-115">See on summa, mida arvele eeldame.</span><span class="sxs-lookup"><span data-stu-id="535fd-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="535fd-116">Valige toimingupaanil **Osta**.</span><span class="sxs-lookup"><span data-stu-id="535fd-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="535fd-117">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="535fd-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="535fd-118">Arve loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="535fd-118">Create and post and invoice</span></span>
1. <span data-ttu-id="535fd-119">Minge navigeerimispaanil jaotisse **Moodulid > Ostureskontro > Arved > Arveregister**.</span><span class="sxs-lookup"><span data-stu-id="535fd-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="535fd-120">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="535fd-120">Select **New**.</span></span>
3. <span data-ttu-id="535fd-121">Avage otsing, et valida arveregistri nimi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="535fd-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="535fd-122">Valige selle arveregistri nimi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="535fd-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="535fd-123">Registri avamiseks ja kuluridade sisestamiseks valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="535fd-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="535fd-124">Valige otsingus hankija.</span><span class="sxs-lookup"><span data-stu-id="535fd-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="535fd-125">Näiteks valige tarnija **1001**.</span><span class="sxs-lookup"><span data-stu-id="535fd-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="535fd-126">Sisestage arve number väljale **Arve**.</span><span class="sxs-lookup"><span data-stu-id="535fd-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="535fd-127">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="535fd-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="535fd-128">Sisestage number väljale **Kreedit**.</span><span class="sxs-lookup"><span data-stu-id="535fd-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="535fd-129">Väljal **Ostutellimus** avage ripploend, et valida varem loodud ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="535fd-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="535fd-130">Väljal **Kinnitaja** tõstke esile kinnitaja ja klõpsake kinnitaja valimiseks **Vali**.</span><span class="sxs-lookup"><span data-stu-id="535fd-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="535fd-131">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="535fd-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="535fd-132">Arve avamine kaustast ja selle vastendamine ostutellimusega arve protsessi lõpetamiseks</span><span class="sxs-lookup"><span data-stu-id="535fd-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="535fd-133">Avage navigeerimispaanil **Moodulid > Ostureskontro > Arved > Arvekaust**.</span><span class="sxs-lookup"><span data-stu-id="535fd-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="535fd-134">Valige **Ostutellimus**, et luua arvete kaustast tarnija arve.</span><span class="sxs-lookup"><span data-stu-id="535fd-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="535fd-135">Valige arve, mida soovite vaadata.</span><span class="sxs-lookup"><span data-stu-id="535fd-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="535fd-136">Vastenduse lõpetamiseks valige **Vastenduse oleku värskendamine**.</span><span class="sxs-lookup"><span data-stu-id="535fd-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="535fd-137">Toimingupaanil valige **Suvandid**.</span><span class="sxs-lookup"><span data-stu-id="535fd-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="535fd-138">Valige **Muuda vaadet**.</span><span class="sxs-lookup"><span data-stu-id="535fd-138">Select **Change view**.</span></span>
7. <span data-ttu-id="535fd-139">Valige **Ruudustiku vaade**.</span><span class="sxs-lookup"><span data-stu-id="535fd-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="535fd-140">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="535fd-140">Select **Post**.</span></span>
9. <span data-ttu-id="535fd-141">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="535fd-141">Close the form.</span></span>
10. <span data-ttu-id="535fd-142">Navigeerimispaanil avage **Moodulid > Ostureskontro > Tarnijad > Tarnijad**.</span><span class="sxs-lookup"><span data-stu-id="535fd-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="535fd-143">Valige ostutellimusel olnud hankija.</span><span class="sxs-lookup"><span data-stu-id="535fd-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="535fd-144">Näiteks valige tarnija **1001**.</span><span class="sxs-lookup"><span data-stu-id="535fd-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="535fd-145">Valige toimingupaanil **Tarnija**.</span><span class="sxs-lookup"><span data-stu-id="535fd-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="535fd-146">Valige **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="535fd-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="535fd-147">Valige loodud arve.</span><span class="sxs-lookup"><span data-stu-id="535fd-147">Select the invoice that you created.</span></span> <span data-ttu-id="535fd-148">Arve registri juurdekasv tühistati ja sisestati asjakohasele kulu kontole.</span><span class="sxs-lookup"><span data-stu-id="535fd-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]