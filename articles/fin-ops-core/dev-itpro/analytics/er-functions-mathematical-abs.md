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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041649"
---
# <span data-ttu-id="43b95-103"><a name="ABS">ER-i funktsioon ABS</a></span><span class="sxs-lookup"><span data-stu-id="43b95-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43b95-104">Funktsioon `ABS` annab määratud numbri absoluutväärtuse *tegeliku* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="43b95-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="43b95-105">Teisisõnu tagastab see arvu ilma selle märgita.</span><span class="sxs-lookup"><span data-stu-id="43b95-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="43b95-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="43b95-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="43b95-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="43b95-107">Arguments</span></span>

<span data-ttu-id="43b95-108">`number`: *tegelik*</span><span class="sxs-lookup"><span data-stu-id="43b95-108">`number`: *Real*</span></span>

<span data-ttu-id="43b95-109">Numbriline väärtus, mille absoluutväärtust soovite.</span><span class="sxs-lookup"><span data-stu-id="43b95-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="43b95-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="43b95-110">Return values</span></span>

<span data-ttu-id="43b95-111">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="43b95-111">*Real*</span></span>

<span data-ttu-id="43b95-112">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="43b95-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="43b95-113">Näide</span><span class="sxs-lookup"><span data-stu-id="43b95-113">Example</span></span>

<span data-ttu-id="43b95-114">`ABS (-1)` tagastab **1**.</span><span class="sxs-lookup"><span data-stu-id="43b95-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43b95-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="43b95-115">Additional resources</span></span>

[<span data-ttu-id="43b95-116">Matemaatilised funktsioonid</span><span class="sxs-lookup"><span data-stu-id="43b95-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
