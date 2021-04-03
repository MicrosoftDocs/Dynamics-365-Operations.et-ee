---
title: ER-i funktsioon SPLITLIST
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLITLIST.
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
ms.openlocfilehash: af8c413726ca8d9f92eff18807e7fa9002fc9d37
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559134"
---
# <a name="splitlist-er-function"></a><span data-ttu-id="ebc35-103">ER-i funktsioon SPLITLIST</span><span class="sxs-lookup"><span data-stu-id="ebc35-103">SPLITLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ebc35-104">Funktsioon `SPLITLIST` jaotab määratud loendi alamloenditeks (või partiideks), millest igaüks sisaldab määratud kirjete arvu.</span><span class="sxs-lookup"><span data-stu-id="ebc35-104">The `SPLITLIST` function splits the specified list into sublists (or batches), each of which contains the specified number of records.</span></span> <span data-ttu-id="ebc35-105">See tagastab seejärel tulemuse uue *kirjete loendi* väärtusena, mis koosneb partiidest.</span><span class="sxs-lookup"><span data-stu-id="ebc35-105">It then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc35-106">Süntaks</span><span class="sxs-lookup"><span data-stu-id="ebc35-106">Syntax</span></span>

```vb
SPLITLIST (list, number)
```

## <a name="arguments"></a><span data-ttu-id="ebc35-107">Argumendid</span><span class="sxs-lookup"><span data-stu-id="ebc35-107">Arguments</span></span>

<span data-ttu-id="ebc35-108">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="ebc35-108">`list`: *Record list*</span></span>

<span data-ttu-id="ebc35-109">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="ebc35-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="ebc35-110">`number`: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="ebc35-110">`number`: *Integer*</span></span>

<span data-ttu-id="ebc35-111">Maksimaalne kirjete arv partii kohta.</span><span class="sxs-lookup"><span data-stu-id="ebc35-111">The maximum number of records per batch.</span></span>

## <a name="return-values"></a><span data-ttu-id="ebc35-112">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="ebc35-112">Return values</span></span>

<span data-ttu-id="ebc35-113">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="ebc35-113">*Record list*</span></span>

<span data-ttu-id="ebc35-114">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="ebc35-114">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ebc35-115">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="ebc35-115">Usage notes</span></span>

<span data-ttu-id="ebc35-116">Tagastatav partiide loend sisaldab järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="ebc35-116">The list of batches that is returned contains the following elements:</span></span>

 - <span data-ttu-id="ebc35-117">**Väärtus:** *loend*</span><span class="sxs-lookup"><span data-stu-id="ebc35-117">**Value:** *List*</span></span>

    <span data-ttu-id="ebc35-118">Kirjete loend, mis kuuluvad praegusesse partiisse.</span><span class="sxs-lookup"><span data-stu-id="ebc35-118">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="ebc35-119">**BatchNumber:** *täisarv*</span><span class="sxs-lookup"><span data-stu-id="ebc35-119">**BatchNumber:** *Integer*</span></span>

    <span data-ttu-id="ebc35-120">Praeguse partii number tagastatud loendis.</span><span class="sxs-lookup"><span data-stu-id="ebc35-120">The number of the current batch in the returned list.</span></span>

## <a name="example"></a><span data-ttu-id="ebc35-121">Näide</span><span class="sxs-lookup"><span data-stu-id="ebc35-121">Example</span></span>

<span data-ttu-id="ebc35-122">Järgmisel joonisel luuakse andmeallikas **Read** kolme kirjet omava kirjete loendina.</span><span class="sxs-lookup"><span data-stu-id="ebc35-122">In the following illustration, a **Lines** data source is created as a record list that has three records.</span></span> <span data-ttu-id="ebc35-123">See loend on jaotatud partiideks, millest igaüks sisaldab kuni kahte kirjet.</span><span class="sxs-lookup"><span data-stu-id="ebc35-123">This list is divided into batches, each of which contains up to two records.</span></span>

<a href="./media/picture-splitlist-datasource.jpg"><img src="./media/picture-splitlist-datasource.jpg" alt="Data source that is divided into batches" class="alignnone wp-image-290681 size-full" width="397" height="136" /></a>

<span data-ttu-id="ebc35-124">Järgmisel joonisel on näidatud koostatud vormingu paigutus.</span><span class="sxs-lookup"><span data-stu-id="ebc35-124">The following illustration shows the designed format layout.</span></span> <span data-ttu-id="ebc35-125">Selles vormi paigutuses luuakse andmeallika **Read** sidemed, et luua XML-vormingus väljund.</span><span class="sxs-lookup"><span data-stu-id="ebc35-125">In this format layout, bindings to the **Lines** data source are created to generate output in XML format.</span></span> <span data-ttu-id="ebc35-126">See väljund esitab üksikuid sõlmi igale partiile ja selles olevale kirjele.</span><span class="sxs-lookup"><span data-stu-id="ebc35-126">This output presents individual nodes for each batch and the records in it.</span></span>

<a href="./media/picture-splitlist-format.jpg"><img src="./media/picture-splitlist-format.jpg" alt="Format layout that has bindings to a data source" class="alignnone wp-image-290691 size-full" width="374" height="161" /></a>

<span data-ttu-id="ebc35-127">Järgmisel joonisel on näidatud koostatud vormingu käitamise tulemus.</span><span class="sxs-lookup"><span data-stu-id="ebc35-127">The following illustration shows the result when the designed format is run.</span></span>

<a href="./media/picture-splitlist-result.jpg"><img src="./media/picture-splitlist-result.jpg" alt="Result of running the format" class="alignnone wp-image-290701 size-full" width="358" height="191" /></a>

## <a name="additional-resources"></a><span data-ttu-id="ebc35-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ebc35-128">Additional resources</span></span>

[<span data-ttu-id="ebc35-129">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="ebc35-129">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]