---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (1. osa – andmemudeli koostamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraator või elektroonilise aruandluse arendaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca295d651838f34106c9b91a53efc1f4faad4e4a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182481"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1-design-data-model"></a><span data-ttu-id="f8d16-103">Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (1. osa: andmemudeli koostamine)</span><span class="sxs-lookup"><span data-stu-id="f8d16-103">ER Use financial dimensions as a data source (Part 1: Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f8d16-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraator või elektroonilise aruandluse arendaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="f8d16-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f8d16-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="f8d16-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f8d16-106">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="f8d16-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="f8d16-107">Uue andmemudeli loomine</span><span class="sxs-lookup"><span data-stu-id="f8d16-107">Create a new data model</span></span>
1. <span data-ttu-id="f8d16-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f8d16-109">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="f8d16-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="f8d16-110">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="f8d16-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="f8d16-111">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="f8d16-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f8d16-112">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="f8d16-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="f8d16-113">Tippige väljale Nimi tekst Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="f8d16-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="f8d16-114">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="f8d16-114">Click Create configuration.</span></span>
6. <span data-ttu-id="f8d16-115">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="f8d16-115">Click Designer.</span></span>
7. <span data-ttu-id="f8d16-116">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="f8d16-117">Tippige väljale Nimi sõna Kirje.</span><span class="sxs-lookup"><span data-stu-id="f8d16-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="f8d16-118">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-118">Click Add.</span></span>
10. <span data-ttu-id="f8d16-119">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="f8d16-120">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="f8d16-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="f8d16-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-121">Click Add.</span></span>
    * <span data-ttu-id="f8d16-122">Lisame oma mudelile uue kirjete loendi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-122">We will add to our model a new record list.</span></span> <span data-ttu-id="f8d16-123">See loend toob välja (elektrooniliste aruannete puhul, kus seda mudelit andmeallikana kasutatakse) valitud finantsdimensioonide sätted.</span><span class="sxs-lookup"><span data-stu-id="f8d16-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="f8d16-124">Iga finantsdimensioon esitatakse selles loendis kirjena, millel on vastavad dimensiooni sätet kajastavad väljad.</span><span class="sxs-lookup"><span data-stu-id="f8d16-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="f8d16-125">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="f8d16-126">Tippige Dimensioonide seadistamine väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="f8d16-127">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="f8d16-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="f8d16-128">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-128">Click Add.</span></span>
17. <span data-ttu-id="f8d16-129">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="f8d16-130">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="f8d16-131">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="f8d16-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="f8d16-132">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-132">Click Add.</span></span>
21. <span data-ttu-id="f8d16-133">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="f8d16-134">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="f8d16-135">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-135">Click Add.</span></span>
24. <span data-ttu-id="f8d16-136">Valige puul väärtus Kirje.</span><span class="sxs-lookup"><span data-stu-id="f8d16-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="f8d16-137">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="f8d16-138">Tippige Tööleht väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="f8d16-139">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="f8d16-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="f8d16-140">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-140">Click Add.</span></span>
29. <span data-ttu-id="f8d16-141">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="f8d16-142">Tippige Partii väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="f8d16-143">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="f8d16-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="f8d16-144">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-144">Click Add.</span></span>
33. <span data-ttu-id="f8d16-145">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="f8d16-146">Tippige väljale Nimi valik Kanne.</span><span class="sxs-lookup"><span data-stu-id="f8d16-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="f8d16-147">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="f8d16-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="f8d16-148">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-148">Click Add.</span></span>
37. <span data-ttu-id="f8d16-149">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="f8d16-150">Tippige Kuupäev väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="f8d16-151">Valige väljalt Kaubakood suvand Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="f8d16-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="f8d16-152">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-152">Click Add.</span></span>
41. <span data-ttu-id="f8d16-153">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="f8d16-154">Tippige Deebet väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="f8d16-155">Valige väljalt Kaubakood suvand Tegelik.</span><span class="sxs-lookup"><span data-stu-id="f8d16-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="f8d16-156">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-156">Click Add.</span></span>
45. <span data-ttu-id="f8d16-157">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="f8d16-158">Tippige Kreedit väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="f8d16-159">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-159">Click Add.</span></span>
48. <span data-ttu-id="f8d16-160">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="f8d16-161">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="f8d16-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="f8d16-162">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="f8d16-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="f8d16-163">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-163">Click Add.</span></span>
52. <span data-ttu-id="f8d16-164">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="f8d16-165">Tippige Kanne väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="f8d16-166">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-166">Click Add.</span></span>
55. <span data-ttu-id="f8d16-167">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="f8d16-168">Tippige Dimensioonide andmed väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="f8d16-169">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="f8d16-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="f8d16-170">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-170">Click Add.</span></span>
    * <span data-ttu-id="f8d16-171">Lisasime oma mudelile uue kirjete loendi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-171">We added to our model a new record list.</span></span> <span data-ttu-id="f8d16-172">See loend toob välja (elektrooniliste aruannete puhul, kus seda mudelit andmeallikana kasutatakse) valitud finantsdimensioonide väärtused.</span><span class="sxs-lookup"><span data-stu-id="f8d16-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="f8d16-173">Iga finantsdimensioon esitatakse selles loendis kirjena, millel on vastavad dimensiooni väärtusi kajastavad väljad.</span><span class="sxs-lookup"><span data-stu-id="f8d16-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="f8d16-174">Selles kirjes esitatakse kasutatava väljana ka dimensiooni nimi, kui seda on valimiseks vaja.</span><span class="sxs-lookup"><span data-stu-id="f8d16-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="f8d16-175">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="f8d16-176">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="f8d16-177">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="f8d16-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="f8d16-178">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-178">Click Add.</span></span>
63. <span data-ttu-id="f8d16-179">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="f8d16-180">Sisestage väljale Nimi suvand Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="f8d16-181">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-181">Click Add.</span></span>
66. <span data-ttu-id="f8d16-182">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f8d16-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="f8d16-183">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="f8d16-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="f8d16-184">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f8d16-184">Click Add.</span></span>
69. <span data-ttu-id="f8d16-185">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f8d16-185">Click Save.</span></span>
70. <span data-ttu-id="f8d16-186">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f8d16-186">Close the page.</span></span>

