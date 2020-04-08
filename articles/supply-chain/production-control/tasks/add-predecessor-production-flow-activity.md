---
title: Tootmisvoo tegevusele eelkäija lisamine
description: Tootmisvoo versiooni puhul peavad kõik tegevused olema järjestatud.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e64ad19c557c7b0fd8747bb9b748859e70eaa63a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149385"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="74861-103">Tootmisvoo tegevusele eelkäija lisamine</span><span class="sxs-lookup"><span data-stu-id="74861-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="74861-104">Tootmisvoo versiooni puhul peavad kõik tegevused olema järjestatud.</span><span class="sxs-lookup"><span data-stu-id="74861-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="74861-105">Tegevusel võib olla üks või mitu eelkäijat või järeltulijat.</span><span class="sxs-lookup"><span data-stu-id="74861-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="74861-106">See protseduur näitab, kuidas seostada eelkäijat tegevusega.</span><span class="sxs-lookup"><span data-stu-id="74861-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="74861-107">Selle toimingu tegemiseks vajate tootmisvoogu, mille mustandversioonil on vähemalt kaks tegevust, mille saab ühendada.</span><span class="sxs-lookup"><span data-stu-id="74861-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="74861-108">Lisateavet leiate tehnilisest ülevaatest Lean manufacturingi tootmisvood ja tegevused.</span><span class="sxs-lookup"><span data-stu-id="74861-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="74861-109">Otsige üles tootmisvoog ja versioon</span><span class="sxs-lookup"><span data-stu-id="74861-109">Find the production flow and version</span></span>
1. <span data-ttu-id="74861-110">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="74861-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="74861-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="74861-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="74861-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="74861-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="74861-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="74861-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="74861-114">Klõpsake suvandit Tegevused.</span><span class="sxs-lookup"><span data-stu-id="74861-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="74861-115">Valige tegevus ja lisage eelkäija</span><span class="sxs-lookup"><span data-stu-id="74861-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="74861-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="74861-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="74861-117">Klõpsake valikut Eelkäija lisamine.</span><span class="sxs-lookup"><span data-stu-id="74861-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="74861-118">Valige või sisestage väärtus väljal Tegevus.</span><span class="sxs-lookup"><span data-stu-id="74861-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="74861-119">Sisestage number väljale Tsükliaja määr.</span><span class="sxs-lookup"><span data-stu-id="74861-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="74861-120">Tegevusseoste kogumi tsükli aja vaikimisi väärtus on 1.</span><span class="sxs-lookup"><span data-stu-id="74861-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="74861-121">See eeldab, et mõlemaid tegevusi käitatakse samas tempos või takti ajas.</span><span class="sxs-lookup"><span data-stu-id="74861-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="74861-122">Kui eelkäija töötab kiiremini (väiksema takti ajaga), peaks suhe olema väiksem kui 1; kui eelkäija töötab aeglasemalt (suurema takti ajaga), on tsükli aja suhe suurem kui 1.</span><span class="sxs-lookup"><span data-stu-id="74861-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="74861-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="74861-123">Click OK.</span></span>

