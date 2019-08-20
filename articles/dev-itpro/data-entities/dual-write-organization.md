---
title: Organisatsiooni hierarhia teenusesCommon Data Service
description: Selles teemas kirjeldatakse organisatsiooniliste andmete integreerimist Finance and Operationsi ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789178"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="da197-103">Organisatsiooni hierarhia teenusesCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="da197-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="da197-104">Kuna Microsoft Dynamics 365 for Finance and Operations on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="da197-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="da197-105">Ettevõtte rahandusasju ja operatsioone saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.</span><span class="sxs-lookup"><span data-stu-id="da197-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="da197-106">Kuigi teenuses Common Data Service ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu.</span><span class="sxs-lookup"><span data-stu-id="da197-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="da197-107">Common Data Service’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="da197-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="da197-108">Andmevoog</span><span class="sxs-lookup"><span data-stu-id="da197-108">Data flow</span></span>

<span data-ttu-id="da197-109">Ettevõtte ökosüsteemil, mis koosneb Finance and Operationsist ja Common Data Service’ist, on jätkuvalt organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="da197-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="da197-110">See organisatsiooni hierarhia on loodud Finance and Operationsis, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Common Data Service’is.</span><span class="sxs-lookup"><span data-stu-id="da197-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="da197-111">Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Common Data Service’i ühesuunaline andmevoona Finance and Operationsist teenusesse Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="da197-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Ülesehituse tõmmis](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="da197-113">Mallid</span><span class="sxs-lookup"><span data-stu-id="da197-113">Templates</span></span>

<span data-ttu-id="da197-114">Organisatsiooni hierarhia olemi kaardid on saadaval andmete ühesuunalisel sünkroonimiselt Finance and Operationsist teenusesse Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="da197-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="da197-115">Organisatsiooni hierarhia eesmärkide haldamine</span><span class="sxs-lookup"><span data-stu-id="da197-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="da197-116">See mall pakub organisatsiooni hierarhia eesmärgi olemi ühesuunalise sünkroonimist Finance and Operationsilt rakendusse Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="da197-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="da197-117">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="da197-117">Source field</span></span> | <span data-ttu-id="da197-118">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-118">Map type</span></span> | <span data-ttu-id="da197-119">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="da197-119">Destination field</span></span>
---|---|---
<span data-ttu-id="da197-120">Hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="da197-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="da197-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="da197-122">Hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="da197-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="da197-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="da197-124">Hierarhia eesmärk</span><span class="sxs-lookup"><span data-stu-id="da197-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="da197-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="da197-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="da197-126">Muudetamatu</span><span class="sxs-lookup"><span data-stu-id="da197-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="da197-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="da197-127">msdyn\_immutable</span></span>
<span data-ttu-id="da197-128">Sea vaikeväärtused</span><span class="sxs-lookup"><span data-stu-id="da197-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="da197-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="da197-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="da197-130">Organisatsiooni hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="da197-131">See mall pakub organisatsiooni hierarhia tüübi olemi ühesuunaline sünkroonimine Finance and Operations kliendi kaasamine.</span><span class="sxs-lookup"><span data-stu-id="da197-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="da197-132">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="da197-132">Source field</span></span> | <span data-ttu-id="da197-133">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-133">Map type</span></span> | <span data-ttu-id="da197-134">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="da197-134">Destination field</span></span>
---|---|---
<span data-ttu-id="da197-135">NIMI</span><span class="sxs-lookup"><span data-stu-id="da197-135">NAME</span></span> | \> | <span data-ttu-id="da197-136">msdyn\_nimi</span><span class="sxs-lookup"><span data-stu-id="da197-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="da197-137">Organisatsiooni hierarhia</span><span class="sxs-lookup"><span data-stu-id="da197-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="da197-138">See mall pakub organisatsiooni hierarhia eesmärgi olemi ühesuunaline sünkroonimine Finance and Operations kliendi kaasamine.</span><span class="sxs-lookup"><span data-stu-id="da197-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="da197-139">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="da197-139">Source field</span></span> | <span data-ttu-id="da197-140">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-140">Map type</span></span> | <span data-ttu-id="da197-141">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="da197-141">Destination field</span></span>
---|---|---
<span data-ttu-id="da197-142">Kehtib</span><span class="sxs-lookup"><span data-stu-id="da197-142">VALIDTO</span></span> | \> | <span data-ttu-id="da197-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="da197-143">msdyn\_validto</span></span>
<span data-ttu-id="da197-144">Kehtivuse algus</span><span class="sxs-lookup"><span data-stu-id="da197-144">VALIDFROM</span></span> | \> | <span data-ttu-id="da197-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="da197-145">msdyn\_validfrom</span></span>
<span data-ttu-id="da197-146">Hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="da197-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="da197-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="da197-148">Peaorganisatsiooni partii number</span><span class="sxs-lookup"><span data-stu-id="da197-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="da197-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="da197-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="da197-150">Alamorganisatsiooni partii number</span><span class="sxs-lookup"><span data-stu-id="da197-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="da197-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="da197-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="da197-152">Hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="da197-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="da197-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="da197-154">Alamorganisatsiooni partii number</span><span class="sxs-lookup"><span data-stu-id="da197-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="da197-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="da197-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="da197-156">Peaorganisatsiooni partii number</span><span class="sxs-lookup"><span data-stu-id="da197-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="da197-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="da197-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="da197-158">Sisemine korraldus</span><span class="sxs-lookup"><span data-stu-id="da197-158">Internal Organization</span></span>

