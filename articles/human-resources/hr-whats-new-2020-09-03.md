---
title: Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (03. september 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 3. septembri 2020 uusi või muutunud funktsioone.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10978d8843e7bce2800d62b63e58152569be9631
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891765"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a><span data-ttu-id="8b55e-103">Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (3. september 2020)</span><span class="sxs-lookup"><span data-stu-id="8b55e-103">What's new or changed in Dynamics 365 Human Resources (September 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8b55e-104">Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="8b55e-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8b55e-105">Muudatused rakenduvad versioonile number 8.1.3504.</span><span class="sxs-lookup"><span data-stu-id="8b55e-105">Changes apply to build number 8.1.3504.</span></span> <span data-ttu-id="8b55e-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8b55e-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

<span data-ttu-id="8b55e-107">Lisateavet rakenduse Human Resources tulevaste funktsioonide kohta vt teemast [Dynamics 365 Human Resourcesi 2019. aasta väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span><span class="sxs-lookup"><span data-stu-id="8b55e-107">For more information about upcoming features in Human Resources, see [Overview of Dynamics 365 Human Resources 2019 release wave 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span></span> <span data-ttu-id="8b55e-108">Rakenduse Human Resources värskendamisprotsessi kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="8b55e-108">For more information about the update process for Human Resources, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-this-release"></a><span data-ttu-id="8b55e-109">Selles väljalaskes</span><span class="sxs-lookup"><span data-stu-id="8b55e-109">In this release</span></span>

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a><span data-ttu-id="8b55e-110">Uued finantsdimensioonide vaikeruudustik ja dialoogi vaikemuster rakenduses Human Resources (469495)</span><span class="sxs-lookup"><span data-stu-id="8b55e-110">New default financial dimensions grid and dialog pattern throughout Human Resources (469495)</span></span>

<span data-ttu-id="8b55e-111">Finantsdimensioonide uus muster on nüüd saadaval järgmistes valdkondades.</span><span class="sxs-lookup"><span data-stu-id="8b55e-111">The new pattern for financial dimensions is now available in the following areas:</span></span>

- <span data-ttu-id="8b55e-112">Ametikoha tegevused (vorm: **HcmPositionActionDetail**)</span><span class="sxs-lookup"><span data-stu-id="8b55e-112">Position actions  (Form: **HcmPositionActionDetail**)</span></span>
- <span data-ttu-id="8b55e-113">Palga tulukoodid (vorm: **PayrollEarningCode**)</span><span class="sxs-lookup"><span data-stu-id="8b55e-113">Payroll earning codes  (Form: **PayrollEarningCode**)</span></span>

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a><span data-ttu-id="8b55e-114">Kirjeid ei kuvata ettevõtte puhkusekalendris, kui „Puhkuse- ja puudumiste kalendri täiustused” pole lubatud (484406)</span><span class="sxs-lookup"><span data-stu-id="8b55e-114">Entries don't appear in company leave calendar if Leave and absence calendar enhancements aren't enabled (484406)</span></span>

<span data-ttu-id="8b55e-115">See väljalase parandab probleemi, mille korral ettevõtte puhkusekalendris ei kuvata puhkusekandeid.</span><span class="sxs-lookup"><span data-stu-id="8b55e-115">This release corrects an issue where leave entries aren't displayed in the company leave calendar.</span></span> <span data-ttu-id="8b55e-116">See probleem ilmneb ainult siis, kui funktsioonihalduse suvand **Puhkuse- ja puudumiste kalendri täiustused** pole lubatud.</span><span class="sxs-lookup"><span data-stu-id="8b55e-116">This issue only occurs when the Feature management option **Leave and absence calendar enhancements** isn't enabled.</span></span>

### <a name="benefitplanemployeeentity-issue-467597"></a><span data-ttu-id="8b55e-117">BenefitPlanEmployeeEntity probleem (467597)</span><span class="sxs-lookup"><span data-stu-id="8b55e-117">BenefitPlanEmployeeEntity issue (467597)</span></span>

<span data-ttu-id="8b55e-118">See väljalase parandab üksusega **BenefitsPlanEmployee** seotud probleemi.</span><span class="sxs-lookup"><span data-stu-id="8b55e-118">This release corrects an issue with the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="8b55e-119">Töötaja registreerimiste importimisel määratakse nüüd suvandid **Planeerimise kood** ja **Plaani tüübi kood** õigesti.</span><span class="sxs-lookup"><span data-stu-id="8b55e-119">When importing worker enrollments, the **Coverage code** and the **Plan type code** are now set correctly.</span></span> <span data-ttu-id="8b55e-120">Selle probleemi tõttu kuvatakse vormil **Töövõtja soodustuste plaan** ja vormil **Registreerimise avamine** töövõtjate soodustuste plaanid valesti.</span><span class="sxs-lookup"><span data-stu-id="8b55e-120">This issue caused employee benefit plans to display incorrectly in the **Worker benefits plan** and **Open enrollment** forms in Employee self service.</span></span>

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a><span data-ttu-id="8b55e-121">Elektroonilise faili 1094-C väljundi puuduv tähemärk XML-is (435190)</span><span class="sxs-lookup"><span data-stu-id="8b55e-121">Electronic file 1094-C output missing letter in XML (435190)</span></span>

<span data-ttu-id="8b55e-122">See muudatus parandab probleemi, mille korral puudub väljundfailis 1094-C vajalik märk IRS-ile edastamisel.</span><span class="sxs-lookup"><span data-stu-id="8b55e-122">This change corrects an issue with the 1094-C output file missing a character needed when submitting to the IRS.</span></span>

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a><span data-ttu-id="8b55e-123">Töövõtja ergutussüsteemi tabel, mis on vastendatud fikseeritud hüvituse vormiga (476117)</span><span class="sxs-lookup"><span data-stu-id="8b55e-123">Employee variable compensation table mapped to fixed compensation form (476117)</span></span>

<span data-ttu-id="8b55e-124">See muudatus viib fikseeritud hüvituse väljad vastavusse fikseeritud hüvituse vormiga.</span><span class="sxs-lookup"><span data-stu-id="8b55e-124">This change aligns the fixed compensation fields with the fixed compensation form.</span></span> <span data-ttu-id="8b55e-125">Ergutussüsteemi väljad on nüüd saadaval ainult koos ergutussüsteemi vormiga.</span><span class="sxs-lookup"><span data-stu-id="8b55e-125">Variable compensation fields are now only available with the variable compensation form.</span></span>

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a><span data-ttu-id="8b55e-126">Puhkusetaotlused on lubatud enne registreerimist, kui selle puhkuse tüübi minimaalne saldo on negatiivne (469917)</span><span class="sxs-lookup"><span data-stu-id="8b55e-126">Leave requests allowed before enrollment if that leave type has a negative minimum balance (469917)</span></span>

<span data-ttu-id="8b55e-127">See muudatus keelab puhkusetaotluste sisestamise enne plaani registreerimist, isegi kui registreerimisel on negatiivne miinimaalne saldo.</span><span class="sxs-lookup"><span data-stu-id="8b55e-127">This change prohibits entering leave requests before being enrolled in the plan, even if the enrollment has a negative minimum balance.</span></span> <span data-ttu-id="8b55e-128">Saate sisestada või esitada taotlusi ainult siis, kui plaan on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="8b55e-128">You can only enter or submit requests when the plan is active.</span></span>

### <a name="document-templates-dont-download-457279"></a><span data-ttu-id="8b55e-129">Dokumendimalle ei saa alla laadida (457279)</span><span class="sxs-lookup"><span data-stu-id="8b55e-129">Document templates don't download (457279)</span></span>

<span data-ttu-id="8b55e-130">Selle muudatuse abil saate nüüd kõik dokumendimallid alla laadida.</span><span class="sxs-lookup"><span data-stu-id="8b55e-130">With this change, you can now download all document templates.</span></span> 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a><span data-ttu-id="8b55e-131">Andmed kuvatakse hüvituse plaani aruande välja Palgamäär ridade asemel veerupäises (476077)</span><span class="sxs-lookup"><span data-stu-id="8b55e-131">Data displays as column headers instead of rows for the Pay rate field in the compensation plan report (476077)</span></span>

<span data-ttu-id="8b55e-132">Analüüsi aruanne kuvab nüüd jaotises **Palgamäär** õiget teavet.</span><span class="sxs-lookup"><span data-stu-id="8b55e-132">The analytics report now displays the correct information for **Pay rate**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="8b55e-133">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="8b55e-133">In preview</span></span>

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="8b55e-134">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="8b55e-134">Human Resources application in Teams</span></span>

<span data-ttu-id="8b55e-135">Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8b55e-135">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="8b55e-136">Nad saavad suhelda botiga, et luua puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="8b55e-136">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="8b55e-137">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="8b55e-137">For more information, see:</span></span>

- <span data-ttu-id="8b55e-138">[Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 1 plaanis</span><span class="sxs-lookup"><span data-stu-id="8b55e-138">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="8b55e-139">[Teamsi rakendus Human Resources](./hr-admin-teams-leave-app.md) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="8b55e-139">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="8b55e-140">Rakendus Human Resources Teamsis eelversioonifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="8b55e-140">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="8b55e-141">**Teatised**: vaba aja taotluste esitajaid ja kinnitajaid teavitatakse Teamsi rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8b55e-141">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="8b55e-142">Kinnitajad saavad puhkeajataotlusi heaks kiita või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="8b55e-142">Approvers will be able to approve or deny time-off requests.</span></span> <span data-ttu-id="8b55e-143">Kui taotlus on heaks kiidetud või tagasi lükatud, teavitatakse sellest edastajat.</span><span class="sxs-lookup"><span data-stu-id="8b55e-143">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="8b55e-144">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="8b55e-144">For more information, see:</span></span>
   - <span data-ttu-id="8b55e-145">[Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis</span><span class="sxs-lookup"><span data-stu-id="8b55e-145">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="8b55e-146">[Teamsi rakenduse Human Resources teatiste lubamine](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="8b55e-146">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="8b55e-147">[Üksikutele kasutajate jaoks Teamsi teatiste sisse- või väljalülitamine](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) Rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="8b55e-147">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="8b55e-148">[Teamsi teatised](./hr-teams-leave-app.md#respond-to-teams-notifications) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="8b55e-148">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="8b55e-149">[Oma töörühma puhkusekalendri vaatamine](./hr-teams-leave-app.md#view-your-teams-leave-calendar) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="8b55e-149">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="8b55e-150">**Juhi vaba aja kalender**: juhid saavad vaadata oma otseste alluvate kinnitatud ja ootel vabu aegu kalendrivaates.</span><span class="sxs-lookup"><span data-stu-id="8b55e-150">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="8b55e-151">Selle vaate abil näeb hõlpsalt, millal nende meeskonnaliikmed töölt puuduvad.</span><span class="sxs-lookup"><span data-stu-id="8b55e-151">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="8b55e-152">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="8b55e-152">For more information, see:</span></span>
   - <span data-ttu-id="8b55e-153">[Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis</span><span class="sxs-lookup"><span data-stu-id="8b55e-153">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="8b55e-154">[Oma töörühma puhkusekalendri vaatamine](./hr-teams-leave-app.md#view-your-teams-leave-calendar) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="8b55e-154">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="8b55e-155">Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks (477004)</span><span class="sxs-lookup"><span data-stu-id="8b55e-155">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="8b55e-156">Nüüd on saadaval uus suvand loendi **Mulle määratud tööüksused** paigutamiseks armatuurlaua parempoolsesse veergu.</span><span class="sxs-lookup"><span data-stu-id="8b55e-156">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="8b55e-157">Selle muudatusega kuvatakse kõik tööüksused ja ülesandeloendid samas alas.</span><span class="sxs-lookup"><span data-stu-id="8b55e-157">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="8b55e-158">Lubage see funktsioon, lülitades funktsioonihalduses sisse suvandi **Eelversioon – töövoo kasutuskogemuse täiustused**.</span><span class="sxs-lookup"><span data-stu-id="8b55e-158">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="8b55e-159">Lisateavet eelvaatefunktsioonide sisselülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="8b55e-159">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="8b55e-160">See funktsioon pakub ka töövoosuvandeid, mis kuvatakse personalitoimingute vormidel.</span><span class="sxs-lookup"><span data-stu-id="8b55e-160">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="8b55e-161">Töövoosuvandid kuvatakse kiireks juurdepääsuks ka tegevuse kiirkaardi kohal.</span><span class="sxs-lookup"><span data-stu-id="8b55e-161">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="8b55e-162">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="8b55e-162">For more information, see:</span></span> 

- <span data-ttu-id="8b55e-163">[Organisatsiooni ja personalijuhtimise töövoo kasutuskogemuse täiustused](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis</span><span class="sxs-lookup"><span data-stu-id="8b55e-163">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Mulle määratud tööüksused](./media/hr-workflow-work-items-assigned-to-me.png)

![Töövoo üksuste kiirjuurdepääs](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a><span data-ttu-id="8b55e-166">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="8b55e-166">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="8b55e-167">Dataverse'is kaasatud kontroll-loendi üksused</span><span class="sxs-lookup"><span data-stu-id="8b55e-167">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="8b55e-168">Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="8b55e-168">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="8b55e-169">Soodustuste halduse põhjusekoodid</span><span class="sxs-lookup"><span data-stu-id="8b55e-169">Benefits management reason codes</span></span>

<span data-ttu-id="8b55e-170">Soodustuste halduse põhjusekoodid kombineeritakse peagi Human Resourcesi olemasolevate põhjusekoodidega.</span><span class="sxs-lookup"><span data-stu-id="8b55e-170">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="8b55e-171">Kui lõite soodustuste halduses põhjusekoodid, mis on pikemad kui 15 tähemärki, peate soodustuste halduse vormil **Põhjusekoodid** muutma põhjusekoodi nime nii, et see poleks pikem kui 15 tähemärki.</span><span class="sxs-lookup"><span data-stu-id="8b55e-171">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="8b55e-172">Pärast nime värskendamist kuvatakse põhjusekood personalihalduse olemasoleva põhjusekoodi vormi all.</span><span class="sxs-lookup"><span data-stu-id="8b55e-172">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="8b55e-173">See muudatus on tulevikus saadaval ja see ei mõjuta olemasolevaid funktsioone.</span><span class="sxs-lookup"><span data-stu-id="8b55e-173">This change will be available in the future and won't affect existing functionally.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b55e-174">Vt ka</span><span class="sxs-lookup"><span data-stu-id="8b55e-174">See also</span></span>

[<span data-ttu-id="8b55e-175">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="8b55e-175">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="8b55e-176">Dynamics 365 Human Resourcesi 2019. aasta väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="8b55e-176">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="8b55e-177">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="8b55e-177">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="8b55e-178">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="8b55e-178">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
