---
title: Veose täiendustellimuse loomine
description: Selles teemas selgitatakse, kuidas luua veose täiendustellimust, kus saate jälgida hankija eeldatavat tarnet oma veose varudesse.
author: mkirknel
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentReplenishmentOrder, ConsignmentReplenishmentOrderCreate, InventTrans, ConsignmentDraftReplenishmentOrderJournal, InventOnhandMovement, InventOnhandItem, InventItemIdLookupSimple, ConsignmentProductReceiptJournal, ConsignmentReplenishmentOrderLineQuantity
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e993190150e2d82088390d8db4b7c5ada2b0161
ms.sourcegitcommit: e3f4dd2257a3255c2982f4fc7b72a1121275b88a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4018349"
---
# <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="2e014-103">Veose täiendustellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="2e014-103">Create a consignment replenishment order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e014-104">Selles teemas selgitatakse, kuidas luua veose täiendustellimust, kus saate jälgida hankija eeldatavat tarnet oma veose varudesse.</span><span class="sxs-lookup"><span data-stu-id="2e014-104">This topic explains how to create a consignment replenishment order where you can track the expected delivery from a vendor into your consignment inventory.</span></span> <span data-ttu-id="2e014-105">Samuti näitab see, kuidas registreerida toodete sissetulekut, et veose varud oleksid registreeritud hankijale kuuluva vaba kaubavaruna.</span><span class="sxs-lookup"><span data-stu-id="2e014-105">It also shows how to record a receipt of products so that the consignment inventory is registered as on-hand inventory owned by the vendor.</span></span> <span data-ttu-id="2e014-106">Selle protseduuri viib tavaliselt läbi hankespetsialist.</span><span class="sxs-lookup"><span data-stu-id="2e014-106">This procedure would typically be done by a procurement professional.</span></span> <span data-ttu-id="2e014-107">Saate seda juhendit kasutada demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="2e014-107">You can use this guide in demo data company USMF.</span></span> <span data-ttu-id="2e014-108">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="2e014-108">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>

