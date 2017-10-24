--- 
title: "Pakkumiskutse pakkumiste sisestamine ja võrdlemine ning lepingute määramine"
description: "See protseduur näitab, kuidas sisestada pakkumiskutsele vastuseid, pakkumisi hinnata ja võrrelda ning seejärel määrata pakkumine ühele hankijatest."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
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
ms.openlocfilehash: 5dea9d7bfb1bf7b11f6c49cccaab1b73d4e58d16
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="da08e-103">Pakkumiskutse pakkumiste sisestamine ja võrdlemine ning lepingute määramine</span><span class="sxs-lookup"><span data-stu-id="da08e-103">Enter and compare RFQ bids and award contracts</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="da08e-104">See protseduur näitab, kuidas sisestada pakkumiskutsele vastuseid, pakkumisi hinnata ja võrrelda ning seejärel määrata pakkumine ühele hankijatest.</span><span class="sxs-lookup"><span data-stu-id="da08e-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="da08e-105">Saate seda protseduuri kasutada demoandmete ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="da08e-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="da08e-106">Enne alustamist peab teil olema pakkumiskutse kahe reaga, mis on saadetud vähemalt kahele hankijale.</span><span class="sxs-lookup"><span data-stu-id="da08e-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="da08e-107">Selle loomiseks saate käitada eeltingimusena protseduuri Pakkumiskutse loomine.</span><span class="sxs-lookup"><span data-stu-id="da08e-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="da08e-108">Teil on vaja seadistada hindamiskriteeriumid, enne kui saate seda protseduuri käitada.</span><span class="sxs-lookup"><span data-stu-id="da08e-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="da08e-109">Hankija vastuse sisestamine</span><span class="sxs-lookup"><span data-stu-id="da08e-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="da08e-110">Avage Hanked > Pakkumiskutsed > Kõik pakkumiskutsed.</span><span class="sxs-lookup"><span data-stu-id="da08e-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="da08e-111">Valige pakkumiskutse, mille olek on Saadetud, ja klõpsake linki pakkumiskutse juhtumi numbril.</span><span class="sxs-lookup"><span data-stu-id="da08e-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="da08e-112">Pakkumiskutse peaks olema saadetud vähemalt 2 hankijale.</span><span class="sxs-lookup"><span data-stu-id="da08e-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="da08e-113">Klõpsake päist, et avada hankijate loend.</span><span class="sxs-lookup"><span data-stu-id="da08e-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="da08e-114">Valige hankija, kellele soovite pakkumiskutses vastust sisestada.</span><span class="sxs-lookup"><span data-stu-id="da08e-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="da08e-115">Klõpsake nuppu Sisesta vastus.</span><span class="sxs-lookup"><span data-stu-id="da08e-115">Click Enter reply.</span></span>
6. <span data-ttu-id="da08e-116">Klõpsake toimingupaanil käsku Vasta.</span><span class="sxs-lookup"><span data-stu-id="da08e-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="da08e-117">Klõpsake käsku Kopeeri andmed vastuseväljadele.</span><span class="sxs-lookup"><span data-stu-id="da08e-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="da08e-118">Selle toiminguga kopeeritakse valitud andmed, näiteks kogus pakkumiskutse juhtumist pakkumiskutse vastusesse.</span><span class="sxs-lookup"><span data-stu-id="da08e-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="da08e-119">Teise võimalusena saate selle toimingu vahele jätta ja täita kõik väljad käsitsi vastust redigeerides.</span><span class="sxs-lookup"><span data-stu-id="da08e-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="da08e-120">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="da08e-120">Click Edit.</span></span>
9. <span data-ttu-id="da08e-121">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="da08e-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="da08e-122">Valige muu pakkumise rida.</span><span class="sxs-lookup"><span data-stu-id="da08e-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="da08e-123">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="da08e-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="da08e-124">Pakkumise hindamine</span><span class="sxs-lookup"><span data-stu-id="da08e-124">Score the bid</span></span>
1. <span data-ttu-id="da08e-125">Klõpsake päist, et avada pakkumise hindamine.</span><span class="sxs-lookup"><span data-stu-id="da08e-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="da08e-126">Laiendage jaotist Pakkumise hindamine.</span><span class="sxs-lookup"><span data-stu-id="da08e-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="da08e-127">Sisestage väljale Punktisumma number ühe hindamiskriteeriumi kohta.</span><span class="sxs-lookup"><span data-stu-id="da08e-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="da08e-128">Kui liigute hiirega üle mõne hindamiskriteeriumi, näitab kohtspikker vahemiku, millesse punktisumma peab jääma.</span><span class="sxs-lookup"><span data-stu-id="da08e-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="da08e-129">Selles demos saate lisada mis tahes kriteeriumidele arvu vahemikus 1 ja 5.</span><span class="sxs-lookup"><span data-stu-id="da08e-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="da08e-130">Valige teine hindamiskriteerium.</span><span class="sxs-lookup"><span data-stu-id="da08e-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="da08e-131">Sisestage väljale Punktisumma number.</span><span class="sxs-lookup"><span data-stu-id="da08e-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="da08e-132">Laiendage jaotist Küsimustikud.</span><span class="sxs-lookup"><span data-stu-id="da08e-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="da08e-133">Kui pakkumiskutse juhtumil on küsimustik, mis saadeti hankijatele, saate sisestada nende vastused küsimustiku ossa.</span><span class="sxs-lookup"><span data-stu-id="da08e-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="da08e-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da08e-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="da08e-135">Teisele hankijale vastuse sisestamine</span><span class="sxs-lookup"><span data-stu-id="da08e-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="da08e-136">Valige järgmine hankija, kustutades hankija, kellele äsja vastuse sisestasite, ja valides seejärel rea järgmisele hankijale.</span><span class="sxs-lookup"><span data-stu-id="da08e-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="da08e-137">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="da08e-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="da08e-138">Klõpsake nuppu Sisesta vastus.</span><span class="sxs-lookup"><span data-stu-id="da08e-138">Click Enter reply.</span></span>
4. <span data-ttu-id="da08e-139">Klõpsake käsku Kopeeri andmed vastuseväljadele.</span><span class="sxs-lookup"><span data-stu-id="da08e-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="da08e-140">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="da08e-140">Click Edit.</span></span>
6. <span data-ttu-id="da08e-141">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="da08e-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="da08e-142">Valige muu pakkumise rida.</span><span class="sxs-lookup"><span data-stu-id="da08e-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="da08e-143">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="da08e-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="da08e-144">Teise pakkumise hindamine</span><span class="sxs-lookup"><span data-stu-id="da08e-144">Score the second bid</span></span>
1. <span data-ttu-id="da08e-145">Klõpsake päist, et avada pakkumise hindamine.</span><span class="sxs-lookup"><span data-stu-id="da08e-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="da08e-146">Sisestage väljale Punktisumma number.</span><span class="sxs-lookup"><span data-stu-id="da08e-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="da08e-147">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="da08e-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="da08e-148">Sisestage väljale Punktisumma number.</span><span class="sxs-lookup"><span data-stu-id="da08e-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="da08e-149">Vastuste võrdlemine</span><span class="sxs-lookup"><span data-stu-id="da08e-149">Compare the replies</span></span>
1. <span data-ttu-id="da08e-150">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="da08e-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="da08e-151">Klõpsake käsku Võrdle vastuseid.</span><span class="sxs-lookup"><span data-stu-id="da08e-151">Click Compare replies.</span></span>
3. <span data-ttu-id="da08e-152">Sisestage väljale Tase number.</span><span class="sxs-lookup"><span data-stu-id="da08e-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="da08e-153">See leht näitab pakkumisi päise ja ridadega ning punktide kogusummat päise tasemel.</span><span class="sxs-lookup"><span data-stu-id="da08e-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="da08e-154">Saate ridu võrrelda, sortides ruudustikus nii, et võrreldavad read on üksteise kõrval.</span><span class="sxs-lookup"><span data-stu-id="da08e-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="da08e-155">Teave hõlmab ka väärtust Kogus: hankija pakutud kogus.</span><span class="sxs-lookup"><span data-stu-id="da08e-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="da08e-156">See ei pruugi võrduda pakkumiskutses määratud kogusega.</span><span class="sxs-lookup"><span data-stu-id="da08e-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="da08e-157">Netosumma: hankija määratud hind real olevatele kaupadele pärast mis tahes allahindluste lahutamist.</span><span class="sxs-lookup"><span data-stu-id="da08e-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="da08e-158">Hälve: Deviation – päevade arv, mille võrra pakkumise päise või rea tarnekuupäev pakkumiskutses päises või real taotletud tarnekuupäevast hälbib.</span><span class="sxs-lookup"><span data-stu-id="da08e-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="da08e-159">Saate sisestada taseme iga pakkumise puhul.</span><span class="sxs-lookup"><span data-stu-id="da08e-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="da08e-160">Valige päise rida teisele pakkumisele, mida soovite järjestada.</span><span class="sxs-lookup"><span data-stu-id="da08e-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="da08e-161">Sisestage väljale Tase number.</span><span class="sxs-lookup"><span data-stu-id="da08e-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="da08e-162">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="da08e-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="da08e-163">Pakkumise tagasilükkamine</span><span class="sxs-lookup"><span data-stu-id="da08e-163">Reject a bid</span></span>
1. <span data-ttu-id="da08e-164">Valige päise rida pakkumisele, mille soovite tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="da08e-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="da08e-165">Ühe pakkumise puhul saate korraga aktsepteerida, tagasi lükata või tagastada ühe pakkumise või rea.</span><span class="sxs-lookup"><span data-stu-id="da08e-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="da08e-166">Märkige ruut Märgi.</span><span class="sxs-lookup"><span data-stu-id="da08e-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="da08e-167">Kui valite pakkumise päises märkeruudu Märgi, märgitakse ka kõik read.</span><span class="sxs-lookup"><span data-stu-id="da08e-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="da08e-168">Samuti saate märkida pakkumise puhul ridade alamkogumi selle tagasilükkamiseks või aktsepteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="da08e-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="da08e-169">On võimalik aktsepteerida ühe hankija pakkumise pakkumiskutse mõne rea puhul ja siis määrata muud pakkumiskutse read erinevale hankijale, kuid teil tuleb seda teha kahes etapis, korraga ühes pakkumises.</span><span class="sxs-lookup"><span data-stu-id="da08e-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="da08e-170">Kui on olemas alternatiivsed read, saate aktsepteerida ainult esialgse pakkumise rea või selle alternatiivi, kuid mitte mõlemaid.</span><span class="sxs-lookup"><span data-stu-id="da08e-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="da08e-171">Klõpsake käsku Lükka tagasi.</span><span class="sxs-lookup"><span data-stu-id="da08e-171">Click Reject.</span></span>
4. <span data-ttu-id="da08e-172">Klõpsake suvandit Parameetrid rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="da08e-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="da08e-173">Väljal Tagasilükkamise põhjus sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="da08e-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="da08e-174">Tagasilükkamise põhjus salvestatakse vastuses.</span><span class="sxs-lookup"><span data-stu-id="da08e-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="da08e-175">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da08e-175">Click OK.</span></span>
7. <span data-ttu-id="da08e-176">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da08e-176">Click OK.</span></span>
8. <span data-ttu-id="da08e-177">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da08e-177">Close the page.</span></span>
9. <span data-ttu-id="da08e-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da08e-178">Close the page.</span></span>
10. <span data-ttu-id="da08e-179">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="da08e-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="da08e-180">Pakkumise aktsepteerimine</span><span class="sxs-lookup"><span data-stu-id="da08e-180">Accept a bid</span></span>
1. <span data-ttu-id="da08e-181">Valige pakkumine, mille soovite aktsepteerida, ja seejärel klõpsake linki väljal Pakkumiskutse.</span><span class="sxs-lookup"><span data-stu-id="da08e-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="da08e-182">Klõpsake toimingupaanil käsku Vasta.</span><span class="sxs-lookup"><span data-stu-id="da08e-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="da08e-183">Klõpsake suvandit Nõustu.</span><span class="sxs-lookup"><span data-stu-id="da08e-183">Click Accept.</span></span>
    * <span data-ttu-id="da08e-184">Kui olete märkinud teatud read ja mitte teisi, hõlmab aktsepteerimistoiming ainult märgitud ridu.</span><span class="sxs-lookup"><span data-stu-id="da08e-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="da08e-185">Kui soovite aktsepteerida kõiki pakkumise ridu, siis ei pea te ridu märkima.</span><span class="sxs-lookup"><span data-stu-id="da08e-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="da08e-186">Klõpsake suvandit Parameetrid rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="da08e-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="da08e-187">See võimaldab teil salvestada pakkumise aktsepteerimise põhjuse.</span><span class="sxs-lookup"><span data-stu-id="da08e-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="da08e-188">Põhjus salvestatakse pakkumisse.</span><span class="sxs-lookup"><span data-stu-id="da08e-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="da08e-189">Väljal Aktsepteerimise põhjus sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="da08e-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="da08e-190">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da08e-190">Click OK.</span></span>
