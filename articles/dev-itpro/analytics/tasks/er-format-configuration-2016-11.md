---
title: Elektrooniline aruandlus. Vormingu konfiguratsiooni loomine (november 2016)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul.
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 582e1a2baee805fe6770465edc7958954f638f1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544767"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="c80ea-103">Elektrooniline aruandlus. Vormingu konfiguratsiooni loomine (november 2016)</span><span class="sxs-lookup"><span data-stu-id="c80ea-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c80ea-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul.</span><span class="sxs-lookup"><span data-stu-id="c80ea-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="c80ea-105">See vormingu konfiguratsioon määrab elektrooniliste dokumentide vormingu, mida maksete töötlemisel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="c80ea-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="c80ea-106">Selles näites loote vormingu konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Nende etappide lõpuleviimiseks peate kõigepealt läbima etapid protseduuris Andmemudeli vastendamine valitud andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="c80ea-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="c80ea-107">Uue vormingu konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="c80ea-107">Create a new format configuration</span></span>
1. <span data-ttu-id="c80ea-108">Avage **Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="c80ea-109">Klõpsake valikut **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="c80ea-110">Valige puul suvand **Maksed (lihtsustatud mudel)**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="c80ea-111">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="c80ea-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="c80ea-112">Kui te ei näe valikut **Loo konfiguratsioon**, peate lubama kujundusrežiimi lehel **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="c80ea-113">Sisestage väljale **Uus suvand** **Andmemudelil PaymentModel põhinev vorming**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="c80ea-114">Sisestage väljale **Nimi** suvand **BACS (UK fiktiivne)**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="c80ea-115">Sisestage väljale **Kirjeldus** suvand **BACS-i hankija maksevorming (UK fiktiivne)**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="c80ea-116">Aktiivne konfiguratsiooni pakkuja sisestatakse siia automaatselt.</span><span class="sxs-lookup"><span data-stu-id="c80ea-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="c80ea-117">See pakkuja saab seda konfiguratsiooni hallata.</span><span class="sxs-lookup"><span data-stu-id="c80ea-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="c80ea-118">Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.</span><span class="sxs-lookup"><span data-stu-id="c80ea-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="c80ea-119">Määratleda saab elektroonilise dokumendi kindla vormingu.</span><span class="sxs-lookup"><span data-stu-id="c80ea-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="c80ea-120">Jätke see väli tühjaks, kui soovite valida vormingu käitusajal.</span><span class="sxs-lookup"><span data-stu-id="c80ea-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="c80ea-121">Sisestage või valige väärtus väljal **Andmemudeli definitsioon**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="c80ea-122">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-122">Click **Create configuration**.</span></span> <span data-ttu-id="c80ea-123">Uus konfiguratsioon on loodud.</span><span class="sxs-lookup"><span data-stu-id="c80ea-123">A new configuration has been created.</span></span> <span data-ttu-id="c80ea-124">Mustandversiooni saab kasutada vormingu kujunduse salvestamiseks elektrooniliste dokumentide haldamise puhul.</span><span class="sxs-lookup"><span data-stu-id="c80ea-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="c80ea-125">Elektroonilise dokumendi vormingu kujundus</span><span class="sxs-lookup"><span data-stu-id="c80ea-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="c80ea-126">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-126">Click **Designer**.</span></span>
2. <span data-ttu-id="c80ea-127">Klõpsake suvandit **Lisa juur** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c80ea-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="c80ea-128">Valige puul suvand **Üldine\Fail**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="c80ea-129">Sisestage väljale **Nimi** suvand **Xml**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="c80ea-130">Sisestage väljale **Kodeerimine** suvand **UTF-8**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="c80ea-131">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-131">Click **OK**.</span></span>
7. <span data-ttu-id="c80ea-132">Klõpsake vahekaarti **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-132">Click **Add**.</span></span>
8. <span data-ttu-id="c80ea-133">Valige puul suvand **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="c80ea-134">Sisestage väljale **Nimi** suvand **Teade**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="c80ea-135">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-135">Click **OK**.</span></span>
11. <span data-ttu-id="c80ea-136">Puuvaates valige **Xml\Teade**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="c80ea-137">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="c80ea-138">Sisestage väljale **Nimi** suvand **Töötlemiskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="c80ea-139">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-139">Click **OK**.</span></span>
15. <span data-ttu-id="c80ea-140">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="c80ea-141">Sisestage väljale Nimi suvand **TeateId**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="c80ea-142">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-142">Click **OK**.</span></span>
18. <span data-ttu-id="c80ea-143">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="c80ea-144">Sisestage väljale **Nimi** suvand **Maksed**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="c80ea-145">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-145">Click **OK**.</span></span>
21. <span data-ttu-id="c80ea-146">Puuvaates valige **Xml\Teade\Maksed**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="c80ea-147">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="c80ea-148">Sisestage väljale **Nimi** suvand **Kaup**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="c80ea-149">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-149">Click **OK**.</span></span>
25. <span data-ttu-id="c80ea-150">Puuvaates valige **Xml\Teade\Maksed\Kaup**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="c80ea-151">Klõpsake vahekaarti **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-151">Click **Add**.</span></span>
27. <span data-ttu-id="c80ea-152">Valige puul suvand **XML\Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="c80ea-153">Sisestage väljale Nimi suvand **Id**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="c80ea-154">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-154">Click **OK**.</span></span>
30. <span data-ttu-id="c80ea-155">Klõpsake vahekaarti **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-155">Click **Add**.</span></span>
31. <span data-ttu-id="c80ea-156">Valige puul suvand **XML\Element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="c80ea-157">Sisestage väljale Nimi suvand **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="c80ea-158">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-158">Click **OK**.</span></span>
34. <span data-ttu-id="c80ea-159">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="c80ea-160">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="c80ea-161">Sisestage väljale Nimi suvand **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="c80ea-162">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-162">Click **OK**.</span></span>
38. <span data-ttu-id="c80ea-163">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="c80ea-164">Sisestage väljale **Nimi** suvand **Pank**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="c80ea-165">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-165">Click **OK**.</span></span>
41. <span data-ttu-id="c80ea-166">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Pank**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="c80ea-167">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="c80ea-168">Sisestage väljale **Nimi** suvand **Marsruudinumber**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="c80ea-169">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-169">Click **OK**.</span></span>
45. <span data-ttu-id="c80ea-170">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="c80ea-171">Sisestage väljale **Nimi** suvand **Kontonumber**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="c80ea-172">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-172">Click **OK**.</span></span>
48. <span data-ttu-id="c80ea-173">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="c80ea-174">Klõpsake käsku **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-174">Click **Copy**.</span></span>
50. <span data-ttu-id="c80ea-175">Puuvaates valige **Xml\Teade\Maksed\Kaup**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="c80ea-176">Klõpsake käsku **Kleebi**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-176">Click **Paste**.</span></span>
52. <span data-ttu-id="c80ea-177">Sisestage väljale **Nimi** suvand **Maksja**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="c80ea-178">Puuvaates valige **Xml\Teade\Maksed\Kaup**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="c80ea-179">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="c80ea-180">Sisestage väljale **Nimi** suvand **Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="c80ea-181">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-181">Click **OK**.</span></span>
57. <span data-ttu-id="c80ea-182">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="c80ea-183">Sisestage väljale **Nimi** suvand **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="c80ea-184">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-184">Click **OK**.</span></span>
60. <span data-ttu-id="c80ea-185">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="c80ea-186">Sisestage väljale Nimi suvand **Transkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="c80ea-187">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-187">Click **OK**.</span></span>
63. <span data-ttu-id="c80ea-188">Klõpsake käsku **Lisa element**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="c80ea-189">Sisestage väljale Nimi suvand **Summa**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="c80ea-190">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="c80ea-191">Vormingu komponentide ettevalmistamine andmemudeli elementidega vastendamiseks</span><span class="sxs-lookup"><span data-stu-id="c80ea-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="c80ea-192">Puuvaates valige **Xml\Teade\Töötlemiskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="c80ea-193">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c80ea-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="c80ea-194">Puuvaates valige **Tekst\Kuupäev**”.</span><span class="sxs-lookup"><span data-stu-id="c80ea-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="c80ea-195">Sisestage väljale **Vorming** suvand **aaaa-kk-pp**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="c80ea-196">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-196">Click **OK**.</span></span>
6. <span data-ttu-id="c80ea-197">Puuvaates valige **Xml\Teade\Maksed\Kaup\Transkuupäev**”</span><span class="sxs-lookup"><span data-stu-id="c80ea-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="c80ea-198">Klõpsake valikut **Lisa kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="c80ea-199">Sisestage väljale **Vorming** suvand **aaaa-kk-pp**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="c80ea-200">Väljal **Kuupäev** valige **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="c80ea-201">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-201">Click **OK**.</span></span>
11. <span data-ttu-id="c80ea-202">Puuvaates valige **Xml\Teade\TeateId**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="c80ea-203">Klõpsake valikut **Lisa** rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="c80ea-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="c80ea-204">Valige puul suvand **Tekst\String**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="c80ea-205">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-205">Click **OK**.</span></span>
15. <span data-ttu-id="c80ea-206">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Nimi**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="c80ea-207">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-207">Click **Add String**.</span></span>
17. <span data-ttu-id="c80ea-208">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-208">Click **OK**.</span></span>
18. <span data-ttu-id="c80ea-209">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Pank\Marsruudinumber**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="c80ea-210">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-210">Click **Add String**.</span></span>
20. <span data-ttu-id="c80ea-211">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-211">Click **OK**.</span></span>
21. <span data-ttu-id="c80ea-212">Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Pank\Kontonumber**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="c80ea-213">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-213">Click **Add String**.</span></span>
23. <span data-ttu-id="c80ea-214">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-214">Click **OK**.</span></span>
24. <span data-ttu-id="c80ea-215">Puuvaates valige **Xml\Teade\Maksed\Kaup\Maksed\Nimi**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="c80ea-216">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-216">Click **Add String**.</span></span>
26. <span data-ttu-id="c80ea-217">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-217">Click **OK**.</span></span>
27. <span data-ttu-id="c80ea-218">Puuvaates valige **Xml\Teade\Maksed\Kaup\Maksja\Pank\Marsruudinumber**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="c80ea-219">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-219">Click **Add String**.</span></span>
29. <span data-ttu-id="c80ea-220">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-220">Click **OK**.</span></span>
30. <span data-ttu-id="c80ea-221">Puuvaates valige **Xml\Teade\Maksed\Kaup\Maksja\Pank\Kontonumber**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="c80ea-222">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-222">Click **Add String**.</span></span>
32. <span data-ttu-id="c80ea-223">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-223">Click **OK**.</span></span>
33. <span data-ttu-id="c80ea-224">Puuvaates valige **Xml\Teade\Maksed\Kaup\Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="c80ea-225">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-225">Click **Add String**.</span></span>
35. <span data-ttu-id="c80ea-226">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-226">Click **OK**.</span></span>
36. <span data-ttu-id="c80ea-227">Puuvaates valige **Xml\Teade\Maksed\Kaup\Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="c80ea-228">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-228">Click **Add String**.</span></span>
38. <span data-ttu-id="c80ea-229">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-229">Click **OK**.</span></span>
39. <span data-ttu-id="c80ea-230">Puuvaates valige **Xml\Teade\Maksed\Kaup\Summa**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="c80ea-231">Klõpsake käsku **Lisa string**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-231">Click **Add String**.</span></span>
41. <span data-ttu-id="c80ea-232">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-232">Click **OK**.</span></span>
42. <span data-ttu-id="c80ea-233">Klõpsake nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c80ea-233">Click **Save**.</span></span>
43. <span data-ttu-id="c80ea-234">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c80ea-234">Close the page.</span></span>

