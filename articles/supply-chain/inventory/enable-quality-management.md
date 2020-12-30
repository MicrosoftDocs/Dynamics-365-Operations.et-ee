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
ms.openlocfilehash: e1d7828e6bb9a3684c1d76e2cfac96174a8dfbf4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426330"
---
# <a name="quality-management-overview"></a><span data-ttu-id="919cb-103">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="919cb-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="919cb-104">Selles teemas kirjeldatakse, kuidas kasutada rakenduses Dynamics 365 Supply Chain Management kvaliteedijuhtimist, et täiustada tarneahela toote kvaliteeti.</span><span class="sxs-lookup"><span data-stu-id="919cb-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="919cb-105">Kvaliteedijuhtimise abil saate hallata ümberpööramise aegu, kui käsitsete mittevastavaid tooteid, olenemata nende päritolukohast.</span><span class="sxs-lookup"><span data-stu-id="919cb-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="919cb-106">Kuna diagnostikatüübid on seotud parandustest teatamisega, saab Supply Chain Management plaanida ülesandeid probleemide kõrvaldamiseks ja nende kordumise vältimiseks.</span><span class="sxs-lookup"><span data-stu-id="919cb-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="919cb-107">Lisaks mittevastavuste haldamiseks mõeldud funktsioonidele hõlmab kvaliteedijuhtimine funktsioone probleemide jälgimiseks probleemi tüübi alusel (isegi sisemiste probleemide puhul) ja lühiajaliste või pikaajaliste lahenduste tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="919cb-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="919cb-108">Tulemuslikkuse võtmenäitajate (KPI) statistika annab ülevaate varasematest mittevastavuse probleemidest ja nende kõrvaldamiseks kasutatud lahendustest.</span><span class="sxs-lookup"><span data-stu-id="919cb-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="919cb-109">Saate kasutada varasemaid andmeid eelmiste kvaliteedimeetmete tulemuslikkuse ülevaatamiseks ja sobivate tulevikus kasutatavate meetmete määramiseks.</span><span class="sxs-lookup"><span data-stu-id="919cb-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="919cb-110">Kvaliteediseose seadistamisel saab Supply Chain Management koostada kvaliteettellimusi mitmesugustele äriprotsessidele, sündmustele ja tingimustele.</span><span class="sxs-lookup"><span data-stu-id="919cb-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="919cb-111">Kvaliteediseos võib hõlmata konkreetset kaupa, konkreetset kaubagruppi või kõiki kaupu.</span><span class="sxs-lookup"><span data-stu-id="919cb-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="919cb-112">Kvaliteedijuhtimise kasutamise näited</span><span class="sxs-lookup"><span data-stu-id="919cb-112">Examples of the use of quality management</span></span>
<span data-ttu-id="919cb-113">Kvaliteedijuhtimine on paindlik ja seda saab rakendada mitmesugusel moel, et järgida konkreetsete tarneahela toimingute tasemete nõudeid.</span><span class="sxs-lookup"><span data-stu-id="919cb-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="919cb-114">Järgmised näited illustreerivad nende funktsioonide võimalikke kasutusviise.</span><span class="sxs-lookup"><span data-stu-id="919cb-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="919cb-115">Saate kvaliteedikontrolli protsessi automaatselt käivitada, tuginedes eelnevalt määratletud kriteeriumidele (konkreetse hankija ostutellimuse registreerimisel laos).</span><span class="sxs-lookup"><span data-stu-id="919cb-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="919cb-116">Kontrollimise ajal varude blokeerimine, et vältida heakskiitmata varude kasutamist (ostutellimuse koguste täielik blokeerimine).</span><span class="sxs-lookup"><span data-stu-id="919cb-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="919cb-117">Saate kasutada kauba valimit kvaliteediseose osana jooksvate füüsiliste varude hulga määratlemiseks, mida kontrollida tuleb.</span><span class="sxs-lookup"><span data-stu-id="919cb-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="919cb-118">Valimi aluseks võib olla fikseeritud kogus, protsent või kogu litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="919cb-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="919cb-119">Funktsioon _Kvaliteedijuhtimine laoprotsesside jaoks_ laiendab kvaliteedijuhtimise võimalusi.</span><span class="sxs-lookup"><span data-stu-id="919cb-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="919cb-120">Kui kasutate seda funktsiooni, leiate jaotisest [Kvaliteedijuhtimine laoprotsesside jaoks](quality-management-for-warehouses-processes.md) näiteid selle kohta, kuidas kvaliteedijuhtimine lubamise korral töötab.</span><span class="sxs-lookup"><span data-stu-id="919cb-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="919cb-121">Looge kvaliteettellimused osaliste tarnete jaoks.</span><span class="sxs-lookup"><span data-stu-id="919cb-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="919cb-122">Kvaliteettellimuse loomiseks, mis põhineb tellimusega füüsiliselt saadud kogusel, peate märkima ruudu **Värskendatud koguse kohta** vormil **Kauba valim**.</span><span class="sxs-lookup"><span data-stu-id="919cb-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="919cb-123">Saate luua katsetüüpe, mis sisaldavad katse minimaalset, maksimaalset ja sihtväärtust ning teha kvalitatiivset vs kvantitatiivset kontrolli, millel on eelnevalt määratud valideerimistulemused.</span><span class="sxs-lookup"><span data-stu-id="919cb-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="919cb-124">Määrake sobiv kvaliteeditase (AQL) kvaliteedimeetme hälvete kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="919cb-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="919cb-125">Saate määrata ressursid, mida kontrollimistoiming nõuab, nt katsepiirkond ja katseinstrumendid.</span><span class="sxs-lookup"><span data-stu-id="919cb-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="919cb-126">Kvaliteediseostega töötamine</span><span class="sxs-lookup"><span data-stu-id="919cb-126">Working with quality associations</span></span>
<span data-ttu-id="919cb-127">Kvaliteediseost kasutav äriprotsess võib olla seotud mitmesuguste lähtedokumentidega, nt ostutellimuste, müügitellimuste või tootmistellimustega.</span><span class="sxs-lookup"><span data-stu-id="919cb-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="919cb-128">Iga kvaliteediseose kirje määrab ka katsete kogumi, AQL-i ning valikukava, mida rakendatakse loodud kvaliteettellimustele.</span><span class="sxs-lookup"><span data-stu-id="919cb-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="919cb-129">Peate iga äriprotsessi variatsiooni jaoks määratlema kvaliteediseose kirje.</span><span class="sxs-lookup"><span data-stu-id="919cb-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="919cb-130">Näiteks saate seadistada kvaliteediseose, mis koostab kvaliteettellimuse, kui ostutellimuse toote sissetulekut värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="919cb-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="919cb-131">Olenevalt käivitamisplaani seadistusest saab käivitusprotsessi enese blokeerida, kui on olemas avatud kvaliteettellimus, või saab blokeerida järgmised protsessid, nt ostutellimuse eest arve esitamise.</span><span class="sxs-lookup"><span data-stu-id="919cb-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="919cb-132">**Märkus.** avatud kvaliteettellimuste olemasolu korral blokeeritakse automaatselt varude koguste väljastamine.</span><span class="sxs-lookup"><span data-stu-id="919cb-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="919cb-133">Olenevalt valiku **Täielik blokeerimine** seadistusest lehel **Kaubaproovid** on kogus kas kvaliteettellimusel olev kogus või lähtedokumendi real olev kogus.</span><span class="sxs-lookup"><span data-stu-id="919cb-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="919cb-134">Nimetatud äriprotsessi puhul määratleb kvaliteediseose kirje sündmuse ja tingimused, mille jaoks kvaliteettellimus on loodud.</span><span class="sxs-lookup"><span data-stu-id="919cb-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="919cb-135">Tingimused võivad olla asukoha või juriidilise isiku põhised.</span><span class="sxs-lookup"><span data-stu-id="919cb-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="919cb-136">Purustavaid katseid hõlmavat kvaliteettellimust saab luua ainult siis, kui sündmusel on olemas vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="919cb-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="919cb-137">Järgmistes näidetes on näha, kuidas kvaliteediseose kirjet määratakse iga äriprotsessi variatsioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="919cb-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="919cb-138">Iga näite puhul võetakse järgmises tabelis kokku sündmused ja tingimused, mis on kvaliteediseose kirjega määratletud.</span><span class="sxs-lookup"><span data-stu-id="919cb-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="919cb-139">Viite tüüp</span><span class="sxs-lookup"><span data-stu-id="919cb-139">Reference type</span></span></th>
<th><span data-ttu-id="919cb-140">Sündmuse tüüp</span><span class="sxs-lookup"><span data-stu-id="919cb-140">Event type</span></span></th>
<th><span data-ttu-id="919cb-141">Käivitamine</span><span class="sxs-lookup"><span data-stu-id="919cb-141">Execution</span></span></th>
<th><span data-ttu-id="919cb-142">Sündmuse blokeerimine</span><span class="sxs-lookup"><span data-stu-id="919cb-142">Event blocking</span></span></th>
<th><span data-ttu-id="919cb-143">Dokumendi viide</span><span class="sxs-lookup"><span data-stu-id="919cb-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="919cb-144">Varud</span><span class="sxs-lookup"><span data-stu-id="919cb-144">Inventory</span></span></td>
<td><span data-ttu-id="919cb-145">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="919cb-145">Not applicable</span></span></td>
<td><span data-ttu-id="919cb-146">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="919cb-146">Not applicable</span></span></td>
<td><span data-ttu-id="919cb-147">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-147">None</span></span></td>
<td><span data-ttu-id="919cb-148">Kõik</span><span class="sxs-lookup"><span data-stu-id="919cb-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="919cb-149">Müük</span><span class="sxs-lookup"><span data-stu-id="919cb-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="919cb-150">Komplekteerimise protsess on plaanitud</span><span class="sxs-lookup"><span data-stu-id="919cb-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="919cb-151">Enne</span><span class="sxs-lookup"><span data-stu-id="919cb-151">Before</span></span></td>
<td><span data-ttu-id="919cb-152">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="919cb-153">Ainult Konkreetne ID, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="919cb-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-154">Komplekteerimise protsess</span><span class="sxs-lookup"><span data-stu-id="919cb-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-155">Saateleht</span><span class="sxs-lookup"><span data-stu-id="919cb-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-156">Arve</span><span class="sxs-lookup"><span data-stu-id="919cb-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="919cb-157">Saateleht</span><span class="sxs-lookup"><span data-stu-id="919cb-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-158">Enne</span><span class="sxs-lookup"><span data-stu-id="919cb-158">Before</span></span></td>
<td><span data-ttu-id="919cb-159">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-160">Saateleht</span><span class="sxs-lookup"><span data-stu-id="919cb-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-161">Arve</span><span class="sxs-lookup"><span data-stu-id="919cb-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="919cb-162">Ost</span><span class="sxs-lookup"><span data-stu-id="919cb-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="919cb-163">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="919cb-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="919cb-164">Enne</span><span class="sxs-lookup"><span data-stu-id="919cb-164">Before</span></span></td>
<td><span data-ttu-id="919cb-165">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-166">Sissetulekute loend</span><span class="sxs-lookup"><span data-stu-id="919cb-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-167">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="919cb-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-168">Arve</span><span class="sxs-lookup"><span data-stu-id="919cb-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="919cb-169">Pärast</span><span class="sxs-lookup"><span data-stu-id="919cb-169">After</span></span></td>
<td><span data-ttu-id="919cb-170">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-171">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="919cb-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-172">Arve</span><span class="sxs-lookup"><span data-stu-id="919cb-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="919cb-173">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="919cb-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-174">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="919cb-174">Not applicable</span></span></td>
<td><span data-ttu-id="919cb-175">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-176">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="919cb-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-177">Arve</span><span class="sxs-lookup"><span data-stu-id="919cb-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="919cb-178">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="919cb-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-179">Enne</span><span class="sxs-lookup"><span data-stu-id="919cb-179">Before</span></span></td>
<td><span data-ttu-id="919cb-180">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-181">Toote sissetulek</span><span class="sxs-lookup"><span data-stu-id="919cb-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-182">Arve</span><span class="sxs-lookup"><span data-stu-id="919cb-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="919cb-183">Pärast</span><span class="sxs-lookup"><span data-stu-id="919cb-183">After</span></span></td>
<td><span data-ttu-id="919cb-184">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-185">Arve</span><span class="sxs-lookup"><span data-stu-id="919cb-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="919cb-186">Tootmine</span><span class="sxs-lookup"><span data-stu-id="919cb-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-187">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="919cb-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-188">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="919cb-188">Not applicable</span></span></td>
<td><span data-ttu-id="919cb-189">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="919cb-190">Kõik</span><span class="sxs-lookup"><span data-stu-id="919cb-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-191">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="919cb-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-192">Lõpp</span><span class="sxs-lookup"><span data-stu-id="919cb-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="919cb-193">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="919cb-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-194">Enne</span><span class="sxs-lookup"><span data-stu-id="919cb-194">Before</span></span></td>
<td><span data-ttu-id="919cb-195">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-196">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="919cb-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-197">Lõpp</span><span class="sxs-lookup"><span data-stu-id="919cb-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="919cb-198">Pärast</span><span class="sxs-lookup"><span data-stu-id="919cb-198">After</span></span></td>
<td><span data-ttu-id="919cb-199">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-200">Lõpp</span><span class="sxs-lookup"><span data-stu-id="919cb-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="919cb-201">Vaheladu</span><span class="sxs-lookup"><span data-stu-id="919cb-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-202">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="919cb-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="919cb-203">Enne</span><span class="sxs-lookup"><span data-stu-id="919cb-203">Before</span></span></td>
<td><span data-ttu-id="919cb-204">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="919cb-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-205">Lõpp</span><span class="sxs-lookup"><span data-stu-id="919cb-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-206">Pärast</span><span class="sxs-lookup"><span data-stu-id="919cb-206">After</span></span></td>
<td><span data-ttu-id="919cb-207">Lõpp</span><span class="sxs-lookup"><span data-stu-id="919cb-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-208">Lõpp</span><span class="sxs-lookup"><span data-stu-id="919cb-208">End</span></span></td>
<td><span data-ttu-id="919cb-209">Enne</span><span class="sxs-lookup"><span data-stu-id="919cb-209">Before</span></span></td>
<td><span data-ttu-id="919cb-210">Lõpp</span><span class="sxs-lookup"><span data-stu-id="919cb-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="919cb-211">Protsessi operatsioon</span><span class="sxs-lookup"><span data-stu-id="919cb-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-212">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="919cb-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="919cb-213">Enne</span><span class="sxs-lookup"><span data-stu-id="919cb-213">Before</span></span></td>
<td><span data-ttu-id="919cb-214">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-215">Konkreetne ID, Grupp või Kõik ja Ressursipõhine, Grupp või Kõik</span><span class="sxs-lookup"><span data-stu-id="919cb-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-216">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="919cb-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-217">Pärast</span><span class="sxs-lookup"><span data-stu-id="919cb-217">After</span></span></td>
<td><span data-ttu-id="919cb-218">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="919cb-219">Kaastoote tootmine</span><span class="sxs-lookup"><span data-stu-id="919cb-219">Co-product production</span></span></td>
<td><span data-ttu-id="919cb-220">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="919cb-220">Registration</span></span></td>
<td><span data-ttu-id="919cb-221">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="919cb-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-222">Puudub</span><span class="sxs-lookup"><span data-stu-id="919cb-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="919cb-223">Kõik</span><span class="sxs-lookup"><span data-stu-id="919cb-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="919cb-224">Teata lõpetamisest</span><span class="sxs-lookup"><span data-stu-id="919cb-224">Report as finished</span></span></td>
<td><span data-ttu-id="919cb-225">Enne</span><span class="sxs-lookup"><span data-stu-id="919cb-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-226">Pärast</span><span class="sxs-lookup"><span data-stu-id="919cb-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="919cb-227">Järgmises tabelis on veel teavet kvaliteettellimuste loomise kohta konkreetset tüüpi protsessidele.</span><span class="sxs-lookup"><span data-stu-id="919cb-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="919cb-228">Protsessi tüüp</span><span class="sxs-lookup"><span data-stu-id="919cb-228">Type of process</span></span></th>
<th><span data-ttu-id="919cb-229">Millal saab kvaliteettellimusi automaatselt luua</span><span class="sxs-lookup"><span data-stu-id="919cb-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="919cb-230">Millal saab kvaliteettellimusi luua, kui on vajalik purustav katsetamine</span><span class="sxs-lookup"><span data-stu-id="919cb-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="919cb-231">Tingimuse teave</span><span class="sxs-lookup"><span data-stu-id="919cb-231">Condition information</span></span></th>
<th><span data-ttu-id="919cb-232">Käsitsi loomise teave</span><span class="sxs-lookup"><span data-stu-id="919cb-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="919cb-233">Ostutellimus</span><span class="sxs-lookup"><span data-stu-id="919cb-233">Purchase order</span></span></td>
<td><span data-ttu-id="919cb-234">Enne või pärast sissetulekute loendi või vastuvõetava materjali toote sissetuleku sisestamist</span><span class="sxs-lookup"><span data-stu-id="919cb-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="919cb-235">Pärast vastuvõetava materjali toote sissetuleku sisestamist, kuna materjal peab olema kättesaadav purustavaks katsetamiseks</span><span class="sxs-lookup"><span data-stu-id="919cb-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="919cb-236">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="919cb-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="919cb-237">Käsitsi loodud ostutellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="919cb-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-238">Vahelao order</span><span class="sxs-lookup"><span data-stu-id="919cb-238">Quarantine order</span></span></td>
<td><span data-ttu-id="919cb-239">Enne või pärast vahelao tellimuse lõpetatuna kinnitamist või lõpetamist</span><span class="sxs-lookup"><span data-stu-id="919cb-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="919cb-240">Purustavaid katseid nõudvaid kvaliteettellimusi ei saa koostada.</span><span class="sxs-lookup"><span data-stu-id="919cb-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="919cb-241">Eeldatakse, et karantiinitellimuse funktsioon tegeleb rikutud materjali likvideerimisega.</span><span class="sxs-lookup"><span data-stu-id="919cb-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="919cb-242">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või hankijat või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="919cb-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="919cb-243">Käsitsi loodud vahelaoorderile viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="919cb-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-244">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="919cb-244">Sales order</span></span></td>
<td><span data-ttu-id="919cb-245">Enne plaanitud komplekteerimisprotsessi või saatelehe uuendamist lähetatavate kaupade puhul</span><span class="sxs-lookup"><span data-stu-id="919cb-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="919cb-246">Igas etapis</span><span class="sxs-lookup"><span data-stu-id="919cb-246">At any step</span></span></td>
<td><span data-ttu-id="919cb-247">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või klienti või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="919cb-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="919cb-248">Käsitsi loodud müügitellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="919cb-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-249">Tootmistellimus</span><span class="sxs-lookup"><span data-stu-id="919cb-249">Production order</span></span></td>
<td><span data-ttu-id="919cb-250">Enne või pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="919cb-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="919cb-251">Pärast tootmistellimuse lõpetatud kogusest teatamist</span><span class="sxs-lookup"><span data-stu-id="919cb-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="919cb-252">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala või kaupa või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="919cb-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="919cb-253">Käsitsi loodud tootmistellimusele viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="919cb-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-254">Tootmistellimus, millel on protsessitoiming</span><span class="sxs-lookup"><span data-stu-id="919cb-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="919cb-255">Enne või pärast toimingu aruande lõpetamist</span><span class="sxs-lookup"><span data-stu-id="919cb-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="919cb-256">Pärast viimase toimingu tootmise lõpetamisest teatamist</span><span class="sxs-lookup"><span data-stu-id="919cb-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="919cb-257">Kvaliteettellimuse vajadus võib kajastada konkreetset laoala, kaupa või operatsiooniressurssi või nende tingimuste kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="919cb-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="919cb-258">Käsitsi loodud protsessitoimingule viitav kvaliteettellimus saab kasutada kvaliteediseose kirje teavet (nt katse valimiplaani).</span><span class="sxs-lookup"><span data-stu-id="919cb-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="919cb-259">Varud</span><span class="sxs-lookup"><span data-stu-id="919cb-259">Inventory</span></span></td>
<td><span data-ttu-id="919cb-260">Kvaliteettellimust ei saa automaatselt koostada varude töölehe kandele või üleviimistellimuse kandele.</span><span class="sxs-lookup"><span data-stu-id="919cb-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="919cb-261">Kvaliteettellimus tuleb kauba laokogusele käsitsi koostada.</span><span class="sxs-lookup"><span data-stu-id="919cb-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="919cb-262">Nõutav on füüsiline vaba laovaru.</span><span class="sxs-lookup"><span data-stu-id="919cb-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="919cb-263">Kvaliteettellimuse automaatse loomise näited</span><span class="sxs-lookup"><span data-stu-id="919cb-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="919cb-264">Ostmine</span><span class="sxs-lookup"><span data-stu-id="919cb-264">Purchasing</span></span>

