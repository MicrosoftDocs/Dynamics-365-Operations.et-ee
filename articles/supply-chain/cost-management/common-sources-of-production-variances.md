---
title: Tootmishälvete üldpõhjused
description: Selles artiklis selgitatakse erinevaid igat tüüpi tootmishälvete tavalisemaid põhjuseid.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da09e24d7ed041686385b8239287288228d3668e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201958"
---
# <a name="common-sources-of-production-variances"></a><span data-ttu-id="ee62b-103">Tootmishälvete üldpõhjused</span><span class="sxs-lookup"><span data-stu-id="ee62b-103">Common sources of production variances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee62b-104">Selles artiklis selgitatakse erinevaid igat tüüpi tootmishälvete tavalisemaid põhjuseid.</span><span class="sxs-lookup"><span data-stu-id="ee62b-104">This article explains various typical sources of each type of production variance.</span></span> 

<span data-ttu-id="ee62b-105">Siin on mõned tavalised **saatepartii suuruse** hälvete põhjused.</span><span class="sxs-lookup"><span data-stu-id="ee62b-105">Here are some typical sources of a **lot size** variance:</span></span>

-   <span data-ttu-id="ee62b-106">Tootmistellimuse õige kogus erineb kalkulatsiooni kogusest, mida kasutatakse standardses kulu kalkulatsioonis.</span><span class="sxs-lookup"><span data-stu-id="ee62b-106">The good quantity for a production order differs from the calculation quantity that is used in the standard cost calculation.</span></span> <span data-ttu-id="ee62b-107">Kogus moodustab aluse püsikulude amortiseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="ee62b-107">The quantity provides the basis for amortizing constant costs.</span></span>
-   <span data-ttu-id="ee62b-108">Püsikulude väärtus tootmistellimuses erineb püsikuludest, mida kasutatakse standardses kulukalkulatsioonis.</span><span class="sxs-lookup"><span data-stu-id="ee62b-108">The value of constant costs on the production order differs from the constant costs that are used in the standard cost calculation.</span></span> <span data-ttu-id="ee62b-109">Tootmistellimuse püsikulud võivad olla erinevad mitmetel põhjustel.</span><span class="sxs-lookup"><span data-stu-id="ee62b-109">The constant costs on the production order can differ for several reasons.</span></span> <span data-ttu-id="ee62b-110">Näiteks võivad püsikulud kajastada järgmisi tegureid.</span><span class="sxs-lookup"><span data-stu-id="ee62b-110">For example, the constant costs might reflect the following factors:</span></span>
    -   <span data-ttu-id="ee62b-111">Tootmise koosluse või protsessi käsitsi muutmine</span><span class="sxs-lookup"><span data-stu-id="ee62b-111">Manual changes to the production bill of materials (BOM) or route</span></span>
    -   <span data-ttu-id="ee62b-112">Erineva koosluse versiooni või protsessi versiooni valimine tootmistellimuse loomisel</span><span class="sxs-lookup"><span data-stu-id="ee62b-112">The selection of a different BOM version or route version when you create the production order</span></span>
    -   <span data-ttu-id="ee62b-113">Plaanitud tehnilise lahenduse muudatused kaubale määratud koosluse versioonis või protsessi versioonis</span><span class="sxs-lookup"><span data-stu-id="ee62b-113">Planned engineering changes to the BOM version or route version that is assigned to the item</span></span>

<span data-ttu-id="ee62b-114">Siin on mõned tavalised **tootmishinna** hälvete põhjused.</span><span class="sxs-lookup"><span data-stu-id="ee62b-114">Here are some typical sources of a **production price** variance:</span></span>

