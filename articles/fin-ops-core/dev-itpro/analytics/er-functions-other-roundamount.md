---
title: ER-i funktsioon ROUNDAMOUNT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ROUNDAMOUNT.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a80587236d17160a996d701ca4ae38be21c818c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563290"
---
# <a name="roundamount-er-function"></a><span data-ttu-id="930f7-103">ER-i funktsioon ROUNDAMOUNT</span><span class="sxs-lookup"><span data-stu-id="930f7-103">ROUNDAMOUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="930f7-104">Funktsioon `ROUNDAMOUNT` tagastab määratud arvu määratud ümardamisreegli kohaselt lähima teise arvu kordseni ümardamise tulemusena *tegeliku* väärtuse.</span><span class="sxs-lookup"><span data-stu-id="930f7-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="930f7-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="930f7-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="930f7-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="930f7-106">Arguments</span></span>

<span data-ttu-id="930f7-107">`number`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="930f7-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="930f7-108">Numbriline väärtus, mis tuleb ümardada.</span><span class="sxs-lookup"><span data-stu-id="930f7-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="930f7-109">`decimals`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="930f7-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="930f7-110">Arv, mida parameetri `number` väärtus peab kordseni ümardama.</span><span class="sxs-lookup"><span data-stu-id="930f7-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="930f7-111">`round rule`: *loetelu väärtus*</span><span class="sxs-lookup"><span data-stu-id="930f7-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="930f7-112">Loetelu **RoundOffType** loendamise väärtus, mis määratleb ümardamise reegli.</span><span class="sxs-lookup"><span data-stu-id="930f7-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="930f7-113">See loendamine pakub järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="930f7-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="930f7-114">Tavaline (Ordinary)</span><span class="sxs-lookup"><span data-stu-id="930f7-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="930f7-115">Allapoole (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="930f7-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="930f7-116">Ümardamine üles (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="930f7-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="930f7-117">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="930f7-117">Return values</span></span>

<span data-ttu-id="930f7-118">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="930f7-118">*Real*</span></span>

<span data-ttu-id="930f7-119">Tulemuseks olev arvväärtus on parameetri `decimals` määratud väärtuse korrutis ja on kõige lähemal parameetri `number` määratud väärtusele.</span><span class="sxs-lookup"><span data-stu-id="930f7-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="930f7-120">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="930f7-120">Usage notes</span></span>

<span data-ttu-id="930f7-121">Kui parameeter `number` on null, tagastab funktsioon alati nulli.</span><span class="sxs-lookup"><span data-stu-id="930f7-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="930f7-122">Kui parameeter `decimals` on null, ümardab see funktsioon vaikimisi ümardamisväärtuseni.</span><span class="sxs-lookup"><span data-stu-id="930f7-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="930f7-123">Kui parameeter `round rule` on seatud suvandile **RoundOffType.Ordinary**, on ümardamise vaikeväärtus **0,01.**</span><span class="sxs-lookup"><span data-stu-id="930f7-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="930f7-124">Vastasel juhul on ümardamise vaikeväärtus **1,0**.</span><span class="sxs-lookup"><span data-stu-id="930f7-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="930f7-125">Kui parameeter `round rule` on seatud suvandile **RoundOffType.Ordinary**, ümardab see funktsioon lähima ümardatud summani.</span><span class="sxs-lookup"><span data-stu-id="930f7-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="930f7-126">Kui parameeter `round rule` on seatud suvandile **RoundOffType.RoundDown**, ümardab see funktsioon nulli suunas lähima ümardatud summani.</span><span class="sxs-lookup"><span data-stu-id="930f7-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="930f7-127">Kui parameeter `round rule` on seatud suvandile **RoundOffType.RoundUp**, ümardab see funktsioon nullist eemale lähima ümardatud summani.</span><span class="sxs-lookup"><span data-stu-id="930f7-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="930f7-128">Kui parameeter `round rule` on seatud suvandile **RoundOffType.Ordinary**, käitub see funktsioon sarnaselt Exceli funktsioonile [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) ja X++ funktsioonile [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round).</span><span class="sxs-lookup"><span data-stu-id="930f7-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="930f7-129">Märkused</span><span class="sxs-lookup"><span data-stu-id="930f7-129">Remarks</span></span>

<span data-ttu-id="930f7-130">Arvväärtuse ümardamiseks määratud arvu kümnendkohani kasutage funktsiooni [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="930f7-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="930f7-131">Näide</span><span class="sxs-lookup"><span data-stu-id="930f7-131">Example</span></span>

<span data-ttu-id="930f7-132">Kui parameeter **model.RoundOff** on seatud suvandile **RoundOffType.Ordinary**, tagastab `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` väärtuse 7,35.</span><span class="sxs-lookup"><span data-stu-id="930f7-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="930f7-133">Kui parameeter **model.RoundOff** on seatud suvandile **RoundOffType.RoundDown**, tagastab `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` väärtuse 7,35.</span><span class="sxs-lookup"><span data-stu-id="930f7-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="930f7-134">Kui parameeter **model.RoundOff** on seatud suvandile **RoundOffType.RoundUp**, tagastab `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` väärtuse 8,4.</span><span class="sxs-lookup"><span data-stu-id="930f7-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="930f7-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="930f7-135">Additional resources</span></span>

[<span data-ttu-id="930f7-136">Muud (ettevõtte domeenipõhised) funktsioonid</span><span class="sxs-lookup"><span data-stu-id="930f7-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="930f7-137">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="930f7-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]