---
title: Lähtedokumentide jaoks auditipoliitikate määratlemine
description: Selles protseduuris näitlikustatakse, kuidas seadistada ja käitada auditi poliitikareegleid.
author: ryansandness
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17b712f07a0ffe6874eb6d98b47ced96f5a54483
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846483"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="8ba24-103">Lähtedokumentide jaoks auditipoliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="8ba24-103">Define audit policies for source documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ba24-104">Selles protseduuris näitlikustatakse, kuidas seadistada ja käitada auditi poliitikareegleid.</span><span class="sxs-lookup"><span data-stu-id="8ba24-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="8ba24-105">Näites kasutatakse hotelli kulu tüübiga kuluaruandeid.</span><span class="sxs-lookup"><span data-stu-id="8ba24-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="8ba24-106">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="8ba24-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="8ba24-107">Audiitori roll sisaldab nende ülesannete teostamiseks vajalikke õigusi.</span><span class="sxs-lookup"><span data-stu-id="8ba24-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="8ba24-108">Minge jaotisse Auditi töölaud > Seadistus > Poliitika reegli tüüp.</span><span class="sxs-lookup"><span data-stu-id="8ba24-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="8ba24-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8ba24-109">Click New.</span></span>
3. <span data-ttu-id="8ba24-110">Sisestage väärtus väljale Reegli nimi.</span><span class="sxs-lookup"><span data-stu-id="8ba24-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="8ba24-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="8ba24-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8ba24-112">Valige Kuluaruande rida väljal Päringu nimi</span><span class="sxs-lookup"><span data-stu-id="8ba24-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="8ba24-113">Valige Koonda väljal Päringu tüüp.</span><span class="sxs-lookup"><span data-stu-id="8ba24-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="8ba24-114">Valige Juriidiline isik väljal Juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="8ba24-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="8ba24-115">Valige Muudetud kuupäev ja kellaaeg väljal Dokumendi kuupäeva viide</span><span class="sxs-lookup"><span data-stu-id="8ba24-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="8ba24-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="8ba24-116">Click Save.</span></span>
10. <span data-ttu-id="8ba24-117">Minge jaotisse Auditi töölaud > Seadistus > Auditipoliitikad.</span><span class="sxs-lookup"><span data-stu-id="8ba24-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="8ba24-118">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8ba24-118">Click New.</span></span>
12. <span data-ttu-id="8ba24-119">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="8ba24-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="8ba24-120">Laiendage jaotist Poliitika organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="8ba24-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="8ba24-121">Valige puul Contoso Entertainment System USA.</span><span class="sxs-lookup"><span data-stu-id="8ba24-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="8ba24-122">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8ba24-122">Click Add.</span></span>
16. <span data-ttu-id="8ba24-123">Valige puul Contoso Consulting USA.</span><span class="sxs-lookup"><span data-stu-id="8ba24-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="8ba24-124">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8ba24-124">Click Add.</span></span>
18. <span data-ttu-id="8ba24-125">Valige puul Contoso Retail USA.</span><span class="sxs-lookup"><span data-stu-id="8ba24-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="8ba24-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8ba24-126">Click Add.</span></span>
20. <span data-ttu-id="8ba24-127">Ahendage jaotist Poliitika organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="8ba24-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="8ba24-128">Laiendage jaotist Poliitika reeglid.</span><span class="sxs-lookup"><span data-stu-id="8ba24-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="8ba24-129">Leidke ja valige loendist varem loodud poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="8ba24-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="8ba24-130">Klõpsake valikut Loo poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="8ba24-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="8ba24-131">Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="8ba24-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="8ba24-132">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="8ba24-132">Click Filter.</span></span>
26. <span data-ttu-id="8ba24-133">Valige loendist kulukategooria rida ja seadke üksikasjadeks Hotell</span><span class="sxs-lookup"><span data-stu-id="8ba24-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="8ba24-134">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="8ba24-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="8ba24-135">Klõpsake vahekaarti Koondamine.</span><span class="sxs-lookup"><span data-stu-id="8ba24-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="8ba24-136">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8ba24-136">Click Add.</span></span>
30. <span data-ttu-id="8ba24-137">Valige loendist kandesumma väärtus</span><span class="sxs-lookup"><span data-stu-id="8ba24-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="8ba24-138">Sisestage või valige väärtus väljal Väli.</span><span class="sxs-lookup"><span data-stu-id="8ba24-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="8ba24-139">Valige Summa väljal AggregateFunction.</span><span class="sxs-lookup"><span data-stu-id="8ba24-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="8ba24-140">Klõpsake vahekaarti Grupeerimisalus.</span><span class="sxs-lookup"><span data-stu-id="8ba24-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="8ba24-141">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8ba24-141">Click Add.</span></span>
35. <span data-ttu-id="8ba24-142">Valige loendist väärtus Töötaja </span><span class="sxs-lookup"><span data-stu-id="8ba24-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="8ba24-143">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8ba24-143">Click Add.</span></span>
37. <span data-ttu-id="8ba24-144">Valige loendist väärtus Kulukategooria</span><span class="sxs-lookup"><span data-stu-id="8ba24-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="8ba24-145">Sisestage või valige väärtus väljal Väli.</span><span class="sxs-lookup"><span data-stu-id="8ba24-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="8ba24-146">Klõpsake vahekaarti Saamine.</span><span class="sxs-lookup"><span data-stu-id="8ba24-146">Click the Having tab.</span></span>
40. <span data-ttu-id="8ba24-147">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8ba24-147">Click Add.</span></span>
41. <span data-ttu-id="8ba24-148">Valige Kandesumma</span><span class="sxs-lookup"><span data-stu-id="8ba24-148">Select Transaction amount</span></span>
42. <span data-ttu-id="8ba24-149">Sisestage või valige väärtus väljal Väli.</span><span class="sxs-lookup"><span data-stu-id="8ba24-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="8ba24-150">Valige Summa väljal AggregateFunction.</span><span class="sxs-lookup"><span data-stu-id="8ba24-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="8ba24-151">Sisestage väljale Kriteeriumid väärtus >2000.</span><span class="sxs-lookup"><span data-stu-id="8ba24-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="8ba24-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8ba24-152">Click OK.</span></span>
46. <span data-ttu-id="8ba24-153">Klõpsake nuppu Test.</span><span class="sxs-lookup"><span data-stu-id="8ba24-153">Click Test.</span></span>
47. <span data-ttu-id="8ba24-154">Sisestage kuupäev ja kellaaeg väljale Dokumendivaliku alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="8ba24-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="8ba24-155">Sisestage kuupäev ja kellaaeg väljale Dokumendivaliku lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="8ba24-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="8ba24-156">Klõpsake käsku Käivita test.</span><span class="sxs-lookup"><span data-stu-id="8ba24-156">Click Run test.</span></span>
50. <span data-ttu-id="8ba24-157">Klõpsake toimingupaanil valikut Auditipoliitika.</span><span class="sxs-lookup"><span data-stu-id="8ba24-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="8ba24-158">Klõpsa valikut Lisasuvandid.</span><span class="sxs-lookup"><span data-stu-id="8ba24-158">Click Additional options.</span></span>
52. <span data-ttu-id="8ba24-159">Sisestage kuupäev ja kellaaeg väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="8ba24-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="8ba24-160">Sisestage kuupäev ja kellaaeg väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="8ba24-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="8ba24-161">Klõpsake valikut Partii.</span><span class="sxs-lookup"><span data-stu-id="8ba24-161">Click Batch.</span></span>
55. <span data-ttu-id="8ba24-162">Laiendage jaotist Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="8ba24-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="8ba24-163">Valige suvand Jah väljal Pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="8ba24-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="8ba24-164">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8ba24-164">Click OK.</span></span>
58. <span data-ttu-id="8ba24-165">Minge jaotisse Auditi töölaud > Auditijuhtumid.</span><span class="sxs-lookup"><span data-stu-id="8ba24-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="8ba24-166">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="8ba24-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="8ba24-167">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8ba24-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="8ba24-168">Laiendage jaotist Seosed.</span><span class="sxs-lookup"><span data-stu-id="8ba24-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="8ba24-169">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="8ba24-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="8ba24-170">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8ba24-170">In the list, click the link in the selected row.</span></span>

