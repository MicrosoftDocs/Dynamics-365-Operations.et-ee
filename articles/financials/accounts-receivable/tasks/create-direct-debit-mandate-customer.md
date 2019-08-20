---
title: Kliendi jaoks otsekorralduse loa loomine
description: See ülesande juhend näitab, kuidas luua otsekorralduse luba ja seda arvel kasutada.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, BankAccountTable, CustPaymMode, CustDirectDebitMandate, BankAccountTableLookUp, SrsReportViewerForm,  LogisticsAddressCityLookup, CustFreeInvoice, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c93a1aba6ca32e783a6ed6f005c72aab3e06978
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842997"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="d0b85-103">Kliendi jaoks otsekorralduse loa loomine</span><span class="sxs-lookup"><span data-stu-id="d0b85-103">Create a direct debit mandate for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0b85-104">See ülesande juhend näitab, kuidas luua otsekorralduse luba ja seda arvel kasutada.</span><span class="sxs-lookup"><span data-stu-id="d0b85-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="d0b85-105">Pangakonto loomine</span><span class="sxs-lookup"><span data-stu-id="d0b85-105">Create a bank account</span></span>
1. <span data-ttu-id="d0b85-106">Avage Müügireskontro > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="d0b85-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="d0b85-107">Näiteks valige US-001</span><span class="sxs-lookup"><span data-stu-id="d0b85-107">For example, select US-001</span></span>
3. <span data-ttu-id="d0b85-108">Klõpsake toimingupaanil suvandit Klient.</span><span class="sxs-lookup"><span data-stu-id="d0b85-108">On the Action Pane, click Customer.</span></span>
4. <span data-ttu-id="d0b85-109">Klõpsake valikut Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="d0b85-109">Click Bank accounts.</span></span>
5. <span data-ttu-id="d0b85-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d0b85-110">Click New.</span></span>
6. <span data-ttu-id="d0b85-111">Sisestage väärtus väljale Pangakonto.</span><span class="sxs-lookup"><span data-stu-id="d0b85-111">In the Bank account field, type a value.</span></span>
7. <span data-ttu-id="d0b85-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d0b85-112">In the Name field, type a value.</span></span>
8. <span data-ttu-id="d0b85-113">Sisestage väärtus väljale IBAN.</span><span class="sxs-lookup"><span data-stu-id="d0b85-113">In the IBAN field, type a value.</span></span>
9. <span data-ttu-id="d0b85-114">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="d0b85-114">In the Currency field, type a value.</span></span>
10. <span data-ttu-id="d0b85-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d0b85-115">Click Save.</span></span>
11. <span data-ttu-id="d0b85-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d0b85-116">Close the page.</span></span>
12. <span data-ttu-id="d0b85-117">Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="d0b85-117">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
13. <span data-ttu-id="d0b85-118">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d0b85-118">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="d0b85-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d0b85-119">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="d0b85-120">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="d0b85-120">Click Edit.</span></span>
16. <span data-ttu-id="d0b85-121">Laiendage jaotist Täiendav identifitseerimine.</span><span class="sxs-lookup"><span data-stu-id="d0b85-121">Expand the Additional identification section.</span></span>
17. <span data-ttu-id="d0b85-122">Tippige väärtus väljale Otsekorralduse ID.</span><span class="sxs-lookup"><span data-stu-id="d0b85-122">In the Direct debit ID field, type a value.</span></span>
18. <span data-ttu-id="d0b85-123">Sisestage väärtus väljale IBAN.</span><span class="sxs-lookup"><span data-stu-id="d0b85-123">In the IBAN field, type a value.</span></span>
19. <span data-ttu-id="d0b85-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d0b85-124">Close the page.</span></span>
20. <span data-ttu-id="d0b85-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d0b85-125">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="d0b85-126">Elektroonilise makseviisi määratlemine</span><span class="sxs-lookup"><span data-stu-id="d0b85-126">Define the electronic payment method</span></span>
1. <span data-ttu-id="d0b85-127">Avage Müügireskontro > Maksete seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="d0b85-127">Go to Accounts receivable > Payments setup > Methods of payment.</span></span>
2. <span data-ttu-id="d0b85-128">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d0b85-128">Click New.</span></span>
3. <span data-ttu-id="d0b85-129">Sisestage väärtus väljale Makseviis.</span><span class="sxs-lookup"><span data-stu-id="d0b85-129">In the Method of payment field, type a value.</span></span>
4. <span data-ttu-id="d0b85-130">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d0b85-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d0b85-131">Makse tüübiks peab otsekorralduse loa makseviisi puhul olema elektrooniline makse.</span><span class="sxs-lookup"><span data-stu-id="d0b85-131">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="d0b85-132">Valige väljal Nõua luba suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="d0b85-132">Select Yes in the Require mandate field.</span></span>
7. <span data-ttu-id="d0b85-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d0b85-133">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="d0b85-134">Kliendile otsekorralduse loa lisamine.</span><span class="sxs-lookup"><span data-stu-id="d0b85-134">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="d0b85-135">Avage Müügireskontro > Kliendid > Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="d0b85-135">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="d0b85-136">Näiteks valige US-001</span><span class="sxs-lookup"><span data-stu-id="d0b85-136">For example, select US-001</span></span>
3. <span data-ttu-id="d0b85-137">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="d0b85-137">Click Edit.</span></span>
4. <span data-ttu-id="d0b85-138">Laiendage jaotist Makse vaikeandmed.</span><span class="sxs-lookup"><span data-stu-id="d0b85-138">Expand the Payment defaults section.</span></span>
5. <span data-ttu-id="d0b85-139">Valige või sisestage väärtus väljal Makseviis.</span><span class="sxs-lookup"><span data-stu-id="d0b85-139">In the Method of payment field, enter or select a value.</span></span>
6. <span data-ttu-id="d0b85-140">Laiendage jaotist Makse vaikeandmed.</span><span class="sxs-lookup"><span data-stu-id="d0b85-140">Expand the Payment defaults section.</span></span>
7. <span data-ttu-id="d0b85-141">Laiendage jaotist Otsekorralduse load.</span><span class="sxs-lookup"><span data-stu-id="d0b85-141">Expand the Direct debit mandates section.</span></span>
8. <span data-ttu-id="d0b85-142">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d0b85-142">Click Add.</span></span>
9. <span data-ttu-id="d0b85-143">Sisestage väärtus väljale Pangakonto või valige see.</span><span class="sxs-lookup"><span data-stu-id="d0b85-143">In the Bank account field, enter or select a value.</span></span>
10. <span data-ttu-id="d0b85-144">Sisestage väärtus väljale Kreeditori pangakonto või valige see.</span><span class="sxs-lookup"><span data-stu-id="d0b85-144">In the Creditor bank account field, enter or select a value.</span></span>
11. <span data-ttu-id="d0b85-145">Sisestage maksete arv, mille loodate selle loa puhul töödelda.</span><span class="sxs-lookup"><span data-stu-id="d0b85-145">Enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="d0b85-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0b85-146">Click OK.</span></span>
13. <span data-ttu-id="d0b85-147">Klõpsake Prindi.</span><span class="sxs-lookup"><span data-stu-id="d0b85-147">Click Print.</span></span>
14. <span data-ttu-id="d0b85-148">Klõpsake suvandit Loa aruanne.</span><span class="sxs-lookup"><span data-stu-id="d0b85-148">Click Mandate report.</span></span>
15. <span data-ttu-id="d0b85-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d0b85-149">Close the page.</span></span>
16. <span data-ttu-id="d0b85-150">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="d0b85-150">Click Edit.</span></span>
17. <span data-ttu-id="d0b85-151">Sisestage kuupäev väljale Allkirjastamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="d0b85-151">In the Signature date field, enter a date.</span></span>
18. <span data-ttu-id="d0b85-152">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="d0b85-152">Click Yes.</span></span>
19. <span data-ttu-id="d0b85-153">Sisestage asukoht, kus luba allkirjastati.</span><span class="sxs-lookup"><span data-stu-id="d0b85-153">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="d0b85-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0b85-154">Click OK.</span></span>
21. <span data-ttu-id="d0b85-155">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d0b85-155">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="d0b85-156">Vabas vormis arve loomine loaga</span><span class="sxs-lookup"><span data-stu-id="d0b85-156">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="d0b85-157">Avage Müügireskontro > Arved > Kõik vabas vormis arved.</span><span class="sxs-lookup"><span data-stu-id="d0b85-157">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="d0b85-158">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d0b85-158">Click New.</span></span>
3. <span data-ttu-id="d0b85-159">Valige klient, kellele loa lisasite.</span><span class="sxs-lookup"><span data-stu-id="d0b85-159">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="d0b85-160">Sisestage või valige väärtus väljal Otsekorralduse luba.</span><span class="sxs-lookup"><span data-stu-id="d0b85-160">In the Direct debit mandate ID field, enter or select a value.</span></span>

