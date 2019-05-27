---
title: Ostutellimuste jaoks töömalli seadistamine
description: See protseduur keskendub lihtsa töömalli seadistamisele, mida saab kasutada saadud kaupade paigutamiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkTemplateTable, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d737f9dfd1888602266a87853e54407618ae2781
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558315"
---
# <a name="set-up-a-work-template-for-purchase-orders"></a><span data-ttu-id="2fe2e-103">Ostutellimuste jaoks töömalli seadistamine</span><span class="sxs-lookup"><span data-stu-id="2fe2e-103">Set up a work template for purchase orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2fe2e-104">See protseduur keskendub lihtsa töömalli seadistamisele, mida saab kasutada saadud kaupade paigutamiseks.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-104">This procedure focuses on the set up of a simple work template to be used when putting away received items.</span></span> <span data-ttu-id="2fe2e-105">Töömallid määravad juhiste kogumi, mis esitatakse laotöötajale mobiilsel seadmel, kui kaupu vastuvõtualalt ära viiakse.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-105">Work templates determine the set of instructions presented to the warehouse worker on a mobile device when moving items from the receiving area.</span></span> <span data-ttu-id="2fe2e-106">Saate kasutada seda protseduuri demoettevõttes USMF nimetatud andmetega.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-106">You can use this procedure with the data mentioned in demo data company USMF.</span></span> <span data-ttu-id="2fe2e-107">Enne selle juhendi käivitamist looge töökausta ID.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-107">Before you start this guide, create a work pool ID.</span></span> <span data-ttu-id="2fe2e-108">Selles näites kasutatakse töökausta ID-d nimega Sissetulev.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-108">In this example, a work pool ID called in Inbound is used.</span></span> <span data-ttu-id="2fe2e-109">See protseduur on mõeldud laohaldurile.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-109">This procedure is intended for the warehouse manager.</span></span>

1. <span data-ttu-id="2fe2e-110">Avage Laohaldus > Seadistus > Töö > Töömallid.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-110">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="2fe2e-111">Valige väljal Töötellimuse tüüp suvand Ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-111">In the Work order type field, select 'Purchase orders'.</span></span>

## <a name="create-a-work-template-header"></a><span data-ttu-id="2fe2e-112">Töömalli päise loomine</span><span class="sxs-lookup"><span data-stu-id="2fe2e-112">Create a work template header</span></span>
1. <span data-ttu-id="2fe2e-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-113">Click New.</span></span>
2. <span data-ttu-id="2fe2e-114">Sisestage number väljale Seerianumber.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-114">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="2fe2e-115">See on järjestus, milles töömalle hinnatakse.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-115">This is the sequence in which the work templates are evaluated.</span></span> <span data-ttu-id="2fe2e-116">Vajaduse korral saate järjestust muuta.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-116">You can modify the sequence, if needed.</span></span>  
3. <span data-ttu-id="2fe2e-117">Sisestage väärtus väljale Töömall.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-117">In the Work template field, type a value.</span></span>
    * <span data-ttu-id="2fe2e-118">See on selle malli ainuidentifikaator.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-118">This is the unique identifier for this template.</span></span>  
4. <span data-ttu-id="2fe2e-119">Tippige väärtus väljale Töömalli kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-119">In the Work template description field, type a value.</span></span>
    * <span data-ttu-id="2fe2e-120">Suvandit Kehtiv ei märgita enne, kui olete lisanud kõik malli puhul vajaliku teabe ja klõpsanud seejärel käsku Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-120">The Valid option will not be checked until you’ve completed all the information that's needed by the template and have then clicked Save.</span></span>  
    * <span data-ttu-id="2fe2e-121">Töötellimuse tüüpi Ostutellimus ei saa automaatselt töödelda, seega jätke valiku Töötle automaatselt suvandiks Ei.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-121">A work order of type Purchase order cannot be automatically processed, so leave the  Automatically process option set to No.</span></span>  
5. <span data-ttu-id="2fe2e-122">Tippige väärtus väljale Töökausta ID.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-122">In the Work pool ID field, type a value.</span></span>
    * <span data-ttu-id="2fe2e-123">Töökaustade ID-de abil saate töö gruppidesse korraldada.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-123">Work pool IDs allow you to organize work into groups.</span></span> <span data-ttu-id="2fe2e-124">Siin määratud väärtus on vaikeväärtus selle malli abil loodud tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-124">The value that you set here will be the default value for any work that’s created using this template.</span></span>  
