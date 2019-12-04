---
title: Kvaliteedijuhtimise ülevaade
description: Selles teemas kirjeldatakse, kuidas kasutada rakenduses Dynamics 365 Supply Chain Management kvaliteedijuhtimist, et täiustada tarneahela toote kvaliteeti.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2d51c659d9d06f075458359d81de978e7a6d14b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814394"
---
# <a name="quality-management-overview"></a><span data-ttu-id="8344d-103">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="8344d-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8344d-104">Selles teemas kirjeldatakse, kuidas kasutada rakenduses Dynamics 365 Supply Chain Management kvaliteedijuhtimist, et täiustada tarneahela toote kvaliteeti.</span><span class="sxs-lookup"><span data-stu-id="8344d-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="8344d-105">Kvaliteedijuhtimise abil saate hallata ümberpööramise aegu, kui käsitsete mittevastavaid tooteid, olenemata nende päritolukohast.</span><span class="sxs-lookup"><span data-stu-id="8344d-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="8344d-106">Kuna diagnostikatüübid on seotud parandustest teatamisega, saab Supply Chain Management plaanida ülesandeid probleemide kõrvaldamiseks ja nende kordumise vältimiseks.</span><span class="sxs-lookup"><span data-stu-id="8344d-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="8344d-107">Lisaks mittevastavuste haldamiseks mõeldud funktsioonidele hõlmab kvaliteedijuhtimine funktsioone probleemide jälgimiseks probleemi tüübi alusel (isegi sisemiste probleemide puhul) ja lühiajaliste või pikaajaliste lahenduste tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="8344d-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="8344d-108">Tulemuslikkuse võtmenäitajate (KPI) statistika annab ülevaate varasematest mittevastavuse probleemidest ja nende kõrvaldamiseks kasutatud lahendustest.</span><span class="sxs-lookup"><span data-stu-id="8344d-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="8344d-109">Saate kasutada varasemaid andmeid eelmiste kvaliteedimeetmete tulemuslikkuse ülevaatamiseks ja sobivate tulevikus kasutatavate meetmete määramiseks.</span><span class="sxs-lookup"><span data-stu-id="8344d-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="8344d-110">Kvaliteediseose seadistamisel saab Supply Chain Management koostada kvaliteettellimusi mitmesugustele äriprotsessidele, sündmustele ja tingimustele.</span><span class="sxs-lookup"><span data-stu-id="8344d-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="8344d-111">Kvaliteediseos võib hõlmata konkreetset kaupa, konkreetset kaubagruppi või kõiki kaupu.</span><span class="sxs-lookup"><span data-stu-id="8344d-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="8344d-112">Kvaliteedijuhtimise kasutamise näited</span><span class="sxs-lookup"><span data-stu-id="8344d-112">Examples of the use of quality management</span></span>
<span data-ttu-id="8344d-113">Kvaliteedijuhtimine on paindlik ja seda saab rakendada mitmesugusel moel, et järgida konkreetsete tarneahela toimingute tasemete nõudeid.</span><span class="sxs-lookup"><span data-stu-id="8344d-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="8344d-114">Järgmised näited illustreerivad nende funktsioonide võimalikke kasutusviise.</span><span class="sxs-lookup"><span data-stu-id="8344d-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="8344d-115">Saate kvaliteedikontrolli protsessi automaatselt käivitada, tuginedes eelnevalt määratletud kriteeriumidele (konkreetse hankija ostutellimuse registreerimisel laos).</span><span class="sxs-lookup"><span data-stu-id="8344d-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="8344d-116">Kontrollimise ajal varude blokeerimine, et vältida heakskiitmata varude kasutamist (ostutellimuse koguste täielik blokeerimine).</span><span class="sxs-lookup"><span data-stu-id="8344d-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="8344d-117">Saate kasutada kauba valimit kvaliteediseose osana jooksvate füüsiliste varude hulga määratlemiseks, mida kontrollida tuleb.</span><span class="sxs-lookup"><span data-stu-id="8344d-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="8344d-118">Valimi aluseks võib olla fikseeritud kogus või protsent.</span><span class="sxs-lookup"><span data-stu-id="8344d-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="8344d-119">Looge kvaliteettellimused osaliste tarnete jaoks.</span><span class="sxs-lookup"><span data-stu-id="8344d-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="8344d-120">Kvaliteettellimuse loomiseks, mis põhineb tellimusega füüsiliselt saadud kogusel, peate märkima ruudu **Värskendatud koguse kohta** vormil **Kauba valim**.</span><span class="sxs-lookup"><span data-stu-id="8344d-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="8344d-121">Saate luua katsetüüpe, mis sisaldavad katse minimaalset, maksimaalset ja sihtväärtust ning teha kvalitatiivset vs kvantitatiivset kontrolli, millel on eelnevalt määratud valideerimistulemused.</span><span class="sxs-lookup"><span data-stu-id="8344d-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="8344d-122">Määrake sobiv kvaliteeditase (AQL) kvaliteedimeetme hälvete kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="8344d-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="8344d-123">Saate määrata ressursid, mida kontrollimistoiming nõuab, nt katsepiirkond ja katseinstrumendid.</span><span class="sxs-lookup"><span data-stu-id="8344d-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="8344d-124">Kvaliteediseostega töötamine</span><span class="sxs-lookup"><span data-stu-id="8344d-124">Working with quality associations</span></span>
<span data-ttu-id="8344d-125">Kvaliteediseost kasutav äriprotsess võib olla seotud mitmesuguste lähtedokumentidega, nt ostutellimuste, müügitellimuste või tootmistellimustega.</span><span class="sxs-lookup"><span data-stu-id="8344d-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="8344d-126">Iga kvaliteediseose kirje määrab ka katsete kogumi, AQL-i ning valikukava, mida rakendatakse loodud kvaliteettellimustele.</span><span class="sxs-lookup"><span data-stu-id="8344d-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="8344d-127">Peate iga äriprotsessi variatsiooni jaoks määratlema kvaliteediseose kirje.</span><span class="sxs-lookup"><span data-stu-id="8344d-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="8344d-128">Näiteks saate seadistada kvaliteediseose, mis koostab kvaliteettellimuse, kui ostutellimuse toote sissetulekut värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="8344d-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="8344d-129">Olenevalt käivitamisplaani seadistusest saab käivitusprotsessi enese blokeerida, kui on olemas avatud kvaliteettellimus, või saab blokeerida järgmised protsessid, nt ostutellimuse eest arve esitamise.</span><span class="sxs-lookup"><span data-stu-id="8344d-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="8344d-130">**Märkus.** avatud kvaliteettellimuste olemasolu korral blokeeritakse automaatselt varude koguste väljastamine.</span><span class="sxs-lookup"><span data-stu-id="8344d-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="8344d-131">Olenevalt valiku **Täielik blokeerimine** seadistusest lehel **Kaubaproovid** on kogus kas kvaliteettellimusel olev kogus või lähtedokumendi real olev kogus.</span><span class="sxs-lookup"><span data-stu-id="8344d-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="8344d-132">Nimetatud äriprotsessi puhul määratleb kvaliteediseose kirje sündmuse ja tingimused, mille jaoks kvaliteettellimus on loodud.</span><span class="sxs-lookup"><span data-stu-id="8344d-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="8344d-133">Tingimused võivad olla asukoha või juriidilise isiku põhised.</span><span class="sxs-lookup"><span data-stu-id="8344d-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="8344d-134">Purustavaid katseid hõlmavat kvaliteettellimust saab luua ainult siis, kui sündmusel on olemas vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="8344d-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="8344d-135">Järgmistes näidetes on näha, kuidas kvaliteediseose kirjet määratakse iga äriprotsessi variatsioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="8344d-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="8344d-136">Iga näite puhul võetakse järgmises tabelis kokku sündmused ja tingimused, mis on kvaliteediseose kirjega määratletud.</span><span class="sxs-lookup"><span data-stu-id="8344d-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="8344d-137">Viite tüüp</span><span class="sxs-lookup"><span data-stu-id="8344d-137">Reference type</span></span></th>
<th><span data-ttu-id="8344d-138">Sündmuse tüüp</span><span class="sxs-lookup"><span data-stu-id="8344d-138">Event type</span></span></th>
<th><span data-ttu-id="8344d-139">Käivitamine</span><span class="sxs-lookup"><span data-stu-id="8344d-139">Execution</span></span></th>
<th><span data-ttu-id="8344d-140">Sündmuse blokeerimine</span><span class="sxs-lookup"><span data-stu-id="8344d-140">Event blocking</span></span></th>
<th><span data-ttu-id="8344d-141">Dokumendi viide</span><span class="sxs-lookup"><span data-stu-id="8344d-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="8344d-142">Varud</span><span class="sxs-lookup"><span data-stu-id="8344d-142">Inventory</span></span></td>
<td><span data-ttu-id="8344d-143">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="8344d-143">Not applicable</span></span></td>
<td><span data-ttu-id="8344d-144">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="8344d-144">Not applicable</span></span></td>
<td><span data-ttu-id="8344d-145">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-145">None</span></span></td>
<td><span data-ttu-id="8344d-146">Kõik</span><span class="sxs-lookup"><span data-stu-id="8344d-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="8344d-147">Müük</span><span class="sxs-lookup"><span data-stu-id="8344d-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="8344d-148">Komplekteerimise protsess on plaanitud</span><span class="sxs-lookup"><span data-stu-id="8344d-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="8344d-149">Enne</span><span class="sxs-lookup"><span data-stu-id="8344d-149">Before</span></span></td>
<td><span data-ttu-id="8344d-150">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="8344d-151">Ainult Konkreetne ID, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="8344d-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-152">Komplekteerimise protsess</span><span class="sxs-lookup"><span data-stu-id="8344d-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-153">Saateleht</span><span class="sxs-lookup"><span data-stu-id="8344d-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-154">Arve</span><span class="sxs-lookup"><span data-stu-id="8344d-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8344d-155">Saateleht</span><span class="sxs-lookup"><span data-stu-id="8344d-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-156">Enne</span><span class="sxs-lookup"><span data-stu-id="8344d-156">Before</span></span></td>
<td><span data-ttu-id="8344d-157">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-158">Saateleht</span><span class="sxs-lookup"><span data-stu-id="8344d-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-159">Arve</span><span class="sxs-lookup"><span data-stu-id="8344d-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="8344d-160">Ost</span><span class="sxs-lookup"><span data-stu-id="8344d-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="8344d-161">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="8344d-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="8344d-162">Enne</span><span class="sxs-lookup"><span data-stu-id="8344d-162">Before</span></span></td>
<td><span data-ttu-id="8344d-163">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-164">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="8344d-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-165">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="8344d-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-166">Arve</span><span class="sxs-lookup"><span data-stu-id="8344d-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8344d-167">Pärast</span><span class="sxs-lookup"><span data-stu-id="8344d-167">After</span></span></td>
<td><span data-ttu-id="8344d-168">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-169">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="8344d-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-170">Arve</span><span class="sxs-lookup"><span data-stu-id="8344d-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8344d-171">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="8344d-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-172">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="8344d-172">Not applicable</span></span></td>
<td><span data-ttu-id="8344d-173">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-174">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="8344d-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-175">Arve</span><span class="sxs-lookup"><span data-stu-id="8344d-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="8344d-176">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="8344d-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-177">Enne</span><span class="sxs-lookup"><span data-stu-id="8344d-177">Before</span></span></td>
<td><span data-ttu-id="8344d-178">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-179">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="8344d-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-180">Arve</span><span class="sxs-lookup"><span data-stu-id="8344d-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8344d-181">Pärast</span><span class="sxs-lookup"><span data-stu-id="8344d-181">After</span></span></td>
<td><span data-ttu-id="8344d-182">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-183">Arve</span><span class="sxs-lookup"><span data-stu-id="8344d-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="8344d-184">Tootmine</span><span class="sxs-lookup"><span data-stu-id="8344d-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-185">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="8344d-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-186">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="8344d-186">Not applicable</span></span></td>
<td><span data-ttu-id="8344d-187">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="8344d-188">Kõik</span><span class="sxs-lookup"><span data-stu-id="8344d-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-189">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="8344d-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-190">Lõpp</span><span class="sxs-lookup"><span data-stu-id="8344d-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="8344d-191">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="8344d-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-192">Enne</span><span class="sxs-lookup"><span data-stu-id="8344d-192">Before</span></span></td>
<td><span data-ttu-id="8344d-193">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-194">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="8344d-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-195">Lõpp</span><span class="sxs-lookup"><span data-stu-id="8344d-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8344d-196">Pärast</span><span class="sxs-lookup"><span data-stu-id="8344d-196">After</span></span></td>
<td><span data-ttu-id="8344d-197">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-198">Lõpp</span><span class="sxs-lookup"><span data-stu-id="8344d-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="8344d-199">Vaheladu</span><span class="sxs-lookup"><span data-stu-id="8344d-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-200">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="8344d-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="8344d-201">Enne</span><span class="sxs-lookup"><span data-stu-id="8344d-201">Before</span></span></td>
<td><span data-ttu-id="8344d-202">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="8344d-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-203">Lõpp</span><span class="sxs-lookup"><span data-stu-id="8344d-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-204">Pärast</span><span class="sxs-lookup"><span data-stu-id="8344d-204">After</span></span></td>
<td><span data-ttu-id="8344d-205">Lõpp</span><span class="sxs-lookup"><span data-stu-id="8344d-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-206">Lõpp</span><span class="sxs-lookup"><span data-stu-id="8344d-206">End</span></span></td>
<td><span data-ttu-id="8344d-207">Enne</span><span class="sxs-lookup"><span data-stu-id="8344d-207">Before</span></span></td>
<td><span data-ttu-id="8344d-208">Lõpp</span><span class="sxs-lookup"><span data-stu-id="8344d-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8344d-209">Protsessi operatsioon</span><span class="sxs-lookup"><span data-stu-id="8344d-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-210">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="8344d-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="8344d-211">Enne</span><span class="sxs-lookup"><span data-stu-id="8344d-211">Before</span></span></td>
<td><span data-ttu-id="8344d-212">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-213">Konkreetne ID, Grupp või Kõik ja Ressursipõhine, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="8344d-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-214">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="8344d-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-215">Pärast</span><span class="sxs-lookup"><span data-stu-id="8344d-215">After</span></span></td>
<td><span data-ttu-id="8344d-216">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8344d-217">Kaastoote tootmine</span><span class="sxs-lookup"><span data-stu-id="8344d-217">Co-product production</span></span></td>
<td><span data-ttu-id="8344d-218">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="8344d-218">Registration</span></span></td>
<td><span data-ttu-id="8344d-219">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="8344d-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-220">Puudub</span><span class="sxs-lookup"><span data-stu-id="8344d-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="8344d-221">Kõik</span><span class="sxs-lookup"><span data-stu-id="8344d-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8344d-222">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="8344d-222">Report as finished</span></span></td>
<td><span data-ttu-id="8344d-223">Enne</span><span class="sxs-lookup"><span data-stu-id="8344d-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-224">Pärast</span><span class="sxs-lookup"><span data-stu-id="8344d-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8344d-225">Järgmises tabelis on veel teavet kvaliteettellimuste loomise kohta konkreetset tüüpi protsessidele.</span><span class="sxs-lookup"><span data-stu-id="8344d-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="8344d-226">Protsessi tüüp</span><span class="sxs-lookup"><span data-stu-id="8344d-226">Type of process</span></span></th>
<th><span data-ttu-id="8344d-227">Millal saab kvaliteettellimusi automaatselt luua</span><span class="sxs-lookup"><span data-stu-id="8344d-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="8344d-228">Millal saab kvaliteettellimusi luua, kui on vajalik purustav katsetamine</span><span class="sxs-lookup"><span data-stu-id="8344d-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="8344d-229">Tingimuse teave</span><span class="sxs-lookup"><span data-stu-id="8344d-229">Condition information</span></span></th>
<th><span data-ttu-id="8344d-230">Käsitsi loomise teave</span><span class="sxs-lookup"><span data-stu-id="8344d-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="8344d-231">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="8344d-231">Purchase order</span></span></td>
<td><span data-ttu-id="8344d-232">Enne või pärast sissetulekute loendi või vastuvõetava materjali toote sissetuleku sisestamist</span><span class="sxs-lookup"><span data-stu-id="8344d-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="8344d-233">Pärast vastuvõetava materjali toote sissetuleku sisestamist, kuna materjal peab olema kättesaadav purustavaks katsetamiseks</span><span class="sxs-lookup"><span data-stu-id="8344d-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="8344d-234">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="8344d-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8344d-235">Käsitsi loodud ostutellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="8344d-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-236">Vahelao order</span><span class="sxs-lookup"><span data-stu-id="8344d-236">Quarantine order</span></span></td>
<td><span data-ttu-id="8344d-237">Enne või pärast vahelao tellimuse lõpetatuna kinnitamist või lõpetamist</span><span class="sxs-lookup"><span data-stu-id="8344d-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="8344d-238">Purustavaid katseid nõudvaid kvaliteettellimusi ei saa koostada.</span><span class="sxs-lookup"><span data-stu-id="8344d-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="8344d-239">Eeldatakse, et vahelao tellimuse funktsioon tegeleb rikutud materjali likvideerimisega.</span><span class="sxs-lookup"><span data-stu-id="8344d-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="8344d-240">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="8344d-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8344d-241">Käsitsi loodud vahelaoorderile viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="8344d-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-242">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="8344d-242">Sales order</span></span></td>
<td><span data-ttu-id="8344d-243">Enne plaanitud komplekteerimisprotsessi või saatelehe uuendamist lähetatavate kaupade puhul</span><span class="sxs-lookup"><span data-stu-id="8344d-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="8344d-244">Igas etapis</span><span class="sxs-lookup"><span data-stu-id="8344d-244">At any step</span></span></td>
<td><span data-ttu-id="8344d-245">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või klienti või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="8344d-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8344d-246">Käsitsi loodud müügitellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="8344d-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-247">Tootmistellimus</span><span class="sxs-lookup"><span data-stu-id="8344d-247">Production order</span></span></td>
<td><span data-ttu-id="8344d-248">Enne või pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="8344d-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="8344d-249">Pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="8344d-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="8344d-250">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala või kaupa või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="8344d-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8344d-251">Käsitsi loodud tootmistellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="8344d-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-252">Tootmistellimus, millel on protsessitoiming</span><span class="sxs-lookup"><span data-stu-id="8344d-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="8344d-253">Enne või pärast toimingu aruande lõpetamist</span><span class="sxs-lookup"><span data-stu-id="8344d-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="8344d-254">Pärast viimase toimingu tootmise lõpetamisest teatamist</span><span class="sxs-lookup"><span data-stu-id="8344d-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="8344d-255">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või operatsiooniressurssi või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="8344d-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="8344d-256">Käsitsi loodud protsessitoimingule viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="8344d-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8344d-257">Varud</span><span class="sxs-lookup"><span data-stu-id="8344d-257">Inventory</span></span></td>
<td><span data-ttu-id="8344d-258">Kvaliteettellimust ei saa automaatselt koostada varude töölehe kandele või üleviimistellimuse kandele.</span><span class="sxs-lookup"><span data-stu-id="8344d-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="8344d-259">Kvaliteettellimus tuleb kauba laokogusele käsitsi koostada.</span><span class="sxs-lookup"><span data-stu-id="8344d-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="8344d-260">Nõutav on füüsiline vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="8344d-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="8344d-261">Kvaliteettellimuse automaatse loomise näited</span><span class="sxs-lookup"><span data-stu-id="8344d-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="8344d-262">Ostmine</span><span class="sxs-lookup"><span data-stu-id="8344d-262">Purchasing</span></span>

