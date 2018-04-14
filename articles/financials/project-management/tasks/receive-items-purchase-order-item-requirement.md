--- 
title: "Ostutellimusel olevate kaupade kaubavajadusest vastuvõtmine"
description: "See protseduur näitab, kuidas ostutellimusel olevaid kaupu kaubavajadusest vastu võtta."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fef6a597ed126ff4e1148fd9710b214c0425c3ab
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="3219f-103">Ostutellimusel olevate kaupade kaubavajadusest vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="3219f-103">Receive items on purchase order from item requirement</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3219f-104">See protseduur näitab, kuidas ostutellimusel olevaid kaupu kaubavajadusest vastu võtta.</span><span class="sxs-lookup"><span data-stu-id="3219f-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="3219f-105">Kasutades kaubakannete asemel kaubavajadusi, saate planeerida tarne just selleks ajaks, mil kaupa tegelikult kasutatakse, luua ostutellimuse, kaasata kauba kaubandusleppe raamistikku ja kaasata kaubavajaduse tootmisplaanidesse.</span><span class="sxs-lookup"><span data-stu-id="3219f-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="3219f-106">Ülesandes kasutatakse USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="3219f-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="3219f-107">Avage Projektihaldus ja -arvestus > Projektid > Kõik projektid.</span><span class="sxs-lookup"><span data-stu-id="3219f-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="3219f-108">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3219f-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="3219f-109">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="3219f-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="3219f-110">Klõpsake nuppu Kaubavajadused.</span><span class="sxs-lookup"><span data-stu-id="3219f-110">Click Item requirements.</span></span>
5. <span data-ttu-id="3219f-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3219f-111">Click New.</span></span>
6. <span data-ttu-id="3219f-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="3219f-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3219f-113">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="3219f-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="3219f-114">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="3219f-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="3219f-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3219f-115">Click Save.</span></span>
10. <span data-ttu-id="3219f-116">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="3219f-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="3219f-117">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="3219f-117">Click Functions.</span></span>
12. <span data-ttu-id="3219f-118">Klõpsake nuppu Loo ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="3219f-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="3219f-119">Märkige ruut Kaasata.</span><span class="sxs-lookup"><span data-stu-id="3219f-119">Select the Include check box.</span></span>
14. <span data-ttu-id="3219f-120">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="3219f-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="3219f-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3219f-121">Click OK.</span></span>
16. <span data-ttu-id="3219f-122">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="3219f-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="3219f-123">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3219f-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="3219f-124">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="3219f-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="3219f-125">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="3219f-125">Click Confirm.</span></span>
20. <span data-ttu-id="3219f-126">Klõpsake toimingupaanil valikut Vastuvõtt.</span><span class="sxs-lookup"><span data-stu-id="3219f-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="3219f-127">Klõpsake valikut Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="3219f-127">Click Product receipt.</span></span>
22. <span data-ttu-id="3219f-128">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="3219f-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="3219f-129">Sisestage väärtus väljale Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="3219f-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="3219f-130">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3219f-130">Click OK.</span></span>


