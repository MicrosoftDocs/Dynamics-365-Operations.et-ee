---
title: Töötaja soodustuste programmi pakkumine
description: Selles artiklis näidatakse, kuidas luua soodustuse elemente, mida uue soodustuse loomisel kasutakse.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: b8631e4f8cb2947ec7e09de86a7ceb075a83a453
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008818"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="bffa8-103">Töötaja soodustuste programmi pakkumine</span><span class="sxs-lookup"><span data-stu-id="bffa8-103">Deliver employee benefits program</span></span>

<span data-ttu-id="bffa8-104">Selles artiklis näidatakse, kuidas luua soodustuse elemente, mida uue soodustuse loomisel kasutakse.</span><span class="sxs-lookup"><span data-stu-id="bffa8-104">This article shows you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="bffa8-105">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="bffa8-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="bffa8-106">See ülesanne on mõeldud hüvitise ja eeliste haldurile.</span><span class="sxs-lookup"><span data-stu-id="bffa8-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="bffa8-107">Soodustuse elementide loomine</span><span class="sxs-lookup"><span data-stu-id="bffa8-107">Create benefit elements</span></span>
1. <span data-ttu-id="bffa8-108">See ülesanne algab leheküljelt Soodustuste loend.</span><span class="sxs-lookup"><span data-stu-id="bffa8-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="bffa8-109">Ülesande täitmise alustamiseks avage see leht või otsige lehekülge Soodustuste loend.</span><span class="sxs-lookup"><span data-stu-id="bffa8-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="bffa8-110">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="bffa8-110">Click New.</span></span>
3. <span data-ttu-id="bffa8-111">Sisestage loodava soodustuse tüüp väljale Tüüp.</span><span class="sxs-lookup"><span data-stu-id="bffa8-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="bffa8-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="bffa8-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bffa8-113">Valige suvand väljal Samaaegne registreerimine.</span><span class="sxs-lookup"><span data-stu-id="bffa8-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="bffa8-114">Töötajate mitmesse meditsiiniplaani registreerumise vältimiseks valige Üks registreerimine tüübi kohta.</span><span class="sxs-lookup"><span data-stu-id="bffa8-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="bffa8-115">Valige suvand väljal Palgakategooria.</span><span class="sxs-lookup"><span data-stu-id="bffa8-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="bffa8-116">Klõpsake vahekaardil Plaanid.</span><span class="sxs-lookup"><span data-stu-id="bffa8-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="bffa8-117">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="bffa8-117">Click New.</span></span>
9. <span data-ttu-id="bffa8-118">Sisestage väärtus väljale Plaan.</span><span class="sxs-lookup"><span data-stu-id="bffa8-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="bffa8-119">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="bffa8-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="bffa8-120">Klõpsake väljal Tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bffa8-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="bffa8-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bffa8-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="bffa8-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bffa8-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="bffa8-123">Valige suvand väljal Palga mõju.</span><span class="sxs-lookup"><span data-stu-id="bffa8-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="bffa8-124">Klõpsake vahekaarti Suvandid.</span><span class="sxs-lookup"><span data-stu-id="bffa8-124">Click the Options tab.</span></span>
16. <span data-ttu-id="bffa8-125">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="bffa8-125">Click New.</span></span>
17. <span data-ttu-id="bffa8-126">Sisestage väärtus väljale Suvand.</span><span class="sxs-lookup"><span data-stu-id="bffa8-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="bffa8-127">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="bffa8-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="bffa8-128">Soodustuse loomine</span><span class="sxs-lookup"><span data-stu-id="bffa8-128">Create a benefit</span></span>
1. <span data-ttu-id="bffa8-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bffa8-129">Close the page.</span></span>
2. <span data-ttu-id="bffa8-130">Avage Personaliarvestus > Soodustused > Soodustused.</span><span class="sxs-lookup"><span data-stu-id="bffa8-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="bffa8-131">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bffa8-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="bffa8-132">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bffa8-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="bffa8-133">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bffa8-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="bffa8-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bffa8-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="bffa8-135">Klõpsake väljal Suvand otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bffa8-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bffa8-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bffa8-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="bffa8-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bffa8-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="bffa8-138">Sisestage jõustumiskuupäev ja -kellaaeg väljale Jõustunud.</span><span class="sxs-lookup"><span data-stu-id="bffa8-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="bffa8-139">Klõpsake valikut Loo soodustus.</span><span class="sxs-lookup"><span data-stu-id="bffa8-139">Click Create benefit.</span></span>
12. <span data-ttu-id="bffa8-140">Lülitage jaotise Palga üksikasjad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="bffa8-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="bffa8-141">Klõpsake väljal Sagedus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bffa8-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="bffa8-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bffa8-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="bffa8-143">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bffa8-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="bffa8-144">Valige suvand väljal Alus.</span><span class="sxs-lookup"><span data-stu-id="bffa8-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="bffa8-145">Sisestage arv väljale Summa või määr.</span><span class="sxs-lookup"><span data-stu-id="bffa8-145">In the Amount or rate field, enter a number.</span></span>
