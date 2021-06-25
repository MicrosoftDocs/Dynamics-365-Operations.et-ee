---
title: Regulatory Configuration Service
description: See teema annab ülevaate Regulatory Configuration Service (RCS) võimalustest ja selgitab, kuidas teenusele juurde pääseda.
author: JaneA07
ms.date: 06/04/2021
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
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216558"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="7a8c8-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="7a8c8-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a8c8-104">Regulatory Configuration Service (RCS) on autonoomne disainer ja elutsükli haldamise teenus koodita/vähese koodiga globaliseerumisfunktsioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="7a8c8-105">RCS-i globaliseerumise sidusrühmad laiendavad ja kohandavad peamisi globaliseerumisvaldkondi nagu maksud, e-arved, regulatiivne aruandlus, pangandus ja äridokumendid, ilma et nad peaksid arendajaid kaasama.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="7a8c8-106">See koodita/vähese koodiga globaalne lähenemine muudab globaliseerumise lihtsamaks, kiiremaks ja kulutõhusamaks, et seda luua või laiendada.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="7a8c8-107">RCS pakub järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="7a8c8-108">Kõigi elektroonilise aruandluse (ER) pakutavate funktsioonide tugi.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="7a8c8-109">Uute globaliseerumismikroteenuste konfigureerimise eeltingimus.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="7a8c8-110">Elektroonilise arvelduse tugi.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="7a8c8-111">Lisateavet leiate teemast [E-arveldus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span><span class="sxs-lookup"><span data-stu-id="7a8c8-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="7a8c8-112">Toetab maksuarvestust.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="7a8c8-113">Lisateavet vt jaotisest [Maksuteenus](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span><span class="sxs-lookup"><span data-stu-id="7a8c8-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="7a8c8-114">Uute globaliseerumisfunktsioonide funktsioonide tugi, mis lihtsustab mitmekomponendiliste funktsioonide elutsükli haldamist ning pakub lisavõimalusi toimingute konfigureerimiseks ja funktsiooniparameetrite seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="7a8c8-115">Lisateavet vt teemast [Regulatory Configuration Service – globaliseerumisteenuste lihtsustatud globaliseerumisfunktsioonide haldamine](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span><span class="sxs-lookup"><span data-stu-id="7a8c8-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="7a8c8-116">Globaalses hoidlas kohandatud konfiguratsioonide tsentraliseeritud avaldamise, salvestamise ja ühiskasutuse tugi, et lihtsustada konfiguratsioonihaldust, ilma et oleks vaja kasutada Microsoft Dynamics Lifecycle Services (LCS) teenuseid.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="7a8c8-117">RCS ligipääs</span><span class="sxs-lookup"><span data-stu-id="7a8c8-117">Access RCS</span></span>

<span data-ttu-id="7a8c8-118">RCS-i saate registreeruda või sisse logida [Regulatory Configuration Service lehel](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="7a8c8-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RCS-i registreerimine ja sisselogimine](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="7a8c8-120">Vaadake lehel **Regulatory Configuration Service** üle ja nõustuge teenuse kasutamise täiendavate tingimustega ning valige üks järgmistest nuppudest.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="7a8c8-121">**Registreeri**, kui olete teenuse esmakordne kasutaja ja kasutate ettevõtte meiliaadressi oma organisatsiooni teenusekeskkonna ettevalmistamiseks</span><span class="sxs-lookup"><span data-stu-id="7a8c8-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="7a8c8-122">**Logi sisse**, kui olete varem teenuse kasutajaks registreerunud ja soovite pääseda ligi oma ettevõtte keskkonnale</span><span class="sxs-lookup"><span data-stu-id="7a8c8-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="7a8c8-123">Piirkondlik kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="7a8c8-123">Regional availability</span></span>

<span data-ttu-id="7a8c8-124">RCS on üldiselt saadaval järgmistes piirkondades:</span><span class="sxs-lookup"><span data-stu-id="7a8c8-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="7a8c8-125">Ameerika Ühendriigid</span><span class="sxs-lookup"><span data-stu-id="7a8c8-125">United States</span></span>
- <span data-ttu-id="7a8c8-126">India</span><span class="sxs-lookup"><span data-stu-id="7a8c8-126">India</span></span>
- <span data-ttu-id="7a8c8-127">Prantsusmaa</span><span class="sxs-lookup"><span data-stu-id="7a8c8-127">France</span></span>
- <span data-ttu-id="7a8c8-128">Euroopa</span><span class="sxs-lookup"><span data-stu-id="7a8c8-128">Europe</span></span>

<span data-ttu-id="7a8c8-129">Regioonide täieliku nimekirja saamiseks vt teemat [Dynamics 365 ja Power Platform: saadavus, andmete asukoht, keel ja lokaliseerimine](https://aka.ms/dynamics_365_international_availability_deck).</span><span class="sxs-lookup"><span data-stu-id="7a8c8-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="7a8c8-130">RCS väikeettevõte</span><span class="sxs-lookup"><span data-stu-id="7a8c8-130">RCS default company</span></span>

<span data-ttu-id="7a8c8-131">RCS-is kasutatav kujundusaja funktsioon on ühiskasutuses kõigi ettevõtete vahel.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="7a8c8-132">Ettevõttepõhiseid funktsioone pole.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-132">There is no company-specific functionality.</span></span> <span data-ttu-id="7a8c8-133">Seetõttu soovitame teil kasutada ühte ettevõtet, **DAT**, koos teie RCS-keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="7a8c8-134">Mõne stsenaariumi puhul võite siiski soovida, et ER-vormingud kasutaks konkreetse juriidilise isikuga seotud parameetreid.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="7a8c8-135">Ainult sellistes stsenaariumides peaksite kasutama ettevõtte vaikelülitit.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="7a8c8-136">Näite vaatamiseks vt [ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="7a8c8-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="7a8c8-137">Seotud RCS-dokumentatsioon</span><span class="sxs-lookup"><span data-stu-id="7a8c8-137">Related RCS documentation</span></span>

<span data-ttu-id="7a8c8-138">Seotud komponentide kohta lisateabe saamiseks vaadake järgmisi peatükke:</span><span class="sxs-lookup"><span data-stu-id="7a8c8-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="7a8c8-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="7a8c8-139">**RCS:**</span></span>

    - [<span data-ttu-id="7a8c8-140">ER-konfiguratsioonide loomine RCS-is ja üleslaadimine globaalsesse hoidlasse</span><span class="sxs-lookup"><span data-stu-id="7a8c8-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="7a8c8-141">**Globaalse hoidla:**</span><span class="sxs-lookup"><span data-stu-id="7a8c8-141">**Global repository:**</span></span>

    - [<span data-ttu-id="7a8c8-142">ER-i konfiguratsiooni loomine ja üleslaadimine globaalsesse reposse</span><span class="sxs-lookup"><span data-stu-id="7a8c8-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="7a8c8-143">Ühiskasutuse konfiguratsioon globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="7a8c8-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="7a8c8-144">Täiustatud filtreerimine globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="7a8c8-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="7a8c8-145">ER-i konfiguratsioonide allalaadimine globaalsest hoidlast</span><span class="sxs-lookup"><span data-stu-id="7a8c8-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="7a8c8-146">Konfiguratsioonide katkestamine globaalses hoidlas</span><span class="sxs-lookup"><span data-stu-id="7a8c8-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="7a8c8-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine</span><span class="sxs-lookup"><span data-stu-id="7a8c8-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="7a8c8-148">**Globaliseerimisfunktsioon:**</span><span class="sxs-lookup"><span data-stu-id="7a8c8-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="7a8c8-149">Regulatory Configuration Service (RCS) – globaliseerumise funktsioon</span><span class="sxs-lookup"><span data-stu-id="7a8c8-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="7a8c8-150">RCS logimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="7a8c8-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="7a8c8-151">Kui registreerite teenuse leheküljelt RCS-i, võib teil tekkida probleem, mis on seotud rakendusega Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="7a8c8-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="7a8c8-152">Tõrketeade näitab, et RCS-ile registreerimine on praegu välja lülitatud ja tuleb sisse lülitada, enne kui saate allkirjastamisprotsessi lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![RCS-i registreerumise tõrketeade](media/01_RCSSignUpError.jpg)

<span data-ttu-id="7a8c8-154">Probleem ilmneb, kuna olete blokeerinud registreerumise sihttellimustele ja atribuut peab olema teie `AllowAdHocSubscriptions` rentnikus lubatud.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="7a8c8-155">Kui teie IT-osakond haldab teie organisatsiooni Azure'i rentnikku, võtke probleemist aru anda selle osakonnaga ühendust.</span><span class="sxs-lookup"><span data-stu-id="7a8c8-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="7a8c8-156">Kui vastutate Azure rentnike haldamise eest, saate probleemid lahendada, järgides [Mis on iseteeninduse registreerimine rakenduses Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span><span class="sxs-lookup"><span data-stu-id="7a8c8-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
