---
title: Koondplaneerimise käitamise jälgimine
description: Tootmise plaanija soovib näha, kui koondplaneerimise käitamine on pooleli.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845109"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="e8e18-103">Koondplaneerimise käitamise jälgimine</span><span class="sxs-lookup"><span data-stu-id="e8e18-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e8e18-104">Tootmise plaanija soovib näha, kui koondplaneerimise käitamine on pooleli.</span><span class="sxs-lookup"><span data-stu-id="e8e18-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="e8e18-105">Kasutage protseduuri lõpuleviimiseks demoandmete ettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="e8e18-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="e8e18-106">Koondplaneerimise käivitamine</span><span class="sxs-lookup"><span data-stu-id="e8e18-106">Run master planning</span></span>
1. <span data-ttu-id="e8e18-107">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="e8e18-107">Click Master planning.</span></span>
    * <span data-ttu-id="e8e18-108">Leiate selle vaikimisi armatuurlaualt.</span><span class="sxs-lookup"><span data-stu-id="e8e18-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="e8e18-109">Valige või sisestage väärtus väljal Plaan.</span><span class="sxs-lookup"><span data-stu-id="e8e18-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="e8e18-110">Näide: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="e8e18-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="e8e18-111">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="e8e18-111">Click Run.</span></span>
4. <span data-ttu-id="e8e18-112">Tehke väljal Töötlemisaja jälgimine valik Jah.</span><span class="sxs-lookup"><span data-stu-id="e8e18-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="e8e18-113">Kui väli on juba valitud, jätke see etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="e8e18-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="e8e18-114">Sisestage number väljale Lõimede arv.</span><span class="sxs-lookup"><span data-stu-id="e8e18-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="e8e18-115">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="e8e18-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="e8e18-116">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="e8e18-116">Click Filter.</span></span>
8. <span data-ttu-id="e8e18-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e8e18-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e8e18-118">Märkige rida, kus väli = kauba kood.</span><span class="sxs-lookup"><span data-stu-id="e8e18-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="e8e18-119">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="e8e18-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="e8e18-120">Näide: T0001.</span><span class="sxs-lookup"><span data-stu-id="e8e18-120">Example: T0001</span></span>  
10. <span data-ttu-id="e8e18-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e8e18-121">Click OK.</span></span>
11. <span data-ttu-id="e8e18-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e8e18-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="e8e18-123">Koondplaneerimise käitamise jälgimine</span><span class="sxs-lookup"><span data-stu-id="e8e18-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="e8e18-124">Klõpsake nuppu Ajalugu.</span><span class="sxs-lookup"><span data-stu-id="e8e18-124">Click History.</span></span>
2. <span data-ttu-id="e8e18-125">Klõpsake suvandit Päringud.</span><span class="sxs-lookup"><span data-stu-id="e8e18-125">Click Inquiries.</span></span>
3. <span data-ttu-id="e8e18-126">Klõpsake suvandit Protsessiülesande kestus.</span><span class="sxs-lookup"><span data-stu-id="e8e18-126">Click Process task duration.</span></span>
4. <span data-ttu-id="e8e18-127">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e8e18-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e8e18-128">Iga kauba puhul saate ülevaate, kui kaua võttis aega iga planeerimise etapi lõpule viimine.</span><span class="sxs-lookup"><span data-stu-id="e8e18-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

