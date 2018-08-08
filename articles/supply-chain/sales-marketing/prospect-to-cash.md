---
title: Potentsiaalne klient sularahaks
description: "See teema annab ülevaate lahendusest Potentsiaalne klient sularahaks rakenduste Microsoft Dynamics 365 for Finance and Operations ja Microsoft Dynamics 365 for Sales vahel."
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 801407183ad90f08bde928a1d3da13cba38cfc27
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="76d4c-103">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="76d4c-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76d4c-104">Lahendus Potentsiaalne klient sularahaks võimaldab vahetut sünkroonimist rakenduste Dynamics 365 for Finance and Operations ja Dynamics 365 for Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="76d4c-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="76d4c-105">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Finance, Operations ja Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="76d4c-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="76d4c-106">Andmete edastamise ajal rakenduste Finance and Operations ja Sales vahel saate teha Salesis müügi- ja turundustegevusi ning täita Finance and Operationsis varude halduse abil tellimusi.</span><span class="sxs-lookup"><span data-stu-id="76d4c-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="76d4c-107">Lisateabe saamiseks lahenduse Potentsiaalne klient sularahaks kohta vaadake YouTube’i lühivideot: [![](https://img.youtube.com/vi/AVV9x5x-XCg/0.jpg)](https://www.youtube.com/watch?v=AVV9x5x-XCg)</span><span class="sxs-lookup"><span data-stu-id="76d4c-107">For more information about the Prospect to cash integration, watch the short YouTube video: [![](https://img.youtube.com/vi/AVV9x5x-XCg/0.jpg)](https://www.youtube.com/watch?v=AVV9x5x-XCg)</span></span>


