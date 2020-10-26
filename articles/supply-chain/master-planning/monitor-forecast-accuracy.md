---
title: Prognoosi täpsuse jälgimine
description: Selles teemas kirjeldatakse, millist tüüpi prognoosi täpsust Dynamics 365 Supply Chain Management arvutab, ning selgitatakse, kuidas täpsuse väärtusi vaadata.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60e5425e54f9e0093888f355a51064e7f0057976
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976060"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="a949f-103">Prognoosi täpsuse jälgimine</span><span class="sxs-lookup"><span data-stu-id="a949f-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a949f-104">Selles teemas kirjeldatakse, millist tüüpi prognoosi täpsust Microsoft Dynamics 365 Supply Chain Management arvutab, ning selgitatakse, kuidas täpsuse väärtusi vaadata.</span><span class="sxs-lookup"><span data-stu-id="a949f-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="a949f-105">Supply Chain Management arvutab järgmised prognoosi täpsuse tüübid.</span><span class="sxs-lookup"><span data-stu-id="a949f-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="a949f-106">Ajalooline prognoosi täpsus, kus võrreldakse koondplaneerimises kasutatavat prognoosi ajaloolise nõudlusega.</span><span class="sxs-lookup"><span data-stu-id="a949f-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="a949f-107">Ajaloolise prognoosi täpsuse väärtuste (nii absoluutsete väärtuste kui ka väärtuste protsendi) vaatamiseks klõpsake lehel **Nõudluse prognoosi üksikasjad** nuppu **Kuva täpsus**.</span><span class="sxs-lookup"><span data-stu-id="a949f-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="a949f-108">Prognooside loomisel kasutatud prognoosimudeli eeldatav täpsus.</span><span class="sxs-lookup"><span data-stu-id="a949f-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="a949f-109">Saate vaadata täpsusprotsenti lehe **Nõudluse prognoosi üksikasjad** jaotisest **Mudeli üksikasjad – MAPE**.</span><span class="sxs-lookup"><span data-stu-id="a949f-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="a949f-110">Kui kasutate nõudluse prognoosimise Microsoft Azure’i masinõpet, põhineb sisemise mudeli täpsuse arvutus katseandmete kogumil.</span><span class="sxs-lookup"><span data-stu-id="a949f-110">If you use the Demand forecasting Microsoft Azure Machine Learning, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="a949f-111">Testandmete kogumi suuruse määramiseks seadke lehel **Nõudluse prognoosimise parameetrid** parameeter **TEST\_SET\_SIZE\_PERCENT**.</span><span class="sxs-lookup"><span data-stu-id="a949f-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="a949f-112">Näiteks kui seate väärtuseks **20**, kasutatakse sisemise mudeli täpsuse arvutamiseks viimast 20% ajaloolistest andmetest.</span><span class="sxs-lookup"><span data-stu-id="a949f-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="a949f-113">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a949f-113">Additional resources</span></span>
--------

[<span data-ttu-id="a949f-114">Korrigeeritud prognoosi autoriseerimine</span><span class="sxs-lookup"><span data-stu-id="a949f-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="a949f-115">Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost</span><span class="sxs-lookup"><span data-stu-id="a949f-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



