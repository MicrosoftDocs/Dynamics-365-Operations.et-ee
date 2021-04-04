---
title: ER-i funktsioon TRANSLATE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TRANSLATE.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: f17d3439870710766906013e74452c2e76fec4ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560009"
---
# <a name="translate-er-function"></a><span data-ttu-id="52a5f-103">ER-i funktsioon TRANSLATE</span><span class="sxs-lookup"><span data-stu-id="52a5f-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52a5f-104">Funktsioon `TRANSLATE` tagastab väärtuse *String*, mis sisaldab määratud teksti tähemärkide muu sisestatud märgikomplektiga asendamise tulemust.</span><span class="sxs-lookup"><span data-stu-id="52a5f-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="52a5f-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="52a5f-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="52a5f-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="52a5f-106">Arguments</span></span>

<span data-ttu-id="52a5f-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="52a5f-107">`text`: *String*</span></span>

<span data-ttu-id="52a5f-108">Tüübi *String* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="52a5f-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="52a5f-109">`pattern`: *string*</span><span class="sxs-lookup"><span data-stu-id="52a5f-109">`pattern`: *String*</span></span>

<span data-ttu-id="52a5f-110">Tekst, mis tuleb asendada.</span><span class="sxs-lookup"><span data-stu-id="52a5f-110">The text that must be replaced.</span></span>

<span data-ttu-id="52a5f-111">`replacement`: *string*</span><span class="sxs-lookup"><span data-stu-id="52a5f-111">`replacement`: *String*</span></span>

<span data-ttu-id="52a5f-112">Asendamiseks kasutatav tekst.</span><span class="sxs-lookup"><span data-stu-id="52a5f-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="52a5f-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="52a5f-113">Return values</span></span>

<span data-ttu-id="52a5f-114">*String*</span><span class="sxs-lookup"><span data-stu-id="52a5f-114">*String*</span></span>

<span data-ttu-id="52a5f-115">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="52a5f-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="52a5f-116">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="52a5f-116">Usage notes</span></span>

<span data-ttu-id="52a5f-117">Funktsioon `TRANSLATE` asendab ühe tähemärgi korraga.</span><span class="sxs-lookup"><span data-stu-id="52a5f-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="52a5f-118">Funktsioon asendab argumendi `text` esimese tähemärgi argumendi `pattern` esimese tähemärgiga ja seejärel asendab kõik ülejäänud tähemärgid sama moodi.</span><span class="sxs-lookup"><span data-stu-id="52a5f-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="52a5f-119">Kui argumentide `text` ja `pattern` tähemärgid ühtivad, asendatakse argumendi `pattern` tähemärk argumendi `replacement` samas kohas asuva tähemärgiga.</span><span class="sxs-lookup"><span data-stu-id="52a5f-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="52a5f-120">Kui tähemärk kuvatakse argumendis `pattern` mitu korda, kasutatakse selle tähemärgi esimesele esinemisele vastavat argumendi `replacement` vastendust.</span><span class="sxs-lookup"><span data-stu-id="52a5f-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="52a5f-121">Näide 1</span><span class="sxs-lookup"><span data-stu-id="52a5f-121">Example 1</span></span>

<span data-ttu-id="52a5f-122">`TRANSLATE ("abcdef", "cd", "GH")` asendab määratud teksti **„abcdef”** tähemärgi **„c”** teksti `replacement` tähemärgiga **„G”** järgmistel põhjustel.</span><span class="sxs-lookup"><span data-stu-id="52a5f-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="52a5f-123">Tähemärk **„c”** asub tekstis `pattern` esimesel positsioonil.</span><span class="sxs-lookup"><span data-stu-id="52a5f-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="52a5f-124">Teksti `replacement` esimesel positsioonil asub tähemärk **„G”**.</span><span class="sxs-lookup"><span data-stu-id="52a5f-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="52a5f-125">Näide 2</span><span class="sxs-lookup"><span data-stu-id="52a5f-125">Example 2</span></span>

<span data-ttu-id="52a5f-126">`TRANSLATE ("abcdef", "ccd", "GH")` tagastab **„abGdef”**.</span><span class="sxs-lookup"><span data-stu-id="52a5f-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="52a5f-127">Näide 3</span><span class="sxs-lookup"><span data-stu-id="52a5f-127">Example 3</span></span>

<span data-ttu-id="52a5f-128">`TRANSLATE ("abccba", "abc", "123")` tagastab **„123321”**.</span><span class="sxs-lookup"><span data-stu-id="52a5f-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="52a5f-129">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="52a5f-129">Additional resources</span></span>

[<span data-ttu-id="52a5f-130">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="52a5f-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]