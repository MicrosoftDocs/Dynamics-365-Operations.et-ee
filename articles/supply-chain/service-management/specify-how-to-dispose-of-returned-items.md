---
title: Tagastatud kaupade likvideerimise viisi määratlemine
description: Määratlege tagastatud kaupade likvideerimise viis.
author: ShylaThompson
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eaeb2589329809e57ac01aba85067e94c15477c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5817481"
---
# <a name="specify-how-to-dispose-of-returned-items"></a><span data-ttu-id="366ff-103">Tagastatud kaupade likvideerimise viisi määratlemine</span><span class="sxs-lookup"><span data-stu-id="366ff-103">Specify how to dispose of returned items</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="366ff-104">Kui töötlete tagastuskorraldust, peate määrama põhjusekoodi selgitamaks, miks toode tagastatakse.</span><span class="sxs-lookup"><span data-stu-id="366ff-104">When you handle a return order, you must specify a reason return code to identify why the product is being returned.</span></span> <span data-ttu-id="366ff-105">Peate määrama ka likvideerimiskoodi ja likvideerimistegevuse, et määratleda, mida teha tagastatud tootega.</span><span class="sxs-lookup"><span data-stu-id="366ff-105">You must also specify a disposition code and a disposition action to determine what should be done with the returned product itself.</span></span>

<span data-ttu-id="366ff-106">Likvideerimiskoodi saab rakendada, kui loote tagastustellimuse, registreerite kauba saabumise või kauba saabumise saatelehe uuenduse ja lõpetate vahelao orderi.</span><span class="sxs-lookup"><span data-stu-id="366ff-106">A disposition code can be applied when you create the return order, register item arrival or packing-slip update an item arrival, and end a quarantine order.</span></span>

