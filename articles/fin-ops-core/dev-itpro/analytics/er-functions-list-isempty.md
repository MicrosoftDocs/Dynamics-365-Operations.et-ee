---
title: ER-i funktsioon ISEMPTY
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni ISEMPTY.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: c8450c17fe2de964016951197b0d4e231c550a99
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916127"
---
# <span data-ttu-id="80deb-103"><a name="ISEMPTY">ER-i funktsioon ISEMPTY</a></span><span class="sxs-lookup"><span data-stu-id="80deb-103"><a name="ISEMPTY">ISEMPTY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80deb-104">Kui määratud loend ei sisalda ühtegi kirjet, tagastab funktsioon `ISEMPTY` *kahendmuutuja* väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="80deb-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="80deb-105">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="80deb-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="80deb-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="80deb-106">Syntax</span></span>

```
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="80deb-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="80deb-107">Arguments</span></span>

<span data-ttu-id="80deb-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="80deb-108">`list`: *Record list*</span></span>

<span data-ttu-id="80deb-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="80deb-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="80deb-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="80deb-110">Return values</span></span>

<span data-ttu-id="80deb-111">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="80deb-111">*Boolean*</span></span>

<span data-ttu-id="80deb-112">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="80deb-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="80deb-113">Näide 1</span><span class="sxs-lookup"><span data-stu-id="80deb-113">Example 1</span></span>

<span data-ttu-id="80deb-114">Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `ISEMPTY(DS)` väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="80deb-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="80deb-115">Näide 2</span><span class="sxs-lookup"><span data-stu-id="80deb-115">Example 2</span></span>

<span data-ttu-id="80deb-116">Avaldis `ISEMPTY (SPLIT ("",1))` tagastab väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="80deb-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80deb-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="80deb-117">Additional resources</span></span>

[<span data-ttu-id="80deb-118">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="80deb-118">List functions</span></span>](er-functions-category-list.md)
