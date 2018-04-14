---
title: "Toodetud kaupade standardkulude säilitamise ettevalmistus"
description: Selles teemas kirjeldatakse toodetud kaupade kulude haldamiseks ette valmistamise etappe.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 40bcde0a43386cfd9e55d96e4a1cbc82b47e8494
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---


# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="983d7-103">Toodetud kaupade standardkulude säilitamise ettevalmistus</span><span class="sxs-lookup"><span data-stu-id="983d7-103">Prepare to maintain standard costs for manufactured items</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="983d7-104">Selles teemas kirjeldatakse toodetud kaupade kulude haldamiseks ette valmistamise etappe.</span><span class="sxs-lookup"><span data-stu-id="983d7-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="983d7-105">Toodetud kaupade etapid erinevad veidi ostetud kaupade etappidest.</span><span class="sxs-lookup"><span data-stu-id="983d7-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="983d7-106">Toodetavatele kaupadele määratud tegevuspõhimõtted võivad mõjutada kulu kalkulatsioone toodetava põhikauba puhul.</span><span class="sxs-lookup"><span data-stu-id="983d7-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="983d7-107">Toodetud kaupade kulude haldamise ettevalmistamiseks tehke läbi järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="983d7-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="983d7-108">Määrake toodetavale kaubale kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="983d7-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="983d7-109">Kauba mudeligrupp määrab standardsete kulude kasutamise.</span><span class="sxs-lookup"><span data-stu-id="983d7-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="983d7-110">Määrake toodetavale kaubale kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="983d7-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="983d7-111">Kaubagrupp sisaldab toodetavale kaubale kehtivaid pearaamatukontosid.</span><span class="sxs-lookup"><span data-stu-id="983d7-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="983d7-112">Standardse kulu laomudeliga toodetava kauba pearaamatukontod hõlmavad mitut tootmiskulude hälvet, kulu muutmise hälvet ja varude kulu ümberhindlust.</span><span class="sxs-lookup"><span data-stu-id="983d7-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="983d7-113">Määrake kaubale lao mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="983d7-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="983d7-114">Kauba kulud esitatakse alati kauba lao mõõtühikutes.</span><span class="sxs-lookup"><span data-stu-id="983d7-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="983d7-115">Ärge määrake oodetavale kaubale kulugruppi, välja arvatud juhul, kui seda käsitletakse ostetud kaubana.</span><span class="sxs-lookup"><span data-stu-id="983d7-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="983d7-116">Määrake toodetavale kaubale koosluse kalkulatsioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="983d7-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="983d7-117">Kauba koosluse kalkulatsioonigrupp määratleb kehtivad hoiatustingimused.</span><span class="sxs-lookup"><span data-stu-id="983d7-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="983d7-118">Sel viisil saab pärast koosluse kalkulatsiooni luua hoiatussõnumeid arvutusvigade võimalike allikate kohta.</span><span class="sxs-lookup"><span data-stu-id="983d7-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="983d7-119">Näiteks võib hoiatussõnum määrata, kui aktiivne kooslus või protsess puudub.</span><span class="sxs-lookup"><span data-stu-id="983d7-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="983d7-120">Koosluse kalkulatsioonigrupp sisaldab koosnevuse peatamise poliitikat, mis määrab, millal tuleb toodetavat kaupa ostetud kaubana käsitleda.</span><span class="sxs-lookup"><span data-stu-id="983d7-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="983d7-121">Kui toodetud kaubal on püsikuld, määrake sellele standardne tellimiskogus.</span><span class="sxs-lookup"><span data-stu-id="983d7-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="983d7-122">Standardne tellimiskogus on raamatupidamise saatepartii suurus püsikulude amortiseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="983d7-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="983d7-123">Püsikulude näited hõlmavad seadistusaegu protsessi operatsioonides ja komponentide püsikogust koosluses.</span><span class="sxs-lookup"><span data-stu-id="983d7-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="983d7-124">Määrake toodetavale kaubale kooslus.</span><span class="sxs-lookup"><span data-stu-id="983d7-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="983d7-125">Toodetavale kaubale saab määrata ühe või mitu koosluse versiooni.</span><span class="sxs-lookup"><span data-stu-id="983d7-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="983d7-126">Kontrollige, et soovitud versioonid oleksid märgitud kui kinnitatud ja aktiivsed ning et neil on soovitud kehtivuse kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="983d7-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="983d7-127">Koosluse versioon võib hõlmata kogu ettevõtet või olla laoala-põhine.</span><span class="sxs-lookup"><span data-stu-id="983d7-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="983d7-128">Määrake toodetavale kaubale protsess.</span><span class="sxs-lookup"><span data-stu-id="983d7-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="983d7-129">Toodetavale kaubale saab määrata ühe või mitu protsessiversiooni.</span><span class="sxs-lookup"><span data-stu-id="983d7-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="983d7-130">Kontrollige, et soovitud versioonid oleksid märgitud kui kinnitatud ja aktiivsed ning et neil on soovitud kehtivuse kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="983d7-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="983d7-131">Protsessiversioon peab olema laoala-põhine.</span><span class="sxs-lookup"><span data-stu-id="983d7-131">The route version must be site-specific.</span></span>

<span data-ttu-id="983d7-132">Kui soovite protsesside teavet kasutada kulueesmärkidel, peate tegema ettevalmistavaid lisasamme.</span><span class="sxs-lookup"><span data-stu-id="983d7-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="983d7-133">Näiteks peavad protsessi operatsioonidele määratud kulukategooriad olema õiged ja lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="983d7-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="983d7-134">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="983d7-134">Related topics</span></span>
--------

[<span data-ttu-id="983d7-135">Toodetud kauba püsikulude amortiseerimine</span><span class="sxs-lookup"><span data-stu-id="983d7-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="983d7-136">Toodetavate või hangitavate toodete seadistamine</span><span class="sxs-lookup"><span data-stu-id="983d7-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)


