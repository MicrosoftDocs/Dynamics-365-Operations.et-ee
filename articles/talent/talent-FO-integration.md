---
title: Rakenduse Dynamics 365 for Talent rakendusse Dynamics 365 for Finance and Operations integreerimise KKK
description: Selles teemas selgitatakse, millised andmed sünkroonitakse rakenduste Talent ja Finance and Operations integratsioonis.
author: negudava
manager: AnnBe
ms.date: 01/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: aea025bc4898d6399e82030cf1f52b21949e014f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304083"
---
# <a name="dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations-integration-faq"></a><span data-ttu-id="df8bb-103">Rakenduse Dynamics 365 for Talent rakendusse Dynamics 365 for Finance and Operations integreerimise KKK</span><span class="sxs-lookup"><span data-stu-id="df8bb-103">Dynamics 365 for Talent to Dynamics 365 for Finance and Operations integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="df8bb-104">Teemas on toodud vastused peamistele küsimustele selle kohta, milliseid andmeid sünkroonitakse, kui Dynamics 365 for Talent integreeritakse rakendusega Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="df8bb-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 for Talent is integrated with Dynamics 365 for Finance and Operations.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="df8bb-105">Kas sünkroonitakse kõik andmed või ainult mõned andmeüksused?</span><span class="sxs-lookup"><span data-stu-id="df8bb-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="df8bb-106">Rakenduse Core Human Resources (HR) puhul sünkroonitakse andmete alamkogum.</span><span class="sxs-lookup"><span data-stu-id="df8bb-106">With Core Human Resources (HR), a subset of the data is synchronized.</span></span> <span data-ttu-id="df8bb-107">Kõigi üksuste loendi leiate teemast [Integratsioon rakendusest Dynamics 365 for Talent rakendusse Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="df8bb-107">For a list of all the entities, see [Integration from Dynamics 365 for Talent to Dynamics 365 for Finance and Operations](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="df8bb-108">Rakenduste Attract ja Onboard puhul on kõik andmed teenuse Common Data Services (CDS) for Apps omaandmed.</span><span class="sxs-lookup"><span data-stu-id="df8bb-108">For Attract and Onboard, all data is native to Common Data Services (CDS) for Apps.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="df8bb-109">Kas uue vastenduse saab luua malle kasutamata?</span><span class="sxs-lookup"><span data-stu-id="df8bb-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="df8bb-110">Mallid on alguspunkt.</span><span class="sxs-lookup"><span data-stu-id="df8bb-110">Templates are the starting point.</span></span> <span data-ttu-id="df8bb-111">Saate luua oma malli, kuid malli on integratsiooniprojekti loomisel alati vaja.</span><span class="sxs-lookup"><span data-stu-id="df8bb-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="df8bb-112">Lisateavet andmeintegraatori (DI), mallide ja projektide kohta vt teemast [Andmete integreerimine teenusesse Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="df8bb-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance-and-operations"></a><span data-ttu-id="df8bb-113">Kas ma saan vastendada finantsdimensioonide edastamise rakenduste Talent ja Finance and Operations vahel?</span><span class="sxs-lookup"><span data-stu-id="df8bb-113">Can I map financial dimensions to transfer between Talent and Finance and Operations?</span></span>

<span data-ttu-id="df8bb-114">Finantsdimensioonid puuduvad praegu teenusest CDS for Apps ja seetõttu ei ole need ka vaikemalli osa.</span><span class="sxs-lookup"><span data-stu-id="df8bb-114">Financial dimensions aren’t currently in CDS for Apps and as a result aren’t part of the default template.</span></span> <span data-ttu-id="df8bb-115">See üksus on kavas, kuid praegu pole väljastamise ajakava saadaval.</span><span class="sxs-lookup"><span data-stu-id="df8bb-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="df8bb-116">Andmete puhul, mis on olemas rakenduses Finance and Operations, kuid puuduvad rakendusest Talent, linkige kaks süsteemi kokku, kasutades Talenti funktsiooni **Linkide konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="df8bb-116">For data that resides in Finance and Operations but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="df8bb-117">Lisateavet linkide konfigureerimise kohta rakenduste Talent ja Finance and Operations vahel vt teemast [Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent Core HR (31. oktoober 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="df8bb-117">For more information about how to configure links between Talent and Finance and Operations, see [What's new or changed in Dynamics 365 for Talent Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-and-operations-why"></a><span data-ttu-id="df8bb-118">Töövõtjate importimisel liiguvad need mõnikord rakenduses Finance and Operations passiivsete töötajate loendisse.</span><span class="sxs-lookup"><span data-stu-id="df8bb-118">Sometimes when I import employees, they go into inactive workers in Finance and Operations.</span></span> <span data-ttu-id="df8bb-119">Miks?</span><span class="sxs-lookup"><span data-stu-id="df8bb-119">Why?</span></span>

