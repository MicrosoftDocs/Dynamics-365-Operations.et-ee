---
title: Konto ja dimensioonide kombinatsioonide sisestamine (segmenditud sisestamise juhtimine)
description: "Selles artiklis kirjeldatakse, kuidas sisestada konto ja dimensiooni kombinatsioone või pearaamatukontosid. Kande kogemust nimetatakse sageli segmenditud sisestuse juhtelemendiks."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4b4210c32cba62f98ae1d5974e76d146f03a40bc
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="ee26a-104">Konto ja dimensioonide kombinatsioonide sisestamine (segmenditud sisestamise juhtimine)</span><span class="sxs-lookup"><span data-stu-id="ee26a-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee26a-105">Selles artiklis kirjeldatakse, kuidas sisestada konto ja dimensiooni kombinatsioone või pearaamatukontosid.</span><span class="sxs-lookup"><span data-stu-id="ee26a-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="ee26a-106">Kande kogemust nimetatakse sageli segmenditud sisestuse juhtelemendiks.</span><span class="sxs-lookup"><span data-stu-id="ee26a-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="ee26a-107">Kasutajad sisestavad konto ja dimensiooni kombinatsioonid mitmesugustele lehtedele, nt pearaamatu, eelarvestamise ja sisestamisdefinitsioonide lehtedele.</span><span class="sxs-lookup"><span data-stu-id="ee26a-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="ee26a-108">Kehtivad konto ja dimensiooni kombinatsioonid sõltuvad pearaamatule määratud kontostruktuuridest ja täpsematest kontostruktuuridele määratud reeglitest.</span><span class="sxs-lookup"><span data-stu-id="ee26a-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="ee26a-109">Kui kasutajad kombinatsioone sisestavad, võivad nad tippida väärtusi käsitsi või kasutada rikast otsingukogemust.</span><span class="sxs-lookup"><span data-stu-id="ee26a-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="ee26a-110">Kui väljale sisenedes tippima hakkate, siis otsitakse väärtust ja kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="ee26a-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="ee26a-111">Näiteks kui tipite 180, siis otsitakse igasugust selle numbrikombinatsiooniga algavat väärtust.</span><span class="sxs-lookup"><span data-stu-id="ee26a-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="ee26a-112">Või tippige Raha ja otsitakse mis tahes väärtust, mille kirjeldus algab sõnaga Raha.</span><span class="sxs-lookup"><span data-stu-id="ee26a-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="ee26a-113">Võite kasutada ka metamärke, nt \*Raha või \*180, et otsida, kas väärtus või kirjeldus sisaldavad otsingukriteeriume.</span><span class="sxs-lookup"><span data-stu-id="ee26a-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="ee26a-114">Järgmises tabelis on kirjeldatud klaviatuuri otseteed, mida saab kasutada, kui otsing on suletud.</span><span class="sxs-lookup"><span data-stu-id="ee26a-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee26a-115">Kiirklahv</span><span class="sxs-lookup"><span data-stu-id="ee26a-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="ee26a-116">Tegevus</span><span class="sxs-lookup"><span data-stu-id="ee26a-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee26a-117">Alt + allanool</span><span class="sxs-lookup"><span data-stu-id="ee26a-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="ee26a-118">Avatakse otsing.</span><span class="sxs-lookup"><span data-stu-id="ee26a-118">Open the lookup.</span></span> <span data-ttu-id="ee26a-119">Kui vajutate klahvikombinatsiooni Alt + allanool teist korda, liigub fookus hüpiku segmentidele.</span><span class="sxs-lookup"><span data-stu-id="ee26a-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ee26a-120">Enter ja Shift + Enter</span><span class="sxs-lookup"><span data-stu-id="ee26a-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="ee26a-121">Kontoplaani eraldaja</span><span class="sxs-lookup"><span data-stu-id="ee26a-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="ee26a-122">Paremnool ja vasaknool</span><span class="sxs-lookup"><span data-stu-id="ee26a-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="ee26a-123">Järgmise eelmise segmendi juurde liikumine.</span><span class="sxs-lookup"><span data-stu-id="ee26a-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee26a-124">Vahekaart</span><span class="sxs-lookup"><span data-stu-id="ee26a-124">Tab</span></span></td>
<td><span data-ttu-id="ee26a-125">Minge ruudustikus järgmisele väljale.</span><span class="sxs-lookup"><span data-stu-id="ee26a-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ee26a-126">Järgmises tabelis on kirjeldatud klaviatuuri otseteed, mida saab kasutada, kui otsing on avatud.</span><span class="sxs-lookup"><span data-stu-id="ee26a-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee26a-127">Kiirklahv</span><span class="sxs-lookup"><span data-stu-id="ee26a-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="ee26a-128">Tegevus</span><span class="sxs-lookup"><span data-stu-id="ee26a-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee26a-129">Esc-klahv</span><span class="sxs-lookup"><span data-stu-id="ee26a-129">Esc</span></span></td>
<td><span data-ttu-id="ee26a-130">Suleb otsingu.</span><span class="sxs-lookup"><span data-stu-id="ee26a-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ee26a-131">Üles- või allanool</span><span class="sxs-lookup"><span data-stu-id="ee26a-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="ee26a-132">Page Up ja Page Down</span><span class="sxs-lookup"><span data-stu-id="ee26a-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="ee26a-133">Home ja End</span><span class="sxs-lookup"><span data-stu-id="ee26a-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="ee26a-134">Loendites eelmise või järgmise väärtuse juurde, eelmise või järgmise väärtuste grupi või otsingu esimese või viimase elemendi juurde liikumine.</span><span class="sxs-lookup"><span data-stu-id="ee26a-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ee26a-135">Kontoplaani eraldaja</span><span class="sxs-lookup"><span data-stu-id="ee26a-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="ee26a-136">Paremnool ja vasaknool</span><span class="sxs-lookup"><span data-stu-id="ee26a-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="ee26a-137">Järgmise eelmise segmendi juurde liikumine.</span><span class="sxs-lookup"><span data-stu-id="ee26a-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ee26a-138">Vahekaart</span><span class="sxs-lookup"><span data-stu-id="ee26a-138">Tab</span></span></td>
<td><span data-ttu-id="ee26a-139">Minge ruudustikus järgmisele väljale.</span><span class="sxs-lookup"><span data-stu-id="ee26a-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ee26a-140">Alt + W</span><span class="sxs-lookup"><span data-stu-id="ee26a-140">Alt+W</span></span></td>
<td><span data-ttu-id="ee26a-141">Valikute <strong>Kuva kõik</strong> ja <strong>Kuva kehtivad</strong> vahetamine.</span><span class="sxs-lookup"><span data-stu-id="ee26a-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>






