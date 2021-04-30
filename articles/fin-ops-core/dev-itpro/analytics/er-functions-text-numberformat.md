---
title: ER-i funktsioon NUMBERFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NUMBERFORMAT.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890379"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="8d083-103">ER-i funktsioon NUMBERFORMAT</span><span class="sxs-lookup"><span data-stu-id="8d083-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d083-104">Funktsioon `NUMBERFORMAT` tagastab *stringi* väärtuse, mis esitab määratud numbri määratud vormingus ja valikuliselt määratletud [kultuuris](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="8d083-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="8d083-105">Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](/dotnet/standard/base-types/standard-numeric-format-strings) ja [kohandatud](/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="8d083-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-numeric-format-strings) and [custom](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="8d083-106">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="8d083-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="8d083-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="8d083-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="8d083-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="8d083-108">Arguments</span></span>

<span data-ttu-id="8d083-109">`number`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="8d083-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="8d083-110">Numbriline väärtus, mis määrab arvu, mis tuleb välja vormindada.</span><span class="sxs-lookup"><span data-stu-id="8d083-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="8d083-111">`format`: *string*</span><span class="sxs-lookup"><span data-stu-id="8d083-111">`format` : *String*</span></span>

<span data-ttu-id="8d083-112">*Stringi* väärtus, mis tähistab vormingut.</span><span class="sxs-lookup"><span data-stu-id="8d083-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="8d083-113">`culture`: *string*</span><span class="sxs-lookup"><span data-stu-id="8d083-113">`culture`: *String*</span></span>

<span data-ttu-id="8d083-114">*Stringi* väärtus, mis tähistab vormindamiseks kasutatavat kultuuri.</span><span class="sxs-lookup"><span data-stu-id="8d083-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d083-115">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="8d083-115">Return values</span></span>

<span data-ttu-id="8d083-116">*String*</span><span class="sxs-lookup"><span data-stu-id="8d083-116">*String*</span></span>

<span data-ttu-id="8d083-117">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="8d083-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8d083-118">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="8d083-118">Usage notes</span></span>

<span data-ttu-id="8d083-119">Kui kultuuri ei määratleta kutsutava funktsiooni argumendina, määratleb kontekst, mida selle funktsiooni käitamiseks kasutatakse, numbrite vormindamiseks kasutatava kultuuri.</span><span class="sxs-lookup"><span data-stu-id="8d083-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="8d083-120">Näide 1</span><span class="sxs-lookup"><span data-stu-id="8d083-120">Example 1</span></span>

<span data-ttu-id="8d083-121">Kultuuris **EN-US** `NUMBERFORMAT (0.45, "p")` tagastab **„45.00 %”** ja `NUMBERFORMAT (10.45, "#")` tagastab **„10”**.</span><span class="sxs-lookup"><span data-stu-id="8d083-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="8d083-122">Näide 2</span><span class="sxs-lookup"><span data-stu-id="8d083-122">Example 2</span></span>

<span data-ttu-id="8d083-123">`NUMBERFORMAT (10/3, "F2", "de")` tagastab **3,33**, samas kui `NUMBERFORMAT (10/3, "F2", "en-us")` tagastab **3.33**.</span><span class="sxs-lookup"><span data-stu-id="8d083-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d083-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8d083-124">Additional resources</span></span>

[<span data-ttu-id="8d083-125">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="8d083-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]