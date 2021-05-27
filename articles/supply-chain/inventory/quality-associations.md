---
title: Kvaliteediseosed
description: See teema kirjeldab, kuidas saate kasutada Microsoft Dynamics 365 Supply Chain Management kvaliteediseoseid, et luua automaatselt teie müügi-, ostu- ja tootmisprotsessidega seotud kvaliteettellimusi.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c6fab1b89b7e58d9e443c27da03a6b13afcc9c6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022320"
---
# <a name="quality-associations"></a><span data-ttu-id="3340b-103">Kvaliteediseosed</span><span class="sxs-lookup"><span data-stu-id="3340b-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3340b-104">See teema kirjeldab, kuidas saate kasutada Microsoft Dynamics 365 Supply Chain Management kvaliteediseoseid, et luua automaatselt teie müügi-, ostu- ja tootmisprotsessidega seotud kvaliteettellimusi.</span><span class="sxs-lookup"><span data-stu-id="3340b-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="3340b-105">Kvaliteediseos määratleb koostatava kvaliteettellimuse puhul kogu järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="3340b-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="3340b-106">Kande sündmus</span><span class="sxs-lookup"><span data-stu-id="3340b-106">The transaction event</span></span>
- <span data-ttu-id="3340b-107">Kaupade puhul tehtavate katsete kogum</span><span class="sxs-lookup"><span data-stu-id="3340b-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="3340b-108">Vastuvõetav kvaliteeditase (AQL)</span><span class="sxs-lookup"><span data-stu-id="3340b-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="3340b-109">Valimi plaan</span><span class="sxs-lookup"><span data-stu-id="3340b-109">The sampling plan</span></span>

<span data-ttu-id="3340b-110">Kvaliteediseos tuleb automaatset kvaliteettellimuse genereerimist nõudvas äriprotsessis määrata iga variatsiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="3340b-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="3340b-111">Näiteks saab kvaliteettellimuse koostada ostutellimuste, vahelaotellimuste, müügitellimuste ja tootmistellimuste äriprotsessides.</span><span class="sxs-lookup"><span data-stu-id="3340b-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="3340b-112">Kvaliteediseostega töötamine</span><span class="sxs-lookup"><span data-stu-id="3340b-112">Working with quality associations</span></span>

