---
title: Potentsiaalne klient sularahaks
description: "See teema annab ülevaate lahendusest Potentsiaalne klient sularahaks rakenduste Dynamics 365 for Finance and Operations, Enterprise edition, ja Dynamics 365 for Sales vahel."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: et-ee
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="b42e1-103">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="b42e1-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b42e1-104">Lahendus Potentsiaalne klient sularahaks kasutab [andmete integratsiooni](/common-data-service/entity-reference/dynamics-365-integration), et sünkroonida andmeid rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, ja Dynamics 365 for Sales eksemplarides teenuse Common Data Service (CDS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="b42e1-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="b42e1-105">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Dynamics 365 for Finance ja Operations and Dynamics 365 for Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="b42e1-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="b42e1-106">Andmete edastamise ajal rakenduste Finance and Operations ja Sales vahel saate teha Salesis müügi- ja turundustegevusi ning täita Finance and Operationsis varude halduse abil tellimusi.</span><span class="sxs-lookup"><span data-stu-id="b42e1-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="b42e1-107">See lahendus võimaldab integratsiooni järgmistes valdkondades.</span><span class="sxs-lookup"><span data-stu-id="b42e1-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="b42e1-108">Kontode haldamine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b42e1-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="b42e1-109">Kontaktide haldamine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b42e1-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="b42e1-110">Toodete haldamine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="b42e1-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="b42e1-111">Müügipakkumiste loomine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b42e1-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="b42e1-112">Müügitellimuste loomine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="b42e1-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="b42e1-113">Müügiarvete loomine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="b42e1-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

<span data-ttu-id="b42e1-114">See lahendus võimaldab vahetut sünkroonimist järgmistes valdkondades.</span><span class="sxs-lookup"><span data-stu-id="b42e1-114">This solution provides direct synchronization in the following areas:</span></span>

-   [<span data-ttu-id="b42e1-115">Kontode haldamine rakenduses Sales ja nende sünkroonimine rakendusest Sales rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b42e1-115">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
-   [<span data-ttu-id="b42e1-116">Toodete haldamine rakenduses Finance and Operations ja nende vahetu sünkroonimine rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="b42e1-116">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
-   [<span data-ttu-id="b42e1-117">Kontaktid haldamine rakenduses Sales ja vahetu sünkroonimine rakenduse Finance and Operations kontaktide või klientidega</span><span class="sxs-lookup"><span data-stu-id="b42e1-117">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
-   [<span data-ttu-id="b42e1-118">Rakenduse Sales müügipakkumise päiste ja ridade vahetu sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b42e1-118">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping-sales-fin.md)
-   [<span data-ttu-id="b42e1-119">Müügitellimuste loomine rakenduses Finance and Operations ja nende vahetu sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="b42e1-119">Create sales orders in Finance and Operations and sync them directly to Sales</span></span>](sales-order-template-mapping-direct.md)
-  [<span data-ttu-id="b42e1-120">Müügitellimuse päiste ja ridade vahetu sünkroonimine rakenduste Sales ja Finance and Operations vahel</span><span class="sxs-lookup"><span data-stu-id="b42e1-120">Synchronize sales order headers and lines directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-between-sales-fin.md)
-   [<span data-ttu-id="b42e1-121">Müügitellimuste vahetu sünkroonimine rakenduste Sales ja Finance and Operations vahel</span><span class="sxs-lookup"><span data-stu-id="b42e1-121">Synchronize sales orders directly between Sales and Finance and Operations</span></span>](sales-order-template-mapping-direct-two-ways.md)
-   [<span data-ttu-id="b42e1-122">Müügiarvete loomine rakenduses Finance and Operations ja nende vahetu sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="b42e1-122">Create sales invoices in Finance and Operations and sync them directly to Sales</span></span>](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="b42e1-123">Dynamics 365 for Finance and Operations, Enterprise Editioni süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="b42e1-123">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="b42e1-124">Lahenduse Lahendus Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmine.</span><span class="sxs-lookup"><span data-stu-id="b42e1-124">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="b42e1-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juuli 2017) platvormivärskendusega 8 (rakendus 7.2.11792.56024 platvormiga 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="b42e1-125">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="b42e1-126">Kiirparandused rakendusele Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017).</span><span class="sxs-lookup"><span data-stu-id="b42e1-126">Hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>
        
    -  <span data-ttu-id="b42e1-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160): see kiirparandus lubab andmete integreerimise funktsiooniga müügitellimuste sünkroonimise rakendusest Sales rakendusse Finance and Operations ning hõlmab ka mitmesuguseid muid täiustusi.</span><span class="sxs-lookup"><span data-stu-id="b42e1-127">[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - This hotfix enabels support for sales order synchronization with the Data Integration feature from Sales to Finance and Operations, along with a number of other enhancements.</span></span>

    -  <span data-ttu-id="b42e1-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – see kiirparandus võimaldab müügitellimuse rea sünkroonimist andmete integratsiooni funktsiooniga rakendusest Finance and Operations rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="b42e1-128">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="b42e1-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – see kiirparandus võimaldab müügitellimuse sünkroonimist andmete integratsiooni funktsiooniga rakendusest Finance and Operations rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="b42e1-129">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>

<span data-ttu-id="b42e1-130">**Märkus**. KB4045570 tuleb installida ainult sellepärast, et installifail sisaldab muudatusi muudest KB-dest.</span><span class="sxs-lookup"><span data-stu-id="b42e1-130">**Note**: You only need to install KB4045570 because the installation includes the changes from the other KB's.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="b42e1-131">Rakenduse Dynamics 365 for Sales süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="b42e1-131">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="b42e1-132">Lahenduse Lahendus Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmine.</span><span class="sxs-lookup"><span data-stu-id="b42e1-132">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="b42e1-133">Rakenduse Dynamics 365 for Sales versiooni 1612 (8.2.1.207) (DB 8.2.1.207) veebiversioon.</span><span class="sxs-lookup"><span data-stu-id="b42e1-133">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online.</span></span>
- <span data-ttu-id="b42e1-134">Lahendus Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales, versioon 1.14.0.0 (v14) või hilisem.</span><span class="sxs-lookup"><span data-stu-id="b42e1-134">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b42e1-135">Installige lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="b42e1-135">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="b42e1-136">Laadige alla [lahenduse Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales paketi ZIP-fail](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSource’ist.</span><span class="sxs-lookup"><span data-stu-id="b42e1-136">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="b42e1-137">Veenduge, et ZIP-fail poleks blokeeritud, et te ei saaks lahendusepaketi installimisel tõrketeadet „Impordipakette ei leitud”.</span><span class="sxs-lookup"><span data-stu-id="b42e1-137">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="b42e1-138">Faili blokeeringu tühistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b42e1-138">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="b42e1-139">Paremklõpsake ZIP-faili.</span><span class="sxs-lookup"><span data-stu-id="b42e1-139">Right-click the zip file.</span></span>
    -  <span data-ttu-id="b42e1-140">Valige **Atribuudid** ja seejärel valige **Tühista blokeering**.</span><span class="sxs-lookup"><span data-stu-id="b42e1-140">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="b42e1-141">Pakkige lahti PackageDeployer.exe ja käivitage see.</span><span class="sxs-lookup"><span data-stu-id="b42e1-141">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="b42e1-142">Installige lahendus Potentsiaalne klient sularahaks oma rakenduse Sales eksemplari.</span><span class="sxs-lookup"><span data-stu-id="b42e1-142">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="b42e1-143">Valige juurutuse tüüp **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="b42e1-143">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="b42e1-144">Valige **Kuva täpsem**.</span><span class="sxs-lookup"><span data-stu-id="b42e1-144">Select **Show advanced**.</span></span>
    - <span data-ttu-id="b42e1-145">Kiirinstallimiseks valige **Regioon**.</span><span class="sxs-lookup"><span data-stu-id="b42e1-145">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="b42e1-146">Kui valite **Ei tea**, otsib süsteem kõiki regioone ja installimine võtab kauem aega.</span><span class="sxs-lookup"><span data-stu-id="b42e1-146">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="b42e1-147">Sisestage installimise kasutajaõigustega administraatorist kasutaja **Kasutajanimi** ja **Parool**.</span><span class="sxs-lookup"><span data-stu-id="b42e1-147">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

