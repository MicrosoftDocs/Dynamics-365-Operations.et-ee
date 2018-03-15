---
title: Hooldusintervallid
description: "Hooldusintervall näitab sagedust, millega hooldustellimuse ridu hooldusleppe ridade jaoks hooldustellimuste automaatsel loomisel luuakse."
author: YuyuScheller
manager: AnnBe
ms.date: 02/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 4ea10e4c0fbfd21538bba16d2b01deb3e4b3a10d
ms.openlocfilehash: 4a51a3c3483e81cefdaf3d8e62a4f1f47fcd706b
ms.contentlocale: et-ee
ms.lasthandoff: 02/20/2018

---

# <a name="service-intervals"></a><span data-ttu-id="aed6b-103">Hooldusintervallid</span><span class="sxs-lookup"><span data-stu-id="aed6b-103">Service intervals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="aed6b-104">Hooldusleppe intervall näitab sagedust, millega hooldustellimuse ridu hooldusleppe ridade jaoks hooldustellimuste automaatsel loomisel luuakse.</span><span class="sxs-lookup"><span data-stu-id="aed6b-104">The service agreement interval indicates the frequency with which service order lines are created for service agreement lines when you create service orders automatically.</span></span>

<span data-ttu-id="aed6b-105">Kui te loote hooldustellimusi automaatselt, luuakse hooldustellimuse read vastavalt intervallile, mis te olete hooldusleppe rea jaoks määranud leppe rea alguskuupäevast alates.</span><span class="sxs-lookup"><span data-stu-id="aed6b-105">When you create service orders automatically, service order lines are created according to the interval that you have specified for the service agreement line from the start date of the agreement line.</span></span>

<span data-ttu-id="aed6b-106">Kui hooldusleppe rea väli **Intervall** on lehel **Hoolduslepped** tühi, on rida ühekordne sündmus ja seda ei kasutata korduvalt hooldustellimuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="aed6b-106">If the **Interval** field of a service agreement line in the **Service agreements** page is blank, the line is a one-time event, and it is not used to create service orders repeatedly.</span></span>

## <a name="example"></a><span data-ttu-id="aed6b-107">Näide</span><span class="sxs-lookup"><span data-stu-id="aed6b-107">Example</span></span>

<span data-ttu-id="aed6b-108">See näide illustreerib, kuidas hooldusintervall hooldusleppe ja hooldustellimuse ridasid hooldustellimuses mõjutab.</span><span class="sxs-lookup"><span data-stu-id="aed6b-108">This example illustrates how a service interval will affect service agreement lines and service order lines on a service order.</span></span>

### <a name="create-a-service-agreement"></a><span data-ttu-id="aed6b-109">Hooldusleppe loomine.</span><span class="sxs-lookup"><span data-stu-id="aed6b-109">Create a service agreement</span></span>

<span data-ttu-id="aed6b-110">Esmalt looge hoolduslepe ja seadke suvand **Hooldustellimuste ühendamine** väärtusele **Hooldusleppega**.</span><span class="sxs-lookup"><span data-stu-id="aed6b-110">First, you create a service agreement and set the **Combine service orders** option to **By service agreement**.</span></span>

1. <span data-ttu-id="aed6b-111">Klõpsake valikut **Hoolduslepped**</span><span class="sxs-lookup"><span data-stu-id="aed6b-111">Click **Service agreements**</span></span>
2. <span data-ttu-id="aed6b-112">Uue hooldusleppe loomiseks klõpsake **toimingupaani** vahekaardi **Hoolduslepe** grupis **Uus** valikut **Hoolduslepe**.</span><span class="sxs-lookup"><span data-stu-id="aed6b-112">On the **Action Pane**, on the **Service agreement** tab, in the **New** group, click **Service agreement** to create a new service agreement.</span></span>
3. <span data-ttu-id="aed6b-113">Sisestage kirjeldus, valige väljal **Projekti ID** projekt ja sisestage kuupäev väljale **Alguskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="aed6b-113">Enter a description, select a project in the **Project ID** field, and enter a date in the **Start date** field.</span></span>
4. <span data-ttu-id="aed6b-114">Väljal **Hooldustellimuste ühendamine** valige **Hooldusleppega**.</span><span class="sxs-lookup"><span data-stu-id="aed6b-114">In the **Combine service orders** field, select **By service agreement**.</span></span>