<span data-ttu-id="3340b-113">Kvaliteediseost kasutav äriprotsess võib olla seotud mitmesuguste lähtedokumentidega, nt ostutellimuste, müügitellimuste või tootmistellimustega.</span><span class="sxs-lookup"><span data-stu-id="3340b-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="3340b-114">Iga kvaliteediseose kirje määrab ka katsete kogumi, AQL-i ning valikukava, mida rakendatakse loodud kvaliteettellimustele.</span><span class="sxs-lookup"><span data-stu-id="3340b-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="3340b-115">Peate iga äriprotsessi variatsiooni jaoks määratlema kvaliteediseose kirje.</span><span class="sxs-lookup"><span data-stu-id="3340b-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="3340b-116">Näiteks saate seadistada kvaliteediseose, mis koostab kvaliteettellimuse, kui ostutellimuse toote sissetulekut värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="3340b-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="3340b-117">Sõltuvalt täitmisplaani seadistusest saab käivitamisprotsessi ise blokeerida, kui on avatud kvaliteettellimus.</span><span class="sxs-lookup"><span data-stu-id="3340b-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="3340b-118">Teise võimalusena saab blokeerida järgnevad protsessid, näiteks ostutellimuse arveldamine.</span><span class="sxs-lookup"><span data-stu-id="3340b-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="3340b-119">Kui on avatud kvaliteettellimusi, blokeeritakse varude koguste väljastamine automaatselt.</span><span class="sxs-lookup"><span data-stu-id="3340b-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="3340b-120">Olenevalt valiku **Täielik blokeerimine** seadistusest lehel **Kaubaproovid** on kogus kas kvaliteettellimusel olev kogus või lähtedokumendi real olev kogus.</span><span class="sxs-lookup"><span data-stu-id="3340b-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="3340b-121">Lisateavet vt [Kvaliteedijuhtimise kauba valim](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="3340b-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="3340b-122">Konkreetse äriprotsessi jaoks määratleb kvaliteediseos kirje sündmuse ja tingimused, mille jaoks kvaliteettellimus genereeritakse.</span><span class="sxs-lookup"><span data-stu-id="3340b-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="3340b-123">Tingimused võivad olla asukoha või juriidilise isiku põhised.</span><span class="sxs-lookup"><span data-stu-id="3340b-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="3340b-124">Purustavaid katseid hõlmavat kvaliteettellimust saab luua ainult siis, kui sündmusel on olemas vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="3340b-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="3340b-125">Kvaliteediseostega tööks minge **Varude haldus \> Seadistus \> Kvaliteedikontroll \> Kvaliteediseosed**.</span><span class="sxs-lookup"><span data-stu-id="3340b-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="3340b-126">Järgmistes näidetes on näha, kuidas kvaliteediseose kirjet määratakse iga äriprotsessi variatsiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="3340b-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="3340b-127">Iga näite puhul võetakse järgmises tabelis kokku sündmused ja tingimused, mis on kvaliteediseose kirjega määratletud.</span><span class="sxs-lookup"><span data-stu-id="3340b-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3340b-128">Viite tüüp</span><span class="sxs-lookup"><span data-stu-id="3340b-128">Reference type</span></span></th>
<th><span data-ttu-id="3340b-129">Sündmuse tüüp</span><span class="sxs-lookup"><span data-stu-id="3340b-129">Event type</span></span></th>
<th><span data-ttu-id="3340b-130">Käivitamine</span><span class="sxs-lookup"><span data-stu-id="3340b-130">Execution</span></span></th>
<th><span data-ttu-id="3340b-131">Sündmuse blokeerimine</span><span class="sxs-lookup"><span data-stu-id="3340b-131">Event blocking</span></span></th>
<th><span data-ttu-id="3340b-132">Dokumendi viide</span><span class="sxs-lookup"><span data-stu-id="3340b-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3340b-133">Varud</span><span class="sxs-lookup"><span data-stu-id="3340b-133">Inventory</span></span></td>
<td><span data-ttu-id="3340b-134">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="3340b-134">Not applicable</span></span></td>
<td><span data-ttu-id="3340b-135">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="3340b-135">Not applicable</span></span></td>
<td><span data-ttu-id="3340b-136">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-136">None</span></span></td>
<td><span data-ttu-id="3340b-137">Kõik</span><span class="sxs-lookup"><span data-stu-id="3340b-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="3340b-138">Müük</span><span class="sxs-lookup"><span data-stu-id="3340b-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="3340b-139">Komplekteerimise protsess on plaanitud</span><span class="sxs-lookup"><span data-stu-id="3340b-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="3340b-140">Enne</span><span class="sxs-lookup"><span data-stu-id="3340b-140">Before</span></span></td>
<td><span data-ttu-id="3340b-141">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="3340b-142">Ainult Konkreetne ID, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="3340b-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-143">Komplekteerimise protsess</span><span class="sxs-lookup"><span data-stu-id="3340b-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-144">Saateleht</span><span class="sxs-lookup"><span data-stu-id="3340b-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-145">Arve</span><span class="sxs-lookup"><span data-stu-id="3340b-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3340b-146">Saateleht</span><span class="sxs-lookup"><span data-stu-id="3340b-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-147">Enne</span><span class="sxs-lookup"><span data-stu-id="3340b-147">Before</span></span></td>
<td><span data-ttu-id="3340b-148">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-149">Saateleht</span><span class="sxs-lookup"><span data-stu-id="3340b-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-150">Arve</span><span class="sxs-lookup"><span data-stu-id="3340b-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="3340b-151">Ost</span><span class="sxs-lookup"><span data-stu-id="3340b-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="3340b-152">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="3340b-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="3340b-153">Enne</span><span class="sxs-lookup"><span data-stu-id="3340b-153">Before</span></span></td>
<td><span data-ttu-id="3340b-154">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-155">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="3340b-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-156">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="3340b-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-157">Arve</span><span class="sxs-lookup"><span data-stu-id="3340b-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3340b-158">Pärast</span><span class="sxs-lookup"><span data-stu-id="3340b-158">After</span></span></td>
<td><span data-ttu-id="3340b-159">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-160">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="3340b-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-161">Arve</span><span class="sxs-lookup"><span data-stu-id="3340b-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3340b-162">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="3340b-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-163">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="3340b-163">Not applicable</span></span></td>
<td><span data-ttu-id="3340b-164">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-165">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="3340b-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-166">Arve</span><span class="sxs-lookup"><span data-stu-id="3340b-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3340b-167">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="3340b-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-168">Enne</span><span class="sxs-lookup"><span data-stu-id="3340b-168">Before</span></span></td>
<td><span data-ttu-id="3340b-169">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-170">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="3340b-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-171">Arve</span><span class="sxs-lookup"><span data-stu-id="3340b-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3340b-172">Pärast</span><span class="sxs-lookup"><span data-stu-id="3340b-172">After</span></span></td>
<td><span data-ttu-id="3340b-173">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-174">Arve</span><span class="sxs-lookup"><span data-stu-id="3340b-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="3340b-175">Tootmine</span><span class="sxs-lookup"><span data-stu-id="3340b-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-176">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="3340b-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-177">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="3340b-177">Not applicable</span></span></td>
<td><span data-ttu-id="3340b-178">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="3340b-179">Kõik</span><span class="sxs-lookup"><span data-stu-id="3340b-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-180">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="3340b-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-181">Lõpp</span><span class="sxs-lookup"><span data-stu-id="3340b-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3340b-182">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="3340b-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-183">Enne</span><span class="sxs-lookup"><span data-stu-id="3340b-183">Before</span></span></td>
<td><span data-ttu-id="3340b-184">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-185">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="3340b-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-186">Lõpp</span><span class="sxs-lookup"><span data-stu-id="3340b-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3340b-187">Pärast</span><span class="sxs-lookup"><span data-stu-id="3340b-187">After</span></span></td>
<td><span data-ttu-id="3340b-188">Puudub</span><span class="sxs-lookup"><span data-stu-id="3340b-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-189">Lõpp</span><span class="sxs-lookup"><span data-stu-id="3340b-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="3340b-190">Vaheladu</span><span class="sxs-lookup"><span data-stu-id="3340b-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-191">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="3340b-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="3340b-192">Enne</span><span class="sxs-lookup"><span data-stu-id="3340b-192">Before</span></span></td>
<td><span data-ttu-id="3340b-193">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="3340b-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-194">Lõpp</span><span class="sxs-lookup"><span data-stu-id="3340b-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-195">Pärast</span><span class="sxs-lookup"><span data-stu-id="3340b-195">After</span></span></td>
<td><span data-ttu-id="3340b-196">Lõpp</span><span class="sxs-lookup"><span data-stu-id="3340b-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-197">Lõpp</span><span class="sxs-lookup"><span data-stu-id="3340b-197">End</span></span></td>
<td><span data-ttu-id="3340b-198">Enne</span><span class="sxs-lookup"><span data-stu-id="3340b-198">Before</span></span></td>
<td><span data-ttu-id="3340b-199">Lõpp</span><span class="sxs-lookup"><span data-stu-id="3340b-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3340b-200">Protsessi operatsioon</span><span class="sxs-lookup"><span data-stu-id="3340b-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-201">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="3340b-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="3340b-202">Enne</span><span class="sxs-lookup"><span data-stu-id="3340b-202">Before</span></span></td>
<td><span data-ttu-id="3340b-203">None</span><span class="sxs-lookup"><span data-stu-id="3340b-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-204">Konkreetne ID, Grupp või Kõik ja Ressursipõhine, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="3340b-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-205">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="3340b-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-206">Pärast</span><span class="sxs-lookup"><span data-stu-id="3340b-206">After</span></span></td>
<td><span data-ttu-id="3340b-207">None</span><span class="sxs-lookup"><span data-stu-id="3340b-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3340b-208">Kaastoote tootmine</span><span class="sxs-lookup"><span data-stu-id="3340b-208">Co-product production</span></span></td>
<td><span data-ttu-id="3340b-209">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="3340b-209">Registration</span></span></td>
<td><span data-ttu-id="3340b-210">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="3340b-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-211">None</span><span class="sxs-lookup"><span data-stu-id="3340b-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="3340b-212">Kõik</span><span class="sxs-lookup"><span data-stu-id="3340b-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3340b-213">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="3340b-213">Report as finished</span></span></td>
<td><span data-ttu-id="3340b-214">Enne</span><span class="sxs-lookup"><span data-stu-id="3340b-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-215">Pärast</span><span class="sxs-lookup"><span data-stu-id="3340b-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="3340b-216">Funktsioon *Kvaliteedijuhtimine laoprotsesside jaoks* lisab võimalusi kvaliteettellimuse töötlemiseks tootmise puhul, mille **Sündmuse tüüp** on seatud väärtusele *Teata lõpetamisest* ja **Käivitamine** väärtusele *Pärast*, ning ostude puhul, mille **Sündmuse tüüp** on seatud väärtusele *Registreerimine*.</span><span class="sxs-lookup"><span data-stu-id="3340b-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="3340b-217">Lisateabe saamiseks vt [Kvaliteedijuhtimine laoprotsesside jaoks](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="3340b-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="3340b-218">Järgmises tabelis on veel teavet kvaliteettellimuste loomise kohta konkreetset tüüpi protsessidele.</span><span class="sxs-lookup"><span data-stu-id="3340b-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="3340b-219">Protsessi tüüp</span><span class="sxs-lookup"><span data-stu-id="3340b-219">Type of process</span></span></th>
<th><span data-ttu-id="3340b-220">Millal saab kvaliteettellimusi automaatselt luua</span><span class="sxs-lookup"><span data-stu-id="3340b-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="3340b-221">Millal saab kvaliteettellimusi luua, kui on vajalik purustav katsetamine</span><span class="sxs-lookup"><span data-stu-id="3340b-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="3340b-222">Tingimuse teave</span><span class="sxs-lookup"><span data-stu-id="3340b-222">Condition information</span></span></th>
<th><span data-ttu-id="3340b-223">Käsitsi loomise teave</span><span class="sxs-lookup"><span data-stu-id="3340b-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3340b-224">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="3340b-224">Purchase order</span></span></td>
<td><span data-ttu-id="3340b-225">Enne või pärast sissetulekute loendi või vastuvõetava materjali toote sissetuleku sisestamist</span><span class="sxs-lookup"><span data-stu-id="3340b-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="3340b-226">Pärast vastuvõetava materjali toote sissetuleku sisestamist, kuna materjal peab olema kättesaadav purustavaks katsetamiseks</span><span class="sxs-lookup"><span data-stu-id="3340b-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="3340b-227">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="3340b-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3340b-228">Käsitsi loodud ostutellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="3340b-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-229">Vahelao order</span><span class="sxs-lookup"><span data-stu-id="3340b-229">Quarantine order</span></span></td>
<td><span data-ttu-id="3340b-230">Enne või pärast vahelao tellimuse lõpetatuna kinnitamist või lõpetamist</span><span class="sxs-lookup"><span data-stu-id="3340b-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="3340b-231">Destruktiivseid katseid nõudvaid kvaliteettellimusi ei saa luua.</span><span class="sxs-lookup"><span data-stu-id="3340b-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="3340b-232">Eeldatakse, et garantiitellimuse funktsionaalsus käsitleb hävinenud materjali käsitlemist.</span><span class="sxs-lookup"><span data-stu-id="3340b-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="3340b-233">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="3340b-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3340b-234">Käsitsi loodud vahelaoorderile viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="3340b-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-235">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="3340b-235">Sales order</span></span></td>
<td><span data-ttu-id="3340b-236">Enne plaanitud komplekteerimisprotsessi või saatelehe uuendamist lähetatavate kaupade puhul</span><span class="sxs-lookup"><span data-stu-id="3340b-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="3340b-237">Igas etapis</span><span class="sxs-lookup"><span data-stu-id="3340b-237">At any step</span></span></td>
<td><span data-ttu-id="3340b-238">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või klienti või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="3340b-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3340b-239">Käsitsi loodud müügitellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="3340b-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-240">Tootmistellimus</span><span class="sxs-lookup"><span data-stu-id="3340b-240">Production order</span></span></td>
<td><span data-ttu-id="3340b-241">Enne või pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="3340b-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="3340b-242">Pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="3340b-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="3340b-243">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="3340b-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3340b-244">Käsitsi loodud tootmistellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="3340b-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-245">Tootmistellimus, millel on protsessitoiming</span><span class="sxs-lookup"><span data-stu-id="3340b-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="3340b-246">Enne või pärast toimingu aruande lõpetamist</span><span class="sxs-lookup"><span data-stu-id="3340b-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="3340b-247">Pärast viimase toimingu tootmise lõpetamisest teatamist</span><span class="sxs-lookup"><span data-stu-id="3340b-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="3340b-248">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või toimingute ressurssi või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="3340b-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="3340b-249">Käsitsi loodud protsessitoimingule viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="3340b-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3340b-250">Varud</span><span class="sxs-lookup"><span data-stu-id="3340b-250">Inventory</span></span></td>
<td><span data-ttu-id="3340b-251">Kvaliteettellimust ei saa automaatselt koostada varude töölehe kandele või ülekandetellimuse tehingutele.</span><span class="sxs-lookup"><span data-stu-id="3340b-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="3340b-252">Kvaliteettellimus tuleb kauba laokogusele käsitsi koostada.</span><span class="sxs-lookup"><span data-stu-id="3340b-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="3340b-253">Nõutav on füüsiline vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="3340b-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="3340b-254">Kvaliteettellimuste automaatse genereerimise näited</span><span class="sxs-lookup"><span data-stu-id="3340b-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="3340b-255">Ostmine</span><span class="sxs-lookup"><span data-stu-id="3340b-255">Purchasing</span></span>

<span data-ttu-id="3340b-256">Kui määrate ostmisel välja **Sündmuse tüüp** väärtuseks *Toote sissetulek* ja välja **Käivitamine** väärtuseks *Pärast* lehel **Kvaliteediseosed**, saate järgmised tulemused:</span><span class="sxs-lookup"><span data-stu-id="3340b-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="3340b-257">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud *Jah*, luuakse iga sissetuleku kohta kvaliteettellimus ostutellimuse suhtes, võttes aluseks sissetulnud koguse ja kauba valimi sätted.</span><span class="sxs-lookup"><span data-stu-id="3340b-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="3340b-258">Iga kord, kui ostutellimuse vastu on saadud kogus, luuakse äsja vastuvõetud koguse põhjal uued kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="3340b-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="3340b-259">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud *Ei*, luuakse sissetulnud koguse põhjal esimese sissetuleku kohta kvaliteettellimus ostutellimuse suhtes.</span><span class="sxs-lookup"><span data-stu-id="3340b-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="3340b-260">Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt jälgimisdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="3340b-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="3340b-261">Kvaliteettellimusi ei looda järgnevate sissetulekute kohta ostutellimuse suhtes.</span><span class="sxs-lookup"><span data-stu-id="3340b-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="3340b-262">Tootmine</span><span class="sxs-lookup"><span data-stu-id="3340b-262">Production</span></span>

<span data-ttu-id="3340b-263">Kui määrate tootmisel välja **Sündmuse tüüp** väärtuseks *Lõpetamise kinnitamine* ja välja **Käivitamine** väärtuseks *Pärast* lehel **Kvaliteediseosed**, saate järgmised tulemused:</span><span class="sxs-lookup"><span data-stu-id="3340b-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="3340b-264">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud *Jah*, luuakse kvaliteettellimus iga lõpetatud koguse ja kauba valimi sätete alusel.</span><span class="sxs-lookup"><span data-stu-id="3340b-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="3340b-265">Iga kord, kui kogus märgitakse tootmistellimuse suhtes lõpetatuks, luuakse äsja lõpetatud koguse põhjal uued kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="3340b-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="3340b-266">See loomisloogika on kooskõlas ostuga.</span><span class="sxs-lookup"><span data-stu-id="3340b-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="3340b-267">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud *Ei*, luuakse lõpetatud koguse põhjal kvaliteettellimus esimesel korral, kui kogus kinnitatakse lõpetatuks.</span><span class="sxs-lookup"><span data-stu-id="3340b-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="3340b-268">Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt kauba valimi jälgimisdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="3340b-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="3340b-269">Hilisemate lõpetatud koguste kohta ei looda kvaliteettellimusi.</span><span class="sxs-lookup"><span data-stu-id="3340b-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="3340b-270">Kvaliteedi spetsifikatsioon</span><span class="sxs-lookup"><span data-stu-id="3340b-270">Quality specification</span></span></th>
<th><span data-ttu-id="3340b-271">Värskendatud koguse kohta</span><span class="sxs-lookup"><span data-stu-id="3340b-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="3340b-272">Jälgimisdimensiooni kohta</span><span class="sxs-lookup"><span data-stu-id="3340b-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="3340b-273">Tulemus</span><span class="sxs-lookup"><span data-stu-id="3340b-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3340b-274">Protsent: 10%</span><span class="sxs-lookup"><span data-stu-id="3340b-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="3340b-275">Jah</span><span class="sxs-lookup"><span data-stu-id="3340b-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="3340b-276">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="3340b-276">Batch number: No</span></span></p>
<p><span data-ttu-id="3340b-277">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="3340b-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="3340b-278">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="3340b-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="3340b-279">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="3340b-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3340b-280">Kvaliteettellimus 1 3 kohta (10% 30-st)</span><span class="sxs-lookup"><span data-stu-id="3340b-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3340b-281">Teata 70 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="3340b-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="3340b-282">Kvaliteettellimus 2 7 kohta (10% järelejäänud tellimuse kogusest, mis võrdub sel juhul 70-ga)</span><span class="sxs-lookup"><span data-stu-id="3340b-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3340b-283">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="3340b-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3340b-284">Ei</span><span class="sxs-lookup"><span data-stu-id="3340b-284">No</span></span></td>
<td>
<p><span data-ttu-id="3340b-285">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="3340b-285">Batch number: No</span></span></p>
<p><span data-ttu-id="3340b-286">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="3340b-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="3340b-287">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="3340b-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="3340b-288">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="3340b-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="3340b-289">Kvaliteettellimus 1 1 kohta (esimese lõpetatuna kinnitatud koguse jaoks, millel on fikseeritud väärtus 1)</span><span class="sxs-lookup"><span data-stu-id="3340b-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="3340b-290">Kvaliteettellimus 2 1 kohta (järelejäänud koguse jaoks, millel on ikka fikseeritud väärtus 1)</span><span class="sxs-lookup"><span data-stu-id="3340b-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3340b-291">Teata 10 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="3340b-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="3340b-292">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="3340b-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3340b-293">Teata 60 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="3340b-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="3340b-294">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="3340b-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="3340b-295">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="3340b-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="3340b-296">Jah</span><span class="sxs-lookup"><span data-stu-id="3340b-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="3340b-297">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="3340b-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3340b-298">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="3340b-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3340b-299">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="3340b-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3340b-300">Lõpetatuna kinnitamine 3: 1 partiinumbri b1 puhul, seerianumber s1; 1 partiinumbri b2 puhul, seerianumber s2; ja 1 partiinumbri b3 puhul, seerianumber s3</span><span class="sxs-lookup"><span data-stu-id="3340b-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="3340b-301">Kvaliteettellimus 1 1 kohta partiist b1, seerianumber s1</span><span class="sxs-lookup"><span data-stu-id="3340b-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="3340b-302">Kvaliteettellimus 2 1 kohta partiist b2, seerianumber s2</span><span class="sxs-lookup"><span data-stu-id="3340b-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="3340b-303">Kvaliteettellimus 3 1 kohta partiist b3, seerianumber s3</span><span class="sxs-lookup"><span data-stu-id="3340b-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3340b-304">Teata lõpetatuna: 2: 1 partiinumbri b4 puhul, seerianumber s4; ja 1 partiinumbri b5 puhul, seerianumber s5</span><span class="sxs-lookup"><span data-stu-id="3340b-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="3340b-305">Kvaliteettellimus 4 1 kohta partiist b4, seerianumber s4</span><span class="sxs-lookup"><span data-stu-id="3340b-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="3340b-306">Kvaliteettellimus 5 1 kohta partiist b5, seerianumber s5</span><span class="sxs-lookup"><span data-stu-id="3340b-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="3340b-307"><strong>Märkus.</strong> Partiid saab uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="3340b-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="3340b-308">Fikseeritud kogus: 2</span><span class="sxs-lookup"><span data-stu-id="3340b-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="3340b-309">Ei</span><span class="sxs-lookup"><span data-stu-id="3340b-309">No</span></span></td>
<td>
<p><span data-ttu-id="3340b-310">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="3340b-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="3340b-311">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="3340b-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="3340b-312">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="3340b-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="3340b-313">Lõpetatuna kinnitamine 3: 1 partiinumbri b1 puhul, seerianumber s1; 1 partiinumbri b2 puhul, seerianumber s2; 1 partiinumbri b3 puhul, seerianumber s3 ja 1 partiinumbri b4 puhul, seerianumber s4</span><span class="sxs-lookup"><span data-stu-id="3340b-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="3340b-314">Kvaliteettellimus 1 1 kohta partiist b1, seerianumber s1</span><span class="sxs-lookup"><span data-stu-id="3340b-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="3340b-315">Kvaliteettellimus 2 1 kohta partiist b2, seerianumber s2</span><span class="sxs-lookup"><span data-stu-id="3340b-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="3340b-316">Kvaliteettellimus 3 1 kohta partiist b3, seerianumber s3</span><span class="sxs-lookup"><span data-stu-id="3340b-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="3340b-317">Kvaliteettellimus 4 1 kohta partiist b4, seerianumber s4</span><span class="sxs-lookup"><span data-stu-id="3340b-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="3340b-318">Kvaliteettellimus 5 2 kohta,ilma viiteta partiile ja seerianumbrile</span><span class="sxs-lookup"><span data-stu-id="3340b-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="3340b-319">Teata lõpetatuna 6: 1 partiinumbri b5 puhul, seerianumber s5; 1 partiinumbri b6 puhul, seerianumber s6; 1 partiinumbri b7 puhul, seerianumber s7; 1 partiinumbri b8 puhul, seerianumber s8; 1 partiinumbri b9 puhul, seerianumber s9; ja 1 partiinumbri b10 puhul, seerianumber s10</span><span class="sxs-lookup"><span data-stu-id="3340b-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="3340b-320">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="3340b-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="3340b-321">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3340b-321">Additional resources</span></span>

- [<span data-ttu-id="3340b-322">Kvaliteedijuhtimise protsessid</span><span class="sxs-lookup"><span data-stu-id="3340b-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="3340b-323">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="3340b-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="3340b-324">Laoprotsesside kvaliteedijuhtimine</span><span class="sxs-lookup"><span data-stu-id="3340b-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
