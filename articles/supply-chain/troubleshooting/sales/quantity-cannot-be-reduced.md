---
title: Kogust ei saa müügitellimuse tühistamisel vähendada
description: Kogust ei saa müügitellimuse tühistamisel vähendada.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1a2cc9c9fd3d085508fc652bc9ee0a352d869dee
ms.sourcegitcommit: a02d3d64c899f8554b74342d5a1856d824bf1abe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/11/2021
ms.locfileid: "6230832"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a><span data-ttu-id="35799-103">Kogust ei saa müügitellimuse tühistamisel vähendada</span><span class="sxs-lookup"><span data-stu-id="35799-103">The quantity can't be reduced when a sales order is canceled</span></span>

<span data-ttu-id="35799-104">Tõrkekood: SYS138831</span><span class="sxs-lookup"><span data-stu-id="35799-104">Error code: SYS138831</span></span>

## <a name="symptoms"></a><span data-ttu-id="35799-105">Sümptomid</span><span class="sxs-lookup"><span data-stu-id="35799-105">Symptoms</span></span>

<span data-ttu-id="35799-106">Süsteem näitab järgmist tõrketeadet:</span><span class="sxs-lookup"><span data-stu-id="35799-106">The system shows the following error message:</span></span>

> <span data-ttu-id="35799-107">Kogust ei saa vähendada.</span><span class="sxs-lookup"><span data-stu-id="35799-107">The quantity cannot be reduced.</span></span> <span data-ttu-id="35799-108">Tellimuse laokannete arv on liiga väike, kuna kogusele või osale sellest viidatakse väljaminekuorderiga või tootmistellimusega või kui see on märgitud teiste kannete suhtes.</span><span class="sxs-lookup"><span data-stu-id="35799-108">The number of inventory transactions on order is too low because the quantity or part of it is referenced by an output order or a production order or is marked against other transactions.</span></span>

## <a name="cause"></a><span data-ttu-id="35799-109">Põhjus</span><span class="sxs-lookup"><span data-stu-id="35799-109">Cause</span></span>

<span data-ttu-id="35799-110">Kui töö on seotud müügitellimusega, ei saa müügitellimust tühistada enne töö tühistamist.</span><span class="sxs-lookup"><span data-stu-id="35799-110">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="35799-111">See nõue kehtib ka juhul, kui müügitellimusega seotud töö on suletud.</span><span class="sxs-lookup"><span data-stu-id="35799-111">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

## <a name="resolution"></a><span data-ttu-id="35799-112">Lahendus</span><span class="sxs-lookup"><span data-stu-id="35799-112">Resolution</span></span>

<span data-ttu-id="35799-113">Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:</span><span class="sxs-lookup"><span data-stu-id="35799-113">To fix this issue, complete the following tasks:</span></span>

1. <span data-ttu-id="35799-114">Tühista avatud töö.</span><span class="sxs-lookup"><span data-stu-id="35799-114">Cancel open work.</span></span>
1. <span data-ttu-id="35799-115">Kustutage koorem.</span><span class="sxs-lookup"><span data-stu-id="35799-115">Delete the load.</span></span>
1. <span data-ttu-id="35799-116">Vähenda komplekteeritavat kogust.</span><span class="sxs-lookup"><span data-stu-id="35799-116">Reduce the picked quantity.</span></span>

### <a name="cancel-open-work"></a><span data-ttu-id="35799-117">Tühista avatud töö</span><span class="sxs-lookup"><span data-stu-id="35799-117">Cancel open work</span></span>

<span data-ttu-id="35799-118">Avatud töö tühistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="35799-118">To cancel open work, follow these steps.</span></span>

1. <span data-ttu-id="35799-119">Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.</span><span class="sxs-lookup"><span data-stu-id="35799-119">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="35799-120">Väljal **Töö ID** määrake töö ID, mida soovite tühistada ja millel on **Töö oleku** väärtuseks kas *Ava*, *Pooleli*, *Tühistatud*, *Kombineeritud* või *Suletud*.</span><span class="sxs-lookup"><span data-stu-id="35799-120">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="35799-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="35799-121">Select **OK**.</span></span>
1. <span data-ttu-id="35799-122">Valige **Jah**, et kinnitada, et soovite töö tühistada.</span><span class="sxs-lookup"><span data-stu-id="35799-122">Select **Yes** to confirm that you want to cancel the work.</span></span>

### <a name="delete-the-load"></a><span data-ttu-id="35799-123">Kustutage koorem</span><span class="sxs-lookup"><span data-stu-id="35799-123">Delete the load</span></span>

<span data-ttu-id="35799-124">Koorma kustutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="35799-124">To delete a load, follow these steps.</span></span>

