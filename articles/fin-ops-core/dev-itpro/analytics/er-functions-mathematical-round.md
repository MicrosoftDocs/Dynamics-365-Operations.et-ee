---
title: ER-i funktsioon ROUND
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ROUND.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 716ac0bbc9fec992ec1bbfc99bfc86434bf97984
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570394"
---
# <a name="round-er-function"></a><span data-ttu-id="a951e-103">ER-i funktsioon ROUND</span><span class="sxs-lookup"><span data-stu-id="a951e-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a951e-104">Funktsioon `ROUND` tagastab määratud numbri *tõese* väärtusena pärast selle ümardamist määratud arvu komakohtadeni.</span><span class="sxs-lookup"><span data-stu-id="a951e-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="a951e-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="a951e-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="a951e-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="a951e-106">Arguments</span></span>

<span data-ttu-id="a951e-107">`number`: *tegelik*</span><span class="sxs-lookup"><span data-stu-id="a951e-107">`number`: *Real*</span></span>

<span data-ttu-id="a951e-108">Numbriline väärtus, mis tuleb ümardada.</span><span class="sxs-lookup"><span data-stu-id="a951e-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="a951e-109">`decimals`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="a951e-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="a951e-110">Arvuline väärtus, mis tähistab kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="a951e-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="a951e-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="a951e-111">Return values</span></span>

<span data-ttu-id="a951e-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="a951e-112">*Real*</span></span>

<span data-ttu-id="a951e-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="a951e-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a951e-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="a951e-114">Usage notes</span></span>

<span data-ttu-id="a951e-115">Kui argumendi `decimals` väärtus on suurem kui 0 (null), ümardatakse määratud number nii paljude komakohtadeni.</span><span class="sxs-lookup"><span data-stu-id="a951e-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="a951e-116">Kui argumendi `decimals` väärtus on **0** (null), ümardatakse määratud number lähima paarisarvuni.</span><span class="sxs-lookup"><span data-stu-id="a951e-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="a951e-117">Kui argumendi `decimals` väärtus on väiksem kui 0 (null), ümardatakse määratud number komakohast vasakule.</span><span class="sxs-lookup"><span data-stu-id="a951e-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="a951e-118">Näide 1</span><span class="sxs-lookup"><span data-stu-id="a951e-118">Example 1</span></span>

<span data-ttu-id="a951e-119">`ROUND (1200.767, 2)` ümardab kahe komakohani ja tagastab väärtuse **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="a951e-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a951e-120">Näide 2</span><span class="sxs-lookup"><span data-stu-id="a951e-120">Example 2</span></span>

<span data-ttu-id="a951e-121">`ROUND (1200.767, -3)` ümardab lähima 1000 kordseni ja tagastab väärtuse **1000**.</span><span class="sxs-lookup"><span data-stu-id="a951e-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="a951e-122">Näide 3</span><span class="sxs-lookup"><span data-stu-id="a951e-122">Example 3</span></span>

<span data-ttu-id="a951e-123">`ROUND (1200.5, 0)` ümardab lähima täisarvuni ja tagastab väärtuse **1200**, samas kui `ROUND (1201.5, 0)` teeb sama ja tagastab väärtuse **1202**.</span><span class="sxs-lookup"><span data-stu-id="a951e-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a951e-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a951e-124">Additional resources</span></span>

[<span data-ttu-id="a951e-125">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="a951e-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]