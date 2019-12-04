---
title: Planeerimise optimiseerimise kasutamise alustamine
description: Selles teemas selgitatakse, kuidas hakata kasutama planeerimise optimeerimise funktsiooni.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
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
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773939"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="fab4d-103">Planeerimise optimiseerimise kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="fab4d-103">Get started with Planning Optimization</span></span>

<span data-ttu-id="fab4d-104">Planeerimise optimeerimise funktsioon ei toeta hetkel kõiki funktsioone, mis on Microsoft Dynamics 365 Supply Chain Managementi ehitatud planeerimismootoris saadaval.</span><span class="sxs-lookup"><span data-stu-id="fab4d-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fab4d-105">Seega on oluline, et hindaksite, kas hetkel planeerimise optimeerimises saadaolev funktsioonide komplekt vastab teie nõuetele.</span><span class="sxs-lookup"><span data-stu-id="fab4d-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="fab4d-106">Vaikimisi ei ole planeerimise optimeerimise funktsioon portaalis Dynamics Lifecycle Services (LCS) sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="fab4d-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="fab4d-107">Seetõttu on teil võimalus teha oma hindamine enne selle sisselülitamist.</span><span class="sxs-lookup"><span data-stu-id="fab4d-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="fab4d-108">Lõpuks asendab planeerimise optimeerimine olemasoleva sisseehitatud tarneahela halduse planeerimismootori.</span><span class="sxs-lookup"><span data-stu-id="fab4d-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="fab4d-109">Enne planeerimise optimeerimise sisselülitamist soovitame teil hinnata planeerimise optimeerimise sobivuse analüüsi tulemusi.</span><span class="sxs-lookup"><span data-stu-id="fab4d-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="fab4d-110">Lisateavet vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="fab4d-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="fab4d-111">Litsentsimine</span><span class="sxs-lookup"><span data-stu-id="fab4d-111">Licensing</span></span>

<span data-ttu-id="fab4d-112">Kui saate käivitada koondplaneerimise oma praegust litsentsi kasutades, ei pea te täiendavat litsentsi ostma, et hakata planeerimise optimeerimist kasutama.</span><span class="sxs-lookup"><span data-stu-id="fab4d-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="fab4d-113">Lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="fab4d-113">Install the add-in</span></span>

<span data-ttu-id="fab4d-114">Planeerimise optimeerimise kasutamiseks installige Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="fab4d-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fab4d-115">Saate kasutada lisandmoodulit oma LCS projektist ja lülitada planeerimise optimeerimise funktsiooni sisse tarneahela halduse kasutajaliidesest.</span><span class="sxs-lookup"><span data-stu-id="fab4d-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

1. <span data-ttu-id="fab4d-116">Logige LCS-i sisse ja avage soovitud keskkond.</span><span class="sxs-lookup"><span data-stu-id="fab4d-116">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="fab4d-117">Avage **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="fab4d-117">Go to **Full details**.</span></span>
1. <span data-ttu-id="fab4d-118">Valige **Hooldamine** või kerige alla kiirkaardile **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="fab4d-118">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="fab4d-119">Valige **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="fab4d-119">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="fab4d-120">Valige **Planeerimise optimeerimine**.</span><span class="sxs-lookup"><span data-stu-id="fab4d-120">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="fab4d-121">Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.</span><span class="sxs-lookup"><span data-stu-id="fab4d-121">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="fab4d-122">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="fab4d-122">Select **Install**.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="fab4d-123">Planeerimise optimeerimise integreerimine</span><span class="sxs-lookup"><span data-stu-id="fab4d-123">Planning Optimization integration</span></span>

<span data-ttu-id="fab4d-124">Konfigureerimaks, kas planeerimise optimeerimise lisandmoodulit peaks koondplaneerimise jaoks kasutama, avage **Koondplaneerimine** \> **Seadistamine** \> **Planeerimise optimeerimise integreerimine** \> **Integreerimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="fab4d-124">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization integration** \> **Integration parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="fab4d-125">Ühenduse olek</span><span class="sxs-lookup"><span data-stu-id="fab4d-125">Connection status</span></span>

<span data-ttu-id="fab4d-126">Ühenduse olek näitab tarneahela halduse ja planeerimise optimeerimise teenuse vahelise ühenduse hetkeolekut.</span><span class="sxs-lookup"><span data-stu-id="fab4d-126">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="fab4d-127">Järgmine tabel näitab võimalikke väärtuseid.</span><span class="sxs-lookup"><span data-stu-id="fab4d-127">The following table shows the possible values.</span></span>

