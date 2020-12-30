---
title: Tegevuskoha jaoks plaani loomine
description: Tootmise plaanija arvutab materjali ja võimsuse nõuded konkreetse kauba tootmiseks.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 52721d948554d4853f9e1d4dec45e45e619a4829
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426276"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="dc28b-103">Tegevuskoha jaoks plaani loomine</span><span class="sxs-lookup"><span data-stu-id="dc28b-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dc28b-104">Tootmise plaanija arvutab materjali ja võimsuse nõuded konkreetse kauba tootmiseks.</span><span class="sxs-lookup"><span data-stu-id="dc28b-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="dc28b-105">Pärast hankimissoovituste loomist otsib ta planeeritava tegevuskoha tellimused ja kinnitab tellimused, alustades pakilisematega.</span><span class="sxs-lookup"><span data-stu-id="dc28b-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="dc28b-106">Kõige pakilisemad tellimused on need, mis tuleb kinnitada käesoleval kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="dc28b-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="dc28b-107">Kasutage nende ülesannete täitmiseks demoandmete ettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="dc28b-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="dc28b-108">Kaubale materjalide ja võimsuse plaani loomine</span><span class="sxs-lookup"><span data-stu-id="dc28b-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="dc28b-109">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="dc28b-109">Click Master planning.</span></span>
    * <span data-ttu-id="dc28b-110">Peate liikuma vaikearmatuurlauale.</span><span class="sxs-lookup"><span data-stu-id="dc28b-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="dc28b-111">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="dc28b-111">Click Run.</span></span>
3. <span data-ttu-id="dc28b-112">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="dc28b-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="dc28b-113">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="dc28b-113">Click Filter.</span></span>
5. <span data-ttu-id="dc28b-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="dc28b-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="dc28b-115">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="dc28b-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="dc28b-116">Näide: D0001.</span><span class="sxs-lookup"><span data-stu-id="dc28b-116">Example: D0001</span></span>  
7. <span data-ttu-id="dc28b-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dc28b-117">Click OK.</span></span>
8. <span data-ttu-id="dc28b-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dc28b-118">Click OK.</span></span>
    * <span data-ttu-id="dc28b-119">Selleks võib kuluda mõni minut.</span><span class="sxs-lookup"><span data-stu-id="dc28b-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="dc28b-120">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="dc28b-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="dc28b-121">Pakiliste plaanitud kaubatellimuste tuvastamine</span><span class="sxs-lookup"><span data-stu-id="dc28b-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="dc28b-122">Avage veeru Kaubakood filter.</span><span class="sxs-lookup"><span data-stu-id="dc28b-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="dc28b-123">Rakendage väljal Kaubakood filtrit väärtusega „D0001”ning kasutage filtri tehtemärki algab järgmisega.</span><span class="sxs-lookup"><span data-stu-id="dc28b-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="dc28b-124">Avage veeru Tellimuse kuupäev filter.</span><span class="sxs-lookup"><span data-stu-id="dc28b-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="dc28b-125">Rakendage filtrit väljal Tellimuse kuupäev koos praeguse kuupäeva väärtusega, kasutades filtrit väärtusega „on täpselt”.</span><span class="sxs-lookup"><span data-stu-id="dc28b-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="dc28b-126">Kõikide pakiliste kaubatellimuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="dc28b-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="dc28b-127">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="dc28b-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="dc28b-128">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="dc28b-128">Click Firm.</span></span>
3. <span data-ttu-id="dc28b-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dc28b-129">Click OK.</span></span>

