---
title: Vahelaoorderid
description: See teema kirjeldab vahelaoorderite kasutamist varude blokeerimiseks.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 523e51c705d76b6e8624887292395f8f239bcb65
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "362575"
---
# <a name="quarantine-orders"></a><span data-ttu-id="ee71e-103">Vahelaoorderid</span><span class="sxs-lookup"><span data-stu-id="ee71e-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee71e-104">See teema kirjeldab vahelaoorderite kasutamist varude blokeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="ee71e-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="ee71e-105">Vahelaoordereid saab kasutada varude blokeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="ee71e-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="ee71e-106">Näiteks võib olla vaja kvaliteedikontrolliks kaubad vahelattu paigutada.</span><span class="sxs-lookup"><span data-stu-id="ee71e-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="ee71e-107">Karantiinis olevad kaubad edastatakse vahelattu.</span><span class="sxs-lookup"><span data-stu-id="ee71e-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="ee71e-108">**Märkus:** täpsema laohalduse protsesside kasutamisel (laohalduse moodulis) kasutatakse vahelao tellimuse töötlemist ainult müügi tagastustellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="ee71e-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="ee71e-109">Vabade laokaupade paigutamine vahelattu</span><span class="sxs-lookup"><span data-stu-id="ee71e-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="ee71e-110">Kui saadate kaubad vahelattu, saate luua vahelaoorderid käsitsi või seadistada süsteemi looma sissetuleva töötluse ajal vahelaoordereid automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ee71e-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="ee71e-111">Vahelaoorderite automaatseks loomiseks tehke valik **Vahelao haldus** vahekaardil **Varude poliitikad** lehel **Kauba mudeligrupid**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="ee71e-112">Peate määrama vastuvõtvatele ladudele ka vaikevahelao väljal **Vaheladu**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="ee71e-113">Kaubad pannakse Microsoft Dynamics 365 for Finance and Operationsis automaatselt vahelattu, kui füüsiliselt vaba kaubavaru tootmistellimusel või ostutellimusel salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="ee71e-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="ee71e-114">Selline liikumine toimub, kuna vahelaoorderi olekuks määratakse **Alustatud**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="ee71e-115">Kui loote vahelaoorderid käsitsi, ei pea kaupa seotud kauba mudeligrupis vahelao halduseks seadistama.</span><span class="sxs-lookup"><span data-stu-id="ee71e-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="ee71e-116">Selle protsessi jaoks peate määrama vaba kaubavaru, mis tuleks vahelattu paigutada, ja kasutatava vahelao.</span><span class="sxs-lookup"><span data-stu-id="ee71e-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="ee71e-117">Protsessi plaanimisel saate kasutada abivahendina vahelaoorderi olekuid.</span><span class="sxs-lookup"><span data-stu-id="ee71e-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="ee71e-118">Vahelaoorderi olekud</span><span class="sxs-lookup"><span data-stu-id="ee71e-118">Quarantine order statuses</span></span>
<span data-ttu-id="ee71e-119">Vahelaoorderite olek võib olla järgmine:</span><span class="sxs-lookup"><span data-stu-id="ee71e-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="ee71e-120">Loodud</span><span class="sxs-lookup"><span data-stu-id="ee71e-120">Created</span></span>
-   <span data-ttu-id="ee71e-121">Alustatud</span><span class="sxs-lookup"><span data-stu-id="ee71e-121">Started</span></span>
-   <span data-ttu-id="ee71e-122">Lõpetamine kinnitatud</span><span class="sxs-lookup"><span data-stu-id="ee71e-122">Reported as finished</span></span>
-   <span data-ttu-id="ee71e-123">Lõpetatud</span><span class="sxs-lookup"><span data-stu-id="ee71e-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="ee71e-124">Loodud</span><span class="sxs-lookup"><span data-stu-id="ee71e-124">Created</span></span>

<span data-ttu-id="ee71e-125">Kui vahelaoorder on loodud käsitsi, kuid kaup ei ole veel vahelattu pandud, siis on vahelaoorderi olek **Loodud**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="ee71e-126">Luuakse kaks laokannet.</span><span class="sxs-lookup"><span data-stu-id="ee71e-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="ee71e-127">Üks kanne on väljaminekukanne, mille olek võib olla **Tellimusel**, **Füüsiliselt reserveeritud** või **Komplekteeritud**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="ee71e-128">Teine kanne on sissetulekukanne, mille olek võib vahelaos olla **Tellitud** või **Registreeritud**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="ee71e-129">Saate reserveerida, komplekteerida ja registreerida varude värskendusi tavaliste protsesside abil.</span><span class="sxs-lookup"><span data-stu-id="ee71e-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="ee71e-130">Alustatud</span><span class="sxs-lookup"><span data-stu-id="ee71e-130">Started</span></span>

<span data-ttu-id="ee71e-131">Kui vahelaoorderi oleks on **Alustatud**, edastatakse varud tavalisest laost vahelattu ja luuakse kaks laokannet.</span><span class="sxs-lookup"><span data-stu-id="ee71e-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="ee71e-132">Ühe kande olek on **Maha arvatud** ja teise kande olek on **Vastu võetud**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="ee71e-133">Samal ajal luuakse kaks laokannet tagastuse käsitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="ee71e-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="ee71e-134">Need kanded ei ole kuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="ee71e-134">These transactions aren't dated.</span></span> <span data-ttu-id="ee71e-135">Ühe kande olek on **Füüsiliselt reserveeritud** ja teise kande olek on **Tellitud**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="ee71e-136">Lõpetamine kinnitatud</span><span class="sxs-lookup"><span data-stu-id="ee71e-136">Reported as finished</span></span>

<span data-ttu-id="ee71e-137">Kui klõpsate nuppu **Kinnita lõpetamine**, saate kinnitada alustatud vahelaoorder lõpetamise.</span><span class="sxs-lookup"><span data-stu-id="ee71e-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="ee71e-138">Kaup on vahelaost väljastatud, kuid ei ole veel tavalisse lattu tagasi viidud.</span><span class="sxs-lookup"><span data-stu-id="ee71e-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="ee71e-139">Tavalisse lattu tagasiviimist saab töödelda saabuva kauba töölehe kaudu, mille saab käivitada lõpetatuna kinnitamise protsessi ajal.</span><span class="sxs-lookup"><span data-stu-id="ee71e-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="ee71e-140">Lõpetatud</span><span class="sxs-lookup"><span data-stu-id="ee71e-140">Ended</span></span>

<span data-ttu-id="ee71e-141">Kui vahelaoorder lõppeb, viiakse kaup vahelaost tagasi tavalisse lattu.</span><span class="sxs-lookup"><span data-stu-id="ee71e-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="ee71e-142">Kauba kande olekuks on vahelaos **Müüdud** ja tavalises laos **Ostetud**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="ee71e-143">Vahelaoorderi praak</span><span class="sxs-lookup"><span data-stu-id="ee71e-143">Quarantine order scrap</span></span>
<span data-ttu-id="ee71e-144">Vahelaoorderi protsessi osana on võimalik ka varusid praakida.</span><span class="sxs-lookup"><span data-stu-id="ee71e-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="ee71e-145">Praagi töötlemisel määratakse vahelao väljaminekukandega varude olekuks **Müüdud**.</span><span class="sxs-lookup"><span data-stu-id="ee71e-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="ee71e-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ee71e-146">Additional resources</span></span>
--------

[<span data-ttu-id="ee71e-147">Varude blokeerimine</span><span class="sxs-lookup"><span data-stu-id="ee71e-147">Inventory blocking</span></span>](inventory-blocking.md)
