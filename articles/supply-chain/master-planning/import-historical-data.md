---
title: Nõudluse prognooside kohta varasemate andmete importimine
description: Täpsete nõudluse prognooside saamiseks on vaja varasemaid nõudluse andmeid kauba või kauba eraldamisvõtme kohta. Selles teemas selgitatakse, kuidas kasutada andmeüksusi varasemate nõudluse andmete importimiseks mis tahes süsteemist, et nõudluse prognoosi andmed oleksid olemas pikema perioodi kohta.
author: roxanadiaconu
manager: tfehr
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97e84b478b8fd65313d8c3be5c9a50756d8b4924
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213834"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="fe1c1-104">Nõudluse prognooside kohta varasemate andmete importimine</span><span class="sxs-lookup"><span data-stu-id="fe1c1-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe1c1-105">Nõudluse prognooside täpsuse tagamiseks peab varasemaid nõudluse andmeid olema kauba või kauba eraldamisvõtme kohta võimalikult palju.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="fe1c1-106">Kui varasemaid nõudluse andmeid pole veel imporditud, siis kasutage nende importimiseks andmeüksust **Varasem väline nõudlus** (ReqDemPlanHistoricalExternalDemandEntity) rakenduses Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="fe1c1-107">Tööruumis **Andmehaldus** näete ülevaadet kõigist üksuse väljadest.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="fe1c1-108">Avage tööruum **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="fe1c1-109">Klõpsake paani **Andmeüksused**.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="fe1c1-110">Otsige valiku **Varasem väline nõudlus** üksuste loendit.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="fe1c1-111">Klõpsake valikut **Sihtväljad**.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-111">Click **Target fields**.</span></span> <span data-ttu-id="fe1c1-112">Järgmised üksuste väljad on kohustuslikud: laoala (**DeliveringSiteId**), kuupäev (**DemandDate**), kogus (**DemandQuantity**) ja kas kaubakood (**ItemNumber**) või kauba eraldamisvõti (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="fe1c1-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="fe1c1-113">Andmeüksuse kasutamiseks peab teil olema Microsoft Exceli fail või komaeraldusega (CSV) fail, mis sisaldab varasema nõudluse andmeid.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="fe1c1-114">Järgmine näide selgitab andmete importimist CSV-failist.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="fe1c1-115">Näide</span><span class="sxs-lookup"><span data-stu-id="fe1c1-115">Example</span></span>

<span data-ttu-id="fe1c1-116">Näitena saab kasutada järgmist faili.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-116">You can use the following file as an example.</span></span> <span data-ttu-id="fe1c1-117">Laadige alla [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="fe1c1-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="fe1c1-118">See fail sisaldab kauba D0001 varasema nõudluse andmeid.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="fe1c1-119">See sisaldab järgmisi kohustuslikke välju: laoala, kogus ja nõudluse kuupäev.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="fe1c1-120">Valige ettevõtte, mille alla varasema nõudluse andmed importida.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="fe1c1-121">Avage tööruum **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="fe1c1-122">Klõpsake paani **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="fe1c1-123">Sisestage impordiprojekti nimi, nt **Kauba D0001 varasema nõudluse importimine**.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="fe1c1-124">Valige väljalt **Lähteandmete vorming** imporditava faili vorming.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="fe1c1-125">Selles näites valige faili HistoricalDemandData importimiseks **CSV**.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="fe1c1-126">Tehke väljal **Üksuse nimi** valik **Varasem väline nõudlus**.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="fe1c1-127">Salvestage fail arvutisse ja laadige see siis üles.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="fe1c1-128">Klõpsake nuppu **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-128">Click **Import**.</span></span>
9. <span data-ttu-id="fe1c1-129">Leht **Täitmise kokkuvõte** avaneb automaatselt.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="fe1c1-130">Kontrollige lehelt imporditud andmeid.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="fe1c1-131">Pärast ajalooliste andmete importimist saate nõudluse prognoosi koostada.</span><span class="sxs-lookup"><span data-stu-id="fe1c1-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fe1c1-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fe1c1-132">Additional resources</span></span>

[<span data-ttu-id="fe1c1-133">Statistilise alusprognoosi loomine</span><span class="sxs-lookup"><span data-stu-id="fe1c1-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)
