---
title: ER-i funktsioon DATEFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATEFORMAT.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 5a38f0016f69792e5beffa5d8224c70d6e5261c4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747031"
---
# <a name="dateformat-er-function"></a><span data-ttu-id="65491-103">ER-i funktsioon DATEFORMAT</span><span class="sxs-lookup"><span data-stu-id="65491-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65491-104">Funktsioon `DATEFORMAT` tagastab *stringi* väärtuse, mis esitab antud kuupäeva väärtuse määratud vormingus tekstina ja valikuliselt määratletud [kultuuris](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="65491-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="65491-105">Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="65491-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="65491-106">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="65491-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="65491-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="65491-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="65491-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="65491-108">Arguments</span></span>

<span data-ttu-id="65491-109">`date`: *kuupäev*</span><span class="sxs-lookup"><span data-stu-id="65491-109">`date`: *Date*</span></span>

<span data-ttu-id="65491-110">Kuupäeva väärtus, mis tähistab vormindatavat kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="65491-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="65491-111">`format`: *string*</span><span class="sxs-lookup"><span data-stu-id="65491-111">`format`: *String*</span></span>

<span data-ttu-id="65491-112">Väljundstringi vorming.</span><span class="sxs-lookup"><span data-stu-id="65491-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="65491-113">Vormingu string on tõstutundlik, kui kasutate kas standardvormingut või kohandatud vormingut.</span><span class="sxs-lookup"><span data-stu-id="65491-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="65491-114">Näiteks [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) vormingu määraja „d” tagastab kuupäeva, kasutades lühikest kuupäeva mustrit, samas kui standardne vormingu määraja „D” tagastab kuupäeva pikka kuupäeva mustrit kasutades.</span><span class="sxs-lookup"><span data-stu-id="65491-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="65491-115">Lisaks tagastab [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) vormingu määraja „M” kuu vahemikus 1 kuni 12, samas kui kohandatud vormingu määraja „m” tagastab minuti vahemikus 0 kuni 59.</span><span class="sxs-lookup"><span data-stu-id="65491-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="65491-116">`culture`: *string*</span><span class="sxs-lookup"><span data-stu-id="65491-116">`culture`: *String*</span></span>

<span data-ttu-id="65491-117">Vormindamiseks kasutatav kultuur.</span><span class="sxs-lookup"><span data-stu-id="65491-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="65491-118">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="65491-118">Return values</span></span>

<span data-ttu-id="65491-119">*String*</span><span class="sxs-lookup"><span data-stu-id="65491-119">*String*</span></span>

<span data-ttu-id="65491-120">Tulemiks saadud stringi väärtus.</span><span class="sxs-lookup"><span data-stu-id="65491-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="65491-121">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="65491-121">Usage notes</span></span>

<span data-ttu-id="65491-122">Kui kultuur pole määratletud kutsutud funktsiooni argumendina, määratleb olemi `culture` väärtuse kutse kontekst.</span><span class="sxs-lookup"><span data-stu-id="65491-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="65491-123">Näiteks kui funktsioon `DATEFORMAT` on kutsutud kasutades süntaksit 1 elektroonilise aruandluse (ER) vormingus elemendile **FILE**, mis on konfigureeritud kasutama saksa kultuuri, toimub teisendamine saksa kultuuri kasutades.</span><span class="sxs-lookup"><span data-stu-id="65491-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="65491-124">Olemi `culture` vaikeväärtus on **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="65491-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="65491-125">Näide 1</span><span class="sxs-lookup"><span data-stu-id="65491-125">Example 1</span></span>

<span data-ttu-id="65491-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` tagastab praeguse rakendusserveri kuupäeva väärtuse 24. detsember 2015 stringi kujul **„24-12-2015”** määratud kohandatud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="65491-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="65491-127">Näide 2</span><span class="sxs-lookup"><span data-stu-id="65491-127">Example 2</span></span>

<span data-ttu-id="65491-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` tagastab praeguse rakenduse seansi kuupäeva 24. detsember 2015 stringina **„24-12-2015”** valitud saksa kultuuri ja määratud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="65491-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65491-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="65491-129">Additional resources</span></span>

[<span data-ttu-id="65491-130">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="65491-130">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]