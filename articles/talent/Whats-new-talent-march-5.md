---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (5. märts 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e6b490a696dc0a00c47e56f57373f330d0e53dde
ms.sourcegitcommit: 479b8cda7e411830bf1f579fab3692c980dcf850
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/08/2019
ms.locfileid: "782845"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-5-2019"></a><span data-ttu-id="dcab7-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 for Talent (5. märts 2019)</span><span class="sxs-lookup"><span data-stu-id="dcab7-103">What's new or changed in Dynamics 365 for Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dcab7-104">Selles teemas kirjeldatakse Talenti uusi või muutunud funktsioone</span><span class="sxs-lookup"><span data-stu-id="dcab7-104">This topic describes features that are either new or changed in Talent</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="dcab7-105">Muutused Attractis</span><span class="sxs-lookup"><span data-stu-id="dcab7-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="dcab7-106">Suvandikomplektide laiendamine Attractis</span><span class="sxs-lookup"><span data-stu-id="dcab7-106">Extending option sets in Attract</span></span>

<span data-ttu-id="dcab7-107">Attractis on mitu välja, mis on teenuse Common Data Service (CDS) suvandikomplektid.</span><span class="sxs-lookup"><span data-stu-id="dcab7-107">In Attract, there are multiple fields that are option sets within the Common Data Service (CDS).</span></span> <span data-ttu-id="dcab7-108">Suvandikomplektide laiendamiseks on kasutusele võetud uusi võimalusi, alustades väljadega **Tagasilükkamise põhjus**, **Töösuhte tüüp** ja **Staaži tüüp**.</span><span class="sxs-lookup"><span data-stu-id="dcab7-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcab7-109">Funktsioon Töö sisestamine LinkedIni nõuab lehel **Töö üksikasjad** väljade **Töösuhte tüüp** ja **Staaži tüüp** kasutamist.</span><span class="sxs-lookup"><span data-stu-id="dcab7-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="dcab7-110">LinkedIn toetab nende väljade vaikeväärtuseid ja need kuvatakse pärast töö sisestamist.</span><span class="sxs-lookup"><span data-stu-id="dcab7-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="dcab7-111">Kui sisestate töid LinkedIni ja muudate nende väljade olemasolevaid suvandikomplekti väärtusi, töö siiski sisestatakse, kuid LinkedIn ei kuva väljade **Töösuhte tüüp** ja **Staaži tüüp** kohandatud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="dcab7-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="dcab7-112">Muutused kasutuselevõtus</span><span class="sxs-lookup"><span data-stu-id="dcab7-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="dcab7-113">Kasutuselevõtu meeskondade privaatne eelvaade</span><span class="sxs-lookup"><span data-stu-id="dcab7-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="dcab7-114">Nüüd saate malle kogu oma ettevõtte ulatuses hõlpsasti ühiskasutusse anda ja nendega koostööd teha.</span><span class="sxs-lookup"><span data-stu-id="dcab7-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="dcab7-115">Lisateabe saamiseks vt jaotist [Kasutuselevõtu meeskondade abil parimate tavade ühiskasutusse andmine kogu ettevõtte ulatuses](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="dcab7-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="dcab7-116">Täitjate kohatäidete privaatne eelvaade</span><span class="sxs-lookup"><span data-stu-id="dcab7-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="dcab7-117">Saate oma malle rikastada, kui määrate tegevusi isikute asemel rollidele.</span><span class="sxs-lookup"><span data-stu-id="dcab7-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="dcab7-118">Seejärel määratakse rollid juhendi loomisel isikutele.</span><span class="sxs-lookup"><span data-stu-id="dcab7-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="dcab7-119">Lisateabe saamiseks vt jaotist [Juhendi haldamise rollitegevuste määramise abil sujuvamaks muutmine](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="dcab7-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="dcab7-120">Core HR-i muudatused</span><span class="sxs-lookup"><span data-stu-id="dcab7-120">Changes in Core HR</span></span>
<span data-ttu-id="dcab7-121">**Järk 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="dcab7-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="dcab7-122">Konfigureerige töövoog automaatselt kinnitama või jälgima töövoogu, kui inimressursside või rea haldur esitab või värskendab puhkusetaotlusi</span><span class="sxs-lookup"><span data-stu-id="dcab7-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="dcab7-123">Lisatud on uued töövoo tingimused, mis võimaldavad puhkusetaotluste automaatset kinnitamist juhul, kui need esitab töövõtja haldur või personalihaldur.</span><span class="sxs-lookup"><span data-stu-id="dcab7-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="dcab7-124">Üks võimalus töövoo automaatse kinnitamise saavutamiseks on lubada töövoo kinnitamisel automaatne tegevus.</span><span class="sxs-lookup"><span data-stu-id="dcab7-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="dcab7-125">Lisatud tingimused sisaldavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="dcab7-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="dcab7-126">Edastaja – kasutatakse selle kasutaja, kes taotluse töövoogu esitas, süsteemikasutaja ID hindamiseks.</span><span class="sxs-lookup"><span data-stu-id="dcab7-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="dcab7-127">Kelle nimel edastatud – kasutatakse hindamaks, kas puhkusetaotlus esitati taotlusega seostatud töötaja nimel.</span><span class="sxs-lookup"><span data-stu-id="dcab7-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="dcab7-128">Inimressursside edastatud – kasutatakse hindamaks, kas taotluse töövoogu esitanud süsteemikasutaja omab inimressursside rolli.</span><span class="sxs-lookup"><span data-stu-id="dcab7-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="dcab7-129">Halduri edastatud – kasutatakse hindamaks, kas puhkusetaotluse töövoogu esitanud kasutaja on taotlusega seotud töötaja reahierarhia haldur.</span><span class="sxs-lookup"><span data-stu-id="dcab7-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="dcab7-130">Töövõtja põhipalga lubamine tulevaste ametikoha määrangute jaoks</span><span class="sxs-lookup"><span data-stu-id="dcab7-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="dcab7-131">Tavaliselt liituvad töövõtjad ettevõttega tulevikus oleva alguskuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="dcab7-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="dcab7-132">See muudatus võimaldab määrata põhipalka tulevaste ametikoha määramistega töövõtjatele.</span><span class="sxs-lookup"><span data-stu-id="dcab7-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="dcab7-133">Ametikoha palgaarvestuse väljad on ametikoha redigeerimisel tühjad</span><span class="sxs-lookup"><span data-stu-id="dcab7-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="dcab7-134">Selle muudatuse tõttu määratakse olemasolevate ametikohtade muudatuste taotlemisel palgaarvestuse väljade vaikeväärtusteks praegused väärtused.</span><span class="sxs-lookup"><span data-stu-id="dcab7-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="dcab7-135">Muud mitmesugused veaparandused</span><span class="sxs-lookup"><span data-stu-id="dcab7-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="dcab7-136">See versioon sisaldab ka muid väikesi veaparandusi.</span><span class="sxs-lookup"><span data-stu-id="dcab7-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-cds-for-apps"></a><span data-ttu-id="dcab7-137">Täiendamine teenusele CDS for Apps</span><span class="sxs-lookup"><span data-stu-id="dcab7-137">Upgrade to CDS for Apps</span></span>
<span data-ttu-id="dcab7-138">Teenusele CDS for Apps täiendamise tähtajad lähenevad kiirelt.</span><span class="sxs-lookup"><span data-stu-id="dcab7-138">Deadlines to upgrade to CDS for Apps are quickly approaching.</span></span> <span data-ttu-id="dcab7-139">Logige sisse PowerAppsi halduskeskusesse, et määrata, kas teie andmebaas vajab täiendamist.</span><span class="sxs-lookup"><span data-stu-id="dcab7-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="dcab7-140">Lisateavet tähtaegade ja täiendamiseks nõutavate etappide kohta vt jaotisest [Täiendamine teenusele Common Data Service for Apps](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="dcab7-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service for Apps](https://docs.microsoft.com/en-us/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="dcab7-141">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="dcab7-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="dcab7-142">Täpsem hüvitusturve (fikseeritud ja muutuv)</span><span class="sxs-lookup"><span data-stu-id="dcab7-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="dcab7-143">Paljudes ettevõtetes pääsevad hüvitise ja eeliste haldurid juurde ainult teatud hüvituskirjetele, nagu juhtkonna või piirkonnapõhiste töövõtjate kirjed.</span><span class="sxs-lookup"><span data-stu-id="dcab7-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="dcab7-144">Selle muudatusega saate ettevõttesiseselt hüvitusplaane hallata ja säilitada erinevate töövõtjate populatsioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="dcab7-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="dcab7-145">Fikseeritud ja muutuvatele plaanidele saab määrata turberolle, mis määravad plaanide juurdepääsu ja plaanidega seotud töövõtja andmed, näiteks palga või lisakulumikirjed.</span><span class="sxs-lookup"><span data-stu-id="dcab7-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="dcab7-146">Nende töövõtjate hüvitisi saavad töödelda ainult rollid, millele on antud juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="dcab7-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24"></a><span data-ttu-id="dcab7-147">Platvormivärskendus update 24</span><span class="sxs-lookup"><span data-stu-id="dcab7-147">Platform update 24</span></span>
<span data-ttu-id="dcab7-148">Lisateavet platvormivärskenduse 24 kohta vt jaotisest [Mis on rakenduse Finance and Operations platvormivärskenduses 24 uut või mida on muudetud (märts 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="dcab7-148">For additional details about Platform update 24, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
