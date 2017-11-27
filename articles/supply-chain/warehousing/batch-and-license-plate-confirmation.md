---
title: Partii ja litsentsiplaadi kinnitus
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada partii ning litsentsiplaadi kinnitust mobiilselt seadmelt.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0444caa0f1cc176153c322b8619db65bd377ddd0
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="e39e1-103">Partii ja litsentsiplaadi kinnitus</span><span class="sxs-lookup"><span data-stu-id="e39e1-103">Batch and license plate confirmation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e39e1-104">Partii kinnitamine võimaldab kontrollida, kas mobiilselt seadmelt võetakse õige partii.</span><span class="sxs-lookup"><span data-stu-id="e39e1-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="e39e1-105">Algsel töö komplekteerimisel ainult eespool oleva partii kaupadest, kus eespool olev partii näitab partiivahemikke, mis on kõrgemal kui asukoht otsinguhierarhias, peate kontrollima, et komplekteeritav partii vastaks töö real olevale partiile.</span><span class="sxs-lookup"><span data-stu-id="e39e1-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="e39e1-106">Litsentsiplaadi kinnitamine võimaldab kontrollida, kas mobiilselt seadmelt võetakse õige litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="e39e1-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="e39e1-107">Töö komplekteerimisel etapi asukohast peate kontrollima, et komplekteeritav litsentsiplaat vastaks tööga seostatud litsentsiplaadile.</span><span class="sxs-lookup"><span data-stu-id="e39e1-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="e39e1-108">Kui tööd alustatakse litsentsiplaadi skannimisega, siis jäetakse see kinnitamise etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="e39e1-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="e39e1-109">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="e39e1-109">Where it applies</span></span>
<span data-ttu-id="e39e1-110">Kinnitus kehtib järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="e39e1-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="e39e1-111">Partii kinnitus kehtib töö algsel komplekteerimisel eespool oleva partii kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="e39e1-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="e39e1-112">Litsentsiplaadi kinnitus kehtib komplekteerimiste korral etapi asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="e39e1-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="e39e1-113">Partii ja litsentsiplaadi kinnituse seadistamine</span><span class="sxs-lookup"><span data-stu-id="e39e1-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="e39e1-114">Partii ja litsentsiplaadi kinnitust saab konfigureerida mobiilse seadme menüüelementidest.</span><span class="sxs-lookup"><span data-stu-id="e39e1-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="e39e1-115">Sisenege mobiilse seadme menüüelementidest töö kinnitamise seadistusse.</span><span class="sxs-lookup"><span data-stu-id="e39e1-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="e39e1-116">Valige partii või litsentsiplaadi kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="e39e1-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="e39e1-117">Mõlemad valikud on saadaval töö tüübi komplekteerimiste puhul, millel pole automaatne kinnitamine lubatud.</span><span class="sxs-lookup"><span data-stu-id="e39e1-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  

