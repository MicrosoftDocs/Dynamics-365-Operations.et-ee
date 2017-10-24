--- 
title: "Müügilepingute täitmine"
description: "See protseduur näitab, kuidas müügilepingut täita, seostades sellega müügitellimused."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f0894bf962c139c2e9e4c9f8d1589fd933afcedb
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="0144b-103">Müügilepingute täitmine</span><span class="sxs-lookup"><span data-stu-id="0144b-103">Fulfill sales agreements</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0144b-104">See protseduur näitab, kuidas müügilepingut täita, seostades sellega müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="0144b-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="0144b-105">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="0144b-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="0144b-106">Enne selle juhendiga alustamist veenduge, et teil on olemas kehtiv müügileping, mille tüüp on Toote väärtuse kohustus.</span><span class="sxs-lookup"><span data-stu-id="0144b-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="0144b-107">Teine võimalus on käivitada ülesanne nimega Müügilepingute koostamine.</span><span class="sxs-lookup"><span data-stu-id="0144b-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="0144b-108">Müügitellimuse väljastamine lepingust</span><span class="sxs-lookup"><span data-stu-id="0144b-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="0144b-109">Avage Müük ja turundus > Müügilepingud > Müügilepingud.</span><span class="sxs-lookup"><span data-stu-id="0144b-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="0144b-110">Avage loendist leping, mille suhtes soovite tellimuse väljastada.</span><span class="sxs-lookup"><span data-stu-id="0144b-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="0144b-111">Klõpsake tegumiribal valikut Müügileping.</span><span class="sxs-lookup"><span data-stu-id="0144b-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="0144b-112">Klõpsake valikut Väljalaskeorder.</span><span class="sxs-lookup"><span data-stu-id="0144b-112">Click Release order.</span></span>
    * <span data-ttu-id="0144b-113">Nagu lehe Loo väljalaskeorder ülaosas näidatud, erinevad müügitellimuse ridade puhul nõutavad andmed, olenevalt sellest, kas leping on koguse- või väärtusepõhine.</span><span class="sxs-lookup"><span data-stu-id="0144b-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="0144b-114">Selles juhendis on lepingu tüüp Toote väärtuse kohustus.</span><span class="sxs-lookup"><span data-stu-id="0144b-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="0144b-115">Sellepärast on selle lehe ridade jaotis tühi.</span><span class="sxs-lookup"><span data-stu-id="0144b-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="0144b-116">Kui kohustus põhineks kogusel, kopeeritaks rea teave lepingust.</span><span class="sxs-lookup"><span data-stu-id="0144b-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="0144b-117">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="0144b-117">Click Create.</span></span>
    * <span data-ttu-id="0144b-118">Saate teate, et müügitellimus on loodud.</span><span class="sxs-lookup"><span data-stu-id="0144b-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="0144b-119">Kuna tellimus ei sisalda ühtegi rida, peate vabastusprotsessi lõpuleviimiseks sisestama tellimuserea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="0144b-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="0144b-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0144b-120">Close the page.</span></span>
7. <span data-ttu-id="0144b-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0144b-121">Close the page.</span></span>
8. <span data-ttu-id="0144b-122">Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="0144b-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="0144b-123">Otsige loendist üles ja avage tellimus, mis koostati eelmises ülesandes tellimuse väljastamise tulemusena.</span><span class="sxs-lookup"><span data-stu-id="0144b-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="0144b-124">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="0144b-124">Click Add line.</span></span>
11. <span data-ttu-id="0144b-125">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="0144b-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="0144b-126">Tippige või valige väljal Kaubakood seotud müügilepingul määratud kaup.</span><span class="sxs-lookup"><span data-stu-id="0144b-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="0144b-127">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="0144b-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="0144b-128">Veenduge, et sisestate koguse, mis toob netosumma seotud müügilepingu väärtuse alt.</span><span class="sxs-lookup"><span data-stu-id="0144b-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="0144b-129">Pange tähele, et müügitellimus on lepinguga seotud, kokkulepitud allahindluse protsent on tellimuse reale rakendatud.</span><span class="sxs-lookup"><span data-stu-id="0144b-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="0144b-130">Klõpsake käsku Värskenda rida.</span><span class="sxs-lookup"><span data-stu-id="0144b-130">Click Update line.</span></span>
15. <span data-ttu-id="0144b-131">Klõpsake valikut Seotud.</span><span class="sxs-lookup"><span data-stu-id="0144b-131">Click Attached.</span></span>
    * <span data-ttu-id="0144b-132">Lisatud lepingu lehel on kuvatud selle lepingu ID ja tingimused, millest rida on väljastatud.</span><span class="sxs-lookup"><span data-stu-id="0144b-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="0144b-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0144b-133">Close the page.</span></span>
17. <span data-ttu-id="0144b-134">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="0144b-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="0144b-135">Klõpsake valikut Manustatud müügileping.</span><span class="sxs-lookup"><span data-stu-id="0144b-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="0144b-136">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="0144b-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="0144b-137">Klõpsake vahekaarti Täitmine.</span><span class="sxs-lookup"><span data-stu-id="0144b-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="0144b-138">Täitmise vahekaardil on kõigi selle kohustusega seotud müügitellimuse ridade kokkuvõte ja nende täitmise olek ning summa või kogus, mida pole veel väljastatud.</span><span class="sxs-lookup"><span data-stu-id="0144b-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="0144b-139">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0144b-139">Close the page.</span></span>
22. <span data-ttu-id="0144b-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0144b-140">Close the page.</span></span>
23. <span data-ttu-id="0144b-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0144b-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="0144b-142">Müügilepingu rakendamine tellimuse protsessis</span><span class="sxs-lookup"><span data-stu-id="0144b-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="0144b-143">Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="0144b-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="0144b-144">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0144b-144">Click New.</span></span>
3. <span data-ttu-id="0144b-145">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="0144b-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="0144b-146">Otsige loendist üles ja valige müügilepingus määratud klient.</span><span class="sxs-lookup"><span data-stu-id="0144b-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="0144b-147">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0144b-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="0144b-148">Laiendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="0144b-148">Expand the General section.</span></span>
7. <span data-ttu-id="0144b-149">Klõpsake väljal Müügilepingu ID otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="0144b-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0144b-150">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0144b-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="0144b-151">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="0144b-151">Click Yes.</span></span>
10. <span data-ttu-id="0144b-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0144b-152">Click OK.</span></span>
11. <span data-ttu-id="0144b-153">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="0144b-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="0144b-154">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="0144b-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="0144b-155">Tippige või valige väljal Kaubakood seotud müügilepingul määratud kaup.</span><span class="sxs-lookup"><span data-stu-id="0144b-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="0144b-156">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0144b-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="0144b-157">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0144b-157">Click Save.</span></span>
16. <span data-ttu-id="0144b-158">Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.</span><span class="sxs-lookup"><span data-stu-id="0144b-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="0144b-159">Klõpsake valikut Saatelehe sisestamine.</span><span class="sxs-lookup"><span data-stu-id="0144b-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="0144b-160">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0144b-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="0144b-161">Valige väljal Sisestamine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="0144b-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="0144b-162">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0144b-162">Click OK.</span></span>
21. <span data-ttu-id="0144b-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0144b-163">Click OK.</span></span>
22. <span data-ttu-id="0144b-164">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="0144b-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="0144b-165">Klõpsake valikut Manustatud müügileping.</span><span class="sxs-lookup"><span data-stu-id="0144b-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="0144b-166">Klõpsake vahekaarti Täitmine.</span><span class="sxs-lookup"><span data-stu-id="0144b-166">Click the Fulfillment tab.</span></span>