<span data-ttu-id="919cb-265">Kui määrate ostmisel välja **Sündmuse tüüp** väärtuseks **Toote sissetulek** ja välja **Käivitamine** väärtuseks **Pärast** lehel **Kvaliteediseosed**, saate järgmised tulemused:</span><span class="sxs-lookup"><span data-stu-id="919cb-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="919cb-266">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Jah**, luuakse iga sissetuleku kohta kvaliteettellimus ostutellimuse suhtes, võttes aluseks sissetulnud koguse ja kauba valimi sätted.</span><span class="sxs-lookup"><span data-stu-id="919cb-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="919cb-267">Iga kord, kui ostutellimuse vastu on saadud kogus, luuakse äsja vastuvõetud koguse põhjal uued kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="919cb-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="919cb-268">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Ei**, luuakse sissetulnud koguse põhjal esimese sissetuleku kohta kvaliteettellimus ostutellimuse suhtes.</span><span class="sxs-lookup"><span data-stu-id="919cb-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="919cb-269">Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt jälgimisdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="919cb-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="919cb-270">Kvaliteettellimusi ei looda järgnevate sissetulekute kohta ostutellimuse suhtes.</span><span class="sxs-lookup"><span data-stu-id="919cb-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="919cb-271">Tootmine</span><span class="sxs-lookup"><span data-stu-id="919cb-271">Production</span></span>

