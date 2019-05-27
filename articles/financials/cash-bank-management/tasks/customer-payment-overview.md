---
title: Kliendimaksete ülevaade
description: Sellest tegevusejuhisest leiate ülevaate klindimaksete sisestamiseks kasutatavate eri meetodite kohta.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, CustPaymEntry, CustTableLookup, LedgerJournalTransCustPaym, CustOpenTrans, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6e82be0d68165f62bbdc72a70b0675c7418b14ae
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566129"
---
# <a name="customer-payment-overview"></a><span data-ttu-id="845aa-103">Kliendimaksete ülevaade</span><span class="sxs-lookup"><span data-stu-id="845aa-103">Customer payment overview</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="845aa-104">Sellest tegevusejuhisest leiate ülevaate klindimaksete sisestamiseks kasutatavate eri meetodite kohta.</span><span class="sxs-lookup"><span data-stu-id="845aa-104">This task guide walks through various methods used to enter customer payments.</span></span> <span data-ttu-id="845aa-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="845aa-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="845aa-106">Avage Müügireskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="845aa-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="845aa-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="845aa-107">Click New.</span></span>
3. <span data-ttu-id="845aa-108">Valige maksetööleht, millele kliendi maksed salvestatakse.</span><span class="sxs-lookup"><span data-stu-id="845aa-108">Select the payment journal which the customer payments will be saved.</span></span>
4. <span data-ttu-id="845aa-109">Valige tööleht või sisestage see käsitsi.</span><span class="sxs-lookup"><span data-stu-id="845aa-109">Select or manually enter the journal.</span></span>
5. <span data-ttu-id="845aa-110">Klõpsake valikut Sisesta kliendimaksed.</span><span class="sxs-lookup"><span data-stu-id="845aa-110">Click Enter customer payments.</span></span>
    * <span data-ttu-id="845aa-111">Valikut Sisesta kliendimaksed kasutatakse ühe kliendimakse kirjendamiseks korraga.</span><span class="sxs-lookup"><span data-stu-id="845aa-111">Enter customer payments is used to record one customer payment at a time.</span></span> <span data-ttu-id="845aa-112">Makseteabe sisestate lehe ülaossa ja seejärel saate sama lehe kaudu märkida kõik maksega tasutud arved.</span><span class="sxs-lookup"><span data-stu-id="845aa-112">You enter the payment information at the top, and then you can mark the invoices that were paid by the payment, all from the same page.</span></span>  
6. <span data-ttu-id="845aa-113">Sisestage klient, kellelt makse saite.</span><span class="sxs-lookup"><span data-stu-id="845aa-113">Enter the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="845aa-114">Kui te ei tea klienti, kuid teate makstud kannet, saate makse sisestamiseks kasutada välja Kanne.</span><span class="sxs-lookup"><span data-stu-id="845aa-114">If you don't know the customer but do know a transaction that was paid, you can use the Transaction field to enter the payment.</span></span> <span data-ttu-id="845aa-115">Sisestage või valige arve väljal Kanne.</span><span class="sxs-lookup"><span data-stu-id="845aa-115">Enter or select the invoice in the Transaction field.</span></span> <span data-ttu-id="845aa-116">Klient tuuakse pärast kande valimist vaikimisi automaatselt.</span><span class="sxs-lookup"><span data-stu-id="845aa-116">The customer will automatically default after you select the transaction.</span></span>  
7. <span data-ttu-id="845aa-117">Sisestage makseviide väljale Makseviide.</span><span class="sxs-lookup"><span data-stu-id="845aa-117">In the Payment reference field, enter a payment reference.</span></span>
    * <span data-ttu-id="845aa-118">Makseviide võib olla kliendi tšekinumber või kliendi elektroonilise makse viide.</span><span class="sxs-lookup"><span data-stu-id="845aa-118">The payment reference could be the customer's check number or a reference from the customer's electronic payment.</span></span> <span data-ttu-id="845aa-119">Makseviide on vajalik vaid juhul, kui märgite makse kaasamise deposiidikviitungile.</span><span class="sxs-lookup"><span data-stu-id="845aa-119">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="845aa-120">Valige, kas makse kaasatakse deposiitkviitungile.</span><span class="sxs-lookup"><span data-stu-id="845aa-120">Select whether the payment will be included on a deposit slip.</span></span> 
