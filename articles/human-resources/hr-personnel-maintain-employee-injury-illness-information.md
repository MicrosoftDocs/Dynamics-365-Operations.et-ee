---
title: Töötajate vigastuste ja haiguste teabe haldamine
description: Soovitatav on esmalt järgida ülesande juhendit „Vigastuse ja haiguse häälestamine”, kuna osa häälestusteavet kasutatakse siin.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 786461338d994ab04dfa57428e7720162ab16f86
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008782"
---
# <a name="maintain-employee-injury-and-illness-information"></a><span data-ttu-id="84ec0-103">Töötajate vigastuste ja haiguste teabe haldamine</span><span class="sxs-lookup"><span data-stu-id="84ec0-103">Maintain employee injury and illness information</span></span>



<span data-ttu-id="84ec0-104">Soovitatav on esmalt järgida ülesande juhendit „Vigastuse ja haiguse häälestamine”, kuna osa häälestusteavet kasutatakse siin.</span><span class="sxs-lookup"><span data-stu-id="84ec0-104">It is recommended to complete the 'Setup injury and illness' task guide first, as some of the setup information is used here.</span></span> 



<span data-ttu-id="84ec0-105">Ülesande salvestis hõlmab põhiteavet vigastus- või haigusjuhtumi loomise kohta.</span><span class="sxs-lookup"><span data-stu-id="84ec0-105">This task recording covers the basic steps to creating an injury or illness case.</span></span> <span data-ttu-id="84ec0-106">Peale vigastuse või haiguse üksikasjade jälgimise jälgitakse ka juhtumi olekut.</span><span class="sxs-lookup"><span data-stu-id="84ec0-106">Besides tracking the details of the injury or illness, there is a case status that is tracked as well.</span></span>  <span data-ttu-id="84ec0-107">Vaikimisi on juhtumi olek „Avatud”.</span><span class="sxs-lookup"><span data-stu-id="84ec0-107">The case defaults with an 'open' status.</span></span>  <span data-ttu-id="84ec0-108">Olekuid saab hallata lehe ülaosas menüü-üksuses „Juhtumi olek”.</span><span class="sxs-lookup"><span data-stu-id="84ec0-108">The statuses can be managed from the 'Case status' menu item at the top of the page.</span></span>

1. <span data-ttu-id="84ec0-109">Avage jaotis Personaliarvestus > Töötajad > Vigastus ja haigus > Vigastus- või haigusjuhtumid.</span><span class="sxs-lookup"><span data-stu-id="84ec0-109">Go to Human resources > Workers > Injury and illness > Injury or illness incidents.</span></span>
2. <span data-ttu-id="84ec0-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="84ec0-110">Click New.</span></span>
3. <span data-ttu-id="84ec0-111">Sisestage väärtus väljale Juhtumi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="84ec0-111">In the Case description field, type a value.</span></span>
    * <span data-ttu-id="84ec0-112">Näide: randmevigastus</span><span class="sxs-lookup"><span data-stu-id="84ec0-112">Example:  Wrist injury</span></span>  
4. <span data-ttu-id="84ec0-113">Valige või sisestage väärtus väljal Töötaja.</span><span class="sxs-lookup"><span data-stu-id="84ec0-113">In the Worker field, enter or select a value.</span></span>
    * <span data-ttu-id="84ec0-114">Näide: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="84ec0-114">Example: Ahmed Barnett</span></span>  
5. <span data-ttu-id="84ec0-115">Sisestage kuupäev ja kellaaeg väljale Juhtumi kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="84ec0-115">In the Date and time of incident field, enter a date and time.</span></span>
    * <span data-ttu-id="84ec0-116">Näide: 20.01.2016 10.00</span><span class="sxs-lookup"><span data-stu-id="84ec0-116">Example:  1/20/2016 10:00 AM</span></span>  
6. <span data-ttu-id="84ec0-117">Sisestage või valige väärtus väljal Vigastuse või haiguse tüüp.</span><span class="sxs-lookup"><span data-stu-id="84ec0-117">In the Injury or illness type field, enter or select a value.</span></span>
    * <span data-ttu-id="84ec0-118">Näide: luumurd</span><span class="sxs-lookup"><span data-stu-id="84ec0-118">Example:  Fracture</span></span>  