<span data-ttu-id="df8bb-120">See tõrge võib ilmneda, kui töövõtjal pole Talentis aktiivse töösuhte üksikasjade kirjet.</span><span class="sxs-lookup"><span data-stu-id="df8bb-120">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="df8bb-121">Probleemi lahendamiseks minge jaotisse **Personalihaldus \> Töövõtjad \> Töösuhte ajalugu \> Kuupäevahaldur** ja kontrollige, kas seal on aktiivse töösuhte üksikasjade kirje olemas.</span><span class="sxs-lookup"><span data-stu-id="df8bb-121">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="df8bb-122">Kui soovin vastendada ainult väljade alamkogumi, siis kas vastendamata väljade muutmine käivitab sünkroonimise?</span><span class="sxs-lookup"><span data-stu-id="df8bb-122">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="df8bb-123">Andmete sünkroonimine järgib käivitusgraafikut.</span><span class="sxs-lookup"><span data-stu-id="df8bb-123">Data sync follows the execution schedule.</span></span> <span data-ttu-id="df8bb-124">Integratsioon valib kirje, kui selle mis tahes väli muutub, olenemata sellest, kas väli on integratsioonivastenduse osa või mitte.</span><span class="sxs-lookup"><span data-stu-id="df8bb-124">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="df8bb-125">Kuidas saata ainult aktiivse töötaja muudatused, mitte lõpetatud kirjed?</span><span class="sxs-lookup"><span data-stu-id="df8bb-125">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="df8bb-126">Kasutades täpsemat päringut, saate lähteandmeid filtreerida ja ümber kujundada, enne kui edastate need sihtkohta.</span><span class="sxs-lookup"><span data-stu-id="df8bb-126">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-and-operations-for-a-specific-entity"></a><span data-ttu-id="df8bb-127">Kas saan määrata, millised väljad saadetakse rakendusse Finance and Operations kindla üksuse puhul?</span><span class="sxs-lookup"><span data-stu-id="df8bb-127">Can I specify which fields to send to Finance and Operations for a specific entity?</span></span>

<span data-ttu-id="df8bb-128">Integratsiooniülesandele saab välju lisada või neid eemaldada.</span><span class="sxs-lookup"><span data-stu-id="df8bb-128">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="df8bb-129">Kõiki andmevälju, mis on teenuse CDS for Apps (CDS 2.0) üksuses olemas, ei asustata rakendusest Core HR.</span><span class="sxs-lookup"><span data-stu-id="df8bb-129">Not all data fields that exist on the CDS for Apps (CDS 2.0) entity will be populated from Core HR.</span></span>
<span data-ttu-id="df8bb-130">Lisaandmeid saab asustada PowerAppsi kaudu.</span><span class="sxs-lookup"><span data-stu-id="df8bb-130">Additional data can be populated via PowerApps.</span></span>

