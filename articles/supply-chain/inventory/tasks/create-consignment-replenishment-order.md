---
title: Veose täiendustellimuse loomine
description: See protseduur näitab, kuidas koostada veose täiendustellimust, kus saate jälgida hankija eeldatavat tarnet oma veose varudesse.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d3e33008d04ea8bb7d145c7b63cec23a4a45dd2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "315494"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="c14cf-103">Veose täiendustellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="c14cf-103">Create a consignment replenishment order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c14cf-104">See protseduur näitab, kuidas koostada veose täiendustellimust, kus saate jälgida hankija eeldatavat tarnet oma veose varudesse.</span><span class="sxs-lookup"><span data-stu-id="c14cf-104">This procedure shows how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="c14cf-105">Samuti näitab see, kuidas registreerida toodete sissetulekut, et veose varud oleksid registreeritud hankijale kuuluva vaba kaubavaruna.</span><span class="sxs-lookup"><span data-stu-id="c14cf-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="c14cf-106">Selle protseduuri viib tavaliselt läbi hankespetsialist.</span><span class="sxs-lookup"><span data-stu-id="c14cf-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="c14cf-107">Saate seda juhendit kasutada demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="c14cf-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="c14cf-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="c14cf-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>




## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="c14cf-109">Veose täiendustellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="c14cf-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="c14cf-110">Avage Hanked > Saadetis > Saadetise täiendustellimused.</span><span class="sxs-lookup"><span data-stu-id="c14cf-110">Go to Procurement and sourcing > Consignment > Consignment replenishment orders.</span></span>
2. <span data-ttu-id="c14cf-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c14cf-111">Click New.</span></span>
3. <span data-ttu-id="c14cf-112">Valige väljalt Hankija konto hankija US-104.</span><span class="sxs-lookup"><span data-stu-id="c14cf-112">In the Vendor account field, select vendor US-104.</span></span>
    * <span data-ttu-id="c14cf-113">Peate valima hankija, kes on registreeritud omanikuna lehel Varude omanikud.</span><span class="sxs-lookup"><span data-stu-id="c14cf-113">You must select a vendor that’s registered as an owner in the Inventory owners page.</span></span>  
4. <span data-ttu-id="c14cf-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c14cf-114">Click OK.</span></span>
5. <span data-ttu-id="c14cf-115">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="c14cf-115">Click Add line.</span></span>
6. <span data-ttu-id="c14cf-116">Tippige väärtus M9211CI väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="c14cf-116">In the Item number field, type M9211CI.</span></span>
    * <span data-ttu-id="c14cf-117">Peate valima kauba, mis on seadistatud veose kaubavaruna.</span><span class="sxs-lookup"><span data-stu-id="c14cf-117">You must select an item that is set up for consignment inventory.</span></span>  
7. <span data-ttu-id="c14cf-118">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="c14cf-118">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="c14cf-119">Sisestage kuupäev väljale Nõutav tarnekuupäev.</span><span class="sxs-lookup"><span data-stu-id="c14cf-119">In the Requested delivery date field, enter a date.</span></span>
    * <span data-ttu-id="c14cf-120">MRP moodul kasutab nõutud ja kinnitatud kuupäevi kaupade eeldatava saabumise jaoks.</span><span class="sxs-lookup"><span data-stu-id="c14cf-120">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="c14cf-121">Sisestage kuupäev väljale Kinnitatud tarnekuupäev.</span><span class="sxs-lookup"><span data-stu-id="c14cf-121">In the Confirmed delivery date field, enter a date.</span></span>
10. <span data-ttu-id="c14cf-122">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="c14cf-122">Expand the Line details section.</span></span>
11. <span data-ttu-id="c14cf-123">Klõpsake vahekaarti Varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="c14cf-123">Click the Inventory dimensions tab.</span></span>
12. <span data-ttu-id="c14cf-124">Omaniku näitamiseks väljal Laodimensioonide omanik värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="c14cf-124">To show the owner in the Inventory dimensions owner field, refresh the page.</span></span>
    * <span data-ttu-id="c14cf-125">Hankija US-104 on nüüd omanikuna registreeritud.</span><span class="sxs-lookup"><span data-stu-id="c14cf-125">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="c14cf-126">Kontrollige kande kuupäeva olekut</span><span class="sxs-lookup"><span data-stu-id="c14cf-126">Check the inventory transaction status</span></span>
1. <span data-ttu-id="c14cf-127">Klõpsake Ladu.</span><span class="sxs-lookup"><span data-stu-id="c14cf-127">Click Inventory.</span></span>
2. <span data-ttu-id="c14cf-128">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="c14cf-128">Click Transactions.</span></span>
3. <span data-ttu-id="c14cf-129">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="c14cf-129">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c14cf-130">Pange tähele, et välja Sissetulek olekuks on määratud Tellitud.</span><span class="sxs-lookup"><span data-stu-id="c14cf-130">Notice that the Receipt field is set to Ordered.</span></span>  
4. <span data-ttu-id="c14cf-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c14cf-131">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="c14cf-132">Võta kaubad vastu</span><span class="sxs-lookup"><span data-stu-id="c14cf-132">Receive items</span></span>
1. <span data-ttu-id="c14cf-133">Klõpsake valikut Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="c14cf-133">Click Product receipt.</span></span>
2. <span data-ttu-id="c14cf-134">Tippige väärtus väljale Väline toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="c14cf-134">In the External product receipt field, type a value.</span></span>
3. <span data-ttu-id="c14cf-135">Sisestage väljale Kogus seal kuvatud numbrist väiksem number.</span><span class="sxs-lookup"><span data-stu-id="c14cf-135">In the Quantity field, enter a number that’s lower than the number that’s shown there.</span></span> 
4. <span data-ttu-id="c14cf-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c14cf-136">Click OK.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="c14cf-137">Kontrollige vaba kaubavaru</span><span class="sxs-lookup"><span data-stu-id="c14cf-137">Check the on-hand inventory</span></span>
1. <span data-ttu-id="c14cf-138">Klõpsake Ladu.</span><span class="sxs-lookup"><span data-stu-id="c14cf-138">Click Inventory.</span></span>
2. <span data-ttu-id="c14cf-139">Klõpsake valikut Laoseis.</span><span class="sxs-lookup"><span data-stu-id="c14cf-139">Click On-hand.</span></span>
3. <span data-ttu-id="c14cf-140">Klõpsake valikut Ülevaade.</span><span class="sxs-lookup"><span data-stu-id="c14cf-140">Click Overview.</span></span>
    * <span data-ttu-id="c14cf-141">Kaubad, mis on saadud hankijale kuuluva veose kaubavaruna, on vaba varuna saadaval.</span><span class="sxs-lookup"><span data-stu-id="c14cf-141">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="c14cf-142">Ülejäänud kogus veose täiendustellimusel on näidatud väljal Tellitud kokku.</span><span class="sxs-lookup"><span data-stu-id="c14cf-142">The remaining quantity on the consignment replenishment order is shown in the Ordered in total field.</span></span>  
4. <span data-ttu-id="c14cf-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c14cf-143">Close the page.</span></span>
5. <span data-ttu-id="c14cf-144">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="c14cf-144">Click Close.</span></span>

