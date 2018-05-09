---
title: Intrastat
description: "Selles artiklis antakse teavet Euroopa Liidu (EL-i) riikide/regioonide vahelise kauba- ja mõnel juhul teenuste vahetuse Intrastati aruandluse kohta. Antakse ülevaade aruandlusprotsessist ning kirjeldatakse nõutavaid sätteid ja eeltingimusi."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d927f827b9cbc0dc6d9ba5a22c8a05371836faff
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="intrastat"></a><span data-ttu-id="2c090-104">Intrastat</span><span class="sxs-lookup"><span data-stu-id="2c090-104">Intrastat</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2c090-105">Selles artiklis antakse teavet Euroopa Liidu (EL-i) riikide/regioonide vahelise kauba- ja mõnel juhul teenuste vahetuse Intrastati aruandluse kohta.</span><span class="sxs-lookup"><span data-stu-id="2c090-105">This article provides information about Intrastat reporting for the trade of goods and, in some cases, services among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="2c090-106">Antakse ülevaade aruandlusprotsessist ning kirjeldatakse nõutavaid sätteid ja eeltingimusi.</span><span class="sxs-lookup"><span data-stu-id="2c090-106">It provides an overview of the reporting process, and describes the required settings and prerequisites.</span></span>

<span data-ttu-id="2c090-107">Intrastat on Euroopa Liidu (EL-i) riikide/regioonide vahelise kaubavahetuse teabe kogumise ja statistika koostamise süsteem.</span><span class="sxs-lookup"><span data-stu-id="2c090-107">Intrastat is the system for collecting information and generating statistics about the trade of goods among countries/regions of the European Union (EU).</span></span> <span data-ttu-id="2c090-108">Intrastat-aruandlus on nõutav, kui toote ületab teise ELi riigi/regiooni piiri.</span><span class="sxs-lookup"><span data-stu-id="2c090-108">Intrastat reporting is required whenever a product crosses the border of another EU country/region.</span></span> <span data-ttu-id="2c090-109">Mitmes riigis/regioonis kehtib Intrastat-aruandlus ka teenustele.</span><span class="sxs-lookup"><span data-stu-id="2c090-109">In several countries/regions, Intrastat reporting also applies to services.</span></span> <span data-ttu-id="2c090-110">Intrastat-aruandluses võidakse koguda kohustuslikke ja valikulisi elemente.</span><span class="sxs-lookup"><span data-stu-id="2c090-110">Mandatory and optional elements can be collected in Intrastat reporting.</span></span> <span data-ttu-id="2c090-111">Järgmised elemendid on kohustuslikud: teabe esitamise eest vastutava osapoole käibemaksukohustuslase number, viiteperiood, voog (saabumine või lähetamine), kaheksakohaline kaubakood, partneri liikmesriik (saatmise liikmesriik saabumise puhul ja lähetuste puhul sihtliikmesriik), kauba väärtus, kaubakogus (netomass ja täiendav ühik) ning kande iseloom.</span><span class="sxs-lookup"><span data-stu-id="2c090-111">The following elements are mandatory: the value-added tax (VAT) number of the party that is responsible for providing information, the reference period, the flow (arrival or dispatch), the eight-digit commodity code, the partner member state (member state of consignment on arrivals and member state of destination on dispatches), the value of the goods, the quantity of the goods (net mass and supplementary unit), and the nature of the transaction.</span></span> <span data-ttu-id="2c090-112">Riigid/regioonid võivad koguda mitmesugustel tingimustel ka valikulisi elemente.</span><span class="sxs-lookup"><span data-stu-id="2c090-112">Countries/regions can also collect optional elements under various conditions.</span></span> <span data-ttu-id="2c090-113">Mõned valikulised elemendid on päritoluriik/-regioon, tarnetingimused, transpordiliik, üksikasjalikum kaubakood kui CN8, lähetuste puhul lähtepiirkond ja saabumiste puhul sihtpiirkond, statistiline protseduur, statistiline väärtus, kauba kirjeldus ja laadimise/mahalaadimise sadam/lennujaam.</span><span class="sxs-lookup"><span data-stu-id="2c090-113">Some optional elements are the country/region of origin, the delivery terms, the mode of transport, a more detailed commodity code than CN8, the region of origin on dispatches and the region of destination on arrivals, the statistical procedure, the statistical value, a description of the goods, and the port/airport of loading/unloading.</span></span>

## <a name="overview-of-the-intrastat-reporting-process"></a><span data-ttu-id="2c090-114">Intrastat-aruandluse protsessi ülevaade</span><span class="sxs-lookup"><span data-stu-id="2c090-114">Overview of the Intrastat reporting process</span></span>
<span data-ttu-id="2c090-115">Järgmised jaotised kirjeldavad üldist teabevoogu, mida Intrastat-aruandluses kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="2c090-115">The following sections describe the overall flow of information that is used for Intrastat reporting.</span></span>

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a><span data-ttu-id="2c090-116">1. Sisestage kanne, mis ületab teise ELi riigi/regiooni piiri</span><span class="sxs-lookup"><span data-stu-id="2c090-116">1. Enter a transaction that crosses the border of another EU country/region</span></span>