7. <span data-ttu-id="84ec0-119">Valige või sisestage väärtus väljal Kehaosa.</span><span class="sxs-lookup"><span data-stu-id="84ec0-119">In the Body part field, enter or select a value.</span></span>
    * <span data-ttu-id="84ec0-120">Näide: ranne</span><span class="sxs-lookup"><span data-stu-id="84ec0-120">Example:  Wrist</span></span>  
8. <span data-ttu-id="84ec0-121">Sisestage või valige väärtus väljal Tulemuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="84ec0-121">In the Outcome type field, enter or select a value.</span></span>
    * <span data-ttu-id="84ec0-122">Näide: ravi</span><span class="sxs-lookup"><span data-stu-id="84ec0-122">Example:  Therapy</span></span>  
9. <span data-ttu-id="84ec0-123">Sisestage kuupäev ja kellaaeg väljale Teatamise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="84ec0-123">In the Date and time reported field, enter a date and time.</span></span>
    * <span data-ttu-id="84ec0-124">Teatamise kuupäev ja kellaaeg peavad olema hilisemad kui juhtumi kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="84ec0-124">The date and time reported must be later than the date and time of incident.</span></span>  
10. <span data-ttu-id="84ec0-125">Sisestage või valige väärtus väljal Juhtumist teatanud isik.</span><span class="sxs-lookup"><span data-stu-id="84ec0-125">In the Person who reported case field, enter or select a value.</span></span>
    * <span data-ttu-id="84ec0-126">See võib olla töötaja või mõni muu juhtumi tunnistaja.</span><span class="sxs-lookup"><span data-stu-id="84ec0-126">This could be the employee or another witness to the incident.</span></span>  <span data-ttu-id="84ec0-127">Näide: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="84ec0-127">Example: Ahmed Barnett</span></span>  
11. <span data-ttu-id="84ec0-128">Laiendage jaotist Juhtum.</span><span class="sxs-lookup"><span data-stu-id="84ec0-128">Expand the Incident section.</span></span>
12. <span data-ttu-id="84ec0-129">Sisestage väärtus väljale Õnnetusjuhtumi toimumiskoht.</span><span class="sxs-lookup"><span data-stu-id="84ec0-129">In the Where incident occurred field, type a value.</span></span>
    * <span data-ttu-id="84ec0-130">Näide: ladu</span><span class="sxs-lookup"><span data-stu-id="84ec0-130">Example:  Warehouse</span></span>  
13. <span data-ttu-id="84ec0-131">Valige väljal Tööjuures suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="84ec0-131">Select Yes in the On work premises field.</span></span>
    * <span data-ttu-id="84ec0-132">Kui õnnetusjuhtum toimus töö juures, valige Jah.</span><span class="sxs-lookup"><span data-stu-id="84ec0-132">If the incident occurred on work premises, select yes.</span></span>  
14. <span data-ttu-id="84ec0-133">Sisestage kuupäev ja kellaaeg väljale Töö alustamise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="84ec0-133">In the Date and time began work field, enter a date and time.</span></span>
    * <span data-ttu-id="84ec0-134">Sisestage isiku töö alguse kuupäev ja kellaaeg enne juhtumit.</span><span class="sxs-lookup"><span data-stu-id="84ec0-134">Enter the date and time that affected individual started working, prior to the incident occurring.</span></span>  
15. <span data-ttu-id="84ec0-135">Sisestage väärtus väljale Töötaja töö või ülesanne.</span><span class="sxs-lookup"><span data-stu-id="84ec0-135">In the Employee job or task field, type a value.</span></span>
    * <span data-ttu-id="84ec0-136">Sisestage töö või ülesanne, mida töötaja juhtumi ilmnemise ajal täitis.</span><span class="sxs-lookup"><span data-stu-id="84ec0-136">Enter the job or task the worker was performing when the incident occurred.</span></span>  <span data-ttu-id="84ec0-137">Näide: kastide laadimine</span><span class="sxs-lookup"><span data-stu-id="84ec0-137">Example:  Loading boxes</span></span>  
