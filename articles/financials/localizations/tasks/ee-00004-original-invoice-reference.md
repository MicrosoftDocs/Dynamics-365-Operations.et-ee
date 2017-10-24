--- 
title: Algse arve viide (Ida-Euroopa)
description: "See ülesanne näitab teile, kuidas luua parandusridu müügitellimuse kreeditarvele."
author: sndray
manager: AnnBe
ms.date: 02/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Estonia
ms.author: sndray
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 023a23410acf4133658b7954ee41aa196d78ede6
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="original-invoice-reference-eastern-europe"></a><span data-ttu-id="34656-103">Algse arve viide (Ida-Euroopa)</span><span class="sxs-lookup"><span data-stu-id="34656-103">Original invoice reference (Eastern Europe)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="34656-104">See ülesanne näitab teile, kuidas luua parandusridu müügitellimuse kreeditarvele.</span><span class="sxs-lookup"><span data-stu-id="34656-104">This task walks you through creating corrective lines in a credit note for a sales order.</span></span> <span data-ttu-id="34656-105">Ülesande loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Poola, andmeid.</span><span class="sxs-lookup"><span data-stu-id="34656-105">This task was created using the demo data company DEMF with a primary address in Poland.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="34656-106">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="34656-106">Create a sales order</span></span>
1. <span data-ttu-id="34656-107">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="34656-107">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="34656-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="34656-108">Click New.</span></span>
3. <span data-ttu-id="34656-109">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="34656-109">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="34656-110">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34656-110">Click OK.</span></span>
5. <span data-ttu-id="34656-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="34656-111">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="34656-112">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="34656-112">In the Item number field, enter or select a value.</span></span>
7. <span data-ttu-id="34656-113">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="34656-113">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="34656-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="34656-114">Click Save.</span></span>
9. <span data-ttu-id="34656-115">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="34656-115">On the Action Pane, click Invoice.</span></span>
10. <span data-ttu-id="34656-116">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="34656-116">Click Invoice.</span></span>
11. <span data-ttu-id="34656-117">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="34656-117">Expand the Parameters section.</span></span>
12. <span data-ttu-id="34656-118">Valige suvand väljal Kogus.</span><span class="sxs-lookup"><span data-stu-id="34656-118">In the Quantity field, select an option.</span></span>
13. <span data-ttu-id="34656-119">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="34656-119">Expand the Setup section.</span></span>
14. <span data-ttu-id="34656-120">Sisestage kuupäev väljale Müügikuupäev.</span><span class="sxs-lookup"><span data-stu-id="34656-120">In the Sales date field, enter a date.</span></span>
15. <span data-ttu-id="34656-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="34656-121">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="34656-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34656-122">Click OK.</span></span>
17. <span data-ttu-id="34656-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34656-123">Click OK.</span></span>

## <a name="create-a-credit-note"></a><span data-ttu-id="34656-124">Kreeditarve loomine</span><span class="sxs-lookup"><span data-stu-id="34656-124">Create a credit note</span></span>
1. <span data-ttu-id="34656-125">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="34656-125">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="34656-126">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="34656-126">Click New.</span></span>
3. <span data-ttu-id="34656-127">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="34656-127">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="34656-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34656-128">Click OK.</span></span>
5. <span data-ttu-id="34656-129">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="34656-129">On the Action Pane, click Sell.</span></span>
6. <span data-ttu-id="34656-130">Klõpsake valikut Kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="34656-130">Click Credit note.</span></span>
7. <span data-ttu-id="34656-131">Märkige ruut Vali kõik.</span><span class="sxs-lookup"><span data-stu-id="34656-131">Select the Select all check box.</span></span>
8. <span data-ttu-id="34656-132">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="34656-132">Expand the Parameters section.</span></span>
9. <span data-ttu-id="34656-133">Sisestage või valige väärtus väljal Põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="34656-133">In the Reason code field, enter or select a value.</span></span>
10. <span data-ttu-id="34656-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34656-134">Click OK.</span></span>
11. <span data-ttu-id="34656-135">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="34656-135">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="34656-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="34656-136">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="34656-137">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="34656-137">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="34656-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34656-138">Click OK.</span></span>
15. <span data-ttu-id="34656-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="34656-139">Click Save.</span></span>
16. <span data-ttu-id="34656-140">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="34656-140">On the Action Pane, click Invoice.</span></span>
17. <span data-ttu-id="34656-141">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="34656-141">Click Invoice.</span></span>
18. <span data-ttu-id="34656-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="34656-142">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="34656-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34656-143">Click OK.</span></span>
20. <span data-ttu-id="34656-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34656-144">Click OK.</span></span>


