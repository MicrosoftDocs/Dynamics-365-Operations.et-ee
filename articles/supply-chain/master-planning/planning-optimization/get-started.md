---
title: Planeerimise optimiseerimise kasutamise alustamine
description: Selles teemas selgitatakse, kuidas hakata kasutama planeerimise optimeerimise funktsiooni.
author: ChristianRytt
manager: tfehr
ms.date: 10/09/2020
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
ms.openlocfilehash: 54ad180b7f4691ead3563b077eadadc3b9b20588
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4426704"
---
# <a name="get-started-with-planning-optimization"></a><span data-ttu-id="cc817-103">Planeerimise optimeerimisega alustamine</span><span class="sxs-lookup"><span data-stu-id="cc817-103">Get started with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc817-104">Nagu [eelnevalt välja kuulutatud](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), asendab planeerimise optimeerimine varsti olemasoleva sisseehitatud koondplaneerimise mootori.</span><span class="sxs-lookup"><span data-stu-id="cc817-104">As [previously announced](https://docs.microsoft.com/dynamics365/supply-chain/get-started/removed-deprecated-features-scm-updates#use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios), Planning Optimization is scheduled to replace the existing built-in master planning engine.</span></span>

<span data-ttu-id="cc817-105">Kui kasutate praegu sisseehitatud koondplaneerimise mootorit, peaksite hakkama tegema kohe plaane migreerimiseks planeerimise optimeerimisse.</span><span class="sxs-lookup"><span data-stu-id="cc817-105">If you currently use the built-in master planning engine, you should start planning your migration to Planning Optimization now.</span></span> <span data-ttu-id="cc817-106">On oluline alustada migreerimisprotsessi kohe, sest teie toiminguid võidakse mõjutada, kui iganemine jõustatakse.</span><span class="sxs-lookup"><span data-stu-id="cc817-106">It is important to start the migration process right away because your operations may be impacted when deprecation is enforced.</span></span> <span data-ttu-id="cc817-107">Et vältida viimasel hetkel tekkivaid probleeme iganemise jõustamisel, soovitame teil tungivalt migreerimise lõpule viia enne 1. detsembrit 2020.</span><span class="sxs-lookup"><span data-stu-id="cc817-107">To avoid last-minutes issues when deprecation is enforced, we strongly encourage you to complete the migration before December 1, 2020.</span></span> 

<span data-ttu-id="cc817-108">Planeerimise optimeerimise funktsioon ei toeta hetkel kõiki funktsioone, mis on rakendusse Supply Chain Management ehitatud planeerimismootoris saadaval.</span><span class="sxs-lookup"><span data-stu-id="cc817-108">The Planning Optimization functionality doesn't currently support all the features that are available in the planning engine that is built into Supply Chain Management.</span></span> <span data-ttu-id="cc817-109">Seega on oluline, et hindaksite, kas hetkel planeerimise optimeerimises saadaolev funktsioonide komplekt vastab teie nõuetele.</span><span class="sxs-lookup"><span data-stu-id="cc817-109">Therefore, it's important that you evaluate whether the feature set that is currently available in Planning Optimization will meet your requirements.</span></span> <span data-ttu-id="cc817-110">Planeerimise optimeerimise funktsioon ei ole praegu vaikimisi sisse lülitatud lahenduses Dynamics Lifecycle Services (LCS), seega on teil võimalus teha oma hinnang enne funktsiooni sisselülitamist.</span><span class="sxs-lookup"><span data-stu-id="cc817-110">The Planning Optimization functionality isn't currently turned on by default in Dynamics Lifecycle Services (LCS), so you have the opportunity to do your evaluation before the feature is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="cc817-111">Peate taotlema planeerimise optimeerimise funktsiooni migreerumiseks erandit, kui teie koondplaneerimise protsess ei hõlma tootmist (koondplaneerimise loodud plaanitud tootmistellimused) ja vajate sisseehitatud koondplaneerimise mootori versioonist 10.0.15 uuemat versiooni.</span><span class="sxs-lookup"><span data-stu-id="cc817-111">You need to request an exception from migration to Planning Optimization if your master planning process does not include production (master planning generated planned production orders) and you require the built-in master planning engine beyond version 10.0.15.</span></span> <span data-ttu-id="cc817-112">Alates versioonist 10.0.16 kuvatakse tõrge keskkondades, kus sisseehitatud koondplaneerimine töötab ilma plaanitud tootmistellimuste loomiseta.</span><span class="sxs-lookup"><span data-stu-id="cc817-112">Starting in version 10.0.16, an error will be shown in environments when running built-in master planning without generation of planned production orders.</span></span> <span data-ttu-id="cc817-113">Planeerimise optimeerimise funktsiooni tuleks kasutada kõigi uute juurutuste puhul, mis ei loo koondplaneerimise ajal plaanitud tootmistellimusi.</span><span class="sxs-lookup"><span data-stu-id="cc817-113">Planning Optimization should be used for all new deployments that do not generate planned production orders during master planning.</span></span> <span data-ttu-id="cc817-114">Selliste olemasolevate keskkondade omanikud, milles käitatakse sisseehitatud koondplaneerimise mootorit ilma plaanitud tootmistellimuste loomiseta, saavad e-kirja koos üksikasjadega erandiprotsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="cc817-114">Owners of existing environments running the built-in master planning engine without generation of Planned production orders, will receive a mail with details about the exception process.</span></span> <span data-ttu-id="cc817-115">Soovitame töötada koos partneriga, et hinnata ja planeerida migreerumist planeerimise optimeerimise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="cc817-115">We recommend that you work with a partner to evaluate and plan the migration to Planning Optimization.</span></span>

