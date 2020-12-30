---
title: ER-i funktsioon LEN
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LEN.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 8d766b8effa9d6936de7a3def252536603330965
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680356"
---
# <a name="len-er-function"></a><span data-ttu-id="ebca5-103">ER-i funktsioon LEN</span><span class="sxs-lookup"><span data-stu-id="ebca5-103">LEN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebca5-104">Funktsioon `LEN` tagastab tähemärkide arvu määratud stringis *täisarvu* väärtusena.</span><span class="sxs-lookup"><span data-stu-id="ebca5-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebca5-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="ebca5-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="ebca5-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="ebca5-106">Arguments</span></span>

<span data-ttu-id="ebca5-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="ebca5-107">`text`: *String*</span></span>

<span data-ttu-id="ebca5-108">*Stringi* väärtus, mis määrab teksti.</span><span class="sxs-lookup"><span data-stu-id="ebca5-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="ebca5-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="ebca5-109">Return values</span></span>

<span data-ttu-id="ebca5-110">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="ebca5-110">*Integer*</span></span>

<span data-ttu-id="ebca5-111">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="ebca5-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="ebca5-112">Näide</span><span class="sxs-lookup"><span data-stu-id="ebca5-112">Example</span></span>

<span data-ttu-id="ebca5-113">`LEN ("Sample")` tagastab **6**.</span><span class="sxs-lookup"><span data-stu-id="ebca5-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ebca5-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ebca5-114">Additional resources</span></span>

[<span data-ttu-id="ebca5-115">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="ebca5-115">Text functions</span></span>](er-functions-category-text.md)
