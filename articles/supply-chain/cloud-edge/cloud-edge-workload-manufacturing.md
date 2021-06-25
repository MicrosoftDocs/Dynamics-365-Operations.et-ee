---
title: Tootmise täideviimise töökoormused pilv- ja perimeeterskaalaüksuste jaoks
description: See teema kirjeldab, kuidas tootmise läbiviimise töömahud töötavad koos pilv- ja perimeeterskaalaüksustega.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 9cd7dd8b9241171bdfdb3cc1379211a2fe99bbe1
ms.sourcegitcommit: 8d50c905a0c9d4347519549b587bdebab8ffc628
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2021
ms.locfileid: "6183992"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="dc6be-103">Tootmise täideviimise töökoormused pilv- ja perimeeterskaalaüksuste jaoks</span><span class="sxs-lookup"><span data-stu-id="dc6be-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="dc6be-104">Tootmise käivitamise töökoormus on praegu eelvaates saadaval.</span><span class="sxs-lookup"><span data-stu-id="dc6be-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="dc6be-105">Mõni ettevõtte funktsionaalsus ei ole avalikus eelvaates täielikult toetatud juhul, kui kasutatakse töökoormuse skaalaüksusi.</span><span class="sxs-lookup"><span data-stu-id="dc6be-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="dc6be-106">Tootmise käivitamisel pakuvad mastaabiüksused järgmisi võimalusi:</span><span class="sxs-lookup"><span data-stu-id="dc6be-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="dc6be-107">Masina operaatorid ja tööde juhtimise haldurid pääsevad ligi operatiivsele tootmisplaanile.</span><span class="sxs-lookup"><span data-stu-id="dc6be-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="dc6be-108">Masina operaatorid saavad plaani ajakohasena hoida, töötades eraldi ja menetledes tootmise töid.</span><span class="sxs-lookup"><span data-stu-id="dc6be-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="dc6be-109">Tööde juhtimise haldur saab tegevuskava korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="dc6be-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="dc6be-110">Töötajatel on juurdepääs aja ja kohalolekt sisse-ja väljaregistreerimisele serval, et tagada õiglane töötaja tasu arvutamine.</span><span class="sxs-lookup"><span data-stu-id="dc6be-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="dc6be-111">See teema kirjeldab, kuidas tootmise läbiviimise töömahud töötavad koos pilv- ja perimeeterskaalaüksustega.</span><span class="sxs-lookup"><span data-stu-id="dc6be-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="dc6be-112">Tootmise elutsükkel</span><span class="sxs-lookup"><span data-stu-id="dc6be-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="dc6be-113">Nagu järgnev illustratsioon näitab, on tootmise elutsükkel jagatud kolmeks faasiks: *Planeeri*, *Käivita* ja *Lõpeta*.</span><span class="sxs-lookup"><span data-stu-id="dc6be-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="dc6be-114">[![Ühe keskkonna kasutamisel on tootmise käivitamise faasid](media/mes-phases.png "Tootmise täideviimisfaasid ühe keskkonna kasutamisel")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="dc6be-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="dc6be-115">_Planeerimise_ faas hõlmab toote määratlust, planeerimist, tellimuse loomist ja ajastamist ning müügile laskmist.</span><span class="sxs-lookup"><span data-stu-id="dc6be-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="dc6be-116">Müügile laskmise etapp näitab üleminekut _planeerimise_ faasist _käivitamise_ faasi.</span><span class="sxs-lookup"><span data-stu-id="dc6be-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="dc6be-117">Kui tootmistellimus on müügile lastud, on tootmistellimuse tööd tootmiskorrusel nähtavad ja valmis täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="dc6be-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="dc6be-118">Kui tootmistöö on märgitud lõpetatuks, liigub see käivitamise _Käivitamise_ faasist _lõpetamise_ faasi.</span><span class="sxs-lookup"><span data-stu-id="dc6be-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="dc6be-119">_Lõpetamise_ faasis kinnitatakse *Käivitamise* faasi registreerimised läbi töövoo, kus need arvutatakse, kinnitatakse ja kantakse üle.</span><span class="sxs-lookup"><span data-stu-id="dc6be-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="dc6be-120">Sel hetkel on tootmistellimus lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="dc6be-120">At that point, the production order is completed.</span></span> <span data-ttu-id="dc6be-121">Seetõttu luuakse töötajate töötasu alus.</span><span class="sxs-lookup"><span data-stu-id="dc6be-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="dc6be-122">Käivitamise etapi tükeldamine eraldi töökoormuseks</span><span class="sxs-lookup"><span data-stu-id="dc6be-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="dc6be-123">Nagu järgmine illustratsioon näitab, kui kasutatakse astmiku ühikuid, tükeldatakse _Käivitamise_ faas eraldi töökoormusena.</span><span class="sxs-lookup"><span data-stu-id="dc6be-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="dc6be-124">[![Tootmise käivitamise faasid, kui kasutatakse astmiku ühikuid](media/mes-phases-workloads.png "Tootmise käivitamise faasid, kui kasutatakse astmiku ühikuid")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="dc6be-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="dc6be-125">Mudel läheb nüüd kohesest installist mudelile, mis põhineb keskusel ja skaala ühikutel.</span><span class="sxs-lookup"><span data-stu-id="dc6be-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="dc6be-126">Faasid _Plaanimine_ ja _Lõpetamine_ käivitatakse keskuses tagatoatoimingutena ja tootmise täideviimise töökoormus käivitatakse skaalaüksustes.</span><span class="sxs-lookup"><span data-stu-id="dc6be-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="dc6be-127">Andmed edastatakse asünkroonselt keskuse ja astmiku ühikute vahel.</span><span class="sxs-lookup"><span data-stu-id="dc6be-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="dc6be-128">Kui tootmistellimus vabastatakse keskuses, kantakse kõik tootmise tööde töötlemiseks vajalikud andmed üle skaalajaotise üksusse.</span><span class="sxs-lookup"><span data-stu-id="dc6be-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="dc6be-129">Need andmed hõlmavad tootmistellimusi, tootmisviise, materjaliarveid ja tooteid.</span><span class="sxs-lookup"><span data-stu-id="dc6be-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="dc6be-130">Andmed, mis ei ole seotud tootmistellimusega (nagu kaudsed tegevused, koodide puudumised ja tootmisprotsessi parameetrid), kantakse samuti keskusest üle astmiku ühikusse.</span><span class="sxs-lookup"><span data-stu-id="dc6be-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="dc6be-131">Reeglina, andmed, mis pärinevad keskusest ja mis kantakse üle skaala ühikule, saab luua või uuendada ainult keskuses.</span><span class="sxs-lookup"><span data-stu-id="dc6be-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="dc6be-132">Näiteks ei saa uut puudumise koodi või kaudset toimingut luua skaala ühikus&mdash;mida saab kasutada ainult registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="dc6be-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="dc6be-133">Mooduli käivitamisel tehtud registreerimised viiakse seejärel üle keskusesse, kus töödeldakse aja ja kohalolu kinnitust, laoseisu ja finantsvärskendusi.</span><span class="sxs-lookup"><span data-stu-id="dc6be-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="dc6be-134">Tootmise käivitamise toimingud, mida saab töömahu korral käitada</span><span class="sxs-lookup"><span data-stu-id="dc6be-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="dc6be-135">Järgmisi tootmise käivitamise toiminguid saab praegu käitada töömahu puhul, kui kasutatakse skaala ühikuid:</span><span class="sxs-lookup"><span data-stu-id="dc6be-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="dc6be-136">Sisseregistreerimine, sisselogimine, väljaregistreerimine ja puudumine</span><span class="sxs-lookup"><span data-stu-id="dc6be-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="dc6be-137">Alusta tööd</span><span class="sxs-lookup"><span data-stu-id="dc6be-137">Start job</span></span>
- <span data-ttu-id="dc6be-138">Tööde kogum</span><span class="sxs-lookup"><span data-stu-id="dc6be-138">Bundle jobs</span></span>
- <span data-ttu-id="dc6be-139">Edenemisest teadaandmine</span><span class="sxs-lookup"><span data-stu-id="dc6be-139">Report progress</span></span>
- <span data-ttu-id="dc6be-140">Teata praagist</span><span class="sxs-lookup"><span data-stu-id="dc6be-140">Report scrap</span></span>
- <span data-ttu-id="dc6be-141">Kaudne tegevus</span><span class="sxs-lookup"><span data-stu-id="dc6be-141">Indirect activity</span></span>
- <span data-ttu-id="dc6be-142">Paus</span><span class="sxs-lookup"><span data-stu-id="dc6be-142">Break</span></span>
- <span data-ttu-id="dc6be-143">Teata lõpetamisest ja ära panemisest (nõuab, et käivitate ka lao käivitamise töökoormuse oma kaaluühikul, vt ka [Lõpetatuna kinnitamine ja mõõtude laadimine kaaluühikul](#RAF))</span><span class="sxs-lookup"><span data-stu-id="dc6be-143">Report as finished and putaway (requires that you also run the warehouse execution workload on your scale unit, see also [Report as finished and putaway on a scale unit](#RAF))</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="dc6be-144">Töötamine tootmise käivitamise töömahuga keskuses</span><span class="sxs-lookup"><span data-stu-id="dc6be-144">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="dc6be-145">Tavaliselt käivituvad tootmise käivitamise töökoormuse käitamiseks vajalikud protsessid automaatselt, et hoida keskus ja kõik ühikud sünkroonis vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="dc6be-145">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="dc6be-146">Kuid kui teil on probleeme, saate käsitsi käivitada töötlemata registreerimiste töötluse, mis on saadud töömahustt ja/või kontrollida registreerimise töötluse logi.</span><span class="sxs-lookup"><span data-stu-id="dc6be-146">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="dc6be-147">Töötlemata registreerimiste käsitsi töötlemine</span><span class="sxs-lookup"><span data-stu-id="dc6be-147">Manually process raw registrations</span></span>

<span data-ttu-id="dc6be-148">Pakett-töö töötleb rakenduses Supply Chain Management automaatselt kõiki töökoormusest saadud registreerimisi.</span><span class="sxs-lookup"><span data-stu-id="dc6be-148">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="dc6be-149">See töö loob nõutavad tootmis töölehed ja logiraamatu kirjed, kui valmis tööle on töömahus registreeritud.</span><span class="sxs-lookup"><span data-stu-id="dc6be-149">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="dc6be-150">Kuigi töö tavaliselt käivitub automaatselt, saate selle käivitada käsitsi mis tahes ajal, logides keskusesse sisse ja minnes **Tootmise kontrolli \> Perioodilised ülesanded \> BackOffice töömahu haldamise \> Töötle töötlemata registreerimisi**.</span><span class="sxs-lookup"><span data-stu-id="dc6be-150">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="dc6be-151">Kontrollige töötlemata registreerimise töötluse logis</span><span class="sxs-lookup"><span data-stu-id="dc6be-151">Check the raw registration processing log</span></span>

<span data-ttu-id="dc6be-152">Registreerimise töötlemise Logi ülevaatamiseks logige keskusesse sisse ja minge **Tootmise juhtimise \> Perioodiliste ülesannete \> BackOffice töökoormuse haldamine \> töötlemata registreerimise töötlemise Logi**.</span><span class="sxs-lookup"><span data-stu-id="dc6be-152">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="dc6be-153">Lehel **Töötlemata registreerimise töötluse logi** kuvatakse töötlemata registreerimiste loend ja iga registreerimise olek.</span><span class="sxs-lookup"><span data-stu-id="dc6be-153">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="dc6be-154">![Töötlemata registreerimise töötluse logi](media/mes-processing-log.png "Töötlemata registreerimise töötluse logi")</span><span class="sxs-lookup"><span data-stu-id="dc6be-154">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="dc6be-155">Saate töötada mis tahes registreerimisega loendis valides selle ja seejärel valides Tegevuse Paanilt ühe järgmistest nuppudest:</span><span class="sxs-lookup"><span data-stu-id="dc6be-155">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="dc6be-156">**Töötle** – Valitud registreerimise käsitsi töötlemine.</span><span class="sxs-lookup"><span data-stu-id="dc6be-156">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="dc6be-157">See tegevus võib olla kasulik, kui _Protsessi töötlemata registreerimiste_ töö pole käivitatud või kui see nurjus.</span><span class="sxs-lookup"><span data-stu-id="dc6be-157">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="dc6be-158">**Tühista** – valitud registreeringu tühistamine.</span><span class="sxs-lookup"><span data-stu-id="dc6be-158">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="dc6be-159">Töötamine tootmise käivitamise töömahuga skaalaühikus</span><span class="sxs-lookup"><span data-stu-id="dc6be-159">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="dc6be-160">Tavaliselt käivituvad tootmise käivitamise töökoormuse käitamiseks vajalikud protsessid automaatselt, et hoida keskus ja kõik ühikud sünkroonis vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="dc6be-160">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="dc6be-161">Kui teil on probleeme, saate kontrollida skaala ühikus töödeldud tellimuste ajalugu või käitada käsitsi _Tootmise keskust, et mastaapida ühiku teate protsessori_ töö.</span><span class="sxs-lookup"><span data-stu-id="dc6be-161">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="dc6be-162">Vaata skaalaühikus töödeldud tootmistööde ajalugu</span><span class="sxs-lookup"><span data-stu-id="dc6be-162">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="dc6be-163">Skaala ühikus töödeldud tööde ajaloo ülevaatamiseks logige sisse skaala ühiku masinasse ja minge **Tootmise juhtimise \> Perioodiliste ülesannete \> BackOffice töökoormuse haldamine \> Tööde töötlemise ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="dc6be-163">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="dc6be-164">Lehel **Tootmise tööde töötluse ajalugu** kuvatakse tootmistellimuste töötluse ajalugu skaalaühikul.</span><span class="sxs-lookup"><span data-stu-id="dc6be-164">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="dc6be-165">Saate töötada mis tahes tootmistellimusega loendis valides selle ja seejärel valides Tegevuse Paanilt ühe järgmistest nuppudest:</span><span class="sxs-lookup"><span data-stu-id="dc6be-165">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="dc6be-166">**Töötle** – Valitud tootmistellimuse käsitsi töötlemine.</span><span class="sxs-lookup"><span data-stu-id="dc6be-166">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="dc6be-167">**Tühista** – Tühistab valitud tootmistellimuse.</span><span class="sxs-lookup"><span data-stu-id="dc6be-167">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="dc6be-168">Tootmiskeskus skaala ühiku teade protsessori töö jaoks</span><span class="sxs-lookup"><span data-stu-id="dc6be-168">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="dc6be-169">_Tootmise keskus skaala ühiku teade protsessori_ töö töötleb andmeid keskusest skaala ühikule.</span><span class="sxs-lookup"><span data-stu-id="dc6be-169">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="dc6be-170">See töö käivitatakse automaatselt, kui tootmise käivitamise töökoormus on kasutusel.</span><span class="sxs-lookup"><span data-stu-id="dc6be-170">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="dc6be-171">Kuid saate seda käitada käsitsi igal ajal, minnes **Tootmise juhtimise \> Perioodiliste ülesannete \> BackOffice töökoormuse halduse \> Tootmise keskusestt skaala ühiku teate protsessorisse**.</span><span class="sxs-lookup"><span data-stu-id="dc6be-171">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

<a name="RAF"></a>

## <a name="report-as-finished-and-putaway-on-a-scale-unit"></a><span data-ttu-id="dc6be-172">Lõpetamisest ja kõrvale panekust teatamine kaaluühikul</span><span class="sxs-lookup"><span data-stu-id="dc6be-172">Report as finished and putaway on a scale unit</span></span>

<!-- KFM: 
This section describes how to enable the abilities to report as finished and then putaway finished items when you are using to a scale unit.

### Enable and use report as finished and putaway on a scale unit -->

<span data-ttu-id="dc6be-173">Selles väljaandes teavitatakse lõpp- ja varjatud toimingutest (valmistoodete, kaastoodete ja kõrvalsaaduste puhul) mis on toeatatud [varude täiskoormuse puhul](cloud-edge-workload-warehousing.md) (mitte tootmise täiskoormuse puhul).</span><span class="sxs-lookup"><span data-stu-id="dc6be-173">In the current release, report as finished and putaway operations (for finished products, co-products, and by-products) are supported by the [warehouse execution workload](cloud-edge-workload-warehousing.md) (not the manufacturing execution workload).</span></span> <span data-ttu-id="dc6be-174">Seetõttu peate selle funktsiooni kasutamiseks, kui see on ühendatud kaaluühikuga, tegema järgmist:</span><span class="sxs-lookup"><span data-stu-id="dc6be-174">Therefore, to use this functionality when connected to a scale unit, you must do the following:</span></span>

- <span data-ttu-id="dc6be-175">Installige oma kaaluühikusse nii lao käivitamise töökoormus kui ka tootmise käivitamise töökoormus.</span><span class="sxs-lookup"><span data-stu-id="dc6be-175">Install both the warehouse execution workload and the manufacturing execution workload on your scale unit.</span></span>
- <span data-ttu-id="dc6be-176">Warehouse Management mobiilirakenduse abil saate teatada lõpetatund ja töödeldud töödest.</span><span class="sxs-lookup"><span data-stu-id="dc6be-176">Use the Warehouse Management mobile app to report as finished and process the putaway work.</span></span> <span data-ttu-id="dc6be-177">Tootmispinna käivitamise liides ei toeta praegu neid protsesse.</span><span class="sxs-lookup"><span data-stu-id="dc6be-177">The production floor execution interface does not currently support these processes.</span></span>

<!-- KFM: API details needed

### Customize report as finished and putaway functionality

 -->

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
