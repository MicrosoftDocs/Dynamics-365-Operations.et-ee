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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7169d9d3d2cdfb9f36bb77c1688922549e79ff32
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040867"
---
# <span data-ttu-id="0db75-103"><a name="RIGHT">ER-i funktsioon RIGHT</a></span><span class="sxs-lookup"><span data-stu-id="0db75-103"><a name="RIGHT">RIGHT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0db75-104">Funktsioon `RIGHT` tagastab *stringi* väärtuse, mis esindab määratud tähemärkide arvu määratud stringi lõpust.</span><span class="sxs-lookup"><span data-stu-id="0db75-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0db75-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="0db75-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="0db75-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="0db75-106">Arguments</span></span>

<span data-ttu-id="0db75-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="0db75-107">`text`: *String*</span></span>

<span data-ttu-id="0db75-108">*Stringi* väärtus, mis tähistab algteksti.</span><span class="sxs-lookup"><span data-stu-id="0db75-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="0db75-109">`number`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="0db75-109">`number`: *Integer*</span></span>

<span data-ttu-id="0db75-110">Märkide arv, mis tuleb algteksti lõpust tagastada.</span><span class="sxs-lookup"><span data-stu-id="0db75-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="0db75-111">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="0db75-111">Return values</span></span>

<span data-ttu-id="0db75-112">*String*</span><span class="sxs-lookup"><span data-stu-id="0db75-112">*String*</span></span>

<span data-ttu-id="0db75-113">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="0db75-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="0db75-114">Näide</span><span class="sxs-lookup"><span data-stu-id="0db75-114">Example</span></span>

<span data-ttu-id="0db75-115">`RIGHT ("Sample", 3)` tagastab **„ple”**.</span><span class="sxs-lookup"><span data-stu-id="0db75-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0db75-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0db75-116">Additional resources</span></span>

[<span data-ttu-id="0db75-117">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="0db75-117">Text functions</span></span>](er-functions-category-text.md)
