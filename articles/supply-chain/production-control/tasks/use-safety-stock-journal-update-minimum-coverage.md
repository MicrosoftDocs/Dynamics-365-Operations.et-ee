--- 
title: Puhvervaru abil minimaalse laovaru uuendamine
description: "See protseduur näitab, kuidas arvutada varasemate kannete põhjal minimaalse laovaru soovitusi ja uuendada siis soovituste abil kauba laovaru."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 7a6e217d476cedc0318c382e12b7dc2036e557c3
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="5713a-103">Puhvervaru abil minimaalse laovaru uuendamine</span><span class="sxs-lookup"><span data-stu-id="5713a-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5713a-104">See protseduur näitab, kuidas arvutada varasemate kannete põhjal minimaalse laovaru soovitusi ja uuendada siis soovituste abil kauba laovaru.</span><span class="sxs-lookup"><span data-stu-id="5713a-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="5713a-105">Seda tehakse puhvervaru töölehe abil.</span><span class="sxs-lookup"><span data-stu-id="5713a-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="5713a-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="5713a-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="5713a-107">See ülesanne on mõeldud tootmise plaanijale minimaalsete laovarude säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="5713a-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="5713a-108">Uue puhvervaru töölehe nime loomine</span><span class="sxs-lookup"><span data-stu-id="5713a-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="5713a-109">Avage Puhvervaru töölehe nimed.</span><span class="sxs-lookup"><span data-stu-id="5713a-109">Go to Safety stock journal names.</span></span>
2. <span data-ttu-id="5713a-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5713a-110">Click New.</span></span>
3. <span data-ttu-id="5713a-111">Tippige väljale Nimi väärtus Materjal.</span><span class="sxs-lookup"><span data-stu-id="5713a-111">In the Name field, type 'Material'.</span></span>
4. <span data-ttu-id="5713a-112">Tippige väljale Kirjeldus väärtus Materjal.</span><span class="sxs-lookup"><span data-stu-id="5713a-112">In the Description field, type 'Material'.</span></span>
5. <span data-ttu-id="5713a-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5713a-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="5713a-114">Puhvervaru töölehe loomine</span><span class="sxs-lookup"><span data-stu-id="5713a-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="5713a-115">Avage Puhvervaru arvutamine.</span><span class="sxs-lookup"><span data-stu-id="5713a-115">Go to Safety stock calculation.</span></span>
2. <span data-ttu-id="5713a-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="5713a-116">Click New.</span></span>
3. <span data-ttu-id="5713a-117">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="5713a-117">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="5713a-118">Valige puhvervaru töölehe nimi, mille lõite, nt Materjal.</span><span class="sxs-lookup"><span data-stu-id="5713a-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="5713a-119">Klõpsake suvandit Loo read.</span><span class="sxs-lookup"><span data-stu-id="5713a-119">Click Create lines.</span></span>
5. <span data-ttu-id="5713a-120">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="5713a-120">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="5713a-121">Määrake kuupäevaks 2015-01-02.</span><span class="sxs-lookup"><span data-stu-id="5713a-121">Set the date to '2015-01-02'.</span></span>  
6. <span data-ttu-id="5713a-122">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="5713a-122">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="5713a-123">Määrake kuupäevaks 2015-12-30.</span><span class="sxs-lookup"><span data-stu-id="5713a-123">Set the date to '2015-12-30'.</span></span>  
7. <span data-ttu-id="5713a-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5713a-124">Click OK.</span></span>
    * <span data-ttu-id="5713a-125">See loob read dimensioonidele, millel on laokanded.</span><span class="sxs-lookup"><span data-stu-id="5713a-125">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="5713a-126">Arvuta soovitus</span><span class="sxs-lookup"><span data-stu-id="5713a-126">Calculate proposal</span></span>
