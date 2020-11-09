---
title: Vedajate seadistamine
description: See teema näitab, kuidas seadistada tarne vedaja ja määratleda üksikasjad, nt teenus, saadetise režiim, transpordi maksevahend, transpordi piirangud ja tarnekulu.
author: ShylaThompson
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSShippingCarrierCustomerAccount,TMSCarrier
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a71ea3983018b136d4fe3b22eadc0c332d2a698
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016443"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="ab4d2-103">Vedajate seadistamine</span><span class="sxs-lookup"><span data-stu-id="ab4d2-103">Set up shipping carriers</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab4d2-104">See teema näitab, kuidas seadistada tarne vedaja ja määratleda üksikasjad, nt teenus, saadetise režiim, transpordi maksevahend, transpordi piirangud ja tarnekulu.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-104">This topic shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="ab4d2-105">Transpordi koordinaator saab seejärel määrata saadetise vedaja sissetulevale või väljaminevale koormale.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="ab4d2-106">Uue kättetoimetaja loomine</span><span class="sxs-lookup"><span data-stu-id="ab4d2-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="ab4d2-107">Valige **Navigeerimispaneel > Moodulid > Transpordi haldus > Seadistus > Vedajad > Kättetoimetajad**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-107">Go to **Navigation pane > Modules > Transportation management > Setup > Carriers > Shipping carriers**.</span></span>
2. <span data-ttu-id="ab4d2-108">Valige Toimingupaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-108">Select **New** on the Action Pane.</span></span>
3. <span data-ttu-id="ab4d2-109">Sisestage väärtus väljale **Kättetoimetaja**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-109">In the **Shipping carrier** field, type a value.</span></span>
4. <span data-ttu-id="ab4d2-110">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-110">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ab4d2-111">Valige väljal **Režiim** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-111">In the **Mode** field, select an option from the drop-down menu.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="ab4d2-112">Kättetoimetaja üldise teabe sisestamine</span><span class="sxs-lookup"><span data-stu-id="ab4d2-112">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="ab4d2-113">Laiendage jaotist **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-113">Toggle the expansion of the **Overview** section.</span></span>
2. <span data-ttu-id="ab4d2-114">Märkige või tühjendage ruut **Aktiveeri saadetise vedaja**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-114">Check or uncheck the **Activate shipping carrier** checkbox.</span></span>
3. <span data-ttu-id="ab4d2-115">Valige väljal **Hankija konto** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-115">In the **Vendor account** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="ab4d2-116">Valige hankija konto, millele tarne vedaja määrata.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-116">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="ab4d2-117">Valige suvand väljal **Transpordi maksevahendi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-117">In the **Transportation tender type** field, select an option.</span></span> <span data-ttu-id="ab4d2-118">Valige transpordi maksevahendi lehe kasutamiseks **Juhend** või valige **EDI** , pakkumist värskendada elektroonilise andmevahetuse (EDI) abil.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-118">Select **Manual** to use the Transportation Tender page, or select **EDI** to update the tender by using Electronic Data Interchange (EDI).</span></span>  
5. <span data-ttu-id="ab4d2-119">Märkige või tühjendage ruut **Aktiveeri vedaja hinnang** .</span><span class="sxs-lookup"><span data-stu-id="ab4d2-119">Check or uncheck the **Activate carrier rating** checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="ab4d2-120">Kättetoimetaja vajalike teenuste loomine</span><span class="sxs-lookup"><span data-stu-id="ab4d2-120">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="ab4d2-121">Laiendage jaotist **Teenused**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-121">Toggle the expansion of the **Services** section.</span></span>
2. <span data-ttu-id="ab4d2-122">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-122">Select **New**.</span></span>
3. <span data-ttu-id="ab4d2-123">Sisestage väärtus väljale **Vedaja teenus**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-123">In the **Carrier service** field, type a value.</span></span>
4. <span data-ttu-id="ab4d2-124">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-124">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ab4d2-125">Valige väljal **Transpordimeetod** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-125">In the **Transportation method** field, select an option from the drop-down menu.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="ab4d2-126">Vedaja aadressi seadistamine (valikuline)</span><span class="sxs-lookup"><span data-stu-id="ab4d2-126">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="ab4d2-127">Lülitage ümber jaotis **Aadressid**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-127">Toggle the expansion of the **Addresses** section.</span></span>
2. <span data-ttu-id="ab4d2-128">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-128">Select **New**.</span></span>
3. <span data-ttu-id="ab4d2-129">Sisestage väärtus väljale **Nimi või kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-129">In the **Name or description** field, type a value.</span></span>
4. <span data-ttu-id="ab4d2-130">Valige väljal **Riik/regioon** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-130">In the **Country/region** field, select an option from the drop-down menu.</span></span>
5. <span data-ttu-id="ab4d2-131">Valige väljal **Postiindeks** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-131">In the **ZIP/postal code** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="ab4d2-132">Sisestage väärtus väljale **Tänav**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-132">In the **Street** field, type a value.</span></span>
7. <span data-ttu-id="ab4d2-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-133">Select **OK**.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="ab4d2-134">Kättetoimetaja hinnanguprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="ab4d2-134">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="ab4d2-135">Laiendage jaotist **Hinnanguprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-135">Toggle the expansion of the **Rating profiles** section.</span></span>
2. <span data-ttu-id="ab4d2-136">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-136">Select **New**.</span></span>
3. <span data-ttu-id="ab4d2-137">Sisestage väärtus väljale **Hinnanguprofiil**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-137">In the **Rating profile** field, type a value.</span></span>
4. <span data-ttu-id="ab4d2-138">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ab4d2-139">Valige väljal **Sait** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-139">In the **Site** field, select an option from the drop-down menu.</span></span>
6. <span data-ttu-id="ab4d2-140">Valige väljal **Ladu** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-140">In the **Warehouse** field, select an option from the drop-down menu.</span></span>
7. <span data-ttu-id="ab4d2-141">Valige väljal **Määra mootor** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-141">In the **Rate engine** field, select an option from the drop-down menu.</span></span> <span data-ttu-id="ab4d2-142">Valige Määra mootor, mis on kooskõlas vedaja lepinguga.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-142">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
8. <span data-ttu-id="ab4d2-143">Valige väljal **Määra juht** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-143">In the **Rate master** field, select an option from the drop-down menu.</span></span>
9. <span data-ttu-id="ab4d2-144">Valige väljal **Transiidiaja mootor** ripploendist suvand.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-144">In the **Transit time engine** field, select an option from the drop-down menu.</span></span>
10. <span data-ttu-id="ab4d2-145">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ab4d2-145">Select **Save**.</span></span>

