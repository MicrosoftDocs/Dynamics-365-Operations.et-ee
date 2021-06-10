---
title: Oskuste konfigureerimine
description: Saate jälgida oma töötajate oskusi rakenduses Dynamics 365 Human Resources. Samuti saate määrata oskused, mida on vaja konkreetse töö jaoks.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076555"
---
# <a name="configure-skills"></a><span data-ttu-id="42517-104">Oskuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="42517-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="42517-105">Saate jälgida oma töötajate oskusi rakenduses Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="42517-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="42517-106">Samuti saate määrata oskused, mida on vaja konkreetse töö jaoks.</span><span class="sxs-lookup"><span data-stu-id="42517-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="42517-107">Oskused, mida saate jälgida, on muu hulgas:</span><span class="sxs-lookup"><span data-stu-id="42517-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="42517-108">Kontrollioskus: oskus teiste töö järele valvata.</span><span class="sxs-lookup"><span data-stu-id="42517-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="42517-109">Juhivõimed: võime juhtida töötajaid ja äridomeene.</span><span class="sxs-lookup"><span data-stu-id="42517-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="42517-110">Kavandamine - Võime vaadata tulevikku, luua kujutlusi ja neid ellu viia.</span><span class="sxs-lookup"><span data-stu-id="42517-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="42517-111">HTML: oskus kirjutada HTML-koodi.</span><span class="sxs-lookup"><span data-stu-id="42517-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="42517-112">Kui te pole oskuste tüüpe ja reitingumudeleid veel seadistanud, peate need enne oskuste loomist lisama.</span><span class="sxs-lookup"><span data-stu-id="42517-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="42517-113">Töötaja oskused saavad sisestada järgmised inimesed:</span><span class="sxs-lookup"><span data-stu-id="42517-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="42517-114">Töötajad saavad enda jaoks töötaja iseteeninduses oskusi sisestada.</span><span class="sxs-lookup"><span data-stu-id="42517-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="42517-115">Need oskused vajavad juhi kinnitust.</span><span class="sxs-lookup"><span data-stu-id="42517-115">These skills require manager approval.</span></span>
- <span data-ttu-id="42517-116">Juhatajad saavad töötajate oskuseid sisestada.</span><span class="sxs-lookup"><span data-stu-id="42517-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="42517-117">Saate luua töövoo, mis kinnitab need oskused automaatselt.</span><span class="sxs-lookup"><span data-stu-id="42517-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="42517-118">Oskuse tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="42517-118">Create a skill type</span></span>

<span data-ttu-id="42517-119">Oskuste tüübid on kategooriad, mille alla kuuluvad üksikud oskused nagu näiteks haldus või müük.</span><span class="sxs-lookup"><span data-stu-id="42517-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="42517-120">**Töötaja arenduse** tööruumis valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="42517-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="42517-121">Valige **Kompetentsi häälestus** jaotises suvand **Oskuse tüübid**.</span><span class="sxs-lookup"><span data-stu-id="42517-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="42517-122">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="42517-122">Select **New**.</span></span>

4. <span data-ttu-id="42517-123">Täitke järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="42517-123">Complete the following fields:</span></span>

   - <span data-ttu-id="42517-124">**Oskuse tüüp**: Sisestage nimi oskuse tüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="42517-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="42517-125">**Kirjeldus**: Sisestage oskuse tüübi jaoks kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="42517-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="42517-126">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="42517-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="42517-127">Hindamismudeli loomine</span><span class="sxs-lookup"><span data-stu-id="42517-127">Create a rating model</span></span>

<span data-ttu-id="42517-128">Hindamismudelid aitavad hinnata isiku oskuste tegelikku taset, taset, mille poole isik peaks püüdlema, või töö jaoks vajaliku oskuse taset.</span><span class="sxs-lookup"><span data-stu-id="42517-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="42517-129">Igale hindamismudelis olevale tasemele määratakse tegur.</span><span class="sxs-lookup"><span data-stu-id="42517-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="42517-130">**Töötaja arenduse** tööruumis valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="42517-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="42517-131">Valige **Kompetentsi häälestus** jaotises suvand **Hindamismudelid**.</span><span class="sxs-lookup"><span data-stu-id="42517-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="42517-132">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="42517-132">Select **New**.</span></span>

