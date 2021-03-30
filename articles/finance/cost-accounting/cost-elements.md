---
title: Kuluelemendi dimensioonid
description: Ühe kuluarvestuse tuumsambana kasutatakse kuluelemendi dimensioone, et kategoriseerida ja jälgida, kuhu kulud voolavad.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: be2f984c1ce5c76e3f995108d25f57c29e8c8457
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226356"
---
# <a name="cost-element-dimensions"></a><span data-ttu-id="e2ae3-103">Kuluelemendi dimensioonid</span><span class="sxs-lookup"><span data-stu-id="e2ae3-103">Cost element dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2ae3-104">Ühe kuluarvestuse tuumsambana kasutatakse kuluelemendi dimensioone, et kategoriseerida ja jälgida, kuhu kulud voolavad.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-104">As one of the core pillars in Cost accounting, cost element dimensions are used to categorize and track where costs flow to.</span></span> 

<span data-ttu-id="e2ae3-105">Kuluelement vastab kulu asjakohasele kaubale kontoplaanis.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-105">A cost element corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="e2ae3-106">Põhimõtteliselt võib see olla mis tahes tüüpi element ettevõtte madalaimal tasandil, kuhu kulud saavad voolata.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-106">Basically, it can be any type of element at the lowest level in a business where costs can flow to.</span></span> <span data-ttu-id="e2ae3-107">Kuluelemendid kontseptsioonina ulatuvad pearaamatukontost kõigi kulu asjakohaste ressurssideni.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-107">Cost elements as a concept range from ledger accounts to all cost-relevant resources.</span></span> <span data-ttu-id="e2ae3-108">Praegu toetab kuluarvestus pearaamatukontosid.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-108">Currently, Cost accounting supports ledger accounts.</span></span>

## <a name="two-types-of-cost-elements"></a><span data-ttu-id="e2ae3-109">Kahte tüüpi kuluelemendid</span><span class="sxs-lookup"><span data-stu-id="e2ae3-109">Two types of cost elements</span></span>
<span data-ttu-id="e2ae3-110">On kahte tüüpi kuluelemente: esmased kuluelemendid ja teisesed kuluelemendid.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-110">There are two types of cost elements: primary cost elements and secondary cost elements.</span></span> <span data-ttu-id="e2ae3-111">Järgmine tabel kirjeldab erinevust nende kahe tüübi vahel.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-111">The following table describes the difference between the two types.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e2ae3-112"><strong>Esmased kuluelemendid</strong></span><span class="sxs-lookup"><span data-stu-id="e2ae3-112"><strong>Primary cost elements</strong></span></span></td>
<td><span data-ttu-id="e2ae3-113"><strong>Sekundaarsed kuluelemendid</strong></span><span class="sxs-lookup"><span data-stu-id="e2ae3-113"><strong>Secondary cost elements</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e2ae3-114">Esmased kuluelemendid tähistavad kulude voogu finantsaruandlusest kuluarvestusse.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-114">The primary cost elements represent the flow of costs from financial accounting to cost accounting.</span></span> <span data-ttu-id="e2ae3-115">Kuluelemendi struktuur vastab pearaamatus kasumi ja kahjumi kontostruktuurile, kus kuluelement võib vastata põhikontole.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-115">The cost element structure corresponds to the profit and loss account structure in the general ledger, where a cost element can correspond to a main account.</span></span> <span data-ttu-id="e2ae3-116">Mitte kõiki põhikontosid ei pea ilmtingimata ärinõuetest sõltuvalt tähistama kuluelementidena.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-116">Not all main accounts may necessarily be represented as cost elements depending on the business needs.</span></span> <span data-ttu-id="e2ae3-117">Näiteid esmastest kuluelementidest.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-117">Examples of primary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="e2ae3-118">Müüdud kaupade kulud</span><span class="sxs-lookup"><span data-stu-id="e2ae3-118">Costs of goods sold (COGs)</span></span></li>
<li><span data-ttu-id="e2ae3-119">Kaudsed materjalikulud</span><span class="sxs-lookup"><span data-stu-id="e2ae3-119">Indirect material costs</span></span></li>
<li><span data-ttu-id="e2ae3-120">Personalikulud</span><span class="sxs-lookup"><span data-stu-id="e2ae3-120">Personnel costs</span></span></li>
<li><span data-ttu-id="e2ae3-121">Energiakulud</span><span class="sxs-lookup"><span data-stu-id="e2ae3-121">Energy costs</span></span></li>
</ul></td>
<td><span data-ttu-id="e2ae3-122">Teisesed kuluelemendid tähistavad kulude sisevoolu, kuna neid kulusid luuakse ja kasutatakse ainult kuluarvestuses.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-122">The secondary cost elements represent the flow of costs internally because these costs are created and used only in Cost accounting.</span></span> <span data-ttu-id="e2ae3-123">Neid kasutatakse tagamaks, et kulude allikat saab jälgida.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-123">They are used to secure that the source of costs can be traced.</span></span> <span data-ttu-id="e2ae3-124">Neid kuluelemente kasutatakse kulude eraldamises ja üldkulude arvutustes.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-124">These cost elements are used in cost allocations and overhead calculations.</span></span> <span data-ttu-id="e2ae3-125">Näiteid teisestest kuluelementidest.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-125">Examples of secondary cost elements include:</span></span>
<ul>
<li><span data-ttu-id="e2ae3-126">Tootmiskulud</span><span class="sxs-lookup"><span data-stu-id="e2ae3-126">Production costs</span></span></li>
<li><span data-ttu-id="e2ae3-127">Tootmine, materjal ja turustamise üldkulud</span><span class="sxs-lookup"><span data-stu-id="e2ae3-127">Production, material, and marketing overheads</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a><span data-ttu-id="e2ae3-128">Kuluelemendi dimensioonid ja kuluelemendi dimensiooni liikmed</span><span class="sxs-lookup"><span data-stu-id="e2ae3-128">Cost element dimensions and cost element dimension members</span></span>
<span data-ttu-id="e2ae3-129">Kuluelemente nimetatakse *kuluelemendi dimensioonideks* .</span><span class="sxs-lookup"><span data-stu-id="e2ae3-129">Cost elements are referred to as *cost element dimensions* .</span></span> <span data-ttu-id="e2ae3-130">Individuaalseid dimensiooniväärtuseid nimetatakse *kuluelemendi dimensiooni liikmeteks*.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-130">The individual dimension values are called *cost element dimension members*.</span></span> <span data-ttu-id="e2ae3-131">Näiteks on teil USA kontoplaani struktuur (COA), mis on teie seadusliku aruandluse alus.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-131">For example, you have a US chart of accounts structure (COA) that is the base for your statutory reporting.</span></span> <span data-ttu-id="e2ae3-132">Seda COA-d kasutatakse kuluelemendi dimensioonina.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-132">This COA is used as the cost element dimension.</span></span> <span data-ttu-id="e2ae3-133">Kontosid, mis on esmased kuluelemendid, tähistatakse kuluarvestuses kuluelemendi dimensiooniliikmetena.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-133">The accounts, which are primary cost elements, are represented as the cost element dimension members in Cost accounting.</span></span> <span data-ttu-id="e2ae3-134">Järgmine kuvatõmmis näitab näidet põhikontodest kuluelemendi dimensioonina, kus selle tegelikud põhikontod on kuluelemendi dimensiooni liikmed.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-134">The following screenshot shows an example of Main Accounts as the cost element dimension with its actual main accounts as the cost element dimension members.</span></span> 

