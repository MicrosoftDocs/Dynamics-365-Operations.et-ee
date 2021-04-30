---
title: Regulatory Configuration Service
description: See teema annab ülevaate Regulatory Configuration Service (RCS) võimalustest ja selgitab, kuidas teenusele juurde pääseda.
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890796"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="1e7d8-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="1e7d8-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e7d8-104">Regulatory Configuration Service (RCS) on autonoomne disainer ja elutsükli haldamise teenus koodita/vähese koodiga globaliseerumisfunktsioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="1e7d8-105">RCS-i globaliseerumise sidusrühmad laiendavad ja kohandavad peamisi globaliseerumisvaldkondi nagu maksud, e-arved, regulatiivne aruandlus, pangandus ja äridokumendid, ilma et nad peaksid arendajaid kaasama.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="1e7d8-106">See koodita/vähese koodiga globaalne lähenemine muudab globaliseerumise lihtsamaks, kiiremaks ja kulutõhusamaks, et seda luua või laiendada.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="1e7d8-107">RCS pakub järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="1e7d8-108">Kõigi elektroonilise aruandluse (ER) pakutavate funktsioonide tugi.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="1e7d8-109">Uute globaliseerumismikroteenuste konfigureerimise eeltingimus.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="1e7d8-110">Elektroonilise arvelduse tugi.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="1e7d8-111">Lisateavet leiate teemast [E-arveldus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="1e7d8-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="1e7d8-112">Toetab maksuarvestust.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="1e7d8-113">Lisateavet vt jaotisest [Maksuteenus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="1e7d8-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="1e7d8-114">Uute globaliseerumisfunktsioonide funktsioonide tugi, mis lihtsustab mitmekomponendiliste funktsioonide elutsükli haldamist ning pakub lisavõimalusi toimingute konfigureerimiseks ja funktsiooniparameetrite seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="1e7d8-115">Lisateavet vt teemast [Regulatory Configuration Service – globaliseerumisteenuste lihtsustatud globaliseerumisfunktsioonide haldamine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="1e7d8-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="1e7d8-116">Globaalses hoidlas kohandatud konfiguratsioonide tsentraliseeritud avaldamise, salvestamise ja ühiskasutuse tugi, et lihtsustada konfiguratsioonihaldust, ilma et oleks vaja kasutada Microsoft Dynamics Lifecycle Services (LCS) teenuseid.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="1e7d8-117">RCS ligipääs</span><span class="sxs-lookup"><span data-stu-id="1e7d8-117">Access RCS</span></span>

<span data-ttu-id="1e7d8-118">RCS-i saate registreeruda või sisse logida [Regulatory Configuration Service lehel](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="1e7d8-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS-i registreerimine ja sisselogimine](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="1e7d8-120">Vaadake lehel **Regulatory Configuration Service** üle ja nõustuge teenuse kasutamise täiendavate tingimustega ning valige üks järgmistest nuppudest.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="1e7d8-121">**Registreeri**, kui olete teenuse esmakordne kasutaja ja kasutate ettevõtte meiliaadressi oma organisatsiooni teenusekeskkonna ettevalmistamiseks</span><span class="sxs-lookup"><span data-stu-id="1e7d8-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="1e7d8-122">**Logi sisse**, kui olete varem teenuse kasutajaks registreerunud ja soovite pääseda ligi oma ettevõtte keskkonnale</span><span class="sxs-lookup"><span data-stu-id="1e7d8-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="1e7d8-123">Piirkondlik kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="1e7d8-123">Regional availability</span></span>

<span data-ttu-id="1e7d8-124">RCS on üldiselt saadaval järgmistes piirkondades:</span><span class="sxs-lookup"><span data-stu-id="1e7d8-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="1e7d8-125">Ameerika Ühendriigid</span><span class="sxs-lookup"><span data-stu-id="1e7d8-125">United States</span></span>
- <span data-ttu-id="1e7d8-126">India</span><span class="sxs-lookup"><span data-stu-id="1e7d8-126">India</span></span>
- <span data-ttu-id="1e7d8-127">Prantsusmaa</span><span class="sxs-lookup"><span data-stu-id="1e7d8-127">France</span></span>
- <span data-ttu-id="1e7d8-128">Euroopa</span><span class="sxs-lookup"><span data-stu-id="1e7d8-128">Europe</span></span>

<span data-ttu-id="1e7d8-129">Regioonide täieliku nimekirja saamiseks vt teemat [Dynamics 365 ja Power Platform: saadavus, andmete asukoht, keel ja lokaliseerimine](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="1e7d8-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="1e7d8-130">Seotud RCS-dokumentatsioon</span><span class="sxs-lookup"><span data-stu-id="1e7d8-130">Related RCS documentation</span></span>

<span data-ttu-id="1e7d8-131">Seotud komponentide kohta lisateabe saamiseks vaadake järgmist dokumentatsiooni.</span><span class="sxs-lookup"><span data-stu-id="1e7d8-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="1e7d8-132">**Globaalse hoidla:**</span><span class="sxs-lookup"><span data-stu-id="1e7d8-132">**Global repository:**</span></span>

    - [<span data-ttu-id="1e7d8-133">ER-i konfiguratsiooni loomine ja üleslaadimine globaalsesse reposse</span><span class="sxs-lookup"><span data-stu-id="1e7d8-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="1e7d8-134">Ühiskasutuse konfiguratsioon globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="1e7d8-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="1e7d8-135">Täiustatud filtreerimine globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="1e7d8-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="1e7d8-136">ER-i konfiguratsioonide allalaadimine globaalsest hoidlast</span><span class="sxs-lookup"><span data-stu-id="1e7d8-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="1e7d8-137">Konfiguratsioonide katkestamine globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="1e7d8-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="1e7d8-138">**Globaliseerimisfunktsioon:**</span><span class="sxs-lookup"><span data-stu-id="1e7d8-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="1e7d8-139">Regulatory Configuration Service (RCS) – globaliseerumise funktsioon</span><span class="sxs-lookup"><span data-stu-id="1e7d8-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)