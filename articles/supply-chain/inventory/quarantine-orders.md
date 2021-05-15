---
title: Vahelaoorderid
description: See teema kirjeldab garantiitellimuste kasutamist varude blokeerimiseks.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956178"
---
# <a name="quarantine-orders"></a><span data-ttu-id="2e931-103">Vahelaoorderid</span><span class="sxs-lookup"><span data-stu-id="2e931-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e931-104">See teema kirjeldab garantiitellimuste kasutamist varude blokeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="2e931-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="2e931-105">Garantiitellimused lasevad teil varud blokeerida.</span><span class="sxs-lookup"><span data-stu-id="2e931-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="2e931-106">Näiteks võib olla vaja kvaliteedikontrolliks kaubad vahelattu paigutada.</span><span class="sxs-lookup"><span data-stu-id="2e931-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="2e931-107">Karantiinis olevad kaubad edastatakse vahelattu.</span><span class="sxs-lookup"><span data-stu-id="2e931-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="2e931-108">Edasijõudnud laohalduse protsesside kasutamisel (laohalduse moodulis) kasutatakse garantiitellimuse töötlemist ainult müügi tagastustellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="2e931-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="2e931-109">Vabade laokaupade paigutamine vahelattu</span><span class="sxs-lookup"><span data-stu-id="2e931-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="2e931-110">Kaupade garantiisse saatmisel saate kas käsitsi luua garantiitellimused või seadistada süsteemi neid sissetuleva töötluse ajal automaatselt looma.</span><span class="sxs-lookup"><span data-stu-id="2e931-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="2e931-111">Süsteemi automaatseks garantiitellimuste loomiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="2e931-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="2e931-112">Avage **Varude haldus \> Seadistus \> Varud \> Kauba mudeligrupid**.</span><span class="sxs-lookup"><span data-stu-id="2e931-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="2e931-113">Valige loendist olemasolev mudelgrupp või looge uus mudelgrupp.</span><span class="sxs-lookup"><span data-stu-id="2e931-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="2e931-114">Valige kiirkaardil **Varude poliitikad** märkeruut **Garantiihaldus**.</span><span class="sxs-lookup"><span data-stu-id="2e931-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="2e931-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2e931-115">Close the page.</span></span>
1. <span data-ttu-id="2e931-116">Peate määrama vastuvõtvatele ladudele ka vaikegarantiilao väljal **Garantiiladu**.</span><span class="sxs-lookup"><span data-stu-id="2e931-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="2e931-117">Kui laos vastuvõetuna registreeritud kaup kuulub mudelirühma, kus on valitud märkeruut **Garantii haldus**, genereerib süsteem selle jaoks garantiitellimuse.</span><span class="sxs-lookup"><span data-stu-id="2e931-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="2e931-118">Garantiitellimus annab töötajatele korralduse viia toode garantiilattu.</span><span class="sxs-lookup"><span data-stu-id="2e931-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="2e931-119">Kui loote garantiitellimusi käsitsi **Garantiitellimused** lehel, ei pea kaup olema seotud kauba mudelirühmas garantii haldamiseks seadistatud.</span><span class="sxs-lookup"><span data-stu-id="2e931-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="2e931-120">Selle protsessi jaoks peate määrama vaba kaubavaru, mis tuleks vahelattu paigutada, ja kasutatava vahelao.</span><span class="sxs-lookup"><span data-stu-id="2e931-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="2e931-121">Protsessi plaanimisel saate kasutada abivahendina vahelaoorderi olekuid.</span><span class="sxs-lookup"><span data-stu-id="2e931-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="2e931-122">Vahelaoorderi olekud</span><span class="sxs-lookup"><span data-stu-id="2e931-122">Quarantine order statuses</span></span>

<span data-ttu-id="2e931-123">Vahelaoorderite olek võib olla järgmine:</span><span class="sxs-lookup"><span data-stu-id="2e931-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="2e931-124">Loodud</span><span class="sxs-lookup"><span data-stu-id="2e931-124">Created</span></span>
- <span data-ttu-id="2e931-125">Alustatud</span><span class="sxs-lookup"><span data-stu-id="2e931-125">Started</span></span>
- <span data-ttu-id="2e931-126">Lõpetamine kinnitatud</span><span class="sxs-lookup"><span data-stu-id="2e931-126">Reported as finished</span></span>
- <span data-ttu-id="2e931-127">Lõpetatud</span><span class="sxs-lookup"><span data-stu-id="2e931-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="2e931-128">Loodud</span><span class="sxs-lookup"><span data-stu-id="2e931-128">Created</span></span>

