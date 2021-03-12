---
title: Eelarvekohase ostutellimuse loomine
description: Kasutage seda protseduuri, et luua ostutellimus, mida kontrollitakse saadaoleva eelarve osas.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbfbbef3bd7c7398f0f17b6cddbbff8c4755638d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963709"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="14e81-103">Eelarvekohase ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="14e81-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14e81-104">Kasutage seda protseduuri, et luua ostutellimus, mida kontrollitakse saadaoleva eelarve osas.</span><span class="sxs-lookup"><span data-stu-id="14e81-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="14e81-105">See salvestis kasutab USMF demoandmete ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="14e81-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="14e81-106">Vaadake üle eelarve juhtimise konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="14e81-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="14e81-107">Avage Eelarve koostamine > Häälestamine > Eelarve juhtimine > Eelarve juhtimise konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="14e81-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="14e81-108">Klõpsake vahekaarti Saadaval eelarvefondid.</span><span class="sxs-lookup"><span data-stu-id="14e81-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="14e81-109">Klõpsake vahekaarti Dokumendid ja töölehed.</span><span class="sxs-lookup"><span data-stu-id="14e81-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="14e81-110">Klõpsake vahekaarti Eelarve juhtimise määratlemine.</span><span class="sxs-lookup"><span data-stu-id="14e81-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="14e81-111">Klõpsake vahekaarti Eelarvegruppide määratlemine.</span><span class="sxs-lookup"><span data-stu-id="14e81-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="14e81-112">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="14e81-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="14e81-113">Ostutellimuse päise loomine</span><span class="sxs-lookup"><span data-stu-id="14e81-113">Create the purchase order header</span></span>
1. <span data-ttu-id="14e81-114">Avage Hanked > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="14e81-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="14e81-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="14e81-115">Click New.</span></span>
3. <span data-ttu-id="14e81-116">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="14e81-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="14e81-117">Laiendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="14e81-117">Expand the General section.</span></span>
5. <span data-ttu-id="14e81-118">Määrake aruandluskuupäeva väljal kuupäev „2016-01-01”.</span><span class="sxs-lookup"><span data-stu-id="14e81-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="14e81-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="14e81-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="14e81-120">Ostutellimuse rea lisamine</span><span class="sxs-lookup"><span data-stu-id="14e81-120">Add a purchase order line</span></span>
1. <span data-ttu-id="14e81-121">Sisestage või valige väärtus väljal Hanke kategooria.</span><span class="sxs-lookup"><span data-stu-id="14e81-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="14e81-122">Valige välja Kogus väärtuseks 2.</span><span class="sxs-lookup"><span data-stu-id="14e81-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="14e81-123">Sisestage või valige väärtus väljal Ühik.</span><span class="sxs-lookup"><span data-stu-id="14e81-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="14e81-124">Määrake ühiku hinna väärtuseks „10000”.</span><span class="sxs-lookup"><span data-stu-id="14e81-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="14e81-125">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="14e81-125">Click Financials.</span></span>
6. <span data-ttu-id="14e81-126">Klõpsake suvandit Summade jaotamine.</span><span class="sxs-lookup"><span data-stu-id="14e81-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="14e81-127">Määrake pearaamatukonto väljal väärtus „601300-001-023--”.</span><span class="sxs-lookup"><span data-stu-id="14e81-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="14e81-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="14e81-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="14e81-129">Eelarve kontrollimine</span><span class="sxs-lookup"><span data-stu-id="14e81-129">Perform budget checking</span></span>
1. <span data-ttu-id="14e81-130">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="14e81-130">Click Financials.</span></span>
2. <span data-ttu-id="14e81-131">Klõpsake valikut Eelarve kontrollimine.</span><span class="sxs-lookup"><span data-stu-id="14e81-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="14e81-132">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="14e81-132">Click Financials.</span></span>
4. <span data-ttu-id="14e81-133">Klõpsake valikut Eelarvekontrolli tõrked ja hoiatused.</span><span class="sxs-lookup"><span data-stu-id="14e81-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="14e81-134">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="14e81-134">Click Close.</span></span>

