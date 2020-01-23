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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917116"
---
# <span data-ttu-id="74a7e-103"><a name="OR">ER-i funktsioon OR</a></span><span class="sxs-lookup"><span data-stu-id="74a7e-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74a7e-104">Kui kõik määratud tingimused on väärad, tagastab funktsioon `OR` *kahendmuutuja* väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="74a7e-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="74a7e-105">Kui mõni määratud tingimustest on tõene, tagastab funktsioon *kahendmuutuja* väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="74a7e-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="74a7e-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="74a7e-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="74a7e-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="74a7e-107">Arguments</span></span>

<span data-ttu-id="74a7e-108">`condition 1`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="74a7e-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="74a7e-109">Kehtiv tingimuslik avaldis, mida tuleb testida.</span><span class="sxs-lookup"><span data-stu-id="74a7e-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="74a7e-110">See argument on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="74a7e-110">This argument is required.</span></span>

<span data-ttu-id="74a7e-111">`condition N`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="74a7e-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="74a7e-112">Kehtiv tingimuslik avaldis, mida tuleb testida.</span><span class="sxs-lookup"><span data-stu-id="74a7e-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="74a7e-113">Need täiendavad argumendid on valikulised.</span><span class="sxs-lookup"><span data-stu-id="74a7e-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="74a7e-114">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="74a7e-114">Return values</span></span>

<span data-ttu-id="74a7e-115">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="74a7e-115">*Boolean*</span></span>

<span data-ttu-id="74a7e-116">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="74a7e-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="74a7e-117">Näide</span><span class="sxs-lookup"><span data-stu-id="74a7e-117">Example</span></span>

<span data-ttu-id="74a7e-118">`OR (1=2, "a"="a")` tagastab väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="74a7e-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74a7e-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="74a7e-119">Additional resources</span></span>

[<span data-ttu-id="74a7e-120">Loogilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="74a7e-120">Logical functions</span></span>](er-functions-category-logical.md)