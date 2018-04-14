--- 
title: "Kaupade vastuvõtu registreerimine ostutellimusel"
description: "See protseduur näitab, kuidas kaupade sissetulekut otse ostutellimusel registreerida."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d8a47dac61705831b330f7b4939a18c865a8ace7
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="3d9de-103">Kaupade vastuvõtu registreerimine ostutellimusel</span><span class="sxs-lookup"><span data-stu-id="3d9de-103">Record the receipt of goods on the purchase order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d9de-104">See protseduur näitab, kuidas kaupade sissetulekut otse ostutellimusel registreerida.</span><span class="sxs-lookup"><span data-stu-id="3d9de-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="3d9de-105">Võimalik on registreerida toote sissetulek ka laos ja siis hiljem ostutellimusel.</span><span class="sxs-lookup"><span data-stu-id="3d9de-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="3d9de-106">Selle toimingu teeb tavaliselt ostuagent või ostureskontro koordinaator.</span><span class="sxs-lookup"><span data-stu-id="3d9de-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="3d9de-107">Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul.</span><span class="sxs-lookup"><span data-stu-id="3d9de-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="3d9de-108">Näites on toimingud lihtsa ostutellimuse koostamiseks, et saaksite esitada protseduuri tegevusjuhisena.</span><span class="sxs-lookup"><span data-stu-id="3d9de-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="3d9de-109">Kui kasutaksite protseduuri oma andmetega, tuleks alustada alamülesandest Kaupade vastuvõtu registreerimine.</span><span class="sxs-lookup"><span data-stu-id="3d9de-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="3d9de-110">Uue ostutellimuse koostamine kaupade vastuvõtmiseks</span><span class="sxs-lookup"><span data-stu-id="3d9de-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="3d9de-111">Avage Hanked > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="3d9de-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="3d9de-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3d9de-112">Click New.</span></span>
3. <span data-ttu-id="3d9de-113">Sisestage väljale Hankija konto väärtus US-101.</span><span class="sxs-lookup"><span data-stu-id="3d9de-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="3d9de-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3d9de-114">Click OK.</span></span>
5. <span data-ttu-id="3d9de-115">Sisestage väljale Kauba kood väärtus M0001.</span><span class="sxs-lookup"><span data-stu-id="3d9de-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="3d9de-116">Sisestage väljale Kogus number 5.</span><span class="sxs-lookup"><span data-stu-id="3d9de-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="3d9de-117">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="3d9de-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="3d9de-118">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="3d9de-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="3d9de-119">Kaupade vastuvõtu salvestamine</span><span class="sxs-lookup"><span data-stu-id="3d9de-119">Record receipt of goods</span></span>
1. <span data-ttu-id="3d9de-120">Klõpsake toimingupaanil valikut Vastuvõtt.</span><span class="sxs-lookup"><span data-stu-id="3d9de-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="3d9de-121">Klõpsake valikut Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="3d9de-121">Click Product receipt.</span></span>
    * <span data-ttu-id="3d9de-122">Koguse väli võimaldab teha erinevaid valikuid koguse kohta, mida soovite vastu võtta.</span><span class="sxs-lookup"><span data-stu-id="3d9de-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="3d9de-123">Näiteks kui kogus on eelnevalt laos registreeritud, võite teha valiku Registreeritud kogus.</span><span class="sxs-lookup"><span data-stu-id="3d9de-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="3d9de-124">Selle näite puhul kasutage väärtust Tellitud kogus.</span><span class="sxs-lookup"><span data-stu-id="3d9de-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="3d9de-125">Sisestage suvaline väärtus väljale Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="3d9de-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="3d9de-126">Seda välja kasutatakse viite sisestamiseks, mida kasutatakse toote sissetuleku töölehe kandena.</span><span class="sxs-lookup"><span data-stu-id="3d9de-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="3d9de-127">Laiendage jaotist Read.</span><span class="sxs-lookup"><span data-stu-id="3d9de-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="3d9de-128">Määrake koguse väärtuseks 4.</span><span class="sxs-lookup"><span data-stu-id="3d9de-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="3d9de-129">Siin saate määrata käsitsi koguse, mida iga tellimuse rea puhul vastu võetakse.</span><span class="sxs-lookup"><span data-stu-id="3d9de-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="3d9de-130">Ahendage jaotist Read.</span><span class="sxs-lookup"><span data-stu-id="3d9de-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="3d9de-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3d9de-131">Click OK.</span></span>
    * <span data-ttu-id="3d9de-132">Kaup on nüüd ostutellimusel vastuvõetuks registreeritud ja seda kajastava dokumendina on loodud toote sissetuleku tööleht.</span><span class="sxs-lookup"><span data-stu-id="3d9de-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="3d9de-133">Saate kasutada toimingut Toote sissetulek ostutellimuse juurde loodud töölehtede ülevaatamiseks, et näha, mis millal vastu võeti.</span><span class="sxs-lookup"><span data-stu-id="3d9de-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


