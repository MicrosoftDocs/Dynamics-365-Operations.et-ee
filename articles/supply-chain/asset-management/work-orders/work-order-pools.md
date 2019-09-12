---
title: Töökäsu kaustad
description: Selles teemas kirjeldatakse, kuidas töötada varahalduses töökäsu kaustadega.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875610"
---
# <a name="work-order-pools"></a><span data-ttu-id="a4ab1-103">Töökäsu kaustad</span><span class="sxs-lookup"><span data-stu-id="a4ab1-103">Work order pools</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="a4ab1-104">Töökäsu kaustu saate kasutada töökäskude grupeerimiseks, millel on midagi ühist.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-104">You can use work order pools to group work orders that have something in common.</span></span> <span data-ttu-id="a4ab1-105">Näiteks saate luua töökäsu kaustu</span><span class="sxs-lookup"><span data-stu-id="a4ab1-105">For example, you can create work order pools for</span></span>

- <span data-ttu-id="a4ab1-106">töömeeskondadele, näiteks hooldustööde meeskond A, hooldustööde meeskond B</span><span class="sxs-lookup"><span data-stu-id="a4ab1-106">work crews, for example, Maintenance Crew A, Maintenance Crew B</span></span>  

- <span data-ttu-id="a4ab1-107">Kutseoskustele, näiteks elektrikud või torumehed</span><span class="sxs-lookup"><span data-stu-id="a4ab1-107">professional skills, for example, electricians or plumbers</span></span>  

- <span data-ttu-id="a4ab1-108">füüsilisele asukohale</span><span class="sxs-lookup"><span data-stu-id="a4ab1-108">physical locations</span></span>  

- <span data-ttu-id="a4ab1-109">ajagraafikutele, nt nädalad või muud perioodid</span><span class="sxs-lookup"><span data-stu-id="a4ab1-109">time schedules, for example, weeks or other periods</span></span>  


<span data-ttu-id="a4ab1-110">Vajadusel saab ühe töökäsu paigutada mitmesse töökäsukausta.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-110">If required, one work order can be placed in many work order pools.</span></span>


## <a name="create-work-order-pool"></a><span data-ttu-id="a4ab1-111">Töökäskude kaustade loomine</span><span class="sxs-lookup"><span data-stu-id="a4ab1-111">Create work order pool</span></span>

<span data-ttu-id="a4ab1-112">Kõigis **Töökäskude kaustades** või **Aktiivsete töökäskude** kaustades saate ülevaate oma töökäskude kaustadest ja luua uusi kaustu.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-112">In **All work order pools** or **Active work order pools**, you can get an overview of your work order pools and create new pools.</span></span>

1. <span data-ttu-id="a4ab1-113">Klõpsake **Varahaldus** > **Ühised** > **Töökäskude kaustad** > **Kõik töökäskude kaustad** või **Aktiivsed töökäskude kaustad**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-113">Click **Asset management** > **Common** > **Work order pools** > **All work order pools** or **Active work order pools**.</span></span>

2. <span data-ttu-id="a4ab1-114">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-114">Click **New**.</span></span>

3. <span data-ttu-id="a4ab1-115">Sisestage töökäsu ID väljale **Kaust** ja nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-115">Insert a work order pool ID in the **Pool** field and a name in the **Name** field.</span></span>

4. <span data-ttu-id="a4ab1-116">Valige Jah nupul **Aktiivne**, et näidata, et töökäsu kaust on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-116">Select "Yes" on the **Active** toggle button to indicate that the work order pool is active.</span></span>

5. <span data-ttu-id="a4ab1-117">Kui soovite, et töökäsud töökäskude kaustast automaatselt eemaldatakse, märkige ruut **Kustuta töökäskude seosed**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-117">Select "Yes" on the **Delete work order relations** toggle button if you want work orders to be automatically removed from the work order pool.</span></span>

6. <span data-ttu-id="a4ab1-118">Valige väljal **Kustuta töötsükli olek** tööoleku töötsükli olek.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-118">In the **Delete lifecycle state** field, select the work order lifecycle state.</span></span> <span data-ttu-id="a4ab1-119">Näiteks saab töökäsu töötsükli olekuks määrata, et automaatselt kustutatakse seosed töökäskude kaustades.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-119">For example, the work order lifecycle state for completing a work order could be set to automatically delete relations to work order pools.</span></span>

7. <span data-ttu-id="a4ab1-120">Saate alustada töökäskude lisamist oma töökäskude kausta kohe.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-120">You can start adding work orders to your work order pool right away.</span></span> <span data-ttu-id="a4ab1-121">Klõpsake kiirkaardil **Töökäsud** valikut **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-121">On the **Work orders** FastTab, click **Add line**.</span></span>

8. <span data-ttu-id="a4ab1-122">Väljal **Töökäsu tüüp** valige töökäsu tüüp.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-122">Select a work order in the **Work order** field.</span></span> <span data-ttu-id="a4ab1-123">Seotud väljad värskendatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-123">The related fields are automatically updated.</span></span>

9. <span data-ttu-id="a4ab1-124">Kui soovite lisada rohkem töökäske, korrake samme 7-8.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-124">Repeat steps 7-8 if you want to add more work orders.</span></span>

10. <span data-ttu-id="a4ab1-125">Väljal **Sorteerimisjärjestus**saate näidata, kas töökäsud tuleb täita kindlas järjekorras.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-125">In the **Sort order** field, you can indicate if the work orders should be carried out in a certain order.</span></span> <span data-ttu-id="a4ab1-126">Sisestage numbrid 1, 2, 3 jne, et näidata valitud töökäskude kindlat järjestust.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-126">Insert numbers 1, 2, 3, and so on to indicate a specific sequence for the selected work orders.</span></span>

