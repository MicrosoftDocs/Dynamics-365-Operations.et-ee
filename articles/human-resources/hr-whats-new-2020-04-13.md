---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (13. aprill, 2020)?
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 13. aprilli 2020 uusi või muutunud funktsioone.
author: andreabichsel
manager: tfehr
ms.date: 04/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3afc112f8a30bb187fbe37c9062afe7943e986ec
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127893"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="a19a6-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (13. aprill, 2020)?</span><span class="sxs-lookup"><span data-stu-id="a19a6-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a19a6-104">Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="a19a6-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a19a6-105">Muudatused rakenduvad versioonile number 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="a19a6-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="a19a6-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="a19a6-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="a19a6-107">Uus tootmise väljalaskesagedus</span><span class="sxs-lookup"><span data-stu-id="a19a6-107">New production release cadence</span></span>

<span data-ttu-id="a19a6-108">Alates selle nädala väljalaskest läheb Human Resourcesi väljalaskesagedus üle iganädalaselt värskenduselt kahenädalasele.</span><span class="sxs-lookup"><span data-stu-id="a19a6-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="a19a6-109">Ohutute juurutustavadega vastavusse viimise tagamiseks ning teenuse stabiilsuse ja töökindluse kõrgete standardite säilitamiseks kestab teenusevärskenduste juurutamine nüüd kõigisse piirkondadesse kaks nädalat.</span><span class="sxs-lookup"><span data-stu-id="a19a6-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="a19a6-110">Täiendavad katsetamis- ja jälgimismeetodid on täidetud, et kinnitada edukat juurutamist protsessi igas etapis.</span><span class="sxs-lookup"><span data-stu-id="a19a6-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="a19a6-111">Väljalaskesageduse kohta lisateabe saamiseks vaadake teemat [Värskendusprotsess](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="a19a6-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="a19a6-112">Ümardamistäpsuse välja ei saa pärast ümardamise tüübi määramist redigeerida (435616)</span><span class="sxs-lookup"><span data-stu-id="a19a6-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="a19a6-113">Selle muudatusega on väli **Ümardamistäpsus** nüüd saadaval pärast välja **Ümardamise tüüp** värskendamist.</span><span class="sxs-lookup"><span data-stu-id="a19a6-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="a19a6-114">Puhkuse registreerimise lõppkuupäeva ei saa redigeerida, kui puhkuse plaanil pole viitvõlgade perioode (413628)</span><span class="sxs-lookup"><span data-stu-id="a19a6-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="a19a6-115">Nüüd saate muuta registreerimise lõppkuupäeva, ilma et kuvatakse tõrketeate „Välja lisandumise kuupäeva alus peab olema täidetud”.</span><span class="sxs-lookup"><span data-stu-id="a19a6-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a><span data-ttu-id="a19a6-116">Tööhõive üksust ei sünkroonita Dataverse'iga (430834)</span><span class="sxs-lookup"><span data-stu-id="a19a6-116">Employment entity doesn't sync to Dataverse (430834)</span></span>

<span data-ttu-id="a19a6-117">See muudatus parandab probleemi, mille korral töötamise andmeid ei sünkroonitud Dataverse'iga pärast finantsdimensioonide lisamist.</span><span class="sxs-lookup"><span data-stu-id="a19a6-117">This change corrects an issue where the employment data wasn't syncing to Dataverse after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="a19a6-118">Töökalendri ajaintervalli üksuse (431775) mitme ülemüksuse eemaldamine</span><span class="sxs-lookup"><span data-stu-id="a19a6-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="a19a6-119">See muudatus eemaldab **töökalendri ajaintervalli** üksuse mitu ülemüksust.</span><span class="sxs-lookup"><span data-stu-id="a19a6-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="a19a6-120">Filtri CAST funktsiooniga ei tööta OData kutse ametikoha töötaja määramise üksuses (431699)</span><span class="sxs-lookup"><span data-stu-id="a19a6-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="a19a6-121">See värskendus sisaldab muudatust, et lubada ODatas CAST-i funktsiooniga filter üksuse **Ametikoha töötaja määramine** jaoks.</span><span class="sxs-lookup"><span data-stu-id="a19a6-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="a19a6-122">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="a19a6-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="a19a6-123">Puhkuse peatamine</span><span class="sxs-lookup"><span data-stu-id="a19a6-123">Leave suspension</span></span>

<span data-ttu-id="a19a6-124">Saate peatada töövõtja puhkuse Human Resourcesis.</span><span class="sxs-lookup"><span data-stu-id="a19a6-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="a19a6-125">Puhkuse peatamine lõpetab puhkuse viitvõlad valitud puhkusetüüpide puhul.</span><span class="sxs-lookup"><span data-stu-id="a19a6-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="a19a6-126">Kui peatamine toimub pärast viitvõla töötlemist, loob peatatav puhkus eelmääratud korrigeerimise töötaja puhkusesaldo jaoks.</span><span class="sxs-lookup"><span data-stu-id="a19a6-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="a19a6-127">Lisateabe saamiseks vt [Puhkuse peatamine](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="a19a6-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="a19a6-128">Edasikandmise reeglid</span><span class="sxs-lookup"><span data-stu-id="a19a6-128">Carry forward rules</span></span>

