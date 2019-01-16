---
title: "Mis on Dynamics 365 for Talent Core HR-is uut või mida on muudetud (14. detsember 2018)"
description: "Teema kirjeldab funktsioone, mis on Microsoft Dynamics 365 for Talent Core HR-is kas uued või muudetud."
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: 844c23fc908c962203e644f1154cc480425d830b
ms.openlocfilehash: 7d2866923efd7f115ad5290f35ed4fcac5e47573
ms.contentlocale: et-ee
ms.lasthandoff: 12/18/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="96fa5-103">Mis on Dynamics 365 for Talent Core HR-is uut või mida on muudetud (14. detsember 2018)</span><span class="sxs-lookup"><span data-stu-id="96fa5-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="96fa5-104">**Järk 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="96fa5-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="96fa5-105">Teema kirjeldab funktsioone, mis on Core HR-is kas uued või muudetud.</span><span class="sxs-lookup"><span data-stu-id="96fa5-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="96fa5-106">Muudatused</span><span class="sxs-lookup"><span data-stu-id="96fa5-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="96fa5-107">US - ACA (Taskukohase ravikindlustuse eelnõu) toetavad maksuaasta 2018 1095-B ja 1095-C vorme</span><span class="sxs-lookup"><span data-stu-id="96fa5-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="96fa5-108">Igal aastal peab Kohaldatav suur tööandja (ALE) andma igale täistööajaga töötajale vormi 1095-C.</span><span class="sxs-lookup"><span data-stu-id="96fa5-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="96fa5-109">PEale selle, kui tööandja pakub enda kindlustust, peab ta väljastama vormi 1095-C (kui nad on ALE) ja 1095-B (kui nad on väike tööandja) kõigile töötajatele, täis- või osalise tööajaga, kes on nende pakutava tervisekindlustusega kaetud.</span><span class="sxs-lookup"><span data-stu-id="96fa5-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="96fa5-110">See funktsioon annab vormide 1095-C ja 1095-B prinditavad vormid.</span><span class="sxs-lookup"><span data-stu-id="96fa5-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="96fa5-111">Importimise ajal eiratakse HcmPerfJournalEntity välja SubmittedByPersonId</span><span class="sxs-lookup"><span data-stu-id="96fa5-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="96fa5-112">Jõudluse töölehe kannete importimisel/eksportimisel ignoreeritakse välja **Edastaja**.</span><span class="sxs-lookup"><span data-stu-id="96fa5-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="96fa5-113">Selle muudatusega peegeldab väärtus **imporditud/eksporditud** tabeli väärtust ekspordi ajal, kui importides uuendatakse süsteemi impordifailis antud väärtusega.</span><span class="sxs-lookup"><span data-stu-id="96fa5-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="96fa5-114">Analüüsi vahekaart tööruumis "Puhkused ja puudumine" kuvab mitte-administraatori rollide korral viga "OpenConnectionError"</span><span class="sxs-lookup"><span data-stu-id="96fa5-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="96fa5-115">Selle värkendusega ei anta vahekaardi **Analüüs** avamisel tööruumis **Puhkused ja puudumine** viga.</span><span class="sxs-lookup"><span data-stu-id="96fa5-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="96fa5-116">Töötaja iseteeninduskeskuses ei saa ametikoha hierarhia süvitsi minemine emasõlme</span><span class="sxs-lookup"><span data-stu-id="96fa5-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="96fa5-117">Tehtud on muudatus vea "Emasõlme hankimine ebaõnnestus" parandamiseks juhul, kui ametikoha hierarhia on kohandatud ilmuma olemasolevasse tööruumi ja hierarhias valitud ametikohale.</span><span class="sxs-lookup"><span data-stu-id="96fa5-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="96fa5-118">Ametikoha lehel vahekaardi Palk nägemiseks peab olema süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="96fa5-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="96fa5-119">Tehtud on muudatus õige turvaelemendid kaasamiseks olemasolevas privileegis: "Palga töötaja ja ametikoha üksikasjade säilitamine".</span><span class="sxs-lookup"><span data-stu-id="96fa5-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="96fa5-120">Selle muudatusega on Palgaarvestuse administraatoril vaikimisi juurdepääs ametikoha lehekülge palga väljadele.</span><span class="sxs-lookup"><span data-stu-id="96fa5-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="96fa5-121">Tõrge jõudluse ülevaate esitamisel juhile ja kohatäidet %Reviews.PerfPeriod% kasutatakse saatmisjuhistes</span><span class="sxs-lookup"><span data-stu-id="96fa5-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="96fa5-122">Tehtud on muudatus, mis parandab vea "Nullviide" kohatäite %Reviews.PerfPeriod% kasutamisel saatmisjuhistes.</span><span class="sxs-lookup"><span data-stu-id="96fa5-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="96fa5-123">Tööjõu Power BI aruandes kuvatakse viga, kui töötaja staaži kuupäv on liigaastal</span><span class="sxs-lookup"><span data-stu-id="96fa5-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="96fa5-124">Selle muudatusega toetab Power BI nüüd liigaastaid.</span><span class="sxs-lookup"><span data-stu-id="96fa5-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="96fa5-125">Integratsioon Core HR ja Attracti vahel</span><span class="sxs-lookup"><span data-stu-id="96fa5-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="96fa5-126">Tehtud on muudatus Core HR ja Attracti palgatavate kandidaatide integratsiooni värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="96fa5-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="96fa5-127">Et palgatavad kandidaadid oleksid tööruumis **Personalihaldus** nähtavad, kasutatakse järgmisi CDS for Apps (CDS 2.0) üksuseid.</span><span class="sxs-lookup"><span data-stu-id="96fa5-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following CDS for Apps (CDS 2.0) entities are used:</span></span>

