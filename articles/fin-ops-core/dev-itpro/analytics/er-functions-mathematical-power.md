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
ms.openlocfilehash: 080b2f9b1ada55209c9470386aceab2d3ef456af
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744571"
---
# <a name="power-er-function"></a><span data-ttu-id="6f759-103">ER-i funktsioon POWER</span><span class="sxs-lookup"><span data-stu-id="6f759-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f759-104">Funktsioon `POWER` tagastab *tegeliku* väärtuse, mis kajastab määratud astmele määratud positiivse numbri tõstmise tulemi.</span><span class="sxs-lookup"><span data-stu-id="6f759-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f759-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6f759-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="6f759-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="6f759-106">Arguments</span></span>

<span data-ttu-id="6f759-107">`number`: *tegelik* või *täisarv*</span><span class="sxs-lookup"><span data-stu-id="6f759-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="6f759-108">Numbriline väärtus, mis tuleb tõsta määratud määratud astmele.</span><span class="sxs-lookup"><span data-stu-id="6f759-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="6f759-109">`power`: *tegelik* või *täisarv*</span><span class="sxs-lookup"><span data-stu-id="6f759-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="6f759-110">Arvuline väärtus, mis tähistab määratud astet.</span><span class="sxs-lookup"><span data-stu-id="6f759-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="6f759-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="6f759-111">Return values</span></span>

<span data-ttu-id="6f759-112">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="6f759-112">*Real*</span></span>

<span data-ttu-id="6f759-113">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="6f759-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="6f759-114">Näide 1</span><span class="sxs-lookup"><span data-stu-id="6f759-114">Example 1</span></span>

<span data-ttu-id="6f759-115">`POWER (10, 2)` tagastab **100**.</span><span class="sxs-lookup"><span data-stu-id="6f759-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6f759-116">Näide 2</span><span class="sxs-lookup"><span data-stu-id="6f759-116">Example 2</span></span>

<span data-ttu-id="6f759-117">`POWER (4, 0.5)` tagastab **2**.</span><span class="sxs-lookup"><span data-stu-id="6f759-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f759-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6f759-118">Additional resources</span></span>

[<span data-ttu-id="6f759-119">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6f759-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
