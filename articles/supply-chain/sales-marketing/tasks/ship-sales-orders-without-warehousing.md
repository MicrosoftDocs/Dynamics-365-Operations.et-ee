---
title: Müügitellimuste lähetamine ladustamiseta
description: Selles teemas selgitatakse, kuidas värskendada müügitellimust, kui tooted on kliendile tarnitud.
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b6b1dbb4d53785c226f7c9d40339d9dd19f47152
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426535"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="1a504-103">Müügitellimuste lähetamine ladustamiseta</span><span class="sxs-lookup"><span data-stu-id="1a504-103">Ship sales orders without warehousing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1a504-104">Selles teemas selgitatakse, kuidas värskendada müügitellimust, kui tooted on kliendile tarnitud.</span><span class="sxs-lookup"><span data-stu-id="1a504-104">This topic explains how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="1a504-105">Juhend kehtib täitmisvoo puhul, mis pole seadistatud laohalduse jaoks (ei põhi- ega täpsema lao puhul) ega nõua seetõttu toote komplekteerimise registreerimist enne tarnimist.</span><span class="sxs-lookup"><span data-stu-id="1a504-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="1a504-106">Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="1a504-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="1a504-107">Mõlemal juhul tuleb enne selle ülesande alustamist luua müügitellimus varundatud tootele, mille kogus on suurem kui 1.</span><span class="sxs-lookup"><span data-stu-id="1a504-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="1a504-108">Sisestamise tõrke vältimiseks peab kontrollima, et toote saadaolev kogus tellimusel valitud asukohas ja laos vastab tellitud kogusele.</span><span class="sxs-lookup"><span data-stu-id="1a504-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you've selected on the order covers the order quantity.</span></span>

## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="1a504-109">Tellimuse saatelehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="1a504-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="1a504-110">Avage navigeerimispaanil **Moodulid > Müük ja turundus > Müügitellimused > Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="1a504-110">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="1a504-111">Leidke ja valige loendist selle ülesande jaoks loodud tellimus.</span><span class="sxs-lookup"><span data-stu-id="1a504-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="1a504-112">Klõpsake tegevuspaneelil valikut **Komplekteerimine ja pakkimine.**</span><span class="sxs-lookup"><span data-stu-id="1a504-112">On the Action Pane, select **Pick and pack**.</span></span>
4. <span data-ttu-id="1a504-113">Vali **Sisesta saateleht**.</span><span class="sxs-lookup"><span data-stu-id="1a504-113">Select **Post packing slip**.</span></span>
5. <span data-ttu-id="1a504-114">Laiendage või ahendage jaotist **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1a504-114">Expand or collapse the **Parameters** section.</span></span>
6. <span data-ttu-id="1a504-115">Valige väljal **Kogus** suvand **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="1a504-115">In the **Quantity** field, select **All**.</span></span>
    - <span data-ttu-id="1a504-116">Muud suvandid on **Tarni kohe** ja **Komplekteeritud**.</span><span class="sxs-lookup"><span data-stu-id="1a504-116">Other options include **Deliver now** and **Picked**.</span></span> <span data-ttu-id="1a504-117">Kui tellimuserida tuleb tarnida osaliselt ja tellimuserea väli **Tarni kohe** sisaldab kogust, valige suvand **Tarni kohe**.</span><span class="sxs-lookup"><span data-stu-id="1a504-117">If the order line is to be shipped partially and the **Deliver now** field on the order line contains a quantity, you would select **Deliver now**.</span></span> <span data-ttu-id="1a504-118">Kui teie organisatsiooni täitmisvoog sisaldab komplekteerimist eraldi protsessina, mida hallatakse ja registreeritakse komplekteerimisloendiga, valige suvand **Komplekteeritud**.</span><span class="sxs-lookup"><span data-stu-id="1a504-118">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select **Picked**.</span></span>  
    - <span data-ttu-id="1a504-119">Kontrollige, kas suvandi **Sisestamine** sätteks on valitud **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1a504-119">Check that the **Posting** option is set to **Yes**.</span></span>  
