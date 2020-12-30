---
title: ER-i funktsioon INT64VALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni INT64VALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: bb750116312df82448f5a0048e380f9e5274f8e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686046"
---
# <a name="int64value-er-function"></a><span data-ttu-id="69e2c-103">ER-i funktsioon INT64VALUE</span><span class="sxs-lookup"><span data-stu-id="69e2c-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="69e2c-104">Funktsioon `INT64VALUE` tagastab väärtuse *Int64*, mis tähistab määratud stringi.</span><span class="sxs-lookup"><span data-stu-id="69e2c-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="69e2c-105">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="69e2c-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="69e2c-106">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="69e2c-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="69e2c-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="69e2c-107">Arguments</span></span>

<span data-ttu-id="69e2c-108">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="69e2c-108">`text`: *String*</span></span>

<span data-ttu-id="69e2c-109">Teksti väärtus, mis tuleb teisendada numbriks *Int64*.</span><span class="sxs-lookup"><span data-stu-id="69e2c-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="69e2c-110">`number`: *tegelik* või *täisarv*</span><span class="sxs-lookup"><span data-stu-id="69e2c-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="69e2c-111">Numbriline *tegelik* või *täisarvuline* väärtus, mis tuleb teisendada numbriks *Int64*.</span><span class="sxs-lookup"><span data-stu-id="69e2c-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="69e2c-112">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="69e2c-112">Return values</span></span>

<span data-ttu-id="69e2c-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="69e2c-113">*Int64*</span></span>

<span data-ttu-id="69e2c-114">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="69e2c-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="69e2c-115">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="69e2c-115">Usage notes</span></span>

<span data-ttu-id="69e2c-116">Kümnendkohad kärbitakse.</span><span class="sxs-lookup"><span data-stu-id="69e2c-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="69e2c-117">Näide 1</span><span class="sxs-lookup"><span data-stu-id="69e2c-117">Example 1</span></span>

<span data-ttu-id="69e2c-118">`INT64VALUE ("22565422744")` tagastab *Int64* väärtuse **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="69e2c-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="69e2c-119">Näide 2</span><span class="sxs-lookup"><span data-stu-id="69e2c-119">Example 2</span></span>

<span data-ttu-id="69e2c-120">`INT64VALUE ( VALUE("22565422744.77"))` tagastab *Int64* väärtuse **22565422744**.</span><span class="sxs-lookup"><span data-stu-id="69e2c-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69e2c-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="69e2c-121">Additional resources</span></span>

[<span data-ttu-id="69e2c-122">Tüübiteisenduse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="69e2c-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
