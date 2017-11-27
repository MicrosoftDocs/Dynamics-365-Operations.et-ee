---
title: "Füüsilised ja finantsilised värskendamised"
description: "Käesolev teema annab ülevaate selle kohta, millised kande tüübid suurendavad või vähendavad laokoguseid."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e62bdbfb7b88f66ea1f6e4d57b6150c8b0bffb04
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="physical-and-financial-updates"></a><span data-ttu-id="c76d2-103">Füüsilised ja finantsilised värskendamised</span><span class="sxs-lookup"><span data-stu-id="c76d2-103">Physical and financial updates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c76d2-104">Käesolev teema annab ülevaate selle kohta, millised kande tüübid suurendavad või vähendavad laokoguseid.</span><span class="sxs-lookup"><span data-stu-id="c76d2-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="c76d2-105">Laokandeid saab füüsiliselt uuendada ja finantsiliselt uuendada Microsoft Dynamics 365 for Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="c76d2-105">Inventory transactions can be physically updated and financially updated in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="c76d2-106">Mõnd tüüpi füüsilised ja finantsilised kanded suurendavad varude koguseid ja mõned teised tüübid vähendavad koguseid.</span><span class="sxs-lookup"><span data-stu-id="c76d2-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="c76d2-107">Füüsiline suurendamine</span><span class="sxs-lookup"><span data-stu-id="c76d2-107">Physical increases</span></span>
<span data-ttu-id="c76d2-108">Kui füüsiline kanne on sisestatud, on kande kirje olek **Vastu võetud**.</span><span class="sxs-lookup"><span data-stu-id="c76d2-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="c76d2-109">Järgmisi kandeid peetakse füüsilisteks tõusudeks:</span><span class="sxs-lookup"><span data-stu-id="c76d2-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="c76d2-110">Ostutellimuse sissetulek</span><span class="sxs-lookup"><span data-stu-id="c76d2-110">Purchase order receipt</span></span>
-   <span data-ttu-id="c76d2-111">Müügitellimuse saatelehe tagastus</span><span class="sxs-lookup"><span data-stu-id="c76d2-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="c76d2-112">Tootmistellimuse lõpetatuks kinnitamine</span><span class="sxs-lookup"><span data-stu-id="c76d2-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="c76d2-113">Kõrvalsaadus tootmistellimuse komplekteerimislehel</span><span class="sxs-lookup"><span data-stu-id="c76d2-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="c76d2-114">Rahaline suurendamine</span><span class="sxs-lookup"><span data-stu-id="c76d2-114">Financial increases</span></span>
<span data-ttu-id="c76d2-115">Kui finantsilise sissetuleku kanne on sisestatud, on kogust suurendava kande kirje olek **Ostetud**.</span><span class="sxs-lookup"><span data-stu-id="c76d2-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="c76d2-116">Järgmisi kandeid peetakse finantsilisteks tõusudeks:</span><span class="sxs-lookup"><span data-stu-id="c76d2-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="c76d2-117">Hankijaarve</span><span class="sxs-lookup"><span data-stu-id="c76d2-117">Vendor invoice</span></span>
-   <span data-ttu-id="c76d2-118">Müügitellimuse arve tagastuseks</span><span class="sxs-lookup"><span data-stu-id="c76d2-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="c76d2-119">Tootmistellimuse omahinna arvutamine</span><span class="sxs-lookup"><span data-stu-id="c76d2-119">Production order costing</span></span>
-   <span data-ttu-id="c76d2-120">Positiivse koguse laotöölehed, nt liikumine, kasum ja kaotus, inventuur, kooslus ja üleviimine</span><span class="sxs-lookup"><span data-stu-id="c76d2-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="c76d2-121">Kanded, mis suurendavad kogust</span><span class="sxs-lookup"><span data-stu-id="c76d2-121">Transactions that increase quantity</span></span>
<span data-ttu-id="c76d2-122">Kogust suurendavad kanded sisestatakse jooksva keskmise omahinnaga.</span><span class="sxs-lookup"><span data-stu-id="c76d2-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="c76d2-123">Finance and Operations arvutab jooksva keskmise omahinna, mis põhineb iga finantsiliselt jälgitava varude dimensiooni iga kande kulul.</span><span class="sxs-lookup"><span data-stu-id="c76d2-123">Finance and Operations calculates a running average cost price that is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="c76d2-124">Lisateavet jooksva keskmise omahinna kohta vt jaotisest [Jooksev keskmine omahind](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="c76d2-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="c76d2-125">Kanded, mis vähendavad kogust</span><span class="sxs-lookup"><span data-stu-id="c76d2-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="c76d2-126">Finance and Operations kasutab arvutatud keskmist jooksvat omahinda, kui sisestatakse kanne, mis vähendab kogust, sõltumata sellest, milline varude mudel on selle laovaruga seostatud.</span><span class="sxs-lookup"><span data-stu-id="c76d2-126">Finance and Operations uses the calculated running average cost price when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="c76d2-127">Kogust vähendav kanne ei tohi enne sisestamist teise kande juurde märgitud olla.</span><span class="sxs-lookup"><span data-stu-id="c76d2-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="c76d2-128">Kui füüsiline vaba kaubavaru muutub negatiivseks, kasutab Finance and Operations kaubale lehel **Kaup** määratud laokulu.</span><span class="sxs-lookup"><span data-stu-id="c76d2-128">If the physical on-hand inventory becomes negative, Finance and Operations uses the inventory cost that is defined for the item on the **Item** page.</span></span> <span data-ttu-id="c76d2-129">**Märkus.** Kui mitme asukoha funktsioon on lubatud, on see kulu asukohale lehel **Tellimuse vaikesätted** määratud varude kulu.</span><span class="sxs-lookup"><span data-stu-id="c76d2-129">**Note:** If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="c76d2-130">Füüsilised väljaminekud vs rahalised väljaminekud</span><span class="sxs-lookup"><span data-stu-id="c76d2-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="c76d2-131">Kui füüsilise väljamineku kanne on sisestatud, on kande kirje olek **Maha arvatud**.</span><span class="sxs-lookup"><span data-stu-id="c76d2-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="c76d2-132">Järgmisi kandeid peetakse füüsilisteks väljaminekuteks:</span><span class="sxs-lookup"><span data-stu-id="c76d2-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="c76d2-133">Tootmistellimuse komplekteerimislehe tööleht</span><span class="sxs-lookup"><span data-stu-id="c76d2-133">Production order picking list journal</span></span>
-   <span data-ttu-id="c76d2-134">Müügitellimuse saateleht</span><span class="sxs-lookup"><span data-stu-id="c76d2-134">Sales order packing slip</span></span>
-   <span data-ttu-id="c76d2-135">Ostutellimuse saatelehe tagastus</span><span class="sxs-lookup"><span data-stu-id="c76d2-135">Purchase order packing slip return</span></span>

