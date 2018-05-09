--- 
title: "Küsimustike levitamine ajastamise abil"
description: "Küsimustiku planeerimine võimaldab plaanida ja jaotada küsimustikke mitmele vastajale."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e0eb499367cd56e40b57796076d5a54773107df4
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="347c5-103">Küsimustike levitamine ajastamise abil</span><span class="sxs-lookup"><span data-stu-id="347c5-103">Distribute questionnaires using scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="347c5-104">Küsimustiku planeerimine võimaldab plaanida ja jaotada küsimustikke mitmele vastajale.</span><span class="sxs-lookup"><span data-stu-id="347c5-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="347c5-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="347c5-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="347c5-106">Küsimustiku graafiku loomine</span><span class="sxs-lookup"><span data-stu-id="347c5-106">Create a questionnaire schedule</span></span>
1. <span data-ttu-id="347c5-107">Tehke valik Küsimustik > Jaota > Küsimustiku graafikud.</span><span class="sxs-lookup"><span data-stu-id="347c5-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>
2. <span data-ttu-id="347c5-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="347c5-108">Click New.</span></span>
3. <span data-ttu-id="347c5-109">Sisestage väärtus väljale Plaanimine.</span><span class="sxs-lookup"><span data-stu-id="347c5-109">In the Scheduling field, type a value.</span></span>
4. <span data-ttu-id="347c5-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="347c5-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="347c5-111">Määrake graafik olekusse Anonüümne, kui soovite vastused salvestada kujul, kus vastustega ei ole seotud nimesid.</span><span class="sxs-lookup"><span data-stu-id="347c5-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="347c5-112">Anonüümsete tulemuste lubamine tuleb esmalt inimressursside parameetrites seadistada.</span><span class="sxs-lookup"><span data-stu-id="347c5-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  
5. <span data-ttu-id="347c5-113">Valige väljalt Tüüp plaanimise tüüp.</span><span class="sxs-lookup"><span data-stu-id="347c5-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="347c5-114">Selles näites kasutame tüüpi Rahulolu.</span><span class="sxs-lookup"><span data-stu-id="347c5-114">In this example we will use the Satisfaction type.</span></span>
6. <span data-ttu-id="347c5-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="347c5-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="347c5-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="347c5-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="347c5-117">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="347c5-117">In the Date field, enter a date.</span></span>
9. <span data-ttu-id="347c5-118">Laiendage jaotist Töötaja iseteeninduse meil.</span><span class="sxs-lookup"><span data-stu-id="347c5-118">Expand the Email for employee self service section.</span></span>
10. <span data-ttu-id="347c5-119">Sisestage väärtus väljale Teema.</span><span class="sxs-lookup"><span data-stu-id="347c5-119">In the Subject field, type a value.</span></span>
    * <span data-ttu-id="347c5-120">Näide: küsimustik on saadaval</span><span class="sxs-lookup"><span data-stu-id="347c5-120">Example: Questionnaire available</span></span>  
11. <span data-ttu-id="347c5-121">Tippige väljale Tekst meilisõnumi sisu.</span><span class="sxs-lookup"><span data-stu-id="347c5-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="347c5-122">Pange tähele, et süsteemis saab kasutada väärtuste asendamiseks muutujat.</span><span class="sxs-lookup"><span data-stu-id="347c5-122">Note, the variable can be used to substitute values in the system.</span></span>
    * <span data-ttu-id="347c5-123">Näide. Lugupeetud %P%, töötajate tervise küsitluse täitmiseks palun logige sisse töötaja iseteenindusse.</span><span class="sxs-lookup"><span data-stu-id="347c5-123">Example:   Dear %P%,  Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="347c5-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="347c5-124">Contoso</span></span>  
12. <span data-ttu-id="347c5-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="347c5-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="347c5-126">Kasutage seadistuse üksikasju vastamiseks küsimustik(e) valimiseks ja päringuid vastajate valimiseks.</span><span class="sxs-lookup"><span data-stu-id="347c5-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>
1. <span data-ttu-id="347c5-127">Klõpsake valikut Seadistuse üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="347c5-127">Click Setup details.</span></span>
2. <span data-ttu-id="347c5-128">Valige loendist päring, mille abil süsteemist küsimustikule vastajaid leida.</span><span class="sxs-lookup"><span data-stu-id="347c5-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>
    * <span data-ttu-id="347c5-129">Näide: töötajad</span><span class="sxs-lookup"><span data-stu-id="347c5-129">Example: Workers</span></span>  