<span data-ttu-id="96fa5-128">Tööavaldus</span><span class="sxs-lookup"><span data-stu-id="96fa5-128">Job Application</span></span>
- <span data-ttu-id="96fa5-129">Olek Põhjus peab olema määratud Pakkumine vastu võetud peale</span><span class="sxs-lookup"><span data-stu-id="96fa5-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="96fa5-130">Annab kandidaadi ja vaba töökoha</span><span class="sxs-lookup"><span data-stu-id="96fa5-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="96fa5-131">Kandidaat</span><span class="sxs-lookup"><span data-stu-id="96fa5-131">Candidate</span></span>
-   <span data-ttu-id="96fa5-132">Annab kandidaadi teabe</span><span class="sxs-lookup"><span data-stu-id="96fa5-132">Provides Candidate information</span></span>

<span data-ttu-id="96fa5-133">Vaba töökoht</span><span class="sxs-lookup"><span data-stu-id="96fa5-133">Job Opening</span></span>
-   <span data-ttu-id="96fa5-134">Annab vaba töökoha ID ja vaba töökoha osalejad</span><span class="sxs-lookup"><span data-stu-id="96fa5-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="96fa5-135">Vaba töökoha osalised</span><span class="sxs-lookup"><span data-stu-id="96fa5-135">Job Opening Participants</span></span>
-   <span data-ttu-id="96fa5-136">Annab värbamisjuhi</span><span class="sxs-lookup"><span data-stu-id="96fa5-136">Provides Hiring Manager</span></span>