| <span data-ttu-id="fab4d-128">Ühenduse olek</span><span class="sxs-lookup"><span data-stu-id="fab4d-128">Connection status</span></span> | <span data-ttu-id="fab4d-129">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="fab4d-129">Description</span></span> | <span data-ttu-id="fab4d-130">Kas planeerimise optimeerimist saab kasutada?</span><span class="sxs-lookup"><span data-stu-id="fab4d-130">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="fab4d-131">Ühendus on loodud</span><span class="sxs-lookup"><span data-stu-id="fab4d-131">Connected</span></span> | <span data-ttu-id="fab4d-132">Planeerimise optimeerimise teenuse ja tarneahela halduse vahel on loodud ühendus.</span><span class="sxs-lookup"><span data-stu-id="fab4d-132">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="fab4d-133">Jah</span><span class="sxs-lookup"><span data-stu-id="fab4d-133">Yes</span></span> |
| <span data-ttu-id="fab4d-134">Ühenduse loomine</span><span class="sxs-lookup"><span data-stu-id="fab4d-134">Enabling connection</span></span> | <span data-ttu-id="fab4d-135">Planeerimise optimeerimise teenuse ühendamise sisselülitamise taotlus on praegu tööd.</span><span class="sxs-lookup"><span data-stu-id="fab4d-135">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="fab4d-136">Ei</span><span class="sxs-lookup"><span data-stu-id="fab4d-136">No</span></span> |
| <span data-ttu-id="fab4d-137">Ühendus on katkestatud</span><span class="sxs-lookup"><span data-stu-id="fab4d-137">Disconnected</span></span> | <span data-ttu-id="fab4d-138">Planeerimise optimeerimise teenusega puudub ühendus.</span><span class="sxs-lookup"><span data-stu-id="fab4d-138">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="fab4d-139">Ühenduse saab lülitada sisse LCS-ist, nagu selles teemas varasemalt on kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="fab4d-139">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="fab4d-140">Ei</span><span class="sxs-lookup"><span data-stu-id="fab4d-140">No</span></span> |
| <span data-ttu-id="fab4d-141">Ühenduse katkestamine</span><span class="sxs-lookup"><span data-stu-id="fab4d-141">Disabling connection</span></span> | <span data-ttu-id="fab4d-142">Planeerimise optimeerimise teenuse ühendamise väljalülitamise taotlus on praegu tööd.</span><span class="sxs-lookup"><span data-stu-id="fab4d-142">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="fab4d-143">Ei</span><span class="sxs-lookup"><span data-stu-id="fab4d-143">No</span></span> |
| <span data-ttu-id="fab4d-144">Oleku hankimine</span><span class="sxs-lookup"><span data-stu-id="fab4d-144">Getting status</span></span> | <span data-ttu-id="fab4d-145">Süsteem ootab planeerimise optimeerimise teenuselt oleku teavet.</span><span class="sxs-lookup"><span data-stu-id="fab4d-145">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="fab4d-146">Ei</span><span class="sxs-lookup"><span data-stu-id="fab4d-146">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="fab4d-147">Planeerimise optimeerimise kasutamise suvand</span><span class="sxs-lookup"><span data-stu-id="fab4d-147">The Use Planning Optimization option</span></span>

<span data-ttu-id="fab4d-148">Suvandi **Planeerimise optimeerimise kasutamine** säte määrab, millist planeerimismootorit koondplaneerimiseks kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="fab4d-148">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="fab4d-149">**Jah** – planeerimise optimeerimist kasutatakse koondplaneerimiseks.</span><span class="sxs-lookup"><span data-stu-id="fab4d-149">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="fab4d-150">**Ei** – koondplaneerimise jaoks kasutatakse sisseehitatud tarneahela halduse planeerimise mootorit.</span><span class="sxs-lookup"><span data-stu-id="fab4d-150">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="fab4d-151">Kui olemasoleva planeerimise paketi tööd, mis sisseehitatud tarneahela halduse planeerimismootori jaoks loodi, käivitatakse sel ajal, kui suvandi **Planeerimise optimeerimise kasutamine** väärtuseks on seatud **Jah**, siis need tööd nurjuvad.</span><span class="sxs-lookup"><span data-stu-id="fab4d-151">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="fab4d-152">Integreerimine seadistamisega</span><span class="sxs-lookup"><span data-stu-id="fab4d-152">Integration with the setup</span></span>

<span data-ttu-id="fab4d-153">Kui planeerimise optimeerimise eelvaade on sisse lülitatud, tehakse koondplaneerimine planeerimise optimeerimise lisandmoodulit kasutades.</span><span class="sxs-lookup"><span data-stu-id="fab4d-153">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="fab4d-154">Sel juhul on koondplaneerimise tulemused ja funktsioonid mõjutatud.</span><span class="sxs-lookup"><span data-stu-id="fab4d-154">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="fab4d-155">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="fab4d-155">Related resources</span></span>

[<span data-ttu-id="fab4d-156">Eelvaate tingimused ja nõuded</span><span class="sxs-lookup"><span data-stu-id="fab4d-156">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="fab4d-157">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="fab4d-157">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="fab4d-158">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="fab4d-158">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="fab4d-159">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="fab4d-159">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="fab4d-160">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="fab4d-160">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="fab4d-161">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="fab4d-161">Cancel a planning job</span></span>](cancel-planning-job.md)
