---
title: Potentsiaalne klient sularahaks
description: "See teema annab ülevaate lahendusest Potentsiaalne klient sularahaks rakenduste Dynamics 365 for Finance and Operations, Enterprise edition, ja Dynamics 365 for Sales vahel."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="4e51c-103">Potentsiaalne klient sularahaks</span><span class="sxs-lookup"><span data-stu-id="4e51c-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4e51c-104">Lahendus Potentsiaalne klient sularahaks kasutab [andmete integratsiooni](/common-data-service/entity-reference/dynamics-365-integration), et sünkroonida andmeid rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, ja Dynamics 365 for Sales eksemplarides teenuse Common Data Service (CDS) kaudu.</span><span class="sxs-lookup"><span data-stu-id="4e51c-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="4e51c-105">Andmete integratsiooniga saadaolevad lahenduse Potentsiaalne klient sularahaks mallid võimaldavad kontode, kontaktide, toodete, müügipakkumiste, müügitellimuste ja müügiarvete andmete liikumist rakenduste Dynamics 365 for Finance ja Operations and Dynamics 365 for Sales vahel.</span><span class="sxs-lookup"><span data-stu-id="4e51c-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="4e51c-106">Andmete edastamise ajal rakenduste Finance and Operations ja Sales vahel saate teha Salesis müügi- ja turundustegevusi ning täita Finance and Operationsis varude halduse abil tellimusi.</span><span class="sxs-lookup"><span data-stu-id="4e51c-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="4e51c-107">See lahendus võimaldab integratsiooni järgmistes valdkondades.</span><span class="sxs-lookup"><span data-stu-id="4e51c-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="4e51c-108">Kontode haldamine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4e51c-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="4e51c-109">Kontaktide haldamine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="4e51c-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="4e51c-110">Toodete haldamine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales.</span><span class="sxs-lookup"><span data-stu-id="4e51c-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="4e51c-111">Müügipakkumiste loomine rakenduses Sales ja nende sünkroonimine rakendusega Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4e51c-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="4e51c-112">Müügitellimuste loomine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="4e51c-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="4e51c-113">Müügiarvete loomine rakenduses Finance and Operations ja nende sünkroonimine rakendusega Sales</span><span class="sxs-lookup"><span data-stu-id="4e51c-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="4e51c-114">Dynamics 365 for Finance and Operations, Enterprise Editioni süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="4e51c-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="4e51c-115">Lahenduse Lahendus Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmine.</span><span class="sxs-lookup"><span data-stu-id="4e51c-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="4e51c-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juuli 2017) platvormivärskendusega 8 (rakendus 7.2.11792.56024 platvormiga 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="4e51c-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="4e51c-117">Kaks kiirparandust rakendusele Dynamics 365 for Finance and Operations, Enterprise Edition (juuli 2017).</span><span class="sxs-lookup"><span data-stu-id="4e51c-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="4e51c-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – see kiirparandus võimaldab müügitellimuse rea sünkroonimist andmete integratsiooni funktsiooniga rakendusest Finance and Operations rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="4e51c-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="4e51c-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) – see kiirparandus võimaldab müügitellimuse sünkroonimist andmete integratsiooni funktsiooniga rakendusest Finance and Operations rakendusse Sales.</span><span class="sxs-lookup"><span data-stu-id="4e51c-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="4e51c-120">**Märkus**. KB4036524 tuleb installida ainult sellepärast, et installifail sisaldab muudatusi versioonist KB4036461.</span><span class="sxs-lookup"><span data-stu-id="4e51c-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="4e51c-121">Rakenduse Dynamics 365 for Sales süsteeminõuded</span><span class="sxs-lookup"><span data-stu-id="4e51c-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="4e51c-122">Lahenduse Lahendus Potentsiaalne klient sularahaks kasutamiseks tuleb installida järgmine.</span><span class="sxs-lookup"><span data-stu-id="4e51c-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="4e51c-123">Rakenduse Dynamics 365 for Sales versiooni 1612 (8.2.1.207) (DB 8.2.1.207) veebiversioon või hilisem.</span><span class="sxs-lookup"><span data-stu-id="4e51c-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="4e51c-124">Lahendus Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales, versioon 1.14.0.0 (v14) või hilisem.</span><span class="sxs-lookup"><span data-stu-id="4e51c-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="4e51c-125">Installige lahendus Potentsiaalne klient sularahaks rakendusele Sales</span><span class="sxs-lookup"><span data-stu-id="4e51c-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="4e51c-126">Laadige alla [lahenduse Potentsiaalne klient sularahaks rakendusele Dynamics 365 for Sales paketi ZIP-fail](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) CustomerSource’ist.</span><span class="sxs-lookup"><span data-stu-id="4e51c-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="4e51c-127">Veenduge, et ZIP-fail poleks blokeeritud, et te ei saaks lahendusepaketi installimisel tõrketeadet „Impordipakette ei leitud”.</span><span class="sxs-lookup"><span data-stu-id="4e51c-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="4e51c-128">Faili blokeeringu tühistamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="4e51c-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="4e51c-129">Paremklõpsake ZIP-faili.</span><span class="sxs-lookup"><span data-stu-id="4e51c-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="4e51c-130">Valige **Atribuudid** ja seejärel valige **Tühista blokeering**.</span><span class="sxs-lookup"><span data-stu-id="4e51c-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="4e51c-131">Pakkige lahti PackageDeployer.exe ja käivitage see.</span><span class="sxs-lookup"><span data-stu-id="4e51c-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="4e51c-132">Installige lahendus Potentsiaalne klient sularahaks oma rakenduse Sales eksemplari.</span><span class="sxs-lookup"><span data-stu-id="4e51c-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="4e51c-133">Valige juurutuse tüüp **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="4e51c-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="4e51c-134">Valige **Kuva täpsem**.</span><span class="sxs-lookup"><span data-stu-id="4e51c-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="4e51c-135">Kiirinstallimiseks valige **Regioon**.</span><span class="sxs-lookup"><span data-stu-id="4e51c-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="4e51c-136">Kui valite **Ei tea**, otsib süsteem kõiki regioone ja installimine võtab kauem aega.</span><span class="sxs-lookup"><span data-stu-id="4e51c-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="4e51c-137">Sisestage installimise kasutajaõigustega administraatorist kasutaja **Kasutajanimi** ja **Parool**.</span><span class="sxs-lookup"><span data-stu-id="4e51c-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

