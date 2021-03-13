---
title: Elektrooniline aruandlus. Loodud vormingu komponentide vastendamine andmemudeli elementidega (november 2016)
description: Selles teemas kirjeldatakse, kuidas vastendada andmemudeli elemente loodud elektroonilise aruandluse (ER) konfiguratsiooni komponentidega.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 043c66cf3345678aa7750ef50323700384579299
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093769"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="ef408-103">Elektrooniline aruandlus. Loodud vormingu komponentide vastendamine andmemudeli elementidega (november 2016)</span><span class="sxs-lookup"><span data-stu-id="ef408-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef408-104">Järgmine protseduur näitab, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis olev kasutaja saab vastendada andmemudeli elemente loodud elektroonilise aruandluse (ER) konfiguratsiooni komponentidega, mis määratleb maksete äridomeeni elektroonilise dokumendi.</span><span class="sxs-lookup"><span data-stu-id="ef408-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="ef408-105">Seda vormingut kasutatakse hiljem maksete töötlemiseks elektrooniliste dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="ef408-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="ef408-106">Selles näites saate luua vormingukonfiguratsiooni näidisettevõttele „Litware, Inc.”.</span><span class="sxs-lookup"><span data-stu-id="ef408-106">In this example, you will create a format configuration for the sample company, 'Litware, Inc.'.</span></span> <span data-ttu-id="ef408-107">Neid toiminguid saab teha igas ettevõttes, kuna ER-i konfiguratsioonid on kõigi ettevõtete vahel ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="ef408-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="ef408-108">Nende etappide lõpule viimiseks peate esmalt viima lõpule tegevusejuhises „Vormingu konfiguratsiooni loomine” esitatud etapid.</span><span class="sxs-lookup"><span data-stu-id="ef408-108">To complete these steps, you must first complete the steps in the "Create a format configuration" task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="ef408-109">Vormingu konfiguratsiooni valimine</span><span class="sxs-lookup"><span data-stu-id="ef408-109">Select a format configuration</span></span>
1. <span data-ttu-id="ef408-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="ef408-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ef408-111">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="ef408-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ef408-112">Laiendage puustruktuuris suvandit Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="ef408-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="ef408-113">Tehke puustruktuuris valik 'Maksed (lihtsustatud mudel)\BACS (UK fiktiivne)'.</span><span class="sxs-lookup"><span data-stu-id="ef408-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="ef408-114">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="ef408-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="ef408-115">Vormingu komponentide vastendamine andmemudeli elementidega</span><span class="sxs-lookup"><span data-stu-id="ef408-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="ef408-116">Klõpsake nuppu Laienda/ahenda.</span><span class="sxs-lookup"><span data-stu-id="ef408-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="ef408-117">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="ef408-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="ef408-118">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="ef408-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="ef408-119">Puuvaates valige „Xml\Teade\ProcessingDate\DateTime”.</span><span class="sxs-lookup"><span data-stu-id="ef408-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="ef408-120">Puuvaates valige „mudel\ProcessingDateTime”.</span><span class="sxs-lookup"><span data-stu-id="ef408-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="ef408-121">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-121">Click Bind.</span></span>
7. <span data-ttu-id="ef408-122">Puuvaates valige „Xml\Teade\MessageId\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="ef408-123">Puuvaates valige „mudel\MessageIdentification”.</span><span class="sxs-lookup"><span data-stu-id="ef408-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="ef408-124">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-124">Click Bind.</span></span>
10. <span data-ttu-id="ef408-125">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="ef408-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="ef408-126">Puuvaates valige „Xml\Teade\Maksed\Kaup\Summa\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="ef408-127">Puuvaates valige „mudel\Maksed\InstructedAmount”.</span><span class="sxs-lookup"><span data-stu-id="ef408-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="ef408-128">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-128">Click Bind.</span></span>
14. <span data-ttu-id="ef408-129">Puuvaates valige „Xml\Teated\Maksed\Kaup\TransDate\DateTime”.</span><span class="sxs-lookup"><span data-stu-id="ef408-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="ef408-130">Puuvaates valige „mudel\Maksed\TransactionDate”.</span><span class="sxs-lookup"><span data-stu-id="ef408-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="ef408-131">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-131">Click Bind.</span></span>
17. <span data-ttu-id="ef408-132">Puuvaates valige „Xml\Teade\Maksed\Kaup\Kirjeldus\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="ef408-133">Valige puul suvand model\Payments\Description.</span><span class="sxs-lookup"><span data-stu-id="ef408-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="ef408-134">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-134">Click Bind.</span></span>
20. <span data-ttu-id="ef408-135">Puuvaates valige „Xml\Teade\Maksed\Kaup\Valuuta\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="ef408-136">Valige puul väärtus model\Payments\Currency.</span><span class="sxs-lookup"><span data-stu-id="ef408-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="ef408-137">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-137">Click Bind.</span></span>
23. <span data-ttu-id="ef408-138">Puuvaates valige „Xml\Teade\Maksed\Kaup\ID”.</span><span class="sxs-lookup"><span data-stu-id="ef408-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="ef408-139">Puuvaates valige „mudel\Maksed\End2EndID”.</span><span class="sxs-lookup"><span data-stu-id="ef408-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="ef408-140">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-140">Click Bind.</span></span>
26. <span data-ttu-id="ef408-141">Laiendage puus sõlme model\Payments\Creditor.</span><span class="sxs-lookup"><span data-stu-id="ef408-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="ef408-142">Laiendage puus sõlme model\Payments\Creditor\Account.</span><span class="sxs-lookup"><span data-stu-id="ef408-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="ef408-143">Laiendage puus sõlme model\Payments\Creditor\Agent.</span><span class="sxs-lookup"><span data-stu-id="ef408-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="ef408-144">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Nimi\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="ef408-145">Valige puul suvand model\Payments\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="ef408-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="ef408-146">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-146">Click Bind.</span></span>
32. <span data-ttu-id="ef408-147">Puuvaates valige „Xml\Teated\Maksed\Kaup\Hankija\Pank\RoutingNumber\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="ef408-148">Puuvaates valige „mudel\Maksed\Kreeditor\Agent\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="ef408-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="ef408-149">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-149">Click Bind.</span></span>
35. <span data-ttu-id="ef408-150">Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\AccountNumber\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="ef408-151">Valige puul suvand model\Payments\Creditor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="ef408-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="ef408-152">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-152">Click Bind.</span></span>
38. <span data-ttu-id="ef408-153">Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Nimi\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="ef408-154">Laiendage puus sõlme model\Payments\Debtor.</span><span class="sxs-lookup"><span data-stu-id="ef408-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="ef408-155">Laiendage puus sõlme model\Payments\Debtor\Account.</span><span class="sxs-lookup"><span data-stu-id="ef408-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="ef408-156">Laiendage puus sõlme model\Payments\Debtor\Agent.</span><span class="sxs-lookup"><span data-stu-id="ef408-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="ef408-157">Valige puul suvand model\Payments\Debtor\Name.</span><span class="sxs-lookup"><span data-stu-id="ef408-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="ef408-158">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-158">Click Bind.</span></span>
44. <span data-ttu-id="ef408-159">Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\RoutingNumber\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="ef408-160">Puuvaates valige „mudel\Maksed\Deebitor\Agent\RoutingNumber”.</span><span class="sxs-lookup"><span data-stu-id="ef408-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="ef408-161">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-161">Click Bind.</span></span>
47. <span data-ttu-id="ef408-162">Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\AccountNumber\String”.</span><span class="sxs-lookup"><span data-stu-id="ef408-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="ef408-163">Valige puul suvand model\Payments\Debtor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="ef408-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="ef408-164">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-164">Click Bind.</span></span>
50. <span data-ttu-id="ef408-165">Puuvaates valige „Xml\Teade\Maksed\Kaup”.</span><span class="sxs-lookup"><span data-stu-id="ef408-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="ef408-166">Valige puul suvand model\Payments.</span><span class="sxs-lookup"><span data-stu-id="ef408-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="ef408-167">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="ef408-167">Click Bind.</span></span>
53. <span data-ttu-id="ef408-168">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ef408-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="ef408-169">Vormingu vastendamise kinnitamine</span><span class="sxs-lookup"><span data-stu-id="ef408-169">Validate format mapping</span></span>
1. <span data-ttu-id="ef408-170">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="ef408-170">Click Validate.</span></span>
    * <span data-ttu-id="ef408-171">Kinnitage uus vastendus tagamaks, et kõikide sidumistega on korras.</span><span class="sxs-lookup"><span data-stu-id="ef408-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="ef408-172">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ef408-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="ef408-173">Vormingu konfiguratsiooni praeguse versiooni oleku muutmine</span><span class="sxs-lookup"><span data-stu-id="ef408-173">Change status of the current version of format configuration</span></span>
