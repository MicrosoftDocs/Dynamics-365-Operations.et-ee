---
title: ER-i funktsioon DATEVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATEVALUE.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 43e65055b0803ed330a19568f9565c3fae488ab2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682409"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="d7213-103">ER-i funktsioon DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="d7213-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7213-104">Funktsioon `DATEVALUE` tagastab *kuupäeva* väärtuse, mis on antud teksti väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva väärtuse [kultuuris](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="d7213-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="d7213-105">Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="d7213-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="d7213-106">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="d7213-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="d7213-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="d7213-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="d7213-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="d7213-108">Arguments</span></span>

<span data-ttu-id="d7213-109">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="d7213-109">`text`: *String*</span></span>

<span data-ttu-id="d7213-110">Tekst, mis tähistab vormindatavat väärtust.</span><span class="sxs-lookup"><span data-stu-id="d7213-110">Text that represents the value to format.</span></span>

<span data-ttu-id="d7213-111">`format`: *string*</span><span class="sxs-lookup"><span data-stu-id="d7213-111">`format`: *String*</span></span>

<span data-ttu-id="d7213-112">Antud teksti vorming.</span><span class="sxs-lookup"><span data-stu-id="d7213-112">The format of the given text.</span></span>

<span data-ttu-id="d7213-113">`culture`: *string*</span><span class="sxs-lookup"><span data-stu-id="d7213-113">`culture`: *String*</span></span>

<span data-ttu-id="d7213-114">Kultuur, mida kasutatakse antud teksti vormindamiseks.</span><span class="sxs-lookup"><span data-stu-id="d7213-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="d7213-115">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="d7213-115">Return values</span></span>

<span data-ttu-id="d7213-116">*Kuupäev*</span><span class="sxs-lookup"><span data-stu-id="d7213-116">*Date*</span></span>

<span data-ttu-id="d7213-117">Tulemiks saadud kuupäeva väärtus.</span><span class="sxs-lookup"><span data-stu-id="d7213-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d7213-118">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="d7213-118">Usage notes</span></span>

<span data-ttu-id="d7213-119">Kui kultuur pole määratletud kutsutud funktsiooni argumendina, määratleb olemi `culture` väärtuse kutse kontekst.</span><span class="sxs-lookup"><span data-stu-id="d7213-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="d7213-120">Näiteks kui funktsioon `DATEVALUE` on kutsutud kasutades süntaksit 1 elektroonilise aruandluse (ER) vormingus elemendile **FILE**, mis on konfigureeritud kasutama saksa kultuuri, toimub teisendamine saksa kultuuri kasutades.</span><span class="sxs-lookup"><span data-stu-id="d7213-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="d7213-121">Olemi `culture` vaikeväärtus on **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="d7213-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="d7213-122">Näide 1</span><span class="sxs-lookup"><span data-stu-id="d7213-122">Example 1</span></span>

<span data-ttu-id="d7213-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` tagastab kuupäeva väärtuse **21. detsember 2016**, mis põhineb määratletud kohandatud vormingul ja vaikerakenduse **EN-US** kultuuril.</span><span class="sxs-lookup"><span data-stu-id="d7213-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="d7213-124">Näide 2</span><span class="sxs-lookup"><span data-stu-id="d7213-124">Example 2</span></span>

<span data-ttu-id="d7213-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` tagastab kuupäeva väärtuse **21. jaanuar 2016**, mis põhineb määratletud kohandatud vormingul ja kultuuril.</span><span class="sxs-lookup"><span data-stu-id="d7213-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="d7213-126">Stringiga `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` ilmneb aga erand, mis teavitab kasutajat sellest, et seda stringi ei tuvastata määratletud kultuuri kehtiva kuupäeva väärtusena.</span><span class="sxs-lookup"><span data-stu-id="d7213-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d7213-127">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d7213-127">Additional resources</span></span>

[<span data-ttu-id="d7213-128">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="d7213-128">Date and time functions</span></span>](er-functions-category-datetime.md)