<span data-ttu-id="a19a6-129">Saate määrata edasikandmise puhkuse tüübi edasikantavale saldole, mille edasikandmise korrigeerimised kantakse üle.</span><span class="sxs-lookup"><span data-stu-id="a19a6-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="a19a6-130">Näiteks kui töövõtja kannab edasi 10 päeva, saate valida nende 10 päeva jaoks teistsuguse puhkuse tüübi.</span><span class="sxs-lookup"><span data-stu-id="a19a6-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="a19a6-131">Lisateabe saamiseks vt [Puhkuse ja puudumise tüüpide konfigureerimine](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="a19a6-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="a19a6-132">Teadaolevad probleemid</span><span class="sxs-lookup"><span data-stu-id="a19a6-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="a19a6-133">Tööhõive üksikasjade üksus</span><span class="sxs-lookup"><span data-stu-id="a19a6-133">Employment Details entity</span></span>

<span data-ttu-id="a19a6-134">**Tööhõive üksikasjade** üksus on värskendatud järgmiste väljadega:</span><span class="sxs-lookup"><span data-stu-id="a19a6-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="a19a6-135">**Maksesagedus**</span><span class="sxs-lookup"><span data-stu-id="a19a6-135">**PayFrequency**</span></span>
- <span data-ttu-id="a19a6-136">**Tööhõive kategooria ID**</span><span class="sxs-lookup"><span data-stu-id="a19a6-136">**Employment Category ID**</span></span>
- <span data-ttu-id="a19a6-137">**Tööhõive tüüp**</span><span class="sxs-lookup"><span data-stu-id="a19a6-137">**Employment Type**</span></span>
- <span data-ttu-id="a19a6-138">**Tööhõive tüübi ID**</span><span class="sxs-lookup"><span data-stu-id="a19a6-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="a19a6-139">**Soodustuse tööhõive olek**</span><span class="sxs-lookup"><span data-stu-id="a19a6-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="a19a6-140">Nende väljade häälestamise andmed sõltuvad **funktsioonihalduses** lubatavast eeliste haldusest.</span><span class="sxs-lookup"><span data-stu-id="a19a6-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="a19a6-141">Ärge asustage ega värskendage neid välju olemis **Tööhõive üksikasjad**, kuna see põhjustab importimisel tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="a19a6-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="a19a6-142">SharePointi eelvaade ei tööta mõnes keskkonnas</span><span class="sxs-lookup"><span data-stu-id="a19a6-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="a19a6-143">Kui SharePointi talletatud dokumentide dokumendieelvaade ei tööta, proovige järgmist toimingut.</span><span class="sxs-lookup"><span data-stu-id="a19a6-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="a19a6-144">Kinnitage, et administraatori kasutajakontol on kasutaja kirjega seotud meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="a19a6-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="a19a6-145">Seda teavet saate vaadata lehel **Kasutaja**.</span><span class="sxs-lookup"><span data-stu-id="a19a6-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="a19a6-146">Kui meiliaadressi ei ole seadistatud, peate lisama meili ja pakkuja OData Exceli lisandmooduli kaudu.</span><span class="sxs-lookup"><span data-stu-id="a19a6-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="a19a6-147">Vaikimisi ei ole Exceli kujunduses meiliaadressi kaasatud.</span><span class="sxs-lookup"><span data-stu-id="a19a6-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="a19a6-148">Peate redigeerima Exceli kujundust, lisama kõik väljad, rakendama ja värskendama.</span><span class="sxs-lookup"><span data-stu-id="a19a6-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="a19a6-149">Kui olete need toimingud teinud, saate värskendada administraatori kontot.</span><span class="sxs-lookup"><span data-stu-id="a19a6-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="a19a6-150">Kui administraatoril on seostatud meilikonto, logige sisse Human Resourcesisse administraatori mandaatidega.</span><span class="sxs-lookup"><span data-stu-id="a19a6-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="a19a6-151">Juurdepääs SharePointi manusele dokumendieelvaate käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="a19a6-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="a19a6-152">Logige sisse teise kasutajakontoga, millel on juurdepääs manustele ja kinnitage, et eelvaade töötab ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="a19a6-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="a19a6-153">Vt ka</span><span class="sxs-lookup"><span data-stu-id="a19a6-153">See also</span></span>

[<span data-ttu-id="a19a6-154">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="a19a6-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="a19a6-155">Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="a19a6-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="a19a6-156">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="a19a6-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="a19a6-157">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="a19a6-157">Manage features</span></span>](hr-admin-manage-features.md)