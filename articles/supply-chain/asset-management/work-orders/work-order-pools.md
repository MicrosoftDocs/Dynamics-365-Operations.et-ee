---
title: Töökäsu kaustad
description: Selles teemas kirjeldatakse, kuidas töötada varahalduses töökäsu kaustadega.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: afea5b8d0f958c3ab53d6cef8c9a0e9030d7c67b
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/16/2021
ms.locfileid: "5017513"
---
# <a name="work-order-pools"></a><span data-ttu-id="0f13d-103">Töökäsu kaustad</span><span class="sxs-lookup"><span data-stu-id="0f13d-103">Work order pools</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="0f13d-104">Töökäsu kaustu saate kasutada töökäskude grupeerimiseks, millel on midagi ühist.</span><span class="sxs-lookup"><span data-stu-id="0f13d-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="0f13d-105">Siin on mõned näited asjadest, mille jaoks saate luua töökäskude kaustu.</span><span class="sxs-lookup"><span data-stu-id="0f13d-105">Here are some examples of things that you can create  work order pools for:</span></span>

- <span data-ttu-id="0f13d-106">Töömeeskonnad, näiteks hooldustööde meeskond A või hooldustööde meeskond B</span><span class="sxs-lookup"><span data-stu-id="0f13d-106">Work crews, for example, Maintenance Crew A or Maintenance Crew B</span></span>  

- <span data-ttu-id="0f13d-107">Kutseoskused, nagu elektrikud või torumehed</span><span class="sxs-lookup"><span data-stu-id="0f13d-107">Professional skills, such as electricians or plumbers</span></span>  

- <span data-ttu-id="0f13d-108">Füüsilised asukohad</span><span class="sxs-lookup"><span data-stu-id="0f13d-108">Physical locations</span></span>  

- <span data-ttu-id="0f13d-109">Ajagraafikud, nagu nädalad või muud perioodid</span><span class="sxs-lookup"><span data-stu-id="0f13d-109">Time schedules, such as weeks or other periods</span></span>  

<span data-ttu-id="0f13d-110">Kui vaja, saate panna ühe töökäsu mitmesse töökäsukausta.</span><span class="sxs-lookup"><span data-stu-id="0f13d-110">As you require, you can put one work order in multiple work order pools.</span></span>


## <a name="create-a-work-order-pool"></a><span data-ttu-id="0f13d-111">Töökäsukaustade loomine</span><span class="sxs-lookup"><span data-stu-id="0f13d-111">Create a work order pool</span></span>

<span data-ttu-id="0f13d-112">Loendilehel **Kõik töökäskude kaustad** või **Aktiivsed töökäskude kaustad** saate ülevaate oma töökäskude kaustadest ja luua uusi kaustu.</span><span class="sxs-lookup"><span data-stu-id="0f13d-112">On the **All work order pools** or **Active work order pools** list page, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="0f13d-113">Valige **Varahaldus** > **Üldine** > **Töökäskude kaustad** > **Kõik töökäskude kaustad** või **Aktiivsed töökäskude kaustad**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-113">Select **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="0f13d-114">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-114">Select **New**.</span></span>

3. <span data-ttu-id="0f13d-115">Väljale **Kaust** sisestage töökäsukausta ID.</span><span class="sxs-lookup"><span data-stu-id="0f13d-115">In the **Pool** field, enter an ID for the work order pool.</span></span>

4. <span data-ttu-id="0f13d-116">Väljale **Nimi** sisestage nimi.</span><span class="sxs-lookup"><span data-stu-id="0f13d-116">the **Name** field, enter a name.</span></span>

5. <span data-ttu-id="0f13d-117">Seadke suvandi **Aktiive** väärtuseks **Jah**, et näidata, et töökäsukaust on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="0f13d-117">Set the **Active** option to **Yes** to indicate that the work order pool is active.</span></span>

6. <span data-ttu-id="0f13d-118">Seadke suvandi **Kustuta töökäsu seosed** väärtuseks **Jah**, kui töökäsud tuleb töökäskude kaustast automaatselt eemaldada.</span><span class="sxs-lookup"><span data-stu-id="0f13d-118">Set the **Delete work order relations** option to **Yes** if work orders should automatically be removed from the work order pool.</span></span>

