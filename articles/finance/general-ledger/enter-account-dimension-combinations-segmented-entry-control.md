---
title: Konto ja dimensioonide kombinatsioonide sisestamine (segmenditud sisestamise juhtimine)
description: Selles artiklis kirjeldatakse, kuidas sisestada konto ja dimensiooni kombinatsioone või pearaamatukontosid. Kande kogemust nimetatakse sageli segmenditud sisestuse juhtelemendiks.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure
audience: Application User
ms.reviewer: roschlom
ms.custom: 14071
ms.assetid: e6fce826-c403-4d91-a78b-e9a58c44ac03
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bed6a13a721269550fa72c495e7ecfddadf9d8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260777"
---
# <a name="enter-account-and-dimension-combinations-segmented-entry-control"></a><span data-ttu-id="ae0b6-104">Konto ja dimensioonide kombinatsioonide sisestamine (segmenditud sisestamise juhtimine)</span><span class="sxs-lookup"><span data-stu-id="ae0b6-104">Enter account and dimension combinations (segmented entry control)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae0b6-105">Selles artiklis kirjeldatakse, kuidas sisestada konto ja dimensiooni kombinatsioone või pearaamatukontosid.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-105">This article describes how to enter account and dimension combinations or ledger accounts.</span></span> <span data-ttu-id="ae0b6-106">Kande kogemust nimetatakse sageli segmenditud sisestuse juhtelemendiks.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-106">The entry experience is often referred to as segmented entry control.</span></span>

<span data-ttu-id="ae0b6-107">Kasutajad sisestavad konto ja dimensiooni kombinatsioonid mitmesugustele lehtedele, nt pearaamatu, eelarvestamise ja sisestamisdefinitsioonide lehtedele.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-107">Users enter account and dimension combinations on various pages, such as pages for general journals, budgeting, and posting definitions.</span></span> <span data-ttu-id="ae0b6-108">Kehtivad konto ja dimensiooni kombinatsioonid sõltuvad pearaamatule määratud kontostruktuuridest ja täpsematest kontostruktuuridele määratud reeglitest.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-108">The valid account and dimension combinations depend on the account structures that are assigned to the ledger and the advanced rules that are assigned to the account structures.</span></span> <span data-ttu-id="ae0b6-109">Kui kasutajad kombinatsioone sisestavad, võivad nad tippida väärtusi käsitsi või kasutada rikast otsingukogemust.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-109">When users enter a combination, they can either manually type the values or take advantage of a rich, lookup experience.</span></span> <span data-ttu-id="ae0b6-110">Kui väljale sisenedes tippima hakkate, siis otsitakse väärtust ja kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-110">When you enter the field, you can start to type and it will search the value and the description.</span></span> <span data-ttu-id="ae0b6-111">Näiteks kui tipite 180, siis otsitakse igasugust selle numbrikombinatsiooniga algavat väärtust.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-111">For example, if you type 180 it will search any value that begins with that number combination.</span></span> <span data-ttu-id="ae0b6-112">Või tippige Raha ja otsitakse mis tahes väärtust, mille kirjeldus algab sõnaga Raha.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-112">Or you may type Cash and it will search any value that has a description that begins with Cash.</span></span> <span data-ttu-id="ae0b6-113">Võite kasutada ka metamärke, nt \*Raha või \*180, et otsida, kas väärtus või kirjeldus sisaldavad otsingukriteeriume.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-113">You can also use a wildcard, such as \*Cash or \*180 to search if the value or description contain the search criteria.</span></span> 

