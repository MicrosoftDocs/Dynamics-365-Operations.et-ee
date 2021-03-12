---
title: Puhvervaru abil minimaalse laovaru uuendamine
description: See protseduur näitab, kuidas arvutada varasemate kannete põhjal minimaalse laovaru soovitusi ja uuendada siis soovituste abil kauba laovaru.
author: ChristianRytt
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqItemJournalName, ReqItemJournalSafetyStock, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0b0985169f7ffadbf97ed4f237c8ec11120cfc3e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980979"
---
# <a name="use-the-safety-stock-journal-to-update-minimum-coverage"></a><span data-ttu-id="962e9-103">Puhvervaru abil minimaalse laovaru uuendamine</span><span class="sxs-lookup"><span data-stu-id="962e9-103">Use the safety stock journal to update minimum coverage</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="962e9-104">See protseduur näitab, kuidas arvutada varasemate kannete põhjal minimaalse laovaru soovitusi ja uuendada siis soovituste abil kauba laovaru.</span><span class="sxs-lookup"><span data-stu-id="962e9-104">This procedure shows how to calculate minimum coverage proposals based on historical transactions and then update the item coverage with the proposals.</span></span> <span data-ttu-id="962e9-105">Seda tehakse puhvervaru töölehe abil.</span><span class="sxs-lookup"><span data-stu-id="962e9-105">This is done using the safety stock journal.</span></span> <span data-ttu-id="962e9-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="962e9-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="962e9-107">See ülesanne on mõeldud tootmise plaanijale minimaalsete laovarude säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="962e9-107">This task is intended for the production planner, to help maintain minimum coverage.</span></span>


## <a name="create-a-new-safety-stock-journal-name"></a><span data-ttu-id="962e9-108">Uue puhvervaru töölehe nime loomine</span><span class="sxs-lookup"><span data-stu-id="962e9-108">Create a new safety stock journal name</span></span>
1. <span data-ttu-id="962e9-109">Avage **Navigeerimispaneelil** **Koondplaneerimine > Seadistus > Puhvervaru töölehe nimed**.</span><span class="sxs-lookup"><span data-stu-id="962e9-109">In the **Navigation pane**, go to **Master planning > Setup > Safety stock journal names**.</span></span>
2. <span data-ttu-id="962e9-110">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="962e9-110">Click **New**.</span></span>
3. <span data-ttu-id="962e9-111">Tippige väljale **Nimi** väärtus Materjal.</span><span class="sxs-lookup"><span data-stu-id="962e9-111">In the **Name** field, type 'Material'.</span></span>
4. <span data-ttu-id="962e9-112">Tippige väljale **Kirjeldus** väärtus Materjal.</span><span class="sxs-lookup"><span data-stu-id="962e9-112">In the **Description** field, type 'Material'.</span></span>
5. <span data-ttu-id="962e9-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="962e9-113">Close the page.</span></span>

## <a name="create-a-safety-stock-journal"></a><span data-ttu-id="962e9-114">Puhvervaru töölehe loomine</span><span class="sxs-lookup"><span data-stu-id="962e9-114">Create a safety stock journal</span></span>
1. <span data-ttu-id="962e9-115">Avage **Navigeerimispaneelil** **Koondplaneerimine > Koondplaneerimine > Käivita > Puhvervaru arvutus**.</span><span class="sxs-lookup"><span data-stu-id="962e9-115">In the **Navigation pane**, go to **Master planning > Master planning > Run > Safety stock calculation**.</span></span>
2. <span data-ttu-id="962e9-116">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="962e9-116">Click **New**.</span></span>
3. <span data-ttu-id="962e9-117">Sisestage või valige väärtus väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="962e9-117">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="962e9-118">Valige puhvervaru töölehe nimi, mille lõite, nt Materjal.</span><span class="sxs-lookup"><span data-stu-id="962e9-118">Select the safety stock journal name that you created, for example, Material.</span></span>  
4. <span data-ttu-id="962e9-119">Klõpsake suvandit **Loo read**.</span><span class="sxs-lookup"><span data-stu-id="962e9-119">Click **Create lines**.</span></span>
5. <span data-ttu-id="962e9-120">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="962e9-120">In the **From date** field, enter a date.</span></span>  
6. <span data-ttu-id="962e9-121">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="962e9-121">In the **To date** field, enter a date.</span></span>
7. <span data-ttu-id="962e9-122">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="962e9-122">Click **OK**.</span></span> <span data-ttu-id="962e9-123">See loob read dimensioonidele, millel on laokanded.</span><span class="sxs-lookup"><span data-stu-id="962e9-123">This will create lines for the dimensions that have inventory transactions.</span></span>  

