---
title: "Prognoosi täpsuse jälgimine"
description: "Selles artiklis kirjeldatakse, millist tüüpi prognoosi täpsust Microsoft Dynamics 365 for Finance and Operations arvutab ning selgitatakse, kuidas täpsuse väärtusi vaadata."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d7070c15f9ee23cfdba871af68d1fc5954735651
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="b4b45-103">Prognoosi täpsuse jälgimine</span><span class="sxs-lookup"><span data-stu-id="b4b45-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4b45-104">Selles artiklis kirjeldatakse, millist tüüpi prognoosi täpsust Microsoft Dynamics 365 for Finance and Operations arvutab ning selgitatakse, kuidas täpsuse väärtusi vaadata.</span><span class="sxs-lookup"><span data-stu-id="b4b45-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="b4b45-105">Finance and Operations arvutab järgmised prognoosi täpsuse tüübid.</span><span class="sxs-lookup"><span data-stu-id="b4b45-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="b4b45-106">Ajalooline prognoosi täpsus, kus võrreldakse koondplaneerimises kasutatavat prognoosi ajaloolise nõudlusega.</span><span class="sxs-lookup"><span data-stu-id="b4b45-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="b4b45-107">Ajaloolise prognoosi täpsuse väärtuste (nii absoluutsete väärtuste kui ka väärtuste protsendi) vaatamiseks klõpsake lehel **Nõudluse prognoosi üksikasjad** nuppu **Kuva täpsus**.</span><span class="sxs-lookup"><span data-stu-id="b4b45-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="b4b45-108">Prognooside loomisel kasutatud prognoosimudeli eeldatav täpsus.</span><span class="sxs-lookup"><span data-stu-id="b4b45-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="b4b45-109">Saate vaadata täpsusprotsenti lehe **Nõudluse prognoosi üksikasjad** jaotisest **Mudeli üksikasjad – MAPE**.</span><span class="sxs-lookup"><span data-stu-id="b4b45-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="b4b45-110">**Märkus.** Kui kasutate Finance and Operationsi nõudluse prognoosimise Microsoft Azure’i masinõppe teenust, põhineb sisemise mudeli täpsuse arvutus testandmete kogumil.</span><span class="sxs-lookup"><span data-stu-id="b4b45-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="b4b45-111">Testandmete kogumi suuruse määramiseks seadke lehel **Nõudluse prognoosimise parameetrid** parameeter **TEST\_SET\_SIZE\_PERCENT**.</span><span class="sxs-lookup"><span data-stu-id="b4b45-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="b4b45-112">Näiteks kui seate väärtuseks **20**, kasutatakse sisemise mudeli täpsuse arvutamiseks viimast 20% ajaloolistest andmetest.</span><span class="sxs-lookup"><span data-stu-id="b4b45-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="b4b45-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b4b45-113">Additional resources</span></span>
--------

[<span data-ttu-id="b4b45-114">Korrigeeritud prognoosi autoriseerimine</span><span class="sxs-lookup"><span data-stu-id="b4b45-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="b4b45-115">Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost</span><span class="sxs-lookup"><span data-stu-id="b4b45-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




