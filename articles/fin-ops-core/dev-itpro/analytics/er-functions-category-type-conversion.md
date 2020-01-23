---
title: ER-i funktsioonide loend tüübiteisenduse kategoorias
description: See teema annab teavet teisendamise funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
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
ms.openlocfilehash: 2cfa5deb3b2c00565759e4334a002bf112f888ac
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917645"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="1e493-103">ER-i funktsioonide loend tüübiteisenduse kategoorias</span><span class="sxs-lookup"><span data-stu-id="1e493-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e493-104">Elektroonilise aruandluse (ER) tüübiteisenduse funktsioone saab kasutada väärtuste teisendamiseks tüüpide vahel.</span><span class="sxs-lookup"><span data-stu-id="1e493-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="1e493-105">See teema sisaldab järgmiste funktsioonide kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="1e493-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="1e493-106">Tüübiteisenduse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="1e493-106">Type conversion functions</span></span>

| <span data-ttu-id="1e493-107">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="1e493-107">Function</span></span> | <span data-ttu-id="1e493-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1e493-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="1e493-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="1e493-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="1e493-110">See funktsioon tagastab väärtuse *Int64*, mis tähistab määratud stringi.</span><span class="sxs-lookup"><span data-stu-id="1e493-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="1e493-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="1e493-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="1e493-112">See funktsioon tagastab väärtuse *Int*, mis tähistab määratud stringi.</span><span class="sxs-lookup"><span data-stu-id="1e493-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="1e493-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="1e493-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="1e493-114">See funktsioon tagastab *tegeliku* väärtuse, mis konverteeritakse määratud *stringi* väärtusest.</span><span class="sxs-lookup"><span data-stu-id="1e493-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="1e493-115">Teisendamise käigus arvestatakse määratud kümnendkoha ja arvu rühmitamise eraldajaga.</span><span class="sxs-lookup"><span data-stu-id="1e493-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="1e493-116">Väärtus</span><span class="sxs-lookup"><span data-stu-id="1e493-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="1e493-117">See funktsioon tagastab *tegeliku* väärtuse, mis konverteeritakse määratud *stringi* väärtusest.</span><span class="sxs-lookup"><span data-stu-id="1e493-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="1e493-118">Tüübiteisenduse funktsioonid kuupäeva ja kellaaja kategoorias</span><span class="sxs-lookup"><span data-stu-id="1e493-118">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="1e493-119">Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [kuupäeva ja kellaaja kategoorias](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="1e493-119">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="1e493-120">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="1e493-120">Function</span></span> | <span data-ttu-id="1e493-121">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1e493-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="1e493-122">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="1e493-122">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="1e493-123">See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis on antud *stringi* väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva/kellaaja väärtuse kultuuris.</span><span class="sxs-lookup"><span data-stu-id="1e493-123">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="1e493-124">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="1e493-124">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="1e493-125">See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis teisendatakse määratud *kuupäeva* väärtusest kuupäeva/kellaaja väärtuseks koordineeritud maailmaajas (Greenwichi aeg \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="1e493-125">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="1e493-126">DateValue</span><span class="sxs-lookup"><span data-stu-id="1e493-126">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="1e493-127">See funktsioon tagastab *kuupäeva* väärtuse, mis on antud *stringi* väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva väärtuse kultuuris.</span><span class="sxs-lookup"><span data-stu-id="1e493-127">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="1e493-128">Tüübiteisenduse funktsioonid loendi kategoorias</span><span class="sxs-lookup"><span data-stu-id="1e493-128">Type conversion functions in the list category</span></span>