<span data-ttu-id="2c090-117">Kliendiarve, vabas vormis arve, ostuarve, projektiarve, kliendi saateleht, hankija toote sissetulek või üleviimistellimus edastatakse Intrastati töölehele ainult juhul, kui sihtkoha (lähetuste puhul) või lähtekoha (saabumiste puhul) riigi/regiooni sihtkoha tüüp on **EU**.</span><span class="sxs-lookup"><span data-stu-id="2c090-117">A customer invoice, free text invoice, purchase invoice, project invoice, customer packing slip, vendor product receipt, or transfer order is transferred to the Intrastat journal only if the country/region type of the destination (on dispatches) or consignment (on arrivals) is **EU**.</span></span> <span data-ttu-id="2c090-118">Seda funktsiooni laiendati Microsoft Dynamics 365 for Operationsile (1611) ja see võimaldab teil määrata laadimisaadressid ELi-siseste kannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="2c090-118">This feature was extended for Microsoft Dynamics 365 for Operations (1611) and allows you to specify lading addresses for an intra-community transaction.</span></span> <span data-ttu-id="2c090-119">Kui laadimisaadress erineb hankija ettevõtte aadressist (või kliendi ettevõtte aadressist tagastustellimuse puhul), kasutab Intrastati aruandlus seda teavet.</span><span class="sxs-lookup"><span data-stu-id="2c090-119">If a lading address differs with a vendor business address (or customer business address for return order) the Intrastat reporting will operate with this information.</span></span> <span data-ttu-id="2c090-120">Kui loote müügitellimuse, vabas vormis arve, ostutellimuse, hankijaarve, projektiarve või üleviimistellimuse, on mõnel väliskaubandusega seotud väljal dokumendi päises või real vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="2c090-120">When you create a sales order, free text invoice, purchase order, vendor invoice, project invoice, or transfer order, some fields that are related to foreign trade have default values in the document header or on the line.</span></span> <span data-ttu-id="2c090-121">Kandekoodi vaikeväärtus võetakse lehe **Väliskaubanduse parameetrid** vastavalt väljalt.</span><span class="sxs-lookup"><span data-stu-id="2c090-121">The default transaction code is taken from the corresponding field on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="2c090-122">Kaubakoodi, päritoluriigi/-regiooni ja päritolumaakonna/-provintsi vaikeväärtused võetakse kaubalt.</span><span class="sxs-lookup"><span data-stu-id="2c090-122">The default commodity code, country/region of origin, and state/province of origin are taken from the item.</span></span> <span data-ttu-id="2c090-123">Vaikeväärtusi saab muuta ja lisada saab ka muud väliskaubandusega seotud teavet: statistikaprotseduuri, transporti ja sadamat.</span><span class="sxs-lookup"><span data-stu-id="2c090-123">You can change the default values and can also fill in other foreign trade–related information: the statistics procedure, transport method, and port.</span></span>

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="2c090-124">2. Looge Intrastati töölehe abil ELi riikide/regioonide vahelise kaubavahetuse teave.</span><span class="sxs-lookup"><span data-stu-id="2c090-124">2. Use the Intrastat journal to generate information about trade among EU countries/regions</span></span>

