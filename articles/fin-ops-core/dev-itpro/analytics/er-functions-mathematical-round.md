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
ms.openlocfilehash: 12af71a024a76fca98fc2e876da9b59e5762cf07
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744547"
---
# <a name="round-er-function"></a><span data-ttu-id="aa90a-103">ER-i funktsioon ROUND</span><span class="sxs-lookup"><span data-stu-id="aa90a-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa90a-104">Funktsioon `ROUND` tagastab määratud numbri *tõese* väärtusena pärast selle ümardamist määratud arvu komakohtadeni.</span><span class="sxs-lookup"><span data-stu-id="aa90a-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa90a-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="aa90a-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="aa90a-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="aa90a-106">Arguments</span></span>

<span data-ttu-id="aa90a-107">`number`: *tegelik*</span><span class="sxs-lookup"><span data-stu-id="aa90a-107">`number`: *Real*</span></span>

<span data-ttu-id="aa90a-108">Numbriline väärtus, mis tuleb ümardada.</span><span class="sxs-lookup"><span data-stu-id="aa90a-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="aa90a-109">`decimals`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="aa90a-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="aa90a-110">Arvuline väärtus, mis tähistab kümnendkohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="aa90a-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="aa90a-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="aa90a-111">Return values</span></span>

<span data-ttu-id="aa90a-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="aa90a-112">*Real*</span></span>

<span data-ttu-id="aa90a-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="aa90a-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="aa90a-114">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="aa90a-114">Usage notes</span></span>

<span data-ttu-id="aa90a-115">Kui argumendi `decimals` väärtus on suurem kui 0 (null), ümardatakse määratud number nii paljude komakohtadeni.</span><span class="sxs-lookup"><span data-stu-id="aa90a-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="aa90a-116">Kui argumendi `decimals` väärtus on **0** (null), ümardatakse määratud number lähima täisarvuni.</span><span class="sxs-lookup"><span data-stu-id="aa90a-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="aa90a-117">Kui argumendi `decimals` väärtus on väiksem kui 0 (null), ümardatakse määratud number komakohast vasakule.</span><span class="sxs-lookup"><span data-stu-id="aa90a-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="aa90a-118">Näide 1</span><span class="sxs-lookup"><span data-stu-id="aa90a-118">Example 1</span></span>

<span data-ttu-id="aa90a-119">`ROUND (1200.767, 2)` ümardab kahe komakohani ja tagastab väärtuse **1200,77**.</span><span class="sxs-lookup"><span data-stu-id="aa90a-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="aa90a-120">Näide 2</span><span class="sxs-lookup"><span data-stu-id="aa90a-120">Example 2</span></span>

<span data-ttu-id="aa90a-121">`ROUND (1200.767, -3)` ümardab lähima 1000 kordseni ja tagastab väärtuse **1000**.</span><span class="sxs-lookup"><span data-stu-id="aa90a-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa90a-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="aa90a-122">Additional resources</span></span>

[<span data-ttu-id="aa90a-123">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="aa90a-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
