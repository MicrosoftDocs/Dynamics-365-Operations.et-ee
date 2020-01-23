---
title: Hankija kujunduste vaheldumisi aktiveerimine
description: Selles teemas kirjeldatakse, kuidas lülitada hankija andmete integreerimise vahel Finance and Operationsi rakenduste ja teenuse Common Data Service vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902721"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="2eec3-103">Hankija kujunduste vaheldumisi aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="2eec3-103">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="2eec3-104">Hankijaandmete voog</span><span class="sxs-lookup"><span data-stu-id="2eec3-104">Vendor data flow</span></span> 

<span data-ttu-id="2eec3-105">Kui kasutate hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite isoleerida hankijateabe klientidest, kasutage seda üldist hankijalahendust.</span><span class="sxs-lookup"><span data-stu-id="2eec3-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Hankija üldine voog](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="2eec3-107">Kui kasutate hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite hankijaandmete salvestamiseks jätkata olemi **Konto** kasutamist, kasutage seda laiendatud hankijalahendust.</span><span class="sxs-lookup"><span data-stu-id="2eec3-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="2eec3-108">Selles lahenduses salvestatakse laiendatud hankijateave, nagu hankija ootelolek ja hankijaprofiil, üksusesse **hankijad** Common Data Service’is.</span><span class="sxs-lookup"><span data-stu-id="2eec3-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Hankija laiendatud voog](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="2eec3-110">Hankija laiendatud voo kasutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2eec3-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="2eec3-111">Lahendusepakett **SupplyChainCommon** sisaldab töövooprotsessi malle, nagu on näha alloleval pildil.</span><span class="sxs-lookup"><span data-stu-id="2eec3-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="2eec3-112">![Töövooprotsessi mallid](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="2eec3-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="2eec3-113">Looge uued töövooprotsessid, kasutades töövooprotsessi malle.</span><span class="sxs-lookup"><span data-stu-id="2eec3-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="2eec3-114">Looge uus töövooprotsess üksusele **Hankija**, kasutades töövooprotsessi malli **Hankijate loomine konto üksuses**, ja klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="2eec3-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="2eec3-115">See töövoog käsitseb üksuse **Konto** hankija loomise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="2eec3-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="2eec3-116">![Hankijate loomine konto üksuses](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="2eec3-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="2eec3-117">Looge uus töövooprotsess üksusele **Hankija**, kasutades töövooprotsessi malli **Kontode üksuse värskendamine**, ja klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="2eec3-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="2eec3-118">See töövoog käsitseb üksuse **Konto** hankija värskendamise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="2eec3-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="2eec3-119">![Kontode üksuse värskendamine](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="2eec3-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="2eec3-120">Looge uued töövooprotsessid mallidest, mis on loodud üksuses **Kontod**.</span><span class="sxs-lookup"><span data-stu-id="2eec3-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="2eec3-121">![Hankijate loomine hankijate üksuses](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="2eec3-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="2eec3-122">![Hankijate üksuse värskendamine](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="2eec3-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="2eec3-123">Saate konfigureerida töövoogusid reaalajas või taustatöövoogudena, olenevalt teie nõuetest.</span><span class="sxs-lookup"><span data-stu-id="2eec3-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="2eec3-124">![Teisendamine taustatöövooks](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="2eec3-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="2eec3-125">Aktiveerige töövood, mille lõite üksustes **Konto** ja **Hankija**, et hakata kasutama hankijateabe salvestamiseks üksust **Konto**.</span><span class="sxs-lookup"><span data-stu-id="2eec3-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
