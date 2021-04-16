---
title: ER-i funktsioonide loend tüübiteisenduse kategoorias
description: See teema annab teavet teisendamise funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
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
ms.openlocfilehash: 199d51ae8a4dbdd7d2f3bd290a2b487ceb1174dc
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752600"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a><span data-ttu-id="27ca4-103">ER-i funktsioonide loend tüübiteisenduse kategoorias</span><span class="sxs-lookup"><span data-stu-id="27ca4-103">List of ER functions in the type conversion category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27ca4-104">Elektroonilise aruandluse (ER) tüübiteisenduse funktsioone saab kasutada väärtuste teisendamiseks tüüpide vahel.</span><span class="sxs-lookup"><span data-stu-id="27ca4-104">Electronic reporting (ER) type conversion functions can be used to convert values between types.</span></span> <span data-ttu-id="27ca4-105">See teema sisaldab järgmiste funktsioonide kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="27ca4-105">This topic provides a summary of these functions.</span></span>

## <a name="type-conversion-functions"></a><span data-ttu-id="27ca4-106">Tüübiteisenduse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="27ca4-106">Type conversion functions</span></span>

| <span data-ttu-id="27ca4-107">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="27ca4-107">Function</span></span> | <span data-ttu-id="27ca4-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="27ca4-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="27ca4-109">Int64Value</span><span class="sxs-lookup"><span data-stu-id="27ca4-109">Int64Value</span></span>](er-functions-conversion-int64value.md)   | <span data-ttu-id="27ca4-110">See funktsioon tagastab väärtuse *Int64*, mis tähistab määratud stringi.</span><span class="sxs-lookup"><span data-stu-id="27ca4-110">This function returns an *Int64* value that represents the specified string.</span></span> |
| [<span data-ttu-id="27ca4-111">IntValue</span><span class="sxs-lookup"><span data-stu-id="27ca4-111">IntValue</span></span>](er-functions-conversion-intvalue.md)       | <span data-ttu-id="27ca4-112">See funktsioon tagastab väärtuse *Int*, mis tähistab määratud stringi.</span><span class="sxs-lookup"><span data-stu-id="27ca4-112">This function returns an *Int* value that represents the specified string.</span></span> |
| [<span data-ttu-id="27ca4-113">NumberValue</span><span class="sxs-lookup"><span data-stu-id="27ca4-113">NumberValue</span></span>](er-functions-conversion-numbervalue.md) | <span data-ttu-id="27ca4-114">See funktsioon tagastab *tegeliku* väärtuse, mis konverteeritakse määratud *stringi* väärtusest.</span><span class="sxs-lookup"><span data-stu-id="27ca4-114">This function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="27ca4-115">Teisendamise käigus arvestatakse määratud kümnendkoha ja arvu rühmitamise eraldajaga.</span><span class="sxs-lookup"><span data-stu-id="27ca4-115">During the conversion, the specified decimal and digit grouping separators are considered.</span></span> |
| [<span data-ttu-id="27ca4-116">Väärtus</span><span class="sxs-lookup"><span data-stu-id="27ca4-116">Value</span></span>](er-functions-conversion-value.md)             | <span data-ttu-id="27ca4-117">See funktsioon tagastab *tegeliku* väärtuse, mis konverteeritakse määratud *stringi* väärtusest.</span><span class="sxs-lookup"><span data-stu-id="27ca4-117">This function returns a *Real* value that is converted from the specified *String* value.</span></span> |

## <a name="type-conversion-functions-in-the-container-category"></a><span data-ttu-id="27ca4-118">Tüübiteisenduse funktsioonid konteineri kategoorias</span><span class="sxs-lookup"><span data-stu-id="27ca4-118">Type conversion functions in the container category</span></span>

<span data-ttu-id="27ca4-119">Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [konteineri](er-functions-category-container.md) kategoorias.</span><span class="sxs-lookup"><span data-stu-id="27ca4-119">The following table describes the type conversion functions in the [container](er-functions-category-container.md) category.</span></span>

| <span data-ttu-id="27ca4-120">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="27ca4-120">Function</span></span> | <span data-ttu-id="27ca4-121">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="27ca4-121">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="27ca4-122">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="27ca4-122">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="27ca4-123">See funktsioon teisendab *stringi* tüübi määratud sisendi andmeüksuseks tüübiga *Konteiner*.</span><span class="sxs-lookup"><span data-stu-id="27ca4-123">This function converts the specified input of the *String* type to a data item of the *Container* type.</span></span> |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a><span data-ttu-id="27ca4-124">Tüübiteisenduse funktsioonid kuupäeva ja kellaaja kategoorias</span><span class="sxs-lookup"><span data-stu-id="27ca4-124">Type conversion functions in the date and time category</span></span>

