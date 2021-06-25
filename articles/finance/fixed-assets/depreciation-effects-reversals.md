---
title: Tühistustega kulumiefektid
description: Selles artiklis käsitletakse põhivara kande ennitamise võimalikke mõjusid.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d47a25835eab16438ea47bf3960132debc8c975
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187888"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="bfaaf-103">Tühistustega kulumiefektid</span><span class="sxs-lookup"><span data-stu-id="bfaaf-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfaaf-104">Selles artiklis käsitletakse põhivara kande ennitamise võimalikke mõjusid.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="bfaaf-105">Põhivarakandeid, ja põhivaraga seotud kandeid saab tühistada.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="bfaaf-106">Samuti saab tühistada pöördkandeid.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="bfaaf-107">Saate tühistada kande, mis ei ole värskeim vara raamatusse sisestatud kanne.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="bfaaf-108">Peaksite kõigepealt välja selgitama, kas pärast tühistatavat kannet on sisestatud mõni kulumikanne.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="bfaaf-109">Seda seetõttu, et kulumit ei arvutata kande tühistamisel ümber.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="bfaaf-110">Seetõttu on kulum pärast tühistamist sageli suurendatud või vähendatud, nagu näidetest näha.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="bfaaf-111">Õige kulumi tagamiseks kande tühistamisel ärge jätkake tühistamisega, kui saate teate, mis ütleb, et kulumit ei arvutata ümber.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="bfaaf-112">Selle asemel tühistage esmalt kulumikanne, mis sisestati pärast kannet, mida üritasite tühistada, ja seejärel jätkake tühistamisega.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="bfaaf-113">Teid ei hoiatata kulumi ümberarvutamise eest ja saate tühistamisega jätkata.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="bfaaf-114">Järgmistes näidetes on arvutused, mis tehakse, kui jätkate pärast hoiatusteate saamist, kulumikandeid esmalt tühistamata.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="bfaaf-115"> Näide 1. Kulumit on suurendatud</span><span class="sxs-lookup"><span data-stu-id="bfaaf-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="bfaaf-116">Vara seadistatakse 5-aastase kasuliku tööea ja lineaarse kulumiga (60 kulumiperioodi).</span><span class="sxs-lookup"><span data-stu-id="bfaaf-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="bfaaf-117">Selles näites on kulumit suurendatud.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="bfaaf-118">Vara kande ajalugu</span><span class="sxs-lookup"><span data-stu-id="bfaaf-118">Asset transaction history</span></span>

| <span data-ttu-id="bfaaf-119">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="bfaaf-119">Date</span></span>       | <span data-ttu-id="bfaaf-120">Kandetüüp</span><span class="sxs-lookup"><span data-stu-id="bfaaf-120">Transaction type</span></span>                                                          | <span data-ttu-id="bfaaf-121">Summa</span><span class="sxs-lookup"><span data-stu-id="bfaaf-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="bfaaf-122">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-122">January 1</span></span>  | <span data-ttu-id="bfaaf-123">Soetamine</span><span class="sxs-lookup"><span data-stu-id="bfaaf-123">Acquisition</span></span>                                                               | <span data-ttu-id="bfaaf-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="bfaaf-124">59,000.00</span></span>                                 |
| <span data-ttu-id="bfaaf-125">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-125">January 1</span></span>  | <span data-ttu-id="bfaaf-126">Soetuse korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="bfaaf-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="bfaaf-127">1 000,00</span><span class="sxs-lookup"><span data-stu-id="bfaaf-127">1,000.00</span></span>                                  |
| <span data-ttu-id="bfaaf-128">31. jaanuar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-128">January 31</span></span> | <span data-ttu-id="bfaaf-129">Kulum (arvutatud, kasutades ühe perioodi kulumisoovitust)</span><span class="sxs-lookup"><span data-stu-id="bfaaf-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="bfaaf-130">1000.00 Arvutus: raamatupidamislik väärtus (59 000 + 1000 kulum) / järelejäänud kulumiperioodide arv (60)</span><span class="sxs-lookup"><span data-stu-id="bfaaf-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="bfaaf-131">Tühistustoiming</span><span class="sxs-lookup"><span data-stu-id="bfaaf-131">Reversal action</span></span>

| <span data-ttu-id="bfaaf-132">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="bfaaf-132">Date</span></span>      | <span data-ttu-id="bfaaf-133">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="bfaaf-133">Transaction type</span></span>                | <span data-ttu-id="bfaaf-134">Summa</span><span class="sxs-lookup"><span data-stu-id="bfaaf-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="bfaaf-135">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-135">January 1</span></span> | <span data-ttu-id="bfaaf-136">Soetamise korrigeerimise tagasivõtmine</span><span class="sxs-lookup"><span data-stu-id="bfaaf-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="bfaaf-137">–1000,00</span><span class="sxs-lookup"><span data-stu-id="bfaaf-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="bfaaf-138">Kulumi mõju</span><span class="sxs-lookup"><span data-stu-id="bfaaf-138">Depreciation effect</span></span>

