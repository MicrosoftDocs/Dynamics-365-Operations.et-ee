---
title: Plaanimistöö tühistamine
description: See teema selgitab, kuidas tühistada aktiivne plaanimistöö, mis kasutab funktsiooni Plaanimise optimeerimine.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 7cee11e6d9e8bc2fe83f5369554ae9ff9ee2b741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008212"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="c6682-103">Plaanimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="c6682-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c6682-104">Microsoft Dynamics 365 Supply Chain Managementis saab tühistada aktiivse plaanimistöö, mis kasutab funktsiooni Plaanimise optimeerimine.</span><span class="sxs-lookup"><span data-stu-id="c6682-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="c6682-105">Kui valite dialoogiboksis käsu **Tühista**, kui plaanimise optimeerimise töö käivitatakse otse kasutajaliidesest (mitte taustal), ei tühista see plaanimise optimeerimise tööd.</span><span class="sxs-lookup"><span data-stu-id="c6682-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="c6682-106">Isegi kui kuvatakse hoiatusteade (nt „Toiming tühistatud”), tuleb teil siiski kasutada järgmisi samme, et tühistada plaanimise optimeerimisega plaanimistöö.</span><span class="sxs-lookup"><span data-stu-id="c6682-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="c6682-107">Aktiivse plaanimistöö tühistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c6682-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="c6682-108">Tühistada saab ainult aktiivseid töid.</span><span class="sxs-lookup"><span data-stu-id="c6682-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="c6682-109">Avage **Koondplaneerimine \> Seadistus \> Plaanid**.</span><span class="sxs-lookup"><span data-stu-id="c6682-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="c6682-110">Valige planeerimise jaoks sobiv plaan.</span><span class="sxs-lookup"><span data-stu-id="c6682-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="c6682-111">Valige **Ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="c6682-111">Select **History**.</span></span>
4. <span data-ttu-id="c6682-112">Valige tühistamiseks plaanimistöö.</span><span class="sxs-lookup"><span data-stu-id="c6682-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="c6682-113">Valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="c6682-113">Select **Cancel**.</span></span>

<span data-ttu-id="c6682-114">Tööolek on **Tühistamine**, kuni Plaanimise optimeerimise teenus kinnitab, et töö on tühistatud.</span><span class="sxs-lookup"><span data-stu-id="c6682-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="c6682-115">Olek muudetakse seejärel väärtusele **Tühistatud**.</span><span class="sxs-lookup"><span data-stu-id="c6682-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="c6682-116">Olekumuudatuste nägemiseks peate värskendama lehte, valides nupu **Värskenda**.</span><span class="sxs-lookup"><span data-stu-id="c6682-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6682-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c6682-117">Additional resources</span></span>

[<span data-ttu-id="c6682-118">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="c6682-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="c6682-119">Planeerimise optimeerimisega alustamine</span><span class="sxs-lookup"><span data-stu-id="c6682-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="c6682-120">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="c6682-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="c6682-121">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="c6682-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="c6682-122">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="c6682-122">Apply filters to a plan</span></span>](plan-filters.md)
