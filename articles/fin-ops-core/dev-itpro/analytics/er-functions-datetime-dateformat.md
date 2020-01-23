---
title: ER-i funktsioon DATEFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATEFORMAT.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: c1453be0c93764f9f0364206822a9e3899061a58
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917576"
---
# <span data-ttu-id="b405a-103"><a name="DATEFORMAT">ER-i funktsioon DATEFORMAT</a></span><span class="sxs-lookup"><span data-stu-id="b405a-103"><a name="DATEFORMAT">DATEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b405a-104">Funktsioon `DATEFORMAT` tagastab *stringi* väärtuse, mis esitab antud kuupäeva väärtuse määratud vormingus tekstina ja valikuliselt määratletud [kultuuris](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="b405a-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="b405a-105">Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="b405a-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b405a-106">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="b405a-106">Syntax 1</span></span>

```
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="b405a-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="b405a-107">Syntax 2</span></span>

```
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="b405a-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="b405a-108">Arguments</span></span>

<span data-ttu-id="b405a-109">`date`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="b405a-109">`date`: *Date*</span></span>

<span data-ttu-id="b405a-110">Kuupäeva väärtus, mis tähistab vormindatavat kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b405a-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="b405a-111">`format`: *string*</span><span class="sxs-lookup"><span data-stu-id="b405a-111">`format`: *String*</span></span>

<span data-ttu-id="b405a-112">Väljundstringi vorming.</span><span class="sxs-lookup"><span data-stu-id="b405a-112">The format of the output string.</span></span>

<span data-ttu-id="b405a-113">`culture`: *string*</span><span class="sxs-lookup"><span data-stu-id="b405a-113">`culture`: *String*</span></span>

<span data-ttu-id="b405a-114">Vormindamiseks kasutatav kultuur.</span><span class="sxs-lookup"><span data-stu-id="b405a-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="b405a-115">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="b405a-115">Return values</span></span>

<span data-ttu-id="b405a-116">*String*</span><span class="sxs-lookup"><span data-stu-id="b405a-116">*String*</span></span>

<span data-ttu-id="b405a-117">Tulemiks saadud stringi väärtus.</span><span class="sxs-lookup"><span data-stu-id="b405a-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b405a-118">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="b405a-118">Usage notes</span></span>

<span data-ttu-id="b405a-119">Kui kultuur pole määratletud kutsutud funktsiooni argumendina, määratleb olemi `culture` väärtuse kutse kontekst.</span><span class="sxs-lookup"><span data-stu-id="b405a-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="b405a-120">Näiteks kui funktsioon `DATEFORMAT` on kutsutud kasutades süntaksit 1 elektroonilise aruandluse (ER) vormingus elemendile **FILE**, mis on konfigureeritud kasutama saksa kultuuri, toimub teisendamine saksa kultuuri kasutades.</span><span class="sxs-lookup"><span data-stu-id="b405a-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="b405a-121">Olemi `culture` vaikeväärtus on **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="b405a-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="b405a-122">Näide 1</span><span class="sxs-lookup"><span data-stu-id="b405a-122">Example 1</span></span>

<span data-ttu-id="b405a-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` tagastab praeguse rakendusserveri kuupäeva väärtuse 24. detsember 2015 stringi kujul **„24-12-2015”** määratud kohandatud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="b405a-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="b405a-124">Näide 2</span><span class="sxs-lookup"><span data-stu-id="b405a-124">Example 2</span></span>

<span data-ttu-id="b405a-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` tagastab praeguse rakenduse seansi kuupäeva 24. detsember 2015 stringina **„24-12-2015”** valitud saksa kultuuri ja määratud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="b405a-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b405a-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b405a-126">Additional resources</span></span>

[<span data-ttu-id="b405a-127">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="b405a-127">Date and time functions</span></span>](er-functions-category-datetime.md)
