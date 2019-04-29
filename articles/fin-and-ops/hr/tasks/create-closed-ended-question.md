---
title: Suletud küsimuse loomine
description: Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e4f9697fc00798d917db6f7f50d7e3b8739233
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "858648"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="af53f-103">Suletud küsimuse loomine</span><span class="sxs-lookup"><span data-stu-id="af53f-103">Create a closed ended question</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="af53f-104">Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida.</span><span class="sxs-lookup"><span data-stu-id="af53f-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="af53f-105">Esmalt peate looma vastusegrupi vastustega, seejärel looma seda vastustegruppi kasutava küsimuse.</span><span class="sxs-lookup"><span data-stu-id="af53f-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="af53f-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="af53f-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="af53f-107">Vastustegrupi loomine</span><span class="sxs-lookup"><span data-stu-id="af53f-107">Create an answer group</span></span>
1. <span data-ttu-id="af53f-108">Avage Küsimustik > Kujundus > Vastustegrupid.</span><span class="sxs-lookup"><span data-stu-id="af53f-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="af53f-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="af53f-109">Click New.</span></span>
3. <span data-ttu-id="af53f-110">Sisestage väärtus väljale Vastustegrupp.</span><span class="sxs-lookup"><span data-stu-id="af53f-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="af53f-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="af53f-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="af53f-112">Kasutage funktsiooni Juhuslikult vastuste juhuslikult eri järjestuses paigutamiseks iga kord, kui vastusegruppi küsimuse puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="af53f-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="af53f-113">Klõpsake suvandit Vastus.</span><span class="sxs-lookup"><span data-stu-id="af53f-113">Click Answer.</span></span>
6. <span data-ttu-id="af53f-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="af53f-114">Click New.</span></span>
    * <span data-ttu-id="af53f-115">Seerianumber juhib vastuste kuvamise järjestust, v.a juhul, kui vastustegrupi puhul on valitud Juhuslikult.</span><span class="sxs-lookup"><span data-stu-id="af53f-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="af53f-116">Vastuste eest saab anda punkte küsimustiku punktiarvestuses kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="af53f-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="af53f-117">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="af53f-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="af53f-118">Õige vastuse saab märkida, näitamaks, et valitud vastus on õige.</span><span class="sxs-lookup"><span data-stu-id="af53f-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="af53f-119">Seda saab kasutada küsimustiku punktiarvestuseks.</span><span class="sxs-lookup"><span data-stu-id="af53f-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="af53f-120">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="af53f-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="af53f-121">Jätkake vastusegrupi vastuse valikuvõimaluste loomist.</span><span class="sxs-lookup"><span data-stu-id="af53f-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="af53f-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="af53f-122">Click New.</span></span>
10. <span data-ttu-id="af53f-123">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="af53f-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="af53f-124">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="af53f-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="af53f-125">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="af53f-125">Click New.</span></span>
13. <span data-ttu-id="af53f-126">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="af53f-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="af53f-127">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="af53f-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="af53f-128">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="af53f-128">Click New.</span></span>
16. <span data-ttu-id="af53f-129">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="af53f-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="af53f-130">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="af53f-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="af53f-131">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="af53f-131">Click New.</span></span>
19. <span data-ttu-id="af53f-132">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="af53f-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="af53f-133">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="af53f-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="af53f-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="af53f-134">Close the page.</span></span>
22. <span data-ttu-id="af53f-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="af53f-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="af53f-136">Küsimuse loomine</span><span class="sxs-lookup"><span data-stu-id="af53f-136">Create the question</span></span>
1. <span data-ttu-id="af53f-137">Avage Küsimustik > Kujundus > Küsimused.</span><span class="sxs-lookup"><span data-stu-id="af53f-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="af53f-138">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="af53f-138">Click New.</span></span>
3. <span data-ttu-id="af53f-139">Kasutage seotud küsimuste koos grupeerimiseks välja Tüüp.</span><span class="sxs-lookup"><span data-stu-id="af53f-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="af53f-140">Saate kinniste küsimuste puhul kasutada sisendi tüüpe Märkeruut, Alternatiivne nupp või Liitboks.</span><span class="sxs-lookup"><span data-stu-id="af53f-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="af53f-141">Valige suvand väljalt Sisendi tüüp.</span><span class="sxs-lookup"><span data-stu-id="af53f-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="af53f-142">Sisestage või valige väärtus väljal Vastustegrupp.</span><span class="sxs-lookup"><span data-stu-id="af53f-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="af53f-143">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="af53f-143">In the Text field, type a value.</span></span>

