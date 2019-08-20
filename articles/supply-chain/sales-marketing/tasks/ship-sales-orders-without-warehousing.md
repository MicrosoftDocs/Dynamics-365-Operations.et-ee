---
title: Müügitellimuste lähetamine ladustamiseta
description: Selles juhendis selgitatakse, kuidas värskendada müügitellimust, kui tooted on kliendile tarnitud.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62bbd65e2d80dca5a07b761e1aa76f1894b667c1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843309"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="7ffdc-103">Müügitellimuste lähetamine ladustamiseta</span><span class="sxs-lookup"><span data-stu-id="7ffdc-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ffdc-104">Selles juhendis selgitatakse, kuidas värskendada müügitellimust, kui tooted on kliendile tarnitud.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="7ffdc-105">Juhend kehtib täitmisvoo puhul, mis pole seadistatud laohalduse jaoks (ei põhi- ega täpsema lao puhul) ega nõua seetõttu toote komplekteerimise registreerimist enne tarnimist.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="7ffdc-106">Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="7ffdc-107">Mõlemal juhul tuleb enne selle ülesande alustamist luua müügitellimus varundatud tootele, mille kogus on suurem kui 1.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="7ffdc-108">Sisestamise tõrke vältimiseks peab kontrollima, et toote saadaolev kogus tellimusel valitud asukohas ja laos vastab tellitud kogusele.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="7ffdc-109">Tellimuse saatelehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="7ffdc-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="7ffdc-110">Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="7ffdc-111">Leidke ja valige loendist selle ülesande jaoks loodud tellimus.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="7ffdc-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7ffdc-113">Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="7ffdc-114">Klõpsake valikut Saatelehe sisestamine.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="7ffdc-115">Laiendage või ahendage jaotist Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="7ffdc-116">Valige väljal Kogus väärtus Kõik.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="7ffdc-117">Muud suvandiud on Tarni kohe ja Komplekteeritud.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="7ffdc-118">Kui tellimuserida tuleb tarnida osaliselt ja tellimuserea väli Tarni kohe sisaldab kogust, valige suvand Tarni kohe.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="7ffdc-119">Kui teie organisatsiooni täitmisvoog sisaldab komplekteerimist eraldi protsessina, mida hallatakse ja registreeritakse komplekteerimisloendiga, valige suvand Komplekteeritud.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="7ffdc-120">Kontrollige, kas suvandi Sisestamine sätteks on valitud Jah.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="7ffdc-121">Määrake suvandi Saatelehe printimine sätteks Jah.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="7ffdc-122">Vahekaart Ülevaade sisaldab loendit selles sisestuses loodavate saatelehtede loendit.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="7ffdc-123">Kui tarnite üksikut tellimust, luuakse tavaliselt üks saateleht.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="7ffdc-124">Kui aga selle tellimuse read tarnitakse erinevatest kohtadest, jaotatakse sisestus automaatselt vastavaks arvuks dokumentideks.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="7ffdc-125">See on kohustuslik tingimus, mida ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="7ffdc-126">Samamoodi jaotatakse sisestus mitmeks dokumendiks, kui tellimuse read tuleb tarnida erinevatele tarneaadressidele ja tarnepoliitika on seadistatud jaotust nõudma.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="7ffdc-127">Valige vahekaardil Read tarnitava tellimuserea jaoks rida.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="7ffdc-128">Sisestage väljale Värskendus algsest kogusest väiksem arv.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="7ffdc-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-129">Click OK.</span></span>
12. <span data-ttu-id="7ffdc-130">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-130">Click Yes.</span></span>
13. <span data-ttu-id="7ffdc-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-131">Close the page.</span></span>
14. <span data-ttu-id="7ffdc-132">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="7ffdc-133">Klõpsake suvandit Muuda vaadet.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-133">Click Change view.</span></span>
16. <span data-ttu-id="7ffdc-134">Klõpsake suvandit Päisevaade.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-134">Click Header view.</span></span>
    * <span data-ttu-id="7ffdc-135">Kui kõik tellimuse read on täielikult tarnitud, muutub tellimuse olek väärtuselt Avatud väärtusele Tarnitud.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="7ffdc-136">Selles näites on tellimuserida tarnitud osaliselt.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="7ffdc-137">Seetõttu jääb tellimuse olekuks Avatud.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="7ffdc-138">Välja Dokumendi olek väärtuseks määratakse Saateleht, kuna vähemalt üks tellimuserida on tarnitud.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="7ffdc-139">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="7ffdc-140">Klõpsake suvandit Rea kogus.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-140">Click Line quantity.</span></span>
19. <span data-ttu-id="7ffdc-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-141">Close the page.</span></span>
20. <span data-ttu-id="7ffdc-142">Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="7ffdc-143">Klõpsake suvandit Saateleht.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-143">Click Packing slip.</span></span>
    * <span data-ttu-id="7ffdc-144">Leht Saatelehe tööleht sisaldab kõiki teie tellimuse jaoks loodud saatelehedokumente.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="7ffdc-145">Saate iga dokumendi üksikasjad soovi korral üle vaadata ja välja printida.</span><span class="sxs-lookup"><span data-stu-id="7ffdc-145">You can review details of each document and print them, if you wish.</span></span>  

