---
title: Kaupade vastuvõtu registreerimine ostutellimusel
description: See protseduur näitab, kuidas kaupade sissetulekut otse ostutellimusel registreerida.
author: mkirknel
manager: tfehr
ms.date: 07/09/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6365ccf4414e49bc1f22bcedb42f192c5c9a5ee8
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207619"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="6b834-103">Kaupade vastuvõtu registreerimine ostutellimusel</span><span class="sxs-lookup"><span data-stu-id="6b834-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b834-104">See protseduur näitab, kuidas kaupade sissetulekut otse ostutellimusel registreerida.</span><span class="sxs-lookup"><span data-stu-id="6b834-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="6b834-105">Võimalik on registreerida toote sissetulek ka laos ja siis hiljem kirjendada ostutellimusel.</span><span class="sxs-lookup"><span data-stu-id="6b834-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="6b834-106">Selle toimingu teeb tavaliselt ostuagent või ostureskontro koordinaator.</span><span class="sxs-lookup"><span data-stu-id="6b834-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="6b834-107">Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul.</span><span class="sxs-lookup"><span data-stu-id="6b834-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="6b834-108">Näites on toimingud lihtsa ostutellimuse koostamiseks, et saaksite esitada protseduuri tegevusjuhisena.</span><span class="sxs-lookup"><span data-stu-id="6b834-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="6b834-109">Kui kasutaksite protseduuri oma andmetega, tuleks alustada alamülesandest **Kaupade vastuvõtu registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="6b834-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="6b834-110">Uue ostutellimuse koostamine kaupade vastuvõtmiseks</span><span class="sxs-lookup"><span data-stu-id="6b834-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="6b834-111">Minge **navigeerimispaanile > Moodulid > Hange ja hankimine > Ostutellimused > Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="6b834-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="6b834-112">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6b834-112">Select **New**.</span></span>
3. <span data-ttu-id="6b834-113">Väljale **Tarnija konto** sisestage `US-101`.</span><span class="sxs-lookup"><span data-stu-id="6b834-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="6b834-114">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b834-114">Select **OK**.</span></span>
5. <span data-ttu-id="6b834-115">Väljale **Kauba kood** sisestage `M0001`.</span><span class="sxs-lookup"><span data-stu-id="6b834-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="6b834-116">Väljale **Kogus** sisestage `5`.</span><span class="sxs-lookup"><span data-stu-id="6b834-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="6b834-117">Valige toimingupaanil **Ostmine**.</span><span class="sxs-lookup"><span data-stu-id="6b834-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="6b834-118">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="6b834-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="6b834-119">Kaupade vastuvõtu salvestamine</span><span class="sxs-lookup"><span data-stu-id="6b834-119">Record receipt of goods</span></span>
1. <span data-ttu-id="6b834-120">Valige toimingupaanil **Vastuvõtmine**.</span><span class="sxs-lookup"><span data-stu-id="6b834-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="6b834-121">**Valige toote** sissetulek.</span><span class="sxs-lookup"><span data-stu-id="6b834-121">Select **Product receipt**.</span></span> <span data-ttu-id="6b834-122">**Koguse** väli võimaldab teha erinevaid valikuid koguse kohta, mida soovite vastu võtta.</span><span class="sxs-lookup"><span data-stu-id="6b834-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="6b834-123">Näiteks kui kogus on eelnevalt laos registreeritud, võite teha valiku **Registreeritud kogus**.</span><span class="sxs-lookup"><span data-stu-id="6b834-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="6b834-124">Selle näite puhul kasutage väärtust **Tellitud kogus**.</span><span class="sxs-lookup"><span data-stu-id="6b834-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="6b834-125">Laiendage jaotist **Ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="6b834-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="6b834-126">**Sisestage suvaline väärtus väljale Toote sissetulek.**</span><span class="sxs-lookup"><span data-stu-id="6b834-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="6b834-127">Seda välja kasutatakse viite sisestamiseks, mida kasutatakse toote sissetuleku töölehe kandena.</span><span class="sxs-lookup"><span data-stu-id="6b834-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="6b834-128">Laiendage jaotist **Read**.</span><span class="sxs-lookup"><span data-stu-id="6b834-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="6b834-129">Määrake **Koguse** väärtuseks 4.</span><span class="sxs-lookup"><span data-stu-id="6b834-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="6b834-130">Siin saate määrata käsitsi koguse, mida iga tellimuse rea puhul vastu võetakse.</span><span class="sxs-lookup"><span data-stu-id="6b834-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="6b834-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="6b834-131">Select **OK**.</span></span> <span data-ttu-id="6b834-132">Kaup on nüüd ostutellimusel vastuvõetuks registreeritud ja seda kajastava dokumendina on loodud toote sissetuleku tööleht.</span><span class="sxs-lookup"><span data-stu-id="6b834-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="6b834-133">Saate kasutada toimingut Toote sissetulek ostutellimuse juurde loodud töölehtede ülevaatamiseks, et näha, mis millal vastu võeti.</span><span class="sxs-lookup"><span data-stu-id="6b834-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

