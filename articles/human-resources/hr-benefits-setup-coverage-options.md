---
title: Katvuse suvandite loomine
description: Katvussuvandid rakenduses Microsoft Dynamics 365 Human Resources on kasutaja valitud soodustuse plaani või programmi katvuse tasemed.
author: andreabichsel
manager: tfehr
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2e1d5fc80d93e41626da8eb5bdf8f389fb0bd531
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5466178"
---
# <a name="create-coverage-options"></a><span data-ttu-id="15681-103">Katvuse suvandite loomine</span><span class="sxs-lookup"><span data-stu-id="15681-103">Create coverage options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="15681-104">Katvussuvandid rakenduses Microsoft Dynamics 365 Human Resources on kasutaja valitud soodustuse plaani või programmi katvuse tasemed.</span><span class="sxs-lookup"><span data-stu-id="15681-104">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program.</span></span> <span data-ttu-id="15681-105">Näiteks võivad katvussuvandid hõlmata suvandit **Ainult töövõtja** meditsiiniplaani jaoks või suvandit **2 × palk** elukindlustuse plaani jaoks.</span><span class="sxs-lookup"><span data-stu-id="15681-105">For example, coverage options could include **Employee Only** for a medical plan, or **2x Salary** for a life insurance plan.</span></span> <span data-ttu-id="15681-106">Kui see on määratletud, saate soodustuse kindlustussuvandeid uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="15681-106">Once defined, you can reuse benefit coverage options.</span></span> <span data-ttu-id="15681-107">Saate siduda suvandi ühe või mitme plaaniga.</span><span class="sxs-lookup"><span data-stu-id="15681-107">You can associate an option with one or more plans.</span></span>

<span data-ttu-id="15681-108">Kui katvuse valikud on määratud, lisage katvuse valikud soodustuse plaani tüübile.</span><span class="sxs-lookup"><span data-stu-id="15681-108">After you define coverage options, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="15681-109">Plaani tüüp seostatakse seejärel soodustuse plaani või programmiga.</span><span class="sxs-lookup"><span data-stu-id="15681-109">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="15681-110">Plaani tüübiga seostatud katvuse valikud on saadaval kõigile selle plaani tüübiga loodud plaanidele.</span><span class="sxs-lookup"><span data-stu-id="15681-110">Coverage options that are associated with a plan type are available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="15681-111">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Katvuse valikud**.</span><span class="sxs-lookup"><span data-stu-id="15681-111">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="15681-112">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="15681-112">Select **New**.</span></span>

