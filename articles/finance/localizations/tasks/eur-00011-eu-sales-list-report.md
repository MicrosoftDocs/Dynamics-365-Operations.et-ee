---
title: EUR-00011 EL-i müügiloendi aruande koostamine
description: See protseduur juhatab teid läbi EL-i käibearuande koostamise protseduuri.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7038af3977797a0be2523f2414800400757b7007
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183597"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a><span data-ttu-id="d0c4f-103">EUR-00011 EL-i müügiloendi aruande koostamine</span><span class="sxs-lookup"><span data-stu-id="d0c4f-103">EUR-00011 Generate the EU sales list report</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0c4f-104">See protseduur juhatab teid läbi EL-i käibearuande koostamise protseduuri.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-104">This procedure walks you through generating the EU sales list report.</span></span> <span data-ttu-id="d0c4f-105">See hõlmab ühendusesisese kaubanduse kannete edastamist ELi käibearuandesse ja aruande käivitamist.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-105">This includes transferring intra-community trade transactions to the EU sales list and running the report.</span></span> <span data-ttu-id="d0c4f-106">See protseduur hõlmab ka ühendusesisese kaubanduse kande loomist demonstreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-106">This procedure also includes creating an intra-community trade transaction for demo purposes.</span></span> <span data-ttu-id="d0c4f-107">Lisateavet EL-i müügiloendi aruandluse, sh nõutavate eeltingimuste kohta leiate spikrist.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-107">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="d0c4f-108">See protseduur kohaldub kõigile Euroopa riikidele/piirkondadele.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-108">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="d0c4f-109">Protseduuri loomisel kasutatakse demoettevõtte DEMF andmeid, seega on kodumaise riigi/piirkonna näiteks Saksamaa.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-109">The procedure was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="d0c4f-110">Protseduur kasutab EL-i riigi/piirkonna näitena ka Portugali.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-110">The procedure also uses Portugal as an exemplar EU country/region.</span></span> <span data-ttu-id="d0c4f-111">Enne selle protseduuri läbimist tuleb konfigureerida EL-i käibearuandlus.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-111">Before you can complete this procedure, you must configure EU sales list reporting.</span></span>

