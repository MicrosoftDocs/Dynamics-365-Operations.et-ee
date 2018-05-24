---
title: Integreerimine rakendusega Microsoft Dynamics 365 for Field Service
description: "Selles teemas antakse ülevaade integreerimisest rakendusega Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
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
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="25250-103">Integreerimine rakendusega Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="25250-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="25250-104">Microsoft Dynamics 365 for Finance and Operations võimaldab sünkroonida äriprotsesse rakenduste Finance and Operations ja Microsoft Dynamics 365 for Field Service vahel.</span><span class="sxs-lookup"><span data-stu-id="25250-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="25250-105">Integreerimisstsenaariume saab konfigureerida äriprotsesside sünkroonimist lubama laiendatavates andmeintegraatori mallides ja Common Data Service’is (CDS).</span><span class="sxs-lookup"><span data-stu-id="25250-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="25250-106">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="25250-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="25250-107">Rakenduste Field Service ja Finance and Operations integreerimise esimeses faasis keskendutakse rakenduse Field Service töötellimuste ja lepingute arveldamise lubamisele rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="25250-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="25250-108">Toetatud voog algab rakenduses Field Service, kus töötellimuste teave sünkroonitakse müügitellimustena rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="25250-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="25250-109">Rakenduses Finance and Operations arveldatakse müügitellimused, et luua arve dokumendid.</span><span class="sxs-lookup"><span data-stu-id="25250-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="25250-110">Lisaks sünkroonitakse rakenduse Field Service lepingu arvete teave rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="25250-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="25250-111">Microsoft Dynamics 365 andmeintegraator sünkroonib andmed kohandatavate projektide abil.</span><span class="sxs-lookup"><span data-stu-id="25250-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="25250-112">Kohandatud integratsiooniprojektide loomiseks saab kasutada standardmalle, kus standardseid ja kohandatud lisavälju, samuti üksusi saab integratsiooni korrigeerimiseks ja konkreetsete nõuetega kooskõlla viimiseks vastendada.</span><span class="sxs-lookup"><span data-stu-id="25250-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="25250-113">Rakenduste Field Service ja Finance and Operations integratsiooni esimeses faasis võimaldatakse sünkroonida järgmisi kaupu.</span><span class="sxs-lookup"><span data-stu-id="25250-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="25250-114">Rakenduse Finance and Operations tooted rakenduse Field Service toote tüübi teavet sisaldavate toodetega</span><span class="sxs-lookup"><span data-stu-id="25250-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="25250-115">Rakenduse Field Service töötellimused rakenduse Finance and Operations müügitellimustega</span><span class="sxs-lookup"><span data-stu-id="25250-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="25250-116">Rakenduse Field Service arved vabas vormis arveteks rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="25250-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="25250-117">Töökäsu sünkroonimise kohta rakenduse Field Service ja rakenduse Finance and Operations vahel vaadake lühikest YouTube’i näitevideot:</span><span class="sxs-lookup"><span data-stu-id="25250-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[<span data-ttu-id="25250-118">Töökäsu sünkroonimine rakenduse Field Service ja rakenduse Finance and Operations vahel (YouTube’i video)</span><span class="sxs-lookup"><span data-stu-id="25250-118">Synchronize a work order between Field Service and Finance and Operations (YouTube video)</span></span>](https://youtu.be/hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="25250-119">Rakenduse Finance and Operations süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="25250-119">System requirements for Finance and Operations</span></span>
<span data-ttu-id="25250-120">Rakenduse Field Service integratsioon toetab järgmisi versioone.</span><span class="sxs-lookup"><span data-stu-id="25250-120">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="25250-121">Dynamics 365 for Finance and Operations versioon 8.0 (aprill 2018) või hilisem</span><span class="sxs-lookup"><span data-stu-id="25250-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="25250-122">Dynamics 365 for Finance and Operations versioon 8.0 (aprill 2018) väljastati aprillis 2018 ja selle rakenduse järgunumber on 8.0.30.8020 platvormivärskendusega 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="25250-122">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="25250-123">Rakenduse Field Service süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="25250-123">System requirements for Field Service</span></span>
<span data-ttu-id="25250-124">Rakenduse Field Service integreerimislahenduse kasutamiseks tuleb installida järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="25250-124">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="25250-125">Microsoft Dynamics 365 for Field Service 9.0 või hilisem</span><span class="sxs-lookup"><span data-stu-id="25250-125">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="25250-126">Rakenduse Dynamics 365 for Field Service versiooni 1612 (9.0.1.733) (DB 9.0.1.733) veebiversioon või hilisem versioon.</span><span class="sxs-lookup"><span data-stu-id="25250-126">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="25250-127">Lahendus Potentsiaalne klient sularahaks (P2C) rakendusele Dynamics 365, versioon 1.15.0.1 või hilisem versioon.</span><span class="sxs-lookup"><span data-stu-id="25250-127">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="25250-128">Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="25250-128">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="25250-129">Rakenduse Field Service integreerimislahendus Dynamics 365 jaoks, versioon 1.0.0.0 või hilisem versioon.</span><span class="sxs-lookup"><span data-stu-id="25250-129">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="25250-130">Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="25250-130">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

