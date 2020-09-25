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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f8a8e2006fe279b25bbf154c6e1802babf51117
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744355"
---
# <a name="padleft-er-function"></a><span data-ttu-id="4fa9e-103">ER-i funktsioon PADLEFT</span><span class="sxs-lookup"><span data-stu-id="4fa9e-103">PADLEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fa9e-104">Funktsioon `PADLEFT` tagastab määratud pikkusega *stringi* väärtuse, milles määratud stringi algusele on lisatud määratud märkidest koosnevad täidismärgid.</span><span class="sxs-lookup"><span data-stu-id="4fa9e-104">The `PADLEFT` function returns a *String* value of the specified length, where the start of the specified string is padded with the specified characters.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa9e-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="4fa9e-105">Syntax</span></span>

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a><span data-ttu-id="4fa9e-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="4fa9e-106">Arguments</span></span>

<span data-ttu-id="4fa9e-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="4fa9e-107">`text`: *String*</span></span>

<span data-ttu-id="4fa9e-108">*Stringi* väärtus, mis tähistab algteksti.</span><span class="sxs-lookup"><span data-stu-id="4fa9e-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="4fa9e-109">`length`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="4fa9e-109">`length`: *Integer*</span></span>

<span data-ttu-id="4fa9e-110">*Täisarvu* väärtus, mis tähistab täidismärkidega stringi lõplikku tähemärkide arvu.</span><span class="sxs-lookup"><span data-stu-id="4fa9e-110">An *Integer* value that represents the final number of characters in the padded string.</span></span>

<span data-ttu-id="4fa9e-111">`padding chars`: *string*</span><span class="sxs-lookup"><span data-stu-id="4fa9e-111">`padding chars`: *String*</span></span>

<span data-ttu-id="4fa9e-112">Täidiseks kasutatavad tähemärgid.</span><span class="sxs-lookup"><span data-stu-id="4fa9e-112">The characters to use for padding.</span></span>

## <a name="return-values"></a><span data-ttu-id="4fa9e-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="4fa9e-113">Return values</span></span>

<span data-ttu-id="4fa9e-114">*String*</span><span class="sxs-lookup"><span data-stu-id="4fa9e-114">*String*</span></span>

<span data-ttu-id="4fa9e-115">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="4fa9e-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4fa9e-116">Näide</span><span class="sxs-lookup"><span data-stu-id="4fa9e-116">Example</span></span>

<span data-ttu-id="4fa9e-117">`PADLEFT ("1234", 10, "`&nbsp;`")` tagastab tekstistringi **„&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234”**.</span><span class="sxs-lookup"><span data-stu-id="4fa9e-117">`PADLEFT ("1234", 10, "`&nbsp;`")` returns the text string **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4fa9e-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4fa9e-118">Additional resources</span></span>

[<span data-ttu-id="4fa9e-119">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="4fa9e-119">Text functions</span></span>](er-functions-category-text.md)
