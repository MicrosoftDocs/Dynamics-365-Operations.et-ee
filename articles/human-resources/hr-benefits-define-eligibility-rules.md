---
title: Soodustuskõlblikkuse reeglite ja poliitikate määratlemine
description: Selles artiklis näidatakse, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 046b045fbdda125c5a2259783c0347f687453528
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053149"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="ea3f3-103">Soodustuskõlblikkuse reeglite ja poliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="ea3f3-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ea3f3-104">Selles teemas näidatakse, kuidas luua soodustuse kõlblikkuse reegleid ja poliitikaid ning seejärel soodustustele reegleid määrata.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="ea3f3-105">Soodustuskõlblikkuse poliitika reegli tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="ea3f3-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="ea3f3-106">Avage **Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitika reeglitüübid**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="ea3f3-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-107">Select **New**.</span></span>
3. <span data-ttu-id="ea3f3-108">Sisestage väljale **Reegli nimi** väärtus.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="ea3f3-109">Sisestage väärtus väljal **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="ea3f3-110">Valige väljal **Päringu nimi** ripploendi nupp otsingu avamiseks.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ea3f3-111">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="ea3f3-112">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-112">Select **Save**.</span></span>
8. <span data-ttu-id="ea3f3-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="ea3f3-114">Sooduskõlblikkuse poliitika</span><span class="sxs-lookup"><span data-stu-id="ea3f3-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="ea3f3-115">Avage **Inimressursid > Soodustused > Kõlblikkus > Soodustuskõlblikkuse poliitikad**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="ea3f3-116">Valige olemasolev soodustuse poliitika.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="ea3f3-117">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="ea3f3-118">Laiendage jaotisi **Poliitika organisatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="ea3f3-119">Saate lisada või eemaldada mis tahes organisatsioone, mida soovite poliitikasse kaasata.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="ea3f3-120">Laiendage või ahendage jaotist **Poliitika reeglid**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="ea3f3-121">Leidke loendist varem loodud poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="ea3f3-122">Valige **Poliitika reegli loomine**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="ea3f3-123">Sisestage väljale **Jõustumiskuupäev** kuupäev, alates millest soovite muuta poliitika jõustuvaks.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="ea3f3-124">Jõustumis- ja lõppkuupäevade seadistamine võimaldab teil poliitika reegleid edaspidi muuta ja et teil pole vaja poliitika juurde naasta, kui soovite, et need muudatused jõustuksid.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="ea3f3-125">Vajadusel lisage väljale **Lisa tingimus** kui-tingimus.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="ea3f3-126">Näiteks kui soovisite reeglit rakendada ainult müügijuhtidele, saite luua Kui tingimuse, mis ütleb järgmist: kui ametikoha kirjeldus võrdub müügijuhi omaga.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="ea3f3-127">Saate reeglisse lisada mitu kui-tingimust koos.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="ea3f3-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-128">Select **OK**.</span></span>
11. <span data-ttu-id="ea3f3-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="ea3f3-130">Reegli määramine soodustusele</span><span class="sxs-lookup"><span data-stu-id="ea3f3-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="ea3f3-131">Avage **Personaliarvestus > Soodustused > Soodustused**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="ea3f3-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ea3f3-133">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="ea3f3-134">Laiendage või ahendage jaotist **Sobivuse reeglid**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="ea3f3-135">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-135">Select **Edit**.</span></span>
6. <span data-ttu-id="ea3f3-136">Valige väljal **Sobivus** väärtus reegel.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="ea3f3-137">Valige väljal **Reegli tüüp** varem loodud reegel.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="ea3f3-138">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="ea3f3-139">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-139">Select **Save**.</span></span>
11. <span data-ttu-id="ea3f3-140">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="ea3f3-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]