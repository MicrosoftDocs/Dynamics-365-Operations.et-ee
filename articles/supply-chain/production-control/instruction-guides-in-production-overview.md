---
title: Hübriidreaalsusjuhendite kasutamise võimaldamine tootmistöötajatele
description: Selles teemas selgitatakse, kuidas integreerida rakenduse Microsoft Dynamics 365 Supply Chain Management tootmishalduse moodul rakendusega Dynamics 365 Guides.
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: d8c2da17d4e3df37c55844f0aad00f883725f741
ms.sourcegitcommit: c55fecae96b4bb27bc313ba10a97eddb9c91350a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989268"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="4f0c0-103">Hübriidreaalsusjuhendite kasutamise võimaldamine tootmistöötajatele</span><span class="sxs-lookup"><span data-stu-id="4f0c0-103">Provide mixed-reality Guides for workers in production</span></span>

<span data-ttu-id="4f0c0-104">Tootmistöötajad saavad kasu asjakohastest juhistest, mida pakutakse nende töö kontekstis õigel ajal.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="4f0c0-105">*Juhised* rakenduvad mitmes töövaldkonnas, sealhulgas koostamine, hooldus, toimingud, sertifitseerimine ja ohutus.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="4f0c0-106">Kõigi nende põhiärifunktsioonide puhul võivad aktiivsed koolitusjuhised aidata töötajatel rohkem ja paremini töötada.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="4f0c0-107">Sissejuhatus</span><span class="sxs-lookup"><span data-stu-id="4f0c0-107">Introduction</span></span>

