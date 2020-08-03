---
title: Dynamics 365 Supply Chain Managementi eemaldatud või aegunud funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Supply Chain Managementis.
author: kamaybac
manager: tfehr
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 07f37488747766dcca96884e204339b425bbd201
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597112"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a><span data-ttu-id="2f694-103">Dynamics 365 Supply Chain Managementi eemaldatud või aegunud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="2f694-103">Removed or deprecated features in Dynamics 365 Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f694-104">See teema uuendatakse, kui uued eemaldatud või aegunud funktsioonid on Dynamics 365 Supply Chain Managementi jaoks dokumenteeritud.</span><span class="sxs-lookup"><span data-stu-id="2f694-104">This topic will be updated as new removed or deprecated features are documented for Dynamics 365 Supply Chain Management.</span></span>

- <span data-ttu-id="2f694-105">*Eemaldatud* funktsioon pole tootes enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="2f694-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="2f694-106">*Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.</span><span class="sxs-lookup"><span data-stu-id="2f694-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="2f694-107">See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta.</span><span class="sxs-lookup"><span data-stu-id="2f694-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span>

> [!NOTE]
> <span data-ttu-id="2f694-108">Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="2f694-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="2f694-109">Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="2f694-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a><span data-ttu-id="2f694-110">Supply Chain Managementi väljalaskest 10.0.11 eemaldatud või aegunud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="2f694-110">Features removed or deprecated in the Supply Chain Management 10.0.11 release</span></span>

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a><span data-ttu-id="2f694-111">Supply Chain Managementi sisseehitatud koondplaneerimise mootori kasutamine jaotusstsenaariumite jaoks</span><span class="sxs-lookup"><span data-stu-id="2f694-111">Use of built-in Supply Chain Management master planning engine for distribution scenarios</span></span>

|   |  |
|------------|--------------------|
| <span data-ttu-id="2f694-112">**Aegumise/eemaldamise põhjus**</span><span class="sxs-lookup"><span data-stu-id="2f694-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="2f694-113">Jõudluse suurendamiseks ja SQL-andmebaasi koormuse minimeerimiseks koondplaneerimise käitamisel asendatakse Supply Chain Managementi sisseehitatud koondplaneerimise mootor planeerimise optimeerimisega.</span><span class="sxs-lookup"><span data-stu-id="2f694-113">To enhance performance and minimize the SQL database load during master planning runs, the built-in Supply Chain Management master planning engine is being replaced by Planning Optimization.</span></span> <span data-ttu-id="2f694-114">Planeerimise optimeerimine võimaldab kiiret planeerimise käitamist, mida saab teostada ka töövälisel ajal.</span><span class="sxs-lookup"><span data-stu-id="2f694-114">Planning Optimization allows for fast planning runs that can be performed even during office hours.</span></span> <span data-ttu-id="2f694-115">See võimaldab planeerijatel kohe nõudluse ja planeerimise parameetrite muutustele reageerida.</span><span class="sxs-lookup"><span data-stu-id="2f694-115">This enables planners to react immediately to changes in demand or planning parameters.</span></span> |
| <span data-ttu-id="2f694-116">**Asendatud teise funktsiooniga?**</span><span class="sxs-lookup"><span data-stu-id="2f694-116">**Replaced by another feature?**</span></span>   | <span data-ttu-id="2f694-117">Jah, planeerimise optimeerimine asendab Supply Chain Managementi olemasoleva sisseehitatud koondplaneerimise mootori.</span><span class="sxs-lookup"><span data-stu-id="2f694-117">Yes, Planning Optimization will replace the existing built-in Supply Chain Management master planning engine.</span></span> |
| <span data-ttu-id="2f694-118">**Mõjutatud tootealad**</span><span class="sxs-lookup"><span data-stu-id="2f694-118">**Product areas affected**</span></span>         | <span data-ttu-id="2f694-119">Supply Chain Management – Koondplaneerimine</span><span class="sxs-lookup"><span data-stu-id="2f694-119">Supply Chain Management - Master planning</span></span> |
| <span data-ttu-id="2f694-120">**Juurutamissuvand**</span><span class="sxs-lookup"><span data-stu-id="2f694-120">**Deployment option**</span></span>              | <span data-ttu-id="2f694-121">Ainult pilv.</span><span class="sxs-lookup"><span data-stu-id="2f694-121">Cloud only.</span></span> <span data-ttu-id="2f694-122">Kohapealsed juurutamised ei toeta planeerimise optimeerimist.</span><span class="sxs-lookup"><span data-stu-id="2f694-122">Planning Optimization is not supported with on-premises deployments.</span></span> |
| <span data-ttu-id="2f694-123">**Olek**</span><span class="sxs-lookup"><span data-stu-id="2f694-123">**Status**</span></span>                         | <span data-ttu-id="2f694-124">Aegunud.</span><span class="sxs-lookup"><span data-stu-id="2f694-124">Deprecated.</span></span> <span data-ttu-id="2f694-125">Alates 2021. aasta aprillist ei toeta jaotamisstsenaariumid enam Dynamics 365 Supply Chain Management-i sisseehitatud koondplaneerimise mootorit.</span><span class="sxs-lookup"><span data-stu-id="2f694-125">On April 2021, distribution scenarios will no longer be supported with the built-in Dynamics 365 Supply Chain Management master planning engine.</span></span> <span data-ttu-id="2f694-126">Kliendid peavad jaotamisstsenaariumite puhul kasutama koondplaneerimise arvutustes planeerimise optimeerimist.</span><span class="sxs-lookup"><span data-stu-id="2f694-126">For distribution scenarios, customers must use Planning Optimization for master planning calculations.</span></span> <span data-ttu-id="2f694-127">Lisateavet vt [Planeerimise optimeerimise dokumentatsioon](https://go.microsoft.com/fwlink/?linkid=2105830).</span><span class="sxs-lookup"><span data-stu-id="2f694-127">For more information, see [Planning Optimization documentation](https://go.microsoft.com/fwlink/?linkid=2105830).</span></span> <span data-ttu-id="2f694-128">Kliendid, kellel on Dynamics 365 Supply Chain Management-i kohapealsed juurutused, võivad jätkata Supply Chain Managementi koondplaneerimise mootori kasutamist jaotamisstsenaariumite jaoks ka pärast 2021. aasta aprilli.</span><span class="sxs-lookup"><span data-stu-id="2f694-128">Customers with on-premises deployments of Dynamics 365 Supply Chain Management may continue to use the Supply Chain Management master planning engine for distribution scenarios after April 2021.</span></span> <span data-ttu-id="2f694-129">Funktsioonitäiustusi aga enam tulevikus ei pakuta.</span><span class="sxs-lookup"><span data-stu-id="2f694-129">However, no more feature enhancements will be provided.</span></span> |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="2f694-130">Varasemad teatised eemaldatud või aegunud funktsioonidest</span><span class="sxs-lookup"><span data-stu-id="2f694-130">Previous announcements about removed or deprecated features</span></span>

<span data-ttu-id="2f694-131">Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span><span class="sxs-lookup"><span data-stu-id="2f694-131">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).</span></span>
