---
title: Kliendi jaoks otsekorralduse loa loomine
description: See ülesande juhend näitab, kuidas luua otsekorralduse luba ja seda arvel kasutada.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: 86d29782f616219b5d84e3567910cb28c60b65ae
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140302"
---
# <a name="create-a-direct-debit-mandate-for-a-customer"></a><span data-ttu-id="8b3af-103">Kliendi jaoks otsekorralduse loa loomine</span><span class="sxs-lookup"><span data-stu-id="8b3af-103">Create a direct debit mandate for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8b3af-104">See ülesande juhend näitab, kuidas luua otsekorralduse luba ja seda arvel kasutada.</span><span class="sxs-lookup"><span data-stu-id="8b3af-104">This task guide demonstrates how to create a direct debit mandate and use it on an invoice.</span></span>


## <a name="create-a-bank-account"></a><span data-ttu-id="8b3af-105">Pangakonto loomine</span><span class="sxs-lookup"><span data-stu-id="8b3af-105">Create a bank account</span></span>
1. <span data-ttu-id="8b3af-106">**Navigeerimispaan**il avage **Moodulid > Müügireskontro > Kliendid > Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="8b3af-107">Valige loendis kirje.</span><span class="sxs-lookup"><span data-stu-id="8b3af-107">In the list, select a record.</span></span> <span data-ttu-id="8b3af-108">Näiteks valige US-001</span><span class="sxs-lookup"><span data-stu-id="8b3af-108">For example, select US-001</span></span>
3. <span data-ttu-id="8b3af-109">Toimingupaanil klõpsake **Klient**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-109">On the Action Pane, click **Customer**.</span></span>
4. <span data-ttu-id="8b3af-110">Klõpsake **Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-110">Click **Bank accounts**.</span></span>
5. <span data-ttu-id="8b3af-111">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-111">Click **New**.</span></span>
6. <span data-ttu-id="8b3af-112">Sisestage väärtus väljale **Pangakonto**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-112">In the **Bank account** field, type a value.</span></span>
7. <span data-ttu-id="8b3af-113">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-113">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="8b3af-114">Sisestage väärtus väljale **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-114">In the **IBAN** field, type a value.</span></span>
9. <span data-ttu-id="8b3af-115">Sisestage väärtus väljale **Valuuta**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-115">In the **Currency** field, type a value.</span></span>
10. <span data-ttu-id="8b3af-116">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-116">Click **Save**.</span></span>
11. <span data-ttu-id="8b3af-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8b3af-117">Close the page.</span></span>
12. <span data-ttu-id="8b3af-118">Paanil **Navigeerimispaan** avage **Moodulid > Sularaha- ja pangahaldus > Pangakontod > Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-118">In the **Navigation pane**, go to **Modules > Cash and bank management > Bank accounts > Bank accounts**.</span></span>
13. <span data-ttu-id="8b3af-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="8b3af-119">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="8b3af-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8b3af-120">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="8b3af-121">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-121">Click **Edit**.</span></span>
16. <span data-ttu-id="8b3af-122">Laiendage kiirkaart **Täiendav identifitseerimine**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-122">Expand the **Additional identification** fastTab.</span></span>
17. <span data-ttu-id="8b3af-123">Väljale **Otsedeebeti ID** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="8b3af-123">In the **Direct debit ID** field, type a value.</span></span>
18. <span data-ttu-id="8b3af-124">Sisestage väärtus väljale **IBAN**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-124">In the **IBAN** field, type a value.</span></span>
19. <span data-ttu-id="8b3af-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8b3af-125">Close the page.</span></span>
20. <span data-ttu-id="8b3af-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8b3af-126">Close the page.</span></span>

## <a name="define-the-electronic-payment-method"></a><span data-ttu-id="8b3af-127">Elektroonilise makseviisi määratlemine</span><span class="sxs-lookup"><span data-stu-id="8b3af-127">Define the electronic payment method</span></span>
1. <span data-ttu-id="8b3af-128">Paanil **Navigeerimispaan** avage **Moodulid > Müügireskontro > Maksete seadistamine > Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-128">In the **Navigation pane**, go to **Modules > Accounts receivable > Payments setup > Methods of payment**.</span></span>
2. <span data-ttu-id="8b3af-129">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-129">Click **New**.</span></span>
3. <span data-ttu-id="8b3af-130">Väljale **Makseviis** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="8b3af-130">In the **Method of payment** field, type a value.</span></span>
4. <span data-ttu-id="8b3af-131">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-131">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="8b3af-132">Väljale **Maksetüüp** sisestage "Elektrooniline makse".</span><span class="sxs-lookup"><span data-stu-id="8b3af-132">In the **Payment type** field, enter 'Electronic payment'.</span></span> <span data-ttu-id="8b3af-133">Makse tüübiks peab otsekorralduse loa makseviisi puhul olema elektrooniline makse.</span><span class="sxs-lookup"><span data-stu-id="8b3af-133">The payment type for a direct debit mandate method of payment must be Electronic payment.</span></span>
6. <span data-ttu-id="8b3af-134">Valige väärtus "Jah" väljal **Nõua luba**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-134">Select Yes in the **Require mandate** field.</span></span>
7. <span data-ttu-id="8b3af-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8b3af-135">Close the page.</span></span>

