---
title: ER-i funktsioon NUMBERVALUE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni NUMBERVALUE.
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755344"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="b7b3e-103">ER-i funktsioon NUMBERVALUE</span><span class="sxs-lookup"><span data-stu-id="b7b3e-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7b3e-104">Funktsioon `NUMBERVALUE` tagastab *tegeliku* väärtuse, mis konverteeritakse määratud *stringi* väärtusest.</span><span class="sxs-lookup"><span data-stu-id="b7b3e-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="b7b3e-105">Teisendamise käigus arvestatakse määratud kümnendkoha ja arvu rühmitamise eraldajaga.</span><span class="sxs-lookup"><span data-stu-id="b7b3e-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7b3e-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="b7b3e-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="b7b3e-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="b7b3e-107">Arguments</span></span>

<span data-ttu-id="b7b3e-108">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="b7b3e-108">`text`: *String*</span></span>

<span data-ttu-id="b7b3e-109">Teksti väärtus, mis tuleb teisendada *täisarvuliseks* numbriks.</span><span class="sxs-lookup"><span data-stu-id="b7b3e-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="b7b3e-110">`decimal separator`: string</span><span class="sxs-lookup"><span data-stu-id="b7b3e-110">`decimal separator`: String</span></span>

<span data-ttu-id="b7b3e-111">Komakohaeraldaja.</span><span class="sxs-lookup"><span data-stu-id="b7b3e-111">A decimal separator.</span></span> <span data-ttu-id="b7b3e-112">Seda kasutatakse kümnendarvu täisarvu ja murdosa eraldamiseks.</span><span class="sxs-lookup"><span data-stu-id="b7b3e-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="b7b3e-113">`digit grouping separator`: *string*</span><span class="sxs-lookup"><span data-stu-id="b7b3e-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="b7b3e-114">Arvu rühmitamise eraldaja.</span><span class="sxs-lookup"><span data-stu-id="b7b3e-114">A digit grouping separator.</span></span> <span data-ttu-id="b7b3e-115">Seda kasutatakse tuhandikeraldajana.</span><span class="sxs-lookup"><span data-stu-id="b7b3e-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="b7b3e-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="b7b3e-116">Return values</span></span>

<span data-ttu-id="b7b3e-117">*Tegelik*</span><span class="sxs-lookup"><span data-stu-id="b7b3e-117">*Real*</span></span>

<span data-ttu-id="b7b3e-118">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="b7b3e-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="b7b3e-119">Näide</span><span class="sxs-lookup"><span data-stu-id="b7b3e-119">Example</span></span>

<span data-ttu-id="b7b3e-120">`NUMBERVALUE( "1 234,56", ",", " ")` tagastab **1234,56**.</span><span class="sxs-lookup"><span data-stu-id="b7b3e-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7b3e-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b7b3e-121">Additional resources</span></span>

[<span data-ttu-id="b7b3e-122">Tüübiteisenduse funktsioonid</span><span class="sxs-lookup"><span data-stu-id="b7b3e-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]