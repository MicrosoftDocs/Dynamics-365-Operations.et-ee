---
title: Partii ja litsentsiplaadi kinnitus
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada partii ning litsentsiplaadi kinnitust mobiilselt seadmelt.
author: Mirzaab
manager: tfehr
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a953b677b1188750241772d7ae966a1dba77b92e
ms.sourcegitcommit: 9f32389715b226c11e74c53547527e0a8b51e300
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514298"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="a2e32-103">Partii ja litsentsiplaadi kinnitus</span><span class="sxs-lookup"><span data-stu-id="a2e32-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a2e32-104">Partii kinnitamine võimaldab kontrollida, kas mobiilselt seadmelt võetakse õige partii.</span><span class="sxs-lookup"><span data-stu-id="a2e32-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="a2e32-105">Algsel töö komplekteerimisel ainult eespool oleva partii kaupadest, kus eespool olev partii näitab partiivahemikke, mis on kõrgemal kui asukoht otsinguhierarhias, peate kontrollima, et komplekteeritav partii vastaks töö real olevale partiile.</span><span class="sxs-lookup"><span data-stu-id="a2e32-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span>

<span data-ttu-id="a2e32-106">Litsentsiplaadi kinnitamine võimaldab kontrollida, kas mobiilselt seadmelt võetakse õige litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="a2e32-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="a2e32-107">Töö komplekteerimisel etapi asukohast peate kontrollima, et komplekteeritav litsentsiplaat vastaks tööga seostatud litsentsiplaadile.</span><span class="sxs-lookup"><span data-stu-id="a2e32-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="a2e32-108">Kui tööd alustatakse litsentsiplaadi skannimisega, siis jäetakse see kinnitamise etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="a2e32-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="a2e32-109">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="a2e32-109">Where it applies</span></span>

<span data-ttu-id="a2e32-110">Kinnitus kehtib järgmistel juhtudel.</span><span class="sxs-lookup"><span data-stu-id="a2e32-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="a2e32-111">Partii kinnitus kehtib töö algsel komplekteerimisel eespool oleva partii kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="a2e32-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="a2e32-112">Litsentsiplaadi kinnitus kehtib komplekteerimiste korral etapi asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="a2e32-112">License plate confirmation applies to picks from stage locations.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2e32-113">Litsentsiplaadi kinnitamisel täiendamist ei toetata.</span><span class="sxs-lookup"><span data-stu-id="a2e32-113">Replenishment is not supported for license plate confirmation.</span></span> <span data-ttu-id="a2e32-114">Täiendamise töö läbiviimisel ei looda ühtegi litsentsiplaadi kinnituse etappi.</span><span class="sxs-lookup"><span data-stu-id="a2e32-114">When executing replenishment work, no license plate confirmation step is created.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="a2e32-115">Partii ja litsentsiplaadi kinnituse seadistamine</span><span class="sxs-lookup"><span data-stu-id="a2e32-115">Set up batch and license plate confirmation</span></span>

<span data-ttu-id="a2e32-116">Partii ja litsentsiplaadi kinnitust saab konfigureerida mobiilse seadme menüüelementidest.</span><span class="sxs-lookup"><span data-stu-id="a2e32-116">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>

1. <span data-ttu-id="a2e32-117">Sisenege mobiilse seadme menüüelementidest töö kinnitamise seadistusse.</span><span class="sxs-lookup"><span data-stu-id="a2e32-117">From the mobile device menu items, enter the work confirmation setup.</span></span>  
1. <span data-ttu-id="a2e32-118">Valige partii või litsentsiplaadi kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="a2e32-118">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="a2e32-119">Mõlemad valikud on saadaval töö tüübi komplekteerimiste puhul, millel pole automaatne kinnitamine lubatud.</span><span class="sxs-lookup"><span data-stu-id="a2e32-119">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  
