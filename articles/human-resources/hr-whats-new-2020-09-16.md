---
title: Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (16. september 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 16. septembri 2020 uusi või muutunud funktsioone.
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14a4c08b0d223bc7fd8044354f5976388af9176b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467453"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="953c7-103">Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (16. september 2020)</span><span class="sxs-lookup"><span data-stu-id="953c7-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="953c7-104">Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="953c7-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="953c7-105">Muudatused rakenduvad versioonile number 8.1.3557.</span><span class="sxs-lookup"><span data-stu-id="953c7-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="953c7-106">Sulgudes olevad numbrid mõne funktsiooni kõrval viitavad toenumbritele teenuses Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="953c7-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="953c7-107">Väljalase hõlmab järgmisi funktsioone</span><span class="sxs-lookup"><span data-stu-id="953c7-107">Included in this release</span></span>

-  [<span data-ttu-id="953c7-108">Salvestatud vaated – üldine kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="953c7-108">Saved views - general availability</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="953c7-109">- Lisateavet leiate teemast [Salvestatud vaated](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views).</span><span class="sxs-lookup"><span data-stu-id="953c7-109">- For more information, see [Saved views](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views).</span></span> 

- <span data-ttu-id="953c7-110">Vormil **Ametikoha tegevus** on värskendatud dimensioonide võrgustik ja uus dialoog (469495).</span><span class="sxs-lookup"><span data-stu-id="953c7-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="953c7-111">Kui seate **Human Resourcesi jagatud parameetrite** **täiustatud juurdepääsus** suvandi **Piira juurdepääsu töötaja teabele** väärtuseks jah, kuvatakse soodustuste vormides ainult asjakohaseid töötajaid (393384).</span><span class="sxs-lookup"><span data-stu-id="953c7-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="953c7-112">Uued kalendri loomise suvandid üksuses **WorkCalendar** (477055).</span><span class="sxs-lookup"><span data-stu-id="953c7-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="953c7-113">- Vaikelõppaeg</span><span class="sxs-lookup"><span data-stu-id="953c7-113">- Default ending time</span></span><br><span data-ttu-id="953c7-114">-    Vaikealgusaeg</span><span class="sxs-lookup"><span data-stu-id="953c7-114">-    Default starting time</span></span><br><span data-ttu-id="953c7-115">- Kas reede on tööpäev?</span><span class="sxs-lookup"><span data-stu-id="953c7-115">-  Is Friday working day</span></span><br><span data-ttu-id="953c7-116">- Kas esmaspäev on tööpäev?</span><span class="sxs-lookup"><span data-stu-id="953c7-116">-  Is Monday working day</span></span><br><span data-ttu-id="953c7-117">- Kas laupäev on tööpäev?</span><span class="sxs-lookup"><span data-stu-id="953c7-117">-  Is Saturday working day</span></span><br><span data-ttu-id="953c7-118">- Kas pühapäev on tööpäev?</span><span class="sxs-lookup"><span data-stu-id="953c7-118">- Is Sunday working day</span></span><br><span data-ttu-id="953c7-119">- Kas neljapäev on tööpäev?</span><span class="sxs-lookup"><span data-stu-id="953c7-119">- Is Thursday working day</span></span><br><span data-ttu-id="953c7-120">- Kas teisipäev on tööpäev?</span><span class="sxs-lookup"><span data-stu-id="953c7-120">- Is Tuesday working day</span></span><br><span data-ttu-id="953c7-121">- Kas kolmapäev on tööpäev?</span><span class="sxs-lookup"><span data-stu-id="953c7-121">- Is Wednesday working day</span></span><br><span data-ttu-id="953c7-122">- Töökalendri pühade ID</span><span class="sxs-lookup"><span data-stu-id="953c7-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="953c7-123">Üksus **LeaveBankTransactionV1** sisaldab nüüd põhjusekoodi (477823).</span><span class="sxs-lookup"><span data-stu-id="953c7-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="953c7-124">Nüüd saate salvestada tegevuse salvestisi (492923).</span><span class="sxs-lookup"><span data-stu-id="953c7-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="953c7-125">Andmeid avaldatakse nüüd üksusest **HCMWorkerContactEntity** edukalt (427620).</span><span class="sxs-lookup"><span data-stu-id="953c7-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="953c7-126">Kiirkaardil **Palk** kuvatakse nüüd vormis **Töötaja tegevused** töövõtja töötaja tüüpi (482494).</span><span class="sxs-lookup"><span data-stu-id="953c7-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="953c7-127">Väljad **Tase** ja **Plaan** on nüüd kohustuslikud, kui seadistate suvandi **Põhipalk**.</span><span class="sxs-lookup"><span data-stu-id="953c7-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="953c7-128">Kui jätate need väljad tühjaks, kuvatakse tõrketeade (482497).</span><span class="sxs-lookup"><span data-stu-id="953c7-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="953c7-129">Väli **Plaani tüüp** on nüüd jaotises **Soodustused** ripploend (488768).</span><span class="sxs-lookup"><span data-stu-id="953c7-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="953c7-130">Süsteemiadministraatorid saavad nüüd teatise, kui kohandatud väli kustutatakse rakendusest Human Resources (481408).</span><span class="sxs-lookup"><span data-stu-id="953c7-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="953c7-131">Töötajaga lepingu lõpetamise protsessi käigus käitub rakendus Human Resources ootuspäraselt ja ei muuda valitud ettevõtet pärast näilist lukustumist (479877).</span><span class="sxs-lookup"><span data-stu-id="953c7-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="953c7-132">Juhatajad ei saa enam lisada numbriveerge isikupärastamise kaudu (485317).</span><span class="sxs-lookup"><span data-stu-id="953c7-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="953c7-133">Juhatajad ei saa enam eemaldada andmevahemiku filtrit aeguvatest ID-numbritest (485321).</span><span class="sxs-lookup"><span data-stu-id="953c7-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="953c7-134">Kui väli **Annab aru** on tühi, kuvatakse ametikoha üksikasjad selle kohal hõljudes ikkagi (433328).</span><span class="sxs-lookup"><span data-stu-id="953c7-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="953c7-135">Töövõtjad saavad nüüd vaadata soodustuste plaani teavet töövõtja iseteenindusest (481676).</span><span class="sxs-lookup"><span data-stu-id="953c7-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="953c7-136">Töövõtjad saavad nüüd vaadata kõiki registreeritud kursusi (429048).</span><span class="sxs-lookup"><span data-stu-id="953c7-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="953c7-137">Nüüd saate piirata lehel **Professionaalsed sertifikaadid** vaatamissuvandeid.</span><span class="sxs-lookup"><span data-stu-id="953c7-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="953c7-138">Saate piirata vaatamissuvandeid kõikidele peale praegusele juriidilisele isikule, töötaja oleku põhjal ja töötaja tüübi põhjal (451501).</span><span class="sxs-lookup"><span data-stu-id="953c7-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="953c7-139">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="953c7-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="953c7-140">Rakendus Human Resources Teamsis</span><span class="sxs-lookup"><span data-stu-id="953c7-140">Human Resources app in Teams</span></span>

<span data-ttu-id="953c7-141">Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="953c7-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="953c7-142">Nad saavad suhelda botiga, et luua puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="953c7-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="953c7-143">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="953c7-143">For more information, see:</span></span>

- <span data-ttu-id="953c7-144">[Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 1 plaanis</span><span class="sxs-lookup"><span data-stu-id="953c7-144">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="953c7-145">[Teamsi rakendus Human Resources](https://go.microsoft.com/fwlink/?linkid=2127841) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="953c7-145">[Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="953c7-146">Rakendus Human Resources Teamsis eelversioonifunktsioonid</span><span class="sxs-lookup"><span data-stu-id="953c7-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="953c7-147">**Teatised**: vaba aja taotluste esitajaid ja kinnitajaid teavitatakse Teamsi rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="953c7-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="953c7-148">Kinnitajad saavad eemalolekuajataotlusi heaks kiita või tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="953c7-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="953c7-149">Kui taotlus on heaks kiidetud või tagasi lükatud, teavitatakse sellest edastajat.</span><span class="sxs-lookup"><span data-stu-id="953c7-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="953c7-150">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="953c7-150">For more information, see:</span></span>
   - <span data-ttu-id="953c7-151">[Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis</span><span class="sxs-lookup"><span data-stu-id="953c7-151">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="953c7-152">[Teamsi rakenduse Human Resources teatiste lubamine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="953c7-152">[Enable notifications for the Human Resources app in Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="953c7-153">[Üksikutele kasutajate jaoks Teamsi teatiste sisse- või väljalülitamine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) Rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="953c7-153">[Turn Teams notifications on or off for individual users](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="953c7-154">[Teamsi teatised](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="953c7-154">[Teams notifications](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="953c7-155">[Oma töörühma puhkusekalendri vaatamine](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="953c7-155">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="953c7-156">**Juhataja eemalolekuaja kalender**: juhatajad saavad vaadata oma otseste alluvate kinnitatud ja ootel eemalolekuaegu kalendrivaates.</span><span class="sxs-lookup"><span data-stu-id="953c7-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="953c7-157">Selle vaate abil näeb hõlpsalt, millal nende meeskonnaliikmed töölt puuduvad.</span><span class="sxs-lookup"><span data-stu-id="953c7-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="953c7-158">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="953c7-158">For more information, see:</span></span>
   - <span data-ttu-id="953c7-159">[Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis</span><span class="sxs-lookup"><span data-stu-id="953c7-159">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="953c7-160">[Oma töörühma puhkusekalendri vaatamine](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) rakenduse Human Resources dokumentatsioonis</span><span class="sxs-lookup"><span data-stu-id="953c7-160">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="953c7-161">Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks (477004)</span><span class="sxs-lookup"><span data-stu-id="953c7-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="953c7-162">Nüüd on saadaval uus suvand loendi **Mulle määratud tööüksused** paigutamiseks armatuurlaua parempoolsesse veergu.</span><span class="sxs-lookup"><span data-stu-id="953c7-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="953c7-163">Selle muudatusega kuvatakse kõik tööüksused ja ülesandeloendid samas alas.</span><span class="sxs-lookup"><span data-stu-id="953c7-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="953c7-164">Lubage see funktsioon, lülitades funktsioonihalduses sisse suvandi **Eelversioon – töövoo kasutuskogemuse täiustused**.</span><span class="sxs-lookup"><span data-stu-id="953c7-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="953c7-165">Lisateavet eelvaatefunktsioonide sisselülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="953c7-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="953c7-166">See funktsioon pakub ka töövoosuvandeid, mis kuvatakse personalitoimingute vormidel.</span><span class="sxs-lookup"><span data-stu-id="953c7-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="953c7-167">Töövoosuvandid kuvatakse kiireks juurdepääsuks ka tegevuse kiirkaardi kohal.</span><span class="sxs-lookup"><span data-stu-id="953c7-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="953c7-168">Lisateabe saamiseks vt:</span><span class="sxs-lookup"><span data-stu-id="953c7-168">For more information, see:</span></span> 

- <span data-ttu-id="953c7-169">[Organisatsiooni ja personalijuhtimise töövoo kasutuskogemuse täiustused](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis</span><span class="sxs-lookup"><span data-stu-id="953c7-169">[Organization and personnel management workflow experience enhancements](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Mulle määratud tööüksused](./media/hr-workflow-work-items-assigned-to-me.png)

![Töövoo üksuste kiirjuurdepääs](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="953c7-172">Puhkuste ja puudumiste kalender</span><span class="sxs-lookup"><span data-stu-id="953c7-172">Leave and absence calendar</span></span>

<span data-ttu-id="953c7-173">See väljalase sisaldab täiendavaid kalendrisuvandeid puhkuste ja puudumiste kalendrite jaoks.</span><span class="sxs-lookup"><span data-stu-id="953c7-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="953c7-174">Lisateavet leiate teemast [Meeskonna ja ettevõtte kalendrite kuvamine](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).</span><span class="sxs-lookup"><span data-stu-id="953c7-174">For more information, see [View team and company calendars](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="953c7-175">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="953c7-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="953c7-176">Dataverse'is kaasatud kontroll-loendi üksused</span><span class="sxs-lookup"><span data-stu-id="953c7-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="953c7-177">Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Dataverse'is.</span><span class="sxs-lookup"><span data-stu-id="953c7-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="953c7-178">Soodustuste halduse põhjusekoodid</span><span class="sxs-lookup"><span data-stu-id="953c7-178">Benefits management reason codes</span></span>

<span data-ttu-id="953c7-179">Soodustuste halduse põhjusekoodid kombineeritakse peagi Human Resourcesi olemasolevate põhjusekoodidega.</span><span class="sxs-lookup"><span data-stu-id="953c7-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="953c7-180">Kui lõite soodustuste halduses põhjusekoodid, mis on pikemad kui 15 tähemärki, peate soodustuste halduse vormil **Põhjusekoodid** muutma põhjusekoodi nime nii, et see poleks pikem kui 15 tähemärki.</span><span class="sxs-lookup"><span data-stu-id="953c7-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="953c7-181">Pärast nime värskendamist kuvatakse põhjusekood personalihalduse olemasoleva põhjusekoodi vormi all.</span><span class="sxs-lookup"><span data-stu-id="953c7-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="953c7-182">See muudatus on saadaval tulevikus ja see ei mõjuta olemasolevaid funktsioone.</span><span class="sxs-lookup"><span data-stu-id="953c7-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="953c7-183">Vt ka</span><span class="sxs-lookup"><span data-stu-id="953c7-183">See also</span></span>

[<span data-ttu-id="953c7-184">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="953c7-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="953c7-185">Dynamics 365 Human Resourcesi 2019. aasta väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="953c7-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="953c7-186">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="953c7-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="953c7-187">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="953c7-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]