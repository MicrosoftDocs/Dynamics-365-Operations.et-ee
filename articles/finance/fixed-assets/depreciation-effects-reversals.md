---
title: Tühistustega kulumiefektid
description: Selles artiklis käsitletakse põhivara kande ennitamise võimalikke mõjusid.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442251"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="e44bd-103">Tühistustega kulumiefektid</span><span class="sxs-lookup"><span data-stu-id="e44bd-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e44bd-104">Selles artiklis käsitletakse põhivara kande ennitamise võimalikke mõjusid.</span><span class="sxs-lookup"><span data-stu-id="e44bd-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="e44bd-105">Põhivarakandeid, ja põhivaraga seotud kandeid saab tühistada.</span><span class="sxs-lookup"><span data-stu-id="e44bd-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="e44bd-106">Samuti saab tühistada pöördkandeid.</span><span class="sxs-lookup"><span data-stu-id="e44bd-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="e44bd-107">Saate tühistada kande, mis ei ole värskeim vara raamatusse sisestatud kanne.</span><span class="sxs-lookup"><span data-stu-id="e44bd-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="e44bd-108">Peaksite kõigepealt välja selgitama, kas pärast tühistatavat kannet on sisestatud mõni kulumikanne.</span><span class="sxs-lookup"><span data-stu-id="e44bd-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="e44bd-109">Seda seetõttu, et kulumit ei arvutata kande tühistamisel ümber.</span><span class="sxs-lookup"><span data-stu-id="e44bd-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="e44bd-110">Seetõttu on kulum pärast tühistamist sageli suurendatud või vähendatud, nagu näidetest näha.</span><span class="sxs-lookup"><span data-stu-id="e44bd-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="e44bd-111">Õige kulumi tagamiseks kande tühistamisel ärge jätkake tühistamisega, kui saate teate, mis ütleb, et kulumit ei arvutata ümber.</span><span class="sxs-lookup"><span data-stu-id="e44bd-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="e44bd-112">Selle asemel tühistage esmalt kulumikanne, mis sisestati pärast kannet, mida üritasite tühistada, ja seejärel jätkake tühistamisega.</span><span class="sxs-lookup"><span data-stu-id="e44bd-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="e44bd-113">Teid ei hoiatata kulumi ümberarvutamise eest ja saate tühistamisega jätkata.</span><span class="sxs-lookup"><span data-stu-id="e44bd-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="e44bd-114">Järgmistes näidetes on arvutused, mis tehakse, kui jätkate pärast hoiatusteate saamist, kulumikandeid esmalt tühistamata.</span><span class="sxs-lookup"><span data-stu-id="e44bd-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="e44bd-115"> Näide 1. Kulumit on suurendatud</span><span class="sxs-lookup"><span data-stu-id="e44bd-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="e44bd-116">Vara seadistatakse 5-aastase kasuliku tööea ja lineaarse kulumiga (60 kulumiperioodi).</span><span class="sxs-lookup"><span data-stu-id="e44bd-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="e44bd-117">Selles näites on kulumit suurendatud.</span><span class="sxs-lookup"><span data-stu-id="e44bd-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="e44bd-118">Vara kande ajalugu</span><span class="sxs-lookup"><span data-stu-id="e44bd-118">Asset transaction history</span></span>

| <span data-ttu-id="e44bd-119">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="e44bd-119">Date</span></span>       | <span data-ttu-id="e44bd-120">Kandetüüp</span><span class="sxs-lookup"><span data-stu-id="e44bd-120">Transaction type</span></span>                                                          | <span data-ttu-id="e44bd-121">Summa</span><span class="sxs-lookup"><span data-stu-id="e44bd-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="e44bd-122">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e44bd-122">January 1</span></span>  | <span data-ttu-id="e44bd-123">Soetamine</span><span class="sxs-lookup"><span data-stu-id="e44bd-123">Acquisition</span></span>                                                               | <span data-ttu-id="e44bd-124">59 000,00</span><span class="sxs-lookup"><span data-stu-id="e44bd-124">59,000.00</span></span>                                 |
| <span data-ttu-id="e44bd-125">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e44bd-125">January 1</span></span>  | <span data-ttu-id="e44bd-126">Soetuse korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="e44bd-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="e44bd-127">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e44bd-127">1,000.00</span></span>                                  |
| <span data-ttu-id="e44bd-128">31. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e44bd-128">January 31</span></span> | <span data-ttu-id="e44bd-129">Kulum (arvutatud, kasutades ühe perioodi kulumisoovitust)</span><span class="sxs-lookup"><span data-stu-id="e44bd-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="e44bd-130">1000.00 Arvutus: raamatupidamislik väärtus (59 000 + 1000 kulum) / järelejäänud kulumiperioodide arv (60)</span><span class="sxs-lookup"><span data-stu-id="e44bd-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="e44bd-131">Tühistustoiming</span><span class="sxs-lookup"><span data-stu-id="e44bd-131">Reversal action</span></span>

| <span data-ttu-id="e44bd-132">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="e44bd-132">Date</span></span>      | <span data-ttu-id="e44bd-133">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="e44bd-133">Transaction type</span></span>                | <span data-ttu-id="e44bd-134">Summa</span><span class="sxs-lookup"><span data-stu-id="e44bd-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="e44bd-135">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e44bd-135">January 1</span></span> | <span data-ttu-id="e44bd-136">Soetamise korrigeerimise tagasivõtmine</span><span class="sxs-lookup"><span data-stu-id="e44bd-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="e44bd-137">–1000,00</span><span class="sxs-lookup"><span data-stu-id="e44bd-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="e44bd-138">Kulumi mõju</span><span class="sxs-lookup"><span data-stu-id="e44bd-138">Depreciation effect</span></span>