| <span data-ttu-id="bfaaf-139">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="bfaaf-139">Date</span></span>        | <span data-ttu-id="bfaaf-140">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="bfaaf-140">Transaction type</span></span>        | <span data-ttu-id="bfaaf-141">Summa</span><span class="sxs-lookup"><span data-stu-id="bfaaf-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfaaf-142">28. veebruar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-142">February 28</span></span> | <span data-ttu-id="bfaaf-143">Kulum (soovitus)</span><span class="sxs-lookup"><span data-stu-id="bfaaf-143">Depreciation (proposal)</span></span> | <span data-ttu-id="bfaaf-144">983.05 Arvutus: raamatupidamislik väärtus (59 000 – 1000 kulum) / järelejäänud kulumiperioodide arv (59)</span><span class="sxs-lookup"><span data-stu-id="bfaaf-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="bfaaf-145">Kulumit on suurendatud 16,95 võrra (1000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="bfaaf-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="bfaaf-146"> Näide 2. Kulumit on vähendatud</span><span class="sxs-lookup"><span data-stu-id="bfaaf-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="bfaaf-147">Vara seadistatakse 5-aastase kasuliku tööea ja lineaarse kulumiga (60 kulumiperioodi).</span><span class="sxs-lookup"><span data-stu-id="bfaaf-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="bfaaf-148">Selles näites on kulumit vähendatud.</span><span class="sxs-lookup"><span data-stu-id="bfaaf-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="bfaaf-149">Vara kande ajalugu</span><span class="sxs-lookup"><span data-stu-id="bfaaf-149">Asset transaction history</span></span>

| <span data-ttu-id="bfaaf-150">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="bfaaf-150">Date</span></span>       | <span data-ttu-id="bfaaf-151">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="bfaaf-151">Transaction type</span></span>                                                          | <span data-ttu-id="bfaaf-152">Summa</span><span class="sxs-lookup"><span data-stu-id="bfaaf-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="bfaaf-153">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-153">January 1</span></span>  | <span data-ttu-id="bfaaf-154">Soetus</span><span class="sxs-lookup"><span data-stu-id="bfaaf-154">Acquisition</span></span>                                                               | <span data-ttu-id="bfaaf-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="bfaaf-155">59,000.00</span></span>                                   |
| <span data-ttu-id="bfaaf-156">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-156">January 1</span></span>  | <span data-ttu-id="bfaaf-157">Allahindlus</span><span class="sxs-lookup"><span data-stu-id="bfaaf-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="bfaaf-158">1 000,00</span><span class="sxs-lookup"><span data-stu-id="bfaaf-158">1,000.00</span></span>                                    |
| <span data-ttu-id="bfaaf-159">31. jaanuar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-159">January 31</span></span> | <span data-ttu-id="bfaaf-160">Kulum (arvutatud, kasutades ühe perioodi kulumisoovitust)</span><span class="sxs-lookup"><span data-stu-id="bfaaf-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="bfaaf-161">966.67 Arvutus: raamatupidamislik väärtus (59 000 – 1000 kulum) / järelejäänud kulumiperioodide arv (60)</span><span class="sxs-lookup"><span data-stu-id="bfaaf-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="bfaaf-162">Tühistustoiming</span><span class="sxs-lookup"><span data-stu-id="bfaaf-162">Reversal action</span></span>

| <span data-ttu-id="bfaaf-163">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="bfaaf-163">Date</span></span>      | <span data-ttu-id="bfaaf-164">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="bfaaf-164">Transaction type</span></span>               | <span data-ttu-id="bfaaf-165">Summa</span><span class="sxs-lookup"><span data-stu-id="bfaaf-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="bfaaf-166">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-166">January 1</span></span> | <span data-ttu-id="bfaaf-167">Allahindluse tühistamine</span><span class="sxs-lookup"><span data-stu-id="bfaaf-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="bfaaf-168">–1000,00</span><span class="sxs-lookup"><span data-stu-id="bfaaf-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="bfaaf-169">Kulumi mõju</span><span class="sxs-lookup"><span data-stu-id="bfaaf-169">Depreciation effect</span></span>

| <span data-ttu-id="bfaaf-170">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="bfaaf-170">Date</span></span>        | <span data-ttu-id="bfaaf-171">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="bfaaf-171">Transaction type</span></span>        | <span data-ttu-id="bfaaf-172">Summa</span><span class="sxs-lookup"><span data-stu-id="bfaaf-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfaaf-173">28. veebruar</span><span class="sxs-lookup"><span data-stu-id="bfaaf-173">February 28</span></span> | <span data-ttu-id="bfaaf-174">Kulum (soovitus)</span><span class="sxs-lookup"><span data-stu-id="bfaaf-174">Depreciation (proposal)</span></span> | <span data-ttu-id="bfaaf-175">983.62 Arvutus: raamatupidamislik väärtus (59 000 – 966.67 kulum) / järelejäänud kulumiperioodide arv (59)</span><span class="sxs-lookup"><span data-stu-id="bfaaf-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="bfaaf-176">Kulumit on vähendatud 16,95 võrra (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="bfaaf-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



## <a name="additional-resources"></a><span data-ttu-id="bfaaf-177">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="bfaaf-177">Additional resources</span></span>

[<span data-ttu-id="bfaaf-178">Põhivara kulum</span><span class="sxs-lookup"><span data-stu-id="bfaaf-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]