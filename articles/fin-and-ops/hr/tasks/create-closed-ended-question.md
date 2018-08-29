--- 
title: "Kinniste küsimuste loomine"
description: "Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida."
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: e6e2535cb606b85ddb55a396a86ec408f1304bbf
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="create-closed-ended-questions"></a><span data-ttu-id="29e8d-103">Kinniste küsimuste loomine</span><span class="sxs-lookup"><span data-stu-id="29e8d-103">Create closed-ended questions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="29e8d-104">Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida.</span><span class="sxs-lookup"><span data-stu-id="29e8d-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="29e8d-105">Esmalt peate looma vastusegrupi vastustega, seejärel looma seda vastustegruppi kasutava küsimuse.</span><span class="sxs-lookup"><span data-stu-id="29e8d-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="29e8d-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="29e8d-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="29e8d-107">Vastustegrupi loomine</span><span class="sxs-lookup"><span data-stu-id="29e8d-107">Create an answer group</span></span>
1. <span data-ttu-id="29e8d-108">Avage Küsimustik > Kujundus > Vastustegrupid.</span><span class="sxs-lookup"><span data-stu-id="29e8d-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="29e8d-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-109">Click New.</span></span>
3. <span data-ttu-id="29e8d-110">Sisestage väärtus väljale Vastustegrupp.</span><span class="sxs-lookup"><span data-stu-id="29e8d-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="29e8d-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="29e8d-112">Kasutage funktsiooni Juhuslikult vastuste juhuslikult eri järjestuses paigutamiseks iga kord, kui vastusegruppi küsimuse puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="29e8d-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="29e8d-113">Klõpsake suvandit Vastus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-113">Click Answer.</span></span>
6. <span data-ttu-id="29e8d-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-114">Click New.</span></span>
    * <span data-ttu-id="29e8d-115">Seerianumber juhib vastuste kuvamise järjestust, v.a juhul, kui vastustegrupi puhul on valitud Juhuslikult.</span><span class="sxs-lookup"><span data-stu-id="29e8d-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="29e8d-116">Vastuste eest saab anda punkte küsimustiku punktiarvestuses kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="29e8d-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="29e8d-117">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="29e8d-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="29e8d-118">Õige vastuse saab märkida, näitamaks, et valitud vastus on õige.</span><span class="sxs-lookup"><span data-stu-id="29e8d-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="29e8d-119">Seda saab kasutada küsimustiku punktiarvestuseks.</span><span class="sxs-lookup"><span data-stu-id="29e8d-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="29e8d-120">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="29e8d-121">Jätkake vastusegrupi vastuse valikuvõimaluste loomist.</span><span class="sxs-lookup"><span data-stu-id="29e8d-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="29e8d-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-122">Click New.</span></span>
10. <span data-ttu-id="29e8d-123">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="29e8d-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="29e8d-124">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="29e8d-125">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-125">Click New.</span></span>
13. <span data-ttu-id="29e8d-126">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="29e8d-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="29e8d-127">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="29e8d-128">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-128">Click New.</span></span>
16. <span data-ttu-id="29e8d-129">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="29e8d-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="29e8d-130">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="29e8d-131">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-131">Click New.</span></span>
19. <span data-ttu-id="29e8d-132">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="29e8d-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="29e8d-133">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="29e8d-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="29e8d-134">Close the page.</span></span>
22. <span data-ttu-id="29e8d-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="29e8d-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="29e8d-136">Küsimuse loomine</span><span class="sxs-lookup"><span data-stu-id="29e8d-136">Create the question</span></span>
1. <span data-ttu-id="29e8d-137">Avage Küsimustik > Kujundus > Küsimused.</span><span class="sxs-lookup"><span data-stu-id="29e8d-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="29e8d-138">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="29e8d-138">Click New.</span></span>
3. <span data-ttu-id="29e8d-139">Kasutage seotud küsimuste koos grupeerimiseks välja Tüüp.</span><span class="sxs-lookup"><span data-stu-id="29e8d-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="29e8d-140">Saate kinniste küsimuste puhul kasutada sisendi tüüpe Märkeruut, Alternatiivne nupp või Liitboks.</span><span class="sxs-lookup"><span data-stu-id="29e8d-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="29e8d-141">Valige suvand väljalt Sisendi tüüp.</span><span class="sxs-lookup"><span data-stu-id="29e8d-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="29e8d-142">Sisestage või valige väärtus väljal Vastustegrupp.</span><span class="sxs-lookup"><span data-stu-id="29e8d-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="29e8d-143">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="29e8d-143">In the Text field, type a value.</span></span>


