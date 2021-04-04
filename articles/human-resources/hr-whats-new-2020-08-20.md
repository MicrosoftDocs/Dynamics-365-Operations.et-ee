---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (20. august 2020)?
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 20. augusti 2020 uusi või muutunud funktsioone.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d964f9a532582b18471550a68032d00e19a065c4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467261"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a><span data-ttu-id="0178b-103">Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (20. august 2020)?</span><span class="sxs-lookup"><span data-stu-id="0178b-103">What's new or changed in Dynamics 365 Human Resources (August 20, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0178b-104">Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="0178b-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0178b-105">Muudatused rakenduvad versioonile number 8.1.3478.</span><span class="sxs-lookup"><span data-stu-id="0178b-105">Changes apply to build number 8.1.3478.</span></span> <span data-ttu-id="0178b-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="0178b-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a><span data-ttu-id="0178b-107">Eelseisvate ja ootel puhkuste teabe kuvamine tööruumi Inimesed kaartidel</span><span class="sxs-lookup"><span data-stu-id="0178b-107">Show upcoming and pending leave of absence information to cards in People workspace</span></span>

<span data-ttu-id="0178b-108">Ootel ja eelseisva puhkusetaotluse suvandid on nüüd saadaval tööruumi **Inimesed** kaartidel Puhkus ja puudumine.</span><span class="sxs-lookup"><span data-stu-id="0178b-108">Pending and upcoming leave request options are now available on the Leave and absence cards in the **People** workspace.</span></span>

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a><span data-ttu-id="0178b-109">Isiklik väli pole töövõtja rolli jaoks töövõtja iseteeninduses (477106) vaikimisi Jah</span><span class="sxs-lookup"><span data-stu-id="0178b-109">Private field isn't Yes by default for Employee role in Employee self service (477106)</span></span>

<span data-ttu-id="0178b-110">Välja **Privaatne** vaikeväärtus on nüüd **Jah**, kui töövõtjad lisavad uue aadressikirje töövõtja iseteeninduse lehe **Isikuandmed** lehe kaudu.</span><span class="sxs-lookup"><span data-stu-id="0178b-110">The **Private** field now defaults to **Yes** when employees add new address records through the **Personal information** page in Employee self service.</span></span> 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a><span data-ttu-id="0178b-111">Personalihalduse palgatavate kandidaatide kiirkaardil kuvatakse kandidaatide vale arv (470110)</span><span class="sxs-lookup"><span data-stu-id="0178b-111">Candidates to hire FastTab in Personnel management shows an incorrect count of candidates (470110)</span></span>

<span data-ttu-id="0178b-112">Lehel **Personalihaldus** kuvatakse nüüd palgatavate kandidaatide õige arv.</span><span class="sxs-lookup"><span data-stu-id="0178b-112">The **Personnel management** page now accurately displays the number of candidates to hire.</span></span> 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a><span data-ttu-id="0178b-113">Lõpetatud lepinguga töövõtja haigust ei saa sisestada, kui viitvõlgade väärtuseks on seatud null (446195)</span><span class="sxs-lookup"><span data-stu-id="0178b-113">Can’t enter sickness for terminated employee when accrual is set to zero (446195)</span></span>

<span data-ttu-id="0178b-114">Puhkusekanded on nüüd lubatud töötajate jaoks, kelle tööleping lõpeb tulevikus ja viitvõlgade väärtuseks on seatud null.</span><span class="sxs-lookup"><span data-stu-id="0178b-114">Leave transactions are now allowed for employees that have been terminated in the future and the accrual is set to zero.</span></span> <span data-ttu-id="0178b-115">Puhkusekandeid saab sisestada kuni töövõtjaga lepingu lõpetamise kuupäevani.</span><span class="sxs-lookup"><span data-stu-id="0178b-115">Leave transactions can be entered up to the termination date of the employee.</span></span> 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a><span data-ttu-id="0178b-116">Kohandatud väljade lisamine uuele töövõtjavormile keelab puhkuse haldamise toimingupaani väljad (473314)</span><span class="sxs-lookup"><span data-stu-id="0178b-116">Adding custom fields to the new Worker form disables the fields in the action pane for Manage leave (473314)</span></span>

