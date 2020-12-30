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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dbba375104b57f9fb09ed4e330d85181ec0dff8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684879"
---
# <a name="isempty-er-function"></a><span data-ttu-id="fb949-103">ER-i funktsioon ISEMPTY</span><span class="sxs-lookup"><span data-stu-id="fb949-103">ISEMPTY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb949-104">Kui määratud loend ei sisalda ühtegi kirjet, tagastab funktsioon `ISEMPTY` *kahendmuutuja* väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="fb949-104">The `ISEMPTY` function returns a *Boolean* value of **TRUE** if the specified list contains no records.</span></span> <span data-ttu-id="fb949-105">Muidu tagastab see *kahendväärtuse* **VÄÄR**.</span><span class="sxs-lookup"><span data-stu-id="fb949-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb949-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="fb949-106">Syntax</span></span>

```vb
ISEMPTY (list)
```

## <a name="arguments"></a><span data-ttu-id="fb949-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="fb949-107">Arguments</span></span>

<span data-ttu-id="fb949-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="fb949-108">`list`: *Record list*</span></span>

<span data-ttu-id="fb949-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="fb949-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="fb949-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="fb949-110">Return values</span></span>

<span data-ttu-id="fb949-111">*Kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="fb949-111">*Boolean*</span></span>

<span data-ttu-id="fb949-112">Tulemiks saadud *kahendmuutuja* väärtus.</span><span class="sxs-lookup"><span data-stu-id="fb949-112">The resulting *Boolean* value.</span></span>

## <a name="example-1"></a><span data-ttu-id="fb949-113">Näide 1</span><span class="sxs-lookup"><span data-stu-id="fb949-113">Example 1</span></span>

<span data-ttu-id="fb949-114">Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `ISEMPTY(DS)` väärtuse **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="fb949-114">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `ISEMPTY(DS)` returns **FALSE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="fb949-115">Näide 2</span><span class="sxs-lookup"><span data-stu-id="fb949-115">Example 2</span></span>

<span data-ttu-id="fb949-116">Avaldis `ISEMPTY (SPLIT ("",1))` tagastab väärtuse **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="fb949-116">The expression `ISEMPTY (SPLIT ("",1))` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fb949-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fb949-117">Additional resources</span></span>

[<span data-ttu-id="fb949-118">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="fb949-118">List functions</span></span>](er-functions-category-list.md)
