---
title: Soodustuskõlblikkuse reeglite ja poliitikate määratlemine
description: Selles artiklis näidatakse, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: fa507591fc89eaebf617deedb15b15a0f93f971d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008819"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="dce71-103">Soodustuskõlblikkuse reeglite ja poliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="dce71-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="dce71-104">Selles artiklis näidatakse, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata.</span><span class="sxs-lookup"><span data-stu-id="dce71-104">This article shows you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="dce71-105">Selle kirje loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="dce71-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="dce71-106">Soodustuskõlblikkuse poliitika reegli tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="dce71-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="dce71-107">Avage Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitika reeglitüübid.</span><span class="sxs-lookup"><span data-stu-id="dce71-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="dce71-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dce71-108">Click New.</span></span>
3. <span data-ttu-id="dce71-109">Sisestage väärtus väljale Reegli nimi.</span><span class="sxs-lookup"><span data-stu-id="dce71-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="dce71-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="dce71-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dce71-111">Klõpsake väljal Päringu nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="dce71-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="dce71-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dce71-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="dce71-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="dce71-113">Click Save.</span></span>
8. <span data-ttu-id="dce71-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dce71-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="dce71-115">Sooduskõlblikkuse poliitika</span><span class="sxs-lookup"><span data-stu-id="dce71-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="dce71-116">Avage Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitikad.</span><span class="sxs-lookup"><span data-stu-id="dce71-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="dce71-117">Valige olemasolev soodustuse poliitika.</span><span class="sxs-lookup"><span data-stu-id="dce71-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="dce71-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dce71-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="dce71-119">Laiendage jaotisi Poliitika organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="dce71-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="dce71-120">Siin saate lisada või eemaldada mis tahes organisatsioone, mida soovite poliitikasse kaasata.</span><span class="sxs-lookup"><span data-stu-id="dce71-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="dce71-121">Laiendage või ahendage jaotist Poliitika reeglid.</span><span class="sxs-lookup"><span data-stu-id="dce71-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="dce71-122">Leidke loendist varem loodud poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="dce71-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="dce71-123">Klõpsake valikut Loo poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="dce71-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="dce71-124">Sisestage väljale Jõustumiskuupäev kuupäev, alates millest soovite muuta poliitika jõustuvaks.</span><span class="sxs-lookup"><span data-stu-id="dce71-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="dce71-125">Jõustumis- ja lõppkuupäevade seadistamine võimaldab teil poliitika reegleid edaspidi muuta ja kõrvaldab vajaduse poliitika juurde naasta, kui soovite, et need muudatused jõustuksid.</span><span class="sxs-lookup"><span data-stu-id="dce71-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="dce71-126">Näiteks kui soovisite reeglit rakendada ainult müügijuhtidele, saite luua Kui tingimuse, mis ütleb järgmist: kui ametikoha kirjeldus võrdub müügijuhi omaga.</span><span class="sxs-lookup"><span data-stu-id="dce71-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="dce71-127">Saate operaatoritega And või Or kaasata reeglisse mitu Kui tingimust.</span><span class="sxs-lookup"><span data-stu-id="dce71-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="dce71-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dce71-128">Click OK.</span></span>
11. <span data-ttu-id="dce71-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dce71-129">Close the page.</span></span>
12. <span data-ttu-id="dce71-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dce71-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="dce71-131">Reegli määramine soodustusele</span><span class="sxs-lookup"><span data-stu-id="dce71-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="dce71-132">Avage Personaliarvestus > Soodustused > Soodustused.</span><span class="sxs-lookup"><span data-stu-id="dce71-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="dce71-133">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="dce71-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="dce71-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dce71-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="dce71-135">Laiendage või ahendage jaotist Sobivuse reeglid.</span><span class="sxs-lookup"><span data-stu-id="dce71-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="dce71-136">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="dce71-136">Click Edit.</span></span>
6. <span data-ttu-id="dce71-137">Valige väljal Sobivus reegel loendi alusel.</span><span class="sxs-lookup"><span data-stu-id="dce71-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="dce71-138">Klõpsake väljal Reegli tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="dce71-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="dce71-139">Leidke ja valige loendist varem loodud reegel.</span><span class="sxs-lookup"><span data-stu-id="dce71-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="dce71-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dce71-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="dce71-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="dce71-141">Click Save.</span></span>
11. <span data-ttu-id="dce71-142">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="dce71-142">Close the form.</span></span>

