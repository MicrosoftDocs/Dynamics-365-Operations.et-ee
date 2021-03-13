---
title: Hooldusgraafik
description: Selles teemas selgitatakse hooldusgraafikut varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d235a3797b1acee9c92c3d81e8b4a20e1f7c5c75
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017947"
---
# <a name="maintenance-schedule"></a><span data-ttu-id="95585-103">Hooldusgraafik</span><span class="sxs-lookup"><span data-stu-id="95585-103">Maintenance schedule</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="95585-104">Hooldusgraafik sisaldab kõigi oodatud teostatavate ennetavate hoolduskavade, hooldusnõuete ja hoolduskordade loendit. Mõned graafiku read võivad olla teisendatud töökäskudeks.</span><span class="sxs-lookup"><span data-stu-id="95585-104">The maintenance schedule contains a list of all the expected preventive maintenance plans, maintenance requests, and maintenance rounds to be carried out. Some schedule lines may have been converted to work orders.</span></span>

<span data-ttu-id="95585-105">Neli hooldusgraafiku vaadet on veidi erinevad, olenevalt sellest, milliseid hooldusgraafiku ridu soovite näha.</span><span class="sxs-lookup"><span data-stu-id="95585-105">The four maintenance schedule views are slightly different, depending on which maintenance schedule lines you want to see.</span></span>