<span data-ttu-id="919cb-272">Kui määrate tootmisel välja **Sündmuse tüüp** väärtuseks **Lõpetamise kinnitamine** ja välja **Käivitamine** väärtuseks **Pärast** lehel **Kvaliteediseosed**, saate järgmised tulemused:</span><span class="sxs-lookup"><span data-stu-id="919cb-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="919cb-273">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Jah**, luuakse kvaliteettellimus iga lõpetatud koguse ja kauba valimi sätete alusel.</span><span class="sxs-lookup"><span data-stu-id="919cb-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="919cb-274">Iga kord, kui kogus märgitakse tootmistellimuse suhtes lõpetatuks, luuakse äsja lõpetatud koguse põhjal uued kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="919cb-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="919cb-275">See loomisloogika on kooskõlas ostuga.</span><span class="sxs-lookup"><span data-stu-id="919cb-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="919cb-276">Kui valiku **Värskendatud koguse kohta** väärtuseks on seatud **Ei**, luuakse lõpetatud koguse põhjal kvaliteettellimus esimesel korral, kui kogus kinnitatakse lõpetatuks.</span><span class="sxs-lookup"><span data-stu-id="919cb-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="919cb-277">Lisaks luuakse üks või mitu kvaliteettellimust järelejäänud koguse põhjal, sõltuvalt kauba valimi jälgimisdimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="919cb-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="919cb-278">Hilisemate lõpetatud koguste kohta ei looda kvaliteettellimusi.</span><span class="sxs-lookup"><span data-stu-id="919cb-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="919cb-279">Kvaliteedi spetsifikatsioon</span><span class="sxs-lookup"><span data-stu-id="919cb-279">Quality specification</span></span></th>
<th><span data-ttu-id="919cb-280">Värskendatud koguse kohta</span><span class="sxs-lookup"><span data-stu-id="919cb-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="919cb-281">Jälgimisdimensiooni kohta</span><span class="sxs-lookup"><span data-stu-id="919cb-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="919cb-282">Tulemus</span><span class="sxs-lookup"><span data-stu-id="919cb-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="919cb-283">Protsent: 10%</span><span class="sxs-lookup"><span data-stu-id="919cb-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="919cb-284">Jah</span><span class="sxs-lookup"><span data-stu-id="919cb-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="919cb-285">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="919cb-285">Batch number: No</span></span></p>
<p><span data-ttu-id="919cb-286">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="919cb-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="919cb-287">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="919cb-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="919cb-288">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="919cb-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="919cb-289">Kvaliteettellimus #1 3 kohta (10% 30-st)</span><span class="sxs-lookup"><span data-stu-id="919cb-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="919cb-290">Teata 70 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="919cb-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="919cb-291">Kvaliteettellimus #2 7 kohta (10% järelejäänud tellimuse kogusest, mis võrdub sel juhul 70-ga)</span><span class="sxs-lookup"><span data-stu-id="919cb-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="919cb-292">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="919cb-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="919cb-293">Ei</span><span class="sxs-lookup"><span data-stu-id="919cb-293">No</span></span></td>
<td>
<p><span data-ttu-id="919cb-294">Partii number: ei</span><span class="sxs-lookup"><span data-stu-id="919cb-294">Batch number: No</span></span></p>
<p><span data-ttu-id="919cb-295">Seerianumber: ei</span><span class="sxs-lookup"><span data-stu-id="919cb-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="919cb-296">Tellimuse kogus: 100</span><span class="sxs-lookup"><span data-stu-id="919cb-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="919cb-297">Teata 30 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="919cb-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="919cb-298">Kavaliteettellimus #1 luuakse 1 kohta (esimese lõpetatuna kinnitatud koguse jaoks, millel on fikseeritud väärtus 1)</span><span class="sxs-lookup"><span data-stu-id="919cb-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="919cb-299">Kavaliteettellimus #2 luuakse 1 kohta (järelejäänud koguse jaoks, millel on ikka fikseeritud väärtus 1)</span><span class="sxs-lookup"><span data-stu-id="919cb-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="919cb-300">Teata 10 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="919cb-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="919cb-301">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="919cb-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="919cb-302">Teata 60 lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="919cb-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="919cb-303">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="919cb-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="919cb-304">Fikseeritud kogus: 1</span><span class="sxs-lookup"><span data-stu-id="919cb-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="919cb-305">Jah</span><span class="sxs-lookup"><span data-stu-id="919cb-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="919cb-306">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="919cb-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="919cb-307">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="919cb-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="919cb-308">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="919cb-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="919cb-309">Kinnita lõpetatuks 3 kohta: 1 #b1, #s1 kohta; 1 #b2, #s2 kohta ja 1 #b3, #s3 kohta</span><span class="sxs-lookup"><span data-stu-id="919cb-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="919cb-310">Kvaliteettellimus #1 1 kohta partiist #b1, seerianumber #s1</span><span class="sxs-lookup"><span data-stu-id="919cb-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="919cb-311">Kvaliteettellimus #2 1 kohta partiist #b2, seerianumber #s2</span><span class="sxs-lookup"><span data-stu-id="919cb-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="919cb-312">Kvaliteettellimus #3 1 kohta partiist #b3, seerianumber #s3</span><span class="sxs-lookup"><span data-stu-id="919cb-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="919cb-313">Kinnita lõpetatuks 2 kohta: 1 #b4, #s4 kohta ja 1 #b5, #s5 kohta</span><span class="sxs-lookup"><span data-stu-id="919cb-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="919cb-314">Kvaliteettellimus #4 1 kohta partiist #b4, seerianumber #s4</span><span class="sxs-lookup"><span data-stu-id="919cb-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="919cb-315">Kvaliteettellimus #5 1 kohta partiist #b5, seerianumber #s5</span><span class="sxs-lookup"><span data-stu-id="919cb-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="919cb-316"><strong>Märkus.</strong> Partiid saab uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="919cb-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="919cb-317">Fikseeritud kogus: 2</span><span class="sxs-lookup"><span data-stu-id="919cb-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="919cb-318">Ei</span><span class="sxs-lookup"><span data-stu-id="919cb-318">No</span></span></td>
<td>
<p><span data-ttu-id="919cb-319">Partii number: jah</span><span class="sxs-lookup"><span data-stu-id="919cb-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="919cb-320">Seerianumber: jah</span><span class="sxs-lookup"><span data-stu-id="919cb-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="919cb-321">Tellimuse kogus: 10</span><span class="sxs-lookup"><span data-stu-id="919cb-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="919cb-322">Kinnita lõpetatuks 4 kohta: 1 #b1, #s1 kohta; 1 #b2, #s2 kohta; 1 #b3, #s3 kohta ja 1 #b4, #s4 kohta</span><span class="sxs-lookup"><span data-stu-id="919cb-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="919cb-323">Kvaliteettellimus #1 1 kohta partiist #b1, seerianumber #s1</span><span class="sxs-lookup"><span data-stu-id="919cb-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="919cb-324">Kvaliteettellimus #2 1 kohta partiist #b2, seerianumber #s2</span><span class="sxs-lookup"><span data-stu-id="919cb-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="919cb-325">Kvaliteettellimus #3 1 kohta partiist #b3, seerianumber #s3</span><span class="sxs-lookup"><span data-stu-id="919cb-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="919cb-326">Kvaliteettellimus #4 1 kohta partiist #b4, seerianumber #s4</span><span class="sxs-lookup"><span data-stu-id="919cb-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="919cb-327">Kvaliteettellimus #5 2 kohta,ilma viiteta partiile ja seerianumbrile</span><span class="sxs-lookup"><span data-stu-id="919cb-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="919cb-328">Kinnita lõpetatuks 6 kohta: 1 #b5, #s5 kohta; 1 #b6, #s6 kohta; 1 #b7, #s7 kohta; 1 #b8, #s8 kohta; 1 #b9, #s9 kohta ja 1 #b10, #s10 kohta</span><span class="sxs-lookup"><span data-stu-id="919cb-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="919cb-329">Ühtegi kvaliteettellimust ei looda.</span><span class="sxs-lookup"><span data-stu-id="919cb-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="919cb-330">Funktsioon *Kvaliteedijuhtimine laoprotsesside jaoks* lisab võimalusi kvaliteettellimuse töötlemiseks tootmise puhul, mille **Sündmuse tüüp** on seatud väärtusele *Teata lõpetamisest* ja **Käivitamine** väärtusele *Pärast*, ning ostude puhul, mille **Sündmuse tüüp** on seatud väärtusele *Registreerimine*.</span><span class="sxs-lookup"><span data-stu-id="919cb-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="919cb-331">Lisateavet leiate jaotisest [Kvaliteedijuhtimine laoprotsesside jaoks](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="919cb-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="919cb-332">Kvaliteedijuhtimise lehed</span><span class="sxs-lookup"><span data-stu-id="919cb-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="919cb-333">Lehekülg</span><span class="sxs-lookup"><span data-stu-id="919cb-333">Page</span></span></th>
<th><span data-ttu-id="919cb-334">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="919cb-334">Description</span></span></th>
<th><span data-ttu-id="919cb-335">Näide</span><span class="sxs-lookup"><span data-stu-id="919cb-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="919cb-336">Kvaliteediseosed</span><span class="sxs-lookup"><span data-stu-id="919cb-336">Quality associations</span></span></td>
<td><span data-ttu-id="919cb-337">Vt selle artikli varasemaid jaotisi.</span><span class="sxs-lookup"><span data-stu-id="919cb-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="919cb-338">Kvaliteediseos määratleb koostatava kvaliteettellimuse puhul kogu järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="919cb-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="919cb-339">Kande sündmus</span><span class="sxs-lookup"><span data-stu-id="919cb-339">The transaction event</span></span></li>
<li><span data-ttu-id="919cb-340">Kaupade puhul tehtavate katsete kogum</span><span class="sxs-lookup"><span data-stu-id="919cb-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="919cb-341">AQL</span><span class="sxs-lookup"><span data-stu-id="919cb-341">The AQL</span></span></li>
<li><span data-ttu-id="919cb-342">Valimi plaan</span><span class="sxs-lookup"><span data-stu-id="919cb-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="919cb-343">Kvaliteediseos tuleb automaatset kvaliteettellimuse genereerimist nõudvas äriprotsessis määrata iga variatsiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="919cb-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="919cb-344">Näiteks saab kvaliteettellimuse koostada ostutellimuste, vahelaotellimuste, müügitellimuste ja tootmistellimuste äriprotsessides.</span><span class="sxs-lookup"><span data-stu-id="919cb-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="919cb-345">Katsed</span><span class="sxs-lookup"><span data-stu-id="919cb-345">Tests</span></span></td>
<td><span data-ttu-id="919cb-346">Määrake ja vaadake selle lehe abil üksikuid katseid, mis määratlevad, kas teie tooted vastavad kvaliteedispetsifikatsioonidele või mitte.</span><span class="sxs-lookup"><span data-stu-id="919cb-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="919cb-347">Saate määrata katsegrupile vähemalt ühe eraldi katse.</span><span class="sxs-lookup"><span data-stu-id="919cb-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="919cb-348">Sellisel juhul määrate ka testipõhised andmed, nt vastuvõetavad mõõtmisväärtused.</span><span class="sxs-lookup"><span data-stu-id="919cb-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="919cb-349">Mõõtmisväärtusi kasutatakse kvantitatiivsete katsete puhul ja katsemuutujaid kasutatakse kvalitatiivsete katsete puhul.</span><span class="sxs-lookup"><span data-stu-id="919cb-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="919cb-350">Kvantitatiivse katse tüüp on <strong>täisarv</strong> või <strong>murd</strong> ja sellele on määratud ka mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="919cb-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="919cb-351">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse numbritena.</span><span class="sxs-lookup"><span data-stu-id="919cb-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="919cb-352">Kvalitatiivse katse tüüp on <strong>valik</strong>.</span><span class="sxs-lookup"><span data-stu-id="919cb-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="919cb-353">Kvalitatiivsed katsed nõuavad lisateavet mõõdetava katsemuutuja ja selle loetletud valikute kohta.</span><span class="sxs-lookup"><span data-stu-id="919cb-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="919cb-354">Kvaliteedispetsifikatsioone ja katsetulemusi väljendatakse tulemuse järgi.</span><span class="sxs-lookup"><span data-stu-id="919cb-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="919cb-355">Tootjaettevõte sooritab kaks katset ostetud materjaliga: kvantitatiivse katse materjali kvaliteedi kohta ja kvalitatiivne katse pakendikahjustuse kohta.</span><span class="sxs-lookup"><span data-stu-id="919cb-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="919cb-356">Ettevõte määrab lisateabe kvalitatiivse katse kohta, et määratleda katse muutuja (kahjustatud pakend) ja selle tulemused.</span><span class="sxs-lookup"><span data-stu-id="919cb-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="919cb-357">Ettevõte kasutab lehte <strong>Katsegrupid</strong>, et määrata katsegrupile kaks katset ning määrata katsepõhine teave.</span><span class="sxs-lookup"><span data-stu-id="919cb-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="919cb-358">Katsegrupp määratakse kvaliteeditellimusele, nii et ettevõte saab teavitada kahe katse katsetulemustest.</span><span class="sxs-lookup"><span data-stu-id="919cb-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="919cb-359">Katsegrupid</span><span class="sxs-lookup"><span data-stu-id="919cb-359">Test groups</span></span></td>
<td><span data-ttu-id="919cb-360">Kasutage antud lehte katsegruppide ja katsegrupile määratud eraldi katsete seadistamiseks, redigeerimiseks ning vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="919cb-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="919cb-361">Ülemine paan kuvab katsegruppe ja alumine paan kuvab valitud katsegruppi määratud katseid.</span><span class="sxs-lookup"><span data-stu-id="919cb-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="919cb-362">Saate määrata katsegrupile mitmed põhimõtted nagu valimiplaani, vastuvõetava kvaliteeditaseme (AQL) ja nõuded purustavale katsetamisele.</span><span class="sxs-lookup"><span data-stu-id="919cb-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="919cb-363">Kui määrate katsegrupile eraldi katse, määratlete lisateabe, näiteks järjestuse, dokumendid ja kehtivuse kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="919cb-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="919cb-364">Kvantitatiivse katse puhul sisaldab teie määratletud teave ka vastuvõetavaid mõõtmisväärtusi.</span><span class="sxs-lookup"><span data-stu-id="919cb-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="919cb-365">Kvalitatiivse katse puhul sisaldab teave katsemuutujat ja vaiketulemust.</span><span class="sxs-lookup"><span data-stu-id="919cb-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="919cb-366">Kvaliteettellimusele määratud katsegrupp määratleb katsete vaikekogumi, mis tuleb määratud kaubaga sooritada.</span><span class="sxs-lookup"><span data-stu-id="919cb-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="919cb-367">Kuid saate kvaliteettellimuse katseid lisada, kustutada või muuta.</span><span class="sxs-lookup"><span data-stu-id="919cb-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="919cb-368">Iga katse tulemused kinnitatakse kvaliteettellimuses.</span><span class="sxs-lookup"><span data-stu-id="919cb-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="919cb-369">Tootmisettevõte määrab iga kvaliteetjuhise variandi puhul katsegrupi.</span><span class="sxs-lookup"><span data-stu-id="919cb-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="919cb-370">Erinevad katsegrupid näitavad erinevusi valimiplaanides, katsehulkasid, mida peab koos läbi viima, vastuvõetavat kvaliteeditaset ja muid tegureid.</span><span class="sxs-lookup"><span data-stu-id="919cb-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="919cb-371">Kvantitatiivsete katsete puhul on erinevused ka vastuvõetavates mõõteväärtustes.</span><span class="sxs-lookup"><span data-stu-id="919cb-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="919cb-372">Kvaliteedipõhimõtteid järgides määrab ettevõte igale reeglile katsegrupi, et koostada automaatselt kvaliteettellimusi lehel <strong>Kvaliteediseosed</strong>, ja määrab katsegrupi ka käsitsi loodud kvaliteettellimustele.</span><span class="sxs-lookup"><span data-stu-id="919cb-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="919cb-373">Üksuse kvaliteedigrupid</span><span class="sxs-lookup"><span data-stu-id="919cb-373">Item quality groups</span></span></td>
<td><span data-ttu-id="919cb-374">Kasutage seda lehte, et seadistada, redigeerida ja vaadata kaupu, mis on määratud kaubale määratud kvaliteedigrupile või kvaliteedigruppidele.</span><span class="sxs-lookup"><span data-stu-id="919cb-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="919cb-375">Kvaliteedigrupp tähistab kaupade üldisi testimisnõudeid.</span><span class="sxs-lookup"><span data-stu-id="919cb-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="919cb-376">Pärast katsenõuete määratlemist lehel <strong>Katsegrupid</strong> saate määratleda reeglid kvaliteettellimuste automaatseks koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="919cb-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="919cb-377">Protsessi hõlbustamiseks ei määratleta reegleid üksikutele kaupadele.</span><span class="sxs-lookup"><span data-stu-id="919cb-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="919cb-378">Selle asemel määratletakse reeglid kvaliteedigrupile, kasutades lehte <strong>Kvaliteediseosed</strong>.</span><span class="sxs-lookup"><span data-stu-id="919cb-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="919cb-379">Saate kasutada valitud kvaliteedigrupi puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kaupade määramiseks sellesse gruppi.</span><span class="sxs-lookup"><span data-stu-id="919cb-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="919cb-380">Saate kasutada valitud kauba puhul ka lehte <strong>Kauba kvaliteedigrupid</strong> sobivate kvaliteedigruppide määramiseks sellele kaubale.</span><span class="sxs-lookup"><span data-stu-id="919cb-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="919cb-381">Tootmisettevõte ostab mitmesuguseid ühesuguste sissetulekukontrolli katsenõuetega toormaterjale.</span><span class="sxs-lookup"><span data-stu-id="919cb-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="919cb-382">Ettevõte määrab kvaliteedigrupi ja määrab sellele grupile toormaterjaliga seotud kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="919cb-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="919cb-383">Hiljem ostab ettevõte uut tüüpi toormaterjali, millel on samad katsenõuded.</span><span class="sxs-lookup"><span data-stu-id="919cb-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="919cb-384">Selle asemel, et seadistada uuele materjalile uued katsenõuded, lisab ettevõte uue materjali kaubakoodi olemasolevasse kvaliteedigruppi.</span><span class="sxs-lookup"><span data-stu-id="919cb-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="919cb-385">Sama tootmisettevõte toodab ka ühesuguste tootmisalaste katsenõuetega kaupu ja lähetab ühesuguste nõuetega kaubad lähetuseelsete katsete tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="919cb-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="919cb-386">Ettevõte määrab kaks täiendavat kvaliteedigruppi ja määrab seejärel igale grupile sobivad kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="919cb-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="919cb-387">Katse muutujad</span><span class="sxs-lookup"><span data-stu-id="919cb-387">Test variables</span></span></td>
<td><span data-ttu-id="919cb-388">Sellel lehel saate määratleda ja kuvada kvalitatiivse katsega seotud muutujaid.</span><span class="sxs-lookup"><span data-stu-id="919cb-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="919cb-389">Iga muutuja puhul saab määratleda nummerdatud tulemused, mis kajastavad võimalikke valikuid.</span><span class="sxs-lookup"><span data-stu-id="919cb-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="919cb-390">Saate määratleda katsed lehel <strong>Katsed</strong>.</span><span class="sxs-lookup"><span data-stu-id="919cb-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="919cb-391">Kvalitatiivsete katsete puhul peate määrama katsetüübi <strong>Valik</strong>.</span><span class="sxs-lookup"><span data-stu-id="919cb-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="919cb-392">Kasutage lehte <strong>Katsegrupid</strong> katse muutuja määramiseks individuaalsele katsele.</span><span class="sxs-lookup"><span data-stu-id="919cb-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="919cb-393">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="919cb-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="919cb-394">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="919cb-394">This inspection test has several variables.</span></span> <span data-ttu-id="919cb-395">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="919cb-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="919cb-396">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="919cb-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="919cb-397">Katse muutuja väljundteated</span><span class="sxs-lookup"><span data-stu-id="919cb-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="919cb-398">Kasutage seda lehte kvalitatiivse katsega seotud muutuja võimalike katsetulemuste seadistamiseks, redigeerimiseks ja vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="919cb-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="919cb-399">Iga tulemuse puhul tuleb määrata olek <strong>läbis</strong> või <strong>ei läbinud</strong>.</span><span class="sxs-lookup"><span data-stu-id="919cb-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="919cb-400">Peate määrama muutuja ja tema väljundid iga kvalitatiivse katse jaoks, mis on määratud lehel <strong>Katsed</strong>.</span><span class="sxs-lookup"><span data-stu-id="919cb-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="919cb-401">(Kvalitatiivsete katsete puhul on katse tüübiks määratud <strong>Valik</strong> lehel <strong>Katsed</strong>.) Kasutage lehte <strong>Katsegrupid</strong> katsemuutuja ja vaikeväärtuse määramiseks kindlale kvalitatiivsele katsele.</span><span class="sxs-lookup"><span data-stu-id="919cb-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="919cb-402">Küpsiseid valmistav tootmisettevõte kasutab valmistoote kontrollkatset.</span><span class="sxs-lookup"><span data-stu-id="919cb-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="919cb-403">Sellel kontrollkatsel on mitu muutujat.</span><span class="sxs-lookup"><span data-stu-id="919cb-403">This inspection test has of several variables.</span></span> <span data-ttu-id="919cb-404">Üks muutuja on maitse ja selle muutuja võimalikud väärtused on hea ja halb.</span><span class="sxs-lookup"><span data-stu-id="919cb-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="919cb-405">Teine muutuja on värvus ja võimalikud tulemused on liiga tume, liiga hele ja õige.</span><span class="sxs-lookup"><span data-stu-id="919cb-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="919cb-406">Igale tulemusele omistatakse väärtus <strong>läbis</strong> või <strong>ei läbinud</strong>.</span><span class="sxs-lookup"><span data-stu-id="919cb-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="919cb-407">Iga muutuja kontrolltesti ajal registreerib katsetaja katse tulemuse, valides ühe väljundi väärtustest.</span><span class="sxs-lookup"><span data-stu-id="919cb-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="919cb-408">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="919cb-408">Additional resources</span></span>
--------

[<span data-ttu-id="919cb-409">Kvaliteedijuhtimise protsessid</span><span class="sxs-lookup"><span data-stu-id="919cb-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="919cb-410">Mittevastavuse haldus</span><span class="sxs-lookup"><span data-stu-id="919cb-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="919cb-411">Kvaliteedijuhtimine laoprotsesside jaoks</span><span class="sxs-lookup"><span data-stu-id="919cb-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)
