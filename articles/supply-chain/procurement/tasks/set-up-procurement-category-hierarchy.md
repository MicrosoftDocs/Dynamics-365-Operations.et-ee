--- 
title: Hankekategooria hierarhia seadistamine
description: "See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat."
author: mkirknel
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b9897b1184e8159b20a45d4cedbba56baef31a3c
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="246d8-103">Hankekategooria hierarhia seadistamine</span><span class="sxs-lookup"><span data-stu-id="246d8-103">Set up a procurement category hierarchy</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="246d8-104">See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat.</span><span class="sxs-lookup"><span data-stu-id="246d8-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="246d8-105">Neid ülesandeid täidab üldjuhul ostujuht.</span><span class="sxs-lookup"><span data-stu-id="246d8-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="246d8-106">Enne, kui saate selle protseduuri käivitada, peab teil olema kategooriahierarhia, mille tüüp on Hange.</span><span class="sxs-lookup"><span data-stu-id="246d8-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="246d8-107">Demoettevõtte kasutamisel saate seda protseduuri käitada ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="246d8-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="246d8-108">Uue hankekategooria lisamine</span><span class="sxs-lookup"><span data-stu-id="246d8-108">Add a new procurement category</span></span>
1. <span data-ttu-id="246d8-109">Tehke valik Hanked > ..</span><span class="sxs-lookup"><span data-stu-id="246d8-109">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="246d8-110">> Hankekategooriad.</span><span class="sxs-lookup"><span data-stu-id="246d8-110">> Procurement categories.</span></span>
2. <span data-ttu-id="246d8-111">Klõpsake suvandit Kategooriahierarhia redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="246d8-111">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="246d8-112">Lehe vasakus servas kuvatakse praegune hankekategooria hierarhia.</span><span class="sxs-lookup"><span data-stu-id="246d8-112">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="246d8-113">Hakkate seda hierarhiat muutma.</span><span class="sxs-lookup"><span data-stu-id="246d8-113">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="246d8-114">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="246d8-114">Click New category node.</span></span>
    * <span data-ttu-id="246d8-115">Süsteem valib vaikimisi ülemise sõlme.</span><span class="sxs-lookup"><span data-stu-id="246d8-115">The system selects the top node by default.</span></span> <span data-ttu-id="246d8-116">Kui käitate seda protseduuri ülesandejuhendina, saate klõpsata nuppu Ava ja valida teise ülataseme sõlme, millesse oma uus sõlm lisada.</span><span class="sxs-lookup"><span data-stu-id="246d8-116">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="246d8-117">Kui see on tehtud, lukustage uuesti ülesandejuhend ja klõpsake sõlme Uus kategooria.</span><span class="sxs-lookup"><span data-stu-id="246d8-117">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="246d8-118">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="246d8-118">In the Name field, type a value.</span></span>
5. <span data-ttu-id="246d8-119">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="246d8-119">In the Description field, type a value.</span></span>
6. <span data-ttu-id="246d8-120">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="246d8-120">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="246d8-121">Hüüdnimi on valikuline.</span><span class="sxs-lookup"><span data-stu-id="246d8-121">The friendly name is optional.</span></span> <span data-ttu-id="246d8-122">See kuvatakse kategooriaotsingutes koos kategooria nimega.</span><span class="sxs-lookup"><span data-stu-id="246d8-122">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="246d8-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="246d8-123">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="246d8-124">Toodete lisamine uude hankekategooriasse</span><span class="sxs-lookup"><span data-stu-id="246d8-124">Add products to your new procurement category</span></span>
1. <span data-ttu-id="246d8-125">Tehke valik Hanked > ..</span><span class="sxs-lookup"><span data-stu-id="246d8-125">Go to Procurement and sourcing > ..</span></span> <span data-ttu-id="246d8-126">> Hankekategooriad.</span><span class="sxs-lookup"><span data-stu-id="246d8-126">> Procurement categories.</span></span>
    * <span data-ttu-id="246d8-127">Valige äsjalisatud sõlm.</span><span class="sxs-lookup"><span data-stu-id="246d8-127">Select the node you just added.</span></span> <span data-ttu-id="246d8-128">Kui käitate seda protseduuri ülesandejuhendina, peate sõlme valimiseks võib-olla ülesandejuhendi avama.</span><span class="sxs-lookup"><span data-stu-id="246d8-128">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="246d8-129">Laiendage jaotist Tooted.</span><span class="sxs-lookup"><span data-stu-id="246d8-129">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="246d8-130">Klõpsake suvandit Lisa, et seostada tooted hankekategooriaga.</span><span class="sxs-lookup"><span data-stu-id="246d8-130">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="246d8-131">Valige toode, mille soovite lisada hankekategooriasse.</span><span class="sxs-lookup"><span data-stu-id="246d8-131">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="246d8-132">Klõpsake toote valimiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="246d8-132">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="246d8-133">Valige teine toode, mille soovite lisada hankekategooriasse.</span><span class="sxs-lookup"><span data-stu-id="246d8-133">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="246d8-134">Klõpsake toote valimiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="246d8-134">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="246d8-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="246d8-135">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="246d8-136">Kinnitatud ja eelistatud hankijate lisamine</span><span class="sxs-lookup"><span data-stu-id="246d8-136">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="246d8-137">Lülitage jaotise Hankijad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="246d8-137">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="246d8-138">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="246d8-138">Click Add.</span></span>
    * <span data-ttu-id="246d8-139">Saate lisada hankekategooriasse hankija ja määrata, kas hankija on eelistatud või kategooria jaoks lihtsalt kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="246d8-139">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="246d8-140">Kui kustutate hankija kategooriast, ei kustutata kategooriast hankija ajaloolisi kandeid.</span><span class="sxs-lookup"><span data-stu-id="246d8-140">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="246d8-141">Leidke hankija, kelle soovite lisada hankekategooriasse.</span><span class="sxs-lookup"><span data-stu-id="246d8-141">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="246d8-142">Klõpsake hankija valimiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="246d8-142">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="246d8-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="246d8-143">Click OK.</span></span>
