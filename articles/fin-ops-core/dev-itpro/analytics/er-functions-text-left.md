---
title: ER-i funktsioon LEFT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LEFT.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8280a05ea180d9de499d87efa53eca8ca912b0e3
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915644"
---
# <span data-ttu-id="f0e00-103"><a name="LEFT">ER-i funktsioon LEFT</a></span><span class="sxs-lookup"><span data-stu-id="f0e00-103"><a name="LEFT">LEFT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f0e00-104">Funktsioon `LEFT` tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringi algusest.</span><span class="sxs-lookup"><span data-stu-id="f0e00-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0e00-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="f0e00-105">Syntax</span></span>

```
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="f0e00-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="f0e00-106">Arguments</span></span>

<span data-ttu-id="f0e00-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="f0e00-107">`text`: *String*</span></span>

<span data-ttu-id="f0e00-108">*Stringi* väärtus, mis tähistab algteksti.</span><span class="sxs-lookup"><span data-stu-id="f0e00-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="f0e00-109">`number`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="f0e00-109">`number`: *Integer*</span></span>

<span data-ttu-id="f0e00-110">Märkide arv, mis tuleb algteksti algusest tagastada.</span><span class="sxs-lookup"><span data-stu-id="f0e00-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="f0e00-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="f0e00-111">Return values</span></span>

<span data-ttu-id="f0e00-112">*String*</span><span class="sxs-lookup"><span data-stu-id="f0e00-112">*String*</span></span>

<span data-ttu-id="f0e00-113">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="f0e00-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f0e00-114">Näide</span><span class="sxs-lookup"><span data-stu-id="f0e00-114">Example</span></span>

<span data-ttu-id="f0e00-115">`LEFT ("Sample", 3)` tagastab tulemuse **„Sam”**.</span><span class="sxs-lookup"><span data-stu-id="f0e00-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f0e00-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f0e00-116">Additional resources</span></span>

[<span data-ttu-id="f0e00-117">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="f0e00-117">Text functions</span></span>](er-functions-category-text.md)
