---
title: ER-i funktsioon INDEX
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni INDEX.
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
ms.openlocfilehash: 45e95751e3adfe6aa208daaba774a349216e1f1f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042063"
---
# <span data-ttu-id="ac21f-103"><a name="INDEX">ER-i funktsioon INDEX</a></span><span class="sxs-lookup"><span data-stu-id="ac21f-103"><a name="INDEX">INDEX ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac21f-104">Funktsioon `INDEX` tagastab *konteineri (kirje)* väärtuse, mis on valitud määratud numbrilise indeksi abil määratud loendis.</span><span class="sxs-lookup"><span data-stu-id="ac21f-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="ac21f-105">Kui indeks on määratud loendis olevate kirjete vahemikust väljas, tehakse erand.</span><span class="sxs-lookup"><span data-stu-id="ac21f-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac21f-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="ac21f-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="ac21f-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="ac21f-107">Arguments</span></span>

<span data-ttu-id="ac21f-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="ac21f-108">`list`: *Record list*</span></span>

<span data-ttu-id="ac21f-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="ac21f-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="ac21f-110">`index`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="ac21f-110">`index`: *Integer*</span></span>

<span data-ttu-id="ac21f-111">Numbriline indeks, mis näitab soovitud kirje asukohta määratud loendis.</span><span class="sxs-lookup"><span data-stu-id="ac21f-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="ac21f-112">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="ac21f-112">Return values</span></span>

<span data-ttu-id="ac21f-113">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="ac21f-113">*Container (record)*</span></span>

<span data-ttu-id="ac21f-114">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="ac21f-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="ac21f-115">Näide 1</span><span class="sxs-lookup"><span data-stu-id="ac21f-115">Example 1</span></span>

<span data-ttu-id="ac21f-116">Kui sisestate andmeallika **DS** tüübile *Arvutatud väli* ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `DS.Value` selle kirjete loendi teisele kirjele teksti väärtuse **„B”**.</span><span class="sxs-lookup"><span data-stu-id="ac21f-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="ac21f-117">Avaldis `INDEX (SPLIT ("A|B|C", "|"), 2).Value` tagastab samuti tekstiväärtuse **„B”**.</span><span class="sxs-lookup"><span data-stu-id="ac21f-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ac21f-118">Näide 2</span><span class="sxs-lookup"><span data-stu-id="ac21f-118">Example 2</span></span>

<span data-ttu-id="ac21f-119">Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `INDEX (SPLIT ("A|B|C", "|"), 4).Value` käitusajal erandi.</span><span class="sxs-lookup"><span data-stu-id="ac21f-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac21f-120">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ac21f-120">Additional resources</span></span>

[<span data-ttu-id="ac21f-121">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="ac21f-121">List functions</span></span>](er-functions-category-list.md)