<span data-ttu-id="cc817-116">Enne planeerimise optimeerimise sisselülitamist soovitame teil hinnata planeerimise optimeerimise sobivuse analüüsi tulemusi.</span><span class="sxs-lookup"><span data-stu-id="cc817-116">Before you turn on Planning Optimization, we strongly recommend that you evaluate the results of the Planning Optimization fit analysis.</span></span> <span data-ttu-id="cc817-117">Lisateavet vt [Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="cc817-117">For more information, see [Planning Optimization fit analysis](planning-optimization-fit-analysis.md).</span></span>

### <a name="availability"></a><span data-ttu-id="cc817-118">Kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="cc817-118">Availability</span></span>
<span data-ttu-id="cc817-119">Planeerimise optimeerimine on hetkel kättesaadav järgmistes Azure'i geograafilistes piirkondades: Ameerika Ühendriigid, Kanada, Euroopa, Ühendkuningriik ja Austraalia.</span><span class="sxs-lookup"><span data-stu-id="cc817-119">Planning Optimization is currently available in the following Azure geographies: United States, Canada, Europe, United Kingdom, and Australia.</span></span> <span data-ttu-id="cc817-120">Kui proovite lisandmoodulit installida muus geograafilises piirkonnas, siis kuvab LCS teate, et seda geograafilist piirkonda ei toetata.</span><span class="sxs-lookup"><span data-stu-id="cc817-120">If you try to install the add-in from another geographic region, then LCS will show a message that this geographic is not supported.</span></span>

<span data-ttu-id="cc817-121">Pange tähele, et planeerimise optimeerimine ei toeta Dynamics 365 Supply Chain Management-i kohapealseid juurutusi.</span><span class="sxs-lookup"><span data-stu-id="cc817-121">Note that Planning Optimization does not support on-premises deployments of Dynamics 365 Supply Chain Management.</span></span>

### <a name="licensing"></a><span data-ttu-id="cc817-122">Litsentsimine</span><span class="sxs-lookup"><span data-stu-id="cc817-122">Licensing</span></span>

<span data-ttu-id="cc817-123">Kui saate käivitada koondplaneerimise oma praegust litsentsi kasutades, ei pea te täiendavat litsentsi ostma, et hakata planeerimise optimeerimist kasutama.</span><span class="sxs-lookup"><span data-stu-id="cc817-123">If you can run master planning by using your current license, you don't have to buy an additional license to start to use Planning Optimization.</span></span>

### <a name="install-the-add-in"></a><span data-ttu-id="cc817-124">Lisandmooduli installimine</span><span class="sxs-lookup"><span data-stu-id="cc817-124">Install the add-in</span></span>

<span data-ttu-id="cc817-125">Planeerimise optimeerimise kasutamiseks installige Dynamics 365 Supply Chain Managementi planeerimise optimeerimise lisandmoodul.</span><span class="sxs-lookup"><span data-stu-id="cc817-125">To use Planning Optimization, install the Planning Optimization Add-in for Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="cc817-126">Saate kasutada lisandmoodulit oma LCS projektist ja lülitada planeerimise optimeerimise funktsiooni sisse tarneahela halduse kasutajaliidesest.</span><span class="sxs-lookup"><span data-stu-id="cc817-126">You can access the add-in from your LCS project and turn on the Planning Optimization functionality from the Supply Chain Management user interface (UI).</span></span>

> [!NOTE]
> <span data-ttu-id="cc817-127">Planeerimise optimeerimise nõue on LCS-i loaga suure kättesaadavusega keskkond, järk 2 või kõrgem, (mitte OneBoxi keskkond) koos Dynamics 365 Supply Chain Management-i versiooniga 10.0.7 või hilisem.</span><span class="sxs-lookup"><span data-stu-id="cc817-127">The requirement for Planning Optimization is an LCS enabled high-availability environment, tier 2 or higher (not a OneBox environment), with Dynamics 365 Supply Chain Management version 10.0.7 or later.</span></span> <span data-ttu-id="cc817-128">Kui proovite paigaldada moodulit OneBoxi keskkonnas, siis ei viida paigaldust lõpule ja te peate paigalduse tühistama.</span><span class="sxs-lookup"><span data-stu-id="cc817-128">If you try to install the add-in on a OneBox environment, the installation will not complete and you will need to cancel the installation.</span></span>

1. <span data-ttu-id="cc817-129">Logige LCS-i sisse ja avage soovitud keskkond.</span><span class="sxs-lookup"><span data-stu-id="cc817-129">Sign in to LCS, and open the desired environment.</span></span>
1. <span data-ttu-id="cc817-130">Avage **Kõik üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="cc817-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="cc817-131">Kerige alla kiirkaardini **Keskkonna lisandmoodulid**.</span><span class="sxs-lookup"><span data-stu-id="cc817-131">Scroll down to the **Environment add-ins** FastTab.</span></span>
1. <span data-ttu-id="cc817-132">Valige **Installi uus lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="cc817-132">Select **Install a new add-in**.</span></span>
1. <span data-ttu-id="cc817-133">Valige **Planeerimise optimeerimine**.</span><span class="sxs-lookup"><span data-stu-id="cc817-133">Select **Planning Optimization**.</span></span>
1. <span data-ttu-id="cc817-134">Täitke paigaldusjuhendit ja nõustuge nõuete ja tingimustega.</span><span class="sxs-lookup"><span data-stu-id="cc817-134">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="cc817-135">Valige **Installi**.</span><span class="sxs-lookup"><span data-stu-id="cc817-135">Select **Install**.</span></span>
1. <span data-ttu-id="cc817-136">Kiirkaardil **Keskkonna lisandmoodulid** peaksite nägema, et planeerimise optimeerimine on installitud.</span><span class="sxs-lookup"><span data-stu-id="cc817-136">On the **Environment add-ins** FastTab you should see that Planning Optimization is installing.</span></span>
1. <span data-ttu-id="cc817-137">Mõne minuti pärast peaks olek **Installimine** muutuma olekuks **Installitud** (võimalik, et peate lehte värskendama).</span><span class="sxs-lookup"><span data-stu-id="cc817-137">After a few minutes **Installing** should change to **Installed** (you may need to refresh the page).</span></span> <span data-ttu-id="cc817-138">Kui installimine on lõpetatud, olete valmis aktiveerima optimeerimise plaanimise rakenduses Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cc817-138">When installed, you are ready to activate Planning Optimization in Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="cc817-139">Planeerimise optimeerimise lisandmooduli installimise peamine eesmärk on ühendada teenus ja keskkond.</span><span class="sxs-lookup"><span data-stu-id="cc817-139">The main purpose of installing the Planning Optimization add-in is to connect the service and the environment.</span></span> <span data-ttu-id="cc817-140">Seetõttu peate installima lisandmooduli eraldi igasse keskkonda, kus te kasutate planeerimise optimeerimist, olenemata mis tahes koodist, mis on teisaldatud keskkondade vahel.</span><span class="sxs-lookup"><span data-stu-id="cc817-140">Therefore, you must install the add-in separately on each environment where you will use Planning Optimization, regardless of any code moved between the environments.</span></span>

### <a name="planning-optimization-integration"></a><span data-ttu-id="cc817-141">Planeerimise optimeerimise integreerimine</span><span class="sxs-lookup"><span data-stu-id="cc817-141">Planning Optimization integration</span></span>

<span data-ttu-id="cc817-142">Konfigureerimaks, kas planeerimise optimeerimise lisandmoodulit peaks koondplaneerimise jaoks kasutama, avage **Koondplaneerimine** \> **Seadistamine** \> **Optimeerimise parameetrite plaanimine**.</span><span class="sxs-lookup"><span data-stu-id="cc817-142">To configure whether the Planning Optimization Add-in should be used for master planning, go to **Master planning** \> **Setup** \> **Planning Optimization parameters**.</span></span>

#### <a name="connection-status"></a><span data-ttu-id="cc817-143">Ühenduse olek</span><span class="sxs-lookup"><span data-stu-id="cc817-143">Connection status</span></span>

<span data-ttu-id="cc817-144">Ühenduse olek näitab tarneahela halduse ja planeerimise optimeerimise teenuse vahelise ühenduse hetkeolekut.</span><span class="sxs-lookup"><span data-stu-id="cc817-144">The connection status indicates the current status of the connection between Supply Chain Management and the Planning Optimization service.</span></span> <span data-ttu-id="cc817-145">Järgmine tabel näitab võimalikke väärtuseid.</span><span class="sxs-lookup"><span data-stu-id="cc817-145">The following table shows the possible values.</span></span>

| <span data-ttu-id="cc817-146">Ühenduse olek</span><span class="sxs-lookup"><span data-stu-id="cc817-146">Connection status</span></span> | <span data-ttu-id="cc817-147">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="cc817-147">Description</span></span> | <span data-ttu-id="cc817-148">Kas planeerimise optimeerimist saab kasutada?</span><span class="sxs-lookup"><span data-stu-id="cc817-148">Can Planning Optimization be used?</span></span> |
|---|---|---|
| <span data-ttu-id="cc817-149">Ühendus on loodud</span><span class="sxs-lookup"><span data-stu-id="cc817-149">Connected</span></span> | <span data-ttu-id="cc817-150">Planeerimise optimeerimise teenuse ja tarneahela halduse vahel on loodud ühendus.</span><span class="sxs-lookup"><span data-stu-id="cc817-150">A connection has been established between the Planning Optimization service and Supply Chain Management.</span></span> | <span data-ttu-id="cc817-151">Jah</span><span class="sxs-lookup"><span data-stu-id="cc817-151">Yes</span></span> |
| <span data-ttu-id="cc817-152">Ühenduse loomine</span><span class="sxs-lookup"><span data-stu-id="cc817-152">Enabling connection</span></span> | <span data-ttu-id="cc817-153">Planeerimise optimeerimise teenuse ühendamise sisselülitamise taotlus on praegu tööd.</span><span class="sxs-lookup"><span data-stu-id="cc817-153">A request to turn on the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="cc817-154">Ei</span><span class="sxs-lookup"><span data-stu-id="cc817-154">No</span></span> |
| <span data-ttu-id="cc817-155">Ühendus on katkestatud</span><span class="sxs-lookup"><span data-stu-id="cc817-155">Disconnected</span></span> | <span data-ttu-id="cc817-156">Planeerimise optimeerimise teenusega puudub ühendus.</span><span class="sxs-lookup"><span data-stu-id="cc817-156">There is no connection to the Planning Optimization service.</span></span> <span data-ttu-id="cc817-157">Ühenduse saab lülitada sisse LCS-ist, nagu selles teemas varasemalt on kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="cc817-157">The connection can be turned on from LCS, as described earlier in this topic.</span></span> | <span data-ttu-id="cc817-158">Ei</span><span class="sxs-lookup"><span data-stu-id="cc817-158">No</span></span> |
| <span data-ttu-id="cc817-159">Ühenduse katkestamine</span><span class="sxs-lookup"><span data-stu-id="cc817-159">Disabling connection</span></span> | <span data-ttu-id="cc817-160">Planeerimise optimeerimise teenuse ühendamise väljalülitamise taotlus on praegu tööd.</span><span class="sxs-lookup"><span data-stu-id="cc817-160">A request to turn off the connection to the Planning Optimization service is currently in progress.</span></span> | <span data-ttu-id="cc817-161">Ei</span><span class="sxs-lookup"><span data-stu-id="cc817-161">No</span></span> |
| <span data-ttu-id="cc817-162">Oleku hankimine</span><span class="sxs-lookup"><span data-stu-id="cc817-162">Getting status</span></span> | <span data-ttu-id="cc817-163">Süsteem ootab planeerimise optimeerimise teenuselt oleku teavet.</span><span class="sxs-lookup"><span data-stu-id="cc817-163">The system is waiting for status information from the Planning Optimization service.</span></span> | <span data-ttu-id="cc817-164">Ei</span><span class="sxs-lookup"><span data-stu-id="cc817-164">No</span></span> |

#### <a name="the-use-planning-optimization-option"></a><span data-ttu-id="cc817-165">Planeerimise optimeerimise kasutamise suvand</span><span class="sxs-lookup"><span data-stu-id="cc817-165">The Use Planning Optimization option</span></span>

<span data-ttu-id="cc817-166">Suvandi **Planeerimise optimeerimise kasutamine** säte määrab, millist planeerimismootorit koondplaneerimiseks kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="cc817-166">The setting of the **Use Planning Optimization** option determines which planning engine is used for master planning:</span></span>

- <span data-ttu-id="cc817-167">**Jah** – planeerimise optimeerimist kasutatakse koondplaneerimiseks.</span><span class="sxs-lookup"><span data-stu-id="cc817-167">**Yes** – Planning Optimization is used for master planning.</span></span>
- <span data-ttu-id="cc817-168">**Ei** – koondplaneerimise jaoks kasutatakse sisseehitatud tarneahela halduse planeerimise mootorit.</span><span class="sxs-lookup"><span data-stu-id="cc817-168">**No** – The built-in Supply Chain Management planning engine is used for master planning.</span></span>

> [!NOTE]
> <span data-ttu-id="cc817-169">Kui olemasoleva planeerimise paketi tööd, mis sisseehitatud tarneahela halduse planeerimismootori jaoks loodi, käivitatakse sel ajal, kui suvandi **Planeerimise optimeerimise kasutamine** väärtuseks on seatud **Jah**, siis need tööd nurjuvad.</span><span class="sxs-lookup"><span data-stu-id="cc817-169">If existing planning batch jobs that were created for the built-in Supply Chain Management planning engine are triggered while the **Use Planning Optimization** option is set to **Yes**, those jobs will fail.</span></span>

### <a name="integration-with-the-setup"></a><span data-ttu-id="cc817-170">Integreerimine seadistamisega</span><span class="sxs-lookup"><span data-stu-id="cc817-170">Integration with the setup</span></span>

<span data-ttu-id="cc817-171">Kui planeerimise optimeerimine on sisse lülitatud, tehakse koondplaneerimine planeerimise optimeerimise lisandmoodulit kasutades.</span><span class="sxs-lookup"><span data-stu-id="cc817-171">If the Planning Optimization is turned on, master planning is done by using the Planning Optimization Add-in.</span></span> <span data-ttu-id="cc817-172">Sel juhul on koondplaneerimise tulemused ja funktsioonid mõjutatud.</span><span class="sxs-lookup"><span data-stu-id="cc817-172">In this case, master planning results and features are affected.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc817-173">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="cc817-173">Additional resources</span></span>

[<span data-ttu-id="cc817-174">Eelvaate tingimused ja nõuded</span><span class="sxs-lookup"><span data-stu-id="cc817-174">Terms and conditions for the preview</span></span>](https://go.microsoft.com/fwlink/?linkid=2015274)

[<span data-ttu-id="cc817-175">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="cc817-175">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="cc817-176">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="cc817-176">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="cc817-177">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="cc817-177">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="cc817-178">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="cc817-178">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="cc817-179">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="cc817-179">Cancel a planning job</span></span>](cancel-planning-job.md)
