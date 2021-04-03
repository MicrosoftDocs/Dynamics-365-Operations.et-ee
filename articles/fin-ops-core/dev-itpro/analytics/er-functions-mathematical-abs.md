---
title: ER-i funktsioon ABS
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ABS.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 12165174806395b3c36a1dbb227ed7a86def77b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565780"
---
# <a name="abs-er-function"></a><span data-ttu-id="81121-103">ER-i funktsioon ABS</span><span class="sxs-lookup"><span data-stu-id="81121-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81121-104">Funktsioon `ABS` annab määratud numbri absoluutväärtuse *tegeliku* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="81121-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="81121-105">Teisisõnu tagastab see arvu ilma selle märgita.</span><span class="sxs-lookup"><span data-stu-id="81121-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="81121-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="81121-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="81121-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="81121-107">Arguments</span></span>

<span data-ttu-id="81121-108">`number`: *tegelik*</span><span class="sxs-lookup"><span data-stu-id="81121-108">`number`: *Real*</span></span>

<span data-ttu-id="81121-109">Numbriline väärtus, mille absoluutväärtust soovite.</span><span class="sxs-lookup"><span data-stu-id="81121-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="81121-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="81121-110">Return values</span></span>

<span data-ttu-id="81121-111">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="81121-111">*Real*</span></span>

<span data-ttu-id="81121-112">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="81121-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="81121-113">Näide</span><span class="sxs-lookup"><span data-stu-id="81121-113">Example</span></span>

<span data-ttu-id="81121-114">`ABS (-1)` tagastab **1**.</span><span class="sxs-lookup"><span data-stu-id="81121-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81121-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="81121-115">Additional resources</span></span>

[<span data-ttu-id="81121-116">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="81121-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]