<span data-ttu-id="96fa5-137">Kui kandidaat lisatakse Personalihaldusesse, saab kandidaati nüüd kandidaadi kaardil oleva uue valiku abil kõrvale jätta.</span><span class="sxs-lookup"><span data-stu-id="96fa5-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="96fa5-138">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="96fa5-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="96fa5-139">Puhkus ja puudumine: tulevaste puhkuste ja puhkusesaldo ennustamine</span><span class="sxs-lookup"><span data-stu-id="96fa5-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="96fa5-140">Vabade päevade kuvamine on muutumas koos muutustega, mida tehakse võimaldamaks töötajatel ennustada vagu päevi ja esitada tulevikus vabade pävade taotlusi ilma praegust vabade pävade saldot mõjutamata.</span><span class="sxs-lookup"><span data-stu-id="96fa5-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="96fa5-141">Praegu kuvatud saldo on taotlemiseks saadaval olev vabade päevade hulk, sealhulgas viitvõlad tänaseni ja kõik heakskiidetud puhkuseavaldused kuni aegade lõpuni.</span><span class="sxs-lookup"><span data-stu-id="96fa5-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="96fa5-142">Kui ennustamise suutlikus on väljastatud, muutub kuvatav saldo puhkusepäevade hetkesaldoks, sealhulgas viitvõlad tänaseni ja tänased taotlused.</span><span class="sxs-lookup"><span data-stu-id="96fa5-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="96fa5-143">Töötajad ja juhid näevad neid värskendatud saldosid töötaja ja juhi iseteeninduses kaardil **Vaba aeg** ja aknas **Puhkusesalde**.</span><span class="sxs-lookup"><span data-stu-id="96fa5-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="96fa5-144">Personalijuhid näevad neid värskendatud saldosid tööruumise **Inimesed** ja töötaja aknas **Määratud puhkuseplaanid**.</span><span class="sxs-lookup"><span data-stu-id="96fa5-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="96fa5-145">Teadaolev probleem</span><span class="sxs-lookup"><span data-stu-id="96fa5-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="96fa5-146">Vastendamise tõrked integreerimisel rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="96fa5-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="96fa5-147">Praegusel mallil on tuvastatud rakendustega Talent ja Dynamics 365 for Finance and Operations integreerimisel järgmised probleemid.</span><span class="sxs-lookup"><span data-stu-id="96fa5-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="96fa5-148">Uus mall avaldatakse varsti ja see rakendatakse kõigile uutele loodavatele integreerimisprojektidele.</span><span class="sxs-lookup"><span data-stu-id="96fa5-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="96fa5-149">Olemasolevate integreerimisprojektide puhul saab ülesande vastendamist uuendada.</span><span class="sxs-lookup"><span data-stu-id="96fa5-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="96fa5-150">Vaadake uuendatud vastendusi järgmisest tabelist.</span><span class="sxs-lookup"><span data-stu-id="96fa5-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="96fa5-151">Andmete integreerimine Ametikohtast Ametikoha peamisele tööülesandele ei toimi.</span><span class="sxs-lookup"><span data-stu-id="96fa5-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="96fa5-152">Seda probleemi praegu uuritakse.</span><span class="sxs-lookup"><span data-stu-id="96fa5-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="96fa5-153">Praegusele vastendusele lahendust ei ole.</span><span class="sxs-lookup"><span data-stu-id="96fa5-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="96fa5-154">Osakonnast tootmisüksusele ülesanded vajavad järgmiste vastenduste uuendamist.</span><span class="sxs-lookup"><span data-stu-id="96fa5-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="96fa5-155">Olemasolev allika väli</span><span class="sxs-lookup"><span data-stu-id="96fa5-155">Existing source field</span></span>          | <span data-ttu-id="96fa5-156">Uus allika väli</span><span class="sxs-lookup"><span data-stu-id="96fa5-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="96fa5-157">cdm_description (kirjeldus)</span><span class="sxs-lookup"><span data-stu-id="96fa5-157">cdm_description (Description)</span></span>  | <span data-ttu-id="96fa5-158">cdm_name (nimi)</span><span class="sxs-lookup"><span data-stu-id="96fa5-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="96fa5-159">Lisada tuleb ka lisanduv vastendamine.</span><span class="sxs-lookup"><span data-stu-id="96fa5-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="96fa5-160">Valige Viimane väli **Puudub**, et lisada järgmine vastendamine.</span><span class="sxs-lookup"><span data-stu-id="96fa5-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="96fa5-161">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="96fa5-161">Source field</span></span>                   | <span data-ttu-id="96fa5-162">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="96fa5-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="96fa5-163">cdm_description (kirjeldus)</span><span class="sxs-lookup"><span data-stu-id="96fa5-163">cdm_description (Description)</span></span>  | <span data-ttu-id="96fa5-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="96fa5-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="96fa5-165">Värskendatud vastendused peaksid välja nägema nagu järgmisel pildil.</span><span class="sxs-lookup"><span data-stu-id="96fa5-165">The updated mappings should look like the following image.</span></span>

![Osakonnast Tootmisüksusesse ülesanne](./media/DepartmentMapping.png)


