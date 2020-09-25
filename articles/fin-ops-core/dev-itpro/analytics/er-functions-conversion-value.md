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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecbffb7e39d7f2f2bccdfe32d593512a65da163c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745509"
---
# <a name="value-er-function"></a><span data-ttu-id="67586-103">ER-i funktsioon VALUE</span><span class="sxs-lookup"><span data-stu-id="67586-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="67586-104">Funktsioon `VALUE` tagastab *tegeliku* väärtuse, mis konverteeritakse määratud stringist.</span><span class="sxs-lookup"><span data-stu-id="67586-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="67586-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="67586-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="67586-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="67586-106">Arguments</span></span>

<span data-ttu-id="67586-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="67586-107">`text`: *String*</span></span>

<span data-ttu-id="67586-108">Stringi väärtus, mis tuleb teisendada numbriliseks väärtuseks.</span><span class="sxs-lookup"><span data-stu-id="67586-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="67586-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="67586-109">Return values</span></span>

<span data-ttu-id="67586-110">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="67586-110">*Real*</span></span>

<span data-ttu-id="67586-111">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="67586-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="67586-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="67586-112">Usage notes</span></span>

<span data-ttu-id="67586-113">Komasid ja punkte (.), loetakse komakohtade eraldajateks ning miinusmärki (–) kasutatakse negatiivse märgina.</span><span class="sxs-lookup"><span data-stu-id="67586-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="67586-114">Käitusajal esitatakse erand, kui määratud stringis on muid mittenumbrilisi märke.</span><span class="sxs-lookup"><span data-stu-id="67586-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="67586-115">Näide 1</span><span class="sxs-lookup"><span data-stu-id="67586-115">Example 1</span></span>

<span data-ttu-id="67586-116">`VALUE ("1 234,56")` annab erandi.</span><span class="sxs-lookup"><span data-stu-id="67586-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="67586-117">Näide 2</span><span class="sxs-lookup"><span data-stu-id="67586-117">Example 2</span></span>

<span data-ttu-id="67586-118">`VALUE ("1234,56")` tagastab **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="67586-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67586-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="67586-119">Additional resources</span></span>

[<span data-ttu-id="67586-120">Tüübiteisenduse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="67586-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