![](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="df8bb-131">Seadistan integratsiooni pakett-tööna, kuid Talentil kadus ühendus sihtsüsteemiga.</span><span class="sxs-lookup"><span data-stu-id="df8bb-131">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="df8bb-132">Kuidas saata sihtsüsteemi sama muudatuste kogum?</span><span class="sxs-lookup"><span data-stu-id="df8bb-132">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="df8bb-133">Erandite töötlemiseks pole eriseadistus vajalik.</span><span class="sxs-lookup"><span data-stu-id="df8bb-133">No special setup is required for exception handling.</span></span> <span data-ttu-id="df8bb-134">Andmeintegraator jäädvustab ja teatab automaatselt tõrgetest, mis ilmnevad lähte- ja sihtkohas, ning lubab käsitsi uuesti proovida.</span><span class="sxs-lookup"><span data-stu-id="df8bb-134">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="df8bb-135">See ei võimalda siiski andmeid käsitsi parandada.</span><span class="sxs-lookup"><span data-stu-id="df8bb-135">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="df8bb-136">Kui andmete värskendamine on vajalik, tuleb seda teha kas lähte- või sihtkohas.</span><span class="sxs-lookup"><span data-stu-id="df8bb-136">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="df8bb-137">Kas saan seadistada kahesuunalise integratsiooni?</span><span class="sxs-lookup"><span data-stu-id="df8bb-137">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="df8bb-138">Ei, integratsioon on praegu ainult ühesuunaline (Talentist Finance and Operationsisse).</span><span class="sxs-lookup"><span data-stu-id="df8bb-138">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="df8bb-139">Siiski on saadaval vaikemall andmete saatmiseks Talentist Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="df8bb-139">However, there is a default template available to send data from Talent to Finance and Operations.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="df8bb-140">Kas saan integratsiooni osana lubada kirjete kustutamise?</span><span class="sxs-lookup"><span data-stu-id="df8bb-140">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="df8bb-141">Ei, andmeintegraator ei talleta kustutatud kirjeid andmeedastuseks.</span><span class="sxs-lookup"><span data-stu-id="df8bb-141">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="df8bb-142">Praegu hõlmab see ainult andmete loomist ja värskendamist (UPSERT).</span><span class="sxs-lookup"><span data-stu-id="df8bb-142">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="df8bb-143">Kas tõrkega käituse saab uuesti käivitada?</span><span class="sxs-lookup"><span data-stu-id="df8bb-143">Can I rerun the errored execution?</span></span> <span data-ttu-id="df8bb-144">Kui jah, siis kas see saadab kogu faili või ainult muudatused?</span><span class="sxs-lookup"><span data-stu-id="df8bb-144">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="df8bb-145">Andmeintegraatori esmane käitamine on alati täielik.</span><span class="sxs-lookup"><span data-stu-id="df8bb-145">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="df8bb-146">Järgmised käitused põhinevad muudatuste jälgimisel.</span><span class="sxs-lookup"><span data-stu-id="df8bb-146">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="df8bb-147">Tõrkega käituse korral eraldab see kõnealused kirjed käitusest ja saadab CDS-ist välja uusimad muudatused.</span><span class="sxs-lookup"><span data-stu-id="df8bb-147">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from CDS.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="df8bb-148">Saan projekti salvestamisel tõrketeate „Projektil on vastendustõrked”.</span><span class="sxs-lookup"><span data-stu-id="df8bb-148">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="df8bb-149">Mida teha?</span><span class="sxs-lookup"><span data-stu-id="df8bb-149">What do I do?</span></span>

<span data-ttu-id="df8bb-150">Kontrollige oma integratsioonivõtmete seadistust, tehke seadistusse vajalikud muudatused ja seejärel värskendage üksuseid projektis.</span><span class="sxs-lookup"><span data-stu-id="df8bb-150">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="df8bb-151">Vaikemalli kasutamisel imporditakse integratsioonivõtmed automaatselt.</span><span class="sxs-lookup"><span data-stu-id="df8bb-151">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="df8bb-152">See probleem võib ilmneda, kui olemasolevale mallile lisatakse uusi ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="df8bb-152">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="df8bb-153">Kui mul on N juriidilist isikut, mille töötajatel on töösuhe, siis kas pean looma neist igaühe jaoks vastenduse?</span><span class="sxs-lookup"><span data-stu-id="df8bb-153">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="df8bb-154">Jah, rakenduses Finance and Operations peab iga juriidilise isiku kohta olema andmeintegratsioonis eraldi integratsiooniprojekt.</span><span class="sxs-lookup"><span data-stu-id="df8bb-154">Yes, for each legal entity in Finance and Operations, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="df8bb-155">Pean edastama andmeid, mis ei ole Microsofti vaikemalli osa.</span><span class="sxs-lookup"><span data-stu-id="df8bb-155">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="df8bb-156">Kas saan seda teha?</span><span class="sxs-lookup"><span data-stu-id="df8bb-156">Can I do this?</span></span>

<span data-ttu-id="df8bb-157">Jah, olemasolevale mallile saab välju lisada või neid eemaldada.</span><span class="sxs-lookup"><span data-stu-id="df8bb-157">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="df8bb-158">Malli saab muuta, kaasates lisaandmeid teistest teenuse CDS for Apps üksustest.</span><span class="sxs-lookup"><span data-stu-id="df8bb-158">The template can be modified to include additional data from other CDS for Apps entities.</span></span> <span data-ttu-id="df8bb-159">Malli kaasamiseks peab üksus olema teenuses CDS for Apps.</span><span class="sxs-lookup"><span data-stu-id="df8bb-159">The entity must be in CDS for Apps for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-operations-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="df8bb-160">Lõin äsja uued Finance and Operationsi ja Talenti keskkonnad ning saan tõrketeate „Andmete väärtus rikub tervikluse piiranguid”.</span><span class="sxs-lookup"><span data-stu-id="df8bb-160">I just created new Finance and Operations and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="df8bb-161">Miks?</span><span class="sxs-lookup"><span data-stu-id="df8bb-161">Why?</span></span>

<span data-ttu-id="df8bb-162">Tõrke põhjused võivad olla järgmised.</span><span class="sxs-lookup"><span data-stu-id="df8bb-162">Reasons for this error can include:</span></span>

- <span data-ttu-id="df8bb-163">Andmeedastuse tulemuseks on topeltkirjete eraldamine lähtekohas (CDS).</span><span class="sxs-lookup"><span data-stu-id="df8bb-163">The data transfer resulted in duplicate records extraction at the source (CDS).</span></span>

- <span data-ttu-id="df8bb-164">Andmeedastusel on Finance and Operationsis vajalike väljade puhul nullväärtused.</span><span class="sxs-lookup"><span data-stu-id="df8bb-164">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="df8bb-165">Kontrollige, kas CDS-is olevad andmed vastavad rakenduse Finance and Operations nõuetele.</span><span class="sxs-lookup"><span data-stu-id="df8bb-165">Verify the data that is in CDS and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="df8bb-166">Kui esineb käivitustõrkeid ja töövõtja ID-d ei sünkroonita, siis kuidas leida ajalooline töö, milles on nurjunud töövõtja kirje?</span><span class="sxs-lookup"><span data-stu-id="df8bb-166">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="df8bb-167">Andmeintegraator loob rakenduses Finance and Operations mitu projekti.</span><span class="sxs-lookup"><span data-stu-id="df8bb-167">Data Integrator will create multiple projects in Finance and Operations.</span></span> <span data-ttu-id="df8bb-168">Seos andmeintegraatori ülesande ja rakenduse Finance and Operations projekti vahel on üksühene.</span><span class="sxs-lookup"><span data-stu-id="df8bb-168">The relationship between the Data Integrator task and the Finance and Operations project is one to one.</span></span>

<span data-ttu-id="df8bb-169">Jälgige aega andmeintegraatori käivitusajaloost ja leidke rakenduses Finance and Operations projekti indeks – 1.</span><span class="sxs-lookup"><span data-stu-id="df8bb-169">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance and Operations.</span></span> <span data-ttu-id="df8bb-170">Kui ülesande number on andmeintegraatoris 9, siis indeks Finance and Operationsis on 8.</span><span class="sxs-lookup"><span data-stu-id="df8bb-170">If the task number is 9 in Data Integrator, the index in Finance and Operations is 8.</span></span>

1. <span data-ttu-id="df8bb-171">Märkige üles ülesande indeks andmeintegraatorist (selles näites 9).</span><span class="sxs-lookup"><span data-stu-id="df8bb-171">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Andmeintegraatorist ülesande indeksi ülesmärkimine](media/CaptureTaskIndex.png)