16. <span data-ttu-id="84ec0-138">Sisestage väärtus väljale Juhtumi põhjus.</span><span class="sxs-lookup"><span data-stu-id="84ec0-138">In the Cause of incident field, type a value.</span></span>
    * <span data-ttu-id="84ec0-139">Sisestage juhtumi põhjus.</span><span class="sxs-lookup"><span data-stu-id="84ec0-139">Enter the cause of the incident.</span></span>  <span data-ttu-id="84ec0-140">Näide: libises märjal põrandal</span><span class="sxs-lookup"><span data-stu-id="84ec0-140">Example:  Slipped on wet floor</span></span>  
17. <span data-ttu-id="84ec0-141">Sisestage või valige väärtus väljal Raskusaste.</span><span class="sxs-lookup"><span data-stu-id="84ec0-141">In the Severity level field, enter or select a value.</span></span>
18. <span data-ttu-id="84ec0-142">Sisestage väärtus väljale Läbiviidav tegevus.</span><span class="sxs-lookup"><span data-stu-id="84ec0-142">In the Action to be taken field, type a value.</span></span>
    * <span data-ttu-id="84ec0-143">Näide: maha sattunud vedelik tuleb kohe puhastada</span><span class="sxs-lookup"><span data-stu-id="84ec0-143">Example:  Clean up spills promptly</span></span>  
19. <span data-ttu-id="84ec0-144">Sisestage arv väljale Oletatav töölt eemal viibimise päevade arv.</span><span class="sxs-lookup"><span data-stu-id="84ec0-144">In the Expected days away from work field, enter a number.</span></span>
    * <span data-ttu-id="84ec0-145">Sisestage eeldatav päevade arv, mil isik on töölt eemal.</span><span class="sxs-lookup"><span data-stu-id="84ec0-145">Enter the number of days that the individual is expected to be away from work.</span></span>  <span data-ttu-id="84ec0-146">Kui isik naaseb tööle, sisestage väljale „Töölt puudutud päevad” tegelik päevade arv, mil töötaja puudus.</span><span class="sxs-lookup"><span data-stu-id="84ec0-146">Once the individual returns to work, update the 'Days away from work' field with the actual number of days away.</span></span>  
20. <span data-ttu-id="84ec0-147">Laiendage jaotist Vigastuse või haiguse kulud.</span><span class="sxs-lookup"><span data-stu-id="84ec0-147">Expand the Injury or illness costs section.</span></span>
21. <span data-ttu-id="84ec0-148">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="84ec0-148">Click Add.</span></span>
22. <span data-ttu-id="84ec0-149">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="84ec0-149">In the Date field, enter a date.</span></span>
23. <span data-ttu-id="84ec0-150">Sisestage või valige väärtus väljal Kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="84ec0-150">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="84ec0-151">Näide: ravi – võite ka sisestada summa ja lisada kulule mis tahes lisadokumente (nt arved või arsti märkused).</span><span class="sxs-lookup"><span data-stu-id="84ec0-151">Example:  Therapy    You can also enter in an amount, and attach any supporting documentation such as invoices or doctor's notes to the cost.</span></span>  
24. <span data-ttu-id="84ec0-152">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="84ec0-152">Click Add.</span></span>
25. <span data-ttu-id="84ec0-153">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="84ec0-153">In the Date field, enter a date.</span></span>
26. <span data-ttu-id="84ec0-154">Sisestage või valige väärtus väljal Kulu tüüp.</span><span class="sxs-lookup"><span data-stu-id="84ec0-154">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="84ec0-155">Näide: arst</span><span class="sxs-lookup"><span data-stu-id="84ec0-155">Example: Doctor</span></span>  
27. <span data-ttu-id="84ec0-156">Laiendage jaotist Vigastuse või haiguse raviprotseduurid.</span><span class="sxs-lookup"><span data-stu-id="84ec0-156">Expand the Injury or illness treatments section.</span></span>
28. <span data-ttu-id="84ec0-157">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="84ec0-157">Click Add.</span></span>
29. <span data-ttu-id="84ec0-158">Sisestage kuupäev ja kellaaeg väljale Ravi.</span><span class="sxs-lookup"><span data-stu-id="84ec0-158">In the Treatment date field, enter a date and time.</span></span>
30. <span data-ttu-id="84ec0-159">Sisestage või valige väärtus väljal Ravi tüüp.</span><span class="sxs-lookup"><span data-stu-id="84ec0-159">In the Treatment type field, enter or select a value.</span></span>
    * <span data-ttu-id="84ec0-160">Näide: lahas</span><span class="sxs-lookup"><span data-stu-id="84ec0-160">Example:  Splint</span></span>  
