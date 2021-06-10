---
title: Tegevuskoha jaoks plaani loomine
description: Tootmise plaanija arvutab materjali ja võimsuse nõuded konkreetse kauba tootmiseks.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d84fcd0012d4f7d87e2bc0769261fbe5f5139670
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102658"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="52b45-103">Tegevuskoha jaoks plaani loomine</span><span class="sxs-lookup"><span data-stu-id="52b45-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52b45-104">Tootmise plaanija arvutab materjali ja võimsuse nõuded konkreetse kauba tootmiseks.</span><span class="sxs-lookup"><span data-stu-id="52b45-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="52b45-105">Pärast hankimissoovituste loomist otsib ta planeeritava tegevuskoha tellimused ja kinnitab tellimused, alustades pakilisematega.</span><span class="sxs-lookup"><span data-stu-id="52b45-105">After the sourcing suggestions are created, they find the orders at the site for which they are planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="52b45-106">Kõige pakilisemad tellimused on need, mis tuleb kinnitada käesoleval kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="52b45-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="52b45-107">Kasutage nende ülesannete täitmiseks demoandmete ettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="52b45-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="52b45-108">Kaubale materjalide ja võimsuse plaani loomine</span><span class="sxs-lookup"><span data-stu-id="52b45-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="52b45-109">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="52b45-109">Click Master planning.</span></span>
    * <span data-ttu-id="52b45-110">Peate liikuma vaikearmatuurlauale.</span><span class="sxs-lookup"><span data-stu-id="52b45-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="52b45-111">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="52b45-111">Click Run.</span></span>
3. <span data-ttu-id="52b45-112">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="52b45-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="52b45-113">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="52b45-113">Click Filter.</span></span>
5. <span data-ttu-id="52b45-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="52b45-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="52b45-115">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="52b45-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="52b45-116">Näide: D0001.</span><span class="sxs-lookup"><span data-stu-id="52b45-116">Example: D0001</span></span>  
7. <span data-ttu-id="52b45-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="52b45-117">Click OK.</span></span>
8. <span data-ttu-id="52b45-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="52b45-118">Click OK.</span></span>
    * <span data-ttu-id="52b45-119">Selleks võib kuluda mõni minut.</span><span class="sxs-lookup"><span data-stu-id="52b45-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="52b45-120">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="52b45-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="52b45-121">Pakiliste plaanitud kaubatellimuste tuvastamine</span><span class="sxs-lookup"><span data-stu-id="52b45-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="52b45-122">Avage veeru Kaubakood filter.</span><span class="sxs-lookup"><span data-stu-id="52b45-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="52b45-123">Rakendage väljal Kaubakood filtrit väärtusega „D0001”ning kasutage filtri tehtemärki algab järgmisega.</span><span class="sxs-lookup"><span data-stu-id="52b45-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="52b45-124">Avage veeru Tellimuse kuupäev filter.</span><span class="sxs-lookup"><span data-stu-id="52b45-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="52b45-125">Rakendage filtrit väljal Tellimuse kuupäev koos praeguse kuupäeva väärtusega, kasutades filtrit väärtusega „on täpselt”.</span><span class="sxs-lookup"><span data-stu-id="52b45-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="52b45-126">Kõikide pakiliste kaubatellimuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="52b45-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="52b45-127">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="52b45-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="52b45-128">Klõpsake nuppu Kinnita.</span><span class="sxs-lookup"><span data-stu-id="52b45-128">Click Firm.</span></span>
3. <span data-ttu-id="52b45-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="52b45-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]