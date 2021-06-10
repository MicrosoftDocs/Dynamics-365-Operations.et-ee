---
title: Värskendamisprotsess
description: Microsoft Dynamics 365 Human Resources on tõeline tarkvara teenusena (Saas), mis pakub pidevaid, puutumatuid teenuse uuendusi rakenduse ja platvormi muudatustele.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2466c53885340991aeeb0a07af83517473b332b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053631"
---
# <a name="update-process"></a><span data-ttu-id="08383-103">Värskendamisprotsess</span><span class="sxs-lookup"><span data-stu-id="08383-103">Update process</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="08383-104">Microsoft Dynamics 365 Human Resources on tõeline tarkvara teenusena (Saas), mis pakub pidevaid, puutumatuid teenuse uuendusi.</span><span class="sxs-lookup"><span data-stu-id="08383-104">Microsoft Dynamics 365 Human Resources is a true software as a service (SaaS) that provides continuous, touchless service updates.</span></span> <span data-ttu-id="08383-105">Need värskendused sisaldavad nii rakenduse kui ka platvormi muudatusi, mis pakuvad sageli teenuse kriitilist täiustust, sh regulatiivsed uuendused.</span><span class="sxs-lookup"><span data-stu-id="08383-105">These updates contain both application and platform changes that often provide critical improvements to the service, including regulatory updates.</span></span>

## <a name="update-policy"></a><span data-ttu-id="08383-106">Värskenduspoliitika</span><span class="sxs-lookup"><span data-stu-id="08383-106">Update policy</span></span>

<span data-ttu-id="08383-107">Värskendusi antakse välja regulaarselt kõikides keskkondades.</span><span class="sxs-lookup"><span data-stu-id="08383-107">Updates are released on a regular cadence to all environments.</span></span> <span data-ttu-id="08383-108">Rakenduse Human Resources tugi põhineb [Microsofti elutsükli poliitikal](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), kust leiate terviklikud ja ennustatavad juhised toe saadavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="08383-108">Human Resources is supported according to the [Microsoft Lifecycle policy](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), which provides consistent and predictable guidelines for the availability of support.</span></span>

## <a name="release-cadence"></a><span data-ttu-id="08383-109">Väljaandmise sagedus</span><span class="sxs-lookup"><span data-stu-id="08383-109">Release cadence</span></span> 

<span data-ttu-id="08383-110">Rakenduse Human Resources värskendusi rakendatakse kõigile keskkondadele automaatselt.</span><span class="sxs-lookup"><span data-stu-id="08383-110">Human Resources updates are applied to all environments automatically.</span></span> <span data-ttu-id="08383-111">Human Resources pakub kahte tüüpi väljaandeid.</span><span class="sxs-lookup"><span data-stu-id="08383-111">Human Resources provides two types of releases:</span></span>

