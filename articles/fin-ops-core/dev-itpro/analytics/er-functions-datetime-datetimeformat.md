---
title: ER-i funktsioon DATETIMEFORMAT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni DATETIMEFORMAT.
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
ms.openlocfilehash: 98919f40751a77465ae26acbd46af4396c588b13
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916403"
---
# <span data-ttu-id="95292-103"><a name="DATETIMEFORMAT">ER-i funktsioon DATETIMEFORMAT</a></span><span class="sxs-lookup"><span data-stu-id="95292-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95292-104">Funktsioon `DATETIMEFORMAT` tagastab *stringi* väärtuse, mis esitab antud kuupäeva/kellaaja väärtuse määratud vormingus tekstina ja valikuliselt määratletud [kultuuris](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span><span class="sxs-lookup"><span data-stu-id="95292-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="95292-105">Toetatud vormingute kohta lisateabe saamiseks vt jaotisi [standardne](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) ja [kohandatud](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="95292-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="95292-106">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="95292-106">Syntax 1</span></span>

```
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="95292-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="95292-107">Syntax 2</span></span>

```
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="95292-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="95292-108">Arguments</span></span>

<span data-ttu-id="95292-109">`datetime`: *kuupäev ja kellaaeg*</span><span class="sxs-lookup"><span data-stu-id="95292-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="95292-110">Kuupäeva/kellaaja väärtus, mis tähistab vormindatavat kuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="95292-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="95292-111">`format`: *string*</span><span class="sxs-lookup"><span data-stu-id="95292-111">`format`: *String*</span></span>

<span data-ttu-id="95292-112">Väljundstringi vorming.</span><span class="sxs-lookup"><span data-stu-id="95292-112">The format of the output string.</span></span>

<span data-ttu-id="95292-113">`culture`: *string*</span><span class="sxs-lookup"><span data-stu-id="95292-113">`culture`: *String*</span></span>

<span data-ttu-id="95292-114">Vormindamiseks kasutatav kultuur.</span><span class="sxs-lookup"><span data-stu-id="95292-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="95292-115">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="95292-115">Return values</span></span>

<span data-ttu-id="95292-116">*String*</span><span class="sxs-lookup"><span data-stu-id="95292-116">*String*</span></span>

<span data-ttu-id="95292-117">Tulemiks saadud stringi väärtus.</span><span class="sxs-lookup"><span data-stu-id="95292-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="95292-118">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="95292-118">Usage notes</span></span>

<span data-ttu-id="95292-119">Kui kultuur pole määratletud kutsutud funktsiooni argumendina, määratleb olemi `culture` väärtuse kutse kontekst.</span><span class="sxs-lookup"><span data-stu-id="95292-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="95292-120">Näiteks kui funktsioon `DATETIMEFORMAT` on kutsutud kasutades süntaksit 1 elektroonilise aruandluse (ER) vormingus elemendile **FILE**, mis on konfigureeritud kasutama saksa kultuuri, toimub teisendamine saksa kultuuri kasutades.</span><span class="sxs-lookup"><span data-stu-id="95292-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="95292-121">Olemi `culture` vaikeväärtus on **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="95292-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="95292-122">Kui funktsioon `DATETIMEFORMAT` teisendab antud kuupäeva/kellaaja väärtuse, siis see arvestab rakenduse kasutaja ajavööndit, kes käitab ER-vormingut, mille kontekstis funktsiooni kutsutakse.</span><span class="sxs-lookup"><span data-stu-id="95292-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="95292-123">Näide 1</span><span class="sxs-lookup"><span data-stu-id="95292-123">Example 1</span></span>

<span data-ttu-id="95292-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` annab vastuseks praeguse rakendusserveri kuupäeva/kellaaja väärtuse 24. detsember 2015 kujul **„24-12-2015”** määratud kohandatud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="95292-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="95292-125">Näide 2</span><span class="sxs-lookup"><span data-stu-id="95292-125">Example 2</span></span>

<span data-ttu-id="95292-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` tagastab praeguse rakenduse seansi kuupäeva/kellaaja väärtuse 24. detsember 2015 kujul **„24.12.2015”** valitud saksa kultuuri ja määratud vormingu kohaselt.</span><span class="sxs-lookup"><span data-stu-id="95292-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="95292-127">Näide 3</span><span class="sxs-lookup"><span data-stu-id="95292-127">Example 3</span></span>

<span data-ttu-id="95292-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` tagastab stringi väärtuse **2019-11-12T08:00:00.0000000-08:00**, kui see kutsutakse toimigu ajal, mis käivitati rakenduse kasutaja poolt, kelle ajavööndi väärtus on **(GMT-08:00) Vaikse ookeani aeg (Ameerika Ühendriigid ja Kanada)** jaotises **Keele ja riigi/regiooni eelistused**.</span><span class="sxs-lookup"><span data-stu-id="95292-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95292-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="95292-129">Additional resources</span></span>

[<span data-ttu-id="95292-130">Kuupäeva ja kellaaja funktsioonid</span><span class="sxs-lookup"><span data-stu-id="95292-130">Date and time functions</span></span>](er-functions-category-datetime.md)
