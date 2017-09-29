--- 
title: Tarnegraafikuga ostutellimuse loomine
description: "See protseduur näitab, kuidas ostutellimuse jaoks tarnegraafikut luua."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1e4a0204d74c8966cd90b52ae13c88e222ebc3ef
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-order-with-a-delivery-schedule"></a><span data-ttu-id="371f8-103">Tarnegraafikuga ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="371f8-103">Create a purchase order with a delivery schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="371f8-104">See protseduur näitab, kuidas ostutellimuse jaoks tarnegraafikut luua.</span><span class="sxs-lookup"><span data-stu-id="371f8-104">This procedure demonstrates how to create a delivery schedule for a purchase order.</span></span> <span data-ttu-id="371f8-105">Tarnegraafikut kasutatakse siis, kui tellimuse või töölehe koguse puhul on nõutav mitme saadetisega tarne.</span><span class="sxs-lookup"><span data-stu-id="371f8-105">A delivery schedule is used when a quantity on an order or a journal is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="371f8-106">Selles juhendis toodud näidet saab kasutada demoandmete ettevõtte USMF puhul.</span><span class="sxs-lookup"><span data-stu-id="371f8-106">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="371f8-107">Selle protseduuri viib tavaliselt läbi ostuagent.</span><span class="sxs-lookup"><span data-stu-id="371f8-107">This procedure would typically be done by a purchasing agent.</span></span>


## <a name="create-a-delivery-schedule"></a><span data-ttu-id="371f8-108">Tarnegraafiku loomine</span><span class="sxs-lookup"><span data-stu-id="371f8-108">Create a delivery schedule</span></span>
1. <span data-ttu-id="371f8-109">Avage Hanked > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="371f8-109">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="371f8-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="371f8-110">Click New.</span></span>
3. <span data-ttu-id="371f8-111">Sisestage väljale Hankija konto väärtus US-101.</span><span class="sxs-lookup"><span data-stu-id="371f8-111">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="371f8-112">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="371f8-112">Click OK.</span></span>
5. <span data-ttu-id="371f8-113">Sisestage väljale Kauba kood väärtus M0001.</span><span class="sxs-lookup"><span data-stu-id="371f8-113">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="371f8-114">Sisestage väljale Kogus number 10.</span><span class="sxs-lookup"><span data-stu-id="371f8-114">In the Quantity field, enter 10.</span></span>
7. <span data-ttu-id="371f8-115">Klõpsake suvandit Ostutellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="371f8-115">Click Purchase order line.</span></span>
8. <span data-ttu-id="371f8-116">Klõpsake valikut Tarnegraafik.</span><span class="sxs-lookup"><span data-stu-id="371f8-116">Click Delivery schedule.</span></span>
    * <span data-ttu-id="371f8-117">Lehel Tarnegraafik saate määrata, mitme saadetisega tellimuse rea lõplik kogus hankijalt tarnitakse.</span><span class="sxs-lookup"><span data-stu-id="371f8-117">The Delivery schedule page allows you to specify the number of shipments in which the total quantity of the order line will be delivered from the vendor.</span></span>  
    * <span data-ttu-id="371f8-118">Vaikimisi kopeerib süsteem esimesele tarnegraafiku reale lõpliku koguse ja muud tarne üksikasjad algselt ostutellimuse realt.</span><span class="sxs-lookup"><span data-stu-id="371f8-118">By default, the system copies the total quantity and other delivery details of the original purchase line into the first delivery schedule line.</span></span> <span data-ttu-id="371f8-119">Selles näites loome kahe saadetisega graafiku, kus teise saadetise kuupäev on nädala võrra hilisem esimese saadetise omast.</span><span class="sxs-lookup"><span data-stu-id="371f8-119">In this example, we’ll create a schedule for two shipments, with the second shipment’s date offset by a week from the first shipment.</span></span>  
9. <span data-ttu-id="371f8-120">Määrake väljal Kogus koguseks 4.</span><span class="sxs-lookup"><span data-stu-id="371f8-120">In the Quantity field, change the quantity to 4.</span></span>
10. <span data-ttu-id="371f8-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="371f8-121">Click New.</span></span>
11. <span data-ttu-id="371f8-122">Sisestage väljale Kogus järelejäänud koguseks 6.</span><span class="sxs-lookup"><span data-stu-id="371f8-122">In the Quantity field, enter 6 as the remaining quantity.</span></span>
    * <span data-ttu-id="371f8-123">Valige väljalt Tarnekuupäev kuupäev, mis on üks nädal pärast esimesel tarne real olevat kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="371f8-123">In the delivery date field, select a date that’s one week after the date on the first delivery line.</span></span>  
    * <span data-ttu-id="371f8-124">Väljade Kokku ja Järelejäänud abil saate jälgida lõplikku kogust, mis tarnegraafiku ridadele eraldati.</span><span class="sxs-lookup"><span data-stu-id="371f8-124">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="371f8-125">Kui järelejäänud kogus on null, eraldati graafikusse algse rea täielik kogus.</span><span class="sxs-lookup"><span data-stu-id="371f8-125">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>  
