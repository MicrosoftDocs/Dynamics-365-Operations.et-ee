---
title: Tootmistellimuse plaanimine
description: See protseduur näitab, kuidas tootmistellimust plaanida.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20e7ee023f39cc5d02b0f5b80fbb3ae3ad0c9774
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "346360"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="82b79-103">Tootmistellimuse plaanimine</span><span class="sxs-lookup"><span data-stu-id="82b79-103">Schedule a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82b79-104">See protseduur näitab, kuidas tootmistellimust plaanida.</span><span class="sxs-lookup"><span data-stu-id="82b79-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="82b79-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="82b79-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="82b79-106">See on kolmas protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="82b79-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="82b79-107">Tootmistellimuse plaanimine</span><span class="sxs-lookup"><span data-stu-id="82b79-107">Schedule a production order</span></span>
1. <span data-ttu-id="82b79-108">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="82b79-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="82b79-109">Valige tootmistellimus, mille olek on Hinnanguline.</span><span class="sxs-lookup"><span data-stu-id="82b79-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="82b79-110">Klõpsake tegumiribal valikut Graafik.</span><span class="sxs-lookup"><span data-stu-id="82b79-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="82b79-111">Klõpsake valikut Tööde planeerimine.</span><span class="sxs-lookup"><span data-stu-id="82b79-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="82b79-112">Plaanimise parameetrid häälestatakse sel lehel.</span><span class="sxs-lookup"><span data-stu-id="82b79-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="82b79-113">Saate häälestada konkreetsete kasutajate või kõigi kasutajate parameetrid.</span><span class="sxs-lookup"><span data-stu-id="82b79-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="82b79-114">Valige väljal Plaanimissuund suvand „Edasi tänasest”.</span><span class="sxs-lookup"><span data-stu-id="82b79-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="82b79-115">Sisestage kuupäev väljale Plaanimiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="82b79-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="82b79-116">Märkige või tühjendage ruut Piiratud võimsus.</span><span class="sxs-lookup"><span data-stu-id="82b79-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="82b79-117">Märkige või tühjendage ruut Limiteeritud materjal.</span><span class="sxs-lookup"><span data-stu-id="82b79-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="82b79-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="82b79-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="82b79-119">Plaanimise tulemuste kuvamine</span><span class="sxs-lookup"><span data-stu-id="82b79-119">View the scheduling results</span></span>
1. <span data-ttu-id="82b79-120">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="82b79-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="82b79-121">Klõpsake valikut Kõik tööd.</span><span class="sxs-lookup"><span data-stu-id="82b79-121">Click All jobs.</span></span>
    * <span data-ttu-id="82b79-122">Lehel kuvatakse äsja loodud plaanitud tööd.</span><span class="sxs-lookup"><span data-stu-id="82b79-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="82b79-123">Laiendage või ahendage jaotist Plaanimine.</span><span class="sxs-lookup"><span data-stu-id="82b79-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="82b79-124">Kiirinfos Plaanimine näete plaanitud kuupäeva ja kellaaega.</span><span class="sxs-lookup"><span data-stu-id="82b79-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="82b79-125">Klõpsake suvandit Päringud.</span><span class="sxs-lookup"><span data-stu-id="82b79-125">Click Inquiries.</span></span>
5. <span data-ttu-id="82b79-126">Klõpsake suvandit Täiskoormus.</span><span class="sxs-lookup"><span data-stu-id="82b79-126">Click Capacity load.</span></span>
    * <span data-ttu-id="82b79-127">Lehel Täiskoormus kuvatakse töö plaanimise kaudu reserveeritud võimekus, ressursi jaoks praegu reserveeritud tundide koguarv ja ressursi töö plaanimise jaoks järelejäänud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="82b79-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="82b79-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="82b79-128">Close the page.</span></span>
7. <span data-ttu-id="82b79-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="82b79-129">Close the page.</span></span>

