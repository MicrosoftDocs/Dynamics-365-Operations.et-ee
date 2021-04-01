---
title: Ülevaade integratsioonist rakendusega Microsoft Dynamics 365 Field Service
description: Selles teemas antakse ülevaade integratsioonist rakendusega Microsoft Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 9b0fafd46143979a734151b4011e537991347862
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237890"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a><span data-ttu-id="e671d-103">Ülevaade integratsioonist rakendusega Microsoft Dynamics 365 Field Service</span><span class="sxs-lookup"><span data-stu-id="e671d-103">Integration with Microsoft Dynamics 365 Field Service overview</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e671d-104">Tarneahela juhtimine võimaldab äriprotsesside sünkrooniminst rakenduste Dynamics 365 Supply Chain Management ja Dynamics 365 Field Service vahel.</span><span class="sxs-lookup"><span data-stu-id="e671d-104">Supply Chain Management enables synchronization of business processes between Dynamics 365 Supply Chain Management and Dynamics 365 Field Service.</span></span> <span data-ttu-id="e671d-105">Integreerimisstsenaariume konfigureeritakse lubama äriprotsesside sünkroonimist laiendatavates andmeintegraatori mallides ja teenuses Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e671d-105">The integration scenarios are configured by using extensible Data integrator templates and Microsoft Dataverse to enable the synchronization of business processes.</span></span>
<span data-ttu-id="e671d-106">Kohandatud integratsiooniprojektide loomiseks saab kasutada standardmalle, kus standardseid ja kohandatud lisaveerge ja tabeleid saab integratsiooni korrigeerimiseks ja konkreetsete ärivajadustega kooskõlla viimiseks vastendada.</span><span class="sxs-lookup"><span data-stu-id="e671d-106">Standard templates can be used to create custom integration projects, where additional standard and custom columns and tables can be mapped to adjust the integration and meet specific business needs.</span></span> 

<span data-ttu-id="e671d-107">Välja teenuse integreerimine rajaneb olemasoleva potentsiaalse kliendi funktsioonil.</span><span class="sxs-lookup"><span data-stu-id="e671d-107">The field service integration builds on top of the existing prospect-to-cash functionality.</span></span>

![Äriprotsesside sünkroniseerimine rakenduste Supply Chain Management ja Field Service vahel.](./media/field-service-integration.png)

<span data-ttu-id="e671d-109">Rakenduste Field Service ja Supply Chain Management integreerimise esimeses faasis keskendutakse rakenduse Field Service töötellimuste ja lepingute arveldamise lubamisele rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e671d-109">The first phase  of the integration between Field Service and Supply Chain Management is focused on enabling work orders and agreements in Field Service to be invoiced in Supply Chain Management.</span></span> <span data-ttu-id="e671d-110">Toetatud voog algab rakenduses Field Service, kus töötellimuste teave sünkroonitakse müügitellimustena rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e671d-110">The supported flow starts in Field Service, where information from work orders is synchronized to Supply Chain Management as sales orders.</span></span> <span data-ttu-id="e671d-111">Rakenduses Supply Chain Management arveldatakse müügitellimused arve dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e671d-111">In Supply Chain Management, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="e671d-112">Lisaks sünkroonitakse rakenduse Field Service lepingu arvete teave rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e671d-112">In addition, the information from Field Service agreement invoices is synchronized to Supply Chain Management.</span></span> <span data-ttu-id="e671d-113">Microsoft Dynamics 365 andmeintegraator sünkroonib andmed kohandatavate projektide abil.</span><span class="sxs-lookup"><span data-stu-id="e671d-113">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="e671d-114">Kohandatud integratsiooniprojektide loomiseks saab kasutada standardmalle, kus standardseid ja kohandatud lisaveerge, samuti tabeleid saab integratsiooni korrigeerimiseks ja konkreetsete nõuetega kooskõlla viimiseks vastendada.</span><span class="sxs-lookup"><span data-stu-id="e671d-114">Standard templates can be used to create custom integration projects where additional standard and custom columns, and also tables, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="e671d-115">Rakenduste Field Service ja Supply Chain Management integratsiooni esimeses faasis võimaldatakse sünkroonida järgmisi kaupu.</span><span class="sxs-lookup"><span data-stu-id="e671d-115">The first phase of the integration between Field Service and Supply Chain Management enables synchronization of the following items:</span></span>

