---
title: "Väljaminev protsess"
description: "Selles teemas antakse ülevaade väljaminevast protsessist moodulis Laohaldus."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: et-ee
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a><span data-ttu-id="346a7-103">Väljaminev protsess</span><span class="sxs-lookup"><span data-stu-id="346a7-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="346a7-104">Selles teemas antakse ülevaade väljaminevast protsessist moodulis Laohaldus.</span><span class="sxs-lookup"><span data-stu-id="346a7-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="346a7-105">Väljaminekuorderid</span><span class="sxs-lookup"><span data-stu-id="346a7-105">Output orders</span></span>

<span data-ttu-id="346a7-106">Müügitellimuse ridade ja üleviimistellimuse ridade seostamiseks komplekteerimislehti kasutavate väljaminevate komplekteerimisprotsessidega kasutatakse väljaminekuordereid.</span><span class="sxs-lookup"><span data-stu-id="346a7-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="346a7-107">Komplekteerimislehtede loomisel müügitellimustest või üleviimistellimustest luuakse automaatselt väljaminekuorderid ja saadetised.</span><span class="sxs-lookup"><span data-stu-id="346a7-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="346a7-108">Komplekteerimislehel on saadetisega üks-ühele suhe.</span><span class="sxs-lookup"><span data-stu-id="346a7-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="346a7-109">Saadetisest saab töödelda üleviimistellimuse saadetise või müügitellimuse saatelehe.</span><span class="sxs-lookup"><span data-stu-id="346a7-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="346a7-110">Järgmisel joonisel on antud ülevaade väljaminekuorderite protsessist.</span><span class="sxs-lookup"><span data-stu-id="346a7-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="346a7-111">[![Ülevaade väljaminekuorderi protsessist](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="346a7-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="346a7-112">Saate seadistada lähetusreeglid, et määratleda, kuidas programm peaks lähetusprotsessi käsitsema.</span><span class="sxs-lookup"><span data-stu-id="346a7-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="346a7-113">Seejärel saab nende reeglite abil lähetusprotsessi juhtida.</span><span class="sxs-lookup"><span data-stu-id="346a7-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="346a7-114">Konkreetsemalt võite kasutada neid reegleid juhtimiseks, millise protsessietapi jooksul saadetis tuleks välja saata.</span><span class="sxs-lookup"><span data-stu-id="346a7-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="346a7-115">Järgmised sätted määratlevad, kuidas väljaminevaid protsesse käsitsetakse.</span><span class="sxs-lookup"><span data-stu-id="346a7-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="346a7-116">Müügi- ja üleviimistellimuste komplekteerimisprotsessi olek</span><span class="sxs-lookup"><span data-stu-id="346a7-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="346a7-117">Avage **Ostureskontro** \> **Seadistus** \> **Ostureskontro parameetrid** ja valige siis vahekaardi **Värskendused** väljalt **Komplekteerimisprotsessi olek** väärtus.</span><span class="sxs-lookup"><span data-stu-id="346a7-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="346a7-118">[![Müügitellimuste komplekteerimisprotsessi oleku väli](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="346a7-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="346a7-119">Kui välja **Komplekteerimisprotsessi olek** väärtuseks on määratud **Lõpule viidud**, toimub komplekteerimisprotsess komplekteerimislehtede koostamise protsessi raames automaatselt.</span><span class="sxs-lookup"><span data-stu-id="346a7-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="346a7-120">Kui välja väärtuseks on määratud **Aktiveeritud**, tuleb komplekteerimislehe read käsitsi värskendada.</span><span class="sxs-lookup"><span data-stu-id="346a7-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="346a7-121">Sama puudutab üleviimistellimusi.</span><span class="sxs-lookup"><span data-stu-id="346a7-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="346a7-122">Avage **Varude haldus** \> **Seadistus** \> **Varude ja laohalduse parameetrid** ja valige siis vahekaardi **Transport** väljalt **Komplekteerimisprotsessi olek** väärtus.</span><span class="sxs-lookup"><span data-stu-id="346a7-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="346a7-123">[![Üleviimistellimuste komplekteerimisprotsessi oleku väli](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="346a7-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="346a7-124">Väljamineku laoorderite lõpetamine</span><span class="sxs-lookup"><span data-stu-id="346a7-124">End output inventory orders</span></span>

<span data-ttu-id="346a7-125">Avage **Varude haldus** \> **Seadistus** \> **Varude ja laohalduse parameetrid** ja määrake siis vahekaardil **Üldine** valik **Lõpeta väljamineku laoorder**.</span><span class="sxs-lookup"><span data-stu-id="346a7-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="346a7-126">[![Valik Lõpeta väljamineku laoorder](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="346a7-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="346a7-127">Mõnikord ei saa varude hulgas mõningaid kaupu komplekteerimislehe protsessi käigus komplekteerida.</span><span class="sxs-lookup"><span data-stu-id="346a7-127">Sometimes, some items in inventory can't be picked as part of the picking list process.</span></span> <span data-ttu-id="346a7-128">Näiteks võib selline olukord tekkida juhul, kui laotöötaja vähendab komplekteerimisridadel olevaid koguseid ja töötleb komplekteerimislehte.</span><span class="sxs-lookup"><span data-stu-id="346a7-128">For example, this situation might occur if a warehouse worker reduces the quantities on picking lines and processes the picking list.</span></span> <span data-ttu-id="346a7-129">Kui valiku **Lõpeta väljamineku laoorder** väärtuseks on määratud **Jah**, registreeritakse ülejäänud komplekteerimata kogused uuesti tellimuse tasandil.</span><span class="sxs-lookup"><span data-stu-id="346a7-129">If the **End output inventory order** option is set to **Yes**, the remaining unpicked quantities are reported back to the order level.</span></span> <span data-ttu-id="346a7-130">Kui valiku väärtuseks on määratud **Ei**, hoitakse ülejäänud komplekteerimata koguseid avatud väljaminekuorderi kogusena.</span><span class="sxs-lookup"><span data-stu-id="346a7-130">If the option is set to **No**, the remaining unpicked quantities are kept as an open output order quantity.</span></span> <span data-ttu-id="346a7-131">Sellisel juhul jäävad need kogused lattu väljastatuks ja need tuleb lisada uuele komplekteerimislehele funktsiooni **Ava väljaminekuorderid** osana.</span><span class="sxs-lookup"><span data-stu-id="346a7-131">In this case, the quantities remain released to the warehouse and must be added to a new picking list as part of the **Open output orders** functionality.</span></span>

<span data-ttu-id="346a7-132">[![Käsk Ava väljaminekuorderid menüüs Funktsioonid](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="346a7-132">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="346a7-133">[![Lehe Ava väljaminekuorderid menüü Funktsioonid](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="346a7-133">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="346a7-134">Vähenda kogust</span><span class="sxs-lookup"><span data-stu-id="346a7-134">Reduce quantity</span></span>

<span data-ttu-id="346a7-135">Kolmas parameeter, mida saate komplekteerimislehe koostamise raames kasutada, on parameeter **Vähenda kogust**.</span><span class="sxs-lookup"><span data-stu-id="346a7-135">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="346a7-136">Selle parameetri seadistus toimib koos sättega **Reserveerimine**, mis käivitab lattu väljastamise raames reserveerimisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="346a7-136">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="346a7-137">[![Parameeter Vähenda kogust](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="346a7-137">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="346a7-138">Müügitellimuse väljamineva protsessi näide</span><span class="sxs-lookup"><span data-stu-id="346a7-138">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="346a7-139">Selle näite puhul on olemas müügitellimus kahele kaubale.</span><span class="sxs-lookup"><span data-stu-id="346a7-139">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="346a7-140">Komplekteerimislehe koostamise ajal tuleb valida parameeter **Vähenda kogust**.</span><span class="sxs-lookup"><span data-stu-id="346a7-140">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="346a7-141">Seetõttu vabastate ja loote komplekteerimisread ainult vabale kaubavarule.</span><span class="sxs-lookup"><span data-stu-id="346a7-141">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="346a7-142">Komplekteerimine tuleb registreerida komplekteerimislehtede registreerimisprotsessi kaudu (**Komplekteerimisprotsessi olek** = **Aktiveeritud**).</span><span class="sxs-lookup"><span data-stu-id="346a7-142">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="346a7-143">Veel reserveerimata kaubavaru reserveeritakse komplekteerimislehe koostamise käigus.</span><span class="sxs-lookup"><span data-stu-id="346a7-143">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="346a7-144">Kaubavaru, mis pole saadaval, võib müügitellimusest eemaldada või väljastada lattu väljamineku töötlemiseks hiljem, kui varud on komplekteerimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="346a7-144">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="346a7-145">[![Komplekteerimislehe värskendamine](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="346a7-145">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="346a7-146">Kohe, kui kõik komplekteerimisread on lehel **Komplekteerimislehe registreerimine** komplekteeritud, lõpetatakse seotud saadetis.</span><span class="sxs-lookup"><span data-stu-id="346a7-146">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="346a7-147">Müügitellimuse saatelehtede protsessi saab siis komplekteeritud varude põhjal lähtestada.</span><span class="sxs-lookup"><span data-stu-id="346a7-147">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="346a7-148">[![Väljuvate saadetiste värskendamine](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="346a7-148">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

