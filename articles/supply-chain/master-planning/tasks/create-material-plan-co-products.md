--- 
title: Kaastoodete jaoks materjaliplaani loomine
description: "Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e2fa2-103">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="e2fa2-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e2fa2-104">Tootmise planeerija plaanib materjalinõudeid valemi kaastoodete kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="e2fa2-105">Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="e2fa2-106">Kaastoote nõude loomine</span><span class="sxs-lookup"><span data-stu-id="e2fa2-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="e2fa2-107">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="e2fa2-108">Klõpsake valikut Müügitellimuse töötlemine ja päring.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="e2fa2-109">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-109">Click New.</span></span>
4. <span data-ttu-id="e2fa2-110">Klõpsake valikut Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-110">Click Sales order.</span></span>
5. <span data-ttu-id="e2fa2-111">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="e2fa2-112">Näide: US-001.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-112">Example: US-001</span></span>  
6. <span data-ttu-id="e2fa2-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-113">Click OK.</span></span>
7. <span data-ttu-id="e2fa2-114">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="e2fa2-115">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-115">Example: P6003</span></span>  
8. <span data-ttu-id="e2fa2-116">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e2fa2-117">Näide: 50000</span><span class="sxs-lookup"><span data-stu-id="e2fa2-117">Example: 50000</span></span>  
9. <span data-ttu-id="e2fa2-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e2fa2-119">Kaastoodete jaoks materjaliplaani loomine</span><span class="sxs-lookup"><span data-stu-id="e2fa2-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="e2fa2-120">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-120">Click Master planning.</span></span>
2. <span data-ttu-id="e2fa2-121">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e2fa2-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2fa2-123">Näide: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="e2fa2-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="e2fa2-124">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-124">Click Run.</span></span>
5. <span data-ttu-id="e2fa2-125">Laiendage või ahendage jaotist Kaasatavad kirjed.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="e2fa2-126">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-126">Click Filter.</span></span>
7. <span data-ttu-id="e2fa2-127">Valige loendist rida, mille väli = kaubakood.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="e2fa2-128">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="e2fa2-129">Näide: P6003.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-129">Example: P6003</span></span>  
9. <span data-ttu-id="e2fa2-130">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-130">Click OK.</span></span>
10. <span data-ttu-id="e2fa2-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-131">Click OK.</span></span>
11. <span data-ttu-id="e2fa2-132">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-132">Click Planned orders.</span></span>
12. <span data-ttu-id="e2fa2-133">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e2fa2-134">Näiteks saate filtrida välja Kaubakood väärtuse P6000 järgi.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="e2fa2-135">Filtrige valemi üksuse järgi, millel on selle kauba kaastoode, mille puhul lõite müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="e2fa2-136">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e2fa2-137">Valige mis tahes filtri tagastatud read.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="e2fa2-138">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="e2fa2-139">Laiendage või ahendage jaotist Sidumine.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="e2fa2-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2fa2-141">Plaanitud tellimus on seotud kaastoote müügitellimusega.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="e2fa2-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e2fa2-142">Close the page.</span></span>