9. <span data-ttu-id="845aa-121">Sisestage kliendimakse summa.</span><span class="sxs-lookup"><span data-stu-id="845aa-121">Enter the amount of the customer payment.</span></span>
    * <span data-ttu-id="845aa-122">Maksesummat ei tooda vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="845aa-122">The payment amount will not default.</span></span> <span data-ttu-id="845aa-123">See tuleb käsitsi sisestada.</span><span class="sxs-lookup"><span data-stu-id="845aa-123">It must be manually entered.</span></span>  
10. <span data-ttu-id="845aa-124">Märkige kliendi makstud arved.</span><span class="sxs-lookup"><span data-stu-id="845aa-124">Mark the invoices that were paid by the customer.</span></span>
    * <span data-ttu-id="845aa-125">Kui makse on ettemaks, ei pea te tasakaalustamiseks märkima ühtegi arvet.</span><span class="sxs-lookup"><span data-stu-id="845aa-125">If the payment is a prepayment, you are not required to mark any invoices for settlement.</span></span> <span data-ttu-id="845aa-126">Makse saab siiski salvestada ja sisestada.</span><span class="sxs-lookup"><span data-stu-id="845aa-126">The payment can still be saved and posted.</span></span> <span data-ttu-id="845aa-127">Arve tasakaalustamine võib toimuda hiljem.</span><span class="sxs-lookup"><span data-stu-id="845aa-127">Settlement to an invoice can happen at a later time.</span></span>  
11. <span data-ttu-id="845aa-128">Sisestage maksesumma, mis tuleks märgitud arvel tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="845aa-128">Enter the amount of the payment that should be settled to the marked invoice.</span></span> 
    * <span data-ttu-id="845aa-129">Seda välja saab kasutada, kui makse on osamakseks.</span><span class="sxs-lookup"><span data-stu-id="845aa-129">This field can be used when the payment is for a partial payment.</span></span> <span data-ttu-id="845aa-130">Kui te summat ei sisesta, määratakse tasakaalustatav summa automaatselt teie eest.</span><span class="sxs-lookup"><span data-stu-id="845aa-130">If you don't enter an amount, the amount to settle will automatically be determined for you.</span></span>  
12. <span data-ttu-id="845aa-131">Klõpsake käsku Salvesta töölehel.</span><span class="sxs-lookup"><span data-stu-id="845aa-131">Click Save in journal.</span></span>
    * <span data-ttu-id="845aa-132">Enne makse töölehele salvestamist veenduge, et vastaskonto oleks määratletud.</span><span class="sxs-lookup"><span data-stu-id="845aa-132">Before you save the payment to the journal, make sure that the offset account is defined.</span></span> <span data-ttu-id="845aa-133">Käsuga Salvesta töölehel salvestatakse makse ja teisaldatakse see töölehele.</span><span class="sxs-lookup"><span data-stu-id="845aa-133">Using Save in journal will save the payment and move it to the journal.</span></span> <span data-ttu-id="845aa-134">Seejärel saate jätkata järgmise makse sisestamist.</span><span class="sxs-lookup"><span data-stu-id="845aa-134">You can then continue entering the next payment.</span></span>  
