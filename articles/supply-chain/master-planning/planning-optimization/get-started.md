---
title: Planeerimise optimiseerimise kasutamise alustamine
description: Selles teemas selgitatakse, kuidas hakata kasutama planeerimise optimeerimise funktsiooni.
author: ChristianRytt
manager: AnnBe
ms.date: 02/10/2020
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
ms.openlocfilehash: 3e64699005387adcc92e2e7c9fefad68a9de85c0
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076128"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="724a1-103">Planeerimise optimiseerimise kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="724a1-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="724a1-104">Planeerimise optimeerimise funktsioon ei toeta hetkel kõiki funktsioone, mis on Microsoft Dynamics 365 Supply Chain Managementi ehitatud planeerimismootoris saadaval.</span><span class="sxs-lookup"><span data-stu-id="724a1-104">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="724a1-105">Seega on oluline, et hindaksite, kas hetkel planeerimise optimeerimises saadaolev funktsioonide komplekt vastab teie nõuetele.</span><span class="sxs-lookup"><span data-stu-id="724a1-105">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="724a1-106">Vaikimisi ei ole planeerimise optimeerimise funktsioon portaalis Dynamics Lifecycle Services (LCS) sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="724a1-106">By default, the Planning Optimization functionality isn't turned on in Dynamics Lifecycle Services (LCS) by default.</span></span> <span data-ttu-id="724a1-107">Seetõttu on teil võimalus teha oma hindamine enne selle sisselülitamist.</span><span class="sxs-lookup"><span data-stu-id="724a1-107">Therefore, you have an opportunity to do your evaluation before it's turned on.</span></span>

<span data-ttu-id="724a1-108">Lõpuks asendab planeerimise optimeerimine olemasoleva sisseehitatud tarneahela halduse planeerimismootori.</span><span class="sxs-lookup"><span data-stu-id="724a1-108">Eventually, Planning Optimization will replace the existing built-in Supply Chain Management planning engine.</span></span>

<span data-ttu-id="724a1-109">Enne planeerimise optimeerimise sisselülitamist soovitame teil hinnata planeerimise optimeerimise sobivuse analüüsi tulemusi.</span><span class="sxs-lookup"><span data-stu-id="724a1-109">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="724a1-110">Lisateavet vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="724a1-110">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="licensing"></a><span data-ttu-id="724a1-111">Litsentsimine</span><span class="sxs-lookup"><span data-stu-id="724a1-111">Licensing</span></span>

<span data-ttu-id="724a1-112">Kui saate käivitada koondplaneerimise oma praegust litsentsi kasutades, ei pea te täiendavat litsentsi ostma, et hakata planeerimise optimeerimist kasutama.</span><span class="sxs-lookup"><span data-stu-id="724a1-112">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="724a1-113">Lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="724a1-113">Install the add-in</span></span>

