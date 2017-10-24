--- 
title: "Tootmisvoo tegevusele eelkäija lisamine"
description: "Tootmisvoo versiooni puhul peavad kõik tegevused olema järjestatud."
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: d19fb20e8cc941daeaa506e4bf1cb0c7031cf2ee
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="73ef9-103">Tootmisvoo tegevusele eelkäija lisamine</span><span class="sxs-lookup"><span data-stu-id="73ef9-103">Add a predecessor to a production flow activity</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73ef9-104">Tootmisvoo versiooni puhul peavad kõik tegevused olema järjestatud.</span><span class="sxs-lookup"><span data-stu-id="73ef9-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="73ef9-105">Tegevusel võib olla üks või mitu eelkäijat või järeltulijat.</span><span class="sxs-lookup"><span data-stu-id="73ef9-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="73ef9-106">See protseduur näitab, kuidas seostada eelkäijat tegevusega.</span><span class="sxs-lookup"><span data-stu-id="73ef9-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="73ef9-107">Selle toimingu tegemiseks vajate tootmisvoogu, mille mustandversioonil on vähemalt kaks tegevust, mille saab ühendada.</span><span class="sxs-lookup"><span data-stu-id="73ef9-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="73ef9-108">Lisateavet leiate tehnilisest ülevaatest Lean manufacturingi tootmisvood ja tegevused.</span><span class="sxs-lookup"><span data-stu-id="73ef9-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="73ef9-109">Otsige üles tootmisvoog ja versioon</span><span class="sxs-lookup"><span data-stu-id="73ef9-109">Find the production flow and version</span></span>
1. <span data-ttu-id="73ef9-110">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="73ef9-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="73ef9-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="73ef9-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="73ef9-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="73ef9-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="73ef9-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="73ef9-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="73ef9-114">Klõpsake suvandit Tegevused.</span><span class="sxs-lookup"><span data-stu-id="73ef9-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="73ef9-115">Valige tegevus ja lisage eelkäija</span><span class="sxs-lookup"><span data-stu-id="73ef9-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="73ef9-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="73ef9-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="73ef9-117">Klõpsake valikut Eelkäija lisamine.</span><span class="sxs-lookup"><span data-stu-id="73ef9-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="73ef9-118">Valige või sisestage väärtus väljal Tegevus.</span><span class="sxs-lookup"><span data-stu-id="73ef9-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="73ef9-119">Sisestage number väljale Tsükliaja määr.</span><span class="sxs-lookup"><span data-stu-id="73ef9-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="73ef9-120">Tegevusseoste kogumi tsükli aja vaikimisi väärtus on 1.</span><span class="sxs-lookup"><span data-stu-id="73ef9-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="73ef9-121">See eeldab, et mõlemaid tegevusi käitatakse samas tempos või takti ajas.</span><span class="sxs-lookup"><span data-stu-id="73ef9-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="73ef9-122">Kui eelkäija töötab kiiremini (väiksema takti ajaga), peaks suhe olema väiksem kui 1; kui eelkäija töötab aeglasemalt (suurema takti ajaga), on tsükli aja suhe suurem kui 1.</span><span class="sxs-lookup"><span data-stu-id="73ef9-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="73ef9-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="73ef9-123">Click OK.</span></span>


