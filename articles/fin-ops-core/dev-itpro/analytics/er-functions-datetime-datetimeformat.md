---
title: ER-i funktsioon DATETIMEFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATETIMEFORMAT.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b7516620763e87440c0fb866ce507c744223a229
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563626"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="3a912-103">ER-i funktsioon DATETIMEFORMAT</span><span class="sxs-lookup"><span data-stu-id="3a912-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a912-104">Funktsioon `DATETIMEFORMAT` tagastab *stringi* väärtuse, mis esitab antud kuupäeva/kellaaja väärtuse määratud vormingus tekstina ja valikuliselt määratletud [kultuuris](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="3a912-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="3a912-105">Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="3a912-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="3a912-106">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="3a912-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="3a912-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="3a912-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="3a912-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="3a912-108">Arguments</span></span>

<span data-ttu-id="3a912-109">`datetime`: *kuupäev ja kellaaeg*</span><span class="sxs-lookup"><span data-stu-id="3a912-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="3a912-110">Kuupäeva/kellaaja väärtus, mis tähistab vormindatavat kuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="3a912-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="3a912-111">`format`: *string*</span><span class="sxs-lookup"><span data-stu-id="3a912-111">`format`: *String*</span></span>

<span data-ttu-id="3a912-112">Väljundstringi vorming.</span><span class="sxs-lookup"><span data-stu-id="3a912-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="3a912-113">Vormingu string on tõstutundlik, kui kasutate kas standardvormingut või kohandatud vormingut.</span><span class="sxs-lookup"><span data-stu-id="3a912-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="3a912-114">Näiteks [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) vormingu määraja „d” tagastab kuupäeva, kasutades lühikest kuupäeva mustrit, samas kui standardne vormingu määraja „D” tagastab kuupäeva pikka kuupäeva mustrit kasutades.</span><span class="sxs-lookup"><span data-stu-id="3a912-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="3a912-115">Lisaks tagastab [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) vormingu määraja „M” kuu vahemikus 1 kuni 12, samas kui kohandatud vormingu määraja „m” tagastab minuti vahemikus 0 kuni 59.</span><span class="sxs-lookup"><span data-stu-id="3a912-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="3a912-116">`culture`: *string*</span><span class="sxs-lookup"><span data-stu-id="3a912-116">`culture`: *String*</span></span>

<span data-ttu-id="3a912-117">Vormindamiseks kasutatav kultuur.</span><span class="sxs-lookup"><span data-stu-id="3a912-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="3a912-118">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="3a912-118">Return values</span></span>

<span data-ttu-id="3a912-119">*String*</span><span class="sxs-lookup"><span data-stu-id="3a912-119">*String*</span></span>

<span data-ttu-id="3a912-120">Tulemiks saadud stringi väärtus.</span><span class="sxs-lookup"><span data-stu-id="3a912-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3a912-121">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="3a912-121">Usage notes</span></span>

<span data-ttu-id="3a912-122">Kui kultuur pole määratletud kutsutud funktsiooni argumendina, määratleb olemi `culture` väärtuse kutse kontekst.</span><span class="sxs-lookup"><span data-stu-id="3a912-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="3a912-123">Näiteks kui funktsioon `DATETIMEFORMAT` on kutsutud kasutades süntaksit 1 elektroonilise aruandluse (ER) vormingus elemendile **FILE**, mis on konfigureeritud kasutama saksa kultuuri, toimub teisendamine saksa kultuuri kasutades.</span><span class="sxs-lookup"><span data-stu-id="3a912-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="3a912-124">Olemi `culture` vaikeväärtus on **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="3a912-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="3a912-125">Kui funktsioon `DATETIMEFORMAT` teisendab antud kuupäeva/kellaaja väärtuse, siis see arvestab rakenduse kasutaja ajavööndit, kes käitab ER-vormingut, mille kontekstis funktsiooni kutsutakse.</span><span class="sxs-lookup"><span data-stu-id="3a912-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="3a912-126">Näide 1</span><span class="sxs-lookup"><span data-stu-id="3a912-126">Example 1</span></span>

<span data-ttu-id="3a912-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` annab vastuseks praeguse rakendusserveri kuupäeva/kellaaja väärtuse 24. detsember 2015 kujul **„24-12-2015”** määratud kohandatud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="3a912-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="3a912-128">Näide 2</span><span class="sxs-lookup"><span data-stu-id="3a912-128">Example 2</span></span>

<span data-ttu-id="3a912-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` tagastab praeguse rakenduse seansi kuupäeva/kellaaja väärtuse 24. detsember 2015 kujul **„24.12.2015”** valitud saksa kultuuri ja määratud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="3a912-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="3a912-130">Näide 3</span><span class="sxs-lookup"><span data-stu-id="3a912-130">Example 3</span></span>

<span data-ttu-id="3a912-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` tagastab stringi väärtuse **2019-11-12T08:00:00.0000000-08:00**, kui see funktsioon kutsutakse toimigu ajal, mis käivitati rakenduse kasutaja poolt, kelle ajavööndi väärtus on **(GMT-08:00) Vaikse ookeani aeg (Ameerika Ühendriigid ja Kanada)** jaotises **Keele ja riigi/regiooni eelistused**.</span><span class="sxs-lookup"><span data-stu-id="3a912-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a912-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3a912-132">Additional resources</span></span>

[<span data-ttu-id="3a912-133">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="3a912-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]