<span data-ttu-id="1e493-129">Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [loendi kategoorias](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="1e493-129">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="1e493-130">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="1e493-130">Function</span></span> | <span data-ttu-id="1e493-131">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1e493-131">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="1e493-132">Loend</span><span class="sxs-lookup"><span data-stu-id="1e493-132">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="1e493-133">See funktsioon tagastab *kirjete loendi* väärtuse uue loendina, mis on loodud *konteineri (kirje)* määratud argumentidest.</span><span class="sxs-lookup"><span data-stu-id="1e493-133">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="1e493-134">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="1e493-134">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="1e493-135">See funktsioon tagastab *kirjete loendi* väärtuse, mis luuakse tüübi *Loetelu* või *Konteiner (kirje)* antud argumendi struktuuri põhjal.</span><span class="sxs-lookup"><span data-stu-id="1e493-135">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="1e493-136">Tükeldamine</span><span class="sxs-lookup"><span data-stu-id="1e493-136">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="1e493-137">See funktsioon tükeldab määratud *stringi* väärtuse alamstringideks ja tagastab tulemuse uue *kirjete loendi* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="1e493-137">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="1e493-138">StringJoin</span><span class="sxs-lookup"><span data-stu-id="1e493-138">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="1e493-139">See funktsioon tagastab *stringi* väärtuse, mis koosneb määratud *kirjete loendi* väärtuse määratud välja liitväärtustest.</span><span class="sxs-lookup"><span data-stu-id="1e493-139">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="1e493-140">Väärtused saab eraldada määratud eraldajaga.</span><span class="sxs-lookup"><span data-stu-id="1e493-140">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="1e493-141">Tüübiteisenduse funktsioonid teksti kategoorias</span><span class="sxs-lookup"><span data-stu-id="1e493-141">Type conversion functions in the text category</span></span>

<span data-ttu-id="1e493-142">Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [teksti kategoorias](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="1e493-142">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="1e493-143">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="1e493-143">Function</span></span> | <span data-ttu-id="1e493-144">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1e493-144">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="1e493-145">Char</span><span class="sxs-lookup"><span data-stu-id="1e493-145">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="1e493-146">See funktsioon tagastab *stringi* väärtuse, mis esindab üksikut märki, millele viitab määratud Unicode’i number.</span><span class="sxs-lookup"><span data-stu-id="1e493-146">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="1e493-147">GuidValue</span><span class="sxs-lookup"><span data-stu-id="1e493-147">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="1e493-148">See funktsioon teisendab *stringi* tüübi määratud sisendi andmeüksuseks tüübiga *GUID*.</span><span class="sxs-lookup"><span data-stu-id="1e493-148">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="1e493-149">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="1e493-149">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="1e493-150">See funktsioon tagastab *stringi* väärtuse, mis esindab määratud numbrit määratud vormingus ja valikuliselt määratletud kultuuris.</span><span class="sxs-lookup"><span data-stu-id="1e493-150">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="1e493-151">QrCode</span><span class="sxs-lookup"><span data-stu-id="1e493-151">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="1e493-152">See funktsioon tagastab *konteineri* väärtuse, mis esitab määratud stringi puhul binaarvormingus ruutkoodi (QR-koodi) pildi.</span><span class="sxs-lookup"><span data-stu-id="1e493-152">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="1e493-153">Tekst</span><span class="sxs-lookup"><span data-stu-id="1e493-153">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="1e493-154">See funktsioon tagastab *stringi* väärtuse, mis esindab määratud numbrit pärast seda, kui see on teisendatud tekstistringiks, mis on vormindatud praeguse rakenduse eksemplari serverilokaadi sätete kohaselt.</span><span class="sxs-lookup"><span data-stu-id="1e493-154">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="1e493-155">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1e493-155">Additional resources</span></span>

[<span data-ttu-id="1e493-156">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="1e493-156">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="1e493-157">Valemikoostaja elektroonilises aruandluses</span><span class="sxs-lookup"><span data-stu-id="1e493-157">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="1e493-158">Elektroonilise aruandluse valemi keel</span><span class="sxs-lookup"><span data-stu-id="1e493-158">Electronic reporting formula language</span></span>](er-formula-language.md)