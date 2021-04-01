---
title: Vedaja kütuseindeksi seadistamine
description: See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09dc948e673bb8be49ac81e5ad2b20bc6c62b286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233651"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="d9312-103">Vedaja kütuseindeksi seadistamine</span><span class="sxs-lookup"><span data-stu-id="d9312-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9312-104">See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.</span><span class="sxs-lookup"><span data-stu-id="d9312-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="d9312-105">Kütuseindeksi regioon määrab, millisele regioonile tuleks kütuseindeksit rakendada ja kütuseindeks määrab kütuse hinna teatud aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="d9312-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="d9312-106">Kütusehinna muudatuste kajastamiseks aja jooksul saate vedajaga seostada mitu kütuseindeksit.</span><span class="sxs-lookup"><span data-stu-id="d9312-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="d9312-107">Neid ülesandeid teeb üldjuhul transpordikoordinaator.</span><span class="sxs-lookup"><span data-stu-id="d9312-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="d9312-108">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="d9312-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="d9312-109">Kütuseindeksi regiooni loomine</span><span class="sxs-lookup"><span data-stu-id="d9312-109">Create a fuel index region</span></span>
1. <span data-ttu-id="d9312-110">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksi regioonid.</span><span class="sxs-lookup"><span data-stu-id="d9312-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="d9312-111">Esmalt peate looma erinevad regioonid, kus töötada, ja arvutama erinevad kütuse lisatasud.</span><span class="sxs-lookup"><span data-stu-id="d9312-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="d9312-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d9312-112">Click New.</span></span>
3. <span data-ttu-id="d9312-113">Sisestage väärtus väljale Regioon.</span><span class="sxs-lookup"><span data-stu-id="d9312-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="d9312-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d9312-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d9312-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d9312-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="d9312-116">Saate luua ka kütuseindeks</span><span class="sxs-lookup"><span data-stu-id="d9312-116">Create a fuel index</span></span>
1. <span data-ttu-id="d9312-117">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksid.</span><span class="sxs-lookup"><span data-stu-id="d9312-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="d9312-118">Seadistatud regioonide puhul peate sisestama kütuse praegused hinnad.</span><span class="sxs-lookup"><span data-stu-id="d9312-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="d9312-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d9312-119">Click New.</span></span>
3. <span data-ttu-id="d9312-120">Klõpsake väljal Regioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d9312-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d9312-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d9312-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d9312-122">Sisestage number väljale Galloni hind.</span><span class="sxs-lookup"><span data-stu-id="d9312-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="d9312-123">Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="d9312-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="d9312-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d9312-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="d9312-125">Vedaja kütuseindeksi loomine</span><span class="sxs-lookup"><span data-stu-id="d9312-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="d9312-126">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Vedaja kütuseindeksid.</span><span class="sxs-lookup"><span data-stu-id="d9312-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="d9312-127">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d9312-127">Click New.</span></span>
3. <span data-ttu-id="d9312-128">Sisestage väärtus väljale Vedaja kütuseindeks.</span><span class="sxs-lookup"><span data-stu-id="d9312-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="d9312-129">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d9312-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d9312-130">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="d9312-130">Click New.</span></span>
6. <span data-ttu-id="d9312-131">Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="d9312-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="d9312-132">Sisestage number väljale Galloni hind alates.</span><span class="sxs-lookup"><span data-stu-id="d9312-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="d9312-133">Selles näites saate seadistada välja Galloni hind alates väärtusele 1,95.</span><span class="sxs-lookup"><span data-stu-id="d9312-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="d9312-134">Sisestage number väljale Galloni hind kuni.</span><span class="sxs-lookup"><span data-stu-id="d9312-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="d9312-135">Selles näites saate seadistada välja Galloni hind kuni väärtusele 2.</span><span class="sxs-lookup"><span data-stu-id="d9312-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="d9312-136">Sisestage number väljale Protsent.</span><span class="sxs-lookup"><span data-stu-id="d9312-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="d9312-137">Selles näites saate seadistada protsendi väärtusele 3.</span><span class="sxs-lookup"><span data-stu-id="d9312-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="d9312-138">Klõpsake väljal Valuuta otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d9312-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d9312-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d9312-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="d9312-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d9312-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="d9312-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d9312-141">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]