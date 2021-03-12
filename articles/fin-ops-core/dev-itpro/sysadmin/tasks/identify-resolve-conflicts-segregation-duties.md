---
title: Kohustuste jagamise konfliktide tuvastamine ja lahendamine
description: Selles teemas kirjeldatakse, kuidas tuvastada ja lahendada konflikte kohustuste jagamisel.
author: peakerbl
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesConflict, SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deff97c7728db91089d3ea834d15de738da500fa
ms.sourcegitcommit: 316200579dd5b04ad76f276a2ed6b0f55fa8c812
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/05/2021
ms.locfileid: "4826364"
---
# <a name="identify-and-resolve-conflicts-in-segregation-of-duties"></a><span data-ttu-id="4967e-103">Kohustuste jagamise konfliktide tuvastamine ja lahendamine</span><span class="sxs-lookup"><span data-stu-id="4967e-103">Identify and resolve conflicts in segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4967e-104">Selles teemas kirjeldatakse, kuidas tuvastada ja lahendada konflikte kohustuste jagamisel.</span><span class="sxs-lookup"><span data-stu-id="4967e-104">This topic explains how to identify and resolve conflicts in segregation of duties.</span></span> <span data-ttu-id="4967e-105">Saate seadistada reeglid nende kohustuste eraldamiseks, mille peavad täitma erinevad kasutajad.</span><span class="sxs-lookup"><span data-stu-id="4967e-105">You can set up rules to separate duties that must be performed by different users.</span></span> <span data-ttu-id="4967e-106">Seda põhimõtet nimetatakse kohustuste jagamiseks.</span><span class="sxs-lookup"><span data-stu-id="4967e-106">This concept is named segregation of duties.</span></span> <span data-ttu-id="4967e-107">Kui turberolli määratlus või kasutaja rollimäärangud rikuvad reegleid, logitakse konflikt.</span><span class="sxs-lookup"><span data-stu-id="4967e-107">When the definition of a security role or the role assignments of a user violate the rules, the conflict is logged.</span></span> <span data-ttu-id="4967e-108">Administraator peab kõik konfliktid lahendama.</span><span class="sxs-lookup"><span data-stu-id="4967e-108">All conflicts must be resolved by the administrator.</span></span> <span data-ttu-id="4967e-109">Konfliktide tuvastamiseks ja lahendamiseks kasutage järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="4967e-109">Complete the following procedure to identify and resolve conflicts.</span></span>

<span data-ttu-id="4967e-110">Pärast reegli lisamist kontrollige, kas kõik olemasolevad rollid ühilduvad.</span><span class="sxs-lookup"><span data-stu-id="4967e-110">After a rule has been added, verify that all existing roles are compliant.</span></span> 

## <a name="verify-that-existing-roles-and-duties-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="4967e-111">Kontrollige, kas olemasolevad rollid ja kohustused vastavad uutele kohustuste jagamise reeglitele</span><span class="sxs-lookup"><span data-stu-id="4967e-111">Verify that existing roles and duties comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="4967e-112">Avage **Süsteemihaldus** > **Turve** > **Kohustuste jagamine** > **Kohustuste jagamise reeglid**.</span><span class="sxs-lookup"><span data-stu-id="4967e-112">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties rules**.</span></span>
3. <span data-ttu-id="4967e-113">Valige **Kohustuste ja rollide kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="4967e-113">Select **Validate duties and roles**.</span></span> <span data-ttu-id="4967e-114">Kui mis tahes roll rikub reegleid, kuvatakse teade, mis sisaldab reegli nime, rolli ja konfliktsete kohustuste nimesid.</span><span class="sxs-lookup"><span data-stu-id="4967e-114">If any roles violate the rules, a message is displayed that contains the name of the rule, the role, and the names of the conflicting duties.</span></span> <span data-ttu-id="4967e-115">Konfliktsed rollid peavad olema muudetud suvandi **Turvakonfiguratsioon** abil ja need ei tohi sisaldada vastuolulisi kohustusi.</span><span class="sxs-lookup"><span data-stu-id="4967e-115">Conflicting roles must be modified using **Security configuration** and can't include conflicting duties.</span></span> <span data-ttu-id="4967e-116">Kui ükski roll valitud reeglit ei riku, kuvatakse teade, et kõik rollid vastavad.</span><span class="sxs-lookup"><span data-stu-id="4967e-116">If no roles violate the selected rule, a message indicates that all roles comply.</span></span>   

