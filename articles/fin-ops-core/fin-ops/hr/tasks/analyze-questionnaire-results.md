---
title: Küsimustiku tulemuste analüüsimine
description: Küsimustiku statistikat saab kasutada keskmiste, summade ja protsentide arvutamiseks demograafiliste andmete põhjal.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d8f9c2fcf0be117f8fcde5113c0d42f11786679
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177462"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="e02bb-103">Küsimustiku tulemuste analüüsimine</span><span class="sxs-lookup"><span data-stu-id="e02bb-103">Analyzing questionnaire results</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e02bb-104">Küsimustiku statistikat saab kasutada keskmiste, summade ja protsentide arvutamiseks demograafiliste andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="e02bb-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="e02bb-105">Selle protseduuri alustamiseks avage Küsimustik > Tulemuste kuvamine ja analüüsimine > Küsimustiku statistika.</span><span class="sxs-lookup"><span data-stu-id="e02bb-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="e02bb-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="e02bb-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="e02bb-107">Küsimustiku statistika kirje loomine</span><span class="sxs-lookup"><span data-stu-id="e02bb-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="e02bb-108">Avage Küsimustiku statistika.</span><span class="sxs-lookup"><span data-stu-id="e02bb-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="e02bb-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e02bb-109">Click New.</span></span>
3. <span data-ttu-id="e02bb-110">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e02bb-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="e02bb-111">Sisestage väärtus väljale Statistika.</span><span class="sxs-lookup"><span data-stu-id="e02bb-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="e02bb-112">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e02bb-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e02bb-113">Klõpsake väljal Küsimustik otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e02bb-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e02bb-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e02bb-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e02bb-115">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="e02bb-115">Click the General tab.</span></span>
    * <span data-ttu-id="e02bb-116">Valige, kas soovite kaasata anonüümseid tulemusi või tulemusi töötajatelt, kontaktidelt ja kandidaatidelt.</span><span class="sxs-lookup"><span data-stu-id="e02bb-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="e02bb-117">Valige või tühjendage märkeruut Töötaja.</span><span class="sxs-lookup"><span data-stu-id="e02bb-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="e02bb-118">Kui vaatate staaži või vanuse tulemusi, määrake vahemikud, mida sooviksite kasutada tulemuste grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="e02bb-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="e02bb-119">Vanusevahemiku puhul 5 sisestamine grupeerib tulemused viieaastaste vanusevahemike põhjal.</span><span class="sxs-lookup"><span data-stu-id="e02bb-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="e02bb-120">Sisestage number väljale Vanus.</span><span class="sxs-lookup"><span data-stu-id="e02bb-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="e02bb-121">Valige, kas soovite käitada arvutamist kogu küsimustiku, iga tulemustegrupi, iga küsimuse või iga küsimuse rea puhul.</span><span class="sxs-lookup"><span data-stu-id="e02bb-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="e02bb-122">Valige, kuidas soovite tulemused grupeerida.</span><span class="sxs-lookup"><span data-stu-id="e02bb-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="e02bb-123">Näiteks kui arvutate keskmised punktid küsimuse kohta, võite soovida näha küsimusi tulemusegrupi järgi grupeerituna.</span><span class="sxs-lookup"><span data-stu-id="e02bb-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="e02bb-124">Valige andmed, mis arvutamisel aluseks võtta.</span><span class="sxs-lookup"><span data-stu-id="e02bb-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="e02bb-125">Näiteks kui soovite vaadata töötajate hulgas saadud küsimustiku keskmist protsenti ja töötajate hulgas saadud punktide keskmist arvu.</span><span class="sxs-lookup"><span data-stu-id="e02bb-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="e02bb-126">Klõpsake vahekaarti Vahemik.</span><span class="sxs-lookup"><span data-stu-id="e02bb-126">Click the Range tab.</span></span>
    * <span data-ttu-id="e02bb-127">Kasutage tulemikomplekti piiramiseks ainult neid vahemikke, mis vahemiku kriteeriumidele vastavad.</span><span class="sxs-lookup"><span data-stu-id="e02bb-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="e02bb-128">Klõpsake vahekaarti Grupeerimisalus.</span><span class="sxs-lookup"><span data-stu-id="e02bb-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="e02bb-129">Kasutage tulemuste kuvamise viisi määramiseks grupeerimisi.</span><span class="sxs-lookup"><span data-stu-id="e02bb-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="e02bb-130">Näiteks grupeerige tulemused esmalt soo, seejärel vanuse järgi.</span><span class="sxs-lookup"><span data-stu-id="e02bb-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="e02bb-131">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e02bb-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e02bb-132">Teisaldage grupeerimised valitud poolele ja pange need soovitud järjekorda.</span><span class="sxs-lookup"><span data-stu-id="e02bb-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="e02bb-133">Statistika arvutamine</span><span class="sxs-lookup"><span data-stu-id="e02bb-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="e02bb-134">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="e02bb-134">Click Execute.</span></span>
    * <span data-ttu-id="e02bb-135">Valige, millist arvutusfunktsiooni soovite tulemuste puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="e02bb-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="e02bb-136">Näiteks arvutage küsimustiku keskmised protsendid valitud grupeerimiste puhul või valitud grupeerimiste tulemustegrupi punktid kokku.</span><span class="sxs-lookup"><span data-stu-id="e02bb-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="e02bb-137">Märkige või tühjendage ruut Kustuta varasemad otsingud.</span><span class="sxs-lookup"><span data-stu-id="e02bb-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="e02bb-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e02bb-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="e02bb-139">Küsimustiku statistika käituse tulemuste kuvamine.</span><span class="sxs-lookup"><span data-stu-id="e02bb-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="e02bb-140">Klõpsake vahekaarti Tulemus.</span><span class="sxs-lookup"><span data-stu-id="e02bb-140">Click Result.</span></span>
2. <span data-ttu-id="e02bb-141">Klõpsake vahekaarti Tulemus.</span><span class="sxs-lookup"><span data-stu-id="e02bb-141">Click Result.</span></span>
3. <span data-ttu-id="e02bb-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e02bb-142">Close the page.</span></span>
