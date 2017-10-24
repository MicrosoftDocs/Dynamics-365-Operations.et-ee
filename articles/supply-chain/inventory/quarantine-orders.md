---
title: Vahelaoorderid
description: See artikkel kirjeldab vahelaoorderite kasutamist varude blokeerimiseks.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 17dde4a4e3380beb98eeb71c719fb898b40a94f7
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="quarantine-orders"></a><span data-ttu-id="3b3df-103">Vahelaoorderid</span><span class="sxs-lookup"><span data-stu-id="3b3df-103">Quarantine orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3b3df-104">See artikkel kirjeldab vahelaoorderite kasutamist varude blokeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="3b3df-104">This article describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="3b3df-105">Vahelaoordereid saab kasutada varude blokeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="3b3df-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="3b3df-106">Näiteks võib olla vaja kvaliteedikontrolliks kaubad vahelattu paigutada.</span><span class="sxs-lookup"><span data-stu-id="3b3df-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="3b3df-107">Karantiinis olevad kaubad edastatakse vahelattu.</span><span class="sxs-lookup"><span data-stu-id="3b3df-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="3b3df-108">**Märkus:** täpsema laohalduse protsesside kasutamisel (laohalduse moodulis) kasutatakse vahelao tellimuse töötlemist ainult müügi tagastustellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="3b3df-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-onhand-inventory-items"></a><span data-ttu-id="3b3df-109">Vabade laokaupade paigutamine vahelattu</span><span class="sxs-lookup"><span data-stu-id="3b3df-109">Quarantine onhand inventory items</span></span>
<span data-ttu-id="3b3df-110">Kui saadate kaubad vahelattu, saate luua vahelaoorderid käsitsi või seadistada süsteemi looma sissetuleva töötluse ajal vahelaoordereid automaatselt.</span><span class="sxs-lookup"><span data-stu-id="3b3df-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="3b3df-111">Vahelaoorderite automaatseks loomiseks tehke valik **Vahelao haldus** vahekaardil **Varude poliitikad** lehel **Kauba mudeligrupid**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="3b3df-112">Peate määrama vastuvõtvatele ladudele ka vaikevahelao väljal **Vaheladu**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="3b3df-113">Kaubad pannakse Microsoft Dynamics 365 for Finance and Operationsis automaatselt vahelattu, kui füüsiliselt vaba kaubavaru tootmistellimusel või ostutellimusel salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="3b3df-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="3b3df-114">Selline liikumine toimub, kuna vahelaoorderi olekuks määratakse **Alustatud**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="3b3df-115">Kui loote vahelaoorderid käsitsi, ei pea kaupa seotud kauba mudeligrupis vahelao halduseks seadistama.</span><span class="sxs-lookup"><span data-stu-id="3b3df-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="3b3df-116">Selle protsessi jaoks peate määrama vaba kaubavaru, mis tuleks vahelattu paigutada, ja kasutatava vahelao.</span><span class="sxs-lookup"><span data-stu-id="3b3df-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="3b3df-117">Protsessi plaanimisel saate kasutada abivahendina vahelaoorderi olekuid.</span><span class="sxs-lookup"><span data-stu-id="3b3df-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="3b3df-118">Vahelaoorderi olekud</span><span class="sxs-lookup"><span data-stu-id="3b3df-118">Quarantine order statuses</span></span>
<span data-ttu-id="3b3df-119">Vahelaoorderite olek võib olla järgmine:</span><span class="sxs-lookup"><span data-stu-id="3b3df-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="3b3df-120">Loodud</span><span class="sxs-lookup"><span data-stu-id="3b3df-120">Created</span></span>
-   <span data-ttu-id="3b3df-121">Alustatud</span><span class="sxs-lookup"><span data-stu-id="3b3df-121">Started</span></span>
-   <span data-ttu-id="3b3df-122">Lõpetamine kinnitatud</span><span class="sxs-lookup"><span data-stu-id="3b3df-122">Reported as finished</span></span>
-   <span data-ttu-id="3b3df-123">Lõpetatud</span><span class="sxs-lookup"><span data-stu-id="3b3df-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="3b3df-124">Loodud</span><span class="sxs-lookup"><span data-stu-id="3b3df-124">Created</span></span>

