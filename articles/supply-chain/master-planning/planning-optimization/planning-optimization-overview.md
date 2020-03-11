---
title: Planeerimise optimeerimise ülevaade
description: Selles teemas antakse planeerimise optimeerimise funktsioonist ülevaade.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9ccf00b6fcd1e3a6002086360b1a4c5c464ba054
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076151"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="ca231-103">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="ca231-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="ca231-104">Rakenduse Microsoft Dynamics 365 Supply Chain Management planeerimise optimeerimise lisandmoodul võimaldab koondplaneerimise arvutuste tegemist väljaspool Dynamics 365 Supply Chain Managementi ja seotud SQL-andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="ca231-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="ca231-105">Planeerimise optimeerimise funktsiooniga seotud eelised hõlmavad paremat jõudlust ja minimaalset mõju SQL-andmebaasile koondplaneerimise käivitamiste ajal.</span><span class="sxs-lookup"><span data-stu-id="ca231-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="ca231-106">Kiireid planeerimise käivitamisi saab teha isegi kontoris viibimise ajal, seega saavad planeerijad nõudlusele või parameetri muutustele kohe reageerida.</span><span class="sxs-lookup"><span data-stu-id="ca231-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="ca231-107">Planeerimise optimeerimise kasutamiseks peate installima planeerimise optimeerimise lisandmooduli oma projektist portaalis Microsoft Dynamics Lifecycle Services (LCS) ja lülitama planeerimise optimeerimise funktsiooni tarneahela halduses sisse.</span><span class="sxs-lookup"><span data-stu-id="ca231-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="ca231-108">Lisateavet vt [Planeerimise optimeerimise kasutamise alustamine](get-started.md).</span><span class="sxs-lookup"><span data-stu-id="ca231-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="ca231-109">Järgmisel joonisel on näha planeerimise optimeerimise kontoris viibimise ajal käivitamise eelis.</span><span class="sxs-lookup"><span data-stu-id="ca231-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Planeerimise optimeerimise kontoris viibimise ajal käitamise eelis](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="ca231-111">Parem jõudlus</span><span class="sxs-lookup"><span data-stu-id="ca231-111">Improved performance</span></span>

<span data-ttu-id="ca231-112">Planeerimise optimeerimist saab kasutada stsenaariumides, mis hõlmavad pikaajalisi koondplaane.</span><span class="sxs-lookup"><span data-stu-id="ca231-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="ca231-113">See on spetsiaalselt loodud väga kiirete arvutuste jaoks, mis hõlmavad väga suurt hulka andmeid.</span><span class="sxs-lookup"><span data-stu-id="ca231-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="ca231-114">Kuna see on loodud hüperskaleeritava mitme rentnikuga teenusena, saavad mitu üksust plaani arvutamiseks samaaegselt koos töötada.</span><span class="sxs-lookup"><span data-stu-id="ca231-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="ca231-115">Lisaks eemaldab planeerimise teenus teie süsteemist koondplaneerimise koormuse ja töötab andmevooga, mis vähendab serveri koormust.</span><span class="sxs-lookup"><span data-stu-id="ca231-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="ca231-116">Planeerimise optimeerimine saab aidata teil saavutada järgmisi eesmärke.</span><span class="sxs-lookup"><span data-stu-id="ca231-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="ca231-117">Planeerimise jõudluse parandamine lühema käitamisaja kaudu.</span><span class="sxs-lookup"><span data-stu-id="ca231-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="ca231-118">Koondplaneerimise käivitamise ajal teistele protsessidele avaldatava mõju vähendamine.</span><span class="sxs-lookup"><span data-stu-id="ca231-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="ca231-119">Sagedasem planeerimise käivitamiste tegemine.</span><span class="sxs-lookup"><span data-stu-id="ca231-119">Do more frequent planning runs.</span></span> <span data-ttu-id="ca231-120">(Te pole piiratud igapäevaste käivitustega.)</span><span class="sxs-lookup"><span data-stu-id="ca231-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="ca231-121">Saate olla kindlad, et äri kasvamine tulevikus ei koorma planeerimise süsteemi üle.</span><span class="sxs-lookup"><span data-stu-id="ca231-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="ca231-122">Arhitektuur ja andmevoog</span><span class="sxs-lookup"><span data-stu-id="ca231-122">Architecture and data flow</span></span>

<span data-ttu-id="ca231-123">Kui planeerimise optimeerimise lisandmoodul on LCS-ist installitud, luuakse turvaline ühendus planeerimise optimeerimise teenusega.</span><span class="sxs-lookup"><span data-stu-id="ca231-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="ca231-124">Teenus asub samas andmekeskuse riigis või piirkonnas kui seotud tarneahela halduse eksemplar.</span><span class="sxs-lookup"><span data-stu-id="ca231-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="ca231-125">Pärast planeerimise optimeerimise seadistamist kui käivitatakse koondplaneerimist, saadetakse koondandmed ja kandeandmed tarneahela haldusest planeerimise optimeerimise teenusesse.</span><span class="sxs-lookup"><span data-stu-id="ca231-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="ca231-126">Kui planeerimise optimeerimise lisandmoodul desinstallitakse, eemaldatakse kõik planeerimise optimeerimise teenusega seotud andmed.</span><span class="sxs-lookup"><span data-stu-id="ca231-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="ca231-127">Kõrgetasemeline andmevoog taasloomise käivitusteks</span><span class="sxs-lookup"><span data-stu-id="ca231-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="ca231-128">Tarneahela halduse klient saadab signaali, et taotleda planeerimise optimeerimiselt planeerimise käivitust.</span><span class="sxs-lookup"><span data-stu-id="ca231-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="ca231-129">Planeerimise optimeerimine taotleb integreeritud konnektori kaudu vajalikke andmeid.</span><span class="sxs-lookup"><span data-stu-id="ca231-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="ca231-130">SQL-andmebaas saadab taotletud teabe häälestuse, koondandmete ja kandeandmete kohta konnektori kaudu planeerimise optimeerimisse.</span><span class="sxs-lookup"><span data-stu-id="ca231-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="ca231-131">Konnektor tõlgendab teavet tarneahela halduse ja planeerimise optimeerimise teenuse vahel.</span><span class="sxs-lookup"><span data-stu-id="ca231-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="ca231-132">Planeerimise optimeerimise teenus hoiab planeerimisega seotud andmeid mälus ja teeb vajalikud arvutused.</span><span class="sxs-lookup"><span data-stu-id="ca231-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="ca231-133">Planeerimise tulemus saadetakse konnektori kaudu tarneahela halduse andmebaasile.</span><span class="sxs-lookup"><span data-stu-id="ca231-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="ca231-134">Tulemused hõlmavad teavet, nagu plaanitud tellimused ja sidumisandmed.</span><span class="sxs-lookup"><span data-stu-id="ca231-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="ca231-135">Planeerimise optimeerimine saadab signaali tarneahela haldusele, et näidata, et planeerimise käivitamine on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="ca231-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="ca231-136">See saadab ka kõik asjakohased teated ja hoiatused.</span><span class="sxs-lookup"><span data-stu-id="ca231-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="ca231-137">Järgmine illustratsioon näitab andmevoogu.</span><span class="sxs-lookup"><span data-stu-id="ca231-137">The following illustration shows the data flow.</span></span>

![Andmevoog taasloomise käivitusteks](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="ca231-139">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="ca231-139">Related resources</span></span>

[<span data-ttu-id="ca231-140">Planeerimise optimiseerimise kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="ca231-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="ca231-141">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="ca231-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="ca231-142">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="ca231-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="ca231-143">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="ca231-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="ca231-144">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="ca231-144">Cancel a planning job</span></span>](cancel-planning-job.md)
