---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (25. juuni 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 23. juuni 2020 uusi või muutunud funktsioone.
author: andreabichsel
manager: tfehr
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0f767ad634a37b7231a7998184ef130668c8a8dc
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463618"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="2680f-103">Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (23. juuni 2020)</span><span class="sxs-lookup"><span data-stu-id="2680f-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2680f-104">Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="2680f-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2680f-105">Muudatused rakenduvad versioonile number 8.1.3347.</span><span class="sxs-lookup"><span data-stu-id="2680f-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="2680f-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="2680f-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="2680f-107">Kui lõpetatud töötaja registreering aegub, tühjendatakse vormilt Puhkuse registreerimine puhkuse tüüp, saldo ja summa (444867)</span><span class="sxs-lookup"><span data-stu-id="2680f-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="2680f-108">Selle valiku tegemisel säilitatakse nüüd väljade **Puhkuse tüüp**, **Saldo** ja **Summa** väärtused nende tühjendamise asemel.</span><span class="sxs-lookup"><span data-stu-id="2680f-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="2680f-109">Vale prognoositud saldo uue funktsiooni (Ühe ettevõtte või lepingu puhkuse viitvõlg) lubamisel (456553)</span><span class="sxs-lookup"><span data-stu-id="2680f-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="2680f-110">Nüüd kuvatakse õige prognoositud saldo, kui ühe ettevõtte või lepingu puhkuse viitvõlg on lubatud.</span><span class="sxs-lookup"><span data-stu-id="2680f-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="2680f-111">Seostega üksused, mille tulemuseks on dubleeritud navigeerimisatribuudid (456486)</span><span class="sxs-lookup"><span data-stu-id="2680f-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="2680f-112">Selles väljaandes on parandatud mitme üksuse navigeerimisatribuutidega (seosega) seotud probleem.</span><span class="sxs-lookup"><span data-stu-id="2680f-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="2680f-113">Tuvastatakse dubleeritud seosed.</span><span class="sxs-lookup"><span data-stu-id="2680f-113">Duplicate relations are detected.</span></span> <span data-ttu-id="2680f-114">Need stsenaariumid on kõik parandatud.</span><span class="sxs-lookup"><span data-stu-id="2680f-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="2680f-115">Kontsernisisesed kommentaarid tulemuslikkuse hindamises (455536)</span><span class="sxs-lookup"><span data-stu-id="2680f-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="2680f-116">Selle parandusega kuvatakse nüüd kontsernisiseseid kommentaare tulemuslikkuse hindamises.</span><span class="sxs-lookup"><span data-stu-id="2680f-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="2680f-117">Selle muudatusega on parandatud läbivaatajate kommentaaride vaade, mis sisestati sama tulemuslikkuse ülevaate jaoks erinevates ettevõtetes.</span><span class="sxs-lookup"><span data-stu-id="2680f-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="2680f-118">Ebakõla hüvituse halduse andmete kuvamisel (432562)</span><span class="sxs-lookup"><span data-stu-id="2680f-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="2680f-119">Hüvituse andmete ühtset vaadet säilitatakse nüüd Juhi iseteeninduses.</span><span class="sxs-lookup"><span data-stu-id="2680f-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="2680f-120">Sõltuvalt sellest, kuidas te liigute töötaja **Hüvituse üksikasjadesse**, kuvatakse juhtidele hüvituse andmeid nüüd ühtselt.</span><span class="sxs-lookup"><span data-stu-id="2680f-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="2680f-121">Põhipalgaplaani kehtivuse alguseks on vaikimisi tänane kuupäev (411994)</span><span class="sxs-lookup"><span data-stu-id="2680f-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="2680f-122">Hüvituse alguskuupäev määratakse nüüd töötajale määratud ametikoha alguskuupäeva järgi.</span><span class="sxs-lookup"><span data-stu-id="2680f-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="2680f-123">Puhkuste ja puudumiste vorm Luba pooliku päeva määratlus on keelatud uue vormi avamisel (452607)</span><span class="sxs-lookup"><span data-stu-id="2680f-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="2680f-124">Selle muudatusega lubatakse **Luba pooliku päeva määratlus** senikaua, kuni on olemas uued puhkuse kanded.</span><span class="sxs-lookup"><span data-stu-id="2680f-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="2680f-125">Olemisse HcmDiscussionEntity ei saa Exceli kaudu avaldada. Välja TotalRatingScore tõrge (453899)</span><span class="sxs-lookup"><span data-stu-id="2680f-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="2680f-126">Saate nüüd värskendada välja **TotalRatingScore** olemi **HCMDiscussionEntity** abil Exceli töövihiku kujundajas.</span><span class="sxs-lookup"><span data-stu-id="2680f-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2680f-127">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="2680f-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="2680f-128">Andmebaasi logimine</span><span class="sxs-lookup"><span data-stu-id="2680f-128">Database logging</span></span>

<span data-ttu-id="2680f-129">Andmebaasi logimine võimaldab teil kindlaks määrata, milliseid tabeleid ja välju tuleks jälgida.</span><span class="sxs-lookup"><span data-stu-id="2680f-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="2680f-130">Samuti võimaldab see kindlaks määrata sündmused, mis peaksid käivitama muudatuste jälgimise.</span><span class="sxs-lookup"><span data-stu-id="2680f-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="2680f-131">Saate kasutada andmebaasi logimise võimalusi, et aja jooksul neid muutusi näha.</span><span class="sxs-lookup"><span data-stu-id="2680f-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="2680f-132">Lisateavet leiate teemast [Andmebaasi logimise konfigureerimine ja haldamine](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="2680f-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="2680f-133">Kohustuslikud väljad</span><span class="sxs-lookup"><span data-stu-id="2680f-133">Mandatory fields</span></span> 

<span data-ttu-id="2680f-134">Saate nüüd muuta väljasid kohustuslikuks Human Resourcesi isikupärastamise võimaluste abil.</span><span class="sxs-lookup"><span data-stu-id="2680f-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="2680f-135">See funktsioon nõuab **Salvestatud vaateid**.</span><span class="sxs-lookup"><span data-stu-id="2680f-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="2680f-136">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="2680f-136">Human Resources application in Teams</span></span>

<span data-ttu-id="2680f-137">Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2680f-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="2680f-138">Nad saavad suhelda botiga, et luua puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="2680f-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="2680f-139">Lisateavet vt teemast [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="2680f-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="2680f-140">Andmehaldusraamistiku (DMF) üksused soodustuste haldamiseks</span><span class="sxs-lookup"><span data-stu-id="2680f-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="2680f-141">Välja tulevad soodustuste haldamise üksused.</span><span class="sxs-lookup"><span data-stu-id="2680f-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="2680f-142">DMF-üksused võimaldavad teil andmeid importida ja eksportida, et lihtsalt soodustuste haldamist konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="2680f-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="2680f-143">Soodustuste haldamise mall on saadaval andmete teisaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="2680f-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="2680f-144">Mall ekspordib ja impordib andmeid andmesõltuvuste arvestamiseks järjestikku.</span><span class="sxs-lookup"><span data-stu-id="2680f-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="2680f-145">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="2680f-145">Buy and sell leave</span></span> 

<span data-ttu-id="2680f-146">Mõned organisatsioonid pakuvad soodustust, mis võimaldab töötajatel oma puhkust müüa või osta.</span><span class="sxs-lookup"><span data-stu-id="2680f-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="2680f-147">Seda protsessi hallatakse sageli käsitsi.</span><span class="sxs-lookup"><span data-stu-id="2680f-147">This process is often managed manually.</span></span> <span data-ttu-id="2680f-148">See funktsioon muudab personaliosakonna jaoks poliitikate ja taotluste haldamise automaatseks.</span><span class="sxs-lookup"><span data-stu-id="2680f-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="2680f-149">See muudab puhkusehalduse protsessi sujuvamaks ja aitab kõrvaldada vigu.</span><span class="sxs-lookup"><span data-stu-id="2680f-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="2680f-150">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="2680f-150">For more information, see:</span></span>

- [<span data-ttu-id="2680f-151">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="2680f-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="2680f-152">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="2680f-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="2680f-153">Puhkuse lisandumine üksiku ettevõtte või plaani puhul</span><span class="sxs-lookup"><span data-stu-id="2680f-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="2680f-154">Kliendid saavad töödelda lisandumisi üksiku ettevõtte või üksiku puhkuste ja puudumiste plaani puhul.</span><span class="sxs-lookup"><span data-stu-id="2680f-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="2680f-155">See võimalus muudab lisandumisprotsessi selgemaks selliste klientide puhul, kellel on eri puhkuseaastad või puhkuse lisandumise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="2680f-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="2680f-156">Lisateavet leiate teemast [Puhkuse lisandumine ettevõtte või puhkuseplaani alusel](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="2680f-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="2680f-157">Eemalolekuaja taotlustele manuste lisamine</span><span class="sxs-lookup"><span data-stu-id="2680f-157">Add attachments to time off requests</span></span>

<span data-ttu-id="2680f-158">Manuste lisamise võimalus kinnitatud puhkusetaotlustele on praegust COVID-19 olukorda arvestades väga oluline.</span><span class="sxs-lookup"><span data-stu-id="2680f-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="2680f-159">Töövõtjad saavad nüüd neid manuseid lisada.</span><span class="sxs-lookup"><span data-stu-id="2680f-159">Employees can now add these attachments.</span></span> <span data-ttu-id="2680f-160">Samuti on neil rohkem teavet selle kohta, kuidas puhkusetaotlusi uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="2680f-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="2680f-161">Lisateavet leiate teemast [Olemasolevale taotlusele manuse lisamine](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="2680f-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="2680f-162">Lisandumise peatamisele põhjusekoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="2680f-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="2680f-163">Lisandumise peatamisele on lisatud põhjusekoodid.</span><span class="sxs-lookup"><span data-stu-id="2680f-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="2680f-164">Edasikandmise reeglid</span><span class="sxs-lookup"><span data-stu-id="2680f-164">Carry forward rules</span></span> 

<span data-ttu-id="2680f-165">Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle.</span><span class="sxs-lookup"><span data-stu-id="2680f-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="2680f-166">Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi.</span><span class="sxs-lookup"><span data-stu-id="2680f-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="2680f-167">Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="2680f-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="2680f-168">Puhkuse lisandumise peatamine kindlate puhkusetüüpide puhul</span><span class="sxs-lookup"><span data-stu-id="2680f-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="2680f-169">Saate luua reegli, et peatada selliste töötajate puhkuse lisandumine, kes on esitanud tasustamata puhkuse taotluse.</span><span class="sxs-lookup"><span data-stu-id="2680f-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="2680f-170">Tasustamata puhkus võib olla tüüp, kuid ei pruugi olla.</span><span class="sxs-lookup"><span data-stu-id="2680f-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="2680f-171">Võite peatada mis tahes muul puhkusetüübil põhineva puhkuse.</span><span class="sxs-lookup"><span data-stu-id="2680f-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="2680f-172">DMF-üksus on saadaval lisandumise peatamiseks</span><span class="sxs-lookup"><span data-stu-id="2680f-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="2680f-173">Nüüdsest on lisandumise peatamiseks saadaval DMF-üksus.</span><span class="sxs-lookup"><span data-stu-id="2680f-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="2680f-174">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="2680f-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="2680f-175">Töövõtja iseteeninduse nime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2680f-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="2680f-176">Jaotises **Human Resourcesi parameetrid** on saadaval uus suvand, et muuta töövõtja iseteeninduse tööruumi nimi iseteeninduseks.</span><span class="sxs-lookup"><span data-stu-id="2680f-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="2680f-177">Dataverse'is kaasatud kontroll-loendi üksused</span><span class="sxs-lookup"><span data-stu-id="2680f-177">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="2680f-178">Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="2680f-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="2680f-179">Vt ka</span><span class="sxs-lookup"><span data-stu-id="2680f-179">See also</span></span>

[<span data-ttu-id="2680f-180">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="2680f-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2680f-181">Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="2680f-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="2680f-182">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="2680f-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="2680f-183">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="2680f-183">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]