---
title: ER-i funktsioon EMPTYLIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni EMPTYLIST.
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
ms.openlocfilehash: a60bc948ff6223b6e3acccd0ba40bf64f238aac2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917392"
---
# <span data-ttu-id="72049-103"><a name="EMPTYLIST">ER-i funktsioon EMPTYLIST</a></span><span class="sxs-lookup"><span data-stu-id="72049-103"><a name="EMPTYLIST">EMPTYLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72049-104">Funktsioon `EMPTYLIST` tagastab tühja *kirjete loendi* väärtuse, kasutades loendi struktuuri allikana määratud loendit.</span><span class="sxs-lookup"><span data-stu-id="72049-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="72049-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="72049-105">Syntax</span></span>

```
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="72049-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="72049-106">Arguments</span></span>

<span data-ttu-id="72049-107">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="72049-107">`list`: *Record list*</span></span>

<span data-ttu-id="72049-108">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="72049-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="72049-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="72049-109">Return values</span></span>

<span data-ttu-id="72049-110">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="72049-110">*Record list*</span></span>

<span data-ttu-id="72049-111">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="72049-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="72049-112">Näide</span><span class="sxs-lookup"><span data-stu-id="72049-112">Example</span></span>

<span data-ttu-id="72049-113">`EMPTYLIST (SPLIT ("abc", 1))` tagastab uue tühja loendi, millel on sama struktuur nagu loendil, mille annab vastuseks funktsioon `SPLIT`, mida kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="72049-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72049-114">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="72049-114">Additional resources</span></span>

[<span data-ttu-id="72049-115">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="72049-115">List functions</span></span>](er-functions-category-list.md)