<span data-ttu-id="4f0c0-108">Juhiseid saate pakkuda eri viisidel.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="4f0c0-109">Üks kohe kasutamiseks valmis tõhus süsteem kasutab rakendust [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="4f0c0-110">Rakendus Dynamics 365 Guides võib aidata teie töötajaid praktilise õppe kaudu.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="4f0c0-111">Saate määratleda standarditud protsesse koos etapiviisiliste juhistega, mis juhatavad teie töötajaid vajalike tööriistade ja osade juurde ning näitavad neile, kuidas tööriistu reaalses tööolukorras kasutada.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="4f0c0-112">Saate lisada juhendeid tootmise juhtimise eri aspektidele, sealhulgas järgmistele.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="4f0c0-113">Ressursid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-113">Resources</span></span>](#resources)
- [<span data-ttu-id="4f0c0-114">Ressursigrupid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="4f0c0-115">Väljastatud tooted</span><span class="sxs-lookup"><span data-stu-id="4f0c0-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="4f0c0-116">Valemid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="4f0c0-117">Valemiversioonid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="4f0c0-118">Kooslused (BOM-id)</span><span class="sxs-lookup"><span data-stu-id="4f0c0-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="4f0c0-119">Koosluse versioonid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="4f0c0-120">Protsessid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-120">Routes</span></span>](#routes)
- [<span data-ttu-id="4f0c0-121">Protsessi versioonid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="4f0c0-122">Protsessi toiminguseosed</span><span class="sxs-lookup"><span data-stu-id="4f0c0-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="4f0c0-123">Saate lisada rakenduse Guides ka varahaldusesse.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="4f0c0-124">Selle võimaluse kohta leiate lisateavet teemast [Rakenduse Dynamics 365 Supply Chain Management (varahaldus) integreerimine rakendusega Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="4f0c0-125">Kui esmatasanditöötaja valib rakenduse Supply Chain Management kaudu tootmisjaoskonnas töö, näeb ta töö kaardil [asjaomaseid juhendeid](#logic).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="4f0c0-126">Kui töötaja valib kindla juhendi, kuvatakse ekraanil selle juhendi QR-kood.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="4f0c0-127">Seejärel kasutab töötaja QR-koodi skannimiseks oma HoloLensi, mis käivitab rakenduse Guides ja kuvab vajalikud juhised.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="4f0c0-128">Järgmistes alajaotistes on kirjeldatud mõnda valitud stsenaariumi, mille puhul võivad kõikide valdkondade ettevõtted ise näha, kui kasulik on rakenduse Guides kasutamine tootmisjuhiste pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="4f0c0-129">Assembler</span><span class="sxs-lookup"><span data-stu-id="4f0c0-129">Assembly</span></span>

<span data-ttu-id="4f0c0-130">![Rakenduse Guides kasutamine koostamisülesannetes](media/instruction-guides-hero-assembly.png "Rakenduse Guides kasutamine hooldusülesannetes")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="4f0c0-131">Koostamistoimingute juhised näitavad töötajatele vajalikke tööriistu ja osasid ning kuidas neid reaalses tööolukorras kasutada.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="4f0c0-132">Tootmisjuhid saavad luua ja määrata juhendeid näiteks [tootmisprotsesside](routes-operations.md), [toiminguseoste](routes-operations.md#operation-relations) või [koosluste](bill-of-material-bom.md) jaoks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="4f0c0-133">Töötajad leiavad asjakohased juhised tootmisjaoskonnas asjaomase toimingu kallal töötades.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="4f0c0-134">Teenus</span><span class="sxs-lookup"><span data-stu-id="4f0c0-134">Service</span></span>

<span data-ttu-id="4f0c0-135">![Rakenduse Guides kasutamine hooldusülesannetes](media/instruction-guides-hero-service.png "Rakenduse Guides kasutamine hooldusülesannetes")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="4f0c0-136">Varustage tehnikud töökohas juhistega, et lisakülastusi poleks vaja plaanida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="4f0c0-137">Hooldusjuhid saavad määrata juhendeid näiteks konkreetsetele [toodetele](../../commerce/product.md), mis pakuvad kvaliteedi hindamise toimingute üksikasju.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="4f0c0-138">Kvaliteet</span><span class="sxs-lookup"><span data-stu-id="4f0c0-138">Quality</span></span>

<span data-ttu-id="4f0c0-139">![Rakenduse Guides kasutamine kvaliteedi tagamise ülesannetes](media/instruction-guides-hero-quality.png "Rakenduse Guides kasutamine kvaliteedi tagamise ülesannetes")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="4f0c0-140">Looge uusi protsesse ja tagage suurem järjepidevus, muutes töötajate teadmised korduvalt kasutatavaks tööriistaks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="4f0c0-141">Kvaliteedi tagamise juhid saavad määrata juhendeid näiteks konkreetsetele [toodetele](../../commerce/product.md), mis pakuvad kvaliteedi hindamise toimingute üksikasju.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="4f0c0-142">Serdid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-142">Certifications</span></span>

<span data-ttu-id="4f0c0-143">![Rakenduse Guides kasutamine sertifitseerimisega seotud ülesannetes](media/instruction-guides-hero-certification.png "Rakenduse Guides kasutamine sertifitseerimisega seotud ülesannetes")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="4f0c0-144">Veenduge, et iga töötaja vastaks standarditele, tehes kiiresti kindlaks, kes vajab abi ja kus.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="4f0c0-145">Ohutus</span><span class="sxs-lookup"><span data-stu-id="4f0c0-145">Safety</span></span>

<span data-ttu-id="4f0c0-146">![Rakenduse Guides kasutamine tööohutusjuhistes](media/instruction-guides-hero-safety.png "Rakenduse Guides kasutamine tööohutusjuhistes")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="4f0c0-147">Looge juhised, mis näitavad ohtlikke olukordi virtuaalselt, enne kui neid päriselt tehakse.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="4f0c0-148">Hübriidreaalsust kasutades saavad töötajad kogeda ohtlikke olukordi virtuaalselt.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="4f0c0-149">Tootmisjuhid võivad pakkuda spetsiaalseid käitlemisjuhiseid ohtlike materjalide käitlemiseks või delikaatset käitlemist vajavate olukordade jaoks, määrates juhised [toodetele](../../commerce/product.md), [protsessidele](routes-operations.md) ja [toimingutele](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="4f0c0-150">Juhiste ja rakenduse Guides kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="4f0c0-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="4f0c0-151">Tootmisprotsessides juhiste lubamiseks pakub rakendus Supply Chain Management integratsiooni rakendusega Dynamics 365 Guides, mis on kasutamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="4f0c0-152">Hübriidreaalsusjuhendite loomiseks, haldamiseks ja määramiseks tootmisvaradele ning tööle on vajalik litsentsitud ja installitud rakenduse Guides eksemplar.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="4f0c0-153">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="4f0c0-153">Prerequisites</span></span>

<span data-ttu-id="4f0c0-154">Selle funktsiooni kasutamiseks peab teie süsteem sisaldama järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="4f0c0-155">Dynamics 365 Supply Chain Managementi versioon 10.0.15 või uuem</span><span class="sxs-lookup"><span data-stu-id="4f0c0-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="4f0c0-156">[Topeltkirjutamine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) Supply Chain Managementi rakenduste jaoks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="4f0c0-157">[Rakenduse Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) versioon 400.0.1.48 või uuem</span><span class="sxs-lookup"><span data-stu-id="4f0c0-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="4f0c0-158">Funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="4f0c0-158">Turn on the feature</span></span>

<span data-ttu-id="4f0c0-159">Et muuta funktsioon oma süsteemis kättesaadavaks, peate lubama selle konfiguratsioonivõtmed.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="4f0c0-160">Peate seda tegema ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-160">You only need to do this once.</span></span> <span data-ttu-id="4f0c0-161">Selleks peab administraator tegema järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="4f0c0-162">Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="4f0c0-163">Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="4f0c0-164">Laiendage jaotis **Hübriidreaalsus** ja valige seejärel märkeruut **Hübriidreaalsusjuhend**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="4f0c0-165">Laiendage jaotis **Tootmishaldus** ja valige seejärel märkeruut **Tootmisjuhised**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="4f0c0-166">Lülitage hooldusrežiim välja, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="4f0c0-167">Rakenduse Guides kujunduse konfigureerimine tootmisjaoskonnas</span><span class="sxs-lookup"><span data-stu-id="4f0c0-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="4f0c0-168">Et konfigureerida, kuidas rakendust Guides tootmisjaoskonnas kuvatakse, avage **Hübriidreaalsus \> Dynamics 365 Guides \> Rakenduse Guides integratsiooni konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="4f0c0-169">![Rakenduse Guides integratsiooni konfigureerimine tootmise jaoks](media/instruction-guides-configure-integration.png "Rakenduse Guides integratsiooni konfigureerimine tootmise jaoks")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="4f0c0-170">Seadistage järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-170">Set the following fields:</span></span>

- <span data-ttu-id="4f0c0-171">**CDS-i keskkonna alamdomeen** – see väli peaks juba väärtust näitama.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-171">**CDS environment subdomain** - This field should already show a value.</span></span> <span data-ttu-id="4f0c0-172">See väli sisaldab Common Data Service'i keskkonna alamdomeeni, kus te oma juhendeid loote.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-172">This field holds the subdomain for the Common Data Service environment where you create your Guides.</span></span> <span data-ttu-id="4f0c0-173">Alamdomeen on URL-i esimene osa ja selleks on tavaliselt teie organisatsiooni nimi.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-173">The subdomain is the first part of the URL and is typically named after your organization.</span></span> <span data-ttu-id="4f0c0-174">Näiteks kui teie Common Data Service'i URL on „contoso.crm4.dynamics.com”, siis sisestage siia *contoso*.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-174">For example, if your Common Data Service URL is "contoso.crm4.dynamics.com", you should enter *contoso* here.</span></span> <span data-ttu-id="4f0c0-175">Seda väärtust kasutatakse juhendite aadresside koostamiseks ja kodeeritakse QR-koodidesse.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-175">This value is used to compose addresses for your guides and will be encoded into the QR codes.</span></span>
- <span data-ttu-id="4f0c0-176">**QR-koodi suurus** – määrake renderdatava QR-koodi suurus.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="4f0c0-177">Soovitame valida suuruse, mis täidab enamiku teie ekraanist, kuid mitte rohkem.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="4f0c0-178">Tavaliselt on *15* hea väärtus.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="4f0c0-179">**QR-koodi veaparanduse tase** – seadke QR-koodi teralisus.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="4f0c0-180">Suurem teralisus võib aidata suurendada koodi usaldusväärsust, kuid teie **QR-koodi suurus** peab olema piisavalt suur, et toetada teie valitud veataseme põhjal vajalikku üksikasjalikkust.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>


> [!TIP]
> - <span data-ttu-id="4f0c0-181">QR-koodide, mis on teie kuva jaoks liiga suured, renderdamine ja siis teie kuvaga kohandamine võtab veidi kauem aega.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="4f0c0-182">Need ei paku eeliseid.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="4f0c0-183">QR-koodid, mis on liiga väikesed, võivad vähendada mõnes keskkonnas HoloLensi võimet koodi korralikult lugeda.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="4f0c0-184">Soovitame teil testida sätteid igas seadmes, milles kuvatakse QR-koodid HoloLensi jaoks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="4f0c0-185">Valige sätted, mis tagavad teie tootmisjaoskonnas piisava loetavuse.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="4f0c0-186">Kõigi määratud juhendite ülevaate hankimine</span><span class="sxs-lookup"><span data-stu-id="4f0c0-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="4f0c0-187">Kasutage lehte **Kõik juhendid**, et näha kõigi teie organisatsioonis saadaolevate juhendite loendit ning kõiki määramisi teie tootmisprotsessidele ja ressurssidele.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="4f0c0-188">Selle avamiseks avage **Hübriidreaalsus \> Juhendid \> Kõik juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="4f0c0-189">Üleval olevas loendis kuvatakse kõik saadaolevad juhendid ja saate seda välja kasutada loendi filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="4f0c0-190">All olevas loendis kuvatakse kõik juhendite määramised ning tööriistariba nende haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="4f0c0-191">![Juhendite haldamine](media/instruction-guides-allguides.png "Juhendite haldamine")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="4f0c0-192">Järgmised jaotised kirjeldavad objektide tüüpe, millele saate juhendeid määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="4f0c0-193">Iga määratud juhend sisaldab juhiseid, mis seotakse automaatselt asjaomaste tootmistöödega ja mis on saadaval tootmisjaoskonnas.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="4f0c0-194">Juhendi seostamine ressursiga</span><span class="sxs-lookup"><span data-stu-id="4f0c0-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="4f0c0-195">Lisage [ressursile](operations-resources.md) juhend, et pakkuda seda asjakohaste tootmistööde kontekstis.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="4f0c0-196">Tüüpiline stsenaarium ressursside kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-196">Typical scenario using resources</span></span>

<span data-ttu-id="4f0c0-197">Näiteks saate lisada üldiste masinaohutus- või käsitsemisjuhistega juhendi ressursile, mille tüüp on masin.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="4f0c0-198">Seejärel on juhend saadaval iga töö puhul, mida masinaga tehakse.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="4f0c0-199">Juhendi lisamine ressursile</span><span class="sxs-lookup"><span data-stu-id="4f0c0-199">Add a Guide to a resource</span></span>

<span data-ttu-id="4f0c0-200">Juhendi lisamiseks ressursile tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="4f0c0-201">Valige **Tootmise juhtimine \> Seadistus \> Ressursid \> Ressursid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="4f0c0-202">Valige loendipaanist ressurss, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-203">Laiendage kiirkaart **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="4f0c0-204">Valige suvand **Lisa** tööribast **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="4f0c0-205">Ruudustikku lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="4f0c0-206">Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="4f0c0-207">Kui teil on palju juhendeid, saate loendit filtreerida, et leida otsitav.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="4f0c0-208">![Juhendite haldamine](media/instruction-guides-allguides.png "Juhendite haldamine")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="4f0c0-209">Juhendi seostamine ressursirühmaga</span><span class="sxs-lookup"><span data-stu-id="4f0c0-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="4f0c0-210">Saate lisada juhendi [ressursirühmadele](tasks/define-discrete-manufacturing-resource-group.md), kui kasutate neid masinate, tootmisridade või töörakkude rühmade haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="4f0c0-211">Tavalised stsenaariumid ressursirühmade kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="4f0c0-212">**Näide 1:** olete määratlenud ressursirühma mitme samast mudelist masina jaoks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="4f0c0-213">Selle asemel, et määrata selle masinamudeli käsitsemise juhiseid sisaldav juhend igale asjaomasele ressursile, võiksite selle asemel määrata juhendi seda masinamudelit kajastava ressursirühma jaoks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="4f0c0-214">**Näide 2:** olete määratlenud ressursirühma töörakule, mis sisaldab eri masinaid, ja teil on juhend, mis pakub üldisi juhiseid tööraku haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="4f0c0-215">Juhend kehtib mis tahes tootmistegevuse puhul selles töörakus.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="4f0c0-216">Juhendi lisamine ressursirühmale</span><span class="sxs-lookup"><span data-stu-id="4f0c0-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="4f0c0-217">Juhendi lisamiseks ressursirühmale tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="4f0c0-218">Valige **Tootmise juhtimine \> Seadistus \> Ressursid \> Ressursirühmad**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="4f0c0-219">Valige loendipaanist ressursirühma, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-220">Laiendage kiirkaart **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="4f0c0-221">Valige suvand **Lisa** tööribast **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="4f0c0-222">Ruudustikku lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="4f0c0-223">Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="4f0c0-224">Kui teil on palju juhendeid, saate loendit filtreerida, et leida otsitav.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="4f0c0-225">![Juhendi lisamine ressursirühmale](media/instruction-guides-resourcegroup.png "Juhendi lisamine ressursirühmale")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="4f0c0-226">Juhendi seostamine väljastatud tootega</span><span class="sxs-lookup"><span data-stu-id="4f0c0-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="4f0c0-227">Saate lisada juhendi igale [väljastatud tootele](../pim/tasks/create-released-product-single-company.md).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="4f0c0-228">Tüüpiline stsenaarium väljastatud toodete kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-228">Typical scenario using released products</span></span>

<span data-ttu-id="4f0c0-229">Tootepõhised juhendid pakuvad tootmisjaoskonna töötajatele juhiseid selle kohta, kuidas toimida iga kindla väljastatud toote või kauba korral ja neid käsitseda.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="4f0c0-230">Juhendi lisamine väljastatud tootele</span><span class="sxs-lookup"><span data-stu-id="4f0c0-230">Add a Guide to a released product</span></span>

<span data-ttu-id="4f0c0-231">Juhendi lisamiseks väljastatud tootele tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="4f0c0-232">Avage **Tootmisteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="4f0c0-233">Avage toode, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-234">Valige toimingupaanil vahekaart **Projekteerimine** ning valige rühmas **Kuvamine** suvand **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="4f0c0-235">Teie valitud toote jaoks avaneb leht **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="4f0c0-236">Valige toimingupaanil suvand **Lisa**, et lisada ruudustikku uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="4f0c0-237">Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="4f0c0-238">![Juhendi lisamine väljastatud tootele](media/instruction-guides-ReleasedProduct-AddGuides.png "Juhendi lisamine väljastatud tootele")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="4f0c0-239">Juhendi seostamine valemiga</span><span class="sxs-lookup"><span data-stu-id="4f0c0-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="4f0c0-240">Saate lisada juhendi igale [valemile](bill-of-material-bom.md#formulas-co-products-and-by-products).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="4f0c0-241">Tüüpiline stsenaarium valemite kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="4f0c0-242">Valemipõhised juhendid pakuvad tootmisjaoskonna töötajatele käsitsemisjuhiseid valemi või retsepti kontekstis.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="4f0c0-243">Juhendeid saab määrata ka valemi versioonidele.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="4f0c0-244">Saate lisada valemipõhiste tootmisprotsesside puhul kehtivad juhised protsessile, protsessi versioonile või protsessi toiminguseostele.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="4f0c0-245">Juhendeid ei saa praegu siduda üksikute valemiridadega.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="4f0c0-246">Juhendi lisamine valemile</span><span class="sxs-lookup"><span data-stu-id="4f0c0-246">Add a Guide to a formula</span></span>

<span data-ttu-id="4f0c0-247">Juhendi lisamiseks valemile tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="4f0c0-248">Avage **Tootmisteabe haldus \> Kooslused ja valemid \> Valemid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="4f0c0-249">Avage valem, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-250">Avage vahekaart **Päis**, mis asub ülemise kiirkaardi kohal.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="4f0c0-251">Laiendage kiirkaart **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="4f0c0-252">Valige suvand **Lisa** tööribast **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="4f0c0-253">Ruudustikku lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="4f0c0-254">Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="4f0c0-255">![Juhendi lisamine valemile](media/instruction-guides-Formula.png "Juhendi lisamine valemile")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="4f0c0-256">Juhendi seostamine valemi versiooniga</span><span class="sxs-lookup"><span data-stu-id="4f0c0-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="4f0c0-257">Saate lisada juhendi igale [valemi versioonile](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="4f0c0-258">Tüüpiline stsenaarium valemi versioonide kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="4f0c0-259">Valemi ühele versioonile lisatud juhendid annavad tootmisjaoskonna töötajatele juhiseid, mis sisaldavad valemiretsepti selle versiooni tootmise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="4f0c0-260">Saate lisada selle valemi versiooni põhiste tootmisprotsesside puhul kehtivad juhised protsessile, protsessi versioonile või protsessi toiminguseostele.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="4f0c0-261">Juhendeid ei saa praegu siduda üksikute valemiridadega.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="4f0c0-262">Juhendi lisamine valemi versioonile</span><span class="sxs-lookup"><span data-stu-id="4f0c0-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="4f0c0-263">Juhendi lisamiseks valemi versioonile tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="4f0c0-264">Avage **Tootmisteabe haldus \> Kooslused ja valemid \> Valemid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="4f0c0-265">Avage valem, mis sisaldab versiooni, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-266">Avage vahekaart **Päis**, mis asub ülemise kiirkaardi kohal.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="4f0c0-267">Valige kiirkaardil **Valemi versioonid** versioon, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-268">Valige tööriistaribal **Valemi versioonid** suvand **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="4f0c0-269">![Valitud valemi versiooniga seotud juhendite avamine](media/instruction-guides-FormulaVersion.png "Valitud valemi versiooniga seotud juhendite avamine")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="4f0c0-270">Teie valitud valemi versiooni jaoks avaneb leht **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="4f0c0-271">Valige toimingupaanil suvand **Lisa**, et lisada ruudustikku uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="4f0c0-272">Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="4f0c0-273">![Juhendi lisamine valemi versioonile](media/instruction-guides-FormulaVersionAddGuide.png "Juhendi lisamine valemi versioonile")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="4f0c0-274">Juhendi seostamine kooslusega</span><span class="sxs-lookup"><span data-stu-id="4f0c0-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="4f0c0-275">Saate lisata juhendi mis tahes [kooslusele](bill-of-material-bom.md) (BOM).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="4f0c0-276">Tüüpiline stsenaarium koosluste kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="4f0c0-277">Kooslusele lisatud juhendid pakuvad tootmisjaoskonna töötajatele juhiseid, mis selgitavad, kuidas koosluses sisalduvat materjali ette valmistada ja käsitseda.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="4f0c0-278">Juhendeid saab määrata ka koosluse versioonidele.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="4f0c0-279">Juhendeid ei saa praegu siduda üksikute koosluseridadega.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="4f0c0-280">Juhendi lisamine kooslusele</span><span class="sxs-lookup"><span data-stu-id="4f0c0-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="4f0c0-281">Juhendi lisamiseks kooslusele tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="4f0c0-282">Minge jaotisse **Tootmisteabe haldus \> Kooslused ja valemid \> Kooslused**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="4f0c0-283">Avage kooslus, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-284">Avage vahekaart **Päis**, mis asub ülemise kiirkaardi kohal.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="4f0c0-285">Laiendage kiirkaart **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="4f0c0-286">Valige suvand **Lisa** tööribast **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="4f0c0-287">Ruudustikku lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="4f0c0-288">Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="4f0c0-289">![Juhendi lisamine kooslusele](media/instruction-guides-BOM.png "Juhendi lisamine kooslusele")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="4f0c0-290">Juhendi seostamine koosluse versiooniga</span><span class="sxs-lookup"><span data-stu-id="4f0c0-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="4f0c0-291">Saate lisata juhendi mis tahes [koosluse versioonile](bill-of-material-bom.md#bom-and-formula-versions).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="4f0c0-292">Tüüpiline stsenaarium koosluse versioonide kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="4f0c0-293">Üksikule koosluse versioonile lisatud juhendid pakuvad tootmisjaoskonna töötajatele juhiseid, mis selgitavad, kuidas valmistada ette ja käsitseda materjali, mis on pärit koosluse versioonist, mis erineb üldisest kooslusest või selle teistest versioonidest.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="4f0c0-294">Juhendeid ei saa praegu siduda üksikute koosluseridadega.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="4f0c0-295">Juhendi lisamine koosluse versioonile</span><span class="sxs-lookup"><span data-stu-id="4f0c0-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="4f0c0-296">Juhendi lisamiseks koosluse versioonile tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="4f0c0-297">Minge jaotisse **Tootmisteabe haldus \> Kooslused ja valemid \> Kooslused**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="4f0c0-298">Avage kooslus, mis sisaldab versiooni, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-299">Avage vahekaart **Päis**, mis asub ülemise kiirkaardi kohal.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="4f0c0-300">Valige kiirkaardil **Koosluse versioonid** versioon, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-301">Valige tööriistaribal **Koosluse versioonid** suvand **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="4f0c0-302">![Valitud koosluse versiooniga seotud juhendite avamine](media/instruction-guides-BOMVersion.png "Valitud koosluse versiooniga seotud juhendite avamine")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="4f0c0-303">Teie valitud koosluse versiooni jaoks avaneb leht **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="4f0c0-304">Valige toimingupaanil suvand **Lisa**, et lisada ruudustikku uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="4f0c0-305">Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="4f0c0-306">![Juhendi lisamine koosluse versioonile](media/instruction-guides-BOMVersionAddGuide.png "Juhendi lisamine koosluse versioonile")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="4f0c0-307">Juhendi seostamine protsessiga</span><span class="sxs-lookup"><span data-stu-id="4f0c0-307">Associate a Guide to a route</span></span>

<span data-ttu-id="4f0c0-308">Saate lisada juhendi igale [protsessile](routes-operations.md).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="4f0c0-309">Tüüpiline stsenaarium protsesside kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-309">Typical scenario using routes</span></span>

<span data-ttu-id="4f0c0-310">Protsesse kasutatakse tavaliselt selleks, et määrata, kuidas kindlat väljastatavat toodet toodetakse koosluse või koosluse versiooni põhjal ning koos ressursside või ressursirühmadega.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="4f0c0-311">Määrake protsessile juhend, et pakkuda etapiviisilisi juhiseid asjaomase tootmisprotsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="4f0c0-312">Juhendi lisamine protsessile</span><span class="sxs-lookup"><span data-stu-id="4f0c0-312">Add a Guide to a route</span></span>

<span data-ttu-id="4f0c0-313">Juhendi lisamiseks protsessile tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="4f0c0-314">Avage **Tootmise juhtimine \> Kõik protsessid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="4f0c0-315">Avage protsess, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-316">Laiendage kiirkaart **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="4f0c0-317">Valige suvand **Lisa** tööribast **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="4f0c0-318">Ruudustikku lisatakse uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="4f0c0-319">Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="4f0c0-320">![Juhendi lisamine protsessile](media/instruction-guides-Route.png "Juhendi lisamine protsessile")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="4f0c0-321">Juhendi seostamine protsessi versiooniga</span><span class="sxs-lookup"><span data-stu-id="4f0c0-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="4f0c0-322">Saate lisada juhendi igale [protsessi versioonile](routes-operations.md#route-versions).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="4f0c0-323">Tüüpiline stsenaarium protsessi versioonide kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-323">Typical scenario using route versions</span></span>

<span data-ttu-id="4f0c0-324">Protsesside versioone kasutatakse tavaliselt olemasoleva protsessi põhjal tootmisprotsesside variantide täpsustamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="4f0c0-325">Saate määrata igale protsessi versioonile erinevad juhendid.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="4f0c0-326">Juhendi lisamine protsessi versioonile</span><span class="sxs-lookup"><span data-stu-id="4f0c0-326">Add a Guide to a route version</span></span>

<span data-ttu-id="4f0c0-327">Juhendi lisamiseks protsessi versioonile tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="4f0c0-328">Avage **Tootmise juhtimine \> Kõik protsessid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="4f0c0-329">Avage protsess, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-330">Valige kiirkaardil **Versioonid** versioon, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-331">Valige tööriistaribal **Versioonid** suvand **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="4f0c0-332">![Valitud protsessi versiooniga seotud juhendite avamine](media/instruction-guides-RouteVersion.png "Valitud protsessi versiooniga seotud juhendite avamine")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="4f0c0-333">Teie valitud koosluse versiooni jaoks avaneb leht **Seotud juhendid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="4f0c0-334">Valige toimingupaanil suvand **Lisa**, et lisada ruudustikku uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="4f0c0-335">Uue rea puhul kasutage veerus **Nimi** ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="4f0c0-336">![Juhendi lisamine protsessi versioonile](media/instruction-guides-RouteVersionAddGuide.png "Juhendi lisamine protsessi versioonile")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="4f0c0-337">Juhendi seostamine protsessi toiminguseosega</span><span class="sxs-lookup"><span data-stu-id="4f0c0-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="4f0c0-338">Saate lisada juhendi igale [protsessi toiminguseosele](routes-operations.md#operation-relations).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="4f0c0-339">Tüüpiline stsenaarium protsessi toiminguseoste kasutamisel</span><span class="sxs-lookup"><span data-stu-id="4f0c0-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="4f0c0-340">Toiminguseosed on kõige kindlam viis tooteprotsessile ja sellega seotud toimingutele juhiste lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="4f0c0-341">Saate määrata juhiseid igale protsessi toimingule ja määrata eri juhised igat tüüpi seosekontekstile, mis on protsessi puhul täpsustatud, nt kindlate kaupade, konfiguratsioonide ja muu jaoks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="4f0c0-342">Samuti saate määrata, milliste toimingu etappide puhul juhend kehtib (nt seadistus, järjekord, töötlemine või transport).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="4f0c0-343">Kui määrate juhendid protsessi mitme toiminguseose jaoks, kuvatakse tootmisjaoskonnas loodud töö puhul nende juhendite hulgast ainult kõige täpsema seose juhendit.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="4f0c0-344">Juhendi lisamine protsessi toiminguseosele</span><span class="sxs-lookup"><span data-stu-id="4f0c0-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="4f0c0-345">Juhendi lisamiseks protsessi toiminguseosele tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="4f0c0-346">Avage **Tootmise juhtimine \> Kõik protsessid**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="4f0c0-347">Avage protsess, millele soovite juhendit määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="4f0c0-348">Valige toimingupaanil vahekaart **Protsess** ning valige rühmas **Haldamine** suvand **Protsessi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="4f0c0-349">Teie valitud protsessi jaoks avaneb leht **Protsessi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="4f0c0-350">Valige ülemises ruudustikus toiming, millele soovite juhiseid pakkuda.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="4f0c0-351">Valige alumises ruudustikus konkreetne seos (või üldine seos **Kõik**).</span><span class="sxs-lookup"><span data-stu-id="4f0c0-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="4f0c0-352">![Toimingu ja seejärel seose valimine](media/instruction-guides-RouteOperationRelation.png "Toimingu ja seejärel seose valimine")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="4f0c0-353">Avage alumise ruudustiku kohal olev vahekaart **Seotud juhendid**.  ![Seotud juhendite vahekaart](media/instruction-guides-RouteOperationRelation-AddGuide.png "Seotud juhendite vahekaart")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="4f0c0-354">Valige alumise ruudustiku ülaosas olevalt tööriistaribalt suvand **Lisa**, et lisada ruudustikku uus rida.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="4f0c0-355">Uue rea puhul kasutage veerus **Nimi** olevat ripploendit, et valida juhend, mida soovite määrata.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="4f0c0-356">Märkige ülejäänud reas märkeruut iga konteksti puhul, kus valitud juhend peaks saadaval olema.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="4f0c0-357">Igale toimingu etapile saate lisada ühe või mitu juhendit.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="4f0c0-358">Juhendite valimine tootmisjaoskonna käivitusliidesest</span><span class="sxs-lookup"><span data-stu-id="4f0c0-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="4f0c0-359">Kui töötaja avab tootmisjaoskonna käivitusliidesest tööde loendi, otsib rakendus Supply Chain Management üles asjaomased juhendid kuvatud tööde jaoks.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="4f0c0-360">Kasutage nuppu **Juhendid**, et vaadata asjakohaseid juhendeid.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="4f0c0-361">![Nupp „Juhendid” tootmisjaoskonna käivitusliideses](media/instruction-guides-Shopfloor1.png "Nupp „Juhendid” tootmisjaoskonna käivitusliideses")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="4f0c0-362">Seejärel pange ette HoloLens ning avage asjakohane juhend, vaadates QR-koodi ja aktiveerides asjakohase juhendi.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="4f0c0-363">![QR-kood juhendite avamiseks HoloLensi abil](media/instruction-guides-Shopfloor2.png "QR-kood juhendite avamiseks HoloLensi abil")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="4f0c0-364">Juhendite valimise loogika lahendamine</span><span class="sxs-lookup"><span data-stu-id="4f0c0-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="4f0c0-365">Saate lisada juhendeid järgmistele tootmisandmetele.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="4f0c0-366">Ressursid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-366">Resources</span></span>](#resources)
- [<span data-ttu-id="4f0c0-367">Ressursigrupid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="4f0c0-368">Väljastatud tooted</span><span class="sxs-lookup"><span data-stu-id="4f0c0-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="4f0c0-369">Valemid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="4f0c0-370">Valemiversioonid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="4f0c0-371">Kooslused (BOM-id)</span><span class="sxs-lookup"><span data-stu-id="4f0c0-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="4f0c0-372">Koosluse versioonid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="4f0c0-373">Marsruudid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-373">Routes</span></span>](#routes)
- [<span data-ttu-id="4f0c0-374">Protsessi versioonid</span><span class="sxs-lookup"><span data-stu-id="4f0c0-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="4f0c0-375">Protsessi toiminguseosed</span><span class="sxs-lookup"><span data-stu-id="4f0c0-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="4f0c0-376">Kui rakendus Supply Chain Management loob tootmisjaoskonna jaoks töid, kogub see kokku asjakohased juhendid nendest allikatest.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="4f0c0-377">Pidage meeles järgmiseid olulisi reegleid.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="4f0c0-378">Kui lisate koosluse versiooni või valemi versiooni protsessile või tootmistellimusele, kuvatakse töö juures kõik selle versiooniga seotud juhendid ning samuti selle versiooni peakoosluse või -valemiga seotud juhendid.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="4f0c0-379">Kui lisate protsessi versiooni tootmistellimusele, kuvatakse töö juures kõik selle versiooniga seotud juhendid ning samuti selle versiooni peaprotsessiga seotud juhendid.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="4f0c0-380">Kui määratlete mitu protsessi toiminguseost, mis sisaldavad seost *Kõik*, ja määrate neile juhendid, kuvatakse töö juures ainult kõige täpsema seose juhendid.</span><span class="sxs-lookup"><span data-stu-id="4f0c0-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="4f0c0-381">![Asjakohaste juhendite lahendamise diagramm](media/instruction-guides-Resolve.png "Asjakohaste juhendite lahendamise diagramm")</span><span class="sxs-lookup"><span data-stu-id="4f0c0-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>