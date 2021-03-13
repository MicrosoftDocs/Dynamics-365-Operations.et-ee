---
title: Hüvitise struktuuri arendamine
description: See artikkel annab ülevaate põhipalga plaani loomisest ja sobivusreeglite abil töötajate plaani lisamisest.
author: andreabichsel
manager: tfehr
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a5e7ef2021e41c13b82523f2dc6a1b09bd1ba9f
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115892"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="89cfc-103">Hüvitise struktuuri arendamine</span><span class="sxs-lookup"><span data-stu-id="89cfc-103">Develop a compensation structure</span></span>

<span data-ttu-id="89cfc-104">See artikkel annab ülevaate põhipalga plaani loomisest ja sobivusreeglite abil töötajate plaani lisamisest.</span><span class="sxs-lookup"><span data-stu-id="89cfc-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="89cfc-105">See artikkel kasutab USMF-i demoandmeid ja kehtib hüvitise ja soodustuste halduritele.</span><span class="sxs-lookup"><span data-stu-id="89cfc-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="89cfc-106">Põhipalga plaani loomine</span><span class="sxs-lookup"><span data-stu-id="89cfc-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="89cfc-107">Valige suvand **Hüvituste haldus**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="89cfc-108">Valige suvand **Põhipalga plaanid**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="89cfc-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-109">Select **New**.</span></span>

4. <span data-ttu-id="89cfc-110">Sisestage väärtus väljale **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="89cfc-111">Sisestage väärtus väljal **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="89cfc-112">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="89cfc-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="89cfc-113">Väljal **Tüüp** valige, kas põhipalgaplaan on **rea-**, **klassi-** või **etapiplaan**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="89cfc-114">Märkeruut **Soovitamine lubatud** toimib protsessi sündmusena plaani lisatud mistahes tegevuse vaikeväärtusena.</span><span class="sxs-lookup"><span data-stu-id="89cfc-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="89cfc-115">Tasu töötlemisel saate soovituste lubamisega tühistada arvutatud juhise summa.</span><span class="sxs-lookup"><span data-stu-id="89cfc-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="89cfc-116">Väli **Vahemikust väljajäämise tolerants** võimaldab määrata, kuidas käsitletakse tasusummasid, mis ei kuulu antud tasemel määratletud tasustruktuuri vahemikku.</span><span class="sxs-lookup"><span data-stu-id="89cfc-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="89cfc-117">Välja **Vahemikust väljajäämise tolerants** määramine suvandile **Puudub** võimaldab kasutada mis tahes hüvitise summat.</span><span class="sxs-lookup"><span data-stu-id="89cfc-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="89cfc-118">Suvand **Paindlik tolerants** hoiatab kasutajaid, kui hüvitise summa on selle taseme viitepunkti summade miinimumist väiksem või maksimumist suurem.</span><span class="sxs-lookup"><span data-stu-id="89cfc-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="89cfc-119">Kasutajad võivad hoiatust ignoreerida ja jätkata.</span><span class="sxs-lookup"><span data-stu-id="89cfc-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="89cfc-120">Valik **Jäik tolerants** annab tõrketeate, kui töötaja tasu jääb väljapoole taseme minimaalset või maksimaalset viitepunkti ning töötaja tasu korrigeeritakse automaatselt määratud vahemikku.</span><span class="sxs-lookup"><span data-stu-id="89cfc-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="89cfc-121">Väli **Palkamise reegel** arvutab protsessi sündmuse ajal töötaja hüvitise.</span><span class="sxs-lookup"><span data-stu-id="89cfc-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="89cfc-122">Suvandi **Palkamise reegel** valik **Protsent** arvutab tõusu, mis jaotub proportsionaalselt töötaja töötamise ajale.</span><span class="sxs-lookup"><span data-stu-id="89cfc-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="89cfc-123">Sisestage väärtus väljale **Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="89cfc-124">Sisestage või valige väärtus väljal **Palgamäära teisendamine**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="89cfc-125">Laiendage jaotist **Palgavahemiku kasutusastme maatriks**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="89cfc-126">Valikuliselt saate lisada palgavahemiku kasutusastme kirjed, et töötajad jõuaksid kiiremini keskpunkti ja aeglasemalt maksimaalsesse vahemikku.</span><span class="sxs-lookup"><span data-stu-id="89cfc-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="89cfc-127">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-127">Select **Save**.</span></span> <span data-ttu-id="89cfc-128">See aktiveerib nupu **Hüvitise seadistamine** nupu ja võimaldab jätkata plaani hüvitise struktuuri määratlemisega.</span><span class="sxs-lookup"><span data-stu-id="89cfc-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="89cfc-129">Valige suvand **Hüvitise seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-129">Select **Set up compensation**.</span></span> <span data-ttu-id="89cfc-130">Saate luua hüvitise struktuuri kasutades üht järgmise kolme viisi seast.</span><span class="sxs-lookup"><span data-stu-id="89cfc-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="89cfc-131">Looge täiesti uus struktuur, valides viitepunktide komplekti ja lisades tasemed, et luua oma struktuur.</span><span class="sxs-lookup"><span data-stu-id="89cfc-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="89cfc-132">Kopeerige hüvitise struktuur olemasolevast plaanist lähtepunktina kasutamiseks ja muutke seda uue plaani jaoks.</span><span class="sxs-lookup"><span data-stu-id="89cfc-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="89cfc-133">Valige olemasolev hüvitise ruudustik.</span><span class="sxs-lookup"><span data-stu-id="89cfc-133">Select an existing compensation grid.</span></span> <span data-ttu-id="89cfc-134">Kui mõni muu plaan juba kasutab hüvitise ruudustikku, kajastuvad kõik ruudustikus tehtud muudatused ka teises plaanis.</span><span class="sxs-lookup"><span data-stu-id="89cfc-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="89cfc-135">Valige suvand **Loo uus olemasolevast tasumaatriksist**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="89cfc-136">Sisestage või valige väärtus väljal **Kopeeri ruudustikust**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="89cfc-137">Teise võimalusena saate muuta uue hüvitise ruudustiku nime, mille valitud ruudustiku kopeerimisega lõite.</span><span class="sxs-lookup"><span data-stu-id="89cfc-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="89cfc-138">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-138">Select **OK**.</span></span>

