---
title: BYOD ajastatud pakett-tööde optimeerimine
description: Selles teemas selgitatakse, kuidas optimeerida jõudlust, kui kasutate teenuses Microsoft Dynamics 365 Human Resources oma andmebaasi toomise (BYOD) funktsiooni.
author: andreabichsel
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-10
ms.dyn365.ops.version: Platform update 36
ms.openlocfilehash: a63ff89a6fcbffc57eff14f310a080a35521ef34
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890072"
---
# <a name="optimize-byod-scheduled-batch-jobs"></a><span data-ttu-id="c8485-103">BYOD ajastatud pakett-tööde optimeerimine</span><span class="sxs-lookup"><span data-stu-id="c8485-103">Optimize BYOD scheduled batch jobs</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c8485-104">Selles teemas selgitatakse, kuidas optimeerida jõudlust, kui kasutate oma andmebaasi toomise (BYOD) funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="c8485-104">This topic explains how to optimize performance when you're using the bring your own database (BYOD) feature.</span></span> <span data-ttu-id="c8485-105">Lisateavet BYOD kohta leiate teemast [Oma andmebaasi toomine (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="c8485-105">For more information about BYOD, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

## <a name="performance-considerations-for-data-export"></a><span data-ttu-id="c8485-106">Andmeekspordi jõudluse kaalutlused</span><span class="sxs-lookup"><span data-stu-id="c8485-106">Performance considerations for data export</span></span>