<span data-ttu-id="ef408-174">Järgmistes etappides muudate vormingu konfiguratsiooni oleku suvandilt Mustand suvandile Lõpule viidud, et muuta see maksedokumendi loomiseks kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="ef408-174">In the next steps, you'll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="ef408-175">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="ef408-175">Click Change status.</span></span>
2. <span data-ttu-id="ef408-176">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="ef408-176">Click Complete.</span></span>
3. <span data-ttu-id="ef408-177">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ef408-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ef408-178">Näiteks „versioon 1”.</span><span class="sxs-lookup"><span data-stu-id="ef408-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="ef408-179">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ef408-179">Click OK.</span></span>
5. <span data-ttu-id="ef408-180">Valige praeguse konfiguratsiooni lõpuleviidud versioon.</span><span class="sxs-lookup"><span data-stu-id="ef408-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="ef408-181">Pange tähele, et konfiguratsioon salvestatakse kui lõpetatud versioon 1.1: andmemudeli versioonil 1 põhineva vormingu versioon 1.</span><span class="sxs-lookup"><span data-stu-id="ef408-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="ef408-182">Vormingu lõpetatud versiooni jõustumiskuupäeva määratlemine</span><span class="sxs-lookup"><span data-stu-id="ef408-182">Define effective date for completed version of format</span></span>
<span data-ttu-id="ef408-183">Iga vormingu versiooni saab konfigureerida kasutamiseks kättesaadavaks teatud kuupäevast alates.</span><span class="sxs-lookup"><span data-stu-id="ef408-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="ef408-184">Kui kindlal kuupäeval on aktiivne rohkem kui ühe vormingu versioon, valitakse kasutamiseks uusim vorming (versiooninumbri põhjal).</span><span class="sxs-lookup"><span data-stu-id="ef408-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="ef408-185">Õige versiooni valimiseks kasutatakse seansi kuupäeva väärtust.</span><span class="sxs-lookup"><span data-stu-id="ef408-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="ef408-186">Juurdepääsu piiramine loodud vormingult ettevõtetelt</span><span class="sxs-lookup"><span data-stu-id="ef408-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="ef408-187">Laiendage jaotist ISO-riigi-/regioonikoodid.</span><span class="sxs-lookup"><span data-stu-id="ef408-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="ef408-188">Iga vormingu juurdepääsu saab piirata, tuvastades teatud riigid/regioonid, kus vormingut rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="ef408-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="ef408-189">Kui teatud vormingu puhul on riikide/regioonide loend tühi, saab seda vormingut kasutada mis tahes ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="ef408-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="ef408-190">Kui riikide/regioonide loendisse sisestatakse mõni ISO-riigi/-regiooni kood, saab seda vormingut kasutada ainult ettevõtetes, mille peamine aadress on riigis/regioonis.</span><span class="sxs-lookup"><span data-stu-id="ef408-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  

