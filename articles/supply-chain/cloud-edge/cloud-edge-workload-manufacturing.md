---
title: Tootmise täideviimise töökoormused pilv- ja perimeeterskaalaüksuste jaoks
description: See teema kirjeldab, kuidas tootmise läbiviimise töömahud töötavad koos pilv- ja perimeeterskaalaüksustega.
author: cabeln
manager: ''
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 6bef28d16236a7862550f3ab87f73baf8dab97b0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251070"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="177e7-103">Tootmise täideviimise töökoormused pilv- ja perimeeterskaalaüksuste jaoks</span><span class="sxs-lookup"><span data-stu-id="177e7-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="177e7-104">Mõni ettevõtte funktsionaalsus ei ole avalikus eelvaates täielikult toetatud juhul, kui kasutatakse töökoormuse skaalaüksusi.</span><span class="sxs-lookup"><span data-stu-id="177e7-104">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="177e7-105">Tootmise käitamisel tarnivad pilve ja perimeeterskaala üksused järgmised võimalused, isegi kui perimeeterskaala üksused pole jaoturiga ühendatud:</span><span class="sxs-lookup"><span data-stu-id="177e7-105">In manufacturing execution, cloud and edge scale units deliver the following capabilities, even when edge units aren't connected to the hub:</span></span>

- <span data-ttu-id="177e7-106">Masina operaatorid ja tööde juhtimise haldurid pääsevad ligi operatiivsele tootmisplaanile.</span><span class="sxs-lookup"><span data-stu-id="177e7-106">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="177e7-107">Masina operaatorid saavad plaani ajakohasena hoida, töötades eraldi ja menetledes tootmise töid.</span><span class="sxs-lookup"><span data-stu-id="177e7-107">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="177e7-108">Tööde juhtimise haldur saab tegevuskava korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="177e7-108">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="177e7-109">Töötajatel on juurdepääs aja ja kohalolekt sisse-ja väljaregistreerimisele serval, et tagada õiglane töötaja tasu arvutamine.</span><span class="sxs-lookup"><span data-stu-id="177e7-109">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="177e7-110">See teema kirjeldab, kuidas tootmise läbiviimise töömahud töötavad koos pilv- ja perimeeterskaalaüksustega.</span><span class="sxs-lookup"><span data-stu-id="177e7-110">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="177e7-111">Tootmise elutsükkel</span><span class="sxs-lookup"><span data-stu-id="177e7-111">The manufacturing lifecycle</span></span>