<span data-ttu-id="27ca4-125">Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [kuupäeva ja kellaaja kategoorias](er-functions-category-datetime.md).</span><span class="sxs-lookup"><span data-stu-id="27ca4-125">The following table describes the type conversion functions in the [date and time category](er-functions-category-datetime.md).</span></span>

| <span data-ttu-id="27ca4-126">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="27ca4-126">Function</span></span> | <span data-ttu-id="27ca4-127">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="27ca4-127">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="27ca4-128">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="27ca4-128">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md)   | <span data-ttu-id="27ca4-129">See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis on antud *stringi* väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva/kellaaja väärtuse kultuuris.</span><span class="sxs-lookup"><span data-stu-id="27ca4-129">This function returns a *DateTime* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="27ca4-130">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="27ca4-130">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="27ca4-131">See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis teisendatakse määratud *kuupäeva* väärtusest kuupäeva/kellaaja väärtuseks koordineeritud maailmaajas (Greenwichi aeg \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="27ca4-131">This function returns a *DateTime* value that is converted from a given *Date* value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="27ca4-132">DateValue</span><span class="sxs-lookup"><span data-stu-id="27ca4-132">DateValue</span></span>](er-functions-datetime-datevalue.md)           | <span data-ttu-id="27ca4-133">See funktsioon tagastab *kuupäeva* väärtuse, mis on antud *stringi* väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva väärtuse kultuuris.</span><span class="sxs-lookup"><span data-stu-id="27ca4-133">This function returns a *Date* value that is converted from a given *String* value in the specified format and in an optionally specified culture to a date value.</span></span> |

## <a name="type-conversion-functions-in-the-list-category"></a><span data-ttu-id="27ca4-134">Tüübiteisenduse funktsioonid loendi kategoorias</span><span class="sxs-lookup"><span data-stu-id="27ca4-134">Type conversion functions in the list category</span></span>

<span data-ttu-id="27ca4-135">Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [loendi kategoorias](er-functions-category-list.md).</span><span class="sxs-lookup"><span data-stu-id="27ca4-135">The following table describes the type conversion functions in the [list category](er-functions-category-list.md).</span></span>

| <span data-ttu-id="27ca4-136">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="27ca4-136">Function</span></span> | <span data-ttu-id="27ca4-137">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="27ca4-137">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="27ca4-138">Loend</span><span class="sxs-lookup"><span data-stu-id="27ca4-138">List</span></span>](er-functions-list-list.md)                 | <span data-ttu-id="27ca4-139">See funktsioon tagastab *kirjete loendi* väärtuse uue loendina, mis on loodud *konteineri (kirje)* määratud argumentidest.</span><span class="sxs-lookup"><span data-stu-id="27ca4-139">This function returns a *Record list* value as a new list that is created from specified arguments of the *Container (record)* type.</span></span> |
| [<span data-ttu-id="27ca4-140">ListOfFields</span><span class="sxs-lookup"><span data-stu-id="27ca4-140">ListOfFields</span></span>](er-functions-list-listoffields.md) | <span data-ttu-id="27ca4-141">See funktsioon tagastab *kirjete loendi* väärtuse, mis luuakse tüübi *Loetelu* või *Konteiner (kirje)* antud argumendi struktuuri põhjal.</span><span class="sxs-lookup"><span data-stu-id="27ca4-141">This function returns a *Record list* value that is created based on the structure of a given argument of the *Enumeration* or *Container (record)* type.</span></span> |
| [<span data-ttu-id="27ca4-142">Tükeldamine</span><span class="sxs-lookup"><span data-stu-id="27ca4-142">Split</span></span>](er-functions-list-split.md)               | <span data-ttu-id="27ca4-143">See funktsioon tükeldab määratud *stringi* väärtuse alamstringideks ja tagastab tulemuse uue *kirjete loendi* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="27ca4-143">This function splits the specified *String* value into substrings and returns the result as a new *Record list* value.</span></span> |
| [<span data-ttu-id="27ca4-144">StringJoin</span><span class="sxs-lookup"><span data-stu-id="27ca4-144">StringJoin</span></span>](er-functions-list-stringjoin.md)     | <span data-ttu-id="27ca4-145">See funktsioon tagastab *stringi* väärtuse, mis koosneb määratud *kirjete loendi* väärtuse määratud välja liitväärtustest.</span><span class="sxs-lookup"><span data-stu-id="27ca4-145">This function returns a *String* value that consists of concatenated values of the specified field from the specified *Record list* value.</span></span> <span data-ttu-id="27ca4-146">Väärtused saab eraldada määratud eraldajaga.</span><span class="sxs-lookup"><span data-stu-id="27ca4-146">The values can be separated by the specified delimiter.</span></span> |