3. <span data-ttu-id="15681-113">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="15681-113">Specify values for the following fields:</span></span>

   | <span data-ttu-id="15681-114">Väli</span><span class="sxs-lookup"><span data-stu-id="15681-114">Field</span></span> | <span data-ttu-id="15681-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="15681-115">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="15681-116">**Katvuse valik**</span><span class="sxs-lookup"><span data-stu-id="15681-116">**Coverage option**</span></span> | <span data-ttu-id="15681-117">Kordumatu katvuse valiku nimi.</span><span class="sxs-lookup"><span data-stu-id="15681-117">A unique coverage option name.</span></span> |
   | <span data-ttu-id="15681-118">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="15681-118">**Description**</span></span> | <span data-ttu-id="15681-119">Katvuse valiku kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="15681-119">A description of the coverage option.</span></span> |
   | <span data-ttu-id="15681-120">**Planeerimise kood**</span><span class="sxs-lookup"><span data-stu-id="15681-120">**Coverage code**</span></span> | <span data-ttu-id="15681-121">Katvuse koodid määravad minimaalsed ja maksimaalsed summad iga sobiva kaetud isiku tüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="15681-121">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="15681-122">Katvuse kood näitab, kes on kaetud või plaani tüübile lubatud katvuse summa.</span><span class="sxs-lookup"><span data-stu-id="15681-122">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="15681-123">Saate väljendada katvuse summat summana dollarites või protsendina.</span><span class="sxs-lookup"><span data-stu-id="15681-123">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="15681-124">Näide:</span><span class="sxs-lookup"><span data-stu-id="15681-124">For example:</span></span></br></br><span data-ttu-id="15681-125">- **EMP+1** – kvalifitseerumiseks peab töövõtjal olema üks sõltuv isik valitud (kui valitud on rohkem kui üks, siis need enam ei kvalifitseeru).</span><span class="sxs-lookup"><span data-stu-id="15681-125">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="15681-126">- **EMP+perekond** – kvalifitseerumiseks peab töövõtjal olema vähemalt kaks sõltuvat isikut valitud.</span><span class="sxs-lookup"><span data-stu-id="15681-126">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="15681-127">**Maksimaalne arv**</span><span class="sxs-lookup"><span data-stu-id="15681-127">**Maximum number**</span></span> | <span data-ttu-id="15681-128">Maksimaalne sõltuvate isikute arv.</span><span class="sxs-lookup"><span data-stu-id="15681-128">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="15681-129">**Olek**</span><span class="sxs-lookup"><span data-stu-id="15681-129">**Status**</span></span> | <span data-ttu-id="15681-130">Katvuse valiku olek.</span><span class="sxs-lookup"><span data-stu-id="15681-130">The status of the coverage option.</span></span> <span data-ttu-id="15681-131">Kui katvuse valiku olek on seatud passiivseks, ei saa plaani tüüpides katvuse valikut valida.</span><span class="sxs-lookup"><span data-stu-id="15681-131">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="15681-132">**Protsent**</span><span class="sxs-lookup"><span data-stu-id="15681-132">**Percent**</span></span> | <span data-ttu-id="15681-133">Protsendi summa.</span><span class="sxs-lookup"><span data-stu-id="15681-133">The percent amount.</span></span> <span data-ttu-id="15681-134">See väli on aktiivne ainult juhul, kui väljal Katvuse kood on valitud % × palk.</span><span class="sxs-lookup"><span data-stu-id="15681-134">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="15681-135">**Jagaja**</span><span class="sxs-lookup"><span data-stu-id="15681-135">**Divisor**</span></span> | <span data-ttu-id="15681-136">Jagaja, mida kasutatakse arvutamisel, kui valite katvuse koodi % × palk.</span><span class="sxs-lookup"><span data-stu-id="15681-136">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="15681-137">**Miinimumprotsent**</span><span class="sxs-lookup"><span data-stu-id="15681-137">**Percent minimum**</span></span> | <span data-ttu-id="15681-138">Minimaalne protsent, kui valite katvuse koodi Protsent.</span><span class="sxs-lookup"><span data-stu-id="15681-138">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="15681-139">**Maksimumprotsent**</span><span class="sxs-lookup"><span data-stu-id="15681-139">**Percent maximum**</span></span> | <span data-ttu-id="15681-140">Maksimaalne protsent, kui valite katvuse koodi Protsent.</span><span class="sxs-lookup"><span data-stu-id="15681-140">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="15681-141">Jaotises **Isikliku kontakti sobivuse suvandid** lisage igale katvuse valikule sobiv isiklike kontaktide sobivuse suvand.</span><span class="sxs-lookup"><span data-stu-id="15681-141">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="15681-142">Vahekaardil **Iseteenindus** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="15681-142">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="15681-143">Väli</span><span class="sxs-lookup"><span data-stu-id="15681-143">Field</span></span> | <span data-ttu-id="15681-144">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="15681-144">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="15681-145">**Luba töövõtja panuse summa määramine**</span><span class="sxs-lookup"><span data-stu-id="15681-145">**Allow employee contribution amount**</span></span> | <span data-ttu-id="15681-146">Määrab, kas lubada töötajatel soodustuste valimisel muuta soodustuste osamakse summat.</span><span class="sxs-lookup"><span data-stu-id="15681-146">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="15681-147">Kui märgite selle ruudu, arvutab süsteem hüvitise plaani parameetrid, võttes aluseks osamakse summa, mille töötaja sisestab soodustuste iseteeninduses.</span><span class="sxs-lookup"><span data-stu-id="15681-147">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="15681-148">**Luba töövõtja kindlustussumma määramine**</span><span class="sxs-lookup"><span data-stu-id="15681-148">**Allow employee coverage amount**</span></span> | <span data-ttu-id="15681-149">Määrab, kas lubada töötajatel soodustuste valimisel muuta soodustuste katvuse summat.</span><span class="sxs-lookup"><span data-stu-id="15681-149">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="15681-150">Kui märgite selle ruudu, arvutab süsteem hüvitise plaani parameetrid, võttes aluseks katvuse summa, mille töötaja sisestab töövõtja iseteeninduses.</span><span class="sxs-lookup"><span data-stu-id="15681-150">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="15681-151">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="15681-151">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]