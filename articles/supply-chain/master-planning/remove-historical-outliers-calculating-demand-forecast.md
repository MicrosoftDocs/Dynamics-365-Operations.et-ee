---
title: "Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost"
description: "Selles artiklis kirjeldatakse, kuidas välistada võõrväärtusi ajaloolistest andmetest, mida kasutatakse nõudluse prognoosi arvutamiseks. Võõrväärtuste välistamisega saate parandada prognoosi täpsust."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3313299876ee8c3e540c7d5ca5cbd160a94784c3
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="41fbd-104">Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost</span><span class="sxs-lookup"><span data-stu-id="41fbd-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="41fbd-105">Selles artiklis kirjeldatakse, kuidas välistada võõrväärtusi ajaloolistest andmetest, mida kasutatakse nõudluse prognoosi arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="41fbd-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="41fbd-106">Võõrväärtuste välistamisega saate parandada prognoosi täpsust.</span><span class="sxs-lookup"><span data-stu-id="41fbd-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="41fbd-107">Prognoosi täpsuse suurendamiseks saab võõrväärtused välistada.</span><span class="sxs-lookup"><span data-stu-id="41fbd-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="41fbd-108">See on valikuline ülesanne.</span><span class="sxs-lookup"><span data-stu-id="41fbd-108">This is an optional task.</span></span> <span data-ttu-id="41fbd-109">Siin on protsessi ülevaade.</span><span class="sxs-lookup"><span data-stu-id="41fbd-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="41fbd-110">Klõpsake valikuid **Koondplaneerimine** &gt; **Seadistus** &gt; **Nõudluse prognoosimine** &gt; **Võõrväärtuse eemaldamine** lehe **Võõrväärtuse eemaldamine** avamiseks, kus saate välistatavate kannete valimiseks päringut kasutada.</span><span class="sxs-lookup"><span data-stu-id="41fbd-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="41fbd-111">Valige ettevõte, millele päring kehtib, ja sisestage seejärel nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="41fbd-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="41fbd-112">Väljale **Päringu kuupäev** lisatakse automaatselt praegune kuupäev.</span><span class="sxs-lookup"><span data-stu-id="41fbd-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="41fbd-113">Märkige ruut **Aktiivne** päringu kaudu leitud kannete välistamiseks ajaloolistest andmetest.</span><span class="sxs-lookup"><span data-stu-id="41fbd-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="41fbd-114">See säte jõustub alusprognoosi loomisel.</span><span class="sxs-lookup"><span data-stu-id="41fbd-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="41fbd-115">Lehel **Võõrväärtuse eemaldamise päring** saate lisada, eemaldada ja valida kriteeriume, mis määravad, millised kanded välistatakse alusprognoosi arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="41fbd-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="41fbd-116">Valige näiteks kindel kaup või tellimuse kanne, mida välistada.</span><span class="sxs-lookup"><span data-stu-id="41fbd-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="41fbd-117">Klõpsake valikut **Kuva kanded**.</span><span class="sxs-lookup"><span data-stu-id="41fbd-117">Click **Display transactions**.</span></span> <span data-ttu-id="41fbd-118">Lehel **Võõrväärtuse kanded** on esitatud kanded, mis täidavad päringus määratud kriteeriume ja mis välistatakse nõudluse prognoosi arvutamisel ajaloolistest andmetest.</span><span class="sxs-lookup"><span data-stu-id="41fbd-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="41fbd-119">**Märkus:** saate luua ka päringu, mis põhineb olemasoleval päringul.</span><span class="sxs-lookup"><span data-stu-id="41fbd-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="41fbd-120">Valige kopeeritav päring ja klõpsake siis käsku **Dubleeri**.</span><span class="sxs-lookup"><span data-stu-id="41fbd-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="41fbd-121">Väli **Päringu kuupäev** tuvastab versiooni.</span><span class="sxs-lookup"><span data-stu-id="41fbd-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="41fbd-122">Võite kasutada päringut olemasoleval kujul või klõpsata kriteeriumide muutmiseks käsku **Redigeeri päringut**.</span><span class="sxs-lookup"><span data-stu-id="41fbd-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="41fbd-123">Soovi korral saate muuta uue päringu nime ja kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="41fbd-123">You can optionally modify the name and description of the new query.</span></span>

<a name="see-also"></a><span data-ttu-id="41fbd-124">Vt ka</span><span class="sxs-lookup"><span data-stu-id="41fbd-124">See also</span></span>
--------

[<span data-ttu-id="41fbd-125">Sissejuhatus nõudluse prognoosimisse</span><span class="sxs-lookup"><span data-stu-id="41fbd-125">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="41fbd-126">Prognoosi täpsuse jälgimine</span><span class="sxs-lookup"><span data-stu-id="41fbd-126">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)




