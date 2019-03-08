---
title: Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost
description: Selles artiklis kirjeldatakse, kuidas välistada võõrväärtusi ajaloolistest andmetest, mida kasutatakse nõudluse prognoosi arvutamiseks. Võõrväärtuste välistamisega saate parandada prognoosi täpsust.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ce8ebaf32b30c57b307f0d8799660ba6b42365a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "323613"
---
# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a><span data-ttu-id="0f804-104">Nõudluse prognoosi arvutamisel võõrväärtuste eemaldamine kandeandmete ajaloost</span><span class="sxs-lookup"><span data-stu-id="0f804-104">Remove outliers from historical transaction data when calculating a demand forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f804-105">Selles artiklis kirjeldatakse, kuidas välistada võõrväärtusi ajaloolistest andmetest, mida kasutatakse nõudluse prognoosi arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="0f804-105">This article describes how to exclude outliers from the historical data that is used to calculate a demand forecast.</span></span> <span data-ttu-id="0f804-106">Võõrväärtuste välistamisega saate parandada prognoosi täpsust.</span><span class="sxs-lookup"><span data-stu-id="0f804-106">By excluding outliers, you can improve forecast accuracy.</span></span>

<span data-ttu-id="0f804-107">Prognoosi täpsuse suurendamiseks saab võõrväärtused välistada.</span><span class="sxs-lookup"><span data-stu-id="0f804-107">You can exclude outliers to improve forecast accuracy.</span></span> <span data-ttu-id="0f804-108">See on valikuline ülesanne.</span><span class="sxs-lookup"><span data-stu-id="0f804-108">This is an optional task.</span></span> <span data-ttu-id="0f804-109">Siin on protsessi ülevaade.</span><span class="sxs-lookup"><span data-stu-id="0f804-109">Here is an overview of the process:</span></span>

1.  <span data-ttu-id="0f804-110">Klõpsake valikuid **Koondplaneerimine** &gt; **Seadistus** &gt; **Nõudluse prognoosimine** &gt; **Võõrväärtuse eemaldamine** lehe **Võõrväärtuse eemaldamine** avamiseks, kus saate välistatavate kannete valimiseks päringut kasutada.</span><span class="sxs-lookup"><span data-stu-id="0f804-110">Click **Master planning** &gt; **Setup** &gt; **Demand forecasting** &gt; **Outlier removal** to open the **Outlier removal** page, where you can use a query to select the transactions to exclude.</span></span>
2.  <span data-ttu-id="0f804-111">Valige ettevõte, millele päring kehtib, ja sisestage seejärel nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="0f804-111">Select the company that the query applies to, and then enter a name and description.</span></span> <span data-ttu-id="0f804-112">Väljale **Päringu kuupäev** lisatakse automaatselt praegune kuupäev.</span><span class="sxs-lookup"><span data-stu-id="0f804-112">The **Query date** field is automatically set to the current date.</span></span>
3.  <span data-ttu-id="0f804-113">Märkige ruut **Aktiivne** päringu kaudu leitud kannete välistamiseks ajaloolistest andmetest.</span><span class="sxs-lookup"><span data-stu-id="0f804-113">Select the **Active** check box to exclude the transactions that the query finds from the historical data.</span></span> <span data-ttu-id="0f804-114">See säte jõustub alusprognoosi loomisel.</span><span class="sxs-lookup"><span data-stu-id="0f804-114">This setting will take effect when you create a baseline forecast.</span></span>
4.  <span data-ttu-id="0f804-115">Lehel **Võõrväärtuse eemaldamise päring** saate lisada, eemaldada ja valida kriteeriume, mis määravad, millised kanded välistatakse alusprognoosi arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="0f804-115">On the **Outlier removal query** page, you can add, remove, and select the criteria that define which transactions will be excluded when the baseline forecast is calculated.</span></span> <span data-ttu-id="0f804-116">Valige näiteks kindel kaup või tellimuse kanne, mida välistada.</span><span class="sxs-lookup"><span data-stu-id="0f804-116">For example, select a specific item or order transaction to exclude.</span></span>
5.  <span data-ttu-id="0f804-117">Klõpsake valikut **Kuva kanded**.</span><span class="sxs-lookup"><span data-stu-id="0f804-117">Click **Display transactions**.</span></span> <span data-ttu-id="0f804-118">Lehel **Võõrväärtuse kanded** on esitatud kanded, mis täidavad päringus määratud kriteeriume ja mis välistatakse nõudluse prognoosi arvutamisel ajaloolistest andmetest.</span><span class="sxs-lookup"><span data-stu-id="0f804-118">The **Outlier transactions** page lists the transactions that meet the criteria that you defined in the query, and that will be excluded from the historical data when the demand forecast is calculated.</span></span>

<span data-ttu-id="0f804-119">**Märkus:** saate luua ka päringu, mis põhineb olemasoleval päringul.</span><span class="sxs-lookup"><span data-stu-id="0f804-119">**Note:** You can also create a query that is based on an existing query.</span></span> <span data-ttu-id="0f804-120">Valige kopeeritav päring ja klõpsake siis käsku **Dubleeri**.</span><span class="sxs-lookup"><span data-stu-id="0f804-120">Select the query to copy, and then click **Duplicate**.</span></span> <span data-ttu-id="0f804-121">Väli **Päringu kuupäev** tuvastab versiooni.</span><span class="sxs-lookup"><span data-stu-id="0f804-121">The **Query date** field identifies the version.</span></span> <span data-ttu-id="0f804-122">Võite kasutada päringut olemasoleval kujul või klõpsata kriteeriumide muutmiseks käsku **Redigeeri päringut**.</span><span class="sxs-lookup"><span data-stu-id="0f804-122">You can use the query as it is, or you can click **Edit query** to modify the criteria.</span></span> <span data-ttu-id="0f804-123">Soovi korral saate muuta uue päringu nime ja kirjeldust.</span><span class="sxs-lookup"><span data-stu-id="0f804-123">You can optionally modify the name and description of the new query.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0f804-124">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0f804-124">Additional resources</span></span>
--------

[<span data-ttu-id="0f804-125">Sissejuhatus nõudluse prognoosimisse</span><span class="sxs-lookup"><span data-stu-id="0f804-125">Introduction to demand forecasting</span></span>](introduction-demand-forecasting.md)

[<span data-ttu-id="0f804-126">Prognoosi täpsuse jälgimine</span><span class="sxs-lookup"><span data-stu-id="0f804-126">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)