- <span data-ttu-id="08383-112">**Teenusevärskendused**: iga kahe nädala tagant toimuvad uuendused, mis sisaldavad veaparandusi ja uusi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="08383-112">**Service updates**: Updates occur every two weeks that include bug fixes and new features.</span></span> <span data-ttu-id="08383-113">Teenusevärskendused sisaldavad ka kehtivaid platvormi värskendusi, kui need väljastatakse.</span><span class="sxs-lookup"><span data-stu-id="08383-113">Service updates also include applicable Platform updates when they release.</span></span> <span data-ttu-id="08383-114">Et saada aimu, millal platvormi värskendusi väljastatakse, vt [tabelit 3: Platvormi väljaanded](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span><span class="sxs-lookup"><span data-stu-id="08383-114">To get an idea of when Platform updates are released, see [Table 3: Platform releases](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases).</span></span> <span data-ttu-id="08383-115">Kahenädalasi värskendusi levitatakse globaalselt kõigis piirkondades etapiliselt.</span><span class="sxs-lookup"><span data-stu-id="08383-115">Biweekly updates have a staged global rollout across regions.</span></span> <span data-ttu-id="08383-116">Lisateavet kahenädalaste uuenduste kohta vt teemat [Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources](hr-admin-whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="08383-116">For more information about biweekly updates, see [What's new or changed in Dynamics 365 Human Resources](hr-admin-whats-new.md).</span></span>

    <span data-ttu-id="08383-117">Kõik toetatud andmekeskused uuendatakse iga kahe nädala tagant, kui pole teisiti märgitud.</span><span class="sxs-lookup"><span data-stu-id="08383-117">All supported data centers update every two weeks, unless otherwise noted.</span></span> <span data-ttu-id="08383-118">USA, Austraalia, Euroopa, Suurbritannia, Aasia ja Kanada piirkonnad sisalduvad kahenädalastes uuendustes.</span><span class="sxs-lookup"><span data-stu-id="08383-118">US, Australia, Europe, UK, Asia, and Canada regions are included in biweekly updates.</span></span> 

- <span data-ttu-id="08383-119">**Lahenduse Dataverse värskendused**: need värskendused toimuvad vastavalt vajadusele ligikaudu iga kuue nädala järel.</span><span class="sxs-lookup"><span data-stu-id="08383-119">**Dataverse solution updates**: These updates occur approximately every six weeks, as needed.</span></span> <span data-ttu-id="08383-120">Need hõlmavad uusi üksusi ja muudatusi olemasolevatele üksustele rakenduses Dataverse.</span><span class="sxs-lookup"><span data-stu-id="08383-120">They include new entities and changes to existing entities in Dataverse.</span></span> <span data-ttu-id="08383-121">Need uuendused vabastatakse samadele piirkondadele kui kahenädalased uuendused ja neil kulub umbes kuus nädalat, et edastada läbi kõikide andmekeskuste.</span><span class="sxs-lookup"><span data-stu-id="08383-121">These updates release to the same regions as the biweekly updates, and they take about six weeks to replicate through all data centers.</span></span> <span data-ttu-id="08383-122">Lahenduse värskendused võivad, kuid ei pruugi olla vastavuses kahenädalaste teenuse uuendustega.</span><span class="sxs-lookup"><span data-stu-id="08383-122">Solution updates may or may not align with biweekly service updates.</span></span>

> [!NOTE]
> <span data-ttu-id="08383-123">Kui need on väljastatud, on lahenduse värskendused saadaval kõigis andmekeskustes.</span><span class="sxs-lookup"><span data-stu-id="08383-123">Solution updates are available on all data centers once they're released.</span></span> <span data-ttu-id="08383-124">Kui te ei soovi, et värskendused edastatakse automaatselt, saate neid värskendusi iga andmekeskuse igas keskkonnas käsitsi rakendada.</span><span class="sxs-lookup"><span data-stu-id="08383-124">If you don't want to wait for the updates to replicate automatically, you can manually apply these updates on any environment in any data center.</span></span>

<span data-ttu-id="08383-125">Vajadusel pakub rakendus Human Resources ka järgmist tüüpi parandusi.</span><span class="sxs-lookup"><span data-stu-id="08383-125">When needed, Human Resources also provides the following types of fixes:</span></span>

- <span data-ttu-id="08383-126">**Redaktsioon (kiirparandus)**: veaparandused, mis võivad ilmneda kas koos kahenädalase teenuseuuenduse väljalaskega või eraldi</span><span class="sxs-lookup"><span data-stu-id="08383-126">**Revision (hotfix)**: Bug fixes that can occur either with or apart from a biweekly service update release</span></span>

- <span data-ttu-id="08383-127">**Erakorraline parandus**: ennetavad ja uuesti aktiivsed kiirparandused, mis on olemuselt eraldiseisvad, võivad sisaldada ainult konfiguratsiooni või koodi muudatusi, et lahendada avaldatud saidi probleeme, ja need võivad ilmneda kahenädalasest teenuseuuenduse väljaandest eraldi</span><span class="sxs-lookup"><span data-stu-id="08383-127">**Emergency fix**: Proactive and reactive hotfixes that are standalone in nature, can include configuration-only or code changes to resolve live site issues, and can occur apart from a biweekly service update release</span></span>

<span data-ttu-id="08383-128">Väljaanded vaadatakse üle, testitakse ja kontrollitakse sisemises keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="08383-128">Releases are reviewed, tested, and validated on an internal environment.</span></span> <span data-ttu-id="08383-129">Pärast järkude kinnitamist edastatakse need tootmisse.</span><span class="sxs-lookup"><span data-stu-id="08383-129">After builds are signed off, they're then deployed to production.</span></span>

## <a name="release-cadence-exceptions-in-2021"></a><span data-ttu-id="08383-130">Erandid väljaandmise sageduses 2021. aastal</span><span class="sxs-lookup"><span data-stu-id="08383-130">Release cadence exceptions in 2021</span></span>

<span data-ttu-id="08383-131">Puhkuse arvestamiseks on 2021. aasta novembri ja detsembri väljastusgraafik järgmine.</span><span class="sxs-lookup"><span data-stu-id="08383-131">To account for holidays, the release schedule for November and December 2021 is as follows:</span></span>

- <span data-ttu-id="08383-132">Novembri väljastus: 1. november – 14. november</span><span class="sxs-lookup"><span data-stu-id="08383-132">November release: November 1 - November 14</span></span>
- <span data-ttu-id="08383-133">Detsembri väljastus: 29. november – 12. detsember</span><span class="sxs-lookup"><span data-stu-id="08383-133">December release: November 29 - December 12</span></span>
 
<span data-ttu-id="08383-134">Kahenädalane väljaandmise sagedus jätkub tavapäraselt 10. jaanuaril 2022.</span><span class="sxs-lookup"><span data-stu-id="08383-134">The two-week release cadence will resume as usual on January 10, 2022.</span></span>

## <a name="communications"></a><span data-ttu-id="08383-135">Suhtlus</span><span class="sxs-lookup"><span data-stu-id="08383-135">Communications</span></span>

<span data-ttu-id="08383-136">Saate teada, mis on rakenduses Human Resources töös ja mida oleme väljastanud, järgmistes asukohtades:</span><span class="sxs-lookup"><span data-stu-id="08383-136">You can find out what's in the works for Human Resources and what we've released in the following locations:</span></span>

- [<span data-ttu-id="08383-137">Dynamics 365 Human Resourcesi teejuht</span><span class="sxs-lookup"><span data-stu-id="08383-137">Dynamics 365 Human Resources roadmap</span></span>](https://dynamics.microsoft.com/roadmap/human-resources/)

- [<span data-ttu-id="08383-138">Dynamics 365 väljalaskeplaanid</span><span class="sxs-lookup"><span data-stu-id="08383-138">Dynamics 365 Release Plans</span></span>](/dynamics365/release-plans/)

- [<span data-ttu-id="08383-139">Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources?</span><span class="sxs-lookup"><span data-stu-id="08383-139">What's new or changed in Dynamics 365 Human Resources</span></span>](hr-admin-whats-new.md)

- <span data-ttu-id="08383-140">[Teenuse Lifecycle Services (LCS) teema otsing](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (ainult platvormiga seotud vigade jaoks)</span><span class="sxs-lookup"><span data-stu-id="08383-140">[Issue search in Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (for Platform-related bugs only)</span></span>

- [<span data-ttu-id="08383-141">Rakenduse Human Resources blogi</span><span class="sxs-lookup"><span data-stu-id="08383-141">Human Resources blog</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [<span data-ttu-id="08383-142">Rakenduse Human Resources Yammeri kogukond</span><span class="sxs-lookup"><span data-stu-id="08383-142">Human Resources Yammer community</span></span>](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a><span data-ttu-id="08383-143">Liivakastikeskkonna eelvaatefunktsioonid</span><span class="sxs-lookup"><span data-stu-id="08383-143">Preview features in a sandbox environment</span></span>

<span data-ttu-id="08383-144">Enne nende tootmiskeskkonnas lubamist saate eelvaatefunktsioonid liivakastikeskkonnas kinnitada.</span><span class="sxs-lookup"><span data-stu-id="08383-144">You can validate preview features in a sandbox environment before enabling them in your production environment.</span></span> <span data-ttu-id="08383-145">Lisateavet funktsioonide lubamise kohta vt [Funktsioonihalduse ülevaade](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="08383-145">For more information about enabling features, see [Feature management overview](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="08383-146">Kõik uued funktsioonid jäävad vähemalt 30 päevaks eelvaatesse ja tavaliselt 30–60 päevaks.</span><span class="sxs-lookup"><span data-stu-id="08383-146">All new features remain in preview for at least 30 days, and typically 30-60 days.</span></span> <span data-ttu-id="08383-147">Peamised funktsioonid on tavaliselt saadaval eelvaate perioodile järgneva iga aasta oktoobris ja aprillis.</span><span class="sxs-lookup"><span data-stu-id="08383-147">Major features are generally available in October and April of each year following the preview period.</span></span> <span data-ttu-id="08383-148">Kohe kui näete tööruumis Funktsioonihaldus uusi võimalusi, saate need sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="08383-148">As soon as you see new capabilities in the Feature management workspace, you can turn them on.</span></span> <span data-ttu-id="08383-149">Mõned funktsioonid võivad olla vaikimisi sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="08383-149">Some features may be on by default.</span></span>

<span data-ttu-id="08383-150">Mõnikord on lahutamatu funktsioon vaikimisi sisse lülitatud ja seda ei saa välja lülitada (nt tööruum Funktsioonihaldus).</span><span class="sxs-lookup"><span data-stu-id="08383-150">At times, an integral feature will be on by default and can't be turned off (for example, the Feature management workspace).</span></span>

<span data-ttu-id="08383-151">Kui funktsioon on üldsusele saadaval, võib selle tootmiskeskkonnas sisse või välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="08383-151">Once a feature is generally available, it may be turned on or off in production environments.</span></span> <span data-ttu-id="08383-152">Tööruum Funktsioonihaldus näitab, millal muutub eelvaate funktsioon kohustuslikuks.</span><span class="sxs-lookup"><span data-stu-id="08383-152">The Feature management workspace indicates when a preview feature will become mandatory.</span></span> <span data-ttu-id="08383-153">See kuupäev on tavaliselt 1. oktoobril või 1. aprillil, et ühitada poolaasta väljalaskeplaanidega.</span><span class="sxs-lookup"><span data-stu-id="08383-153">This date is usually on October 1 or April 1 to align with the semiannual release plans.</span></span> <span data-ttu-id="08383-154">Kohustuslikke funktsioone välja lülitada ei saa.</span><span class="sxs-lookup"><span data-stu-id="08383-154">You can't turn off mandatory features.</span></span> <span data-ttu-id="08383-155">Kuni see muutub kohustuslikuks, saate funktsiooni kõikides keskkondades sisse ja välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="08383-155">Until it becomes mandatory, you can turn a feature on and off in all environments.</span></span>

<span data-ttu-id="08383-156">Soovitame tungivalt vaadata funktsioone liivakasti- või prooviversiooni keskkonnas eelvaates.</span><span class="sxs-lookup"><span data-stu-id="08383-156">We highly recommend previewing features in a sandbox or trial environment.</span></span> <span data-ttu-id="08383-157">Kõige parem on luua liivakastikeskkonda koopia oma praegusest keskkonnast või andmebaasist, et saaksite oma andmetega uusi funktsioone täielikult kogeda.</span><span class="sxs-lookup"><span data-stu-id="08383-157">It's best to create a copy of your current production environment or database into a sandbox environment so you can get the complete experience of the new features with your data.</span></span>

<span data-ttu-id="08383-158">Lisateavet liivakastikeskkonna ettevalmistamise kohta vt [Rakenduse Human Resources projekti ettevalmistamine](hr-admin-setup-provision.md).</span><span class="sxs-lookup"><span data-stu-id="08383-158">For more information about provisioning a sandbox environment, see [Provision a Human Resources project](hr-admin-setup-provision.md).</span></span> <span data-ttu-id="08383-159">Proovikeskkonna eemaldamiseks vt [Eksemplari eemaldamine](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span><span class="sxs-lookup"><span data-stu-id="08383-159">To remove a test environment, see [Remove an instance](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment).</span></span> 

## <a name="report-bugs"></a><span data-ttu-id="08383-160">Vigadest teatamine</span><span class="sxs-lookup"><span data-stu-id="08383-160">Report bugs</span></span>

<span data-ttu-id="08383-161">Eelvaatefunktsioonide testimisel või uute võimaluste proovimisel võite leida üksuseid, mis ei tööta ootuspäraselt.</span><span class="sxs-lookup"><span data-stu-id="08383-161">While testing preview features or trying new capabilities, you might find items that don't work as expected.</span></span> <span data-ttu-id="08383-162">Andke kõikidest vigadest [Microsoft Dynamics 365 toe](https://dynamics.microsoft.com/support/) kaudu teada.</span><span class="sxs-lookup"><span data-stu-id="08383-162">Please report any bugs through [Microsoft Dynamics 365 support](https://dynamics.microsoft.com/support/).</span></span>

## <a name="see-also"></a><span data-ttu-id="08383-163">Vt ka</span><span class="sxs-lookup"><span data-stu-id="08383-163">See also</span></span>

[<span data-ttu-id="08383-164">Dynamics 365 ja Power Platformi väljalaskeplaanid</span><span class="sxs-lookup"><span data-stu-id="08383-164">Dynamics 365 and Power Platform Release Plans</span></span>](/dynamics365/release-plans)</br>
[<span data-ttu-id="08383-165">Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources?</span><span class="sxs-lookup"><span data-stu-id="08383-165">What's new or changed in Dynamics 365 Human Resource</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="08383-166">Tarkvara elutsükli poliitika</span><span class="sxs-lookup"><span data-stu-id="08383-166">Software lifecycle policy</span></span>](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]