2. <span data-ttu-id="df8bb-173">Jälgige projekti käivitusaega.</span><span class="sxs-lookup"><span data-stu-id="df8bb-173">Track the execution time of the project.</span></span>

![Projekti käivitusaja jälgimine](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="df8bb-175">Rakenduses Finance and Operations leidke indeks – 1.</span><span class="sxs-lookup"><span data-stu-id="df8bb-175">In Finance and Operations, identify index - 1.</span></span> <span data-ttu-id="df8bb-176">Selles näites vastab projekt järelliitega 8 ja projekti indeksiga 0 käivitusaeg etapis 2 näidatud käivitusajale.</span><span class="sxs-lookup"><span data-stu-id="df8bb-176">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Indeksi tuvastamine](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-and-operations-i-dont-see-my-talent-data-in-finance-and-operations-what-do-i-do"></a><span data-ttu-id="df8bb-178">Pärast Talenti ja Finance and Operationsi integreerimist ei näe ma enam oma Talenti andmeid rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="df8bb-178">After integrating Talent and Finance and Operations, I don’t see my Talent data in Finance and Operations.</span></span> <span data-ttu-id="df8bb-179">Mida teha?</span><span class="sxs-lookup"><span data-stu-id="df8bb-179">What do I do?</span></span>

<span data-ttu-id="df8bb-180">Integratsioon rakendusse Finance and Operations on kaheetapiline protsess.</span><span class="sxs-lookup"><span data-stu-id="df8bb-180">The integration to Finance and Operations is a two-step process.</span></span> <span data-ttu-id="df8bb-181">Esmalt kontrollige, kas Talenti andmed on värskendatud ja CDS-is saadaval.</span><span class="sxs-lookup"><span data-stu-id="df8bb-181">First, verify that the Talent data is updated and available in CDS.</span></span> <span data-ttu-id="df8bb-182">See on peaaegu reaalajas sünkroonimine ja seda saab kontrollida PowerAppsis, vaadates andmeüksustes olevaid andmeid.</span><span class="sxs-lookup"><span data-stu-id="df8bb-182">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Andmed CDS-is](media/DataInCDS.png)

