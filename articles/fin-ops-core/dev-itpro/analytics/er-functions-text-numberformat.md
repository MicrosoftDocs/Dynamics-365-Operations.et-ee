---
title: ER-i funktsioon NUMBERFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NUMBERFORMAT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 392135abaf7db05d5ac591ab56312a0e0f6ae5ff
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916794"
---
# <span data-ttu-id="d13b4-103"><a name="NUMBERFORMAT">ER-i funktsioon NUMBERFORMAT</a></span><span class="sxs-lookup"><span data-stu-id="d13b4-103"><a name="NUMBERFORMAT">NUMBERFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d13b4-104">Funktsioon `NUMBERFORMAT` tagastab *stringi* väärtuse, mis esitab määratud numbri määratud vormingus ja valikuliselt määratletud [kultuuris](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="d13b4-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="d13b4-105">Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="d13b4-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d13b4-106">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="d13b4-106">Syntax 1</span></span>

```
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d13b4-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="d13b4-107">Syntax 2</span></span>

```
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d13b4-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="d13b4-108">Arguments</span></span>

<span data-ttu-id="d13b4-109">`number`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="d13b4-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="d13b4-110">Numbriline väärtus, mis määrab arvu, mis tuleb välja vormindada.</span><span class="sxs-lookup"><span data-stu-id="d13b4-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="d13b4-111">`format`: *string*</span><span class="sxs-lookup"><span data-stu-id="d13b4-111">`format` : *String*</span></span>

<span data-ttu-id="d13b4-112">*Stringi* väärtus, mis tähistab vormingut.</span><span class="sxs-lookup"><span data-stu-id="d13b4-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="d13b4-113">`culture`: *string*</span><span class="sxs-lookup"><span data-stu-id="d13b4-113">`culture`: *String*</span></span>

<span data-ttu-id="d13b4-114">*Stringi* väärtus, mis tähistab vormindamiseks kasutatavat kultuuri.</span><span class="sxs-lookup"><span data-stu-id="d13b4-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="d13b4-115">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="d13b4-115">Return values</span></span>

<span data-ttu-id="d13b4-116">*String*</span><span class="sxs-lookup"><span data-stu-id="d13b4-116">*String*</span></span>

<span data-ttu-id="d13b4-117">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="d13b4-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d13b4-118">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="d13b4-118">Usage notes</span></span>

<span data-ttu-id="d13b4-119">Kui kultuuri ei määratleta kutsutava funktsiooni argumendina, määratleb kontekst, mida selle funktsiooni käitamiseks kasutatakse, numbrite vormindamiseks kasutatava kultuuri.</span><span class="sxs-lookup"><span data-stu-id="d13b4-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="d13b4-120">Näide 1</span><span class="sxs-lookup"><span data-stu-id="d13b4-120">Example 1</span></span>

<span data-ttu-id="d13b4-121">Kultuuris **EN-US** `NUMBERFORMAT (0.45, "p")` tagastab **„45.00 %”** ja `NUMBERFORMAT (10.45, "#")` tagastab **„10”**.</span><span class="sxs-lookup"><span data-stu-id="d13b4-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d13b4-122">Näide 2</span><span class="sxs-lookup"><span data-stu-id="d13b4-122">Example 2</span></span>

<span data-ttu-id="d13b4-123">`NUMBERFORMAT (10/3, "F2", "de")` tagastab **3,33**, samas kui `NUMBERFORMAT (10/3, "F2", "en-us")` tagastab **3.33**.</span><span class="sxs-lookup"><span data-stu-id="d13b4-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d13b4-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d13b4-124">Additional resources</span></span>

[<span data-ttu-id="d13b4-125">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="d13b4-125">Text functions</span></span>](er-functions-category-text.md)