<span data-ttu-id="2c090-125">Statistilistel eesmärkidel luuakse ELi riikide/regioonide vahelise kaubavahetuse teave iga kuu.</span><span class="sxs-lookup"><span data-stu-id="2c090-125">For statistical purposes, you generate information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="2c090-126">Kandeid saab edastada vabas vormis arvelt, kliendiarvelt, kliendi saatelehelt, hankija arvelt, hankija saatelehelt, projekti arvelt või üleviimistellimuselt, lehel **Väliskaubanduse parameetrid** seadistatud edastuskriteeriumide alusel.</span><span class="sxs-lookup"><span data-stu-id="2c090-126">You can transfer transactions from a free text invoice, customer invoice, customer packing slip, vendor invoice, vendor packing slip, project invoice, or transfer order, according to the transfer criteria that are set up on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="2c090-127">Kandeid saab sisestada ka käsitsi.</span><span class="sxs-lookup"><span data-stu-id="2c090-127">Alternatively, you can enter transactions manually.</span></span> <span data-ttu-id="2c090-128">Saate edastatud kandeid Intrastati töölehel käsitsi muuta, kui muutmine on vajalik.</span><span class="sxs-lookup"><span data-stu-id="2c090-128">You can manually update transferred transactions in the Intrastat journal, if any updates are required.</span></span> <span data-ttu-id="2c090-129">Konkreetsete tingimuste alusel, mis on seadistatud lehel **Intrastati tihendamine**, saate tihendada Intrastati töölehe kandeid.</span><span class="sxs-lookup"><span data-stu-id="2c090-129">Under specific conditions that are set up on the **Compression of Intrastat** page, you can compress the transactions in the Intrastat journal.</span></span> <span data-ttu-id="2c090-130">Mõnes riigis/regioonis on teil lubatud kohaldada väikest kande läve.</span><span class="sxs-lookup"><span data-stu-id="2c090-130">Some countries/regions let you apply a small transaction threshold.</span></span> <span data-ttu-id="2c090-131">Seejärel saate edastada aruandesse kandeid, mis jäävad määratud kaubakoodi all sellest lävest allapoole.</span><span class="sxs-lookup"><span data-stu-id="2c090-131">You can then report transactions that are below that threshold under the specified commodity code.</span></span> <span data-ttu-id="2c090-132">Saate muuta kaubakoodi vastavatel Intrastati töölehe ridadel, tuginedes sättele **Alampiir** lehel **Väliskaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2c090-132">You can update the commodity code on the corresponding Intrastat journal lines, based on the **Minimum limit** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="2c090-133">Saate neid kandeid sätte **Intrastati tihendamine** alusel ka tihendada.</span><span class="sxs-lookup"><span data-stu-id="2c090-133">You can also compress those transactions, based on the **Compression of Intrastat** setting.</span></span> <span data-ttu-id="2c090-134">Saate kinnitada Intrastati töölehel olevate kannete terviklikkuse sätte **Kontrolli seadistust** põhjal lehel **Väliskaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2c090-134">You can validate the completeness of the transactions in the Intrastat journal, based on the **Check setup** setting on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="2c090-135">Vastavatel väljadel olevate andmete terviklikkust saab kontrollida: riik/regioon, maakond või provints, kaal, kaubakood, kande kood, täiendav ühik, sadam, lähtekoht, tarnetingimus, transpordiliik ja maksuvabastuse number.</span><span class="sxs-lookup"><span data-stu-id="2c090-135">The data in corresponding fields might be validated for completeness: country/region, state or province, weight, commodity code, transaction code, additional unit, port, origin, terms of delivery, transport method, and tax exempt number.</span></span> <span data-ttu-id="2c090-136">Kanded, mida ei ole lõpule viidud, märgitakse kehtetuks.</span><span class="sxs-lookup"><span data-stu-id="2c090-136">Transactions that aren't completed will be marked as not valid.</span></span>

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a><span data-ttu-id="2c090-137">3. Koostage Intrastati töölehe abil ELi riikide/regioonide vahelise kaubavahetuse aruanne.</span><span class="sxs-lookup"><span data-stu-id="2c090-137">3. Use the Intrastat journal to report information about trade among EU countries/regions</span></span>

<span data-ttu-id="2c090-138">Statistilistel eesmärkidel koostatakse ELi riikide/regioonide vahelise kaubavahetuse aruanne iga kuu.</span><span class="sxs-lookup"><span data-stu-id="2c090-138">For statistical purposes, you report information about trade among EU countries/regions every month.</span></span> <span data-ttu-id="2c090-139">Saate Intrastat-aruande välja printida, tuginedes lehe **Aruande vormingu vastendamine** sätetele lehel **Väliskaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2c090-139">You can print the Intrastat report, based on the **Report format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="2c090-140">Saate luua ka elektroonilise faili, tuginedes lehe **Failivormingu vastendamine** sätetele lehel **Väliskaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2c090-140">You can also generate an electronic file, based on the **File format mapping** settings on the **Foreign trade parameters** page.</span></span> <span data-ttu-id="2c090-141">Lisateavet Intrastati aruandluse, sh nõutavate eeltingimuste kohta vaadake Intrastati aruandluse tegevuse salvestistest.</span><span class="sxs-lookup"><span data-stu-id="2c090-141">For more information about Intrastat reporting, including required prerequisites, see the Intrastat reporting task recordings:</span></span>

