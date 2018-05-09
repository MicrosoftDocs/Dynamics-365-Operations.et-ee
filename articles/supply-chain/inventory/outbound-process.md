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
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c672a2ce6e962e49043cba4593a9899a8613c23e
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="outbound-process"></a><span data-ttu-id="18ff7-103">Väljaminev protsess</span><span class="sxs-lookup"><span data-stu-id="18ff7-103">Outbound process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="18ff7-104">Selles teemas antakse ülevaade väljaminevast protsessist moodulis Laohaldus.</span><span class="sxs-lookup"><span data-stu-id="18ff7-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="18ff7-105">Väljaminekuorderid</span><span class="sxs-lookup"><span data-stu-id="18ff7-105">Output orders</span></span>

<span data-ttu-id="18ff7-106">Müügitellimuse ridade ja üleviimistellimuse ridade seostamiseks komplekteerimislehti kasutavate väljaminevate komplekteerimisprotsessidega kasutatakse väljaminekuordereid.</span><span class="sxs-lookup"><span data-stu-id="18ff7-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="18ff7-107">Komplekteerimislehtede loomisel müügitellimustest või üleviimistellimustest luuakse automaatselt väljaminekuorderid ja saadetised.</span><span class="sxs-lookup"><span data-stu-id="18ff7-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="18ff7-108">Komplekteerimislehel on saadetisega üks-ühele suhe.</span><span class="sxs-lookup"><span data-stu-id="18ff7-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="18ff7-109">Saadetisest saab töödelda üleviimistellimuse saadetise või müügitellimuse saatelehe.</span><span class="sxs-lookup"><span data-stu-id="18ff7-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="18ff7-110">Järgmisel joonisel on antud ülevaade väljaminekuorderite protsessist.</span><span class="sxs-lookup"><span data-stu-id="18ff7-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="18ff7-111">[![Ülevaade väljaminekuorderi protsessist](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="18ff7-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="18ff7-112">Saate seadistada lähetusreeglid, et määratleda, kuidas programm peaks lähetusprotsessi käsitsema.</span><span class="sxs-lookup"><span data-stu-id="18ff7-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="18ff7-113">Seejärel saab nende reeglite abil lähetusprotsessi juhtida.</span><span class="sxs-lookup"><span data-stu-id="18ff7-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="18ff7-114">Konkreetsemalt võite kasutada neid reegleid juhtimiseks, millise protsessietapi jooksul saadetis tuleks välja saata.</span><span class="sxs-lookup"><span data-stu-id="18ff7-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="18ff7-115">Järgmised sätted määratlevad, kuidas väljaminevaid protsesse käsitsetakse.</span><span class="sxs-lookup"><span data-stu-id="18ff7-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="18ff7-116">Müügi- ja üleviimistellimuste komplekteerimisprotsessi olek</span><span class="sxs-lookup"><span data-stu-id="18ff7-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="18ff7-117">Avage **Ostureskontro** \> **Seadistus** \> **Ostureskontro parameetrid** ja valige siis vahekaardi **Värskendused** väljalt **Komplekteerimisprotsessi olek** väärtus.</span><span class="sxs-lookup"><span data-stu-id="18ff7-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="18ff7-118">[![Müügitellimuste komplekteerimisprotsessi oleku väli](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="18ff7-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="18ff7-119">Kui välja **Komplekteerimisprotsessi olek** väärtuseks on määratud **Lõpule viidud**, toimub komplekteerimisprotsess komplekteerimislehtede koostamise protsessi raames automaatselt.</span><span class="sxs-lookup"><span data-stu-id="18ff7-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="18ff7-120">Kui välja väärtuseks on määratud **Aktiveeritud**, tuleb komplekteerimislehe read käsitsi värskendada.</span><span class="sxs-lookup"><span data-stu-id="18ff7-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="18ff7-121">Sama puudutab üleviimistellimusi.</span><span class="sxs-lookup"><span data-stu-id="18ff7-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="18ff7-122">Avage **Varude haldus** \> **Seadistus** \> **Varude ja laohalduse parameetrid** ja valige siis vahekaardi **Transport** väljalt **Komplekteerimisprotsessi olek** väärtus.</span><span class="sxs-lookup"><span data-stu-id="18ff7-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="18ff7-123">[![Üleviimistellimuste komplekteerimisprotsessi oleku väli](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="18ff7-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="18ff7-124">Väljamineku laoorderite lõpetamine</span><span class="sxs-lookup"><span data-stu-id="18ff7-124">End output inventory orders</span></span>

<span data-ttu-id="18ff7-125">Avage **Varude haldus** \> **Seadistus** \> **Varude ja laohalduse parameetrid** ja määrake siis vahekaardil **Üldine** valik **Lõpeta väljamineku laoorder**.</span><span class="sxs-lookup"><span data-stu-id="18ff7-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="18ff7-126">[![Valik Lõpeta väljamineku laoorder](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="18ff7-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="18ff7-127">Kui laotöötaja vähendab komplekteerimislehe koguseid, eemaldatakse vastavad laoorderi kogused saadetisest.</span><span class="sxs-lookup"><span data-stu-id="18ff7-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="18ff7-128">Kui komplekteerimislehte uuendatakse teatud ajahetkel, registreeritakse ülejäänud kogused uuesti tellimuse tasandil, kui suvand **Lõpeta väljamineku laoorder** on seatud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="18ff7-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="18ff7-129">Kui suvand **Lõpeta väljamineku laoorder** on seatud väärtusele **Ei**, hoitakse ülejäänud koguseid avatud väljaminekuorderi kogusena ja need tuleb uuele komplekteerimislehele lisada funktsiooni **Ava väljaminekuorderid** osana.</span><span class="sxs-lookup"><span data-stu-id="18ff7-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="18ff7-130">[![Käsk Ava väljaminekuorderid menüüs Funktsioonid](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="18ff7-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="18ff7-131">[![Lehe Ava väljaminekuorderid menüü Funktsioonid](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="18ff7-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="18ff7-132">Vähenda kogust</span><span class="sxs-lookup"><span data-stu-id="18ff7-132">Reduce quantity</span></span>

<span data-ttu-id="18ff7-133">Kolmas parameeter, mida saate komplekteerimislehe koostamise raames kasutada, on parameeter **Vähenda kogust**.</span><span class="sxs-lookup"><span data-stu-id="18ff7-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="18ff7-134">Selle parameetri seadistus toimib koos sättega **Reserveerimine**, mis käivitab lattu väljastamise raames reserveerimisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="18ff7-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="18ff7-135">[![Parameeter Vähenda kogust](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="18ff7-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="18ff7-136">Müügitellimuse väljamineva protsessi näide</span><span class="sxs-lookup"><span data-stu-id="18ff7-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="18ff7-137">Selle näite puhul on olemas müügitellimus kahele kaubale.</span><span class="sxs-lookup"><span data-stu-id="18ff7-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="18ff7-138">Komplekteerimislehe koostamise ajal tuleb valida parameeter **Vähenda kogust**.</span><span class="sxs-lookup"><span data-stu-id="18ff7-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="18ff7-139">Seetõttu vabastate ja loote komplekteerimisread ainult vabale kaubavarule.</span><span class="sxs-lookup"><span data-stu-id="18ff7-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="18ff7-140">Komplekteerimine tuleb registreerida komplekteerimislehtede registreerimisprotsessi kaudu (**Komplekteerimisprotsessi olek** = **Aktiveeritud**).</span><span class="sxs-lookup"><span data-stu-id="18ff7-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="18ff7-141">Veel reserveerimata kaubavaru reserveeritakse komplekteerimislehe koostamise käigus.</span><span class="sxs-lookup"><span data-stu-id="18ff7-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="18ff7-142">Kaubavaru, mis pole saadaval, võib müügitellimusest eemaldada või väljastada lattu väljamineku töötlemiseks hiljem, kui varud on komplekteerimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="18ff7-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="18ff7-143">[![Komplekteerimislehe värskendamine](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="18ff7-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="18ff7-144">Kohe, kui kõik komplekteerimisread on lehel **Komplekteerimislehe registreerimine** komplekteeritud, lõpetatakse seotud saadetis.</span><span class="sxs-lookup"><span data-stu-id="18ff7-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="18ff7-145">Müügitellimuse saatelehtede protsessi saab siis komplekteeritud varude põhjal lähtestada.</span><span class="sxs-lookup"><span data-stu-id="18ff7-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="18ff7-146">[![Väljuvate saadetiste värskendamine](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="18ff7-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

