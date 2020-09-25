---
title: ER-i funktsioon AND
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni AND.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 4a246496eca0d5a8538ac7f1577957e6b9eae4e3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743466"
---
# <a name="and-er-function"></a><span data-ttu-id="a0555-103">ER-i funktsioon AND</span><span class="sxs-lookup"><span data-stu-id="a0555-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0555-104">Kui kõik määratud tingimused on tõesed, tagastab funktsioon `AND` *kahendmuutuja* väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="a0555-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="a0555-105">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="a0555-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0555-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="a0555-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="a0555-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="a0555-107">Arguments</span></span>

<span data-ttu-id="a0555-108">`condition 1`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="a0555-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="a0555-109">Kehtiv tingimuslik avaldis, mida tuleb testida.</span><span class="sxs-lookup"><span data-stu-id="a0555-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a0555-110">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="a0555-110">This argument is required.</span></span>

<span data-ttu-id="a0555-111">`condition N`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="a0555-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="a0555-112">Kehtiv tingimuslik avaldis, mida tuleb testida.</span><span class="sxs-lookup"><span data-stu-id="a0555-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a0555-113">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="a0555-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a0555-114">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="a0555-114">Return values</span></span>

<span data-ttu-id="a0555-115">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="a0555-115">*Boolean*</span></span>

<span data-ttu-id="a0555-116">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="a0555-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a0555-117">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="a0555-117">Usage notes</span></span>

<span data-ttu-id="a0555-118">Loogiliste funktsioonide argumentides saate kasutada andmeallika viiteid, numbrilisi ja teksti väärtuseid, kahendmuutuja väärtusi, võrdluse tehtemärke ja teisi elektroonilise aruandluse (ER) funktsioone.</span><span class="sxs-lookup"><span data-stu-id="a0555-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="a0555-119">Samas peavad kõik argumendid olema hinnatud *kahendmuutuja* väärtusele **TRUE** või **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a0555-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="a0555-120">Näide</span><span class="sxs-lookup"><span data-stu-id="a0555-120">Example</span></span>

<span data-ttu-id="a0555-121">`AND (1=1, "a"="a")` tagastab väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="a0555-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="a0555-122">`AND (1=2, "a"="a")` tagastab väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a0555-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0555-123">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a0555-123">Additional resources</span></span>

[<span data-ttu-id="a0555-124">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="a0555-124">Logical functions</span></span>](er-functions-category-logical.md)
