---
title: Kütuseindeksi seostamine vedajaga lisatasuna
description: See juhend näitab, kuidas luua lisade määramist, vedaja lisatasu, lisade koondandmeid kütuse lisatasu puhul ja kuidas seostada vedaja kütuseindeksit vedajaga.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: 0fbd58fb6b03f3c6eb5e54f811d98ad636e65a94
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146372"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a><span data-ttu-id="e02c1-103">Kütuseindeksi seostamine vedajaga lisatasuna</span><span class="sxs-lookup"><span data-stu-id="e02c1-103">Associate a fuel index with a carrier as an accessorial charge</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e02c1-104">See juhend näitab, kuidas luua lisade määramist, vedaja lisatasu, lisade koondandmeid kütuse lisatasu puhul ja kuidas seostada vedaja kütuseindeksit vedajaga.</span><span class="sxs-lookup"><span data-stu-id="e02c1-104">This guide shows how to create an accessorial assignment, carrier accessorial charge, accessorial master for fuel surcharge, and associate a carrier fuel index with a carrier.</span></span> <span data-ttu-id="e02c1-105">Enne selle juhendi käivitamist peab teil olema vedaja kütuseindeks seadistatud.</span><span class="sxs-lookup"><span data-stu-id="e02c1-105">You need to have set up a carrier fuel index before you run this guide.</span></span> <span data-ttu-id="e02c1-106">Saate selleks kasutada juhendit „Vedaja kütuseindeksi seadistamine”.</span><span class="sxs-lookup"><span data-stu-id="e02c1-106">You can use the "Set up a carrier fuel index" guide to do this.</span></span> <span data-ttu-id="e02c1-107">Neid seadistustoiminguid teeb üldjuhul logistika haldur.</span><span class="sxs-lookup"><span data-stu-id="e02c1-107">These setup tasks are typically done by a Logistics manager.</span></span> <span data-ttu-id="e02c1-108">Selle protseduuri loomiseks kasutati demoandmeid USMF.</span><span class="sxs-lookup"><span data-stu-id="e02c1-108">The demo data used to create this procedure is USMF.</span></span>


## <a name="create-an-accessorial-master"></a><span data-ttu-id="e02c1-109">Lisade koondandmete loomine</span><span class="sxs-lookup"><span data-stu-id="e02c1-109">Create an accessorial master</span></span>
1. <span data-ttu-id="e02c1-110">Avage Transpordihaldus > Seadistus > Hinnang > Lisade koondandmed.</span><span class="sxs-lookup"><span data-stu-id="e02c1-110">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="e02c1-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e02c1-111">Click New.</span></span>
3. <span data-ttu-id="e02c1-112">Sisestage väärtus väljale Lisade koondandmed.</span><span class="sxs-lookup"><span data-stu-id="e02c1-112">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="e02c1-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e02c1-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e02c1-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e02c1-114">Click Save.</span></span>

## <a name="create-a-carrier-accessorial-charge"></a><span data-ttu-id="e02c1-115">Vedaja lisatasu loomine</span><span class="sxs-lookup"><span data-stu-id="e02c1-115">Create a carrier accessorial charge</span></span>
1. <span data-ttu-id="e02c1-116">Avage Transpordihaldus > Seadistus > Hinnang > Vedaja lisatasud.</span><span class="sxs-lookup"><span data-stu-id="e02c1-116">Go to Transportation management > Setup > Rating > Carrier accessorial charges.</span></span>
2. <span data-ttu-id="e02c1-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e02c1-117">Click New.</span></span>
3. <span data-ttu-id="e02c1-118">Sisestage väärtus väljale Vedaja lisade ID.</span><span class="sxs-lookup"><span data-stu-id="e02c1-118">In the Carrier accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="e02c1-119">Klõpsake väljal Kättetoimetaja otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e02c1-119">In the Shipping carrier field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e02c1-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e02c1-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e02c1-121">Selles näites valige veoki vedaja.</span><span class="sxs-lookup"><span data-stu-id="e02c1-121">In this example, choose Truck Carrier.</span></span>  
6. <span data-ttu-id="e02c1-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e02c1-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e02c1-123">Klõpsake väljal Vedaja teenus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e02c1-123">In the Carrier service field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e02c1-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e02c1-124">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e02c1-125">Klõpsake väljal Lisade koondandmed otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e02c1-125">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e02c1-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e02c1-126">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e02c1-127">Selle näite puhul valige äsja loodud lisade koond.</span><span class="sxs-lookup"><span data-stu-id="e02c1-127">In this example, choose the newly created Accessorial master.</span></span>  
11. <span data-ttu-id="e02c1-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e02c1-128">Click Save.</span></span>