13. <span data-ttu-id="845aa-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="845aa-135">Close the page.</span></span>
14. <span data-ttu-id="845aa-136">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="845aa-136">Click Lines.</span></span>
    * <span data-ttu-id="845aa-137">Ridade avamisel näete kõiki lehele Kliendimaksete sisestamine ja töölehele salvestatud makseid.</span><span class="sxs-lookup"><span data-stu-id="845aa-137">When opening Lines, you will see any payments you recorded on the Enter customer payments page and saved into the journal.</span></span> <span data-ttu-id="845aa-138">Saate seda lehte kasutada ka uute kliendimaksete sisestamiseks või enne sisestamist olemasoleva kliendimakse redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="845aa-138">You can also use this page to enter new customer payments, or edit existing customer payment before they are posted.</span></span>  
15. <span data-ttu-id="845aa-139">Teise makse loomiseks klõpsake nuppu Uus.</span><span class="sxs-lookup"><span data-stu-id="845aa-139">Click New to create another payment.</span></span> 
16. <span data-ttu-id="845aa-140">Valige klient, kellelt makse saite.</span><span class="sxs-lookup"><span data-stu-id="845aa-140">Select the customer from whom you received the payment.</span></span>
    * <span data-ttu-id="845aa-141">Kui te klienti ei tea, kuid teate maksega tasutud arvet, kasutage arve käsitsi sisestamiseks või valimiseks välja Arve.</span><span class="sxs-lookup"><span data-stu-id="845aa-141">If you don't know the customer but know an invoice paid by the payment, use the Invoice field to manually enter or select the invoice.</span></span> <span data-ttu-id="845aa-142">Klient tuuakse vaikimisi pärast arve valimist.</span><span class="sxs-lookup"><span data-stu-id="845aa-142">The customer will default after the invoice is selected.</span></span>  
17. <span data-ttu-id="845aa-143">Klõpsake tasutud arvete märkimiseks valikut Kannete tasakaalustamine.</span><span class="sxs-lookup"><span data-stu-id="845aa-143">Click Settle transctions to mark invoices that were paid.</span></span>
    * <span data-ttu-id="845aa-144">Te ei pea makset mis tahes arvetel tasakaalustama.</span><span class="sxs-lookup"><span data-stu-id="845aa-144">You are not required to settle the payment to any invoices.</span></span> <span data-ttu-id="845aa-145">Kui tegemist on ettemaksuga või kui te ei tea, milline arve on tasutud, saate makse sisestada.</span><span class="sxs-lookup"><span data-stu-id="845aa-145">If this is a prepayment or if you don't know what invoice was paid, you can enter and post the payment.</span></span> <span data-ttu-id="845aa-146">Makse saab arvel tasakaalustada hiljem.</span><span class="sxs-lookup"><span data-stu-id="845aa-146">The payment can be settled to an invoice at a later point.</span></span>  
18. <span data-ttu-id="845aa-147">Märkige maksega tasutud arved.</span><span class="sxs-lookup"><span data-stu-id="845aa-147">Mark the invoices paid by the payment.</span></span> 
19. <span data-ttu-id="845aa-148">Sisestage maksesumma, mis arvel tasakaalustatakse.</span><span class="sxs-lookup"><span data-stu-id="845aa-148">Enter the amount of the payment that will be settled to the invoice.</span></span>
20. <span data-ttu-id="845aa-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="845aa-149">Click OK.</span></span>
21. <span data-ttu-id="845aa-150">Sisestage makseviide väljale Makseviide.</span><span class="sxs-lookup"><span data-stu-id="845aa-150">In the Payment reference field, Enter a payment reference.</span></span> <span data-ttu-id="845aa-151">.</span><span class="sxs-lookup"><span data-stu-id="845aa-151">.</span></span>
    * <span data-ttu-id="845aa-152">Makseviide on vajalik vaid juhul, kui märgite makse kaasamise deposiidikviitungile.</span><span class="sxs-lookup"><span data-stu-id="845aa-152">The payment reference is only required if you mark to include the payment on a deposit slip.</span></span>  
22. <span data-ttu-id="845aa-153">Sisestage kliendimaksed.</span><span class="sxs-lookup"><span data-stu-id="845aa-153">Post the customer payments.</span></span> 

