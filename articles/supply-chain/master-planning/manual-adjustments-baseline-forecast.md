---
title: "Alusprognoosis käsitsi korrigeerimiste tegemine"
description: "Selles teemas selgitatakse, kuidas alusprognoosi käsitsi korrigeerida ning prognoosi üksikasju kuvada."
author: roxanadiaconu
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: a7c7d1fcaaeef7a01b43886e4d69458dbd942439
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="4d553-103">Alusprognoosis käsitsi korrigeerimiste tegemine</span><span class="sxs-lookup"><span data-stu-id="4d553-103">Make manual adjustments to the baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d553-104">Selles teemas selgitatakse, kuidas alusprognoosi käsitsi korrigeerida ning prognoosi üksikasju kuvada.</span><span class="sxs-lookup"><span data-stu-id="4d553-104">This topic explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="4d553-105">Enne käsitsi korrigeerimiste tegemist on oluline mõista mõnda põhimõtet erinevatel lehekülgedel.</span><span class="sxs-lookup"><span data-stu-id="4d553-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="4d553-106">Korrigeeritud nõudluse prognoosi lehe ruudustik</span><span class="sxs-lookup"><span data-stu-id="4d553-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="4d553-107">Lehe **Korrigeeritud nõudluse prognoos** ruudustikul on järgmine struktuur.</span><span class="sxs-lookup"><span data-stu-id="4d553-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="4d553-108">Esimeses veerus kuvatakse kaubad, kauba eraldamisvõtmed, ettevõtted jms, mille jaoks prognoos loodi.</span><span class="sxs-lookup"><span data-stu-id="4d553-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="4d553-109">Lehe alapealkiri kirjeldab ruudustikus kuvatatud praegusi prognoosi dimensioone.</span><span class="sxs-lookup"><span data-stu-id="4d553-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="4d553-110">Näiteks kui lehe alapealkiri on **Ettevõte / Koht / Kauba eraldamisvõti** ja üks ruudustiku reapäiseid on **USMF / 1 / D\_Alloc**, näitab see rida, et tegemist on USMF-i ettevõtte, koha 1 ja **D\_Alloc** kauba eraldamisvõtme prognoosiga.</span><span class="sxs-lookup"><span data-stu-id="4d553-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="4d553-111">Järgnevad veerud esindavad prognoosivahemikke, mille jaoks prognoos on loodud.</span><span class="sxs-lookup"><span data-stu-id="4d553-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="4d553-112">Iga veeru päis on veerus kuvatava prognoosivahemiku alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="4d553-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="4d553-113">Lahtrite väärtused esitavad ühe kauba, kauba eraldamisvõtme jm kindla prognoosivahemiku prognoosi.</span><span class="sxs-lookup"><span data-stu-id="4d553-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-de-aggregation"></a><span data-ttu-id="4d553-114">Prognoosi koondamine ja jaotamine</span><span class="sxs-lookup"><span data-stu-id="4d553-114">Forecast aggregation and de-aggregation</span></span>
<span data-ttu-id="4d553-115">Lehe alapealkiri näitab prognoosi koondamise taset.</span><span class="sxs-lookup"><span data-stu-id="4d553-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="4d553-116">Näiteks, kui lehe alapealkiri on **Ettevõte / Koht / Eraldamisvõti / Kaubakood / Värv / Suurus / Konfiguratsioon / Stiil**, ei ole prognoosi koondatud ning seda kuvatakse kauba ja selle dimensioonide tasemel.</span><span class="sxs-lookup"><span data-stu-id="4d553-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="4d553-117">Koondamise muutmiseks kasutage lehekülge **Prognoosi dimensioonide muutmine**, mille saate avada rakenduse menüüst.</span><span class="sxs-lookup"><span data-stu-id="4d553-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="4d553-118">Prognoosi muutmiseks klõpsake mistahes saadaoleval lahtril ja sisestage sinna korrigeeritud prognoosi väärtus.</span><span class="sxs-lookup"><span data-stu-id="4d553-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="4d553-119">Redigeeritud lahtri sisu pannakse paksu kirja, et näidata, et selles kuvatav prognoos ei ole nõudluse prognoosimise teenuse loodud prognoos, vaid seda on käsitsi korrigeeritud.</span><span class="sxs-lookup"><span data-stu-id="4d553-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="4d553-120">Kui muudate koondamist selliselt, et lehel rohkem koondatud andmeid kuvada, saate leheküljelt **Nõudluse prognoosi read** koondatud prognoosi üksikuid prognoosi ridu vaadata.</span><span class="sxs-lookup"><span data-stu-id="4d553-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="4d553-121">Näiteks lõite prognoosi kauba tasemel, kuid teate, et selle kauba nõudlus suureneb kampaania või muu taolise sündmuse tõttu kõigis kohtades.</span><span class="sxs-lookup"><span data-stu-id="4d553-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="4d553-122">Sel juhul saate koondamise seada **Ettevõte / Kauba eraldamisvõti / Kaup** leheküljel **Prognoosi dimensioonide muutmine**.</span><span class="sxs-lookup"><span data-stu-id="4d553-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="4d553-123">Kauba globaalselt prognoosi saate korrigeerida kõigis kohtades ruudustikus **Korrigeeritud nõudluse prognoos**.</span><span class="sxs-lookup"><span data-stu-id="4d553-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="4d553-124">Tehtud muudatuste mõju nägemiseks kõigis kohtades avage lehekülg **Nõudluse prognoosi read**.</span><span class="sxs-lookup"><span data-stu-id="4d553-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="4d553-125">Sellel lehel näete kaupa igas kohas eraldi real, korrigeeritud prognoosi kogust ja prognoosi algset kogust.</span><span class="sxs-lookup"><span data-stu-id="4d553-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="4d553-126">Kui prognoositud kogust on korrigeeritud koondamise tasemel, kasutab süsteem kaalutud eraldamist, et jagada muudatus koondatud ridadele.</span><span class="sxs-lookup"><span data-stu-id="4d553-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="4d553-127">Leheküljel **Nõudluse prognoosi read** saate ka käsitsi korrigeerimisi teha, muutes kas väärtust **Üldkogus** või jaotamise ruudustiku lahtreid **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="4d553-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="4d553-128">Prognoosi üksikasjade vaatamine</span><span class="sxs-lookup"><span data-stu-id="4d553-128">Viewing details of the forecast</span></span>
<span data-ttu-id="4d553-129">Prognoosi kohta lisateabe saamiseks avage lehekülg **Nõudluse prognoosi üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="4d553-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="4d553-130">Lehel **Nõudluse prognoosi üksikasjad** kuvatakse graafilises vormingus ja tabelina järgmist teavet:</span><span class="sxs-lookup"><span data-stu-id="4d553-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="4d553-131">prognoosi aluseks olev ajalooline nõudlus;</span><span class="sxs-lookup"><span data-stu-id="4d553-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="4d553-132">praegune prognoos, mida koondplaneerimises kasutatakse;</span><span class="sxs-lookup"><span data-stu-id="4d553-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="4d553-133">käsitsi korrigeeritud uued nõudluse prognoosi väärtused ja summad;</span><span class="sxs-lookup"><span data-stu-id="4d553-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="4d553-134">prognoositud väärtuste usaldusvahemik;</span><span class="sxs-lookup"><span data-stu-id="4d553-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="4d553-135">prognoosi loomiseks kasutatud prognoosimudel.</span><span class="sxs-lookup"><span data-stu-id="4d553-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="4d553-136">Kui vaatate koondatud andmeid, näete loendit kõigist meetoditest, mida koondatud ajaseeriates kasutati;</span><span class="sxs-lookup"><span data-stu-id="4d553-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="4d553-137">mudeli sisemine täpsus (MAPE).</span><span class="sxs-lookup"><span data-stu-id="4d553-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="4d553-138">Prognoosi täpsuse kohta lisateabe saamiseks vt [Prognoosi täpsuse jälgimine](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="4d553-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="4d553-139">**Märkused.**</span><span class="sxs-lookup"><span data-stu-id="4d553-139">**Notes:**</span></span>