## <a name="add-a-direct-debit-mandate-to-a-customer"></a><span data-ttu-id="8b3af-136">Kliendile otsekorralduse loa lisamine.</span><span class="sxs-lookup"><span data-stu-id="8b3af-136">Add a direct debit mandate to a customer.</span></span>
1. <span data-ttu-id="8b3af-137">**Navigeerimispaan**il avage **Moodulid > Müügireskontro > Kliendid > Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-137">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="8b3af-138">Valige loendis kirje.</span><span class="sxs-lookup"><span data-stu-id="8b3af-138">In the list, select a record.</span></span> <span data-ttu-id="8b3af-139">Näiteks valige US-001</span><span class="sxs-lookup"><span data-stu-id="8b3af-139">For example, select US-001</span></span>
3. <span data-ttu-id="8b3af-140">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-140">Click **Edit**.</span></span>
4. <span data-ttu-id="8b3af-141">Laiendage kiirkaart **Makse vaikeandmed**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-141">Expand the **Payment defaults** fastTab.</span></span>
5. <span data-ttu-id="8b3af-142">Valige või sisestage väärtus väljal **Makseviis**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-142">In the **Method of payment** field, enter or select a value.</span></span>
6. <span data-ttu-id="8b3af-143">Laiendage kiirkaart **Makse vaikeandmed**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-143">Expand the **Payment defaults** fastTab.</span></span>
7. <span data-ttu-id="8b3af-144">Laiendage kiirkaart **Otsedeebeti load**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-144">Expand the **Direct debit mandates** fastTab.</span></span>
8. <span data-ttu-id="8b3af-145">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-145">Click **Add**.</span></span>
9. <span data-ttu-id="8b3af-146">Sisestage või valige väärtus väljal **Pangakonto**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-146">In the **Bank account** field, enter or select a value.</span></span>
10. <span data-ttu-id="8b3af-147">Väljale **Kreeditori pangakonto** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="8b3af-147">In the **Creditor bank account** field, enter or select a value.</span></span>
11. <span data-ttu-id="8b3af-148">Väljale **Makse sagedus** sisestage maksete arv, mida selle loa täitmiseks eeldate.</span><span class="sxs-lookup"><span data-stu-id="8b3af-148">In the **Payment frequency** field, enter the number of payments that you expect to process for this mandate.</span></span>
12. <span data-ttu-id="8b3af-149">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-149">Click **OK**.</span></span>
13. <span data-ttu-id="8b3af-150">Klõpsake **Prindi**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-150">Click **Print**.</span></span>
14. <span data-ttu-id="8b3af-151">Klõpsake **Loa aruanne**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-151">Click **Mandate report**.</span></span>
15. <span data-ttu-id="8b3af-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8b3af-152">Close the page.</span></span>
16. <span data-ttu-id="8b3af-153">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-153">Click **Edit**.</span></span>
17. <span data-ttu-id="8b3af-154">Väljale **Allkirjastamise kuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="8b3af-154">In the **Signature date** field, enter a date.</span></span>
18. <span data-ttu-id="8b3af-155">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-155">Click **Yes**.</span></span>
19. <span data-ttu-id="8b3af-156">Sisestage asukoht, kus luba allkirjastati.</span><span class="sxs-lookup"><span data-stu-id="8b3af-156">Enter the location where the mandate was signed.</span></span>
20. <span data-ttu-id="8b3af-157">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-157">Click **OK**.</span></span>
21. <span data-ttu-id="8b3af-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8b3af-158">Close the page.</span></span>

## <a name="create-a-free-text-invoice-with-mandate"></a><span data-ttu-id="8b3af-159">Vabas vormis arve loomine loaga</span><span class="sxs-lookup"><span data-stu-id="8b3af-159">Create a free text invoice with mandate</span></span>
1. <span data-ttu-id="8b3af-160">Paanil **Navigeerimispaan** avage **Moodulid > Müügireskontro > Arved > Kõik vaba tekstiga arved**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-160">In the **Navigation pane**, go to **Modules > Accounts receivable > Invoices > All free text invoices**.</span></span>
2. <span data-ttu-id="8b3af-161">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8b3af-161">Click **New**.</span></span>
3. <span data-ttu-id="8b3af-162">Valige klient, kellele loa lisasite.</span><span class="sxs-lookup"><span data-stu-id="8b3af-162">Select the customer that you added the mandate to.</span></span>
4. <span data-ttu-id="8b3af-163">Väljale **Otsedeebeti loa ID** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="8b3af-163">In the **Direct debit mandate ID** field, enter or select a value.</span></span>

