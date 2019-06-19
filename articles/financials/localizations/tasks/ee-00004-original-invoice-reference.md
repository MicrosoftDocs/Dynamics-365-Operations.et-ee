---
title: Algse arve viide (Ida-Euroopa)
description: See ülesanne näitab teile, kuidas luua parandusridu müügitellimuse kreeditarvele.
author: sndray
manager: AnnBe
ms.date: 02/09/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Estonia
ms.author: sndray
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa88db83b0d172097026e5bf2592187e7fedfdb2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565081"
---
# <a name="original-invoice-reference-eastern-europe"></a><span data-ttu-id="79da9-103">Algse arve viide (Ida-Euroopa)</span><span class="sxs-lookup"><span data-stu-id="79da9-103">Original invoice reference (Eastern Europe)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79da9-104">See ülesanne näitab teile, kuidas luua parandusridu müügitellimuse kreeditarvele.</span><span class="sxs-lookup"><span data-stu-id="79da9-104">This task walks you through creating corrective lines in a credit note for a sales order.</span></span> <span data-ttu-id="79da9-105">Ülesande loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Poola, andmeid.</span><span class="sxs-lookup"><span data-stu-id="79da9-105">This task was created using the demo data company DEMF with a primary address in Poland.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="79da9-106">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="79da9-106">Create a sales order</span></span>
1. <span data-ttu-id="79da9-107">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="79da9-107">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="79da9-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="79da9-108">Click New.</span></span>
3. <span data-ttu-id="79da9-109">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="79da9-109">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="79da9-110">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79da9-110">Click OK.</span></span>
5. <span data-ttu-id="79da9-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="79da9-111">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="79da9-112">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="79da9-112">In the Item number field, enter or select a value.</span></span>
7. <span data-ttu-id="79da9-113">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="79da9-113">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="79da9-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="79da9-114">Click Save.</span></span>
9. <span data-ttu-id="79da9-115">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="79da9-115">On the Action Pane, click Invoice.</span></span>
10. <span data-ttu-id="79da9-116">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="79da9-116">Click Invoice.</span></span>
11. <span data-ttu-id="79da9-117">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="79da9-117">Expand the Parameters section.</span></span>
12. <span data-ttu-id="79da9-118">Valige suvand väljal Kogus.</span><span class="sxs-lookup"><span data-stu-id="79da9-118">In the Quantity field, select an option.</span></span>
13. <span data-ttu-id="79da9-119">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="79da9-119">Expand the Setup section.</span></span>
14. <span data-ttu-id="79da9-120">Sisestage kuupäev väljale Müügikuupäev.</span><span class="sxs-lookup"><span data-stu-id="79da9-120">In the Sales date field, enter a date.</span></span>
15. <span data-ttu-id="79da9-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="79da9-121">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="79da9-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79da9-122">Click OK.</span></span>
17. <span data-ttu-id="79da9-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79da9-123">Click OK.</span></span>

## <a name="create-a-credit-note"></a><span data-ttu-id="79da9-124">Kreeditarve loomine</span><span class="sxs-lookup"><span data-stu-id="79da9-124">Create a credit note</span></span>
1. <span data-ttu-id="79da9-125">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="79da9-125">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="79da9-126">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="79da9-126">Click New.</span></span>
3. <span data-ttu-id="79da9-127">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="79da9-127">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="79da9-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79da9-128">Click OK.</span></span>
5. <span data-ttu-id="79da9-129">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="79da9-129">On the Action Pane, click Sell.</span></span>
6. <span data-ttu-id="79da9-130">Klõpsake valikut Kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="79da9-130">Click Credit note.</span></span>
7. <span data-ttu-id="79da9-131">Märkige ruut Vali kõik.</span><span class="sxs-lookup"><span data-stu-id="79da9-131">Select the Select all check box.</span></span>
8. <span data-ttu-id="79da9-132">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="79da9-132">Expand the Parameters section.</span></span>
9. <span data-ttu-id="79da9-133">Sisestage või valige väärtus väljal Põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="79da9-133">In the Reason code field, enter or select a value.</span></span>
10. <span data-ttu-id="79da9-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79da9-134">Click OK.</span></span>
11. <span data-ttu-id="79da9-135">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="79da9-135">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="79da9-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="79da9-136">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="79da9-137">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="79da9-137">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="79da9-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79da9-138">Click OK.</span></span>
15. <span data-ttu-id="79da9-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="79da9-139">Click Save.</span></span>
16. <span data-ttu-id="79da9-140">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="79da9-140">On the Action Pane, click Invoice.</span></span>
17. <span data-ttu-id="79da9-141">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="79da9-141">Click Invoice.</span></span>
18. <span data-ttu-id="79da9-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="79da9-142">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="79da9-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79da9-143">Click OK.</span></span>
20. <span data-ttu-id="79da9-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79da9-144">Click OK.</span></span>

