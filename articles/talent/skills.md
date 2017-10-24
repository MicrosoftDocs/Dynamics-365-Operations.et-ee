---
title: "Tööjõu oskuste joondamine ärivajadustele"
description: "Saate jälgida oskusi, mis võivad töötajatel, kandidaatidel või kontaktisikutel olla, et oma rolli tõhusalt täita. Samuti saate määrata oskused, mida on vaja konkreetse töö jaoks."
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2b76064049daccdcdff04c9f2fdde9a8b9c9e8e0
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="5a009-104">Tööjõu oskuste joondamine ärivajadustele</span><span class="sxs-lookup"><span data-stu-id="5a009-104">Align workforce skills with business needs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="5a009-105">Saate jälgida oskusi, mis võivad töötajatel, kandidaatidel või kontaktisikutel olla, et oma rolli tõhusalt täita.</span><span class="sxs-lookup"><span data-stu-id="5a009-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="5a009-106">Samuti saate määrata oskused, mida on vaja konkreetse töö jaoks.</span><span class="sxs-lookup"><span data-stu-id="5a009-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="5a009-107">Oskused, mida saate jälgida, on muu hulgas järgmised.</span><span class="sxs-lookup"><span data-stu-id="5a009-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="5a009-108">Kontrollioskus: oskus teiste töö järele valvata.</span><span class="sxs-lookup"><span data-stu-id="5a009-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="5a009-109">Juhivõimed: võime juhtida töötajaid ja äridomeene.</span><span class="sxs-lookup"><span data-stu-id="5a009-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="5a009-110">Kavandamine: võime vaadata tulevikku, luua kujutlusi ja neid ellu viia.</span><span class="sxs-lookup"><span data-stu-id="5a009-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="5a009-111">HTML: oskus kirjutada HTML-koodi.</span><span class="sxs-lookup"><span data-stu-id="5a009-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="5a009-112">Enne kui saate määrata isikule või tööle oskuse, luua oskuste kaardistamise otsingu või oskuste profiili, peate lehel **Oskused** sisestama teabe oskuste kohta.</span><span class="sxs-lookup"><span data-stu-id="5a009-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="5a009-113">Iga oskuse puhul saate valida oskuse tüübi ja määramudeli.</span><span class="sxs-lookup"><span data-stu-id="5a009-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="5a009-114">Reitingumudelid</span><span class="sxs-lookup"><span data-stu-id="5a009-114">Rating models</span></span>
<span data-ttu-id="5a009-115">Määramudelid aitavad hinnata isiku oskuste tegelikku taset, taset, mille poole isik peaks püüdlema, või töö jaoks vajaliku oskuse taset.</span><span class="sxs-lookup"><span data-stu-id="5a009-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="5a009-116">Saate sisestada kuni 10 hindamismudeli taset.</span><span class="sxs-lookup"><span data-stu-id="5a009-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="5a009-117">Igale hindamismudelis olevale tasemele määratakse tegur.</span><span class="sxs-lookup"><span data-stu-id="5a009-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="5a009-118">Teguri väärtust kasutatakse erinevaid hindamismudeleid kasutavate oskusehinnangute ühtlustamiseks.</span><span class="sxs-lookup"><span data-stu-id="5a009-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="5a009-119">Tegur peab olema arv 0–9 ja igal tasemel peab olema üks kordumatu tegur.</span><span class="sxs-lookup"><span data-stu-id="5a009-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="5a009-120">Kõrgemate teguriväärtustega tasemed on hindamismudelis kaalukamad.</span><span class="sxs-lookup"><span data-stu-id="5a009-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="5a009-121">Tööoskuste määramine</span><span class="sxs-lookup"><span data-stu-id="5a009-121">Specify job skills</span></span>
<span data-ttu-id="5a009-122">Töö kohta teabe sisestamisel saate määrata oskused, mis isikul peaks töö jaoks vajaliku töö tegemiseks olema.</span><span class="sxs-lookup"><span data-stu-id="5a009-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="5a009-123">Lisaks saate iga oskuse jaoks soovitud taseme, aga ka oskuse tähtsusastme määrata.</span><span class="sxs-lookup"><span data-stu-id="5a009-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="5a009-124">Erinevate ametikohtade puhul võib sama oskus olla nõutav erisugustel tähtsusastmetel.</span><span class="sxs-lookup"><span data-stu-id="5a009-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="5a009-125">Töötajate, kandidaatide või kontaktisikute oskuste sisestamine</span><span class="sxs-lookup"><span data-stu-id="5a009-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="5a009-126">Saate sisestada töötajate, kandidaatide või kontaktisikute oodatavad oskused või tegelikud oskused.</span><span class="sxs-lookup"><span data-stu-id="5a009-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="5a009-127">Oodatav oskus on oskus, mille isik kavatseb omandada.</span><span class="sxs-lookup"><span data-stu-id="5a009-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="5a009-128">Tegelik oskus on oskus, mis isikul praegu on.</span><span class="sxs-lookup"><span data-stu-id="5a009-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="5a009-129"> Oskuste kaardistamise ja oskuste kaardistamise profiilid</span><span class="sxs-lookup"><span data-stu-id="5a009-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="5a009-130">Saate luua oskuste kaardistamise otsingu, et leida töötaja, kandidaat või kontaktisik, kes on teatud tüüpi ülesande tegemiseks kvalifitseeritud.</span><span class="sxs-lookup"><span data-stu-id="5a009-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="5a009-131">Oskuste kaardistamise otsingud otsivad oskuste, hariduse, sertifikaatide, vastutavate positsioonide ja projekti läbiviimise kogemuse põhjal ning annavad sisestatud kriteeriumidele vastavad tulemused.</span><span class="sxs-lookup"><span data-stu-id="5a009-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return a results that match the criteria entered.</span></span>  <span data-ttu-id="5a009-132">Näiteks võib olla kasulik teada, millised töötajad teie organisatsioonis on teeninud oma CPA.</span><span class="sxs-lookup"><span data-stu-id="5a009-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="5a009-133">Oskuste kaardistamise profiilid võimaldavad leida praegused töötajad või kandidaadid, kellel on kvalifikatsioonid, mis vastavad otseselt ärivajadustele.</span><span class="sxs-lookup"><span data-stu-id="5a009-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="5a009-134">Näiteks võiksite oma organisatsioonis oleva avatud ametikoha jaoks luua oskuste kaardistamise profiili.</span><span class="sxs-lookup"><span data-stu-id="5a009-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="5a009-135">Konkreetse töö jaoks profiili luues ning kopeerides oskused, hariduse ja serdid sellelt töölt profiilile, saate kiiresti otsida töötajaid, kandidaate ja kontaktisikuid, kes vastavad ühele või mitmele profiili sisestatud kriteeriumile, ning kuvada loendi kandidaatidest, kelle oskused ühtivad kõige enam töö jaoks nõutavate oskustega.</span><span class="sxs-lookup"><span data-stu-id="5a009-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

