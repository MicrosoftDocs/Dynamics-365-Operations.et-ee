---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (18. veebruar 2020)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 60b46f5bd8f5eeae8aedc9bf81f1e7892caa0c93
ms.sourcegitcommit: bd9ff0d28718d535356ffbe1cffaaf60310dd430
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/13/2020
ms.locfileid: "3555335"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-18-2020"></a><span data-ttu-id="69f95-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (18. veebruar 2020)</span><span class="sxs-lookup"><span data-stu-id="69f95-103">What's new or changed in Dynamics 365 Human Resources (February 18, 2020)</span></span>

<span data-ttu-id="69f95-104">Selles artiklis kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="69f95-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="69f95-105">Muudatused rakenduvad versioonile number 8.1.2903.</span><span class="sxs-lookup"><span data-stu-id="69f95-105">Changes apply to build number 8.1.2903.</span></span> <span data-ttu-id="69f95-106">Sulgudes olevad numbrid mõnedes pealkirjades viitavad LCS-i toenumbritele viitamise jaoks.</span><span class="sxs-lookup"><span data-stu-id="69f95-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="platform-update-32"></a><span data-ttu-id="69f95-107">Platvormivärskendus update 32</span><span class="sxs-lookup"><span data-stu-id="69f95-107">Platform update 32</span></span> 

