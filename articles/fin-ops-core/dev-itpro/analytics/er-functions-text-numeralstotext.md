---
title: ER-i funktsioon NUMERALSTOTEXT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NUMERALSTOTEXT.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4af3926998d128f8269ab9af46caeb8be896509
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680214"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="56342-103">ER-i funktsioon NUMERALSTOTEXT</span><span class="sxs-lookup"><span data-stu-id="56342-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56342-104">Funktsioon `NUMERALSTOTEXT` tagastab määratud numbri *stringi* väärtusena pärast selle määratud keeles tekstistringideks kirjutamist (st teisendamist).</span><span class="sxs-lookup"><span data-stu-id="56342-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="56342-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="56342-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="56342-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="56342-106">Arguments</span></span>

<span data-ttu-id="56342-107">`number`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="56342-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="56342-108">Numbriline väärtus, mis määrab arvu, mis tuleb välja kirjutada.</span><span class="sxs-lookup"><span data-stu-id="56342-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="56342-109">`language`: *string*</span><span class="sxs-lookup"><span data-stu-id="56342-109">`language`: *String*</span></span>

<span data-ttu-id="56342-110">*Stringi* väärtus, mis tähistab keelekoodi.</span><span class="sxs-lookup"><span data-stu-id="56342-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="56342-111">`currency`: *string*</span><span class="sxs-lookup"><span data-stu-id="56342-111">`currency`: *String*</span></span>

<span data-ttu-id="56342-112">*Stringi* väärtus, mis tähistab valuutakoodi.</span><span class="sxs-lookup"><span data-stu-id="56342-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="56342-113">`print currency name flag`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="56342-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="56342-114">*Kahendmuutuja* väärtus, mis näitab, kas valuuta nimi peab olema lisatud väljakirjutatud tekstile.</span><span class="sxs-lookup"><span data-stu-id="56342-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="56342-115">`decimal points`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="56342-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="56342-116">*Täisarvu* väärtus, mis näitab kümnendkohtade arvu, mis väljakirjutatud tekstil peab olema.</span><span class="sxs-lookup"><span data-stu-id="56342-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="56342-117">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="56342-117">Return values</span></span>

<span data-ttu-id="56342-118">*String*</span><span class="sxs-lookup"><span data-stu-id="56342-118">*String*</span></span>

<span data-ttu-id="56342-119">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="56342-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="56342-120">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="56342-120">Usage notes</span></span>

<span data-ttu-id="56342-121">Keelekood ei ole kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="56342-121">The language code is optional.</span></span> <span data-ttu-id="56342-122">Kui see on määratletud tühja stringina, kasutatakse käitatava konteksti keelekoodi.</span><span class="sxs-lookup"><span data-stu-id="56342-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="56342-123">Vaikimisi keelekood on **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="56342-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="56342-124">Käitatava konteksti keelekood on määratletud töötava elektroonilise aruandluse (ER) vormingu elemendis **Kaust** või **Fail**.</span><span class="sxs-lookup"><span data-stu-id="56342-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="56342-125">Valuutakood ei ole kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="56342-125">The currency code is optional.</span></span> <span data-ttu-id="56342-126">Kui see on määratletud tühja stringina, kasutatakse käitatava konteksti ettevõtte valuutat.</span><span class="sxs-lookup"><span data-stu-id="56342-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="56342-127">Argumente `print currency name flag` ja `decimal points` analüüsitakse ainult järgmiste keelekoodide puhul: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** ja **RU**.</span><span class="sxs-lookup"><span data-stu-id="56342-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="56342-128">Peale selle analüüsitakse argumenti `print currency name flag` ainult nende ettevõtete puhul, mille riigi või piirkonna kontekst toetab valuuta nimede käänamist.</span><span class="sxs-lookup"><span data-stu-id="56342-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="56342-129">Näide 1</span><span class="sxs-lookup"><span data-stu-id="56342-129">Example 1</span></span>

<span data-ttu-id="56342-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` tagastab vastuse **„One Thousand Two Hundred Thirty Four and 56”**.</span><span class="sxs-lookup"><span data-stu-id="56342-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="56342-131">Näide 2</span><span class="sxs-lookup"><span data-stu-id="56342-131">Example 2</span></span>

<span data-ttu-id="56342-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` tagastab vastuse **Sto dwadzieścia**.</span><span class="sxs-lookup"><span data-stu-id="56342-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="56342-133">Näide 3</span><span class="sxs-lookup"><span data-stu-id="56342-133">Example 3</span></span>

<span data-ttu-id="56342-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` tagastab vastuse **„Сто двадцать евро 21 евроцент”**.</span><span class="sxs-lookup"><span data-stu-id="56342-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56342-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="56342-135">Additional resources</span></span>

[<span data-ttu-id="56342-136">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="56342-136">Text functions</span></span>](er-functions-category-text.md)