<span data-ttu-id="2e931-129">Kui vahelaoorder on loodud käsitsi, kuid kaup ei ole veel vahelattu pandud, siis on vahelaoorderi olek **Loodud**.</span><span class="sxs-lookup"><span data-stu-id="2e931-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="2e931-130">Luuakse kaks laokannet.</span><span class="sxs-lookup"><span data-stu-id="2e931-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="2e931-131">Üks kanne on väljaminekukanne, mille olek võib olla **Tellimusel**, **Füüsiliselt reserveeritud** või **Komplekteeritud**.</span><span class="sxs-lookup"><span data-stu-id="2e931-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="2e931-132">Teine kanne on sissetulekukanne, mille olek võib vahelaos olla **Tellitud** või **Registreeritud**.</span><span class="sxs-lookup"><span data-stu-id="2e931-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="2e931-133">Saate reserveerida, komplekteerida ja registreerida varude värskendusi tavaliste protsesside abil.</span><span class="sxs-lookup"><span data-stu-id="2e931-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="2e931-134">Alustatud</span><span class="sxs-lookup"><span data-stu-id="2e931-134">Started</span></span>

<span data-ttu-id="2e931-135">Kui vahelaoorderi oleks on **Alustatud**, edastatakse varud tavalisest laost vahelattu ja luuakse kaks laokannet.</span><span class="sxs-lookup"><span data-stu-id="2e931-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="2e931-136">Ühe kande olek on **Maha arvatud** ja teise kande olek on **Vastu võetud**.</span><span class="sxs-lookup"><span data-stu-id="2e931-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="2e931-137">Samal ajal luuakse kaks laokannet tagastuse käsitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="2e931-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="2e931-138">Need kanded ei ole kuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="2e931-138">These transactions aren't dated.</span></span> <span data-ttu-id="2e931-139">Ühe kande olek on **Füüsiliselt reserveeritud** ja teise kande olek on **Tellitud**.</span><span class="sxs-lookup"><span data-stu-id="2e931-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="2e931-140">Lõpetamine kinnitatud</span><span class="sxs-lookup"><span data-stu-id="2e931-140">Reported as finished</span></span>

<span data-ttu-id="2e931-141">Alustatud garantiitellimuse lõpetatuks märkimiseks avage tellimus ja tehke tegevuspaanil valik **Märgi lõpetatuks**.</span><span class="sxs-lookup"><span data-stu-id="2e931-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="2e931-142">Kaup on garantiist väljastatud, kuid ei ole veel tavalisse lattu tagasi viidud.</span><span class="sxs-lookup"><span data-stu-id="2e931-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="2e931-143">Tagasi tavapärasesse lattu liikumist saab töödelda kauba saabumise päeviku kaudu, mida saab vormistada aruande käigus kui valmis protsessi.</span><span class="sxs-lookup"><span data-stu-id="2e931-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="2e931-144">Lõpetatud</span><span class="sxs-lookup"><span data-stu-id="2e931-144">Ended</span></span>

<span data-ttu-id="2e931-145">Kui vahelaoorder lõppeb, viiakse kaup vahelaost tagasi tavalisse lattu.</span><span class="sxs-lookup"><span data-stu-id="2e931-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="2e931-146">Kauba kande olekuks on vahelaos *Müüdud* ja tavalises laos *Ostetud*.</span><span class="sxs-lookup"><span data-stu-id="2e931-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="2e931-147">Vahelaoorderi praak</span><span class="sxs-lookup"><span data-stu-id="2e931-147">Quarantine order scrap</span></span>

<span data-ttu-id="2e931-148">Vahelaoorderi protsessi osana on võimalik ka varusid praakida.</span><span class="sxs-lookup"><span data-stu-id="2e931-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="2e931-149">Praagi töötlemisel määratakse garantiilao väljaminekukandega varude olekuks *Müüdud*.</span><span class="sxs-lookup"><span data-stu-id="2e931-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e931-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2e931-150">Additional resources</span></span>

- [<span data-ttu-id="2e931-151">Varude blokeerimine</span><span class="sxs-lookup"><span data-stu-id="2e931-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
