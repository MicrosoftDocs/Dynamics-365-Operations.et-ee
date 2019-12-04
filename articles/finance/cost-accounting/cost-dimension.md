---
title: Dimensioonide loomine ja dimensiooniliikmete importimine
description: Kuluarvestus on sõltumatu moodul, mis nõuab koondandmeid teistest moodulitest.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 575b27de845d931c990b1d19254b5218fa6e4199
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770846"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="3b35e-103">Dimensioonide loomine ja dimensiooniliikmete importimine</span><span class="sxs-lookup"><span data-stu-id="3b35e-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b35e-104">Kuluarvestus on sõltumatu moodul, mis nõuab andmeid teistest moodulitest.</span><span class="sxs-lookup"><span data-stu-id="3b35e-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="3b35e-105">Need andmed on jaotatud järgmistesse kategooriatesse:</span><span class="sxs-lookup"><span data-stu-id="3b35e-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="3b35e-106">Kuluelemendid</span><span class="sxs-lookup"><span data-stu-id="3b35e-106">Cost elements</span></span>
-  <span data-ttu-id="3b35e-107">Kuluobjektid</span><span class="sxs-lookup"><span data-stu-id="3b35e-107">Cost objects</span></span>
-  <span data-ttu-id="3b35e-108">Statistilised dimensioonid</span><span class="sxs-lookup"><span data-stu-id="3b35e-108">Statistical dimensions</span></span>

<span data-ttu-id="3b35e-109">**Kuluelement** vastab kuluga seotud kaubale kontoplaanis.</span><span class="sxs-lookup"><span data-stu-id="3b35e-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="3b35e-110">**Kuluobjekt** vastab mis tahes finantsdimensiooni tüübile (nt tooted, kulukeskused ja projektid, mida soovite prognoosida, millele kulusid eraldada või mida otse mõõta).</span><span class="sxs-lookup"><span data-stu-id="3b35e-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="3b35e-111">**Statistilist dimensiooni** ja selle liikmeid kasutatakse mitterahaliste kirjete registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="3b35e-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="3b35e-112">Statistilise dimensiooni liikmeid saab kasutada eraldamisalusena kulujaotuses ja eraldamises.</span><span class="sxs-lookup"><span data-stu-id="3b35e-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="3b35e-113">Järgnev diagramm illustreerib kuluarvestuses kasutatavaid dimensioone.</span><span class="sxs-lookup"><span data-stu-id="3b35e-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="3b35e-114">[![Kuluarvestuse dimensioonid](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="3b35e-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="3b35e-115">Kui andmed on kuluarvestusse imporditud, saab neid kasutada mitmesuguste vaatenurkade koostamiseks, mis annavad ülevaateid kõigi organisatsiooni tasandite juhtidele.</span><span class="sxs-lookup"><span data-stu-id="3b35e-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="3b35e-116">Järgmistes teemades antakse teavet dimensioonide loomise ja dimensiooniliikmete importimise kohta.</span><span class="sxs-lookup"><span data-stu-id="3b35e-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="3b35e-117">Kuluelemendi dimensioonid</span><span class="sxs-lookup"><span data-stu-id="3b35e-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="3b35e-118">Kuluelementide loomine</span><span class="sxs-lookup"><span data-stu-id="3b35e-118">Create cost elements</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="3b35e-119">Kuluobjekti dimensioonid</span><span class="sxs-lookup"><span data-stu-id="3b35e-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="3b35e-120">Kuluelemendi dimensiooniliikmete vastendamine dimensiooniliikmete ühtse mudeliga</span><span class="sxs-lookup"><span data-stu-id="3b35e-120">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="3b35e-121">Kuluelemendi dimensiooni vastendamine</span><span class="sxs-lookup"><span data-stu-id="3b35e-121">Map a cost element dimension</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="3b35e-122">Statistilise dimensiooni liikmed ja statistiliste mõõtude pakkuja mallid</span><span class="sxs-lookup"><span data-stu-id="3b35e-122">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)