19. <span data-ttu-id="89cfc-139">Valige suvand **Massmuudatus**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-139">Select **Mass change**.</span></span> <span data-ttu-id="89cfc-140">**Massmuudatus** võimaldab teil säilitada hüvitise maatriksi summad, tõstes üht või mitut taset ja/või viitepunkti protsendi või kindla summa võrra.</span><span class="sxs-lookup"><span data-stu-id="89cfc-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="89cfc-141">Sisestage arv väljale **Korrigeerimissumma**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="89cfc-142">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="89cfc-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="89cfc-143">Klõpsake käsku **Rakenda ruudustikule**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="89cfc-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="89cfc-144">Close the page.</span></span> <span data-ttu-id="89cfc-145">Pärast hüvitise struktuuri loomist saate valida, milliseid viitepunkte põhipalgaplaani kontrollpunktina kasutada.</span><span class="sxs-lookup"><span data-stu-id="89cfc-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="89cfc-146">Kontrollpunkti kasutatakse töötaja võrdlusteguri arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="89cfc-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="89cfc-147">Sisestage või valige väärtus väljal **Kontrollpunkt**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="89cfc-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="89cfc-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="89cfc-149">Põhipalgaplaanile sobivuse reegli loomine</span><span class="sxs-lookup"><span data-stu-id="89cfc-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="89cfc-150">Te ei saa põhipalgaplaani töötajale määrata enne, kui määratlete plaani jaoks on sobivuse reeglid.</span><span class="sxs-lookup"><span data-stu-id="89cfc-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="89cfc-151">Valige suvand **Sobivuse reeglid**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="89cfc-152">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-152">Select **New**.</span></span>

3. <span data-ttu-id="89cfc-153">Sisestage väärtus väljal **Sobivus**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="89cfc-154">Sisestage väärtus väljal **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="89cfc-155">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="89cfc-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="89cfc-156">Nii põhipalga kui ka tulemustasu plaanid kasutavad sobivuse reegleid.</span><span class="sxs-lookup"><span data-stu-id="89cfc-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="89cfc-157">Valige plaani tüüp väljal **Tüüp**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="89cfc-158">Sisestage või valige väärtus väljal **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="89cfc-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="89cfc-159">Valige, millistele kriteeriumidele peab tasuplaanile sobiv töötaja vastama.</span><span class="sxs-lookup"><span data-stu-id="89cfc-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="89cfc-160">Kriteeriumid võivad hõlmata järgmist.</span><span class="sxs-lookup"><span data-stu-id="89cfc-160">Criteria can include:</span></span>

    - <span data-ttu-id="89cfc-161">**Osakond**</span><span class="sxs-lookup"><span data-stu-id="89cfc-161">**Department**</span></span>
    - <span data-ttu-id="89cfc-162">**Ametiühing**</span><span class="sxs-lookup"><span data-stu-id="89cfc-162">**Labor union**</span></span>
    - <span data-ttu-id="89cfc-163">**Asukoht** (**Hüvituspiirkond**)</span><span class="sxs-lookup"><span data-stu-id="89cfc-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="89cfc-164">**Töö**</span><span class="sxs-lookup"><span data-stu-id="89cfc-164">**Job**</span></span>
    - <span data-ttu-id="89cfc-165">**Funktsioon**</span><span class="sxs-lookup"><span data-stu-id="89cfc-165">**Function**</span></span>
    - <span data-ttu-id="89cfc-166">**Töö tüüp**</span><span class="sxs-lookup"><span data-stu-id="89cfc-166">**Job type**</span></span>
    - <span data-ttu-id="89cfc-167">**Hüvituse tase**</span><span class="sxs-lookup"><span data-stu-id="89cfc-167">**Compensation level**</span></span>
    
    <span data-ttu-id="89cfc-168">Töötaja on tasuplaani jaoks sobiv, kui ta vastab kõigile määratud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="89cfc-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="89cfc-169">Kui te ühtegi kriteeriumit ei määra, on kõik töötajad hüvitusplaani jaoks sobilikud.</span><span class="sxs-lookup"><span data-stu-id="89cfc-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="89cfc-170">Kui töötaja ei vasta sobivuse reeglis määratletud kriteeriumitele või sobivuse reeglit ei ole hüvitusplaani jaoks määratletud, siis töötaja jaoks põhipalga kirje loomisel ei kuvata hüvitusplaani otsingus.</span><span class="sxs-lookup"><span data-stu-id="89cfc-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="89cfc-171">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="89cfc-171">Close the page.</span></span>

8. <span data-ttu-id="89cfc-172">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="89cfc-172">Close the page.</span></span>

