---
title: Vedaja kütuseindeksi seadistamine
description: See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.
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
ms.openlocfilehash: b6f72de7ad54a2b2dc1bf40fd8cb86d8b055e2d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "366577"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="ecec7-103">Vedaja kütuseindeksi seadistamine</span><span class="sxs-lookup"><span data-stu-id="ecec7-103">Set up a carrier fuel index</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ecec7-104">See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.</span><span class="sxs-lookup"><span data-stu-id="ecec7-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="ecec7-105">Kütuseindeksi regioon määrab, millisele regioonile tuleks kütuseindeksit rakendada ja kütuseindeks määrab kütuse hinna teatud aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="ecec7-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="ecec7-106">Kütusehinna muudatuste kajastamiseks aja jooksul saate vedajaga seostada mitu kütuseindeksit.</span><span class="sxs-lookup"><span data-stu-id="ecec7-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="ecec7-107">Neid ülesandeid teeb üldjuhul transpordikoordinaator.</span><span class="sxs-lookup"><span data-stu-id="ecec7-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="ecec7-108">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="ecec7-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="ecec7-109">Kütuseindeksi regiooni loomine</span><span class="sxs-lookup"><span data-stu-id="ecec7-109">Create a fuel index region</span></span>
1. <span data-ttu-id="ecec7-110">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksi regioonid.</span><span class="sxs-lookup"><span data-stu-id="ecec7-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="ecec7-111">Esmalt peate looma erinevad regioonid, kus töötada, ja arvutama erinevad kütuse lisatasud.</span><span class="sxs-lookup"><span data-stu-id="ecec7-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="ecec7-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ecec7-112">Click New.</span></span>
3. <span data-ttu-id="ecec7-113">Sisestage väärtus väljale Regioon.</span><span class="sxs-lookup"><span data-stu-id="ecec7-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="ecec7-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="ecec7-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ecec7-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ecec7-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="ecec7-116">Saate luua ka kütuseindeks</span><span class="sxs-lookup"><span data-stu-id="ecec7-116">Create a fuel index</span></span>
1. <span data-ttu-id="ecec7-117">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksid.</span><span class="sxs-lookup"><span data-stu-id="ecec7-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="ecec7-118">Seadistatud regioonide puhul peate sisestama kütuse praegused hinnad.</span><span class="sxs-lookup"><span data-stu-id="ecec7-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="ecec7-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ecec7-119">Click New.</span></span>
3. <span data-ttu-id="ecec7-120">Klõpsake väljal Regioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ecec7-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ecec7-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ecec7-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ecec7-122">Sisestage number väljale Galloni hind.</span><span class="sxs-lookup"><span data-stu-id="ecec7-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="ecec7-123">Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="ecec7-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="ecec7-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ecec7-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="ecec7-125">Vedaja kütuseindeksi loomine</span><span class="sxs-lookup"><span data-stu-id="ecec7-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="ecec7-126">Avage Transpordihaldus > Seadistus > Kütuseindeksid > Vedaja kütuseindeksid.</span><span class="sxs-lookup"><span data-stu-id="ecec7-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="ecec7-127">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ecec7-127">Click New.</span></span>
3. <span data-ttu-id="ecec7-128">Sisestage väärtus väljale Vedaja kütuseindeks.</span><span class="sxs-lookup"><span data-stu-id="ecec7-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="ecec7-129">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ecec7-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ecec7-130">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="ecec7-130">Click New.</span></span>
6. <span data-ttu-id="ecec7-131">Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="ecec7-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="ecec7-132">Sisestage number väljale Galloni hind alates.</span><span class="sxs-lookup"><span data-stu-id="ecec7-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="ecec7-133">Selles näites saate seadistada välja Galloni hind alates väärtusele 1,95.</span><span class="sxs-lookup"><span data-stu-id="ecec7-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="ecec7-134">Sisestage number väljale Galloni hind kuni.</span><span class="sxs-lookup"><span data-stu-id="ecec7-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="ecec7-135">Selles näites saate seadistada välja Galloni hind kuni väärtusele 2.</span><span class="sxs-lookup"><span data-stu-id="ecec7-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="ecec7-136">Sisestage number väljale Protsent.</span><span class="sxs-lookup"><span data-stu-id="ecec7-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="ecec7-137">Selles näites saate seadistada protsendi väärtusele 3.</span><span class="sxs-lookup"><span data-stu-id="ecec7-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="ecec7-138">Klõpsake väljal Valuuta otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ecec7-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="ecec7-139">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ecec7-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ecec7-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ecec7-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="ecec7-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ecec7-141">Click Save.</span></span>

