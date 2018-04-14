--- 
title: Kanban-koguse soovituste arvutamine
description: See protseduur keskendub kanban-suuruse ja koguste optimeerimisele konkreetse kanban-reegli puhul, kasutades kanban-koguse arvutamist.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9ba09bfba52cd576782e61802e44fa4b80f4711f
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="d1ff9-103">Kanban-koguse soovituste arvutamine</span><span class="sxs-lookup"><span data-stu-id="d1ff9-103">Calculate kanban quantity suggestions</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1ff9-104">See protseduur keskendub kanban-suuruse ja koguste optimeerimisele konkreetse kanban-reegli puhul, kasutades kanban-koguse arvutamist.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="d1ff9-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d1ff9-106">See protseduur on mõeldud väärtuse voo haldurile.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="d1ff9-107">See on eeltingimus, et olete lõpetanud protseduuri Kanban-koguse arvutuspoliitika lisamine kanban-reeglile.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="d1ff9-108">Kanban-koguse arvutamise loomine</span><span class="sxs-lookup"><span data-stu-id="d1ff9-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="d1ff9-109">Avage Tootmise juhtimine > Perioodilised ülesanded > Kanban-koguse arvutamine > Kanban-koguse arvutamine.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="d1ff9-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-110">Click New.</span></span>
3. <span data-ttu-id="d1ff9-111">Sisestage väljale Nimi suvand Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="d1ff9-112">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d1ff9-113">Valige poliitika, mille olete loonud protseduuris Uue kanban-koguse arvutuspoliitika lisamine kanban-reeglile.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="d1ff9-114">Näiteks sisestage Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="d1ff9-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="d1ff9-116">Seadistage kuupäev ja kellaaeg väljal Reegli kehtivuse alguskuupäev väärtusele 2012-12-17T08:00:00.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="d1ff9-117">See kuupäev on nende fikseeritud kanban-reeglite määratlemise aluseks, mis lisatakse kanban-koguse arvutamisse.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="d1ff9-118">Seadistage kuupäev ja kellaaeg väljal Täidetud nõudlusperioodi alguskuupäev väärtusele 2012-11-17T09:00:00.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="d1ff9-119">Alguskuupäev, kui möödunud nõudluse kanded lisatakse kanban-koguse arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="d1ff9-120">Seadistage kuupäev ja kellaaeg väljal Täidetud nõudlusperioodi lõppkuupäev väärtusele 2012-12-17T07:59:59.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="d1ff9-121">Lõppkuupäev, milleni möödunud nõudluse kanded lisatakse kanban-koguse arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="d1ff9-122">Seadistage kuupäev ja kellaaeg väljal Nõudlusperioodi alguskuupäev väärtusele 2012-12-17T08:00:00.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="d1ff9-123">Alguskuupäev, millest alates praeguse nõudluse kanded lisatakse kanban-koguse arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="d1ff9-124">Seadistage kuupäev ja kellaaeg väljal Nõudlusperioodi lõppkuupäev väärtusele 2013-01-16T07:59:59.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="d1ff9-125">Lõppkuupäev, milleni praeguse nõudluse kanded lisatakse kanban-koguse arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="d1ff9-126">Kanban-koguse soovituse loomine</span><span class="sxs-lookup"><span data-stu-id="d1ff9-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="d1ff9-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-127">Click Save.</span></span>
2. <span data-ttu-id="d1ff9-128">Klõpsake suvandit Loo.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-128">Click Generate.</span></span>
    * <span data-ttu-id="d1ff9-129">See loob kanban-koguse soovituse rea kanban-reegli 000020 puhul.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="d1ff9-130">Kanban-koguse arvutamise käivitamine</span><span class="sxs-lookup"><span data-stu-id="d1ff9-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="d1ff9-131">Klõpsake valikut Arvuta.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-131">Click Calculate.</span></span>
    * <span data-ttu-id="d1ff9-132">See arvutab kanban-koguse soovituse.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="d1ff9-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-133">Click OK.</span></span>
3. <span data-ttu-id="d1ff9-134">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d1ff9-135">Pange tähele, et soovitatud kanban-kogus on 2.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="d1ff9-136">Toote koguse muutmine ja uuesti arvutamine</span><span class="sxs-lookup"><span data-stu-id="d1ff9-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="d1ff9-137">Määrake toote koguseks 5.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="d1ff9-138">Klõpsake valikut Arvuta.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-138">Click Calculate.</span></span>
3. <span data-ttu-id="d1ff9-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-139">Click OK.</span></span>
    * <span data-ttu-id="d1ff9-140">Pange tähele, et kanban-kogusega 5 muudetakse soovitus kanban-kogusele 4.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="d1ff9-141">Põhjuseks on see, et väiksema toote kogusega on nõudluse täitmiseks vaja rohkem kanbane.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="d1ff9-142">Kanban-reegli värskendamine</span><span class="sxs-lookup"><span data-stu-id="d1ff9-142">Update kanban rule</span></span>
1. <span data-ttu-id="d1ff9-143">Sisestage kuupäev ja kellaaeg väljale Reegli jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="d1ff9-144">Määrake suvandi Reegli kehtivuse alguskuupäev puhul kuupäev tulevikku.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="d1ff9-145">Näiteks täna + üks aasta.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="d1ff9-146">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-146">Click Update.</span></span>
3. <span data-ttu-id="d1ff9-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-147">Click OK.</span></span>
4. <span data-ttu-id="d1ff9-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="d1ff9-149">Kanban-reegli muudatuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="d1ff9-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="d1ff9-150">Avage Tooteteabe haldus > Lean manufacturing > Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="d1ff9-151">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d1ff9-152">Valige eelmises alamülesandes loodud kanban-reegel.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="d1ff9-153">See peaks olema loendi esimene kanban-reegel, mis on sorditud numbri järgi.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="d1ff9-154">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="d1ff9-155">Pange tähele jõustumiskuupäeva, mis tähendab, et seda reeglit ei aktiveerita kuni selle kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="d1ff9-156">Laiendage jaotist Kogused.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="d1ff9-157">Pange tähele, et see on kanban-koguse arvutamisse sisestatud vaikekogus.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="d1ff9-158">Pange tähele, et see on fikseeritud kanban-kogus 4 kanban-koguse arvutamisest.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="d1ff9-159">Klõpsake vahekaarti ListPanel.</span><span class="sxs-lookup"><span data-stu-id="d1ff9-159">Click the ListPanel tab.</span></span>