<span data-ttu-id="724a1-114">Planeerimise optimeerimise kasutamiseks installige Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="724a1-114">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="724a1-115">Saate kasutada lisandmoodulit oma LCS projektist ja lülitada planeerimise optimeerimise funktsiooni sisse tarneahela halduse kasutajaliidesest.</span><span class="sxs-lookup"><span data-stu-id="724a1-115">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="724a1-116">Planeerimise optimeerimise nõue on LCS-i loaga suure kättesaadavusega keskkond (mitte OneBoxi keskkond) koos Dynamics 365 Supply Chain Managementi versiooniga 10.0.7 või hilisem.</span><span class="sxs-lookup"><span data-stu-id="724a1-116">The requirement for Planning Optimization is an LCS enabled high-availability environment (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span>

1. <span data-ttu-id="724a1-117">Logige LCS-i sisse ja avage soovitud keskkond.</span><span class="sxs-lookup"><span data-stu-id="724a1-117">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="724a1-118">Avage **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="724a1-118">Go to **Full details**.</span></span>
1. <span data-ttu-id="724a1-119">Kerige alla kiirkaardini **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="724a1-119">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="724a1-120">Valige **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="724a1-120">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="724a1-121">Valige **Planeerimise optimeerimine**.</span><span class="sxs-lookup"><span data-stu-id="724a1-121">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="724a1-122">Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.</span><span class="sxs-lookup"><span data-stu-id="724a1-122">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="724a1-123">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="724a1-123">Select **Install**.</span></span>
1. <span data-ttu-id="724a1-124">Kiirkaardil **Keskkonna lisandmoodulid** peaksite nägema, et planeerimise optimeerimine on installitud.</span><span class="sxs-lookup"><span data-stu-id="724a1-124">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="724a1-125">Mõne minuti pärast peaks olek **Installimine** muutuma olekuks **Installitud** (võimalik, et peate lehte värskendama).</span><span class="sxs-lookup"><span data-stu-id="724a1-125">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="724a1-126">Kui installimine on lõpetatud, olete valmis aktiveerima optimeerimise plaanimise rakenduses Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="724a1-126">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="724a1-127">Planeerimise optimeerimise integreerimine</span><span class="sxs-lookup"><span data-stu-id="724a1-127">Planning Optimization integration</span></span>

<span data-ttu-id="724a1-128">Konfigureerimaks, kas planeerimise optimeerimise lisandmoodulit peaks koondplaneerimise jaoks kasutama, avage **Koondplaneerimine** \> **Seadistamine** \> **Optimeerimise parameetrite plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="724a1-128">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="724a1-129">Ühenduse olek</span><span class="sxs-lookup"><span data-stu-id="724a1-129">Connection status</span></span>

<span data-ttu-id="724a1-130">Ühenduse olek näitab tarneahela halduse ja planeerimise optimeerimise teenuse vahelise ühenduse hetkeolekut.</span><span class="sxs-lookup"><span data-stu-id="724a1-130">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="724a1-131">Järgmine tabel näitab võimalikke väärtuseid.</span><span class="sxs-lookup"><span data-stu-id="724a1-131">The following table shows the possible values.</span></span>

| <span data-ttu-id="724a1-132">Ühenduse olek</span><span class="sxs-lookup"><span data-stu-id="724a1-132">Connection status</span></span> | <span data-ttu-id="724a1-133">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="724a1-133">Description</span></span> | <span data-ttu-id="724a1-134">Kas planeerimise optimeerimist saab kasutada?</span><span class="sxs-lookup"><span data-stu-id="724a1-134">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="724a1-135">Ühendus on loodud</span><span class="sxs-lookup"><span data-stu-id="724a1-135">Connected</span></span> | <span data-ttu-id="724a1-136">Planeerimise optimeerimise teenuse ja tarneahela halduse vahel on loodud ühendus.</span><span class="sxs-lookup"><span data-stu-id="724a1-136">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="724a1-137">Jah</span><span class="sxs-lookup"><span data-stu-id="724a1-137">Yes</span></span> |
| <span data-ttu-id="724a1-138">Ühenduse loomine</span><span class="sxs-lookup"><span data-stu-id="724a1-138">Enabling connection</span></span> | <span data-ttu-id="724a1-139">Planeerimise optimeerimise teenuse ühendamise sisselülitamise taotlus on praegu tööd.</span><span class="sxs-lookup"><span data-stu-id="724a1-139">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="724a1-140">Ei</span><span class="sxs-lookup"><span data-stu-id="724a1-140">No</span></span> |
| <span data-ttu-id="724a1-141">Ühendus on katkestatud</span><span class="sxs-lookup"><span data-stu-id="724a1-141">Disconnected</span></span> | <span data-ttu-id="724a1-142">Planeerimise optimeerimise teenusega puudub ühendus.</span><span class="sxs-lookup"><span data-stu-id="724a1-142">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="724a1-143">Ühenduse saab lülitada sisse LCS-ist, nagu selles teemas varasemalt on kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="724a1-143">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="724a1-144">Ei</span><span class="sxs-lookup"><span data-stu-id="724a1-144">No</span></span> |
| <span data-ttu-id="724a1-145">Ühenduse katkestamine</span><span class="sxs-lookup"><span data-stu-id="724a1-145">Disabling connection</span></span> | <span data-ttu-id="724a1-146">Planeerimise optimeerimise teenuse ühendamise väljalülitamise taotlus on praegu tööd.</span><span class="sxs-lookup"><span data-stu-id="724a1-146">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="724a1-147">Ei</span><span class="sxs-lookup"><span data-stu-id="724a1-147">No</span></span> |
| <span data-ttu-id="724a1-148">Oleku hankimine</span><span class="sxs-lookup"><span data-stu-id="724a1-148">Getting status</span></span> | <span data-ttu-id="724a1-149">Süsteem ootab planeerimise optimeerimise teenuselt oleku teavet.</span><span class="sxs-lookup"><span data-stu-id="724a1-149">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="724a1-150">Ei</span><span class="sxs-lookup"><span data-stu-id="724a1-150">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="724a1-151">Planeerimise optimeerimise kasutamise suvand</span><span class="sxs-lookup"><span data-stu-id="724a1-151">The Use Planning Optimization option</span></span>

<span data-ttu-id="724a1-152">Suvandi **Planeerimise optimeerimise kasutamine** säte määrab, millist planeerimismootorit koondplaneerimiseks kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="724a1-152">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="724a1-153">**Jah** – planeerimise optimeerimist kasutatakse koondplaneerimiseks.</span><span class="sxs-lookup"><span data-stu-id="724a1-153">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="724a1-154">**Ei** – koondplaneerimise jaoks kasutatakse sisseehitatud tarneahela halduse planeerimise mootorit.</span><span class="sxs-lookup"><span data-stu-id="724a1-154">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="724a1-155">Kui olemasoleva planeerimise paketi tööd, mis sisseehitatud tarneahela halduse planeerimismootori jaoks loodi, käivitatakse sel ajal, kui suvandi **Planeerimise optimeerimise kasutamine** väärtuseks on seatud **Jah**, siis need tööd nurjuvad.</span><span class="sxs-lookup"><span data-stu-id="724a1-155">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="724a1-156">Integreerimine seadistamisega</span><span class="sxs-lookup"><span data-stu-id="724a1-156">Integration with the setup</span></span>

<span data-ttu-id="724a1-157">Kui planeerimise optimeerimise eelvaade on sisse lülitatud, tehakse koondplaneerimine planeerimise optimeerimise lisandmoodulit kasutades.</span><span class="sxs-lookup"><span data-stu-id="724a1-157">If the Planning Optimization preview is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="724a1-158">Sel juhul on koondplaneerimise tulemused ja funktsioonid mõjutatud.</span><span class="sxs-lookup"><span data-stu-id="724a1-158">In this case, master planning results and features are affected.</span></span>

## <a name="related-resources"></a><span data-ttu-id="724a1-159">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="724a1-159">Related resources</span></span>

[<span data-ttu-id="724a1-160">Eelvaate tingimused ja nõuded</span><span class="sxs-lookup"><span data-stu-id="724a1-160">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="724a1-161">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="724a1-161">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="724a1-162">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="724a1-162">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="724a1-163">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="724a1-163">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="724a1-164">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="724a1-164">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="724a1-165">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="724a1-165">Cancel a planning job</span></span>](cancel-planning-job.md)
