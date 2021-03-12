---
title: Kauba või toormaterjali jälgimine
description: See protseduur näitab, kuidas kasutada kauba jälgimist tuvastamiseks, kus kaupu või toormaterjale on kasutatud või kasutatakse.
author: pjacobse
manager: tfehr
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 044b098b24d8cdf8008824b7ed1359f2b0566a8f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961483"
---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="8372a-103">Kauba või toormaterjali jälgimine</span><span class="sxs-lookup"><span data-stu-id="8372a-103">Trace an item or raw material</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8372a-104">See protseduur näitab, kuidas kasutada kauba jälgimist tuvastamiseks, kus kaupu või toormaterjale on kasutatud või kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="8372a-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="8372a-105">Selle protseduuri abil saate kauba tuvastada, liikuda tagasi selle allika juurde ja seejärel edasi läbi tootmise ja valmis toote müügi.</span><span class="sxs-lookup"><span data-stu-id="8372a-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="8372a-106">Seda protsessi saab kasutada sellest mõjutatud klientide, müügitellimuste ja muu uurimiseks.</span><span class="sxs-lookup"><span data-stu-id="8372a-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="8372a-107">Protseduur kasutab demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="8372a-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="8372a-108">Kauba jälgimine tagasisuunas, kasutades teadaolevat partiinumbrit</span><span class="sxs-lookup"><span data-stu-id="8372a-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="8372a-109">Avage **Navigeerimispaneelil** **Moodulid > Varuhaldus > Päringud ja aruanded > Jälgimisdimensioonid > Kauba jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="8372a-109">In the **Navigation pane**, go to **Modules > Inventory management > Inquiries and reports > Tracking dimensions > Item tracing**.</span></span>
2. <span data-ttu-id="8372a-110">Tehke väljal **Kaubanumber** valik P9100.</span><span class="sxs-lookup"><span data-stu-id="8372a-110">In the **Item number** field, select 'P9100'.</span></span>
3. <span data-ttu-id="8372a-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8372a-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8372a-112">Tehke väljal **Edasi või tagasi** valik Tagasi.</span><span class="sxs-lookup"><span data-stu-id="8372a-112">In the **Forward or backward** field, select 'Backward'.</span></span>
5. <span data-ttu-id="8372a-113">Tehke väljal **Partiinumber** valik 12-344-01.</span><span class="sxs-lookup"><span data-stu-id="8372a-113">In the **Batch number** field, select 'as-12-344-01'.</span></span>
6. <span data-ttu-id="8372a-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8372a-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8372a-115">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="8372a-115">Click **OK**.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="8372a-116">Kauba tuvastamine, selle jälgimine edasisuunas ja analüüsimine</span><span class="sxs-lookup"><span data-stu-id="8372a-116">Identify an item, trace it forward, and make an analysis</span></span>

<span data-ttu-id="8372a-117">Puu ülemine sõlm kajastab valitud kauba ja partii laos olevat kogust.</span><span class="sxs-lookup"><span data-stu-id="8372a-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="8372a-118">Peate laiendama puu sõlmesid, et leida kaup, mille puhul tuleb edastamise jälgimine käivitada.</span><span class="sxs-lookup"><span data-stu-id="8372a-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="8372a-119">Laiendage puus allpool kirjeldatud sõlmesid ja valige sejärel viimane sõlm.</span><span class="sxs-lookup"><span data-stu-id="8372a-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    
    <span data-ttu-id="8372a-120">Laiendage valikuid: P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101 ja valige seejärel see sõlm.</span><span class="sxs-lookup"><span data-stu-id="8372a-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="8372a-121">Laiendage puus allpool kirjeldatud sõlme ja seejärel valige see sõlm.</span><span class="sxs-lookup"><span data-stu-id="8372a-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    
    <span data-ttu-id="8372a-122">Alustades äsja valitud sõlmest, laiendage valikuid M9103 ● Production line B-000050 ● 09.12.2015  ● -160,00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01 ja valige seejärel see sõlm.</span><span class="sxs-lookup"><span data-stu-id="8372a-122">Starting from the node that you've just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="8372a-123">Klõpsake valikut **Jälgi sõlmest**.</span><span class="sxs-lookup"><span data-stu-id="8372a-123">Click **Trace from node**.</span></span>
4. <span data-ttu-id="8372a-124">Klõpsake nuppu **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="8372a-124">Click **Forward**.</span></span>
5. <span data-ttu-id="8372a-125">Klõpsake **Tegumiribal** valikut **Jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="8372a-125">On the **Action Pane**, click **Tracing**.</span></span>
    
    <span data-ttu-id="8372a-126">On mitu jälgimise suvandit, mis annavad teavet jälgitava kauba mõjutatud klientide kohta ning saadetud ja saatmata kaubaga seotud müügitellimuste kohta.</span><span class="sxs-lookup"><span data-stu-id="8372a-126">There are several tracing options which provide information about the customers impacted by the item that you're tracing, and the sales orders related to the item which have and haven't been shipped.</span></span>   
6. <span data-ttu-id="8372a-127">Klõpsake **Kliendid**.</span><span class="sxs-lookup"><span data-stu-id="8372a-127">Click **Customers**.</span></span>
7. <span data-ttu-id="8372a-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8372a-128">Close the page.</span></span>
8. <span data-ttu-id="8372a-129">Klõpsake **Tegumiribal** valikut **Jälgimine**.</span><span class="sxs-lookup"><span data-stu-id="8372a-129">On the **Action Pane**, click **Tracing**.</span></span>
9. <span data-ttu-id="8372a-130">Klõpsake nuppu **Saadetud müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="8372a-130">Click **Shipped sales orders**.</span></span>
10. <span data-ttu-id="8372a-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8372a-131">Close the page.</span></span>

