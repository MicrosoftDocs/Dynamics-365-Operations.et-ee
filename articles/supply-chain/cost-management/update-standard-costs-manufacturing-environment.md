---
title: "Tootmiskeskkonnas standardkulude värskendamine"
description: "Selles artiklis antakse juhiseid tootmiskeskkonnas standardsete kulude värskendamise kohta."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b9ad13071c3e0c3a294e9d4413de160a58559640
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a><span data-ttu-id="5f67f-103">Tootmiskeskkonnas standardkulude värskendamine</span><span class="sxs-lookup"><span data-stu-id="5f67f-103">Update standard costs in a manufacturing environment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5f67f-104">Selles artiklis antakse juhiseid tootmiskeskkonnas standardsete kulude värskendamise kohta.</span><span class="sxs-lookup"><span data-stu-id="5f67f-104">This article provides guidance about how to update standard costs in a manufacturing environment.</span></span> 

<span data-ttu-id="5f67f-105">Värskendused võivad kajastada uusi kaupu, kulukategooriaid või kaudse kulu kalkulatsiooni valemeid.</span><span class="sxs-lookup"><span data-stu-id="5f67f-105">Updates can reflect new items, cost categories, or indirect cost calculation formulas.</span></span> <span data-ttu-id="5f67f-106">Samuti võivad need kajastada parandusi ja kulumuutusi.</span><span class="sxs-lookup"><span data-stu-id="5f67f-106">They can also reflect corrections and cost changes.</span></span> <span data-ttu-id="5f67f-107">Värskendamise tüüp mõjutab etappe, mille peate läbima standardsete kulude värskendamiseks, ja seda illustreerivad järgmised juhtumid.</span><span class="sxs-lookup"><span data-stu-id="5f67f-107">The type of update affects the steps that you must complete to update standard costs, as illustrated in the following cases:</span></span>

-   <span data-ttu-id="5f67f-108">Sisestage ostetud kauba eeldatavad standardse kulu muutmised ja muutke seejärel asjakohasel kuupäeval kauba kulukirjete olekuks **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="5f67f-108">Enter expected standard cost changes for purchased items, and then change the status of the item cost records to **Active** on the appropriate date.</span></span> <span data-ttu-id="5f67f-109">Ärge siiski arvutage uuesti toodetavate kaupade kulusid, mille puhul kasutatakse ostetud kaupu.</span><span class="sxs-lookup"><span data-stu-id="5f67f-109">However, don't recalculate the costs of manufactured items that use the purchased items.</span></span>
-   <span data-ttu-id="5f67f-110">Sisestage standardsed kulud uue ostetud kauba jaoks, kuid ärge arvutage uuesti toodetavate kaupade kulud koosluste versiooniga, mis sisaldab komponendina uusi ostetud kaupu.</span><span class="sxs-lookup"><span data-stu-id="5f67f-110">Enter standard costs for a new purchased item, but don't recalculate the costs of manufactured items that have a bill of materials (BOM) version that contains the new purchased item as a component.</span></span>
-   <span data-ttu-id="5f67f-111">Parandage või muutke ostetud kauba kulu või muutke ostetud kaubale määratud kulugruppi ning arvutage kõigi toodetavate kaupade kulu koosluse versiooniga, mis sisaldab komponendina uut kaupa.</span><span class="sxs-lookup"><span data-stu-id="5f67f-111">Correct or change the cost of a purchased item, or change the cost group that is assigned to a purchased item, and calculate the cost for all manufactured items that have a BOM version that contains the purchased item as a component.</span></span>
-   <span data-ttu-id="5f67f-112">Muutke kulukategooria kulu ja arvutage kõigi toodetavate kaupade kulu protsessi versiooniga, mis sisaldab kulukategooriat kasutavaid protsessi operatsioone.</span><span class="sxs-lookup"><span data-stu-id="5f67f-112">Change the cost for a cost category, and calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="5f67f-113">Muutke protsessioperatsioonidele määratud kulukategooriaid või kulukategooriatele määratud kulugruppi.</span><span class="sxs-lookup"><span data-stu-id="5f67f-113">Change the cost categories that are assigned to routing operations or the cost group that is assigned to cost categories.</span></span> <span data-ttu-id="5f67f-114">Seejärel arvutage kõigi toodetavate kaupade kulu protsessi versiooniga, mis sisaldab kulukategooriat kasutavaid protsessi operatsioone.</span><span class="sxs-lookup"><span data-stu-id="5f67f-114">Then calculate the cost for all manufactured items that have a route version that contains routing operations that use the cost category.</span></span>
-   <span data-ttu-id="5f67f-115">Muutke kaudse kulu kalkulatsiooni valemit ja arvutage kõigi muudatusest mõjutatud toodetavate kaupade kulu.</span><span class="sxs-lookup"><span data-stu-id="5f67f-115">Change an indirect cost calculation formula, and calculate the cost for all manufactured items that are affected by the change.</span></span>
-   <span data-ttu-id="5f67f-116">Muutke või lisage toodetava kauba tootmiskoht ja arvutage kauba tootmiskulu selle jaoks.</span><span class="sxs-lookup"><span data-stu-id="5f67f-116">Change or add a manufacturing site for a manufactured item, and calculate the item's manufactured cost for the site.</span></span>
-   <span data-ttu-id="5f67f-117">Arvutage (või arvutage uuesti) toodetava kauba kulu ja arvutage uuesti kõigi toodetavate kaupade kulu koosluse versiooniga, mis sisaldab komponendina toodetavat kaupa.</span><span class="sxs-lookup"><span data-stu-id="5f67f-117">Calculate, or recalculate, the cost for a manufactured item, and recalculate the cost for all manufactured items that have a BOM version that contains the manufactured item as a component.</span></span>
-   <span data-ttu-id="5f67f-118">Arvutage kulud uue toodetava kauba jaoks, mis põhineb määratud, kinnitatud ja aktiivse koosluse ja protsessi teabel.</span><span class="sxs-lookup"><span data-stu-id="5f67f-118">Calculate costs for a new manufactured item, based on its defined, approved, and active BOM and route information.</span></span>

<span data-ttu-id="5f67f-119">Iga juhtum nõuab hoolikat kaalumist selle osas, kuidas standardseid kulusid värskendada.</span><span class="sxs-lookup"><span data-stu-id="5f67f-119">Each case requires careful consideration about how to update standard costs.</span></span>