## <a name="type-conversion-functions-in-the-text-category"></a><span data-ttu-id="27ca4-147">Tüübiteisenduse funktsioonid teksti kategoorias</span><span class="sxs-lookup"><span data-stu-id="27ca4-147">Type conversion functions in the text category</span></span>

<span data-ttu-id="27ca4-148">Järgmises tabelis kirjeldatakse tüübiteisenduse funktsioone [teksti kategoorias](er-functions-category-text.md).</span><span class="sxs-lookup"><span data-stu-id="27ca4-148">The following table describes the type conversion functions in the [text category](er-functions-category-text.md).</span></span>

| <span data-ttu-id="27ca4-149">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="27ca4-149">Function</span></span> | <span data-ttu-id="27ca4-150">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="27ca4-150">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="27ca4-151">Char</span><span class="sxs-lookup"><span data-stu-id="27ca4-151">Char</span></span>](er-functions-text-char.md)                 | <span data-ttu-id="27ca4-152">See funktsioon tagastab *stringi* väärtuse, mis esindab üksikut märki, millele viitab määratud Unicode’i number.</span><span class="sxs-lookup"><span data-stu-id="27ca4-152">This function returns a *String* value that represents a single character that is referenced by the specified Unicode number.</span></span> |
| [<span data-ttu-id="27ca4-153">GuidValue</span><span class="sxs-lookup"><span data-stu-id="27ca4-153">GuidValue</span></span>](er-functions-text-guidvalue.md)       | <span data-ttu-id="27ca4-154">See funktsioon teisendab *stringi* tüübi määratud sisendi andmeüksuseks tüübiga *GUID*.</span><span class="sxs-lookup"><span data-stu-id="27ca4-154">This function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span> |
| [<span data-ttu-id="27ca4-155">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="27ca4-155">NumberFormat</span></span>](er-functions-text-numberformat.md) | <span data-ttu-id="27ca4-156">See funktsioon tagastab *stringi* väärtuse, mis esindab määratud numbrit määratud vormingus ja valikuliselt määratletud kultuuris.</span><span class="sxs-lookup"><span data-stu-id="27ca4-156">This function returns a *String* value that represents the specified number in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="27ca4-157">QrCode</span><span class="sxs-lookup"><span data-stu-id="27ca4-157">QrCode</span></span>](er-functions-text-qrcode.md)             | <span data-ttu-id="27ca4-158">See funktsioon tagastab *konteineri* väärtuse, mis esitab määratud stringi puhul binaarvormingus ruutkoodi (QR-koodi) pildi.</span><span class="sxs-lookup"><span data-stu-id="27ca4-158">This function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span> |
| [<span data-ttu-id="27ca4-159">Tekst</span><span class="sxs-lookup"><span data-stu-id="27ca4-159">Text</span></span>](er-functions-text-text.md)                 | <span data-ttu-id="27ca4-160">See funktsioon tagastab *stringi* väärtuse, mis esindab määratud numbrit pärast seda, kui see on teisendatud tekstistringiks, mis on vormindatud praeguse rakenduse eksemplari serverilokaadi sätete kohaselt.</span><span class="sxs-lookup"><span data-stu-id="27ca4-160">This function returns a *String* value that represents the specified number after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="27ca4-161">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="27ca4-161">Additional resources</span></span>

[<span data-ttu-id="27ca4-162">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="27ca4-162">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="27ca4-163">Valemikoostaja elektroonilises aruandluses</span><span class="sxs-lookup"><span data-stu-id="27ca4-163">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="27ca4-164">Elektroonilise aruandluse valemi keel</span><span class="sxs-lookup"><span data-stu-id="27ca4-164">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]