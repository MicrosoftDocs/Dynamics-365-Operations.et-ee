---
title: ER-i funktsioon OR
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni OR.
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
ms.openlocfilehash: 107241dbf9a5127d61343fc1cf42c3bab577adb3
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686974"
---
# <a name="or-er-function"></a><span data-ttu-id="a6bf8-103">ER-i funktsioon OR</span><span class="sxs-lookup"><span data-stu-id="a6bf8-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6bf8-104">Kui kõik määratud tingimused on väärad, tagastab funktsioon `OR` *kahendmuutuja* väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="a6bf8-105">Kui mõni määratud tingimustest on tõene, tagastab funktsioon *kahendmuutuja* väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6bf8-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="a6bf8-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="a6bf8-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="a6bf8-107">Arguments</span></span>

<span data-ttu-id="a6bf8-108">`condition 1`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="a6bf8-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="a6bf8-109">Kehtiv tingimuslik avaldis, mida tuleb testida.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a6bf8-110">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-110">This argument is required.</span></span>

<span data-ttu-id="a6bf8-111">`condition N`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="a6bf8-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="a6bf8-112">Kehtiv tingimuslik avaldis, mida tuleb testida.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="a6bf8-113">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="a6bf8-114">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="a6bf8-114">Return values</span></span>

<span data-ttu-id="a6bf8-115">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="a6bf8-115">*Boolean*</span></span>

<span data-ttu-id="a6bf8-116">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="a6bf8-117">Näide</span><span class="sxs-lookup"><span data-stu-id="a6bf8-117">Example</span></span>

<span data-ttu-id="a6bf8-118">`OR (1=2, "a"="a")` tagastab väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="a6bf8-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6bf8-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a6bf8-119">Additional resources</span></span>

[<span data-ttu-id="a6bf8-120">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="a6bf8-120">Logical functions</span></span>](er-functions-category-logical.md)
