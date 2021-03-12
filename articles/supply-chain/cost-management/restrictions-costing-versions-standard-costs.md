---
title: Standardkulude kuluversioonide piirangud
description: Selles teemas kirjeldatakse piiranguid, mis kehtivad standardkulude kuluversiooni puhul.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5339c3c4a62b94a06cbffc200ed1e9b227d6b6af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963784"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a><span data-ttu-id="6d38d-103">Standardkulude kuluversioonide piirangud</span><span class="sxs-lookup"><span data-stu-id="6d38d-103">Restrictions on costing versions for standard costs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d38d-104">Selles teemas kirjeldatakse piiranguid, mis kehtivad standardkulude kuluversiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="6d38d-104">This topic describes the restrictions that apply to a costing version for standard costs.</span></span> 

<span data-ttu-id="6d38d-105">Järgmised piirangud aitavad tagada standardkulude põhimõtetest kinnipidamist.</span><span class="sxs-lookup"><span data-stu-id="6d38d-105">The following restrictions help guarantee adherence to standard costing principles:</span></span>

-  <span data-ttu-id="6d38d-106">Kauba kulusse tuleb kaasata tasud.</span><span class="sxs-lookup"><span data-stu-id="6d38d-106">Charges must be included in an item's cost.</span></span> <span data-ttu-id="6d38d-107">Toodetud kauba tasud näitavad amortiseeritud püsikulusid koosluse ja marsruuditeabe piires.</span><span class="sxs-lookup"><span data-stu-id="6d38d-107">The charges for a manufactured item represent the amortized constant costs in the bill of materials (BOM) and route information.</span></span> <span data-ttu-id="6d38d-108">Seetõttu tuleb nad kaasata ühiku hinda.</span><span class="sxs-lookup"><span data-stu-id="6d38d-108">Therefore, the charges must be included in the unit cost.</span></span> <span data-ttu-id="6d38d-109">Ostetud kauba tasud kaasatakse ka selle kauba ühiku hinda.</span><span class="sxs-lookup"><span data-stu-id="6d38d-109">The charges for a purchased item are also included in the item's unit cost.</span></span>

-  <span data-ttu-id="6d38d-110">Toodetud kaupade standardkulude arvutamine peab põhinema standardkulude kuluversioonis olevatel kulukirjetel.</span><span class="sxs-lookup"><span data-stu-id="6d38d-110">Calculation of standard costs for manufactured items must be based on the cost records in a costing version for standard costs.</span></span> <span data-ttu-id="6d38d-111">Kuluandmete alternatiivseid allikaid saab kasutada ainult planeeritud kulude kuluversiooniga, nt ostuhinna kaubanduslepped ostetud kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="6d38d-111">Alternative sources of cost data can be used only with a costing version for planned costs, such as purchase price trade agreements for purchased items.</span></span> <span data-ttu-id="6d38d-112">Kuluandmete alternatiivsed allikad saab määratleda koosluse kalkulatsioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="6d38d-112">Alternative sources of cost data are defined by the BOM calculation group.</span></span>

-  <span data-ttu-id="6d38d-113">Koosluse kalkulatsioone tuleb teha üksiktaseme tormilise arengu režiimiga.</span><span class="sxs-lookup"><span data-stu-id="6d38d-113">BOM calculations must be performed in a single-level explosion mode.</span></span>

<span data-ttu-id="6d38d-114">Standardkulude kaubakulu andmeid saab kopeerida muusse kuluversiooni, mis sisaldab standardkulusid või planeeritud kulusid.</span><span class="sxs-lookup"><span data-stu-id="6d38d-114">The item cost data for standard costs can be copied to another costing version that contains standard costs or planned costs.</span></span> <span data-ttu-id="6d38d-115">Planeeritud kulude kaubakuluandmeid ei saa siiski kopeerida standardkulusid sisaldavasse kuluversiooni, sest varem selles teemas loetletud piiranguid ei kohaldata planeeritud kuludele.</span><span class="sxs-lookup"><span data-stu-id="6d38d-115">However, the item cost data for planned costs can't be copied to a cost version that contains standard costs, because the restrictions that are listed earlier in this topic don't apply to planned costs.</span></span>

<a name="related-topics"></a><span data-ttu-id="6d38d-116">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="6d38d-116">Related topics</span></span>
--------

[<span data-ttu-id="6d38d-117">Kuluarvutusversioonide ülevaade</span><span class="sxs-lookup"><span data-stu-id="6d38d-117">Costing versions overview</span></span>](costing-versions.md)

[<span data-ttu-id="6d38d-118">Mittetootmiskeskkonnas standardomahindade värskendamine</span><span class="sxs-lookup"><span data-stu-id="6d38d-118">Update standard costs in a non-manufacturing environment</span></span>](update-standard-costs-non-manufacturing-environment.md)

[<span data-ttu-id="6d38d-119">Toodetud kaupade standardkulude säilitamise ettevalmistus</span><span class="sxs-lookup"><span data-stu-id="6d38d-119">Prepare to maintain standard costs for manufactured items</span></span>](update-standard-costs-manufacturing-environment.md)

