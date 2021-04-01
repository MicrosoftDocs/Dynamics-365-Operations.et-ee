---
title: Väljastatud toote loomine ühe ettevõtte jaoks
description: See protseduur annab ülevaate üksiku väljastatud toote loomise kohta ühe juriidilise üksuse kontekstis.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfe93a3084bb8c7f2b181b35d393b8afdabb9f4b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258823"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="25400-103">Väljastatud toote loomine ühe ettevõtte jaoks</span><span class="sxs-lookup"><span data-stu-id="25400-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25400-104">See protseduur annab ülevaate üksiku väljastatud toote loomise kohta ühe juriidilise üksuse kontekstis.</span><span class="sxs-lookup"><span data-stu-id="25400-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="25400-105">Pärast väljastatud toote loomist on see kohe saadaval ainult selles üksuses.</span><span class="sxs-lookup"><span data-stu-id="25400-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="25400-106">Saate selle protseduuriga tutvuda demoettevõtte USMF andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="25400-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="25400-107">Seda ülesannet teeb üldjuhul toote koostaja.</span><span class="sxs-lookup"><span data-stu-id="25400-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="25400-108">Väljastatud toote loomine</span><span class="sxs-lookup"><span data-stu-id="25400-108">Create a released product</span></span>
1. <span data-ttu-id="25400-109">Avage Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="25400-109">Go to Released products.</span></span>
2. <span data-ttu-id="25400-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="25400-110">Click New.</span></span>
3. <span data-ttu-id="25400-111">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="25400-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="25400-112">Kui tootenumbrit ei ole väljale Tootenumber automaatselt sisestatud, sisestage kordumatu tootenumber.</span><span class="sxs-lookup"><span data-stu-id="25400-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="25400-113">See etapp on nõutav ainult siis, kui tootenumbritele pole numbrijada häälestatud.</span><span class="sxs-lookup"><span data-stu-id="25400-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="25400-114">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="25400-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="25400-115">Toote nime kasutatakse vaikimisi otsingunimena.</span><span class="sxs-lookup"><span data-stu-id="25400-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="25400-116">Vajaduse korral saate otsingunime muuta.</span><span class="sxs-lookup"><span data-stu-id="25400-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="25400-117">Klõpsake väljal Kauba mudeligrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-118">Kaubamudeligrupid sisaldavad sätteid, mis määratlevad kaupade kontrollimise ja käsitlemise viisi sissetulekutel ja väljaminekutel.</span><span class="sxs-lookup"><span data-stu-id="25400-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="25400-119">Sätted määratlevad ka kaupade tarbimise arvutusviisi.</span><span class="sxs-lookup"><span data-stu-id="25400-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="25400-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="25400-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="25400-122">Klõpsake väljal Kaubagrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-123">Kaubagruppe kasutatakse varude haldamisel, nende abil saab laokaubad kauba omaduste alusel jagada gruppidesse.</span><span class="sxs-lookup"><span data-stu-id="25400-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="25400-124">Näiteks saate põhikontodele teabe sisestamise viisi haldamiseks luua mitmesuguste kaubagruppide seeriaid, mis on seotud konkreetsete põhikontodega.</span><span class="sxs-lookup"><span data-stu-id="25400-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="25400-125">See võimaldab jälgida kaupade laoväärtust eri etappides.</span><span class="sxs-lookup"><span data-stu-id="25400-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="25400-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="25400-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="25400-128">Klõpsake väljal Laoala dimensiooni grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-129">Laoala dimensioonid aitavad reguleerida kaupade ladustamist ja laost väljastamist.</span><span class="sxs-lookup"><span data-stu-id="25400-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="25400-130">Näiteks saab laoala dimensiooniks olla tegevuskoht ja ladu.</span><span class="sxs-lookup"><span data-stu-id="25400-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="25400-131">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="25400-132">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="25400-133">Klõpsake väljal Jälgimisdimensiooni grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-134">Jälgimisdimensioonigrupp määratleb, milliseid jälgimisdimensioone saate tootele lisada.</span><span class="sxs-lookup"><span data-stu-id="25400-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="25400-135">Näiteks kasutatakse laokaupade jälgimiseks partiinumbrit ja seerianumbrit.</span><span class="sxs-lookup"><span data-stu-id="25400-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="25400-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="25400-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="25400-138">Klõpsake väljal Laoühik otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-139">Laoühik määratleb toote arvestusviisi laos hoidmisel.</span><span class="sxs-lookup"><span data-stu-id="25400-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="25400-140">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="25400-141">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="25400-142">Klõpsake väljal Ostuühik otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-143">Ostuühik määratleb toote arvestusviisi hankijalt ostmisel.</span><span class="sxs-lookup"><span data-stu-id="25400-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="25400-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="25400-145">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="25400-146">Klõpsake väljal Müügiüksus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-147">Müügiühik määratleb toote arvestusviisi kliendile müümisel.</span><span class="sxs-lookup"><span data-stu-id="25400-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="25400-148">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="25400-149">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="25400-150">Klõpsake väljal Koosluse ühik otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-151">Koosluseühik määratleb toote arvestusviisi selle kaasamisel kooslusse (BOM).</span><span class="sxs-lookup"><span data-stu-id="25400-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="25400-152">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="25400-153">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="25400-154">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-155">Kauba käibemaksugrupp müügi maksustamise grupis määratleb käibemaksu arvutamise viisi iga kauba puhul.</span><span class="sxs-lookup"><span data-stu-id="25400-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="25400-156">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="25400-157">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="25400-158">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="25400-159">Kauba käibemaksugrupp ostu maksustamise grupis määratleb ostumaksu arvutamise viisi iga kauba puhul.</span><span class="sxs-lookup"><span data-stu-id="25400-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="25400-160">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="25400-161">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="25400-162">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="25400-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="25400-163">Toote omaduste lisamine</span><span class="sxs-lookup"><span data-stu-id="25400-163">Add product characteristics</span></span>
1. <span data-ttu-id="25400-164">Laiendage või ahendage jaotist Varude haldamine.</span><span class="sxs-lookup"><span data-stu-id="25400-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="25400-165">Sisestage number väljale Netokaal.</span><span class="sxs-lookup"><span data-stu-id="25400-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="25400-166">Sisestage number väljale Taarakaal.</span><span class="sxs-lookup"><span data-stu-id="25400-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="25400-167">Sisestage number väljale Kogumaht.</span><span class="sxs-lookup"><span data-stu-id="25400-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="25400-168">Sisestage number väljale Kogulaius.</span><span class="sxs-lookup"><span data-stu-id="25400-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="25400-169">Sisestage number väljale Kogukõrgus.</span><span class="sxs-lookup"><span data-stu-id="25400-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="25400-170">Sisestage number väljale Maht.</span><span class="sxs-lookup"><span data-stu-id="25400-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="25400-171">Finantsdimensioonide lisamine</span><span class="sxs-lookup"><span data-stu-id="25400-171">Add financial dimensions</span></span>
1. <span data-ttu-id="25400-172">Laiendage või ahendage jaotist Finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="25400-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="25400-173">Klõpsake väljal BusinessUnit otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="25400-174">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="25400-175">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="25400-176">Klõpsake väljal CostCenter otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="25400-177">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="25400-178">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="25400-179">Klõpsake väljal Osakond otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="25400-180">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="25400-181">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="25400-182">Klõpsake väljal ItemGroup otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="25400-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="25400-183">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="25400-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="25400-184">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="25400-184">In the list, click the link in the selected row.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]