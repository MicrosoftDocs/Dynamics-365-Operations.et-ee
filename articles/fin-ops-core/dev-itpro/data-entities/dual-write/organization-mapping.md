---
title: Organisatsiooni hierarhia teenusesCommon Data Service
description: Siin peatükis kirjeldatakse organisatsiooni andmete integratsiooni Finance and Operationsi rakenduste ja teenuse Common Data Service vahel.
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
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019738"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="a317d-103">Organisatsiooni hierarhia teenusesCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="a317d-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="a317d-104">Kuna Dynamics 365 Finance on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="a317d-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="a317d-105">Ettevõtte rahandusasju saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.</span><span class="sxs-lookup"><span data-stu-id="a317d-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="a317d-106">Kuigi teenuses Common Data Service ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu.</span><span class="sxs-lookup"><span data-stu-id="a317d-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="a317d-107">Common Data Service’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a317d-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="a317d-108">Andmevoog</span><span class="sxs-lookup"><span data-stu-id="a317d-108">Data flow</span></span>

<span data-ttu-id="a317d-109">Ettevõtte ökosüsteemil, mis koosneb Finance and Operationsi rakendustest ja Common Data Service’ist, on jätkuvalt organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="a317d-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="a317d-110">See organisatsiooni hierarhia on loodud Finance and Operationsi rakendustes, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Common Data Service’is.</span><span class="sxs-lookup"><span data-stu-id="a317d-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="a317d-111">Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Common Data Service’i ühesuunalise andmevoona Finance and Operationsi rakendustest teenusesse Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a317d-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Ülesehituse tõmmis](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="a317d-113">Mallid</span><span class="sxs-lookup"><span data-stu-id="a317d-113">Templates</span></span>

<span data-ttu-id="a317d-114">Organisatsiooni hierarhia olemi kaardid on saadaval andmete ühesuunalisel sünkroonimiselt Finance and Operationsi rakendustest teenusesse Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="a317d-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="a317d-115">Mallid</span><span class="sxs-lookup"><span data-stu-id="a317d-115">Templates</span></span>

<span data-ttu-id="a317d-116">Toote teave sisaldab kogu teavet, mis on seotud tootega ja selle määratlusega, nagu tootedimensioonid või jälgimis- ja laoala dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="a317d-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="a317d-117">Nagu järgmine tabel näitab, luuakse olemikaartide kogum, et sünkroonida tooteid ja seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="a317d-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="a317d-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a317d-118">Finance and Operations</span></span> | <span data-ttu-id="a317d-119">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="a317d-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="a317d-120">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a317d-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="a317d-121">Organisatsiooni hierarhia eesmärgid</span><span class="sxs-lookup"><span data-stu-id="a317d-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="a317d-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="a317d-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="a317d-123">See mall tagab organisatsiooni hierarhia eesmärgi üksuse ühesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="a317d-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="a317d-124">Organisatsiooni hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="a317d-124">Organization hierarchy type</span></span> | <span data-ttu-id="a317d-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="a317d-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="a317d-126">See mall tagab organisatsiooni hierarhia tüübi üksuse ühesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="a317d-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="a317d-127">Organisatsiooni hierarhia – avaldatud</span><span class="sxs-lookup"><span data-stu-id="a317d-127">Organization hierarchy - published</span></span> | <span data-ttu-id="a317d-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="a317d-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="a317d-129">See mall tagab avaldatud organisatsiooni hierarhia üksuse ühesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="a317d-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="a317d-130">Tootmisüksus</span><span class="sxs-lookup"><span data-stu-id="a317d-130">Operating unit</span></span> | <span data-ttu-id="a317d-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="a317d-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="a317d-132">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="a317d-132">Legal entities</span></span> | <span data-ttu-id="a317d-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="a317d-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="a317d-134">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="a317d-134">Legal entities</span></span> | <span data-ttu-id="a317d-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="a317d-135">cdm_companies</span></span> | <span data-ttu-id="a317d-136">Tagab juriidilise isiku (ettevõtte) teabe kahesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="a317d-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="a317d-137">Sisemine korraldus</span><span class="sxs-lookup"><span data-stu-id="a317d-137">Internal Organization</span></span>

<span data-ttu-id="a317d-138">Sisemine organisatsiooniteave Common Data Service’is pärineb kahest üksusest: **tootmisüksus** ja **juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="a317d-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