<span data-ttu-id="177e7-112">Nagu järgnev illustratsioon näitab, on tootmise elutsükkel jagatud kolmeks faasiks: *Planeeri*, *Käivita* ja *Lõpeta*.</span><span class="sxs-lookup"><span data-stu-id="177e7-112">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="177e7-113">[![Ühe keskkonna kasutamisel on tootmise käivitamise faasid](media/mes-phases.png "Tootmise täideviimisfaasid ühe keskkonna kasutamisel")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="177e7-113">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="177e7-114">_Planeerimise_ faas hõlmab toote määratlust, planeerimist, tellimuse loomist ja ajastamist ning müügile laskmist.</span><span class="sxs-lookup"><span data-stu-id="177e7-114">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="177e7-115">Müügile laskmise etapp näitab üleminekut _planeerimise_ faasist _käivitamise_ faasi.</span><span class="sxs-lookup"><span data-stu-id="177e7-115">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="177e7-116">Kui tootmistellimus on müügile lastud, on tootmistellimuse tööd tootmiskorrusel nähtavad ja valmis täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="177e7-116">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="177e7-117">Kui tootmistöö on märgitud lõpetatuks, liigub see käivitamise _Käivitamise_ faasist _lõpetamise_ faasi.</span><span class="sxs-lookup"><span data-stu-id="177e7-117">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="177e7-118">_Lõpetamise_ faasis kinnitatakse *Käivitamise* faasi registreerimised läbi töövoo, kus need arvutatakse, kinnitatakse ja kantakse üle.</span><span class="sxs-lookup"><span data-stu-id="177e7-118">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="177e7-119">Sel hetkel on tootmistellimus lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="177e7-119">At that point, the production order is completed.</span></span> <span data-ttu-id="177e7-120">Seetõttu luuakse töötajate töötasu alus.</span><span class="sxs-lookup"><span data-stu-id="177e7-120">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="177e7-121">Käivitamise etapi tükeldamine eraldi töökoormuseks</span><span class="sxs-lookup"><span data-stu-id="177e7-121">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="177e7-122">Nagu järgmine illustratsioon näitab, kui kasutatakse astmiku ühikuid, tükeldatakse _Käivitamise_ faas eraldi töökoormusena.</span><span class="sxs-lookup"><span data-stu-id="177e7-122">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="177e7-123">[![Tootmise käivitamise faasid, kui kasutatakse astmiku ühikuid](media/mes-phases-workloads.png "Tootmise käivitamise faasid, kui kasutatakse astmiku ühikuid")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="177e7-123">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="177e7-124">Mudel läheb nüüd kohesest installist mudelile, mis põhineb keskusel ja skaala ühikutel.</span><span class="sxs-lookup"><span data-stu-id="177e7-124">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="177e7-125">Faasid _Plaanimine_ ja _Lõpetamine_ käivitatakse keskuses tagatoatoimingutena ja tootmise täideviimise töökoormus käivitatakse skaalaüksustes.</span><span class="sxs-lookup"><span data-stu-id="177e7-125">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="177e7-126">Andmed edastatakse asünkroonselt keskuse ja astmiku ühikute vahel.</span><span class="sxs-lookup"><span data-stu-id="177e7-126">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="177e7-127">Kui tootmistellimus vabastatakse keskuses, kantakse kõik tootmise tööde töötlemiseks vajalikud andmed üle skaalajaotise üksusse.</span><span class="sxs-lookup"><span data-stu-id="177e7-127">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="177e7-128">Need andmed hõlmavad tootmistellimusi, tootmisviise, materjaliarveid ja tooteid.</span><span class="sxs-lookup"><span data-stu-id="177e7-128">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="177e7-129">Andmed, mis ei ole seotud tootmistellimusega (nagu kaudsed tegevused, koodide puudumised ja tootmisprotsessi parameetrid), kantakse samuti keskusest üle astmiku ühikusse.</span><span class="sxs-lookup"><span data-stu-id="177e7-129">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="177e7-130">Reeglina, andmed, mis pärinevad keskusest ja mis kantakse üle skaala ühikule, saab luua või uuendada ainult keskuses.</span><span class="sxs-lookup"><span data-stu-id="177e7-130">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="177e7-131">Näiteks ei saa uut puudumise koodi või kaudset toimingut luua skaala ühikus&mdash;mida saab kasutada ainult registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="177e7-131">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="177e7-132">Mooduli käivitamisel tehtud registreerimised viiakse seejärel üle keskusesse, kus töödeldakse aja ja kohalolu kinnitust, laoseisu ja finantsvärskendusi.</span><span class="sxs-lookup"><span data-stu-id="177e7-132">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="177e7-133">Tootmise käivitamise toimingud, mida saab töömahu korral käitada</span><span class="sxs-lookup"><span data-stu-id="177e7-133">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="177e7-134">Järgmisi tootmise käivitamise toiminguid saab praegu käitada töömahu puhul, kui kasutatakse skaala ühikuid:</span><span class="sxs-lookup"><span data-stu-id="177e7-134">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="177e7-135">Sisseregistreerimine, sisselogimine, väljaregistreerimine ja puudumine</span><span class="sxs-lookup"><span data-stu-id="177e7-135">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="177e7-136">Alusta tööd</span><span class="sxs-lookup"><span data-stu-id="177e7-136">Start job</span></span>
- <span data-ttu-id="177e7-137">Tööde kogum</span><span class="sxs-lookup"><span data-stu-id="177e7-137">Bundle jobs</span></span>
- <span data-ttu-id="177e7-138">Edenemisest teadaandmine</span><span class="sxs-lookup"><span data-stu-id="177e7-138">Report progress</span></span>
- <span data-ttu-id="177e7-139">Teata praagist</span><span class="sxs-lookup"><span data-stu-id="177e7-139">Report scrap</span></span>
- <span data-ttu-id="177e7-140">Kaudne tegevus</span><span class="sxs-lookup"><span data-stu-id="177e7-140">Indirect activity</span></span>
- <span data-ttu-id="177e7-141">Paus</span><span class="sxs-lookup"><span data-stu-id="177e7-141">Break</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="177e7-142">Töötamine tootmise käivitamise töömahuga keskuses</span><span class="sxs-lookup"><span data-stu-id="177e7-142">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="177e7-143">Tavaliselt käivituvad tootmise käivitamise töökoormuse käitamiseks vajalikud protsessid automaatselt, et hoida keskus ja kõik ühikud sünkroonis vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="177e7-143">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="177e7-144">Kuid kui teil on probleeme, saate käsitsi käivitada töötlemata registreerimiste töötluse, mis on saadud töömahustt ja/või kontrollida registreerimise töötluse logi.</span><span class="sxs-lookup"><span data-stu-id="177e7-144">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="177e7-145">Töötlemata registreerimiste käsitsi töötlemine</span><span class="sxs-lookup"><span data-stu-id="177e7-145">Manually process raw registrations</span></span>

<span data-ttu-id="177e7-146">Pakett-töö töötleb rakenduses Supply Chain Management automaatselt kõiki töökoormusest saadud registreerimisi.</span><span class="sxs-lookup"><span data-stu-id="177e7-146">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="177e7-147">See töö loob nõutavad tootmis töölehed ja logiraamatu kirjed, kui valmis tööle on töömahus registreeritud.</span><span class="sxs-lookup"><span data-stu-id="177e7-147">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="177e7-148">Kuigi töö tavaliselt käivitub automaatselt, saate selle käivitada käsitsi mis tahes ajal, logides keskusesse sisse ja minnes **Tootmise kontrolli \> Perioodilised ülesanded \> BackOffice töömahu haldamise \> Töötle töötlemata registreerimisi**.</span><span class="sxs-lookup"><span data-stu-id="177e7-148">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="177e7-149">Kontrollige töötlemata registreerimise töötluse logis</span><span class="sxs-lookup"><span data-stu-id="177e7-149">Check the raw registration processing log</span></span>

<span data-ttu-id="177e7-150">Registreerimise töötlemise Logi ülevaatamiseks logige keskusesse sisse ja minge **Tootmise juhtimise \> Perioodiliste ülesannete \> BackOffice töökoormuse haldamine \> töötlemata registreerimise töötlemise Logi**.</span><span class="sxs-lookup"><span data-stu-id="177e7-150">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="177e7-151">Lehel **Töötlemata registreerimise töötluse logi** kuvatakse töötlemata registreerimiste loend ja iga registreerimise olek.</span><span class="sxs-lookup"><span data-stu-id="177e7-151">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="177e7-152">![Töötlemata registreerimise töötluse logi](media/mes-processing-log.png "Töötlemata registreerimise töötluse logi")</span><span class="sxs-lookup"><span data-stu-id="177e7-152">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="177e7-153">Saate töötada mis tahes registreerimisega loendis valides selle ja seejärel valides Tegevuse Paanilt ühe järgmistest nuppudest:</span><span class="sxs-lookup"><span data-stu-id="177e7-153">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="177e7-154">**Töötle** – Valitud registreerimise käsitsi töötlemine.</span><span class="sxs-lookup"><span data-stu-id="177e7-154">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="177e7-155">See tegevus võib olla kasulik, kui _Protsessi töötlemata registreerimiste_ töö pole käivitatud või kui see nurjus.</span><span class="sxs-lookup"><span data-stu-id="177e7-155">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="177e7-156">**Tühista** – valitud registreeringu tühistamine.</span><span class="sxs-lookup"><span data-stu-id="177e7-156">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="177e7-157">Töötamine tootmise käivitamise töömahuga skaalaühikus</span><span class="sxs-lookup"><span data-stu-id="177e7-157">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="177e7-158">Tavaliselt käivituvad tootmise käivitamise töökoormuse käitamiseks vajalikud protsessid automaatselt, et hoida keskus ja kõik ühikud sünkroonis vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="177e7-158">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="177e7-159">Kui teil on probleeme, saate kontrollida skaala ühikus töödeldud tellimuste ajalugu või käitada käsitsi _Tootmise keskust, et mastaapida ühiku teate protsessori_ töö.</span><span class="sxs-lookup"><span data-stu-id="177e7-159">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="177e7-160">Vaata skaalaühikus töödeldud tootmistööde ajalugu</span><span class="sxs-lookup"><span data-stu-id="177e7-160">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="177e7-161">Skaala ühikus töödeldud tööde ajaloo ülevaatamiseks logige sisse skaala ühiku masinasse ja minge **Tootmise juhtimise \> Perioodiliste ülesannete \> BackOffice töökoormuse haldamine \> Tööde töötlemise ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="177e7-161">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="177e7-162">Lehel **Tootmise tööde töötluse ajalugu** kuvatakse tootmistellimuste töötluse ajalugu skaalaühikul.</span><span class="sxs-lookup"><span data-stu-id="177e7-162">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="177e7-163">Saate töötada mis tahes tootmistellimusega loendis valides selle ja seejärel valides Tegevuse Paanilt ühe järgmistest nuppudest:</span><span class="sxs-lookup"><span data-stu-id="177e7-163">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="177e7-164">**Töötle** – Valitud tootmistellimuse käsitsi töötlemine.</span><span class="sxs-lookup"><span data-stu-id="177e7-164">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="177e7-165">**Tühista** – Tühistab valitud tootmistellimuse.</span><span class="sxs-lookup"><span data-stu-id="177e7-165">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="177e7-166">Tootmiskeskus skaala ühiku teade protsessori töö jaoks</span><span class="sxs-lookup"><span data-stu-id="177e7-166">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="177e7-167">_Tootmise keskus skaala ühiku teade protsessori_ töö töötleb andmeid keskusest skaala ühikule.</span><span class="sxs-lookup"><span data-stu-id="177e7-167">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="177e7-168">See töö käivitatakse automaatselt, kui tootmise käivitamise töökoormus on kasutusel.</span><span class="sxs-lookup"><span data-stu-id="177e7-168">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="177e7-169">Kuid saate seda käitada käsitsi igal ajal, minnes **Tootmise juhtimise \> Perioodiliste ülesannete \> BackOffice töökoormuse halduse \> Tootmise keskusestt skaala ühiku teate protsessorisse**.</span><span class="sxs-lookup"><span data-stu-id="177e7-169">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]