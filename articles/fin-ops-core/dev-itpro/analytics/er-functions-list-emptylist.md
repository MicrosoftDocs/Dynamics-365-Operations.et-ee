---
title: ER-i funktsioon EMPTYLIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni EMPTYLIST.
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
ms.openlocfilehash: f6c2777065656affc992a427194286008c1df42f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559196"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="7f575-103">ER-i funktsioon EMPTYLIST</span><span class="sxs-lookup"><span data-stu-id="7f575-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7f575-104">Funktsioon `EMPTYLIST` tagastab tühja *kirjete loendi* väärtuse, kasutades loendi struktuuri allikana määratud loendit.</span><span class="sxs-lookup"><span data-stu-id="7f575-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f575-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="7f575-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="7f575-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="7f575-106">Arguments</span></span>

<span data-ttu-id="7f575-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="7f575-107">`list`: *Record list*</span></span>

<span data-ttu-id="7f575-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="7f575-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="7f575-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="7f575-109">Return values</span></span>

<span data-ttu-id="7f575-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="7f575-110">*Record list*</span></span>

<span data-ttu-id="7f575-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="7f575-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="7f575-112">Näide</span><span class="sxs-lookup"><span data-stu-id="7f575-112">Example</span></span>

<span data-ttu-id="7f575-113">`EMPTYLIST (SPLIT ("abc", 1))` tagastab uue tühja loendi, millel on sama struktuur nagu loendil, mille annab vastuseks funktsioon `SPLIT`, mida kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="7f575-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7f575-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7f575-114">Additional resources</span></span>

[<span data-ttu-id="7f575-115">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="7f575-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]