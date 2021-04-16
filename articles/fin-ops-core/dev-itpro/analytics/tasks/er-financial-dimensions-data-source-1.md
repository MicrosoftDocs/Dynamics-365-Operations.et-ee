---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (1. osa – andmemudeli koostamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) mudelit kasutama finantsdimensioone andmeallikana ER-i aruannetele. (1. osa)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92b44532dfae70f03d6686ca1d2f8b6f74345ee6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752456"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="67477-104">Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (1. osa – andmemudeli koostamine)</span><span class="sxs-lookup"><span data-stu-id="67477-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67477-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraator või elektroonilise aruandluse arendaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="67477-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="67477-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="67477-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="67477-107">Etappide lõpule viimiseks, peate esmalt läbima protseduuri „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” etapid.</span><span class="sxs-lookup"><span data-stu-id="67477-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="67477-108">Uue andmemudeli loomine</span><span class="sxs-lookup"><span data-stu-id="67477-108">Create a new data model</span></span>
1. <span data-ttu-id="67477-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="67477-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="67477-110">Veenduge, et „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="67477-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="67477-111">pakkuja on saadaval ja märgitud aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="67477-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="67477-112">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="67477-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="67477-113">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="67477-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="67477-114">Tippige väljale Nimi tekst Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="67477-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="67477-115">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="67477-115">Click Create configuration.</span></span>
6. <span data-ttu-id="67477-116">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="67477-116">Click Designer.</span></span>
7. <span data-ttu-id="67477-117">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="67477-118">Tippige väljale Nimi sõna Kirje.</span><span class="sxs-lookup"><span data-stu-id="67477-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="67477-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-119">Click Add.</span></span>
10. <span data-ttu-id="67477-120">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="67477-121">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="67477-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="67477-122">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-122">Click Add.</span></span>
    * <span data-ttu-id="67477-123">Lisame oma mudelile uue kirjete loendi.</span><span class="sxs-lookup"><span data-stu-id="67477-123">We will add to our model a new record list.</span></span> <span data-ttu-id="67477-124">See loend toob välja (elektrooniliste aruannete puhul, kus seda mudelit andmeallikana kasutatakse) valitud finantsdimensioonide sätted.</span><span class="sxs-lookup"><span data-stu-id="67477-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="67477-125">Iga finantsdimensioon esitatakse selles loendis kirjena, millel on vastavad dimensiooni sätet kajastavad väljad.</span><span class="sxs-lookup"><span data-stu-id="67477-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="67477-126">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="67477-127">Tippige Dimensioonide seadistamine väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="67477-128">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="67477-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="67477-129">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-129">Click Add.</span></span>
17. <span data-ttu-id="67477-130">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="67477-131">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="67477-132">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="67477-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="67477-133">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-133">Click Add.</span></span>
21. <span data-ttu-id="67477-134">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="67477-135">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="67477-136">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-136">Click Add.</span></span>
24. <span data-ttu-id="67477-137">Valige puul väärtus Kirje.</span><span class="sxs-lookup"><span data-stu-id="67477-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="67477-138">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="67477-139">Tippige Tööleht väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="67477-140">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="67477-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="67477-141">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-141">Click Add.</span></span>
29. <span data-ttu-id="67477-142">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="67477-143">Tippige Partii väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="67477-144">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="67477-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="67477-145">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-145">Click Add.</span></span>
33. <span data-ttu-id="67477-146">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="67477-147">Tippige väljale Nimi valik Kanne.</span><span class="sxs-lookup"><span data-stu-id="67477-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="67477-148">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="67477-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="67477-149">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-149">Click Add.</span></span>
37. <span data-ttu-id="67477-150">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="67477-151">Tippige Kuupäev väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="67477-152">Valige väljalt Kaubakood suvand Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="67477-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="67477-153">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-153">Click Add.</span></span>
41. <span data-ttu-id="67477-154">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="67477-155">Tippige Deebet väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="67477-156">Valige väljalt Kaubakood suvand Tegelik.</span><span class="sxs-lookup"><span data-stu-id="67477-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="67477-157">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-157">Click Add.</span></span>
45. <span data-ttu-id="67477-158">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="67477-159">Tippige Kreedit väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="67477-160">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-160">Click Add.</span></span>
48. <span data-ttu-id="67477-161">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="67477-162">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="67477-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="67477-163">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="67477-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="67477-164">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-164">Click Add.</span></span>
52. <span data-ttu-id="67477-165">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="67477-166">Tippige Kanne väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="67477-167">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-167">Click Add.</span></span>
55. <span data-ttu-id="67477-168">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="67477-169">Tippige Dimensioonide andmed väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="67477-170">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="67477-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="67477-171">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-171">Click Add.</span></span>
    * <span data-ttu-id="67477-172">Lisasime oma mudelile uue kirjete loendi.</span><span class="sxs-lookup"><span data-stu-id="67477-172">We added to our model a new record list.</span></span> <span data-ttu-id="67477-173">See loend toob välja (elektrooniliste aruannete puhul, kus seda mudelit andmeallikana kasutatakse) valitud finantsdimensioonide väärtused.</span><span class="sxs-lookup"><span data-stu-id="67477-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="67477-174">Iga finantsdimensioon esitatakse selles loendis kirjena, millel on vastavad dimensiooni väärtusi kajastavad väljad.</span><span class="sxs-lookup"><span data-stu-id="67477-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="67477-175">Selles kirjes esitatakse kasutatava väljana ka dimensiooni nimi, kui seda on valimiseks vaja.</span><span class="sxs-lookup"><span data-stu-id="67477-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="67477-176">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="67477-177">Tippige Kood väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="67477-178">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="67477-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="67477-179">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-179">Click Add.</span></span>
63. <span data-ttu-id="67477-180">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="67477-181">Sisestage väljale Nimi suvand Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="67477-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="67477-182">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-182">Click Add.</span></span>
66. <span data-ttu-id="67477-183">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67477-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="67477-184">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="67477-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="67477-185">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="67477-185">Click Add.</span></span>
69. <span data-ttu-id="67477-186">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="67477-186">Click Save.</span></span>
70. <span data-ttu-id="67477-187">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="67477-187">Close the page.</span></span>

![ER-i andmemudeli kujundaja leht](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]