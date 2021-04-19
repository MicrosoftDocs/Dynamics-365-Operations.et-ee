---
title: Vedaja kütuseindeksi seadistamine
description: See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c1e972f2ba8211c47b11a4b83dac9ff60f813b1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837575"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="94351-103">Vedaja kütuseindeksi seadistamine</span><span class="sxs-lookup"><span data-stu-id="94351-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="94351-104">See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.</span><span class="sxs-lookup"><span data-stu-id="94351-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="94351-105">Kütuseindeksi regioon määrab, millisele regioonile tuleks kütuseindeksit rakendada ja kütuseindeks määrab kütuse hinna teatud aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="94351-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="94351-106">Kütusehinna muudatuste kajastamiseks aja jooksul saate vedajaga seostada mitu kütuseindeksit.</span><span class="sxs-lookup"><span data-stu-id="94351-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="94351-107">Neid ülesandeid teeb üldjuhul transpordikoordinaator.</span><span class="sxs-lookup"><span data-stu-id="94351-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="94351-108">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="94351-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="94351-109">Kütuseindeksi regiooni loomine</span><span class="sxs-lookup"><span data-stu-id="94351-109">Create a fuel index region</span></span>
1. <span data-ttu-id="94351-110">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksi regioonid.</span><span class="sxs-lookup"><span data-stu-id="94351-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="94351-111">Esmalt peate looma erinevad regioonid, kus töötada, ja arvutama erinevad kütuse lisatasud.</span><span class="sxs-lookup"><span data-stu-id="94351-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="94351-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="94351-112">Click New.</span></span>
3. <span data-ttu-id="94351-113">Sisestage väärtus väljale Regioon.</span><span class="sxs-lookup"><span data-stu-id="94351-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="94351-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="94351-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="94351-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="94351-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="94351-116">Saate luua ka kütuseindeks</span><span class="sxs-lookup"><span data-stu-id="94351-116">Create a fuel index</span></span>
1. <span data-ttu-id="94351-117">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksid.</span><span class="sxs-lookup"><span data-stu-id="94351-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="94351-118">Seadistatud regioonide puhul peate sisestama kütuse praegused hinnad.</span><span class="sxs-lookup"><span data-stu-id="94351-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="94351-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="94351-119">Click New.</span></span>
3. <span data-ttu-id="94351-120">Klõpsake väljal Regioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="94351-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="94351-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="94351-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="94351-122">Sisestage number väljale Galloni hind.</span><span class="sxs-lookup"><span data-stu-id="94351-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="94351-123">Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="94351-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="94351-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="94351-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="94351-125">Vedaja kütuseindeksi loomine</span><span class="sxs-lookup"><span data-stu-id="94351-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="94351-126">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Vedaja kütuseindeksid.</span><span class="sxs-lookup"><span data-stu-id="94351-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="94351-127">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="94351-127">Click New.</span></span>
3. <span data-ttu-id="94351-128">Sisestage väärtus väljale Vedaja kütuseindeks.</span><span class="sxs-lookup"><span data-stu-id="94351-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="94351-129">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="94351-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="94351-130">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="94351-130">Click New.</span></span>
6. <span data-ttu-id="94351-131">Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="94351-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="94351-132">Sisestage number väljale Galloni hind alates.</span><span class="sxs-lookup"><span data-stu-id="94351-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="94351-133">Selles näites saate seadistada välja Galloni hind alates väärtusele 1,95.</span><span class="sxs-lookup"><span data-stu-id="94351-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="94351-134">Sisestage number väljale Galloni hind kuni.</span><span class="sxs-lookup"><span data-stu-id="94351-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="94351-135">Selles näites saate seadistada välja Galloni hind kuni väärtusele 2.</span><span class="sxs-lookup"><span data-stu-id="94351-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="94351-136">Sisestage number väljale Protsent.</span><span class="sxs-lookup"><span data-stu-id="94351-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="94351-137">Selles näites saate seadistada protsendi väärtusele 3.</span><span class="sxs-lookup"><span data-stu-id="94351-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="94351-138">Klõpsake väljal Valuuta otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="94351-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="94351-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="94351-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="94351-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="94351-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="94351-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="94351-141">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]