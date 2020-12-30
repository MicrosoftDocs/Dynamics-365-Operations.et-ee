---
title: ER-i funktsioon RIGHT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni RIGHT.
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
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682938"
---
# <a name="right-er-function"></a><span data-ttu-id="5fd3e-103">ER-i funktsioon RIGHT</span><span class="sxs-lookup"><span data-stu-id="5fd3e-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fd3e-104">Funktsioon `RIGHT` tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringi lõpust.</span><span class="sxs-lookup"><span data-stu-id="5fd3e-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd3e-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="5fd3e-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5fd3e-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="5fd3e-106">Arguments</span></span>

<span data-ttu-id="5fd3e-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="5fd3e-107">`text`: *String*</span></span>

<span data-ttu-id="5fd3e-108">*Stringi* väärtus, mis tähistab algteksti.</span><span class="sxs-lookup"><span data-stu-id="5fd3e-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="5fd3e-109">`number`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="5fd3e-109">`number`: *Integer*</span></span>

<span data-ttu-id="5fd3e-110">Märkide arv, mis tuleb algteksti lõpust tagastada.</span><span class="sxs-lookup"><span data-stu-id="5fd3e-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5fd3e-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="5fd3e-111">Return values</span></span>

<span data-ttu-id="5fd3e-112">*String*</span><span class="sxs-lookup"><span data-stu-id="5fd3e-112">*String*</span></span>

<span data-ttu-id="5fd3e-113">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="5fd3e-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5fd3e-114">Näide</span><span class="sxs-lookup"><span data-stu-id="5fd3e-114">Example</span></span>

<span data-ttu-id="5fd3e-115">`RIGHT ("Sample", 3)` tagastab **„ple”**.</span><span class="sxs-lookup"><span data-stu-id="5fd3e-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5fd3e-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5fd3e-116">Additional resources</span></span>

[<span data-ttu-id="5fd3e-117">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="5fd3e-117">Text functions</span></span>](er-functions-category-text.md)
