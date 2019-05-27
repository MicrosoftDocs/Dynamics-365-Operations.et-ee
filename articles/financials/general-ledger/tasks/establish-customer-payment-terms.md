---
title: Kliendi maksetingimuste määramine
description: See protseduur määratleb skonto ja tähtaja seadistamise.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49f4047ab4bff6bdfbe8326a6680f9d8f9762c95
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547929"
---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="df431-103">Kliendi maksetingimuste määramine</span><span class="sxs-lookup"><span data-stu-id="df431-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df431-104">See protseduur määratleb skonto ja tähtaja seadistamise.</span><span class="sxs-lookup"><span data-stu-id="df431-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="df431-105">See ülesande juhend kasutab demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="df431-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="df431-106">Avage Müügireskontro > Maksete seadistus > Maksepäevad.</span><span class="sxs-lookup"><span data-stu-id="df431-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="df431-107">Maksetingimuste seadistust jagatakse Müügireskontro ja Ostureskontroga.</span><span class="sxs-lookup"><span data-stu-id="df431-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="df431-108">Kui määratlete selle moodulis, on see saadaval ka teises moodulis.</span><span class="sxs-lookup"><span data-stu-id="df431-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="df431-109">Selle ülesande juhendi puhul seadistan kõik maksetingimused suvandi Müügireskontro all.</span><span class="sxs-lookup"><span data-stu-id="df431-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="df431-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="df431-110">Click New.</span></span>
    * <span data-ttu-id="df431-111">Looge maksepäev, kui teie maksetingimused nõuavad kindlat nädalapäeva (esmaspäev, teisipäev, jne) või kindlat kuupäeva (5., 10., jne).</span><span class="sxs-lookup"><span data-stu-id="df431-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="df431-112">Sisestage maksepäeva ID maksepäeva väljale Maksepäev.</span><span class="sxs-lookup"><span data-stu-id="df431-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="df431-113">Sisestage maksepäeva kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="df431-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="df431-114">Valige väljal Nädal/kuu Nädal või Kuu.</span><span class="sxs-lookup"><span data-stu-id="df431-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="df431-115">Kui soovite sisestada nädalapäeva, nagu esmaspäev, valige nädal.</span><span class="sxs-lookup"><span data-stu-id="df431-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="df431-116">Kui soovite sisestada kuupäeva, nagu 10., valige kuu.</span><span class="sxs-lookup"><span data-stu-id="df431-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="df431-117">Selle näite puhul valige Kuu.</span><span class="sxs-lookup"><span data-stu-id="df431-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="df431-118">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="df431-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="df431-119">Kuupäev tuleb sisestada numbriga, nagu 10, mitte järgarvuna 10.</span><span class="sxs-lookup"><span data-stu-id="df431-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="df431-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="df431-120">Click Save.</span></span>
8. <span data-ttu-id="df431-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="df431-121">Close the page.</span></span>
9. <span data-ttu-id="df431-122">Avage Müügireskontro > Maksete seadistus > Maksetingimused.</span><span class="sxs-lookup"><span data-stu-id="df431-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="df431-123">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="df431-123">Click New.</span></span>
    * <span data-ttu-id="df431-124">Maksetingimusi kasutatakse määratlemaks, kuidas tähtaegu arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="df431-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="df431-125">Skonto kuupäeva seadistus on määratletud eraldi lehel.</span><span class="sxs-lookup"><span data-stu-id="df431-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="df431-126">Sisestage väljal Maksetingimused ID väljale Maksetingimused.</span><span class="sxs-lookup"><span data-stu-id="df431-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="df431-127">Sisestage kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="df431-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="df431-128">Valige makseviis, nagu Tasutakse kättesaamisel, Neto, Praegune kuu jne.</span><span class="sxs-lookup"><span data-stu-id="df431-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="df431-129">Maksetingimusi kasutatakse määratlemaks, kuidas tähtaja algust arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="df431-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="df431-130">Näiteks netot kasutatakse, kui tähtaeg on alati teatud arv kuid või päevi pärast arve kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="df431-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="df431-131">Suvandit Tasutakse kättesaamisel saab kasutada, kui makset nõutakse arve saamisel, nii et tähtaega ei arvutata.</span><span class="sxs-lookup"><span data-stu-id="df431-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="df431-132">Valige selle ülesande juhendi puhul Käesolev kuu.</span><span class="sxs-lookup"><span data-stu-id="df431-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="df431-133">Valige maksepäev, kui arvutusse on kaasatud kindel nädalapäev või kuupäev.</span><span class="sxs-lookup"><span data-stu-id="df431-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="df431-134">Olenevalt maksetingimustest võite koguse sisestada kuudes või päevades.</span><span class="sxs-lookup"><span data-stu-id="df431-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="df431-135">Võite maksemeetodile lisamiseks kasutada ka valikut Maksegraafik või Maksepäev.</span><span class="sxs-lookup"><span data-stu-id="df431-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="df431-136">Kui tähtaeg on alati järgmise kuu 10. kuupäev, valige Maksepäevaks 10. kuupäev.</span><span class="sxs-lookup"><span data-stu-id="df431-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="df431-137">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="df431-137">Click Save.</span></span>
16. <span data-ttu-id="df431-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="df431-138">Close the page.</span></span>
17. <span data-ttu-id="df431-139">Avage Müügireskontro > Maksete seadistus > Skontod.</span><span class="sxs-lookup"><span data-stu-id="df431-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="df431-140">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="df431-140">Click New.</span></span>
    * <span data-ttu-id="df431-141">Seda lehte kasutatakse määratlemaks, kuidas skonto kuupäeva arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="df431-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="df431-142">Sisestage väljal Skonto ID väljale Skonto.</span><span class="sxs-lookup"><span data-stu-id="df431-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="df431-143">Sisestage kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="df431-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="df431-144">Kui saadaval on mitmetasandiline skonto, valige Järgmine skonto kood, mis on pärast seda uut skontot oluline.</span><span class="sxs-lookup"><span data-stu-id="df431-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="df431-145">Sisestage skonto kuupäeva arvutamiseks kasutatav päevade arv.</span><span class="sxs-lookup"><span data-stu-id="df431-145">Enter the number of days used to calculate the cash dicount date.</span></span>
    * <span data-ttu-id="df431-146">Neto põhimõtte valimisel lisatakse skonto kuupäeva arvutamiseks päevade arv arve kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="df431-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="df431-147">Sisestage skonto protsent.</span><span class="sxs-lookup"><span data-stu-id="df431-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="df431-148">Sisestage põhikonto, millele sisestatakse skonto kliendiarvete puhul.</span><span class="sxs-lookup"><span data-stu-id="df431-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="df431-149">Valige suvand väljalt Allahindluse vastaskontod.</span><span class="sxs-lookup"><span data-stu-id="df431-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="df431-150">Kui valite suvandi Kontod arve real, sisestatakse skonto hankija arve ridadel sama vara/kulu põhikontole.</span><span class="sxs-lookup"><span data-stu-id="df431-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="df431-151">Kui valite suvandi Kasuta hankija arvete puhul põhikontot, sisestatakse skonto põhikontole, mille määratlete suvandis Hankija arvete põhikonto.</span><span class="sxs-lookup"><span data-stu-id="df431-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="df431-152">Selle näite puhul valige suvand Kasuta hankija arvete puhul põhikontot.</span><span class="sxs-lookup"><span data-stu-id="df431-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="df431-153">Sisestage põhikonto, millele sisestatakse skonto hankija arvete puhul.</span><span class="sxs-lookup"><span data-stu-id="df431-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="df431-154">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="df431-154">Click Save.</span></span>

