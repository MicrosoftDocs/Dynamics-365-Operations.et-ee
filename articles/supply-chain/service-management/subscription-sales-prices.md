---
title: Kordustellimuse müügihinnad
description: Kui loote kordustellimuse, tuletatakse müügihind müügihinna seadistusest, mis loodi vormis Müügihind (kordustellimus).
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d6c59c90d49a4dcf3df4672c5f40d52ed639760c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206607"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="880d1-103">Kordustellimuse müügihinnad</span><span class="sxs-lookup"><span data-stu-id="880d1-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="880d1-104">Kui loote kordustellimuse, tuletatakse müügihind müügihinna seadistusest, mis loodi vormis **Müügihind (kordustellimus)**.</span><span class="sxs-lookup"><span data-stu-id="880d1-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="880d1-105">Vormis **Müügihind (kordustellimus)** saate luua müügihinnad konkreetsele kordustellimusele või luua müügihinnad, mis rakenduvad laiemalt.</span><span class="sxs-lookup"><span data-stu-id="880d1-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="880d1-106">Selleks et müügihind rakenduks kordustellimusel, peavad kordustellimuse perioodi kood ja valuuta ning müügihinna perioodi kood ja valuuta olema identsed.</span><span class="sxs-lookup"><span data-stu-id="880d1-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="880d1-107">Kui perioodi kood ja valuuta on kordustellimusel ja müügihinnal identsed, valitakse kordustellimuse müügihinnad alltoodud tabeli prioriteetide alusel.</span><span class="sxs-lookup"><span data-stu-id="880d1-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="880d1-108">Tühi lahter tabelis tähistab tühja välja ja X tähistab väärtust, mis on võrdne väärtusega kordustellimuses, millest tehing koostati.</span><span class="sxs-lookup"><span data-stu-id="880d1-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="880d1-109">Prioriteet </span><span class="sxs-lookup"><span data-stu-id="880d1-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="880d1-110"><strong>Kategooria</strong></span><span class="sxs-lookup"><span data-stu-id="880d1-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="880d1-111"><strong>Projekti ID</strong></span><span class="sxs-lookup"><span data-stu-id="880d1-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="880d1-112"><strong>Kordustellimus</strong></span><span class="sxs-lookup"><span data-stu-id="880d1-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="880d1-113"><strong>Müügivaluuta</strong></span><span class="sxs-lookup"><span data-stu-id="880d1-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="880d1-114"><strong>Perioodi kood</strong></span><span class="sxs-lookup"><span data-stu-id="880d1-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="880d1-115">1</span><span class="sxs-lookup"><span data-stu-id="880d1-115">1</span></span></p></td>
<td><p><span data-ttu-id="880d1-116">X</span><span class="sxs-lookup"><span data-stu-id="880d1-116">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-117">X</span><span class="sxs-lookup"><span data-stu-id="880d1-117">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-118">X</span><span class="sxs-lookup"><span data-stu-id="880d1-118">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-119">X</span><span class="sxs-lookup"><span data-stu-id="880d1-119">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-120">X</span><span class="sxs-lookup"><span data-stu-id="880d1-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="880d1-121">2</span><span class="sxs-lookup"><span data-stu-id="880d1-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="880d1-122">X</span><span class="sxs-lookup"><span data-stu-id="880d1-122">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-123">X</span><span class="sxs-lookup"><span data-stu-id="880d1-123">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-124">X</span><span class="sxs-lookup"><span data-stu-id="880d1-124">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-125">X</span><span class="sxs-lookup"><span data-stu-id="880d1-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="880d1-126">3</span><span class="sxs-lookup"><span data-stu-id="880d1-126">3</span></span></p></td>
<td><p><span data-ttu-id="880d1-127">X</span><span class="sxs-lookup"><span data-stu-id="880d1-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="880d1-128">X</span><span class="sxs-lookup"><span data-stu-id="880d1-128">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-129">X</span><span class="sxs-lookup"><span data-stu-id="880d1-129">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-130">X</span><span class="sxs-lookup"><span data-stu-id="880d1-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="880d1-131">4</span><span class="sxs-lookup"><span data-stu-id="880d1-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="880d1-132">X</span><span class="sxs-lookup"><span data-stu-id="880d1-132">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-133">X</span><span class="sxs-lookup"><span data-stu-id="880d1-133">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-134">X</span><span class="sxs-lookup"><span data-stu-id="880d1-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="880d1-135">5</span><span class="sxs-lookup"><span data-stu-id="880d1-135">5</span></span></p></td>
<td><p><span data-ttu-id="880d1-136">X</span><span class="sxs-lookup"><span data-stu-id="880d1-136">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-137">X</span><span class="sxs-lookup"><span data-stu-id="880d1-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="880d1-138">X</span><span class="sxs-lookup"><span data-stu-id="880d1-138">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-139">X</span><span class="sxs-lookup"><span data-stu-id="880d1-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="880d1-140">6</span><span class="sxs-lookup"><span data-stu-id="880d1-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="880d1-141">X</span><span class="sxs-lookup"><span data-stu-id="880d1-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="880d1-142">X</span><span class="sxs-lookup"><span data-stu-id="880d1-142">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-143">X</span><span class="sxs-lookup"><span data-stu-id="880d1-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="880d1-144">7</span><span class="sxs-lookup"><span data-stu-id="880d1-144">7</span></span></p></td>
<td><p><span data-ttu-id="880d1-145">X</span><span class="sxs-lookup"><span data-stu-id="880d1-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="880d1-146">X</span><span class="sxs-lookup"><span data-stu-id="880d1-146">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-147">X</span><span class="sxs-lookup"><span data-stu-id="880d1-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="880d1-148">8</span><span class="sxs-lookup"><span data-stu-id="880d1-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="880d1-149">X</span><span class="sxs-lookup"><span data-stu-id="880d1-149">X</span></span></p></td>
<td><p><span data-ttu-id="880d1-150">X</span><span class="sxs-lookup"><span data-stu-id="880d1-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="880d1-151">Kui luuakse kordustellimuse tasu, valitakse kordustellimuse müügihinnaks kõrgeima detailsustasemega müügihind, nagu ülaltoodud tabelis märgitud.</span><span class="sxs-lookup"><span data-stu-id="880d1-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="880d1-152">Kordustellimuste müügihindade uuendamine ja indekseerimine</span><span class="sxs-lookup"><span data-stu-id="880d1-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="880d1-153">Saate kordustellimuse müügihinda värskendada värskendades baashinda või indeksit.</span><span class="sxs-lookup"><span data-stu-id="880d1-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="880d1-154">Saate värskendada protsendi kaupa või uue väärtuseni.</span><span class="sxs-lookup"><span data-stu-id="880d1-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="880d1-155">Kordustellimuse tasu müügihinnad</span><span class="sxs-lookup"><span data-stu-id="880d1-155">Subscription fee sales prices</span></span>

