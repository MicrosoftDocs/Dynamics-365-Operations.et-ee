---
title: Hankija maksete ülevaade
description: See ülesande juhend annab ülevaate hankija maksete loomiseks kasutatavate eri meetodite, sh selle kohta, kuidas kasutada maksesoovitust või sisestada ühekordset makset käsitsi.
author: kweekley
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fcf22a3e9564f991b0cb5ebbd6a2282e3e749990
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177361"
---
# <a name="vendor-payment-overview"></a><span data-ttu-id="fd359-103">Hankija maksete ülevaade</span><span class="sxs-lookup"><span data-stu-id="fd359-103">Vendor payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd359-104">See ülesande juhend annab ülevaate hankija maksete loomiseks kasutatavate eri meetodite, sh selle kohta, kuidas kasutada maksesoovitust või sisestada ühekordset makset käsitsi.</span><span class="sxs-lookup"><span data-stu-id="fd359-104">This task guide will walk you through various methods used to create vendor payments, including how to use a payment proposal or manually entering a one-off payment.</span></span> <span data-ttu-id="fd359-105">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="fd359-105">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="fd359-106">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksed > Maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="fd359-106">Go to **Navigation pane > Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="fd359-107">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fd359-107">Click **New**.</span></span>
3. <span data-ttu-id="fd359-108">Valige maksetööleht, millele hankija maksed salvestada.</span><span class="sxs-lookup"><span data-stu-id="fd359-108">Select the payment journal in which to save the vendor payments.</span></span> 
4. <span data-ttu-id="fd359-109">Valige tööleht või sisestage see käsitsi.</span><span class="sxs-lookup"><span data-stu-id="fd359-109">Select the journal or manually enter it.</span></span>
5. <span data-ttu-id="fd359-110">Klõpsake **Read**.</span><span class="sxs-lookup"><span data-stu-id="fd359-110">Click **Lines**.</span></span>
6. <span data-ttu-id="fd359-111">Klõpsake **tegevuspaanil** valikut **Maksesoovitus**.</span><span class="sxs-lookup"><span data-stu-id="fd359-111">On **Ation pane**, click **Payment proposal**.</span></span>
7. <span data-ttu-id="fd359-112">Klõpsake suvandit **Loo maksesoovitus**.</span><span class="sxs-lookup"><span data-stu-id="fd359-112">Click **Create payment proposal**.</span></span> <span data-ttu-id="fd359-113">Maksesoovitus on päring, mida kasutatakse maksearvete valimiseks.</span><span class="sxs-lookup"><span data-stu-id="fd359-113">The payment proposal is a query used to select invoices for payment.</span></span> <span data-ttu-id="fd359-114">Saate redigeerida makstavate arvete loendit enne hankija maksete loomist.</span><span class="sxs-lookup"><span data-stu-id="fd359-114">You can edit the list of invoices to pay before creating or generating the vendor payments.</span></span>
8. <span data-ttu-id="fd359-115">Valige maksearved tähtaja, skonto või mõlema järgi.</span><span class="sxs-lookup"><span data-stu-id="fd359-115">Select invoices for payment by due date, cash discount, or both.</span></span> 
9. <span data-ttu-id="fd359-116">Sisestage tähtaja või skontoga võrdlemiseks kuupäev.</span><span class="sxs-lookup"><span data-stu-id="fd359-116">Enter the date for comparing to the due date or cash discount.</span></span> 
10. <span data-ttu-id="fd359-117">Valikuline: sisestage kõikide maksete puhul kasutatav maksekuupäev.</span><span class="sxs-lookup"><span data-stu-id="fd359-117">Optional: Enter a payment date used for all payments.</span></span> <span data-ttu-id="fd359-118">Siia sisestatud kuupäev on maksekuupäev kõikide lodud maksete puhul, olenemata maksetähtajast või skonto kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="fd359-118">The date entered here will be the payment date for all payments created, regardless of the due date or cash discount date.</span></span>  
11. <span data-ttu-id="fd359-119">Valikuline: sisestage varaseim maksekuupäev, mida võib maksekuupäevana kasutada.</span><span class="sxs-lookup"><span data-stu-id="fd359-119">Optional: Enter a minimum payment date which may be used as the payment date.</span></span> <span data-ttu-id="fd359-120">Varaseim maksekuupäev on maksete loomisel kasutatav varaseim kuupäev.</span><span class="sxs-lookup"><span data-stu-id="fd359-120">The minimum payment date will be the earliest date used when creating payments.</span></span> <span data-ttu-id="fd359-121">Näiteks kui arve tähtaeg on pärast varaseimat maksekuupäeva, muutub tähtaeg varaseima maksekuupäeva asemel maksekuupäevaks, et võimaldada arve maksmist võimalikult hilisel kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="fd359-121">For example, if an invoice has a due date after the minimum payment date, the due date will become the payment date instead of the minimum payment date in order to pay the invoice on the latest possible date.</span></span>
12. <span data-ttu-id="fd359-122">Sisestage täiendavad päringu piirangud jaotises **Kaasatavad kirjed**.</span><span class="sxs-lookup"><span data-stu-id="fd359-122">Enter additional query restrictions under **Records to include** section.</span></span> <span data-ttu-id="fd359-123">Filtrit kasutatakse sageli hankijagrupi või makseviisi makse puhul valitud arvete piiramiseks.</span><span class="sxs-lookup"><span data-stu-id="fd359-123">The filter is often used to restrict the invoices selected for payment by vendor group or method of payment.</span></span> <span data-ttu-id="fd359-124">Näiteks võite lisada filtri, et maksta arveid ainult selle palgaarvestusperioodi registreerimise järgi.</span><span class="sxs-lookup"><span data-stu-id="fd359-124">For example, you may add a filter to only pay invoices by check in this pay run.</span></span>
13. <span data-ttu-id="fd359-125">Sisestage täiendav päringu piirang või makse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="fd359-125">Enter additional query restriction or payment defaults.</span></span> <span data-ttu-id="fd359-126">Täiendavaid parameetreid saab kasutada makse valuuta määratlemiseks või selle palgaarvestusperioodi tsentraliseeritud maksete võimaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="fd359-126">The additional parameters can be used to define the payment currency or to enable centralized payments for this pay run.</span></span>  
14. <span data-ttu-id="fd359-127">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd359-127">Click **OK**.</span></span> <span data-ttu-id="fd359-128">Pärast nupu **OK** klõpsamist kuvatakse päringu tulemused.</span><span class="sxs-lookup"><span data-stu-id="fd359-128">After clicking **OK**, the results of the query will appear.</span></span> <span data-ttu-id="fd359-129">Kui te ei soovi maksmiseks valitud arvete loendit eelvaadata, saate naasta kiirkaardile **Parameteetrid** ja muuta sätte **Maksete loomine ilma arve eelvaateta** valikule Jah.</span><span class="sxs-lookup"><span data-stu-id="fd359-129">If you don't want to preview the list of invoices selected to pay, you can go back to the **Parameters** fast tab and change the setting **Create payments without invoice preview** to "Yes".</span></span>  
15. <span data-ttu-id="fd359-130">Valige nupp **Kuva maksete ülevaade**, et vaadata valitud arvel hankija puhul loodavaid makseid.</span><span class="sxs-lookup"><span data-stu-id="fd359-130">Choose the **Show payment overview** button to view the payments that will be created for the vendor on the invoice selected.</span></span>
16. <span data-ttu-id="fd359-131">Valige maksete peitmiseks nupp **Peida maksete ülevaade**.</span><span class="sxs-lookup"><span data-stu-id="fd359-131">Choose the **Hide payment overview** button to hide the payments.</span></span> 
17. <span data-ttu-id="fd359-132">Klõpsake suvandit **Maksete loomine**.</span><span class="sxs-lookup"><span data-stu-id="fd359-132">Click **Create payments**.</span></span> <span data-ttu-id="fd359-133">Enne nupu **Loo maksed** valimist saate paremklõpsata ruudustikul ja eksportida arvete loendi Excelisse.</span><span class="sxs-lookup"><span data-stu-id="fd359-133">Before choosing **Create payments**, you can right click on the grid and export the list of invoices to Excel.</span></span> <span data-ttu-id="fd359-134">Nupp **Loo maksed**loob makse töölehel hankija maksed.</span><span class="sxs-lookup"><span data-stu-id="fd359-134">The **Create payments** button will create the vendor payments in the payment journal.</span></span>  
18. <span data-ttu-id="fd359-135">Skannige makseid ja veenduge, et makseviis oleks määratletud kõikide maksete puhul.</span><span class="sxs-lookup"><span data-stu-id="fd359-135">Scan your payments and make sure the method of payment is defined for all payments.</span></span> <span data-ttu-id="fd359-136">Maksete loomisel, nt tšeki printimisel või elektroonilise makse loomisel peab olema määratletud makseviis.</span><span class="sxs-lookup"><span data-stu-id="fd359-136">If you generate the payments, such as printing a check or creating an electronic payment, the method of payment must be defined.</span></span> <span data-ttu-id="fd359-137">Makseviis määrab vaikimisi ka pangakonto, millelt makse tehakse.</span><span class="sxs-lookup"><span data-stu-id="fd359-137">The method of payment will also default the bank account from the payment will be made.</span></span>  
19. <span data-ttu-id="fd359-138">Ühekordse makse loomiseks klõpsake nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fd359-138">Click **New** to create a one-off payment.</span></span> <span data-ttu-id="fd359-139">Ühekordse makse saab maksetöölehele lisada mis tahes ajal enne sisestamist.</span><span class="sxs-lookup"><span data-stu-id="fd359-139">A one-off payment can be added to a payment journal at any time prior to posting.</span></span> <span data-ttu-id="fd359-140">Selleks klõpsake **Maksesoovituse** kasutamise asemel pigem nuppu **Uus** ja lisage makseteave käsitsi.</span><span class="sxs-lookup"><span data-stu-id="fd359-140">This is done by clicking the **New** button and adding the payment information manually, rather than using the **Payment proposal**.</span></span>  
20. <span data-ttu-id="fd359-141">Valige hankija, kellele makse tehakse.</span><span class="sxs-lookup"><span data-stu-id="fd359-141">Select the vendor to whom the payment will be made.</span></span>
21. <span data-ttu-id="fd359-142">Kui makstav arve on olemas, valige arve maksmiseks valimiseks suvand **Kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="fd359-142">If an invoice exists to pay, select **Settle transactions** to select the invoice for payment.</span></span> <span data-ttu-id="fd359-143">Kui tegemist on ettemaksuga, on see etapp valikuline.</span><span class="sxs-lookup"><span data-stu-id="fd359-143">If this is a prepayment, this step is optional.</span></span> <span data-ttu-id="fd359-144">Saate luua makse ilma arvet valimata.</span><span class="sxs-lookup"><span data-stu-id="fd359-144">You can create the payment without selecting any invoice.</span></span> 
22. <span data-ttu-id="fd359-145">Märkige kõik arved, mis makstakse.</span><span class="sxs-lookup"><span data-stu-id="fd359-145">Mark any invoices that will be paid.</span></span> <span data-ttu-id="fd359-146">Kasutades maksearvete valimiseks suvandit **Kannete tasakaalustamine**, arvutatakse maksesumma automaatselt selle põhjal, millised arved makse puhul märgite ja millise summa sisestate väljale **Tasakaalustatav summa**.</span><span class="sxs-lookup"><span data-stu-id="fd359-146">If you use the **Settle transactions** to select the invoices for payment, the payment amount will automatically be calculated based on what invoices you mark for payment, and what amount you enter in the **Amount to settle**.</span></span>
23. <span data-ttu-id="fd359-147">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd359-147">Click **OK**.</span></span>
24. <span data-ttu-id="fd359-148">Kui soovite makse kustutada, märkige rida.</span><span class="sxs-lookup"><span data-stu-id="fd359-148">If you want to delete a payment, mark the row.</span></span>
25. <span data-ttu-id="fd359-149">Klõpsake  **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="fd359-149">Click **Delete**.</span></span> <span data-ttu-id="fd359-150">Makse kustutamine kustutab ainult makse.</span><span class="sxs-lookup"><span data-stu-id="fd359-150">Deleting a payment will only delete the payment.</span></span> <span data-ttu-id="fd359-151">Mis tahes makse puhul märgitud arved on teise maksega tasumiseks endiselt saadaval.</span><span class="sxs-lookup"><span data-stu-id="fd359-151">Any invoices marked for payment will still be available to be paid by another payment.</span></span>
26. <span data-ttu-id="fd359-152">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="fd359-152">Click **Yes**.</span></span>
27. <span data-ttu-id="fd359-153">Valige tšekkide printimiseks või elektroonilise maksefaili loomiseks suvand **Loo makse**.</span><span class="sxs-lookup"><span data-stu-id="fd359-153">Choose **Generate payment** to print checks or create the electronic payment file.</span></span>
28. <span data-ttu-id="fd359-154">Valige makseviis, mille soovite luua.</span><span class="sxs-lookup"><span data-stu-id="fd359-154">Select the method of payment that you want to generate.</span></span> <span data-ttu-id="fd359-155">Maksetööleht võib sisaldada makseid nii tšekkide kui ka elektrooniliste maksete puhul, kuid saate luua ainult ühe maksetüübi korraga.</span><span class="sxs-lookup"><span data-stu-id="fd359-155">The payment journal can contain payments for both Checks and electronic payments, but you can only generate one payment type at a time.</span></span>
29. <span data-ttu-id="fd359-156">Valige pangakonto, millelt makseid luua.</span><span class="sxs-lookup"><span data-stu-id="fd359-156">Select the bank account from which to generate the payments.</span></span>
30. <span data-ttu-id="fd359-157">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd359-157">Click **OK**.</span></span> <span data-ttu-id="fd359-158">Maksed luuakse ainult maksete puhul, mis ühtivad teie valitud **makseviisi** ja **pangakontoga**.</span><span class="sxs-lookup"><span data-stu-id="fd359-158">Payments will only be generated for payments that match the **Method of payment** and **Bank account** you selected.</span></span>
31. <span data-ttu-id="fd359-159">**Tšekkide** loomisel valige suvand **Document**, tagamaks tšekkidele õige printimise sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="fd359-159">If you are generating **Checks**, choose **Document** to ensure the correct print destination for the checks.</span></span>
32. <span data-ttu-id="fd359-160">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd359-160">Click **OK**.</span></span>
33. <span data-ttu-id="fd359-161">Maksete loomiseks klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="fd359-161">Click **OK** to generate the payments.</span></span>
34. <span data-ttu-id="fd359-162">Kui kõik maksed on kinnitatud ja loodud, klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="fd359-162">Click **Post** if all the payments are approved and generated.</span></span> 