<span data-ttu-id="366ff-107">Saate määratleda kõiki likvideerimiskoode, mida äriprotsessi toetamiseks tarvis.</span><span class="sxs-lookup"><span data-stu-id="366ff-107">You can define any disposition codes that you need in order to support the business processes.</span></span> <span data-ttu-id="366ff-108">Järgnev tabel annab tavaliselt kasutatavate koodide komplekti, et määrata tagastatud kauba likvideerimine.</span><span class="sxs-lookup"><span data-stu-id="366ff-108">The following table provides a set of typically used codes to assign return-item disposition.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="366ff-109">Likvideerimise tüüp</span><span class="sxs-lookup"><span data-stu-id="366ff-109">Disposition type</span></span></p></th>
<th><p><span data-ttu-id="366ff-110">Tavaline kood</span><span class="sxs-lookup"><span data-stu-id="366ff-110">Common code</span></span></p></th>
<th><p><span data-ttu-id="366ff-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="366ff-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="366ff-112">Likvideerimine</span><span class="sxs-lookup"><span data-stu-id="366ff-112">Disposal</span></span></p></td>
<td><p><span data-ttu-id="366ff-113">SC</span><span class="sxs-lookup"><span data-stu-id="366ff-113">SC</span></span></p></td>
<td><p><span data-ttu-id="366ff-114">Mahakandmine/Hävitamine</span><span class="sxs-lookup"><span data-stu-id="366ff-114">Scrap/Destroy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-115">Likvideerimine</span><span class="sxs-lookup"><span data-stu-id="366ff-115">Disposal</span></span></p></td>
<td><p><span data-ttu-id="366ff-116">DC</span><span class="sxs-lookup"><span data-stu-id="366ff-116">DC</span></span></p></td>
<td><p><span data-ttu-id="366ff-117">Annetamine heategevuseks</span><span class="sxs-lookup"><span data-stu-id="366ff-117">Donate to Charity</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="366ff-118">Likvideerimine</span><span class="sxs-lookup"><span data-stu-id="366ff-118">Disposal</span></span></p></td>
<td><p><span data-ttu-id="366ff-119">TD</span><span class="sxs-lookup"><span data-stu-id="366ff-119">TD</span></span></p></td>
<td><p><span data-ttu-id="366ff-120">Kolmanda osapoole likvideerimine</span><span class="sxs-lookup"><span data-stu-id="366ff-120">Third-Party Disposal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-121">Likvideerimine</span><span class="sxs-lookup"><span data-stu-id="366ff-121">Disposal</span></span></p></td>
<td><p><span data-ttu-id="366ff-122">SL</span><span class="sxs-lookup"><span data-stu-id="366ff-122">SL</span></span></p></td>
<td><p><span data-ttu-id="366ff-123">Jääkväärtus</span><span class="sxs-lookup"><span data-stu-id="366ff-123">Salvage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="366ff-124">Likvideerimine</span><span class="sxs-lookup"><span data-stu-id="366ff-124">Disposal</span></span></p></td>
<td><p><span data-ttu-id="366ff-125">TS</span><span class="sxs-lookup"><span data-stu-id="366ff-125">TS</span></span></p></td>
<td><p><span data-ttu-id="366ff-126">Kolmanda osapoole müük (teisejärgulised turud)</span><span class="sxs-lookup"><span data-stu-id="366ff-126">Third-Party Sale (Secondary Markets)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-127">Paranda/Muuda</span><span class="sxs-lookup"><span data-stu-id="366ff-127">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="366ff-128">RW</span><span class="sxs-lookup"><span data-stu-id="366ff-128">RW</span></span></p></td>
<td><p><span data-ttu-id="366ff-129">Taastöötlus</span><span class="sxs-lookup"><span data-stu-id="366ff-129">Rework</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="366ff-130">Paranda/Muuda</span><span class="sxs-lookup"><span data-stu-id="366ff-130">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="366ff-131">RF</span><span class="sxs-lookup"><span data-stu-id="366ff-131">RF</span></span></p></td>
<td><p><span data-ttu-id="366ff-132">Taastootmine/Remontimine</span><span class="sxs-lookup"><span data-stu-id="366ff-132">Remanufacture/Refurbish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-133">Paranda/Muuda</span><span class="sxs-lookup"><span data-stu-id="366ff-133">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="366ff-134">MD</span><span class="sxs-lookup"><span data-stu-id="366ff-134">MD</span></span></p></td>
<td><p><span data-ttu-id="366ff-135">Muuda</span><span class="sxs-lookup"><span data-stu-id="366ff-135">Modify</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="366ff-136">Paranda/Muuda</span><span class="sxs-lookup"><span data-stu-id="366ff-136">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="366ff-137">RP</span><span class="sxs-lookup"><span data-stu-id="366ff-137">RP</span></span></p></td>
<td><p><span data-ttu-id="366ff-138">Remont</span><span class="sxs-lookup"><span data-stu-id="366ff-138">Repair</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-139">Paranda/Muuda</span><span class="sxs-lookup"><span data-stu-id="366ff-139">Repair/Modify</span></span></p></td>
<td><p><span data-ttu-id="366ff-140">RV</span><span class="sxs-lookup"><span data-stu-id="366ff-140">RV</span></span></p></td>
<td><p><span data-ttu-id="366ff-141">Tagasta tarnijale</span><span class="sxs-lookup"><span data-stu-id="366ff-141">Return to Vendor</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="366ff-142">Muu</span><span class="sxs-lookup"><span data-stu-id="366ff-142">Other</span></span></p></td>
<td><p><span data-ttu-id="366ff-143">AI</span><span class="sxs-lookup"><span data-stu-id="366ff-143">AI</span></span></p></td>
<td><p><span data-ttu-id="366ff-144">Kasuta nii, nagu on</span><span class="sxs-lookup"><span data-stu-id="366ff-144">Use as is</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-145">Muu</span><span class="sxs-lookup"><span data-stu-id="366ff-145">Other</span></span></p></td>
<td><p><span data-ttu-id="366ff-146">RS</span><span class="sxs-lookup"><span data-stu-id="366ff-146">RS</span></span></p></td>
<td><p><span data-ttu-id="366ff-147">Uuestimüük</span><span class="sxs-lookup"><span data-stu-id="366ff-147">Resale</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="366ff-148">Muu</span><span class="sxs-lookup"><span data-stu-id="366ff-148">Other</span></span></p></td>
<td><p><span data-ttu-id="366ff-149">EX</span><span class="sxs-lookup"><span data-stu-id="366ff-149">EX</span></span></p></td>
<td><p><span data-ttu-id="366ff-150">Rahavahetus</span><span class="sxs-lookup"><span data-stu-id="366ff-150">Exchange</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-151">Muu</span><span class="sxs-lookup"><span data-stu-id="366ff-151">Other</span></span></p></td>
<td><p><span data-ttu-id="366ff-152">MS</span><span class="sxs-lookup"><span data-stu-id="366ff-152">MS</span></span></p></td>
<td><p><span data-ttu-id="366ff-153">Muud</span><span class="sxs-lookup"><span data-stu-id="366ff-153">Miscellaneous</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="366ff-154">Iga määratletava likvideerimistähise jaoks peate valima likvideerimistegevuse.</span><span class="sxs-lookup"><span data-stu-id="366ff-154">For each disposition code that you define, you must select a disposition action.</span></span> <span data-ttu-id="366ff-155">Likvideerimistegevus määrab likvideerimiskoodide füüsilised ja majanduslikud mõjud.</span><span class="sxs-lookup"><span data-stu-id="366ff-155">The disposition action determines the physical and financial implications of the disposition codes.</span></span> <span data-ttu-id="366ff-156">Näiteks määrab likvideerimisetegevus tagastatud füüsilise käitlemise, tagastatud kauba rahalise mõju ja kas kliendile tuleb saata asenduskaup.</span><span class="sxs-lookup"><span data-stu-id="366ff-156">For example, the disposition action determines the physical handling of the returned item, the financial effect of the returned item, and if a replacement item must be sent to the customer.</span></span> <span data-ttu-id="366ff-157">Saate määrata piiramatu arvu likvideerimiskoode vastavalt oma ettevõtte vajadustele, kuid on olemas ainult kuus eelmääratletud likvideerimistegevust, mida saab valida.</span><span class="sxs-lookup"><span data-stu-id="366ff-157">You can define an unlimited number of disposition codes according to your business needs, but there are only six predefined disposition actions that you can select from.</span></span> <span data-ttu-id="366ff-158">Järgnev tabel annab likvideerimistegevused ja nende definitsioonid.</span><span class="sxs-lookup"><span data-stu-id="366ff-158">The following table provides the disposition actions and their definitions.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="366ff-159">Likvideerimistegevus</span><span class="sxs-lookup"><span data-stu-id="366ff-159">Disposition action</span></span></p></th>
<th><p><span data-ttu-id="366ff-160">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="366ff-160">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="366ff-161"><strong>Krediit</strong></span><span class="sxs-lookup"><span data-stu-id="366ff-161"><strong>Credit</strong></span></span></p></td>
<td><p><span data-ttu-id="366ff-162">Tagastage kaup varudesse ja tagastage kliendile makse.</span><span class="sxs-lookup"><span data-stu-id="366ff-162">Return the item to inventory and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-163"><strong>Ainult kreedit</strong></span><span class="sxs-lookup"><span data-stu-id="366ff-163"><strong>Credit only</strong></span></span></p></td>
<td><p><span data-ttu-id="366ff-164">Kliendile tagastatakse makse ilma kauba tagastamist nõudmata või eeldamata.</span><span class="sxs-lookup"><span data-stu-id="366ff-164">Credit the customer without requiring or expecting the item to be returned.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="366ff-165"><strong>Praak</strong></span><span class="sxs-lookup"><span data-stu-id="366ff-165"><strong>Scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="366ff-166">Lugege kaup praagiks ja tagastage kliendile makse.</span><span class="sxs-lookup"><span data-stu-id="366ff-166">Scrap the item and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-167"><strong>Asenda ja kanna kreeditisse</strong></span><span class="sxs-lookup"><span data-stu-id="366ff-167"><strong>Replace and credit</strong></span></span></p></td>
<td><p><span data-ttu-id="366ff-168">Tagastage kaup varudesse, looge asenduskorraldus ja tagastage kliendile makse.</span><span class="sxs-lookup"><span data-stu-id="366ff-168">Return the item to inventory, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="366ff-169"><strong>Asenda ja kanna praaki</strong></span><span class="sxs-lookup"><span data-stu-id="366ff-169"><strong>Replace and scrap</strong></span></span></p></td>
<td><p><span data-ttu-id="366ff-170">Lugege kaup praagiks, looge asendamiskorraldus ja tagastage kliendile makse.</span><span class="sxs-lookup"><span data-stu-id="366ff-170">Scrap the item, create a replacement order, and credit the customer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="366ff-171"><strong>Tagasta kliendile</strong></span><span class="sxs-lookup"><span data-stu-id="366ff-171"><strong>Return to customer</strong></span></span></p></td>
<td><p><span data-ttu-id="366ff-172">Lükake kauba tagastamine tagasi ja tagastage see kliendile.</span><span class="sxs-lookup"><span data-stu-id="366ff-172">Reject the returned item and return it to the customer.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a><span data-ttu-id="366ff-173">Likvideerimiskoodi valimine vahelao orderile</span><span class="sxs-lookup"><span data-stu-id="366ff-173">Select a disposition code for a quarantine order</span></span>

1.  <span data-ttu-id="366ff-174">Klõpsake valikuid **Varude haldamine** \> **Perioodiline** \> **Kvaliteedijuhtimine** \> **Vahelao orderid**.</span><span class="sxs-lookup"><span data-stu-id="366ff-174">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="366ff-175">Olemasoleva vahelao orderi jaoks valige tegevus väljalt **Likvideerimiskood** vahekaardil **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="366ff-175">For an existing quarantine order, select an action from the **Disposition code** field on the **Overview** tab.</span></span>



## <a name="see-also"></a><span data-ttu-id="366ff-176">Vt ka</span><span class="sxs-lookup"><span data-stu-id="366ff-176">See also</span></span>

<span data-ttu-id="366ff-177">[Vahelao order (vorm)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="366ff-177">[Quarantine order (form)](https://technet.microsoft.com/library/aa554073(v=ax.60))</span></span>

<span data-ttu-id="366ff-178">[Likvideerimiskoodid (vorm)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="366ff-178">[Disposition codes (form)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))</span></span>

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]