1. <span data-ttu-id="5713a-127">Klõpsake valikut Arvuta soovitus.</span><span class="sxs-lookup"><span data-stu-id="5713a-127">Click Calculate proposal.</span></span>
2. <span data-ttu-id="5713a-128">Tehke valik Kasuta täitmisaja jooksul keskmist väljaminekut.</span><span class="sxs-lookup"><span data-stu-id="5713a-128">Select the Use average issue during lead time option.</span></span>
3. <span data-ttu-id="5713a-129">Määrake valiku Korrutustegur väärtuseks 10.</span><span class="sxs-lookup"><span data-stu-id="5713a-129">Set Multiplication factor to '10'.</span></span>
    * <span data-ttu-id="5713a-130">Tegurit Korruta kasutatakse soovituse korrigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="5713a-130">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="5713a-131">Kuna demoandmetel on vaid mõned kanded, tuleb realistliku soovituse saamiseks tegur määrata.</span><span class="sxs-lookup"><span data-stu-id="5713a-131">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="5713a-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5713a-132">Click OK.</span></span>
    * <span data-ttu-id="5713a-133">Kerige alla M0002 ja M0003 leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="5713a-133">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="5713a-134">Vaadake veergu Arvutatud miinimumkogus.</span><span class="sxs-lookup"><span data-stu-id="5713a-134">View the Calculated minimum quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="5713a-135">Miinimumkoguse uuendamine</span><span class="sxs-lookup"><span data-stu-id="5713a-135">Update minimum quantity</span></span>
1. <span data-ttu-id="5713a-136">Sisestage number väljale Uus miinimumkogus.</span><span class="sxs-lookup"><span data-stu-id="5713a-136">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="5713a-137">Uuendage väärtust Uus miinimumkogus nii, et see vastaks väärtusele jaotises Arvutatud miinimumkogus.</span><span class="sxs-lookup"><span data-stu-id="5713a-137">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="5713a-138">Kui Arvutatud miinimum on null, võite sisestada soovitud tulevase väärtuse.</span><span class="sxs-lookup"><span data-stu-id="5713a-138">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="5713a-139">Näiteks võite sisestada sellele väljale väärtuse Arvutatud miinimumkogus M0002 kohta, millel on ladu 12.</span><span class="sxs-lookup"><span data-stu-id="5713a-139">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="5713a-140">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5713a-140">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5713a-141">Näiteks võite valida M0002, millel on ladu 12.</span><span class="sxs-lookup"><span data-stu-id="5713a-141">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="5713a-142">Sisestage number väljale Uus miinimumkogus.</span><span class="sxs-lookup"><span data-stu-id="5713a-142">In the New minimum quantity field, enter a number.</span></span>
    * <span data-ttu-id="5713a-143">Uuendage väärtust Uus miinimumkogus nii, et see vastaks väärtusele jaotises Arvutatud miinimumkogus.</span><span class="sxs-lookup"><span data-stu-id="5713a-143">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="5713a-144">Kui Arvutatud miinimum on null, võite sisestada soovitud tulevase väärtuse.</span><span class="sxs-lookup"><span data-stu-id="5713a-144">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="5713a-145">Uue miinimumkoguse sisestamine ja tulemuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="5713a-145">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="5713a-146">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="5713a-146">Click Post.</span></span>
2. <span data-ttu-id="5713a-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5713a-147">Click OK.</span></span>
3. <span data-ttu-id="5713a-148">Klõpsake, et järgida linki väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="5713a-148">Click to follow the link in the Item number field.</span></span>
4. <span data-ttu-id="5713a-149">Klõpsake, et järgida linki väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="5713a-149">Click to follow the link in the Item number field.</span></span>
5. <span data-ttu-id="5713a-150">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="5713a-150">On the Action Pane, click Plan.</span></span>
6. <span data-ttu-id="5713a-151">Klõpsake valikut Kauba laovarud.</span><span class="sxs-lookup"><span data-stu-id="5713a-151">Click Item coverage.</span></span>
    * <span data-ttu-id="5713a-152">Pange tähele, et miinimumkoguseks on määratud uus miinimumkogus puhvervaru töölehelt.</span><span class="sxs-lookup"><span data-stu-id="5713a-152">Notice that the Minimum quantity has been updated with the new minimum quantity from the safety stock journal.</span></span>  


