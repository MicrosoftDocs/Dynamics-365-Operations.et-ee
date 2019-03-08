---
title: Partii ja litsentsiplaadi kinnitus
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada partii ning litsentsiplaadi kinnitust mobiilselt seadmelt.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efab5b11782fd2344fb5f532272007d187c1465b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "344221"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="a2523-103">Partii ja litsentsiplaadi kinnitus</span><span class="sxs-lookup"><span data-stu-id="a2523-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2523-104">Partii kinnitamine võimaldab kontrollida, kas mobiilselt seadmelt võetakse õige partii.</span><span class="sxs-lookup"><span data-stu-id="a2523-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="a2523-105">Algsel töö komplekteerimisel ainult eespool oleva partii kaupadest, kus eespool olev partii näitab partiivahemikke, mis on kõrgemal kui asukoht otsinguhierarhias, peate kontrollima, et komplekteeritav partii vastaks töö real olevale partiile.</span><span class="sxs-lookup"><span data-stu-id="a2523-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="a2523-106">Litsentsiplaadi kinnitamine võimaldab kontrollida, kas mobiilselt seadmelt võetakse õige litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="a2523-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="a2523-107">Töö komplekteerimisel etapi asukohast peate kontrollima, et komplekteeritav litsentsiplaat vastaks tööga seostatud litsentsiplaadile.</span><span class="sxs-lookup"><span data-stu-id="a2523-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="a2523-108">Kui tööd alustatakse litsentsiplaadi skannimisega, siis jäetakse see kinnitamise etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="a2523-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="a2523-109">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="a2523-109">Where it applies</span></span>
<span data-ttu-id="a2523-110">Kinnitus kehtib järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="a2523-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="a2523-111">Partii kinnitus kehtib töö algsel komplekteerimisel eespool oleva partii kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="a2523-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="a2523-112">Litsentsiplaadi kinnitus kehtib komplekteerimiste korral etapi asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="a2523-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="a2523-113">Partii ja litsentsiplaadi kinnituse seadistamine</span><span class="sxs-lookup"><span data-stu-id="a2523-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="a2523-114">Partii ja litsentsiplaadi kinnitust saab konfigureerida mobiilse seadme menüüelementidest.</span><span class="sxs-lookup"><span data-stu-id="a2523-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="a2523-115">Sisenege mobiilse seadme menüüelementidest töö kinnitamise seadistusse.</span><span class="sxs-lookup"><span data-stu-id="a2523-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="a2523-116">Valige partii või litsentsiplaadi kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="a2523-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="a2523-117">Mõlemad valikud on saadaval töö tüübi komplekteerimiste puhul, millel pole automaatne kinnitamine lubatud.</span><span class="sxs-lookup"><span data-stu-id="a2523-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  
