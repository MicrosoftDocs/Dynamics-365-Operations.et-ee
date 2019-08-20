---
title: Peaaegu reaalaja andmete integreerimine Finance and Operationsi ja Common Data Service’i vahel.
description: Selles teemas antakse ülevaade integratsioonist rakendusega Microsoft Dynamics 365 for Finance and Operations ja Common Data Service.
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
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797224"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a><span data-ttu-id="8a826-103">Peaaegu reaalaja andmete integreerimine Finance and Operationsi ja Common Data Service’i vahel.</span><span class="sxs-lookup"><span data-stu-id="8a826-103">Near-real-time data integration between Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="8a826-104">Praeguses digitaalmaailmas kasutavad äriökosüsteemid rakenduse Microsoft Dynamics 365 paketti tervikuna.</span><span class="sxs-lookup"><span data-stu-id="8a826-104">In the current digital world, business ecosystems use the Microsoft Dynamics 365 suite as a whole.</span></span> <span data-ttu-id="8a826-105">Kuna inimeste, klientide, operatsioonide ja asjade Interneti (IoT) seadmete andmed voog liigub ühte allikasse, on olemas võimalus digitaalseks tagasiside ringiks.</span><span class="sxs-lookup"><span data-stu-id="8a826-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="8a826-106">Selle kogemuse saavutamiseks on oluline integratsioon rakenduste Dynamics 365 for Finance and Operations ja Dynamics 365 for Customer Engagementi rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="8a826-106">To achieve this experience, integration between Dynamics 365 for Finance and Operations and Dynamics 365 for Customer Engagement applications is essential.</span></span> <span data-ttu-id="8a826-107">Customer Engagementi rakendused on ehitatud Common Data Service’i peale.</span><span class="sxs-lookup"><span data-stu-id="8a826-107">Customer Engagement applications are built on top of Common Data Service.</span></span> <span data-ttu-id="8a826-108">Finance and Operationsi andmete integreermine Common Data Service’iga võimaldab Customer Engagementi rakendustel ühtselt ja ladusalt suhelda Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="8a826-108">Integration between Finance and Operations data with Common Data Service lets Customer Engagement applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="8a826-109">Finance and Operations ja Common Data Service pakuvad reaalajalähedast andmete sünkroonimist Finance and Operationsi ja Customer Engagementi rakenduste vahel topeltkirjutamise raamistiku kaudu.</span><span class="sxs-lookup"><span data-stu-id="8a826-109">Finance and Operations and Common Data Service provide near-real-time data synchronization between Finance and Operations and Customer Engagement applications via a dual-write framework.</span></span> <span data-ttu-id="8a826-110">Katvus on lai ja ulatub 28 Finance and Operationsi valdkonnani.</span><span class="sxs-lookup"><span data-stu-id="8a826-110">The coverage is broad and spans 28 surface areas of Finance and Operations.</span></span> <span data-ttu-id="8a826-111">Eesmärk on pakkuda "ühtset Dynamics 365" kasutaja kogemust tõrgeteta andmevoos, mis ühendab äriprotsessid rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="8a826-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Ülesehituse ülevaatlik diagramm](media/dual-write-overview.jpg)

<span data-ttu-id="8a826-113">Klientide jaoks on saadaval järgmised väärtusettepanekud.</span><span class="sxs-lookup"><span data-stu-id="8a826-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="8a826-114">Organisatsiooni hierarhia teenusesCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="8a826-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="8a826-115">Ettevõtte kontseptsioon rakendusesCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="8a826-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="8a826-116">Hankija koondandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="8a826-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="8a826-117">Müüja koondandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="8a826-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="8a826-118">Ühendatud tooteetalon</span><span class="sxs-lookup"><span data-stu-id="8a826-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="8a826-119">Süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="8a826-119">System requirements</span></span>

<span data-ttu-id="8a826-120">Sünkroonne, kahesuunaline, reaalaja lähedased andmevood nõuavad järgmisi versioone.</span><span class="sxs-lookup"><span data-stu-id="8a826-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="8a826-121">Rakenduse Microsoft Dynamics 365 for Finance and Operations versioon 10.0.4 (november 2019) platvormivärskendusega 28 või uuem</span><span class="sxs-lookup"><span data-stu-id="8a826-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="8a826-122">Microsoft Dynamics 365 for Customer Engagementi versioon 9.1 (4.2) või uuem</span><span class="sxs-lookup"><span data-stu-id="8a826-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="8a826-123">Seadistusjuhised</span><span class="sxs-lookup"><span data-stu-id="8a826-123">Setup instructions</span></span>

<span data-ttu-id="8a826-124">Seadistage rakenduste Finance and Operations ja Common Data Service vaheline integratsioon.</span><span class="sxs-lookup"><span data-stu-id="8a826-124">Follow these steps to set up integration between Finance and Operations and Common Data Service.</span></span>
    
1. <span data-ttu-id="8a826-125">Topeltkirjutamise süsteemi sätestamiseks vaadake [üksikasjalikku juhendit](https://aka.ms/dualwrite-docs) topelkirjutamise eelvaate kohta.</span><span class="sxs-lookup"><span data-stu-id="8a826-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="8a826-126">Laadige alla ja installige lahendus rakenduste [Finance and Operations, Common Data Service ja Customer Engagementi integreerimise](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer rühmast.</span><span class="sxs-lookup"><span data-stu-id="8a826-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="8a826-127">Pakett sisaldab viit lahendust:</span><span class="sxs-lookup"><span data-stu-id="8a826-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="8a826-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="8a826-128">Dynamics365Company</span></span>
    + <span data-ttu-id="8a826-129">Valuuta vahetuskursi määrad</span><span class="sxs-lookup"><span data-stu-id="8a826-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="8a826-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="8a826-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="8a826-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="8a826-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="8a826-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="8a826-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="8a826-133">Järgige täitmistellimust [esialgsete viiteandmete sünkroonimiseks](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="8a826-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="8a826-134">Kui teil esineb topeltkirjutamise sünkroonimisel probleeme, vaadake teemat [Tõrkeotsingu juhend andmete integreerimiseks ](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="8a826-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8a826-135">Te ei saa käivitada topeltkirjutamist [ja raha väljavaadet](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="8a826-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="8a826-136">Kui kasutate raha väljavaate lahendust, peate selle desinstallima.</span><span class="sxs-lookup"><span data-stu-id="8a826-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="8a826-137">Samuti peate keelama kliendi ja hankija topeltkirjutamise mallid, mis on osa raha väljavaate lahendusest.</span><span class="sxs-lookup"><span data-stu-id="8a826-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
