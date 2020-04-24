---
title: Registreerimise sobivuse töötlemine
description: Selles artiklis selgitatakse, kuidas käivitada registreerimise sobivuse töötlemist.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1d978982213e713e362798c49aa57e6dc8b7a862
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2020
ms.locfileid: "3230012"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="7b51c-103">Registreerimise sobivuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="7b51c-103">Process enrollment eligibility</span></span>

<span data-ttu-id="7b51c-104">Selles artiklis selgitatakse, kuidas käivitada registreerimise sobivuse töötlemist.</span><span class="sxs-lookup"><span data-stu-id="7b51c-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="7b51c-105">Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Registreerimise sobivuse töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="7b51c-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="7b51c-106">Dialoogiaknas **Soodustuse registreerimise sobivuse protsessi käitamine** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="7b51c-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="7b51c-107">Väli</span><span class="sxs-lookup"><span data-stu-id="7b51c-107">Field</span></span> | <span data-ttu-id="7b51c-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="7b51c-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7b51c-109">**Registreerimisperiood**</span><span class="sxs-lookup"><span data-stu-id="7b51c-109">**Enrollment period**</span></span> | <span data-ttu-id="7b51c-110">Registreerimisperiood, mille jaoks registreerimise sobilikkust töödelda.</span><span class="sxs-lookup"><span data-stu-id="7b51c-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="7b51c-111">**Juriidiline isik**</span><span class="sxs-lookup"><span data-stu-id="7b51c-111">**Legal entity**</span></span> | <span data-ttu-id="7b51c-112">Juriidiline isik, mille jaoks registreerimise sobilikkust töödelda.</span><span class="sxs-lookup"><span data-stu-id="7b51c-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="7b51c-113">**Töötaja**</span><span class="sxs-lookup"><span data-stu-id="7b51c-113">**Worker**</span></span> | <span data-ttu-id="7b51c-114">Töötaja, kelle jaoks registreerimise sobilikkust töödelda.</span><span class="sxs-lookup"><span data-stu-id="7b51c-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="7b51c-115">Kui jätate selle välja tühjaks, töödeldakse registreerimise sobilikkust kõigi töötajate puhul.</span><span class="sxs-lookup"><span data-stu-id="7b51c-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="7b51c-116">**Soodustusplaan**</span><span class="sxs-lookup"><span data-stu-id="7b51c-116">**Benefit plan**</span></span> | <span data-ttu-id="7b51c-117">Soodustuse plaan, mille jaoks registreerimise sobilikkust töödelda.</span><span class="sxs-lookup"><span data-stu-id="7b51c-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="7b51c-118">Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="7b51c-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="7b51c-119">Sisestage teavet protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="7b51c-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="7b51c-120">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b51c-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="7b51c-121">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b51c-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="7b51c-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b51c-122">Select **OK**.</span></span> <span data-ttu-id="7b51c-123">Protsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="7b51c-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="7b51c-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b51c-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="7b51c-125">Protsessi tulemuste kuvamine</span><span class="sxs-lookup"><span data-stu-id="7b51c-125">View Process Results</span></span>

<span data-ttu-id="7b51c-126">Selles artiklis selgitatakse, kuidas kuvada sobivuse töötlemise tulemusi.</span><span class="sxs-lookup"><span data-stu-id="7b51c-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="7b51c-127">Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Protsessi tulemused**.</span><span class="sxs-lookup"><span data-stu-id="7b51c-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="7b51c-128">Vormil **Protsessi tulemused** on määratud järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="7b51c-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="7b51c-129">Field</span><span class="sxs-lookup"><span data-stu-id="7b51c-129">Field</span></span> | <span data-ttu-id="7b51c-130">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="7b51c-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7b51c-131">**Protsessi ID**</span><span class="sxs-lookup"><span data-stu-id="7b51c-131">**Process ID**</span></span> | <span data-ttu-id="7b51c-132">Töötaja, juriidilise isiku ja protsessi käituse kombinatsiooni ainuidentifikaator.</span><span class="sxs-lookup"><span data-stu-id="7b51c-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="7b51c-133">**Protsessi tüüp**</span><span class="sxs-lookup"><span data-stu-id="7b51c-133">**Process type**</span></span> | <span data-ttu-id="7b51c-134">See tuvastab käivitatud protsessi.</span><span class="sxs-lookup"><span data-stu-id="7b51c-134">This identifies the process that was run.</span></span> <span data-ttu-id="7b51c-135">Näide: registreerimine.</span><span class="sxs-lookup"><span data-stu-id="7b51c-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="7b51c-136">**Ajatempel**</span><span class="sxs-lookup"><span data-stu-id="7b51c-136">**Time stamp**</span></span> | <span data-ttu-id="7b51c-137">Sobivuse töötlemise kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="7b51c-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="7b51c-138">**Juriidiline isik**</span><span class="sxs-lookup"><span data-stu-id="7b51c-138">**Legal entity**</span></span> | <span data-ttu-id="7b51c-139">Registreerimise käigus määratud juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="7b51c-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="7b51c-140">**Töötaja**</span><span class="sxs-lookup"><span data-stu-id="7b51c-140">**Worker**</span></span> | <span data-ttu-id="7b51c-141">Töödeldav töötaja.</span><span class="sxs-lookup"><span data-stu-id="7b51c-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="7b51c-142">\*\*Plaan</span><span class="sxs-lookup"><span data-stu-id="7b51c-142">\*\*Plan</span></span> | <span data-ttu-id="7b51c-143">See soodustusplaan, mille jaoks registreeriti.</span><span class="sxs-lookup"><span data-stu-id="7b51c-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="7b51c-144">**Sobivusreegel**</span><span class="sxs-lookup"><span data-stu-id="7b51c-144">**Eligibility rule**</span></span> | <span data-ttu-id="7b51c-145">Töödeldud sobivusreegel.</span><span class="sxs-lookup"><span data-stu-id="7b51c-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="7b51c-146">Kui enne sobivuse töötlemist ilmnes tõrge, on see tühi.</span><span class="sxs-lookup"><span data-stu-id="7b51c-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="7b51c-147">Näiteks: kui töötaja jaoks pole kompensatsiooni määratud, siis sobivuse töötlemist ei käivitata ja see väli jäetakse tühjaks.</span><span class="sxs-lookup"><span data-stu-id="7b51c-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="7b51c-148">**Tulemi olek**</span><span class="sxs-lookup"><span data-stu-id="7b51c-148">**Result status**</span></span> | <span data-ttu-id="7b51c-149">See on Sobilik või Sobimatu.</span><span class="sxs-lookup"><span data-stu-id="7b51c-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="7b51c-150">Tulemuse olek on Sobimatu, kui töötaja ei vastanud sobivusreegli kriteeriumidele, kui töötaja kohta puudub nõutav teave (nt maksesagedus või põhipalk) või kui puudub teave soodustusplaani kohta, mis takistab töötajate registreerimist.</span><span class="sxs-lookup"><span data-stu-id="7b51c-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="7b51c-151">**Tulemusteade**</span><span class="sxs-lookup"><span data-stu-id="7b51c-151">**Result message**</span></span> | <span data-ttu-id="7b51c-152">Näitab, miks töötaja on soodustusplaani jaoks sobimatu või kui sobivusreegel on edastatud.</span><span class="sxs-lookup"><span data-stu-id="7b51c-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

