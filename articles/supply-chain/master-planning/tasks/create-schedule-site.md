---
title: Tegevuskoha jaoks graafiku loomine
description: See protseduur selgitab, kuidas ajastada tootmistellimusi, mida ei ole tegevuskoha jaoks veel alustatud.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e188c5059b3957f3c0291bc4b8c525aac4d399
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214270"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="585ca-103">Tegevuskoha jaoks graafiku loomine</span><span class="sxs-lookup"><span data-stu-id="585ca-103">Create a schedule for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="585ca-104">See protseduur selgitab, kuidas ajastada tootmistellimusi, mida ei ole tegevuskoha jaoks veel alustatud.</span><span class="sxs-lookup"><span data-stu-id="585ca-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="585ca-105">Selle protseduuri lõpuleviimiseks kasutatakse demoandmete ettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="585ca-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="585ca-106">Käivitamata tootmistellimuste tuvastamine</span><span class="sxs-lookup"><span data-stu-id="585ca-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="585ca-107">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="585ca-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="585ca-108">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="585ca-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="585ca-109">Näiteks filtreerige väljal Tegevuskoht väärtusega 1.</span><span class="sxs-lookup"><span data-stu-id="585ca-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="585ca-110">1 tähistab tegevuskohta USMF-is.</span><span class="sxs-lookup"><span data-stu-id="585ca-110">1 represents a site in USMF.</span></span> <span data-ttu-id="585ca-111">Kui te ei kasuta USMF-i, valige tegevuskoht oma ettevõttest.</span><span class="sxs-lookup"><span data-stu-id="585ca-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="585ca-112">Avage veeru Olek filter.</span><span class="sxs-lookup"><span data-stu-id="585ca-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="585ca-113">Rakendage filtrit väljal Olek koos väärtusega Plaanitud, kasutades filtrit väärtusega „on täpselt”.</span><span class="sxs-lookup"><span data-stu-id="585ca-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="585ca-114">Graafiku loomine</span><span class="sxs-lookup"><span data-stu-id="585ca-114">Create a schedule</span></span>
1. <span data-ttu-id="585ca-115">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="585ca-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="585ca-116">Klõpsake tegumiribal valikut Graafik.</span><span class="sxs-lookup"><span data-stu-id="585ca-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="585ca-117">Klõpsake valikut Tööde plaanimine.</span><span class="sxs-lookup"><span data-stu-id="585ca-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="585ca-118">Valige väljal Planeerimissuund üksus Tarnekuupäevast tagasi.</span><span class="sxs-lookup"><span data-stu-id="585ca-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="585ca-119">Tehke väljal Piiratud võimsus valik Ei.</span><span class="sxs-lookup"><span data-stu-id="585ca-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="585ca-120">Tehke väljal Piiratud materjal valik Ei.</span><span class="sxs-lookup"><span data-stu-id="585ca-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="585ca-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="585ca-121">Click OK.</span></span>
    * <span data-ttu-id="585ca-122">See võib veidi aega võtta.</span><span class="sxs-lookup"><span data-stu-id="585ca-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="585ca-123">Plaanitud tootmistellimuste tulemite vaatamine</span><span class="sxs-lookup"><span data-stu-id="585ca-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="585ca-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="585ca-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="585ca-125">Saate märkida mis tahes rea.</span><span class="sxs-lookup"><span data-stu-id="585ca-125">You can mark any row.</span></span>  
2. <span data-ttu-id="585ca-126">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="585ca-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="585ca-127">Klõpsake valikut Kõik tööd.</span><span class="sxs-lookup"><span data-stu-id="585ca-127">Click All jobs.</span></span>
    * <span data-ttu-id="585ca-128">Sellel lehel saate vaadata tööde loendit.</span><span class="sxs-lookup"><span data-stu-id="585ca-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="585ca-129">Vahekaardil Plaanimine saate vaadata töö algus- ja lõppkuupäeva.</span><span class="sxs-lookup"><span data-stu-id="585ca-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="585ca-130">Klõpsake suvandit Materjalid.</span><span class="sxs-lookup"><span data-stu-id="585ca-130">Click Materials.</span></span>
    * <span data-ttu-id="585ca-131">Sellel lehel saate vaadata tootmistellimuse toimingute eeldatavat materjalikulu ja praegust saadaolevat kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="585ca-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]