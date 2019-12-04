---
title: Elektrooniline aruandlus Elektrooniliste dokumentide loomine vormingu konfiguratsiooni kasutavate maksete jaoks
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kasutada uue elektroonilise aruandluse (ER) vormingu konfiguratsiooni elektrooniliste dokumentide loomiseks maksete töötlemise puhul.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 179e8a20dd65847f90872ae0e56b3e4991a6b00e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184987"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a><span data-ttu-id="567c2-103">Elektrooniline aruandlus Elektrooniliste dokumentide loomine vormingu konfiguratsiooni kasutavate maksete jaoks</span><span class="sxs-lookup"><span data-stu-id="567c2-103">ER Generate electronic documents for payments using a format configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="567c2-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kasutada uue elektroonilise aruandluse (ER) vormingu konfiguratsiooni elektrooniliste dokumentide loomiseks maksete töötlemise puhul.</span><span class="sxs-lookup"><span data-stu-id="567c2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can use a new Electronic reporting (ER) format configuration to generate electronic documents for processing payments.</span></span> <span data-ttu-id="567c2-105">Neid toiminguid saab teha GBSI näidisettevõttes.</span><span class="sxs-lookup"><span data-stu-id="567c2-105">These steps can be performed in the GBSI sample company.</span></span>

<span data-ttu-id="567c2-106">Etappide lõpuleviimiseks peate esmalt läbima etapid protseduuris Maksedokumendi vorminguga konfiguratsiooni loomine.</span><span class="sxs-lookup"><span data-stu-id="567c2-106">To complete these steps, you must first complete the steps in the “Create a configuration with format of payment document” procedure.</span></span>


## <a name="change-the-configuration-of-the-electronic-payment-method"></a><span data-ttu-id="567c2-107">Elektrooniline makseviisi konfiguratsiooni muutmine</span><span class="sxs-lookup"><span data-stu-id="567c2-107">Change the configuration of the electronic payment method</span></span>
1. <span data-ttu-id="567c2-108">Avage Ostureskontro > Makse seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="567c2-108">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
2. <span data-ttu-id="567c2-109">Vajaduse korral vajutage jaotise Failivorming lülitusnuppu, et seda laiendada.</span><span class="sxs-lookup"><span data-stu-id="567c2-109">Toggle the File format section to expand it, if needed.</span></span>
3. <span data-ttu-id="567c2-110">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="567c2-110">Use the Quick Filter to find records.</span></span> <span data-ttu-id="567c2-111">Näiteks filtreerige välja Makseviis väärtusega Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="567c2-111">For example, filter on the Method of payment field with a value of 'Electronic'.</span></span>
4. <span data-ttu-id="567c2-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="567c2-112">Click Edit.</span></span>
5. <span data-ttu-id="567c2-113">Määrake välja Üldine elektrooniline aruandlus väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="567c2-113">Set the General electronic reporting field to Yes.</span></span>
    * <span data-ttu-id="567c2-114">Tehke valik Jah, et kasutada üldist elektroonilise aruandluse mustrit maksefailide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="567c2-114">Select Yes to use the General electronic reporting pattern for payment files generation.</span></span>  
6. <span data-ttu-id="567c2-115">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="567c2-115">In the Name field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="567c2-116">Valige BACS-i (UK fiktiivne) vormingu konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="567c2-116">Select BACS (UK fictitious) format configuration.</span></span>
8. <span data-ttu-id="567c2-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="567c2-117">Click Save.</span></span>
9. <span data-ttu-id="567c2-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="567c2-118">Close the page.</span></span>

## <a name="test-the-format-of-generated-payment-files"></a><span data-ttu-id="567c2-119">Loodud maksefailide vormingu testimine</span><span class="sxs-lookup"><span data-stu-id="567c2-119">Test the format of generated payment files</span></span>
1. <span data-ttu-id="567c2-120">Avage Ostureskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="567c2-120">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="567c2-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="567c2-121">Click New.</span></span>
3. <span data-ttu-id="567c2-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="567c2-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="567c2-123">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="567c2-123">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="567c2-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="567c2-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="567c2-125">Tehke valik VendPay.</span><span class="sxs-lookup"><span data-stu-id="567c2-125">Select VendPay.</span></span>  
6. <span data-ttu-id="567c2-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="567c2-126">Click Save.</span></span>
7. <span data-ttu-id="567c2-127">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="567c2-127">Click Lines.</span></span>
8. <span data-ttu-id="567c2-128">Tippige väljale Ettevõte väärtus DEMF.</span><span class="sxs-lookup"><span data-stu-id="567c2-128">In the Company field, type 'DEMF'.</span></span>
    * <span data-ttu-id="567c2-129">DEMF</span><span class="sxs-lookup"><span data-stu-id="567c2-129">DEMF</span></span>  