<span data-ttu-id="96fa5-167">Töödelt Töö üksikasjade ülesanne vajab järgmiste vastenduste uuendamist.</span><span class="sxs-lookup"><span data-stu-id="96fa5-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="96fa5-168">Olemasolev allika väli</span><span class="sxs-lookup"><span data-stu-id="96fa5-168">Existing source field</span></span>          | <span data-ttu-id="96fa5-169">Uus allika väli</span><span class="sxs-lookup"><span data-stu-id="96fa5-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="96fa5-170">cdm_name (nimi)</span><span class="sxs-lookup"><span data-stu-id="96fa5-170">cdm_name (Name)</span></span>                | <span data-ttu-id="96fa5-171">cdm_description (kirjeldus)</span><span class="sxs-lookup"><span data-stu-id="96fa5-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="96fa5-172">cdm_name (kirjeldus)</span><span class="sxs-lookup"><span data-stu-id="96fa5-172">cdm_name (Description)</span></span>         | <span data-ttu-id="96fa5-173">cdm_description (töökirjeldus)</span><span class="sxs-lookup"><span data-stu-id="96fa5-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="96fa5-174">Värskendatud vastendused peaksid välja nägema nagu alloleval pildil.</span><span class="sxs-lookup"><span data-stu-id="96fa5-174">The updated mappings should look like the image below.</span></span>

![Töödelt töö üksikasjadele ülesanne](./media/JobMapping.png)

<span data-ttu-id="96fa5-176">Töötajatelt Tööülesandele ülesanne vajab järgmiste vastenduste uuendamist.</span><span class="sxs-lookup"><span data-stu-id="96fa5-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="96fa5-177">Olemasolev allika väli</span><span class="sxs-lookup"><span data-stu-id="96fa5-177">Existing source field</span></span>                 | <span data-ttu-id="96fa5-178">Uus allika väli</span><span class="sxs-lookup"><span data-stu-id="96fa5-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="96fa5-179">cdm_emailaddress1 (e-posti aadress 1)</span><span class="sxs-lookup"><span data-stu-id="96fa5-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="96fa5-180">cdm_primaryemailaddress (esmane e-posti aadress)</span><span class="sxs-lookup"><span data-stu-id="96fa5-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="96fa5-181">cdm_telephone1 (telefon 1)</span><span class="sxs-lookup"><span data-stu-id="96fa5-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="96fa5-182">cdm_primarytelephone (esmane telefoninumber)</span><span class="sxs-lookup"><span data-stu-id="96fa5-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="96fa5-183">Soo välja muutmine vajab samuti värskendamist.</span><span class="sxs-lookup"><span data-stu-id="96fa5-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="96fa5-184">Valige vastenduse tüüp **fn** (funktsioon) Soole ja värskendada järgmisi väärtuste vastendusi.</span><span class="sxs-lookup"><span data-stu-id="96fa5-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="96fa5-185">KM väärtus</span><span class="sxs-lookup"><span data-stu-id="96fa5-185">CDS value</span></span>                   | <span data-ttu-id="96fa5-186">Rakenduse Finance and Operations väärtus</span><span class="sxs-lookup"><span data-stu-id="96fa5-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="96fa5-187">75440000</span><span class="sxs-lookup"><span data-stu-id="96fa5-187">75440000</span></span>                    | <span data-ttu-id="96fa5-188">Mees</span><span class="sxs-lookup"><span data-stu-id="96fa5-188">Male</span></span>                                             |
| <span data-ttu-id="96fa5-189">75440001</span><span class="sxs-lookup"><span data-stu-id="96fa5-189">75440001</span></span>                    | <span data-ttu-id="96fa5-190">Naissoost</span><span class="sxs-lookup"><span data-stu-id="96fa5-190">Female</span></span>                                           |
| <span data-ttu-id="96fa5-191">75440002</span><span class="sxs-lookup"><span data-stu-id="96fa5-191">75440002</span></span>                    | <span data-ttu-id="96fa5-192">Pole</span><span class="sxs-lookup"><span data-stu-id="96fa5-192">None</span></span>                                             | 
| <span data-ttu-id="96fa5-193">75440003</span><span class="sxs-lookup"><span data-stu-id="96fa5-193">75440003</span></span>                    | <span data-ttu-id="96fa5-194">NonSpecific</span><span class="sxs-lookup"><span data-stu-id="96fa5-194">NonSpecific</span></span>                                      |

<span data-ttu-id="96fa5-195">Värskendatud vastendused peaksid välja nägema nagu järgmistel piltidel.</span><span class="sxs-lookup"><span data-stu-id="96fa5-195">The updated mappings should look like the following images.</span></span>

![Töötajatelt töötajale ülesanne](./media/WorkerMapping.png)

![Soo välja muutumine](./media/WorkerTransform.png)