<span data-ttu-id="8344d-263">Kui määrate ostmisel välja **Sündmuse tüüp** väärtuseks **Toote sissetulek** ja välja **Käivitamine** väärtuseks **Pärast** lehel **Kvaliteediseosed**, saate järgmised tulemused:</span><span class="sxs-lookup"><span data-stu-id="8344d-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="8344d-264">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Jah**, luuakse iga sissetuleku kohta kvaliteettellimus ostutellimuse suhtes, võttes aluseks sissetulnud koguse ja kauba valimi sätted.</span><span class="sxs-lookup"><span data-stu-id="8344d-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="8344d-265">Iga kord, kui ostutellimuse vastu on saadud kogus, luuakse äsja vastuvõetud koguse põhjal uued kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="8344d-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="8344d-266">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Ei**, luuakse sissetulnud koguse põhjal esimese sissetuleku kohta kvaliteettellimus ostutellimuse suhtes.</span><span class="sxs-lookup"><span data-stu-id="8344d-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="8344d-267">Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt jälgimisdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="8344d-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="8344d-268">Kvaliteettellimusi ei looda järgnevate sissetulekute kohta ostutellimuse suhtes.</span><span class="sxs-lookup"><span data-stu-id="8344d-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="8344d-269">Kvaliteedi spetsifikatsioon</span><span class="sxs-lookup"><span data-stu-id="8344d-269">Quality specification</span></span></th>
<th><span data-ttu-id="8344d-270">Värskendatud koguse kohta</span><span class="sxs-lookup"><span data-stu-id="8344d-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="8344d-271">Jälgimisdimensiooni kohta</span><span class="sxs-lookup"><span data-stu-id="8344d-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="8344d-272">Tulemus</span><span class="sxs-lookup"><span data-stu-id="8344d-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="8344d-273">Protsent: 10%</span><span class="sxs-lookup"><span data-stu-id="8344d-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="8344d-274">Jah</span><span class="sxs-lookup"><span data-stu-id="8344d-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="8344d-275">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="8344d-275">Batch number: No</span></span></p>
<p><span data-ttu-id="8344d-276">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="8344d-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="8344d-277">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="8344d-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="8344d-278">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="8344d-279">Kvaliteettellimus #1 3 kohta (10% 30-st)</span><span class="sxs-lookup"><span data-stu-id="8344d-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-280">Teata 70 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="8344d-281">Kvaliteettellimus #2 7 kohta (10% järelejäänud tellimuse kogusest, mis võrdub sel juhul 70-ga)</span><span class="sxs-lookup"><span data-stu-id="8344d-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="8344d-282">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="8344d-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="8344d-283">Ei</span><span class="sxs-lookup"><span data-stu-id="8344d-283">No</span></span></td>
<td>
<p><span data-ttu-id="8344d-284">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="8344d-284">Batch number: No</span></span></p>
<p><span data-ttu-id="8344d-285">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="8344d-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="8344d-286">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="8344d-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="8344d-287">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="8344d-288">Kavaliteettellimus #1 luuakse 1 kohta (esimese lõpetatuna kinnitatud koguse jaoks, millel on fikseeritud väärtus 1).</span><span class="sxs-lookup"><span data-stu-id="8344d-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="8344d-289">Järelejäänud koguse kohta ei looda enam ühtegi kvaliteettellimust.</span><span class="sxs-lookup"><span data-stu-id="8344d-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-290">Teata 10 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="8344d-291">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="8344d-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-292">Teata 60 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="8344d-293">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="8344d-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="8344d-294">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="8344d-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="8344d-295">Jah</span><span class="sxs-lookup"><span data-stu-id="8344d-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="8344d-296">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="8344d-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="8344d-297">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="8344d-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="8344d-298">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="8344d-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="8344d-299">Teata 3 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="8344d-300">Kvaliteettellimus #1 1 kohta partiist #b1, seerianumber #s1</span><span class="sxs-lookup"><span data-stu-id="8344d-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="8344d-301">Kvaliteettellimus #2 1 kohta partiist #b2, seerianumber #s2</span><span class="sxs-lookup"><span data-stu-id="8344d-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="8344d-302">Kvaliteettellimus #3 1 kohta partiist #b3, seerianumber #s3</span><span class="sxs-lookup"><span data-stu-id="8344d-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-303">Teata 2 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="8344d-304">Kvaliteettellimus #4 1 kohta partiist #b4, seerianumber #s4</span><span class="sxs-lookup"><span data-stu-id="8344d-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="8344d-305">Kvaliteettellimus #5 1 kohta partiist #b5, seerianumber #s5</span><span class="sxs-lookup"><span data-stu-id="8344d-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="8344d-306"><strong>Märkus.</strong> Partiid saab uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="8344d-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="8344d-307">Fikseeritud kogus: 2</span><span class="sxs-lookup"><span data-stu-id="8344d-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="8344d-308">Ei</span><span class="sxs-lookup"><span data-stu-id="8344d-308">No</span></span></td>
<td>
<p><span data-ttu-id="8344d-309">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="8344d-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="8344d-310">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="8344d-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="8344d-311">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="8344d-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="8344d-312">Teata 4 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="8344d-313">Kvaliteettellimus #1 1 kohta partiist #b1, seerianumber #s1.</span><span class="sxs-lookup"><span data-stu-id="8344d-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="8344d-314">Kvaliteettellimus #2 1 kohta partiist #b2, seerianumber #s2.</span><span class="sxs-lookup"><span data-stu-id="8344d-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="8344d-315">Kvaliteettellimus #3 1 kohta partiist #b3, seerianumber #s3.</span><span class="sxs-lookup"><span data-stu-id="8344d-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="8344d-316">Kvaliteettellimus #4 1 kohta partiist #b4, seerianumber #s4.</span><span class="sxs-lookup"><span data-stu-id="8344d-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="8344d-317">Järelejäänud koguse kohta ei looda enam ühtegi kvaliteettellimust.</span><span class="sxs-lookup"><span data-stu-id="8344d-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-318">Teata 6 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="8344d-319">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="8344d-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="8344d-320">Tootmine</span><span class="sxs-lookup"><span data-stu-id="8344d-320">Production</span></span>

