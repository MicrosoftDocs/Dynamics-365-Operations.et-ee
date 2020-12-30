---
title: Dynamics 365 Commerce'i hindamiskeskkonna KKK
description: Selles jaotises antakse vastuseid korduma kippuvatele küsimustele Microsoft Dynamics 365 Commerce'i hindamiskeskkonna kohta.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 637714e28b9f8f4aa66e251e709d8f78bff2739d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411572"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="18b49-103">Dynamics 365 Commerce'i hindamiskeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="18b49-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18b49-104">Selles jaotises antakse vastuseid korduma kippuvatele küsimustele Microsoft Dynamics 365 Commerce'i hindamiskeskkonna kohta.</span><span class="sxs-lookup"><span data-stu-id="18b49-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="18b49-105">**Kas saame kasutada Commerce'i hindamiskeskkonda e-kaubanduse poena klientidele, kes rakendavad praegu jaemüüki?**</span><span class="sxs-lookup"><span data-stu-id="18b49-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="18b49-106">Nr</span><span class="sxs-lookup"><span data-stu-id="18b49-106">No.</span></span> <span data-ttu-id="18b49-107">Commerce'i hindamiskeskkond on ainult hindamiseks.</span><span class="sxs-lookup"><span data-stu-id="18b49-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="18b49-108">Kui vajate jaemüügis kasutatava kliendi jaoks keskkonda, siis kontakteeruge Microsoftiga.</span><span class="sxs-lookup"><span data-stu-id="18b49-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="18b49-109">**Kas Commerce'i hindamiskeskkonda saab kasutada e-kaubanduse funktsioonide pakkumiseks olemasoleva rakenduse/keskkonna jaoks, mis rakendab jaemüüki?**</span><span class="sxs-lookup"><span data-stu-id="18b49-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="18b49-110">Ei (enamasti).</span><span class="sxs-lookup"><span data-stu-id="18b49-110">No (mostly).</span></span> <span data-ttu-id="18b49-111">Commerce'i hindamise komponendid on saadaval ainult keskkondadele, mis vastavad eeltingimustes ja ettevalmistamise juhendis määratud konfiguratsioonidele.</span><span class="sxs-lookup"><span data-stu-id="18b49-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="18b49-112">Lisaks ei ole nõutavad aluseks olevad demoandmed saadaval keskkondades, mis on rakendatud algses väljalaskes, mis on varasem kui 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="18b49-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="18b49-113">**Millised kulud on kaasatud Commerce'i hindamiskeskkonna Microsoft Azure keskkonna kasutamisele läbi Microsoft Dynamics Lifecycle Servicesi (LCS)?**</span><span class="sxs-lookup"><span data-stu-id="18b49-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="18b49-114">Traditsiooniline Dynamics 365 Finance'i / Dynamics 365 Supply Chain Managementi / Dynamics 365 Commerce'i peakontori demokeskkond (virtuaalarvuti \[VM\]) majutatakse teie Azure'i tellimuses.</span><span class="sxs-lookup"><span data-stu-id="18b49-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="18b49-115">Selle kulu hindamiseks saate kasutada [Azure hinnakujunduse kalkulaatorit ](https://azure.microsoft.com/pricing/calculator/).</span><span class="sxs-lookup"><span data-stu-id="18b49-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="18b49-116">Muud komponendid, nt Commerce Scale Unit, Commerce'i saidiehitaja ja teie e-kaubanduse sait, on saadaval tarkvarana teenusena (SaaS) ja majutatakse Microsoftis.</span><span class="sxs-lookup"><span data-stu-id="18b49-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="18b49-117">**Millised Azure'i geograafilised piirkonnad on praegu Commerce'i hindamiskeskkonna jaoks toetatud?**</span><span class="sxs-lookup"><span data-stu-id="18b49-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="18b49-118">Commerce'i hindamiskeskkonda saab kasutada ainult Põhja-Ameerika piirkonnas.</span><span class="sxs-lookup"><span data-stu-id="18b49-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="18b49-119">**Kas on olemas ka allalaaditav virtuaalne kõvaketas (VHD), millel on täielik OneBox virtuaalarvuti (VM) suvand?**</span><span class="sxs-lookup"><span data-stu-id="18b49-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="18b49-120">Dynamics 365 Commerce ja Commerce Scale Unit on täielikult tarkvara teenusena (SaaS) ja peavad olema pilve majutatud.</span><span class="sxs-lookup"><span data-stu-id="18b49-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="18b49-121">**Kui kaua saab Commerce'i hindamiskeskkonda kasutada?**</span><span class="sxs-lookup"><span data-stu-id="18b49-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="18b49-122">Commerce'i hindamiskeskkonnal on 30-päevane ajapiirang alates SaaS-konponentide, nagu Commerce Scale Uniti, Commerce'i saidiehitaja ja teie e-kaubanduse saidi, ettevalmistamise kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="18b49-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="18b49-123">**Kas ma saan oma Commerce'i hindamiskeskkonna ajapiirangut pikendada?**</span><span class="sxs-lookup"><span data-stu-id="18b49-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="18b49-124">Piirangu pikendamine on erand ja seda käsitletakse juhtumipõhiselt.</span><span class="sxs-lookup"><span data-stu-id="18b49-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="18b49-125">Abi saamiseks peaksite pöörduma oma Microsofti partneri kontakti poole.</span><span class="sxs-lookup"><span data-stu-id="18b49-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18b49-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="18b49-126">Additional resources</span></span>

[<span data-ttu-id="18b49-127">Dynamics 365 Commerce'i hindamiskeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="18b49-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="18b49-128">Dynamics 365 Commerce'i hindamiskeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="18b49-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="18b49-129">Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="18b49-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="18b49-130">BOPIS-e konfigureerimine Dynamics 365 Commerce'i hindamiskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="18b49-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="18b49-131">Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="18b49-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)
