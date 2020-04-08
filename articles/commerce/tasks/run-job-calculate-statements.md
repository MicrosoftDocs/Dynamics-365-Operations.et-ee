---
title: Väljavõtete arvutamiseks töö konfigureerimine ja käivitamine
description: See protseduur selgitab korduvate pakett-tööde konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete loomiseks ja arvutamiseks.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 973236acca0cb8c0d57171e4bb9d4daaa7faaf38
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141196"
---
# <a name="configure-and-run-job-to-calculate-statements"></a><span data-ttu-id="cf4f2-103">Väljavõtete arvutamiseks töö konfigureerimine ja käivitamine</span><span class="sxs-lookup"><span data-stu-id="cf4f2-103">Configure and run job to calculate statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf4f2-104">See protseduur selgitab korduvate pakett-tööde konfigureerimist ja käitamist valitud kaupluse või kauplusegrupi jaoks väljavõtete loomiseks ja arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="cf4f2-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="cf4f2-106">Avage Kõik tööruumid > Kaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-106">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="cf4f2-107">Klõpsake suvandit Väljavõtete arvutamine.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="cf4f2-108">Valige kindel kauplus või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="cf4f2-109">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="cf4f2-110">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="cf4f2-111">Valige suvandi Pakktöötlus sätteks Jah.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="cf4f2-112">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-112">Click Recurrence.</span></span>
6. <span data-ttu-id="cf4f2-113">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="cf4f2-114">Sisestage kellaaeg väljale Algusaeg.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="cf4f2-115">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-115">Select the No end date option.</span></span>
9. <span data-ttu-id="cf4f2-116">Sisestage väljale PatternUnit suvand Päevad.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="cf4f2-117">Sisestage number väljale Kohta.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="cf4f2-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-118">Click OK.</span></span>
12. <span data-ttu-id="cf4f2-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cf4f2-119">Click OK.</span></span>

