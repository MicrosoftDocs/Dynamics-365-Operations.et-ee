---
title: Potentsiaalne klient sularahaks
description: Selles teemas antakse ülevaade lahendusest Prospect to cash rakenduste Dynamics 365 Supply Chain Management ja Dynamics 365 Sales vahel.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: fb5abb983811ce736e3494bc85e8d9b23a2e373c
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814071"
---
# <a name="prospect-to-cash"></a><span data-ttu-id="8fe5a-103">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="8fe5a-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fe5a-104">Lahendus Prospect to cash võimaldab otsest sünkroonimist rakenduste Dynamics 365 Supply Chain Management ja Dynamics 365 Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="8fe5a-105">Andmete integratsiooniga saadaolevad lahenduse Prospect to cash mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices.</span></span> <span data-ttu-id="8fe5a-106">Andmete edastamise ajal saate teha Salesis müügi- ja turundustegevusi ning täita Supply Chain Managementis varude halduse abil tellimusi.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-106">While data is flowing, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Supply Chain Management.</span></span> 

<span data-ttu-id="8fe5a-107">Lisateabe saamiseks lahenduse Potentsiaalne klient sularahaks kohta vaadake YouTube’i lühivideot: [Lahenduse Potentsiaalne klient sularahaks integreerimine](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span><span class="sxs-lookup"><span data-stu-id="8fe5a-107">For more information about the Prospect to cash integration, watch the short YouTube video [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span></span>

<span data-ttu-id="8fe5a-108">Lahenduse Potentsiaalne klient sularahaks praegune versioon pakub vahetu sünkroonimise järgmisi tüüpe.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="8fe5a-109">Rakenduse Sales kontode sünkroonimine otse rakenduse Supply Chain Management klientidega</span><span class="sxs-lookup"><span data-stu-id="8fe5a-109">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="8fe5a-110">Rakenduse Supply Chain Management toodete sünkroonimine otse rakenduse Sales toodetega</span><span class="sxs-lookup"><span data-stu-id="8fe5a-110">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="8fe5a-111">Rakenduse Sales kontaktide sünkroonimine otse rakenduse Supply Chain Management kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="8fe5a-111">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="8fe5a-112">Rakenduse Supply Chain Management müügiarvete päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="8fe5a-112">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="8fe5a-113">Müügitellimuste vahetu sünkroonimine rakenduse Sales ja rakenduse Supply Chain Management vahel</span><span class="sxs-lookup"><span data-stu-id="8fe5a-113">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="8fe5a-114">Rakenduse Supply Chain Management arve päiste ja ridade sünkroonimine otse rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="8fe5a-114">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="8fe5a-115">Süsteemi nõuded rakendusele Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="8fe5a-115">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="8fe5a-116">Lahendust Potentsiaalne klient sularahaks toetatakse järgmistel versioonidel.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="8fe5a-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (detsember 2017)</span><span class="sxs-lookup"><span data-stu-id="8fe5a-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="8fe5a-118">Dynamics 365 for Finance and Operations, Enterprise Edition (detsember 2017) – rakenduse järk 7.3.11971.56116 platvormivärskendusega 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="8fe5a-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="8fe5a-119">Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017)</span><span class="sxs-lookup"><span data-stu-id="8fe5a-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="8fe5a-120">Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017) – platvormivärskendusega 8 (rakenduse järk 7.2.11792.56024 platvormijärguga 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="8fe5a-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="8fe5a-121">Nõutavad on järgmised kiirparandused.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="8fe5a-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Sales rakendusse Supply Chain Management andmete integratsiooni funktsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Supply Chain Management via the Data Integration feature.</span></span> <span data-ttu-id="8fe5a-123">See pakub ka mitmesuguseid muid täiustusi.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="8fe5a-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Supply Chain Management rakendusse Sales andmete integratsiooni funktsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="8fe5a-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Supply Chain Management rakendusse Sales andmete integratsiooni funktsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8fe5a-126">KB4045570 tuleb installida ainult sellepärast, et installifail sisaldab muudatusi muudest kiirparandustest.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="8fe5a-127">Rakenduse Dynamics 365 for Finance and Operations versioon 1611 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="8fe5a-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="8fe5a-128">Rakenduse Dynamics 365 for Finance and Operations versioon 1611 (november 2016) platvormivärskendusega 8 või uuem</span><span class="sxs-lookup"><span data-stu-id="8fe5a-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="8fe5a-129">Nõutavad on järgmised kiirparandused.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="8fe5a-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – müügitellimuse sünkroonimine andmete integraatori abil rakendusest Supply Chain Management rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Supply Chain Management to Sales.</span></span> 
  - <span data-ttu-id="8fe5a-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – müügitellimuse sünkroonimine andmete integraatori abil rakendusest Supply Chain Management rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Supply Chain Management to Sales.</span></span>
  - <span data-ttu-id="8fe5a-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – vajalik on tugi lahenduse Potentsiaalne klient sularahaks integreerimiseks andmeüksuste kaudu.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="8fe5a-133">Pärast kiirparanduste installimist peate vormilt **SalesPopulateProspectToCash** käivitama järgmise pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="8fe5a-134">See vorm on peidetud, kuna teil on seda vaja ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="8fe5a-135">Vormile juurdepääsu saamiseks logige keskkonda sisse ja lisage oma brauseri aadressile järgmine URL: *&mi=action:SalesPopulateProspectToCash*, näiteks `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="8fe5a-136">Vormi avanemisel klõpsake OK.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-136">When the form opens, click OK.</span></span> <span data-ttu-id="8fe5a-137">See täidab tabelites **SalesLine**, **SalesQuotationLine** ja **CustInvoiceTrans** uue välja **LineCreationSequnceNumber** kordumatute väärtustega ja värskendab tooteloendit.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="8fe5a-138">See on vajalik lahenduse Potentsiaalne klient sularahaks integratsiooni toimimiseks.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="8fe5a-139">Rakenduse Sales süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="8fe5a-139">System requirements for Sales</span></span>

<span data-ttu-id="8fe5a-140">Lahenduse Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="8fe5a-141">Rakenduse Dynamics 365 Sales versiooni 1612 (8.2.1.207) (DB 8.2.1.207) veebiversioon või hilisem versioon</span><span class="sxs-lookup"><span data-stu-id="8fe5a-141">Dynamics 365 Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="8fe5a-142">Lahendus Prospect to cash (P2C) rakendusele Dynamics 365, versioon 1.15.0.0 või hilisem versioon.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-142">Prospect to cash solution for Dynamics 365 Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="8fe5a-143">Lahendus on allalaadimiseks saadaval AppSource’is.</span><span class="sxs-lookup"><span data-stu-id="8fe5a-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="8fe5a-144">[Lahenduse Dynamics 365, Potentsiaalne klient sularahaks allalaadimine](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="8fe5a-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
