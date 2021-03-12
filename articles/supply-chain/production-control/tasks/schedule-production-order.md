---
title: Tootmistellimuse plaanimine
description: See protseduur näitab, kuidas tootmistellimust plaanida.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fa0f0f38dcb93aff9b3a1d8130fba0a0c836b3b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981102"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="6c139-103">Tootmistellimuse plaanimine</span><span class="sxs-lookup"><span data-stu-id="6c139-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c139-104">See protseduur näitab, kuidas tootmistellimust plaanida.</span><span class="sxs-lookup"><span data-stu-id="6c139-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="6c139-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="6c139-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6c139-106">See on kolmas protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="6c139-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="6c139-107">Tootmistellimuse plaanimine</span><span class="sxs-lookup"><span data-stu-id="6c139-107">Schedule a production order</span></span>
1. <span data-ttu-id="6c139-108">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="6c139-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="6c139-109">Valige tootmistellimus, mille olek on Hinnanguline.</span><span class="sxs-lookup"><span data-stu-id="6c139-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="6c139-110">Klõpsake tegumiribal valikut Graafik.</span><span class="sxs-lookup"><span data-stu-id="6c139-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="6c139-111">Klõpsake valikut Tööde planeerimine.</span><span class="sxs-lookup"><span data-stu-id="6c139-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="6c139-112">Plaanimise parameetrid häälestatakse sel lehel.</span><span class="sxs-lookup"><span data-stu-id="6c139-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="6c139-113">Saate häälestada konkreetsete kasutajate või kõigi kasutajate parameetrid.</span><span class="sxs-lookup"><span data-stu-id="6c139-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="6c139-114">Valige väljal Plaanimissuund suvand „Edasi tänasest”.</span><span class="sxs-lookup"><span data-stu-id="6c139-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="6c139-115">Sisestage kuupäev väljale Plaanimiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="6c139-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="6c139-116">Märkige või tühjendage ruut Piiratud võimsus.</span><span class="sxs-lookup"><span data-stu-id="6c139-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="6c139-117">Märkige või tühjendage ruut Limiteeritud materjal.</span><span class="sxs-lookup"><span data-stu-id="6c139-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="6c139-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c139-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="6c139-119">Plaanimise tulemuste kuvamine</span><span class="sxs-lookup"><span data-stu-id="6c139-119">View the scheduling results</span></span>
1. <span data-ttu-id="6c139-120">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="6c139-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="6c139-121">Klõpsake valikut Kõik tööd.</span><span class="sxs-lookup"><span data-stu-id="6c139-121">Click All jobs.</span></span>
    * <span data-ttu-id="6c139-122">Lehel kuvatakse äsja loodud plaanitud tööd.</span><span class="sxs-lookup"><span data-stu-id="6c139-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="6c139-123">Laiendage või ahendage jaotist Plaanimine.</span><span class="sxs-lookup"><span data-stu-id="6c139-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="6c139-124">Kiirinfos Plaanimine näete plaanitud kuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="6c139-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="6c139-125">Klõpsake suvandit Päringud.</span><span class="sxs-lookup"><span data-stu-id="6c139-125">Click Inquiries.</span></span>
5. <span data-ttu-id="6c139-126">Klõpsake suvandit Täiskoormus.</span><span class="sxs-lookup"><span data-stu-id="6c139-126">Click Capacity load.</span></span>
    * <span data-ttu-id="6c139-127">Lehel Täiskoormus kuvatakse töö plaanimise kaudu reserveeritud võimekus, ressursi jaoks praegu reserveeritud tundide koguarv ja ressursi töö plaanimise jaoks järelejäänud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="6c139-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="6c139-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c139-128">Close the page.</span></span>
7. <span data-ttu-id="6c139-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c139-129">Close the page.</span></span>

