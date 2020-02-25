---
title: Reaalaja lähedane teabe integratsioon teenusega Common Data Service
description: Selles teemas antakse ülevaade integratsioonist rakendusega Finance and Operations ja Common Data Service.
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
ms.openlocfilehash: 1c09b0c0bb695e7695acb7a8821ffb99ae1f6f06
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019742"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="bc372-103">Reaalaja lähedane teabe integratsioon teenusega Common Data Service</span><span class="sxs-lookup"><span data-stu-id="bc372-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="bc372-104">Praeguses digitaalmaailmas kasutavad äriökosüsteemid rakenduste Microsoft Dynamics 365 paketti tervikuna.</span><span class="sxs-lookup"><span data-stu-id="bc372-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="bc372-105">Kuna inimeste, klientide, operatsioonide ja asjade Interneti (IoT) seadmete andmed voog liigub ühte allikasse, on olemas võimalus digitaalseks tagasiside ringiks.</span><span class="sxs-lookup"><span data-stu-id="bc372-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="bc372-106">Selle kogemuse saavutamiseks on oluline integratsioon rakenduste Finance and Operations ja Dynamics 365 vahel.</span><span class="sxs-lookup"><span data-stu-id="bc372-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="bc372-107">Mõned rakendused on ehitatud Common Data Service’i peale.</span><span class="sxs-lookup"><span data-stu-id="bc372-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="bc372-108">Rakenduse Finance and Operations ja Common Data Service andmete integratsioon võimaldab teistel rakendustel sidusalt ja ladusalt Finance and Operationsiga ladusalt suhelda.</span><span class="sxs-lookup"><span data-stu-id="bc372-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="bc372-109">Rakendustekomplekt Finance and Operations ja Common Data Service pakuvad reaalajalähedast andmete sünkroonimist rakendustekomplekti Finance and Operations ja teiste Dynamics 365 rakenduste vahel topeltkirjutamise raamistiku kaudu.</span><span class="sxs-lookup"><span data-stu-id="bc372-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="bc372-110">Katvus on lai ja ulatub 28 rakenduse valdkonnani.</span><span class="sxs-lookup"><span data-stu-id="bc372-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="bc372-111">Eesmärk on pakkuda "ühtset Dynamics 365" kasutaja kogemust tõrgeteta andmevoos, mis ühendab äriprotsessid rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="bc372-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Ülesehituse ülevaatlik diagramm](media/dual-write-overview.jpg)

<span data-ttu-id="bc372-113">Saadaval on järgmised väärtusettepanekud.</span><span class="sxs-lookup"><span data-stu-id="bc372-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="bc372-114">Organisatsiooni hierarhia teenusesCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="bc372-114">Organization hierarchy in Common Data Service</span></span>](organization-mapping.md)
+ [<span data-ttu-id="bc372-115">Ettevõtte kontseptsioon rakendusesCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="bc372-115">Company concept in Common Data Service</span></span>](company-data.md)
+ [<span data-ttu-id="bc372-116">Hankija koondandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="bc372-116">Integrated customer master</span></span>](customer-mapping.md)
+ [<span data-ttu-id="bc372-117">Integreeritud pearaamat</span><span class="sxs-lookup"><span data-stu-id="bc372-117">Integrated ledger</span></span>](ledger-mapping.md)
+ [<span data-ttu-id="bc372-118">Ühendatud toote kasutusfunktsionaalsus</span><span class="sxs-lookup"><span data-stu-id="bc372-118">Unified product experience</span></span>](product-mapping.md)
+ [<span data-ttu-id="bc372-119">Müüja koondandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="bc372-119">Integrated vendor master</span></span>](vendor-mapping.md)
+ [<span data-ttu-id="bc372-120">Integreeritu kohad ja laod</span><span class="sxs-lookup"><span data-stu-id="bc372-120">Integrated sites and warehouses</span></span>](sites-warehouses-mapping.md)
+ [<span data-ttu-id="bc372-121">Integreeritud maksude koondandmed</span><span class="sxs-lookup"><span data-stu-id="bc372-121">Integrated tax master</span></span>](tax-mapping.md)

## <a name="system-requirements"></a><span data-ttu-id="bc372-122">Süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="bc372-122">System requirements</span></span>

<span data-ttu-id="bc372-123">Sünkroonne, kahesuunaline, reaalaja lähedased andmevood nõuavad järgmisi versioone.</span><span class="sxs-lookup"><span data-stu-id="bc372-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="bc372-124">Rakenduse Microsoft Dynamics 365 for Finance and Operations versioon 10.0.4 (november 2019) platvormivärskendusega 28 või uuem</span><span class="sxs-lookup"><span data-stu-id="bc372-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="bc372-125">Microsoft Dynamics 365 for Customer Engagementi versioon 9.1 (4.2) või uuem</span><span class="sxs-lookup"><span data-stu-id="bc372-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="bc372-126">Seadistusjuhised</span><span class="sxs-lookup"><span data-stu-id="bc372-126">Setup instructions</span></span>

<span data-ttu-id="bc372-127">Järgige neid etappe rakendustekomplekti Finance and Operations ja Common Data Servicei integratsiooni seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="bc372-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="bc372-128">Topeltkirjutamise süsteemi sätestamiseks vaadake [üksikasjalikku juhendit](https://aka.ms/dualwrite-docs) topelkirjutamise eelvaate kohta.</span><span class="sxs-lookup"><span data-stu-id="bc372-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="bc372-129">Laadige alla ja installige lahendus [topeltkirjutuse kaudu Fin Opsi ja CDS/CE integratsioonist](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammeri grupis.</span><span class="sxs-lookup"><span data-stu-id="bc372-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="bc372-130">Pakett sisaldab viit lahendust:</span><span class="sxs-lookup"><span data-stu-id="bc372-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="bc372-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="bc372-131">Dynamics365Company</span></span>
    + <span data-ttu-id="bc372-132">Valuuta vahetuskursi määrad</span><span class="sxs-lookup"><span data-stu-id="bc372-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="bc372-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="bc372-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="bc372-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="bc372-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="bc372-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="bc372-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="bc372-136">Järgige täitmistellimust [esialgsete viiteandmete sünkroonimiseks](initial-sync.md).</span><span class="sxs-lookup"><span data-stu-id="bc372-136">Follow the execution order for [synchronizing initial reference data](initial-sync.md).</span></span>
4. <span data-ttu-id="bc372-137">Kui teil esineb topeltkirjutamise sünkroonimisel probleeme, vaadake teemat [Tõrkeotsingu juhend andmete integreerimiseks ](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="bc372-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bc372-138">Te ei saa käivitada topeltkirjutamist [ja raha väljavaadet](../../../../supply-chain/sales-marketing/prospect-to-cash.md) kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="bc372-138">You can’t run dual-write and [Prospect to cash](../../../../supply-chain/sales-marketing/prospect-to-cash.md) side-by-side.</span></span> <span data-ttu-id="bc372-139">Kui kasutate raha väljavaate lahendust, peate selle desinstallima.</span><span class="sxs-lookup"><span data-stu-id="bc372-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="bc372-140">Samuti peate keelama kliendi ja hankija topeltkirjutamise mallid, mis on osa raha väljavaate lahendusest.</span><span class="sxs-lookup"><span data-stu-id="bc372-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
