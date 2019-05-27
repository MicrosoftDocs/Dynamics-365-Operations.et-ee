---
title: Hankekategooria hierarhia seadistamine
description: See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat.
author: mkirknel
manager: AnnBe
ms.date: 11/06/2017
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
ms.openlocfilehash: 01809a8a3256342682d8a9cfb296a355310fe4ed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569887"
---
# <a name="set-up-a-procurement-category-hierarchy"></a><span data-ttu-id="e570c-103">Hankekategooria hierarhia seadistamine</span><span class="sxs-lookup"><span data-stu-id="e570c-103">Set up a procurement category hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e570c-104">See protseduur näitab, kuidas luua hankekategooria hierarhias uusi sõlmi ja konfigureerida hankeprotsessis kasutatavat hankekategooriat.</span><span class="sxs-lookup"><span data-stu-id="e570c-104">This procedure shows you how to create new nodes in a procurement category hierarchy and how to configure a procurement category to be used in a procurement process.</span></span> <span data-ttu-id="e570c-105">Neid ülesandeid täidab üldjuhul ostujuht.</span><span class="sxs-lookup"><span data-stu-id="e570c-105">These tasks would typically be carried out by a Purchasing manager.</span></span> <span data-ttu-id="e570c-106">Enne, kui saate selle protseduuri käivitada, peab teil olema kategooriahierarhia, mille tüüp on Hange.</span><span class="sxs-lookup"><span data-stu-id="e570c-106">Before you can start this procedure, there must be a category hierarchy of type Procurement.</span></span> <span data-ttu-id="e570c-107">Demoettevõtte kasutamisel saate seda protseduuri käitada ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="e570c-107">If you're using a demo data company, you can run this procedure in the USMF company.</span></span>


## <a name="add-a-new-procurement-category"></a><span data-ttu-id="e570c-108">Uue hankekategooria lisamine</span><span class="sxs-lookup"><span data-stu-id="e570c-108">Add a new procurement category</span></span>
1. <span data-ttu-id="e570c-109">Tehke valik Hanked > Hankekategooriad.</span><span class="sxs-lookup"><span data-stu-id="e570c-109">Go to Procurement and sourcing > Procurement categories.</span></span>
2. <span data-ttu-id="e570c-110">Klõpsake suvandit Kategooriahierarhia redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="e570c-110">Click Edit category hierarchy.</span></span>
    * <span data-ttu-id="e570c-111">Lehe vasakus servas kuvatakse praegune hankekategooria hierarhia.</span><span class="sxs-lookup"><span data-stu-id="e570c-111">The current procurement category hierarchy is displayed in the left side of the page.</span></span> <span data-ttu-id="e570c-112">Hakkate seda hierarhiat muutma.</span><span class="sxs-lookup"><span data-stu-id="e570c-112">You  are about to modify the hierarchy.</span></span>  
3. <span data-ttu-id="e570c-113">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="e570c-113">Click New category node.</span></span>
    * <span data-ttu-id="e570c-114">Süsteem valib vaikimisi ülemise sõlme.</span><span class="sxs-lookup"><span data-stu-id="e570c-114">The system selects the top node by default.</span></span> <span data-ttu-id="e570c-115">Kui käitate seda protseduuri ülesandejuhendina, saate klõpsata nuppu Ava ja valida teise ülataseme sõlme, millesse oma uus sõlm lisada.</span><span class="sxs-lookup"><span data-stu-id="e570c-115">If you are running this procedure as a task guide, you can click the Unlock button and select another parent node to insert your new node into.</span></span> <span data-ttu-id="e570c-116">Kui see on tehtud, lukustage uuesti ülesandejuhend ja klõpsake sõlme Uus kategooria.</span><span class="sxs-lookup"><span data-stu-id="e570c-116">Once that is done, lock the task guide again and then click New category node.</span></span>  
4. <span data-ttu-id="e570c-117">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e570c-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e570c-118">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e570c-118">In the Description field, type a value.</span></span>
6. <span data-ttu-id="e570c-119">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="e570c-119">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="e570c-120">Hüüdnimi on valikuline.</span><span class="sxs-lookup"><span data-stu-id="e570c-120">The friendly name is optional.</span></span> <span data-ttu-id="e570c-121">See kuvatakse kategooriaotsingutes koos kategooria nimega.</span><span class="sxs-lookup"><span data-stu-id="e570c-121">It will be displayed in category lookups together with the category name.</span></span>  
7. <span data-ttu-id="e570c-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e570c-122">Click Save.</span></span>

