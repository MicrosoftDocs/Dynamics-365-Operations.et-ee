--- 
title: "Konteinerisse määramise seadistamine"
description: Protseduur kirjeldab koormakonteinerite koostamise automatiseerimist laohalduses.
author: YuyuScheller
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aeb7d956560c513c08d5e20dcf20989b49137a52
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-containerization"></a><span data-ttu-id="6e7bb-103">Konteinerisse määramise seadistamine</span><span class="sxs-lookup"><span data-stu-id="6e7bb-103">Set up containerization</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e7bb-104">Protseduur kirjeldab koormakonteinerite koostamise automatiseerimist laohalduses.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="6e7bb-105">Automaatne konteinerite koostamine loob saadetiste jaoks konteinerid ja komplekteerimistööd pärast voo töötlemist ja töö read saab jagada kogustesse, mis vastavad konteineritele.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="6e7bb-106">See aitab laotöötajatel komplekteerida kaupu otse valitud konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="6e7bb-107">Võrreldes käsitsi pakkimise protsessiga, on sellised toimingud nagu konteinerite loomine, kaupade määramine ja konteinerite sulgemine süsteemi automatiseeritud.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="6e7bb-108">See protseduur kasutab demoettevõtet USMF ja selle viib läbi lao juhataja.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="6e7bb-109">Voomalli seadistamine</span><span class="sxs-lookup"><span data-stu-id="6e7bb-109">Set up a wave template</span></span>
1. <span data-ttu-id="6e7bb-110">Avage Laohaldus > Seadistus > Vood > Voomallid.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="6e7bb-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-111">Click New.</span></span>
3. <span data-ttu-id="6e7bb-112">Tippige väärtus väljale Voomalli nimi.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="6e7bb-113">Tippige väärtus väljale Voomalli kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="6e7bb-114">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="6e7bb-115">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="6e7bb-116">Laiendage jaotist Meetodid.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="6e7bb-117">Paan Valitud meetodid loetleb valitud voomalli tüübi meetodid.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="6e7bb-118">Voomall peab sisaldama konteineri koostamise meetodit.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="6e7bb-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="6e7bb-120">Tippige väärtus väljale Voo etapi kood.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="6e7bb-121">Sisestage lisatud meetodile vooetapi kood, mis võib olla mis tahes kood.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="6e7bb-122">On võimalik lisada meetodit mitu korda ja määrata erinevad vooetapi koodid.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="6e7bb-123">Selleks tehke lehel Vooprotsessi meetodid valik Selles voo mallis korratav.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="6e7bb-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-124">Click Save.</span></span>
11. <span data-ttu-id="6e7bb-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="6e7bb-126">Konteineri tüübi häälestamine</span><span class="sxs-lookup"><span data-stu-id="6e7bb-126">Set up a container type</span></span>
1. <span data-ttu-id="6e7bb-127">Avage Laohaldus > Seadistus > Konteinerid > Konteinerite tüübid.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="6e7bb-128">Saate määratleda oma konteinerid lehel Konteineri tüübid.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="6e7bb-129">Saate konfigureerida konteinerite füüsilised mõõdud, sh taara kaalu ja maksimaalse kaalu, maksimaalse mahu, pikkuse, laiuse ning kõrguse.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="6e7bb-130">Selles näites on meil kolmes erinevas suuruses karpe.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="6e7bb-131">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-131">Click New.</span></span>
3. <span data-ttu-id="6e7bb-132">Tippige väärtus väljale Konteineri tüübi kood.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="6e7bb-133">Sisestage number väljale Taarakaal.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="6e7bb-134">Sisestage number väljale Maksimaalne kaal.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="6e7bb-135">Sisestage number väljale Maht.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="6e7bb-136">Sisestage number väljale Pikkus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="6e7bb-137">Sisestage number väljale Laius.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="6e7bb-138">Sisestage number väljale Kõrgus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="6e7bb-139">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="6e7bb-140">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-140">Click Save.</span></span>
12. <span data-ttu-id="6e7bb-141">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-141">Click New.</span></span>
13. <span data-ttu-id="6e7bb-142">Tippige väärtus väljale Konteineri tüübi kood.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="6e7bb-143">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="6e7bb-144">Sisestage number väljale Taarakaal.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="6e7bb-145">Sisestage number väljale Maksimaalne kaal.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="6e7bb-146">Sisestage number väljale Maht.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="6e7bb-147">Sisestage number väljale Pikkus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="6e7bb-148">Sisestage number väljale Laius.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="6e7bb-149">Sisestage number väljale Kõrgus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="6e7bb-150">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-150">Click Save.</span></span>
22. <span data-ttu-id="6e7bb-151">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-151">Click New.</span></span>
23. <span data-ttu-id="6e7bb-152">Tippige väärtus väljale Konteineri tüübi kood.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="6e7bb-153">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="6e7bb-154">Sisestage number väljale Taarakaal.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="6e7bb-155">Sisestage number väljale Maksimaalne kaal.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="6e7bb-156">Sisestage number väljale Maht.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="6e7bb-157">Sisestage number väljale Pikkus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="6e7bb-158">Sisestage number väljale Laius.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="6e7bb-159">Sisestage number väljale Kõrgus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="6e7bb-160">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-160">Click Save.</span></span>
32. <span data-ttu-id="6e7bb-161">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="6e7bb-162">Konteinerigrupi häälestamine</span><span class="sxs-lookup"><span data-stu-id="6e7bb-162">Set up a container group</span></span>
1. <span data-ttu-id="6e7bb-163">Avage Laohaldus > Seadistus > Konteinerid > Konteinerigrupid.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="6e7bb-164">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-164">Click New.</span></span>
    * <span data-ttu-id="6e7bb-165">Saate häälestada konteineritüüpide loogilised grupid.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="6e7bb-166">Saate iga grupi jaoks määrata järjestuse, mille alusel konteinereid koostada, ja konteinerite täitmisprotsendi. Kauba mõõtude alusel määratakse, kas see mahub konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="6e7bb-167">Kasutatakse konteinerit, mille mõõdud on kaubaga kõige sarnasemad.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="6e7bb-168">Kui grupis on mitu konteineritüüpi, soovitame korraldada järjestuse suuruse alusel, nii et suurim konteiner on esimene, järjekorras nr 1, ja väikseim konteiner viimane.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="6e7bb-169">Tippige väärtus väljale Konteinerigrupi ID.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="6e7bb-170">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6e7bb-171">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-171">Click New.</span></span>
