---
title: ER-i funktsioon ISEMPTY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ISEMPTY.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b689e6d4bb849f07db5d00cf8a9dc5c16646a927
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563868"
---
# <a name="isempty-er-function"></a><span data-ttu-id="94798-103">ER-i funktsioon ISEMPTY</span><span class="sxs-lookup"><span data-stu-id="94798-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94798-104">Kui määratud loend ei sisalda ühtegi kirjet, tagastab funktsioon `ISEMPTY` *kahendmuutuja* väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="94798-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="94798-105">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="94798-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="94798-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="94798-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="94798-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="94798-107">Arguments</span></span>

<span data-ttu-id="94798-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="94798-108">`list`: *Record list*</span></span>

<span data-ttu-id="94798-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="94798-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="94798-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="94798-110">Return values</span></span>

<span data-ttu-id="94798-111">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="94798-111">*Boolean*</span></span>

<span data-ttu-id="94798-112">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="94798-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="94798-113">Näide 1</span><span class="sxs-lookup"><span data-stu-id="94798-113">Example 1</span></span>

<span data-ttu-id="94798-114">Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `ISEMPTY(DS)` väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="94798-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="94798-115">Näide 2</span><span class="sxs-lookup"><span data-stu-id="94798-115">Example 2</span></span>

<span data-ttu-id="94798-116">Avaldis `ISEMPTY (SPLIT ("",1))` tagastab väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="94798-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94798-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="94798-117">Additional resources</span></span>

[<span data-ttu-id="94798-118">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="94798-118">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]