<span data-ttu-id="c8485-107">Pärast seda, kui üksused on sihtkoha andmebaasi avaldatud, saate andmete teisaldamiseks kasutada tööruumi **Andmehaldus** ekspordifunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="c8485-107">After entities are published to the destination database, you can use the Export function in the **Data management** workspace to move data.</span></span> <span data-ttu-id="c8485-108">Ekspordifunktsiooni abil saate määratleda andmete teisaldamise tööd, mis sisaldab mitut üksust.</span><span class="sxs-lookup"><span data-stu-id="c8485-108">The Export function lets you define a Data movement job that contains one or more entities.</span></span> <span data-ttu-id="c8485-109">Lisateavet andmete eksportimise kohta vt [Andmete importimis- ja eksportimistööde ülevaade](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="c8485-109">For more information about data export, see [Data import and export jobs overview](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

<span data-ttu-id="c8485-110">Andmete eksportimiseks muusse sihtvormingusse (nt komaga eraldatud väärtustega (CSV) fail) saate kasutada lehekülge **Eksportimine**.</span><span class="sxs-lookup"><span data-stu-id="c8485-110">You can use the **Export** page to export data into different target data formats, such as a comma-separated values (CSV) file.</span></span> <span data-ttu-id="c8485-111">See lehekülg toetab ka SQL-i andmebaase teise sihtkohana.</span><span class="sxs-lookup"><span data-stu-id="c8485-111">This page also supports SQL databases as another destination.</span></span>

<span data-ttu-id="c8485-112">Saate luua andmeprojekti, millel on mitu üksust, ja kasutada pakett-tööd andmeprojekti käitamise ajastamiseks.</span><span class="sxs-lookup"><span data-stu-id="c8485-112">You can create a data project that has multiple entities and use a batch job to schedule that data project to run.</span></span> <span data-ttu-id="c8485-113">Kui valite suvandi **Eksportimine pakett-tööna**, saate ajastada andmeekspordi regulaarse käitamise.</span><span class="sxs-lookup"><span data-stu-id="c8485-113">If you select the **Export in batch** option, you can schedule the data export job to run periodically.</span></span>

<span data-ttu-id="c8485-114">BYOD ekspordi üldise usaldusväärsuse säilitamiseks peate olema ettevaatlik, kui lisate ekspordiprojektile mitu üksust.</span><span class="sxs-lookup"><span data-stu-id="c8485-114">To help preserve the overall reliability of the BYOD export, you must be careful when you add multiple entities to an export project.</span></span> <span data-ttu-id="c8485-115">Kui määrate samale projektile lisatavate üksuste arvu, kaaluge järgmisi parameetreid.</span><span class="sxs-lookup"><span data-stu-id="c8485-115">When you're determining the number of entities to add to the same project, consider the following parameters:</span></span>

- <span data-ttu-id="c8485-116">Üksuste keerukus</span><span class="sxs-lookup"><span data-stu-id="c8485-116">The complexity of the entities</span></span>
- <span data-ttu-id="c8485-117">Eeldatav andmemaht üksuse kohta</span><span class="sxs-lookup"><span data-stu-id="c8485-117">The expected data volume per entity</span></span>
- <span data-ttu-id="c8485-118">Üldine aeg, mis on vajalik ekspordi lõpetamiseks töö tasemel</span><span class="sxs-lookup"><span data-stu-id="c8485-118">The overall time that will be required to complete the export at the job level</span></span>

<span data-ttu-id="c8485-119">Parima jõudluse saavutamiseks vältige sadade üksuste lisamist ühte projekti.</span><span class="sxs-lookup"><span data-stu-id="c8485-119">For the best performance, avoid adding hundreds of entities to a single project.</span></span> <span data-ttu-id="c8485-120">Soovitame luua mitu tööd, millest igaüks sisaldab vähem üksusi.</span><span class="sxs-lookup"><span data-stu-id="c8485-120">We recommend that you create multiple jobs, each of which contains fewer entities.</span></span>

## <a name="scheduling-byod-batch-jobs"></a><span data-ttu-id="c8485-121">BYOD pakett-tööde ajastamine</span><span class="sxs-lookup"><span data-stu-id="c8485-121">Scheduling BYOD batch jobs</span></span>

<span data-ttu-id="c8485-122">Et aidata vähendada teenuse Microsoft Dynamics 365 Human Resources mõju kasutajatele, käitage BYOD pakett-töid öösiti või väljaspool tööaega.</span><span class="sxs-lookup"><span data-stu-id="c8485-122">To help reduce the impact on users of Microsoft Dynamics 365 Human Resources, run BYOD batch jobs at night or after hours.</span></span> <span data-ttu-id="c8485-123">Kontrollige kindlasti korduvate pakett-tööde ajavööndit.</span><span class="sxs-lookup"><span data-stu-id="c8485-123">Be sure to check the time zone for recurring batch jobs.</span></span> <span data-ttu-id="c8485-124">Osad pakett-tööd võivad kasutada Lääneranniku aega (PST).</span><span class="sxs-lookup"><span data-stu-id="c8485-124">Some batch jobs might use Pacific Standard Time (PST).</span></span>

<span data-ttu-id="c8485-125">Jõudlusprobleemide vältimiseks kaaluge järgmisi tegureid, kui konfigureerite BYOD pakett-tööde ajastamise sagedust.</span><span class="sxs-lookup"><span data-stu-id="c8485-125">To help avoid performance issues, consider the following factors when you configure the scheduling frequency for BYOD batch jobs:</span></span>

- <span data-ttu-id="c8485-126">Iga pakett-töö lõpuleviimiseks vajalik aeg</span><span class="sxs-lookup"><span data-stu-id="c8485-126">The time that is required to complete each batch job</span></span>
- <span data-ttu-id="c8485-127">BYOD andmete ärivajadus</span><span class="sxs-lookup"><span data-stu-id="c8485-127">The business need for the data in BYOD</span></span>

<span data-ttu-id="c8485-128">Määrake iga pakett-töö sagedus väärtusele, mis tagab, et töö saab lõpule viia enne järgmise ajastatud käitusaja algust.</span><span class="sxs-lookup"><span data-stu-id="c8485-128">Set the frequency for each batch job to a value that ensures that the job can be completed well before its next scheduled run time.</span></span> <span data-ttu-id="c8485-129">Vältige mitme töö paralleelset käitamist, kuna selline lähenemine võib negatiivselt mõjutada rakenduse Human Resources jõudlust.</span><span class="sxs-lookup"><span data-stu-id="c8485-129">Avoid running multiple jobs in parallel, because this approach can negatively affect the performance of Human Resources.</span></span>

<span data-ttu-id="c8485-130">Parima jõudluse tagamiseks kasutage BYOD pakett-tööde ajastamiseks suvandit **Ekspordi pakett-tööna** lehel **Eksportimine**.</span><span class="sxs-lookup"><span data-stu-id="c8485-130">For the best performance, always use the **Export in batch** option on the **Export** page to schedule BYOD batch jobs.</span></span> <span data-ttu-id="c8485-131">Vältige korduvate eksportide ajastamist lehel **Halda \> Halda korduvaid andmetöid**.</span><span class="sxs-lookup"><span data-stu-id="c8485-131">Avoid scheduling recurring exports at **Manage \> Manage recurring data jobs**.</span></span>

## <a name="incremental-export"></a><span data-ttu-id="c8485-132">Astmeline eksport</span><span class="sxs-lookup"><span data-stu-id="c8485-132">Incremental export</span></span>

<span data-ttu-id="c8485-133">Kui lisate üksuse andmete eksportimisele, saate teha kas astmelise jaotuse (eksport) või täieliku jaotuse.</span><span class="sxs-lookup"><span data-stu-id="c8485-133">When you add an entity for data export, you can do either an incremental push (export) or a full push.</span></span> <span data-ttu-id="c8485-134">Täielik jaotus kustutab BYOD andmebaasi üksusest kõik olemasolevad kirjed.</span><span class="sxs-lookup"><span data-stu-id="c8485-134">A full push deletes all existing records from an entity in the BYOD database.</span></span> <span data-ttu-id="c8485-135">Seejärel sisestatakse praeguste kirjete kogum rakenduse Human Resources üksusest.</span><span class="sxs-lookup"><span data-stu-id="c8485-135">It then inserts the current set of records from the Human Resources entity.</span></span>

<span data-ttu-id="c8485-136">Astmelise jaotuse tegemiseks peate sisse lülitama lehe **Üksused** iga üksuse muudatuste jälgimise.</span><span class="sxs-lookup"><span data-stu-id="c8485-136">To do an incremental push, you must turn on change tracking for each entity on the **Entities** page.</span></span> <span data-ttu-id="c8485-137">Lisateabe saamiseks vt [Üksuste muudatuste jälgimise lubamine](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="c8485-137">For more information, see [Enable change tracking for entities](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

<span data-ttu-id="c8485-138">Kui valite astmelise jaotuse, on esimene jaotus alati täielik jaotus.</span><span class="sxs-lookup"><span data-stu-id="c8485-138">If you select an incremental push, the first push is always a full push.</span></span> <span data-ttu-id="c8485-139">SQL jälgib muudatusi sellest esimesest jaotusest.</span><span class="sxs-lookup"><span data-stu-id="c8485-139">SQL tracks changes from this first full push.</span></span> <span data-ttu-id="c8485-140">Uue kirje sisestamisel või kirje värskendamisel või kustutamisel kajastub muudatus sihtkoha üksuses.</span><span class="sxs-lookup"><span data-stu-id="c8485-140">When a new record is inserted, or when a record is updated or deleted, the change is reflected in the destination entity.</span></span>

## <a name="time-outs"></a><span data-ttu-id="c8485-141">Ajalõpud</span><span class="sxs-lookup"><span data-stu-id="c8485-141">Time-outs</span></span>

<span data-ttu-id="c8485-142">Siin on BYOD ekspordi vaikimisi ajalõpud.</span><span class="sxs-lookup"><span data-stu-id="c8485-142">Here are the default time-outs for BYOD exports:</span></span>

- <span data-ttu-id="c8485-143">10 minutit kärpimiseks</span><span class="sxs-lookup"><span data-stu-id="c8485-143">Ten minutes for truncation operations</span></span>
- <span data-ttu-id="c8485-144">Üks tund hulgilisamiseks</span><span class="sxs-lookup"><span data-stu-id="c8485-144">One hour for bulk insert operations</span></span>

<span data-ttu-id="c8485-145">Kui mahud on suured, ei pruugi need ajalõpusätted piisavad olla.</span><span class="sxs-lookup"><span data-stu-id="c8485-145">When volumes are high, these time-out settings might not be sufficient.</span></span> <span data-ttu-id="c8485-146">Nende värskendamiseks avage **Dokumendihaldus \> Raamistiku parameetrid \> Oma andmebaasi toomine**.</span><span class="sxs-lookup"><span data-stu-id="c8485-146">To update them, go to **Data management \> Framework parameters \> Bring your own database**.</span></span> <span data-ttu-id="c8485-147">Need ajalõpud on ettevõtte-kohased ja tuleb iga ettevõte jaoks eraldi määrata.</span><span class="sxs-lookup"><span data-stu-id="c8485-147">These time-outs are company-specific and must be set separately for each company.</span></span>

## <a name="known-limitations"></a><span data-ttu-id="c8485-148">Teadaolevad piirangud</span><span class="sxs-lookup"><span data-stu-id="c8485-148">Known limitations</span></span>

<span data-ttu-id="c8485-149">Funktsioonil BYOD on järgmised piirangud.</span><span class="sxs-lookup"><span data-stu-id="c8485-149">The BYOD feature has the following limitations:</span></span>

- <span data-ttu-id="c8485-150">Sünkroonimisel ei tohi andmebaasis olla aktiivseid lukke.</span><span class="sxs-lookup"><span data-stu-id="c8485-150">There should be no active locks on your database during synchronization.</span></span> <span data-ttu-id="c8485-151">Aktiivsed lukud võivad põhjustada aeglast kirjutamist või isegi andmete Azure'i SQL-i andmebaasi eksportimise nurjumist.</span><span class="sxs-lookup"><span data-stu-id="c8485-151">Active locks can cause slow writes or even failure to export data to your Azure SQL database.</span></span>
- <span data-ttu-id="c8485-152">Te ei saa eksportida liitüksusi oma andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="c8485-152">You can't export composite entities into your own database.</span></span> <span data-ttu-id="c8485-153">Praegu ei toetata liitüksusi.</span><span class="sxs-lookup"><span data-stu-id="c8485-153">Currently, composite entities aren't supported.</span></span> <span data-ttu-id="c8485-154">Peate eksportima üksikuid üksusi, mis moodustavad liitüksuse.</span><span class="sxs-lookup"><span data-stu-id="c8485-154">You must export individual entities that make up the composite entity.</span></span> <span data-ttu-id="c8485-155">Siiski saate mõlemaid üksusi samasse projekti eksportida.</span><span class="sxs-lookup"><span data-stu-id="c8485-155">However, you can export both entities in the same data project.</span></span>
- <span data-ttu-id="c8485-156">Üksusi, millel pole kordumatuid võtmeid, ei saa astmelise jaotuse abil eksportida.</span><span class="sxs-lookup"><span data-stu-id="c8485-156">Entities that don't have unique keys can't be exported by using incremental push.</span></span> <span data-ttu-id="c8485-157">Võite sellele piiranguga kokku puutuda eriti siis, kui proovite kirjeid valmisüksustest astmeliselt eksportida.</span><span class="sxs-lookup"><span data-stu-id="c8485-157">You might face this limitation especially when you try to incrementally export records from a few ready-made entities.</span></span> <span data-ttu-id="c8485-158">Kuna need üksused on loodud lubama andmeimporti, pole neil kordumatut võtit.</span><span class="sxs-lookup"><span data-stu-id="c8485-158">Because these entities were designed to enable the import of data, they don't have a unique key.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c8485-159">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="c8485-159">Troubleshooting</span></span>

### <a name="incremental-push-doesnt-work-correctly"></a><span data-ttu-id="c8485-160">Astmeline jaotus ei tööta õigesti</span><span class="sxs-lookup"><span data-stu-id="c8485-160">Incremental push doesn't work correctly</span></span>

<span data-ttu-id="c8485-161">**Probleem:** kui üksuse jaoks tehakse täielik jaotus, kuvatakse BYOD-s suur kirjete kogum, kui kasutate lauset **vali**.</span><span class="sxs-lookup"><span data-stu-id="c8485-161">**Issue:** When a full push occurs for an entity, you see a large set of records in BYOD when you use a **select** statement.</span></span> <span data-ttu-id="c8485-162">Kui te aga teete astmelise jaotuse, kuvatakse BYOD-s ainult mõned kirjed.</span><span class="sxs-lookup"><span data-stu-id="c8485-162">However, when you do an incremental push, you see only a few records in BYOD.</span></span> <span data-ttu-id="c8485-163">Näib, et astmeline jaotus kustutas kõik kirjed ja lisas ainult muudetud kirjed BYOD-s.</span><span class="sxs-lookup"><span data-stu-id="c8485-163">It seems as though the incremental push deleted all the records and added only the changed records in BYOD.</span></span>

<span data-ttu-id="c8485-164">**Lahendus:** SQL-i muudatuste jälgimise tabelid ei pruugi olla eeldatud olekus.</span><span class="sxs-lookup"><span data-stu-id="c8485-164">**Solution:** The SQL change tracking tables might not be in the expected state.</span></span> <span data-ttu-id="c8485-165">Seda tüüpi juhtumite korral soovitame teil üksuse muudatuste jälgimise välja lülitada ja seejärel see uuesti sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="c8485-165">In cases of this type, we recommend that you turn off change tracking for the entity and then turn it back on.</span></span> <span data-ttu-id="c8485-166">Lisateabe saamiseks vt [Üksuste muudatuste jälgimise lubamine](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="c8485-166">For more information, see [Enable change tracking for entities](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

## <a name="see-also"></a><span data-ttu-id="c8485-167">Vt ka</span><span class="sxs-lookup"><span data-stu-id="c8485-167">See also</span></span>

[<span data-ttu-id="c8485-168">Andmehalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="c8485-168">Data management overview</span></span>](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[<span data-ttu-id="c8485-169">Oma andmebaasi toomine (BYOD)</span><span class="sxs-lookup"><span data-stu-id="c8485-169">Bring your own database (BYOD)</span></span>](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[<span data-ttu-id="c8485-170">Andmete importimis- ja eksportimistööde ülevaade</span><span class="sxs-lookup"><span data-stu-id="c8485-170">Data import and export jobs overview</span></span>](../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)<br>
[<span data-ttu-id="c8485-171">Üksuste muudatuste jälgimise lubamine</span><span class="sxs-lookup"><span data-stu-id="c8485-171">Enable change tracking for entities</span></span>](../fin-ops-core/dev-itpro/data-entities/entity-change-track.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]