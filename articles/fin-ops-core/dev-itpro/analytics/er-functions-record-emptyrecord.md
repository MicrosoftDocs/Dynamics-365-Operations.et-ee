---
title: ER-i funktsioon EMPTYRECORD
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni EMPTYRECORD.
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
ms.openlocfilehash: 1cf23f11fa92adfb7a050efd9c68e80e1bee621f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916886"
---
# <span data-ttu-id="c7fb4-103"><a name="EMPTYRECORD">ER-i funktsioon EMPTYRECORD</a></span><span class="sxs-lookup"><span data-stu-id="c7fb4-103"><a name="EMPTYRECORD">EMPTYRECORD ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7fb4-104">Funktsioon `EMPTYRECORD` tagastab *konteineri (kirje)* väärtuse null, millel on sama struktuur, kui määratud kirjete loendil või kirjel.</span><span class="sxs-lookup"><span data-stu-id="c7fb4-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7fb4-105">Süntaks</span><span class="sxs-lookup"><span data-stu-id="c7fb4-105">Syntax</span></span>

```
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="c7fb4-106">Argumendid</span><span class="sxs-lookup"><span data-stu-id="c7fb4-106">Arguments</span></span>

<span data-ttu-id="c7fb4-107">`list`: *kirjete loend* või *konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="c7fb4-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="c7fb4-108">Tüübi *Kirjete loend* või *Konteiner (kirje)* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="c7fb4-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="c7fb4-109">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="c7fb4-109">Return values</span></span>

<span data-ttu-id="c7fb4-110">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="c7fb4-110">*Container (record)*</span></span>

<span data-ttu-id="c7fb4-111">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="c7fb4-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c7fb4-112">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="c7fb4-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="c7fb4-113">Nullkirje on kirje, mille kõikidel väljadel on tühi väärtus.</span><span class="sxs-lookup"><span data-stu-id="c7fb4-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="c7fb4-114">Tühi väärtus on arvude puhul **0** (null), stringide puhul tühi string jne.</span><span class="sxs-lookup"><span data-stu-id="c7fb4-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="c7fb4-115">Näide</span><span class="sxs-lookup"><span data-stu-id="c7fb4-115">Example</span></span>

<span data-ttu-id="c7fb4-116">`EMPTYRECORD (SPLIT ("abc", 1))` tagastab uue tühja kirje, millel on sama struktuur nagu loendil, mille annab vastuseks funktsioon `SPLIT`.</span><span class="sxs-lookup"><span data-stu-id="c7fb4-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="c7fb4-117">Lisateavet vt [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="c7fb4-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c7fb4-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c7fb4-118">Additional resources</span></span>

[<span data-ttu-id="c7fb4-119">Kirje funktsioonid</span><span class="sxs-lookup"><span data-stu-id="c7fb4-119">Record functions</span></span>](er-functions-category-record.md)