6. <span data-ttu-id="246d8-144">Valige selle hankija rida, keda soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="246d8-144">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="246d8-145">Valige suvand väljal Hankija olek.</span><span class="sxs-lookup"><span data-stu-id="246d8-145">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="246d8-146">Hankija valimise säte suvandis Kategooria poliitika reegel määrab, kas ostutaotlusel on saadaval eelistatud hankija, kinnitatud hankija või kõik hankijad.</span><span class="sxs-lookup"><span data-stu-id="246d8-146">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="246d8-147">Kategooriale lisateabe lisamine</span><span class="sxs-lookup"><span data-stu-id="246d8-147">Add additional information to the category</span></span>
1. <span data-ttu-id="246d8-148">Laiendage jaotist Hankija hindamiskriteeriumigrupid.</span><span class="sxs-lookup"><span data-stu-id="246d8-148">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="246d8-149">Sellel vahekaardil saate määratleda, millise kriteeriumi järgi tuleks hankekategoorias olevaid hankijaid hinnata.</span><span class="sxs-lookup"><span data-stu-id="246d8-149">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="246d8-150">Selleks klõpsake suvandit Lisa ja seejärel valige soovitud kriteeriumit sisaldav hankija hindamise grupp.</span><span class="sxs-lookup"><span data-stu-id="246d8-150">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="246d8-151">Laiendage jaotist Küsimustikud.</span><span class="sxs-lookup"><span data-stu-id="246d8-151">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="246d8-152">Sellel vahekaardil saate lisada küsimustikke, mis kuvatakse tellimusel, kui määrate suvandi Tegevuse tüüp sätteks Tellimus.</span><span class="sxs-lookup"><span data-stu-id="246d8-152">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="246d8-153">Sel juhul peab tellija enne hankekategooriasse kuuluva kindla toote või toodete tellimuse esitamist täitma küsimustiku.</span><span class="sxs-lookup"><span data-stu-id="246d8-153">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="246d8-154">Laiendage jaotist Kauba käibemaksugrupid.</span><span class="sxs-lookup"><span data-stu-id="246d8-154">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="246d8-155">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="246d8-155">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="246d8-156">Saate valida käibemaksugrupi.</span><span class="sxs-lookup"><span data-stu-id="246d8-156">Select a sales tax group.</span></span>
6. <span data-ttu-id="246d8-157">Laiendage jaotist Kategooria leht.</span><span class="sxs-lookup"><span data-stu-id="246d8-157">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="246d8-158">Kategooria lehed luuakse lehel Kategooria hierarhia.</span><span class="sxs-lookup"><span data-stu-id="246d8-158">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="246d8-159">Need sisaldavad teavet hankekategooria kohta, näiteks kategoorias olevate toodete tüüp, kategoorias olevate toodete pildid või teated, näiteks kategoorias saadaolevad allahindlused.</span><span class="sxs-lookup"><span data-stu-id="246d8-159">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="246d8-160">Kategooria lehel olev teave kuvatakse ostutaotlustel.</span><span class="sxs-lookup"><span data-stu-id="246d8-160">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="246d8-161">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="246d8-161">Close the page.</span></span>