<span data-ttu-id="aed6b-115">Olete loonud järgmise hooldusleppe.</span><span class="sxs-lookup"><span data-stu-id="aed6b-115">You have now created the following service agreement:</span></span>

| <span data-ttu-id="aed6b-116">Project</span><span class="sxs-lookup"><span data-stu-id="aed6b-116">Project</span></span>      | <span data-ttu-id="aed6b-117">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="aed6b-117">Start date</span></span>                                                                         |
|--------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="aed6b-118">Teie projekt</span><span class="sxs-lookup"><span data-stu-id="aed6b-118">Your project</span></span> | <span data-ttu-id="aed6b-119">Projektile määratud kuupäev.</span><span class="sxs-lookup"><span data-stu-id="aed6b-119">The date you specified for the project.</span></span> <span data-ttu-id="aed6b-120">Selles näites on kasutatud tänast kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="aed6b-120">In this example, the current date is used.</span></span> |

### <a name="create-a-service-agreement-line"></a><span data-ttu-id="aed6b-121">Hooldusleppe rea loomine</span><span class="sxs-lookup"><span data-stu-id="aed6b-121">Create a service agreement line</span></span>

<span data-ttu-id="aed6b-122">Järgmiseks loote hooldusleppe rea kande tüübiga **Tund**.</span><span class="sxs-lookup"><span data-stu-id="aed6b-122">Next, you create a service agreement line that has the transaction type **Hour**.</span></span>

<span data-ttu-id="aed6b-123">Selle näite osa lõpetamiseks peate lehel **Hooldusintervallid** looma 10-päevase hooldusintervalli.</span><span class="sxs-lookup"><span data-stu-id="aed6b-123">To complete this part of the example, you must create a service interval of 10 days in the **Service intervals** page.</span></span> 

1. <span data-ttu-id="aed6b-124">Valige äsja loodud hoolduslepe.</span><span class="sxs-lookup"><span data-stu-id="aed6b-124">Select the service agreement that you just created.</span></span> 
2. <span data-ttu-id="aed6b-125">Kiirkaardil **Read** klõpsake nuppu **Lisamine** lehe **Hoolduslepped** alumisel paanil uue rea loomiseks.</span><span class="sxs-lookup"><span data-stu-id="aed6b-125">On the **Lines** FastTab, click the **Add** button to create a new line in the lower pane of the **Service agreements** page.</span></span>
3. <span data-ttu-id="aed6b-126">Väljal **Kande tüüp** valige **Tund**.</span><span class="sxs-lookup"><span data-stu-id="aed6b-126">In the **Transaction type** field, select **Hour**.</span></span>
4. <span data-ttu-id="aed6b-127">Väljal **Töötaja** valige töötaja, kes hooldust teostab.</span><span class="sxs-lookup"><span data-stu-id="aed6b-127">In the **Worker** field, select the worker who will deliver the service.</span></span>
5. <span data-ttu-id="aed6b-128">Väljal **Hooldusintervall** valige 10-päevane intervall.</span><span class="sxs-lookup"><span data-stu-id="aed6b-128">In the **Service interval** field, select the 10 days interval.</span></span>

<span data-ttu-id="aed6b-129">Olete loonud järgmise teabega hooldusleppe rea.</span><span class="sxs-lookup"><span data-stu-id="aed6b-129">You have now created a service agreement line with the following information:</span></span>