-   <span data-ttu-id="ee62b-115">Protsessi operatsiooni teavitatud tarbimise kulukategooria (ja kulukategooria hind) erineb kulukategooriast, mida kasutatakse standardses kulukalkulatsioonis.</span><span class="sxs-lookup"><span data-stu-id="ee62b-115">The cost category (and cost category price) for the reported consumption of a routing operation differs from the cost category that is used in standard cost calculation.</span></span>
-   <span data-ttu-id="ee62b-116">Kulukategooria hinna aktiivkulu erineb kulukategooria hinnast, mida kasutatakse standardses kulukalkulatsioonis.</span><span class="sxs-lookup"><span data-stu-id="ee62b-116">The active cost for the cost category price differs from the cost category price that is used in standard cost calculation.</span></span>

<span data-ttu-id="ee62b-117">Siin on mõned tavalised **tootmiskoguse** hälvete põhjused.</span><span class="sxs-lookup"><span data-stu-id="ee62b-117">Here are some typical sources of a **production quantity** variance:</span></span>

-   <span data-ttu-id="ee62b-118">Materjali komponendi liigväljastus või alaväljastus.</span><span class="sxs-lookup"><span data-stu-id="ee62b-118">You over-issue or under-issue a material component.</span></span>
-   <span data-ttu-id="ee62b-119">Protsessi operatsiooniks kuluva aja ülehindamine või alahindamine.</span><span class="sxs-lookup"><span data-stu-id="ee62b-119">You over-report or under-report the time for a routing operation.</span></span>
-   <span data-ttu-id="ee62b-120">Emakauba hea koguse ülevastuvõtt või alavastuvõtt tellimuse koguse suhtes.</span><span class="sxs-lookup"><span data-stu-id="ee62b-120">You over-receive or under-receive the good quantity of the parent item, relative to the order quantity.</span></span> <span data-ttu-id="ee62b-121">Siiski väljastate komponendid ja aruande operatsioonid täielikult tootmistellimuse tellimuskoguse alusel.</span><span class="sxs-lookup"><span data-stu-id="ee62b-121">However, you issue components and report operations completely, based on the order quantity for the production order.</span></span>

<span data-ttu-id="ee62b-122">Siin on mõned tavalised **tootmise asendamise** hälvete põhjused.</span><span class="sxs-lookup"><span data-stu-id="ee62b-122">Here are some typical sources of a **production substitution** variance:</span></span>

-   <span data-ttu-id="ee62b-123">Väljastage materjali komponendi, mida pole tootmise koosluses.</span><span class="sxs-lookup"><span data-stu-id="ee62b-123">You issue a material component that isn't on the production BOM.</span></span>
-   <span data-ttu-id="ee62b-124">Lisage tootmise kooslusele komponent käsitsi ja kinnitage see tarbituna.</span><span class="sxs-lookup"><span data-stu-id="ee62b-124">You manually add a component to the production BOM and report that component as consumed.</span></span>
-   <span data-ttu-id="ee62b-125">Kinnitage kaup tarbituna, kuid ei lisa seda käsitsi tootmise kooslusele.</span><span class="sxs-lookup"><span data-stu-id="ee62b-125">You report an item as consumed but don't manually add it to the production BOM.</span></span>
-   <span data-ttu-id="ee62b-126">Lisage tootmise protsessile operatsioon käsitsi ja kinnitage see tarbituna.</span><span class="sxs-lookup"><span data-stu-id="ee62b-126">You manually add an operation to the production route and report that operation as consumed.</span></span>
-   <span data-ttu-id="ee62b-127">Valige tootmistellimust luues erinev koosluse versioon, kus koosluse versioon erineb standardses kulukalkulatsioonis kasutatavast.</span><span class="sxs-lookup"><span data-stu-id="ee62b-127">When you create the production order, you select a BOM version that differs from the BOM version that is used in the standard cost calculation.</span></span>
-   <span data-ttu-id="ee62b-128">Valige tootmistellimust luues erinev protsessi versioon, kus protsessi versioon erineb standardses kulukalkulatsioonis kasutatavast.</span><span class="sxs-lookup"><span data-stu-id="ee62b-128">When you create the production order, you select a route version that differs from the route version that is used in the standard cost calculation.</span></span>




