--- 
title: "Perioodiliste töölehtede sisestamine"
description: "Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse."
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 233d145a9d3441ffc2b816b8514e58988b517136
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="post-periodic-journals"></a><span data-ttu-id="6162c-103">Perioodiliste töölehtede sisestamine</span><span class="sxs-lookup"><span data-stu-id="6162c-103">Post periodic journals</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6162c-104">Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="6162c-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="6162c-105">Perioodilise töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu.</span><span class="sxs-lookup"><span data-stu-id="6162c-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="6162c-106">Selles tegevuse juhises luuakse igakuise kordumismustriga perioodiline tööleht.</span><span class="sxs-lookup"><span data-stu-id="6162c-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="6162c-107">>Avage Pearaamat >Perioodilised ülesanded > Perioodilised töölehed.</span><span class="sxs-lookup"><span data-stu-id="6162c-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="6162c-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6162c-108">Click New.</span></span>
3. <span data-ttu-id="6162c-109">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="6162c-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="6162c-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6162c-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6162c-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6162c-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="6162c-112">See kirjeldus on hiljem ka perioodilise töölehe nimi, seetõttu tasub sellele anda asjakohane nimi.</span><span class="sxs-lookup"><span data-stu-id="6162c-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="6162c-113">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="6162c-113">Click Lines.</span></span>
    * <span data-ttu-id="6162c-114">Perioodilisel töölehel on tavaliselt mitu töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="6162c-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="6162c-115">Selles ülesandes lisatakse sellele siiski vaid üks rida.</span><span class="sxs-lookup"><span data-stu-id="6162c-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="6162c-116">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="6162c-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="6162c-117">Väli Kuupäev sisaldab järgmise päevase töölehe kande sisestuskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="6162c-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="6162c-118">Igakuiste töölehtede puhul on soovitatav kasutada kuupäeva, mil see sisestatakse, tavaliselt kas esimene viimane kuupäev perioodis.</span><span class="sxs-lookup"><span data-stu-id="6162c-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="6162c-119">Kasutades välja Tühi kuupäev võite jätta välja Kuupäev tühjaks ning lisada selle siis, kui tööleht on toodud.</span><span class="sxs-lookup"><span data-stu-id="6162c-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="6162c-120">Välja värskendatakse automaatselt järgmise korduva kuupäevani, kui kandeid tuuakse.</span><span class="sxs-lookup"><span data-stu-id="6162c-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="6162c-121">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="6162c-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="6162c-122">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6162c-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="6162c-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6162c-123">Close the page.</span></span>
11. <span data-ttu-id="6162c-124">Sisestage arv väljale Deebet.</span><span class="sxs-lookup"><span data-stu-id="6162c-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="6162c-125">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="6162c-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="6162c-126">Valige Kuud väljal Ühik.</span><span class="sxs-lookup"><span data-stu-id="6162c-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="6162c-127">Sisestage number 1 väljale Ühikute arv.</span><span class="sxs-lookup"><span data-stu-id="6162c-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="6162c-128">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="6162c-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="6162c-129">Eelmise perioodi viimase kuupäeva sisestamine aitab vältida kogemata korduvtöölehe loomist valesse algusperioodi.</span><span class="sxs-lookup"><span data-stu-id="6162c-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="6162c-130">Viimast kuupäeva värskendatakse hiljem iga kord, kui perioodilist töölehte tuuakse.</span><span class="sxs-lookup"><span data-stu-id="6162c-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="6162c-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6162c-131">Click Save.</span></span>
17. <span data-ttu-id="6162c-132">Avage Vaikearmatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="6162c-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="6162c-133">Avage Pearaamat > Töölehe sisestused > Päevaraamatud.</span><span class="sxs-lookup"><span data-stu-id="6162c-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="6162c-134">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6162c-134">Click New.</span></span>
20. <span data-ttu-id="6162c-135">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="6162c-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="6162c-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6162c-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="6162c-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6162c-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="6162c-138">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6162c-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="6162c-139">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="6162c-139">Click Lines.</span></span>
25. <span data-ttu-id="6162c-140">Klõpsake valikut Perioodi tööleht.</span><span class="sxs-lookup"><span data-stu-id="6162c-140">Click Period journal.</span></span>
26. <span data-ttu-id="6162c-141">Klõpsake käsku Too tööleht.</span><span class="sxs-lookup"><span data-stu-id="6162c-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="6162c-142">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="6162c-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="6162c-143">Lõpukuupäev toimib perioodiliste kannete ridadel nagu äralõikekuupäev.</span><span class="sxs-lookup"><span data-stu-id="6162c-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="6162c-144">Olenevalt kordussätetest võivad samal real paiknevad Viimane kuupäev ja Lõpukuupäev esineda tulemuseks oleval töölehel rohkem kui ühel korral.</span><span class="sxs-lookup"><span data-stu-id="6162c-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="6162c-145">Lõpukuupäeva värskendatakse automaatselt olenevalt perioodilise rea viimase töölehele ülekandmise seansi kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="6162c-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="6162c-146">Sisestage või valige väärtus väljal Perioodilise töölehe kood.</span><span class="sxs-lookup"><span data-stu-id="6162c-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="6162c-147">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6162c-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="6162c-148">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6162c-148">Click OK.</span></span>
    * <span data-ttu-id="6162c-149">Sõltuvalt nõuetest ja seadistusest saab nüüd perioodi töölehte üle vaadata, kinnitada või sisestada.</span><span class="sxs-lookup"><span data-stu-id="6162c-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


