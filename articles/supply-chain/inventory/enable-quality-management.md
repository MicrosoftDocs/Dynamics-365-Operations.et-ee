---
title: Kvaliteedijuhtimise ülevaade
description: Selles teemas kirjeldatakse, kuidas kasutada rakenduses Dynamics 365 Supply Chain Management kvaliteedijuhtimist, et täiustada tarneahela toote kvaliteeti.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b090450c6b39607f9661667f8063998bbe5ff52
ms.sourcegitcommit: c79062ba89498aa3fe3d86e478d9f32484f5f6dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/03/2020
ms.locfileid: "3224905"
---
# <a name="quality-management-overview"></a><span data-ttu-id="b1075-103">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="b1075-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1075-104">Selles teemas kirjeldatakse, kuidas kasutada rakenduses Dynamics 365 Supply Chain Management kvaliteedijuhtimist, et täiustada tarneahela toote kvaliteeti.</span><span class="sxs-lookup"><span data-stu-id="b1075-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="b1075-105">Kvaliteedijuhtimise abil saate hallata ümberpööramise aegu, kui käsitsete mittevastavaid tooteid, olenemata nende päritolukohast.</span><span class="sxs-lookup"><span data-stu-id="b1075-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="b1075-106">Kuna diagnostikatüübid on seotud parandustest teatamisega, saab Supply Chain Management plaanida ülesandeid probleemide kõrvaldamiseks ja nende kordumise vältimiseks.</span><span class="sxs-lookup"><span data-stu-id="b1075-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="b1075-107">Lisaks mittevastavuste haldamiseks mõeldud funktsioonidele hõlmab kvaliteedijuhtimine funktsioone probleemide jälgimiseks probleemi tüübi alusel (isegi sisemiste probleemide puhul) ja lühiajaliste või pikaajaliste lahenduste tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="b1075-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="b1075-108">Tulemuslikkuse võtmenäitajate (KPI) statistika annab ülevaate varasematest mittevastavuse probleemidest ja nende kõrvaldamiseks kasutatud lahendustest.</span><span class="sxs-lookup"><span data-stu-id="b1075-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="b1075-109">Saate kasutada varasemaid andmeid eelmiste kvaliteedimeetmete tulemuslikkuse ülevaatamiseks ja sobivate tulevikus kasutatavate meetmete määramiseks.</span><span class="sxs-lookup"><span data-stu-id="b1075-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="b1075-110">Kvaliteediseose seadistamisel saab Supply Chain Management koostada kvaliteettellimusi mitmesugustele äriprotsessidele, sündmustele ja tingimustele.</span><span class="sxs-lookup"><span data-stu-id="b1075-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="b1075-111">Kvaliteediseos võib hõlmata konkreetset kaupa, konkreetset kaubagruppi või kõiki kaupu.</span><span class="sxs-lookup"><span data-stu-id="b1075-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="b1075-112">Kvaliteedijuhtimise kasutamise näited</span><span class="sxs-lookup"><span data-stu-id="b1075-112">Examples of the use of quality management</span></span>
<span data-ttu-id="b1075-113">Kvaliteedijuhtimine on paindlik ja seda saab rakendada mitmesugusel moel, et järgida konkreetsete tarneahela toimingute tasemete nõudeid.</span><span class="sxs-lookup"><span data-stu-id="b1075-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="b1075-114">Järgmised näited illustreerivad nende funktsioonide võimalikke kasutusviise.</span><span class="sxs-lookup"><span data-stu-id="b1075-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="b1075-115">Saate kvaliteedikontrolli protsessi automaatselt käivitada, tuginedes eelnevalt määratletud kriteeriumidele (konkreetse hankija ostutellimuse registreerimisel laos).</span><span class="sxs-lookup"><span data-stu-id="b1075-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="b1075-116">Kontrollimise ajal varude blokeerimine, et vältida heakskiitmata varude kasutamist (ostutellimuse koguste täielik blokeerimine).</span><span class="sxs-lookup"><span data-stu-id="b1075-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="b1075-117">Saate kasutada kauba valimit kvaliteediseose osana jooksvate füüsiliste varude hulga määratlemiseks, mida kontrollida tuleb.</span><span class="sxs-lookup"><span data-stu-id="b1075-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="b1075-118">Valimi aluseks võib olla fikseeritud kogus või protsent.</span><span class="sxs-lookup"><span data-stu-id="b1075-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="b1075-119">Looge kvaliteettellimused osaliste tarnete jaoks.</span><span class="sxs-lookup"><span data-stu-id="b1075-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="b1075-120">Kvaliteettellimuse loomiseks, mis põhineb tellimusega füüsiliselt saadud kogusel, peate märkima ruudu **Värskendatud koguse kohta** vormil **Kauba valim**.</span><span class="sxs-lookup"><span data-stu-id="b1075-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="b1075-121">Saate luua katsetüüpe, mis sisaldavad katse minimaalset, maksimaalset ja sihtväärtust ning teha kvalitatiivset vs kvantitatiivset kontrolli, millel on eelnevalt määratud valideerimistulemused.</span><span class="sxs-lookup"><span data-stu-id="b1075-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="b1075-122">Määrake sobiv kvaliteeditase (AQL) kvaliteedimeetme hälvete kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="b1075-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="b1075-123">Saate määrata ressursid, mida kontrollimistoiming nõuab, nt katsepiirkond ja katseinstrumendid.</span><span class="sxs-lookup"><span data-stu-id="b1075-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="b1075-124">Kvaliteediseostega töötamine</span><span class="sxs-lookup"><span data-stu-id="b1075-124">Working with quality associations</span></span>
<span data-ttu-id="b1075-125">Kvaliteediseost kasutav äriprotsess võib olla seotud mitmesuguste lähtedokumentidega, nt ostutellimuste, müügitellimuste või tootmistellimustega.</span><span class="sxs-lookup"><span data-stu-id="b1075-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="b1075-126">Iga kvaliteediseose kirje määrab ka katsete kogumi, AQL-i ning valikukava, mida rakendatakse loodud kvaliteettellimustele.</span><span class="sxs-lookup"><span data-stu-id="b1075-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="b1075-127">Peate iga äriprotsessi variatsiooni jaoks määratlema kvaliteediseose kirje.</span><span class="sxs-lookup"><span data-stu-id="b1075-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="b1075-128">Näiteks saate seadistada kvaliteediseose, mis koostab kvaliteettellimuse, kui ostutellimuse toote sissetulekut värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="b1075-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="b1075-129">Olenevalt käivitamisplaani seadistusest saab käivitusprotsessi enese blokeerida, kui on olemas avatud kvaliteettellimus, või saab blokeerida järgmised protsessid, nt ostutellimuse eest arve esitamise.</span><span class="sxs-lookup"><span data-stu-id="b1075-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="b1075-130">**Märkus.** avatud kvaliteettellimuste olemasolu korral blokeeritakse automaatselt varude koguste väljastamine.</span><span class="sxs-lookup"><span data-stu-id="b1075-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="b1075-131">Olenevalt valiku **Täielik blokeerimine** seadistusest lehel **Kaubaproovid** on kogus kas kvaliteettellimusel olev kogus või lähtedokumendi real olev kogus.</span><span class="sxs-lookup"><span data-stu-id="b1075-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="b1075-132">Nimetatud äriprotsessi puhul määratleb kvaliteediseose kirje sündmuse ja tingimused, mille jaoks kvaliteettellimus on loodud.</span><span class="sxs-lookup"><span data-stu-id="b1075-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="b1075-133">Tingimused võivad olla asukoha või juriidilise isiku põhised.</span><span class="sxs-lookup"><span data-stu-id="b1075-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="b1075-134">Purustavaid katseid hõlmavat kvaliteettellimust saab luua ainult siis, kui sündmusel on olemas vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="b1075-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="b1075-135">Järgmistes näidetes on näha, kuidas kvaliteediseose kirjet määratakse iga äriprotsessi variatsioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="b1075-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="b1075-136">Iga näite puhul võetakse järgmises tabelis kokku sündmused ja tingimused, mis on kvaliteediseose kirjega määratletud.</span><span class="sxs-lookup"><span data-stu-id="b1075-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="b1075-137">Viite tüüp</span><span class="sxs-lookup"><span data-stu-id="b1075-137">Reference type</span></span></th>
<th><span data-ttu-id="b1075-138">Sündmuse tüüp</span><span class="sxs-lookup"><span data-stu-id="b1075-138">Event type</span></span></th>
<th><span data-ttu-id="b1075-139">Käivitamine</span><span class="sxs-lookup"><span data-stu-id="b1075-139">Execution</span></span></th>
<th><span data-ttu-id="b1075-140">Sündmuse blokeerimine</span><span class="sxs-lookup"><span data-stu-id="b1075-140">Event blocking</span></span></th>
<th><span data-ttu-id="b1075-141">Dokumendi viide</span><span class="sxs-lookup"><span data-stu-id="b1075-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b1075-142">Varud</span><span class="sxs-lookup"><span data-stu-id="b1075-142">Inventory</span></span></td>
<td><span data-ttu-id="b1075-143">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="b1075-143">Not applicable</span></span></td>
<td><span data-ttu-id="b1075-144">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="b1075-144">Not applicable</span></span></td>
<td><span data-ttu-id="b1075-145">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-145">None</span></span></td>
<td><span data-ttu-id="b1075-146">Kõik</span><span class="sxs-lookup"><span data-stu-id="b1075-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="b1075-147">Müük</span><span class="sxs-lookup"><span data-stu-id="b1075-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="b1075-148">Komplekteerimise protsess on plaanitud</span><span class="sxs-lookup"><span data-stu-id="b1075-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="b1075-149">Enne</span><span class="sxs-lookup"><span data-stu-id="b1075-149">Before</span></span></td>
<td><span data-ttu-id="b1075-150">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="b1075-151">Ainult Konkreetne ID, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="b1075-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-152">Komplekteerimise protsess</span><span class="sxs-lookup"><span data-stu-id="b1075-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-153">Saateleht</span><span class="sxs-lookup"><span data-stu-id="b1075-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-154">Arve</span><span class="sxs-lookup"><span data-stu-id="b1075-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1075-155">Saateleht</span><span class="sxs-lookup"><span data-stu-id="b1075-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-156">Enne</span><span class="sxs-lookup"><span data-stu-id="b1075-156">Before</span></span></td>
<td><span data-ttu-id="b1075-157">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-158">Saateleht</span><span class="sxs-lookup"><span data-stu-id="b1075-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-159">Arve</span><span class="sxs-lookup"><span data-stu-id="b1075-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="b1075-160">Ost</span><span class="sxs-lookup"><span data-stu-id="b1075-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="b1075-161">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="b1075-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="b1075-162">Enne</span><span class="sxs-lookup"><span data-stu-id="b1075-162">Before</span></span></td>
<td><span data-ttu-id="b1075-163">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-164">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="b1075-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-165">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="b1075-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-166">Arve</span><span class="sxs-lookup"><span data-stu-id="b1075-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1075-167">Pärast</span><span class="sxs-lookup"><span data-stu-id="b1075-167">After</span></span></td>
<td><span data-ttu-id="b1075-168">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-169">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="b1075-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-170">Arve</span><span class="sxs-lookup"><span data-stu-id="b1075-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1075-171">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="b1075-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-172">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="b1075-172">Not applicable</span></span></td>
<td><span data-ttu-id="b1075-173">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-174">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="b1075-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-175">Arve</span><span class="sxs-lookup"><span data-stu-id="b1075-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b1075-176">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="b1075-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-177">Enne</span><span class="sxs-lookup"><span data-stu-id="b1075-177">Before</span></span></td>
<td><span data-ttu-id="b1075-178">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-179">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="b1075-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-180">Arve</span><span class="sxs-lookup"><span data-stu-id="b1075-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b1075-181">Pärast</span><span class="sxs-lookup"><span data-stu-id="b1075-181">After</span></span></td>
<td><span data-ttu-id="b1075-182">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-183">Arve</span><span class="sxs-lookup"><span data-stu-id="b1075-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="b1075-184">Tootmine</span><span class="sxs-lookup"><span data-stu-id="b1075-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-185">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="b1075-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-186">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="b1075-186">Not applicable</span></span></td>
<td><span data-ttu-id="b1075-187">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="b1075-188">Kõik</span><span class="sxs-lookup"><span data-stu-id="b1075-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-189">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="b1075-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-190">Lõpp</span><span class="sxs-lookup"><span data-stu-id="b1075-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b1075-191">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="b1075-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-192">Enne</span><span class="sxs-lookup"><span data-stu-id="b1075-192">Before</span></span></td>
<td><span data-ttu-id="b1075-193">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-194">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="b1075-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-195">Lõpp</span><span class="sxs-lookup"><span data-stu-id="b1075-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b1075-196">Pärast</span><span class="sxs-lookup"><span data-stu-id="b1075-196">After</span></span></td>
<td><span data-ttu-id="b1075-197">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-198">Lõpp</span><span class="sxs-lookup"><span data-stu-id="b1075-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="b1075-199">Vaheladu</span><span class="sxs-lookup"><span data-stu-id="b1075-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-200">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="b1075-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="b1075-201">Enne</span><span class="sxs-lookup"><span data-stu-id="b1075-201">Before</span></span></td>
<td><span data-ttu-id="b1075-202">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="b1075-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-203">Lõpp</span><span class="sxs-lookup"><span data-stu-id="b1075-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-204">Pärast</span><span class="sxs-lookup"><span data-stu-id="b1075-204">After</span></span></td>
<td><span data-ttu-id="b1075-205">Lõpp</span><span class="sxs-lookup"><span data-stu-id="b1075-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-206">Lõpp</span><span class="sxs-lookup"><span data-stu-id="b1075-206">End</span></span></td>
<td><span data-ttu-id="b1075-207">Enne</span><span class="sxs-lookup"><span data-stu-id="b1075-207">Before</span></span></td>
<td><span data-ttu-id="b1075-208">Lõpp</span><span class="sxs-lookup"><span data-stu-id="b1075-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1075-209">Protsessi operatsioon</span><span class="sxs-lookup"><span data-stu-id="b1075-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-210">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="b1075-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="b1075-211">Enne</span><span class="sxs-lookup"><span data-stu-id="b1075-211">Before</span></span></td>
<td><span data-ttu-id="b1075-212">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-213">Konkreetne ID, Grupp või Kõik ja Ressursipõhine, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="b1075-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-214">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="b1075-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-215">Pärast</span><span class="sxs-lookup"><span data-stu-id="b1075-215">After</span></span></td>
<td><span data-ttu-id="b1075-216">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1075-217">Kaastoote tootmine</span><span class="sxs-lookup"><span data-stu-id="b1075-217">Co-product production</span></span></td>
<td><span data-ttu-id="b1075-218">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="b1075-218">Registration</span></span></td>
<td><span data-ttu-id="b1075-219">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="b1075-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-220">Puudub</span><span class="sxs-lookup"><span data-stu-id="b1075-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="b1075-221">Kõik</span><span class="sxs-lookup"><span data-stu-id="b1075-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b1075-222">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="b1075-222">Report as finished</span></span></td>
<td><span data-ttu-id="b1075-223">Enne</span><span class="sxs-lookup"><span data-stu-id="b1075-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-224">Pärast</span><span class="sxs-lookup"><span data-stu-id="b1075-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b1075-225">Järgmises tabelis on veel teavet kvaliteettellimuste loomise kohta konkreetset tüüpi protsessidele.</span><span class="sxs-lookup"><span data-stu-id="b1075-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="b1075-226">Protsessi tüüp</span><span class="sxs-lookup"><span data-stu-id="b1075-226">Type of process</span></span></th>
<th><span data-ttu-id="b1075-227">Millal saab kvaliteettellimusi automaatselt luua</span><span class="sxs-lookup"><span data-stu-id="b1075-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="b1075-228">Millal saab kvaliteettellimusi luua, kui on vajalik purustav katsetamine</span><span class="sxs-lookup"><span data-stu-id="b1075-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="b1075-229">Tingimuse teave</span><span class="sxs-lookup"><span data-stu-id="b1075-229">Condition information</span></span></th>
<th><span data-ttu-id="b1075-230">Käsitsi loomise teave</span><span class="sxs-lookup"><span data-stu-id="b1075-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b1075-231">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="b1075-231">Purchase order</span></span></td>
<td><span data-ttu-id="b1075-232">Enne või pärast sissetulekute loendi või vastuvõetava materjali toote sissetuleku sisestamist</span><span class="sxs-lookup"><span data-stu-id="b1075-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="b1075-233">Pärast vastuvõetava materjali toote sissetuleku sisestamist, kuna materjal peab olema kättesaadav purustavaks katsetamiseks</span><span class="sxs-lookup"><span data-stu-id="b1075-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="b1075-234">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="b1075-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b1075-235">Käsitsi loodud ostutellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="b1075-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-236">Vahelao order</span><span class="sxs-lookup"><span data-stu-id="b1075-236">Quarantine order</span></span></td>
<td><span data-ttu-id="b1075-237">Enne või pärast vahelao tellimuse lõpetatuna kinnitamist või lõpetamist</span><span class="sxs-lookup"><span data-stu-id="b1075-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="b1075-238">Purustavaid katseid nõudvaid kvaliteettellimusi ei saa koostada.</span><span class="sxs-lookup"><span data-stu-id="b1075-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="b1075-239">Eeldatakse, et vahelao tellimuse funktsioon tegeleb rikutud materjali likvideerimisega.</span><span class="sxs-lookup"><span data-stu-id="b1075-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="b1075-240">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="b1075-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b1075-241">Käsitsi loodud vahelaoorderile viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="b1075-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-242">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="b1075-242">Sales order</span></span></td>
<td><span data-ttu-id="b1075-243">Enne plaanitud komplekteerimisprotsessi või saatelehe uuendamist lähetatavate kaupade puhul</span><span class="sxs-lookup"><span data-stu-id="b1075-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="b1075-244">Igas etapis</span><span class="sxs-lookup"><span data-stu-id="b1075-244">At any step</span></span></td>
<td><span data-ttu-id="b1075-245">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või klienti või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="b1075-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b1075-246">Käsitsi loodud müügitellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="b1075-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-247">Tootmistellimus</span><span class="sxs-lookup"><span data-stu-id="b1075-247">Production order</span></span></td>
<td><span data-ttu-id="b1075-248">Enne või pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="b1075-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="b1075-249">Pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="b1075-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="b1075-250">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala või kaupa või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="b1075-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b1075-251">Käsitsi loodud tootmistellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="b1075-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-252">Tootmistellimus, millel on protsessitoiming</span><span class="sxs-lookup"><span data-stu-id="b1075-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="b1075-253">Enne või pärast toimingu aruande lõpetamist</span><span class="sxs-lookup"><span data-stu-id="b1075-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="b1075-254">Pärast viimase toimingu tootmise lõpetamisest teatamist</span><span class="sxs-lookup"><span data-stu-id="b1075-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="b1075-255">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või operatsiooniressurssi või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="b1075-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="b1075-256">Käsitsi loodud protsessitoimingule viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="b1075-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1075-257">Varud</span><span class="sxs-lookup"><span data-stu-id="b1075-257">Inventory</span></span></td>
<td><span data-ttu-id="b1075-258">Kvaliteettellimust ei saa automaatselt koostada varude töölehe kandele või üleviimistellimuse kandele.</span><span class="sxs-lookup"><span data-stu-id="b1075-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="b1075-259">Kvaliteettellimus tuleb kauba laokogusele käsitsi koostada.</span><span class="sxs-lookup"><span data-stu-id="b1075-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="b1075-260">Nõutav on füüsiline vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="b1075-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="b1075-261">Kvaliteettellimuse automaatse loomise näited</span><span class="sxs-lookup"><span data-stu-id="b1075-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="b1075-262">Ostmine</span><span class="sxs-lookup"><span data-stu-id="b1075-262">Purchasing</span></span>