<span data-ttu-id="0178b-117">Toimingupaani suvandid lehe **Puhkuste haldus** uuel vormil **Töövõtja** pole enam keelatud, kui vormile **Töövõtja** on lisatud kohandatud väljad.</span><span class="sxs-lookup"><span data-stu-id="0178b-117">Action pane options on the new **Worker** form in **Manage leave** will no longer be disabled if custom fields have been added to the new **Worker** form.</span></span>

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a><span data-ttu-id="0178b-118">Puhkuse kommentaarivälja kohustuslikuks muutmine võimaldab puhkusetaotlust edastada kommentaari lisamata (473543)</span><span class="sxs-lookup"><span data-stu-id="0178b-118">Making the Leave comment field mandatory allows a leave request to be submitted when no comment is entered (473543)</span></span>

<span data-ttu-id="0178b-119">Kommentaarväljad saavad olla nüüd kohustuslikud ja puhkusetaotlused saavad seda sätet kasutada.</span><span class="sxs-lookup"><span data-stu-id="0178b-119">Comment fields can now be mandatory, and leave requests honor this setting.</span></span> <span data-ttu-id="0178b-120">Kohustuslik väli on eelversioonifunktsioon.</span><span class="sxs-lookup"><span data-stu-id="0178b-120">Mandatory fields is a preview feature.</span></span>

### <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="0178b-121">DMF-üksus on saadaval lisandumise peatamiseks</span><span class="sxs-lookup"><span data-stu-id="0178b-121">DMF entity available for accrual suspensions</span></span>

<span data-ttu-id="0178b-122">Nüüdsest on lisandumise peatamiseks saadaval DMF-üksus.</span><span class="sxs-lookup"><span data-stu-id="0178b-122">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="in-preview"></a><span data-ttu-id="0178b-123">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="0178b-123">In preview</span></span>

### <a name="mandatory-fields"></a><span data-ttu-id="0178b-124">Kohustuslikud väljad</span><span class="sxs-lookup"><span data-stu-id="0178b-124">Mandatory fields</span></span>

<span data-ttu-id="0178b-125">Saate muuta väljasid kohustuslikuks Human Resourcesi isikupärastamise võimaluste abil.</span><span class="sxs-lookup"><span data-stu-id="0178b-125">You can make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="0178b-126">See funktsioon nõuab **Salvestatud vaateid**.</span><span class="sxs-lookup"><span data-stu-id="0178b-126">This feature requires **Saved views**.</span></span> <span data-ttu-id="0178b-127">Lisateavet salvestatud vaadete kohta leiate siit.</span><span class="sxs-lookup"><span data-stu-id="0178b-127">For more information about saved views, see:</span></span>

