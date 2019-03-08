---
title: Hankekategooria hierarhiate poliitikate seadistamine
description: Kasutage seda protseduuri, et seadistada reeglid kategooria toodete tellimiseks.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, SysPolicy, ProcCategoryAccessPolicyRule, ProcCategoryPolicyRule, EcoResCategorySingleLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1fdf357466de12bd0188fc43cd266c67af762c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "323153"
---
# <a name="set-up-policies-for-procurement-category-hierarchies"></a><span data-ttu-id="a16b3-103">Hankekategooria hierarhiate poliitikate seadistamine</span><span class="sxs-lookup"><span data-stu-id="a16b3-103">Set up policies for procurement category hierarchies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a16b3-104">Kasutage seda protseduuri, et seadistada reeglid kategooria toodete tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="a16b3-104">Use this procedure to set up rules for ordering products in a category.</span></span> <span data-ttu-id="a16b3-105">Reeglid määratletakse konkreetsele ostupoliitikale.</span><span class="sxs-lookup"><span data-stu-id="a16b3-105">The rules are defined for a specific purchasing policy.</span></span> <span data-ttu-id="a16b3-106">Kategooria juurdepääsureegel juhib seda, millistele hankekategooriatele on töötajatel juurdepääs, kui nad taotluse loovad.</span><span class="sxs-lookup"><span data-stu-id="a16b3-106">The category access rule controls which procurement categories employees have access to when they create a requisition.</span></span> <span data-ttu-id="a16b3-107">Taotluse loomise ajal määratakse rakendatav ostupoliitika ja kategooria juurdepääsureegel juriidilise isiku ja tootmisüksuse põhjal, kuhu töötaja kuulub.</span><span class="sxs-lookup"><span data-stu-id="a16b3-107">When a requisition is being created, the purchasing policy and category access rule that should be applied are determined by the legal entity and the operational unit that the employee belongs to.</span></span> <span data-ttu-id="a16b3-108">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="a16b3-108">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="a16b3-109">Seda ülesannet täidab tavaliselt ostujuht.</span><span class="sxs-lookup"><span data-stu-id="a16b3-109">This task would typically be carried out by a purchasing manager.</span></span>


## <a name="find-the-procurement-policy"></a><span data-ttu-id="a16b3-110">Hankepoliitika otsimine</span><span class="sxs-lookup"><span data-stu-id="a16b3-110">Find the procurement policy</span></span>
1. <span data-ttu-id="a16b3-111">Valige Hanked > Seadistus > Poliitikad > Ostupoliitikad.</span><span class="sxs-lookup"><span data-stu-id="a16b3-111">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="a16b3-112">Klõpsake poliitika Hankepoliitika USMF linki.</span><span class="sxs-lookup"><span data-stu-id="a16b3-112">Click the link on the Procurement Policy USMF policy.</span></span>
    * <span data-ttu-id="a16b3-113">See on poliitika, millele reegli lisate.</span><span class="sxs-lookup"><span data-stu-id="a16b3-113">This is the policy that you’ll add a rule to.</span></span> <span data-ttu-id="a16b3-114">See peab olema aktiivne poliitika.</span><span class="sxs-lookup"><span data-stu-id="a16b3-114">It must be an Active policy.</span></span>  

## <a name="create-a-category-access-rule"></a><span data-ttu-id="a16b3-115">Kategooria juurdepääsureegli loomine</span><span class="sxs-lookup"><span data-stu-id="a16b3-115">Create a category access rule</span></span>
1. <span data-ttu-id="a16b3-116">Valige kategooria juurdepääsupoliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="a16b3-116">Select the Category access policy rule.</span></span>
    * <span data-ttu-id="a16b3-117">Kui nupp Loo poliitikareegel on tuhm, siis on kategooria juurdepääsul juba aktiivne poliitikareegel olemas.</span><span class="sxs-lookup"><span data-stu-id="a16b3-117">If the Create policy rule button is dimmed, it’s because there’s already an active policy rule for Category access.</span></span> <span data-ttu-id="a16b3-118">Kontrollige jõustumis- ja aegumiskuupäeva välju, et määrata, mis see on, ning seejärel valige see ja klõpsake valikut Määra poliitikareegel aegunuks.</span><span class="sxs-lookup"><span data-stu-id="a16b3-118">Check the Effective and Expiration date fields to determine which it is, then select it, and click Retire policy rule.</span></span> <span data-ttu-id="a16b3-119">Kui nupp Loo poliitikareegel on saadaval, pole midagi vaja teha.</span><span class="sxs-lookup"><span data-stu-id="a16b3-119">If the Create policy rule button is available, you don’t need to do anything.</span></span>  
