---
title: ER-i funktsioon COUNT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni COUNT.
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
ms.openlocfilehash: 2d29b82a8c3b108f7651e6d593cb17e7ec8ca872
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916242"
---
# <span data-ttu-id="0d712-103"><a name="COUNT">ER-i funktsioon COUNT</a></span><span class="sxs-lookup"><span data-stu-id="0d712-103"><a name="COUNT">COUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d712-104">Funktsioon `COUNT` tagastab *täisarvu* väärtuse, mis tähistab kirjete arvu määratud loendis, kui loend pole tühi.</span><span class="sxs-lookup"><span data-stu-id="0d712-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="0d712-105">Kui loend on tühi, tagastab funktsioon väärtuse **0** (null).</span><span class="sxs-lookup"><span data-stu-id="0d712-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d712-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="0d712-106">Syntax</span></span>

```
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="0d712-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="0d712-107">Arguments</span></span>

<span data-ttu-id="0d712-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="0d712-108">`list`: *Record list*</span></span>

<span data-ttu-id="0d712-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="0d712-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="0d712-110">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="0d712-110">Return values</span></span>

<span data-ttu-id="0d712-111">*Täisarv*</span><span class="sxs-lookup"><span data-stu-id="0d712-111">*Integer*</span></span>

<span data-ttu-id="0d712-112">Tulemiks saadud numbriline väärtus.</span><span class="sxs-lookup"><span data-stu-id="0d712-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="0d712-113">Näide</span><span class="sxs-lookup"><span data-stu-id="0d712-113">Example</span></span>

<span data-ttu-id="0d712-114">`COUNT (SPLIT("abcd" , 3))` tagastab väärtuse **2**, kuna funktsioon `SPLIT`, mida selles näites kasutatakse, loob loendi, mis koosneb kahest kirjest.</span><span class="sxs-lookup"><span data-stu-id="0d712-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d712-115">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0d712-115">Additional resources</span></span>

[<span data-ttu-id="0d712-116">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="0d712-116">List functions</span></span>](er-functions-category-list.md)
