---
title: Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (08. juuli 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 8. juuli 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 07/08/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba0bb54b44f66aa73056667a93a3f8e6f7f618ee
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528469"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="705e6-103">Mis on uut ja mida on muudetud rakenduses Dynamics 365 Human Resources (8. juuli 2020)</span><span class="sxs-lookup"><span data-stu-id="705e6-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="705e6-104">Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="705e6-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="705e6-105">Muudatused rakenduvad versioonile number 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="705e6-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="705e6-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="705e6-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="705e6-107">Andmebaasi logimine</span><span class="sxs-lookup"><span data-stu-id="705e6-107">Database logging</span></span>

<span data-ttu-id="705e6-108">Andmebaasi logimine võimaldab teil kindlaks määrata, milliseid tabeleid ja välju tuleks jälgida.</span><span class="sxs-lookup"><span data-stu-id="705e6-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="705e6-109">Samuti võimaldab see kindlaks määrata sündmused, mis peaksid käivitama muudatuste jälgimise.</span><span class="sxs-lookup"><span data-stu-id="705e6-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="705e6-110">Saate kasutada andmebaasi logimise võimalusi, et aja jooksul neid muutusi näha.</span><span class="sxs-lookup"><span data-stu-id="705e6-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="705e6-111">Lisateavet leiate teemast [Andmebaasi logimise konfigureerimine ja haldamine](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="705e6-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="705e6-112">Töövõtja iseteeninduse nime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="705e6-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="705e6-113">Saate nüüd jaotises **Human Resources' parameetrites** muuta tööruumi **Töövõtja iseteenindus** nimeks **Iseteenindus**.</span><span class="sxs-lookup"><span data-stu-id="705e6-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="705e6-114">Lisateavet leiate teemast [Töövõtja iseteeninduse tööruumi nime muutmine](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="705e6-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="705e6-115">Soodustuste halduse avatud registreerimise juurdepääs väljaspool perioodi</span><span class="sxs-lookup"><span data-stu-id="705e6-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="705e6-116">Selles väljalaskes on parandatud viga, kus töötajad saavad juurdepääsu soodustuste avatud registreerimisele väljaspool registreerimisperioodi või ilma elusündmuseta.</span><span class="sxs-lookup"><span data-stu-id="705e6-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="705e6-117">Selle tulemusena, kui vajate avatud registreerimise demo töövõtja iseteeninduses, peate kohandama avatud registreerimise kuupäevi tänaseks (või varasemaks), et muuta see kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="705e6-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="705e6-118">Seda sätet saate muuta jaotises **Soodustuste haldus > Reeglite ja valikute perioodid**.</span><span class="sxs-lookup"><span data-stu-id="705e6-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="705e6-119">Töövõtja registreerimise kinnituse saatmine meili teel</span><span class="sxs-lookup"><span data-stu-id="705e6-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="705e6-120">Nüüd saate pärast soodustuste valimist töövõtjatele meile saata.</span><span class="sxs-lookup"><span data-stu-id="705e6-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="705e6-121">Saate saata vaikimisi sõnumi või kasutada organisatsiooni meilimalli.</span><span class="sxs-lookup"><span data-stu-id="705e6-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="705e6-122">Need sätted on jaotises **Inimressursside parameetrid > Soodustuste haldus**.</span><span class="sxs-lookup"><span data-stu-id="705e6-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="705e6-123">Tühistatud puhkust kuvatakse endiselt inimeste tööruumi tulevase vaba aja all (441358)</span><span class="sxs-lookup"><span data-stu-id="705e6-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="705e6-124">Tühistatud puhkust ei kuvata enam tulevase vaba aja all puhkuse kaartidel tööruumis **Inimesed**.</span><span class="sxs-lookup"><span data-stu-id="705e6-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="705e6-125">Osakonna üksuse atribuuti ei saa kasutada PositionV2 üksuses (456486)</span><span class="sxs-lookup"><span data-stu-id="705e6-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="705e6-126">Nüüd saate lisada osakonna ilma topeltseost loomata.</span><span class="sxs-lookup"><span data-stu-id="705e6-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="705e6-127">PayrollWorkerEnrolledBenefitDetailEntity peaks kasutama pensioni plaanide puhul ainult arvutatud välja (459779)</span><span class="sxs-lookup"><span data-stu-id="705e6-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="705e6-128">Üksuse **PayrollWorkerEnrolledBenefitDetailEntity** eksportimisel määratleb eksportimine, kas see peaks kasutama arvutatud välja määra tabeli alusel või kasutama kindlustamistabeli välja **ContributionAmountCur**.</span><span class="sxs-lookup"><span data-stu-id="705e6-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="705e6-129">Andmeüksuse kasutatav loogika kasutab määra tabelit olukordades, kus rakendus seda tavaliselt ei tee.</span><span class="sxs-lookup"><span data-stu-id="705e6-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="705e6-130">See loogika põhjustab üksuse eksportimist, et tagastada null-väärtus selle veeru jaoks, kuna arvutuse määra tabelit pole ja toode ei luba kliendil seda määrata.</span><span class="sxs-lookup"><span data-stu-id="705e6-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="705e6-131">Segased tõlked Tšehhi keeles personalihalduses ja töövõtjate iseteeninduses (400276)</span><span class="sxs-lookup"><span data-stu-id="705e6-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="705e6-132">Selles väljalaskes on parandatud tõlked **Ettevõtte kataloog**, **Järgmine registreeritud kursus**, **Töö** ja **Ametikoht**.</span><span class="sxs-lookup"><span data-stu-id="705e6-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="705e6-133">Tabelis WorkCalendarEmployment pole loodud ja muudetud süsteemi väljad lubatud (460171)</span><span class="sxs-lookup"><span data-stu-id="705e6-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="705e6-134">Loodud ja muudetud süsteemi väljad on nüüd lubatud Human Resourcesi tabelis **WorkCalendarEmployment**.</span><span class="sxs-lookup"><span data-stu-id="705e6-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="705e6-135">Tühi viite erand tulevase töövõtja palkamise ja üksikasjade lisamise jaoks (455475)</span><span class="sxs-lookup"><span data-stu-id="705e6-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="705e6-136">Selles väljalaskes on parandatud tõrge (tühi viide) sujuvamas töövõtjate sisestamises, kui palkate töövõtja suvandi **Palkamise ja üksikasjade lisamine** abil.</span><span class="sxs-lookup"><span data-stu-id="705e6-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="705e6-137">Common Data Service'i töövõtja üksuses tehtud muudatused ei kajastu Human Resourcesis (455652)</span><span class="sxs-lookup"><span data-stu-id="705e6-137">Changes made in the Common Data Service Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="705e6-138">Common Data Service'i üksuse **Töövõtja** järgmistel väljadel tehtud muudatused kuvatakse nüüd Human Resourcesis.</span><span class="sxs-lookup"><span data-stu-id="705e6-138">Changes made to the following fields in the **Worker** entity in Common Data Service will now show up in Human Resources:</span></span>

- <span data-ttu-id="705e6-139">**Töötab kodus**</span><span class="sxs-lookup"><span data-stu-id="705e6-139">**Works from home**</span></span>
- <span data-ttu-id="705e6-140">**Staaž kuupäeval**</span><span class="sxs-lookup"><span data-stu-id="705e6-140">**Seniority date**</span></span>
- <span data-ttu-id="705e6-141">**Tähtpäeva kuupäev**</span><span class="sxs-lookup"><span data-stu-id="705e6-141">**Anniversary date**</span></span>
- <span data-ttu-id="705e6-142">**Värbamise algne kuupäev**</span><span class="sxs-lookup"><span data-stu-id="705e6-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="705e6-143">Õige hüvituse tase ei ole vaikimisi ametikohale määratud töö alusel (394136)</span><span class="sxs-lookup"><span data-stu-id="705e6-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="705e6-144">Selle muudatusega on õiged hüvituse taseme vaikimisi jaotise **Hüvituse plaani määramine** suvandite **Ametikoha üksikasjad** ja **Alguskuupäev** kirjete **Kehtib alates** põhjal.</span><span class="sxs-lookup"><span data-stu-id="705e6-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="705e6-145">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="705e6-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="705e6-146">Kohustuslikud väljad</span><span class="sxs-lookup"><span data-stu-id="705e6-146">Mandatory fields</span></span> 

<span data-ttu-id="705e6-147">Saate nüüd muuta väljasid kohustuslikuks Human Resourcesi isikupärastamise võimaluste abil.</span><span class="sxs-lookup"><span data-stu-id="705e6-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="705e6-148">See funktsioon nõuab **Salvestatud vaateid**.</span><span class="sxs-lookup"><span data-stu-id="705e6-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="705e6-149">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="705e6-149">Human Resources application in Teams</span></span>

<span data-ttu-id="705e6-150">Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="705e6-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="705e6-151">Nad saavad suhelda botiga, et luua puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="705e6-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="705e6-152">Lisateavet vt teemast [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="705e6-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="705e6-153">Andmehaldusraamistiku (DMF) üksused soodustuste haldamiseks</span><span class="sxs-lookup"><span data-stu-id="705e6-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="705e6-154">Välja tulevad soodustuste haldamise üksused.</span><span class="sxs-lookup"><span data-stu-id="705e6-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="705e6-155">DMF-üksused võimaldavad teil andmeid importida ja eksportida, et lihtsalt soodustuste haldamist konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="705e6-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="705e6-156">Soodustuste haldamise mall on saadaval andmete teisaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="705e6-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="705e6-157">Mall ekspordib ja impordib andmeid andmesõltuvuste arvestamiseks järjestikku.</span><span class="sxs-lookup"><span data-stu-id="705e6-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="705e6-158">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="705e6-158">Buy and sell leave</span></span> 

<span data-ttu-id="705e6-159">Mõned organisatsioonid pakuvad soodustust, mis võimaldab töötajatel oma puhkust müüa või osta.</span><span class="sxs-lookup"><span data-stu-id="705e6-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="705e6-160">Seda protsessi hallatakse sageli käsitsi.</span><span class="sxs-lookup"><span data-stu-id="705e6-160">This process is often managed manually.</span></span> <span data-ttu-id="705e6-161">See funktsioon muudab personaliosakonna jaoks poliitikate ja taotluste haldamise automaatseks.</span><span class="sxs-lookup"><span data-stu-id="705e6-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="705e6-162">See muudab puhkusehalduse protsessi sujuvamaks ja aitab kõrvaldada vigu.</span><span class="sxs-lookup"><span data-stu-id="705e6-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="705e6-163">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="705e6-163">For more information, see:</span></span>

- [<span data-ttu-id="705e6-164">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="705e6-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="705e6-165">Puhkuse ostmine ja müümine</span><span class="sxs-lookup"><span data-stu-id="705e6-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="705e6-166">Puhkuse lisandumine üksiku ettevõtte või plaani puhul</span><span class="sxs-lookup"><span data-stu-id="705e6-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="705e6-167">Kliendid saavad töödelda lisandumisi üksiku ettevõtte või üksiku puhkuste ja puudumiste plaani puhul.</span><span class="sxs-lookup"><span data-stu-id="705e6-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="705e6-168">See võimalus muudab lisandumisprotsessi selgemaks selliste klientide puhul, kellel on eri puhkuseaastad või puhkuse viitvõla poliitikad.</span><span class="sxs-lookup"><span data-stu-id="705e6-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="705e6-169">Lisateavet leiate teemast [Puhkuse lisandumine ettevõtte või puhkuseplaani alusel](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="705e6-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="705e6-170">Puhkusetaotlustele manuste lisamine</span><span class="sxs-lookup"><span data-stu-id="705e6-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="705e6-171">Manuste lisamise võimalus kinnitatud puhkusetaotlustele on praegust COVID-19 olukorda arvestades väga oluline.</span><span class="sxs-lookup"><span data-stu-id="705e6-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="705e6-172">Töövõtjad saavad nüüd neid manuseid lisada.</span><span class="sxs-lookup"><span data-stu-id="705e6-172">Employees can now add these attachments.</span></span> <span data-ttu-id="705e6-173">Samuti on neil rohkem teavet selle kohta, kuidas puhkusetaotlusi uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="705e6-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="705e6-174">Lisateavet leiate teemast [Olemasolevale taotlusele manuse lisamine](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="705e6-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="705e6-175">Lisandumise peatamisele põhjusekoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="705e6-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="705e6-176">Lisandumise peatamisele on lisatud põhjusekoodid.</span><span class="sxs-lookup"><span data-stu-id="705e6-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="705e6-177">Edasikandmise reeglid</span><span class="sxs-lookup"><span data-stu-id="705e6-177">Carry forward rules</span></span> 

<span data-ttu-id="705e6-178">Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle.</span><span class="sxs-lookup"><span data-stu-id="705e6-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="705e6-179">Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi.</span><span class="sxs-lookup"><span data-stu-id="705e6-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="705e6-180">Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="705e6-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="705e6-181">Puhkuse lisandumise peatamine kindlate puhkusetüüpide puhul</span><span class="sxs-lookup"><span data-stu-id="705e6-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="705e6-182">Saate luua reegli, et peatada selliste töötajate puhkuse lisandumine, kes on esitanud tasustamata puhkuse taotluse.</span><span class="sxs-lookup"><span data-stu-id="705e6-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="705e6-183">Tasustamata puhkus võib olla tüüp, kuid ei pruugi olla.</span><span class="sxs-lookup"><span data-stu-id="705e6-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="705e6-184">Võite peatada mis tahes muul puhkusetüübil põhineva puhkuse.</span><span class="sxs-lookup"><span data-stu-id="705e6-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="705e6-185">DMF-üksus on saadaval lisandumise peatamiseks</span><span class="sxs-lookup"><span data-stu-id="705e6-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="705e6-186">Nüüdsest on lisandumise peatamiseks saadaval DMF-üksus.</span><span class="sxs-lookup"><span data-stu-id="705e6-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="705e6-187">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="705e6-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="705e6-188">Common Data Service'is kaasatud kontroll-loendi üksused</span><span class="sxs-lookup"><span data-stu-id="705e6-188">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="705e6-189">Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Common Data Service'is.</span><span class="sxs-lookup"><span data-stu-id="705e6-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="705e6-190">Vt ka</span><span class="sxs-lookup"><span data-stu-id="705e6-190">See also</span></span>

[<span data-ttu-id="705e6-191">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="705e6-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="705e6-192">Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="705e6-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="705e6-193">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="705e6-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="705e6-194">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="705e6-194">Manage features</span></span>](hr-admin-manage-features.md)
