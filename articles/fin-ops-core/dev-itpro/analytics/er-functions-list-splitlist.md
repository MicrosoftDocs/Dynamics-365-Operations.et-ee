---
title: ER-i funktsioon SPLITLIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLITLIST.
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
ms.openlocfilehash: b324d42a53b35074ba62ccf3df7b77cb4db70450
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917208"
---
# <span data-ttu-id="ffe79-103"><a name="SPLITLIST">ER-i funktsioon SPLITLIST</a></span><span class="sxs-lookup"><span data-stu-id="ffe79-103"><a name="SPLITLIST">SPLITLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffe79-104">Funktsioon `SPLITLIST` jaotab määratud loendi alamloenditeks (või partiideks), millest igaüks sisaldab määratud kirjete arvu.</span><span class="sxs-lookup"><span data-stu-id="ffe79-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="ffe79-105">See tagastab seejärel tulemuse uue *kirjete loendi* väärtusena, mis koosneb partiidest.</span><span class="sxs-lookup"><span data-stu-id="ffe79-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffe79-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="ffe79-106">Syntax</span></span>

```
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="ffe79-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="ffe79-107">Arguments</span></span>

<span data-ttu-id="ffe79-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="ffe79-108">`list`: *Record list*</span></span>

<span data-ttu-id="ffe79-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="ffe79-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="ffe79-110">`number`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="ffe79-110">`number`: *Integer*</span></span>

<span data-ttu-id="ffe79-111">Maksimaalne kirjete arv partii kohta.</span><span class="sxs-lookup"><span data-stu-id="ffe79-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="ffe79-112">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="ffe79-112">Return values</span></span>

<span data-ttu-id="ffe79-113">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="ffe79-113">*Record list*</span></span>

<span data-ttu-id="ffe79-114">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="ffe79-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ffe79-115">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="ffe79-115">Usage notes</span></span>

<span data-ttu-id="ffe79-116">Tagastatav partiide loend sisaldab järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="ffe79-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="ffe79-117">**Väärtus:** *loend*</span><span class="sxs-lookup"><span data-stu-id="ffe79-117">**Value:** *List*</span></span>

    <span data-ttu-id="ffe79-118">Kirjete loend, mis kuuluvad praegusesse partiisse.</span><span class="sxs-lookup"><span data-stu-id="ffe79-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="ffe79-119">**BatchNumber:** *täisarv*</span><span class="sxs-lookup"><span data-stu-id="ffe79-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="ffe79-120">Praeguse partii number tagastatud loendis.</span><span class="sxs-lookup"><span data-stu-id="ffe79-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="ffe79-121">Näide</span><span class="sxs-lookup"><span data-stu-id="ffe79-121">Example</span></span>

<span data-ttu-id="ffe79-122">Järgmisel joonisel luuakse andmeallikas **Read** kolme kirjet omava kirjete loendina.</span><span class="sxs-lookup"><span data-stu-id="ffe79-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="ffe79-123">See loend on jaotatud partiideks, millest igaüks sisaldab kuni kahte kirjet.</span><span class="sxs-lookup"><span data-stu-id="ffe79-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="ffe79-124">Järgmisel joonisel on näidatud koostatud vormingu paigutus.</span><span class="sxs-lookup"><span data-stu-id="ffe79-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="ffe79-125">Selles vormi paigutuses luuakse andmeallika **Read** sidemed, et luua XML-vormingus väljund.</span><span class="sxs-lookup"><span data-stu-id="ffe79-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="ffe79-126">See väljund esitab üksikuid sõlmi igale partiile ja selles olevale kirjele.</span><span class="sxs-lookup"><span data-stu-id="ffe79-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="ffe79-127">Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.</span><span class="sxs-lookup"><span data-stu-id="ffe79-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="ffe79-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ffe79-128">Additional resources</span></span>

[<span data-ttu-id="ffe79-129">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="ffe79-129">List functions</span></span>](er-functions-category-list.md)