- <span data-ttu-id="0178b-128">[Salvestatud vaated – üldine kättesaadavus](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis</span><span class="sxs-lookup"><span data-stu-id="0178b-128">[Saved views - general availability](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) in the Dynamics 365 2020 release wave 2 plan</span></span>
- [<span data-ttu-id="0178b-129">Koostage vorme, mis täielikult kasutavad salvestatud vaateid</span><span class="sxs-lookup"><span data-stu-id="0178b-129">Build forms that fully utilize saved views</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="0178b-130">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="0178b-130">Human Resources application in Teams</span></span>

<span data-ttu-id="0178b-131">Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="0178b-131">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="0178b-132">Nad saavad suhelda botiga, et luua puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="0178b-132">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="0178b-133">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="0178b-133">For more information, see:</span></span>

- <span data-ttu-id="0178b-134">[Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 1 plaanis</span><span class="sxs-lookup"><span data-stu-id="0178b-134">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- [<span data-ttu-id="0178b-135">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="0178b-135">Human Resources app in Teams</span></span>](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a><span data-ttu-id="0178b-136">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="0178b-136">Coming soon</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="0178b-137">Rakendus Human Resources Teamsis eelversioonifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="0178b-137">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="0178b-138">**Teatised**: vaba aja taotluste esitajaid ja kinnitajaid teavitatakse Teamsi rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="0178b-138">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="0178b-139">Kinnitajad saavad vaba aja taotlusi kinnitada või tagasi lükata ja esitajaid teavitatakse sellest, kas taotlus kinnitati või lükati tagasi.</span><span class="sxs-lookup"><span data-stu-id="0178b-139">Approvers will be able to approve or deny time-off requests, and submitters will be notified if the request was approved or denied.</span></span>
 
- <span data-ttu-id="0178b-140">**Juhi vaba aja kalender**: juhid saavad vaadata oma otseste alluvate kinnitatud ja ootel vabu aegu kalendrivaates.</span><span class="sxs-lookup"><span data-stu-id="0178b-140">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="0178b-141">Selle vaate abil näeb hõlpsalt, millal nende meeskonnaliikmed töölt puuduvad.</span><span class="sxs-lookup"><span data-stu-id="0178b-141">This view provides an easy understanding of when their team members are away from work.</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="0178b-142">Dataverse'is kaasatud kontroll-loendi üksused</span><span class="sxs-lookup"><span data-stu-id="0178b-142">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="0178b-143">Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="0178b-143">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="known-issues"></a><span data-ttu-id="0178b-144">Teadaolevad probleemid</span><span class="sxs-lookup"><span data-stu-id="0178b-144">Known issues</span></span>

<span data-ttu-id="0178b-145">Tööruumis **Funktsioonihaldus** võidakse kuvada funktsioone, mis on eelvaatefunktsioonidena keelatud, kuigi need on üldiselt kättesaadavad.</span><span class="sxs-lookup"><span data-stu-id="0178b-145">The **Feature management** workspace may be displaying features that are disabled as preview features when they are generally available.</span></span> <span data-ttu-id="0178b-146">Allpool on loend üldiselt kättesaadavatest funktsioonidest, mille olek on vale.</span><span class="sxs-lookup"><span data-stu-id="0178b-146">Below is a list of generally available features that show an incorrect status.</span></span> 

- <span data-ttu-id="0178b-147">Soodustuste haldus</span><span class="sxs-lookup"><span data-stu-id="0178b-147">Benefits management</span></span>
- <span data-ttu-id="0178b-148">Juhtumihaldus</span><span class="sxs-lookup"><span data-stu-id="0178b-148">Case management</span></span>
- <span data-ttu-id="0178b-149">Andmebaasi logimine (auditeerimine)</span><span class="sxs-lookup"><span data-stu-id="0178b-149">Database logging (Auditing)</span></span>
- <span data-ttu-id="0178b-150">Puhkuse lisandumine ühe ettevõtte või ühe plaani kohta</span><span class="sxs-lookup"><span data-stu-id="0178b-150">Leave accrual for a single company or a single plan</span></span>
- <span data-ttu-id="0178b-151">Puhkuste ja puudumiste lisandumise peatamine</span><span class="sxs-lookup"><span data-stu-id="0178b-151">Leave and absence accrual suspension</span></span>
- <span data-ttu-id="0178b-152">Saldo korrigeerimise põhjusekood ja kommentaar</span><span class="sxs-lookup"><span data-stu-id="0178b-152">Balance adjustment reason code and comment</span></span>
- <span data-ttu-id="0178b-153">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="0178b-153">Buy and sell leave</span></span>
- <span data-ttu-id="0178b-154">Puhkuste ja puudumiste kalender</span><span class="sxs-lookup"><span data-stu-id="0178b-154">Leave and absence calendar</span></span>
- <span data-ttu-id="0178b-155">Puhkuse edasikandmise reeglid</span><span class="sxs-lookup"><span data-stu-id="0178b-155">Leave carry-forward rules</span></span>
- <span data-ttu-id="0178b-156">Puhkuse lisandumise auditeerimine</span><span class="sxs-lookup"><span data-stu-id="0178b-156">Leave accrual auditing</span></span>
- <span data-ttu-id="0178b-157">Puhkuse lisandumise kustutamine</span><span class="sxs-lookup"><span data-stu-id="0178b-157">Leave accrual deletion</span></span>
- <span data-ttu-id="0178b-158">Puhkuse lisandumise ümardamine</span><span class="sxs-lookup"><span data-stu-id="0178b-158">Leave accrual rounding</span></span>
- <span data-ttu-id="0178b-159">Ühel puhkuseplaanil mitme puhkusetüübi konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0178b-159">Configure multiple leave types on a single leave plan</span></span>
- <span data-ttu-id="0178b-160">Eemalolekuaja täiustuste värskendamine</span><span class="sxs-lookup"><span data-stu-id="0178b-160">Update time-off enhancements</span></span>
- <span data-ttu-id="0178b-161">Lisandumiste jaoks töövõtja täistööaja vaste kasutamine</span><span class="sxs-lookup"><span data-stu-id="0178b-161">Use an employee's FTE for accruals</span></span>
- <span data-ttu-id="0178b-162">Ettevõtteülene hüvitusevaade</span><span class="sxs-lookup"><span data-stu-id="0178b-162">Cross company compensation view</span></span>
- <span data-ttu-id="0178b-163">Jõudluse ülevaadete printimine</span><span class="sxs-lookup"><span data-stu-id="0178b-163">Print performance reviews</span></span>
- <span data-ttu-id="0178b-164">Puhkuse viitvõla parandused</span><span class="sxs-lookup"><span data-stu-id="0178b-164">Leave accrual holiday corrections</span></span>

### <a name="benefit-plan-employee-entity"></a><span data-ttu-id="0178b-165">Soodustusplaani töövõtjaüksus</span><span class="sxs-lookup"><span data-stu-id="0178b-165">Benefit plan employee entity</span></span> 

<span data-ttu-id="0178b-166">Oleme hiljuti avastanud kaks probleemi seoses üksusega **BenefitsPlanEmployee**.</span><span class="sxs-lookup"><span data-stu-id="0178b-166">We have recently discovered two issues regarding the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="0178b-167">Töötaja registreerimiste importimisel on suvandid **Planeerimise kood** ja **Plaani tüübi kood** valesti määratud.</span><span class="sxs-lookup"><span data-stu-id="0178b-167">When importing worker enrollments, the **Coverage code** and the **Plan type code** are being set incorrectly.</span></span> <span data-ttu-id="0178b-168">Selle probleemi tõttu kuvatakse vormil **Töövõtja soodustuste plaan** ja vormil **Registreerimise avamine** töövõtjate soodustuste plaanid valesti.</span><span class="sxs-lookup"><span data-stu-id="0178b-168">This issue causes employee benefit plans to display incorrectly in the **Worker benefits plan** form and in the **Open enrollment** form in Employee self service.</span></span> <span data-ttu-id="0178b-169">See probleem võib mõjutada ka töövõtja võimalust valida plaane töövõtja iseteeninduses.</span><span class="sxs-lookup"><span data-stu-id="0178b-169">This issue can also impact the employee's ability to select plans in Employee self service.</span></span> <span data-ttu-id="0178b-170">Praegu ei ole lahendust.</span><span class="sxs-lookup"><span data-stu-id="0178b-170">Currently there isn't a workaround.</span></span> <span data-ttu-id="0178b-171">Käsitleme seda kui kõrge prioriteediga parandust ja laseme paranduse välja meie järgmise väljalaskega.</span><span class="sxs-lookup"><span data-stu-id="0178b-171">We're treating this as a high-priority fix and will roll out the fix with our next release.</span></span>

## <a name="see-also"></a><span data-ttu-id="0178b-172">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0178b-172">See also</span></span>

[<span data-ttu-id="0178b-173">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="0178b-173">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="0178b-174">Dynamics 365 Human Resourcesi 2019. aasta väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="0178b-174">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="0178b-175">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="0178b-175">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="0178b-176">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="0178b-176">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]