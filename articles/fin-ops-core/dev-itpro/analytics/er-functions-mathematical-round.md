---
title: ER-i funktsioon ROUND
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ROUND.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041603"
---
# <span data-ttu-id="6fe8b-103"><a name="ROUND">ER-i funktsioon ROUND</a></span><span class="sxs-lookup"><span data-stu-id="6fe8b-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fe8b-104">Funktsioon `ROUND` tagastab määratud numbri *tõese* väärtusena pärast selle ümardamist määratud arvu komakohtadeni.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fe8b-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6fe8b-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="6fe8b-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="6fe8b-106">Arguments</span></span>

<span data-ttu-id="6fe8b-107">`number`: *tegelik*</span><span class="sxs-lookup"><span data-stu-id="6fe8b-107">`number`: *Real*</span></span>

<span data-ttu-id="6fe8b-108">Numbriline väärtus, mis tuleb ümardada.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="6fe8b-109">`decimals`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="6fe8b-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="6fe8b-110">Arvuline väärtus, mis tähistab kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="6fe8b-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="6fe8b-111">Return values</span></span>

<span data-ttu-id="6fe8b-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="6fe8b-112">*Real*</span></span>

<span data-ttu-id="6fe8b-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6fe8b-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="6fe8b-114">Usage notes</span></span>

<span data-ttu-id="6fe8b-115">Kui argumendi `decimals` väärtus on suurem kui 0 (null), ümardatakse määratud number nii paljude komakohtadeni.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="6fe8b-116">Kui argumendi `decimals` väärtus on **0** (null), ümardatakse määratud number lähima täisarvuni.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="6fe8b-117">Kui argumendi `decimals` väärtus on väiksem kui 0 (null), ümardatakse määratud number komakohast vasakule.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="6fe8b-118">Näide 1</span><span class="sxs-lookup"><span data-stu-id="6fe8b-118">Example 1</span></span>

<span data-ttu-id="6fe8b-119">`ROUND (1200.767, 2)` ümardab kahe komakohani ja tagastab väärtuse **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6fe8b-120">Näide 2</span><span class="sxs-lookup"><span data-stu-id="6fe8b-120">Example 2</span></span>

<span data-ttu-id="6fe8b-121">`ROUND (1200.767, -3)` ümardab lähima 1000 kordseni ja tagastab väärtuse **1000**.</span><span class="sxs-lookup"><span data-stu-id="6fe8b-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6fe8b-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6fe8b-122">Additional resources</span></span>

[<span data-ttu-id="6fe8b-123">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6fe8b-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
