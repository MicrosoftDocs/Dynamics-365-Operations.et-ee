--- 
title: "Müügi komisjonitasu reeglite seadistamine"
description: "See protseduur selgitab, kuidas seadistada ja lubada müügi komisjonitasu arvutamist ning jälgimist."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0ab5b3b5447e56eb8ed012a67454400cb2357af4
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="9a32d-103">Müügi komisjonitasu reeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="9a32d-103">Set up sales commission rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a32d-104">See protseduur selgitab, kuidas seadistada ja lubada müügi komisjonitasu arvutamist ning jälgimist.</span><span class="sxs-lookup"><span data-stu-id="9a32d-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="9a32d-105">Samuti selgitab see, kuidas luua nii kliendi kui ka kauba komisjonigruppe ning linkida valitud klient ja toode vastavate gruppidega.</span><span class="sxs-lookup"><span data-stu-id="9a32d-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="9a32d-106">Seejärel kasutatakse neid gruppe komisjonitasu arvutamise seadistuses kliendi, kauba ja müügiesindajate kombinatsiooni loomiseks, mis tuleb vastendada müügitellimusega, et anda müügiisikutele õigus komisjonitasu saamiseks.</span><span class="sxs-lookup"><span data-stu-id="9a32d-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="9a32d-107">Kliendi ja kauba komisjonitasu gruppide loomine on valikuline, kuna komisjonitasu saab arvutada ka üksiku kliendi ja/või kauba kohta.</span><span class="sxs-lookup"><span data-stu-id="9a32d-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="9a32d-108">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="9a32d-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="9a32d-109">Komisjonitasu gruppide ja komisjonitasu määrade seadistamine</span><span class="sxs-lookup"><span data-stu-id="9a32d-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="9a32d-110">Tehke valik Müük ja turundus > Komisjonitasud > Komisjonitasu kliendigrupid.</span><span class="sxs-lookup"><span data-stu-id="9a32d-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="9a32d-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9a32d-111">Click New.</span></span>
3. <span data-ttu-id="9a32d-112">Sisestage väärtus väljale Grupp.</span><span class="sxs-lookup"><span data-stu-id="9a32d-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="9a32d-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9a32d-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9a32d-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9a32d-114">Click Save.</span></span>
6. <span data-ttu-id="9a32d-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a32d-115">Close the page.</span></span>
7. <span data-ttu-id="9a32d-116">Tehke valik Müük ja turundus > Komisjonitasud > Kaubagrupid.</span><span class="sxs-lookup"><span data-stu-id="9a32d-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="9a32d-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9a32d-117">Click New.</span></span>
9. <span data-ttu-id="9a32d-118">Sisestage väärtus väljale Grupp.</span><span class="sxs-lookup"><span data-stu-id="9a32d-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="9a32d-119">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9a32d-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="9a32d-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a32d-120">Close the page.</span></span>
12. <span data-ttu-id="9a32d-121">Tehke valik Müük ja turundus > Komisjonitasud > Müügigrupid.</span><span class="sxs-lookup"><span data-stu-id="9a32d-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="9a32d-122">Komisjonitasu müügigrupp määrab töötajad müügiesindaja rollis, kellel on õigus saada komisjonitasu, kui asjakohase müügigrupiga seostatud klient ostab teatud kaupu.</span><span class="sxs-lookup"><span data-stu-id="9a32d-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="9a32d-123">Demoettevõtte USMF andmetes on müügigrupp nimega USA müügiesindajad.</span><span class="sxs-lookup"><span data-stu-id="9a32d-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="9a32d-124">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="9a32d-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="9a32d-125">Klõpsake suvandit Müügiesindaja.</span><span class="sxs-lookup"><span data-stu-id="9a32d-125">Click Sales rep..</span></span>
    * <span data-ttu-id="9a32d-126">Müügiesindaja</span><span class="sxs-lookup"><span data-stu-id="9a32d-126">The Sales rep.</span></span> <span data-ttu-id="9a32d-127">lehel kuvatakse ettevõtte müügiinimesed, kes on seotud kindla komisjonitasu grupiga.</span><span class="sxs-lookup"><span data-stu-id="9a32d-127">page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="9a32d-128">Saate määrata mitu müügiesindajat samasse gruppi ja määratleda nende osa lõppkomisjonitasust protsentuaalselt.</span><span class="sxs-lookup"><span data-stu-id="9a32d-128">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="9a32d-129">Komisjonitasu kogumäär kõigi töötajate peale kokku ei tohi olla üle 100.</span><span class="sxs-lookup"><span data-stu-id="9a32d-129">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="9a32d-130">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="9a32d-130">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="9a32d-131">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9a32d-131">Click Edit.</span></span>
