---
title: ER-i funktsioon SPLITLISTBYLIMIT
description: See teema sisaldab teavet selle kohta, kuidas kasutatakse elektroonilise aruandluse (ER) funktsiooni SPLITLISTBYLIMIT.
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
ms.openlocfilehash: 54c78f36c93e1bdb472b84fc7ca6428d20088bad
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041856"
---
# <span data-ttu-id="08ded-103"><a name="SPLITLISTBYLIMIT">ER-i funktsioon SPLITLISTBYLIMIT</a></span><span class="sxs-lookup"><span data-stu-id="08ded-103"><a name="SPLITLISTBYLIMIT">SPLITLISTBYLIMIT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08ded-104">Funktsioon `SPLITLISTBYLIMIT` jaotab määratud loendi alamloendite (partiide) uueks loendiks.</span><span class="sxs-lookup"><span data-stu-id="08ded-104">The `SPLITLISTBYLIMIT` function splits the specified list into a new list of sublists (batches).</span></span> <span data-ttu-id="08ded-105">Iga partii kirjete arv arvutatakse dünaamiliselt.</span><span class="sxs-lookup"><span data-stu-id="08ded-105">The number of records in each batch is dynamically calculated.</span></span> <span data-ttu-id="08ded-106">Funktsioon tagastab tulemuse uue *kirjete loendi* väärtusena, mis koosneb partiidest.</span><span class="sxs-lookup"><span data-stu-id="08ded-106">The function then returns the result as a new *Record list* value that consists of the batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="08ded-107">Süntaks</span><span class="sxs-lookup"><span data-stu-id="08ded-107">Syntax</span></span>

```vb
SPLITLISTBYLIMIT (list, limit value, limit source)
```

## <a name="arguments"></a><span data-ttu-id="08ded-108">Argumendid</span><span class="sxs-lookup"><span data-stu-id="08ded-108">Arguments</span></span>

<span data-ttu-id="08ded-109">`list`: *kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="08ded-109">`list`: *Record list*</span></span>

<span data-ttu-id="08ded-110">Andmetüübi *Kirjete loend* andmeallika kehtiv tee.</span><span class="sxs-lookup"><span data-stu-id="08ded-110">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="08ded-111">`limit value`: *täisarv* või *tegelik*</span><span class="sxs-lookup"><span data-stu-id="08ded-111">`limit value`: *Integer* or *Real*</span></span>

<span data-ttu-id="08ded-112">Piirangu maksimaalne väärtus, mida kasutatakse algse loendi partiideks tükeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="08ded-112">The maximum value of the limit that is used to split the original list into batches.</span></span>

<span data-ttu-id="08ded-113">`limit source`: *väli*</span><span class="sxs-lookup"><span data-stu-id="08ded-113">`limit source`: *Field*</span></span>

<span data-ttu-id="08ded-114">Tüübi *Täisarv* või *Tegelik* välja kehtiv tee määratud loendis.</span><span class="sxs-lookup"><span data-stu-id="08ded-114">The valid path of a field of the *Integer* or *Real* type in the specified list.</span></span> <span data-ttu-id="08ded-115">Selle välja väärtus määratleb sammu, millal kogusummat suurendatakse.</span><span class="sxs-lookup"><span data-stu-id="08ded-115">The value of this field defines the step that the total sum is increased on.</span></span>

## <a name="return-values"></a><span data-ttu-id="08ded-116">Tagastusväärtused</span><span class="sxs-lookup"><span data-stu-id="08ded-116">Return values</span></span>

<span data-ttu-id="08ded-117">*Kirjete loend*</span><span class="sxs-lookup"><span data-stu-id="08ded-117">*Record list*</span></span>

<span data-ttu-id="08ded-118">Saadud kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="08ded-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="08ded-119">Kasutamise märkused</span><span class="sxs-lookup"><span data-stu-id="08ded-119">Usage notes</span></span>

<span data-ttu-id="08ded-120">Tagastatav partiide loend sisaldab järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="08ded-120">The list of batches that is returned contains the following elements:</span></span>

- <span data-ttu-id="08ded-121">**Väärtus**: *loend*</span><span class="sxs-lookup"><span data-stu-id="08ded-121">**Value**: *List*</span></span>

    <span data-ttu-id="08ded-122">Kirjete loend, mis kuuluvad praegusesse partiisse.</span><span class="sxs-lookup"><span data-stu-id="08ded-122">The list of records that belong to the current batch.</span></span>

- <span data-ttu-id="08ded-123">**BatchNumber**: *täisarv*</span><span class="sxs-lookup"><span data-stu-id="08ded-123">**BatchNumber**: *Integer*</span></span>

    <span data-ttu-id="08ded-124">Praeguse partii number tagastatud loendis.</span><span class="sxs-lookup"><span data-stu-id="08ded-124">The number of the current batch in the returned list.</span></span>