<span data-ttu-id="c76d2-136">Kui finantsiline kanne on sisestatud, on kande kirje olek **Müüdud**.</span><span class="sxs-lookup"><span data-stu-id="c76d2-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="c76d2-137">Järgmisi kandeid peetakse füüsilisteks väljaminekuteks:</span><span class="sxs-lookup"><span data-stu-id="c76d2-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="c76d2-138">Tootmistellimuse lõpetamine</span><span class="sxs-lookup"><span data-stu-id="c76d2-138">Ending a production order</span></span>
-   <span data-ttu-id="c76d2-139">Müügitellimuse arve</span><span class="sxs-lookup"><span data-stu-id="c76d2-139">Sales order invoice</span></span>
-   <span data-ttu-id="c76d2-140">Hankija arve tagastus</span><span class="sxs-lookup"><span data-stu-id="c76d2-140">Vendor invoice return</span></span>
-   <span data-ttu-id="c76d2-141">Negatiivse koguse laotöölehed, nt liikumine, kasum ja kaotus, inventuur, kooslus ja üleviimine</span><span class="sxs-lookup"><span data-stu-id="c76d2-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="c76d2-142">Kogust vähendavad kanded sisestatakse jooksva keskmise omahinnaga.</span><span class="sxs-lookup"><span data-stu-id="c76d2-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="c76d2-143">Seega on vajalik laosulgemisprotseduur väljaminekukannete tasakaalustamiseks sissetulekukannetega igale kaubale määratud laomudeli alusel.</span><span class="sxs-lookup"><span data-stu-id="c76d2-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>




