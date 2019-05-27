---
title: Tarbimistaotluse loomine
description: See protseduur selgitab ostutaotluse loomise protsessi.
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560640"
---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="da9d8-103">Tarbimistaotluse loomine</span><span class="sxs-lookup"><span data-stu-id="da9d8-103">Create a requisition for consumption</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da9d8-104">See protseduur selgitab ostutaotluse loomise protsessi.</span><span class="sxs-lookup"><span data-stu-id="da9d8-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="da9d8-105">See näitab erinevaid viise toodete otsimiseks hankekataloogist ja toodete lisamiseks, mis ei ole kataloogis.</span><span class="sxs-lookup"><span data-stu-id="da9d8-105">It shows you different ways to search for products in your procurement catalog and how to add a product that isn’t in your catalog.</span></span> <span data-ttu-id="da9d8-106">Enne selle protseduuri alustamist peab teil olema seadistatud ostupoliitika, mille ostutaotluse vaiketüübiks on Tarbimine.</span><span class="sxs-lookup"><span data-stu-id="da9d8-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="da9d8-107">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="da9d8-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="da9d8-108">Protseduuri saab teha ainult kasutajaprofiiliga, mis on seadistatud töötaja profiilina.</span><span class="sxs-lookup"><span data-stu-id="da9d8-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="da9d8-109">Seda ülesannet teeb tavaliselt töötaja.</span><span class="sxs-lookup"><span data-stu-id="da9d8-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="da9d8-110">Töötaja turberoll võimaldab ülesandeid teha; või juhul, kui kasutate USMF-i, saate sisse logida nime Alicia alt.</span><span class="sxs-lookup"><span data-stu-id="da9d8-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="da9d8-111">Uue tellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="da9d8-111">Create a new requisition</span></span>
1. <span data-ttu-id="da9d8-112">Tehke valik Hanked > Ostutaotlused > Minu ettevalmistatud ostutaotlused.</span><span class="sxs-lookup"><span data-stu-id="da9d8-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="da9d8-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="da9d8-113">Click New.</span></span>
3. <span data-ttu-id="da9d8-114">Sisestage väljale Nimi tellimuse jaoks nimi.</span><span class="sxs-lookup"><span data-stu-id="da9d8-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="da9d8-115">Sisestage kuupäev väljale Nõutav kuupäev.</span><span class="sxs-lookup"><span data-stu-id="da9d8-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="da9d8-116">Vaikimisi kopeeritakse nõutav kuupäev ja aruandluskuupäev ostutellimuste ridadele.</span><span class="sxs-lookup"><span data-stu-id="da9d8-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="da9d8-117">Neid saab muuta rea tasandil.</span><span class="sxs-lookup"><span data-stu-id="da9d8-117">They can be changed at the line level.</span></span> <span data-ttu-id="da9d8-118">Nõudekuupäev on nõutud kättetoimetamiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="da9d8-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="da9d8-119">Sisestage kuupäev väljale Aruandluskuupäev.</span><span class="sxs-lookup"><span data-stu-id="da9d8-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="da9d8-120">Raamatupidamise kuupäeva kasutatakse raamatupidamiskirje salvestamiseks pearaamatusse ja kinnitamaks, kas eelarvevahendid on saadaval.</span><span class="sxs-lookup"><span data-stu-id="da9d8-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="da9d8-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da9d8-121">Click OK.</span></span>
7. <span data-ttu-id="da9d8-122">Klõpsake väljal Põhjus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="da9d8-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="da9d8-123">Vaikimisi ilmub valitav äriline põhjendus ostutaotluse ridadel, kuid seda saab rea tasandil muuta.</span><span class="sxs-lookup"><span data-stu-id="da9d8-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="da9d8-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="da9d8-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="da9d8-125">Valige põhjus.</span><span class="sxs-lookup"><span data-stu-id="da9d8-125">Select the reason</span></span>
10. <span data-ttu-id="da9d8-126">Sisestage väljale Üksikasjad tellimuse põhjalikum kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="da9d8-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="da9d8-127">Tellimusele rea lisamine</span><span class="sxs-lookup"><span data-stu-id="da9d8-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="da9d8-128">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="da9d8-128">Click Add line.</span></span>
    * <span data-ttu-id="da9d8-129">Ostutaotlusele ridade lisamiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="da9d8-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="da9d8-130">Kui teate juba tootenumbrit või teate, et taotlete toodet, mis ei ole tootekataloogis, saate rea lisada otse suvandiga „Lisa rida”.</span><span class="sxs-lookup"><span data-stu-id="da9d8-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalog, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="da9d8-131">Teine võimalus on kasutada suvandit „Lisa tooteid”, mille puhul saate kaupade tootekataloogist otsimiseks kasutada otsingut ja filtreerimist.</span><span class="sxs-lookup"><span data-stu-id="da9d8-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalog.</span></span>    