-   <span data-ttu-id="2c090-142">EL-i Intrastati deklaratsiooni loomine.</span><span class="sxs-lookup"><span data-stu-id="2c090-142">Generate an EU Intrastat declaration,</span></span>
-   <span data-ttu-id="2c090-143">Kannete ülekandmine Intrastati.</span><span class="sxs-lookup"><span data-stu-id="2c090-143">Transfer transactions to the Intrastat,</span></span>
-   <span data-ttu-id="2c090-144">Laadimisaadressi määramine ühendusesisesele kandele.</span><span class="sxs-lookup"><span data-stu-id="2c090-144">Specifying lading address for an intra-community transaction.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2c090-145">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="2c090-145">Prerequisites</span></span>
<span data-ttu-id="2c090-146">Järgmises tabelis on loetletud Intrastati aruandluse eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="2c090-146">The following table lists the prerequisites for Intrastat reporting.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c090-147">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="2c090-147">Prerequisite</span></span></th>
<th><span data-ttu-id="2c090-148">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2c090-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c090-149">Aadressi häälestamine</span><span class="sxs-lookup"><span data-stu-id="2c090-149">Address setup</span></span></td>
<td><span data-ttu-id="2c090-150">Saate seadistada riikide/regioonide ISO (Rahvusvahelise Standardiorganisatsiooni) koodid.</span><span class="sxs-lookup"><span data-stu-id="2c090-150">Set up International Organization for Standardization (ISO) codes for countries/regions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c090-151">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="2c090-151">Legal entity</span></span></td>
<td><span data-ttu-id="2c090-152">Saate seadistada impordi/ekspordi maksuvabastuse numbrid, impordi/ekspordi filiaali koodi laiendi ja juriidilisele isikule määratud Intrastati koodi.</span><span class="sxs-lookup"><span data-stu-id="2c090-152">Set up tax exempt numbers for import/export, the branch number extension for import/export, and the Intrastat code that is assigned to the legal entity.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c090-153">Toote kategooriahierarhia (müügihierarhia, hankehierarhia)</span><span class="sxs-lookup"><span data-stu-id="2c090-153">Product category hierarchy (sales hierarchy, procurement hierarchy)</span></span></td>
<td><span data-ttu-id="2c090-154">Saate määrata Intrastati kaubakoodid kategooriasõlmedele vahekaardil <strong>Kaubakoodid</strong> lehel <strong>Kategooriahierarhia</strong>.</span><span class="sxs-lookup"><span data-stu-id="2c090-154">Assign the Intrastat commodity codes to the category nodes on the <strong>Commodity codes</strong> tab of the <strong>Category hierarchy</strong> page.</span></span> <span data-ttu-id="2c090-155">Kui määrate kaubakoodi peamisele kategooriasõlmele, kehtib see kood kõigile kategooria alamsõlmedele.</span><span class="sxs-lookup"><span data-stu-id="2c090-155">When you assign a commodity code to a parent category node, that code is applicable to all child category nodes.</span></span> <span data-ttu-id="2c090-156">Valitud kaubakoodid on saadaval vaates <strong>Valitud</strong>, kui valite väljastatud toote üksikasjades ja müügitellimuse, ostutellimuse ja üleviimistellimuse ridadel kaubakoodi.</span><span class="sxs-lookup"><span data-stu-id="2c090-156">The selected commodity codes will be available in the <strong>Selected</strong> view when you select a commodity code in the released product details, and on sales order, purchase order, and transfer order lines.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c090-157">Väljastatud toote üksikasjad</span><span class="sxs-lookup"><span data-stu-id="2c090-157">Released product details</span></span></td>
<td><span data-ttu-id="2c090-158">Saate seadistada järgmised väljastatud toodete väliskaubanduse andmed.</span><span class="sxs-lookup"><span data-stu-id="2c090-158">Set up the following foreign trade data for released products:</span></span>
<ul>
<li><span data-ttu-id="2c090-159"><strong>Kaubakood</strong> – valige määratud tootekategooriatest toodud valitud kaupade loendist või Intrastati kaubakoodide tervikloendist.</span><span class="sxs-lookup"><span data-stu-id="2c090-159"><strong>Commodity code</strong> – Select from either the list of selected commodities that is retrieved from assigned product categories or the full list of Intrastat commodity codes.</span></span></li>
<li><span data-ttu-id="2c090-160"><strong>Statistiliste tasude protsent</strong></span><span class="sxs-lookup"><span data-stu-id="2c090-160"><strong>Statistical charges percentage</strong></span></span></li>
<li><span data-ttu-id="2c090-161"><strong>Päritoluriik/-regioon</strong> – saate valida vaikeriigi/-regiooni, kust kaup täielikult hangiti või kus see toodeti.</span><span class="sxs-lookup"><span data-stu-id="2c090-161"><strong>Country/region of origin</strong> – Select the default country/region where the goods were completely obtained or produced.</span></span></li>
<li><span data-ttu-id="2c090-162"><strong>Lähte-/sihtmaakond/-provints</strong> – valige sihtmaakonna/-provintsi vaikeväärtus saabumiste puhul ja lähtemaakond/-provints lähetuste puhul.</span><span class="sxs-lookup"><span data-stu-id="2c090-162"><strong>State/province of origin/destination</strong> – Select the default state/province of destination for arrivals and the state/province of origin for dispatches.</span></span></li>
<li><span data-ttu-id="2c090-163"><strong>Netokaal (kg)</strong></span><span class="sxs-lookup"><span data-stu-id="2c090-163"><strong>Net weight in kg</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c090-164">Kliendid</span><span class="sxs-lookup"><span data-stu-id="2c090-164">Customers</span></span></td>
<td><span data-ttu-id="2c090-165">Saate seadistada kliendi tarneaadressi ELi riigis/regioonis.</span><span class="sxs-lookup"><span data-stu-id="2c090-165">Set up the customer delivery address in the EU country/region.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c090-166">Hankijad</span><span class="sxs-lookup"><span data-stu-id="2c090-166">Vendors</span></span></td>
<td><span data-ttu-id="2c090-167">Saate seadistada hankija aadressi ELi riigis/regioonis.</span><span class="sxs-lookup"><span data-stu-id="2c090-167">Set up the vendor address in the EU country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c090-168">Mitmesugused tasud</span><span class="sxs-lookup"><span data-stu-id="2c090-168">Miscellaneous charges</span></span></td>
<td><span data-ttu-id="2c090-169">Saate seadistada lisakulude koodi arve summale, statistilisele summale või mõlemale lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="2c090-169">Set up the miscellaneous charges code to include in the invoice amount, the statistical amount, or both.</span></span> <span data-ttu-id="2c090-170">Aktiveerige lehel <strong>Tasukoodid</strong> vahekaardil <strong>Väliskaubandus</strong> valik <strong>Intrastati arve väärtus</strong>, et kaasata tasusumma arve väärtusse, ja aktiveerige valik <strong>Intrastati statistiline väärtus</strong> tasusumma kaasamiseks statistilisse väärtusse.</span><span class="sxs-lookup"><span data-stu-id="2c090-170">On the <strong>Charges codes</strong> page, on the <strong>Foreign trade</strong> tab, enable <strong>Intrastat invoice value</strong> to include the charges amount in the invoice value, and enable <strong>Intrastat statistical value</strong> to include the charges amount in the statistical value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c090-171">Elektrooniline aruandlus</span><span class="sxs-lookup"><span data-stu-id="2c090-171">Electronic reporting</span></span></td>
<td><span data-ttu-id="2c090-172">Saate seadistada elektroonilise aruandluse konfiguratsioonid Intrastati andmete eksportimiseks elektroonilisse faili, mis on vastavate asutuste nõutavas vormingus, ja Intrastati andmete eelvaate kuvamiseks kasutajasõbralikus, loetavas vormingus (nt Microsoft Excelis).</span><span class="sxs-lookup"><span data-stu-id="2c090-172">Set up electronic reporting configurations to export Intrastat data in an electronic file that has the format that is requested by the relevant authorities, and to preview Intrastat data in a user-friendly, readable format (for example, in Microsoft Excel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c090-173">Ladustamine</span><span class="sxs-lookup"><span data-stu-id="2c090-173">Warehousing</span></span></td>
<td><span data-ttu-id="2c090-174">Saate seostada hankijakontosid laokoodidega maksukohustuslase koodi lisamiseks üleviimistellimuse üleviimisel.</span><span class="sxs-lookup"><span data-stu-id="2c090-174">Associate vendor accounts with warehouse codes for filling tax exempt number when transferring Transfer order.</span></span></td>
</tr>
</tbody>
</table>

## <a name="setup"></a><span data-ttu-id="2c090-175">Seadistamine</span><span class="sxs-lookup"><span data-stu-id="2c090-175">Setup</span></span>
<span data-ttu-id="2c090-176">Järgmised jaotised kirjeldavad sätteid, mida on Intrastat-aruandluse jaoks vaja.</span><span class="sxs-lookup"><span data-stu-id="2c090-176">The following sections describe the settings that are required for Intrastat reporting.</span></span>

### <a name="set-up-all-required-intrastat-related-lists"></a><span data-ttu-id="2c090-177">Kõigi vajalike Intrastatiga seotud loendite seadistamine</span><span class="sxs-lookup"><span data-stu-id="2c090-177">Set up all required Intrastat-related lists</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c090-178">Loend</span><span class="sxs-lookup"><span data-stu-id="2c090-178">List</span></span></th>
<th><span data-ttu-id="2c090-179">Lisateave</span><span class="sxs-lookup"><span data-stu-id="2c090-179">Additional information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c090-180">Kaubaartiklite koodid</span><span class="sxs-lookup"><span data-stu-id="2c090-180">Commodity codes</span></span></td>
<td><span data-ttu-id="2c090-181">Saate seadistada kategooriahierarhia tüübiga <strong>Kaubakood</strong> ja sisestada kõik kaubakoodid kombineeritud nomenklatuuriloendi alusel.</span><span class="sxs-lookup"><span data-stu-id="2c090-181">Set up a category hierarchy of type <strong>Commodity code</strong>, and enter all commodity codes according to the combined nomenclature list.</span></span> <span data-ttu-id="2c090-182">Iga kauba kohta saate seadistada järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="2c090-182">For each commodity, you set up the following information:</span></span>
<ul>
<li><span data-ttu-id="2c090-183">Kauba nimi ja kaubakood</span><span class="sxs-lookup"><span data-stu-id="2c090-183">The name of the commodity and the commodity code</span></span></li>
<li><span data-ttu-id="2c090-184">Hüüdnimi ja/või tõlgitud nimi</span><span class="sxs-lookup"><span data-stu-id="2c090-184">The friendly name and/or translated name</span></span></li>
<li><span data-ttu-id="2c090-185">Lisaühikute (täiendavate ühikute) aruandluse sätted vahekaardil <strong>Väliskaubandus</strong>. Lisaühiku saab valida ühikute loendist.</span><span class="sxs-lookup"><span data-stu-id="2c090-185">Settings for reporting additional (supplementary) units on the <strong>Foreign trade</strong> tab. You can select the additional unit in the unit list.</span></span> <span data-ttu-id="2c090-186">Samuti saate määrata, kas kaupade kaal tuleb lisaks valitud lisaühikule aruandesse lisada.</span><span class="sxs-lookup"><span data-stu-id="2c090-186">You can also specify whether the weight of commodities must be reported in addition to the selected additional unit.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c090-187">Kandekoodid</span><span class="sxs-lookup"><span data-stu-id="2c090-187">Transaction codes</span></span></td>
<td><span data-ttu-id="2c090-188">Saate seadistada kande iseloomu teie riigi/regiooni nõuete kohaselt.</span><span class="sxs-lookup"><span data-stu-id="2c090-188">Set up the nature of the transaction according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="2c090-189">Iga seadistatava kandekoodi puhul peate seadistama reeglid üleviimistellimuste ja müügi-/ostutellimuste arvesummade ja statistiliste summade arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="2c090-189">For each transaction code that you set up, you must set up the rules for calculating invoice amounts and statistical amounts for transfer orders and sales/purchase orders.</span></span>
<ul>
<li><span data-ttu-id="2c090-190">Üleviimistellimuste puhul saate seadistada arvesummade ja statistiliste summade arvutamiseks ühe järgmistest reeglitest.</span><span class="sxs-lookup"><span data-stu-id="2c090-190">For transfer orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="2c090-191"><strong>Tühi</strong> – summa on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2c090-191"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="2c090-192"><strong>Finantsomahind</strong> – summa on võrdne finantsomahinnaga.</span><span class="sxs-lookup"><span data-stu-id="2c090-192"><strong>Financial cost amount</strong> – The amount will be equal to the financial cost.</span></span></li>
<li><span data-ttu-id="2c090-193"><strong>Kogumaksumus</strong> – summa on võrdne kande kogumaksumusega.</span><span class="sxs-lookup"><span data-stu-id="2c090-193"><strong>Total cost</strong> – The amount will be equal to the total cost of the transaction.</span></span></li>
<li><span data-ttu-id="2c090-194"><strong>Käsitsi</strong> – summa on võrdne üleviimistellimuse käsitsi määratud summaga.</span><span class="sxs-lookup"><span data-stu-id="2c090-194"><strong>Manual</strong> – The amount will be equal to the amount that is manually specified on the transfer order line.</span></span></li>
</ul></li>
<li><span data-ttu-id="2c090-195">Müügi- ja ostutellimuste puhul saate seadistada arvesummade ja statistiliste summade arvutamiseks ühe järgmistest reeglitest.</span><span class="sxs-lookup"><span data-stu-id="2c090-195">For sales orders and purchase orders, you set up one of the following rules for calculating invoice amounts and statistical amounts:</span></span>
<ul>
<li><span data-ttu-id="2c090-196"><strong>Tühi</strong> – summa on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2c090-196"><strong>Empty</strong> – The amount will be 0 (zero).</span></span></li>
<li><span data-ttu-id="2c090-197"><strong>Arve summa</strong> – summa on võrdne kauba eest esitatud arvel oleva summaga.</span><span class="sxs-lookup"><span data-stu-id="2c090-197"><strong>Invoice amount</strong> – The amount will be equal to the amount that is invoiced for the commodity.</span></span></li>
<li><span data-ttu-id="2c090-198"><strong>Baassumma</strong> – summa on võrdne enne allahindluse rakendamist arvel oleva summaga.</span><span class="sxs-lookup"><span data-stu-id="2c090-198"><strong>Base amount</strong> – The amount will be equal to the amount that would be invoiced before any discount is applied.</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c090-199">Transpordimeetodid</span><span class="sxs-lookup"><span data-stu-id="2c090-199">Transport methods</span></span></td>
<td><span data-ttu-id="2c090-200">Saate seadistada transpordiliigi teie riigi/regiooni nõuete kohaselt.</span><span class="sxs-lookup"><span data-stu-id="2c090-200">Set up the transport mode according to your country&#39;s/region&#39;s requirements.</span></span> <span data-ttu-id="2c090-201">Saate määrata iga tarneviisi jaoks vahekaardil <strong>Väliskaubandus</strong> vaike-transpordiliigi.</span><span class="sxs-lookup"><span data-stu-id="2c090-201">For each delivery mode, you can set up a default transport method on the <strong>Foreign trade</strong> tab.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c090-202">Sadamad</span><span class="sxs-lookup"><span data-stu-id="2c090-202">Ports</span></span></td>
<td><span data-ttu-id="2c090-203">Saate seadistada laadimise/mahalaadimise sadama/lennujaama, kui teie riigis/regioonis neid andmeid kogutakse.</span><span class="sxs-lookup"><span data-stu-id="2c090-203">Set up the port/airport of loading/unloading if this information is collected by your country/region.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c090-204">Statistikaprotseduurid</span><span class="sxs-lookup"><span data-stu-id="2c090-204">Statistics procedures</span></span></td>
<td><span data-ttu-id="2c090-205">Saate seadistada statistilise protseduuri, kui seda teavet teie riigis/regioonis kogutakse.</span><span class="sxs-lookup"><span data-stu-id="2c090-205">Set up the statistical procedure if this information is collected by your country/region.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a><span data-ttu-id="2c090-206">Intrastati kannete tihendamise reeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="2c090-206">Set up rules for compressing Intrastat transactions</span></span>

<span data-ttu-id="2c090-207">Lehel **Intrastati tihendamine** saate valida tihendamiseks kasutatavad väljad.</span><span class="sxs-lookup"><span data-stu-id="2c090-207">On the **Compression of Intrastat** page, you can select the fields to use for compression.</span></span> <span data-ttu-id="2c090-208">Kõik kanded, millel on Intrastati töölehel valitud väljadel sama väärtuste kombinatsioon, tihendatakse üheks kandeks, kui kasutate Intrastati töölehel tihendamise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="2c090-208">All transactions that have the same combination of values for the selected fields in the Intrastat journal will be compressed into a single transaction when you run the Compress function in the Intrastat journal.</span></span>

### <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="2c090-209">Väliskaubanduse parameetrite häälestamine</span><span class="sxs-lookup"><span data-stu-id="2c090-209">Set up foreign trade parameters</span></span>

<span data-ttu-id="2c090-210">Kasutage lehte **Väliskaubanduse parameetrid** parameetrite seadistamiseks järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="2c090-210">Use the **Foreign trade parameters** page to set up the parameters in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c090-211">Vahekaart</span><span class="sxs-lookup"><span data-stu-id="2c090-211">Tab</span></span></th>
<th><span data-ttu-id="2c090-212">Parameetrid</span><span class="sxs-lookup"><span data-stu-id="2c090-212">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c090-213">Üldine</span><span class="sxs-lookup"><span data-stu-id="2c090-213">General</span></span></td>
<td><ul>
<li><span data-ttu-id="2c090-214"><strong>Üldine</strong> – määrake järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="2c090-214"><strong>General</strong> – Specify the following information:</span></span>
<ul>
<li><span data-ttu-id="2c090-215">Müügi- ja ostutellimuste, kreeditarvete ja üleviimistellimuste kandekoodide vaikeväärtus.</span><span class="sxs-lookup"><span data-stu-id="2c090-215">The default transaction codes for sales orders, purchase orders, credit notes, and transfer orders.</span></span> <span data-ttu-id="2c090-216">Kreeditarvetele seadistatud kandekoodi kasutatakse ka füüsiliste kaupade tagastamise koodina ning seda kasutatakse füüsiliste tagastuste ja parandamise kreeditarvete hälbe puhul.</span><span class="sxs-lookup"><span data-stu-id="2c090-216">The transaction code that is set up for credit notes is also used as the code for physical goods return and is used for deviating physical returns versus correction credit notes.</span></span></li>
<li><span data-ttu-id="2c090-217">Töötaja, kes vastutab Intrastati aruannete koostamise eest.</span><span class="sxs-lookup"><span data-stu-id="2c090-217">The employee who is responsible for preparing Intrastat reports.</span></span></li>
</ul></li>
<li><span data-ttu-id="2c090-218"><strong>Alampiir</strong> – määrake lävest allapoole jäävate kannete muutmise sätted.</span><span class="sxs-lookup"><span data-stu-id="2c090-218"><strong>Minimum limit</strong> – Specify the settings for updating transactions that are below the threshold:</span></span>
<ul>
<li><span data-ttu-id="2c090-219">Läve summa ja kaal</span><span class="sxs-lookup"><span data-stu-id="2c090-219">The threshold amount and weight</span></span></li>
<li><span data-ttu-id="2c090-220">Lävest allapoole jäävate kannete puhul kohaldatav kaubakood</span><span class="sxs-lookup"><span data-stu-id="2c090-220">The commodity code to apply to transactions that are under the threshold</span></span></li>
</ul></li>
<li><span data-ttu-id="2c090-221"><strong>Ülekanne</strong> – määrake kriteeriumid kannete ülekandmiseks Intrastati töölehele.</span><span class="sxs-lookup"><span data-stu-id="2c090-221"><strong>Transfer</strong> – Specify the criteria for transferring transactions to the Intrastat journal.</span></span> <span data-ttu-id="2c090-222">Saate määrata, et kanded kantakse üle ainult siis, kui kaubad vastavad ühele või kõigile järgmistele kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="2c090-222">You can specify that transactions are transferred only when the items meet one or all of the following criteria:</span></span>
<ul>
<li><span data-ttu-id="2c090-223">Kaubad ei ole teenusüksused.</span><span class="sxs-lookup"><span data-stu-id="2c090-223">The items aren&#39;t service items.</span></span></li>
<li><span data-ttu-id="2c090-224">Kaupadel on kaubakood.</span><span class="sxs-lookup"><span data-stu-id="2c090-224">The items have a commodity code.</span></span></li>
<li><span data-ttu-id="2c090-225">Kaupadel on kaal.</span><span class="sxs-lookup"><span data-stu-id="2c090-225">The items have a weight.</span></span></li>
<li><span data-ttu-id="2c090-226">Kaupadel on lisaühikud.</span><span class="sxs-lookup"><span data-stu-id="2c090-226">The items have additional units.</span></span></li>
</ul></li>
<li><span data-ttu-id="2c090-227"><strong>Seadistuse kontrollimine</strong> – määrake reeglid Intrastati andmete terviklikkuse kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="2c090-227"><strong>Check setup</strong> – Specify the rules for validating the completeness of Intrastat data.</span></span> <span data-ttu-id="2c090-228">Saate valida, milliseid andmeid kontrollitakse.</span><span class="sxs-lookup"><span data-stu-id="2c090-228">You can select which data is validated.</span></span></li>
<li><span data-ttu-id="2c090-229"><strong>Ümardamisreeglid</strong> – määrake järgmised sätted summade ja kaalude ümardamiseks Intrastati aruandes.</span><span class="sxs-lookup"><span data-stu-id="2c090-229"><strong>Rounding rules</strong> – Specify the following settings for rounding amounts and weights in Intrastat reporting:</span></span>
<ul>
<li><span data-ttu-id="2c090-230">Ümardamisreegel (täpsus)</span><span class="sxs-lookup"><span data-stu-id="2c090-230">The rounding rule (precision)</span></span></li>
<li><span data-ttu-id="2c090-231">Ümardamismeetod: üles, alla või tavaline</span><span class="sxs-lookup"><span data-stu-id="2c090-231">The rounding method: up, down, or normal</span></span></li>
<li><span data-ttu-id="2c090-232">Summade ja kaalude kümnendkohtade arv</span><span class="sxs-lookup"><span data-stu-id="2c090-232">The number of decimal places for amounts and weights</span></span></li>
<li><span data-ttu-id="2c090-233">Juhised alla 1 kilogrammi (kg) suuruste kaalude ümardamiseks: üles 1 kg-ni, tavaline või ilma ümardamiseta</span><span class="sxs-lookup"><span data-stu-id="2c090-233">Instructions for rounding weights that are less than 1 kilogram (kg): up to 1 kg, normal, or no rounding</span></span></li>
</ul></li>
<li><span data-ttu-id="2c090-234"><strong>Elektrooniline aruandlus</strong> – määrake elektroonilise aruandluse konfiguratsioonide viited, et saaksite luua elektroonilise faili ja aruande.</span><span class="sxs-lookup"><span data-stu-id="2c090-234"><strong>Electronic reporting</strong> – Specify references to electronic reporting configurations, so that you can generate an electronic file and report.</span></span></li>
<li><span data-ttu-id="2c090-235"><strong>Kaubakoodide hierarhia</strong> – määrake kategooriahierarhia <strong>Kaubakoodi</strong> tüübile, mis kajastab Intrastati kaubakoodi CN8.</span><span class="sxs-lookup"><span data-stu-id="2c090-235"><strong>Commodity code hierarchy</strong> – Specify the category hierarchy of the <strong>Commodity code</strong> type that represents Intrastat commodity code CN8.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c090-236">Agendi kontaktandmed</span><span class="sxs-lookup"><span data-stu-id="2c090-236">Agent contact information</span></span></td>
<td><span data-ttu-id="2c090-237">Määrake agendi nimi, aadress, maksukohustuslase kood, telefoninumber ja faksinumber.</span><span class="sxs-lookup"><span data-stu-id="2c090-237">Specify the agent&#39;s name, address, tax exempt number, telephone number, and fax number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c090-238">Riigi/regiooni atribuudid</span><span class="sxs-lookup"><span data-stu-id="2c090-238">Country/region properties</span></span></td>
<td><span data-ttu-id="2c090-239">Määrake praeguse juriidilise isiku riigiks/regiooniks <strong>Kodumaine</strong>.</span><span class="sxs-lookup"><span data-stu-id="2c090-239">Set the country/region of the current legal entity to <strong>Domestic</strong>.</span></span> <span data-ttu-id="2c090-240">Määrake praeguse juriidilise isikuga ELi kaubanduses osalevate ELi riikide/regioonide riigiks/koodiks <strong>EL</strong>.</span><span class="sxs-lookup"><span data-stu-id="2c090-240">Set the country/region of EU countries/regions that participate in EU trade with the current legal entity to <strong>EU</strong>.</span></span> <span data-ttu-id="2c090-241">Iga riigi/regiooni puhul saate määrata ka riigi/regiooni koodi väliskaubanduse eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="2c090-241">For each country/region, you also identify country/region code for foreign trade purposes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c090-242">Numbriseeria</span><span class="sxs-lookup"><span data-stu-id="2c090-242">Number sequence</span></span></td>
<td><span data-ttu-id="2c090-243">Saate määrata Intrastati töölehe numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="2c090-243">Specify the number sequence for the Intrastat journal.</span></span></td>
</tr>
</tbody>
</table>