7. <span data-ttu-id="0f13d-119">Valige väljal **Kustuta töötsükli olek** tööoleku töötsükli olek.</span><span class="sxs-lookup"><span data-stu-id="0f13d-119">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="0f13d-120">Näiteks saab töökäsu töötsükli olekuks määrata, et automaatselt kustutatakse seosed töökäskude kaustades.</span><span class="sxs-lookup"><span data-stu-id="0f13d-120">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

    <span data-ttu-id="0f13d-121">Saate alustada töökäskude lisamist oma töökäskude kausta kohe.</span><span class="sxs-lookup"><span data-stu-id="0f13d-121">You can start adding work orders to your work order pool right away.</span></span>

8. <span data-ttu-id="0f13d-122">Tehke kiirkaardil **Töökäsud** valik **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-122">On the **Work orders** FastTab, select **Add line**.</span></span>

9. <span data-ttu-id="0f13d-123">Väljal **Töökäsk** valige töökäsk.</span><span class="sxs-lookup"><span data-stu-id="0f13d-123">In the **Work order** field, select a work order.</span></span> <span data-ttu-id="0f13d-124">Seotud väljad värskendatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="0f13d-124">The related fields are automatically updated.</span></span>

10. <span data-ttu-id="0f13d-125">Täiendavate töökäskude lisamiseks korrake samme 8 kuni 9.</span><span class="sxs-lookup"><span data-stu-id="0f13d-125">Repeat steps 8 through 9 to add more work orders.</span></span>

11. <span data-ttu-id="0f13d-126">Kui lisatud töökäsud tuleb teha kindlas järjekorras, saate käsu täpsustamiseks sisestada väljal **Sortimisjärjestus** numbrid **1**, **2**, **3** jne.</span><span class="sxs-lookup"><span data-stu-id="0f13d-126">If the work orders that you added should be done in a specific order, in the **Sort order** field, you can enter the numbers **1**, **2**, **3**, and so on, to specify that order.</span></span>

12. <span data-ttu-id="0f13d-127">Töökäsukausta kõigi töökäskude loendi vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Töökäskude kaustade kuvamisega seotud** valik **Töökäsud**, et avada loendileht **Kõik töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-127">To view a list of all the work orders that are included in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Work orders** to open the **All work orders** list page.</span></span>

13. <span data-ttu-id="0f13d-128">Hooldusgraafiku, planeerimata töökäskude ja plaanitud töökäskude täiskoormuse arvutamiseks ja vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Töökäskude kaustade kuvamisega seotud** valik **Täiskoormus**, et avada dialoogiboks **Täiskoormuse arvutamine**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-128">To calculate and view capacity load for the maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Capacity load** to open the **Calculate capacity load** dialog.</span></span>

14. <span data-ttu-id="0f13d-129">Hooldusgraafikuga, planeerimata töökäskudega ja plaanitud töökäskudega seotud kaupade (varuosad ja muud nõutavad kaubad) prognooside arvutamiseks ja vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Töökäskude kaustade kuvamisega seotud** valik **Kauba prognoos**, et avada dialoogiboks **Kauba prognoosi arvutamine**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-129">To calculate and view forecasts for items (spare parts and other required items) that are related to maintenance schedule, unscheduled work orders, and scheduled work orders, on the Action Pane, on the **Work order pool** tab, in the **View work order pool related** group, select **Item forecast** to open the **Calculate item forecast** dialog.</span></span>

15. <span data-ttu-id="0f13d-130">Töökäsukausta töökäskudega seotud ostutaotluste loendi vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Hange** valik **Töökäsu ostutaotlus**, et avada loendileht **Töökäsu ostutaotlus**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-130">To view a list of purchase requisitions that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase requisition** to open the **Work order purchase requisition** list page.</span></span>

16. <span data-ttu-id="0f13d-131">Töökäsukausta töökäskudega seotud ostutellimuste loendi vaatamiseks tehke toimingupaanil vahekaardi **Töökäskude kaust** grupis **Hange** valik **Töökäsu ost**, et avada loendileht **Töökäsu ost**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-131">To view a list of purchase orders that are related to the work orders in the work order pool, on the Action Pane, on the **Work order pool** tab, in the **Procurement** group, select **Work order purchase** to open the **Work order purchase** list page.</span></span>

>[!NOTE]
><span data-ttu-id="0f13d-132">Kui töökäsukaust ei ole enam teie tööplaanis oluline, määrake lehe **Töökäskude kaust** loendivaates selle kausta suvandi **Aktiivne** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-132">When a work order pool is no longer relevant to your work planning, set the **Active** option for that pool to **No** in the list view of the **Work order pool** page.</span></span>

