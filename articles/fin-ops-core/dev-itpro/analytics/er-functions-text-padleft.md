---
title: ER-i funktsioon PADLEFT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni PADLEFT.
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
ms.openlocfilehash: 268941d8bc0bd4dc6de6d2597c05a11c1f530f15
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680142"
---
# <a name="padleft-er-function"></a><span data-ttu-id="554e4-103">ER-i funktsioon PADLEFT</span><span class="sxs-lookup"><span data-stu-id="554e4-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="554e4-104">Funktsioon `PADLEFT` tagastab määratud pikkusega *stringi* väärtuse, milles määratud stringi algusele on lisatud määratud märkidest koosnevad täidismärgid.</span><span class="sxs-lookup"><span data-stu-id="554e4-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="554e4-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="554e4-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="554e4-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="554e4-106">Arguments</span></span>

<span data-ttu-id="554e4-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="554e4-107">`text`: *String*</span></span>

<span data-ttu-id="554e4-108">*Stringi* väärtus, mis tähistab algteksti.</span><span class="sxs-lookup"><span data-stu-id="554e4-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="554e4-109">`length`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="554e4-109">`length`: *Integer*</span></span>

<span data-ttu-id="554e4-110">*Täisarvu* väärtus, mis tähistab täidismärkidega stringi lõplikku tähemärkide arvu.</span><span class="sxs-lookup"><span data-stu-id="554e4-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="554e4-111">`padding chars`: *string*</span><span class="sxs-lookup"><span data-stu-id="554e4-111">`padding chars`: *String*</span></span>

<span data-ttu-id="554e4-112">Täidiseks kasutatavad tähemärgid.</span><span class="sxs-lookup"><span data-stu-id="554e4-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="554e4-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="554e4-113">Return values</span></span>

<span data-ttu-id="554e4-114">*String*</span><span class="sxs-lookup"><span data-stu-id="554e4-114">*String*</span></span>

<span data-ttu-id="554e4-115">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="554e4-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="554e4-116">Näide</span><span class="sxs-lookup"><span data-stu-id="554e4-116">Example</span></span>

<span data-ttu-id="554e4-117">`PADLEFT ("1234", 10, "`&nbsp;`")` tagastab tekstistringi **„&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234”**.</span><span class="sxs-lookup"><span data-stu-id="554e4-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="554e4-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="554e4-118">Additional resources</span></span>

[<span data-ttu-id="554e4-119">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="554e4-119">Text functions</span></span>](er-functions-category-text.md)