31. <span data-ttu-id="84ec0-161">Soovi korral võite valida haigla traumapunkti külastamise jaotises suvandi Jah.</span><span class="sxs-lookup"><span data-stu-id="84ec0-161">Optionally, set the emergency room hospital visit section to Yes.</span></span>
32. <span data-ttu-id="84ec0-162">Sisestage väärtus väljale Ravi kommentaarid.</span><span class="sxs-lookup"><span data-stu-id="84ec0-162">In the Treatment comments field, type a value.</span></span>
    * <span data-ttu-id="84ec0-163">Näide: lahas 2 nädalat</span><span class="sxs-lookup"><span data-stu-id="84ec0-163">Example:  Splint for 2 weeks</span></span>  
33. <span data-ttu-id="84ec0-164">Sisestage väärtus väljale Arsti nimi.</span><span class="sxs-lookup"><span data-stu-id="84ec0-164">In the Physician name field, type a value.</span></span>
    * <span data-ttu-id="84ec0-165">Näide:  dr Anderson</span><span class="sxs-lookup"><span data-stu-id="84ec0-165">Example:  Dr. Anderson</span></span>  
34. <span data-ttu-id="84ec0-166">Sisestage või valige väärtus väljal Raviasutus ja asukoht.</span><span class="sxs-lookup"><span data-stu-id="84ec0-166">In the Treatment facility and location field, type a value.</span></span>
    * <span data-ttu-id="84ec0-167">Näide: Jalaka tn traumapunkt</span><span class="sxs-lookup"><span data-stu-id="84ec0-167">Example:  Elm St. Emergency</span></span>  
35. <span data-ttu-id="84ec0-168">Sisestage väärtus väljale Ravi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="84ec0-168">In the Treatment details field, type a value.</span></span>
    * <span data-ttu-id="84ec0-169">Näide: röntgen kinnitab murdu, kanda lahast</span><span class="sxs-lookup"><span data-stu-id="84ec0-169">Example:  Xray confirms fracture, wear splint</span></span>  
36. <span data-ttu-id="84ec0-170">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="84ec0-170">Click Save.</span></span>
    * <span data-ttu-id="84ec0-171">Juhtumi olekut saab igal ajal värskendada.</span><span class="sxs-lookup"><span data-stu-id="84ec0-171">The case status can be updated at any time.</span></span>  <span data-ttu-id="84ec0-172">Määrake juhtum pooleliolevaks, kui vigastuse või haiguse käsitlemine on pooleli.</span><span class="sxs-lookup"><span data-stu-id="84ec0-172">Set the case to in process, if the processing of the injury or illness is in process.</span></span>  <span data-ttu-id="84ec0-173">Pärast juhtumi sulgemist saate ainult lisada ja eemaldada juhtumiga seotud kulusid, raviandmeid või sissekandeid.</span><span class="sxs-lookup"><span data-stu-id="84ec0-173">Once you close the incident you can only add or remove costs, treatments or filings related to the incident.</span></span>  <span data-ttu-id="84ec0-174">Muu teabe muutmiseks avage juhtum uuesti.</span><span class="sxs-lookup"><span data-stu-id="84ec0-174">To modify other information, reopen the case.</span></span>  