## <a name="create-an-accessorial-assignment"></a><span data-ttu-id="e02c1-129">Lisade määrangu loomine</span><span class="sxs-lookup"><span data-stu-id="e02c1-129">Create an accessorial assignment</span></span>
1. <span data-ttu-id="e02c1-130">Klõpsake suvandit Lisade määrangud.</span><span class="sxs-lookup"><span data-stu-id="e02c1-130">Click Accessorial assignments.</span></span>
2. <span data-ttu-id="e02c1-131">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e02c1-131">Click New.</span></span>
3. <span data-ttu-id="e02c1-132">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e02c1-132">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e02c1-133">Laiendage jaotist Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="e02c1-133">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="e02c1-134">Kriteeriumides saate alati valida kütuse lisatasu rakendamise või näiteks selle, et see kehtib ainult teatud regioonis.</span><span class="sxs-lookup"><span data-stu-id="e02c1-134">In the criteria, you can choose to always apply the fuel surcharge or for this example choose that it only applies within a certain region.</span></span>  
5. <span data-ttu-id="e02c1-135">Sisestage väärtus väljale Sihtnumber alates.</span><span class="sxs-lookup"><span data-stu-id="e02c1-135">In the ZIP/postal code from field, type a value.</span></span>
6. <span data-ttu-id="e02c1-136">Sisestage väärtus väljale Sihtnumber kuni.</span><span class="sxs-lookup"><span data-stu-id="e02c1-136">In the ZIP/postal code to field, type a value.</span></span>
7. <span data-ttu-id="e02c1-137">Laiendage jaotist Arvutamine.</span><span class="sxs-lookup"><span data-stu-id="e02c1-137">Toggle the expansion of the Calculation section.</span></span>
    * <span data-ttu-id="e02c1-138">Arvutamise jaotises saate määrata, kuidas kütuse lisatasu arvutada.</span><span class="sxs-lookup"><span data-stu-id="e02c1-138">In the calculation section you can specify how to calculate the fuel surcharge.</span></span> <span data-ttu-id="e02c1-139">Arvutamine oleneb teie arvutuse aluseks valitud lisade ühikust.</span><span class="sxs-lookup"><span data-stu-id="e02c1-139">This calculation depends on the Accessorial unit that you chose as the base for your calculation.</span></span>  
8. <span data-ttu-id="e02c1-140">Valige väljal Lisatasu tüüp suvand Kütuse lisatasu.</span><span class="sxs-lookup"><span data-stu-id="e02c1-140">In the Accessorial fee type field, select 'Fuel surcharge'.</span></span>
9. <span data-ttu-id="e02c1-141">Valige väljal Lisade ühik suvand Läbisõit.</span><span class="sxs-lookup"><span data-stu-id="e02c1-141">In the Accessorial unit field, select 'Mileage'.</span></span>
10. <span data-ttu-id="e02c1-142">Klõpsake väljal Regioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e02c1-142">In the Region field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e02c1-143">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e02c1-143">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e02c1-144">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e02c1-144">Click Save.</span></span>

## <a name="update-the-carrier-rating-profile"></a><span data-ttu-id="e02c1-145">Vedaja hinnanguprofiili värskendamine</span><span class="sxs-lookup"><span data-stu-id="e02c1-145">Update the carrier rating profile</span></span>
1. <span data-ttu-id="e02c1-146">Tehke valik Transpordi haldus > Seadistus > Vedajad > Kättetoimetajad.</span><span class="sxs-lookup"><span data-stu-id="e02c1-146">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="e02c1-147">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e02c1-147">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e02c1-148">Laiendage jaotist Hinnanguprofiilid.</span><span class="sxs-lookup"><span data-stu-id="e02c1-148">Toggle the expansion of the Rating profiles section.</span></span>
4. <span data-ttu-id="e02c1-149">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="e02c1-149">Click Edit.</span></span>
5. <span data-ttu-id="e02c1-150">Klõpsake väljal Vedaja kütuseindeks otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e02c1-150">In the Carrier fuel index field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e02c1-151">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e02c1-151">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e02c1-152">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e02c1-152">Click Save.</span></span>