3. <span data-ttu-id="347c5-130">Klõpsake valikut Kuva või muuda päringut, et kindlaid inimesi valida, või kohandage päringut inimeste leidmiseks, kes vastavad teatud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="347c5-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>
    * <span data-ttu-id="347c5-131">Pange tähele, et kõik vastajad peavad olema süsteemi kasutajad.</span><span class="sxs-lookup"><span data-stu-id="347c5-131">Note that all respondents must also be users in the system.</span></span>  
4. <span data-ttu-id="347c5-132">Märkige loendis rida nimega Person</span><span class="sxs-lookup"><span data-stu-id="347c5-132">In the list, mark the row for Person</span></span>
5. <span data-ttu-id="347c5-133">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="347c5-133">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="347c5-134">Valige Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="347c5-134">Select Julia Funderburk</span></span>  
6. <span data-ttu-id="347c5-135">Valige loendist Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="347c5-135">In the list, select Julia Funderburk</span></span>
7. <span data-ttu-id="347c5-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="347c5-136">Click OK.</span></span>
8. <span data-ttu-id="347c5-137">Klõpsake vahekaarti Küsimustikud.</span><span class="sxs-lookup"><span data-stu-id="347c5-137">Click the Questionnaires tab.</span></span>
9. <span data-ttu-id="347c5-138">Laiendage puul valikut „sõlm küsimustiku tüübi Rahuoluküsitlus kohta”.</span><span class="sxs-lookup"><span data-stu-id="347c5-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>
10. <span data-ttu-id="347c5-139">Märkige puul valik Töötajate tervise hindamine.</span><span class="sxs-lookup"><span data-stu-id="347c5-139">In the tree, check 'Workforce Health Assessment'.</span></span>
11. <span data-ttu-id="347c5-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="347c5-140">Click OK.</span></span>
12. <span data-ttu-id="347c5-141">Klõpsake valikut Planeeritud vastamisseanss.</span><span class="sxs-lookup"><span data-stu-id="347c5-141">Click Planned answer session.</span></span>
    * <span data-ttu-id="347c5-142">Pange tähele, et Planeeritud vastamisseansid on loodud iga valitud/päringuga leitud kasutaja jaoks.</span><span class="sxs-lookup"><span data-stu-id="347c5-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  
13. <span data-ttu-id="347c5-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="347c5-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="347c5-144">Küsimustiku graafiku käivitamine küsimustiku vastajatele kättesaadavaks muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="347c5-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>
1. <span data-ttu-id="347c5-145">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="347c5-145">Click Functions.</span></span>
2. <span data-ttu-id="347c5-146">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="347c5-146">Click Start.</span></span>
3. <span data-ttu-id="347c5-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="347c5-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="347c5-148">Meili saatmine vastajate teavitamiseks saadaolevast küsimustikust.</span><span class="sxs-lookup"><span data-stu-id="347c5-148">Send the email to inform respondents of the available questionnaire.</span></span>
1. <span data-ttu-id="347c5-149">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="347c5-149">Click Functions.</span></span>
2. <span data-ttu-id="347c5-150">Klõpsake valikut Saada meil.</span><span class="sxs-lookup"><span data-stu-id="347c5-150">Click Send email.</span></span>
3. <span data-ttu-id="347c5-151">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="347c5-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="347c5-152">Kasutage Valikut Planeeritud vastamisseansid, et jälgida, kes peab küsimustiku täitma.</span><span class="sxs-lookup"><span data-stu-id="347c5-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>
1. <span data-ttu-id="347c5-153">Klõpsake valikut Planeeritud vastamisseanss.</span><span class="sxs-lookup"><span data-stu-id="347c5-153">Click Planned answer session.</span></span>
    * <span data-ttu-id="347c5-154">Kustutage kõik ülejäänud planeeritud vastamisseansid, kui olete valmis planeeritud seansi lõpetamiseks.</span><span class="sxs-lookup"><span data-stu-id="347c5-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  
2. <span data-ttu-id="347c5-155">Klõpsake  Kustuta.</span><span class="sxs-lookup"><span data-stu-id="347c5-155">Click Delete.</span></span>
3. <span data-ttu-id="347c5-156">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="347c5-156">Click Yes.</span></span>
4. <span data-ttu-id="347c5-157">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="347c5-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="347c5-158">Lõpetage graafik, kui kõik vastajad on küsimustiku täitnud ja/või kõik järelejäänud plaanitud vastuseseansid on kustutatud.</span><span class="sxs-lookup"><span data-stu-id="347c5-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>
1. <span data-ttu-id="347c5-159">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="347c5-159">Click Functions.</span></span>
2. <span data-ttu-id="347c5-160">Klõpsake suvandit Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="347c5-160">Click End.</span></span>
3. <span data-ttu-id="347c5-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="347c5-161">Click OK.</span></span>


