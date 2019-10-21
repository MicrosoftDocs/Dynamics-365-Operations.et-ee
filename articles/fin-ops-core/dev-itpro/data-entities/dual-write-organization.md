---
title: Organisatsiooni hierarhia teenusesCommon Data Service
description: Selles teemas kirjeldatakse organisatsiooniliste andmete integreerimist Finance and Operationsi rakenduste ja teenuse Common Data Service vahel.
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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182021"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="182e1-103">Organisatsiooni hierarhia teenusesCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="182e1-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="182e1-104">Kuna Dynamics 365 Finance on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="182e1-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="182e1-105">Ettevõtte rahandusasju saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.</span><span class="sxs-lookup"><span data-stu-id="182e1-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="182e1-106">Kuigi teenuses Common Data Service ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu.</span><span class="sxs-lookup"><span data-stu-id="182e1-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="182e1-107">Common Data Service’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="182e1-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="182e1-108">Andmevoog</span><span class="sxs-lookup"><span data-stu-id="182e1-108">Data flow</span></span>

<span data-ttu-id="182e1-109">Ettevõtte ökosüsteemil, mis koosneb Finance and Operationsi rakendustest ja Common Data Service’ist, on jätkuvalt organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="182e1-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="182e1-110">See organisatsiooni hierarhia on loodud Finance and Operationsi rakendustes, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Common Data Service’is.</span><span class="sxs-lookup"><span data-stu-id="182e1-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="182e1-111">Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Common Data Service’i ühesuunaline andmevoona Finance and Operationsi rakendustest teenusesse Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="182e1-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Ülesehituse tõmmis](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="182e1-113">Mallid</span><span class="sxs-lookup"><span data-stu-id="182e1-113">Templates</span></span>

<span data-ttu-id="182e1-114">Organisatsiooni hierarhia olemi kaardid on saadaval andmete ühesuunalisel sünkroonimiselt Finance and Operationsi rakendustest teenusesse Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="182e1-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="182e1-115">Organisatsiooni hierarhia eesmärkide haldamine</span><span class="sxs-lookup"><span data-stu-id="182e1-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="182e1-116">See mall pakub organisatsiooni hierarhia eesmärgi olemi ühesuunalise sünkroonimist Finance and Operationsist teistesse Dynamics 365 rakendustesse.</span><span class="sxs-lookup"><span data-stu-id="182e1-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="182e1-117">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="182e1-117">Source field</span></span> | <span data-ttu-id="182e1-118">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-118">Map type</span></span> | <span data-ttu-id="182e1-119">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="182e1-119">Destination field</span></span>
---|---|---
<span data-ttu-id="182e1-120">Hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="182e1-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="182e1-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="182e1-122">Hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="182e1-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="182e1-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="182e1-124">Hierarhia eesmärk</span><span class="sxs-lookup"><span data-stu-id="182e1-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="182e1-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="182e1-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="182e1-126">Muudetamatu</span><span class="sxs-lookup"><span data-stu-id="182e1-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="182e1-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="182e1-127">msdyn\_immutable</span></span>
<span data-ttu-id="182e1-128">Sea vaikeväärtused</span><span class="sxs-lookup"><span data-stu-id="182e1-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="182e1-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="182e1-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="182e1-130">Organisatsiooni hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="182e1-131">See mall pakub organisatsiooni hierarhia tüübii olemi ühesuunalise sünkroonimist Finance and Operationsist teistesse Dynamics 365 rakendustesse.</span><span class="sxs-lookup"><span data-stu-id="182e1-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="182e1-132">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="182e1-132">Source field</span></span> | <span data-ttu-id="182e1-133">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-133">Map type</span></span> | <span data-ttu-id="182e1-134">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="182e1-134">Destination field</span></span>
---|---|---
<span data-ttu-id="182e1-135">NIMI</span><span class="sxs-lookup"><span data-stu-id="182e1-135">NAME</span></span> | \> | <span data-ttu-id="182e1-136">msdyn\_nimi</span><span class="sxs-lookup"><span data-stu-id="182e1-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="182e1-137">Organisatsiooni hierarhia</span><span class="sxs-lookup"><span data-stu-id="182e1-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="182e1-138">See mall pakub organisatsiooni hierarhia avaldatud olemi ühesuunalist sünkroonimist Finance and Operationsist teistesse Dynamics 365 rakendustesse.</span><span class="sxs-lookup"><span data-stu-id="182e1-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="182e1-139">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="182e1-139">Source field</span></span> | <span data-ttu-id="182e1-140">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-140">Map type</span></span> | <span data-ttu-id="182e1-141">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="182e1-141">Destination field</span></span>
---|---|---
<span data-ttu-id="182e1-142">Kehtib</span><span class="sxs-lookup"><span data-stu-id="182e1-142">VALIDTO</span></span> | \> | <span data-ttu-id="182e1-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="182e1-143">msdyn\_validto</span></span>
<span data-ttu-id="182e1-144">Kehtivuse algus</span><span class="sxs-lookup"><span data-stu-id="182e1-144">VALIDFROM</span></span> | \> | <span data-ttu-id="182e1-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="182e1-145">msdyn\_validfrom</span></span>
<span data-ttu-id="182e1-146">Hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="182e1-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="182e1-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="182e1-148">Peaorganisatsiooni partii number</span><span class="sxs-lookup"><span data-stu-id="182e1-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="182e1-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="182e1-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="182e1-150">Alamorganisatsiooni partii number</span><span class="sxs-lookup"><span data-stu-id="182e1-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="182e1-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="182e1-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="182e1-152">Hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="182e1-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="182e1-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="182e1-154">Alamorganisatsiooni partii number</span><span class="sxs-lookup"><span data-stu-id="182e1-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="182e1-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="182e1-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="182e1-156">Peaorganisatsiooni partii number</span><span class="sxs-lookup"><span data-stu-id="182e1-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="182e1-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="182e1-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="182e1-158">Sisemine korraldus</span><span class="sxs-lookup"><span data-stu-id="182e1-158">Internal Organization</span></span>