7. <span data-ttu-id="da08e-191">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="da08e-191">Click OK.</span></span>
    * <span data-ttu-id="da08e-192">Kui klõpsate nuppu OK, luuakse ostutellimus pakkumiskutse kinnitusse lisatud ridade alusel.</span><span class="sxs-lookup"><span data-stu-id="da08e-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="da08e-193">Kui on teisi pakkumisi, mida ei ole töödeldud (aktsepteeritud, tagasi lükatud või tagastatud), siis palub süsteem teil ülejäänud pakkumised tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="da08e-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="da08e-194">Loodud ostutellimuse vaatamine</span><span class="sxs-lookup"><span data-stu-id="da08e-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="da08e-195">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="da08e-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="da08e-196">Klõpsake valikut Ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="da08e-196">Click Purchase order.</span></span>
    * <span data-ttu-id="da08e-197">Siin saate vaadata ostutellimust, mis loodi pakkumise aktsepteerimisel.</span><span class="sxs-lookup"><span data-stu-id="da08e-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="da08e-198">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da08e-198">Close the page.</span></span>
4. <span data-ttu-id="da08e-199">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da08e-199">Close the page.</span></span>
5. <span data-ttu-id="da08e-200">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da08e-200">Close the page.</span></span>
6. <span data-ttu-id="da08e-201">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da08e-201">Close the page.</span></span>


