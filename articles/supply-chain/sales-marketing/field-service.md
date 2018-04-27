---
title: Integreerimine rakendusega Microsoft Dynamics 365 for Field Service
description: "Selles teemas antakse ülevaade integreerimisest rakendusega Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: et-ee
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="a63c0-103">Integreerimine rakendusega Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="a63c0-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a63c0-104">Microsoft Dynamics 365 for Finance and Operations võimaldab sünkroonida äriprotsesse rakenduste Finance and Operations ja Microsoft Dynamics 365 for Field Service vahel.</span><span class="sxs-lookup"><span data-stu-id="a63c0-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="a63c0-105">Integreerimisstsenaariume saab konfigureerida äriprotsesside sünkroonimist lubama laiendatavates andmeintegraatori mallides ja Common Data Service’is (CDS).</span><span class="sxs-lookup"><span data-stu-id="a63c0-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="a63c0-106">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="a63c0-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="a63c0-107">Rakenduste Field Service ja Finance and Operations integreerimise esimeses faasis keskendutakse rakenduse Field Service töötellimuste ja lepingute arveldamise lubamisele rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a63c0-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="a63c0-108">Toetatud voog algab rakenduses Field Service, kus töötellimuste teave sünkroonitakse müügitellimustena rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a63c0-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="a63c0-109">Rakenduses Finance and Operations arveldatakse müügitellimused, et luua arve dokumendid.</span><span class="sxs-lookup"><span data-stu-id="a63c0-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="a63c0-110">Lisaks sünkroonitakse rakenduse Field Service lepingu arvete teave rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a63c0-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="a63c0-111">Microsoft Dynamics 365 andmeintegraator sünkroonib andmed kohandatavate projektide abil.</span><span class="sxs-lookup"><span data-stu-id="a63c0-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="a63c0-112">Kohandatud integratsiooniprojektide loomiseks saab kasutada standardmalle, kus standardseid ja kohandatud lisavälju, samuti üksusi saab integratsiooni korrigeerimiseks ja konkreetsete nõuetega kooskõlla viimiseks vastendada.</span><span class="sxs-lookup"><span data-stu-id="a63c0-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="a63c0-113">Rakenduste Field Service ja Finance and Operations integratsiooni esimeses faasis võimaldatakse sünkroonida järgmisi kaupu.</span><span class="sxs-lookup"><span data-stu-id="a63c0-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="a63c0-114">Rakenduse Finance and Operations tooted rakenduse Field Service toote tüübi teavet sisaldavate toodetega</span><span class="sxs-lookup"><span data-stu-id="a63c0-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="a63c0-115">Rakenduse Field Service töötellimused rakenduse Finance and Operations müügitellimustega</span><span class="sxs-lookup"><span data-stu-id="a63c0-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="a63c0-116">Rakenduse Field Service arved vabas vormis arveteks rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a63c0-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="a63c0-117">Rakenduse Finance and Operations süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="a63c0-117">System requirements for Finance and Operations</span></span>
<span data-ttu-id="a63c0-118">Rakenduse Field Service integratsioon toetab järgmisi versioone.</span><span class="sxs-lookup"><span data-stu-id="a63c0-118">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="a63c0-119">Dynamics 365 for Finance and Operations versioon 8.0 (aprill 2018) või hilisem</span><span class="sxs-lookup"><span data-stu-id="a63c0-119">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="a63c0-120">Dynamics 365 for Finance and Operations versioon 8.0 (aprill 2018) väljastati aprillis 2018 ja selle rakenduse järgunumber on 8.0.30.8020 platvormivärskendusega 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="a63c0-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="a63c0-121">Rakenduse Field Service süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="a63c0-121">System requirements for Field Service</span></span>
<span data-ttu-id="a63c0-122">Rakenduse Field Service integreerimislahenduse kasutamiseks tuleb installida järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="a63c0-122">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="a63c0-123">Microsoft Dynamics 365 for Field Service 9.0 või hilisem</span><span class="sxs-lookup"><span data-stu-id="a63c0-123">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="a63c0-124">Rakenduse Dynamics 365 for Field Service versiooni 1612 (9.0.1.733) (DB 9.0.1.733) veebiversioon või hilisem versioon.</span><span class="sxs-lookup"><span data-stu-id="a63c0-124">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="a63c0-125">Lahendus Potentsiaalne klient sularahaks (P2C) rakendusele Dynamics 365, versioon 1.15.0.1 või hilisem versioon.</span><span class="sxs-lookup"><span data-stu-id="a63c0-125">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="a63c0-126">Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="a63c0-126">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="a63c0-127">Rakenduse Field Service integreerimislahendus Dynamics 365 jaoks, versioon 1.0.0.0 või hilisem versioon.</span><span class="sxs-lookup"><span data-stu-id="a63c0-127">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="a63c0-128">Lahendus on allalaadimiseks saadaval AppSource’is.</span><span class="sxs-lookup"><span data-stu-id="a63c0-128">The solution is available for download from AppSource.</span></span> <span data-ttu-id="a63c0-129">**(VÄLJASTAMISE OOTEL)**</span><span class="sxs-lookup"><span data-stu-id="a63c0-129">**(PENDING RELEASE)**</span></span>

