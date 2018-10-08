--- 
title: Varude saadavuse kontrollimine
description: "See protseduur näitab, kuidas kontrollida vaba kaubavaru ja füüsilist vaba kaubavaru kindla kaubakoodi puhul."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand
audience: Application User
ms.reviewer: 
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 657c19896b20a514dc5308bf7fb086085b482fec
ms.openlocfilehash: 26a8f51eda1f4249862a23fa0103b7a144d974a1
ms.contentlocale: et-ee
ms.lasthandoff: 10/08/2018

---
# <a name="check-the-availability-of-stock"></a><span data-ttu-id="c9628-103">Varude saadavuse kontrollimine</span><span class="sxs-lookup"><span data-stu-id="c9628-103">Check the availability of stock</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9628-104">See protseduur näitab, kuidas kontrollida vaba kaubavaru ja füüsilist vaba kaubavaru kindla kaubakoodi puhul.</span><span class="sxs-lookup"><span data-stu-id="c9628-104">This procedure shows you how to check on-hand and physical on-hand inventory for a specific item number.</span></span> <span data-ttu-id="c9628-105">Samuti näitab see, kuidas hankida kaubaga seotud tarneteavet.</span><span class="sxs-lookup"><span data-stu-id="c9628-105">It also shows you how to get supply information related to an item.</span></span> <span data-ttu-id="c9628-106">Füüsiline vaba kaubavaru on vaba kaubavaru, mis on saadaval – s.t see on ostetud, vastu võetud ja registreeritud.</span><span class="sxs-lookup"><span data-stu-id="c9628-106">Physical on-hand inventory is the on-hand inventory that’s available – that is, it’s purchased, received and registered.</span></span> <span data-ttu-id="c9628-107">Vaba kaubavaru sisaldab saadaolevat vaba kaubavaru, kuid ka varusid, mis on tellitud ja mida oodatakse, aga mida pole veel vastu võetud või registreeritud.</span><span class="sxs-lookup"><span data-stu-id="c9628-107">On-hand inventory includes the available on-hand inventory, but also the inventory that’s been ordered and is expected, but not yet received or registered.</span></span> <span data-ttu-id="c9628-108">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="c9628-108">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="c9628-109">USMF-i kasutamisel saate kasutada kuvatavaid näidisväärtusi.</span><span class="sxs-lookup"><span data-stu-id="c9628-109">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="c9628-110">Neid ülesandeid täidab üldjuhul laotöötaja.</span><span class="sxs-lookup"><span data-stu-id="c9628-110">These tasks would typically be carried out by a warehouse worker.</span></span>


## <a name="check-on-hand-inventory-for-an-item"></a><span data-ttu-id="c9628-111">Kauba vaba kaubavaru kontrollimine</span><span class="sxs-lookup"><span data-stu-id="c9628-111">Check on-hand inventory for an item</span></span>
1. <span data-ttu-id="c9628-112">Avage Laohaldus > Päringud ja aruanded > Vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="c9628-112">Go to Inventory management > Inquiries and reports > On-hand inventory.</span></span>
2. <span data-ttu-id="c9628-113">Valige kaubakoodi rida.</span><span class="sxs-lookup"><span data-stu-id="c9628-113">Select the Item number row.</span></span>
    * <span data-ttu-id="c9628-114">Vaba kaubavaru päringute esitamiseks kaubakoodi alusel valige rida, kus tabel on seatud vabale kaubavarule ja väli on seatud kaubakoodile.</span><span class="sxs-lookup"><span data-stu-id="c9628-114">To query the on-hand inventory by item number, select the row where the Table is set to On-hand inventory and Field is set to Item number.</span></span>  
3. <span data-ttu-id="c9628-115">Valige väljal Kriteeriumid kaup, mille puhul soovite päringu esitada.</span><span class="sxs-lookup"><span data-stu-id="c9628-115">In the Criteria field, select the item you want to query.</span></span>
    * <span data-ttu-id="c9628-116">Ettevõtte USMF demoandmete kasutamisel võite valida väärtuse M9201.</span><span class="sxs-lookup"><span data-stu-id="c9628-116">If you're using the USMF demo data company, you can select 'M9201'.</span></span>  
4. <span data-ttu-id="c9628-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c9628-117">Click OK.</span></span>
5. <span data-ttu-id="c9628-118">Klõpsake valikut Dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="c9628-118">Click Dimensions.</span></span>
    * <span data-ttu-id="c9628-119">Vahekaart Dimensioonid võimaldab valida, kui palju üksikasju soovite vaba kaubavaru kohta vaadata.</span><span class="sxs-lookup"><span data-stu-id="c9628-119">The Dimensions tab allows you select how much detail you want to see about your on-hand inventory.</span></span> <span data-ttu-id="c9628-120">Kui teil on vaja reserveerimisega seotud andmeid, peate kuvama kõik täiustatud laotoimingute (WHS) protsesse kasutavate kaupade varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="c9628-120">If you need data related to reservation, you must display all inventory dimensions for the items that use advanced warehouse (WHS) processes.</span></span>  
