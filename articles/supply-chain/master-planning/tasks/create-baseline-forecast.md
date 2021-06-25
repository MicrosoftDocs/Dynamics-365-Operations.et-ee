---
title: 'Juhend: baasprognoosi koostamine'
description: Tootmise planeerija saab luua alusprognoosi, kasutades kas ajaseeria prognoosimudeleid või kopeerides ajaloolise nõudluse.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 95a20b30827c9096dd8d8f67d149305cf594ff05
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6223958"
---
# <a name="guide-create-a-baseline-forecast"></a><span data-ttu-id="2c0f6-103">Juhend: baasprognoosi koostamine</span><span class="sxs-lookup"><span data-stu-id="2c0f6-103">Guide: Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c0f6-104">Tootmise planeerija saab luua alusprognoosi, kasutades kas ajaseeria prognoosimudeleid või kopeerides ajaloolise nõudluse.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="2c0f6-105">See protseduur näitab, kuidas kopeerida ajaloolist nõudlust, et luua alusprognoos kõigi toodete puhul, mis kasutavad ühte kauba eraldamisvõtit.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span>

## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="2c0f6-106">Kauba eraldamisvõtme seadistamine</span><span class="sxs-lookup"><span data-stu-id="2c0f6-106">Set up an item allocation key</span></span>

1. <span data-ttu-id="2c0f6-107">Avage **Koondplaneerimine > Seadistus > Kontsernisisesed plaanimisgrupid**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-107">Go to **Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="2c0f6-108">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2c0f6-109">Näiteks saate filtrida välja *Nimi* väärtuse *10* järgi.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-109">For example, filter on the *Name* field with a value of *10*.</span></span>
    * <span data-ttu-id="2c0f6-110">Nõudluse prognoos töötab juriidiliste isikute vahel.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="2c0f6-111">Seetõttu peate seadistama kõik ettevõtted, mille puhul soovite ühes kontsernisiseses plaanimisgrupis prognoose luua.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="2c0f6-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="2c0f6-113">Klõpsake suvandit **Kauba eraldamisvõtmed**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-113">Select **Item allocation keys**.</span></span>
    * <span data-ttu-id="2c0f6-114">Valige kõik kauba eraldamisvõtmed, mille puhul soovite prognoose luua.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="2c0f6-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2c0f6-116">Valige kauba eraldamisvõti D_Aloc.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="2c0f6-117">Valige **>**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-117">Select **>**.</span></span>
7. <span data-ttu-id="2c0f6-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-118">Close the page.</span></span>
8. <span data-ttu-id="2c0f6-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="2c0f6-120">Nõudluse prognoosiparameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="2c0f6-120">Set up the demand forecasting parameters</span></span>

1. <span data-ttu-id="2c0f6-121">Avage **Koondplaneerimine > Seadistus > Nõudluse prognoos > Nõudluse prognoosiparameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-121">Go to **Master planning > Setup > Demand forecasting > Demand forecasting parameters**.</span></span>
2. <span data-ttu-id="2c0f6-122">Laiendage jaotist **Prognoosi algoritmi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-122">Expand the **Forecast algorithm parameters** section.</span></span>
3. <span data-ttu-id="2c0f6-123">Valige väljal **Prognoosi koostamise strateegia** suvand **Kopeeri ajalooline nõudlus ümber**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-123">In the **Forecast generation strategy** field, select **Copy over historical demand**.</span></span>
4. <span data-ttu-id="2c0f6-124">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-124">Select **Save**.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="2c0f6-125">Alusprognoosi loomine</span><span class="sxs-lookup"><span data-stu-id="2c0f6-125">Create a baseline forecast</span></span>

1. <span data-ttu-id="2c0f6-126">Avage **Koondplaneerimine > Prognoosimine > Nõudluse prognoos > Statistilise alusprognoosi loomine**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-126">Go to **Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast**.</span></span>
2. <span data-ttu-id="2c0f6-127">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-127">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="2c0f6-128">Kui teil on müügitellimusi alates 1. jaanuarist 2015, sisestage see kuupäev.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="2c0f6-129">Kui pole, sisestage müügitellimuste varaseim kuupäev.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="2c0f6-130">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-130">In the **To date** field, enter a date.</span></span>
    * <span data-ttu-id="2c0f6-131">Sisestage müügitellimuste viimane kuupäev, näiteks *31.03.2015*.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-131">Enter the last date of your sales orders, for example *2015-03-31*.</span></span>  
