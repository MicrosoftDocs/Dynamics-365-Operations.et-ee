---
title: Maksete loomine kliendile, kellel on otsekorralduse load
description: See protseduur näitab, kuidas luua ISO20022 otsekorralduse maksefaili kliendile, kellel on konfigureeritud otsekorraldus ja tasumisele kuuluv arve.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice, CustTableLookup, CustPostInvoiceJob, LedgerJournalTable, LedgerJournalTransCustPaym, SysQueryForm, CustPaymProposalEdit, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a4714f1f1b24554684219fc1d766b4b87cff7bb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141599"
---
# <a name="create-payments-for-a-customer-who-have-direct-debit-mandates"></a><span data-ttu-id="6c438-103">Maksete loomine kliendile, kellel on otsekorralduse load</span><span class="sxs-lookup"><span data-stu-id="6c438-103">Create payments for a customer who have direct debit mandates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c438-104">See protseduur näitab, kuidas luua ISO20022 otsekorralduse maksefaili kliendile, kellel on konfigureeritud otsekorraldus ja tasumisele kuuluv arve.</span><span class="sxs-lookup"><span data-stu-id="6c438-104">This procedure shows how to generate an ISO20022 direct debit payment file for a customer who has direct debit configured and an invoice to be paid.</span></span> <span data-ttu-id="6c438-105">Arve loomine ja sisestamine on valikuline.</span><span class="sxs-lookup"><span data-stu-id="6c438-105">Creating and posting an invoice is optional.</span></span> <span data-ttu-id="6c438-106">Tasumisele kuuluva arve asemel võite valida töölehel loa enne maksefaili loomist, toetades kliendi ettemakse stsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="6c438-106">Instead of having an invoice to be paid you can select a mandate in a journal prior to generating a payment file, to support a customer prepayment scenario.</span></span>



<span data-ttu-id="6c438-107">Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.</span><span class="sxs-lookup"><span data-stu-id="6c438-107">The demo data company used to create this procedure is DEMF.</span></span>



<span data-ttu-id="6c438-108">See on viies viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="6c438-108">This is the fifth of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span> <span data-ttu-id="6c438-109">Enne selle toimingu lõpetamist tuleb lõpetada varasemad toimingud.</span><span class="sxs-lookup"><span data-stu-id="6c438-109">Before you can complete this task, you must complete the earlier tasks.</span></span> <span data-ttu-id="6c438-110">Kõigepealt tuleb importida kliendimakse elektroonilise aruandluse konfiguratsioonid, konfigureerida makseviisid ning seadistada teie ettevõtte ja kliendi andmed.</span><span class="sxs-lookup"><span data-stu-id="6c438-110">You must first import customer payment electronic reporting configurations, configure method of payments, and set up your company and customer information.</span></span> 


## <a name="post-a-free-text-invoice-with-direct-debit-information"></a><span data-ttu-id="6c438-111">Otsekorralduse andmetega vabas vormis arve sisestamine</span><span class="sxs-lookup"><span data-stu-id="6c438-111">Post a free text invoice with direct debit information</span></span>
1. <span data-ttu-id="6c438-112">Avage Müügireskontro > Arved > Kõik vabas vormis arved.</span><span class="sxs-lookup"><span data-stu-id="6c438-112">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="6c438-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c438-113">Click New.</span></span>
3. <span data-ttu-id="6c438-114">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="6c438-114">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="6c438-115">Valige näiteks DE-010.</span><span class="sxs-lookup"><span data-stu-id="6c438-115">For example, select DE-010.</span></span>  
4. <span data-ttu-id="6c438-116">Valige või sisestage väärtus väljal Makseviis.</span><span class="sxs-lookup"><span data-stu-id="6c438-116">In the Method of payment field, enter or select a value.</span></span>
    * <span data-ttu-id="6c438-117">Näide.</span><span class="sxs-lookup"><span data-stu-id="6c438-117">For example.</span></span> <span data-ttu-id="6c438-118">valige Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="6c438-118">select Electronic.</span></span>  
5. <span data-ttu-id="6c438-119">Sisestage või valige väärtus väljal Otsekorralduse luba.</span><span class="sxs-lookup"><span data-stu-id="6c438-119">In the Direct debit mandate ID field, enter or select a value.</span></span>
6. <span data-ttu-id="6c438-120">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="6c438-120">Click Add line.</span></span>
7. <span data-ttu-id="6c438-121">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="6c438-121">In the Description field, type a value.</span></span>
8. <span data-ttu-id="6c438-122">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="6c438-122">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="6c438-123">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="6c438-123">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="6c438-124">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="6c438-124">Click Post.</span></span>
11. <span data-ttu-id="6c438-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c438-125">Click OK.</span></span>

## <a name="create-a-payment"></a><span data-ttu-id="6c438-126">Makse loomine</span><span class="sxs-lookup"><span data-stu-id="6c438-126">Create a payment</span></span>
1. <span data-ttu-id="6c438-127">Avage Müügireskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="6c438-127">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="6c438-128">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c438-128">Click New.</span></span>
3. <span data-ttu-id="6c438-129">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="6c438-129">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="6c438-130">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="6c438-130">Click Lines.</span></span>
5. <span data-ttu-id="6c438-131">Klõpsake suvandit Maksesoovitus.</span><span class="sxs-lookup"><span data-stu-id="6c438-131">Click Payment proposal.</span></span>
6. <span data-ttu-id="6c438-132">Klõpsake suvandit Loo maksesoovitus.</span><span class="sxs-lookup"><span data-stu-id="6c438-132">Click Create payment proposal.</span></span>
7. <span data-ttu-id="6c438-133">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="6c438-133">Expand the Records to include section.</span></span>
8. <span data-ttu-id="6c438-134">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="6c438-134">Click Filter.</span></span>
9. <span data-ttu-id="6c438-135">Valige loendist tabeli Kliendi kanded rida ja väli Makseviis.</span><span class="sxs-lookup"><span data-stu-id="6c438-135">In the list, select the row for the Customer transactions table and the Method of payment field.</span></span>
    * <span data-ttu-id="6c438-136">Maksmiseks kliendi kannete valimisel võite rakendada mis tahes kriteeriumi.</span><span class="sxs-lookup"><span data-stu-id="6c438-136">You can apply any criteria for selecting customer transactions to pay.</span></span> <span data-ttu-id="6c438-137">Selle näite puhul kasutage kannete filtreerimiseks makseviisi Elektrooniline.</span><span class="sxs-lookup"><span data-stu-id="6c438-137">For this example, use Electronic as a method of payment to filter transactions.</span></span>  
10. <span data-ttu-id="6c438-138">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="6c438-138">In the Criteria field, enter or select a value.</span></span>
11. <span data-ttu-id="6c438-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c438-139">Click OK.</span></span>
12. <span data-ttu-id="6c438-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c438-140">Click OK.</span></span>
13. <span data-ttu-id="6c438-141">Klõpsake suvandit Maksete loomine.</span><span class="sxs-lookup"><span data-stu-id="6c438-141">Click Create payments.</span></span>