| <span data-ttu-id="e44bd-139">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="e44bd-139">Date</span></span>        | <span data-ttu-id="e44bd-140">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="e44bd-140">Transaction type</span></span>        | <span data-ttu-id="e44bd-141">Summa</span><span class="sxs-lookup"><span data-stu-id="e44bd-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e44bd-142">28. veebruar</span><span class="sxs-lookup"><span data-stu-id="e44bd-142">February 28</span></span> | <span data-ttu-id="e44bd-143">Kulum (soovitus)</span><span class="sxs-lookup"><span data-stu-id="e44bd-143">Depreciation (proposal)</span></span> | <span data-ttu-id="e44bd-144">983.05 Arvutus: raamatupidamislik väärtus (59 000 – 1000 kulum) / järelejäänud kulumiperioodide arv (59)</span><span class="sxs-lookup"><span data-stu-id="e44bd-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="e44bd-145">Kulumit on suurendatud 16,95 võrra (1000 - 983,05).</span><span class="sxs-lookup"><span data-stu-id="e44bd-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="e44bd-146"> Näide 2. Kulumit on vähendatud</span><span class="sxs-lookup"><span data-stu-id="e44bd-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="e44bd-147">Vara seadistatakse 5-aastase kasuliku tööea ja lineaarse kulumiga (60 kulumiperioodi).</span><span class="sxs-lookup"><span data-stu-id="e44bd-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="e44bd-148">Selles näites on kulumit vähendatud.</span><span class="sxs-lookup"><span data-stu-id="e44bd-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="e44bd-149">Vara kande ajalugu</span><span class="sxs-lookup"><span data-stu-id="e44bd-149">Asset transaction history</span></span>

| <span data-ttu-id="e44bd-150">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="e44bd-150">Date</span></span>       | <span data-ttu-id="e44bd-151">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="e44bd-151">Transaction type</span></span>                                                          | <span data-ttu-id="e44bd-152">Summa</span><span class="sxs-lookup"><span data-stu-id="e44bd-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="e44bd-153">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e44bd-153">January 1</span></span>  | <span data-ttu-id="e44bd-154">Soetus</span><span class="sxs-lookup"><span data-stu-id="e44bd-154">Acquisition</span></span>                                                               | <span data-ttu-id="e44bd-155">59 000,00</span><span class="sxs-lookup"><span data-stu-id="e44bd-155">59,000.00</span></span>                                   |
| <span data-ttu-id="e44bd-156">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e44bd-156">January 1</span></span>  | <span data-ttu-id="e44bd-157">Allahindlus</span><span class="sxs-lookup"><span data-stu-id="e44bd-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="e44bd-158">1 000,00</span><span class="sxs-lookup"><span data-stu-id="e44bd-158">1,000.00</span></span>                                    |
| <span data-ttu-id="e44bd-159">31. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e44bd-159">January 31</span></span> | <span data-ttu-id="e44bd-160">Kulum (arvutatud, kasutades ühe perioodi kulumisoovitust)</span><span class="sxs-lookup"><span data-stu-id="e44bd-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="e44bd-161">966.67 Arvutus: raamatupidamislik väärtus (59 000 – 1000 kulum) / järelejäänud kulumiperioodide arv (60)</span><span class="sxs-lookup"><span data-stu-id="e44bd-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="e44bd-162">Tühistustoiming</span><span class="sxs-lookup"><span data-stu-id="e44bd-162">Reversal action</span></span>

| <span data-ttu-id="e44bd-163">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="e44bd-163">Date</span></span>      | <span data-ttu-id="e44bd-164">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="e44bd-164">Transaction type</span></span>               | <span data-ttu-id="e44bd-165">Summa</span><span class="sxs-lookup"><span data-stu-id="e44bd-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="e44bd-166">1. jaanuar</span><span class="sxs-lookup"><span data-stu-id="e44bd-166">January 1</span></span> | <span data-ttu-id="e44bd-167">Allahindluse tühistamine</span><span class="sxs-lookup"><span data-stu-id="e44bd-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="e44bd-168">–1000,00</span><span class="sxs-lookup"><span data-stu-id="e44bd-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="e44bd-169">Kulumi mõju</span><span class="sxs-lookup"><span data-stu-id="e44bd-169">Depreciation effect</span></span>

| <span data-ttu-id="e44bd-170">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="e44bd-170">Date</span></span>        | <span data-ttu-id="e44bd-171">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="e44bd-171">Transaction type</span></span>        | <span data-ttu-id="e44bd-172">Summa</span><span class="sxs-lookup"><span data-stu-id="e44bd-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e44bd-173">28. veebruar</span><span class="sxs-lookup"><span data-stu-id="e44bd-173">February 28</span></span> | <span data-ttu-id="e44bd-174">Kulum (soovitus)</span><span class="sxs-lookup"><span data-stu-id="e44bd-174">Depreciation (proposal)</span></span> | <span data-ttu-id="e44bd-175">983.62 Arvutus: raamatupidamislik väärtus (59 000 – 966.67 kulum) / järelejäänud kulumiperioodide arv (59)</span><span class="sxs-lookup"><span data-stu-id="e44bd-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="e44bd-176">Kulumit on vähendatud 16,95 võrra (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="e44bd-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="e44bd-177">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e44bd-177">Additional resources</span></span>
--------

[<span data-ttu-id="e44bd-178">Põhivara kulum</span><span class="sxs-lookup"><span data-stu-id="e44bd-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)