12. <span data-ttu-id="371f8-126">Laiendage jaotist Tasude teisendamine.</span><span class="sxs-lookup"><span data-stu-id="371f8-126">Expand the Charges conversion section.</span></span>
    * <span data-ttu-id="371f8-127">Siin olevad valikud võimaldavad teil juhtida, kuidas soovite tasusid tarnegraafiku ridade vahel jagada.</span><span class="sxs-lookup"><span data-stu-id="371f8-127">The options here allow you to control how you want charges to be distributed across the delivery schedule lines.</span></span> <span data-ttu-id="371f8-128">Kui valite Kopeeri brutosummad, kopeeritakse igale tarnereale algsel tellimuse real olev tasu summa.</span><span class="sxs-lookup"><span data-stu-id="371f8-128">If you select Copy gross amounts, the charge amount on the original order line is copied to each delivery line.</span></span> <span data-ttu-id="371f8-129">Valik Eralda tarneridadele jagab algse rea tasu koguse järgi igale tarnereale.</span><span class="sxs-lookup"><span data-stu-id="371f8-129">The Allocate to delivery lines option divides the original line charge according to the quantity on each delivery line.</span></span>  
13. <span data-ttu-id="371f8-130">Ahendage jaotist Tasude teisendamine.</span><span class="sxs-lookup"><span data-stu-id="371f8-130">Collapse the Charges conversion section.</span></span>
14. <span data-ttu-id="371f8-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="371f8-131">Click OK.</span></span>
    * <span data-ttu-id="371f8-132">Tarnegraafik on nüüd tellimusele rakendatud.</span><span class="sxs-lookup"><span data-stu-id="371f8-132">The delivery schedule has now been applied to the order.</span></span>  
    * <span data-ttu-id="371f8-133">Algne tellimuse rida, mida nimetatakse nüüd äriandmete reaks, on teisendatud mitme tarnega tellimuse reaks.</span><span class="sxs-lookup"><span data-stu-id="371f8-133">The original order line, now referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="371f8-134">See on tähistatud eristatava ikooniga ja see toimib nagu tarneridade päis.</span><span class="sxs-lookup"><span data-stu-id="371f8-134">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
15. <span data-ttu-id="371f8-135">Valige teine tellimuse rida, mis on kahest tarnereast esimene.</span><span class="sxs-lookup"><span data-stu-id="371f8-135">Select the second order line, which is the first of the two delivery lines.</span></span>
    * <span data-ttu-id="371f8-136">Kaks uut rida, mida nimetatakse tarneridadeks, moodustavad ühe tarnegraafiku.</span><span class="sxs-lookup"><span data-stu-id="371f8-136">The two new lines, referred to as Delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="371f8-137">Tellimust töödeldakse nende ridade, mitte algse rea alusel.</span><span class="sxs-lookup"><span data-stu-id="371f8-137">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="371f8-138">Dokumentide, nagu kinnitused, toote sissetuleku töölehed või arved, printimisel kuvatakse ainult tarneread.</span><span class="sxs-lookup"><span data-stu-id="371f8-138">If documents such as confirmations, product receipt journals, or invoices are printed, only the delivery lines are shown.</span></span>  

## <a name="change-the-delivery-schedule"></a><span data-ttu-id="371f8-139">Tarnegraafiku muutmine</span><span class="sxs-lookup"><span data-stu-id="371f8-139">Change the delivery schedule</span></span>
    * <span data-ttu-id="371f8-140">Saate tarneridadel koguseid muuta.</span><span class="sxs-lookup"><span data-stu-id="371f8-140">You can change the quantity on delivery lines.</span></span> <span data-ttu-id="371f8-141">Kui seda teete, uuendatakse tarneridade lõpliku koguse järgi automaatselt äriandmete rida.</span><span class="sxs-lookup"><span data-stu-id="371f8-141">If you do this, the commercial line is automatically updated to the total quantity in the delivery lines.</span></span>  