> [!NOTE]
> <span data-ttu-id="4967e-117">Kinnitamine tehakse ainult valitud reeglile.</span><span class="sxs-lookup"><span data-stu-id="4967e-117">The validation is only performed for the selected rule.</span></span> <span data-ttu-id="4967e-118">Oluline on kontrollida vastavust iga reegli puhul.</span><span class="sxs-lookup"><span data-stu-id="4967e-118">It is important to validate compliance for each rule.</span></span>   

<span data-ttu-id="4967e-119">Rolli loomisel või muutmisel jõustatakse kohustuste jagamise reeglid automaatselt.</span><span class="sxs-lookup"><span data-stu-id="4967e-119">When you create or modify a role, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="4967e-120">Rollile ei saa määrata vastuolulisi kohustusi.</span><span class="sxs-lookup"><span data-stu-id="4967e-120">You cannot assign conflicting duties to a role.</span></span>

<span data-ttu-id="4967e-121">Järgmisena kontrollige, kas kõik olemasolevad rollimäärangud ühilduvad.</span><span class="sxs-lookup"><span data-stu-id="4967e-121">Next, verify that all existing role assignments are compliant.</span></span>

## <a name="verify-that-user-role-assignments-comply-with-new-rules-for-segregation-of-duties"></a><span data-ttu-id="4967e-122">Kontrollige, kas kasutajarolli määramised vastavad uutele kohustuste jagamise reeglitele</span><span class="sxs-lookup"><span data-stu-id="4967e-122">Verify that user role assignments comply with new rules for segregation of duties</span></span>
1. <span data-ttu-id="4967e-123">Avage **Süsteemihaldus > Turve > Kohustuste jagamine > Kasutaja rollimäärangute vastavuse kontrollimine**.</span><span class="sxs-lookup"><span data-stu-id="4967e-123">Go to **System administration > Security > Segregation of duties > Verify compliance of user-role assignments**.</span></span>
2. <span data-ttu-id="4967e-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4967e-124">Select **OK**.</span></span> <span data-ttu-id="4967e-125">Kuvatakse teade kinnitamise tulemustega.</span><span class="sxs-lookup"><span data-stu-id="4967e-125">A notification displays the results of the validation.</span></span> <span data-ttu-id="4967e-126">Konfliktid logitakse lehel **Kohustuste jagamise lahendamata konfliktid**.</span><span class="sxs-lookup"><span data-stu-id="4967e-126">Conflicts are logged on the **Segregation of duties unresolved conflicts** page.</span></span>   

<span data-ttu-id="4967e-127">Kasutajate rollide määramisel jõustatakse kohustuste jagamise reeglid automaatselt.</span><span class="sxs-lookup"><span data-stu-id="4967e-127">When you assign users to roles, the rules for segregation of duties are automatically enforced.</span></span> <span data-ttu-id="4967e-128">Kui proovite määrata kasutajat rollidele, mis sisaldavad vastuolulisi kohustusi, kuvatakse tõrketeade.</span><span class="sxs-lookup"><span data-stu-id="4967e-128">If you try to assign a user to roles that contain conflicting duties, you receive an error message.</span></span> <span data-ttu-id="4967e-129">Seejärel peate konflikti lahendama, keelates või lubades täiendava rollimäärangu.</span><span class="sxs-lookup"><span data-stu-id="4967e-129">You must then resolve the conflict by denying or allowing the additional role assignment.</span></span> <span data-ttu-id="4967e-130">Lisaroll määratakse pärast määramise lubamist.</span><span class="sxs-lookup"><span data-stu-id="4967e-130">The additional role will be assigned after the assignment is allowed.</span></span> 