## <a name="calculate-proposal"></a><span data-ttu-id="962e9-124">Arvuta soovitus</span><span class="sxs-lookup"><span data-stu-id="962e9-124">Calculate proposal</span></span>
1. <span data-ttu-id="962e9-125">Klõpsake valikut **Arvuta soovitus**.</span><span class="sxs-lookup"><span data-stu-id="962e9-125">Click **Calculate proposal**.</span></span>
2. <span data-ttu-id="962e9-126">Tehke valik **Kasuta täitmisaja jooksul keskmist väljaminekut**.</span><span class="sxs-lookup"><span data-stu-id="962e9-126">Select the **Use average issue during lead time** option.</span></span>
3. <span data-ttu-id="962e9-127">Määrake valiku **Korrutustegur** väärtuseks 10.</span><span class="sxs-lookup"><span data-stu-id="962e9-127">Set **Multiplication factor** to '10'.</span></span> <span data-ttu-id="962e9-128">Tegurit Korruta kasutatakse soovituse korrigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="962e9-128">The Multiply factor is used to adjust the proposal.</span></span> <span data-ttu-id="962e9-129">Kuna demoandmetel on vaid mõned kanded, tuleb realistliku soovituse saamiseks tegur määrata.</span><span class="sxs-lookup"><span data-stu-id="962e9-129">Because demo data only has a few transactions, you will need to set the factor to get a realistic proposal.</span></span>  
4. <span data-ttu-id="962e9-130">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="962e9-130">Click **OK**.</span></span> <span data-ttu-id="962e9-131">Kerige alla M0002 ja M0003 leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="962e9-131">Scroll down to find M0002 and M0003.</span></span> <span data-ttu-id="962e9-132">Vaadake veergu **Arvutatud miinimumkogus**.</span><span class="sxs-lookup"><span data-stu-id="962e9-132">View the **Calculated minimum** quantity column.</span></span>   

## <a name="update-minimum-quantity"></a><span data-ttu-id="962e9-133">Miinimumkoguse uuendamine</span><span class="sxs-lookup"><span data-stu-id="962e9-133">Update minimum quantity</span></span>
1. <span data-ttu-id="962e9-134">Sisestage number väljale **Uus miinimumkogus**.</span><span class="sxs-lookup"><span data-stu-id="962e9-134">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="962e9-135">Uuendage väärtust Uus miinimumkogus nii, et see vastaks väärtusele jaotises Arvutatud miinimumkogus.</span><span class="sxs-lookup"><span data-stu-id="962e9-135">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="962e9-136">Kui Arvutatud miinimum on null, võite sisestada soovitud tulevase väärtuse.</span><span class="sxs-lookup"><span data-stu-id="962e9-136">If the Calculated minimum is zero,  you can enter the desired future value.</span></span> <span data-ttu-id="962e9-137">Näiteks võite sisestada sellele väljale väärtuse Arvutatud miinimumkogus M0002 kohta, millel on ladu 12.</span><span class="sxs-lookup"><span data-stu-id="962e9-137">For example, you can enter the Calculated minimum quantity in this field for M0002 that has warehouse 12.</span></span>  
2. <span data-ttu-id="962e9-138">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="962e9-138">In the list, find and select the desired record.</span></span> <span data-ttu-id="962e9-139">Näiteks võite valida M0002, millel on ladu 12.</span><span class="sxs-lookup"><span data-stu-id="962e9-139">For example, you can select M0002 that has warehouse 12.</span></span>  
3. <span data-ttu-id="962e9-140">Sisestage number väljale **Uus miinimumkogus**.</span><span class="sxs-lookup"><span data-stu-id="962e9-140">In the **New minimum quantity** field, enter a number.</span></span> <span data-ttu-id="962e9-141">Uuendage väärtust Uus miinimumkogus nii, et see vastaks väärtusele jaotises Arvutatud miinimumkogus.</span><span class="sxs-lookup"><span data-stu-id="962e9-141">Update the New minimum quantity to match the value in the Calculated minimum quantity.</span></span> <span data-ttu-id="962e9-142">Kui Arvutatud miinimum on null, võite sisestada soovitud tulevase väärtuse.</span><span class="sxs-lookup"><span data-stu-id="962e9-142">If the Calculated minimum is zero you can enter the desired future value.</span></span>  

## <a name="post-the-new-minimum-quantity-and-validate-the-result"></a><span data-ttu-id="962e9-143">Uue miinimumkoguse sisestamine ja tulemuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="962e9-143">Post the new minimum quantity and validate the result</span></span>
1. <span data-ttu-id="962e9-144">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="962e9-144">Click **Post**.</span></span>
2. <span data-ttu-id="962e9-145">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="962e9-145">Click **OK**.</span></span>
3. <span data-ttu-id="962e9-146">Klõpsake, et järgida linki väljal **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="962e9-146">Click to follow the link in the **Item number** field.</span></span>
4. <span data-ttu-id="962e9-147">Klõpsake, et järgida linki väljal **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="962e9-147">Click to follow the link in the **Item number** field.</span></span>
5. <span data-ttu-id="962e9-148">Klõpsake **Toimingupaanil** valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="962e9-148">On the **Action Pane**, click Plan.</span></span>
6. <span data-ttu-id="962e9-149">Klõpsake valikut **Kauba laovarud**.</span><span class="sxs-lookup"><span data-stu-id="962e9-149">Click **Item coverage**.</span></span> <span data-ttu-id="962e9-150">Pange tähele, et väärtuseks **Miinimumkogus** on määratud uus miinimumkogus puhvervaru töölehelt.</span><span class="sxs-lookup"><span data-stu-id="962e9-150">Notice that the **Minimum quantity** has been updated with the new minimum quantity from the safety stock journal.</span></span>  

