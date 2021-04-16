---
title: ER-i funktsioon VALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni VALUE.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752576"
---
# <a name="value-er-function"></a><span data-ttu-id="18050-103">ER-i funktsioon VALUE</span><span class="sxs-lookup"><span data-stu-id="18050-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18050-104">Funktsioon `VALUE` tagastab *tegeliku* väärtuse, mis konverteeritakse määratud stringist.</span><span class="sxs-lookup"><span data-stu-id="18050-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="18050-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="18050-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="18050-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="18050-106">Arguments</span></span>

<span data-ttu-id="18050-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="18050-107">`text`: *String*</span></span>

<span data-ttu-id="18050-108">Stringi väärtus, mis tuleb teisendada numbriliseks väärtuseks.</span><span class="sxs-lookup"><span data-stu-id="18050-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="18050-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="18050-109">Return values</span></span>

<span data-ttu-id="18050-110">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="18050-110">*Real*</span></span>

<span data-ttu-id="18050-111">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="18050-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="18050-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="18050-112">Usage notes</span></span>

<span data-ttu-id="18050-113">Komasid ja punkte (.), loetakse komakohtade eraldajateks ning miinusmärki (–) kasutatakse negatiivse märgina.</span><span class="sxs-lookup"><span data-stu-id="18050-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="18050-114">Käitusajal esitatakse erand, kui määratud stringis on muid mittenumbrilisi märke.</span><span class="sxs-lookup"><span data-stu-id="18050-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="18050-115">Näide 1</span><span class="sxs-lookup"><span data-stu-id="18050-115">Example 1</span></span>

<span data-ttu-id="18050-116">`VALUE ("1 234,56")` annab erandi.</span><span class="sxs-lookup"><span data-stu-id="18050-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="18050-117">Näide 2</span><span class="sxs-lookup"><span data-stu-id="18050-117">Example 2</span></span>

<span data-ttu-id="18050-118">`VALUE ("1234,56")` tagastab **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="18050-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18050-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="18050-119">Additional resources</span></span>

[<span data-ttu-id="18050-120">Tüübiteisenduse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="18050-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]