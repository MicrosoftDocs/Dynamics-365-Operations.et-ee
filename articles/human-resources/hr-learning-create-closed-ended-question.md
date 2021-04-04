---
title: Suletud küsimuse loomine
description: Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMAnswerCollection, KMAnswer, KMQuestion, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09bf57b26111be0e3de358a6c955b3df7bf50668
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467887"
---
# <a name="create-a-closed-ended-question"></a><span data-ttu-id="dd808-103">Suletud küsimuse loomine</span><span class="sxs-lookup"><span data-stu-id="dd808-103">Create a closed ended question</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="dd808-104">Kinnised küsimused võimaldavad teil pakkuda valikuid, mille hulgast vastaja saab valida.</span><span class="sxs-lookup"><span data-stu-id="dd808-104">Closed-ended questions allow you to provide options for the respondent to choose from.</span></span> <span data-ttu-id="dd808-105">Esmalt peate looma vastusegrupi vastustega, seejärel looma seda vastustegruppi kasutava küsimuse.</span><span class="sxs-lookup"><span data-stu-id="dd808-105">First, you need to create the Answer group with the answers, then create the question that will use the answer group.</span></span> <span data-ttu-id="dd808-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="dd808-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-an-answer-group"></a><span data-ttu-id="dd808-107">Vastustegrupi loomine</span><span class="sxs-lookup"><span data-stu-id="dd808-107">Create an answer group</span></span>
1. <span data-ttu-id="dd808-108">Avage Küsimustik > Kujundus > Vastustegrupid.</span><span class="sxs-lookup"><span data-stu-id="dd808-108">Go to Questionnaire > Design > Answer groups.</span></span>
2. <span data-ttu-id="dd808-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dd808-109">Click New.</span></span>
3. <span data-ttu-id="dd808-110">Sisestage väärtus väljale Vastustegrupp.</span><span class="sxs-lookup"><span data-stu-id="dd808-110">In the Answer group field, type a value.</span></span>
4. <span data-ttu-id="dd808-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="dd808-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="dd808-112">Kasutage funktsiooni Juhuslikult vastuste juhuslikult eri järjestuses paigutamiseks iga kord, kui vastusegruppi küsimuse puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="dd808-112">Use the Randomize functionality to randomly place the answers in a different order each time the answer group is used for a question.</span></span>  
5. <span data-ttu-id="dd808-113">Klõpsake suvandit Vastus.</span><span class="sxs-lookup"><span data-stu-id="dd808-113">Click Answer.</span></span>
6. <span data-ttu-id="dd808-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dd808-114">Click New.</span></span>
    * <span data-ttu-id="dd808-115">Seerianumber juhib vastuste kuvamise järjestust, v.a juhul, kui vastustegrupi puhul on valitud Juhuslikult.</span><span class="sxs-lookup"><span data-stu-id="dd808-115">Sequence number controls the order in which the answers are displayed, unless Randomize is selected for the Answer group.</span></span>  
    * <span data-ttu-id="dd808-116">Vastuste eest saab anda punkte küsimustiku punktiarvestuses kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="dd808-116">Points can be awarded to answers for use in scoring the questionnaire.</span></span>  
7. <span data-ttu-id="dd808-117">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="dd808-117">In the Points field, enter a number.</span></span>
    * <span data-ttu-id="dd808-118">Õige vastuse saab märkida, näitamaks, et valitud vastus on õige.</span><span class="sxs-lookup"><span data-stu-id="dd808-118">The correct answer can be marked to indicate that the selected answer is the correct one.</span></span> <span data-ttu-id="dd808-119">Seda saab kasutada küsimustiku punktiarvestuseks.</span><span class="sxs-lookup"><span data-stu-id="dd808-119">This can be used for scoring the questionnaire.</span></span>  
8. <span data-ttu-id="dd808-120">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="dd808-120">In the Answer field, type a value.</span></span>
    * <span data-ttu-id="dd808-121">Jätkake vastusegrupi vastuse valikuvõimaluste loomist.</span><span class="sxs-lookup"><span data-stu-id="dd808-121">Continue to create answer selection options for the answer group.</span></span>  
9. <span data-ttu-id="dd808-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dd808-122">Click New.</span></span>
10. <span data-ttu-id="dd808-123">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="dd808-123">In the Points field, enter a number.</span></span>
11. <span data-ttu-id="dd808-124">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="dd808-124">In the Answer field, type a value.</span></span>
12. <span data-ttu-id="dd808-125">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="dd808-125">Click New.</span></span>
13. <span data-ttu-id="dd808-126">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="dd808-126">In the Points field, enter a number.</span></span>
14. <span data-ttu-id="dd808-127">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="dd808-127">In the Answer field, type a value.</span></span>
15. <span data-ttu-id="dd808-128">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="dd808-128">Click New.</span></span>
16. <span data-ttu-id="dd808-129">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="dd808-129">In the Points field, enter a number.</span></span>
17. <span data-ttu-id="dd808-130">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="dd808-130">In the Answer field, type a value.</span></span>
18. <span data-ttu-id="dd808-131">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="dd808-131">Click New.</span></span>
19. <span data-ttu-id="dd808-132">Sisestage number väljale Punktid.</span><span class="sxs-lookup"><span data-stu-id="dd808-132">In the Points field, enter a number.</span></span>
20. <span data-ttu-id="dd808-133">Sisestage väärtus väljale Vastus.</span><span class="sxs-lookup"><span data-stu-id="dd808-133">In the Answer field, type a value.</span></span>
21. <span data-ttu-id="dd808-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dd808-134">Close the page.</span></span>
22. <span data-ttu-id="dd808-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dd808-135">Close the page.</span></span>

## <a name="create-the-question"></a><span data-ttu-id="dd808-136">Küsimuse loomine</span><span class="sxs-lookup"><span data-stu-id="dd808-136">Create the question</span></span>
1. <span data-ttu-id="dd808-137">Avage Küsimustik > Kujundus > Küsimused.</span><span class="sxs-lookup"><span data-stu-id="dd808-137">Go to Questionnaire > Design > Questions.</span></span>
2. <span data-ttu-id="dd808-138">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dd808-138">Click New.</span></span>
3. <span data-ttu-id="dd808-139">Kasutage seotud küsimuste koos grupeerimiseks välja Tüüp.</span><span class="sxs-lookup"><span data-stu-id="dd808-139">Use the Type field to group related questions together.</span></span>
    * <span data-ttu-id="dd808-140">Saate kinniste küsimuste puhul kasutada sisendi tüüpe Märkeruut, Alternatiivne nupp või Liitboks.</span><span class="sxs-lookup"><span data-stu-id="dd808-140">You can use input types of Check box, Alternative button, or Combo box for closed-ended questions.</span></span>  
4. <span data-ttu-id="dd808-141">Valige suvand väljalt Sisendi tüüp.</span><span class="sxs-lookup"><span data-stu-id="dd808-141">In the Input type field, select an option.</span></span>
5. <span data-ttu-id="dd808-142">Sisestage või valige väärtus väljal Vastustegrupp.</span><span class="sxs-lookup"><span data-stu-id="dd808-142">In the Answer group field, enter or select a value.</span></span>
6. <span data-ttu-id="dd808-143">Sisestage väärtus väljale Tekst.</span><span class="sxs-lookup"><span data-stu-id="dd808-143">In the Text field, type a value.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]