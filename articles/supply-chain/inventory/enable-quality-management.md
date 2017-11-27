---
title: "Kvaliteedijuhtimise ülevaade"
description: "Selles teemas kirjeldatakse, kuidas kasutada Microsoft Dynamics 365 for Finance and Operationsis kvaliteedijuhtimist, et täiustada tarneahela toote kvaliteeti."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c8961d1c62167192fcf32d17c2941b8813ea0629
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="quality-management-overview"></a><span data-ttu-id="bf881-103">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="bf881-103">Quality management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="bf881-104">Selles teemas kirjeldatakse, kuidas kasutada Microsoft Dynamics 365 for Finance and Operationsis kvaliteedijuhtimist, et täiustada tarneahela toote kvaliteeti.</span><span class="sxs-lookup"><span data-stu-id="bf881-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="bf881-105">Kvaliteedijuhtimise abil saate hallata ümberpööramise aegu, kui käsitsete mittevastavaid tooteid, olenemata nende päritolukohast.</span><span class="sxs-lookup"><span data-stu-id="bf881-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="bf881-106">Kuna diagnostikatüübid on seotud parandustest teatamisega, saab Microsoft Dynamics 365 for Finance and Operations plaanida ülesandeid probleemide kõrvaldamiseks ja nende kordumise vältimiseks.</span><span class="sxs-lookup"><span data-stu-id="bf881-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="bf881-107">Lisaks mittevastavuste haldamiseks mõeldud funktsioonidele hõlmab kvaliteedijuhtimine funktsioone probleemide jälgimiseks probleemi tüübi alusel (isegi sisemiste probleemide puhul) ja lühiajaliste või pikaajaliste lahenduste tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="bf881-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="bf881-108">Tulemuslikkuse võtmenäitajate (KPI) statistika annab ülevaate varasematest mittevastavuse probleemidest ja nende kõrvaldamiseks kasutatud lahendustest.</span><span class="sxs-lookup"><span data-stu-id="bf881-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="bf881-109">Saate kasutada varasemaid andmeid eelmiste kvaliteedimeetmete tulemuslikkuse ülevaatamiseks ja sobivate tulevikus kasutatavate meetmete määramiseks.</span><span class="sxs-lookup"><span data-stu-id="bf881-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="bf881-110">Kvaliteediseose seadistamisel saab Finance and Operations koostada kvaliteettellimusi mitmesugustele äriprotsessidele, sündmustele ja tingimustele.</span><span class="sxs-lookup"><span data-stu-id="bf881-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="bf881-111">Kvaliteediseos võib hõlmata konkreetset kaupa, konkreetset kaubagruppi või kõiki kaupu.</span><span class="sxs-lookup"><span data-stu-id="bf881-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="bf881-112">Kvaliteedijuhtimise kasutamise näited</span><span class="sxs-lookup"><span data-stu-id="bf881-112">Examples of the use of quality management</span></span>
<span data-ttu-id="bf881-113">Kvaliteedijuhtimine on paindlik ja seda saab rakendada mitmesugusel moel, et järgida konkreetsete tarneahela toimingute tasemete nõudeid.</span><span class="sxs-lookup"><span data-stu-id="bf881-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="bf881-114">Järgmised näited illustreerivad nende funktsioonide võimalikke kasutusviise.</span><span class="sxs-lookup"><span data-stu-id="bf881-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="bf881-115">Saate kvaliteedikontrolli protsessi automaatselt käivitada, tuginedes eelnevalt määratletud kriteeriumidele (konkreetse hankija ostutellimuse registreerimisel laos).</span><span class="sxs-lookup"><span data-stu-id="bf881-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="bf881-116">Kontrollimise ajal varude blokeerimine, et vältida heakskiitmata varude kasutamist (ostutellimuse koguste täielik blokeerimine).</span><span class="sxs-lookup"><span data-stu-id="bf881-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="bf881-117">Saate kasutada kauba valimit kvaliteediseose osana jooksvate füüsiliste varude hulga määratlemiseks, mida kontrollida tuleb.</span><span class="sxs-lookup"><span data-stu-id="bf881-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="bf881-118">Valimi aluseks võib olla fikseeritud kogus või protsent.</span><span class="sxs-lookup"><span data-stu-id="bf881-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="bf881-119">Looge kvaliteettellimused osaliste tarnete jaoks.</span><span class="sxs-lookup"><span data-stu-id="bf881-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="bf881-120">Kvaliteettellimuse loomiseks, mis põhineb tellimusega füüsiliselt saadud kogusel, peate märkima ruudu **Värskendatud koguse kohta** vormil **Kauba valim**.</span><span class="sxs-lookup"><span data-stu-id="bf881-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="bf881-121">Saate luua katsetüüpe, mis sisaldavad katse minimaalset, maksimaalset ja sihtväärtust ning teha kvalitatiivset vs kvantitatiivset kontrolli, millel on eelnevalt määratud valideerimistulemused.</span><span class="sxs-lookup"><span data-stu-id="bf881-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="bf881-122">Määrake sobiv kvaliteeditase (AQL) kvaliteedimeetme hälvete kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="bf881-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="bf881-123">Saate määrata ressursid, mida kontrollimistoiming nõuab, nt katsepiirkond ja katseinstrumendid.</span><span class="sxs-lookup"><span data-stu-id="bf881-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="bf881-124">Kvaliteediseostega töötamine</span><span class="sxs-lookup"><span data-stu-id="bf881-124">Working with quality associations</span></span>
<span data-ttu-id="bf881-125">Kvaliteediseost kasutav äriprotsess võib olla seotud mitmesuguste lähtedokumentidega, nt ostutellimuste, müügitellimuste või tootmistellimustega.</span><span class="sxs-lookup"><span data-stu-id="bf881-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="bf881-126">Iga kvaliteediseose kirje määrab ka katsete kogumi, AQL-i ning valikukava, mida rakendatakse loodud kvaliteettellimustele.</span><span class="sxs-lookup"><span data-stu-id="bf881-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="bf881-127">Peate iga äriprotsessi variatsiooni jaoks määratlema kvaliteediseose kirje.</span><span class="sxs-lookup"><span data-stu-id="bf881-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="bf881-128">Näiteks saate seadistada kvaliteediseose, mis koostab kvaliteettellimuse, kui ostutellimuse toote sissetulekut värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="bf881-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="bf881-129">Olenevalt käivitamisplaani seadistusest saab käivitusprotsessi enese blokeerida, kui on olemas avatud kvaliteettellimus, või saab blokeerida järgmised protsessid, nt ostutellimuse eest arve esitamise.</span><span class="sxs-lookup"><span data-stu-id="bf881-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="bf881-130">**Märkus.** avatud kvaliteettellimuste olemasolu korral blokeeritakse automaatselt varude koguste väljastamine.</span><span class="sxs-lookup"><span data-stu-id="bf881-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="bf881-131">Olenevalt valiku **Täielik blokeerimine** seadistusest lehel **Kaubaproovid** on kogus kas kvaliteettellimusel olev kogus või lähtedokumendi real olev kogus.</span><span class="sxs-lookup"><span data-stu-id="bf881-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="bf881-132">Nimetatud äriprotsessi puhul määratleb kvaliteediseose kirje sündmuse ja tingimused, mille jaoks kvaliteettellimus on loodud.</span><span class="sxs-lookup"><span data-stu-id="bf881-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="bf881-133">Tingimused võivad olla asukoha või juriidilise isiku põhised.</span><span class="sxs-lookup"><span data-stu-id="bf881-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="bf881-134">Purustavaid katseid hõlmavat kvaliteettellimust saab luua ainult siis, kui sündmusel on olemas vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="bf881-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="bf881-135">Järgmistes näidetes on näha, kuidas kvaliteediseose kirjet määratakse iga äriprotsessi variatsioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="bf881-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="bf881-136">Iga näite puhul võetakse järgmises tabelis kokku sündmused ja tingimused, mis on kvaliteediseose kirjega määratletud.</span><span class="sxs-lookup"><span data-stu-id="bf881-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="bf881-137">Viite tüüp</span><span class="sxs-lookup"><span data-stu-id="bf881-137">Reference type</span></span></th>
<th><span data-ttu-id="bf881-138">Sündmuse tüüp</span><span class="sxs-lookup"><span data-stu-id="bf881-138">Event type</span></span></th>
<th><span data-ttu-id="bf881-139">Käivitamine</span><span class="sxs-lookup"><span data-stu-id="bf881-139">Execution</span></span></th>
<th><span data-ttu-id="bf881-140">Sündmuse blokeerimine</span><span class="sxs-lookup"><span data-stu-id="bf881-140">Event blocking</span></span></th>
<th><span data-ttu-id="bf881-141">Dokumendi viide</span><span class="sxs-lookup"><span data-stu-id="bf881-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="bf881-142">Varud</span><span class="sxs-lookup"><span data-stu-id="bf881-142">Inventory</span></span></td>
<td><span data-ttu-id="bf881-143">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="bf881-143">Not applicable</span></span></td>
<td><span data-ttu-id="bf881-144">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="bf881-144">Not applicable</span></span></td>
<td><span data-ttu-id="bf881-145">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-145">None</span></span></td>
<td><span data-ttu-id="bf881-146">Kõik</span><span class="sxs-lookup"><span data-stu-id="bf881-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="bf881-147">Müük</span><span class="sxs-lookup"><span data-stu-id="bf881-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="bf881-148">Komplekteerimise protsess on plaanitud</span><span class="sxs-lookup"><span data-stu-id="bf881-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="bf881-149">Enne</span><span class="sxs-lookup"><span data-stu-id="bf881-149">Before</span></span></td>
<td><span data-ttu-id="bf881-150">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="bf881-151">Ainult Konkreetne ID, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="bf881-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-152">Komplekteerimise protsess</span><span class="sxs-lookup"><span data-stu-id="bf881-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-153">Saateleht</span><span class="sxs-lookup"><span data-stu-id="bf881-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-154">Arve</span><span class="sxs-lookup"><span data-stu-id="bf881-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bf881-155">Saateleht</span><span class="sxs-lookup"><span data-stu-id="bf881-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-156">Enne</span><span class="sxs-lookup"><span data-stu-id="bf881-156">Before</span></span></td>
<td><span data-ttu-id="bf881-157">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-158">Saateleht</span><span class="sxs-lookup"><span data-stu-id="bf881-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-159">Arve</span><span class="sxs-lookup"><span data-stu-id="bf881-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="bf881-160">Ost</span><span class="sxs-lookup"><span data-stu-id="bf881-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="bf881-161">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="bf881-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="bf881-162">Enne</span><span class="sxs-lookup"><span data-stu-id="bf881-162">Before</span></span></td>
<td><span data-ttu-id="bf881-163">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-164">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="bf881-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-165">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="bf881-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-166">Arve</span><span class="sxs-lookup"><span data-stu-id="bf881-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bf881-167">Pärast</span><span class="sxs-lookup"><span data-stu-id="bf881-167">After</span></span></td>
<td><span data-ttu-id="bf881-168">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-169">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="bf881-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-170">Arve</span><span class="sxs-lookup"><span data-stu-id="bf881-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bf881-171">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="bf881-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-172">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="bf881-172">Not applicable</span></span></td>
<td><span data-ttu-id="bf881-173">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-174">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="bf881-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-175">Arve</span><span class="sxs-lookup"><span data-stu-id="bf881-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="bf881-176">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="bf881-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-177">Enne</span><span class="sxs-lookup"><span data-stu-id="bf881-177">Before</span></span></td>
<td><span data-ttu-id="bf881-178">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-179">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="bf881-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-180">Arve</span><span class="sxs-lookup"><span data-stu-id="bf881-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bf881-181">Pärast</span><span class="sxs-lookup"><span data-stu-id="bf881-181">After</span></span></td>
<td><span data-ttu-id="bf881-182">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-183">Arve</span><span class="sxs-lookup"><span data-stu-id="bf881-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="bf881-184">Tootmine</span><span class="sxs-lookup"><span data-stu-id="bf881-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-185">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="bf881-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-186">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="bf881-186">Not applicable</span></span></td>
<td><span data-ttu-id="bf881-187">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="bf881-188">Kõik</span><span class="sxs-lookup"><span data-stu-id="bf881-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-189">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="bf881-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-190">Lõpp</span><span class="sxs-lookup"><span data-stu-id="bf881-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="bf881-191">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="bf881-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-192">Enne</span><span class="sxs-lookup"><span data-stu-id="bf881-192">Before</span></span></td>
<td><span data-ttu-id="bf881-193">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-194">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="bf881-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-195">Lõpp</span><span class="sxs-lookup"><span data-stu-id="bf881-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bf881-196">Pärast</span><span class="sxs-lookup"><span data-stu-id="bf881-196">After</span></span></td>
<td><span data-ttu-id="bf881-197">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-198">Lõpp</span><span class="sxs-lookup"><span data-stu-id="bf881-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="bf881-199">Vaheladu</span><span class="sxs-lookup"><span data-stu-id="bf881-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-200">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="bf881-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="bf881-201">Enne</span><span class="sxs-lookup"><span data-stu-id="bf881-201">Before</span></span></td>
<td><span data-ttu-id="bf881-202">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="bf881-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-203">Lõpp</span><span class="sxs-lookup"><span data-stu-id="bf881-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-204">Pärast</span><span class="sxs-lookup"><span data-stu-id="bf881-204">After</span></span></td>
<td><span data-ttu-id="bf881-205">Lõpp</span><span class="sxs-lookup"><span data-stu-id="bf881-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-206">Lõpp</span><span class="sxs-lookup"><span data-stu-id="bf881-206">End</span></span></td>
<td><span data-ttu-id="bf881-207">Enne</span><span class="sxs-lookup"><span data-stu-id="bf881-207">Before</span></span></td>
<td><span data-ttu-id="bf881-208">Lõpp</span><span class="sxs-lookup"><span data-stu-id="bf881-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bf881-209">Protsessi operatsioon</span><span class="sxs-lookup"><span data-stu-id="bf881-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-210">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="bf881-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="bf881-211">Enne</span><span class="sxs-lookup"><span data-stu-id="bf881-211">Before</span></span></td>
<td><span data-ttu-id="bf881-212">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-213">Konkreetne ID, Grupp või Kõik ja Ressursipõhine, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="bf881-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-214">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="bf881-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-215">Pärast</span><span class="sxs-lookup"><span data-stu-id="bf881-215">After</span></span></td>
<td><span data-ttu-id="bf881-216">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="bf881-217">Kaastoote tootmine</span><span class="sxs-lookup"><span data-stu-id="bf881-217">Co-product production</span></span></td>
<td><span data-ttu-id="bf881-218">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="bf881-218">Registration</span></span></td>
<td><span data-ttu-id="bf881-219">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="bf881-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-220">Puudub</span><span class="sxs-lookup"><span data-stu-id="bf881-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="bf881-221">Kõik</span><span class="sxs-lookup"><span data-stu-id="bf881-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="bf881-222">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="bf881-222">Report as finished</span></span></td>
<td><span data-ttu-id="bf881-223">Enne</span><span class="sxs-lookup"><span data-stu-id="bf881-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-224">Pärast</span><span class="sxs-lookup"><span data-stu-id="bf881-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="bf881-225">Järgmises tabelis on veel teavet kvaliteettellimuste loomise kohta konkreetset tüüpi protsessidele.</span><span class="sxs-lookup"><span data-stu-id="bf881-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="bf881-226">Protsessi tüüp</span><span class="sxs-lookup"><span data-stu-id="bf881-226">Type of process</span></span></th>
<th><span data-ttu-id="bf881-227">Millal saab kvaliteettellimusi automaatselt luua</span><span class="sxs-lookup"><span data-stu-id="bf881-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="bf881-228">Millal saab kvaliteettellimusi luua, kui on vajalik purustav katsetamine</span><span class="sxs-lookup"><span data-stu-id="bf881-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="bf881-229">Tingimuse teave</span><span class="sxs-lookup"><span data-stu-id="bf881-229">Condition information</span></span></th>
<th><span data-ttu-id="bf881-230">Käsitsi loomise teave</span><span class="sxs-lookup"><span data-stu-id="bf881-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="bf881-231">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="bf881-231">Purchase order</span></span></td>
<td><span data-ttu-id="bf881-232">Enne või pärast sissetulekute loendi või vastuvõetava materjali toote sissetuleku sisestamist</span><span class="sxs-lookup"><span data-stu-id="bf881-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="bf881-233">Pärast vastuvõetava materjali toote sissetuleku sisestamist, kuna materjal peab olema kättesaadav purustavaks katsetamiseks</span><span class="sxs-lookup"><span data-stu-id="bf881-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="bf881-234">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="bf881-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="bf881-235">Käsitsi loodud ostutellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="bf881-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-236">Vahelao order</span><span class="sxs-lookup"><span data-stu-id="bf881-236">Quarantine order</span></span></td>
<td><span data-ttu-id="bf881-237">Enne või pärast vahelao tellimuse lõpetatuna kinnitamist või lõpetamist</span><span class="sxs-lookup"><span data-stu-id="bf881-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="bf881-238">Purustavaid katseid nõudvaid kvaliteettellimusi ei saa koostada.</span><span class="sxs-lookup"><span data-stu-id="bf881-238">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="bf881-239">Eeldatakse, et vahelao tellimuse funktsioon tegeleb rikutud materjali likvideerimisega.</span><span class="sxs-lookup"><span data-stu-id="bf881-239">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="bf881-240">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="bf881-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="bf881-241">Käsitsi loodud vahelaoorderile viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="bf881-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-242">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="bf881-242">Sales order</span></span></td>
<td><span data-ttu-id="bf881-243">Enne plaanitud komplekteerimisprotsessi või saatelehe uuendamist lähetatavate kaupade puhul</span><span class="sxs-lookup"><span data-stu-id="bf881-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="bf881-244">Igas etapis</span><span class="sxs-lookup"><span data-stu-id="bf881-244">At any step</span></span></td>
<td><span data-ttu-id="bf881-245">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või klienti või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="bf881-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="bf881-246">Käsitsi loodud müügitellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="bf881-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-247">Tootmistellimus</span><span class="sxs-lookup"><span data-stu-id="bf881-247">Production order</span></span></td>
<td><span data-ttu-id="bf881-248">Enne või pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="bf881-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="bf881-249">Pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="bf881-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="bf881-250">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala või kaupa või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="bf881-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="bf881-251">Käsitsi loodud tootmistellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="bf881-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-252">Tootmistellimus, millel on protsessitoiming</span><span class="sxs-lookup"><span data-stu-id="bf881-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="bf881-253">Enne või pärast toimingu aruande lõpetamist</span><span class="sxs-lookup"><span data-stu-id="bf881-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="bf881-254">Pärast viimase toimingu tootmise lõpetamisest teatamist</span><span class="sxs-lookup"><span data-stu-id="bf881-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="bf881-255">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või operatsiooniressurssi või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="bf881-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="bf881-256">Käsitsi loodud protsessitoimingule viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="bf881-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bf881-257">Varud</span><span class="sxs-lookup"><span data-stu-id="bf881-257">Inventory</span></span></td>
<td><span data-ttu-id="bf881-258">Kvaliteettellimust ei saa automaatselt koostada varude töölehe kandele või üleviimistellimuse kandele.</span><span class="sxs-lookup"><span data-stu-id="bf881-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="bf881-259">Kvaliteettellimus tuleb kauba laokogusele käsitsi koostada.</span><span class="sxs-lookup"><span data-stu-id="bf881-259">A quality order must be created manually for an item's inventory quantity.</span></span> <span data-ttu-id="bf881-260">Nõutav on füüsiline vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="bf881-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="bf881-261">Kvaliteedijuhtimise lehed</span><span class="sxs-lookup"><span data-stu-id="bf881-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf881-262">Lehekülg</span><span class="sxs-lookup"><span data-stu-id="bf881-262">Page</span></span></th>
<th><span data-ttu-id="bf881-263">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bf881-263">Description</span></span></th>
<th><span data-ttu-id="bf881-264">Näide</span><span class="sxs-lookup"><span data-stu-id="bf881-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf881-265">Kvaliteediseosed</span><span class="sxs-lookup"><span data-stu-id="bf881-265">Quality associations</span></span></td>
<td><span data-ttu-id="bf881-266">Vt selle artikli varasemaid jaotisi.</span><span class="sxs-lookup"><span data-stu-id="bf881-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="bf881-267">Kvaliteediseos määratleb koostatava kvaliteettellimuse puhul kogu järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="bf881-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="bf881-268">Kande sündmus</span><span class="sxs-lookup"><span data-stu-id="bf881-268">The transaction event</span></span></li>
<li><span data-ttu-id="bf881-269">Kaupade puhul tehtavate katsete kogum</span><span class="sxs-lookup"><span data-stu-id="bf881-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="bf881-270">AQL</span><span class="sxs-lookup"><span data-stu-id="bf881-270">The AQL</span></span></li>
<li><span data-ttu-id="bf881-271">Valimi plaan</span><span class="sxs-lookup"><span data-stu-id="bf881-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="bf881-272">Kvaliteediseos tuleb automaatset kvaliteettellimuse genereerimist nõudvas äriprotsessis määrata iga variatsiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="bf881-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="bf881-273">Näiteks saab kvaliteettellimuse koostada ostutellimuste, vahelaotellimuste, müügitellimuste ja tootmistellimuste äriprotsessides.</span><span class="sxs-lookup"><span data-stu-id="bf881-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf881-274">Katsed</span><span class="sxs-lookup"><span data-stu-id="bf881-274">Tests</span></span></td>
<td><span data-ttu-id="bf881-275">Määrake ja vaadake selle lehe abil üksikuid katseid, mis määratlevad, kas teie tooted vastavad kvaliteedispetsifikatsioonidele või mitte.</span><span class="sxs-lookup"><span data-stu-id="bf881-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="bf881-276">Saate määrata katsegrupile vähemalt ühe eraldi katse.</span><span class="sxs-lookup"><span data-stu-id="bf881-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="bf881-277">Sellisel juhul määrate ka testipõhised andmed, nt vastuvõetavad mõõtmisväärtused.</span><span class="sxs-lookup"><span data-stu-id="bf881-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="bf881-278">Mõõtmisväärtusi kasutatakse kvantitatiivsete katsete puhul ja katsemuutujaid kasutatakse kvalitatiivsete katsete puhul.</span><span class="sxs-lookup"><span data-stu-id="bf881-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="bf881-279">Kvantitatiivse katse tüüp on <strong>täisarv</strong> või <strong>murd</strong> ja sellele on määratud ka mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="bf881-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="bf881-280">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse numbritena.</span><span class="sxs-lookup"><span data-stu-id="bf881-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="bf881-281">Kvalitatiivse katse tüüp on <strong>valik</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf881-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="bf881-282">Kvalitatiivsed katsed nõuavad lisateavet mõõdetava katsemuutuja ja selle loetletud valikute kohta.</span><span class="sxs-lookup"><span data-stu-id="bf881-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="bf881-283">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse tulemuse järgi.</span><span class="sxs-lookup"><span data-stu-id="bf881-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="bf881-284">Tootjaettevõte sooritab kaks katset ostetud materjaliga: kvantitatiivse katse materjali kvaliteedi kohta ja kvalitatiivne katse pakendikahjustuse kohta.</span><span class="sxs-lookup"><span data-stu-id="bf881-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="bf881-285">Ettevõte määrab lisateabe kvalitatiivse katse kohta, et määratleda katse muutuja (kahjustatud pakend) ja selle tulemused.</span><span class="sxs-lookup"><span data-stu-id="bf881-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="bf881-286">Ettevõte kasutab lehte <strong>Katsegrupid</strong>, et määrata katsegrupile kaks katset ning määrata katsepõhine teave.</span><span class="sxs-lookup"><span data-stu-id="bf881-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="bf881-287">Katsegrupp määratakse kvaliteeditellimusele, nii et ettevõte saab teavitada kahe katse katsetulemustest.</span><span class="sxs-lookup"><span data-stu-id="bf881-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf881-288">Katsegrupid</span><span class="sxs-lookup"><span data-stu-id="bf881-288">Test groups</span></span></td>
<td><span data-ttu-id="bf881-289">Kasutage antud lehte katsegruppide ja katsegrupile määratud eraldi katsete seadistamiseks, redigeerimiseks ning vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="bf881-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="bf881-290">Ülemine paan kuvab katsegruppe ja alumine paan kuvab valitud katsegruppi määratud katseid.</span><span class="sxs-lookup"><span data-stu-id="bf881-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="bf881-291">Saate määrata katsegrupile mitmed põhimõtted nagu valimiplaani, vastuvõetava kvaliteeditaseme (AQL) ja nõuded purustavale katsetamisele.</span><span class="sxs-lookup"><span data-stu-id="bf881-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="bf881-292">Kui määrate katsegrupile eraldi katse, määratlete lisateabe, näiteks järjestuse, dokumendid ja kehtivuse kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="bf881-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="bf881-293">Kvantitatiivse katse puhul sisaldab teie määratletud teave ka vastuvõetavaid mõõtmisväärtusi.</span><span class="sxs-lookup"><span data-stu-id="bf881-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="bf881-294">Kvalitatiivse katse puhul sisaldab teave katsemuutujat ja vaiketulemust.</span><span class="sxs-lookup"><span data-stu-id="bf881-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="bf881-295">Kvaliteettellimusele määratud katsegrupp määratleb katsete vaikekogumi, mis tuleb määratud kaubaga sooritada.</span><span class="sxs-lookup"><span data-stu-id="bf881-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="bf881-296">Kuid saate kvaliteettellimuse katseid lisada, kustutada või muuta.</span><span class="sxs-lookup"><span data-stu-id="bf881-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="bf881-297">Iga katse tulemused kinnitatakse kvaliteettellimuses.</span><span class="sxs-lookup"><span data-stu-id="bf881-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="bf881-298">Tootmisettevõte määrab iga kvaliteetjuhise variandi puhul katsegrupi.</span><span class="sxs-lookup"><span data-stu-id="bf881-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="bf881-299">Erinevad katsegrupid näitavad erinevusi valimiplaanides, katsehulkasid, mida peab koos läbi viima, vastuvõetavat kvaliteeditaset ja muid tegureid.</span><span class="sxs-lookup"><span data-stu-id="bf881-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="bf881-300">Kvantitatiivsete katsete puhul on erinevused ka vastuvõetavates mõõteväärtustes.</span><span class="sxs-lookup"><span data-stu-id="bf881-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="bf881-301">Kvaliteedipõhimõtteid järgides määrab ettevõte igale reeglile katsegrupi, et koostada automaatselt kvaliteettellimusi lehel <strong>Kvaliteediseosed</strong>, ja määrab katsegrupi ka käsitsi loodud kvaliteettellimustele.</span><span class="sxs-lookup"><span data-stu-id="bf881-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf881-302">Üksuse kvaliteedigrupid</span><span class="sxs-lookup"><span data-stu-id="bf881-302">Item quality groups</span></span></td>
<td><span data-ttu-id="bf881-303">Kasutage seda lehte, et seadistada, redigeerida ja vaadata kaupu, mis on määratud kaubale määratud kvaliteedigrupile või kvaliteedigruppidele.</span><span class="sxs-lookup"><span data-stu-id="bf881-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="bf881-304">Kvaliteedigrupp tähistab kaupade üldisi testimisnõudeid.</span><span class="sxs-lookup"><span data-stu-id="bf881-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="bf881-305">Pärast katsenõuete määratlemist lehel <strong>Katsegrupid</strong> saate määratleda reeglid kvaliteettellimuste automaatseks koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="bf881-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="bf881-306">Protsessi hõlbustamiseks ei määratleta reegleid üksikutele kaupadele.</span><span class="sxs-lookup"><span data-stu-id="bf881-306">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="bf881-307">Selle asemel määratletakse reeglid kvaliteedigrupile, kasutades lehte <strong>Kvaliteediseosed</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf881-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="bf881-308">Saate kasutada valitud kvaliteedigrupi puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kaupade määramiseks sellesse gruppi.</span><span class="sxs-lookup"><span data-stu-id="bf881-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="bf881-309">Saate kasutada valitud kauba puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kvaliteedigruppide määramiseks sellele kaubale.</span><span class="sxs-lookup"><span data-stu-id="bf881-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="bf881-310">Tootmisettevõte ostab mitmesuguseid ühesuguste sissetulekukontrolli katsenõuetega toormaterjale.</span><span class="sxs-lookup"><span data-stu-id="bf881-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="bf881-311">Ettevõte määrab kvaliteedigrupi ja määrab sellele grupile toormaterjaliga seotud kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="bf881-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="bf881-312">Hiljem ostab ettevõte uut tüüpi toormaterjali, millel on samad katsenõuded.</span><span class="sxs-lookup"><span data-stu-id="bf881-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="bf881-313">Selle asemel, et seadistada uuele materjalile uued katsenõuded, lisab ettevõte uue materjali kaubakoodi olemasolevasse kvaliteedigruppi.</span><span class="sxs-lookup"><span data-stu-id="bf881-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="bf881-314">Sama tootmisettevõte toodab ka ühesuguste tootmisalaste katsenõuetega kaupu ja lähetab ühesuguste nõuetega kaubad lähetuseelsete katsete tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="bf881-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="bf881-315">Ettevõte määrab kaks täiendavat kvaliteedigruppi ja määrab seejärel igale grupile sobivad kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="bf881-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf881-316">Katse muutujad</span><span class="sxs-lookup"><span data-stu-id="bf881-316">Test variables</span></span></td>
<td><span data-ttu-id="bf881-317">Sellel lehel saate määratleda ja kuvada kvalitatiivse katsega seotud muutujaid.</span><span class="sxs-lookup"><span data-stu-id="bf881-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="bf881-318">Iga muutuja puhul saab määratleda nummerdatud tulemused, mis kajastavad võimalikke valikuid.</span><span class="sxs-lookup"><span data-stu-id="bf881-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="bf881-319">Saate määratleda katsed lehel <strong>Katsed</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf881-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="bf881-320">Kvalitatiivsete katsete puhul peate määrama katsetüübi <strong>Valik</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf881-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="bf881-321">Kasutage lehte <strong>Katsegrupid</strong> katse muutuja määramiseks individuaalsele katsele.</span><span class="sxs-lookup"><span data-stu-id="bf881-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="bf881-322">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="bf881-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="bf881-323">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="bf881-323">This inspection test has several variables.</span></span> <span data-ttu-id="bf881-324">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="bf881-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="bf881-325">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="bf881-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf881-326">Katse muutuja väljundteated</span><span class="sxs-lookup"><span data-stu-id="bf881-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="bf881-327">Kasutage seda lehte kvalitatiivse katsega seotud muutuja võimalike katsetulemuste seadistamiseks, redigeerimiseks ja vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="bf881-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="bf881-328">Iga tulemuse puhul tuleb määrata olek <strong>läbis</strong> või <strong>ei läbinud</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf881-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="bf881-329">Peate määrama muutuja ja tema väljundid iga kvalitatiivse katse jaoks, mis on määratud lehel <strong>Katsed</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf881-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="bf881-330">(Kvalitatiivsete katsete puhul on katse tüübiks määratud <strong>Valik</strong> lehel <strong>Katsed</strong>.) Kasutage lehte <strong>Katsegrupid</strong> katsemuutuja ja vaikeväärtuse määramiseks kindlale kvalitatiivsele katsele.</span><span class="sxs-lookup"><span data-stu-id="bf881-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="bf881-331">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="bf881-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="bf881-332">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="bf881-332">This inspection test has of several variables.</span></span> <span data-ttu-id="bf881-333">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="bf881-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="bf881-334">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="bf881-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="bf881-335">Igale tulemusele omistatakse väärtus <strong>läbis</strong> või <strong>ei läbinud</strong>.</span><span class="sxs-lookup"><span data-stu-id="bf881-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="bf881-336">Iga muutuja kontrolltesti ajal registreerib katsetaja katse tulemuse, valides ühe väljundi väärtustest.</span><span class="sxs-lookup"><span data-stu-id="bf881-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="bf881-337">Vt ka</span><span class="sxs-lookup"><span data-stu-id="bf881-337">See also</span></span>
--------

[<span data-ttu-id="bf881-338">Kvaliteedijuhtimise protsessid</span><span class="sxs-lookup"><span data-stu-id="bf881-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="bf881-339">Mittevastavuse haldamise võimaldamine</span><span class="sxs-lookup"><span data-stu-id="bf881-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)

