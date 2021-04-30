---
title: Dynamics 365 globaliseerimisteenused
description: Teema annab ülevaate Microsoft Dynamics 365 globaliseerimisteenustest.
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893044"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="78159-103">Dynamics 365 globaliseerimisteenused</span><span class="sxs-lookup"><span data-stu-id="78159-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="78159-104">Microsoft Dynamics 365 võrguteenuse võimaluste laiendamiseks saab konfigureerida järgmisi globaliseerumisteenuseid.</span><span class="sxs-lookup"><span data-stu-id="78159-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="78159-105">**Regulatory Configuration Service (RCS)** toetab erinevat tüüpi elektrooniliste dokumentide ja aruannete konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="78159-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="78159-106">RCS pakub täiustatud versiooni elektroonilise aruandluse (ER) kujundajast, kus konfiguratsioonihoidla on autonoomne teenus.</span><span class="sxs-lookup"><span data-stu-id="78159-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="78159-107">Lisateavet vt teemast [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="78159-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="78159-108">**E-arveldamine** koondab konfigureeritavad vormingud teisendusteks, digitaalallkirjadeks ja konfigureeritavateks integratsioonideks ühenduvuseks väliste veebiteenustega, sealhulgas sertifitseerimiseks ja reageerimiseks.</span><span class="sxs-lookup"><span data-stu-id="78159-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="78159-109">Lisateavet leiate teemast [E-arveldus](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="78159-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="78159-110">**Maksuarvestus** pakub suuremat paindlikkust, toetades mitut maksu-ID-d, maksukoodi määramist, maksuarvestuse kujundajat ja käitusaja mootorit, et täita keerulisi maksueeskirju kogu maailmas.</span><span class="sxs-lookup"><span data-stu-id="78159-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="78159-111">Lisateavet vt jaotisest [Maksuarvestus](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="78159-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="78159-112">Need globaliseerumisteenused pakuvad out-of-box integratsiooni järgmiste Dynamics 365 võrguteenustega.</span><span class="sxs-lookup"><span data-stu-id="78159-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="78159-113">Võrguteenus</span><span class="sxs-lookup"><span data-stu-id="78159-113">Online service</span></span> | <span data-ttu-id="78159-114">RCS</span><span class="sxs-lookup"><span data-stu-id="78159-114">RCS</span></span> | <span data-ttu-id="78159-115">Elektrooniline arveldus</span><span class="sxs-lookup"><span data-stu-id="78159-115">Electronic Invoicing</span></span> | <span data-ttu-id="78159-116">Maksuarvutus (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="78159-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="78159-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="78159-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="78159-118">Jah</span><span class="sxs-lookup"><span data-stu-id="78159-118">Yes</span></span> | <span data-ttu-id="78159-119">Jah</span><span class="sxs-lookup"><span data-stu-id="78159-119">Yes</span></span> | <span data-ttu-id="78159-120">Jah</span><span class="sxs-lookup"><span data-stu-id="78159-120">Yes</span></span> | 
| <span data-ttu-id="78159-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="78159-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="78159-122">Jah</span><span class="sxs-lookup"><span data-stu-id="78159-122">Yes</span></span> | <span data-ttu-id="78159-123">Jah</span><span class="sxs-lookup"><span data-stu-id="78159-123">Yes</span></span> | <span data-ttu-id="78159-124">Jah</span><span class="sxs-lookup"><span data-stu-id="78159-124">Yes</span></span> | 
| <span data-ttu-id="78159-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="78159-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="78159-126">Jah</span><span class="sxs-lookup"><span data-stu-id="78159-126">Yes</span></span> | <span data-ttu-id="78159-127">Jah</span><span class="sxs-lookup"><span data-stu-id="78159-127">Yes</span></span> | <span data-ttu-id="78159-128">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="78159-128">Not applicable</span></span> | 
| <span data-ttu-id="78159-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="78159-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="78159-130">Jah</span><span class="sxs-lookup"><span data-stu-id="78159-130">Yes</span></span> | <span data-ttu-id="78159-131">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="78159-131">Not applicable</span></span> | <span data-ttu-id="78159-132">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="78159-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="78159-133">RCS-i Azure'i geograafiliste asukohtade (geode) kättesaadavuse erinevuste tõttu võib selle teenuse konfigureerimine põhjustada kliendiandmete edastamise väljaspool rakenduse Dynamics 365 veebiteenuse jaoks valitud geograafilist piirkonda.</span><span class="sxs-lookup"><span data-stu-id="78159-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="78159-134">Lisateavet vt teemast [Dynamics 365 ja Power Platform: saadavus, andmete asukoht, keel ja lokaliseerimine](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="78159-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>