2. <span data-ttu-id="da9d8-132">Klõpsake äsja loodud rida.</span><span class="sxs-lookup"><span data-stu-id="da9d8-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="da9d8-133">Nõude esitaja on töötaja, kes esitas tellimuse.</span><span class="sxs-lookup"><span data-stu-id="da9d8-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="da9d8-134">Vaikimisi on tellimuse koostaja töötaja, kes selle esitab.</span><span class="sxs-lookup"><span data-stu-id="da9d8-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="da9d8-135">Teile peab olema antud õigus teise töötaja nimel tellimuserida ette valmistada.</span><span class="sxs-lookup"><span data-stu-id="da9d8-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="da9d8-136">Kui teil on see õigus olemas, kuvatakse selles otsingus teised töötajad.</span><span class="sxs-lookup"><span data-stu-id="da9d8-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="da9d8-137">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="da9d8-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="da9d8-138">Teile valimiseks saada olevad kaubad on piiratud kategooria juurdepääsupoliitika ja ostva juriidilise isiku hankekataloogiga.</span><span class="sxs-lookup"><span data-stu-id="da9d8-138">The items that are available for you to choose are limited by the category access policy and the procurement catalog for the buying legal entity.</span></span>   
4. <span data-ttu-id="da9d8-139">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="da9d8-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="da9d8-140">Tellimusele lisatoodete lisamine</span><span class="sxs-lookup"><span data-stu-id="da9d8-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="da9d8-141">Klõpsake suvandit Lisa tooteid.</span><span class="sxs-lookup"><span data-stu-id="da9d8-141">Click Add products.</span></span>
    * <span data-ttu-id="da9d8-142">Selle suvandi puhul saate otsida tooteid tootekataloogist.</span><span class="sxs-lookup"><span data-stu-id="da9d8-142">This is the option where you can search for products in the product catalog.</span></span>    
