---
title: Hankija kujunduste vaheldumisi aktiveerimine
description: Selles teemas kirjeldatakse, kuidas lülitada hankija andmete integreerimist teenusekomplekti Finance and Operations rakenduste ja teenuse Common Data Service vahel.
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
ms.openlocfilehash: 587a9b98f28b11e303aff4b59e9726f220d956eb
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019733"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="6cf10-103">Hankija kujunduste vaheldumisi aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="6cf10-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="6cf10-104">Hankijaandmete voog</span><span class="sxs-lookup"><span data-stu-id="6cf10-104">Vendor data flow</span></span> 

<span data-ttu-id="6cf10-105">Kui kasutate hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite isoleerida hankijateabe klientidest, kasutage seda üldist hankijalahendust.</span><span class="sxs-lookup"><span data-stu-id="6cf10-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Hankija üldine voog](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="6cf10-107">Kui kasutate hankija koondandmete jaoks teisi Dynamics 365 rakendusi ja soovite hankijaandmete salvestamiseks jätkata olemi **Konto** kasutamist, kasutage seda laiendatud hankijalahendust.</span><span class="sxs-lookup"><span data-stu-id="6cf10-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="6cf10-108">Selles lahenduses salvestatakse laiendatud hankijateave, nagu hankija ootelolek ja hankijaprofiil, üksusesse **hankijad** Common Data Service’is.</span><span class="sxs-lookup"><span data-stu-id="6cf10-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Hankija laiendatud voog](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="6cf10-110">Hankija laiendatud voo kasutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6cf10-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="6cf10-111">Lahendusepakett **SupplyChainCommon** sisaldab töövooprotsessi malle, nagu on näha alloleval pildil.</span><span class="sxs-lookup"><span data-stu-id="6cf10-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="6cf10-112">![Töövooprotsessi mallid](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="6cf10-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="6cf10-113">Looge uued töövooprotsessid, kasutades töövooprotsessi malle.</span><span class="sxs-lookup"><span data-stu-id="6cf10-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="6cf10-114">Looge uus töövooprotsess üksusele **Hankija**, kasutades töövooprotsessi malli **Hankijate loomine konto üksuses**, ja klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cf10-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="6cf10-115">See töövoog käsitseb üksuse **Konto** hankija loomise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="6cf10-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="6cf10-116">![Hankijate loomine konto üksuses](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="6cf10-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="6cf10-117">Looge uus töövooprotsess üksusele **Hankija**, kasutades töövooprotsessi malli **Kontode üksuse värskendamine**, ja klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cf10-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="6cf10-118">See töövoog käsitseb üksuse **Konto** hankija värskendamise stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="6cf10-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="6cf10-119">![Kontode üksuse värskendamine](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="6cf10-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="6cf10-120">Looge uued töövooprotsessid mallidest, mis on loodud üksuses **Kontod**.</span><span class="sxs-lookup"><span data-stu-id="6cf10-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="6cf10-121">![Hankijate loomine hankijate üksuses](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="6cf10-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="6cf10-122">![Hankijate üksuse värskendamine](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="6cf10-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="6cf10-123">Saate konfigureerida töövoogusid reaalajas või taustatöövoogudena, olenevalt teie nõuetest.</span><span class="sxs-lookup"><span data-stu-id="6cf10-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="6cf10-124">![Teisendamine taustatöövooks](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="6cf10-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="6cf10-125">Aktiveerige töövood, mille lõite üksustes **Konto** ja **Hankija**, et hakata kasutama hankijateabe salvestamiseks üksust **Konto**.</span><span class="sxs-lookup"><span data-stu-id="6cf10-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