<span data-ttu-id="e2ae3-135">[![Kuvatõmmis põhikontodest kui kuluelemendi dimensioonist](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="e2ae3-135">[![Screenshot of Main Accounts as cost element dimension](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)</span></span>

## <a name="import-cost-element-dimension-members-through-data-connectors"></a><span data-ttu-id="e2ae3-136">Kuluelemendi dimensiooni liikmete importimine andmekonnektorite kaudu</span><span class="sxs-lookup"><span data-stu-id="e2ae3-136">Import cost element dimension members through data connectors</span></span>
<span data-ttu-id="e2ae3-137">Kuluelemendi dimensiooni liikmete seadistamise lihtsustamiseks kuluarvestuses saate kasutada andmekonnektoreid, mis on eelnevalt ehitatud või teie järgi kohandatud, et tuua esmased kuluelemendid ühest või mitmest lähtesüsteemist.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-137">To ease the setup of cost element dimension members in Cost accounting, you can use data connectors that are either pre-built or your custom build to retrieve the primary cost elements from one or more source systems.</span></span>

## <a name="implementation-considerations"></a><span data-ttu-id="e2ae3-138">Juurutamise kaalutlused</span><span class="sxs-lookup"><span data-stu-id="e2ae3-138">Implementation considerations</span></span>
<span data-ttu-id="e2ae3-139">Kuna kuluelemendid tähistavad kulu üksikasjade madalaimat tasanit, peaksite tagama, et kõik juhtimisaruandluse tegemiseks vajalikud kuluelemendi on kuluelemendi struktuuri juurutamisel kaasatud.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-139">As cost elements represent the lowest level of cost details, you should make sure that all the cost elements required to make the managerial reporting are included when you implement the cost elements structure.</span></span> <span data-ttu-id="e2ae3-140">See võib olla väljakutse, et leida kulujuhtimise jaoks kuluelementide sobiv number.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-140">It can be a challenge to find an appropriate number of cost elements for cost control.</span></span> <span data-ttu-id="e2ae3-141">Tuhandete kuluelementide omamine võib muuta iga kuluelemendi juhtimise keeruliseks.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-141">Having thousands of cost elements can make it difficult to control each cost element.</span></span> <span data-ttu-id="e2ae3-142">Alternatiivina saate kuluelemente grupeerida ja hallata kulu juhtimist koondtasemel.</span><span class="sxs-lookup"><span data-stu-id="e2ae3-142">As an alternative, you can group cost elements and manage cost control at an aggregated level.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]