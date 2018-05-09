--- 
title: Konfiguratsioonireeglite loomine
description: "See protseduur loob konfiguratsioonireeglid, mida saab kasutada dimensioonipõhise konfiguratsiooni jaoks, et koosluseridade teatud kombinatsioone jõustada või takistada."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0abe7a8ef1c8d4053b341f6c0117f400492a3808
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="create-configuration-rules"></a><span data-ttu-id="a98f3-103">Konfiguratsioonireeglite loomine</span><span class="sxs-lookup"><span data-stu-id="a98f3-103">Create configuration rules</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a98f3-104">See protseduur loob konfiguratsioonireeglid, mida saab kasutada dimensioonipõhise konfiguratsiooni jaoks, et koosluseridade teatud kombinatsioone jõustada või takistada.</span><span class="sxs-lookup"><span data-stu-id="a98f3-104">This procedure creates configuration rules that can be used for dimension-based configuration to enforce or prevent certain combinations of BOM lines.</span></span> <span data-ttu-id="a98f3-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="a98f3-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="a98f3-106">See on seitsmes protseduur kaheksast, mis selgitab kombinatsioonide loomist dimensioonipõhise konfiguratsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="a98f3-106">This is the seventh procedure out of eight that explains how to build combinations for dimension-based configuration.</span></span>

1. <span data-ttu-id="a98f3-107">Minge jaotisse Tooteteabe haldus > Kooslused ja valemid > Kooslused.</span><span class="sxs-lookup"><span data-stu-id="a98f3-107">Go to Product information management > Bills of materials and formulas > Bills of materials.</span></span>
2. <span data-ttu-id="a98f3-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a98f3-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a98f3-109">Leidke ja valige kooslus dimensioonipõhise konfiguratsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="a98f3-109">Find and select the BOM for the dimension-based configuration.</span></span>  
3. <span data-ttu-id="a98f3-110">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="a98f3-110">On the Action Pane, click Options.</span></span>
4. <span data-ttu-id="a98f3-111">Klõpsake suvandit Muuda vaadet.</span><span class="sxs-lookup"><span data-stu-id="a98f3-111">Click Change view.</span></span>
5. <span data-ttu-id="a98f3-112">Klõpsake suvandit Päisevaade.</span><span class="sxs-lookup"><span data-stu-id="a98f3-112">Click Header view.</span></span>
    * <span data-ttu-id="a98f3-113">Avage päisevaade, et pääseda juurde kiirkaardile Konfiguratsiooniprotsess.</span><span class="sxs-lookup"><span data-stu-id="a98f3-113">Open the header view to access the Configuration route FastTab.</span></span>  
6. <span data-ttu-id="a98f3-114">Laiendage või ahendage jaotist Konfiguratsiooniprotsess.</span><span class="sxs-lookup"><span data-stu-id="a98f3-114">Expand or collapse the Configuration route section.</span></span>
    * <span data-ttu-id="a98f3-115">Kiirkaart Konfiguratsiooniprotsess peab olema laiendatud režiimis.</span><span class="sxs-lookup"><span data-stu-id="a98f3-115">The Configuration route FastTab must be in the expanded mode.</span></span>  
7. <span data-ttu-id="a98f3-116">Klõpsake suvandit Konfiguratsioonireeglid.</span><span class="sxs-lookup"><span data-stu-id="a98f3-116">Click Configuration rules.</span></span>
8. <span data-ttu-id="a98f3-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a98f3-117">Click New.</span></span>
9. <span data-ttu-id="a98f3-118">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a98f3-118">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="a98f3-119">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a98f3-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a98f3-120">Kuvatakse praeguses konfiguratsioonigrupis olevad kaubad.</span><span class="sxs-lookup"><span data-stu-id="a98f3-120">The items in the current configuration group are displayed.</span></span> <span data-ttu-id="a98f3-121">Valige see, mis kujutab reeglis olevat tingimust.</span><span class="sxs-lookup"><span data-stu-id="a98f3-121">Select the one that represents the condition in the rule.</span></span>  
11. <span data-ttu-id="a98f3-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a98f3-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="a98f3-123">Valige suvand väljalt Meetod.</span><span class="sxs-lookup"><span data-stu-id="a98f3-123">In the Method field, select an option.</span></span>
    * <span data-ttu-id="a98f3-124">Võimalik on jõustada kas teisest konfiguratsioonigrupist pärit kauba valik või valiku tühistamine.</span><span class="sxs-lookup"><span data-stu-id="a98f3-124">It is possible to enforce either a selection or a deselection of an item from another configuration group.</span></span>  
13. <span data-ttu-id="a98f3-125">Klõpsake väljal Tuletatud grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a98f3-125">In the Derived group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="a98f3-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a98f3-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="a98f3-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a98f3-127">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a98f3-128">Valige soovitud konfiguratsioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="a98f3-128">Select the desired configuration group.</span></span>  
16. <span data-ttu-id="a98f3-129">Klõpsake väljal Tuletatud kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a98f3-129">In the Derived item number field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="a98f3-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a98f3-130">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a98f3-131">Valige kaubakood, mis olenevalt valitud meetodist kas valitakse või mille valik tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="a98f3-131">Select the item number that will be either selected or deselected depending on the chosen method.</span></span>  
18. <span data-ttu-id="a98f3-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a98f3-132">Close the page.</span></span>


