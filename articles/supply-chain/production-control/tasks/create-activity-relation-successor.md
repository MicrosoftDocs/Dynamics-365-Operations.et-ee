---
title: Tegevuste seose loomine – Järgnev tegevus
description: Lean manufacturingi tootmisvoo tegevuste voog talletatakse tegevusseoste kaudu.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 91e1535ab6b53ad60394967d0377606a0cd27d01
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983442"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="b464e-103">Tegevuste seose loomine – Järgnev tegevus</span><span class="sxs-lookup"><span data-stu-id="b464e-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b464e-104">Lean manufacturingi tootmisvoo tegevuste voog talletatakse tegevusseoste kaudu.</span><span class="sxs-lookup"><span data-stu-id="b464e-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="b464e-105">See salvestus näitab, kuidas luua tegevusseoste kogumit.</span><span class="sxs-lookup"><span data-stu-id="b464e-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="b464e-106">Eeltingimused:</span><span class="sxs-lookup"><span data-stu-id="b464e-106">Prerequisites:</span></span>

- <span data-ttu-id="b464e-107">Tootmisvoog ja mustand mustandirežiimis.</span><span class="sxs-lookup"><span data-stu-id="b464e-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="b464e-108">Kaks tootmisvoos üksteisele järgnevat tegevust on loodud, kuid pole seotud.</span><span class="sxs-lookup"><span data-stu-id="b464e-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="b464e-109">Tootmisvoo versiooni leidmine</span><span class="sxs-lookup"><span data-stu-id="b464e-109">Find the production flow version</span></span> 
1. <span data-ttu-id="b464e-110">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="b464e-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="b464e-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b464e-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b464e-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b464e-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b464e-113">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b464e-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="b464e-114">Valige loendist mustandversioon.</span><span class="sxs-lookup"><span data-stu-id="b464e-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="b464e-115">Tegevuse seosed saab lisada nii tootmisvoo mustand- kui ka aktiivsetele versioonidele.</span><span class="sxs-lookup"><span data-stu-id="b464e-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="b464e-116">Tegevuse ülevaate avamine</span><span class="sxs-lookup"><span data-stu-id="b464e-116">Open the activity overview</span></span>
1. <span data-ttu-id="b464e-117">Klõpsake suvandit Tegevused.</span><span class="sxs-lookup"><span data-stu-id="b464e-117">Click Activities.</span></span>
    * <span data-ttu-id="b464e-118">Pange tähele, et vormil kuvatakse kõik tootmisvoo tegevused, mis on eraldatud nende tootmisvoogude versioonile, millega töötate.</span><span class="sxs-lookup"><span data-stu-id="b464e-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="b464e-119">Järeltulija lisamine</span><span class="sxs-lookup"><span data-stu-id="b464e-119">Add a Successor</span></span>
1. <span data-ttu-id="b464e-120">Klõpsake suvandit Järeltulija lisamine.</span><span class="sxs-lookup"><span data-stu-id="b464e-120">Click Add successor.</span></span>
2. <span data-ttu-id="b464e-121">Klõpsake väljal Tegevus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b464e-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="b464e-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b464e-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="b464e-123">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b464e-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b464e-124">Märkige ruut Piirang.</span><span class="sxs-lookup"><span data-stu-id="b464e-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="b464e-125">Sisestage number väljale Piirangu väärtus.</span><span class="sxs-lookup"><span data-stu-id="b464e-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="b464e-126">Piirangu aeg on aeg, mis plaanitakse eelkäija plaanitud lõpu (tähtaja kuupäev ja kellaaeg) ning järeltulija planeeritud alguse vahele.</span><span class="sxs-lookup"><span data-stu-id="b464e-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="b464e-127">Sisestage väärtus väljale Ühikud.</span><span class="sxs-lookup"><span data-stu-id="b464e-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="b464e-128">Sisestage number väljale Tsükliaja määr.</span><span class="sxs-lookup"><span data-stu-id="b464e-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="b464e-129">Kui mõlemad tegevused toimivad samas taktis, siis peab tsükli aja suhte väärtus olema 1.</span><span class="sxs-lookup"><span data-stu-id="b464e-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="b464e-130">Kui eelnev tegevus toimib järgnevast kaks korda kiiremini, siis peab suhte väärtus olema 2.</span><span class="sxs-lookup"><span data-stu-id="b464e-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="b464e-131">Tsükli aja suhteid kasutatakse tootmisvoo tegevuste individuaalsete tsükli aegade arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b464e-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="b464e-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b464e-132">Click OK.</span></span>
10. <span data-ttu-id="b464e-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b464e-133">Close the page.</span></span>
11. <span data-ttu-id="b464e-134">Klõpsake vahekaarti GridPanel.</span><span class="sxs-lookup"><span data-stu-id="b464e-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="b464e-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b464e-135">Close the page.</span></span>
13. <span data-ttu-id="b464e-136">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="b464e-136">Refresh the page.</span></span>