17. <span data-ttu-id="9a32d-132">Määrake komisjonitasu osaks 50.</span><span class="sxs-lookup"><span data-stu-id="9a32d-132">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="9a32d-133">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9a32d-133">Click New.</span></span>
19. <span data-ttu-id="9a32d-134">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9a32d-134">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="9a32d-135">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="9a32d-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9a32d-136">Näiteks saate filtreerida välja Nime väärtuse Susan Burk järgi.</span><span class="sxs-lookup"><span data-stu-id="9a32d-136">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="9a32d-137">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="9a32d-137">Click Select.</span></span>
22. <span data-ttu-id="9a32d-138">Määrake komisjonitasu osaks 50.</span><span class="sxs-lookup"><span data-stu-id="9a32d-138">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="9a32d-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9a32d-139">Click Save.</span></span>
24. <span data-ttu-id="9a32d-140">Tehke valik Müük ja turundus > Komisjonitasud > Komisjonitasu arvutamine.</span><span class="sxs-lookup"><span data-stu-id="9a32d-140">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="9a32d-141">Komisjonitasu arvutamise lehel saate määratleda komisjonitasu määra, mille töötaja saab müügikande eest, kui see sisaldab kliendi ja toote eelmääratud kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="9a32d-141">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="9a32d-142">Komisjonitasu määra seadistamise osana peate määrama komisjonitasu arvutamise aluse ja selle, kas see peaks sisaldama või välistama allahindlusi.</span><span class="sxs-lookup"><span data-stu-id="9a32d-142">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="9a32d-143">Saate sisestada ka kehtivusperioodi, mille vältel on komisjonitasu määr aktiivne.</span><span class="sxs-lookup"><span data-stu-id="9a32d-143">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="9a32d-144">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9a32d-144">Click New.</span></span>
26. <span data-ttu-id="9a32d-145">Valige väljalt Kaubakood suvand Grupp.</span><span class="sxs-lookup"><span data-stu-id="9a32d-145">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="9a32d-146">Klõpsake väljal Kauba seos otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9a32d-146">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="9a32d-147">Leidke ja valige loendist varem loodud grupp.</span><span class="sxs-lookup"><span data-stu-id="9a32d-147">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="9a32d-148">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9a32d-148">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="9a32d-149">Valige väljal Kliendikood suvand Grupp.</span><span class="sxs-lookup"><span data-stu-id="9a32d-149">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="9a32d-150">Klõpsake väljal Kliendi seos otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9a32d-150">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="9a32d-151">Valige loendist varem seadistatud grupp.</span><span class="sxs-lookup"><span data-stu-id="9a32d-151">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="9a32d-152">Müügiesindaja</span><span class="sxs-lookup"><span data-stu-id="9a32d-152">In the Sales rep.</span></span> <span data-ttu-id="9a32d-153">seose väljal klõpsake otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9a32d-153">relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="9a32d-154">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9a32d-154">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9a32d-155">Saate säilitada suvandi Enne rea allahindlust.</span><span class="sxs-lookup"><span data-stu-id="9a32d-155">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="9a32d-156">Saate säilitada komisjonitasu väärtuse arvutamise alusena suvandi Tulu.</span><span class="sxs-lookup"><span data-stu-id="9a32d-156">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="9a32d-157">Sisestage arv väljale Komisjonitasu protsent.</span><span class="sxs-lookup"><span data-stu-id="9a32d-157">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="9a32d-158">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9a32d-158">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="9a32d-159">Komisjonitasu sisestamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="9a32d-159">Setting up commission posting</span></span>
1. <span data-ttu-id="9a32d-160">Tehke valik Müük ja turundus > Komisjonitasud > Komisjonitasu sisestamine.</span><span class="sxs-lookup"><span data-stu-id="9a32d-160">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="9a32d-161">Komisjonitasud on töötajatele väljamakstavad ja seetõtu tuleb need seadistada, et tagada õige finantssisestus asjakohastele pearaamatu kontodele.</span><span class="sxs-lookup"><span data-stu-id="9a32d-161">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="9a32d-162">Seda tehakse komisjonitasu sisestamise lehel.</span><span class="sxs-lookup"><span data-stu-id="9a32d-162">This is done in the Commission posting page.</span></span> <span data-ttu-id="9a32d-163">Vaadake praeguse ettevõtte jaoks saadaolev seadistus üle.</span><span class="sxs-lookup"><span data-stu-id="9a32d-163">Review the setup that is available for the current company.</span></span> <span data-ttu-id="9a32d-164">Tavaliselt sisestatakse komisjonitasu summad spetsiaalsele kulukontole ja need on spetsiaalse ostureskontro vastaskontod.</span><span class="sxs-lookup"><span data-stu-id="9a32d-164">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="9a32d-165">Kui teil pole komisjonitasu sisestamisreeglid seadistatud, ei saa süsteem õigustatud komisjonitasudega müügitellimuse arveldust lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="9a32d-165">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="9a32d-166">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9a32d-166">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="9a32d-167">Kliendile ja tootele komisjonitasu grupi määramine</span><span class="sxs-lookup"><span data-stu-id="9a32d-167">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="9a32d-168">Tehke valik Müük ja turundus > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="9a32d-168">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="9a32d-169">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9a32d-169">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9a32d-170">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9a32d-170">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9a32d-171">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9a32d-171">Click Edit.</span></span>
5. <span data-ttu-id="9a32d-172">Laiendage jaotist Müügitellimuse vaikeandmed.</span><span class="sxs-lookup"><span data-stu-id="9a32d-172">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="9a32d-173">Klõpsake väljal Komisjonitasu grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9a32d-173">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9a32d-174">Valige loendist varem loodud grupp.</span><span class="sxs-lookup"><span data-stu-id="9a32d-174">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="9a32d-175">Klõpsake väljal Müügigrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9a32d-175">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="9a32d-176">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9a32d-176">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="9a32d-177">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9a32d-177">Click Save.</span></span>
11. <span data-ttu-id="9a32d-178">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="9a32d-178">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="9a32d-179">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="9a32d-179">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9a32d-180">Näiteks saate filtreerida välja Kaubakood väärtuse T0020 järgi.</span><span class="sxs-lookup"><span data-stu-id="9a32d-180">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="9a32d-181">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9a32d-181">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9a32d-182">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9a32d-182">Click Edit.</span></span>
15. <span data-ttu-id="9a32d-183">Laiendage jaotist Müük.</span><span class="sxs-lookup"><span data-stu-id="9a32d-183">Expand the Sell section.</span></span>
16. <span data-ttu-id="9a32d-184">Klõpsake väljal Komisjonitasu grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9a32d-184">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="9a32d-185">Valige loendist varem loodud komisjonitasu grupp.</span><span class="sxs-lookup"><span data-stu-id="9a32d-185">In the list, select the commission group that you created earlier.</span></span>


