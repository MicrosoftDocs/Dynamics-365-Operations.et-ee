---
title: ER-i funktsioon POWER
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni POWER.
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
ms.openlocfilehash: cb768b400e3ddb99e7c8b05905d7a2dd9e4392de
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915897"
---
# <span data-ttu-id="1e970-103"><a name="POWER">ER-i funktsioon POWER</a></span><span class="sxs-lookup"><span data-stu-id="1e970-103"><a name="POWER">POWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e970-104">Funktsioon `POWER` tagastab *tegeliku* väärtuse, mis kajastab määratud astmele määratud positiivse numbri tõstmise tulemi.</span><span class="sxs-lookup"><span data-stu-id="1e970-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e970-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="1e970-105">Syntax</span></span>

```
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="1e970-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="1e970-106">Arguments</span></span>

<span data-ttu-id="1e970-107">`number`: *tegelik* või *täisarv*</span><span class="sxs-lookup"><span data-stu-id="1e970-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="1e970-108">Numbriline väärtus, mis tuleb tõsta määratud määratud astmele.</span><span class="sxs-lookup"><span data-stu-id="1e970-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="1e970-109">`power`: *tegelik* või *täisarv*</span><span class="sxs-lookup"><span data-stu-id="1e970-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="1e970-110">Arvuline väärtus, mis tähistab määratud astet.</span><span class="sxs-lookup"><span data-stu-id="1e970-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="1e970-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="1e970-111">Return values</span></span>

<span data-ttu-id="1e970-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="1e970-112">*Real*</span></span>

<span data-ttu-id="1e970-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="1e970-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="1e970-114">Näide 1</span><span class="sxs-lookup"><span data-stu-id="1e970-114">Example 1</span></span>

<span data-ttu-id="1e970-115">`POWER (10, 2)` tagastab **100**.</span><span class="sxs-lookup"><span data-stu-id="1e970-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1e970-116">Näide 2</span><span class="sxs-lookup"><span data-stu-id="1e970-116">Example 2</span></span>

<span data-ttu-id="1e970-117">`POWER (4, 0.5)` tagastab **2**.</span><span class="sxs-lookup"><span data-stu-id="1e970-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e970-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1e970-118">Additional resources</span></span>

[<span data-ttu-id="1e970-119">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="1e970-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