| <span data-ttu-id="95585-106">Menüü-üksus</span><span class="sxs-lookup"><span data-stu-id="95585-106">Menu item</span></span>                  | <span data-ttu-id="95585-107">Sisu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="95585-107">Description of contents</span></span>                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95585-108">Kogu hooldusgraafik</span><span class="sxs-lookup"><span data-stu-id="95585-108">All maintenance schedule</span></span>       | <span data-ttu-id="95585-109">Kuvatakse kõiki hooldusgraafiku ridu.</span><span class="sxs-lookup"><span data-stu-id="95585-109">All maintenance schedule lines are shown.</span></span>     |
| <span data-ttu-id="95585-110">Minu vara graafik</span><span class="sxs-lookup"><span data-stu-id="95585-110">My asset schedule</span></span>        | <span data-ttu-id="95585-111">Selles loendis kuvatakse kõiki hooldusgraafikute ridu, mis sisaldavad nendesse töö asukohtadesse paigaldatud varasid, millega te töötajana seotud olete (seadistatud jaotises [Hooldustöötajad ja töötajate rühmad](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="95585-111">All maintenance schedule lines containing assets installed on functional locations to which you are related as a worker (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)) are shown in this list.</span></span> |
| <span data-ttu-id="95585-112">Hooldusgraafiku ridade avamine</span><span class="sxs-lookup"><span data-stu-id="95585-112">Open maintenance schedule lines</span></span> | <span data-ttu-id="95585-113">Selles loendis kuvatakse hooldusgraafiku ridu, mille olek on "Loodud", mis tähendab, et need ei ole veel töökäsuks teisendatud ega hüljatud.</span><span class="sxs-lookup"><span data-stu-id="95585-113">Maintenance schedule lines with status "Created" - meaning they have not yet been converted to a work order or discarded - are shown in this list.</span></span>                                            |
| <span data-ttu-id="95585-114">Hooldusgraafiku kaustade avamine</span><span class="sxs-lookup"><span data-stu-id="95585-114">Open maintenance schedule pools</span></span> | <span data-ttu-id="95585-115">Selles loendis näidatakse töökäskude kogumiga seotud hooldusgraafiku ridu.</span><span class="sxs-lookup"><span data-stu-id="95585-115">Maintenance schedule lines related to a work order pool are shown in this list.</span></span>                                                                                                                  |

>[!NOTE]
><span data-ttu-id="95585-116">Kui hooldusgraafiku rida sisaldub mitmes töökäsu kogumis (vt [Töökäskude kogumid](../work-orders/work-order-pools.md)), kuvatakse ühte kirjet igas jaotise **Avatud hooldusgraafiku kogumid** kogumis.</span><span class="sxs-lookup"><span data-stu-id="95585-116">If a maintenance schedule line is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="95585-117">Seda tehakse töökäsu kogumite filtreerimisvalikute optimeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="95585-117">This is done to optimize filtering options on work order pools.</span></span>

<span data-ttu-id="95585-118">Hooldusgraafiku avamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="95585-118">To open a maintenance schedule:</span></span>

1. <span data-ttu-id="95585-119">Klõpsake **Varahaldus** > **Üldine** > **Hooldusgraafik** > **Kõik hooldusgraafikud** või **Avatud hooldusgraafiku read** või **Avatud hooldusgraafiku kogumid**.</span><span class="sxs-lookup"><span data-stu-id="95585-119">Click **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="95585-120">Hooldusgraafiku värskendamiseks klõpsake **Hoolduskava** või **Hoolduskorrad**.</span><span class="sxs-lookup"><span data-stu-id="95585-120">To update the maintenance schedule, click **Maintenance plan** or **Maintenance rounds**.</span></span> 

3. <span data-ttu-id="95585-121">Võite redigeerida hooldusgraafiku rida valides selle ja klõpsates **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="95585-121">You can edit a maintenance schedule line by selecting it and clicking **Edit**.</span></span> <span data-ttu-id="95585-122">Näiteks saate kerge vaevaga värskendada töö eest vastutava töötaja teenindustaset.</span><span class="sxs-lookup"><span data-stu-id="95585-122">For example, you can easily update the service level or the worker responsible for the job.</span></span> <span data-ttu-id="95585-123">Võite redigeerida ainult neid hooldusgraafiku ridu, mis ei ole veel töökäsuga ühendatud.</span><span class="sxs-lookup"><span data-stu-id="95585-123">You can only edit maintenance schedule lines that have not yet been connected to a work order.</span></span>

4. <span data-ttu-id="95585-124">Võite kustutada hooldusgraafiku rea valides selle loendi lehelt ja klõpsates **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="95585-124">You can delete a maintenance schedule line by selecting it in the list page and clicking **Delete**.</span></span>

5. <span data-ttu-id="95585-125">Võite hüljata hooldusgraafiku rea valides selle loendi lehelt ja klõpsates **Hülga**.</span><span class="sxs-lookup"><span data-stu-id="95585-125">You can discard a maintenance schedule line by selecting it in the list page and clicking **Discard**.</span></span> <span data-ttu-id="95585-126">See funktsioon on kasulik näiteks siis, kui varal on 2 000 km hoolduskava ja 10 000 km hoolduskava.</span><span class="sxs-lookup"><span data-stu-id="95585-126">This function is useful if, for example, an asset has a 2,000 km maintenance plan and a 10,000 km maintenance plan.</span></span> <span data-ttu-id="95585-127">Siis võite soovida hüljata 2 000 km hoolduskavast loodud rea, kui see langeb kokku 10 000 km-ga, 20 000 km-ga, 30 000 km-ga jne.</span><span class="sxs-lookup"><span data-stu-id="95585-127">Then, you may want to discard the line created from the 2,000 km maintenance plan when it coincides with 10,000 km, 20,000 km, 30,000 km, and so on.</span></span> <span data-ttu-id="95585-128">Kui hülgate hoolduskavaga seotud hooldusgraafiku rea, ei kuvata seda rida kunagi hoolduskava ajastamisel uuesti.</span><span class="sxs-lookup"><span data-stu-id="95585-128">If you discard a maintenance schedule line related to a maintenance plan, that line will never again appear when that maintenance plan is scheduled.</span></span>

6. <span data-ttu-id="95585-129">Võite valida mitu hooldusgraafiku rida jaotisest **Kõik hooldusgraafikud** ja klõpsata valikut **Töökäskude kogum**, kui soovite, et kõik valitud read sisalduksid töökäsu kogumis.</span><span class="sxs-lookup"><span data-stu-id="95585-129">You can select a number of maintenance schedule lines in **All maintenance schedule** and click **Work order pool**, if you want all selected lines to be included in the same work order pool.</span></span>

7. <span data-ttu-id="95585-130">Võite valida mitu hooldusgraafiku rida jaotises **Kõik hooldusgraafikud** või **Avatud hooldusgraafiku read** või **Avatud hooldusgraafiku kogumid** ja klõpsata valikut **Reguleeri graafikut**, kui soovita teha samu muudatusi mitmele reale.</span><span class="sxs-lookup"><span data-stu-id="95585-130">You can select a number of maintenance schedule lines in **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** and click **Adjust schedule** if you want to make the same adjustments on several lines.</span></span> <span data-ttu-id="95585-131">Võite muuta valitud hooldusgraafiku ridadega seotud oodatud alguse- ja lõppkuupäevi, teenindustaset ja vastutavat hooldustöötajate rühma või vastutavat hooldustöötajat.</span><span class="sxs-lookup"><span data-stu-id="95585-131">You can change expected start and end dates, service level, and the responsible maintenance worker group or responsible maintenance worker related to the selected maintenance schedule lines.</span></span>

- <span data-ttu-id="95585-132">Kui hooldusgraafiku rida on seotud töökäsuga, kuvatakse töökäsu IDd väljal **Töökäsk**.</span><span class="sxs-lookup"><span data-stu-id="95585-132">When a maintenance schedule line has been related to a work order, the work order ID will be displayed in the **Work order** field.</span></span>  
- <span data-ttu-id="95585-133">Varale saate hoolduskavasid valida jaotise **Kõik varad** üksikasjade vaate > kiirkaardil **Vara hoolduskavad**.</span><span class="sxs-lookup"><span data-stu-id="95585-133">In **All assets** details view > **Asset maintenance plans** FastTab, you can select maintenance plans for the asset.</span></span> <span data-ttu-id="95585-134">Hiljem, kui kustutate jaotise **Kõik varad** varaga seotud hoolduskava rea, kustutate automaatselt kõik hooldusgraafiku read olekuga "Loodud", mis on loodud selle hoolduskava põhjal.</span><span class="sxs-lookup"><span data-stu-id="95585-134">Later, if you delete a maintenance plan line related to an asset in **All assets**, you also automatically delete all maintenance schedule lines with status "Created" that have been created based on that maintenance plan.</span></span> <span data-ttu-id="95585-135">Vaadake ka jaotist [Vara loomine](../objects/create-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="95585-135">See also [Create an asset](../objects/create-an-object.md).</span></span>

<span data-ttu-id="95585-136">Alloleval joonisel on kujutatud jaotise **Kõik hooldusgraafikud** loendi lehte.</span><span class="sxs-lookup"><span data-stu-id="95585-136">The illustration below shows the **All maintenance schedule** list page.</span></span>

![Joonis 1](media/16-preventive-maintenance.png)

