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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: 4d1022eec633bf0a9edb4d5b26982853cec836d7
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997888"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="c866c-103">Varude saadavus topeltkirjutuses</span><span class="sxs-lookup"><span data-stu-id="c866c-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c866c-104">Varude saadavuse abil saate kontrollida oma varusid enne, kui lisate toote rakenduses Microsoft Dynamics 365 Sales lehtedele **Pakkumised** , **Tellimused** või **Arved**.</span><span class="sxs-lookup"><span data-stu-id="c866c-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations** , **Orders** , or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="c866c-105">Näiteks kontrollite te protsessi [potentsiaalne klient sularahaks](dual-write-prospect-to-cash.md) käigus ühe olulise ülesandena varusid ja määrate täitmiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="c866c-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="c866c-106">Kui teil puuduvad piisavad varud, siis saate eeldatava varude vastuvõtu ja väljastamise alusel tarneaega prognoosida.</span><span class="sxs-lookup"><span data-stu-id="c866c-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="c866c-107">Samuti saate kontrollida lubamiseks saadaval (ATP) toote teavet, kust leiate lubamiseks saadaval koguse eelmääratletud ajavahemiku raames.</span><span class="sxs-lookup"><span data-stu-id="c866c-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="c866c-108">Vaba kaubavaru</span><span class="sxs-lookup"><span data-stu-id="c866c-108">On-hand inventory</span></span>

<span data-ttu-id="c866c-109">Rakenduses Dynamics 365 Sales on lehtede **Pakkumised** , **Tellimused** ja **Arved** päisesse lisatud uus nupp **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="c866c-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="c866c-110">Nupule klõpsates ilmub dialoogiboks, kus saate määratleda ettevõtte ja toote, mille puhul soovite kontrollida vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="c866c-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="c866c-111">Selles dialoogiboksis kuvatav teave ühtib teemas [Vaba kaubavaru](../../../../supply-chain/inventory/tasks/check-availability-stock.md) kirjeldatud teabega.</span><span class="sxs-lookup"><span data-stu-id="c866c-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="c866c-112">Dialoogiboksis kuvatakse Dynamics 365 Supply Chain Managementist pärit teavet varude kohta.</span><span class="sxs-lookup"><span data-stu-id="c866c-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="c866c-113">See teave sisaldab järgmiseid koguseid.</span><span class="sxs-lookup"><span data-stu-id="c866c-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="c866c-114">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-114">On-hand quantity</span></span>
- <span data-ttu-id="c866c-115">Reserveeritud laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="c866c-116">Saadaolev laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-116">Available on-hand quantity</span></span>
- <span data-ttu-id="c866c-117">Tellitud kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-117">Ordered quantity</span></span>
- <span data-ttu-id="c866c-118">Tellimisel kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-118">On-order quantity</span></span>
- <span data-ttu-id="c866c-119">Reserveeritud tellitud kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="c866c-120">Saadaolev kogus kokku</span><span class="sxs-lookup"><span data-stu-id="c866c-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="c866c-121">ATP teave</span><span class="sxs-lookup"><span data-stu-id="c866c-121">ATP information</span></span>

<span data-ttu-id="c866c-122">Rakenduses Sales on lisatud lehtede **Pakkumised** , **Tellimused** ja **Arved** reakaupadele uus nupp **ATP teave**.</span><span class="sxs-lookup"><span data-stu-id="c866c-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes** , **Orders** , and **Invoices** pages.</span></span> <span data-ttu-id="c866c-123">Nupule klõpsates ilmub dialoogiboks, kus saate määratleda ettevõtte, toote, varude saidi, varude lao ja tellimuse koguse.</span><span class="sxs-lookup"><span data-stu-id="c866c-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="c866c-124">Selle dialoogiboksi sätted ühtivad teemas [Tellimuse lubamine](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) kirjeldatutega.</span><span class="sxs-lookup"><span data-stu-id="c866c-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="c866c-125">Dialoogiboksis kuvatakse Supply Chain Managementist pärit ATP teave.</span><span class="sxs-lookup"><span data-stu-id="c866c-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="c866c-126">See teave sisaldab järgmiseid koguseid.</span><span class="sxs-lookup"><span data-stu-id="c866c-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="c866c-127">ATP kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-127">ATP quantity</span></span>
- <span data-ttu-id="c866c-128">Sissetuleku kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-128">Receipt quantity</span></span>
- <span data-ttu-id="c866c-129">Väljamineku kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-129">Issue quantity</span></span>
- <span data-ttu-id="c866c-130">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="c866c-130">On-hand quantity</span></span>
