--- 
title: Ostulepingu loomine
description: See protseduur selgitab, kuidas luua ostulepingut.
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0d0cc6508071bea3f622bc21f06aa55d2b757b6f
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="e0820-103">Ostulepingu loomine</span><span class="sxs-lookup"><span data-stu-id="e0820-103">Create a purchase agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e0820-104">See protseduur selgitab, kuidas luua ostulepingut.</span><span class="sxs-lookup"><span data-stu-id="e0820-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="e0820-105">Seda teeb tavaliselt ostujuht.</span><span class="sxs-lookup"><span data-stu-id="e0820-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="e0820-106">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="e0820-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="e0820-107">Enne alustamist peate seadistama ostulepingu klassifikatsioonid.</span><span class="sxs-lookup"><span data-stu-id="e0820-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="e0820-108">Kui olete lepingu loonud, saate seda kasutada ostutellimuse loomisel ning sellega kopeeritakse ostulepingu tingimused lepinguga seotud tellimuse päisesse ja kõigile ridadele.</span><span class="sxs-lookup"><span data-stu-id="e0820-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="e0820-109">Uue ostulepingu loomine</span><span class="sxs-lookup"><span data-stu-id="e0820-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="e0820-110">Avage Hanked > Ostulepingud > Ostulepingud.</span><span class="sxs-lookup"><span data-stu-id="e0820-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="e0820-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e0820-111">Click New.</span></span>
3. <span data-ttu-id="e0820-112">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e0820-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e0820-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e0820-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="e0820-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e0820-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e0820-115">Klõpsake väljal Ostulepingu klassifikatsioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e0820-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e0820-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e0820-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e0820-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e0820-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e0820-118">Laiendage jaotis Üldine.</span><span class="sxs-lookup"><span data-stu-id="e0820-118">Expand the General section.</span></span>
10. <span data-ttu-id="e0820-119">Sisestage kuupäev väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="e0820-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="e0820-120">Aegumiskuupäev kehtib vaikimisi kõigile kohustuseridadele ja määratleb, kui kaua konkreetne kohustus kehtib.</span><span class="sxs-lookup"><span data-stu-id="e0820-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="e0820-121">Sisestage väljale Dokumendi pealkiri oma ostulepingu nimi.</span><span class="sxs-lookup"><span data-stu-id="e0820-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="e0820-122">Jätke välja Vaikekohustus sätteks Toote koguse kohustus (või muutke seda, kui see on midagi muud).</span><span class="sxs-lookup"><span data-stu-id="e0820-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="e0820-123">Vaikekohustuse väärtus määratleb teie suvandid lepingu ridadel.</span><span class="sxs-lookup"><span data-stu-id="e0820-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="e0820-124">Kui vajate lepingu ridade loomisel uut kohustuse tüüpi, peate muutma päises vaikekohustust.</span><span class="sxs-lookup"><span data-stu-id="e0820-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="e0820-125">Kohustusi on nelja tüüpi: toote koguse kohustus – toote kindla koguse puhul; toote väärtuse kohustus – toote kindla valuutasumma kohta; tootekategooria väärtuse kohustus – kindla valuutasumma kohta hankekategoorias, kus summa võib kehtida kataloogikauba või mittekataloogikauba kohta; väärtuse kohustus – kindla valuutasumma puhul, mille saab täita mis tahes toote või mis tahes hankekategooriaga.</span><span class="sxs-lookup"><span data-stu-id="e0820-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="e0820-126">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e0820-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="e0820-127">Kommentaari lisamine</span><span class="sxs-lookup"><span data-stu-id="e0820-127">Add a commitment</span></span>
1. <span data-ttu-id="e0820-128">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="e0820-128">Click Add line.</span></span>
2. <span data-ttu-id="e0820-129">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e0820-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="e0820-130">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e0820-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e0820-131">Valige toode, mille puhul soovite kohustuse lisada.</span><span class="sxs-lookup"><span data-stu-id="e0820-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="e0820-132">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e0820-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e0820-133">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="e0820-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e0820-134">See on lõplik kogus, mille ostmises oma hankijalt olete kokku leppinud.</span><span class="sxs-lookup"><span data-stu-id="e0820-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="e0820-135">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="e0820-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="e0820-136">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e0820-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="e0820-137">Määrake suvandi Maksimaalne on jõustatud sätteks Jah.</span><span class="sxs-lookup"><span data-stu-id="e0820-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="e0820-138">Suvand Maksimaalne on jõustatud piirab kohustuse kasutamist.</span><span class="sxs-lookup"><span data-stu-id="e0820-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="e0820-139">Saate osta ainult kuni koguseni, mis on määratud rea väljal Kogus.</span><span class="sxs-lookup"><span data-stu-id="e0820-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="e0820-140">Ahendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e0820-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="e0820-141">Päise tingimuste lisamine</span><span class="sxs-lookup"><span data-stu-id="e0820-141">Add header conditions</span></span>
1. <span data-ttu-id="e0820-142">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="e0820-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="e0820-143">Klõpsake suvandit Muuda vaadet.</span><span class="sxs-lookup"><span data-stu-id="e0820-143">Click Change view.</span></span>
3. <span data-ttu-id="e0820-144">Klõpsake suvandit Päisevaade.</span><span class="sxs-lookup"><span data-stu-id="e0820-144">Click Header view.</span></span>
4. <span data-ttu-id="e0820-145">Laiendage jaotist Tingimused.</span><span class="sxs-lookup"><span data-stu-id="e0820-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="e0820-146">Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e0820-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e0820-147">Maksetingimused hankija kontolt kuvatakse siin vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="e0820-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="e0820-148">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e0820-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e0820-149">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e0820-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e0820-150">Klõpsake väljal Tarneviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e0820-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e0820-151">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e0820-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="e0820-152">Klõpsake väljal Tarnetingimused otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e0820-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e0820-153">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e0820-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="e0820-154">Leppe kinnitamine ja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="e0820-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="e0820-155">Klõpsake toimingupaanil suvandit Ostuleping.</span><span class="sxs-lookup"><span data-stu-id="e0820-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="e0820-156">Klõpsake suvandit Kinnitus.</span><span class="sxs-lookup"><span data-stu-id="e0820-156">Click Confirmation.</span></span>
    * <span data-ttu-id="e0820-157">Määrake suvandi Märgi lepe kehtivaks sätteks Jah.</span><span class="sxs-lookup"><span data-stu-id="e0820-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="e0820-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e0820-158">Click OK.</span></span>
4. <span data-ttu-id="e0820-159">Klõpsake toimingupaanil suvandit Ostuleping.</span><span class="sxs-lookup"><span data-stu-id="e0820-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="e0820-160">Klõpsake suvandit Ostulepingu kinnitused.</span><span class="sxs-lookup"><span data-stu-id="e0820-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="e0820-161">Suvand Eelvaade/printimine võimaldab luua ostutellimuse kohta dokumendi, mille saate seejärel välja printida või hankijale saata.</span><span class="sxs-lookup"><span data-stu-id="e0820-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="e0820-162">Lepingu hiljem muutmisel ja uuesti kinnitamisel kuvatakse siin mõlemad versioonid.</span><span class="sxs-lookup"><span data-stu-id="e0820-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="e0820-163">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e0820-163">Close the page.</span></span>