4. <span data-ttu-id="2c0f6-132">Sisestage kuupäev väljale **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-132">In the **From date** field, enter a date.</span></span>
    * <span data-ttu-id="2c0f6-133">Sisestage *01.04.2015*.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-133">Enter *2015-04-01*.</span></span> <span data-ttu-id="2c0f6-134">See kuupäev arvutatakse automaatselt järgmise prognoosi vahemiku alguskuupäevana.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="2c0f6-135">Jaotise kaasamiseks laiendage valikut **Kirjed**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-135">Expand the **Records to include** section.</span></span>
6. <span data-ttu-id="2c0f6-136">Valige **Filter**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-136">Select **Filter**.</span></span>
7. <span data-ttu-id="2c0f6-137">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="2c0f6-138">Märkige rida, kus **Väli** = *Kontsernisisene plaanimisgrupp*.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-138">Mark the row where **Field** = *Intercompany planning group*.</span></span>  
8. <span data-ttu-id="2c0f6-139">Sisestage väärtus väljale **Kriteerium**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-139">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="2c0f6-140">Sisestage kontsernisisene plaanimisgrupp (nt *10*), mida kasutasite esimeses ülesandes.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-140">Type the intercompany planning group (for example, *10*) that you used in the first task.</span></span>  
9. <span data-ttu-id="2c0f6-141">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="2c0f6-142">Valige rida, kus **Väli** = *Kauba eraldamisvõti*.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-142">Select the row where **Field** = *Item allocation key*.</span></span>  
10. <span data-ttu-id="2c0f6-143">Sisestage väärtus väljale **Kriteerium**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-143">In the **Criteria** field, type a value.</span></span>
11. <span data-ttu-id="2c0f6-144">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-144">Select **OK**.</span></span>
12. <span data-ttu-id="2c0f6-145">Laiendage jaotist **Täpsemad parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-145">Expand the **Advanced parameters** section.</span></span>
13. <span data-ttu-id="2c0f6-146">Valige väljal **Prognoosi vahemik** suvand *Kuu*.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-146">In the **Forecast bucket** field, select *Month*.</span></span>
14. <span data-ttu-id="2c0f6-147">Sisestage väljale **Prognoosi periood** väärtus *3*.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-147">In the **Forecast horizon** field, enter *3*.</span></span>
15. <span data-ttu-id="2c0f6-148">Sisestage väljale **Ajapiiri külmutamine** väärtus *1*.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-148">In the **Freeze time fence** field, enter *1*.</span></span>
16. <span data-ttu-id="2c0f6-149">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-149">Select **OK**.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="2c0f6-150">Nõudluse prognoosi visualiseerimine</span><span class="sxs-lookup"><span data-stu-id="2c0f6-150">Visualize the demand forecast</span></span>

1. <span data-ttu-id="2c0f6-151">Avage **Koondplaneerimine > Prognoosimine > Nõudluse prognoos > Korrigeeritud nõudluse prognoos**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-151">Go to **Master planning > Forecasting > Demand forecasting > Adjusted demand forecast**.</span></span>
2. <span data-ttu-id="2c0f6-152">Valige koondtabelis lahter reas 1 ja veerus 2.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="2c0f6-153">See on teine kuu, mille jaoks olete prognoosi loonud.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="2c0f6-154">Määrake lahtri **QtyCell** väärtuseks *400*.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-154">Set **QtyCell** to *400*.</span></span>
    * <span data-ttu-id="2c0f6-155">Sisestage lahtrisse prognoositust teistsugune number, nt 400.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="2c0f6-156">Olete prognoosi käsitsi korrigeerinud.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="2c0f6-157">Pöörake tähelepanu järgmises etapis olevale graafilisele näidikule.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="2c0f6-158">Klõpsake suvandit **Prognoosi rea andmed**.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-158">Select **Forecast line details**.</span></span>
    * <span data-ttu-id="2c0f6-159">Sellel lehel näete täpsuse väärtusi, ajaloolist nõudlust ja prognoosi.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="2c0f6-160">Saate ka prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="2c0f6-160">You can make changes to the forecast as well.</span></span>  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]