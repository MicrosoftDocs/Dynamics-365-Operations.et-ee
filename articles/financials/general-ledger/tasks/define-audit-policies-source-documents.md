--- 
title: "Lähtedokumentide jaoks auditipoliitikate määratlemine"
description: "Selles protseduuris näitlikustatakse, kuidas seadistada ja käitada auditi poliitikareegleid."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1bcea6257447cc1d1532f30acc2fb6bb4d524810
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="c87ea-103">Lähtedokumentide jaoks auditipoliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="c87ea-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c87ea-104">Selles protseduuris näitlikustatakse, kuidas seadistada ja käitada auditi poliitikareegleid.</span><span class="sxs-lookup"><span data-stu-id="c87ea-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="c87ea-105">Näites kasutatakse hotelli kulu tüübiga kuluaruandeid.</span><span class="sxs-lookup"><span data-stu-id="c87ea-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="c87ea-106">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="c87ea-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="c87ea-107">Audiitori roll sisaldab nende ülesannete teostamiseks vajalikke õigusi.</span><span class="sxs-lookup"><span data-stu-id="c87ea-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="c87ea-108">Minge jaotisse Auditi töölaud > Seadistus > Poliitika reegli tüüp.</span><span class="sxs-lookup"><span data-stu-id="c87ea-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="c87ea-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c87ea-109">Click New.</span></span>
3. <span data-ttu-id="c87ea-110">Sisestage väärtus väljale Reegli nimi.</span><span class="sxs-lookup"><span data-stu-id="c87ea-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="c87ea-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="c87ea-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c87ea-112">Valige Kuluaruande rida väljal Päringu nimi</span><span class="sxs-lookup"><span data-stu-id="c87ea-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="c87ea-113">Valige Koonda väljal Päringu tüüp.</span><span class="sxs-lookup"><span data-stu-id="c87ea-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="c87ea-114">Valige Juriidiline isik väljal Juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="c87ea-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="c87ea-115">Valige Muudetud kuupäev ja kellaaeg väljal Dokumendi kuupäeva viide</span><span class="sxs-lookup"><span data-stu-id="c87ea-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="c87ea-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c87ea-116">Click Save.</span></span>
10. <span data-ttu-id="c87ea-117">Minge jaotisse Auditi töölaud > Seadistus > Auditipoliitikad.</span><span class="sxs-lookup"><span data-stu-id="c87ea-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="c87ea-118">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c87ea-118">Click New.</span></span>
12. <span data-ttu-id="c87ea-119">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c87ea-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="c87ea-120">Laiendage jaotist Poliitika organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="c87ea-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="c87ea-121">Valige puul Contoso Entertainment System USA.</span><span class="sxs-lookup"><span data-stu-id="c87ea-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="c87ea-122">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c87ea-122">Click Add.</span></span>
16. <span data-ttu-id="c87ea-123">Valige puul Contoso Consulting USA.</span><span class="sxs-lookup"><span data-stu-id="c87ea-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="c87ea-124">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c87ea-124">Click Add.</span></span>
18. <span data-ttu-id="c87ea-125">Valige puul Contoso Retail USA.</span><span class="sxs-lookup"><span data-stu-id="c87ea-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="c87ea-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c87ea-126">Click Add.</span></span>
20. <span data-ttu-id="c87ea-127">Ahendage jaotist Poliitika organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="c87ea-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="c87ea-128">Laiendage jaotist Poliitika reeglid.</span><span class="sxs-lookup"><span data-stu-id="c87ea-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="c87ea-129">Leidke ja valige loendist varem loodud poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="c87ea-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="c87ea-130">Klõpsake valikut Loo poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="c87ea-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="c87ea-131">Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="c87ea-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="c87ea-132">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="c87ea-132">Click Filter.</span></span>
26. <span data-ttu-id="c87ea-133">Valige loendist kulukategooria rida ja seadke üksikasjadeks Hotell</span><span class="sxs-lookup"><span data-stu-id="c87ea-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="c87ea-134">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="c87ea-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="c87ea-135">Klõpsake vahekaarti Koondamine.</span><span class="sxs-lookup"><span data-stu-id="c87ea-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="c87ea-136">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c87ea-136">Click Add.</span></span>
30. <span data-ttu-id="c87ea-137">Valige loendist kandesumma väärtus</span><span class="sxs-lookup"><span data-stu-id="c87ea-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="c87ea-138">Sisestage või valige väärtus väljal Väli.</span><span class="sxs-lookup"><span data-stu-id="c87ea-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="c87ea-139">Valige Summa väljal AggregateFunction.</span><span class="sxs-lookup"><span data-stu-id="c87ea-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="c87ea-140">Klõpsake vahekaarti Grupeerimisalus.</span><span class="sxs-lookup"><span data-stu-id="c87ea-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="c87ea-141">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c87ea-141">Click Add.</span></span>
35. <span data-ttu-id="c87ea-142">Valige loendist väärtus Töötaja </span><span class="sxs-lookup"><span data-stu-id="c87ea-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="c87ea-143">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c87ea-143">Click Add.</span></span>
37. <span data-ttu-id="c87ea-144">Valige loendist väärtus Kulukategooria</span><span class="sxs-lookup"><span data-stu-id="c87ea-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="c87ea-145">Sisestage või valige väärtus väljal Väli.</span><span class="sxs-lookup"><span data-stu-id="c87ea-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="c87ea-146">Klõpsake vahekaarti Saamine.</span><span class="sxs-lookup"><span data-stu-id="c87ea-146">Click the Having tab.</span></span>
40. <span data-ttu-id="c87ea-147">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c87ea-147">Click Add.</span></span>
41. <span data-ttu-id="c87ea-148">Valige Kandesumma</span><span class="sxs-lookup"><span data-stu-id="c87ea-148">Select Transaction amount</span></span>
42. <span data-ttu-id="c87ea-149">Sisestage või valige väärtus väljal Väli.</span><span class="sxs-lookup"><span data-stu-id="c87ea-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="c87ea-150">Valige Summa väljal AggregateFunction.</span><span class="sxs-lookup"><span data-stu-id="c87ea-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="c87ea-151">Sisestage väljale Kriteeriumid väärtus >2000.</span><span class="sxs-lookup"><span data-stu-id="c87ea-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="c87ea-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c87ea-152">Click OK.</span></span>
46. <span data-ttu-id="c87ea-153">Klõpsake nuppu Test.</span><span class="sxs-lookup"><span data-stu-id="c87ea-153">Click Test.</span></span>
47. <span data-ttu-id="c87ea-154">Sisestage kuupäev ja kellaaeg väljale Dokumendivaliku alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="c87ea-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="c87ea-155">Sisestage kuupäev ja kellaaeg väljale Dokumendivaliku lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="c87ea-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="c87ea-156">Klõpsake käsku Käivita test.</span><span class="sxs-lookup"><span data-stu-id="c87ea-156">Click Run test.</span></span>
50. <span data-ttu-id="c87ea-157">Klõpsake toimingupaanil valikut Auditipoliitika.</span><span class="sxs-lookup"><span data-stu-id="c87ea-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="c87ea-158">Klõpsa valikut Lisasuvandid.</span><span class="sxs-lookup"><span data-stu-id="c87ea-158">Click Additional options.</span></span>
52. <span data-ttu-id="c87ea-159">Sisestage kuupäev ja kellaaeg väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="c87ea-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="c87ea-160">Sisestage kuupäev ja kellaaeg väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="c87ea-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="c87ea-161">Klõpsake valikut Partii.</span><span class="sxs-lookup"><span data-stu-id="c87ea-161">Click Batch.</span></span>
55. <span data-ttu-id="c87ea-162">Laiendage jaotist Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="c87ea-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="c87ea-163">Valige suvand Jah väljal Pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="c87ea-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="c87ea-164">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c87ea-164">Click OK.</span></span>
58. <span data-ttu-id="c87ea-165">Minge jaotisse Auditi töölaud > Auditijuhtumid.</span><span class="sxs-lookup"><span data-stu-id="c87ea-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="c87ea-166">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c87ea-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="c87ea-167">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c87ea-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="c87ea-168">Laiendage jaotist Seosed.</span><span class="sxs-lookup"><span data-stu-id="c87ea-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="c87ea-169">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c87ea-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="c87ea-170">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c87ea-170">In the list, click the link in the selected row.</span></span>