<span data-ttu-id="76d4c-108">Lahenduse Potentsiaalne klient sularahaks praegune versioon pakub vahetu sünkroonimise järgmisi tüüpe.</span><span class="sxs-lookup"><span data-stu-id="76d4c-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="76d4c-109">Kontode haldamine rakenduses Sales ja nende sünkroonimine rakendusest Sales rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="76d4c-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="76d4c-110">Toodete haldamine rakenduses Finance and Operations ja nende vahetu sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="76d4c-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="76d4c-111">Kontaktide haldamine rakenduses Sales ja nende vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="76d4c-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="76d4c-112">Rakenduse Sales müügipakkumise vahetu sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="76d4c-112">Synchronize sales quotation directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="76d4c-113">Müügitellimuste vahetu sünkroonimine rakenduse Finance and Operations ja rakenduse Sales vahel</span><span class="sxs-lookup"><span data-stu-id="76d4c-113">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="76d4c-114">Müügiarve vahetu sünkroonimine rakendusest Finance and Operations rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="76d4c-114">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="76d4c-115">Rakenduse Finance and Operations süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="76d4c-115">System requirements for Finance and Operations</span></span>
<span data-ttu-id="76d4c-116">Lahendust Potentsiaalne klient sularahaks toetatakse järgmistel versioonidel.</span><span class="sxs-lookup"><span data-stu-id="76d4c-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="76d4c-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (detsember 2017)</span><span class="sxs-lookup"><span data-stu-id="76d4c-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="76d4c-118">Dynamics 365 for Finance and Operations, Enterprise Edition (detsember 2017) – rakenduse järk 7.3.11971.56116 platvormivärskendusega 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="76d4c-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="76d4c-119">Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017)</span><span class="sxs-lookup"><span data-stu-id="76d4c-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="76d4c-120">Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017) – platvormivärskendusega 8 (rakenduse järk 7.2.11792.56024 platvormi järguga 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="76d4c-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="76d4c-121">Nõutavad on järgmised kiirparandused.</span><span class="sxs-lookup"><span data-stu-id="76d4c-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="76d4c-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Sales rakendusse Finance and Operations andmete integratsiooni funktsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="76d4c-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="76d4c-123">See pakub ka mitmesuguseid muid täiustusi.</span><span class="sxs-lookup"><span data-stu-id="76d4c-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="76d4c-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – see kiirparandus võimaldab müügitellimuse rea sünkroonimist rakendusest Finance and Operations rakendusse Sales andmete integratsiooni funktsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="76d4c-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="76d4c-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – see kiirparandus võimaldab müügitellimuse sünkroonimist rakendusest Finance and Operations rakendusse Sales andmete integratsiooni funktsiooni kaudu.</span><span class="sxs-lookup"><span data-stu-id="76d4c-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="76d4c-126">KB4045570 tuleb installida ainult sellepärast, et installifail sisaldab muudatusi muudest kiirparandustest.</span><span class="sxs-lookup"><span data-stu-id="76d4c-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="76d4c-127">Rakenduse Dynamics 365 for Finance and Operations versioon 1611 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="76d4c-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="76d4c-128">Rakenduse Dynamics 365 for Finance and Operations versioon 1611 (november 2016) platvormivärskendusega 8 või uuemaga</span><span class="sxs-lookup"><span data-stu-id="76d4c-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="76d4c-129">Nõutavad on järgmised kiirparandused.</span><span class="sxs-lookup"><span data-stu-id="76d4c-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="76d4c-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** – müügitellimuse sünkroonimine andmete integraatori abil rakendusest Finance and Operations rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="76d4c-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
  - <span data-ttu-id="76d4c-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** – müügitellimuse päise ja ridade sünkroonimine andmete integraatori abil rakendusest Finance and Operations rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="76d4c-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
  - <span data-ttu-id="76d4c-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** – vajalik on tugi lahenduse Potentsiaalne klient sularahaks integreerimiseks andmeüksuste kaudu.</span><span class="sxs-lookup"><span data-stu-id="76d4c-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="76d4c-133">Pärast kiirparanduste installimist peate vormilt **SalesPopulateProspectToCash** käivitama järgmise pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="76d4c-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="76d4c-134">See vorm on peidetud, kuna teil on seda vaja ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="76d4c-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="76d4c-135">Vormile juurdepääsu saamiseks logige keskkonda sisse ja lisage oma brauseri aadressile järgmine URL: *&mi=action:SalesPopulateProspectToCash*, näiteks `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="76d4c-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="76d4c-136">Vormi avanemisel klõpsake OK.</span><span class="sxs-lookup"><span data-stu-id="76d4c-136">When the form opens, click OK.</span></span> <span data-ttu-id="76d4c-137">See täidab tabelites **SalesLine**, **SalesQuotationLine** ja **CustInvoiceTrans** uue välja **LineCreationSequnceNumber** kordumatute väärtustega ja värskendab tooteloendit.</span><span class="sxs-lookup"><span data-stu-id="76d4c-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="76d4c-138">See on vajalik lahenduse Potentsiaalne klient sularahaks integratsiooni toimimiseks.</span><span class="sxs-lookup"><span data-stu-id="76d4c-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="76d4c-139">Rakenduse Sales süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="76d4c-139">System requirements for Sales</span></span>

<span data-ttu-id="76d4c-140">Lahenduse Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmised komponendid.</span><span class="sxs-lookup"><span data-stu-id="76d4c-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="76d4c-141">Rakenduse Dynamics 365 for Sales versiooni 1612 (8.2.1.207) (DB 8.2.1.207) veebiversioon või hilisem versioon</span><span class="sxs-lookup"><span data-stu-id="76d4c-141">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="76d4c-142">Lahendus Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales, versioon 1.15.0.0 või hilisem.</span><span class="sxs-lookup"><span data-stu-id="76d4c-142">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="76d4c-143">Lahendus on allalaadimiseks saadaval AppSource’is.</span><span class="sxs-lookup"><span data-stu-id="76d4c-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="76d4c-144">[Lahenduse Dynamics 365, Potentsiaalne klient sularahaks allalaadimine](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="76d4c-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>