> [!NOTE]
> <span data-ttu-id="4967e-131">Vastuolusid ei kontrollita praegu kasutajatele, kellele on Active Directory domeenigruppide alusel määratud rollid.</span><span class="sxs-lookup"><span data-stu-id="4967e-131">Conflicts are currently not verified for users that are assigned roles based on the Active Directory Domain groups.</span></span>

## <a name="view-and-resolve-conflicting-user-role-assignments"></a><span data-ttu-id="4967e-132">Konfliktsete kasutaja rollimäärangute kuvamine ja lahendamine</span><span class="sxs-lookup"><span data-stu-id="4967e-132">View and resolve conflicting user role assignments</span></span>
1. <span data-ttu-id="4967e-133">Avage **Süsteemihaldus** > **Turve** > **Kohustuste jagamine** > **Kohustuste jagamise lahendamata konfliktid**.</span><span class="sxs-lookup"><span data-stu-id="4967e-133">Go to **System administration** > **Security** > **Segregation of duties** > **Segregation of duties unresolved conflicts**.</span></span> 
2. <span data-ttu-id="4967e-134">Valige vastuolu ja valige seejärel üks järgmistest tegevustest.</span><span class="sxs-lookup"><span data-stu-id="4967e-134">Select a conflict, and then select one of the following actions:</span></span> 

  - <span data-ttu-id="4967e-135">**Määrangu keelamine**: sellega keelatakse kasutaja määramine täiendavale turberollile.</span><span class="sxs-lookup"><span data-stu-id="4967e-135">**Deny assignment**: This will deny the assignment of the user to the additional security role.</span></span> <span data-ttu-id="4967e-136">Automaatse Rollimäärangu keelamisel märgitakse kasutaja rollist välistatuks.</span><span class="sxs-lookup"><span data-stu-id="4967e-136">If you deny an automatic role assignment, the user is marked as excluded from the role.</span></span> <span data-ttu-id="4967e-137">Välistatud kasutajale ei anta rolliga seotud juurdepääsu ja teda ei saa sellesse rolli määrata seni, kuni administraator välistuse eemaldab.</span><span class="sxs-lookup"><span data-stu-id="4967e-137">The excluded user isn't granted the access associated with the role and can't be assigned to the role until the administrator removes the exclusion.</span></span> 
-  <span data-ttu-id="4967e-138">**Luba määramine**: see alistab vastuolu ja kasutajale on võimalik määrata täiendav turberoll.</span><span class="sxs-lookup"><span data-stu-id="4967e-138">**Allow assignment**: This will override the conflict and allow the user to be assigned to the additional security role.</span></span> <span data-ttu-id="4967e-139">Kui alistate konflikti, siis peate sisestama põhjuse väljale **Alistamise põhjus**.</span><span class="sxs-lookup"><span data-stu-id="4967e-139">If you override a conflict, you must enter a reason in the **Reason for override** field.</span></span> <span data-ttu-id="4967e-140">Kõiki alistatud rollimääranguid saab vaadata lehel **Kohustuste jagamise konfliktid**.</span><span class="sxs-lookup"><span data-stu-id="4967e-140">All overridden role assignments can be viewed on the **Segregation of duties conflicts** page.</span></span>  

> [!NOTE]
> <span data-ttu-id="4967e-141">Kui sama kasutaja kohta on loetletud mitu konflikti, valige kasutajakirje ja hinnake lehel **Kasutajad** määratud rolle.</span><span class="sxs-lookup"><span data-stu-id="4967e-141">If several conflicts are listed for the same user, select the user record and evaluate assigned roles on the **Users** page.</span></span> <span data-ttu-id="4967e-142">Konflikti vältimiseks kontrollige iga reeglit pärast selle lisamist või muutmist.</span><span class="sxs-lookup"><span data-stu-id="4967e-142">To avoid this conflict, validate each rule after it's added or modified.</span></span>