<span data-ttu-id="69f95-108">Platvormivärskendus 32 on nüüd saadaval.</span><span class="sxs-lookup"><span data-stu-id="69f95-108">Platform update 32 is now available.</span></span> <span data-ttu-id="69f95-109">Lisateavet leiate teemast [Teenuse Finance and Operationsi platvormivärskenduse 32 uued või muudetud funktsioonid (veebruar 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span><span class="sxs-lookup"><span data-stu-id="69f95-109">For more information, see [What's new or changed in Platform update 32 for Finance and Operations (February 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32).</span></span>

## <a name="search-values-are-remembered-when-changing-view-options-in-streamlined-employee-form-383833"></a><span data-ttu-id="69f95-110">Otsinguväärtusi mäletatakse, kui sujuva töötaja vormi vaatevalikuid muudetakse (383833)</span><span class="sxs-lookup"><span data-stu-id="69f95-110">Search values are remembered when changing view options in streamlined employee form (383833)</span></span>

<span data-ttu-id="69f95-111">Uue vorm **Töötaja** jätab nüüd otsinguväärtused meelde, kui muudate vaate suvandeid ja rakendate muudatused.</span><span class="sxs-lookup"><span data-stu-id="69f95-111">The new **Worker** form now remembers  search values when you change the view options and apply changes.</span></span>

## <a name="compensation-management-summary-tiles-in-preview-feature-redirect-to-wrong-form-401861"></a><span data-ttu-id="69f95-112">Hüvituste halduse kokkuvõttepaanid eelvaate funktsioonis suunavad valele vormile (401861)</span><span class="sxs-lookup"><span data-stu-id="69f95-112">Compensation management summary tiles in preview feature redirect to wrong form (401861)</span></span>

<span data-ttu-id="69f95-113">Põhipalga ja tulemustasu halduspaanid kuvavad nüüd uues vormis **Töötaja** õigeid kirjeid.</span><span class="sxs-lookup"><span data-stu-id="69f95-113">Fixed and variable compensation management tiles now display the correct records in the new **Worker** form.</span></span> <span data-ttu-id="69f95-114">Kehtib ainult sujuva töötaja vormi eelvaate funktsioonile.</span><span class="sxs-lookup"><span data-stu-id="69f95-114">Applies only to the streamlined employee form preview feature.</span></span> <span data-ttu-id="69f95-115">Saate lubada selle eelvaate funktsiooni suvandis **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="69f95-115">You can enable this preview feature in **Feature management**.</span></span> <span data-ttu-id="69f95-116">Lisateabe saamiseks vaadake jaotist [Funktsioonide haldamine](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="69f95-116">For more information, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="empty-status-field-for-some-leave-request-records-in-common-data-service-414915"></a><span data-ttu-id="69f95-117">Teenuse Common Data Service osade puhkusetaotluste kirjete väli Olek on tühi (414915)</span><span class="sxs-lookup"><span data-stu-id="69f95-117">Empty Status field for some leave request records in Common Data Service (414915)</span></span>

<span data-ttu-id="69f95-118">See muudatus parandab teenuse Common Data Service probleemi, kui väli **Olek** puhkusetaotluses on seatud olekusse **Ülevaatus**.</span><span class="sxs-lookup"><span data-stu-id="69f95-118">This change corrects an issue in Common Data Service when the **Status** field in a leave request is set to **Review**.</span></span> <span data-ttu-id="69f95-119">Common Data Service peegeldab nüüd olekut.</span><span class="sxs-lookup"><span data-stu-id="69f95-119">Common Data Service now reflects the status.</span></span>

## <a name="skill-gap-analysis-only-possible-for-assigned-job-411390"></a><span data-ttu-id="69f95-120">Oskuste erinevuse analüüs on võimalik ainult määratud töö jaoks (411390)</span><span class="sxs-lookup"><span data-stu-id="69f95-120">Skill gap analysis only possible for assigned job (411390)</span></span>

<span data-ttu-id="69f95-121">Nüüd saate teha oskuste erinevuse analüüsi mis tahes rakenduse Human Resources määratletud töö jaoks.</span><span class="sxs-lookup"><span data-stu-id="69f95-121">You can now do a skill gap analysis on any job defined in Human Resources.</span></span>

## <a name="system-currency-doesnt-sync-from-common-data-service-to-human-resources-in-new-environments-418011"></a><span data-ttu-id="69f95-122">Süsteemi valuuta ei sünkroonita uutes keskkondades teenusest Common Data Service rakendusse Human Resources (418011)</span><span class="sxs-lookup"><span data-stu-id="69f95-122">System currency doesn't sync from Common Data Service to Human Resources in new environments (418011)</span></span>

<span data-ttu-id="69f95-123">Süsteemi valuuta saab nüüd sünkroonida teenusest Common Data Service rakendusse Human Resources.</span><span class="sxs-lookup"><span data-stu-id="69f95-123">The system currency in Common Data Service can now sync to Human Resources.</span></span>

## <a name="in-preview"></a><span data-ttu-id="69f95-124">Eelvaates</span><span class="sxs-lookup"><span data-stu-id="69f95-124">In preview</span></span>

- [<span data-ttu-id="69f95-125">Puhkuste ja puudumiste eelvaatefunktsioonid</span><span class="sxs-lookup"><span data-stu-id="69f95-125">Leave and absence preview features</span></span>](hr-leave-and-absence-overview.md?leave-and-absence-preview-features)

- [<span data-ttu-id="69f95-126">Soodustuste halduse eelvaatefunktsioonid</span><span class="sxs-lookup"><span data-stu-id="69f95-126">Benefits management preview features</span></span>](hr-benefits-management-overview.md)

## <a name="coming-soon"></a><span data-ttu-id="69f95-127">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="69f95-127">Coming soon</span></span>

### <a name="updated-common-data-service-solution"></a><span data-ttu-id="69f95-128">Värskendatud lahendus Common Data Service</span><span class="sxs-lookup"><span data-stu-id="69f95-128">Updated Common Data Service solution</span></span>

<span data-ttu-id="69f95-129">Uus lahendus Common Data Service on varsti saadaval järgmiste muudatustega.</span><span class="sxs-lookup"><span data-stu-id="69f95-129">A new Common Data Service solution will be available soon with the following changes:</span></span>

| <span data-ttu-id="69f95-130">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="69f95-130">Description</span></span> | <span data-ttu-id="69f95-131">Muutmine</span><span class="sxs-lookup"><span data-stu-id="69f95-131">Change</span></span> |
| ----------------------------------------- | --- |
| <span data-ttu-id="69f95-132">Üksuse **Töö/ametikoht** muudatused</span><span class="sxs-lookup"><span data-stu-id="69f95-132">**Job/Position** entity changes</span></span> | <span data-ttu-id="69f95-133">Lisatud **Hüvituspiirkond**</span><span class="sxs-lookup"><span data-stu-id="69f95-133">**Compensation region** added</span></span></br><span data-ttu-id="69f95-134">Lisatud **Finantsdimensioonid**</span><span class="sxs-lookup"><span data-stu-id="69f95-134">**Financial dimensions** added</span></span> |
| <span data-ttu-id="69f95-135">Üksuse **Töötaja** muudatused</span><span class="sxs-lookup"><span data-stu-id="69f95-135">**Worker** entity changes</span></span> | <span data-ttu-id="69f95-136">Lisatud **Nimeseeria**</span><span class="sxs-lookup"><span data-stu-id="69f95-136">**Name sequence** added</span></span></br><span data-ttu-id="69f95-137">Lisatud **Töötab kodust**</span><span class="sxs-lookup"><span data-stu-id="69f95-137">**Works from home** added</span></span></br><span data-ttu-id="69f95-138">Lisatud **Keel**</span><span class="sxs-lookup"><span data-stu-id="69f95-138">**Language** added</span></span></br><span data-ttu-id="69f95-139">Lisatud **Staaži kuupäev**</span><span class="sxs-lookup"><span data-stu-id="69f95-139">**Seniority date** added</span></span></br><span data-ttu-id="69f95-140">Lisatud **Tähtpäeva kuupäev**</span><span class="sxs-lookup"><span data-stu-id="69f95-140">**Anniversary date** added</span></span></br><span data-ttu-id="69f95-141">Lisatud **Värbamise algne kuupäev**</span><span class="sxs-lookup"><span data-stu-id="69f95-141">**Original hire date** added</span></span> |
| <span data-ttu-id="69f95-142">Olemi **Tööhõive** muudatused</span><span class="sxs-lookup"><span data-stu-id="69f95-142">**Employment** entity changes</span></span> | <span data-ttu-id="69f95-143">Lisatud **Finantsdimensioonid**</span><span class="sxs-lookup"><span data-stu-id="69f95-143">**Financial dimensions** added</span></span></br><span data-ttu-id="69f95-144">Lisatud **Lõpetamise põhjus**</span><span class="sxs-lookup"><span data-stu-id="69f95-144">**Termination reason** added</span></span></br><span data-ttu-id="69f95-145">Suvand **Lõpetamiskuupäev** on nimetatud ümber suvandist **Üleviimise kuupäeva**</span><span class="sxs-lookup"><span data-stu-id="69f95-145">**Termination date** renamed from **Transition date**</span></span></br><span data-ttu-id="69f95-146">Lisatud **Katseaja kuupäev**</span><span class="sxs-lookup"><span data-stu-id="69f95-146">**Probation date** added</span></span> |
| <span data-ttu-id="69f95-147">Üksuse **Töötaja aadress** muudatused</span><span class="sxs-lookup"><span data-stu-id="69f95-147">**Worker address** entity changes</span></span> | <span data-ttu-id="69f95-148">Lisatud **Tänavanimi**</span><span class="sxs-lookup"><span data-stu-id="69f95-148">**Street address** added</span></span></br><span data-ttu-id="69f95-149">Suvandid **Aadressirida 1**, **Aadressirida 2** ja **Aadressirida 3** on märgistatud kasutuselt eemaldamiseks</span><span class="sxs-lookup"><span data-stu-id="69f95-149">**Address line 1**, **Address line 2**, and **Address line 3** marked for deprecation</span></span> |
| <span data-ttu-id="69f95-150">Uued ergutussüsteemi seadistuse üksused</span><span class="sxs-lookup"><span data-stu-id="69f95-150">New variable compensation setup entities</span></span> | <span data-ttu-id="69f95-151">**Muutuva hüvitisplaani tüüp**</span><span class="sxs-lookup"><span data-stu-id="69f95-151">**Compensation variable plan type**</span></span></br><span data-ttu-id="69f95-152">**Kompensatsiooni tulemusplaan**</span><span class="sxs-lookup"><span data-stu-id="69f95-152">**Compensation variable plan**</span></span></br><span data-ttu-id="69f95-153">**Pensionireeglid**</span><span class="sxs-lookup"><span data-stu-id="69f95-153">**Vesting rules**</span></span></br><span data-ttu-id="69f95-154">**Muutuva hüvitisplaani tase**</span><span class="sxs-lookup"><span data-stu-id="69f95-154">**Compensation variable plan level**</span></span> |
| <span data-ttu-id="69f95-155">Uus olem **Töötaja kalendri tööhõive**</span><span class="sxs-lookup"><span data-stu-id="69f95-155">New **Worker calendar employment** entity</span></span> | <span data-ttu-id="69f95-156">Lisatud **Töökalendri üksus**</span><span class="sxs-lookup"><span data-stu-id="69f95-156">**Work calendar entity** added</span></span> |
| <span data-ttu-id="69f95-157">Uus olem **Palgaarvestuse ametikoha üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="69f95-157">New **Payroll position detail** entity</span></span> | <span data-ttu-id="69f95-158">Lisatud **Palgaarvestuse ametikoha üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="69f95-158">**Payroll position detail** added</span></span> |
| <span data-ttu-id="69f95-159">Uus üksus **Ametinimetus**</span><span class="sxs-lookup"><span data-stu-id="69f95-159">New **Title** entity</span></span> | <span data-ttu-id="69f95-160">Lisatud **Ametinimetus**.</span><span class="sxs-lookup"><span data-stu-id="69f95-160">**Title** added.</span></span> <span data-ttu-id="69f95-161">Uus üksus **Pealkiri** kaasatakse sünkroonimisprotsessi rakenduse Human Resources ja teenuse Common Data Service vahel.</span><span class="sxs-lookup"><span data-stu-id="69f95-161">The new **Title** entity will be included in the sync process between Human Resources and Common Data Service.</span></span> <span data-ttu-id="69f95-162">Kuid algselt ei viidata sellele üksustelt **Ametikoht** või **Töö**.</span><span class="sxs-lookup"><span data-stu-id="69f95-162">It won't be initially referenced from **Job Position** or **Job** entities.</span></span> |

## <a name="see-also"></a><span data-ttu-id="69f95-163">Vt ka</span><span class="sxs-lookup"><span data-stu-id="69f95-163">See also</span></span>

[<span data-ttu-id="69f95-164">Mis on uut või mida on muudetud rakenduses Human Resources?</span><span class="sxs-lookup"><span data-stu-id="69f95-164">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="69f95-165">Dynamics 365 Human Resources 2019 väljalaskevoo 2 ülevaade</span><span class="sxs-lookup"><span data-stu-id="69f95-165">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="69f95-166">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="69f95-166">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="69f95-167">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="69f95-167">Manage features</span></span>](hr-admin-manage-features.md)