<span data-ttu-id="182e1-159">Sisemine organisatsiooniteave Common Data Service’is pärineb kahest üksusest: **tootmisüksus** ja **juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="182e1-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="182e1-160">Tootmisüksus</span><span class="sxs-lookup"><span data-stu-id="182e1-160">Operating unit</span></span>

<span data-ttu-id="182e1-161">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="182e1-161">Source field</span></span> | <span data-ttu-id="182e1-162">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-162">Map type</span></span> | <span data-ttu-id="182e1-163">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="182e1-163">Destination field</span></span>
---|---|---
<span data-ttu-id="182e1-164">keel</span><span class="sxs-lookup"><span data-stu-id="182e1-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="182e1-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="182e1-165">msdyn\_languageid</span></span>
<span data-ttu-id="182e1-166">Nime pseudonüüm</span><span class="sxs-lookup"><span data-stu-id="182e1-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="182e1-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="182e1-167">msdyn\_namealias</span></span>
<span data-ttu-id="182e1-168">NIMI</span><span class="sxs-lookup"><span data-stu-id="182e1-168">NAME</span></span> | \> | <span data-ttu-id="182e1-169">msdyn\_nimi</span><span class="sxs-lookup"><span data-stu-id="182e1-169">msdyn\_name</span></span>
<span data-ttu-id="182e1-170">Osapoole number</span><span class="sxs-lookup"><span data-stu-id="182e1-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="182e1-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="182e1-171">msdyn\_partynumber</span></span>
<span data-ttu-id="182e1-172">Tootmisüksuse tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="182e1-173">msdyn\_tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="182e1-174">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="182e1-174">Legal entity</span></span>

<span data-ttu-id="182e1-175">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="182e1-175">Source field</span></span> | <span data-ttu-id="182e1-176">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-176">Map type</span></span> | <span data-ttu-id="182e1-177">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="182e1-177">Destination field</span></span>
---|---|---
<span data-ttu-id="182e1-178">Nime pseudonüüm</span><span class="sxs-lookup"><span data-stu-id="182e1-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="182e1-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="182e1-179">msdyn\_namealias</span></span>
<span data-ttu-id="182e1-180">keel</span><span class="sxs-lookup"><span data-stu-id="182e1-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="182e1-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="182e1-181">msdyn\_languageid</span></span>
<span data-ttu-id="182e1-182">NIMI</span><span class="sxs-lookup"><span data-stu-id="182e1-182">NAME</span></span> | \> | <span data-ttu-id="182e1-183">msdyn\_nimi</span><span class="sxs-lookup"><span data-stu-id="182e1-183">msdyn\_name</span></span>
<span data-ttu-id="182e1-184">Osapoole number</span><span class="sxs-lookup"><span data-stu-id="182e1-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="182e1-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="182e1-185">msdyn\_partynumber</span></span>
<span data-ttu-id="182e1-186">Pole</span><span class="sxs-lookup"><span data-stu-id="182e1-186">none</span></span> | \>\> | <span data-ttu-id="182e1-187">msdyn\_tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-187">msdyn\_type</span></span>
<span data-ttu-id="182e1-188">Juriidilise isiku ID</span><span class="sxs-lookup"><span data-stu-id="182e1-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="182e1-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="182e1-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="182e1-190">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="182e1-190">Company</span></span>

<span data-ttu-id="182e1-191">Pakub juriidilise isiku (ettevõtte) teabe kahesuunalist sünkroonimist Finance and Operationsi ja teiste Dynamics 365 rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="182e1-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="182e1-192">Lähteväli</span><span class="sxs-lookup"><span data-stu-id="182e1-192">Source field</span></span> | <span data-ttu-id="182e1-193">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="182e1-193">Map type</span></span> | <span data-ttu-id="182e1-194">Sihtväli</span><span class="sxs-lookup"><span data-stu-id="182e1-194">Destination field</span></span>
---|---|---
<span data-ttu-id="182e1-195">NIMI</span><span class="sxs-lookup"><span data-stu-id="182e1-195">NAME</span></span> | = | <span data-ttu-id="182e1-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="182e1-196">cdm\_name</span></span>
<span data-ttu-id="182e1-197">Juriidilise isiku ID</span><span class="sxs-lookup"><span data-stu-id="182e1-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="182e1-198">CDM\_companycode</span><span class="sxs-lookup"><span data-stu-id="182e1-198">cdm\_companycode</span></span>
