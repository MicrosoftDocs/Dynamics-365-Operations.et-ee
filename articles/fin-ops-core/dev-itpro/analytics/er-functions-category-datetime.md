---
title: ER-i funktsioonide loend kuupäeva ja kellaaja kategoorias
description: See teema annab teavet kuupäeva ja kellaaja funktsioonide kohta, mida toetatakse elektroonilises aruandluses (ER).
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916564"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="3799d-103">ER-i funktsioonide loend kuupäeva ja kellaaja kategoorias</span><span class="sxs-lookup"><span data-stu-id="3799d-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3799d-104">Elektroonilise aruandluse (ER) kuupäeva ja kellaaja funktsioone saab kasutada kuupäeva ja kellaaja väärtustest teabe ekstraktimiseks ning nende kohta toimingute tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="3799d-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="3799d-105">See teema sisaldab järgmiste funktsioonide kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="3799d-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="3799d-106">Toetatud funktsioonide loend</span><span class="sxs-lookup"><span data-stu-id="3799d-106">List of supported functions</span></span>

| <span data-ttu-id="3799d-107">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="3799d-107">Function</span></span> | <span data-ttu-id="3799d-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3799d-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="3799d-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="3799d-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="3799d-110">See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis on määratud alguskuupäevast varasemate või hilisemate päevade arv.</span><span class="sxs-lookup"><span data-stu-id="3799d-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="3799d-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="3799d-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="3799d-112">See funktsioon tagastab *stringi* väärtuse, mis esitab antud kuupäeva väärtuse määratud vormingus tekstina ja valikuliselt määratletud kultuuris.</span><span class="sxs-lookup"><span data-stu-id="3799d-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="3799d-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="3799d-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="3799d-114">See funktsioon tagastab *stringi* väärtuse, mis esitab antud kuupäeva/kellaaja väärtuse määratud vormingus tekstina ja valikuliselt määratletud kultuuris.</span><span class="sxs-lookup"><span data-stu-id="3799d-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="3799d-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="3799d-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="3799d-116">See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis on antud teksti väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva/kellaaja väärtuse kultuuris.</span><span class="sxs-lookup"><span data-stu-id="3799d-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="3799d-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="3799d-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="3799d-118">See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis teisendatakse määratud kuupäevast väärtusest kuupäeva/kellaaja väärtuseks koordineeritud maailmaajas (Greenwichi aeg \[GMT\]).</span><span class="sxs-lookup"><span data-stu-id="3799d-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="3799d-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="3799d-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="3799d-120">See funktsioon tagastab *kuupäeva* väärtuse, mis on antud teksti väärtusest konverteeritud väärtus määratud vormingus tekstina ja valikuliselt määratletud kuupäeva väärtuse kultuuris.</span><span class="sxs-lookup"><span data-stu-id="3799d-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="3799d-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="3799d-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="3799d-122">See funktsioon tagastab *täisarvu* väärtuse, mis tähistab 1. jaanuari ja määratud kuupäeva vahelise päevade arvu täisarvuna.</span><span class="sxs-lookup"><span data-stu-id="3799d-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="3799d-123">Päevi</span><span class="sxs-lookup"><span data-stu-id="3799d-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="3799d-124">See funktsioon tagastab *täisarvu* väärtuse, mis tähistab ühe määratud kuupäeva ja teise määratud kuupäeva vahelise päevade arvu täisarvuna.</span><span class="sxs-lookup"><span data-stu-id="3799d-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="3799d-125">Now</span><span class="sxs-lookup"><span data-stu-id="3799d-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="3799d-126">Selle funktsiooniga tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab rakendusserveri praegust kuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="3799d-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="3799d-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="3799d-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="3799d-128">See funktsioon tagastab *kuupäeva* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuaril 1900).</span><span class="sxs-lookup"><span data-stu-id="3799d-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="3799d-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="3799d-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="3799d-130">See funktsioon tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab kuupäeva väärtust **null** (1. jaanuaril 1900) koordineeritud maailmaajas.</span><span class="sxs-lookup"><span data-stu-id="3799d-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="3799d-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="3799d-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="3799d-132">Selle funktsiooniga tagastab *kuupäeva ja kellaaja* väärtuse, mis tähistab rakenduse seansi praegust kuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="3799d-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="3799d-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="3799d-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="3799d-134">Selle funktsiooniga tagastab *kuupäeva* väärtuse, mis tähistab rakenduse seansi praegust kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="3799d-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="3799d-135">Täna</span><span class="sxs-lookup"><span data-stu-id="3799d-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="3799d-136">Selle funktsiooniga tagastab *kuupäeva* väärtuse, mis tähistab rakendusserveri praegust kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="3799d-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="3799d-137">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3799d-137">Additional resources</span></span>

[<span data-ttu-id="3799d-138">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="3799d-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="3799d-139">Valemikoostaja elektroonilises aruandluses</span><span class="sxs-lookup"><span data-stu-id="3799d-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="3799d-140">Elektroonilise aruandluse valemi keel</span><span class="sxs-lookup"><span data-stu-id="3799d-140">Electronic reporting formula language</span></span>](er-formula-language.md)
