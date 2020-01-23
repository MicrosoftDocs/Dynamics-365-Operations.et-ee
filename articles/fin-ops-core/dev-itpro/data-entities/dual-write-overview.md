---
title: Reaalaja lähedane teabe integratsioon teenusega Common Data Service
description: Selles teemas antakse ülevaade integreerimisest Finance and Operationsi ja teenuse Common Data Service vahel.
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
ms.openlocfilehash: 072564446b74318ffc8e8e6ad4fd16f4421e7854
ms.sourcegitcommit: d0322d1ed6c798301058e44dae76227a0e1f49ac
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/26/2019
ms.locfileid: "2853902"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="df4ee-103">Reaalaja lähedane teabe integratsioon teenusega Common Data Service</span><span class="sxs-lookup"><span data-stu-id="df4ee-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df4ee-104">Praeguses digitaalmaailmas kasutavad äriökosüsteemid rakenduste Microsoft Dynamics 365 paketti tervikuna.</span><span class="sxs-lookup"><span data-stu-id="df4ee-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="df4ee-105">Kuna inimeste, klientide, operatsioonide ja asjade Interneti (IoT) seadmete andmed voog liigub ühte allikasse, on olemas võimalus digitaalseks tagasiside ringiks.</span><span class="sxs-lookup"><span data-stu-id="df4ee-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="df4ee-106">Selle kogemuse saavutamiseks on oluline integratsioon rakenduste Finance and Operations ja Dynamics 365 vahel.</span><span class="sxs-lookup"><span data-stu-id="df4ee-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="df4ee-107">Mõned rakendused on ehitatud Common Data Service’i peale.</span><span class="sxs-lookup"><span data-stu-id="df4ee-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="df4ee-108">Finance and Operationsi rakenduste andmete integreermine Common Data Service’iga võimaldab teistel rakendustel ühtselt ja ladusalt suhelda Finance and Operationsis.</span><span class="sxs-lookup"><span data-stu-id="df4ee-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="df4ee-109">Finance and Operationsi rakendused ja Common Data Service pakuvad reaalajalähedast andmete sünkroonimist Finance and Operationsi rakenduste ja Dynamics 365 rakenduste vahel topeltkirjutamise raamistiku kaudu.</span><span class="sxs-lookup"><span data-stu-id="df4ee-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="df4ee-110">Katvus on lai ja ulatub 28 rakenduse valdkonnani.</span><span class="sxs-lookup"><span data-stu-id="df4ee-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="df4ee-111">Eesmärk on pakkuda "ühtset Dynamics 365" kasutaja kogemust tõrgeteta andmevoos, mis ühendab äriprotsessid rakenduste vahel.</span><span class="sxs-lookup"><span data-stu-id="df4ee-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![Ülesehituse ülevaatlik diagramm](media/dual-write-overview.jpg)

<span data-ttu-id="df4ee-113">Saadaval on järgmised väärtusettepanekud.</span><span class="sxs-lookup"><span data-stu-id="df4ee-113">The following value propositions are available:</span></span>

