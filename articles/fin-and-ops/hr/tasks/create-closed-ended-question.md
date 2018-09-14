--- 
title: "Suletud küsimuse loomine"
description: "Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6b08988a3872cec39b7592732d23862e959aae79
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="855a2-103">Suletud küsimuse loomine</span><span class="sxs-lookup"><span data-stu-id="855a2-103">Create a closed ended question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="855a2-104">Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida.</span><span class="sxs-lookup"><span data-stu-id="855a2-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="855a2-105">Esmalt peate looma vastusegrupi vastustega, seejärel looma seda vastustegruppi kasutava küsimuse.</span><span class="sxs-lookup"><span data-stu-id="855a2-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="855a2-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="855a2-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="855a2-107">Vastustegrupi loomine</span><span class="sxs-lookup"><span data-stu-id="855a2-107">Create an answer group</span></span>
1. <span data-ttu-id="855a2-108">Avage Küsimustik > Kujundus > Vastustegrupid.</span><span class="sxs-lookup"><span data-stu-id="855a2-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="855a2-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="855a2-109">Click New.</span></span>
3. <span data-ttu-id="855a2-110">Sisestage väärtus väljale Vastustegrupp.</span><span class="sxs-lookup"><span data-stu-id="855a2-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="855a2-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="855a2-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="855a2-112">Kasutage funktsiooni Juhuslikult vastuste juhuslikult eri järjestuses paigutamiseks iga kord, kui vastusegruppi küsimuse puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="855a2-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="855a2-113">Klõpsake suvandit Vastus.</span><span class="sxs-lookup"><span data-stu-id="855a2-113">Click Answer.</span></span>
6. <span data-ttu-id="855a2-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="855a2-114">Click New.</span></span>
    * <span data-ttu-id="855a2-115">Seerianumber juhib vastuste kuvamise järjestust, v.a juhul, kui vastustegrupi puhul on valitud Juhuslikult.</span><span class="sxs-lookup"><span data-stu-id="855a2-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="855a2-116">Vastuste eest saab anda punkte küsimustiku punktiarvestuses kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="855a2-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="855a2-117">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="855a2-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="855a2-118">Õige vastuse saab märkida, näitamaks, et valitud vastus on õige.</span><span class="sxs-lookup"><span data-stu-id="855a2-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="855a2-119">Seda saab kasutada küsimustiku punktiarvestuseks.</span><span class="sxs-lookup"><span data-stu-id="855a2-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="855a2-120">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="855a2-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="855a2-121">Jätkake vastusegrupi vastuse valikuvõimaluste loomist.</span><span class="sxs-lookup"><span data-stu-id="855a2-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="855a2-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="855a2-122">Click New.</span></span>
10. <span data-ttu-id="855a2-123">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="855a2-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="855a2-124">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="855a2-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="855a2-125">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="855a2-125">Click New.</span></span>
13. <span data-ttu-id="855a2-126">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="855a2-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="855a2-127">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="855a2-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="855a2-128">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="855a2-128">Click New.</span></span>
16. <span data-ttu-id="855a2-129">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="855a2-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="855a2-130">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="855a2-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="855a2-131">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="855a2-131">Click New.</span></span>
19. <span data-ttu-id="855a2-132">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="855a2-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="855a2-133">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="855a2-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="855a2-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="855a2-134">Close the page.</span></span>
22. <span data-ttu-id="855a2-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="855a2-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="855a2-136">Küsimuse loomine</span><span class="sxs-lookup"><span data-stu-id="855a2-136">Create the question</span></span>
1. <span data-ttu-id="855a2-137">Avage Küsimustik > Kujundus > Küsimused.</span><span class="sxs-lookup"><span data-stu-id="855a2-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="855a2-138">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="855a2-138">Click New.</span></span>
3. <span data-ttu-id="855a2-139">Kasutage seotud küsimuste koos grupeerimiseks välja Tüüp.</span><span class="sxs-lookup"><span data-stu-id="855a2-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="855a2-140">Saate kinniste küsimuste puhul kasutada sisendi tüüpe Märkeruut, Alternatiivne nupp või Liitboks.</span><span class="sxs-lookup"><span data-stu-id="855a2-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="855a2-141">Valige suvand väljalt Sisendi tüüp.</span><span class="sxs-lookup"><span data-stu-id="855a2-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="855a2-142">Sisestage või valige väärtus väljal Vastustegrupp.</span><span class="sxs-lookup"><span data-stu-id="855a2-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="855a2-143">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="855a2-143">In the Text field, type a value.</span></span>


