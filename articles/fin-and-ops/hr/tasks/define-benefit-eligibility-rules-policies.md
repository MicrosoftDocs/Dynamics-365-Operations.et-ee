--- 
title: "Soodustuskõlblikkuse reeglite ja poliitikate määratlemine"
description: "See registreerimine näitab, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d346c3277e8f19020d6aa96cf6961c4c52ac28fb
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="ff08d-103">Soodustuskõlblikkuse reeglite ja poliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="ff08d-103">Define benefit eligibility rules and policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff08d-104">See registreerimine näitab, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata.</span><span class="sxs-lookup"><span data-stu-id="ff08d-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="ff08d-105">Selle kirje loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ff08d-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="ff08d-106">Soodustuskõlblikkuse poliitika reegli tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="ff08d-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="ff08d-107">Avage Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitika reeglitüübid.</span><span class="sxs-lookup"><span data-stu-id="ff08d-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="ff08d-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ff08d-108">Click New.</span></span>
3. <span data-ttu-id="ff08d-109">Sisestage väärtus väljale Reegli nimi.</span><span class="sxs-lookup"><span data-stu-id="ff08d-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="ff08d-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ff08d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ff08d-111">Klõpsake väljal Päringu nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ff08d-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ff08d-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ff08d-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ff08d-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ff08d-113">Click Save.</span></span>
8. <span data-ttu-id="ff08d-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ff08d-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="ff08d-115">Sooduskõlblikkuse poliitika</span><span class="sxs-lookup"><span data-stu-id="ff08d-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="ff08d-116">Avage Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitikad.</span><span class="sxs-lookup"><span data-stu-id="ff08d-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="ff08d-117">Valige olemasolev soodustuse poliitika.</span><span class="sxs-lookup"><span data-stu-id="ff08d-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="ff08d-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ff08d-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ff08d-119">Laiendage jaotisi Poliitika organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="ff08d-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="ff08d-120">Siin saate lisada või eemaldada mis tahes organisatsioone, mida soovite poliitikasse kaasata.</span><span class="sxs-lookup"><span data-stu-id="ff08d-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="ff08d-121">Laiendage või ahendage jaotist Poliitika reeglid.</span><span class="sxs-lookup"><span data-stu-id="ff08d-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="ff08d-122">Leidke loendist varem loodud poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="ff08d-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="ff08d-123">Klõpsake valikut Loo poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="ff08d-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="ff08d-124">Sisestage väljale Jõustumiskuupäev kuupäev, alates millest soovite muuta poliitika jõustuvaks.</span><span class="sxs-lookup"><span data-stu-id="ff08d-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="ff08d-125">Jõustumis- ja lõppkuupäevade seadistamine võimaldab teil poliitika reegleid edaspidi muuta ja kõrvaldab vajaduse poliitika juurde naasta, kui soovite, et need muudatused jõustuksid.</span><span class="sxs-lookup"><span data-stu-id="ff08d-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="ff08d-126">Näiteks kui soovisite reeglit rakendada ainult müügijuhtidele, saite luua Kui tingimuse, mis ütleb järgmist: kui ametikoha kirjeldus võrdub müügijuhi omaga.</span><span class="sxs-lookup"><span data-stu-id="ff08d-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="ff08d-127">Saate operaatoritega And või Or kaasata reeglisse mitu Kui tingimust.</span><span class="sxs-lookup"><span data-stu-id="ff08d-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="ff08d-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ff08d-128">Click OK.</span></span>
11. <span data-ttu-id="ff08d-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ff08d-129">Close the page.</span></span>
12. <span data-ttu-id="ff08d-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ff08d-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="ff08d-131">Reegli määramine soodustusele</span><span class="sxs-lookup"><span data-stu-id="ff08d-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="ff08d-132">Avage Personaliarvestus > Soodustused > Soodustused.</span><span class="sxs-lookup"><span data-stu-id="ff08d-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="ff08d-133">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ff08d-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ff08d-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ff08d-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ff08d-135">Laiendage või ahendage jaotist Sobivuse reeglid.</span><span class="sxs-lookup"><span data-stu-id="ff08d-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="ff08d-136">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="ff08d-136">Click Edit.</span></span>
6. <span data-ttu-id="ff08d-137">Valige väljal Sobivus reegel loendi alusel.</span><span class="sxs-lookup"><span data-stu-id="ff08d-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="ff08d-138">Klõpsake väljal Reegli tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ff08d-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="ff08d-139">Leidke ja valige loendist varem loodud reegel.</span><span class="sxs-lookup"><span data-stu-id="ff08d-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="ff08d-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ff08d-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ff08d-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ff08d-141">Click Save.</span></span>
11. <span data-ttu-id="ff08d-142">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="ff08d-142">Close the form.</span></span>


