---
title: ER-i funktsioon OR
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni OR.
author: NickSelin
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
ms.openlocfilehash: 9763cdbabfbaba1af433c1fd753b03982ecb550d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751709"
---
# <a name="or-er-function"></a><span data-ttu-id="c09b3-103">ER-i funktsioon OR</span><span class="sxs-lookup"><span data-stu-id="c09b3-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c09b3-104">Kui kõik määratud tingimused on väärad, tagastab funktsioon `OR` *kahendmuutuja* väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="c09b3-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="c09b3-105">Kui mõni määratud tingimustest on tõene, tagastab funktsioon *kahendmuutuja* väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="c09b3-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c09b3-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="c09b3-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="c09b3-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="c09b3-107">Arguments</span></span>

<span data-ttu-id="c09b3-108">`condition 1`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="c09b3-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="c09b3-109">Kehtiv tingimuslik avaldis, mida tuleb testida.</span><span class="sxs-lookup"><span data-stu-id="c09b3-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="c09b3-110">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="c09b3-110">This argument is required.</span></span>

<span data-ttu-id="c09b3-111">`condition N`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="c09b3-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="c09b3-112">Kehtiv tingimuslik avaldis, mida tuleb testida.</span><span class="sxs-lookup"><span data-stu-id="c09b3-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="c09b3-113">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="c09b3-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="c09b3-114">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="c09b3-114">Return values</span></span>

<span data-ttu-id="c09b3-115">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="c09b3-115">*Boolean*</span></span>

<span data-ttu-id="c09b3-116">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="c09b3-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="c09b3-117">Näide</span><span class="sxs-lookup"><span data-stu-id="c09b3-117">Example</span></span>

<span data-ttu-id="c09b3-118">`OR (1=2, "a"="a")` tagastab väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="c09b3-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c09b3-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c09b3-119">Additional resources</span></span>

[<span data-ttu-id="c09b3-120">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="c09b3-120">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]