2. <span data-ttu-id="da9d8-143">Sisestage väljale Leia hankekategooria sõlm otsitava kategooria nime algus, seejärel klõpsake sisestusklahvi Enter.</span><span class="sxs-lookup"><span data-stu-id="da9d8-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="da9d8-144">Sisestage näiteks „arvut”.</span><span class="sxs-lookup"><span data-stu-id="da9d8-144">For example, type comput.</span></span>  
3. <span data-ttu-id="da9d8-145">Kasutage otseteed InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="da9d8-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="da9d8-146">Kasutage valitud kategooria toodete loendi filtreerimiseks suvandit Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="da9d8-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="da9d8-147">Valige tootekaart, mille soovite tellimusele lisada.</span><span class="sxs-lookup"><span data-stu-id="da9d8-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="da9d8-148">Klõpsake suvandit Lisam ridadele.</span><span class="sxs-lookup"><span data-stu-id="da9d8-148">Click Add to lines.</span></span>
7. <span data-ttu-id="da9d8-149">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="da9d8-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="da9d8-150">Sisestage väljale Leia hankekategooria sõlm otsitava kategooria nime algus, seejärel klõpsake sisestusklahvi Enter.</span><span class="sxs-lookup"><span data-stu-id="da9d8-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="da9d8-151">Sisestage näiteks „Esilet” (esiletõstupliiatsid).</span><span class="sxs-lookup"><span data-stu-id="da9d8-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="da9d8-152">Kasutage otseteed InvokeDefaultButton.</span><span class="sxs-lookup"><span data-stu-id="da9d8-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="da9d8-153">Hankekataloogis puuduva toote lisamiseks klõpsake suvandit Loendist puuduva toote lisamine ridadele.</span><span class="sxs-lookup"><span data-stu-id="da9d8-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalog.</span></span>
11. <span data-ttu-id="da9d8-154">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="da9d8-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="da9d8-155">Sisestage väärtus väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="da9d8-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="da9d8-156">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da9d8-156">Click OK.</span></span>
14. <span data-ttu-id="da9d8-157">Sisestage väljale Kauba kirjeldus toote kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="da9d8-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="da9d8-158">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="da9d8-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="da9d8-159">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="da9d8-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="da9d8-160">Kui teate kindla hankija hinda (kelle valite hankija konto väljal), saate sisestada selle hinna</span><span class="sxs-lookup"><span data-stu-id="da9d8-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="da9d8-161">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="da9d8-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="da9d8-162">Sellel väljal saadaolevad hankijad olenevad ostupoliitikatest ja hankija olekust praeguses hankekategoorias.</span><span class="sxs-lookup"><span data-stu-id="da9d8-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="da9d8-163">Hankija siin valimise asemel võite klõpsata ka nuppu Soovita hankijat.</span><span class="sxs-lookup"><span data-stu-id="da9d8-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="da9d8-164">Valige loendist hankija, keda soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="da9d8-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="da9d8-165">Sisestage väärtus väljale Väline kaubakood.</span><span class="sxs-lookup"><span data-stu-id="da9d8-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="da9d8-166">See on hankijale teada olev toote viitenumber.</span><span class="sxs-lookup"><span data-stu-id="da9d8-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="da9d8-167">See võib olla näiteks toote kaubakood hankija enda kataloogis.</span><span class="sxs-lookup"><span data-stu-id="da9d8-167">For example, this could be the item number of the product in the vendor's own catalog.</span></span>  
20. <span data-ttu-id="da9d8-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da9d8-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="da9d8-169">Summade jaotamine</span><span class="sxs-lookup"><span data-stu-id="da9d8-169">Distribute amounts</span></span>
1. <span data-ttu-id="da9d8-170">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="da9d8-170">Click Financials.</span></span>
2. <span data-ttu-id="da9d8-171">Klõpsake suvandit Summade jaotamine.</span><span class="sxs-lookup"><span data-stu-id="da9d8-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="da9d8-172">See protsess selgitab, kuidas jaotada esimese rea kulu kahe konto vahel.</span><span class="sxs-lookup"><span data-stu-id="da9d8-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="da9d8-173">Seda saate teha ka hiljem, kui tellimus on läbivaatusel.</span><span class="sxs-lookup"><span data-stu-id="da9d8-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="da9d8-174">Klõpsake uue jaotusrea lisamiseks suvandit Tükelda.</span><span class="sxs-lookup"><span data-stu-id="da9d8-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="da9d8-175">Valige väljal Pearaamatukonto esimene kulukeskus, mis peaks olema kulu osa.</span><span class="sxs-lookup"><span data-stu-id="da9d8-175">In the Ledger account field select the first cost center that should take part of the cost.</span></span>
5. <span data-ttu-id="da9d8-176">Valige teine jaotusrida.</span><span class="sxs-lookup"><span data-stu-id="da9d8-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="da9d8-177">Määrake väljal Pearaamatukonto teine kulukeskus.</span><span class="sxs-lookup"><span data-stu-id="da9d8-177">In the Ledger account field specify the other cost center.</span></span>
7. <span data-ttu-id="da9d8-178">Klõpsake suvandit Jaota võrdselt.</span><span class="sxs-lookup"><span data-stu-id="da9d8-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="da9d8-179">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da9d8-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="da9d8-180">Kuva rea üksikasjad</span><span class="sxs-lookup"><span data-stu-id="da9d8-180">View line details</span></span>
1. <span data-ttu-id="da9d8-181">Lülitage jaotise Rea üksikasjad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="da9d8-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="da9d8-182">Tellimuse esitamine</span><span class="sxs-lookup"><span data-stu-id="da9d8-182">Submit the requisition</span></span>
1. <span data-ttu-id="da9d8-183">Klõpsake suvandit Töövoog rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="da9d8-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="da9d8-184">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="da9d8-184">Click Submit.</span></span>
3. <span data-ttu-id="da9d8-185">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da9d8-185">Close the page.</span></span>
4. <span data-ttu-id="da9d8-186">Sisestage väljale Kommentaar märkus tellimuse kinnitajale.</span><span class="sxs-lookup"><span data-stu-id="da9d8-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="da9d8-187">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="da9d8-187">Click Submit.</span></span>
6. <span data-ttu-id="da9d8-188">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da9d8-188">Close the page.</span></span>
7. <span data-ttu-id="da9d8-189">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="da9d8-189">Refresh the page.</span></span>

