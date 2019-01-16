--- 
title: Elektrooniline aruandlus. Vormingu konfiguratsiooni loomine (november 2016)
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul."
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 13469aad7fdcefb3a1706eec0527f29968e007eb
ms.openlocfilehash: 10511fe5b936135471b522fc7152a54686a3be87
ms.contentlocale: et-ee
ms.lasthandoff: 12/18/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="209ef-103">Elektrooniline aruandlus. Vormingu konfiguratsiooni loomine (november 2016)</span><span class="sxs-lookup"><span data-stu-id="209ef-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="209ef-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul.</span><span class="sxs-lookup"><span data-stu-id="209ef-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="209ef-105">See vormingu konfiguratsioon määrab elektrooniliste dokumentide vormingu, mida maksete töötlemisel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="209ef-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="209ef-106">Selles näites loote vormingu konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Nende etappide lõpuleviimiseks peate kõigepealt läbima etapid protseduuris Andmemudeli vastendamine valitud andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="209ef-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="209ef-107">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="209ef-107">Create a new format configuration</span></span>
1. <span data-ttu-id="209ef-108">Avage **Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="209ef-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="209ef-109">Klõpsake valikut **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="209ef-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="209ef-110">Valige puul suvand **Maksed (lihtsustatud mudel)**.</span><span class="sxs-lookup"><span data-stu-id="209ef-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="209ef-111">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="209ef-111">Click **Create configuration** to open the drop dialog.</span></span>
 > [!NOTE]
 > <span data-ttu-id="209ef-112">Kui te ei näe valikut **Loo konfiguratsioon**, peate lubama kujundusrežiimi lehel **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="209ef-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
5. <span data-ttu-id="209ef-113">Sisestage väljale **Uus suvand** **Andmemudelil PaymentModel põhinev vorming**.</span><span class="sxs-lookup"><span data-stu-id="209ef-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="209ef-114">Sisestage väljale **Nimi** suvand **BACS (UK fiktiivne)**.</span><span class="sxs-lookup"><span data-stu-id="209ef-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="209ef-115">Sisestage väljale **Kirjeldus** suvand **BACS-i hankija maksevorming (UK fiktiivne)**.</span><span class="sxs-lookup"><span data-stu-id="209ef-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="209ef-116">Aktiivne konfiguratsiooni pakkuja sisestatakse siia automaatselt.</span><span class="sxs-lookup"><span data-stu-id="209ef-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="209ef-117">See pakkuja saab seda konfiguratsiooni hallata.</span><span class="sxs-lookup"><span data-stu-id="209ef-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="209ef-118">Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.</span><span class="sxs-lookup"><span data-stu-id="209ef-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="209ef-119">Määratleda saab elektroonilise dokumendi kindla vormingu.</span><span class="sxs-lookup"><span data-stu-id="209ef-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="209ef-120">Jätke see väli tühjaks, kui soovite valida vormingu käitusajal.</span><span class="sxs-lookup"><span data-stu-id="209ef-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="209ef-121">Sisestage või valige väärtus väljal **Andmemudeli definitsioon**.</span><span class="sxs-lookup"><span data-stu-id="209ef-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="209ef-122">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="209ef-122">Click **Create configuration**.</span></span> <span data-ttu-id="209ef-123">Uus konfiguratsioon on loodud.</span><span class="sxs-lookup"><span data-stu-id="209ef-123">A new configuration has been created.</span></span> <span data-ttu-id="209ef-124">Mustandversiooni saab kasutada vormingu kujunduse salvestamiseks elektrooniliste dokumentide haldamise puhul.</span><span class="sxs-lookup"><span data-stu-id="209ef-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  
 > [!NOTE]
 > <span data-ttu-id="209ef-125">Kui te ei näe valikut **Loo konfiguratsioon**, peate lubama kujundusrežiimi lehel **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="209ef-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="209ef-126">Elektroonilise dokumendi vormingu kujundus</span><span class="sxs-lookup"><span data-stu-id="209ef-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="209ef-127">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="209ef-127">Click **Designer**.</span></span>