<span data-ttu-id="da197-159">Sisemine organisatsiooniteave Common Data Service’is pärineb kahest Finance and Operationsi üksusest: **tootmisüksus** ja **juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="da197-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="da197-160">Tootmisüksus</span><span class="sxs-lookup"><span data-stu-id="da197-160">Operating unit</span></span>

<span data-ttu-id="da197-161">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="da197-161">Source field</span></span> | <span data-ttu-id="da197-162">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-162">Map type</span></span> | <span data-ttu-id="da197-163">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="da197-163">Destination field</span></span>
---|---|---
<span data-ttu-id="da197-164">keel</span><span class="sxs-lookup"><span data-stu-id="da197-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="da197-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="da197-165">msdyn\_languageid</span></span>
<span data-ttu-id="da197-166">Nime pseudonüüm</span><span class="sxs-lookup"><span data-stu-id="da197-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="da197-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="da197-167">msdyn\_namealias</span></span>
<span data-ttu-id="da197-168">NIMI</span><span class="sxs-lookup"><span data-stu-id="da197-168">NAME</span></span> | \> | <span data-ttu-id="da197-169">msdyn\_nimi</span><span class="sxs-lookup"><span data-stu-id="da197-169">msdyn\_name</span></span>
<span data-ttu-id="da197-170">Osapoole number</span><span class="sxs-lookup"><span data-stu-id="da197-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="da197-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="da197-171">msdyn\_partynumber</span></span>
<span data-ttu-id="da197-172">Tootmisüksuse tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="da197-173">msdyn\_tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="da197-174">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="da197-174">Legal entity</span></span>

<span data-ttu-id="da197-175">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="da197-175">Source field</span></span> | <span data-ttu-id="da197-176">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-176">Map type</span></span> | <span data-ttu-id="da197-177">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="da197-177">Destination field</span></span>
---|---|---
<span data-ttu-id="da197-178">Nime pseudonüüm</span><span class="sxs-lookup"><span data-stu-id="da197-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="da197-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="da197-179">msdyn\_namealias</span></span>
<span data-ttu-id="da197-180">keel</span><span class="sxs-lookup"><span data-stu-id="da197-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="da197-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="da197-181">msdyn\_languageid</span></span>
<span data-ttu-id="da197-182">NIMI</span><span class="sxs-lookup"><span data-stu-id="da197-182">NAME</span></span> | \> | <span data-ttu-id="da197-183">msdyn\_nimi</span><span class="sxs-lookup"><span data-stu-id="da197-183">msdyn\_name</span></span>
<span data-ttu-id="da197-184">Osapoole number</span><span class="sxs-lookup"><span data-stu-id="da197-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="da197-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="da197-185">msdyn\_partynumber</span></span>
<span data-ttu-id="da197-186">Pole</span><span class="sxs-lookup"><span data-stu-id="da197-186">none</span></span> | \>\> | <span data-ttu-id="da197-187">msdyn\_tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-187">msdyn\_type</span></span>
<span data-ttu-id="da197-188">Juriidilise isiku ID</span><span class="sxs-lookup"><span data-stu-id="da197-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="da197-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="da197-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="da197-190">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="da197-190">Company</span></span>

<span data-ttu-id="da197-191">Pakub juriidilise isiku (ettevõtte) teabe kahesuunalist sünkroonimist Finance and Operationsi ja Customer Engagementi vahel.</span><span class="sxs-lookup"><span data-stu-id="da197-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="da197-192">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="da197-192">Source field</span></span> | <span data-ttu-id="da197-193">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="da197-193">Map type</span></span> | <span data-ttu-id="da197-194">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="da197-194">Destination field</span></span>
---|---|---
<span data-ttu-id="da197-195">NIMI</span><span class="sxs-lookup"><span data-stu-id="da197-195">NAME</span></span> | = | <span data-ttu-id="da197-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="da197-196">cdm\_name</span></span>
<span data-ttu-id="da197-197">Juriidilise isiku ID</span><span class="sxs-lookup"><span data-stu-id="da197-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="da197-198">CDM\_companycode</span><span class="sxs-lookup"><span data-stu-id="da197-198">cdm\_companycode</span></span>
