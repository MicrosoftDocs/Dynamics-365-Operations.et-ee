---
title: Plaanimistöö tühistamine
description: See teema selgitab, kuidas tühistada aktiivne plaanimistöö, mis kasutab funktsiooni Plaanimise optimeerimine.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
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
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773944"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="510c1-103">Plaanimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="510c1-103">Cancel a planning job</span></span>

<span data-ttu-id="510c1-104">Microsoft Dynamics 365 Supply Chain Managementis saab tühistada aktiivse plaanimistöö, mis kasutab funktsiooni Plaanimise optimeerimine.</span><span class="sxs-lookup"><span data-stu-id="510c1-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="510c1-105">Aktiivse plaanimistöö tühistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="510c1-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="510c1-106">Tühistada saab ainult aktiivseid töid.</span><span class="sxs-lookup"><span data-stu-id="510c1-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="510c1-107">Avage **Koondplaneerimine \> Seadistus \> Plaanid**.</span><span class="sxs-lookup"><span data-stu-id="510c1-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="510c1-108">Valige planeerimise jaoks sobiv plaan.</span><span class="sxs-lookup"><span data-stu-id="510c1-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="510c1-109">Valige **Ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="510c1-109">Select **History**.</span></span>
4. <span data-ttu-id="510c1-110">Valige tühistamiseks plaanimistöö.</span><span class="sxs-lookup"><span data-stu-id="510c1-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="510c1-111">Valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="510c1-111">Select **Cancel**.</span></span>

<span data-ttu-id="510c1-112">Tööolek on **Tühistamine**, kuni Plaanimise optimeerimise teenus kinnitab, et töö on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="510c1-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="510c1-113">Olek muudetakse seejärel väärtusele **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="510c1-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="510c1-114">Olekumuudatuste nägemiseks peate värskendama lehte, valides nupu **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="510c1-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="510c1-115">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="510c1-115">Related resources</span></span>

[<span data-ttu-id="510c1-116">Plaanimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="510c1-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="510c1-117">Planeerimise optimiseerimise kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="510c1-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="510c1-118">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="510c1-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="510c1-119">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="510c1-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="510c1-120">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="510c1-120">Apply filters to a plan</span></span>](plan-filters.md)
