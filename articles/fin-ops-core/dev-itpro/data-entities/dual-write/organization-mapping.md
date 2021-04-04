---
title: Organisatsiooni hierarhia teenusesDataverse
description: Siin peatükis kirjeldatakse organisatsiooni andmete integratsiooni Finance and Operationsi rakenduste ja teenuse Dataverse vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: f265d49a87383e2abf129b8d1d67567fc4b9e0de
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559575"
---
# <a name="organization-hierarchy-in-dataverse"></a><span data-ttu-id="64a3d-103">Organisatsiooni hierarhia teenusesDataverse</span><span class="sxs-lookup"><span data-stu-id="64a3d-103">Organization hierarchy in Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="64a3d-104">Kuna Dynamics 365 Finance on finantssüsteem, on *organisatsioon* keskne mõiste ja süsteemi seadistus algab organisatsiooni hierarhia konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="64a3d-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="64a3d-105">Ettevõtte rahandusasju saab seejärel jälgida organisatsiooni tasemel ja mis tahes tasemel organisatsiooni hierarhias.</span><span class="sxs-lookup"><span data-stu-id="64a3d-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="64a3d-106">Kuigi teenuses Dataverse ei ole organisatsiooni hierarhia mõistet, on sellel mõned lahtised kontseptsioonid, nagu müügi kogutulu.</span><span class="sxs-lookup"><span data-stu-id="64a3d-106">Although Dataverse doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="64a3d-107">Dataverse’i integratsiooni osana lisatakse organisatsiooni hierarhia andmestruktuur teenusele Dataverse.</span><span class="sxs-lookup"><span data-stu-id="64a3d-107">As part of Dataverse integration, the organization hierarchy data structure is added to Dataverse.</span></span>

## <a name="data-flow"></a><span data-ttu-id="64a3d-108">Andmevoog</span><span class="sxs-lookup"><span data-stu-id="64a3d-108">Data flow</span></span>

<span data-ttu-id="64a3d-109">Ettevõtte ökosüsteemil, mis koosneb Finance and Operationsi rakendustest ja Dataverse’ist, on jätkuvalt organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="64a3d-109">A business ecosystem that consists of Finance and Operations apps and Dataverse will continue to have an organization hierarchy.</span></span> <span data-ttu-id="64a3d-110">See organisatsiooni hierarhia on loodud Finance and Operationsi rakendustes, kuid see on informatiivsel ja laiendatavuse eesmärgil esitatud Dataverse’is.</span><span class="sxs-lookup"><span data-stu-id="64a3d-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Dataverse for informational and extensibility purposes.</span></span> <span data-ttu-id="64a3d-111">Järgmine illustratsioon näitab organisatsiooni hierarhia teavet, mis on avatud Dataverse’i ühesuunalise andmevoona Finance and Operationsi rakendustest teenusesse Dataverse.</span><span class="sxs-lookup"><span data-stu-id="64a3d-111">The following illustration shows the organization hierarchy information that is exposed in Dataverse as a one-way data flow from Finance and Operations apps to Dataverse.</span></span>

![Ülesehituse tõmmis](media/dual-write-data-flow.png)

<span data-ttu-id="64a3d-113">Organisatsiooni hierarhia tabeli kaardid on saadaval andmete ühesuunalisel sünkroonimiselt Finance and Operationsi rakendustest teenusesse Dataverse.</span><span class="sxs-lookup"><span data-stu-id="64a3d-113">Organization hierarchy table maps are available for one-way synchronization of data from Finance and Operations apps to Dataverse.</span></span>

## <a name="templates"></a><span data-ttu-id="64a3d-114">Mallid</span><span class="sxs-lookup"><span data-stu-id="64a3d-114">Templates</span></span>

<span data-ttu-id="64a3d-115">Toote teave sisaldab kogu teavet, mis on seotud tootega ja selle määratlusega, nagu tootedimensioonid või jälgimis- ja laoala dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="64a3d-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="64a3d-116">Nagu järgmine tabel näitab, luuakse tabeli kaartide kogum, et sünkroonida tooteid ja seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="64a3d-116">As the following table shows, a collection of table maps is created to sync products and related information.</span></span>

<span data-ttu-id="64a3d-117">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="64a3d-117">Finance and Operations apps</span></span> | <span data-ttu-id="64a3d-118">Muud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="64a3d-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="64a3d-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64a3d-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="64a3d-120">Organisatsiooni hierarhia eesmärgid</span><span class="sxs-lookup"><span data-stu-id="64a3d-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="64a3d-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="64a3d-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="64a3d-122">See mall tagab organisatsiooni hierarhia eesmärgi tabeli ühesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="64a3d-122">This template provides one-way synchronization of the Organization Hierarchy Purpose table.</span></span>
<span data-ttu-id="64a3d-123">Organisatsiooni hierarhia tüüp</span><span class="sxs-lookup"><span data-stu-id="64a3d-123">Organization hierarchy type</span></span> | <span data-ttu-id="64a3d-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="64a3d-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="64a3d-125">See mall tagab organisatsiooni hierarhia tüübi tabeli ühesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="64a3d-125">This template provides one-way synchronization of the Organization Hierarchy Type table.</span></span>
<span data-ttu-id="64a3d-126">Organisatsioonihierarhia – avaldatud</span><span class="sxs-lookup"><span data-stu-id="64a3d-126">Organization hierarchy - published</span></span> | <span data-ttu-id="64a3d-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="64a3d-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="64a3d-128">See mall tagab avaldatud organisatsiooni hierarhia tabeli ühesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="64a3d-128">This template provides one-way synchronization of the Organization Hierarchy Published table.</span></span>
<span data-ttu-id="64a3d-129">Tootmisüksus</span><span class="sxs-lookup"><span data-stu-id="64a3d-129">Operating unit</span></span> | <span data-ttu-id="64a3d-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="64a3d-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="64a3d-131">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="64a3d-131">Legal entities</span></span> | <span data-ttu-id="64a3d-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="64a3d-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="64a3d-133">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="64a3d-133">Legal entities</span></span> | <span data-ttu-id="64a3d-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="64a3d-134">cdm_companies</span></span> | <span data-ttu-id="64a3d-135">Tagab juriidilise isiku (ettevõtte) teabe kahesuunalise sünkroonimise.</span><span class="sxs-lookup"><span data-stu-id="64a3d-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="64a3d-136">Sisemine korraldus</span><span class="sxs-lookup"><span data-stu-id="64a3d-136">Internal Organization</span></span>

<span data-ttu-id="64a3d-137">Sisemine organisatsiooniteave Dataverse’is pärineb kahest tabelist: **tootmisüksus** ja **juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="64a3d-137">Internal organization information in Dataverse comes from two tables, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]