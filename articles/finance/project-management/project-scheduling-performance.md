---
title: Projekti ressursi plaanimise tulemused
description: Selles teemas antakse teavet selle kohta, kuidas parandada suure hulga projektide ressursi planeerimise tulemusi.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760529"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="eebef-103">Projekti ressursi plaanimise tulemused</span><span class="sxs-lookup"><span data-stu-id="eebef-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="eebef-104">Ressursi planeerimise tulemustega seotud probleemid võivad ilmneda siis, kui projektide arv jõuab tuhandeteni.</span><span class="sxs-lookup"><span data-stu-id="eebef-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="eebef-105">Ressursi planeerimise tulemuste parandamiseks on saadaval funktsioon, mis võimaldab kasutajatel ressursi kättesaadavuse vormi käivitamiseks kuluvat aega vähendada.</span><span class="sxs-lookup"><span data-stu-id="eebef-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="eebef-106">See eemaldab ressursi tulemuste kokkuvõtete sünkroonimisprotsessi ja kasutab ressursiotsingu kiirendamiseks tabelit **ResProjectResource**.</span><span class="sxs-lookup"><span data-stu-id="eebef-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="eebef-107">Pange tähele, et tabelit **ResRollup** enam ei kasutata.</span><span class="sxs-lookup"><span data-stu-id="eebef-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="eebef-108">Kui ressursi tulemuste kokkuvõtete sünkroonimisprotsessist või tabelist **ResProjectResource** on sõltuvus, ärge seda funktsiooni kasutage.</span><span class="sxs-lookup"><span data-stu-id="eebef-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="eebef-109">Ressursi ajastamise toimivuse täiustamise lubamine</span><span class="sxs-lookup"><span data-stu-id="eebef-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="eebef-110">Ressursi ajastamise toimivuse täiustamise lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="eebef-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="eebef-111">Avage **Funktsioonihaldus** > **Kõik** ja otsige funktsioonide loendist üles suvand **Luba projekti ressursi ajastamise toimivuse täiustamise funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="eebef-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="eebef-112">Valige **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="eebef-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="eebef-113">Kui te ei leia funktsiooni loendist, tehke loendi värskendamiseks valik **Otsi värskendusi**.</span><span class="sxs-lookup"><span data-stu-id="eebef-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="eebef-114">Värskendage oma brauserit ja seejärel avage **Projektihaldus ja -arvestus** > **Perioodilised** > **Projekti ressursid** > **Sünkrooni ressursi kalendrite võimsust kõigis ettevõtetes**.</span><span class="sxs-lookup"><span data-stu-id="eebef-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="eebef-115">Eelmiste andmete eemaldamiseks seadke suvandi **Eemalda olemasolevad võimsuse kirjed** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="eebef-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="eebef-116">Kui soovite luua inkrementandmeid, seadke selle väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="eebef-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="eebef-117">Valige väljal **Perioodi kood** periood, mille jooksul tuleks andmed genereerida.</span><span class="sxs-lookup"><span data-stu-id="eebef-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="eebef-118">Kui valite perioodi koodi, ei pea te algus- ja lõppkuupäeva määratlema.</span><span class="sxs-lookup"><span data-stu-id="eebef-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="eebef-119">Kui jätate välja **Perioodi kood** tühjaks, valige teabe loomiseks kindlad algus- ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="eebef-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="eebef-120">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="eebef-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="eebef-121">See jaotab üldandmed tabelisse **ResCalendarCapacity** kõigis teie keskkonna ettevõtetes, seega tuleb pakett-tööd käitada ainult ühes juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="eebef-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="eebef-122">Selle pakett-töö andmeid on vaja ressursi tulemuste arvutamiseks seostuva kalendri kaudu.</span><span class="sxs-lookup"><span data-stu-id="eebef-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="eebef-123">Avage **Projektihaldus ja -arvestus** > **Perioodilised** > **Projekti ressursid** > **Asusta projekti ressursid kõigis ettevõtetes** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="eebef-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="eebef-124">See on üldandmete täiendamise skript tabelites **ResProjectResource**, **ResCalendarDateTimeRange** ja **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="eebef-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="eebef-125">Uuendatakse ka välja **PSAPRojSchedRole.RootActivity** väärtusi.</span><span class="sxs-lookup"><span data-stu-id="eebef-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="eebef-126">Kui seda ei käitata, kuvatakse ressursi ajastamise toimingute käivitamisel hoiatus.</span><span class="sxs-lookup"><span data-stu-id="eebef-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="eebef-127">Ressursi ajastamise toimivuse täiustamise väljalülitamine</span><span class="sxs-lookup"><span data-stu-id="eebef-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="eebef-128">Avage **Funktsioonihaldus** > **Kõik** ja otsige üles suvand **Luba projekti ressursi ajastamise toimivuse täiustamise funktsioon**.</span><span class="sxs-lookup"><span data-stu-id="eebef-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="eebef-129">Valige funktsioon ja seejärel valige nupp **Keela**.</span><span class="sxs-lookup"><span data-stu-id="eebef-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="eebef-130">Värskendage oma brauserit.</span><span class="sxs-lookup"><span data-stu-id="eebef-130">Refresh your browser.</span></span>
4. <span data-ttu-id="eebef-131">Valige **Projektihaldus ja raamatupidamine** > **Perioodiline** > **Võimsuse sünkroonimine** > **Ressursside võimsuse kokkuvõtete sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="eebef-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="eebef-132">Varasemate andmete eemaldamiseks seadke lehel **Tulemuste kokkuvõtete sünkroonimine** suvandi **Eemalda olemasolevad võimsuse kirjed** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="eebef-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="eebef-133">Kui soovite luua inkrementandmeid, seadke selle väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="eebef-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="eebef-134">Valige väljal **Perioodi kood** periood, mille jooksul tuleks andmed genereerida.</span><span class="sxs-lookup"><span data-stu-id="eebef-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="eebef-135">Kui valite perioodi koodi, ei pea te algus- ja lõppkuupäeva määratlema.</span><span class="sxs-lookup"><span data-stu-id="eebef-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="eebef-136">Kui jätate välja **Perioodi kood** tühjaks, valige teabe loomiseks kindlad algus- ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="eebef-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="eebef-137">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="eebef-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="eebef-138">See jaotab üldandmed tabelisse **ResRollup** kõigis teie keskkonna ettevõtetes, seega tuleb pakett-tööd käitada ainult ühes juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="eebef-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="eebef-139">See pakett-töö on vajalik kõigi vaadete **Ressursi kättesaadavus** korral.</span><span class="sxs-lookup"><span data-stu-id="eebef-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="eebef-140">Kui seda pakett-tööd ei käitata, luuakse **ResRollupi** andmed käigu pealt, mis võib aega võtta.</span><span class="sxs-lookup"><span data-stu-id="eebef-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