6. <span data-ttu-id="2fe2e-125">Sisestage väljale Töö prioriteet väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-125">In the Work priority field, enter '1'.</span></span>
    * <span data-ttu-id="2fe2e-126">See näitab töö olulisust ja siin määratud väärtus on selle malli abil loodud töö puhul vaikeväärtus.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-126">This indicates the importance of the work, and the value that you set here will be the default for any work created using this template.</span></span>  
7. <span data-ttu-id="2fe2e-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-127">Click Save.</span></span>
    * <span data-ttu-id="2fe2e-128">Enne, kui saab kasutada nuppu Päringu redigeerimine, tuleb töömalli päis salvestada.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-128">You must save the work template header before the Edit Query button becomes available.</span></span>  

## <a name="set-up-the-query-for-the-work-template"></a><span data-ttu-id="2fe2e-129">Töömalli jaoks kasutatava päringu häälestamine</span><span class="sxs-lookup"><span data-stu-id="2fe2e-129">Set up the query for the work template</span></span>
1. <span data-ttu-id="2fe2e-130">Klõpsake suvandit Redigeeri päringut.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-130">Click Edit query.</span></span>
    * <span data-ttu-id="2fe2e-131">Määrame piirangu, et malli saab kasutada ainult konkreetses laos.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-131">We’ll set a limitation that the template can only be used within a specific warehouse.</span></span>  
2. <span data-ttu-id="2fe2e-132">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-132">Click Add.</span></span>
3. <span data-ttu-id="2fe2e-133">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-133">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2fe2e-134">Sisestage väljale Väli sõna „ladu”.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-134">In the Field field, type 'warehouse'.</span></span>
5. <span data-ttu-id="2fe2e-135">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-135">In the Criteria field, type a value.</span></span>
6. <span data-ttu-id="2fe2e-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-136">Click OK.</span></span>
7. <span data-ttu-id="2fe2e-137">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-137">Click Yes.</span></span>

## <a name="set-work-template-details"></a><span data-ttu-id="2fe2e-138">Töömalli üksikasjade häälestamine</span><span class="sxs-lookup"><span data-stu-id="2fe2e-138">Set work template details</span></span>
1. <span data-ttu-id="2fe2e-139">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-139">Click New.</span></span>
2. <span data-ttu-id="2fe2e-140">Tehke väljal Töö tüüp valik Komplekteeri.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-140">In the Work type field, select 'Pick'.</span></span>
3. <span data-ttu-id="2fe2e-141">Sisestage väljale Tööklassi ID sõna „ost”.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-141">In the Work class ID field, type 'purchase'.</span></span>
    * <span data-ttu-id="2fe2e-142">Siin määratud tööklassist saab vaikeväärtus kõigile tööridadele tüübiga Komplekteerimine, mis selle malli abil luuakse.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-142">The work class that you set here will be the default on all work lines of type Pick that are created using this template.</span></span> <span data-ttu-id="2fe2e-143">Töötellimuse ridadelt ei saa tööklassi alistada.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-143">The work class cannot be overridden from the work order lines.</span></span> <span data-ttu-id="2fe2e-144">Tööklassidega suunatakse ja/või piiratakse töötellimuse ridade tüüp, mida laotöötaja saab mobiilses seadmes töödelda.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-144">Work classes are used to direct and/or limit the type of work order lines a warehouse worker can process on a mobile device.</span></span>  
4. <span data-ttu-id="2fe2e-145">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-145">Click New.</span></span>
5. <span data-ttu-id="2fe2e-146">Valige väljal Töö tüüp suvand Pane.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-146">In the Work type field, select 'Put'.</span></span>
6. <span data-ttu-id="2fe2e-147">Sisestage väärtus väljale Tööklassi ID.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-147">In the Work class ID field, type a value.</span></span>
    * <span data-ttu-id="2fe2e-148">Komplekteerimise ja asetamise juhised on üks kogum.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-148">The pick and put instructions are a set.</span></span> <span data-ttu-id="2fe2e-149">Igal komplekteerimise ja asetamise kogumil peab olema sama töö klass.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-149">Each pick/put set must have the same work class.</span></span> <span data-ttu-id="2fe2e-150">Kasutage sama töö klassi, mille komplekteerimisjuhise jaoks andsite.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-150">Use the same work class that you provided for the pick instruction.</span></span>  
7. <span data-ttu-id="2fe2e-151">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-151">Click Save.</span></span>
    * <span data-ttu-id="2fe2e-152">Pange tähele, et märkeruut Kehtiv on nüüd märgitud.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-152">Note that the Valid checkbox is now checked.</span></span>  

