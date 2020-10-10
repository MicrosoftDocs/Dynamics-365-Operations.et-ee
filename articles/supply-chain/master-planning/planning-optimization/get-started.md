---
title: Planeerimise optimiseerimise kasutamise alustamine
description: Selles teemas selgitatakse, kuidas hakata kasutama planeerimise optimeerimise funktsiooni.
author: ChristianRytt
manager: tfehr
ms.date: 05/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 04b39469ccf4f088bb33bdfc73ce40eece6f5f2e
ms.sourcegitcommit: cde71bc7d14ea6cdff2c4e991057d39a6a0473d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2020
ms.locfileid: "3887260"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="a8c98-103">Planeerimise optimiseerimise kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="a8c98-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a8c98-104">Planeerimise optimeerimise funktsioon ei toeta hetkel kõiki funktsioone, mis on Microsoft Dynamics 365 Supply Chain Managementi ehitatud planeerimismootoris saadaval.</span><span class="sxs-lookup"><span data-stu-id="a8c98-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a8c98-105">Seega on oluline, et hindaksite, kas hetkel planeerimise optimeerimises saadaolev funktsioonide komplekt vastab teie nõuetele.</span><span class="sxs-lookup"><span data-stu-id="a8c98-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="a8c98-106">Vaikimisi ei ole planeerimise optimeerimise funktsioon portaalis Dynamics Lifecycle Services (LCS) sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="a8c98-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="a8c98-107">Seetõttu on teil võimalus teha oma hindamine enne selle sisselülitamist.</span><span class="sxs-lookup"><span data-stu-id="a8c98-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="a8c98-108">Lõpuks asendab planeerimise optimeerimine olemasoleva sisseehitatud tarneahela halduse planeerimismootori.</span><span class="sxs-lookup"><span data-stu-id="a8c98-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="a8c98-109">Enne planeerimise optimeerimise sisselülitamist soovitame teil hinnata planeerimise optimeerimise sobivuse analüüsi tulemusi.</span><span class="sxs-lookup"><span data-stu-id="a8c98-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="a8c98-110">Lisateavet vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="a8c98-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="a8c98-111">Kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="a8c98-111">Availability</span></span>
<span data-ttu-id="a8c98-112">Planeerimise optimeerimine on hetkel kättesaadav järgmistes Azure'i geograafilistes piirkondades: Ameerika Ühendriigid, Kanada, Euroopa, Ühendkuningriik ja Austraalia.</span><span class="sxs-lookup"><span data-stu-id="a8c98-112">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="a8c98-113">Kui proovite lisandmoodulit installida muus geograafilises piirkonnas, siis kuvab LCS teate, et seda geograafilist piirkonda ei toetata.</span><span class="sxs-lookup"><span data-stu-id="a8c98-113">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="a8c98-114">Pange tähele, et planeerimise optimeerimine ei toeta Dynamics 365 Supply Chain Management-i kohapealseid juurutusi.</span><span class="sxs-lookup"><span data-stu-id="a8c98-114">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="a8c98-115">Litsentsimine</span><span class="sxs-lookup"><span data-stu-id="a8c98-115">Licensing</span></span>

<span data-ttu-id="a8c98-116">Kui saate käivitada koondplaneerimise oma praegust litsentsi kasutades, ei pea te täiendavat litsentsi ostma, et hakata planeerimise optimeerimist kasutama.</span><span class="sxs-lookup"><span data-stu-id="a8c98-116">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="a8c98-117">Lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="a8c98-117">Install the add-in</span></span>

