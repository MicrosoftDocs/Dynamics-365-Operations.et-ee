---
title: Katvussuvandite loomine
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 27b43d858a92beac526ac0fc40b544649ef658b0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008696"
---
# <a name="create-coverage-options"></a><span data-ttu-id="9da80-102">Katvussuvandite loomine</span><span class="sxs-lookup"><span data-stu-id="9da80-102">Create coverage options</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="9da80-103">Katvussuvandid rakenduses Microsoft Dynamics 365 Human Resources on kasutaja valitud soodustuse plaani või programmi katvuse tasemed, nagu meditsiiniplaani jaoks suvand Ainult töövõtja või elukindlustuse plaani jaoks 2 × palk.</span><span class="sxs-lookup"><span data-stu-id="9da80-103">Coverage options in Microsoft Dynamics 365 Human Resources are levels of coverage for a participant's election in a benefit plan or program, such as Employee Only for a medical plan, or 2x Salary for a life insurance plan.</span></span> <span data-ttu-id="9da80-104">Kui see on määratletud, siis on soodustuse katvuse valikud uuesti kasutatavad ja saate siduda valiku ühe või mitme plaaniga.</span><span class="sxs-lookup"><span data-stu-id="9da80-104">Once defined, benefit coverage options are re-usable and you can associate an option with one or more plans.</span></span>

<span data-ttu-id="9da80-105">Kui katvuse valikud on määratud, lisage katvuse valikud soodustuse plaani tüübile.</span><span class="sxs-lookup"><span data-stu-id="9da80-105">Once the coverage options are defined, attach the coverage options to a benefit plan type.</span></span> <span data-ttu-id="9da80-106">Plaani tüüp seostatakse seejärel soodustuse plaani või programmiga.</span><span class="sxs-lookup"><span data-stu-id="9da80-106">The plan type is then associated with a benefit plan or program.</span></span> <span data-ttu-id="9da80-107">Plaani tüübiga seostatud katvuse valikud on saadaval kõigile selle plaani tüübiga loodud plaanidele.</span><span class="sxs-lookup"><span data-stu-id="9da80-107">Coverage options that are associated with a plan type will be available to all plans that are created with that plan type.</span></span> 

1. <span data-ttu-id="9da80-108">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Katvuse valikud**.</span><span class="sxs-lookup"><span data-stu-id="9da80-108">In the **Benefits management** workspace, under **Setup**, select **Coverage options**.</span></span>

2. <span data-ttu-id="9da80-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9da80-109">Select **New**.</span></span>

3. <span data-ttu-id="9da80-110">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="9da80-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="9da80-111">Väli</span><span class="sxs-lookup"><span data-stu-id="9da80-111">Field</span></span> | <span data-ttu-id="9da80-112">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9da80-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9da80-113">**Katvuse valik**</span><span class="sxs-lookup"><span data-stu-id="9da80-113">**Coverage option**</span></span> | <span data-ttu-id="9da80-114">Kordumatu katvuse valiku nimi.</span><span class="sxs-lookup"><span data-stu-id="9da80-114">A unique coverage option name.</span></span> |
   | <span data-ttu-id="9da80-115">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="9da80-115">**Description**</span></span> | <span data-ttu-id="9da80-116">Katvuse valiku kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9da80-116">A description of the coverage option.</span></span> |
   | <span data-ttu-id="9da80-117">**Planeerimise kood**</span><span class="sxs-lookup"><span data-stu-id="9da80-117">**Coverage code**</span></span> | <span data-ttu-id="9da80-118">Katvuse koodid määravad minimaalsed ja maksimaalsed summad iga sobiva kaetud isiku tüübi jaoks.</span><span class="sxs-lookup"><span data-stu-id="9da80-118">Coverage codes assign minimum and maximum amounts for each eligible covered person type.</span></span> <span data-ttu-id="9da80-119">Katvuse kood näitab, kes on kaetud või plaani tüübile lubatud katvuse summa.</span><span class="sxs-lookup"><span data-stu-id="9da80-119">A coverage code indicates who is covered or the amount of coverage allowed for a plan type.</span></span> <span data-ttu-id="9da80-120">Saate väljendada katvuse summat summana dollarites või protsendina.</span><span class="sxs-lookup"><span data-stu-id="9da80-120">You can express the amount of coverage as a dollar amount or a percentage.</span></span> <span data-ttu-id="9da80-121">Näide:</span><span class="sxs-lookup"><span data-stu-id="9da80-121">For example:</span></span></br></br><span data-ttu-id="9da80-122">- **EMP+1** – kvalifitseerumiseks peab töövõtjal olema üks sõltuv isik valitud (kui valitud on rohkem kui üks, siis need enam ei kvalifitseeru).</span><span class="sxs-lookup"><span data-stu-id="9da80-122">- **Emp+1** – to be qualified, the employee must have one dependent selected (if more than one is selected, they no longer qualify).</span></span></br></br><span data-ttu-id="9da80-123">- **EMP+perekond** – kvalifitseerumiseks peab töövõtjal olema vähemalt kaks sõltuvat isikut valitud.</span><span class="sxs-lookup"><span data-stu-id="9da80-123">- **Emp+family** – to be qualified, the employee must have at least two dependents selected.</span></span> |
   | <span data-ttu-id="9da80-124">**Maksimaalne arv**</span><span class="sxs-lookup"><span data-stu-id="9da80-124">**Maximum number**</span></span> | <span data-ttu-id="9da80-125">Maksimaalne sõltuvate isikute arv.</span><span class="sxs-lookup"><span data-stu-id="9da80-125">The maximum number of dependents.</span></span> |
   | <span data-ttu-id="9da80-126">**Olek**</span><span class="sxs-lookup"><span data-stu-id="9da80-126">**Status**</span></span> | <span data-ttu-id="9da80-127">Katvuse valiku olek.</span><span class="sxs-lookup"><span data-stu-id="9da80-127">The status of the coverage option.</span></span> <span data-ttu-id="9da80-128">Kui katvuse valiku olek on seatud passiivseks, ei saa plaani tüüpides katvuse valikut valida.</span><span class="sxs-lookup"><span data-stu-id="9da80-128">If the Coverage option status is set to Inactive, the Coverage option can’t be selected on plan types.</span></span> |
   | <span data-ttu-id="9da80-129">**Protsent**</span><span class="sxs-lookup"><span data-stu-id="9da80-129">**Percent**</span></span> | <span data-ttu-id="9da80-130">Protsendi summa.</span><span class="sxs-lookup"><span data-stu-id="9da80-130">The percent amount.</span></span> <span data-ttu-id="9da80-131">See väli on aktiivne ainult juhul, kui väljal Katvuse kood on valitud % × palk.</span><span class="sxs-lookup"><span data-stu-id="9da80-131">This field is only active if % x Salary was selected in the Coverage code field.</span></span> |
   | <span data-ttu-id="9da80-132">**Jagaja**</span><span class="sxs-lookup"><span data-stu-id="9da80-132">**Divisor**</span></span> | <span data-ttu-id="9da80-133">Jagaja, mida kasutatakse arvutamisel, kui valite katvuse koodi % × palk.</span><span class="sxs-lookup"><span data-stu-id="9da80-133">The divisor to use in the calculation when you select the coverage code % x salary.</span></span> |
   | <span data-ttu-id="9da80-134">**Miinimumprotsent**</span><span class="sxs-lookup"><span data-stu-id="9da80-134">**Percent minimum**</span></span> | <span data-ttu-id="9da80-135">Minimaalne protsent, kui valite katvuse koodi Protsent.</span><span class="sxs-lookup"><span data-stu-id="9da80-135">The minimum percentage when you select the Percentage coverage code.</span></span> |
   | <span data-ttu-id="9da80-136">**Maksimumprotsent**</span><span class="sxs-lookup"><span data-stu-id="9da80-136">**Percent maximum**</span></span> | <span data-ttu-id="9da80-137">Maksimaalne protsent, kui valite katvuse koodi Protsent.</span><span class="sxs-lookup"><span data-stu-id="9da80-137">The maximum percentage when you select the Percentage coverage code.</span></span> |

