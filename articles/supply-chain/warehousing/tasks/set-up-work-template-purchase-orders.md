---
title: Ostutellimuste jaoks töömalli seadistamine
description: See teema keskendub lihtsa töömalli seadistamisele, mida saab kasutada saadud kaupade paigutamiseks.
author: ShylaThompson
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3e91fe67ed97b37bfb89f5f487e2bc59c3f7bb8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216754"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="e6c9f-103">Ostutellimuste jaoks töömalli seadistamine</span><span class="sxs-lookup"><span data-stu-id="e6c9f-103">Set up a work template for purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6c9f-104">See teema keskendub lihtsa töömalli seadistamisele, mida saab kasutada saadud kaupade paigutamiseks.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-104">This topic describes how to set up a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="e6c9f-105">Töömallid määravad juhiste kogumi, mis esitatakse laotöötajale mobiilsel seadmel, kui kaupu vastuvõtualalt ära viiakse.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="e6c9f-106">Saate kasutada seda protseduuri demoettevõttes USMF nimetatud andmetega.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="e6c9f-107">Enne selle juhendi käivitamist looge töökausta ID.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="e6c9f-108">Selles näites kasutatakse töökausta ID-d nimega Sissetulev.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="e6c9f-109">See protseduur on mõeldud laohaldurile.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="e6c9f-110">Avage navigeerimispaneelil **Moodulid > Laohaldus > Seadistus > Töö > Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-110">In the navigation pane, go to **Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="e6c9f-111">Valige väljal **Töökäsu tüüp** suvand **Ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-111">In the **Work order type** field, select **Purchase orders**.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="e6c9f-112">Töömalli päise loomine</span><span class="sxs-lookup"><span data-stu-id="e6c9f-112">Create a work template header</span></span>
1. <span data-ttu-id="e6c9f-113">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-113">Select **New**.</span></span>
2. <span data-ttu-id="e6c9f-114">Sisestage arv väljale **Järjekorranumber**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-114">In the **Sequence number** field, enter a number.</span></span> <span data-ttu-id="e6c9f-115">See on järjestus, milles töömalle hinnatakse.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="e6c9f-116">Vajaduse korral saate järjestust muuta.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="e6c9f-117">Sisestage väärtus välja **Töömall**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-117">In the **Work template** field, type a value.</span></span> <span data-ttu-id="e6c9f-118">See on selle malli ainuidentifikaator.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="e6c9f-119">Tippige väärtus väljale **Töömalli kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-119">In the **Work template description** field, type a value.</span></span>
    - <span data-ttu-id="e6c9f-120">Suvandit **Kehtiv** ei märgita enne, kui olete lisanud kõik malli puhul vajaliku teabe ja klõpsanud seejärel käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-120">The **Valid** option will not be checked until you've completed all the information that's needed by the template and have then selected **Save**.</span></span>  
    - <span data-ttu-id="e6c9f-121">Töökäsu tüüpi **Ostutellimus** ei saa automaatselt töödelda, seega jätke valiku **Töötle automaatselt** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-121">A work order of type **Purchase order** cannot be automatically processed, so leave the **Automatically process** option set to **No**.</span></span>  
5. <span data-ttu-id="e6c9f-122">Tippige väärtus väljale **Töökausta ID**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-122">In the **Work pool ID** field, type a value.</span></span> <span data-ttu-id="e6c9f-123">Töökaustade ID-de abil saate töö gruppidesse korraldada.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="e6c9f-124">Siin määratud väärtus on vaikeväärtus selle malli abil loodud tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-124">The value that you set here will be the default value for any work that's created using this template.</span></span>  
6. <span data-ttu-id="e6c9f-125">Sisestage väljale **Töö prioriteet** väärtus `1`.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-125">In the **Work priority** field, enter `1`.</span></span> <span data-ttu-id="e6c9f-126">See näitab töö olulisust ja siin määratud väärtus on selle malli abil loodud töö puhul vaikeväärtus.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="e6c9f-127">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-127">Select **Save**.</span></span> <span data-ttu-id="e6c9f-128">Enne, kui saab kasutada nuppu **Päringu redigeerimine**, tuleb töömalli päis salvestada.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-128">You must save the work template header before the **Edit Query** button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="e6c9f-129">Töömalli jaoks kasutatava päringu häälestamine</span><span class="sxs-lookup"><span data-stu-id="e6c9f-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="e6c9f-130">Valige **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-130">Select **Edit query**.</span></span> <span data-ttu-id="e6c9f-131">Määrame piirangu, et malli saab kasutada ainult konkreetses laos.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-131">We'll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="e6c9f-132">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-132">Select **Add**.</span></span>
3. <span data-ttu-id="e6c9f-133">Tippige uue tea väljale **Väli** `warehouse`.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-133">In the **Field** field of the new row, type `warehouse`.</span></span>
4. <span data-ttu-id="e6c9f-134">Sisestage väärtus väljale **Kriteerium**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-134">In the **Criteria** field, type a value.</span></span>
5. <span data-ttu-id="e6c9f-135">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-135">Select **OK**.</span></span>
6. <span data-ttu-id="e6c9f-136">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-136">Select **Yes**.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="e6c9f-137">Töömalli üksikasjade häälestamine</span><span class="sxs-lookup"><span data-stu-id="e6c9f-137">Set work template details</span></span>
1. <span data-ttu-id="e6c9f-138">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-138">Select **New**.</span></span>
2. <span data-ttu-id="e6c9f-139">Tehke väljal **Töö tüüp** valik **Komplekteeri**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-139">In the **Work type** field, select **Pick**.</span></span>
3. <span data-ttu-id="e6c9f-140">Sisestage väljale **Tööklassi ID** sõna `purchase`.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-140">In the **Work class ID** field, type `purchase`.</span></span> <span data-ttu-id="e6c9f-141">Siin määratud tööklassist saab vaikeväärtus kõigile tööridadele tüübiga Komplekteerimine, mis selle malli abil luuakse.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-141">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="e6c9f-142">Töötellimuse ridadelt ei saa tööklassi alistada.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-142">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="e6c9f-143">Tööklassidega suunatakse ja/või piiratakse töötellimuse ridade tüüp, mida laotöötaja saab mobiilses seadmes töödelda.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-143">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="e6c9f-144">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-144">Select **New**.</span></span>
5. <span data-ttu-id="e6c9f-145">Väljal **Töö tüüp** valige **Paigal**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-145">In the **Work type** field, select **Put**.</span></span>
6. <span data-ttu-id="e6c9f-146">Väljale **Tööklassi ID** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-146">In the **Work class ID** field, type a value.</span></span> <span data-ttu-id="e6c9f-147">Komplekteerimise ja asetamise juhised on üks kogum.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-147">The pick and put instructions are a set.</span></span> <span data-ttu-id="e6c9f-148">Igal komplekteerimise ja asetamise kogumil peab olema sama töö klass.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-148">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="e6c9f-149">Kasutage sama töö klassi, mille komplekteerimisjuhise jaoks andsite.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-149">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="e6c9f-150">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-150">Select **Save**.</span></span> <span data-ttu-id="e6c9f-151">Pange tähele, et märkeruut **Kehtiv** on nüüd märgitud.</span><span class="sxs-lookup"><span data-stu-id="e6c9f-151">Note that the **Valid** checkbox is now checked.</span></span>  