<span data-ttu-id="a8c98-118">Planeerimise optimeerimise kasutamiseks installige Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="a8c98-118">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a8c98-119">Saate kasutada lisandmoodulit oma LCS projektist ja lülitada planeerimise optimeerimise funktsiooni sisse tarneahela halduse kasutajaliidesest.</span><span class="sxs-lookup"><span data-stu-id="a8c98-119">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="a8c98-120">Planeerimise optimeerimise nõue on LCS-i loaga suure kättesaadavusega keskkond, järk 2 või kõrgem, (mitte OneBoxi keskkond) koos Dynamics 365 Supply Chain Management-i versiooniga 10.0.7 või hilisem.</span><span class="sxs-lookup"><span data-stu-id="a8c98-120">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="a8c98-121">Kui proovite paigaldada moodulit OneBoxi keskkonnas, siis ei viida paigaldust lõpule ja te peate paigalduse tühistama.</span><span class="sxs-lookup"><span data-stu-id="a8c98-121">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="a8c98-122">Logige LCS-i sisse ja avage soovitud keskkond.</span><span class="sxs-lookup"><span data-stu-id="a8c98-122">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="a8c98-123">Avage **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="a8c98-123">Go to **Full details**.</span></span>
1. <span data-ttu-id="a8c98-124">Kerige alla kiirkaardini **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="a8c98-124">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="a8c98-125">Valige **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="a8c98-125">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="a8c98-126">Valige **Planeerimise optimeerimine**.</span><span class="sxs-lookup"><span data-stu-id="a8c98-126">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="a8c98-127">Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.</span><span class="sxs-lookup"><span data-stu-id="a8c98-127">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="a8c98-128">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="a8c98-128">Select **Install**.</span></span>
1. <span data-ttu-id="a8c98-129">Kiirkaardil **Keskkonna lisandmoodulid** peaksite nägema, et planeerimise optimeerimine on installitud.</span><span class="sxs-lookup"><span data-stu-id="a8c98-129">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="a8c98-130">Mõne minuti pärast peaks olek **Installimine** muutuma olekuks **Installitud** (võimalik, et peate lehte värskendama).</span><span class="sxs-lookup"><span data-stu-id="a8c98-130">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="a8c98-131">Kui installimine on lõpetatud, olete valmis aktiveerima optimeerimise plaanimise rakenduses Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a8c98-131">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="a8c98-132">Planeerimise optimeerimise integreerimine</span><span class="sxs-lookup"><span data-stu-id="a8c98-132">Planning Optimization integration</span></span>

<span data-ttu-id="a8c98-133">Konfigureerimaks, kas planeerimise optimeerimise lisandmoodulit peaks koondplaneerimise jaoks kasutama, avage **Koondplaneerimine** \> **Seadistamine** \> **Optimeerimise parameetrite plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="a8c98-133">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="a8c98-134">Ühenduse olek</span><span class="sxs-lookup"><span data-stu-id="a8c98-134">Connection status</span></span>

<span data-ttu-id="a8c98-135">Ühenduse olek näitab tarneahela halduse ja planeerimise optimeerimise teenuse vahelise ühenduse hetkeolekut.</span><span class="sxs-lookup"><span data-stu-id="a8c98-135">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="a8c98-136">Järgmine tabel näitab võimalikke väärtuseid.</span><span class="sxs-lookup"><span data-stu-id="a8c98-136">The following table shows the possible values.</span></span>