7. <span data-ttu-id="1a504-120">Määrake suvandi **Saatelehe printimine** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1a504-120">Set the **Print packing slip** option to **Yes**.</span></span> <span data-ttu-id="1a504-121">Vahekaart **Ülevaade** sisaldab loendit selles sisestuses loodavate saatelehtede loendit.</span><span class="sxs-lookup"><span data-stu-id="1a504-121">The **Overview** tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="1a504-122">Kui tarnite üksikut tellimust, luuakse tavaliselt üks saateleht.</span><span class="sxs-lookup"><span data-stu-id="1a504-122">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="1a504-123">Kui aga selle tellimuse read tarnitakse erinevatest kohtadest, jaotatakse sisestus automaatselt vastavaks arvuks dokumentideks.</span><span class="sxs-lookup"><span data-stu-id="1a504-123">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="1a504-124">See on kohustuslik tingimus, mida ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="1a504-124">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="1a504-125">Samamoodi jaotatakse sisestus mitmeks dokumendiks, kui tellimuse read tuleb tarnida erinevatele tarneaadressidele ja tarnepoliitika on seadistatud jaotust nõudma.</span><span class="sxs-lookup"><span data-stu-id="1a504-125">Similarly, the posting will also be split into multiple documents if the order's lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
8. <span data-ttu-id="1a504-126">Valige vahekaardil **Read** tarnitava tellimuserea jaoks rida.</span><span class="sxs-lookup"><span data-stu-id="1a504-126">On the **Lines** tab, select the row for the order line to be shipped.</span></span>
9. <span data-ttu-id="1a504-127">Sisestage väljale **Värskendus** algsest kogusest väiksem arv.</span><span class="sxs-lookup"><span data-stu-id="1a504-127">In the **Update** field, enter a number lower than the original quantity.</span></span>
10. <span data-ttu-id="1a504-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a504-128">Select **OK**.</span></span>
11. <span data-ttu-id="1a504-129">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1a504-129">Select **Yes**.</span></span>
12. <span data-ttu-id="1a504-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1a504-130">Close the page.</span></span>
13. <span data-ttu-id="1a504-131">Toimingupaanil valige **Suvandid**.</span><span class="sxs-lookup"><span data-stu-id="1a504-131">On the Action Pane, select **Options**.</span></span>
14. <span data-ttu-id="1a504-132">Valige **Muuda vaadet**.</span><span class="sxs-lookup"><span data-stu-id="1a504-132">Select **Change view**.</span></span>
15. <span data-ttu-id="1a504-133">Valige **Päise vaade**.</span><span class="sxs-lookup"><span data-stu-id="1a504-133">Select **Header view**.</span></span>
    - <span data-ttu-id="1a504-134">Kui kõik tellimuse read on täielikult tarnitud, muutub tellimuse olek väärtuselt Avatud väärtusele Tarnitud.</span><span class="sxs-lookup"><span data-stu-id="1a504-134">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    - <span data-ttu-id="1a504-135">Selles näites on tellimuserida tarnitud osaliselt.</span><span class="sxs-lookup"><span data-stu-id="1a504-135">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="1a504-136">Seetõttu jääb tellimuse olekuks Avatud.</span><span class="sxs-lookup"><span data-stu-id="1a504-136">This is why the the order status remains Open.</span></span>     
    - <span data-ttu-id="1a504-137">Välja **Dokumendi olek** väärtuseks määratakse Saateleht, kuna vähemalt üks tellimuserida on tarnitud.</span><span class="sxs-lookup"><span data-stu-id="1a504-137">The **Document status** field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
16. <span data-ttu-id="1a504-138">Valige toimingupaanil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="1a504-138">On the Action Pane, select **General**.</span></span>
17. <span data-ttu-id="1a504-139">Valige **Rea kogus**.</span><span class="sxs-lookup"><span data-stu-id="1a504-139">Select **Line quantity**.</span></span>
18. <span data-ttu-id="1a504-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1a504-140">Close the page.</span></span>
19. <span data-ttu-id="1a504-141">Klõpsake tegevuspaneelil valikut **Komplekteerimine ja pakkimine.**</span><span class="sxs-lookup"><span data-stu-id="1a504-141">On the Action Pane, select **Pick and pack**.</span></span>
20. <span data-ttu-id="1a504-142">Vali **Saateleht**.</span><span class="sxs-lookup"><span data-stu-id="1a504-142">Select **Packing slip**.</span></span> <span data-ttu-id="1a504-143">Leht **Saatelehe tööleht** sisaldab kõiki teie tellimuse jaoks loodud saatelehedokumente.</span><span class="sxs-lookup"><span data-stu-id="1a504-143">The **Packing slip journal** page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="1a504-144">Saate iga dokumendi üksikasjad soovi korral üle vaadata ja välja printida.</span><span class="sxs-lookup"><span data-stu-id="1a504-144">You can review details of each document and print them, if you wish.</span></span>  

