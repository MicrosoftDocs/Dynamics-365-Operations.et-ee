---
title: Vedajate seadistamine
description: See teema näitab, kuidas seadistada tarne vedaja ja määratleda üksikasjad, nt teenus, saadetise režiim, transpordi maksevahend, transpordi piirangud ja tarnekulu.
author: ShylaThompson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb39d58336e7f867e19d7ba6d9f801200de5a0aa
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148551"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="6cf68-103">Vedajate seadistamine</span><span class="sxs-lookup"><span data-stu-id="6cf68-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6cf68-104">See teema näitab, kuidas seadistada tarne vedaja ja määratleda üksikasjad, nt teenus, saadetise režiim, transpordi maksevahend, transpordi piirangud ja tarnekulu.</span><span class="sxs-lookup"><span data-stu-id="6cf68-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="6cf68-105">Transpordi koordinaator saab seejärel määrata saadetise vedaja sissetulevale või väljaminevale koormale.</span><span class="sxs-lookup"><span data-stu-id="6cf68-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="6cf68-106">Uue kättetoimetaja loomine</span><span class="sxs-lookup"><span data-stu-id="6cf68-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="6cf68-107">Valige **Navigeerimispaneel > Moodulid > Transpordi haldus > Seadistus > Vedajad > Kättetoimetajad**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="6cf68-108">Valige toimingupaanil **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-108">Select **New** in the Action pane.</span></span>
3. <span data-ttu-id="6cf68-109">Sisestage väärtus väljale **Kättetoimetaja**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="6cf68-110">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="6cf68-111">Valige väljal **Režiim** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="6cf68-112">Kättetoimetaja üldise teabe sisestamine</span><span class="sxs-lookup"><span data-stu-id="6cf68-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="6cf68-113">Laiendage jaotist **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="6cf68-114">Märkige või tühjendage ruut **Aktiveeri saadetise vedaja**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="6cf68-115">Valige väljal **Hankija konto** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="6cf68-116">Valige hankija konto, millele tarne vedaja määrata.</span><span class="sxs-lookup"><span data-stu-id="6cf68-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="6cf68-117">Valige suvand väljal **Transpordi maksevahendi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="6cf68-118">Valige transpordi maksevahendi lehe kasutamiseks **Juhend** või valige **EDI**, pakkumist värskendada elektroonilise andmevahetuse (EDI) abil.</span><span class="sxs-lookup"><span data-stu-id="6cf68-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="6cf68-119">Märkige või tühjendage ruut **Aktiveeri vedaja hinnang** .</span><span class="sxs-lookup"><span data-stu-id="6cf68-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="6cf68-120">Kättetoimetaja vajalike teenuste loomine</span><span class="sxs-lookup"><span data-stu-id="6cf68-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="6cf68-121">Laiendage jaotist **Teenused**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="6cf68-122">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-122">Select **New**.</span></span>
3. <span data-ttu-id="6cf68-123">Sisestage väärtus väljale **Vedaja teenus**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="6cf68-124">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="6cf68-125">Valige väljal **Transpordimeetod** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="6cf68-126">Vedaja aadressi seadistamine (valikuline)</span><span class="sxs-lookup"><span data-stu-id="6cf68-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="6cf68-127">Lülitage ümber jaotis **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="6cf68-128">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-128">Select **New**.</span></span>
3. <span data-ttu-id="6cf68-129">Sisestage väärtus väljale **Nimi või kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="6cf68-130">Valige väljal **Riik/regioon** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="6cf68-131">Valige väljal **Postiindeks** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="6cf68-132">Sisestage väärtus väljale **Tänav**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="6cf68-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="6cf68-134">Kättetoimetaja hinnanguprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="6cf68-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="6cf68-135">Laiendage jaotist **Hinnanguprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="6cf68-136">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-136">Select **New**.</span></span>
3. <span data-ttu-id="6cf68-137">Sisestage väärtus väljale **Hinnanguprofiil**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="6cf68-138">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="6cf68-139">Valige väljal **Sait** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="6cf68-140">Valige väljal **Ladu** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="6cf68-141">Valige väljal **Määra mootor** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="6cf68-142">Valige Määra mootor, mis on kooskõlas vedaja lepinguga.</span><span class="sxs-lookup"><span data-stu-id="6cf68-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="6cf68-143">Valige väljal **Määra juht** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="6cf68-144">Valige väljal **Transiidiaja mootor** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="6cf68-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="6cf68-145">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6cf68-145">Select **Save**.</span></span>