<span data-ttu-id="08ded-125">Piirangut ei rakendata algse loendi üksikule üksusele, kui piirallikas ületab määratud piirangut.</span><span class="sxs-lookup"><span data-stu-id="08ded-125">The limit isn't applied to a single item of the original list if the limit source exceeds the defined limit.</span></span>

## <a name="example"></a><span data-ttu-id="08ded-126">Näide</span><span class="sxs-lookup"><span data-stu-id="08ded-126">Example</span></span>

<span data-ttu-id="08ded-127">Järgmine joonis näitab elektroonilise aruandluse (ER) vormingut.</span><span class="sxs-lookup"><span data-stu-id="08ded-127">The following illustration shows an Electronic reporting (ER) format.</span></span>

<a href="./media/ger-splitlistbylimit-format.png"><img src="./media/ger-splitlistbylimit-format.png" alt="Format" class="alignnone size-full wp-image-1204063" width="396" height="195" /></a>

<span data-ttu-id="08ded-128">Järgmisel joonisel on näidatud vormingu puhul kasutatud andmeallikad.</span><span class="sxs-lookup"><span data-stu-id="08ded-128">The following illustration shows the data sources that are used for the format.</span></span>

<a href="./media/ger-splitlistbylimit-datasources.png"><img src="./media/ger-splitlistbylimit-datasources.png" alt="Data sources" class="alignnone size-full wp-image-1204073" width="320" height="208" /></a>

<span data-ttu-id="08ded-129">Järgmisel joonisel on näidatud vormingu käitamise tulemus.</span><span class="sxs-lookup"><span data-stu-id="08ded-129">The following illustration shows the result when the format is run.</span></span> <span data-ttu-id="08ded-130">Sel juhul on väljund tarbekaupade lame loend.</span><span class="sxs-lookup"><span data-stu-id="08ded-130">In this case, the output is a flat list of commodity items.</span></span>

<a href="./media/ger-splitlistbylimit-output.png"><img src="./media/ger-splitlistbylimit-output.png" alt="Output" class="alignnone size-full wp-image-1204083" width="462" height="204" /></a>

<span data-ttu-id="08ded-131">Järgmistes näidetes on sama vormingut kohandatud nii, et see esitab tarbekaupade loendi partiidena, kui üksik partii peab sisaldama tarbekaupu ja kogukaal ei tohi ületada piirangut 9.</span><span class="sxs-lookup"><span data-stu-id="08ded-131">In the following illustrations, the same format has been adjusted so that it presents the list of commodity items in batches if a single batch must include commodities and the total weight should not exceed a limit of 9.</span></span>

<a href="./media/ger-splitlistbylimit-format-1.png"><img src="./media/ger-splitlistbylimit-format-1.png" alt="Adjusted format" class="alignnone size-full wp-image-1204103" width="466" height="438" /></a>

<a href="./media/ger-splitlistbylimit-datasources-1.png"><img src="./media/ger-splitlistbylimit-datasources-1.png" alt="Data sources for the adjusted format" class="alignnone size-full wp-image-1204093" width="645" height="507" /></a>

<span data-ttu-id="08ded-132">Järgmisel joonisel on näidatud kohandatud vormingu käitamise tulemus.</span><span class="sxs-lookup"><span data-stu-id="08ded-132">The following illustration shows the result when the adjusted format is run.</span></span>

<a href="./media/ger-splitlistbylimit-output-1.png"><img src="./media/ger-splitlistbylimit-output-1.png" alt="Output of the adjusted format" class="alignnone size-full wp-image-1204113" width="676" height="611" /></a>

> [!NOTE] 
> <span data-ttu-id="08ded-133">Piirangut ei rakendata algse loendi viimasele üksusele, kuna selle piirangu allika (**mass**) väärtus (**11**) ületab määratletud piirangut (**9**).</span><span class="sxs-lookup"><span data-stu-id="08ded-133">The limit isn't applied to the last item of the original list, because the value (**11**) of the limit source (**weight**) exceeds the defined limit (**9**).</span></span> <span data-ttu-id="08ded-134">Aruande loomisel alamloendite ignoreerimiseks kasutage vastavalt vajadusele kas funktsiooni `WHERE` või vastava vormingu elemendi avaldist **Lubatud**.</span><span class="sxs-lookup"><span data-stu-id="08ded-134">To ignore sublists during report generation, use either the `WHERE` function or the **Enabled** expression of the corresponding format element, as you require.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08ded-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="08ded-135">Additional resources</span></span>

[<span data-ttu-id="08ded-136">Loendi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="08ded-136">List functions</span></span>](er-functions-category-list.md)