6. <span data-ttu-id="c9628-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c9628-121">Click OK.</span></span>
7. <span data-ttu-id="c9628-122">Klõpsake toimingupaanil suvandit Seotud teave.</span><span class="sxs-lookup"><span data-stu-id="c9628-122">On the Action Pane, click Related information.</span></span>
    * <span data-ttu-id="c9628-123">Kui seda ei kuvata, võib teil olla vaja toimingupaani täiendavate suvandite nägemiseks klõpsata kolmikpunkti nuppu (...).</span><span class="sxs-lookup"><span data-stu-id="c9628-123">If you don’t see this, you may need to click on the Ellipsis button (…) to see additional action pane options.</span></span>  
8. <span data-ttu-id="c9628-124">Klõpsake suvandit Tarne ülevaade.</span><span class="sxs-lookup"><span data-stu-id="c9628-124">Click Supply overview.</span></span>
    * <span data-ttu-id="c9628-125">Vahekaart Tarne ülevaade pakub tarneteavet kindla kauba, nagu laoseisu koguse, täitmisaja ja hankijateabe kohta.</span><span class="sxs-lookup"><span data-stu-id="c9628-125">The Supply overview tab provides supply information for a specific item, such as the quantity on-hand, the lead time, and vendor information.</span></span>  
9. <span data-ttu-id="c9628-126">Laiendage jaotist Laoseis.</span><span class="sxs-lookup"><span data-stu-id="c9628-126">Expand the On-hand section.</span></span>
10. <span data-ttu-id="c9628-127">Laiendage jaotist Hankijad.</span><span class="sxs-lookup"><span data-stu-id="c9628-127">Expand the Vendors section.</span></span>
11. <span data-ttu-id="c9628-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c9628-128">Close the page.</span></span>
12. <span data-ttu-id="c9628-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c9628-129">Close the page.</span></span>

## <a name="check-physical-on-hand-inventory"></a><span data-ttu-id="c9628-130">Füüsilise vaba kaubavaru kontrollimine</span><span class="sxs-lookup"><span data-stu-id="c9628-130">Check physical on-hand inventory</span></span>
1. <span data-ttu-id="c9628-131">Avage Laohaldus > Päringud ja aruanded > Füüsiline vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="c9628-131">Go to Warehouse management > Inquiries and reports > Physical on-hand inventory.</span></span>
2. <span data-ttu-id="c9628-132">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="c9628-132">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="c9628-133">Saate kasutada välju Sait ja Ladu kaupade loendi filtrimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9628-133">You can use the Site and Warehouse fields to filter the list of items.</span></span>  
3. <span data-ttu-id="c9628-134">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="c9628-134">Refresh the page.</span></span>
4. <span data-ttu-id="c9628-135">Klõpsake suvandit Dimensioonide kuvamine.</span><span class="sxs-lookup"><span data-stu-id="c9628-135">Click Display Dimensions.</span></span>
    * <span data-ttu-id="c9628-136">Vahekaart Dimensioonide kuvamine võimaldab teil valida, kui palju üksikasju soovite vaba kaubavaru kohta vaadata.</span><span class="sxs-lookup"><span data-stu-id="c9628-136">The Dimensions Display tab allows you select how much detail you want to see about your on-hand inventory.</span></span>  
5. <span data-ttu-id="c9628-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c9628-137">Click OK.</span></span>
6. <span data-ttu-id="c9628-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c9628-138">Close the page.</span></span>

## <a name="check-on-hand-inventory-by-location"></a><span data-ttu-id="c9628-139">Vaba kaubavaru kontrollimine asukoha järgi</span><span class="sxs-lookup"><span data-stu-id="c9628-139">Check on-hand inventory by location</span></span>
1. <span data-ttu-id="c9628-140">Avage Laohaldus > Päringud ja aruanded > Vaba kaubavaru asukoha järgi.</span><span class="sxs-lookup"><span data-stu-id="c9628-140">Go to Warehouse management > Inquiries and reports > On hand by location.</span></span>
2. <span data-ttu-id="c9628-141">Sisestage väärtus väljale Ladu.</span><span class="sxs-lookup"><span data-stu-id="c9628-141">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="c9628-142">Ettevõtte USMF demoandmete kasutamisel saate kasutada suvandit 51.</span><span class="sxs-lookup"><span data-stu-id="c9628-142">If you're using the USMF demo data company, you can use '51'.</span></span>  
3. <span data-ttu-id="c9628-143">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="c9628-143">Refresh the page.</span></span>
4. <span data-ttu-id="c9628-144">Klõpsake suvandit Dimensioonide kuvamine.</span><span class="sxs-lookup"><span data-stu-id="c9628-144">Click Display Dimensions.</span></span>
5. <span data-ttu-id="c9628-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c9628-145">Click OK.</span></span>
6. <span data-ttu-id="c9628-146">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c9628-146">Close the page.</span></span>


