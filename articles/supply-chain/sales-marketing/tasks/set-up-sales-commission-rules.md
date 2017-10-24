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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8d81765884f741443d1c0f5b0cb8bc545945e1a1
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="82d17-103">Müügi komisjonitasu reeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="82d17-103">Set up sales commission rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82d17-104">See protseduur selgitab, kuidas seadistada ja lubada müügi komisjonitasu arvutamist ning jälgimist.</span><span class="sxs-lookup"><span data-stu-id="82d17-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="82d17-105">Samuti selgitab see, kuidas luua nii kliendi kui ka kauba komisjonigruppe ning linkida valitud klient ja toode vastavate gruppidega.</span><span class="sxs-lookup"><span data-stu-id="82d17-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="82d17-106">Seejärel kasutatakse neid gruppe komisjonitasu arvutamise seadistuses kliendi, kauba ja müügiesindajate kombinatsiooni loomiseks, mis tuleb vastendada müügitellimusega, et anda müügiisikutele õigus komisjonitasu saamiseks.</span><span class="sxs-lookup"><span data-stu-id="82d17-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="82d17-107">Kliendi ja kauba komisjonitasu gruppide loomine on valikuline, kuna komisjonitasu saab arvutada ka üksiku kliendi ja/või kauba kohta.</span><span class="sxs-lookup"><span data-stu-id="82d17-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="82d17-108">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="82d17-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="82d17-109">Komisjonitasu gruppide ja komisjonitasu määrade seadistamine</span><span class="sxs-lookup"><span data-stu-id="82d17-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="82d17-110">Tehke valik Müük ja turundus > Komisjonitasud > Komisjonitasu kliendigrupid.</span><span class="sxs-lookup"><span data-stu-id="82d17-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="82d17-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="82d17-111">Click New.</span></span>
3. <span data-ttu-id="82d17-112">Sisestage väärtus väljale Grupp.</span><span class="sxs-lookup"><span data-stu-id="82d17-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="82d17-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="82d17-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="82d17-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="82d17-114">Click Save.</span></span>
6. <span data-ttu-id="82d17-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="82d17-115">Close the page.</span></span>
7. <span data-ttu-id="82d17-116">Tehke valik Müük ja turundus > Komisjonitasud > Kaubagrupid.</span><span class="sxs-lookup"><span data-stu-id="82d17-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="82d17-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="82d17-117">Click New.</span></span>
9. <span data-ttu-id="82d17-118">Sisestage väärtus väljale Grupp.</span><span class="sxs-lookup"><span data-stu-id="82d17-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="82d17-119">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="82d17-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="82d17-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="82d17-120">Close the page.</span></span>
12. <span data-ttu-id="82d17-121">Tehke valik Müük ja turundus > Komisjonitasud > Müügigrupid.</span><span class="sxs-lookup"><span data-stu-id="82d17-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="82d17-122">Komisjonitasu müügigrupp määrab töötajad müügiesindaja rollis, kellel on õigus saada komisjonitasu, kui asjakohase müügigrupiga seostatud klient ostab teatud kaupu.</span><span class="sxs-lookup"><span data-stu-id="82d17-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="82d17-123">Demoettevõtte USMF andmetes on müügigrupp nimega USA müügiesindajad.</span><span class="sxs-lookup"><span data-stu-id="82d17-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="82d17-124">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="82d17-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="82d17-125">Klõpsake suvandit Müügiesindaja.</span><span class="sxs-lookup"><span data-stu-id="82d17-125">Click Sales rep..</span></span>
    * <span data-ttu-id="82d17-126">Müügiaruande lehel kuvatakse ettevõtte müügiinimesed, kes on seotud kindla komisjonitasu grupiga.</span><span class="sxs-lookup"><span data-stu-id="82d17-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="82d17-127">Saate määrata mitu müügiesindajat samasse gruppi ja määratleda nende osa lõppkomisjonitasust protsentuaalselt.</span><span class="sxs-lookup"><span data-stu-id="82d17-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="82d17-128">Komisjonitasu kogumäär kõigi töötajate peale kokku ei tohi olla üle 100.</span><span class="sxs-lookup"><span data-stu-id="82d17-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="82d17-129">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="82d17-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="82d17-130">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="82d17-130">Click Edit.</span></span>
