---
title: Müügitellimuse arvete loomine
description: Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d2e1dd552f529d09756c1ddeec39fc54a1f073a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241582"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="b2aba-103">Müügitellimuse arvete loomine</span><span class="sxs-lookup"><span data-stu-id="b2aba-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2aba-104">Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="b2aba-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="b2aba-105">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b2aba-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="b2aba-106">Müügitellimusest arve loomine</span><span class="sxs-lookup"><span data-stu-id="b2aba-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="b2aba-107">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Ilma arvet väljastamata lähetatud müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="b2aba-108">Valige loendist müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="b2aba-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="b2aba-109">Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="b2aba-110">Pange tähele, et selle müügitellimusega on seostatud mitu saatelehte.</span><span class="sxs-lookup"><span data-stu-id="b2aba-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="b2aba-111">Saatelehe numbri asemel kuvatakse ainult sõna <multiple> (mitu).</span><span class="sxs-lookup"><span data-stu-id="b2aba-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="b2aba-112">Laiendage jaotist **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="b2aba-113">Arve sisestamiseks peab sisestamise väärtuseks olema määratud Jah.</span><span class="sxs-lookup"><span data-stu-id="b2aba-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="b2aba-114">Võite ka sisestamise välja lülitada ja arve ainult printida.</span><span class="sxs-lookup"><span data-stu-id="b2aba-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="b2aba-115">Sama tulemuse saate ka siis, kui loote arve asemel esialgse arve.</span><span class="sxs-lookup"><span data-stu-id="b2aba-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="b2aba-116">Seda suvandit kasutatakse pakett-tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="b2aba-116">This option is used for batch jobs.</span></span> <span data-ttu-id="b2aba-117">Päring käivitatakse pakett-töö käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="b2aba-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="b2aba-118">Väljal **Printimine** valige „Pärast”.</span><span class="sxs-lookup"><span data-stu-id="b2aba-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="b2aba-119">Väljal **Prindi arve** valige suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="b2aba-120">Prindihaldus võimaldab mitme arve koopiat printida, samuti PDF‑vormingus arvet meiliga saata.</span><span class="sxs-lookup"><span data-stu-id="b2aba-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="b2aba-121">Väljal **Prinditasud** valige „Summeerimine”.</span><span class="sxs-lookup"><span data-stu-id="b2aba-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="b2aba-122">Väljal **Krediidilimiidi kontrollimine** valige „Saldo”.</span><span class="sxs-lookup"><span data-stu-id="b2aba-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="b2aba-123">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="b2aba-124">Tellimuste ühte arvesse ühendamine</span><span class="sxs-lookup"><span data-stu-id="b2aba-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="b2aba-125">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="b2aba-126">Leidke klient, kellel on mitu arvet avatud.</span><span class="sxs-lookup"><span data-stu-id="b2aba-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="b2aba-127">Saate valida mitu avatud müügitellimust kliendi kohta.</span><span class="sxs-lookup"><span data-stu-id="b2aba-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="b2aba-128">Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="b2aba-129">Laiendage jaotist **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="b2aba-130">Väljal **Kogus** valige Kõik.</span><span class="sxs-lookup"><span data-stu-id="b2aba-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="b2aba-131">Pange tähele, et ülevaate jaotises on loetletud kaks arvet.</span><span class="sxs-lookup"><span data-stu-id="b2aba-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="b2aba-132">Ühendame need nüüd ühte arvesse.</span><span class="sxs-lookup"><span data-stu-id="b2aba-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="b2aba-133">Väljal **Koondsisestamine** valige „Arve konto”.</span><span class="sxs-lookup"><span data-stu-id="b2aba-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="b2aba-134">Müügitellimuste ühte arvesse ühendamiseks klõpsake käsku **Korralda**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="b2aba-135">Kaks müügitellimust on nüüd ühte arvesse ühendatud.</span><span class="sxs-lookup"><span data-stu-id="b2aba-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="b2aba-136">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="b2aba-137">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="b2aba-138">Partii jaoks arvete sisestamine</span><span class="sxs-lookup"><span data-stu-id="b2aba-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="b2aba-139">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Arved > Partii arveldamine > Arve**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="b2aba-140">Klõpsake **Vali**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-140">Click **Select**.</span></span>
3. <span data-ttu-id="b2aba-141">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-141">Click **OK**.</span></span>
4. <span data-ttu-id="b2aba-142">Klõpsake valikut **Partii**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-142">Click **Batch**.</span></span>
5. <span data-ttu-id="b2aba-143">Valige suvandi **Pakktöötlus** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="b2aba-144">Klõpsake valikul **Korduvus**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="b2aba-145">Valige **Päevad**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-145">Select **Days**.</span></span>
8. <span data-ttu-id="b2aba-146">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-146">Click **OK**.</span></span>
9. <span data-ttu-id="b2aba-147">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-147">Click **OK**.</span></span>
10. <span data-ttu-id="b2aba-148">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="b2aba-149">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b2aba-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]