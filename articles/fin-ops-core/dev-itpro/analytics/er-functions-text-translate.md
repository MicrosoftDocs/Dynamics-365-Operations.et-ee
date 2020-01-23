---
title: ER-i funktsioon TRANSLATE
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni TRANSLATE.
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
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916702"
---
# <span data-ttu-id="f9a1c-103"><a name="TRANSLATE">ER-i funktsioon TRANSLATE</a></span><span class="sxs-lookup"><span data-stu-id="f9a1c-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9a1c-104">Funktsioon `TRANSLATE` tagastab määratud tekstistringi *stringi* väärtusena pärast seda, kui kõik või osa sellest on asendatud teise stringiga.</span><span class="sxs-lookup"><span data-stu-id="f9a1c-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a1c-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="f9a1c-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="f9a1c-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="f9a1c-106">Arguments</span></span>

<span data-ttu-id="f9a1c-107">`text`: *string*</span><span class="sxs-lookup"><span data-stu-id="f9a1c-107">`text`: *String*</span></span>

<span data-ttu-id="f9a1c-108">Tüübi *String* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="f9a1c-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="f9a1c-109">`pattern`: *string*</span><span class="sxs-lookup"><span data-stu-id="f9a1c-109">`pattern`: *String*</span></span>

<span data-ttu-id="f9a1c-110">Tekst, mis tuleb asendada.</span><span class="sxs-lookup"><span data-stu-id="f9a1c-110">The text that must be replaced.</span></span>

<span data-ttu-id="f9a1c-111">`replacement`: *string*</span><span class="sxs-lookup"><span data-stu-id="f9a1c-111">`replacement`: *String*</span></span>

<span data-ttu-id="f9a1c-112">Asendamiseks kasutatav tekst.</span><span class="sxs-lookup"><span data-stu-id="f9a1c-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="f9a1c-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="f9a1c-113">Return values</span></span>

<span data-ttu-id="f9a1c-114">*String*</span><span class="sxs-lookup"><span data-stu-id="f9a1c-114">*String*</span></span>

<span data-ttu-id="f9a1c-115">Tulemiks saadud teksti väärtus.</span><span class="sxs-lookup"><span data-stu-id="f9a1c-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="f9a1c-116">Näide</span><span class="sxs-lookup"><span data-stu-id="f9a1c-116">Example</span></span>

<span data-ttu-id="f9a1c-117">`TRANSLATE ("abcdef", "cd", "GH")` asendab mustri **„cd”** stringiga **„GH”** ja tagastab väärtuse **„abGHef”**.</span><span class="sxs-lookup"><span data-stu-id="f9a1c-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f9a1c-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f9a1c-118">Additional resources</span></span>

[<span data-ttu-id="f9a1c-119">Tekstifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="f9a1c-119">Text functions</span></span>](er-functions-category-text.md)
