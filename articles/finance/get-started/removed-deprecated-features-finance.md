---
title: Dynamics 365 Financei eemaldatud või aegunud funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Finance'ist.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127973"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a><span data-ttu-id="ad234-103">Dynamics 365 Financei eemaldatud või aegunud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="ad234-103">Removed or deprecated features in Dynamics 365 Finance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad234-104">See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Finance'ist.</span><span class="sxs-lookup"><span data-stu-id="ad234-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Finance.</span></span>

- <span data-ttu-id="ad234-105">*Eemaldatud* funktsioon pole tootes enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="ad234-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="ad234-106">*Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.</span><span class="sxs-lookup"><span data-stu-id="ad234-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="ad234-107">See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta.</span><span class="sxs-lookup"><span data-stu-id="ad234-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="ad234-108">Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="ad234-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="ad234-109">Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="ad234-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a><span data-ttu-id="ad234-110">Finance'i väljalaskest 10.0.12 eemaldatud või aegunud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="ad234-110">Features removed or deprecated in the Finance 10.0.12 release</span></span>

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a><span data-ttu-id="ad234-111">Poola SSRS-i aruanded: arvestatud käibemaksu register, sisendkäibemaksu register, EL-i koondkäibemaksu register – funktsiooni viide PL-00014</span><span class="sxs-lookup"><span data-stu-id="ad234-111">Polish SSRS reports: Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="ad234-112">**Aegumise/eemaldamise põhjus**</span><span class="sxs-lookup"><span data-stu-id="ad234-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ad234-113">Juriidiliselt pole vajalik.</span><span class="sxs-lookup"><span data-stu-id="ad234-113">Not legally required.</span></span>  |
| <span data-ttu-id="ad234-114">**Asendatud teise funktsiooniga?**</span><span class="sxs-lookup"><span data-stu-id="ad234-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ad234-115">Jah (Exceli vorming standardse auditifaili jaoks KM-i deklaratsiooniga – JPK_VDEK)</span><span class="sxs-lookup"><span data-stu-id="ad234-115">Yes (Excel format for Standard Audit File with VAT declaration - JPK_VDEK)</span></span> |
| <span data-ttu-id="ad234-116">**Mõjutatud tootealad**</span><span class="sxs-lookup"><span data-stu-id="ad234-116">**Product areas affected**</span></span>         | <span data-ttu-id="ad234-117">Rakendus</span><span class="sxs-lookup"><span data-stu-id="ad234-117">Application</span></span> |
| <span data-ttu-id="ad234-118">**Juurutamissuvand**</span><span class="sxs-lookup"><span data-stu-id="ad234-118">**Deployment option**</span></span>              | <span data-ttu-id="ad234-119">Kõik</span><span class="sxs-lookup"><span data-stu-id="ad234-119">All</span></span> |
| <span data-ttu-id="ad234-120">**Olek**</span><span class="sxs-lookup"><span data-stu-id="ad234-120">**Status**</span></span>                         | <span data-ttu-id="ad234-121">Aegub 1. juuliks 2021, plaanime mitte enam toetada SSRS-i aruandeid: **arvestatud käibemaksu register, sisendkäibemaksu register, EL-i koondkäibemaksu register – funktsiooni viide PL-00014**.</span><span class="sxs-lookup"><span data-stu-id="ad234-121">Deprecated: By July 1, 2021, we plan to no longer support the SSRS reports: **Sales VAT register, Purchase VAT register, EU summary VAT register – Feature reference PL-00014**.</span></span> <span data-ttu-id="ad234-122">Selle asemel võetakse kasutusele Exceli vormingu standardse auditifaili näide koos KM-i deklaratsiooniga (JPK_VDEK).</span><span class="sxs-lookup"><span data-stu-id="ad234-122">Excel format example for Standard Audit File with VAT declaration (JPK_VDEK) will be introduced instead.</span></span> |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a><span data-ttu-id="ad234-123">Finance'i väljalaskest 10.0.7 eemaldatud või aegunud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="ad234-123">Features removed or deprecated in the Finance 10.0.7 release</span></span>

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a><span data-ttu-id="ad234-124">Töövoo taotluse muutmise dialoogiboks ei sisalda enam kasutaja valiku ripploendit</span><span class="sxs-lookup"><span data-stu-id="ad234-124">Workflow request change dialog box no longer includes user selection drop-down list</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="ad234-125">**Aegumise/eemaldamise põhjus**</span><span class="sxs-lookup"><span data-stu-id="ad234-125">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="ad234-126">Muudetud funktsiooniks, mis sisaldab konto gruppide valikut.</span><span class="sxs-lookup"><span data-stu-id="ad234-126">Changed to the feature with account groups selection.</span></span>  |
| <span data-ttu-id="ad234-127">**Asendatud teise funktsiooniga?**</span><span class="sxs-lookup"><span data-stu-id="ad234-127">**Replaced by another feature?**</span></span>   | <span data-ttu-id="ad234-128">Jah</span><span class="sxs-lookup"><span data-stu-id="ad234-128">Yes</span></span> |
| <span data-ttu-id="ad234-129">**Mõjutatud tootealad**</span><span class="sxs-lookup"><span data-stu-id="ad234-129">**Product areas affected**</span></span>         | <span data-ttu-id="ad234-130">Töövoog</span><span class="sxs-lookup"><span data-stu-id="ad234-130">Workflow</span></span> |
| <span data-ttu-id="ad234-131">**Juurutamissuvand**</span><span class="sxs-lookup"><span data-stu-id="ad234-131">**Deployment option**</span></span>              | <span data-ttu-id="ad234-132">Kõik</span><span class="sxs-lookup"><span data-stu-id="ad234-132">All</span></span> |
| <span data-ttu-id="ad234-133">**Olek**</span><span class="sxs-lookup"><span data-stu-id="ad234-133">**Status**</span></span>                         | <span data-ttu-id="ad234-134">Aegub: 1. detsembril 2020. Me ei plaani enam toetada Hiina kandetüüpide seadistust ilma konto gruppide valikuta.</span><span class="sxs-lookup"><span data-stu-id="ad234-134">Deprecated: By December 1, 2020, we plan to no longer support Chinese voucher types setup without Account groups selection.</span></span> <span data-ttu-id="ad234-135">Lisateavet uue kujunduse kohta leiate teemast [Mis on uut versioonis 10.0.7](whats-new-changed-10-0-7.md).</span><span class="sxs-lookup"><span data-stu-id="ad234-135">Find more details about the new design in [What's new in 10.0.7](whats-new-changed-10-0-7.md).</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="ad234-136">Varasemad teatised eemaldatud või aegunud funktsioonidest</span><span class="sxs-lookup"><span data-stu-id="ad234-136">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="ad234-137">Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="ad234-137">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
