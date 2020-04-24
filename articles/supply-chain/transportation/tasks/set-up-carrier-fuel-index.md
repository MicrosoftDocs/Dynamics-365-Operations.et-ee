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
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69bf6e3a896e560b1dbb96c8f997f6ee8dbb9ec1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214914"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="15b41-103">Vedaja kütuseindeksi seadistamine</span><span class="sxs-lookup"><span data-stu-id="15b41-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15b41-104">See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.</span><span class="sxs-lookup"><span data-stu-id="15b41-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="15b41-105">Kütuseindeksi regioon määrab, millisele regioonile tuleks kütuseindeksit rakendada ja kütuseindeks määrab kütuse hinna teatud aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="15b41-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="15b41-106">Kütusehinna muudatuste kajastamiseks aja jooksul saate vedajaga seostada mitu kütuseindeksit.</span><span class="sxs-lookup"><span data-stu-id="15b41-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="15b41-107">Neid ülesandeid teeb üldjuhul transpordikoordinaator.</span><span class="sxs-lookup"><span data-stu-id="15b41-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="15b41-108">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="15b41-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="15b41-109">Kütuseindeksi regiooni loomine</span><span class="sxs-lookup"><span data-stu-id="15b41-109">Create a fuel index region</span></span>
1. <span data-ttu-id="15b41-110">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksi regioonid.</span><span class="sxs-lookup"><span data-stu-id="15b41-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="15b41-111">Esmalt peate looma erinevad regioonid, kus töötada, ja arvutama erinevad kütuse lisatasud.</span><span class="sxs-lookup"><span data-stu-id="15b41-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="15b41-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="15b41-112">Click New.</span></span>
3. <span data-ttu-id="15b41-113">Sisestage väärtus väljale Regioon.</span><span class="sxs-lookup"><span data-stu-id="15b41-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="15b41-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="15b41-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="15b41-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="15b41-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="15b41-116">Saate luua ka kütuseindeks</span><span class="sxs-lookup"><span data-stu-id="15b41-116">Create a fuel index</span></span>
1. <span data-ttu-id="15b41-117">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksid.</span><span class="sxs-lookup"><span data-stu-id="15b41-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="15b41-118">Seadistatud regioonide puhul peate sisestama kütuse praegused hinnad.</span><span class="sxs-lookup"><span data-stu-id="15b41-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="15b41-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="15b41-119">Click New.</span></span>
3. <span data-ttu-id="15b41-120">Klõpsake väljal Regioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="15b41-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="15b41-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="15b41-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="15b41-122">Sisestage number väljale Galloni hind.</span><span class="sxs-lookup"><span data-stu-id="15b41-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="15b41-123">Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="15b41-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="15b41-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="15b41-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="15b41-125">Vedaja kütuseindeksi loomine</span><span class="sxs-lookup"><span data-stu-id="15b41-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="15b41-126">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Vedaja kütuseindeksid.</span><span class="sxs-lookup"><span data-stu-id="15b41-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="15b41-127">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="15b41-127">Click New.</span></span>
3. <span data-ttu-id="15b41-128">Sisestage väärtus väljale Vedaja kütuseindeks.</span><span class="sxs-lookup"><span data-stu-id="15b41-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="15b41-129">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="15b41-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="15b41-130">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="15b41-130">Click New.</span></span>
6. <span data-ttu-id="15b41-131">Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="15b41-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="15b41-132">Sisestage number väljale Galloni hind alates.</span><span class="sxs-lookup"><span data-stu-id="15b41-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="15b41-133">Selles näites saate seadistada välja Galloni hind alates väärtusele 1,95.</span><span class="sxs-lookup"><span data-stu-id="15b41-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="15b41-134">Sisestage number väljale Galloni hind kuni.</span><span class="sxs-lookup"><span data-stu-id="15b41-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="15b41-135">Selles näites saate seadistada välja Galloni hind kuni väärtusele 2.</span><span class="sxs-lookup"><span data-stu-id="15b41-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="15b41-136">Sisestage number väljale Protsent.</span><span class="sxs-lookup"><span data-stu-id="15b41-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="15b41-137">Selles näites saate seadistada protsendi väärtusele 3.</span><span class="sxs-lookup"><span data-stu-id="15b41-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="15b41-138">Klõpsake väljal Valuuta otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="15b41-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="15b41-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="15b41-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="15b41-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="15b41-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="15b41-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="15b41-141">Click Save.</span></span>

