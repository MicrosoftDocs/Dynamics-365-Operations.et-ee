---
title: Organisatsiooni hierarhia teenusesDataverse
description: Siin peatükis kirjeldatakse organisatsiooni andmete integratsiooni Finance and Operationsi rakenduste ja teenuse Dataverse vahel.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: e2b652f11db62eb58ffc2ec2fc4322149e7d45d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680068"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="9c699-103">Organisatsiooni hierarhia teenusesDataverse</span><span class="sxs-lookup"><span data-stu-id="9c699-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9c699-104">Kuna Dynamics 365 Finance on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="9c699-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="9c699-105">Ettevõtte rahandusasju saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.</span><span class="sxs-lookup"><span data-stu-id="9c699-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="9c699-106">Kuigi teenuses Dataverse ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu.</span><span class="sxs-lookup"><span data-stu-id="9c699-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="9c699-107">Dataverse’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c699-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="9c699-108">Andmevoog</span><span class="sxs-lookup"><span data-stu-id="9c699-108">Data flow</span></span>

<span data-ttu-id="9c699-109">Ettevõtte ökosüsteemil, mis koosneb Finance and Operationsi rakendustest ja Dataverse’ist, on jätkuvalt organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="9c699-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="9c699-110">See organisatsiooni hierarhia on loodud Finance and Operationsi rakendustes, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Dataverse’is.</span><span class="sxs-lookup"><span data-stu-id="9c699-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="9c699-111">Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Dataverse’i ühesuunalise andmevoona Finance and Operationsi rakendustest teenusesse Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c699-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Ülesehituse tõmmis](media/dual-write-data-flow.png)

<span data-ttu-id="9c699-113">Organisatsiooni hierarhia tabeli kaardid on saadaval andmete ühesuunalisel sünkroonimiselt Finance and Operationsi rakendustest teenusesse Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9c699-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="9c699-114">Mallid</span><span class="sxs-lookup"><span data-stu-id="9c699-114">Templates</span></span>

<span data-ttu-id="9c699-115">Toote teave sisaldab kogu teavet, mis on seotud tootega ja selle määratlusega, nagu tootedimensioonid või jälgimis- ja laoala dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="9c699-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="9c699-116">Nagu järgmine tabel näitab, luuakse tabeli kaartide kogum, et sünkroonida tooteid ja seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="9c699-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="9c699-117">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="9c699-117">Finance and Operations apps</span></span> | <span data-ttu-id="9c699-118">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="9c699-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="9c699-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="9c699-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="9c699-120">Organisatsiooni hierarhia eesmärgid</span><span class="sxs-lookup"><span data-stu-id="9c699-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="9c699-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="9c699-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="9c699-122">See mall tagab organisatsiooni hierarhia eesmärgi üksuse ühesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="9c699-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="9c699-123">Organisatsiooni hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="9c699-123">Organization hierarchy type</span></span> | <span data-ttu-id="9c699-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="9c699-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="9c699-125">See mall tagab organisatsiooni hierarhia tüübi üksuse ühesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="9c699-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="9c699-126">Organisatsiooni hierarhia – avaldatud</span><span class="sxs-lookup"><span data-stu-id="9c699-126">Organization hierarchy - published</span></span> | <span data-ttu-id="9c699-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="9c699-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="9c699-128">See mall tagab avaldatud organisatsiooni hierarhia üksuse ühesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="9c699-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="9c699-129">Tootmisüksus</span><span class="sxs-lookup"><span data-stu-id="9c699-129">Operating unit</span></span> | <span data-ttu-id="9c699-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="9c699-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="9c699-131">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="9c699-131">Legal entities</span></span> | <span data-ttu-id="9c699-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="9c699-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="9c699-133">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="9c699-133">Legal entities</span></span> | <span data-ttu-id="9c699-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="9c699-134">cdm_companies</span></span> | <span data-ttu-id="9c699-135">Tagab juriidilise isiku (ettevõtte) teabe kahesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="9c699-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="9c699-136">Sisemine korraldus</span><span class="sxs-lookup"><span data-stu-id="9c699-136">Internal Organization</span></span>

<span data-ttu-id="9c699-137">Sisemine organisatsiooniteave Dataverse’is pärineb kahest tabelist: **tootmisüksus** ja **juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="9c699-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