## <a name="create-a-consignment-replenishment-order"></a><span data-ttu-id="2e014-109">Veose täiendustellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="2e014-109">Create a consignment replenishment order</span></span>
1. <span data-ttu-id="2e014-110">Navigeerimispaanil avage **Moodulid > Hanked > Veos > Veose täiendustellimused**.</span><span class="sxs-lookup"><span data-stu-id="2e014-110">In the navigation pane, go to **Modules > Procurement and sourcing > Consignment > Consignment replenishment orders**.</span></span>
2. <span data-ttu-id="2e014-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2e014-111">Select **New**.</span></span>
3. <span data-ttu-id="2e014-112">Väljal **Hankija konto** valige hankija **US-104** (peate valima hankija, mis on lehel **varude omanikud** omanikuna registreeritud).</span><span class="sxs-lookup"><span data-stu-id="2e014-112">In the **Vendor account** field, select vendor **US-104** (you must select a vendor that's registered as an owner in the **inventory owners** page).</span></span> 
4. <span data-ttu-id="2e014-113">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e014-113">Select **OK**.</span></span>
5. <span data-ttu-id="2e014-114">Valige **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="2e014-114">Select **Add line**.</span></span>
6. <span data-ttu-id="2e014-115">Väljale **Kaubakood** sisestage `M9211CI` (peate valima kauba, mis on seadistatud veose varude jaoks).</span><span class="sxs-lookup"><span data-stu-id="2e014-115">In the **Item number** field, type `M9211CI` (you must select an item that is set up for consignment inventory).</span></span>
7. <span data-ttu-id="2e014-116">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="2e014-116">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="2e014-117">Väljale **Nõutud tarnekuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="2e014-117">In the **Requested delivery date** field, enter a date.</span></span> <span data-ttu-id="2e014-118">MRP moodul kasutab nõutud ja kinnitatud kuupäevi kaupade eeldatava saabumise jaoks.</span><span class="sxs-lookup"><span data-stu-id="2e014-118">The requested and confirmed dates are used by the MRP engine for the expected arrival of the goods.</span></span>  
9. <span data-ttu-id="2e014-119">Väljale **Kinnitatud tarnekuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="2e014-119">In the **Confirmed delivery date** field, enter a date.</span></span>
10. <span data-ttu-id="2e014-120">Laiendage jaotist **Rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="2e014-120">Expand the **Line details** section.</span></span>
11. <span data-ttu-id="2e014-121">Valige vahekaart **Varude dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="2e014-121">Select the **Inventory dimensions** tab.</span></span>
12. <span data-ttu-id="2e014-122">Värskendage lehte omaniku kuvamiseks väljal **Varude dimensioonide omanik**.</span><span class="sxs-lookup"><span data-stu-id="2e014-122">To show the owner in the **Inventory dimensions owner** field, refresh the page.</span></span> <span data-ttu-id="2e014-123">Hankija US-104 on nüüd omanikuna registreeritud.</span><span class="sxs-lookup"><span data-stu-id="2e014-123">Vendor US-104 is now listed as the owner.</span></span>  

## <a name="check-the-inventory-transaction-status"></a><span data-ttu-id="2e014-124">Kontrollige kande kuupäeva olekut</span><span class="sxs-lookup"><span data-stu-id="2e014-124">Check the inventory transaction status</span></span>
1. <span data-ttu-id="2e014-125">Valige **Laoseis**.</span><span class="sxs-lookup"><span data-stu-id="2e014-125">Select **Inventory**.</span></span>
2. <span data-ttu-id="2e014-126">Valige **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="2e014-126">Select **Transactions**.</span></span>
3. <span data-ttu-id="2e014-127">Pange tähele, et soovitud rea väli **Sissetulek** on seadistatud olekule **Tellitud**.</span><span class="sxs-lookup"><span data-stu-id="2e014-127">In the desired row, notice that the **Receipt** field is set to **Ordered**.</span></span>  
4. <span data-ttu-id="2e014-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2e014-128">Close the page.</span></span>

## <a name="receive-items"></a><span data-ttu-id="2e014-129">Võta kaubad vastu</span><span class="sxs-lookup"><span data-stu-id="2e014-129">Receive items</span></span>
1. <span data-ttu-id="2e014-130">Valige **Toote sissetulek**.</span><span class="sxs-lookup"><span data-stu-id="2e014-130">Select **Product receipt**.</span></span>
2. <span data-ttu-id="2e014-131">Väljale **Väline toote sissetulek** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="2e014-131">In the **External product receipt** field, type a value.</span></span>
3. <span data-ttu-id="2e014-132">Väljale **Kogus** sisestage arv, mis on väiksem kui arv, mida seal kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="2e014-132">In the **Quantity** field, enter a number that's lower than the number that's shown there.</span></span> 
4. <span data-ttu-id="2e014-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e014-133">Select **OK**.</span></span>

## <a name="check-the-on-hand-inventory"></a><span data-ttu-id="2e014-134">Kontrollige vaba kaubavaru</span><span class="sxs-lookup"><span data-stu-id="2e014-134">Check the on-hand inventory</span></span>
1. <span data-ttu-id="2e014-135">Valige **Laoseis**.</span><span class="sxs-lookup"><span data-stu-id="2e014-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="2e014-136">Valige **Varu**.</span><span class="sxs-lookup"><span data-stu-id="2e014-136">Select **On-hand**.</span></span>
3. <span data-ttu-id="2e014-137">Valige **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="2e014-137">Select **Overview**.</span></span> <span data-ttu-id="2e014-138">Kaubad, mis on saadud hankijale kuuluva veose kaubavaruna, on vaba varuna saadaval.</span><span class="sxs-lookup"><span data-stu-id="2e014-138">The items that have been received as consignment inventory owned by the vendor are available on-hand.</span></span> <span data-ttu-id="2e014-139">Veose täiendustellimuse järelejäänud kogus kuvatakse väljal **Tellitud kokku**.</span><span class="sxs-lookup"><span data-stu-id="2e014-139">The remaining quantity on the consignment replenishment order is shown in the **Ordered in total** field.</span></span>  
4. <span data-ttu-id="2e014-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2e014-140">Close the page.</span></span>