<span data-ttu-id="b1075-263">Kui määrate ostmisel välja **Sündmuse tüüp** väärtuseks **Toote sissetulek** ja välja **Käivitamine** väärtuseks **Pärast** lehel **Kvaliteediseosed**, saate järgmised tulemused:</span><span class="sxs-lookup"><span data-stu-id="b1075-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="b1075-264">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Jah**, luuakse iga sissetuleku kohta kvaliteettellimus ostutellimuse suhtes, võttes aluseks sissetulnud koguse ja kauba valimi sätted.</span><span class="sxs-lookup"><span data-stu-id="b1075-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="b1075-265">Iga kord, kui ostutellimuse vastu on saadud kogus, luuakse äsja vastuvõetud koguse põhjal uued kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="b1075-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="b1075-266">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Ei**, luuakse sissetulnud koguse põhjal esimese sissetuleku kohta kvaliteettellimus ostutellimuse suhtes.</span><span class="sxs-lookup"><span data-stu-id="b1075-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="b1075-267">Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt jälgimisdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="b1075-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="b1075-268">Kvaliteettellimusi ei looda järgnevate sissetulekute kohta ostutellimuse suhtes.</span><span class="sxs-lookup"><span data-stu-id="b1075-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="b1075-269">Tootmine</span><span class="sxs-lookup"><span data-stu-id="b1075-269">Production</span></span>

