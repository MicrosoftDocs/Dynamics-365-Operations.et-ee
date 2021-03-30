---
title: Plaanile filtrite rakendamine
description: Selles teemas selgitatakse, kuidas kasutada filtreid plaaniga, kui kasutatakse planeerimise optimeerimise funktsiooni.
author: ChristianRytt
manager: tfehr
ms.date: 01/08/2020
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
ms.openlocfilehash: b5262cc5dc72ffcc50770cf5a2e2dda216d7ff8e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212098"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="b1393-103">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="b1393-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b1393-104">Planeerimise optimeerimise funktsiooni kasutamisel saate rakendada plaanile filtri.</span><span class="sxs-lookup"><span data-stu-id="b1393-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="b1393-105">Suvand **Plaani filter** rakendatakse alati koondplaneerimise käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="b1393-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="b1393-106">Suvand **Plaani filter** on kasulik, kui soovite piiritleda plaani kindlale tootegrupile ja veenduda, et ükski teine kaup ei oleks tulemiks saadud koondplaneerimisse kaasatud.</span><span class="sxs-lookup"><span data-stu-id="b1393-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="b1393-107">Kui suvandit **Plaani filter** rakendatakse ja koondplaneerimise käivitamisel rakendatakse ka käitusaja filtrit, kaasatakse planeerimise käivitamisel ainult kahe filtri lõikuv osa.</span><span class="sxs-lookup"><span data-stu-id="b1393-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="b1393-108">Suvandile **Plaani filter** pääseb optimeerimise planeerimisel kasutamise ajal juurde suvandist **Koondplaanid**.</span><span class="sxs-lookup"><span data-stu-id="b1393-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b1393-109">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="b1393-109">Example scenario</span></span>

<span data-ttu-id="b1393-110">Plaani filter on seadistatud hõlmama kaupu A, B ja C. Koondplaneerimise käitamine käivitatakse seejärel sama plaani jaoks, kuid rakendatakse erinevaid käitusaja filtreid.</span><span class="sxs-lookup"><span data-stu-id="b1393-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="b1393-111">**Käitusaja filter, mis sisaldab kaupa D**: ühtegi kaupa ei ole planeeritud, kuna plaani filtri ja käitusaja filtri vahel pole lõikuvat osa.</span><span class="sxs-lookup"><span data-stu-id="b1393-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="b1393-112">**Käitusaja filter, mis sisaldab kaupa A ja D**: planeerimise käivitamisel kaasatakse ainult kaup A, kuna kaup D pole plaani filtri osa.</span><span class="sxs-lookup"><span data-stu-id="b1393-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="b1393-113">**Käitusaja filter, mis sisaldab kaupa B**: planeerimise käivitamisel kaasatakse ainult kaup B ja eelmise kauba A planeerimise väljund hoitakse alles.</span><span class="sxs-lookup"><span data-stu-id="b1393-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="b1393-114">**Käitusaja filter, mis sisaldab kõiki kaupu (tühi filter)** : kaubad A, B ja C kaasatakse planeerimise käivitamisse ning kaupade A ja B eelmine planeerimise väljund kirjutatakse üle.</span><span class="sxs-lookup"><span data-stu-id="b1393-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="b1393-115">Peaksite vältima plaani filtri seadmist plaanile, mis on valitud kui **Praegune dünaamiline koondplaan** lehel **Koondplaneerimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b1393-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="b1393-116">Vastasel juhul on dünaamilise koondplaani funktsioon piiratud filtreeritud kaupadega.</span><span class="sxs-lookup"><span data-stu-id="b1393-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="b1393-117">Näiteks kui uuendatakse kauba netonõudeid, mis ei ole plaani filtri osaks, tulemusi ei looda.</span><span class="sxs-lookup"><span data-stu-id="b1393-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="b1393-118">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="b1393-118">Related resources</span></span>

[<span data-ttu-id="b1393-119">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="b1393-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="b1393-120">Planeerimise optimiseerimise kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="b1393-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="b1393-121">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="b1393-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="b1393-122">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="b1393-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="b1393-123">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="b1393-123">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]