| <span data-ttu-id="a8c98-137">Ühenduse olek</span><span class="sxs-lookup"><span data-stu-id="a8c98-137">Connection status</span></span> | <span data-ttu-id="a8c98-138">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a8c98-138">Description</span></span> | <span data-ttu-id="a8c98-139">Kas planeerimise optimeerimist saab kasutada?</span><span class="sxs-lookup"><span data-stu-id="a8c98-139">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="a8c98-140">Ühendus on loodud</span><span class="sxs-lookup"><span data-stu-id="a8c98-140">Connected</span></span> | <span data-ttu-id="a8c98-141">Planeerimise optimeerimise teenuse ja tarneahela halduse vahel on loodud ühendus.</span><span class="sxs-lookup"><span data-stu-id="a8c98-141">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="a8c98-142">Jah</span><span class="sxs-lookup"><span data-stu-id="a8c98-142">Yes</span></span> |
| <span data-ttu-id="a8c98-143">Ühenduse loomine</span><span class="sxs-lookup"><span data-stu-id="a8c98-143">Enabling connection</span></span> | <span data-ttu-id="a8c98-144">Planeerimise optimeerimise teenuse ühendamise sisselülitamise taotlus on praegu tööd.</span><span class="sxs-lookup"><span data-stu-id="a8c98-144">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="a8c98-145">Ei</span><span class="sxs-lookup"><span data-stu-id="a8c98-145">No</span></span> |
| <span data-ttu-id="a8c98-146">Ühendus on katkestatud</span><span class="sxs-lookup"><span data-stu-id="a8c98-146">Disconnected</span></span> | <span data-ttu-id="a8c98-147">Planeerimise optimeerimise teenusega puudub ühendus.</span><span class="sxs-lookup"><span data-stu-id="a8c98-147">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="a8c98-148">Ühenduse saab lülitada sisse LCS-ist, nagu selles teemas varasemalt on kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="a8c98-148">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="a8c98-149">Ei</span><span class="sxs-lookup"><span data-stu-id="a8c98-149">No</span></span> |
| <span data-ttu-id="a8c98-150">Ühenduse katkestamine</span><span class="sxs-lookup"><span data-stu-id="a8c98-150">Disabling connection</span></span> | <span data-ttu-id="a8c98-151">Planeerimise optimeerimise teenuse ühendamise väljalülitamise taotlus on praegu tööd.</span><span class="sxs-lookup"><span data-stu-id="a8c98-151">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="a8c98-152">Ei</span><span class="sxs-lookup"><span data-stu-id="a8c98-152">No</span></span> |
| <span data-ttu-id="a8c98-153">Oleku hankimine</span><span class="sxs-lookup"><span data-stu-id="a8c98-153">Getting status</span></span> | <span data-ttu-id="a8c98-154">Süsteem ootab planeerimise optimeerimise teenuselt oleku teavet.</span><span class="sxs-lookup"><span data-stu-id="a8c98-154">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="a8c98-155">Ei</span><span class="sxs-lookup"><span data-stu-id="a8c98-155">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="a8c98-156">Planeerimise optimeerimise kasutamise suvand</span><span class="sxs-lookup"><span data-stu-id="a8c98-156">The Use Planning Optimization option</span></span>

<span data-ttu-id="a8c98-157">Suvandi **Planeerimise optimeerimise kasutamine** säte määrab, millist planeerimismootorit koondplaneerimiseks kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="a8c98-157">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="a8c98-158">**Jah** – planeerimise optimeerimist kasutatakse koondplaneerimiseks.</span><span class="sxs-lookup"><span data-stu-id="a8c98-158">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="a8c98-159">**Ei** – koondplaneerimise jaoks kasutatakse sisseehitatud tarneahela halduse planeerimise mootorit.</span><span class="sxs-lookup"><span data-stu-id="a8c98-159">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="a8c98-160">Kui olemasoleva planeerimise paketi tööd, mis sisseehitatud tarneahela halduse planeerimismootori jaoks loodi, käivitatakse sel ajal, kui suvandi **Planeerimise optimeerimise kasutamine** väärtuseks on seatud **Jah**, siis need tööd nurjuvad.</span><span class="sxs-lookup"><span data-stu-id="a8c98-160">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="a8c98-161">Integreerimine seadistamisega</span><span class="sxs-lookup"><span data-stu-id="a8c98-161">Integration with the setup</span></span>

<span data-ttu-id="a8c98-162">Kui planeerimise optimeerimise eelvaade on sisse lülitatud, tehakse koondplaneerimine planeerimise optimeerimise lisandmoodulit kasutades.</span><span class="sxs-lookup"><span data-stu-id="a8c98-162">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="a8c98-163">Sel juhul on koondplaneerimise tulemused ja funktsioonid mõjutatud.</span><span class="sxs-lookup"><span data-stu-id="a8c98-163">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8c98-164">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a8c98-164">Additional resources</span></span>

[<span data-ttu-id="a8c98-165">Eelvaate tingimused ja nõuded</span><span class="sxs-lookup"><span data-stu-id="a8c98-165">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="a8c98-166">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="a8c98-166">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="a8c98-167">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="a8c98-167">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="a8c98-168">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="a8c98-168">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="a8c98-169">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="a8c98-169">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="a8c98-170">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="a8c98-170">Cancel a planning job</span></span>](cancel-planning-job.md)