-   <span data-ttu-id="4d553-140">Jaotises **Prognoos** kuvatud usaldusvahemik tähistab usaldusvahemiku ülem- ja alampiiri erinevust.</span><span class="sxs-lookup"><span data-stu-id="4d553-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="4d553-141">Ülem- ja alampiiri väärtuste vaatamiseks liikuge üle diagrammi jaotises **Varasem nõudlus ja prognoos graafiliselt**.</span><span class="sxs-lookup"><span data-stu-id="4d553-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="4d553-142">Kui kasutate Finance and Operationsi nõudluse prognoosimise Microsoft Azure’i masinõppe teenust, saate määrata loodava prognoosi usaldusväärsuse taseme protsendi.</span><span class="sxs-lookup"><span data-stu-id="4d553-142">If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="4d553-143">Usaldusvahemik koosneb väärtuste vahemikust, mille järgi on nõudluse prognoosi hea hinnata.</span><span class="sxs-lookup"><span data-stu-id="4d553-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="4d553-144">Usaldusväärsuse tase 95% näitab, et on olemas 5% tõenäosus, et nõudluse prognoos jääb usaldusväärsusintervalli vahemikust välja.</span><span class="sxs-lookup"><span data-stu-id="4d553-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="4d553-145">Leheküljel **Nõudluse prognoosi üksikasjad** saate prognoosis käsitsi korrigeerimis teha, muutes väärtusi reas **Prognoos** jaotises **Prognoos**.</span><span class="sxs-lookup"><span data-stu-id="4d553-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="additional-resources"></a><span data-ttu-id="4d553-146">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4d553-146">Additional resources</span></span>
--------

[<span data-ttu-id="4d553-147">Prognoosi täpsuse jälgimine</span><span class="sxs-lookup"><span data-stu-id="4d553-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="4d553-148">Statistilise alusprognoosi loomine</span><span class="sxs-lookup"><span data-stu-id="4d553-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)




