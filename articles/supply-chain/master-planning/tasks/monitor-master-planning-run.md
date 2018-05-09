--- 
title: "Koondplaneerimise käitamise jälgimine"
description: "Tootmise plaanija soovib näha, kui koondplaneerimise käitamine on pooleli."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 550e2de01187d889ef968a4ff6828f93bb44a8a1
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="5a1f4-103">Koondplaneerimise käitamise jälgimine</span><span class="sxs-lookup"><span data-stu-id="5a1f4-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5a1f4-104">Tootmise plaanija soovib näha, kui koondplaneerimise käitamine on pooleli.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="5a1f4-105">Kasutage protseduuri lõpuleviimiseks demoandmete ettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="5a1f4-106">Koondplaneerimise käivitamine</span><span class="sxs-lookup"><span data-stu-id="5a1f4-106">Run master planning</span></span>
1. <span data-ttu-id="5a1f4-107">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-107">Click Master planning.</span></span>
    * <span data-ttu-id="5a1f4-108">Leiate selle vaikimisi armatuurlaualt.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="5a1f4-109">Valige või sisestage väärtus väljal Plaan.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="5a1f4-110">Näide: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="5a1f4-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="5a1f4-111">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-111">Click Run.</span></span>
4. <span data-ttu-id="5a1f4-112">Tehke väljal Töötlemisaja jälgimine valik Jah.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="5a1f4-113">Kui väli on juba valitud, jätke see etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="5a1f4-114">Sisestage number väljale Lõimede arv.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="5a1f4-115">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="5a1f4-116">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-116">Click Filter.</span></span>
8. <span data-ttu-id="5a1f4-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5a1f4-118">Märkige rida, kus väli = kauba kood.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="5a1f4-119">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="5a1f4-120">Näide: T0001.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-120">Example: T0001</span></span>  
10. <span data-ttu-id="5a1f4-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-121">Click OK.</span></span>
11. <span data-ttu-id="5a1f4-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="5a1f4-123">Koondplaneerimise käitamise jälgimine</span><span class="sxs-lookup"><span data-stu-id="5a1f4-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="5a1f4-124">Klõpsake nuppu Ajalugu.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-124">Click History.</span></span>
2. <span data-ttu-id="5a1f4-125">Klõpsake suvandit Päringud.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-125">Click Inquiries.</span></span>
3. <span data-ttu-id="5a1f4-126">Klõpsake suvandit Protsessiülesande kestus.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-126">Click Process task duration.</span></span>
4. <span data-ttu-id="5a1f4-127">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5a1f4-128">Iga kauba puhul saate ülevaate, kui kaua võttis aega iga planeerimise etapi lõpule viimine.</span><span class="sxs-lookup"><span data-stu-id="5a1f4-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