<span data-ttu-id="3b3df-125">Kui vahelaoorder on loodud käsitsi, kuid kaup ei ole veel vahelattu pandud, siis on vahelaoorderi olek **Loodud**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="3b3df-126">Luuakse kaks laokannet.</span><span class="sxs-lookup"><span data-stu-id="3b3df-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="3b3df-127">Üks kanne on väljaminekukanne, mille olek võib olla **Tellimusel**, **Füüsiliselt reserveeritud** või **Komplekteeritud**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="3b3df-128">Teine kanne on sissetulekukanne, mille olek võib vahelaos olla **Tellitud** või **Registreeritud**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="3b3df-129">Saate reserveerida, komplekteerida ja registreerida varude värskendusi tavaliste protsesside abil.</span><span class="sxs-lookup"><span data-stu-id="3b3df-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="3b3df-130">Alustatud</span><span class="sxs-lookup"><span data-stu-id="3b3df-130">Started</span></span>

<span data-ttu-id="3b3df-131">Kui vahelaoorderi oleks on **Alustatud**, edastatakse varud tavalisest laost vahelattu ja luuakse kaks laokannet.</span><span class="sxs-lookup"><span data-stu-id="3b3df-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="3b3df-132">Ühe kande olek on **Maha arvatud** ja teise kande olek on **Vastu võetud**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="3b3df-133">Samal ajal luuakse kaks laokannet tagastuse käsitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="3b3df-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="3b3df-134">Need kanded ei ole kuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="3b3df-134">These transactions aren't dated.</span></span> <span data-ttu-id="3b3df-135">Ühe kande olek on **Füüsiliselt reserveeritud** ja teise kande olek on **Tellitud**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="3b3df-136">Lõpetamine kinnitatud</span><span class="sxs-lookup"><span data-stu-id="3b3df-136">Reported as finished</span></span>

<span data-ttu-id="3b3df-137">Kui klõpsate nuppu **Kinnita lõpetamine**, saate kinnitada alustatud vahelaoorder lõpetamise.</span><span class="sxs-lookup"><span data-stu-id="3b3df-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="3b3df-138">Kaup on vahelaost väljastatud, kuid ei ole veel tavalisse lattu tagasi viidud.</span><span class="sxs-lookup"><span data-stu-id="3b3df-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="3b3df-139">Tavalisse lattu tagasiviimist saab töödelda saabuva kauba töölehe kaudu, mille saab käivitada lõpetatuna kinnitamise protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="3b3df-139">The movement back to the regular warehouse can be procesed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="3b3df-140">Lõpetatud</span><span class="sxs-lookup"><span data-stu-id="3b3df-140">Ended</span></span>

<span data-ttu-id="3b3df-141">Kui vahelaoorder lõppeb, viiakse kaup vahelaost tagasi tavalisse lattu.</span><span class="sxs-lookup"><span data-stu-id="3b3df-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="3b3df-142">Kauba kande olekuks on vahelaos **Müüdud** ja tavalises laos **Ostetud**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="3b3df-143">Vahelaoorderi praak</span><span class="sxs-lookup"><span data-stu-id="3b3df-143">Quarantine order scrap</span></span>
<span data-ttu-id="3b3df-144">Vahelaoorderi protsessi osana on võimalik ka varusid praakida.</span><span class="sxs-lookup"><span data-stu-id="3b3df-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="3b3df-145">Praagi töötlemisel määratakse vahelao väljaminekukandega varude olekuks **Müüdud**.</span><span class="sxs-lookup"><span data-stu-id="3b3df-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="see-also"></a><span data-ttu-id="3b3df-146">Vt ka</span><span class="sxs-lookup"><span data-stu-id="3b3df-146">See also</span></span>
--------

[<span data-ttu-id="3b3df-147">Varude blokeerimine</span><span class="sxs-lookup"><span data-stu-id="3b3df-147">Inventory blocking</span></span>](inventory-blocking.md)