<span data-ttu-id="b1075-270">Kui määrate tootmisel välja **Sündmuse tüüp** väärtuseks **Lõpetamise kinnitamine** ja välja **Käivitamine** väärtuseks **Pärast** lehel **Kvaliteediseosed**, saate järgmised tulemused:</span><span class="sxs-lookup"><span data-stu-id="b1075-270">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="b1075-271">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Jah**, luuakse kvaliteettellimus iga lõpetatud koguse ja kauba valimi sätete alusel.</span><span class="sxs-lookup"><span data-stu-id="b1075-271">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="b1075-272">Iga kord, kui kogus märgitakse tootmistellimuse suhtes lõpetatuks, luuakse äsja lõpetatud koguse põhjal uued kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="b1075-272">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="b1075-273">See loomisloogika on kooskõlas ostuga.</span><span class="sxs-lookup"><span data-stu-id="b1075-273">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="b1075-274">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Ei**, luuakse lõpetatud koguse põhjal kvaliteettellimus esimesel korral, kui kogus kinnitatakse lõpetatuks.</span><span class="sxs-lookup"><span data-stu-id="b1075-274">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="b1075-275">Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt kauba valimi jälgimisdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="b1075-275">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="b1075-276">Hilisemate lõpetatud koguste kohta ei looda kvaliteettellimusi.</span><span class="sxs-lookup"><span data-stu-id="b1075-276">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="b1075-277">Kvaliteedi spetsifikatsioon</span><span class="sxs-lookup"><span data-stu-id="b1075-277">Quality specification</span></span></th>
<th><span data-ttu-id="b1075-278">Värskendatud koguse kohta</span><span class="sxs-lookup"><span data-stu-id="b1075-278">Per updated quantity</span></span></th>
<th><span data-ttu-id="b1075-279">Jälgimisdimensiooni kohta</span><span class="sxs-lookup"><span data-stu-id="b1075-279">Per tracking dimension</span></span></th>
<th><span data-ttu-id="b1075-280">Tulemus</span><span class="sxs-lookup"><span data-stu-id="b1075-280">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="b1075-281">Protsent: 10%</span><span class="sxs-lookup"><span data-stu-id="b1075-281">Percentage: 10%</span></span></td>
<td><span data-ttu-id="b1075-282">Jah</span><span class="sxs-lookup"><span data-stu-id="b1075-282">Yes</span></span></td>
<td>
<p><span data-ttu-id="b1075-283">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="b1075-283">Batch number: No</span></span></p>
<p><span data-ttu-id="b1075-284">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="b1075-284">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="b1075-285">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="b1075-285">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="b1075-286">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="b1075-286">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="b1075-287">Kvaliteettellimus #1 3 kohta (10% 30-st)</span><span class="sxs-lookup"><span data-stu-id="b1075-287">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b1075-288">Teata 70 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="b1075-288">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="b1075-289">Kvaliteettellimus #2 7 kohta (10% järelejäänud tellimuse kogusest, mis võrdub sel juhul 70-ga)</span><span class="sxs-lookup"><span data-stu-id="b1075-289">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b1075-290">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="b1075-290">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="b1075-291">Ei</span><span class="sxs-lookup"><span data-stu-id="b1075-291">No</span></span></td>
<td>
<p><span data-ttu-id="b1075-292">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="b1075-292">Batch number: No</span></span></p>
<p><span data-ttu-id="b1075-293">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="b1075-293">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="b1075-294">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="b1075-294">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="b1075-295">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="b1075-295">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="b1075-296">Kavaliteettellimus #1 luuakse 1 kohta (esimese lõpetatuna kinnitatud koguse jaoks, millel on fikseeritud väärtus 1)</span><span class="sxs-lookup"><span data-stu-id="b1075-296">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="b1075-297">Kavaliteettellimus #2 luuakse 1 kohta (järelejäänud koguse jaoks, millel on ikka fikseeritud väärtus 1)</span><span class="sxs-lookup"><span data-stu-id="b1075-297">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b1075-298">Teata 10 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="b1075-298">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="b1075-299">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="b1075-299">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b1075-300">Teata 60 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="b1075-300">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="b1075-301">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="b1075-301">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b1075-302">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="b1075-302">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="b1075-303">Jah</span><span class="sxs-lookup"><span data-stu-id="b1075-303">Yes</span></span></td>
<td>
<p><span data-ttu-id="b1075-304">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="b1075-304">Batch number: Yes</span></span></p>
<p><span data-ttu-id="b1075-305">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="b1075-305">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="b1075-306">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="b1075-306">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="b1075-307">Kinnita lõpetatuks 3 kohta: 1 #b1, #s1 kohta; 1 #b2, #s2 kohta ja 1 #b3, #s3 kohta</span><span class="sxs-lookup"><span data-stu-id="b1075-307">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="b1075-308">Kvaliteettellimus #1 1 kohta partiist #b1, seerianumber #s1</span><span class="sxs-lookup"><span data-stu-id="b1075-308">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="b1075-309">Kvaliteettellimus #2 1 kohta partiist #b2, seerianumber #s2</span><span class="sxs-lookup"><span data-stu-id="b1075-309">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="b1075-310">Kvaliteettellimus #3 1 kohta partiist #b3, seerianumber #s3</span><span class="sxs-lookup"><span data-stu-id="b1075-310">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b1075-311">Kinnita lõpetatuks 2 kohta: 1 #b4, #s4 kohta ja 1 #b5, #s5 kohta</span><span class="sxs-lookup"><span data-stu-id="b1075-311">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="b1075-312">Kvaliteettellimus #4 1 kohta partiist #b4, seerianumber #s4</span><span class="sxs-lookup"><span data-stu-id="b1075-312">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="b1075-313">Kvaliteettellimus #5 1 kohta partiist #b5, seerianumber #s5</span><span class="sxs-lookup"><span data-stu-id="b1075-313">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="b1075-314"><strong>Märkus.</strong> Partiid saab uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="b1075-314"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="b1075-315">Fikseeritud kogus: 2</span><span class="sxs-lookup"><span data-stu-id="b1075-315">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="b1075-316">Ei</span><span class="sxs-lookup"><span data-stu-id="b1075-316">No</span></span></td>
<td>
<p><span data-ttu-id="b1075-317">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="b1075-317">Batch number: Yes</span></span></p>
<p><span data-ttu-id="b1075-318">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="b1075-318">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="b1075-319">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="b1075-319">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="b1075-320">Kinnita lõpetatuks 4 kohta: 1 #b1, #s1 kohta; 1 #b2, #s2 kohta; 1 #b3, #s3 kohta ja 1 #b4, #s4 kohta</span><span class="sxs-lookup"><span data-stu-id="b1075-320">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="b1075-321">Kvaliteettellimus #1 1 kohta partiist #b1, seerianumber #s1</span><span class="sxs-lookup"><span data-stu-id="b1075-321">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="b1075-322">Kvaliteettellimus #2 1 kohta partiist #b2, seerianumber #s2</span><span class="sxs-lookup"><span data-stu-id="b1075-322">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="b1075-323">Kvaliteettellimus #3 1 kohta partiist #b3, seerianumber #s3</span><span class="sxs-lookup"><span data-stu-id="b1075-323">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="b1075-324">Kvaliteettellimus #4 1 kohta partiist #b4, seerianumber #s4</span><span class="sxs-lookup"><span data-stu-id="b1075-324">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="b1075-325">Kvaliteettellimus #5 2 kohta,ilma viiteta partiile ja seerianumbrile</span><span class="sxs-lookup"><span data-stu-id="b1075-325">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="b1075-326">Kinnita lõpetatuks 6 kohta: 1 #b5, #s5 kohta; 1 #b6, #s6 kohta; 1 #b7, #s7 kohta; 1 #b8, #s8 kohta; 1 #b9, #s9 kohta ja 1 #b10, #s10 kohta</span><span class="sxs-lookup"><span data-stu-id="b1075-326">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="b1075-327">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="b1075-327">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="b1075-328">Kvaliteedijuhtimise lehed</span><span class="sxs-lookup"><span data-stu-id="b1075-328">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1075-329">Leht</span><span class="sxs-lookup"><span data-stu-id="b1075-329">Page</span></span></th>
<th><span data-ttu-id="b1075-330">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b1075-330">Description</span></span></th>
<th><span data-ttu-id="b1075-331">Näide</span><span class="sxs-lookup"><span data-stu-id="b1075-331">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b1075-332">Kvaliteediseosed</span><span class="sxs-lookup"><span data-stu-id="b1075-332">Quality associations</span></span></td>
<td><span data-ttu-id="b1075-333">Vt selle artikli varasemaid jaotisi.</span><span class="sxs-lookup"><span data-stu-id="b1075-333">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="b1075-334">Kvaliteediseos määratleb koostatava kvaliteettellimuse puhul kogu järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="b1075-334">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="b1075-335">Kande sündmus</span><span class="sxs-lookup"><span data-stu-id="b1075-335">The transaction event</span></span></li>
<li><span data-ttu-id="b1075-336">Kaupade puhul tehtavate katsete kogum</span><span class="sxs-lookup"><span data-stu-id="b1075-336">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="b1075-337">AQL</span><span class="sxs-lookup"><span data-stu-id="b1075-337">The AQL</span></span></li>
<li><span data-ttu-id="b1075-338">Valimi plaan</span><span class="sxs-lookup"><span data-stu-id="b1075-338">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="b1075-339">Kvaliteediseos tuleb automaatset kvaliteettellimuse genereerimist nõudvas äriprotsessis määrata iga variatsiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="b1075-339">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="b1075-340">Näiteks saab kvaliteettellimuse koostada ostutellimuste, vahelaotellimuste, müügitellimuste ja tootmistellimuste äriprotsessides.</span><span class="sxs-lookup"><span data-stu-id="b1075-340">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1075-341">Katsed</span><span class="sxs-lookup"><span data-stu-id="b1075-341">Tests</span></span></td>
<td><span data-ttu-id="b1075-342">Määrake ja vaadake selle lehe abil üksikuid katseid, mis määratlevad, kas teie tooted vastavad kvaliteedispetsifikatsioonidele või mitte.</span><span class="sxs-lookup"><span data-stu-id="b1075-342">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="b1075-343">Saate määrata katsegrupile vähemalt ühe eraldi katse.</span><span class="sxs-lookup"><span data-stu-id="b1075-343">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="b1075-344">Sellisel juhul määrate ka testipõhised andmed, nt vastuvõetavad mõõtmisväärtused.</span><span class="sxs-lookup"><span data-stu-id="b1075-344">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="b1075-345">Mõõtmisväärtusi kasutatakse kvantitatiivsete katsete puhul ja katsemuutujaid kasutatakse kvalitatiivsete katsete puhul.</span><span class="sxs-lookup"><span data-stu-id="b1075-345">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="b1075-346">Kvantitatiivse katse tüüp on <strong>täisarv</strong> või <strong>murd</strong> ja sellele on määratud ka mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="b1075-346">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="b1075-347">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse numbritena.</span><span class="sxs-lookup"><span data-stu-id="b1075-347">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="b1075-348">Kvalitatiivse katse tüüp on <strong>valik</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1075-348">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="b1075-349">Kvalitatiivsed katsed nõuavad lisateavet mõõdetava katsemuutuja ja selle loetletud valikute kohta.</span><span class="sxs-lookup"><span data-stu-id="b1075-349">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="b1075-350">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse tulemuse järgi.</span><span class="sxs-lookup"><span data-stu-id="b1075-350">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="b1075-351">Tootjaettevõte sooritab kaks katset ostetud materjaliga: kvantitatiivse katse materjali kvaliteedi kohta ja kvalitatiivne katse pakendikahjustuse kohta.</span><span class="sxs-lookup"><span data-stu-id="b1075-351">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="b1075-352">Ettevõte määrab lisateabe kvalitatiivse katse kohta, et määratleda katse muutuja (kahjustatud pakend) ja selle tulemused.</span><span class="sxs-lookup"><span data-stu-id="b1075-352">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="b1075-353">Ettevõte kasutab lehte <strong>Katsegrupid</strong>, et määrata katsegrupile kaks katset ning määrata katsepõhine teave.</span><span class="sxs-lookup"><span data-stu-id="b1075-353">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="b1075-354">Katsegrupp määratakse kvaliteeditellimusele, nii et ettevõte saab teavitada kahe katse katsetulemustest.</span><span class="sxs-lookup"><span data-stu-id="b1075-354">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1075-355">Katsegrupid</span><span class="sxs-lookup"><span data-stu-id="b1075-355">Test groups</span></span></td>
<td><span data-ttu-id="b1075-356">Kasutage antud lehte katsegruppide ja katsegrupile määratud eraldi katsete seadistamiseks, redigeerimiseks ning vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="b1075-356">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="b1075-357">Ülemine paan kuvab katsegruppe ja alumine paan kuvab valitud katsegruppi määratud katseid.</span><span class="sxs-lookup"><span data-stu-id="b1075-357">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="b1075-358">Saate määrata katsegrupile mitmed põhimõtted nagu valimiplaani, vastuvõetava kvaliteeditaseme (AQL) ja nõuded purustavale katsetamisele.</span><span class="sxs-lookup"><span data-stu-id="b1075-358">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="b1075-359">Kui määrate katsegrupile eraldi katse, määratlete lisateabe, näiteks järjestuse, dokumendid ja kehtivuse kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="b1075-359">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="b1075-360">Kvantitatiivse katse puhul sisaldab teie määratletud teave ka vastuvõetavaid mõõtmisväärtusi.</span><span class="sxs-lookup"><span data-stu-id="b1075-360">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="b1075-361">Kvalitatiivse katse puhul sisaldab teave katsemuutujat ja vaiketulemust.</span><span class="sxs-lookup"><span data-stu-id="b1075-361">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="b1075-362">Kvaliteettellimusele määratud katsegrupp määratleb katsete vaikekogumi, mis tuleb määratud kaubaga sooritada.</span><span class="sxs-lookup"><span data-stu-id="b1075-362">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="b1075-363">Kuid saate kvaliteettellimuse katseid lisada, kustutada või muuta.</span><span class="sxs-lookup"><span data-stu-id="b1075-363">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="b1075-364">Iga katse tulemused kinnitatakse kvaliteettellimuses.</span><span class="sxs-lookup"><span data-stu-id="b1075-364">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="b1075-365">Tootmisettevõte määrab iga kvaliteetjuhise variandi puhul katsegrupi.</span><span class="sxs-lookup"><span data-stu-id="b1075-365">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="b1075-366">Erinevad katsegrupid näitavad erinevusi valimiplaanides, katsehulkasid, mida peab koos läbi viima, vastuvõetavat kvaliteeditaset ja muid tegureid.</span><span class="sxs-lookup"><span data-stu-id="b1075-366">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="b1075-367">Kvantitatiivsete katsete puhul on erinevused ka vastuvõetavates mõõteväärtustes.</span><span class="sxs-lookup"><span data-stu-id="b1075-367">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="b1075-368">Kvaliteedipõhimõtteid järgides määrab ettevõte igale reeglile katsegrupi, et koostada automaatselt kvaliteettellimusi lehel <strong>Kvaliteediseosed</strong>, ja määrab katsegrupi ka käsitsi loodud kvaliteettellimustele.</span><span class="sxs-lookup"><span data-stu-id="b1075-368">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1075-369">Üksuse kvaliteedigrupid</span><span class="sxs-lookup"><span data-stu-id="b1075-369">Item quality groups</span></span></td>
<td><span data-ttu-id="b1075-370">Kasutage seda lehte, et seadistada, redigeerida ja vaadata kaupu, mis on määratud kaubale määratud kvaliteedigrupile või kvaliteedigruppidele.</span><span class="sxs-lookup"><span data-stu-id="b1075-370">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="b1075-371">Kvaliteedigrupp tähistab kaupade üldisi testimisnõudeid.</span><span class="sxs-lookup"><span data-stu-id="b1075-371">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="b1075-372">Pärast katsenõuete määratlemist lehel <strong>Katsegrupid</strong> saate määratleda reeglid kvaliteettellimuste automaatseks koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="b1075-372">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="b1075-373">Protsessi hõlbustamiseks ei määratleta reegleid üksikutele kaupadele.</span><span class="sxs-lookup"><span data-stu-id="b1075-373">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="b1075-374">Selle asemel määratletakse reeglid kvaliteedigrupile, kasutades lehte <strong>Kvaliteediseosed</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1075-374">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="b1075-375">Saate kasutada valitud kvaliteedigrupi puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kaupade määramiseks sellesse gruppi.</span><span class="sxs-lookup"><span data-stu-id="b1075-375">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="b1075-376">Saate kasutada valitud kauba puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kvaliteedigruppide määramiseks sellele kaubale.</span><span class="sxs-lookup"><span data-stu-id="b1075-376">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="b1075-377">Tootmisettevõte ostab mitmesuguseid ühesuguste sissetulekukontrolli katsenõuetega toormaterjale.</span><span class="sxs-lookup"><span data-stu-id="b1075-377">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="b1075-378">Ettevõte määrab kvaliteedigrupi ja määrab sellele grupile toormaterjaliga seotud kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="b1075-378">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="b1075-379">Hiljem ostab ettevõte uut tüüpi toormaterjali, millel on samad katsenõuded.</span><span class="sxs-lookup"><span data-stu-id="b1075-379">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="b1075-380">Selle asemel, et seadistada uuele materjalile uued katsenõuded, lisab ettevõte uue materjali kaubakoodi olemasolevasse kvaliteedigruppi.</span><span class="sxs-lookup"><span data-stu-id="b1075-380">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="b1075-381">Sama tootmisettevõte toodab ka ühesuguste tootmisalaste katsenõuetega kaupu ja lähetab ühesuguste nõuetega kaubad lähetuseelsete katsete tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="b1075-381">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="b1075-382">Ettevõte määrab kaks täiendavat kvaliteedigruppi ja määrab seejärel igale grupile sobivad kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="b1075-382">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1075-383">Katse muutujad</span><span class="sxs-lookup"><span data-stu-id="b1075-383">Test variables</span></span></td>
<td><span data-ttu-id="b1075-384">Sellel lehel saate määratleda ja kuvada kvalitatiivse katsega seotud muutujaid.</span><span class="sxs-lookup"><span data-stu-id="b1075-384">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="b1075-385">Iga muutuja puhul saab määratleda nummerdatud tulemused, mis kajastavad võimalikke valikuid.</span><span class="sxs-lookup"><span data-stu-id="b1075-385">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="b1075-386">Saate määratleda katsed lehel <strong>Katsed</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1075-386">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="b1075-387">Kvalitatiivsete katsete puhul peate määrama katsetüübi <strong>Valik</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1075-387">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="b1075-388">Kasutage lehte <strong>Katsegrupid</strong> katse muutuja määramiseks individuaalsele katsele.</span><span class="sxs-lookup"><span data-stu-id="b1075-388">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="b1075-389">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="b1075-389">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="b1075-390">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="b1075-390">This inspection test has several variables.</span></span> <span data-ttu-id="b1075-391">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="b1075-391">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="b1075-392">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="b1075-392">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1075-393">Katse muutuja väljundteated</span><span class="sxs-lookup"><span data-stu-id="b1075-393">Test variable outcomes</span></span></td>
<td><span data-ttu-id="b1075-394">Kasutage seda lehte kvalitatiivse katsega seotud muutuja võimalike katsetulemuste seadistamiseks, redigeerimiseks ja vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="b1075-394">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="b1075-395">Iga tulemuse puhul tuleb määrata olek <strong>läbis</strong> või <strong>ei läbinud</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1075-395">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="b1075-396">Peate määrama muutuja ja tema väljundid iga kvalitatiivse katse jaoks, mis on määratud lehel <strong>Katsed</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1075-396">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="b1075-397">(Kvalitatiivsete katsete puhul on katse tüübiks määratud <strong>Valik</strong> lehel <strong>Katsed</strong>.) Kasutage lehte <strong>Katsegrupid</strong> katsemuutuja ja vaikeväärtuse määramiseks kindlale kvalitatiivsele katsele.</span><span class="sxs-lookup"><span data-stu-id="b1075-397">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="b1075-398">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="b1075-398">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="b1075-399">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="b1075-399">This inspection test has of several variables.</span></span> <span data-ttu-id="b1075-400">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="b1075-400">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="b1075-401">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="b1075-401">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="b1075-402">Igale tulemusele omistatakse väärtus <strong>läbis</strong> või <strong>ei läbinud</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1075-402">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="b1075-403">Iga muutuja kontrolltesti ajal registreerib katsetaja katse tulemuse, valides ühe väljundi väärtustest.</span><span class="sxs-lookup"><span data-stu-id="b1075-403">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="b1075-404">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b1075-404">Additional resources</span></span>
--------

[<span data-ttu-id="b1075-405">Kvaliteedijuhtimise protsessid</span><span class="sxs-lookup"><span data-stu-id="b1075-405">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="b1075-406">Mittevastavuse haldus</span><span class="sxs-lookup"><span data-stu-id="b1075-406">Nonconformance management</span></span>](enable-nonconformance-management.md)
