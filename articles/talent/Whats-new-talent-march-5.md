---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (5. märts 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 855eafaca88d180997cf5a68c7f0fe975c177f88
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898915"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a><span data-ttu-id="2c071-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent (5. märts 2019)</span><span class="sxs-lookup"><span data-stu-id="2c071-103">What's new or changed in Dynamics 365 Talent (March 5, 2019)</span></span>

<span data-ttu-id="2c071-104">Selles teemas kirjeldatakse Talenti uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="2c071-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="2c071-105">Muutused Attractis</span><span class="sxs-lookup"><span data-stu-id="2c071-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="2c071-106">Suvandikomplektide laiendamine Attractis</span><span class="sxs-lookup"><span data-stu-id="2c071-106">Extending option sets in Attract</span></span>

<span data-ttu-id="2c071-107">Attractis on mitu välja, mis on teenuse Common Data Service suvandikomplektid.</span><span class="sxs-lookup"><span data-stu-id="2c071-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="2c071-108">Suvandikomplektide laiendamiseks on kasutusele võetud uusi võimalusi, alustades väljadega **Tagasilükkamise põhjus**, **Töösuhte tüüp** ja **Staaži tüüp**.</span><span class="sxs-lookup"><span data-stu-id="2c071-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2c071-109">Funktsioon Töö sisestamine LinkedIni nõuab lehel **Töö üksikasjad** väljade **Töösuhte tüüp** ja **Staaži tüüp** kasutamist.</span><span class="sxs-lookup"><span data-stu-id="2c071-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="2c071-110">LinkedIn toetab nende väljade vaikeväärtuseid ja need kuvatakse pärast töö sisestamist.</span><span class="sxs-lookup"><span data-stu-id="2c071-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="2c071-111">Kui sisestate töid LinkedIni ja muudate nende väljade olemasolevaid suvandikomplekti väärtusi, töö siiski sisestatakse, kuid LinkedIn ei kuva väljade **Töösuhte tüüp** ja **Staaži tüüp** kohandatud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="2c071-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="2c071-112">Muutused kasutuselevõtus</span><span class="sxs-lookup"><span data-stu-id="2c071-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="2c071-113">Kasutuselevõtu meeskondade privaatne eelvaade</span><span class="sxs-lookup"><span data-stu-id="2c071-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="2c071-114">Nüüd saate malle kogu oma ettevõtte ulatuses hõlpsasti ühiskasutusse anda ja nendega koostööd teha.</span><span class="sxs-lookup"><span data-stu-id="2c071-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="2c071-115">Lisateabe saamiseks vt jaotist [Kasutuselevõtu meeskondade abil parimate tavade ühiskasutusse andmine kogu ettevõtte ulatuses](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span><span class="sxs-lookup"><span data-stu-id="2c071-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="2c071-116">Täitjate kohatäidete privaatne eelvaade</span><span class="sxs-lookup"><span data-stu-id="2c071-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="2c071-117">Saate oma malle rikastada, kui määrate tegevusi isikute asemel rollidele.</span><span class="sxs-lookup"><span data-stu-id="2c071-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="2c071-118">Seejärel määratakse rollid juhendi loomisel isikutele.</span><span class="sxs-lookup"><span data-stu-id="2c071-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="2c071-119">Lisateabe saamiseks vt jaotist [Juhendi haldamise rollitegevuste määramise abil sujuvamaks muutmine](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span><span class="sxs-lookup"><span data-stu-id="2c071-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="2c071-120">Core HR-i muudatused</span><span class="sxs-lookup"><span data-stu-id="2c071-120">Changes in Core HR</span></span>
<span data-ttu-id="2c071-121">**Järk 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="2c071-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="2c071-122">Konfigureerige töövoog automaatselt kinnitama või jälgima töövoogu, kui inimressursside või rea haldur esitab või värskendab puhkusetaotlusi</span><span class="sxs-lookup"><span data-stu-id="2c071-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="2c071-123">Lisatud on uued töövoo tingimused, mis võimaldavad puhkusetaotluste automaatset kinnitamist juhul, kui need esitab töövõtja haldur või personalihaldur.</span><span class="sxs-lookup"><span data-stu-id="2c071-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="2c071-124">Üks võimalus töövoo automaatse kinnitamise saavutamiseks on lubada töövoo kinnitamisel automaatne tegevus.</span><span class="sxs-lookup"><span data-stu-id="2c071-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="2c071-125">Lisatud tingimused sisaldavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="2c071-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="2c071-126">Edastaja – kasutatakse selle kasutaja, kes taotluse töövoogu esitas, süsteemikasutaja ID hindamiseks.</span><span class="sxs-lookup"><span data-stu-id="2c071-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="2c071-127">Kelle nimel edastatud – kasutatakse hindamaks, kas puhkusetaotlus esitati taotlusega seostatud töötaja nimel.</span><span class="sxs-lookup"><span data-stu-id="2c071-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="2c071-128">Inimressursside edastatud – kasutatakse hindamaks, kas taotluse töövoogu esitanud süsteemikasutaja omab inimressursside rolli.</span><span class="sxs-lookup"><span data-stu-id="2c071-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="2c071-129">Halduri edastatud – kasutatakse hindamaks, kas puhkusetaotluse töövoogu esitanud kasutaja on taotlusega seotud töötaja reahierarhia haldur.</span><span class="sxs-lookup"><span data-stu-id="2c071-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="2c071-130">Töövõtja põhipalga lubamine tulevaste ametikoha määrangute jaoks</span><span class="sxs-lookup"><span data-stu-id="2c071-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="2c071-131">Tavaliselt liituvad töövõtjad ettevõttega tulevikus oleva alguskuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="2c071-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="2c071-132">See muudatus võimaldab määrata põhipalka tulevaste ametikoha määramistega töövõtjatele.</span><span class="sxs-lookup"><span data-stu-id="2c071-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="2c071-133">Ametikoha palgaarvestuse väljad on ametikoha redigeerimisel tühjad</span><span class="sxs-lookup"><span data-stu-id="2c071-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="2c071-134">Selle muudatuse tõttu määratakse olemasolevate ametikohtade muudatuste taotlemisel palgaarvestuse väljade vaikeväärtusteks praegused väärtused.</span><span class="sxs-lookup"><span data-stu-id="2c071-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="2c071-135">Muud mitmesugused veaparandused</span><span class="sxs-lookup"><span data-stu-id="2c071-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="2c071-136">See versioon sisaldab ka muid väikesi veaparandusi.</span><span class="sxs-lookup"><span data-stu-id="2c071-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="2c071-137">Common Data Service'i värskendus</span><span class="sxs-lookup"><span data-stu-id="2c071-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="2c071-138">Tähtajad Common Data Service'i värskendamiseks lähenevad kiiresti.</span><span class="sxs-lookup"><span data-stu-id="2c071-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="2c071-139">Logige sisse Power Appsi halduskeskusesse, et teha kindlaks, kas teie andmebaas vajab värskendamist.</span><span class="sxs-lookup"><span data-stu-id="2c071-139">Sign in to the Power Apps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="2c071-140">Lisateavet tähtaegade ja täiendamiseks nõutavate etappide kohta vt jaotisest [Täiendamine teenusele Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span><span class="sxs-lookup"><span data-stu-id="2c071-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="2c071-141">Peagi tulekul</span><span class="sxs-lookup"><span data-stu-id="2c071-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="2c071-142">Täpsem hüvitusturve (fikseeritud ja muutuv)</span><span class="sxs-lookup"><span data-stu-id="2c071-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="2c071-143">Paljudes ettevõtetes pääsevad hüvitise ja eeliste haldurid juurde ainult teatud hüvituskirjetele, nagu juhtkonna või piirkonnapõhiste töövõtjate kirjed.</span><span class="sxs-lookup"><span data-stu-id="2c071-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="2c071-144">Selle muudatusega saate ettevõttesiseselt hüvitusplaane hallata ja säilitada erinevate töövõtjate populatsioonide jaoks.</span><span class="sxs-lookup"><span data-stu-id="2c071-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="2c071-145">Fikseeritud ja muutuvatele plaanidele saab määrata turberolle, mis määravad plaanide juurdepääsu ja plaanidega seotud töövõtja andmed, näiteks palga või lisakulumikirjed.</span><span class="sxs-lookup"><span data-stu-id="2c071-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="2c071-146">Nende töövõtjate hüvitisi saavad töödelda ainult rollid, millele on antud juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="2c071-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24-for-finance-and-operations"></a><span data-ttu-id="2c071-147">Finance and Operationsi 24. platvormi värskendus</span><span class="sxs-lookup"><span data-stu-id="2c071-147">Platform update 24 for Finance and Operations</span></span>
<span data-ttu-id="2c071-148">Lisateavet Finance and Operationsi platvormivärskenduse 24 kohta vt jaotisest [Mis on rakenduse Finance and Operations platvormivärskenduses 24 uut või mida on muudetud (märts 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span><span class="sxs-lookup"><span data-stu-id="2c071-148">For additional details about Platform update 24 for Finance and Operations, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
