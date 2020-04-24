---
title: Planeerimise optimeerimise sobivuse analüüs
description: Selles teemas selgitatakse, kuidas kontrollida praegust seadistust ja andmeid planeerimise optimeerimise funktsiooni võimaluste suhtes.
author: ChristianRytt
manager: tfehr
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
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
ms.openlocfilehash: 17114d4c0ef2c74ab1bb56d41e4a008150c21f36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208750"
---
# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="9a42f-103">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="9a42f-103">Planning Optimization fit analysis</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a42f-104">Et näha, kui hästi teie praegune seadistus ja andmed planeerimise optimeerimise funktsiooniga ühilduvad, avage **Koondplaneerimine** \> **Seadistus** \> **Planeerimise optimeerimise sobivuse analüüs** ja valige seejärel **Käivita analüüs**.</span><span class="sxs-lookup"><span data-stu-id="9a42f-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="9a42f-105">Kui analüüs tuvastab vastuolusid, loetletakse need samal lehel.</span><span class="sxs-lookup"><span data-stu-id="9a42f-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="9a42f-106">(Analüüsimise käitamiseks võib kuluda mõni minut.)</span><span class="sxs-lookup"><span data-stu-id="9a42f-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="9a42f-107">Kui leitakse vastuolusid, saate planeerimise optimeerimist endiselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="9a42f-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="9a42f-108">Sobivuse analüüsi tulemused näitavad lihtsalt kohti, kus planeerimise teenus ei arvesta teie praeguse seadistusega.</span><span class="sxs-lookup"><span data-stu-id="9a42f-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="9a42f-109">Teisisõnu näitavad need kohti, kus mõnda protsessi võidakse ignoreerida või ei toetata.</span><span class="sxs-lookup"><span data-stu-id="9a42f-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="9a42f-110">Analüüsi tulemused: näide 1</span><span class="sxs-lookup"><span data-stu-id="9a42f-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="9a42f-111">**Funktsioon:** tootmine</span><span class="sxs-lookup"><span data-stu-id="9a42f-111">**Feature:** Production</span></span>
- <span data-ttu-id="9a42f-112">**Väljastus:** kaubad, mille koosluse tase on suurem kui null: 56</span><span class="sxs-lookup"><span data-stu-id="9a42f-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="9a42f-113">**Selgitus:** sobivuse analüüsis leiti 56 kaupa, millel on tootmiseks koosluse seadistus.</span><span class="sxs-lookup"><span data-stu-id="9a42f-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="9a42f-114">Kuna planeerimise optimeerimise praegune versiooni ei toetata tootmist, loob planeerimise optimeerimine plaanitud tootmistellimuste asemel plaanitud ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="9a42f-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="9a42f-115">Samuti kuvatakse hoiatus, mis loendab mõjutatud kaubad.</span><span class="sxs-lookup"><span data-stu-id="9a42f-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="9a42f-116">Analüüsi tulemused: näide 2</span><span class="sxs-lookup"><span data-stu-id="9a42f-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="9a42f-117">**Funktsioon:** tegevused</span><span class="sxs-lookup"><span data-stu-id="9a42f-117">**Feature:** Actions</span></span>
- <span data-ttu-id="9a42f-118">**Väljastus:** laovarude grupid, mille tegevuse arvutamine on lubatud: 6</span><span class="sxs-lookup"><span data-stu-id="9a42f-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="9a42f-119">**Selgitus:** sobivuse analüüs leidis kuus laovarude gruppi, kus tegevuse arvutamine on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="9a42f-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="9a42f-120">Kuna planeerimise optimeerimise praegune versioon ei toetata tegevusi, siis koondplaneerimise käigus tegevusi ei looda.</span><span class="sxs-lookup"><span data-stu-id="9a42f-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="9a42f-121">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="9a42f-121">Related resources</span></span>

[<span data-ttu-id="9a42f-122">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="9a42f-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="9a42f-123">Planeerimise optimiseerimise kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="9a42f-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="9a42f-124">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="9a42f-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="9a42f-125">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="9a42f-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="9a42f-126">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="9a42f-126">Cancel a planning job</span></span>](cancel-planning-job.md)
