---
title: Planeerimise optimeerimise sobivuse analüüs
description: Selles teemas selgitatakse, kuidas kontrollida praegust seadistust ja andmeid planeerimise optimeerimise funktsiooni võimaluste suhtes.
author: ChristianRytt
manager: AnnBe
ms.date: 1030/2019
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
ms.openlocfilehash: 26b067f8526df16474c0ab52d0abf816170ff5cb
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773942"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="9bd8b-103">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="9bd8b-103">Planning Optimization fit analysis</span></span>

<span data-ttu-id="9bd8b-104">Et näha, kui hästi teie praegune seadistus ja andmed planeerimise optimeerimise funktsiooniga ühilduvad, avage **Koondplaneerimine** \> **Seadistus** \> **Planeerimise optimeerimise sobivuse analüüs** ja valige seejärel **Käivita analüüs**.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="9bd8b-105">Kui analüüs tuvastab vastuolusid, loetletakse need samal lehel.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="9bd8b-106">(Analüüsimise käitamiseks võib kuluda mõni minut.)</span><span class="sxs-lookup"><span data-stu-id="9bd8b-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="9bd8b-107">Kui leitakse vastuolusid, saate planeerimise optimeerimist endiselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="9bd8b-108">Sobivuse analüüsi tulemused näitavad lihtsalt kohti, kus planeerimise teenus ei arvesta teie praeguse seadistusega.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="9bd8b-109">Teisisõnu näitavad need kohti, kus mõnda protsessi võidakse ignoreerida või ei toetata.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="9bd8b-110">Analüüsi tulemused: näide 1</span><span class="sxs-lookup"><span data-stu-id="9bd8b-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="9bd8b-111">**Funktsioon:** tootmine</span><span class="sxs-lookup"><span data-stu-id="9bd8b-111">**Feature:** Production</span></span>
- <span data-ttu-id="9bd8b-112">**Väljastus:** kaubad, mille koosluse tase on suurem kui null: 56</span><span class="sxs-lookup"><span data-stu-id="9bd8b-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="9bd8b-113">**Selgitus:** sobivuse analüüsis leiti 56 kaupa, millel on tootmiseks koosluse seadistus.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="9bd8b-114">Kuna planeerimise optimeerimise praegune versiooni ei toetata tootmist, loob planeerimise optimeerimine plaanitud tootmistellimuste asemel plaanitud ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="9bd8b-115">Samuti kuvatakse hoiatus, mis loendab mõjutatud kaubad.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="9bd8b-116">Analüüsi tulemused: näide 2</span><span class="sxs-lookup"><span data-stu-id="9bd8b-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="9bd8b-117">**Funktsioon:** tegevused</span><span class="sxs-lookup"><span data-stu-id="9bd8b-117">**Feature:** Actions</span></span>
- <span data-ttu-id="9bd8b-118">**Väljastus:** laovarude grupid, mille tegevuse arvutamine on lubatud: 6</span><span class="sxs-lookup"><span data-stu-id="9bd8b-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="9bd8b-119">**Selgitus:** sobivuse analüüs leidis kuus laovarude gruppi, kus tegevuse arvutamine on sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="9bd8b-120">Kuna planeerimise optimeerimise praegune versioon ei toetata tegevusi, siis koondplaneerimise käigus tegevusi ei looda.</span><span class="sxs-lookup"><span data-stu-id="9bd8b-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="9bd8b-121">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="9bd8b-121">Related resources</span></span>

[<span data-ttu-id="9bd8b-122">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="9bd8b-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="9bd8b-123">Planeerimise optimiseerimise kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="9bd8b-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="9bd8b-124">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="9bd8b-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="9bd8b-125">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="9bd8b-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="9bd8b-126">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="9bd8b-126">Cancel a planning job</span></span>](cancel-planning-job.md)