2. <span data-ttu-id="a16b3-120">Klõpsake valikut Loo poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="a16b3-120">Click Create policy rule.</span></span>
3. <span data-ttu-id="a16b3-121">Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="a16b3-121">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="a16b3-122">Aeg ei tohi kattuda teise juba aktiivse reegliga.</span><span class="sxs-lookup"><span data-stu-id="a16b3-122">The time must not overlap with another rule that’s already active.</span></span>  
    * <span data-ttu-id="a16b3-123">Valige kategooria, millele reegel rakendub.</span><span class="sxs-lookup"><span data-stu-id="a16b3-123">Select a category that the rule will apply to.</span></span> <span data-ttu-id="a16b3-124">Märkige üles, milline kategooria see on – seda on hiljem vaja.</span><span class="sxs-lookup"><span data-stu-id="a16b3-124">Make a note of which category this is – you’ll need it later.</span></span> <span data-ttu-id="a16b3-125">Kategooria valimisel lisatakse loendisse Valitud kategooriad selle põhikategooria või -kategooriad.</span><span class="sxs-lookup"><span data-stu-id="a16b3-125">When you select a category, its parent category or categories will also be added to the Selected categories list.</span></span>  
    * <span data-ttu-id="a16b3-126">Kui soovite, et reegel kehtiks kõigile valitud kategooria alamkategooriatele, märkige ruut Kaasa alamkategooriad.</span><span class="sxs-lookup"><span data-stu-id="a16b3-126">If you want the rule to apply to all subcategories of the selected category, select the Include subcategories check box.</span></span>  
4. <span data-ttu-id="a16b3-127">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="a16b3-127">Click Add.</span></span>
    * <span data-ttu-id="a16b3-128">Kui määrate valiku Kaasa põhireegel väärtuseks Jah, määratakse põhireeglile määratletud poliitikareegel ka selle alamkategooriatele, kui alamkategooriatele on poliitikareegel määratletud.</span><span class="sxs-lookup"><span data-stu-id="a16b3-128">If you set the Include parent rule option to Yes, the policy rule that you define for a parent category is also assigned to its child categories, if no policy rule has been defined for the child categories.</span></span>  
5. <span data-ttu-id="a16b3-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a16b3-129">Click OK.</span></span>

## <a name="create-a-category-policy-rule"></a><span data-ttu-id="a16b3-130">Kategooria poliitikareegli loomine</span><span class="sxs-lookup"><span data-stu-id="a16b3-130">Create a category policy rule</span></span>
1. <span data-ttu-id="a16b3-131">Valige kategooria poliitikareegel</span><span class="sxs-lookup"><span data-stu-id="a16b3-131">Select the Category policy rule</span></span>
    * <span data-ttu-id="a16b3-132">Kui nupp Loo poliitikareegel on tuhm, valige aktiivne poliitikareegel ja klõpsake valikut Määra poliitikareegel aegunuks.</span><span class="sxs-lookup"><span data-stu-id="a16b3-132">If the Create policy rule button is dimmed, select the active policy rule, and then click Retire policy rule.</span></span>  
2. <span data-ttu-id="a16b3-133">Klõpsake valikut Loo poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="a16b3-133">Click Create policy rule.</span></span>
3. <span data-ttu-id="a16b3-134">Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="a16b3-134">In the Effective date field, enter a date and time.</span></span>
4. <span data-ttu-id="a16b3-135">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="a16b3-135">Click Add.</span></span>
5. <span data-ttu-id="a16b3-136">Valige sama kategooria, mida kasutasite kategooria juurdepääsureegli puhul.</span><span class="sxs-lookup"><span data-stu-id="a16b3-136">Select the same category that you used for the Category access rule.</span></span>
6. <span data-ttu-id="a16b3-137">Tehke valik väljal Hankija olek.</span><span class="sxs-lookup"><span data-stu-id="a16b3-137">In the Vendor selection field, select an option.</span></span>
    * <span data-ttu-id="a16b3-138">Valige reegel, et juhtida, milliseid hankijaid võib taotluste loomisel kategooriale valida.</span><span class="sxs-lookup"><span data-stu-id="a16b3-138">Select a rule to control which kind of vendors can be selected for the category when requisitions are created.</span></span>  
7. <span data-ttu-id="a16b3-139">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="a16b3-139">Click Close.</span></span>
    * <span data-ttu-id="a16b3-140">Teie määratletud poliitikareeglid on olnud taotlustele tüübiga Tarbimine.</span><span class="sxs-lookup"><span data-stu-id="a16b3-140">The policy rules that you have defined have been for requisitions of type Consumption.</span></span> <span data-ttu-id="a16b3-141">Kui soovite määratleda poliitikad taotlustele tüübiga Täiendamine, tuleb luua reegel poliitikareegli tüübile nimega Täiendamise kategooria juurdepääsupoliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="a16b3-141">If you wanted to define policies for requisitions of type Replenishment, you would create a rule for the Policy rule type called “Replenishment category access policy rule”.</span></span>  