><span data-ttu-id="5a009-136">**Märkus.** Oskuste kaardistamise tulemuste loendis saab kuvada või oskuste profiilile lisada vaid need töötajad, kandidaadid ja kontaktisikud, kes on lisatud oskuste kaardistamise otsingusse.</span><span class="sxs-lookup"><span data-stu-id="5a009-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="5a009-137">Töötaja, kandidaadi või kontaktisiku lisamiseks oskuste kaardistamise otsingusse valige suvandi **Kaasa oskuste kaardistamisse** sätteks Jah järgmistel lehtedel.</span><span class="sxs-lookup"><span data-stu-id="5a009-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>

> + <span data-ttu-id="5a009-138">Töötaja</span><span class="sxs-lookup"><span data-stu-id="5a009-138">Worker</span></span>
> + <span data-ttu-id="5a009-139">Töötaja</span><span class="sxs-lookup"><span data-stu-id="5a009-139">Employee</span></span>
> + <span data-ttu-id="5a009-140">Kandidaat</span><span class="sxs-lookup"><span data-stu-id="5a009-140">Applicant</span></span>
> + <span data-ttu-id="5a009-141">Kontaktid</span><span class="sxs-lookup"><span data-stu-id="5a009-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="5a009-142">Oskuste vahe analüüs ja oskuste profiili analüüs</span><span class="sxs-lookup"><span data-stu-id="5a009-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="5a009-143">Saate luua oskuste profiili analüüsi, et vaadata töötaja, kandidaadi või kontaktisiku pädevuste loendit alates kindlast kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="5a009-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="5a009-144">Oskuste vahe analüüsiga saate võrrelda isiku oskusi ja kindla töö jaoks vajalikke oskusi.</span><span class="sxs-lookup"><span data-stu-id="5a009-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="see-also"></a><span data-ttu-id="5a009-145">Vt ka</span><span class="sxs-lookup"><span data-stu-id="5a009-145">See also</span></span>
--------

[<span data-ttu-id="5a009-146">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="5a009-146">Human resources</span></span>](index.md)




