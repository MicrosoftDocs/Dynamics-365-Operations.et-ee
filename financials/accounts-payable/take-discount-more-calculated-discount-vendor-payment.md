---
title: "Hankija makse arvutatud skontost suurema skonto võtmine"
description: "See artikkel juhatab teid läbi stsenaariumi, kus skonto võetakse summast, mis on suurem kui algselt arvel olev allahindlus. See stsenaarium võib ilmneda juhul, kui organisatsioon lepib müüjaga kokku arvel väiksema summa maksmises."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 39830014593b7b1bc2868afffcca0f77a0c8a029
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="d8fdd-104">Hankija makse arvutatud skontost suurema skonto võtmine</span><span class="sxs-lookup"><span data-stu-id="d8fdd-104">Take a discount that is more than the calculated discount for a vendor payment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d8fdd-105">See artikkel juhatab teid läbi stsenaariumi, kus skonto võetakse summast, mis on suurem kui algselt arvel olev allahindlus.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="d8fdd-106">See stsenaarium võib ilmneda juhul, kui organisatsioon lepib müüjaga kokku arvel väiksema summa maksmises.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="d8fdd-107">Hankija 3051 annab Fabrikamile 4% skontot, kui arve tasutakse seitsme päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="d8fdd-108">April sisestab 29. juunil arve summas 1000,00.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="d8fdd-109">Hankija laseb Aprilil võtta skonto summas 60,00 vaikimisi arve jaoks saadaval oleva skonto 40,00 asemel.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="d8fdd-110">April kirjendab ühekordse makse, kasutades töölehte Ostureskontro makse.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="d8fdd-111">Ta sisestab makse jaoks hankija ja avab seejärel lehe **Kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="d8fdd-112">Ta märgib arve ja muudab välja **Skonto summa** väärtuseks **60,00**.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>
| <span data-ttu-id="d8fdd-113">Märge</span><span class="sxs-lookup"><span data-stu-id="d8fdd-113">Mark</span></span>     | <span data-ttu-id="d8fdd-114">Kasuta skontot</span><span class="sxs-lookup"><span data-stu-id="d8fdd-114">Use cash discount</span></span> | <span data-ttu-id="d8fdd-115">Kanne</span><span class="sxs-lookup"><span data-stu-id="d8fdd-115">Voucher</span></span>   | <span data-ttu-id="d8fdd-116">Konto</span><span class="sxs-lookup"><span data-stu-id="d8fdd-116">Account</span></span> | <span data-ttu-id="d8fdd-117">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="d8fdd-117">Date</span></span>      | <span data-ttu-id="d8fdd-118">Tähtaeg</span><span class="sxs-lookup"><span data-stu-id="d8fdd-118">Due date</span></span>  | <span data-ttu-id="d8fdd-119">Arve</span><span class="sxs-lookup"><span data-stu-id="d8fdd-119">Invoice</span></span> | <span data-ttu-id="d8fdd-120">Summa kandevaluutas</span><span class="sxs-lookup"><span data-stu-id="d8fdd-120">Amount in transaction currency</span></span> | <span data-ttu-id="d8fdd-121">Valuuta</span><span class="sxs-lookup"><span data-stu-id="d8fdd-121">Currency</span></span> | <span data-ttu-id="d8fdd-122">Tasakaalustatav summa</span><span class="sxs-lookup"><span data-stu-id="d8fdd-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="d8fdd-123">Valitud</span><span class="sxs-lookup"><span data-stu-id="d8fdd-123">Selected</span></span> | <span data-ttu-id="d8fdd-124">Tavaline</span><span class="sxs-lookup"><span data-stu-id="d8fdd-124">Normal</span></span>            | <span data-ttu-id="d8fdd-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="d8fdd-125">Inv-10040</span></span> | <span data-ttu-id="d8fdd-126">3051</span><span class="sxs-lookup"><span data-stu-id="d8fdd-126">3051</span></span>    | <span data-ttu-id="d8fdd-127">29.06.2015</span><span class="sxs-lookup"><span data-stu-id="d8fdd-127">6/29/2015</span></span> | <span data-ttu-id="d8fdd-128">29.07.2015</span><span class="sxs-lookup"><span data-stu-id="d8fdd-128">7/29/2015</span></span> | <span data-ttu-id="d8fdd-129">10040</span><span class="sxs-lookup"><span data-stu-id="d8fdd-129">10040</span></span>   | <span data-ttu-id="d8fdd-130">1 000,00</span><span class="sxs-lookup"><span data-stu-id="d8fdd-130">1,000.00</span></span>                       | <span data-ttu-id="d8fdd-131">USA dollar</span><span class="sxs-lookup"><span data-stu-id="d8fdd-131">USD</span></span>      | <span data-ttu-id="d8fdd-132">940,00</span><span class="sxs-lookup"><span data-stu-id="d8fdd-132">940.00</span></span>           |

<span data-ttu-id="d8fdd-133">Teave märgitud arve allahindluse kohta kuvatakse lehe **Kannete tasakaalustamine** allosas.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>
|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="d8fdd-134">Skonto kuupäev</span><span class="sxs-lookup"><span data-stu-id="d8fdd-134">Cash discount date</span></span>           | <span data-ttu-id="d8fdd-135">12.07.2015</span><span class="sxs-lookup"><span data-stu-id="d8fdd-135">7/12/2015</span></span> |
| <span data-ttu-id="d8fdd-136">Skonto summa</span><span class="sxs-lookup"><span data-stu-id="d8fdd-136">Cash discount amount</span></span>         | <span data-ttu-id="d8fdd-137">60,00</span><span class="sxs-lookup"><span data-stu-id="d8fdd-137">60.00</span></span>     |
| <span data-ttu-id="d8fdd-138">Kasuta skontot</span><span class="sxs-lookup"><span data-stu-id="d8fdd-138">Use cash discount</span></span>            | <span data-ttu-id="d8fdd-139">Tavaline</span><span class="sxs-lookup"><span data-stu-id="d8fdd-139">Normal</span></span>    |
| <span data-ttu-id="d8fdd-140">Võetud skonto</span><span class="sxs-lookup"><span data-stu-id="d8fdd-140">Cash discount taken</span></span>          | <span data-ttu-id="d8fdd-141">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fdd-141">0.00</span></span>      |
| <span data-ttu-id="d8fdd-142">Skonto summa võtmiseks</span><span class="sxs-lookup"><span data-stu-id="d8fdd-142">Cash discount amount to take</span></span> | <span data-ttu-id="d8fdd-143">60,00</span><span class="sxs-lookup"><span data-stu-id="d8fdd-143">60.00</span></span>     |

<span data-ttu-id="d8fdd-144">April sisestab maksetöölehe.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-144">April posts the payment journal.</span></span> <span data-ttu-id="d8fdd-145">Arve on täielikult tasakaalustatud maksega summas 940,00 ja skontoga summas 60,00.</span><span class="sxs-lookup"><span data-stu-id="d8fdd-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>