4. <span data-ttu-id="42517-133">Täitke järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="42517-133">Complete the following fields:</span></span>

   - <span data-ttu-id="42517-134">**Hinnang**: Sisestage hindamismudeli nimi, näiteks **Oskused**.</span><span class="sxs-lookup"><span data-stu-id="42517-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="42517-135">**Kirjeldus**: Sisestage hindamismudeli kirjeldus, näiteks **Oskuse hinnangud**.</span><span class="sxs-lookup"><span data-stu-id="42517-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="42517-136">Valige **Tasemed** jaotises väärtus **Uus**.</span><span class="sxs-lookup"><span data-stu-id="42517-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="42517-137">Täitke iga lisatava taseme puhul järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="42517-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="42517-138">**Tase**: Sisestage taseme nimi.</span><span class="sxs-lookup"><span data-stu-id="42517-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="42517-139">**Kirjeldus**: Sisestage taseme kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="42517-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="42517-140">**Tegur**: Sisestage teguri väärtus 0-9.</span><span class="sxs-lookup"><span data-stu-id="42517-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="42517-141">Faktorid aitavad normaliseerida erinevaid hindamismudeleid kasutavate oskuste hindeid.</span><span class="sxs-lookup"><span data-stu-id="42517-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="42517-142">Igal tasemel peab olema kordumatu tegur.</span><span class="sxs-lookup"><span data-stu-id="42517-142">Each level must have a unique factor.</span></span> <span data-ttu-id="42517-143">Kõrgemate teguriväärtustega tasemed on hindamismudelis kaalukamad.</span><span class="sxs-lookup"><span data-stu-id="42517-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="42517-144">Jätkake vajadusel tasemete lisamist.</span><span class="sxs-lookup"><span data-stu-id="42517-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="42517-145">Saate sisestada kuni 10 hindamismudeli taset.</span><span class="sxs-lookup"><span data-stu-id="42517-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="42517-146">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="42517-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="42517-147">Oskuse loomine</span><span class="sxs-lookup"><span data-stu-id="42517-147">Create a skill</span></span>

<span data-ttu-id="42517-148">Enne kui saate määrata isikule või tööle oskuse, luua oskuste kaardistamise otsingu või oskuste profiili, peate lehel **Oskused** sisestama teabe oskuse kohta.</span><span class="sxs-lookup"><span data-stu-id="42517-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="42517-149">Iga oskuse puhul saate valida oskuse tüübi ja määramudeli.</span><span class="sxs-lookup"><span data-stu-id="42517-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="42517-150">**Töötaja arenduse** tööruumis valige **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="42517-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="42517-151">Valige **Kompetentsi häälestus** jaotises suvand **Oskused**.</span><span class="sxs-lookup"><span data-stu-id="42517-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="42517-152">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="42517-152">Select **New**.</span></span>

4. <span data-ttu-id="42517-153">Täitke järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="42517-153">Complete the following fields:</span></span>

   - <span data-ttu-id="42517-154">**Oskus**: Sisestage nimi oskuse tüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="42517-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="42517-155">**Kirjeldus**: Sisestage oskuse tüübi jaoks kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="42517-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="42517-156">**Hindamine**: Valige hindamismudel, mida soovite selle oskuse jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="42517-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="42517-157">**Oskuse tüüp**: Valige oskuste tüüpide loendist.</span><span class="sxs-lookup"><span data-stu-id="42517-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="42517-158">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="42517-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="42517-159">Vt ka</span><span class="sxs-lookup"><span data-stu-id="42517-159">See also</span></span>

[<span data-ttu-id="42517-160">Sisestage oskused</span><span class="sxs-lookup"><span data-stu-id="42517-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="42517-161">Oskuste kaardimine</span><span class="sxs-lookup"><span data-stu-id="42517-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]