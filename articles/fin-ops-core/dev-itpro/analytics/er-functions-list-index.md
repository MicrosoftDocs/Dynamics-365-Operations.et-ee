---
title: ER-i funktsioon INDEX
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni INDEX.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087747"
---
# <a name="index-er-function"></a><span data-ttu-id="e9405-103">ER-i funktsioon INDEX</span><span class="sxs-lookup"><span data-stu-id="e9405-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9405-104">Funktsioon `INDEX` tagastab *konteineri (kirje)* väärtuse, mis on valitud määratud numbrilise indeksi abil määratud loendis.</span><span class="sxs-lookup"><span data-stu-id="e9405-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="e9405-105">Kui indeks on määratud loendis olevate kirjete vahemikust väljas, tehakse erand.</span><span class="sxs-lookup"><span data-stu-id="e9405-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9405-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="e9405-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="e9405-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="e9405-107">Arguments</span></span>

<span data-ttu-id="e9405-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="e9405-108">`list`: *Record list*</span></span>

<span data-ttu-id="e9405-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="e9405-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="e9405-110">`index`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="e9405-110">`index`: *Integer*</span></span>

<span data-ttu-id="e9405-111">Numbriline indeks, mis näitab soovitud kirje asukohta määratud loendis.</span><span class="sxs-lookup"><span data-stu-id="e9405-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

> [!NOTE]
> <span data-ttu-id="e9405-112">Kuna selle funktsiooni puhul kasutatakse ühe põhinumbrit, määrake määratud loendi esimese kirje tagastamiseks väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="e9405-112">Because one-based numbering is used for this function, specify the value **1** to return the first record of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="e9405-113">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="e9405-113">Return values</span></span>

<span data-ttu-id="e9405-114">*Konteiner (kirje)*</span><span class="sxs-lookup"><span data-stu-id="e9405-114">*Container (record)*</span></span>

<span data-ttu-id="e9405-115">Tulemuseks olev kirje väärtus.</span><span class="sxs-lookup"><span data-stu-id="e9405-115">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="e9405-116">Näide 1</span><span class="sxs-lookup"><span data-stu-id="e9405-116">Example 1</span></span>

<span data-ttu-id="e9405-117">Kui sisestate andmeallika **DS** tüübile *Arvutatud väli* ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `DS.Value` selle kirjete loendi teisele kirjele teksti väärtuse **„B”**.</span><span class="sxs-lookup"><span data-stu-id="e9405-117">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="e9405-118">Avaldis `INDEX (SPLIT ("A|B|C", "|"), 2).Value` tagastab samuti tekstiväärtuse **„B”**.</span><span class="sxs-lookup"><span data-stu-id="e9405-118">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="e9405-119">Näide 2</span><span class="sxs-lookup"><span data-stu-id="e9405-119">Example 2</span></span>

<span data-ttu-id="e9405-120">Kui sisestate tüübi *Arvutatud väli* andmeallika **DS** ja see sisaldab avaldist `SPLIT ("A|B|C", "|")`, tagastab avaldis `INDEX (SPLIT ("A|B|C", "|"), 4).Value` käitusajal erandi.</span><span class="sxs-lookup"><span data-stu-id="e9405-120">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9405-121">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e9405-121">Additional resources</span></span>

[<span data-ttu-id="e9405-122">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="e9405-122">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
