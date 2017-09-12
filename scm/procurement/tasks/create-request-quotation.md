--- 
title: Pakkumiskutse loomine
description: Selles protseduuris kirjeldatakse, kuidas luua pakkumiskutset.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
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
ms.openlocfilehash: 331f516f3483acd79be4ef7b95b53adcfbef1ae2
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="3d1d9-103">Pakkumiskutse loomine</span><span class="sxs-lookup"><span data-stu-id="3d1d9-103">Create a request for quotation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d1d9-104">Selles protseduuris kirjeldatakse, kuidas luua pakkumiskutset.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="3d1d9-105">Seda teeb tavaliselt ostuagent.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="3d1d9-106">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="3d1d9-107">Enne alustamist peavad olema seadistatud kutsetüübid.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="3d1d9-108">Kui olete selle ülesande lõpule viinud ning loonud ja saatnud pakkumiskutse, saate sisestada vastused hankija kohta, neid võrrelda ning määrata lepingu.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="3d1d9-109">Uue pakkumiskutse ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="3d1d9-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="3d1d9-110">Avage Hanked > Pakkumiskutsed > Kõik pakkumiskutsed.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="3d1d9-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-111">Click New.</span></span>
    * <span data-ttu-id="3d1d9-112">Saadaval on järgmised ostu tüübid. Ostutellimus (see on vaikesäte): dokument, mis kinnitab toodete ostmise pakkumise, või makse asemel toodete müümise pakkumise aktsepteerimine.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="3d1d9-113">Ostutaotlus: see tüüp valitakse automaatselt, kui loote pakkumiskutse otse ostutaotlusest.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="3d1d9-114">Kui valite selle suvandi käsitsi, kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="3d1d9-115">Ostuleping: lepe osta aja jooksul teatud koguses või väärtuses tooteid.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="3d1d9-116">Kui valite selle suvandi, peate valima ostulepingule kehtiva kuupäevavahemiku.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="3d1d9-117">Tippige väljale Dokumendi pealkiri väärtus.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="3d1d9-118">Sisestage või valige väljal Kutse tüüp väärtus.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="3d1d9-119">Kui hindamismeetod on seostatud kutse tüübiga, on see loodava pakkumiskutse vaikehindamismeetod.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="3d1d9-120">Hiljem on võimalik hindamismeetodit muuta.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="3d1d9-121">Sisestage kuupäev väljale Tarnekuupäev.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="3d1d9-122">Valige kuupäev, millal soovite kaubad saada.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="3d1d9-123">Sisestage väljale Aegumiskuupäev ja -kellaaeg kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="3d1d9-124">Määrake kuupäev ja kellaaeg, mis ajaks peavad hankijad pakkumiskutsele vastama.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="3d1d9-125">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="3d1d9-126">Tarneaadress on vaikimisi lao aadress.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="3d1d9-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="3d1d9-128">Lisa read</span><span class="sxs-lookup"><span data-stu-id="3d1d9-128">Add lines</span></span>
    * <span data-ttu-id="3d1d9-129">Pärast pakkumiskutse põhiteabe määramist saate määrata kaubad või teenused, mille kohta soovite hankijatelt pakkumisi saada.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="3d1d9-130">Kaup on rea vaiketüüp.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="3d1d9-131">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="3d1d9-132">Kui kasutate USMF-i, saate teha valiku T0020.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="3d1d9-133">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="3d1d9-134">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-134">Click Add line.</span></span>
4. <span data-ttu-id="3d1d9-135">Valige väljal Rea tüüp suvand Kategooria.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="3d1d9-136">Võite kasutada rea tüüpi Kategooria, et luua pakkumiskutseid mittelaokaupade või teenuste kohta.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="3d1d9-137">Teil tuleb valida kaupade või teenuste tüüp hankekategooriate hierarhiast.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="3d1d9-138">Sisestage või valige väärtus väljal Hanke kategooria.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="3d1d9-139">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="3d1d9-140">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="3d1d9-141">Sisestage või valige väärtus väljal Ühik.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="3d1d9-142">Hankijate lisamine</span><span class="sxs-lookup"><span data-stu-id="3d1d9-142">Add vendors</span></span>
1. <span data-ttu-id="3d1d9-143">Klõpsake päist, et lülituda reavaatekt päisevaatele.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="3d1d9-144">Laiendage üksuse Hankija jaotist.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="3d1d9-145">Klõpsake suvandit Hankijate automaatne lisamine.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="3d1d9-146">Saate hankijaid taotletud kaupade hankekategooria põhjal pakkumiskutsele automaatselt lisada.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="3d1d9-147">Kui ridadele lisatud kategooriate puhul pole kinnitatud hankijaid, saate lisada hankijad käsitsi.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="3d1d9-148">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-148">Click Add.</span></span>
5. <span data-ttu-id="3d1d9-149">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="3d1d9-150">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-150">Click Add.</span></span>
7. <span data-ttu-id="3d1d9-151">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="3d1d9-152">Kui olete hankija valinud, on olek Loodud.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="3d1d9-153">See tähendab, et hankija andmed on salvestatud pakkumiskutsesse, kuid te pole pakkumiskutset hankijale saatnud.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="3d1d9-154">Hankija saate lisada pakkumiskutsesse hankija olekust sõltumata.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="3d1d9-155">Pakkumiskutse saatmine hankijatele</span><span class="sxs-lookup"><span data-stu-id="3d1d9-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="3d1d9-156">Klõpsake käsku Saada.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-156">Click Send.</span></span>
    * <span data-ttu-id="3d1d9-157">Kontrollige lehel Pakkumiskutse saatmine, kas loendis on hankijad, kellele soovite pakkumiskutse saata.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="3d1d9-158">Klõpsake Prindi.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-158">Click Print.</span></span>
    * <span data-ttu-id="3d1d9-159">See dialoog võimaldab teil pakkumiskutset printida.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="3d1d9-160">Kui soovite printida vastuselehe, määratletakse selle sisu hankeparameetrites.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="3d1d9-161">Valimaks, kuidas vastuselehti printida, klõpsake pärast dialoogi Prindi avamist suvandit Täpsemad prindisuvandid.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="3d1d9-162">Iga hankija kohta prinditakse üks pakkumiskutse, mis sisaldab ridu olekus Loodud või Saadetud.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="3d1d9-163">Tühistatud ridu ja registreeritud vastustega ridu ei prindita.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="3d1d9-164">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-164">Click Cancel.</span></span>
4. <span data-ttu-id="3d1d9-165">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-165">Click OK.</span></span>
5. <span data-ttu-id="3d1d9-166">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-166">Close the page.</span></span>
6. <span data-ttu-id="3d1d9-167">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="3d1d9-168">Pakkumiskutse töölehe kuvamine</span><span class="sxs-lookup"><span data-stu-id="3d1d9-168">View the RFQ journal</span></span>
1. <span data-ttu-id="3d1d9-169">Avage Hanked > Pakkumiskutsed > Pakkumiskutsete järeltoimingud > Pakkumiskutse töölehed.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="3d1d9-170">Klõpsake suvandit Eelvaade/prindi.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="3d1d9-171">Klõpsake suvandit Algne eelvaade.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-171">Click Original preview.</span></span>
4. <span data-ttu-id="3d1d9-172">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-172">Close the page.</span></span>
5. <span data-ttu-id="3d1d9-173">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3d1d9-173">Close the page.</span></span>