## <a name="add-products-to-your-new-procurement-category"></a><span data-ttu-id="e570c-123">Toodete lisamine uude hankekategooriasse</span><span class="sxs-lookup"><span data-stu-id="e570c-123">Add products to your new procurement category</span></span>
1. <span data-ttu-id="e570c-124">Tehke valik Hanked > Hankekategooriad.</span><span class="sxs-lookup"><span data-stu-id="e570c-124">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="e570c-125">Valige äsjalisatud sõlm.</span><span class="sxs-lookup"><span data-stu-id="e570c-125">Select the node you just added.</span></span> <span data-ttu-id="e570c-126">Kui käitate seda protseduuri ülesandejuhendina, peate sõlme valimiseks võib-olla ülesandejuhendi avama.</span><span class="sxs-lookup"><span data-stu-id="e570c-126">If you’re running this procedure as a task guide you might need to unlock the task guide to select the node.</span></span>  
2. <span data-ttu-id="e570c-127">Laiendage jaotist Tooted.</span><span class="sxs-lookup"><span data-stu-id="e570c-127">Toggle the expansion of the Products section.</span></span>
3. <span data-ttu-id="e570c-128">Klõpsake suvandit Lisa, et seostada tooted hankekategooriaga.</span><span class="sxs-lookup"><span data-stu-id="e570c-128">Click Add to associate products with the procurement category.</span></span>
4. <span data-ttu-id="e570c-129">Valige toode, mille soovite lisada hankekategooriasse.</span><span class="sxs-lookup"><span data-stu-id="e570c-129">Select the product you want to add to the procurement category.</span></span>
5. <span data-ttu-id="e570c-130">Klõpsake toote valimiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="e570c-130">Click the arrow to select the product.</span></span>
6. <span data-ttu-id="e570c-131">Valige teine toode, mille soovite lisada hankekategooriasse.</span><span class="sxs-lookup"><span data-stu-id="e570c-131">Select another product to add to the procurement category.</span></span>
7. <span data-ttu-id="e570c-132">Klõpsake toote valimiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="e570c-132">Click the arrow to select the product.</span></span>
8. <span data-ttu-id="e570c-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e570c-133">Click OK.</span></span>

## <a name="add-approved-and-preferred-vendors"></a><span data-ttu-id="e570c-134">Kinnitatud ja eelistatud hankijate lisamine</span><span class="sxs-lookup"><span data-stu-id="e570c-134">Add approved and preferred vendors</span></span>
1. <span data-ttu-id="e570c-135">Lülitage jaotise Hankijad laiendamist.</span><span class="sxs-lookup"><span data-stu-id="e570c-135">Toggle the expansion of the Vendors section.</span></span>
2. <span data-ttu-id="e570c-136">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e570c-136">Click Add.</span></span>
    * <span data-ttu-id="e570c-137">Saate lisada hankekategooriasse hankija ja määrata, kas hankija on eelistatud või kategooria jaoks lihtsalt kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="e570c-137">You can add a vendor to a procurement category and specify whether a vendor is preferred or just approved for the category.</span></span> <span data-ttu-id="e570c-138">Kui kustutate hankija kategooriast, ei kustutata kategooriast hankija ajaloolisi kandeid.</span><span class="sxs-lookup"><span data-stu-id="e570c-138">When you delete a vendor from a category, the historical transactions with the vendor in the category are not deleted.</span></span>   
3. <span data-ttu-id="e570c-139">Leidke hankija, kelle soovite lisada hankekategooriasse.</span><span class="sxs-lookup"><span data-stu-id="e570c-139">Find the vendor you want to add to the category.</span></span>
4. <span data-ttu-id="e570c-140">Klõpsake hankija valimiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="e570c-140">Click the arrow to select the vendor.</span></span>
5. <span data-ttu-id="e570c-141">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e570c-141">Click OK.</span></span>
6. <span data-ttu-id="e570c-142">Valige selle hankija rida, keda soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="e570c-142">Select the vendor row that you want to modify.</span></span>
7. <span data-ttu-id="e570c-143">Valige suvand väljal Hankija olek.</span><span class="sxs-lookup"><span data-stu-id="e570c-143">In the Vendor status field, select an option.</span></span>
    * <span data-ttu-id="e570c-144">Hankija valimise säte suvandis Kategooria poliitika reegel määrab, kas ostutaotlusel on saadaval eelistatud hankija, kinnitatud hankija või kõik hankijad.</span><span class="sxs-lookup"><span data-stu-id="e570c-144">The vendor selection setting in the Category policy rule governs whether preferred, approved, or all vendors are available on purchase requisitions.</span></span>   