<span data-ttu-id="d0c4f-112">See protseduur on mõeldud raamatupidajatele.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-112">This procedure is intended for accountants.</span></span>


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a><span data-ttu-id="d0c4f-113">Ühendusesisese müügikande loomine demonstreerimiseks</span><span class="sxs-lookup"><span data-stu-id="d0c4f-113">Create an intra-community sales transaction for demo purposes</span></span>
1. <span data-ttu-id="d0c4f-114">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-114">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="d0c4f-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-115">Click New.</span></span>
3. <span data-ttu-id="d0c4f-116">Sisestage väljale Kliendi konto tekst „PRT-001”.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-116">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="d0c4f-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-117">Click OK.</span></span>
5. <span data-ttu-id="d0c4f-118">Sisestage väljale Kaubakood tüüp D0001.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-118">In the Item number field, type 'D0001'.</span></span>
6. <span data-ttu-id="d0c4f-119">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-119">Expand the Line details section.</span></span>
7. <span data-ttu-id="d0c4f-120">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-120">Click the Setup tab.</span></span>
8. <span data-ttu-id="d0c4f-121">Sisestage FULL väljale Kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-121">In the Item sales tax group field, type 'FULL'.</span></span>
9. <span data-ttu-id="d0c4f-122">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-122">Click Add line.</span></span>
10. <span data-ttu-id="d0c4f-123">Sisestage väljale Kaubakood tüüp D0003.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-123">In the Item number field, type 'D0003'.</span></span>
11. <span data-ttu-id="d0c4f-124">Sisestage RED väljale Kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-124">In the Item sales tax group field, type 'RED'.</span></span>
12. <span data-ttu-id="d0c4f-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-125">Click Save.</span></span>
13. <span data-ttu-id="d0c4f-126">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-126">On the Action Pane, click Invoice.</span></span>
14. <span data-ttu-id="d0c4f-127">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-127">Click Invoice.</span></span>
15. <span data-ttu-id="d0c4f-128">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-128">Expand the Parameters section.</span></span>
16. <span data-ttu-id="d0c4f-129">Valige väljal Kogus väärtus Kõik.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-129">In the Quantity field, select 'All'.</span></span>
17. <span data-ttu-id="d0c4f-130">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-130">Expand the Setup section.</span></span>
18. <span data-ttu-id="d0c4f-131">Määrake väljal Arve kuupäev kuupäevaks 01/11/2016.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-131">In the Invoice date field, set the date to '01/11/2016'.</span></span>
19. <span data-ttu-id="d0c4f-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-132">Click OK.</span></span>
20. <span data-ttu-id="d0c4f-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-133">Click OK.</span></span>

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a><span data-ttu-id="d0c4f-134">Ühendusesisese kaubanduse kannete edastamine ELi käibearuandesse</span><span class="sxs-lookup"><span data-stu-id="d0c4f-134">Transfer intra-community trade transactions to the EU sales list</span></span>
1. <span data-ttu-id="d0c4f-135">Avage Maks > Deklaratsioonid > Väliskaubandus > EL-i käibearuanne.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-135">Go to Tax > Declarations > Foreign trade > EU sales list.</span></span>
2. <span data-ttu-id="d0c4f-136">Klõpsake käsku Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-136">Click Transfer.</span></span>
3. <span data-ttu-id="d0c4f-137">Kauba kannete edastamiseks valige Jah väljal Kaup.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-137">Select Yes in the Item field to transfer item transactions.</span></span>
4. <span data-ttu-id="d0c4f-138">Teenuse kannete edastamiseks valige Jah väljal Teenus.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-138">Select Yes in the Service field to transfer service transactions.</span></span>
    * <span data-ttu-id="d0c4f-139">Saate määrata lisafiltreid ka edastatavatele ühendusesisese kaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-139">You can also specify additional filters on intra-community trade transactions to transfer.</span></span>  
5. <span data-ttu-id="d0c4f-140">Klõpsake käsku Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-140">Click Transfer.</span></span>
    * <span data-ttu-id="d0c4f-141">Kontrollige, et ühendusesisene müügitehing on edukalt EL-i käibearuandesse edastatud.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-141">Verify that the intra-community sales transaction is successfully transferred to the EU sales list.</span></span>  

## <a name="generate-the-eu-sales-list-report"></a><span data-ttu-id="d0c4f-142">EL-i käibearuande loomine</span><span class="sxs-lookup"><span data-stu-id="d0c4f-142">Generate the EU sales list report</span></span>
1. <span data-ttu-id="d0c4f-143">Klõpsake vahekaarti Aruandlus.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-143">Click Reporting.</span></span>
2. <span data-ttu-id="d0c4f-144">Valige Igakuine väljal Aruandlusperiood.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-144">In the Reporting period field, select 'Monthly'.</span></span>
3. <span data-ttu-id="d0c4f-145">Määrake väljal Alguskuupäev kuupäevaks 01/01/2016.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-145">In the From date field, set the date to '01/01/2016'.</span></span>
4. <span data-ttu-id="d0c4f-146">Valige Jah väljal Loo fail.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-146">Select Yes in the Generate file field.</span></span>
5. <span data-ttu-id="d0c4f-147">Valige Jah väljal Loo aruanne.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-147">Select Yes in the Generate report field.</span></span>
6. <span data-ttu-id="d0c4f-148">Tippige väljale Faili nimi väärtus EUSalesList.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-148">In the File name field, type 'EUSalesList'.</span></span>
7. <span data-ttu-id="d0c4f-149">Tippige väljale Aruandefaili nimi väärtus EUSalesList.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-149">In the Report file name field, type 'EUSalesList'.</span></span>
8. <span data-ttu-id="d0c4f-150">Tippige väljale EL-i käibearuande registreerimise ID väärtus 123.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-150">In the EU Sales List Registration ID field, type '123'.</span></span>
    * <span data-ttu-id="d0c4f-151">See väli on saadaval ainult Saksamaa puhul.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-151">This field is only available for Germany.</span></span>  
    * <span data-ttu-id="d0c4f-152">Saate määrata lisafiltreid ka aruandesse lisatavatele ühendusesisese kaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-152">You can also specify additional filters on intra-community trade transactions to include in the report.</span></span>  
