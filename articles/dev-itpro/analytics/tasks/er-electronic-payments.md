--- 
title: Elektrooniliste dokumentide loomine maksete jaoks, kasutades vormingu konfiguratsioone
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kasutada uue elektroonilise aruandluse (ER) vormingu konfiguratsiooni elektrooniliste dokumentide loomiseks maksete töötlemise puhul."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 805e6f377d452e9c50240c8c9fc2ea6f5cb487e6
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="generate-electronic-documents-for-payments-by-using-format-configurations"></a><span data-ttu-id="b91d6-103">Elektrooniliste dokumentide loomine maksete jaoks, kasutades vormingu konfiguratsioone</span><span class="sxs-lookup"><span data-stu-id="b91d6-103">Generate electronic documents for payments by using format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b91d6-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kasutada uue elektroonilise aruandluse (ER) vormingu konfiguratsiooni elektrooniliste dokumentide loomiseks maksete töötlemise puhul.</span><span class="sxs-lookup"><span data-stu-id="b91d6-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="b91d6-105">Neid toiminguid saab teha GBSI näidisettevõttes.</span><span class="sxs-lookup"><span data-stu-id="b91d6-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="b91d6-106">Etappide lõpuleviimiseks peate esmalt läbima etapid protseduuris Maksedokumendi vorminguga konfiguratsiooni loomine.</span><span class="sxs-lookup"><span data-stu-id="b91d6-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="b91d6-107">Elektrooniline makseviisi konfiguratsiooni muutmine</span><span class="sxs-lookup"><span data-stu-id="b91d6-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="b91d6-108">Avage Ostureskontro > Makse seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="b91d6-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="b91d6-109">Vajaduse korral vajutage jaotise Failivorming lülitusnuppu, et seda laiendada.</span><span class="sxs-lookup"><span data-stu-id="b91d6-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="b91d6-110">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="b91d6-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b91d6-111">Näiteks filtreerige välja Makseviis väärtusega Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="b91d6-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="b91d6-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="b91d6-112">Click Edit.</span></span>
5. <span data-ttu-id="b91d6-113">Määrake välja Üldine elektrooniline aruandlus väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="b91d6-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="b91d6-114">Tehke valik Jah, et kasutada üldist elektroonilise aruandluse mustrit maksefailide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b91d6-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="b91d6-115">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b91d6-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b91d6-116">Valige BACS-i (UK fiktiivne) vormingu konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="b91d6-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="b91d6-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b91d6-117">Click Save.</span></span>
9. <span data-ttu-id="b91d6-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b91d6-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="b91d6-119">Loodud maksefailide vormingu testimine</span><span class="sxs-lookup"><span data-stu-id="b91d6-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="b91d6-120">Avage Ostureskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="b91d6-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="b91d6-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b91d6-121">Click New.</span></span>
3. <span data-ttu-id="b91d6-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b91d6-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="b91d6-123">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b91d6-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b91d6-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b91d6-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b91d6-125">Tehke valik VendPay.</span><span class="sxs-lookup"><span data-stu-id="b91d6-125">Select VendPay.</span></span>  
6. <span data-ttu-id="b91d6-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b91d6-126">Click Save.</span></span>
7. <span data-ttu-id="b91d6-127">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="b91d6-127">Click Lines.</span></span>
8. <span data-ttu-id="b91d6-128">Tippige väljale Ettevõte väärtus DEMF.</span><span class="sxs-lookup"><span data-stu-id="b91d6-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="b91d6-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="b91d6-129">DEMF</span></span>  
9. <span data-ttu-id="b91d6-130">Määrake väljal Konto 'DE-01001' väärtused.</span><span class="sxs-lookup"><span data-stu-id="b91d6-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="b91d6-131">DE – 01001</span><span class="sxs-lookup"><span data-stu-id="b91d6-131">DE-01001</span></span>  
10. <span data-ttu-id="b91d6-132">Tippige väljale Kirjeldus väärtus Makse.</span><span class="sxs-lookup"><span data-stu-id="b91d6-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="b91d6-133">Makse</span><span class="sxs-lookup"><span data-stu-id="b91d6-133">Payment</span></span>  
11. <span data-ttu-id="b91d6-134">Sisestage arv väljale Deebet.</span><span class="sxs-lookup"><span data-stu-id="b91d6-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="b91d6-135">1000</span><span class="sxs-lookup"><span data-stu-id="b91d6-135">1000</span></span>  
12. <span data-ttu-id="b91d6-136">Klõpsake vahekaarti Makse.</span><span class="sxs-lookup"><span data-stu-id="b91d6-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="b91d6-137">Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b91d6-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="b91d6-138">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b91d6-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b91d6-139">Valige elektrooniline väärtus.</span><span class="sxs-lookup"><span data-stu-id="b91d6-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="b91d6-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b91d6-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="b91d6-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b91d6-141">Click Save.</span></span>
17. <span data-ttu-id="b91d6-142">Klõpsake valikut Loo maksed.</span><span class="sxs-lookup"><span data-stu-id="b91d6-142">Click Generate payments.</span></span>
18. <span data-ttu-id="b91d6-143">Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b91d6-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="b91d6-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b91d6-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b91d6-145">Valige elektrooniline väärtus.</span><span class="sxs-lookup"><span data-stu-id="b91d6-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="b91d6-146">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b91d6-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b91d6-147">Valige elektrooniline väärtus.</span><span class="sxs-lookup"><span data-stu-id="b91d6-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="b91d6-148">Sisestage väärtus väljale Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="b91d6-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="b91d6-149">Tippige näiteks väärtus Maksed.</span><span class="sxs-lookup"><span data-stu-id="b91d6-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="b91d6-150">Klõpsake väljal Pangakonto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b91d6-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="b91d6-151">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b91d6-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b91d6-152">Valige väärtus GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="b91d6-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="b91d6-153">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b91d6-153">Click OK.</span></span>
25. <span data-ttu-id="b91d6-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b91d6-154">Click OK.</span></span>
    * <span data-ttu-id="b91d6-155">Analüüsige loodud maksefaili XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="b91d6-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="b91d6-156">Võrrelge seda koostatud dokumendi paigutusega ja määratletud maksekande atribuutidega.</span><span class="sxs-lookup"><span data-stu-id="b91d6-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  