## <a name="add-additional-information-to-the-category"></a><span data-ttu-id="e570c-145">Kategooriale lisateabe lisamine</span><span class="sxs-lookup"><span data-stu-id="e570c-145">Add additional information to the category</span></span>
1. <span data-ttu-id="e570c-146">Laiendage jaotist Hankija hindamiskriteeriumigrupid.</span><span class="sxs-lookup"><span data-stu-id="e570c-146">Toggle the expansion of the Vendor evaluation criterion groups section.</span></span>
    * <span data-ttu-id="e570c-147">Sellel vahekaardil saate määratleda, millise kriteeriumi järgi tuleks hankekategoorias olevaid hankijaid hinnata.</span><span class="sxs-lookup"><span data-stu-id="e570c-147">This tab allows you to define which criteria the vendors in the procurement category should be rated against.</span></span> <span data-ttu-id="e570c-148">Selleks klõpsake suvandit Lisa ja seejärel valige soovitud kriteeriumit sisaldav hankija hindamise grupp.</span><span class="sxs-lookup"><span data-stu-id="e570c-148">To do this you would click Add and then select a vendor evaluation group that contains the criteria you want.</span></span>  
2. <span data-ttu-id="e570c-149">Laiendage jaotist Küsimustikud.</span><span class="sxs-lookup"><span data-stu-id="e570c-149">Toggle the expansion of the Questionnaires section.</span></span>
    * <span data-ttu-id="e570c-150">Sellel vahekaardil saate lisada küsimustikke, mis kuvatakse tellimusel, kui määrate suvandi Tegevuse tüüp sätteks Tellimus.</span><span class="sxs-lookup"><span data-stu-id="e570c-150">This tab allows you to add questionnaires that will appear on the requisition, as long as you set the Activity type to "Requisition".</span></span> <span data-ttu-id="e570c-151">Sel juhul peab tellija enne hankekategooriasse kuuluva kindla toote või toodete tellimuse esitamist täitma küsimustiku.</span><span class="sxs-lookup"><span data-stu-id="e570c-151">The requester then has to fill out a questionnaire before they submit a requisition for the specific product or products in the procurement category.</span></span>  
3. <span data-ttu-id="e570c-152">Laiendage jaotist Kauba käibemaksugrupid.</span><span class="sxs-lookup"><span data-stu-id="e570c-152">Toggle the expansion of the Item sales tax groups section.</span></span>
4. <span data-ttu-id="e570c-153">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e570c-153">In the Item sales tax group: field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e570c-154">Saate valida käibemaksugrupi.</span><span class="sxs-lookup"><span data-stu-id="e570c-154">Select a sales tax group.</span></span>
6. <span data-ttu-id="e570c-155">Laiendage jaotist Kategooria leht.</span><span class="sxs-lookup"><span data-stu-id="e570c-155">Toggle the expansion of the Category page section.</span></span>
    * <span data-ttu-id="e570c-156">Kategooria lehed luuakse lehel Kategooria hierarhia.</span><span class="sxs-lookup"><span data-stu-id="e570c-156">Category pages are created in the Category hierarchy page.</span></span> <span data-ttu-id="e570c-157">Need sisaldavad teavet hankekategooria kohta, näiteks kategoorias olevate toodete tüüp, kategoorias olevate toodete pildid või teated, näiteks kategoorias saadaolevad allahindlused.</span><span class="sxs-lookup"><span data-stu-id="e570c-157">They contain information about the procurement category such as information about the type of products in a category, images of products in a category, or announcements such as the discounts that are available in a category.</span></span> <span data-ttu-id="e570c-158">Kategooria lehel olev teave kuvatakse ostutaotlustel.</span><span class="sxs-lookup"><span data-stu-id="e570c-158">The information in a category page is displayed on purchase requisitions.</span></span>  
7. <span data-ttu-id="e570c-159">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e570c-159">Close the page.</span></span>