<span data-ttu-id="df8bb-184">Kui andmeid ei kuvata CDS-is oodatud viisil, siis kontrollige, kas integratsioon toetab üksust.</span><span class="sxs-lookup"><span data-stu-id="df8bb-184">If the data is not appearing as expected in CDS, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="df8bb-185">CDS-i lisaandmete kaasamiseks on vajalik muudatus Microsofti poolel.</span><span class="sxs-lookup"><span data-stu-id="df8bb-185">To include additional data in CDS, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="df8bb-186">Kui üksust toetatakse ja andmed on CDS-is saadaval, siis kontrollige, kas vastendus on andmeintegraatoris õige.</span><span class="sxs-lookup"><span data-stu-id="df8bb-186">If the entity is supported and the data is available in CDS, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="df8bb-187">Kui integraatori vastendus tundub olevat korras, siis kontrollige edukalt käitatud andmehalduse töid.</span><span class="sxs-lookup"><span data-stu-id="df8bb-187">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="df8bb-188">Tõrked võivad ilmneda pakett-tööde käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="df8bb-188">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="df8bb-189">Lisateavet andmehalduse kohta vt teemast [Andmehaldus](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="df8bb-189">For more information about Data Management, see [Data management](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-and-operations-what-should-i-do"></a><span data-ttu-id="df8bb-190">Pärast töövõtjate importimist rakendusse Finance and Operations on nende aadressid valed.</span><span class="sxs-lookup"><span data-stu-id="df8bb-190">The addresses for my employees are incorrect after I import them into Finance and Operations.</span></span> <span data-ttu-id="df8bb-191">Mida teha?</span><span class="sxs-lookup"><span data-stu-id="df8bb-191">What should I do?</span></span>

<span data-ttu-id="df8bb-192">**Asukoha ID** numbriseeria kasutab rakendustes Talent ja Finance and Operations sama mustrit.</span><span class="sxs-lookup"><span data-stu-id="df8bb-192">The number sequence for **Location ID** uses the same pattern in both Talent and Finance and Operations.</span></span> <span data-ttu-id="df8bb-193">Numbriseeria peab olema mõlemal poolel kordumatu, et andmete integreerimisel CDS-ist rakendusse Finance and Operations ei tekiks aadressivastuolusid.</span><span class="sxs-lookup"><span data-stu-id="df8bb-193">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from CDS to Finance and Operations.</span></span>

<span data-ttu-id="df8bb-194">Talenti juurutamise ajal kontrollige, et numbriseeriad poleks Talentis ja Finance and Operationsis samad.</span><span class="sxs-lookup"><span data-stu-id="df8bb-194">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance and Operations.</span></span> <span data-ttu-id="df8bb-195">Veenduge, et ükski numbriseeria poleks identne, kui andmeid võidakse hallata mõlemas süsteemis.</span><span class="sxs-lookup"><span data-stu-id="df8bb-195">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="df8bb-196">Ühendusekogumi loomisel ei näe ma ühendust ripploendis Ühendus.</span><span class="sxs-lookup"><span data-stu-id="df8bb-196">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="df8bb-197">Mida teha?</span><span class="sxs-lookup"><span data-stu-id="df8bb-197">What do I do?</span></span>

<span data-ttu-id="df8bb-198">Veenduge, et valiksite ühenduste loomisel suvandid Dynamics 365 for Finance and Operations (praegu eelvaateversioonis) ja Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="df8bb-198">Make sure when creating your connections, you choose Dynamics 365 for Finance and Operations (currently in preview) and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfofk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="df8bb-199">Saan töösuhete sünkroonimisel tõrketeate „Atribuuti CompanyInfo_FK pole olemas” või „Väärtust 12/31/2154 23:59:59 väljal Töösuhte lõppkuupäev ei leitud seotud tabelist Töösuhe”. Mida teha?</span><span class="sxs-lookup"><span data-stu-id="df8bb-199">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="df8bb-200">Veendute, et vastendaksite õigete juriidiliste isikutega.</span><span class="sxs-lookup"><span data-stu-id="df8bb-200">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="df8bb-201">Juriidilise isiku sünkroonimine pole vaikemalli osa, seega peaks iga Talentis ja CDS-is olev juriidiline isik olemas olema ka Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="df8bb-201">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and CDS is also present in Finance and Operations.</span></span>
<span data-ttu-id="df8bb-202">Veenduge ka, et valiksite seostatud ühendusekogumi jaoks õiged juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="df8bb-202">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-and-operations-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="df8bb-203">Pärast projekti seadistamist kuvatakse väljavastendus Finance and Operationsi puhul tühjana.</span><span class="sxs-lookup"><span data-stu-id="df8bb-203">After setting up my project, the field mapping for Finance and Operations appears to be empty.</span></span> <span data-ttu-id="df8bb-204">Mida teha?</span><span class="sxs-lookup"><span data-stu-id="df8bb-204">What should I do?</span></span>

<span data-ttu-id="df8bb-205">Värskendage andmeüksuseid rakenduses Finance and Operations, minnes jaotisse **Andmehaldus \> Raamistiku parameetrid \> Üksuse sätted \> Värskenda üksuste loendit.**</span><span class="sxs-lookup"><span data-stu-id="df8bb-205">Refresh the data entities in Finance and Operations by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="df8bb-206">Selle lõpuleviimiseks kulub mõni minut, seejärel peaksite neid vastendusi nägema.</span><span class="sxs-lookup"><span data-stu-id="df8bb-206">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="df8bb-207">See probleem ilmneb uute projektide loomisel.</span><span class="sxs-lookup"><span data-stu-id="df8bb-207">This issue occurs when new projects are created.</span></span>

![Puuduv väljavastendus](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="df8bb-209">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="df8bb-209">Additional resources</span></span>

- <span data-ttu-id="df8bb-210">Andmeintegraator (DI):</span><span class="sxs-lookup"><span data-stu-id="df8bb-210">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="df8bb-211">Andmete integreerimine teenusesse Common Data Service for Apps</span><span class="sxs-lookup"><span data-stu-id="df8bb-211">Integrate data into Common Data Service for Apps</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="df8bb-212">Andmeintegraatori tõrkehaldus ja tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="df8bb-212">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="df8bb-213">DSR-i taotlustele vastamine süsteemi loodud logide puhul teenustes PowerApps, Microsoft Flow ja teenuses Common Data Service for Apps</span><span class="sxs-lookup"><span data-stu-id="df8bb-213">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service for Apps</span></span>](https://docs.microsoft.com/en-us/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="df8bb-214">Andmehaldus</span><span class="sxs-lookup"><span data-stu-id="df8bb-214">Data Management:</span></span>

  - [<span data-ttu-id="df8bb-215">Andmehaldus</span><span class="sxs-lookup"><span data-stu-id="df8bb-215">Data management</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