<span data-ttu-id="0f13d-133">Kõigi töötaja tellimuseridade kustutamiseks seadke suvandi **Kustuta töökäsu seosed** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-133">To delete all worker order lines, set the **Delete work order relations** option to **Yes**.</span></span> <span data-ttu-id="0f13d-134">See suvand on kasulik näiteks juhul, kui soovite luua tühja kausta, mida saate hiljem kasutada teiste töökäskude jaoks.</span><span class="sxs-lookup"><span data-stu-id="0f13d-134">This option is useful if, for example, you want to create an empty pool that you can use later for other work orders.</span></span> <span data-ttu-id="0f13d-135">Kui olete hiljem valmis kasutama töökäsukausta uute töökäsusuhete loomiseks, pidage meeles, et suvandi **Kustuta töökäsu seosed** väärtuseks tuleb määrata **Ei**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-135">When you're ready to use the work order pool to create new work order relations later, remember to set the **Delete work order relations** option to **No**.</span></span>

<span data-ttu-id="0f13d-136">Alloleval joonisel on kujutatud loendilehe **Töökäskude kaust** näide.</span><span class="sxs-lookup"><span data-stu-id="0f13d-136">The illustration below shows an example of the **Work order pool** list page.</span></span>

![Joonis 1](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a><span data-ttu-id="0f13d-138">Töökäsukaustale töökäsu lisamine</span><span class="sxs-lookup"><span data-stu-id="0f13d-138">Add a work order to a work order pool</span></span>

<span data-ttu-id="0f13d-139">Nagu on kirjeldatud eelmises jaotises, saate töökäsu kaustale lisada töökäsu, kui loote selle kausta.</span><span class="sxs-lookup"><span data-stu-id="0f13d-139">As described in the previous section, you can add work orders to a work order pool when you create that pool.</span></span> <span data-ttu-id="0f13d-140">Töökäsukausta saate töökäske lisada ka loendilehel **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-140">You can also add work orders to a work order pool on the **All work orders** or **Active work orders** list page.</span></span>

1. <span data-ttu-id="0f13d-141">Valige töökäsk ja seejärel tehke toimingupaani vahekaardi **Töökäsk** grupis **Hooldamine** valik **Töökäskude kaust**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-141">Select the work order, and then, on the Action Pane, on the **Work order** tab, in the **Maintain** group, select **Work order pool**.</span></span>

2. <span data-ttu-id="0f13d-142">Valige loendist töökäsk ja klõpsake käsku **Töökäsukaust.**</span><span class="sxs-lookup"><span data-stu-id="0f13d-142">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="0f13d-143">Dialoogiaknas **Töökäskude kausta hooldamine** tehke väljal **Lisa/eemalda** valik **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-143">In the **Maintain work order pool** dialog, in the **Add/remove** field, select **Add**.</span></span>

4. <span data-ttu-id="0f13d-144">Väljal **Kaust** valige töökäsukaust.</span><span class="sxs-lookup"><span data-stu-id="0f13d-144">In the **Pool** field, select the work order pool.</span></span>

5. <span data-ttu-id="0f13d-145">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-145">Select **OK**.</span></span>

6. <span data-ttu-id="0f13d-146">Selleks, et seada lisatud töökäsud töökäsukaustas kindlasse järjekorda, valige kaust loendilehel **Kõik töökäskude kaustad** või **Aktiivsed töökäskude kaustad** ja seejärel valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-146">To put the work order that you added in a specific order in the work order pool, on the **All work order pools** or **Active work order pools** list page, select the pool, and then select **Edit**.</span></span> <span data-ttu-id="0f13d-147">Seejärel kasutage lehe **Töökäskude kaust** kiirkaardil **Töökäsud** välja **Sortimisjärjestus**, et kohandada kausta kuuluvate töökäskude sortimisjärjestust.</span><span class="sxs-lookup"><span data-stu-id="0f13d-147">Then, on the **Work order pool** page, on the **Work orders** FastTab, use the **Sort order** field to adjust the sort order of the work orders that are included in pool.</span></span>

<span data-ttu-id="0f13d-148">Töökäsukaustast mõne töökäsu eemaldamiseks korrake neid etappe, kuid valige 3. etapis **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="0f13d-148">To remove a work order from a work order pool, repeat these steps, but select **Remove** in step 3.</span></span>

