---
title: Tellimuste ooteloleku haldamine
description: See protseduur näitab, kuidas seada kliendi müügitellimusi ootele, kuidas töötada ootel tellimuse väljaregistreerimisega ja kuidas tellimuse ootelolekut eemaldada.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7168d13ef0b24d06aa28fbbc22bbb4e6093df24
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/11/2019
ms.locfileid: "1994906"
---
# <a name="manage-order-holds"></a><span data-ttu-id="2fcb5-103">Tellimuste ooteloleku haldamine</span><span class="sxs-lookup"><span data-stu-id="2fcb5-103">Manage order holds</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2fcb5-104">See protseduur näitab, kuidas seada kliendi müügitellimusi ootele, kuidas töötada ootel tellimuse väljaregistreerimisega ja kuidas tellimuse ootelolekut eemaldada.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="2fcb5-105">Tellimus võidakse ootele panna mitmel põhjusel.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="2fcb5-106">Näiteks võidakse tellimus ootele panna seni, kuni kliendi aadressi või makseviisi saab kinnitada või kuni haldur saab kliendi krediidilimiidi üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="2fcb5-107">Kui tellimus on ootel, ei saa ladu seda lähetamiseks töödelda.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="2fcb5-108">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="2fcb5-109">Tellimuse ootelolekute häälestamine</span><span class="sxs-lookup"><span data-stu-id="2fcb5-109">Set up order holds</span></span>
1. <span data-ttu-id="2fcb5-110">Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Häälestamine > Müügitellimused > Tellimuse ooteloleku koodid**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="2fcb5-111">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-111">Click **New**.</span></span>
3. <span data-ttu-id="2fcb5-112">Tippige väärtus väljale **Ooteloleku kood**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="2fcb5-113">Näiteks tippige „Helista tagasi”.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="2fcb5-114">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="2fcb5-115">Näiteks Kliendi tagasihelistuse ootel hoitav tellimus.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="2fcb5-116">Valikuliselt valige märkeruut **Eemalda reserveeringud**, et selle ooteloleku koodi lisamisel eemaldada tellimuselt mis tahes füüsilised reserveerimised.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="2fcb5-117">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="2fcb5-118">Tellimuse ootele seadmine</span><span class="sxs-lookup"><span data-stu-id="2fcb5-118">Place order on hold</span></span>
1. <span data-ttu-id="2fcb5-119">Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Müügitellimused > Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="2fcb5-120">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-120">Click **New**.</span></span>
3. <span data-ttu-id="2fcb5-121">Väljale **Kliendi konto** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="2fcb5-122">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-122">Click **OK**.</span></span>
5. <span data-ttu-id="2fcb5-123">Sisestage või valige väärtus väljale **Kauba kood**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="2fcb5-124">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="2fcb5-125">Klõpsake **Tegevuspaanil** valikut **Müügitellimus**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="2fcb5-126">Klõpsake nuppu **Ootelolevad tellimused**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="2fcb5-127">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-127">Click **New**.</span></span>
10. <span data-ttu-id="2fcb5-128">Väljal **Ooteloleku kood** valige eelmises alamülesandes loodud kood.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="2fcb5-129">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-129">Click **Save**.</span></span>
12. <span data-ttu-id="2fcb5-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-130">Close the page.</span></span>
13. <span data-ttu-id="2fcb5-131">Avage **Müük ja turundus > Müügitellimused > Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="2fcb5-132">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-132">In the list, mark the selected row.</span></span> <span data-ttu-id="2fcb5-133">Praegu ootelolevatel tellimustel on väljad „Ära töötle” ja „Pane ootele” märgitud.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="2fcb5-134">Klõpsake tegevuspaanil valikut **Komplekteerimine ja pakkimine.**</span><span class="sxs-lookup"><span data-stu-id="2fcb5-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="2fcb5-135">Tellimuste ooteloleku haldamine</span><span class="sxs-lookup"><span data-stu-id="2fcb5-135">Manage order holds</span></span>
1. <span data-ttu-id="2fcb5-136">Avage **Müük ja turundus > Müügitellimused > Avatud tellimused > Ootelolevad tellimused**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="2fcb5-137">**Ootelolevate tellimuste** lehekülg funktsioneerib töölauana, kus saate hankida ülevaate kõigist praegustest ja töödeldud ootelolekutest ning käsitleda neid ja seotud müügitellimusi.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="2fcb5-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2fcb5-139">**Tegumiribal** klõpsake nuppu **Väljaregistreerimise ootelepanek**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="2fcb5-140">Klõpsake nuppu **Registreeri välja**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-140">Click **Check out**.</span></span>
5. <span data-ttu-id="2fcb5-141">Eemaldage loendis valitud realt märge.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="2fcb5-142">Väli **Väljaregistreerimine** näitab nüüd teie kasutaja ID-d.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="2fcb5-143">Klõpsake nuppu **Tühjenda väljaregistreerimine**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="2fcb5-144">**Tegumiribal** klõpsake nuppu **Eemalda ootelolek**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="2fcb5-145">Kui olete valmis ooteloleku eemaldama ja lubama tellimusel järgmisesse täitmise etappi liikuda, peate ooteloleku tühistama.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="2fcb5-146">Kui tellimus ei nõua muudatuste tegemist, saate käivitada toimingu Tühjenda ootelolekud.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="2fcb5-147">Siiski saate kasutada toimingut Eemalda ja muuda, kui pärast ooteloleku tühistamist tuleb tellimust värskendada.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="2fcb5-148">Toiming **Eemalda ja saada** on kohaldatav ainult siis, kui kasutate kõnekeskuse funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="2fcb5-149">Klõpsake nuppu **Tühjenda ootelolekud**.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-149">Click **Clear holds**.</span></span> <span data-ttu-id="2fcb5-150">Ootelolek on nüüd tellimusest ja aktiivsete ootelolekute loendist eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="2fcb5-151">Nägemaks kõiki ootelolekuid ja nende alamkogumit konkreetse oleku järgi, muutke välja Kuva väärtust.</span><span class="sxs-lookup"><span data-stu-id="2fcb5-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

