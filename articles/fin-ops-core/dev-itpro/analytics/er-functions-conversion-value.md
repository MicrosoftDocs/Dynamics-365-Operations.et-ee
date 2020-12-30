---
title: ER-i funktsioon VALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni VALUE.
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
ms.openlocfilehash: 56b32a802674725347ab496d3a09b99c8f04446d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681204"
---
# <a name="value-er-function"></a><span data-ttu-id="1c2fc-103">ER-i funktsioon VALUE</span><span class="sxs-lookup"><span data-stu-id="1c2fc-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c2fc-104">Funktsioon `VALUE` tagastab *tegeliku* väärtuse, mis konverteeritakse määratud stringist.</span><span class="sxs-lookup"><span data-stu-id="1c2fc-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2fc-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="1c2fc-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="1c2fc-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="1c2fc-106">Arguments</span></span>

<span data-ttu-id="1c2fc-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="1c2fc-107">`text`: *String*</span></span>

<span data-ttu-id="1c2fc-108">Stringi väärtus, mis tuleb teisendada numbriliseks väärtuseks.</span><span class="sxs-lookup"><span data-stu-id="1c2fc-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="1c2fc-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="1c2fc-109">Return values</span></span>

<span data-ttu-id="1c2fc-110">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="1c2fc-110">*Real*</span></span>

<span data-ttu-id="1c2fc-111">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="1c2fc-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1c2fc-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="1c2fc-112">Usage notes</span></span>

<span data-ttu-id="1c2fc-113">Komasid ja punkte (.), loetakse komakohtade eraldajateks ning miinusmärki (–) kasutatakse negatiivse märgina.</span><span class="sxs-lookup"><span data-stu-id="1c2fc-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="1c2fc-114">Käitusajal esitatakse erand, kui määratud stringis on muid mittenumbrilisi märke.</span><span class="sxs-lookup"><span data-stu-id="1c2fc-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="1c2fc-115">Näide 1</span><span class="sxs-lookup"><span data-stu-id="1c2fc-115">Example 1</span></span>

<span data-ttu-id="1c2fc-116">`VALUE ("1 234,56")` annab erandi.</span><span class="sxs-lookup"><span data-stu-id="1c2fc-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="1c2fc-117">Näide 2</span><span class="sxs-lookup"><span data-stu-id="1c2fc-117">Example 2</span></span>

<span data-ttu-id="1c2fc-118">`VALUE ("1234,56")` tagastab **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="1c2fc-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c2fc-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1c2fc-119">Additional resources</span></span>

[<span data-ttu-id="1c2fc-120">Tüübiteisenduse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="1c2fc-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
