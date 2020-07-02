---
title: Varude saadavus topeltkirjutuses
description: Selles teemas saate teada, kuidas kontrollida varude saadavust topeltkirjutuses.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
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
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 227a2062a7985a787f8278c196f7df2fb6f31691
ms.sourcegitcommit: cf709f1421a0bf66ecea493088ecb4eb08004187
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/12/2020
ms.locfileid: "3443868"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="9930a-103">Varude saadavus topeltkirjutuses</span><span class="sxs-lookup"><span data-stu-id="9930a-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9930a-104">Varude saadavuse abil saate kontrollida oma varusid enne, kui lisate toote rakenduses Microsoft Dynamics 365 Sales lehtedele **Pakkumised**, **Tellimused** või **Arved**.</span><span class="sxs-lookup"><span data-stu-id="9930a-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="9930a-105">Näiteks kontrollite te protsessi [potentsiaalne klient sularahaks](dual-write-prospect-to-cash.md) käigus ühe olulise ülesandena varusid ja määrate täitmiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="9930a-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="9930a-106">Kui teil puuduvad piisavad varud, siis saate eeldatava varude vastuvõtu ja väljastamise alusel tarneaega prognoosida.</span><span class="sxs-lookup"><span data-stu-id="9930a-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="9930a-107">Samuti saate kontrollida lubamiseks saadaval (ATP) toote teavet, kust leiate lubamiseks saadaval koguse eelmääratletud ajavahemiku raames.</span><span class="sxs-lookup"><span data-stu-id="9930a-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="9930a-108">Vaba kaubavaru</span><span class="sxs-lookup"><span data-stu-id="9930a-108">On-hand inventory</span></span>

<span data-ttu-id="9930a-109">Rakenduses Dynamics 365 Sales on lehtede **Pakkumised**, **Tellimused** ja **Arved** päisesse lisatud uus nupp **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="9930a-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="9930a-110">Nupule klõpsates ilmub dialoogiboks, kus saate määratleda ettevõtte ja toote, mille puhul soovite kontrollida vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="9930a-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="9930a-111">Selles dialoogiboksis kuvatav teave ühtib teemas [Vaba kaubavaru](../../../../supply-chain/inventory/tasks/check-availability-stock.md) kirjeldatud teabega.</span><span class="sxs-lookup"><span data-stu-id="9930a-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="9930a-112">Dialoogiboksis kuvatakse Dynamics 365 Supply Chain Managementist pärit teavet varude kohta.</span><span class="sxs-lookup"><span data-stu-id="9930a-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="9930a-113">See teave sisaldab järgmiseid koguseid.</span><span class="sxs-lookup"><span data-stu-id="9930a-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="9930a-114">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-114">On-hand quantity</span></span>
- <span data-ttu-id="9930a-115">Reserveeritud laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="9930a-116">Saadaolev laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-116">Available on-hand quantity</span></span>
- <span data-ttu-id="9930a-117">Tellitud kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-117">Ordered quantity</span></span>
- <span data-ttu-id="9930a-118">Tellimisel kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-118">On-order quantity</span></span>
- <span data-ttu-id="9930a-119">Reserveeritud tellitud kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="9930a-120">Saadaolev kogus kokku</span><span class="sxs-lookup"><span data-stu-id="9930a-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="9930a-121">ATP teave</span><span class="sxs-lookup"><span data-stu-id="9930a-121">ATP information</span></span>

<span data-ttu-id="9930a-122">Rakenduses Sales on lisatud lehtede **Pakkumised**, **Tellimused** ja **Arved** reakaupadele uus nupp **ATP teave**.</span><span class="sxs-lookup"><span data-stu-id="9930a-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="9930a-123">Nupule klõpsates ilmub dialoogiboks, kus saate määratleda ettevõtte, toote, varude saidi, varude lao ja tellimuse koguse.</span><span class="sxs-lookup"><span data-stu-id="9930a-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="9930a-124">Selle dialoogiboksi sätted ühtivad teemas [Tellimuse lubamine](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) kirjeldatutega.</span><span class="sxs-lookup"><span data-stu-id="9930a-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="9930a-125">Dialoogiboksis kuvatakse Supply Chain Managementist pärit ATP teave.</span><span class="sxs-lookup"><span data-stu-id="9930a-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="9930a-126">See teave sisaldab järgmiseid koguseid.</span><span class="sxs-lookup"><span data-stu-id="9930a-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="9930a-127">ATP kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-127">ATP quantity</span></span>
- <span data-ttu-id="9930a-128">Sissetuleku kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-128">Receipt quantity</span></span>
- <span data-ttu-id="9930a-129">Väljamineku kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-129">Issue quantity</span></span>
- <span data-ttu-id="9930a-130">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="9930a-130">On-hand quantity</span></span>