9. <span data-ttu-id="d0c4f-153">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-153">Click OK.</span></span>
    * <span data-ttu-id="d0c4f-154">Kontrollige, et kuvatakse hüpikaknad, mis kinnitavad faili ja kontrollaruande allalaadimist.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-154">Verify that pop-up windows appear to confirm that the file and the control report are being downloaded.</span></span>  

## <a name="mark-eu-sales-list-lines-as-reported"></a><span data-ttu-id="d0c4f-155">ELi käibearuande ridade esitatuks märkimine</span><span class="sxs-lookup"><span data-stu-id="d0c4f-155">Mark EU sales list lines as Reported</span></span>
1. <span data-ttu-id="d0c4f-156">Klõpsake käsku Märgi.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-156">Click Mark.</span></span>
2. <span data-ttu-id="d0c4f-157">Klõpsake käsku Märgi esitatuks.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-157">Click Mark as reported.</span></span>
3. <span data-ttu-id="d0c4f-158">Valige loendist välja Arve kuupäev rida.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-158">In the list, select the row for the Invoice date field.</span></span>
4. <span data-ttu-id="d0c4f-159">Tippige väljale Kriteerium väärtus 01/01/2016..01/31/2016.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-159">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="d0c4f-160">Valige loendist rida väljale Aruandluse olek.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-160">In the list, select the row for the Reporting status field.</span></span>
6. <span data-ttu-id="d0c4f-161">Valige väljal Kriteeriumid väärtus Kaasatud.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-161">In the Criteria field, select 'Included'.</span></span>
    * <span data-ttu-id="d0c4f-162">Saate määrata lisafiltreid ka edastatuks märgitavatele ühendusesisese kaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-162">You can also specify additional filters on intra-community trade transactions to mark as Reported.</span></span>  
7. <span data-ttu-id="d0c4f-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-163">Click OK.</span></span>
8. <span data-ttu-id="d0c4f-164">Valige väljal Valik väärtus Esitatud.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-164">In the Selection field, select 'Reported'.</span></span>

## <a name="mark-eu-sales-list-lines-as-closed"></a><span data-ttu-id="d0c4f-165">ELi käibearuande ridade suletuks märkimine</span><span class="sxs-lookup"><span data-stu-id="d0c4f-165">Mark EU sales list lines as Closed</span></span>
1. <span data-ttu-id="d0c4f-166">Klõpsake käsku Märgi.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-166">Click Mark.</span></span>
2. <span data-ttu-id="d0c4f-167">Klõpsake käsku Märgi suletuks.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-167">Click Mark as closed.</span></span>
3. <span data-ttu-id="d0c4f-168">Märkige loendis välja Arve kuupäev rida.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-168">In the list, mark the row for the Invoice date field.</span></span>
4. <span data-ttu-id="d0c4f-169">Tippige väljale Kriteerium väärtus 01/01/2016..01/31/2016.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-169">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="d0c4f-170">Märkige loendis välja Aruandluse olek rida.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-170">In the list, mark the row for the Reporting status field.</span></span>
6. <span data-ttu-id="d0c4f-171">Valige väljal Kriteeriumid väärtus Esitatud.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-171">In the Criteria field, select ‘Reported’.</span></span>
    * <span data-ttu-id="d0c4f-172">Saate määrata lisafiltreid ka suletuks märgitavatele ühendusesisese kaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-172">You can also specify additional filters on intra-community trade transactions to mark as Closed.</span></span>  
7. <span data-ttu-id="d0c4f-173">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-173">Click OK.</span></span>
8. <span data-ttu-id="d0c4f-174">Valige väljal Valik väärtus Suletud.</span><span class="sxs-lookup"><span data-stu-id="d0c4f-174">In the Selection field, select 'Closed'.</span></span>
