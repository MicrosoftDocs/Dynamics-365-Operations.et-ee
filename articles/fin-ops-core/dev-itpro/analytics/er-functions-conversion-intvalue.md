---
title: ER-i funktsioon INTVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni INTVALUE.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c3e4c8bd918fa1154d2c111970d2f6d0e90e08
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743635"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="97169-103">ER-i funktsioon INTVALUE</span><span class="sxs-lookup"><span data-stu-id="97169-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="97169-104">Funktsioon `INTVALUE` tagastab väärtuse *Int*, mis tähistab määratud stringi.</span><span class="sxs-lookup"><span data-stu-id="97169-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="97169-105">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="97169-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="97169-106">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="97169-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="97169-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="97169-107">Arguments</span></span>

<span data-ttu-id="97169-108">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="97169-108">`text`: *String*</span></span>

<span data-ttu-id="97169-109">Teksti väärtus, mis tuleb teisendada numbriks *Int*.</span><span class="sxs-lookup"><span data-stu-id="97169-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="97169-110">`number`: *tegelik* või *täisarv*</span><span class="sxs-lookup"><span data-stu-id="97169-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="97169-111">Numbriline *tegelik* või *täisarvuline* väärtus, mis tuleb teisendada numbriks *Int*.</span><span class="sxs-lookup"><span data-stu-id="97169-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="97169-112">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="97169-112">Return values</span></span>

<span data-ttu-id="97169-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="97169-113">*Int*</span></span>

<span data-ttu-id="97169-114">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="97169-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="97169-115">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="97169-115">Usage notes</span></span>

<span data-ttu-id="97169-116">Kümnendkohad kärbitakse.</span><span class="sxs-lookup"><span data-stu-id="97169-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="97169-117">Näide 1</span><span class="sxs-lookup"><span data-stu-id="97169-117">Example 1</span></span>

<span data-ttu-id="97169-118">`INTVALUE ("100.77")` tagastab *Int* väärtuse **100**.</span><span class="sxs-lookup"><span data-stu-id="97169-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="97169-119">Näide 2</span><span class="sxs-lookup"><span data-stu-id="97169-119">Example 2</span></span>

<span data-ttu-id="97169-120">`INTVALUE (-100.77)` tagastab *Int* väärtuse **–100**.</span><span class="sxs-lookup"><span data-stu-id="97169-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97169-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="97169-121">Additional resources</span></span>

[<span data-ttu-id="97169-122">Tüübiteisenduse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="97169-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