17. <span data-ttu-id="82d17-131">Määrake komisjonitasu osaks 50.</span><span class="sxs-lookup"><span data-stu-id="82d17-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="82d17-132">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="82d17-132">Click New.</span></span>
19. <span data-ttu-id="82d17-133">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="82d17-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="82d17-134">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="82d17-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="82d17-135">Näiteks saate filtreerida välja Nime väärtuse Susan Burk järgi.</span><span class="sxs-lookup"><span data-stu-id="82d17-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="82d17-136">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="82d17-136">Click Select.</span></span>
22. <span data-ttu-id="82d17-137">Määrake komisjonitasu osaks 50.</span><span class="sxs-lookup"><span data-stu-id="82d17-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="82d17-138">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="82d17-138">Click Save.</span></span>
24. <span data-ttu-id="82d17-139">Tehke valik Müük ja turundus > Komisjonitasud > Komisjonitasu arvutamine.</span><span class="sxs-lookup"><span data-stu-id="82d17-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="82d17-140">Komisjonitasu arvutamise lehel saate määratleda komisjonitasu määra, mille töötaja saab müügikande eest, kui see sisaldab kliendi ja toote eelmääratud kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="82d17-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="82d17-141">Komisjonitasu määra seadistamise osana peate määrama komisjonitasu arvutamise aluse ja selle, kas see peaks sisaldama või välistama allahindlusi.</span><span class="sxs-lookup"><span data-stu-id="82d17-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="82d17-142">Saate sisestada ka kehtivusperioodi, mille vältel on komisjonitasu määr aktiivne.</span><span class="sxs-lookup"><span data-stu-id="82d17-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="82d17-143">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="82d17-143">Click New.</span></span>
26. <span data-ttu-id="82d17-144">Valige väljalt Kaubakood suvand Grupp.</span><span class="sxs-lookup"><span data-stu-id="82d17-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="82d17-145">Klõpsake väljal Kauba seos otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="82d17-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="82d17-146">Leidke ja valige loendist varem loodud grupp.</span><span class="sxs-lookup"><span data-stu-id="82d17-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="82d17-147">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="82d17-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="82d17-148">Valige väljal Kliendikood suvand Grupp.</span><span class="sxs-lookup"><span data-stu-id="82d17-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="82d17-149">Klõpsake väljal Kliendi seos otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="82d17-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="82d17-150">Valige loendist varem seadistatud grupp.</span><span class="sxs-lookup"><span data-stu-id="82d17-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="82d17-151">Väljal Müügiesindaja seos klõpsake otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="82d17-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="82d17-152">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="82d17-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="82d17-153">Saate säilitada suvandi Enne rea allahindlust.</span><span class="sxs-lookup"><span data-stu-id="82d17-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="82d17-154">Saate säilitada komisjonitasu väärtuse arvutamise alusena suvandi Tulu.</span><span class="sxs-lookup"><span data-stu-id="82d17-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="82d17-155">Sisestage arv väljale Komisjonitasu protsent.</span><span class="sxs-lookup"><span data-stu-id="82d17-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="82d17-156">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="82d17-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="82d17-157">Komisjonitasu sisestamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="82d17-157">Setting up commission posting</span></span>
1. <span data-ttu-id="82d17-158">Tehke valik Müük ja turundus > Komisjonitasud > Komisjonitasu sisestamine.</span><span class="sxs-lookup"><span data-stu-id="82d17-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="82d17-159">Komisjonitasud on töötajatele väljamakstavad ja seetõtu tuleb need seadistada, et tagada õige finantssisestus asjakohastele pearaamatu kontodele.</span><span class="sxs-lookup"><span data-stu-id="82d17-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="82d17-160">Seda tehakse komisjonitasu sisestamise lehel.</span><span class="sxs-lookup"><span data-stu-id="82d17-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="82d17-161">Vaadake praeguse ettevõtte jaoks saadaolev seadistus üle.</span><span class="sxs-lookup"><span data-stu-id="82d17-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="82d17-162">Tavaliselt sisestatakse komisjonitasu summad spetsiaalsele kulukontole ja need on spetsiaalse ostureskontro vastaskontod.</span><span class="sxs-lookup"><span data-stu-id="82d17-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="82d17-163">Kui teil pole komisjonitasu sisestamisreeglid seadistatud, ei saa süsteem õigustatud komisjonitasudega müügitellimuse arveldust lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="82d17-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="82d17-164">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="82d17-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="82d17-165">Kliendile ja tootele komisjonitasu grupi määramine</span><span class="sxs-lookup"><span data-stu-id="82d17-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="82d17-166">Tehke valik Müük ja turundus > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="82d17-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="82d17-167">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="82d17-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="82d17-168">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="82d17-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="82d17-169">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="82d17-169">Click Edit.</span></span>
5. <span data-ttu-id="82d17-170">Laiendage jaotist Müügitellimuse vaikeandmed.</span><span class="sxs-lookup"><span data-stu-id="82d17-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="82d17-171">Klõpsake väljal Komisjonitasu grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="82d17-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="82d17-172">Valige loendist varem loodud grupp.</span><span class="sxs-lookup"><span data-stu-id="82d17-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="82d17-173">Klõpsake väljal Müügigrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="82d17-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="82d17-174">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="82d17-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="82d17-175">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="82d17-175">Click Save.</span></span>
11. <span data-ttu-id="82d17-176">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="82d17-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="82d17-177">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="82d17-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="82d17-178">Näiteks saate filtreerida välja Kaubakood väärtuse T0020 järgi.</span><span class="sxs-lookup"><span data-stu-id="82d17-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="82d17-179">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="82d17-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="82d17-180">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="82d17-180">Click Edit.</span></span>
15. <span data-ttu-id="82d17-181">Laiendage jaotist Müük.</span><span class="sxs-lookup"><span data-stu-id="82d17-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="82d17-182">Klõpsake väljal Komisjonitasu grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="82d17-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="82d17-183">Valige loendist varem loodud komisjonitasu grupp.</span><span class="sxs-lookup"><span data-stu-id="82d17-183">In the list, select the commission group that you created earlier.</span></span>


