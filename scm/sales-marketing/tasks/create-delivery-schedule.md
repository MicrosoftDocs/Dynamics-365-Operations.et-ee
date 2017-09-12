--- 
title: Tarnegraafiku loomine
description: "Selles protseduuris näitlikustatakse, kuidas müügitellimuse jaoks tarnegraafikut luua."
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 956edeac33f8531ecebef64301f2318333000429
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-delivery-schedule"></a><span data-ttu-id="3720c-103">Tarnegraafiku loomine</span><span class="sxs-lookup"><span data-stu-id="3720c-103">Create a delivery schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3720c-104">Selles protseduuris näitlikustatakse, kuidas müügitellimuse jaoks tarnegraafikut luua.</span><span class="sxs-lookup"><span data-stu-id="3720c-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="3720c-105">Tarnegraafikut kasutatakse, kui tellimuse või pakkumise koguse puhul on nõutav mitme saadetisega tarne.</span><span class="sxs-lookup"><span data-stu-id="3720c-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="3720c-106">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="3720c-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="3720c-107">Tarnegraafiku loomine</span><span class="sxs-lookup"><span data-stu-id="3720c-107">Create delivery schedule</span></span>
1. <span data-ttu-id="3720c-108">Avage Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="3720c-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="3720c-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3720c-109">Click New.</span></span>
3. <span data-ttu-id="3720c-110">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="3720c-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="3720c-111">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3720c-111">Click OK.</span></span>
5. <span data-ttu-id="3720c-112">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="3720c-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="3720c-113">Sisestage väljale Kogus arv, mis on suurem kui 1.</span><span class="sxs-lookup"><span data-stu-id="3720c-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="3720c-114">Klõpsake valikut Müügitellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="3720c-114">Click Sales order line.</span></span>
8. <span data-ttu-id="3720c-115">Klõpsake valikut Tarnegraafik.</span><span class="sxs-lookup"><span data-stu-id="3720c-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="3720c-116">Lehel Tarnegraafik saate määrata, mitme saadetisega tellimuse rea lõplik kogus kliendile tarnitakse.</span><span class="sxs-lookup"><span data-stu-id="3720c-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="3720c-117">Vaikimisi kopeerib süsteem esimesele tarnegraafiku reale lõpliku koguse ja muud tarne üksikasjad algselt müügitellimuse realt.</span><span class="sxs-lookup"><span data-stu-id="3720c-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="3720c-118">Selles näites loome kahe saadetisega graafiku, kus teise saadetise kuupäev on nädala võrra hilisem esimese omast.</span><span class="sxs-lookup"><span data-stu-id="3720c-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="3720c-119">Sisestage väljale Kogus arv, mis moodustab osa lõplikust kogusest.</span><span class="sxs-lookup"><span data-stu-id="3720c-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="3720c-120">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="3720c-120">Click New.</span></span>
11. <span data-ttu-id="3720c-121">Sisestage järelejäänud kogus väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="3720c-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="3720c-122">Sisestage väljale Nõutav lähetuskuupäev kuupäev, mis on nädala võrra hilisem esimesel tarnereal olevast kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="3720c-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="3720c-123">Kui algsele tellimuse reale on määratud tarnegraafiku read, saate kiirkaardi Tasude teisendamine kahe suvandi abil kontrollida tarnegraafiku ridade kulude jaotust.</span><span class="sxs-lookup"><span data-stu-id="3720c-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="3720c-124">Kui valite Kopeeri brutosummad, kopeeritakse igale reale sama tasu summa.</span><span class="sxs-lookup"><span data-stu-id="3720c-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="3720c-125">Suvand Eralda tarneridadele jagab kulud tarneridade vahel võrdselt.</span><span class="sxs-lookup"><span data-stu-id="3720c-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="3720c-126">Jagada saab ainult püsikulusid, kuid muutuvkulud kopeeritakse ridadele.</span><span class="sxs-lookup"><span data-stu-id="3720c-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="3720c-127">Lehe värskendamiseks võtke kursor teiselt tarnereal ära.</span><span class="sxs-lookup"><span data-stu-id="3720c-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="3720c-128">Väljade Kokku ja Järelejäänud abil saate jälgida lõplikku kogust, mis tarnegraafiku ridadele eraldati.</span><span class="sxs-lookup"><span data-stu-id="3720c-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="3720c-129">Kui järelejäänud kogus on null, eraldati graafikusse algse rea täielik kogus.</span><span class="sxs-lookup"><span data-stu-id="3720c-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="3720c-130">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3720c-130">Click OK.</span></span>
    * <span data-ttu-id="3720c-131">Tarnegraafik on nüüd tellimuse ridadele kopeeritud.</span><span class="sxs-lookup"><span data-stu-id="3720c-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="3720c-132">Algne tellimuse rida, millele on viidatud ka nimega Äriandmete rida, teisendati tellimusreaks Tellimusrida mitme tarnega.</span><span class="sxs-lookup"><span data-stu-id="3720c-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="3720c-133">See tähistatud eristatava ikooniga ja toimib nagu tarneridade päis.</span><span class="sxs-lookup"><span data-stu-id="3720c-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="3720c-134">Kaks uut rida, millele viidatakse ka kui tarneridadele, moodustavad ühe tarnegraafiku.</span><span class="sxs-lookup"><span data-stu-id="3720c-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="3720c-135">Tellimust töödeldakse nende ridade, mitte algse rea alusel.</span><span class="sxs-lookup"><span data-stu-id="3720c-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="3720c-136">Dokumentide, nagu kinnituslehed, komplekteerimislehed, saatelehed või arved, printimisel kuvatakse ainult tarneread.</span><span class="sxs-lookup"><span data-stu-id="3720c-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="3720c-137">Tarneridadel võivad olla erinevad tarnekuupäevad, kogused, tarneviisid ja ladustamisdimensioonid, nagu koht ja ladu.</span><span class="sxs-lookup"><span data-stu-id="3720c-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="3720c-138">Tootedimensioonid peavad siiski alati vastama äriandmete real olevatele ja neid ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="3720c-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="3720c-139">Sisestage väljale Kogus arv, mis on suurem kui praegune.</span><span class="sxs-lookup"><span data-stu-id="3720c-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="3720c-140">Koguse ümberarvutuse mõju nägemiseks valige äriandmete rida.</span><span class="sxs-lookup"><span data-stu-id="3720c-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="3720c-141">Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.</span><span class="sxs-lookup"><span data-stu-id="3720c-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="3720c-142">Klõpsake valikut Saatelehe sisestamine.</span><span class="sxs-lookup"><span data-stu-id="3720c-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="3720c-143">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="3720c-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="3720c-144">Valige väljal Kogus väärtus Kõik.</span><span class="sxs-lookup"><span data-stu-id="3720c-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="3720c-145">Pange tähele, et saateleht luuakse kahe tarnegraafiku rea, mitte algse tellimuse rea jaoks.</span><span class="sxs-lookup"><span data-stu-id="3720c-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="3720c-146">Valige väljal Saatelehe printimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="3720c-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="3720c-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3720c-147">Click OK.</span></span>
23. <span data-ttu-id="3720c-148">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="3720c-148">Click Yes.</span></span>
24. <span data-ttu-id="3720c-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3720c-149">Close the page.</span></span>