1. <span data-ttu-id="371f8-142">Määrake esimese tarnerea väljal Kogus koguseks 4 asemel 5.</span><span class="sxs-lookup"><span data-stu-id="371f8-142">In the Quantity field of the first delivery line, change the quantity from 4 to 5.</span></span>
2. <span data-ttu-id="371f8-143">Valige esimene tellimuse rida (äriandmete rida).</span><span class="sxs-lookup"><span data-stu-id="371f8-143">Select the first order line (the commercial line).</span></span>
    * <span data-ttu-id="371f8-144">Äriandmete real olevaks koguseks on määratud 11.</span><span class="sxs-lookup"><span data-stu-id="371f8-144">The quantity on the commercial line has been changed to 11.</span></span>  

## <a name="process-product-receipt-using-delivery-schedules"></a><span data-ttu-id="371f8-145">Toote sissetuleku töötlemine tarnegraafikuid kasutades</span><span class="sxs-lookup"><span data-stu-id="371f8-145">Process product receipt using delivery schedules</span></span>
    * <span data-ttu-id="371f8-146">Ostutellimus tuleb enne toote sissetuleku töötlemist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="371f8-146">The purchase order must be confirmed before product receipt can be processed.</span></span> <span data-ttu-id="371f8-147">Selles näites kajastatakse sissetulek otse ostutellimusel.</span><span class="sxs-lookup"><span data-stu-id="371f8-147">In this example, receipt is recorded directly on the purchase order.</span></span> <span data-ttu-id="371f8-148">Sissetuleku oleks saanud registreerida ka siis, kui kaubad lattu saabusid.</span><span class="sxs-lookup"><span data-stu-id="371f8-148">Receipt could also have been recorded when the goods arrived in the warehouse.</span></span>  
1. <span data-ttu-id="371f8-149">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="371f8-149">On the Action Pane, click Purchase.</span></span>
2. <span data-ttu-id="371f8-150">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="371f8-150">Click Confirm.</span></span>
3. <span data-ttu-id="371f8-151">Klõpsake toimingupaanil valikut Vastuvõtt.</span><span class="sxs-lookup"><span data-stu-id="371f8-151">On the Action Pane, click Receive.</span></span>
4. <span data-ttu-id="371f8-152">Klõpsake valikut Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="371f8-152">Click Product receipt.</span></span>
5. <span data-ttu-id="371f8-153">Sisestage suvaline väärtus väljale Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="371f8-153">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="371f8-154">Seda välja kasutatakse viite sisestamiseks, mida kasutatakse toote sissetuleku töölehe kandena.</span><span class="sxs-lookup"><span data-stu-id="371f8-154">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
    * <span data-ttu-id="371f8-155">Tehke väljal Kogus valik Tellitud kogus.</span><span class="sxs-lookup"><span data-stu-id="371f8-155">In the Quantity field, select ‘Ordered quantity’.</span></span> <span data-ttu-id="371f8-156">See valik tähendab, et sissetulekut töödeldakse koguse puhul, millega tellimuse read loodi.</span><span class="sxs-lookup"><span data-stu-id="371f8-156">This option means that receipt will process for the quantity that the order lines were created with.</span></span>  
    * <span data-ttu-id="371f8-157">Veenduge, et välja Toote sissetuleku printimine väärtuseks on määratud Ei.</span><span class="sxs-lookup"><span data-stu-id="371f8-157">Make sure that the Print product receipt field is set to No.</span></span> <span data-ttu-id="371f8-158">Selles näites ei ole printimine vajalik.</span><span class="sxs-lookup"><span data-stu-id="371f8-158">Printing isn’t needed in this example.</span></span>  
6. <span data-ttu-id="371f8-159">Laiendage jaotist Read.</span><span class="sxs-lookup"><span data-stu-id="371f8-159">Expand the Lines section.</span></span>
    * <span data-ttu-id="371f8-160">Pange tähele, kuidas toote sissetulek luuakse kahe tarnerea ja mitte algse tellimuse rea puhul.</span><span class="sxs-lookup"><span data-stu-id="371f8-160">Notice how the product receipt is created for the two delivery lines and not the original order line.</span></span> <span data-ttu-id="371f8-161">Kui sissetulek oleks laos registreeritud, oleks see registreeritud ka tarnegraafiku ridadel.</span><span class="sxs-lookup"><span data-stu-id="371f8-161">If receipt had been recorded in the warehouse, it would also have been recorded on the delivery schedule lines.</span></span>  
7. <span data-ttu-id="371f8-162">Ahendage jaotist Read.</span><span class="sxs-lookup"><span data-stu-id="371f8-162">Collapse the Lines section.</span></span>
8. <span data-ttu-id="371f8-163">Klõpsake sissetuleku sisestamiseks nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="371f8-163">Click OK to post the receipt.</span></span>


