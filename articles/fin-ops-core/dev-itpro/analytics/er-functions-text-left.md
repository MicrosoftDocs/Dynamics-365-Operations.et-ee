---
title: ER-i funktsioon LEFT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni LEFT.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569988"
---
# <a name="left-er-function"></a><span data-ttu-id="3a1b7-103">ER-i funktsioon LEFT</span><span class="sxs-lookup"><span data-stu-id="3a1b7-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a1b7-104">Funktsioon `LEFT` tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringi algusest.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a1b7-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="3a1b7-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="3a1b7-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="3a1b7-106">Arguments</span></span>

<span data-ttu-id="3a1b7-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="3a1b7-107">`text`: *String*</span></span>

<span data-ttu-id="3a1b7-108">*Stringi* väärtus, mis tähistab algteksti.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="3a1b7-109">`number`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="3a1b7-109">`number`: *Integer*</span></span>

<span data-ttu-id="3a1b7-110">Märkide arv, mis tuleb algteksti algusest tagastada.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="3a1b7-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="3a1b7-111">Return values</span></span>

<span data-ttu-id="3a1b7-112">*String*</span><span class="sxs-lookup"><span data-stu-id="3a1b7-112">*String*</span></span>

<span data-ttu-id="3a1b7-113">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="3a1b7-114">Näide</span><span class="sxs-lookup"><span data-stu-id="3a1b7-114">Example</span></span>

<span data-ttu-id="3a1b7-115">`LEFT ("Sample", 3)` tagastab tulemuse **„Sam”**.</span><span class="sxs-lookup"><span data-stu-id="3a1b7-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a1b7-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3a1b7-116">Additional resources</span></span>

[<span data-ttu-id="3a1b7-117">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="3a1b7-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]