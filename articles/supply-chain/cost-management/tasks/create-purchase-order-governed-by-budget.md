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
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa16955e0ea407555c7b52b0af37c5891be9bdbb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214282"
---
# <a name="create-a-purchase-order-governed-by-budget"></a><span data-ttu-id="f98fc-103">Eelarvekohase ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="f98fc-103">Create a purchase order governed by budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f98fc-104">Kasutage seda protseduuri, et luua ostutellimus, mida kontrollitakse saadaoleva eelarve osas.</span><span class="sxs-lookup"><span data-stu-id="f98fc-104">Use this procedure to create a purchase order that is checked for available budget.</span></span> <span data-ttu-id="f98fc-105">See salvestis kasutab USMF demoandmete ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="f98fc-105">This recording uses the USMF demo data company.</span></span>


## <a name="review-the-budget-control-configuration"></a><span data-ttu-id="f98fc-106">Vaadake üle eelarve juhtimise konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="f98fc-106">Review the budget control configuration</span></span>
1. <span data-ttu-id="f98fc-107">Avage Eelarve koostamine > Häälestamine > Eelarve juhtimine > Eelarve juhtimise konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="f98fc-107">Go to Budgeting > Setup > Budget control > Budget control configuration.</span></span>
2. <span data-ttu-id="f98fc-108">Klõpsake vahekaarti Saadaval eelarvefondid.</span><span class="sxs-lookup"><span data-stu-id="f98fc-108">Click the Budget funds available tab.</span></span>
3. <span data-ttu-id="f98fc-109">Klõpsake vahekaarti Dokumendid ja töölehed.</span><span class="sxs-lookup"><span data-stu-id="f98fc-109">Click the Documents and journals tab.</span></span>
4. <span data-ttu-id="f98fc-110">Klõpsake vahekaarti Eelarve juhtimise määratlemine.</span><span class="sxs-lookup"><span data-stu-id="f98fc-110">Click the Define budget control rules tab.</span></span>
5. <span data-ttu-id="f98fc-111">Klõpsake vahekaarti Eelarvegruppide määratlemine.</span><span class="sxs-lookup"><span data-stu-id="f98fc-111">Click the Define budget groups tab.</span></span>
6. <span data-ttu-id="f98fc-112">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f98fc-112">Close the page.</span></span>

## <a name="create-the-purchase-order-header"></a><span data-ttu-id="f98fc-113">Ostutellimuse päise loomine</span><span class="sxs-lookup"><span data-stu-id="f98fc-113">Create the purchase order header</span></span>
1. <span data-ttu-id="f98fc-114">Avage Hanked > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="f98fc-114">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="f98fc-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f98fc-115">Click New.</span></span>
3. <span data-ttu-id="f98fc-116">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="f98fc-116">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="f98fc-117">Laiendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="f98fc-117">Expand the General section.</span></span>
5. <span data-ttu-id="f98fc-118">Määrake aruandluskuupäeva väljal kuupäev „2016-01-01”.</span><span class="sxs-lookup"><span data-stu-id="f98fc-118">In the Accounting date field, set the date to '2016-01-01'.</span></span>
6. <span data-ttu-id="f98fc-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f98fc-119">Click OK.</span></span>

## <a name="add-a-purchase-order-line"></a><span data-ttu-id="f98fc-120">Ostutellimuse rea lisamine</span><span class="sxs-lookup"><span data-stu-id="f98fc-120">Add a purchase order line</span></span>
1. <span data-ttu-id="f98fc-121">Sisestage või valige väärtus väljal Hanke kategooria.</span><span class="sxs-lookup"><span data-stu-id="f98fc-121">In the Procurement category field, enter or select a value.</span></span>
2. <span data-ttu-id="f98fc-122">Valige välja Kogus väärtuseks 2.</span><span class="sxs-lookup"><span data-stu-id="f98fc-122">Set Quantity to '2'.</span></span>
3. <span data-ttu-id="f98fc-123">Sisestage või valige väärtus väljal Ühik.</span><span class="sxs-lookup"><span data-stu-id="f98fc-123">In the Unit field, enter or select a value.</span></span>
4. <span data-ttu-id="f98fc-124">Määrake ühiku hinna väärtuseks „10000”.</span><span class="sxs-lookup"><span data-stu-id="f98fc-124">Set Unit price to '10000'.</span></span>
5. <span data-ttu-id="f98fc-125">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="f98fc-125">Click Financials.</span></span>
6. <span data-ttu-id="f98fc-126">Klõpsake suvandit Summade jaotamine.</span><span class="sxs-lookup"><span data-stu-id="f98fc-126">Click Distribute amounts.</span></span>
7. <span data-ttu-id="f98fc-127">Määrake pearaamatukonto väljal väärtus „601300-001-023--”.</span><span class="sxs-lookup"><span data-stu-id="f98fc-127">In the Ledger account field, specify the value '601300-001-023--'.</span></span>
8. <span data-ttu-id="f98fc-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f98fc-128">Close the page.</span></span>

## <a name="perform-budget-checking"></a><span data-ttu-id="f98fc-129">Eelarve kontrollimine</span><span class="sxs-lookup"><span data-stu-id="f98fc-129">Perform budget checking</span></span>
1. <span data-ttu-id="f98fc-130">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="f98fc-130">Click Financials.</span></span>
2. <span data-ttu-id="f98fc-131">Klõpsake valikut Eelarve kontrollimine.</span><span class="sxs-lookup"><span data-stu-id="f98fc-131">Click Perform budget checking.</span></span>
3. <span data-ttu-id="f98fc-132">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="f98fc-132">Click Financials.</span></span>
4. <span data-ttu-id="f98fc-133">Klõpsake valikut Eelarvekontrolli tõrked ja hoiatused.</span><span class="sxs-lookup"><span data-stu-id="f98fc-133">Click Budget check errors or warnings.</span></span>
5. <span data-ttu-id="f98fc-134">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="f98fc-134">Click Close.</span></span>