<span data-ttu-id="8344d-321">Kui määrate tootmisel välja **Sündmuse tüüp** väärtuseks **Lõpetamise kinnitamine** ja välja **Käivitamine** väärtuseks **Pärast** lehel **Kvaliteediseosed**, saate järgmised tulemused:</span><span class="sxs-lookup"><span data-stu-id="8344d-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="8344d-322">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Jah**, luuakse kvaliteettellimus iga lõpetatud koguse ja kauba valimi sätete alusel.</span><span class="sxs-lookup"><span data-stu-id="8344d-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="8344d-323">Iga kord, kui kogus märgitakse tootmistellimuse suhtes lõpetatuks, luuakse äsja lõpetatud koguse põhjal uued kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="8344d-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="8344d-324">See loomisloogika on kooskõlas ostuga.</span><span class="sxs-lookup"><span data-stu-id="8344d-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="8344d-325">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Ei**, luuakse lõpetatud koguse põhjal kvaliteettellimus esimesel korral, kui kogus kinnitatakse lõpetatuks.</span><span class="sxs-lookup"><span data-stu-id="8344d-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="8344d-326">Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt kauba valimi jälgimisdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="8344d-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="8344d-327">Hilisemate lõpetatud koguste kohta ei looda kvaliteettellimusi.</span><span class="sxs-lookup"><span data-stu-id="8344d-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="8344d-328">Kvaliteedi spetsifikatsioon</span><span class="sxs-lookup"><span data-stu-id="8344d-328">Quality specification</span></span></th>
<th><span data-ttu-id="8344d-329">Värskendatud koguse kohta</span><span class="sxs-lookup"><span data-stu-id="8344d-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="8344d-330">Jälgimisdimensiooni kohta</span><span class="sxs-lookup"><span data-stu-id="8344d-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="8344d-331">Tulemus</span><span class="sxs-lookup"><span data-stu-id="8344d-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="8344d-332">Protsent: 10%</span><span class="sxs-lookup"><span data-stu-id="8344d-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="8344d-333">Jah</span><span class="sxs-lookup"><span data-stu-id="8344d-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="8344d-334">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="8344d-334">Batch number: No</span></span></p>
<p><span data-ttu-id="8344d-335">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="8344d-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="8344d-336">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="8344d-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="8344d-337">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="8344d-338">Kvaliteettellimus #1 3 kohta (10% 30-st)</span><span class="sxs-lookup"><span data-stu-id="8344d-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-339">Teata 70 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="8344d-340">Kvaliteettellimus #2 7 kohta (10% järelejäänud tellimuse kogusest, mis võrdub sel juhul 70-ga)</span><span class="sxs-lookup"><span data-stu-id="8344d-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="8344d-341">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="8344d-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="8344d-342">Ei</span><span class="sxs-lookup"><span data-stu-id="8344d-342">No</span></span></td>
<td>
<p><span data-ttu-id="8344d-343">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="8344d-343">Batch number: No</span></span></p>
<p><span data-ttu-id="8344d-344">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="8344d-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="8344d-345">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="8344d-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="8344d-346">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="8344d-347">Kavaliteettellimus #1 luuakse 1 kohta (esimese lõpetatuna kinnitatud koguse jaoks, millel on fikseeritud väärtus 1)</span><span class="sxs-lookup"><span data-stu-id="8344d-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="8344d-348">Kavaliteettellimus #2 luuakse 1 kohta (järelejäänud koguse jaoks, millel on ikka fikseeritud väärtus 1)</span><span class="sxs-lookup"><span data-stu-id="8344d-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-349">Teata 10 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="8344d-350">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="8344d-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-351">Teata 60 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="8344d-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="8344d-352">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="8344d-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="8344d-353">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="8344d-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="8344d-354">Jah</span><span class="sxs-lookup"><span data-stu-id="8344d-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="8344d-355">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="8344d-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="8344d-356">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="8344d-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="8344d-357">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="8344d-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="8344d-358">Kinnita lõpetatuks 3 kohta: 1 #b1, #s1 kohta; 1 #b2, #s2 kohta ja 1 #b3, #s3 kohta</span><span class="sxs-lookup"><span data-stu-id="8344d-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="8344d-359">Kvaliteettellimus #1 1 kohta partiist #b1, seerianumber #s1</span><span class="sxs-lookup"><span data-stu-id="8344d-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="8344d-360">Kvaliteettellimus #2 1 kohta partiist #b2, seerianumber #s2</span><span class="sxs-lookup"><span data-stu-id="8344d-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="8344d-361">Kvaliteettellimus #3 1 kohta partiist #b3, seerianumber #s3</span><span class="sxs-lookup"><span data-stu-id="8344d-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-362">Kinnita lõpetatuks 2 kohta: 1 #b4, #s4 kohta ja 1 #b5, #s5 kohta</span><span class="sxs-lookup"><span data-stu-id="8344d-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="8344d-363">Kvaliteettellimus #4 1 kohta partiist #b4, seerianumber #s4</span><span class="sxs-lookup"><span data-stu-id="8344d-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="8344d-364">Kvaliteettellimus #5 1 kohta partiist #b5, seerianumber #s5</span><span class="sxs-lookup"><span data-stu-id="8344d-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="8344d-365"><strong>Märkus.</strong> Partiid saab uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="8344d-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="8344d-366">Fikseeritud kogus: 2</span><span class="sxs-lookup"><span data-stu-id="8344d-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="8344d-367">Ei</span><span class="sxs-lookup"><span data-stu-id="8344d-367">No</span></span></td>
<td>
<p><span data-ttu-id="8344d-368">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="8344d-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="8344d-369">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="8344d-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="8344d-370">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="8344d-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="8344d-371">Kinnita lõpetatuks 4 kohta: 1 #b1, #s1 kohta; 1 #b2, #s2 kohta; 1 #b3, #s3 kohta ja 1 #b4, #s4 kohta</span><span class="sxs-lookup"><span data-stu-id="8344d-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="8344d-372">Kvaliteettellimus #1 1 kohta partiist #b1, seerianumber #s1</span><span class="sxs-lookup"><span data-stu-id="8344d-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="8344d-373">Kvaliteettellimus #2 1 kohta partiist #b2, seerianumber #s2</span><span class="sxs-lookup"><span data-stu-id="8344d-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="8344d-374">Kvaliteettellimus #3 1 kohta partiist #b3, seerianumber #s3</span><span class="sxs-lookup"><span data-stu-id="8344d-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="8344d-375">Kvaliteettellimus #4 1 kohta partiist #b4, seerianumber #s4</span><span class="sxs-lookup"><span data-stu-id="8344d-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="8344d-376">Kvaliteettellimus #5 2 kohta,ilma viiteta partiile ja seerianumbrile</span><span class="sxs-lookup"><span data-stu-id="8344d-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="8344d-377">Kinnita lõpetatuks 6 kohta: 1 #b5, #s5 kohta; 1 #b6, #s6 kohta; 1 #b7, #s7 kohta; 1 #b8, #s8 kohta; 1 #b9, #s9 kohta ja 1 #b10, #s10 kohta</span><span class="sxs-lookup"><span data-stu-id="8344d-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="8344d-378">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="8344d-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="8344d-379">Kvaliteedijuhtimise lehed</span><span class="sxs-lookup"><span data-stu-id="8344d-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8344d-380">Leht</span><span class="sxs-lookup"><span data-stu-id="8344d-380">Page</span></span></th>
<th><span data-ttu-id="8344d-381">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8344d-381">Description</span></span></th>
<th><span data-ttu-id="8344d-382">Näide</span><span class="sxs-lookup"><span data-stu-id="8344d-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8344d-383">Kvaliteediseosed</span><span class="sxs-lookup"><span data-stu-id="8344d-383">Quality associations</span></span></td>
<td><span data-ttu-id="8344d-384">Vt selle artikli varasemaid jaotisi.</span><span class="sxs-lookup"><span data-stu-id="8344d-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="8344d-385">Kvaliteediseos määratleb koostatava kvaliteettellimuse puhul kogu järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="8344d-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="8344d-386">Kande sündmus</span><span class="sxs-lookup"><span data-stu-id="8344d-386">The transaction event</span></span></li>
<li><span data-ttu-id="8344d-387">Kaupade puhul tehtavate katsete kogum</span><span class="sxs-lookup"><span data-stu-id="8344d-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="8344d-388">AQL</span><span class="sxs-lookup"><span data-stu-id="8344d-388">The AQL</span></span></li>
<li><span data-ttu-id="8344d-389">Valimi plaan</span><span class="sxs-lookup"><span data-stu-id="8344d-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="8344d-390">Kvaliteediseos tuleb automaatset kvaliteettellimuse genereerimist nõudvas äriprotsessis määrata iga variatsiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="8344d-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="8344d-391">Näiteks saab kvaliteettellimuse koostada ostutellimuste, vahelaotellimuste, müügitellimuste ja tootmistellimuste äriprotsessides.</span><span class="sxs-lookup"><span data-stu-id="8344d-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8344d-392">Katsed</span><span class="sxs-lookup"><span data-stu-id="8344d-392">Tests</span></span></td>
<td><span data-ttu-id="8344d-393">Määrake ja vaadake selle lehe abil üksikuid katseid, mis määratlevad, kas teie tooted vastavad kvaliteedispetsifikatsioonidele või mitte.</span><span class="sxs-lookup"><span data-stu-id="8344d-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="8344d-394">Saate määrata katsegrupile vähemalt ühe eraldi katse.</span><span class="sxs-lookup"><span data-stu-id="8344d-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="8344d-395">Sellisel juhul määrate ka testipõhised andmed, nt vastuvõetavad mõõtmisväärtused.</span><span class="sxs-lookup"><span data-stu-id="8344d-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="8344d-396">Mõõtmisväärtusi kasutatakse kvantitatiivsete katsete puhul ja katsemuutujaid kasutatakse kvalitatiivsete katsete puhul.</span><span class="sxs-lookup"><span data-stu-id="8344d-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="8344d-397">Kvantitatiivse katse tüüp on <strong>täisarv</strong> või <strong>murd</strong> ja sellele on määratud ka mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="8344d-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="8344d-398">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse numbritena.</span><span class="sxs-lookup"><span data-stu-id="8344d-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="8344d-399">Kvalitatiivse katse tüüp on <strong>valik</strong>.</span><span class="sxs-lookup"><span data-stu-id="8344d-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="8344d-400">Kvalitatiivsed katsed nõuavad lisateavet mõõdetava katsemuutuja ja selle loetletud valikute kohta.</span><span class="sxs-lookup"><span data-stu-id="8344d-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="8344d-401">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse tulemuse järgi.</span><span class="sxs-lookup"><span data-stu-id="8344d-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="8344d-402">Tootjaettevõte sooritab kaks katset ostetud materjaliga: kvantitatiivse katse materjali kvaliteedi kohta ja kvalitatiivne katse pakendikahjustuse kohta.</span><span class="sxs-lookup"><span data-stu-id="8344d-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="8344d-403">Ettevõte määrab lisateabe kvalitatiivse katse kohta, et määratleda katse muutuja (kahjustatud pakend) ja selle tulemused.</span><span class="sxs-lookup"><span data-stu-id="8344d-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="8344d-404">Ettevõte kasutab lehte <strong>Katsegrupid</strong>, et määrata katsegrupile kaks katset ning määrata katsepõhine teave.</span><span class="sxs-lookup"><span data-stu-id="8344d-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="8344d-405">Katsegrupp määratakse kvaliteeditellimusele, nii et ettevõte saab teavitada kahe katse katsetulemustest.</span><span class="sxs-lookup"><span data-stu-id="8344d-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8344d-406">Katsegrupid</span><span class="sxs-lookup"><span data-stu-id="8344d-406">Test groups</span></span></td>
<td><span data-ttu-id="8344d-407">Kasutage antud lehte katsegruppide ja katsegrupile määratud eraldi katsete seadistamiseks, redigeerimiseks ning vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="8344d-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="8344d-408">Ülemine paan kuvab katsegruppe ja alumine paan kuvab valitud katsegruppi määratud katseid.</span><span class="sxs-lookup"><span data-stu-id="8344d-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="8344d-409">Saate määrata katsegrupile mitmed põhimõtted nagu valimiplaani, vastuvõetava kvaliteeditaseme (AQL) ja nõuded purustavale katsetamisele.</span><span class="sxs-lookup"><span data-stu-id="8344d-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="8344d-410">Kui määrate katsegrupile eraldi katse, määratlete lisateabe, näiteks järjestuse, dokumendid ja kehtivuse kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="8344d-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="8344d-411">Kvantitatiivse katse puhul sisaldab teie määratletud teave ka vastuvõetavaid mõõtmisväärtusi.</span><span class="sxs-lookup"><span data-stu-id="8344d-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="8344d-412">Kvalitatiivse katse puhul sisaldab teave katsemuutujat ja vaiketulemust.</span><span class="sxs-lookup"><span data-stu-id="8344d-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="8344d-413">Kvaliteettellimusele määratud katsegrupp määratleb katsete vaikekogumi, mis tuleb määratud kaubaga sooritada.</span><span class="sxs-lookup"><span data-stu-id="8344d-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="8344d-414">Kuid saate kvaliteettellimuse katseid lisada, kustutada või muuta.</span><span class="sxs-lookup"><span data-stu-id="8344d-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="8344d-415">Iga katse tulemused kinnitatakse kvaliteettellimuses.</span><span class="sxs-lookup"><span data-stu-id="8344d-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="8344d-416">Tootmisettevõte määrab iga kvaliteetjuhise variandi puhul katsegrupi.</span><span class="sxs-lookup"><span data-stu-id="8344d-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="8344d-417">Erinevad katsegrupid näitavad erinevusi valimiplaanides, katsehulkasid, mida peab koos läbi viima, vastuvõetavat kvaliteeditaset ja muid tegureid.</span><span class="sxs-lookup"><span data-stu-id="8344d-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="8344d-418">Kvantitatiivsete katsete puhul on erinevused ka vastuvõetavates mõõteväärtustes.</span><span class="sxs-lookup"><span data-stu-id="8344d-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="8344d-419">Kvaliteedipõhimõtteid järgides määrab ettevõte igale reeglile katsegrupi, et koostada automaatselt kvaliteettellimusi lehel <strong>Kvaliteediseosed</strong>, ja määrab katsegrupi ka käsitsi loodud kvaliteettellimustele.</span><span class="sxs-lookup"><span data-stu-id="8344d-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8344d-420">Üksuse kvaliteedigrupid</span><span class="sxs-lookup"><span data-stu-id="8344d-420">Item quality groups</span></span></td>
<td><span data-ttu-id="8344d-421">Kasutage seda lehte, et seadistada, redigeerida ja vaadata kaupu, mis on määratud kaubale määratud kvaliteedigrupile või kvaliteedigruppidele.</span><span class="sxs-lookup"><span data-stu-id="8344d-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="8344d-422">Kvaliteedigrupp tähistab kaupade üldisi testimisnõudeid.</span><span class="sxs-lookup"><span data-stu-id="8344d-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="8344d-423">Pärast katsenõuete määratlemist lehel <strong>Katsegrupid</strong> saate määratleda reeglid kvaliteettellimuste automaatseks koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="8344d-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="8344d-424">Protsessi hõlbustamiseks ei määratleta reegleid üksikutele kaupadele.</span><span class="sxs-lookup"><span data-stu-id="8344d-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="8344d-425">Selle asemel määratletakse reeglid kvaliteedigrupile, kasutades lehte <strong>Kvaliteediseosed</strong>.</span><span class="sxs-lookup"><span data-stu-id="8344d-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="8344d-426">Saate kasutada valitud kvaliteedigrupi puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kaupade määramiseks sellesse gruppi.</span><span class="sxs-lookup"><span data-stu-id="8344d-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="8344d-427">Saate kasutada valitud kauba puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kvaliteedigruppide määramiseks sellele kaubale.</span><span class="sxs-lookup"><span data-stu-id="8344d-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="8344d-428">Tootmisettevõte ostab mitmesuguseid ühesuguste sissetulekukontrolli katsenõuetega toormaterjale.</span><span class="sxs-lookup"><span data-stu-id="8344d-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="8344d-429">Ettevõte määrab kvaliteedigrupi ja määrab sellele grupile toormaterjaliga seotud kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="8344d-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="8344d-430">Hiljem ostab ettevõte uut tüüpi toormaterjali, millel on samad katsenõuded.</span><span class="sxs-lookup"><span data-stu-id="8344d-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="8344d-431">Selle asemel, et seadistada uuele materjalile uued katsenõuded, lisab ettevõte uue materjali kaubakoodi olemasolevasse kvaliteedigruppi.</span><span class="sxs-lookup"><span data-stu-id="8344d-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="8344d-432">Sama tootmisettevõte toodab ka ühesuguste tootmisalaste katsenõuetega kaupu ja lähetab ühesuguste nõuetega kaubad lähetuseelsete katsete tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="8344d-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="8344d-433">Ettevõte määrab kaks täiendavat kvaliteedigruppi ja määrab seejärel igale grupile sobivad kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="8344d-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8344d-434">Katse muutujad</span><span class="sxs-lookup"><span data-stu-id="8344d-434">Test variables</span></span></td>
<td><span data-ttu-id="8344d-435">Sellel lehel saate määratleda ja kuvada kvalitatiivse katsega seotud muutujaid.</span><span class="sxs-lookup"><span data-stu-id="8344d-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="8344d-436">Iga muutuja puhul saab määratleda nummerdatud tulemused, mis kajastavad võimalikke valikuid.</span><span class="sxs-lookup"><span data-stu-id="8344d-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="8344d-437">Saate määratleda katsed lehel <strong>Katsed</strong>.</span><span class="sxs-lookup"><span data-stu-id="8344d-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="8344d-438">Kvalitatiivsete katsete puhul peate määrama katsetüübi <strong>Valik</strong>.</span><span class="sxs-lookup"><span data-stu-id="8344d-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="8344d-439">Kasutage lehte <strong>Katsegrupid</strong> katse muutuja määramiseks individuaalsele katsele.</span><span class="sxs-lookup"><span data-stu-id="8344d-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="8344d-440">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="8344d-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="8344d-441">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="8344d-441">This inspection test has several variables.</span></span> <span data-ttu-id="8344d-442">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="8344d-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="8344d-443">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="8344d-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8344d-444">Katse muutuja väljundteated</span><span class="sxs-lookup"><span data-stu-id="8344d-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="8344d-445">Kasutage seda lehte kvalitatiivse katsega seotud muutuja võimalike katsetulemuste seadistamiseks, redigeerimiseks ja vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="8344d-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="8344d-446">Iga tulemuse puhul tuleb määrata olek <strong>läbis</strong> või <strong>ei läbinud</strong>.</span><span class="sxs-lookup"><span data-stu-id="8344d-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="8344d-447">Peate määrama muutuja ja tema väljundid iga kvalitatiivse katse jaoks, mis on määratud lehel <strong>Katsed</strong>.</span><span class="sxs-lookup"><span data-stu-id="8344d-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="8344d-448">(Kvalitatiivsete katsete puhul on katse tüübiks määratud <strong>Valik</strong> lehel <strong>Katsed</strong>.) Kasutage lehte <strong>Katsegrupid</strong> katsemuutuja ja vaikeväärtuse määramiseks kindlale kvalitatiivsele katsele.</span><span class="sxs-lookup"><span data-stu-id="8344d-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="8344d-449">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="8344d-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="8344d-450">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="8344d-450">This inspection test has of several variables.</span></span> <span data-ttu-id="8344d-451">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="8344d-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="8344d-452">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="8344d-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="8344d-453">Igale tulemusele omistatakse väärtus <strong>läbis</strong> või <strong>ei läbinud</strong>.</span><span class="sxs-lookup"><span data-stu-id="8344d-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="8344d-454">Iga muutuja kontrolltesti ajal registreerib katsetaja katse tulemuse, valides ühe väljundi väärtustest.</span><span class="sxs-lookup"><span data-stu-id="8344d-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="8344d-455">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8344d-455">Additional resources</span></span>
--------

[<span data-ttu-id="8344d-456">Kvaliteedijuhtimise protsessid</span><span class="sxs-lookup"><span data-stu-id="8344d-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="8344d-457">Mittevastavuse haldus</span><span class="sxs-lookup"><span data-stu-id="8344d-457">Nonconformance management</span></span>](enable-nonconformance-management.md)