+ [<span data-ttu-id="df4ee-114">Organisatsiooni hierarhia teenusesCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="df4ee-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="df4ee-115">Ettevõtte kontseptsioon rakendusesCommon Data Service</span><span class="sxs-lookup"><span data-stu-id="df4ee-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="df4ee-116">Hankija koondandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="df4ee-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="df4ee-117">Integreeritud pearaamat</span><span class="sxs-lookup"><span data-stu-id="df4ee-117">Integrated ledger</span></span>](dual-write-ledger.md)
+ [<span data-ttu-id="df4ee-118">Ühendatud toote kasutusfunktsionaalsus</span><span class="sxs-lookup"><span data-stu-id="df4ee-118">Unified product experience</span></span>](dual-write-product.md)
+ [<span data-ttu-id="df4ee-119">Müüja koondandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="df4ee-119">Integrated vendor master</span></span>](dual-write-vendor.md)
+ [<span data-ttu-id="df4ee-120">Integreeritu kohad ja laod</span><span class="sxs-lookup"><span data-stu-id="df4ee-120">Integrated sites and warehouses</span></span>](dual-write-sites-and-warehouses.md)
+ [<span data-ttu-id="df4ee-121">Integreeritud maksude koondandmed</span><span class="sxs-lookup"><span data-stu-id="df4ee-121">Integrated tax master</span></span>](dual-write-tax.md)

## <a name="system-requirements"></a><span data-ttu-id="df4ee-122">Süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="df4ee-122">System requirements</span></span>

<span data-ttu-id="df4ee-123">Sünkroonne, kahesuunaline, reaalaja lähedased andmevood nõuavad järgmisi versioone.</span><span class="sxs-lookup"><span data-stu-id="df4ee-123">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="df4ee-124">Rakenduse Microsoft Dynamics 365 for Finance and Operations versioon 10.0.4 (november 2019) platvormivärskendusega 28 või uuem</span><span class="sxs-lookup"><span data-stu-id="df4ee-124">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="df4ee-125">Microsoft Dynamics 365 for Customer Engagementi versioon 9.1 (4.2) või uuem</span><span class="sxs-lookup"><span data-stu-id="df4ee-125">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="df4ee-126">Seadistusjuhised</span><span class="sxs-lookup"><span data-stu-id="df4ee-126">Setup instructions</span></span>

<span data-ttu-id="df4ee-127">Seadistage rakenduste Finance and Operationsi rakenduste ja Common Data Service vaheline integratsioon.</span><span class="sxs-lookup"><span data-stu-id="df4ee-127">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="df4ee-128">Topeltkirjutamise süsteemi sätestamiseks vaadake [üksikasjalikku juhendit](https://aka.ms/dualwrite-docs) topelkirjutamise eelvaate kohta.</span><span class="sxs-lookup"><span data-stu-id="df4ee-128">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="df4ee-129">Laadige alla ja installige lahendus [topeltkirjutuse kaudu Fin Opsi ja CDS/CE integratsioonist](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammeri grupis.</span><span class="sxs-lookup"><span data-stu-id="df4ee-129">Download and install the solution from the [Fin Ops and CDS/CE Integration via Dual-Write](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="df4ee-130">Pakett sisaldab viit lahendust:</span><span class="sxs-lookup"><span data-stu-id="df4ee-130">The package contains five solutions:</span></span>

    + <span data-ttu-id="df4ee-131">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="df4ee-131">Dynamics365Company</span></span>
    + <span data-ttu-id="df4ee-132">Valuuta vahetuskursi määrad</span><span class="sxs-lookup"><span data-stu-id="df4ee-132">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="df4ee-133">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="df4ee-133">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="df4ee-134">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="df4ee-134">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="df4ee-135">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="df4ee-135">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="df4ee-136">Järgige täitmistellimust [esialgsete viiteandmete sünkroonimiseks](dual-write-initial.md).</span><span class="sxs-lookup"><span data-stu-id="df4ee-136">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="df4ee-137">Kui teil esineb topeltkirjutamise sünkroonimisel probleeme, vaadake teemat [Tõrkeotsingu juhend andmete integreerimiseks ](dual-write-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="df4ee-137">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df4ee-138">Te ei saa käivitada topeltkirjutamist [ja raha väljavaadet](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) kõrvuti.</span><span class="sxs-lookup"><span data-stu-id="df4ee-138">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="df4ee-139">Kui kasutate raha väljavaate lahendust, peate selle desinstallima.</span><span class="sxs-lookup"><span data-stu-id="df4ee-139">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="df4ee-140">Samuti peate keelama kliendi ja hankija topeltkirjutamise mallid, mis on osa raha väljavaate lahendusest.</span><span class="sxs-lookup"><span data-stu-id="df4ee-140">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