4. <span data-ttu-id="9da80-138">Jaotises **Isikliku kontakti sobivuse suvandid** lisage igale katvuse valikule sobiv isiklike kontaktide sobivuse suvand.</span><span class="sxs-lookup"><span data-stu-id="9da80-138">Under **Personal contact eligibility options**, attach the appropriate personal contacts eligibility option to each coverage option.</span></span>

5. <span data-ttu-id="9da80-139">Vahekaardil **Iseteenindus** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="9da80-139">Under **Self service**, specify values for the following fields:</span></span>

   | <span data-ttu-id="9da80-140">Väli</span><span class="sxs-lookup"><span data-stu-id="9da80-140">Field</span></span> | <span data-ttu-id="9da80-141">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9da80-141">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="9da80-142">**Luba töövõtja panuse summa määramine**</span><span class="sxs-lookup"><span data-stu-id="9da80-142">**Allow employee contribution amount**</span></span> | <span data-ttu-id="9da80-143">Määrab, kas lubada töötajatel soodustuste valimisel muuta soodustuste osamakse summat.</span><span class="sxs-lookup"><span data-stu-id="9da80-143">Specifies whether to allow employees to modify the contribution amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="9da80-144">Kui märgite selle ruudu, arvutab süsteem hüvitise plaani parameetrid, võttes aluseks osamakse summa, mille töötaja sisestab soodustuste iseteeninduses.</span><span class="sxs-lookup"><span data-stu-id="9da80-144">If you select this check box, the system will calculate benefit plan parameters based on the contribution amount the employee enters on benefits self-service.</span></span> |
   | <span data-ttu-id="9da80-145">**Luba töövõtja kindlustussumma määramine**</span><span class="sxs-lookup"><span data-stu-id="9da80-145">**Allow employee coverage amount**</span></span> | <span data-ttu-id="9da80-146">Määrab, kas lubada töötajatel soodustuste valimisel muuta soodustuste katvuse summat.</span><span class="sxs-lookup"><span data-stu-id="9da80-146">Specifies whether to allow employees to modify the coverage amount on benefits self-service when they select benefits.</span></span> <span data-ttu-id="9da80-147">Kui märgite selle ruudu, arvutab süsteem hüvitise plaani parameetrid, võttes aluseks katvuse summa, mille töötaja sisestab töövõtja iseteeninduses.</span><span class="sxs-lookup"><span data-stu-id="9da80-147">If you select this check box, the system will calculate benefit plan parameters based on the coverage amount the employee enters in Employee self service.</span></span> |

6. <span data-ttu-id="9da80-148">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9da80-148">Select **Save**.</span></span> 