- [<span data-ttu-id="e671d-116">Rakenduses Supply Chain Management toodete sünkroonimine rakenduse Field Service toodetega</span><span class="sxs-lookup"><span data-stu-id="e671d-116">Synchronize products in Supply Chain Management to products in Field Service</span></span>](field-service-product.md)
- [<span data-ttu-id="e671d-117">Sünkroonige rakenduse Field Service töötellimused rakenduse Supply Chain Management müügitellimustega</span><span class="sxs-lookup"><span data-stu-id="e671d-117">Synchronize work orders in Field Service to sales orders in Supply Chain Management</span></span>](field-service-work-order.md)
- [<span data-ttu-id="e671d-118">Sünkroonige leppe arved rakenduses Field Service vabas vormis arveteks rakenduses Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e671d-118">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>](field-service-invoice.md)

<span data-ttu-id="e671d-119">Näite saamiseks, kuidas sünkroonida töökäsk Field Service’i ja Supply Chain Managementi vahel, vaadake YouTube’i lühivideot [Töökäsu sünkroonimine rakenduse Microsoft Dynamics 365 integratsiooniga](https://www.youtube.com/watch?v=46ylO7raZAo).</span><span class="sxs-lookup"><span data-stu-id="e671d-119">To see an example of how you can synchronize a work order between Field Service and Supply Chain Management, watch the short YouTube video [How to synchronize a work order with Microsoft Dynamics 365 Integration](https://www.youtube.com/watch?v=46ylO7raZAo).</span></span>

## <a name="integration-with-field-service-including-inventory-and-project-information"></a><span data-ttu-id="e671d-120">Integratsioon rakendusega Field Service, sh arvatud varude ja projekti teave</span><span class="sxs-lookup"><span data-stu-id="e671d-120">Integration with Field Service, including inventory and project information</span></span>

<span data-ttu-id="e671d-121">Lisafunktsioon selles teises etapis on suunatud väljatehnikutele ülevaate andmiseks laoinfo kohta rakendusest Supply Chain Management, võimaldades neil laovarude tasemeid uuendada ja teha materjali ülekanded.</span><span class="sxs-lookup"><span data-stu-id="e671d-121">The additional functionality in this second phase focused on giving field technicians insight about the inventory information from Supply Chain Management, allowing them to update inventory levels and do material transfers.</span></span> <span data-ttu-id="e671d-122">Lisaks saavad installimise või müüdud kaupade hooldamisega tegelevad firmad kasu paremast ülevaatest ja kogu müügi ja teenuse protsessi nähtavusesti koos integratsiooniprojektidega.</span><span class="sxs-lookup"><span data-stu-id="e671d-122">In addition, companies installing or servicing sold goods will benefit from better control and visibility to the full sales and service process with integration from projects.</span></span>

### <a name="functionality-includes-integration-of"></a><span data-ttu-id="e671d-123">Funktsionaalsus sisaldab integratsiooni nende vahel:</span><span class="sxs-lookup"><span data-stu-id="e671d-123">Functionality includes integration of:</span></span>
- <span data-ttu-id="e671d-124">Laoteave</span><span class="sxs-lookup"><span data-stu-id="e671d-124">Warehouse information</span></span>
- <span data-ttu-id="e671d-125">Kaubavaru tegelik teave</span><span class="sxs-lookup"><span data-stu-id="e671d-125">On-hand inventory information</span></span>
- <span data-ttu-id="e671d-126">Varude ülekanded</span><span class="sxs-lookup"><span data-stu-id="e671d-126">Inventory transfers</span></span>
- <span data-ttu-id="e671d-127">Varude reguleerimine</span><span class="sxs-lookup"><span data-stu-id="e671d-127">Inventory adjustments</span></span>
- <span data-ttu-id="e671d-128">Töötellimustega seotud Dynamics 365 Field Service rakenduse Supply Chain Management projektid</span><span class="sxs-lookup"><span data-stu-id="e671d-128">Supply Chain Management projects connected with Dynamics 365 Field Service work orders</span></span>
- <span data-ttu-id="e671d-129">Dynamics 365 Field Service’i töökäsud lingiga Supply Chain Managementi projektidele rakendavad selle projekti numbri müügitellimusele, et lubada projektist arveldamine.</span><span class="sxs-lookup"><span data-stu-id="e671d-129">Dynamics 365 Field Service work orders with link to Supply Chain Management projects, apply this project number to the sales order to allow invoicing from the project.</span></span> 

![Äriprotsesside sünkroniseerimine rakenduste Supply Chain Management ja Field Service vahel.](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a><span data-ttu-id="e671d-131">Rakenduste Field Service ja Supply Chain Management integratsiooni teises faasis võimaldatakse sünkroonida järgmisi malle:</span><span class="sxs-lookup"><span data-stu-id="e671d-131">The second phase of the integration between Field Service and Supply Chain Management enables synchronization with the following templates:</span></span>
- <span data-ttu-id="e671d-132">Laod (rakendus Supply Chain Management rakendusele Field Service) – laod rakendusest Supply Chain Management rakendusse Field Service [Täpsem päring]</span><span class="sxs-lookup"><span data-stu-id="e671d-132">Warehouses (Supply Chain Management to Field Service) - Warehouses from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="e671d-133">Tootevarud (rakendus Supply Chain Management rakendusele Field Service) – varude taseme teave rakendusest Supply Chain Management rakendusse Field Service [Täpsem päring]</span><span class="sxs-lookup"><span data-stu-id="e671d-133">Product Inventory (Supply Chain Management to Field Service) - Inventory level information from Supply Chain Management to Field Service [Advanced Query]</span></span> 
- <span data-ttu-id="e671d-134">Lao korrigeerimine (rakendus Field Service rakendusele Supply Chain Management) – lao korrigeerimised rakendusest Field Service rakendusse Supply Chain Management [Täpsem päring]</span><span class="sxs-lookup"><span data-stu-id="e671d-134">Inventory Adjustment (Field Service to Supply Chain Management) - Inventory adjustments from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="e671d-135">Varude ülekanded (rakendus Field Service rakendusele Supply Chain Management) – varude ülekanded rakendusest Field Service rakendusse Supply Chain Management [Täpsem päring]</span><span class="sxs-lookup"><span data-stu-id="e671d-135">Inventory Transfers (Field Service to Supply Chain Management) - Inventory transfers from Field Service to Supply Chain Management [Advanced Query]</span></span> 
- <span data-ttu-id="e671d-136">Projektid (rakendus Supply Chain Management rakendusele Field Service) – projektiloend rakendusest Supply Chain Management rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="e671d-136">Projects (Supply Chain Management to Field Service) - Project list from Supply Chain Management to Field Service</span></span> 
- <span data-ttu-id="e671d-137">Projekti töötellimused (rakendus Field Service rakendusele Supply Chain Management) – töötellimused rakenduses Field Service müügitellimuste kohta rakenduses Supply Chain Management, koos projektitoega [täpsem päring]</span><span class="sxs-lookup"><span data-stu-id="e671d-137">Work Orders with Project (Field Service to Supply Chain Management) - Work orders in Field Service to Sales orders  in Supply Chain Management, with support for Project [Advanced Query]</span></span> 
- <span data-ttu-id="e671d-138">Rakenduse Field Service tooted laoühikuga (Supply Chain Management müügile) – rakenduse Supply Chain Management „Müüdavad väljastatud tooted” müügile „Tooted” rakenduse Field Service jaoks, sh laoühikud</span><span class="sxs-lookup"><span data-stu-id="e671d-138">Field Service Products with Inventory unit (Supply Chain Management to Sales) - Supply Chain Management 'Sellable released products' to Sales 'Products' for Field Service, including Inventory unit</span></span> 

## <a name="system-requirements"></a><span data-ttu-id="e671d-139">Süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="e671d-139">System requirements</span></span>

### <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="e671d-140">Süsteemi nõuded rakendusele Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="e671d-140">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="e671d-141">Rakenduse Field Service integratsioon toetab järgmisi versioone.</span><span class="sxs-lookup"><span data-stu-id="e671d-141">Field Service integration supports the following versions:</span></span>

- <span data-ttu-id="e671d-142">Rakenduse Dynamics 365 for Finance and Operations versioon 8.1.2 (detsember 2018) väljastati detsembris 2018 ja selle järgunumber on 8.1.195 platvormivärskendusega 22 (7.0.5095).</span><span class="sxs-lookup"><span data-stu-id="e671d-142">Dynamics 365 for Finance and Operations version 8.1.2 (December 2018) was released in December 2018 and has an application build number 8.1.195 with Platform update 22 (7.0.5095).</span></span> 

### <a name="system-requirements-for-field-service"></a><span data-ttu-id="e671d-143">Rakenduse Field Service süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="e671d-143">System requirements for Field Service</span></span>
<span data-ttu-id="e671d-144">Rakenduse Field Service integreerimislahenduse kasutamiseks tuleb installida järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="e671d-144">To use the Field Service integration solution, you must install the following components:</span></span>

- <span data-ttu-id="e671d-145">Rakendus Field Service (versioon 8.2.0.286) või uuem rakenduses Dynamics 365 9.1.x – väljastati novembris 2018</span><span class="sxs-lookup"><span data-stu-id="e671d-145">Field Service (version 8.2.0.286) or a later version on Dynamics 365 9.1.x - Released November 2018</span></span>
- <span data-ttu-id="e671d-146">Lahendus Potentsiaalne klient sularahaks (P2C) rakendusele Dynamics 365, versioon 1.15.0.1 või hilisem versioon.</span><span class="sxs-lookup"><span data-stu-id="e671d-146">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="e671d-147">Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="e671d-147">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="e671d-148">Rakenduse Field Service integreerimis-, projekti- ja laoseisulahendus Dynamics 365 jaoks, versioon 2.0.0.0 või hilisem versioon.</span><span class="sxs-lookup"><span data-stu-id="e671d-148">'Field Service Integration, Project and Inventory' solution for Dynamics 365, version 2.0.0.0 or a later version.</span></span> <span data-ttu-id="e671d-149">Lahendus on allalaadimiseks saadaval [AppSource’is](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span><span class="sxs-lookup"><span data-stu-id="e671d-149">The solution is available for download from [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]