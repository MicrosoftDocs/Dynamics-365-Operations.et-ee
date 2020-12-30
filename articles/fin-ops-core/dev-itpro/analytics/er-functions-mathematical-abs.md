---
title: ER-i funktsioon ABS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ABS.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c7156b9990397822a6bea9ed8b3df8f65490572
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683277"
---
# <a name="abs-er-function"></a><span data-ttu-id="93eb4-103">ER-i funktsioon ABS</span><span class="sxs-lookup"><span data-stu-id="93eb4-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93eb4-104">Funktsioon `ABS` annab määratud numbri absoluutväärtuse *tegeliku* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="93eb4-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="93eb4-105">Teisisõnu tagastab see arvu ilma selle märgita.</span><span class="sxs-lookup"><span data-stu-id="93eb4-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="93eb4-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="93eb4-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="93eb4-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="93eb4-107">Arguments</span></span>

<span data-ttu-id="93eb4-108">`number`: *tegelik*</span><span class="sxs-lookup"><span data-stu-id="93eb4-108">`number`: *Real*</span></span>

<span data-ttu-id="93eb4-109">Numbriline väärtus, mille absoluutväärtust soovite.</span><span class="sxs-lookup"><span data-stu-id="93eb4-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="93eb4-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="93eb4-110">Return values</span></span>

<span data-ttu-id="93eb4-111">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="93eb4-111">*Real*</span></span>

<span data-ttu-id="93eb4-112">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="93eb4-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="93eb4-113">Näide</span><span class="sxs-lookup"><span data-stu-id="93eb4-113">Example</span></span>

<span data-ttu-id="93eb4-114">`ABS (-1)` tagastab **1**.</span><span class="sxs-lookup"><span data-stu-id="93eb4-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="93eb4-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="93eb4-115">Additional resources</span></span>

[<span data-ttu-id="93eb4-116">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="93eb4-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