| <span data-ttu-id="aed6b-130">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="aed6b-130">Transaction type</span></span> | <span data-ttu-id="aed6b-131">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="aed6b-131">Start date</span></span>                               | <span data-ttu-id="aed6b-132">Teenuse intervall</span><span class="sxs-lookup"><span data-stu-id="aed6b-132">Service interval</span></span> |
|------------------|------------------------------------------|------------------|
| <span data-ttu-id="aed6b-133">Tund</span><span class="sxs-lookup"><span data-stu-id="aed6b-133">Hour</span></span>             | <span data-ttu-id="aed6b-134">Tänane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="aed6b-134">The current date.</span></span>                        | <span data-ttu-id="aed6b-135">Iga 10 päeva järel</span><span class="sxs-lookup"><span data-stu-id="aed6b-135">Every 10 days</span></span>    |
| <span data-ttu-id="aed6b-136">Töötaja</span><span class="sxs-lookup"><span data-stu-id="aed6b-136">Worker</span></span>           | <span data-ttu-id="aed6b-137">Hooldust teostav töötaja.</span><span class="sxs-lookup"><span data-stu-id="aed6b-137">The worker who will perform the service.</span></span> |                  |

<span data-ttu-id="aed6b-138">Rea jaoks ei ole määratud kellaaja akent.</span><span class="sxs-lookup"><span data-stu-id="aed6b-138">There is no time window specified for the line.</span></span> 

### <a name="create-planned-service-orders"></a><span data-ttu-id="aed6b-139">Planeeritud hooldustellimuste loomine</span><span class="sxs-lookup"><span data-stu-id="aed6b-139">Create planned service orders</span></span>

<span data-ttu-id="aed6b-140">Nüüd saate luua tuleval kuul planeeritud hooldustellimusi ja hooldustellimuste ridasid.</span><span class="sxs-lookup"><span data-stu-id="aed6b-140">You can now create planned service orders and service order lines for the coming month.</span></span>

1. <span data-ttu-id="aed6b-141">Lehe **Hoolduslepped** **toimingupaanil**, vahekaardil **Tarnimine** klõpsake valikut **Planeeritud hooldustellimused**.</span><span class="sxs-lookup"><span data-stu-id="aed6b-141">In the **Service agreements** page, on the **Action Pane**, on the **Deliver** tab, click **Planned service orders**.</span></span>
2. <span data-ttu-id="aed6b-142">Lehel **Hooldustellimuste loomine** sisestage väljale **Alguskuupäev** tänane kuupäev ning väljale **Lõppkuupäev** tänasest kuupäevast üks kuu hilisem kuupäev.</span><span class="sxs-lookup"><span data-stu-id="aed6b-142">In the **Create service orders** page, enter the current date in the **From date** field and a date that is one month from the current date in the **To date** field.</span></span>
3. <span data-ttu-id="aed6b-143">Seadke liugur **Tund** asendisse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="aed6b-143">Set the **Hour** slider to **Yes**.</span></span> 
4. <span data-ttu-id="aed6b-144">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="aed6b-144">Click **OK**.</span></span>

<span data-ttu-id="aed6b-145">Kuna hooldustellimusel ei toimu grupeerimist (määratud suvandiga **Hooldusleppega** moodulis **Hooldustellimuste ühendamine**), luuakse iga hooldustellimuse kohta üks hooldustellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="aed6b-145">Because there is no grouping on the service order (defined by the **By service agreement** option in the **Combine service orders** field), one service order line is created per service order.</span></span>

### <a name="service-orders-created"></a><span data-ttu-id="aed6b-146">Loodud hooldustellimused</span><span class="sxs-lookup"><span data-stu-id="aed6b-146">Service orders created</span></span>

<span data-ttu-id="aed6b-147">Dialoogiaknas **Hooldustellimuste loomine** määratud ajavahemikus on loodud kolm hooldustellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="aed6b-147">Three service order lines have been created within the time frame that you specified in the **Create service orders** dialog box.</span></span> <span data-ttu-id="aed6b-148">Hooldustellimuse ridasid saate vaadata lehel **Hoolduslepped** (**Toimingupaan** \> vahekaart **Tarnimine** \> nupp **Kuvamine**).</span><span class="sxs-lookup"><span data-stu-id="aed6b-148">You can view the service order lines in the **Service agreements** page (**Action Pane** \> **Deliver** tab \>**View** button).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aed6b-149">Seotud teemad</span><span class="sxs-lookup"><span data-stu-id="aed6b-149">Related topics</span></span>

[<span data-ttu-id="aed6b-150">Hooldusintervallide seadistamine</span><span class="sxs-lookup"><span data-stu-id="aed6b-150">Set up service intervals</span></span>](set-up-service-intervals.md)  