6. <span data-ttu-id="6e7bb-172">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="6e7bb-173">Sisestage või valige väärtus väljal Konteineri tüüp.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="6e7bb-174">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-174">Click New.</span></span>
9. <span data-ttu-id="6e7bb-175">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="6e7bb-176">Sisestage või valige väärtus väljal Konteineri tüüp.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="6e7bb-177">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-177">Click New.</span></span>
12. <span data-ttu-id="6e7bb-178">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="6e7bb-179">Sisestage või valige väärtus väljal Konteineri tüüp.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="6e7bb-180">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-180">Click Save.</span></span>
15. <span data-ttu-id="6e7bb-181">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="6e7bb-182">Konteineri koostemalli häälestamine</span><span class="sxs-lookup"><span data-stu-id="6e7bb-182">Set up a container build template</span></span>
1. <span data-ttu-id="6e7bb-183">Avage Laohaldus > Seadistus > Konteinerid > Konteineri koostemallid.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="6e7bb-184">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-184">Click New.</span></span>
    * <span data-ttu-id="6e7bb-185">Konteineri koostamise mall põhineb sellel, milliseid konteinerite protsesse tehakse.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="6e7bb-186">Iga konteineri koostemall määratleb ühe konteineri loomise protsessi, mida kasutab voo mall.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="6e7bb-187">Suvandi Päringu redigeerimine abil saate määratleda tingimused, mille alusel valitud malli töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="6e7bb-188">Näiteks võite soovida käitada konteinerite loomist ainult teatud klientide, toodete või ladude puhul, või saate lisada vastavad päringuvahemikud malli.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="6e7bb-189">Väli Voo etapi kood näitab, kuidas konteineri koostemall on seotud voomalli etappidega.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="6e7bb-190">Kui voog on käivitatud, määrab see kindlaks, milliseid konteineri koostemalle kasutatakse konteineri koostamise alustamiseks.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="6e7bb-191">Väli Aluspäringu tüübid määrab, mida pakkida ja millel põhineb filtripäring.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="6e7bb-192">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6e7bb-193">Tippige väärtus väljale Konteinerimalli ID.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="6e7bb-194">Sisestage või valige väärtus väljal Konteinerigrupi ID.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="6e7bb-195">Tippige väärtus väljale Voo etapi kood.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="6e7bb-196">Märkige ruut Tükeldatud valiku lubamine.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="6e7bb-197">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-197">Click Save.</span></span>
9. <span data-ttu-id="6e7bb-198">Klõpsake suvandit Konteineri koostamise piirangud.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="6e7bb-199">Koostamisloogika pausid võimaldavad seadistada reeglid eraldusridade konteinerisse pakkimise kohta.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="6e7bb-200">Näiteks kui lisate välja Kauba kood, kui kauou konteineritesse määratakse, luuakse uus konteiner, kui on olemas uus kauba kood.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="6e7bb-201">See takistab töötajaid pakkimast kahe erineva kliendi eraldusridu samasse konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="6e7bb-202">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-202">Click New.</span></span>
11. <span data-ttu-id="6e7bb-203">Valige suvand väljal Tabel.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="6e7bb-204">Sisestage väärtus väljale Vali väli.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="6e7bb-205">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6e7bb-205">Click OK.</span></span>