11. <span data-ttu-id="a4ab1-127">Klõpsake nuppu **Töökäsklused**, et näha loendit kõikidest töökäskude kausta kaasatud töökäskudest.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-127">Click the **Work orders** button to see a list of all the work orders included in the work order pool.</span></span>

12. <span data-ttu-id="a4ab1-128">Klõpsake nuppu **Võimsuse koormus** avamaks **Võimsuse koormus**, et arvutada ja vaadata võimsuse koormust hooldusgraafiku, planeerimata töökäskude ja plaanitud töökäskude jaoks.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-128">Click the **Capacity load** button to open **Capacity load** to calculate and view capacity load for maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

13. <span data-ttu-id="a4ab1-129">Klõpsake nuppu **kauba ennustus** avamaks **kauba ennustus**, et arvutada ja vaadata kaupade (varuosad ja muud vajalikud kaubad), mis on seotud hooldusgraafiku, planeerimata töökäskude ja plaanitud töökäskudega.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-129">Click the **Item forecast** button to open **Item forecast** to calculate and view forecasts for items (spare parts and other required items) related to maintenance schedule, not-scheduled work orders, and scheduled work orders.</span></span>

14. <span data-ttu-id="a4ab1-130">Klõpsake nuppu **Töökäsu ostutaotlus**, et avada loend **Töökäsu ostutaotlus** ja näha töökäsukaustas töökäskudega seotud ostutaotlusi.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-130">Click the **Work order purchase requisition** button to open the **Work order purchase requisition** list to see a list of purchase requisitions related to the work orders in the work order pool.</span></span>

15. <span data-ttu-id="a4ab1-131">Klõpsake nuppu **Töökäsu ostutaotlus**, et avada loend **Töökäsu ostutaotlus** ja näha töökäsukaustas töökäskudega seotud ostutellimusi.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-131">Click the **Work order purchase** button to open the **Work order purchase** list to see a list of purchase orders related to the work orders in the work order pool.</span></span>

>[!NOTE]
><span data-ttu-id="a4ab1-132">Kui töökäsukaust ei ole enam teie tööplaani jaoks oluline, määrake selle kausta märkekast **Aktiivne** loendi **Töökäsukaust** vaates kui Ei.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-132">When a work order pool is no longer relevant for your work planning, set the **Active** check box for that pool to "No" in the **Work order pool** list view.</span></span>

<span data-ttu-id="a4ab1-133">Valige märkeruut **Kustuta töökäsu seosed**, kui soovite kustutada kõik töökäsu read, näiteks tühja kausta loomiseks, mida saate hiljem kasutada teiste töökäskude puhul.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-133">Select the **Delete work order relations** check box if you want to delete all work order lines, for example to create an empty pool that you can later use for other work orders.</span></span> <span data-ttu-id="a4ab1-134">Pidage meeles tühjendada märkeruut **Kustuta töökäsu seosed**, kui soovite kasutada töökäsu kausta hiljem uute töökäskude seoste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-134">Remember to clear the **Delete work order relations** check box if you want to use the work order pool to create new work order relations later.</span></span>


![Joonis 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a><span data-ttu-id="a4ab1-136">Töökäsukaustale töökäsu lisamine</span><span class="sxs-lookup"><span data-stu-id="a4ab1-136">Add work order to a work order pool</span></span>

<span data-ttu-id="a4ab1-137">Nagu on kirjeldatud ülemises jaotises, saate töökäsu kaustale lisada töökäsu, kui loote kausta.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-137">As described in the section above, you can add work orders to a work order pool when you create the pool.</span></span> <span data-ttu-id="a4ab1-138">Töökäsu saate lisada ka töökäsukausta, mis pärineb ühest **Kõik töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-138">You can also add a work order to a work order pool from one of the **All work orders** list.</span></span>

1. <span data-ttu-id="a4ab1-139">Klõpsake **Varahaldus** > **Tavaline** > **Töökäsud** > **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-139">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="a4ab1-140">Valige loendist töökäsk ja klõpsake käsku **Töökäsukaust.**</span><span class="sxs-lookup"><span data-stu-id="a4ab1-140">Select the work order in the list, and click **Work order pool**.</span></span>

3. <span data-ttu-id="a4ab1-141">Valige Lisa väljal **Lisa/eemalda**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-141">Select "Add" in the **Add/remove** field.</span></span>

4. <span data-ttu-id="a4ab1-142">Valige töökäsukaust väljal **Kaust**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-142">Select the work order pool in the **Pool** field.</span></span>

5. <span data-ttu-id="a4ab1-143">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-143">Click **OK**.</span></span>

6. <span data-ttu-id="a4ab1-144">Pärast töökäsu lisamist töökäsukausta, kui soovite töökäsukausta lisada kindlasse seeriasse, avage üks töökäsukausta loendi lehtedest, valige kaust ja klõpsake käsku **Redigeeri** ning korrigeerige töökäskude sortimisjärjestust kaustas vormingul **Töökäsukaust** > kiirkaart **Töökäsud** > väli **Sortimisjärjestus**.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-144">After you have added a work order to a work order pool, if you want to place the work order in a specific sequence in the pool: Open one of the work order pools list pages, select the pool and click **Edit**, and adjust the sort order of the work orders included in pool in the **Work order pool** form > **Work orders** FastTab > **Sort order** field.</span></span>

<span data-ttu-id="a4ab1-145">Kui soovite valitud töökäsu eemaldada töökäsukaustast, valige 3. etapis käsk Eemalda.</span><span class="sxs-lookup"><span data-stu-id="a4ab1-145">If you want to remove the selected work order from a work order pool, select "Remove" in step 3.</span></span>

