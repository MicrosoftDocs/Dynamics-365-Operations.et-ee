---
title: ER-i funktsioon SPLITLIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLITLIST.
author: NickSelin
ms.date: 03/15/2021
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
ms.openlocfilehash: 99e199e238b3132622a8b305895637b430e8f6d2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745565"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="22f98-103">ER-i funktsioon SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="22f98-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22f98-104">Funktsioon `SPLITLIST` jaotab määratud loendi alamloenditeks (või partiideks), millest igaüks sisaldab määratud kirjete arvu.</span><span class="sxs-lookup"><span data-stu-id="22f98-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="22f98-105">See tagastab seejärel tulemuse uue *kirjete loendi* väärtusena, mis koosneb partiidest.</span><span class="sxs-lookup"><span data-stu-id="22f98-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="22f98-106">Süntaks 1</span><span class="sxs-lookup"><span data-stu-id="22f98-106">Syntax 1</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="syntax-2"></a><span data-ttu-id="22f98-107">Süntaks 2</span><span class="sxs-lookup"><span data-stu-id="22f98-107">Syntax 2</span></span>

```vb
SPLITLIST (list, number, on-demand reading flag)
```

## <a name="arguments"></a><span data-ttu-id="22f98-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="22f98-108">Arguments</span></span>

<span data-ttu-id="22f98-109">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="22f98-109">`list`: *Record list*</span></span>

<span data-ttu-id="22f98-110">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="22f98-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="22f98-111">`number`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="22f98-111">`number`: *Integer*</span></span>

<span data-ttu-id="22f98-112">Maksimaalne kirjete arv partii kohta.</span><span class="sxs-lookup"><span data-stu-id="22f98-112">The maximum number of records per batch.</span></span>

<span data-ttu-id="22f98-113">`on-demand reading flag`: *kahendmuutuja*</span><span class="sxs-lookup"><span data-stu-id="22f98-113">`on-demand reading flag`: *Boolean*</span></span>

<span data-ttu-id="22f98-114">*Loogiline* väärtus, mis täpsustab, kas alamloendi elemendid peaksid olema loodud nõudmisel.</span><span class="sxs-lookup"><span data-stu-id="22f98-114">A *Boolean* value that specifies whether elements of sublists should be generated on demand.</span></span>

## <a name="return-values"></a><span data-ttu-id="22f98-115">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="22f98-115">Return values</span></span>

<span data-ttu-id="22f98-116">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="22f98-116">*Record list*</span></span>

<span data-ttu-id="22f98-117">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="22f98-117">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="22f98-118">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="22f98-118">Usage notes</span></span>

<span data-ttu-id="22f98-119">Tagastatav partiide loend sisaldab järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="22f98-119">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="22f98-120">**Väärtus:** *loend*</span><span class="sxs-lookup"><span data-stu-id="22f98-120">**Value:** *List*</span></span>

    <span data-ttu-id="22f98-121">Kirjete loend, mis kuuluvad praegusesse partiisse.</span><span class="sxs-lookup"><span data-stu-id="22f98-121">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="22f98-122">**BatchNumber:** *täisarv*</span><span class="sxs-lookup"><span data-stu-id="22f98-122">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="22f98-123">Praeguse partii number tagastatud loendis.</span><span class="sxs-lookup"><span data-stu-id="22f98-123">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="22f98-124">Kui nõudmisel lugemise lipp on seatud väärtusele **Tõene**, luuakse taotluse korral alamloendid, mis võimaldab mälutarbimise vähendamist, kuid võib põhjustada jõudluse hõivamise, kui elemente ei kasutata järjestikku.</span><span class="sxs-lookup"><span data-stu-id="22f98-124">When the on-demand reading flag is set to **True**, sublists are generated upon request which allows for a reduction in memory consumption but may cause performance degradation if elements aren't used sequentially.</span></span>

## <a name="example"></a><span data-ttu-id="22f98-125">Näide</span><span class="sxs-lookup"><span data-stu-id="22f98-125">Example</span></span>

<span data-ttu-id="22f98-126">Järgmisel joonisel luuakse andmeallikas **Read** kolme kirjet omava kirjete loendina.</span><span class="sxs-lookup"><span data-stu-id="22f98-126">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="22f98-127">See loend on jaotatud partiideks, millest igaüks sisaldab kuni kahte kirjet.</span><span class="sxs-lookup"><span data-stu-id="22f98-127">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="22f98-128">Järgmisel joonisel on näidatud koostatud vormingu paigutus.</span><span class="sxs-lookup"><span data-stu-id="22f98-128">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="22f98-129">Selles vormi paigutuses luuakse andmeallika **Read** sidemed, et luua XML-vormingus väljund.</span><span class="sxs-lookup"><span data-stu-id="22f98-129">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="22f98-130">See väljund esitab üksikuid sõlmi igale partiile ja selles olevale kirjele.</span><span class="sxs-lookup"><span data-stu-id="22f98-130">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="22f98-131">Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.</span><span class="sxs-lookup"><span data-stu-id="22f98-131">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="22f98-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="22f98-132">Additional resources</span></span>

[<span data-ttu-id="22f98-133">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="22f98-133">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