1. <span data-ttu-id="35799-125">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="35799-125">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="35799-126">Avage asjakohane müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="35799-126">Open the relevant sales order.</span></span>
1. <span data-ttu-id="35799-127">Kiirkaardil **Müügitellimuse read** valige **Ladu \> Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="35799-127">On the **Sales order lines** FastTab, select **Warehouse \> Work details**.</span></span>
1. <span data-ttu-id="35799-128">Valige **Töö** lehel vahekaardil **Töö** grupis olev üksus **Töö** ja **Töö tühistamine**.</span><span class="sxs-lookup"><span data-stu-id="35799-128">On the **Work** page, on the Action Pane, on the **Work** tab, in the **Work** group, select **Cancel work**.</span></span>
1. <span data-ttu-id="35799-129">Veenduge, et **töö oleku** väli oleks seatud väärtusele *Tühistatud*.</span><span class="sxs-lookup"><span data-stu-id="35799-129">Confirm that the **Work status** field is set to *Canceled*.</span></span>
1. <span data-ttu-id="35799-130">Sulgege leht **Töö**.</span><span class="sxs-lookup"><span data-stu-id="35799-130">Close the **Work** page.</span></span>
1. <span data-ttu-id="35799-131">Müügitellimuse üksikasjade lehel **müügitellimuse ridade** kiirkaardil valige **Ladu \> Koormuse üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="35799-131">On the sales order details page, on the **Sales order lines** FastTab, select **Warehouse \> Load details**.</span></span>
1. <span data-ttu-id="35799-132">Valige tegumiribal suvand **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="35799-132">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="35799-133">Valige **Jah**, et kinnitada, et soovite koorma kustutada.</span><span class="sxs-lookup"><span data-stu-id="35799-133">Select **Yes** to confirm that you want to delete the load.</span></span>
1. <span data-ttu-id="35799-134">Sulgege **Koorem** leht.</span><span class="sxs-lookup"><span data-stu-id="35799-134">Close the **Load** page.</span></span>

### <a name="reduce-the-picked-quantity"></a><span data-ttu-id="35799-135">Vähenda komplekteeritavat kogust</span><span class="sxs-lookup"><span data-stu-id="35799-135">Reduce the picked quantity</span></span>

<span data-ttu-id="35799-136">Kui kogu töö on tühistatud, järgige komplekteeritud koguse vähendamiseks neid samme.</span><span class="sxs-lookup"><span data-stu-id="35799-136">After all work has been canceled, follow these steps to reduce the picked quantity.</span></span>

1. <span data-ttu-id="35799-137">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="35799-137">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="35799-138">Avage asjakohane müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="35799-138">Open the relevant sales order.</span></span>
1. <span data-ttu-id="35799-139">Kiirkaardil **Müügitellimuse read** valige **Uuenda rida \> Komplekteeri** tööriistaribalt.</span><span class="sxs-lookup"><span data-stu-id="35799-139">On the **Sales order lines** FastTab, select **Update line \> Pick** from the toolbar.</span></span>
1. <span data-ttu-id="35799-140">Valige **Komplekteeritud** leheküljel **Kanded** jaotises rida, kus on välja **Väljamineku olek** väärtuseks määratud *Komplekteeritud*.</span><span class="sxs-lookup"><span data-stu-id="35799-140">On the **Pick** page, in the **Transactions** section, select the line where the **Issue status** field is set to *Picked*.</span></span>
1. <span data-ttu-id="35799-141">Valige jaotises **Kanded** tööriistaribalt **komplekteerimisrea lisamine**.</span><span class="sxs-lookup"><span data-stu-id="35799-141">In the **Transactions** section, select **Add picking line** from the toolbar.</span></span>
1. <span data-ttu-id="35799-142">Valige jaotises **Komplekteerimise read** tööriistaribalt **Kinnita komplekteerimine**.</span><span class="sxs-lookup"><span data-stu-id="35799-142">In the **Picking lines** section, select **Confirm pick all** from the toolbar.</span></span>
1. <span data-ttu-id="35799-143">Sulgege **Komplekteeri** leht.</span><span class="sxs-lookup"><span data-stu-id="35799-143">Close the **Pick** page.</span></span>
1. <span data-ttu-id="35799-144">Valige lehe Müügitellimus tegumiriba vahekaardi **Müügitellimused** grupist **Arvuta** valik **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="35799-144">On the sales order details page, on the Action Pane, on the **Sales order** tab, in the **Maintain** group, select **Cancel**.</span></span>
1. <span data-ttu-id="35799-145">Valige **Jah**, et kinnitada, et soovite müügitellimuse tühistada.</span><span class="sxs-lookup"><span data-stu-id="35799-145">Select **Yes** to confirm that you want to cancel the sales order.</span></span>
