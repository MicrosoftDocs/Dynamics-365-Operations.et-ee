---
title: Alusprognoosi loomine
description: Tootmise planeerija saab luua alusprognoosi, kasutades kas ajaseeria prognoosimudeleid või kopeerides ajaloolise nõudluse.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a1d8fd665ec40efede0a3db8b0c59ac89751a64
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987186"
---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="da2bf-103">Alusprognoosi loomine</span><span class="sxs-lookup"><span data-stu-id="da2bf-103">Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da2bf-104">Tootmise planeerija saab luua alusprognoosi, kasutades kas ajaseeria prognoosimudeleid või kopeerides ajaloolise nõudluse.</span><span class="sxs-lookup"><span data-stu-id="da2bf-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="da2bf-105">See protseduur näitab, kuidas kopeerida ajaloolist nõudlust, et luua alusprognoos kõigi toodete puhul, mis kasutavad ühte kauba eraldamisvõtit.</span><span class="sxs-lookup"><span data-stu-id="da2bf-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="da2bf-106">Kauba eraldamisvõtme seadistamine</span><span class="sxs-lookup"><span data-stu-id="da2bf-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="da2bf-107">Avage Koondplaneerimine > Seadistus > Kontsernisisesed plaanimisgrupid.</span><span class="sxs-lookup"><span data-stu-id="da2bf-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="da2bf-108">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="da2bf-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="da2bf-109">Näiteks saate filtrida välja Nimi väärtuse 10 järgi.</span><span class="sxs-lookup"><span data-stu-id="da2bf-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="da2bf-110">Nõudluse prognoos töötab juriidiliste isikute vahel.</span><span class="sxs-lookup"><span data-stu-id="da2bf-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="da2bf-111">Seetõttu peate seadistama kõik ettevõtted, mille puhul soovite ühes kontsernisiseses plaanimisgrupis prognoose luua.</span><span class="sxs-lookup"><span data-stu-id="da2bf-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="da2bf-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="da2bf-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="da2bf-113">Klõpsake suvandit Kauba eraldamisvõtmed.</span><span class="sxs-lookup"><span data-stu-id="da2bf-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="da2bf-114">Valige kõik kauba eraldamisvõtmed, mille puhul soovite prognoose luua.</span><span class="sxs-lookup"><span data-stu-id="da2bf-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="da2bf-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="da2bf-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="da2bf-116">Valige kauba eraldamisvõti D_Aloc.</span><span class="sxs-lookup"><span data-stu-id="da2bf-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="da2bf-117">Klõpsake >.</span><span class="sxs-lookup"><span data-stu-id="da2bf-117">Click >.</span></span>
7. <span data-ttu-id="da2bf-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da2bf-118">Close the page.</span></span>
8. <span data-ttu-id="da2bf-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da2bf-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-paramters"></a><span data-ttu-id="da2bf-120">Nõudluse prognoosimise parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="da2bf-120">Set up the demand forecasting paramters</span></span>
1. <span data-ttu-id="da2bf-121">Avage Koondplaneerimine > Seadistus > Nõudluse prognoos > Nõudluse prognoosiparameetrid.</span><span class="sxs-lookup"><span data-stu-id="da2bf-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="da2bf-122">Laiendage jaotist Prognoosi algoritmi parameetrid.</span><span class="sxs-lookup"><span data-stu-id="da2bf-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="da2bf-123">Valige väljal Prognoosi koostamise strateegia suvand Kopeeri ajalooline nõudlus ümber.</span><span class="sxs-lookup"><span data-stu-id="da2bf-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="da2bf-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="da2bf-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="da2bf-125">Alusprognoosi loomine</span><span class="sxs-lookup"><span data-stu-id="da2bf-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="da2bf-126">Avage Koondplaneerimine > Prognoosimine > Nõudluse prognoos > Statistilise alusprognoosi loomine.</span><span class="sxs-lookup"><span data-stu-id="da2bf-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="da2bf-127">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="da2bf-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="da2bf-128">Kui teil on müügitellimusi alates 1. jaanuarist 2015, sisestage see kuupäev.</span><span class="sxs-lookup"><span data-stu-id="da2bf-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="da2bf-129">Kui pole, sisestage müügitellimuste varaseim kuupäev.</span><span class="sxs-lookup"><span data-stu-id="da2bf-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="da2bf-130">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="da2bf-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="da2bf-131">Sisestage müügitellimuste viimane kuupäev, näiteks 31.03.2015.</span><span class="sxs-lookup"><span data-stu-id="da2bf-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="da2bf-132">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="da2bf-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="da2bf-133">Sisestage 01.04.2015.</span><span class="sxs-lookup"><span data-stu-id="da2bf-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="da2bf-134">See kuupäev arvutatakse automaatselt järgmise prognoosi vahemiku alguskuupäevana.</span><span class="sxs-lookup"><span data-stu-id="da2bf-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="da2bf-135">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="da2bf-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="da2bf-136">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="da2bf-136">Click Filter.</span></span>
7. <span data-ttu-id="da2bf-137">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="da2bf-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="da2bf-138">Märkige rida, kus väli = Kontsernisisene plaanimisgrupp.</span><span class="sxs-lookup"><span data-stu-id="da2bf-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="da2bf-139">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="da2bf-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="da2bf-140">Sisestage kontsernisisene plaanimisgrupp, nt 10, mida kasutasite esimeses ülesandes.</span><span class="sxs-lookup"><span data-stu-id="da2bf-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="da2bf-141">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="da2bf-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="da2bf-142">Valige rida, kus väli = Kauba eraldamisvõti.</span><span class="sxs-lookup"><span data-stu-id="da2bf-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="da2bf-143">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="da2bf-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="da2bf-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da2bf-144">Click OK.</span></span>
12. <span data-ttu-id="da2bf-145">Laiendage jaotist Täpsemad parameetrid.</span><span class="sxs-lookup"><span data-stu-id="da2bf-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="da2bf-146">Valige väljal Prognoosi vahemik suvand Kuu.</span><span class="sxs-lookup"><span data-stu-id="da2bf-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="da2bf-147">Sisestage väljale Prognoosi periood väärtus 3.</span><span class="sxs-lookup"><span data-stu-id="da2bf-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="da2bf-148">Sisestage väljale Ajapiiri külmutamine väärtus 1.</span><span class="sxs-lookup"><span data-stu-id="da2bf-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="da2bf-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da2bf-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="da2bf-150">Nõudluse prognoosi visualiseerimine</span><span class="sxs-lookup"><span data-stu-id="da2bf-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="da2bf-151">Avage Koondplaneerimine > Prognoosimine > Nõudluse prognoos > Korrigeeritud nõudluse prognoos.</span><span class="sxs-lookup"><span data-stu-id="da2bf-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="da2bf-152">Valige koondtabelis lahter reas 1 ja veerus 2.</span><span class="sxs-lookup"><span data-stu-id="da2bf-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="da2bf-153">See on teine kuu, mille jaoks olete prognoosi loonud.</span><span class="sxs-lookup"><span data-stu-id="da2bf-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="da2bf-154">Määrake lahtri QtyCell väärtuseks 400.</span><span class="sxs-lookup"><span data-stu-id="da2bf-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="da2bf-155">Sisestage lahtrisse prognoositust teistsugune number, nt 400.</span><span class="sxs-lookup"><span data-stu-id="da2bf-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="da2bf-156">Olete prognoosi käsitsi korrigeerinud.</span><span class="sxs-lookup"><span data-stu-id="da2bf-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="da2bf-157">Pöörake tähelepanu järgmises etapis olevale graafilisele näidikule.</span><span class="sxs-lookup"><span data-stu-id="da2bf-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="da2bf-158">Klõpsake suvandit Prognoosi rea andmed.</span><span class="sxs-lookup"><span data-stu-id="da2bf-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="da2bf-159">Sellel lehel näete täpsuse väärtusi, ajaloolist nõudlust ja prognoosi.</span><span class="sxs-lookup"><span data-stu-id="da2bf-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="da2bf-160">Saate ka prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="da2bf-160">You can make changes to the forecast as well.</span></span>  