9. <span data-ttu-id="567c2-130">Määrake väljal Konto 'DE-01001' väärtused.</span><span class="sxs-lookup"><span data-stu-id="567c2-130">In the Account field, specify the values 'DE-01001'.</span></span>
    * <span data-ttu-id="567c2-131">DE – 01001</span><span class="sxs-lookup"><span data-stu-id="567c2-131">DE-01001</span></span>  
10. <span data-ttu-id="567c2-132">Tippige väljale Kirjeldus väärtus Makse.</span><span class="sxs-lookup"><span data-stu-id="567c2-132">In the Description field, type 'Payment'.</span></span>
    * <span data-ttu-id="567c2-133">Makse</span><span class="sxs-lookup"><span data-stu-id="567c2-133">Payment</span></span>  
11. <span data-ttu-id="567c2-134">Sisestage arv väljale Deebet.</span><span class="sxs-lookup"><span data-stu-id="567c2-134">In the Debit field, enter a number.</span></span>
    * <span data-ttu-id="567c2-135">1000</span><span class="sxs-lookup"><span data-stu-id="567c2-135">1000</span></span>  
12. <span data-ttu-id="567c2-136">Klõpsake vahekaarti Makse.</span><span class="sxs-lookup"><span data-stu-id="567c2-136">Click the Payment tab.</span></span>
13. <span data-ttu-id="567c2-137">Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="567c2-137">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="567c2-138">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="567c2-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="567c2-139">Valige elektrooniline väärtus.</span><span class="sxs-lookup"><span data-stu-id="567c2-139">Select the Electronic value.</span></span>  
15. <span data-ttu-id="567c2-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="567c2-140">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="567c2-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="567c2-141">Click Save.</span></span>
17. <span data-ttu-id="567c2-142">Klõpsake valikut Loo maksed.</span><span class="sxs-lookup"><span data-stu-id="567c2-142">Click Generate payments.</span></span>
18. <span data-ttu-id="567c2-143">Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="567c2-143">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="567c2-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="567c2-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="567c2-145">Valige elektrooniline väärtus.</span><span class="sxs-lookup"><span data-stu-id="567c2-145">Select the Electronic value.</span></span>  
20. <span data-ttu-id="567c2-146">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="567c2-146">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="567c2-147">Valige elektrooniline väärtus.</span><span class="sxs-lookup"><span data-stu-id="567c2-147">Select the Electronic value.</span></span>  
21. <span data-ttu-id="567c2-148">Sisestage väärtus väljale Faili nimi.</span><span class="sxs-lookup"><span data-stu-id="567c2-148">In the File name field, type a value.</span></span>
    * <span data-ttu-id="567c2-149">Tippige näiteks väärtus Maksed.</span><span class="sxs-lookup"><span data-stu-id="567c2-149">For example, type 'payments'.</span></span>  
22. <span data-ttu-id="567c2-150">Klõpsake väljal Pangakonto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="567c2-150">In the Bank account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="567c2-151">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="567c2-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="567c2-152">Valige väärtus GBSI OPER.</span><span class="sxs-lookup"><span data-stu-id="567c2-152">Select the value GBSI OPER.</span></span>  
24. <span data-ttu-id="567c2-153">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="567c2-153">Click OK.</span></span>
25. <span data-ttu-id="567c2-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="567c2-154">Click OK.</span></span>
    * <span data-ttu-id="567c2-155">Analüüsige loodud maksefaili XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="567c2-155">Analyze the created payment file in XML format.</span></span> <span data-ttu-id="567c2-156">Võrrelge seda koostatud dokumendi paigutusega ja määratletud maksekande atribuutidega.</span><span class="sxs-lookup"><span data-stu-id="567c2-156">Compare it with the designed document layout and defined payment transaction attributes.</span></span>  