<span data-ttu-id="ae0b6-114">Järgmises tabelis on kirjeldatud klaviatuuri otseteed, mida saab kasutada, kui otsing on suletud.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-114">The following table describes the keyboard shortcuts that can be used when the lookup is closed.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae0b6-115">Kiirklahv</span><span class="sxs-lookup"><span data-stu-id="ae0b6-115">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="ae0b6-116">Tegevus</span><span class="sxs-lookup"><span data-stu-id="ae0b6-116">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae0b6-117">Alt + allanool</span><span class="sxs-lookup"><span data-stu-id="ae0b6-117">Alt+Down Arrow</span></span></td>
<td><span data-ttu-id="ae0b6-118">Avatakse otsing.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-118">Open the lookup.</span></span> <span data-ttu-id="ae0b6-119">Kui vajutate klahvikombinatsiooni Alt + allanool teist korda, liigub fookus hüpiku segmentidele.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-119">If you press Alt+Down Arrow a second time, the focus moves to the segments in the flyout.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ae0b6-120">Enter ja Shift + Enter</span><span class="sxs-lookup"><span data-stu-id="ae0b6-120">Enter and Shift+Enter</span></span></li>
<li><span data-ttu-id="ae0b6-121">Kontoplaani eraldaja</span><span class="sxs-lookup"><span data-stu-id="ae0b6-121">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="ae0b6-122">Paremnool ja vasaknool</span><span class="sxs-lookup"><span data-stu-id="ae0b6-122">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="ae0b6-123">Järgmise eelmise segmendi juurde liikumine.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-123">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae0b6-124">Vahekaart</span><span class="sxs-lookup"><span data-stu-id="ae0b6-124">Tab</span></span></td>
<td><span data-ttu-id="ae0b6-125">Minge ruudustikus järgmisele väljale.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-125">Move to the next field in the grid.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ae0b6-126">Järgmises tabelis on kirjeldatud klaviatuuri otseteed, mida saab kasutada, kui otsing on avatud.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-126">The following table describes the keyboard shortcuts that can be used when the lookup is open.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ae0b6-127">Kiirklahv</span><span class="sxs-lookup"><span data-stu-id="ae0b6-127">Keyboard shortcut</span></span></th>
<th><span data-ttu-id="ae0b6-128">Tegevus</span><span class="sxs-lookup"><span data-stu-id="ae0b6-128">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ae0b6-129">Esc-klahv</span><span class="sxs-lookup"><span data-stu-id="ae0b6-129">Esc</span></span></td>
<td><span data-ttu-id="ae0b6-130">Suleb otsingu.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-130">Close the lookup.</span></span></td>
</tr>
<tr class="even">
<td><ul>
<li><span data-ttu-id="ae0b6-131">Üles- või allanool</span><span class="sxs-lookup"><span data-stu-id="ae0b6-131">Up Arrow and Down Arrow</span></span></li>
<li><span data-ttu-id="ae0b6-132">Page Up ja Page Down</span><span class="sxs-lookup"><span data-stu-id="ae0b6-132">Page Up and Page Down</span></span></li>
<li><span data-ttu-id="ae0b6-133">Home ja End</span><span class="sxs-lookup"><span data-stu-id="ae0b6-133">Home and End</span></span></li>
</ul></td>
<td><span data-ttu-id="ae0b6-134">Loendites eelmise või järgmise väärtuse juurde, eelmise või järgmise väärtuste grupi või otsingu esimese või viimase elemendi juurde liikumine.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-134">Move to the previous or next value in the lists, to the previous or next group of values, or to the first or last element in the lookup.</span></span></td>
</tr>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="ae0b6-135">Kontoplaani eraldaja</span><span class="sxs-lookup"><span data-stu-id="ae0b6-135">Chart of accounts delimiter</span></span></li>
<li><span data-ttu-id="ae0b6-136">Paremnool ja vasaknool</span><span class="sxs-lookup"><span data-stu-id="ae0b6-136">Right Arrow and Left Arrow</span></span></li>
</ul></td>
<td><span data-ttu-id="ae0b6-137">Järgmise eelmise segmendi juurde liikumine.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-137">Move to the next or previous segment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ae0b6-138">Vahekaart</span><span class="sxs-lookup"><span data-stu-id="ae0b6-138">Tab</span></span></td>
<td><span data-ttu-id="ae0b6-139">Minge ruudustikus järgmisele väljale.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-139">Move to the next field in the grid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ae0b6-140">Alt + W</span><span class="sxs-lookup"><span data-stu-id="ae0b6-140">Alt+W</span></span></td>
<td><span data-ttu-id="ae0b6-141">Valikute <strong>Kuva kõik</strong> ja <strong>Kuva kehtivad</strong> vahetamine.</span><span class="sxs-lookup"><span data-stu-id="ae0b6-141">Switch between <strong>Show all</strong> and <strong>Show valid</strong>.</span></span></td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]