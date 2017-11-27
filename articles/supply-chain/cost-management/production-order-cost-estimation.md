---
title: Tootmistellimuse kulu hindamine
description: "Selles artiklis antakse teavet tootmiskulude hindamise kohta. Tootmiskulude hinnang varustab teid kauba tootmiseks planeeritud tootmistellimuse koguse kavandatud materjali ja võimsuse tarbimiskuludega."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 3ea3998014eb9ac2fd4610b5d52bd792d4f73869
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="production-order-cost-estimation"></a><span data-ttu-id="1cff5-104">Tootmistellimuse kulu hindamine</span><span class="sxs-lookup"><span data-stu-id="1cff5-104">Production order cost estimation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1cff5-105">Selles artiklis antakse teavet tootmiskulude hindamise kohta.</span><span class="sxs-lookup"><span data-stu-id="1cff5-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="1cff5-106">Tootmiskulude hinnang varustab teid kauba tootmiseks planeeritud tootmistellimuse koguse kavandatud materjali ja võimsuse tarbimiskuludega.</span><span class="sxs-lookup"><span data-stu-id="1cff5-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="1cff5-107">Pärast tootmistellimuse loomist tuleb hinnata tootmiskulusid.</span><span class="sxs-lookup"><span data-stu-id="1cff5-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="1cff5-108">Eesmärgiks on hinnata tootmisprotsessi kauba ja protsessi tarbimist, sest neid hinnanguid kasutatakse järgnevate planeerimiste ja tootmisprotsesside alusena.</span><span class="sxs-lookup"><span data-stu-id="1cff5-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="1cff5-109">Tootmiskulude hindamine</span><span class="sxs-lookup"><span data-stu-id="1cff5-109">Production cost estimation</span></span>
<span data-ttu-id="1cff5-110">Tootmiskulude hinnangud põhinevad järgmisel teabel.</span><span class="sxs-lookup"><span data-stu-id="1cff5-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="1cff5-111">Tootmistellimuse kogus</span><span class="sxs-lookup"><span data-stu-id="1cff5-111">The quantity on the production order</span></span>
-   <span data-ttu-id="1cff5-112">Tootmise koosluse komponendid</span><span class="sxs-lookup"><span data-stu-id="1cff5-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="1cff5-113">Tootmisprotsessi operatsioonid</span><span class="sxs-lookup"><span data-stu-id="1cff5-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="1cff5-114">Komponentidele ja operatsioonidele rakenduvad kaudsed kulud</span><span class="sxs-lookup"><span data-stu-id="1cff5-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="1cff5-115">Aktiivsed kuluandmed arvutamise kuupäeva seisuga</span><span class="sxs-lookup"><span data-stu-id="1cff5-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="1cff5-116">Kui tootmiskoosluses on fiktiivne rea kaup, kajastavad kalkulatsioonid fiktiivse kauba komponente ja protsessitoiminguid.</span><span class="sxs-lookup"><span data-stu-id="1cff5-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="1cff5-117">Hinnangulist toimingut võib kasutada hinnanguliste kulude ümberarvutamiseks, nii et need kajastavad uuendatud teavet.</span><span class="sxs-lookup"><span data-stu-id="1cff5-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="1cff5-118">Näiteks võib uuendatud teabeks olla muudatused tootmistellimuse koguses, tootmiskoosluse komponendid, tootmisprotsessi protsessitoimingud, kaudsed kulud, mis kohanduvad neile komponentidele ja operatsioonidele või aktiivsed kuluandmed ümberarvutuse kuupäevana.</span><span class="sxs-lookup"><span data-stu-id="1cff5-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="1cff5-119">Eeldatava omahinna arvutused pakuvad ka tootmiskauba müügihinda, mis põhineb kulupõhisel hinnalisandil.</span><span class="sxs-lookup"><span data-stu-id="1cff5-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="1cff5-120">Eeldatava omahinna arvutused võivad valikuliselt kohanduda viitetellimustele, mis kajastavad muid tootmistellimusi, mis on lingitud tootmistellimusele.</span><span class="sxs-lookup"><span data-stu-id="1cff5-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="1cff5-121">Eeldatavate omahindade vaatamine</span><span class="sxs-lookup"><span data-stu-id="1cff5-121">View the estimated costs</span></span>
<span data-ttu-id="1cff5-122">Pärast hinnangu käivitamist saate vaadata tulemusi lehel **Hinnakalkulatsioon**.</span><span class="sxs-lookup"><span data-stu-id="1cff5-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="1cff5-123">Hinnang kalkuleerib järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="1cff5-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="1cff5-124">**Tootmiskulu** – tootmiskulu on hinnangu ülemine rida.</span><span class="sxs-lookup"><span data-stu-id="1cff5-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="1cff5-125">See näitab tootmistellimuse käitamise kogukulu ja tootmise täielikku müügihinda.</span><span class="sxs-lookup"><span data-stu-id="1cff5-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="1cff5-126">See on kõigi hinnangu kuluridade summa.</span><span class="sxs-lookup"><span data-stu-id="1cff5-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="1cff5-127">**Protsessi või ressursi kulud** – protsessi või ressursi kulud on tootmisoperatsioonide kulud.</span><span class="sxs-lookup"><span data-stu-id="1cff5-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="1cff5-128">Need sisaldavad selliste elementide kulusid nagu seadistusaeg, käitusaeg ja üldkulud.</span><span class="sxs-lookup"><span data-stu-id="1cff5-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="1cff5-129">**Materjalikulud** – materjalikulud on kauba tootmiseks nõutavate koosluse komponentide kulud ja hinnad.</span><span class="sxs-lookup"><span data-stu-id="1cff5-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="1cff5-130">Need kulud on eelnevalt kehtestatud ja süsteemi sisestatud.</span><span class="sxs-lookup"><span data-stu-id="1cff5-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="1cff5-131">Kuluhinnangu muud kasutused</span><span class="sxs-lookup"><span data-stu-id="1cff5-131">Other uses of cost estimation</span></span>
<span data-ttu-id="1cff5-132">Kuluhinnang annab ka järgmist teavet:</span><span class="sxs-lookup"><span data-stu-id="1cff5-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="1cff5-133">selgitavad hinnapakkumised,</span><span class="sxs-lookup"><span data-stu-id="1cff5-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="1cff5-134">tellimuse tulususe hinnangud,</span><span class="sxs-lookup"><span data-stu-id="1cff5-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="1cff5-135">toormaterjali kasutamise hinnangud,</span><span class="sxs-lookup"><span data-stu-id="1cff5-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="1cff5-136">eelmiste toodete kuluandmete võrdluse,</span><span class="sxs-lookup"><span data-stu-id="1cff5-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="1cff5-137">eelarve ja prognoosi teabe,</span><span class="sxs-lookup"><span data-stu-id="1cff5-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="1cff5-138">kindla kulu säilitamiseks vajaliku tootmismahu hinnangu.</span><span class="sxs-lookup"><span data-stu-id="1cff5-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>