<span data-ttu-id="880d1-156">Kui loote kordustellimuse tasu, põhineb müügihind kordustellimuse müügihinna seadistusel.</span><span class="sxs-lookup"><span data-stu-id="880d1-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="880d1-157">Võite kasutada kas baashinda kordustellimuse hinnaseadistusest või luua indekseeritud müügihinnad.</span><span class="sxs-lookup"><span data-stu-id="880d1-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="880d1-158">Näide</span><span class="sxs-lookup"><span data-stu-id="880d1-158">Example</span></span>

<span data-ttu-id="880d1-159">Soovite seadistada uuele projektile 9030 500 euro suurused kordustellimuse müügihinnad.</span><span class="sxs-lookup"><span data-stu-id="880d1-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="880d1-160">Vormis **Müügihind (kordustellimus)** saate luua kordustellimuse müügihinna rea, nagu näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="880d1-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="880d1-161">Kehtiv alates</span><span class="sxs-lookup"><span data-stu-id="880d1-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="880d1-162">Kategooria</span><span class="sxs-lookup"><span data-stu-id="880d1-162">Category</span></span></p></th>
<th><p><span data-ttu-id="880d1-163">Project</span><span class="sxs-lookup"><span data-stu-id="880d1-163">Project</span></span></p></th>
<th><p><span data-ttu-id="880d1-164">Korduv tellimus</span><span class="sxs-lookup"><span data-stu-id="880d1-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="880d1-165">Perioodi kood</span><span class="sxs-lookup"><span data-stu-id="880d1-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="880d1-166">Müügivaluuta</span><span class="sxs-lookup"><span data-stu-id="880d1-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="880d1-167">Müügihind</span><span class="sxs-lookup"><span data-stu-id="880d1-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="880d1-168">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="880d1-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="880d1-169">9030</span><span class="sxs-lookup"><span data-stu-id="880d1-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="880d1-170">Kuu</span><span class="sxs-lookup"><span data-stu-id="880d1-170">Month</span></span></p></td>
<td><p><span data-ttu-id="880d1-171"> eurot</span><span class="sxs-lookup"><span data-stu-id="880d1-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="880d1-172">500</span><span class="sxs-lookup"><span data-stu-id="880d1-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="880d1-173">Pange tähele, et väljad **Kategooria** ja **Kordustellimus** on tühjad.</span><span class="sxs-lookup"><span data-stu-id="880d1-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="880d1-174">Seejärel loote järgmised kordustellimused.</span><span class="sxs-lookup"><span data-stu-id="880d1-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="880d1-175">Teenuse kordustellimus</span><span class="sxs-lookup"><span data-stu-id="880d1-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="880d1-176">Project</span><span class="sxs-lookup"><span data-stu-id="880d1-176">Project</span></span></p></th>
<th><p><span data-ttu-id="880d1-177">Kordustellimuste grupp</span><span class="sxs-lookup"><span data-stu-id="880d1-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="880d1-178">Kategooria</span><span class="sxs-lookup"><span data-stu-id="880d1-178">Category</span></span></p></th>
<th><p><span data-ttu-id="880d1-179">Valuuta</span><span class="sxs-lookup"><span data-stu-id="880d1-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="880d1-180">Perioodi kood</span><span class="sxs-lookup"><span data-stu-id="880d1-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="880d1-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="880d1-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="880d1-182">9030</span><span class="sxs-lookup"><span data-stu-id="880d1-182">9030</span></span></p></td>
<td><p><span data-ttu-id="880d1-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="880d1-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="880d1-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="880d1-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="880d1-185"> eurot</span><span class="sxs-lookup"><span data-stu-id="880d1-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="880d1-186">Igakuine</span><span class="sxs-lookup"><span data-stu-id="880d1-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="880d1-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="880d1-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="880d1-188">9030</span><span class="sxs-lookup"><span data-stu-id="880d1-188">9030</span></span></p></td>
<td><p><span data-ttu-id="880d1-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="880d1-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="880d1-190">SubCat2</span><span class="sxs-lookup"><span data-stu-id="880d1-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="880d1-191"> eurot</span><span class="sxs-lookup"><span data-stu-id="880d1-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="880d1-192">Igakuine</span><span class="sxs-lookup"><span data-stu-id="880d1-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="880d1-193">Nüüd loote kordustellimuste tasud mõlemale kordusteelimusele Sub 1 kordustellimuste grupis:</span><span class="sxs-lookup"><span data-stu-id="880d1-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="880d1-194">Klõpsake valikuid **Teenuste haldus** \> **Seadistus** \> **Teenuse kordustellimused** \> **Kordustellimuste grupid**.</span><span class="sxs-lookup"><span data-stu-id="880d1-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="880d1-195">Klõpsake vormis **Kordustellimuste grupid** valikuid **Funktsioon** \> **Kordustellimuse tasu loomine**.</span><span class="sxs-lookup"><span data-stu-id="880d1-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="880d1-196">Sisestage asjakohane teave vormi **Kordustellimuse tasu loomine**.</span><span class="sxs-lookup"><span data-stu-id="880d1-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="880d1-197">Lisateavet vt teemast [Kordustellimuste tasukannete loomine](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="880d1-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="880d1-198">Kordustellimuse tasud, mille müügihind on 500 eurot, luuakse mõlema kordustellimuse jaoks, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="880d1-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="880d1-199">Projekti kuupäev</span><span class="sxs-lookup"><span data-stu-id="880d1-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="880d1-200">Teenuse kordustellimus</span><span class="sxs-lookup"><span data-stu-id="880d1-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="880d1-201">Project</span><span class="sxs-lookup"><span data-stu-id="880d1-201">Project</span></span></p></th>
<th><p><span data-ttu-id="880d1-202">Kategooria</span><span class="sxs-lookup"><span data-stu-id="880d1-202">Category</span></span></p></th>
<th><p><span data-ttu-id="880d1-203">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="880d1-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="880d1-204">Lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="880d1-204">End date</span></span></p></th>
<th><p><span data-ttu-id="880d1-205">Müügivaluuta</span><span class="sxs-lookup"><span data-stu-id="880d1-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="880d1-206">Müügihind</span><span class="sxs-lookup"><span data-stu-id="880d1-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="880d1-207">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="880d1-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="880d1-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="880d1-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="880d1-209">9030</span><span class="sxs-lookup"><span data-stu-id="880d1-209">9030</span></span></p></td>
<td><p><span data-ttu-id="880d1-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="880d1-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="880d1-211">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="880d1-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="880d1-212">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="880d1-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="880d1-213"> eurot</span><span class="sxs-lookup"><span data-stu-id="880d1-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="880d1-214">500</span><span class="sxs-lookup"><span data-stu-id="880d1-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="880d1-215">28.08.2006</span><span class="sxs-lookup"><span data-stu-id="880d1-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="880d1-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="880d1-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="880d1-217">9030</span><span class="sxs-lookup"><span data-stu-id="880d1-217">9030</span></span></p></td>
<td><p><span data-ttu-id="880d1-218">SubCat2</span><span class="sxs-lookup"><span data-stu-id="880d1-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="880d1-219">01.01.2007</span><span class="sxs-lookup"><span data-stu-id="880d1-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="880d1-220">31.03.2007</span><span class="sxs-lookup"><span data-stu-id="880d1-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="880d1-221"> eurot</span><span class="sxs-lookup"><span data-stu-id="880d1-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="880d1-222">500</span><span class="sxs-lookup"><span data-stu-id="880d1-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="880d1-223">Hiljem otsustate, et soovite täpsustada projekti 9030 kategooria SubCat1 müügihindu.</span><span class="sxs-lookup"><span data-stu-id="880d1-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="880d1-224">Seetõttu loote uue 550 euro suuruse müügihinnaga müügihinna rea projekti 9030 ja tasu kategooria SubCat1 kombinatsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="880d1-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="880d1-225">Nüüd on projekt 9030 jaoks olemas kaks kordustellimuse müügihinna rida, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="880d1-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="880d1-226">Kehtiv alates</span><span class="sxs-lookup"><span data-stu-id="880d1-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="880d1-227">Kategooria</span><span class="sxs-lookup"><span data-stu-id="880d1-227">Category</span></span></p></th>
<th><p><span data-ttu-id="880d1-228">Project</span><span class="sxs-lookup"><span data-stu-id="880d1-228">Project</span></span></p></th>
<th><p><span data-ttu-id="880d1-229">Korduv tellimus</span><span class="sxs-lookup"><span data-stu-id="880d1-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="880d1-230">Perioodi kood</span><span class="sxs-lookup"><span data-stu-id="880d1-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="880d1-231">Valuuta</span><span class="sxs-lookup"><span data-stu-id="880d1-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="880d1-232">Müügihind</span><span class="sxs-lookup"><span data-stu-id="880d1-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="880d1-233">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="880d1-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="880d1-234">9030</span><span class="sxs-lookup"><span data-stu-id="880d1-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="880d1-235">Kuu</span><span class="sxs-lookup"><span data-stu-id="880d1-235">Month</span></span></p></td>
<td><p><span data-ttu-id="880d1-236"> eurot</span><span class="sxs-lookup"><span data-stu-id="880d1-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="880d1-237">500</span><span class="sxs-lookup"><span data-stu-id="880d1-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="880d1-238">28.08.2007</span><span class="sxs-lookup"><span data-stu-id="880d1-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="880d1-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="880d1-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="880d1-240">9030</span><span class="sxs-lookup"><span data-stu-id="880d1-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="880d1-241">Kuu</span><span class="sxs-lookup"><span data-stu-id="880d1-241">Month</span></span></p></td>
<td><p><span data-ttu-id="880d1-242"> eurot</span><span class="sxs-lookup"><span data-stu-id="880d1-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="880d1-243">550</span><span class="sxs-lookup"><span data-stu-id="880d1-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="880d1-244">Kordate ülalkirjeldatud protseduuri, et luua kordustellimuste tasud mõlemale kordustellimusele kordustellimuse grupis Sub1.</span><span class="sxs-lookup"><span data-stu-id="880d1-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="880d1-245">Järgmises tabelis on näha kanded, mis luuakse kummagi kordustellimuse grupiga seotud kordustellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="880d1-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="880d1-246">Projekti kuupäev</span><span class="sxs-lookup"><span data-stu-id="880d1-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="880d1-247">Korduv tellimus</span><span class="sxs-lookup"><span data-stu-id="880d1-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="880d1-248">Project</span><span class="sxs-lookup"><span data-stu-id="880d1-248">Project</span></span></p></th>
<th><p><span data-ttu-id="880d1-249">Kategooria</span><span class="sxs-lookup"><span data-stu-id="880d1-249">Category</span></span></p></th>
<th><p><span data-ttu-id="880d1-250">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="880d1-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="880d1-251">Lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="880d1-251">End date</span></span></p></th>
<th><p><span data-ttu-id="880d1-252">Müügivaluuta</span><span class="sxs-lookup"><span data-stu-id="880d1-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="880d1-253">Müügihind</span><span class="sxs-lookup"><span data-stu-id="880d1-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="880d1-254">28.07.2007</span><span class="sxs-lookup"><span data-stu-id="880d1-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="880d1-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="880d1-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="880d1-256">9030</span><span class="sxs-lookup"><span data-stu-id="880d1-256">9030</span></span></p></td>
<td><p><span data-ttu-id="880d1-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="880d1-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="880d1-258">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="880d1-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="880d1-259">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="880d1-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="880d1-260"> eurot</span><span class="sxs-lookup"><span data-stu-id="880d1-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="880d1-261">550</span><span class="sxs-lookup"><span data-stu-id="880d1-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="880d1-262">28.07.2008</span><span class="sxs-lookup"><span data-stu-id="880d1-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="880d1-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="880d1-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="880d1-264">9030</span><span class="sxs-lookup"><span data-stu-id="880d1-264">9030</span></span></p></td>
<td><p><span data-ttu-id="880d1-265">SubCat2</span><span class="sxs-lookup"><span data-stu-id="880d1-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="880d1-266">01.01.2008</span><span class="sxs-lookup"><span data-stu-id="880d1-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="880d1-267">31.03.2008</span><span class="sxs-lookup"><span data-stu-id="880d1-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="880d1-268"> eurot</span><span class="sxs-lookup"><span data-stu-id="880d1-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="880d1-269">500</span><span class="sxs-lookup"><span data-stu-id="880d1-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="880d1-270">Esimeses tehingus kordustellimusele 00020\_135 tuletatakse 550 euro suurune müügihind kordustellimuse müügihinnast, mis on seatud konkreetse projekti ja kategooria kombinatsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="880d1-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="880d1-271">Teises tehingus kordustellimusele 00021\_135 kasutatakse 500 euro suurust müügihinda projekti kordustellimuse müügihinnana, sest projekti 9030 ja kategooria SubCat2 kombinatsioonile pole hinda seatud.</span><span class="sxs-lookup"><span data-stu-id="880d1-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="880d1-272">Vt ka</span><span class="sxs-lookup"><span data-stu-id="880d1-272">See also</span></span>

[<span data-ttu-id="880d1-273">Kordustellimuste müügihindade uuendamine ja indekseerimine</span><span class="sxs-lookup"><span data-stu-id="880d1-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