2. <span data-ttu-id="209ef-128">Klõpsake suvandit **Lisa juur** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="209ef-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="209ef-129">Valige puul suvand **Üldine\Fail**.</span><span class="sxs-lookup"><span data-stu-id="209ef-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="209ef-130">Sisestage väljale **Nimi** suvand **Xml**.</span><span class="sxs-lookup"><span data-stu-id="209ef-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="209ef-131">Sisestage väljale **Kodeerimine** suvand **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="209ef-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="209ef-132">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-132">Click **OK**.</span></span>
7. <span data-ttu-id="209ef-133">Klõpsake vahekaarti **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="209ef-133">Click **Add**.</span></span>
8. <span data-ttu-id="209ef-134">Valige puul suvand **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="209ef-135">Sisestage väljale **Nimi** suvand **Teade**.</span><span class="sxs-lookup"><span data-stu-id="209ef-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="209ef-136">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-136">Click **OK**.</span></span>
11. <span data-ttu-id="209ef-137">Puuvaates valige **Xml\Teade**.</span><span class="sxs-lookup"><span data-stu-id="209ef-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="209ef-138">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="209ef-139">Sisestage väljale **Nimi** suvand **Töötlemiskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="209ef-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="209ef-140">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-140">Click **OK**.</span></span>
15. <span data-ttu-id="209ef-141">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="209ef-142">Sisestage väljale Nimi suvand **TeateId**.</span><span class="sxs-lookup"><span data-stu-id="209ef-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="209ef-143">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-143">Click **OK**.</span></span>
18. <span data-ttu-id="209ef-144">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="209ef-145">Sisestage väljale **Nimi** suvand **Maksed**.</span><span class="sxs-lookup"><span data-stu-id="209ef-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="209ef-146">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-146">Click **OK**.</span></span>
21. <span data-ttu-id="209ef-147">Puuvaates valige **Xml\Teade\Maksed**.</span><span class="sxs-lookup"><span data-stu-id="209ef-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="209ef-148">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="209ef-149">Sisestage väljale **Nimi** suvand **Kaup**.</span><span class="sxs-lookup"><span data-stu-id="209ef-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="209ef-150">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-150">Click **OK**.</span></span>
25. <span data-ttu-id="209ef-151">Puuvaates valige **Xml\Teade\Maksed\Kaup**.</span><span class="sxs-lookup"><span data-stu-id="209ef-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="209ef-152">Klõpsake vahekaarti **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="209ef-152">Click **Add**.</span></span>
27. <span data-ttu-id="209ef-153">Valige puul suvand **XML\Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="209ef-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="209ef-154">Sisestage väljale Nimi suvand **Id**.</span><span class="sxs-lookup"><span data-stu-id="209ef-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="209ef-155">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-155">Click **OK**.</span></span>
30. <span data-ttu-id="209ef-156">Klõpsake vahekaarti **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="209ef-156">Click **Add**.</span></span>
31. <span data-ttu-id="209ef-157">Valige puul suvand **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="209ef-158">Sisestage väljale Nimi suvand **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="209ef-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="209ef-159">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-159">Click **OK**.</span></span>
34. <span data-ttu-id="209ef-160">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija**.</span><span class="sxs-lookup"><span data-stu-id="209ef-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="209ef-161">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="209ef-162">Sisestage väljale Nimi suvand **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="209ef-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="209ef-163">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-163">Click **OK**.</span></span>
38. <span data-ttu-id="209ef-164">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="209ef-165">Sisestage väljale **Nimi** suvand **Pank**.</span><span class="sxs-lookup"><span data-stu-id="209ef-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="209ef-166">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-166">Click **OK**.</span></span>
41. <span data-ttu-id="209ef-167">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Pank**.</span><span class="sxs-lookup"><span data-stu-id="209ef-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="209ef-168">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="209ef-169">Sisestage väljale **Nimi** suvand **Marsruudinumber**.</span><span class="sxs-lookup"><span data-stu-id="209ef-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="209ef-170">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-170">Click **OK**.</span></span>
45. <span data-ttu-id="209ef-171">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="209ef-172">Sisestage väljale **Nimi** suvand **Kontonumber**.</span><span class="sxs-lookup"><span data-stu-id="209ef-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="209ef-173">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-173">Click **OK**.</span></span>
48. <span data-ttu-id="209ef-174">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija**.</span><span class="sxs-lookup"><span data-stu-id="209ef-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="209ef-175">Klõpsake käsku **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="209ef-175">Click **Copy**.</span></span>
50. <span data-ttu-id="209ef-176">Puuvaates valige **Xml\Teade\Maksed\Kaup**.</span><span class="sxs-lookup"><span data-stu-id="209ef-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="209ef-177">Klõpsake käsku **Kleebi**.</span><span class="sxs-lookup"><span data-stu-id="209ef-177">Click **Paste**.</span></span>
52. <span data-ttu-id="209ef-178">Sisestage väljale **Nimi** suvand **Maksja**.</span><span class="sxs-lookup"><span data-stu-id="209ef-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="209ef-179">Puuvaates valige **Xml\Teade\Maksed\Kaup**.</span><span class="sxs-lookup"><span data-stu-id="209ef-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="209ef-180">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="209ef-181">Sisestage väljale **Nimi** suvand **Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="209ef-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="209ef-182">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-182">Click **OK**.</span></span>
57. <span data-ttu-id="209ef-183">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="209ef-184">Sisestage väljale **Nimi** suvand **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="209ef-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="209ef-185">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-185">Click **OK**.</span></span>
60. <span data-ttu-id="209ef-186">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="209ef-187">Sisestage väljale Nimi suvand **Transkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="209ef-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="209ef-188">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-188">Click **OK**.</span></span>
63. <span data-ttu-id="209ef-189">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="209ef-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="209ef-190">Sisestage väljale Nimi suvand **Summa**.</span><span class="sxs-lookup"><span data-stu-id="209ef-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="209ef-191">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="209ef-192">Vormingu komponentide ettevalmistamine andmemudeli elementidega vastendamiseks</span><span class="sxs-lookup"><span data-stu-id="209ef-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="209ef-193">Puuvaates valige **Xml\Teade\Töötlemiskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="209ef-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="209ef-194">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="209ef-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="209ef-195">Puuvaates valige **Tekst\Kuupäev**”.</span><span class="sxs-lookup"><span data-stu-id="209ef-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="209ef-196">Sisestage väljale **Vorming** suvand **aaaa-kk-pp**.</span><span class="sxs-lookup"><span data-stu-id="209ef-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="209ef-197">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-197">Click **OK**.</span></span>
6. <span data-ttu-id="209ef-198">Puuvaates valige **Xml\Teade\Maksed\Kaup\Transkuupäev**”</span><span class="sxs-lookup"><span data-stu-id="209ef-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="209ef-199">Klõpsake valikut **Lisa kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="209ef-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="209ef-200">Sisestage väljale **Vorming** suvand **aaaa-kk-pp**.</span><span class="sxs-lookup"><span data-stu-id="209ef-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="209ef-201">Väljal **Kuupäev** valige **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="209ef-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="209ef-202">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-202">Click **OK**.</span></span>
11. <span data-ttu-id="209ef-203">Puuvaates valige **Xml\Teade\TeateId**.</span><span class="sxs-lookup"><span data-stu-id="209ef-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="209ef-204">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="209ef-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="209ef-205">Valige puul suvand **Tekst\String**.</span><span class="sxs-lookup"><span data-stu-id="209ef-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="209ef-206">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-206">Click **OK**.</span></span>
15. <span data-ttu-id="209ef-207">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Nimi**.</span><span class="sxs-lookup"><span data-stu-id="209ef-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="209ef-208">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="209ef-208">Click **Add String**.</span></span>
17. <span data-ttu-id="209ef-209">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-209">Click **OK**.</span></span>
18. <span data-ttu-id="209ef-210">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Pank\Marsruudinumber**.</span><span class="sxs-lookup"><span data-stu-id="209ef-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="209ef-211">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="209ef-211">Click **Add String**.</span></span>
20. <span data-ttu-id="209ef-212">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-212">Click **OK**.</span></span>
21. <span data-ttu-id="209ef-213">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Pank\Kontonumber**.</span><span class="sxs-lookup"><span data-stu-id="209ef-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="209ef-214">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="209ef-214">Click **Add String**.</span></span>
23. <span data-ttu-id="209ef-215">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-215">Click **OK**.</span></span>
24. <span data-ttu-id="209ef-216">Puuvaates valige **Xml\Teade\Maksed\Kaup\Maksed\Nimi**.</span><span class="sxs-lookup"><span data-stu-id="209ef-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="209ef-217">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="209ef-217">Click **Add String**.</span></span>
26. <span data-ttu-id="209ef-218">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-218">Click **OK**.</span></span>
27. <span data-ttu-id="209ef-219">Puuvaates valige **Xml\Teade\Maksed\Kaup\Maksja\Pank\Marsruudinumber**.</span><span class="sxs-lookup"><span data-stu-id="209ef-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="209ef-220">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="209ef-220">Click **Add String**.</span></span>
29. <span data-ttu-id="209ef-221">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-221">Click **OK**.</span></span>
30. <span data-ttu-id="209ef-222">Puuvaates valige **Xml\Teade\Maksed\Kaup\Maksja\Pank\Kontonumber**.</span><span class="sxs-lookup"><span data-stu-id="209ef-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="209ef-223">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="209ef-223">Click **Add String**.</span></span>
32. <span data-ttu-id="209ef-224">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-224">Click **OK**.</span></span>
33. <span data-ttu-id="209ef-225">Puuvaates valige **Xml\Teade\Maksed\Kaup\Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="209ef-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="209ef-226">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="209ef-226">Click **Add String**.</span></span>
35. <span data-ttu-id="209ef-227">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-227">Click **OK**.</span></span>
36. <span data-ttu-id="209ef-228">Puuvaates valige **Xml\Teade\Maksed\Kaup\Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="209ef-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="209ef-229">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="209ef-229">Click **Add String**.</span></span>
38. <span data-ttu-id="209ef-230">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-230">Click **OK**.</span></span>
39. <span data-ttu-id="209ef-231">Puuvaates valige **Xml\Teade\Maksed\Kaup\Summa**.</span><span class="sxs-lookup"><span data-stu-id="209ef-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="209ef-232">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="209ef-232">Click **Add String**.</span></span>
41. <span data-ttu-id="209ef-233">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="209ef-233">Click **OK**.</span></span>
42. <span data-ttu-id="209ef-234">Klõpsake nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="209ef-234">Click **Save**.</span></span>
43. <span data-ttu-id="209ef-235">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="209ef-235">Close the page.</span></span>


