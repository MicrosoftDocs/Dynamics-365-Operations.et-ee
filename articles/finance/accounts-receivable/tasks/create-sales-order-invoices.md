---
title: Müügitellimuse arvete loomine
description: Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 984bb482f357e35dcfa4c08597a6be9e39817b98
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837101"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="53d7a-103">Müügitellimuse arvete loomine</span><span class="sxs-lookup"><span data-stu-id="53d7a-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53d7a-104">Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="53d7a-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="53d7a-105">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="53d7a-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="53d7a-106">Müügitellimusest arve loomine</span><span class="sxs-lookup"><span data-stu-id="53d7a-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="53d7a-107">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Ilma arvet väljastamata lähetatud müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="53d7a-108">Valige loendist müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="53d7a-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="53d7a-109">Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="53d7a-110">Pange tähele, et selle müügitellimusega on seostatud mitu saatelehte.</span><span class="sxs-lookup"><span data-stu-id="53d7a-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="53d7a-111">Saatelehe numbri asemel kuvatakse ainult sõna <multiple> (mitu).</span><span class="sxs-lookup"><span data-stu-id="53d7a-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="53d7a-112">Laiendage jaotist **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="53d7a-113">Arve sisestamiseks peab sisestamise väärtuseks olema määratud Jah.</span><span class="sxs-lookup"><span data-stu-id="53d7a-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="53d7a-114">Võite ka sisestamise välja lülitada ja arve ainult printida.</span><span class="sxs-lookup"><span data-stu-id="53d7a-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="53d7a-115">Sama tulemuse saate ka siis, kui loote arve asemel esialgse arve.</span><span class="sxs-lookup"><span data-stu-id="53d7a-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="53d7a-116">Seda suvandit kasutatakse pakett-tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="53d7a-116">This option is used for batch jobs.</span></span> <span data-ttu-id="53d7a-117">Päring käivitatakse pakett-töö käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="53d7a-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="53d7a-118">Väljal **Printimine** valige „Pärast”.</span><span class="sxs-lookup"><span data-stu-id="53d7a-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="53d7a-119">Väljal **Prindi arve** valige suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="53d7a-120">Prindihaldus võimaldab mitme arve koopiat printida, samuti PDF‑vormingus arvet meiliga saata.</span><span class="sxs-lookup"><span data-stu-id="53d7a-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="53d7a-121">Väljal **Prinditasud** valige „Summeerimine”.</span><span class="sxs-lookup"><span data-stu-id="53d7a-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="53d7a-122">Väljal **Krediidilimiidi kontrollimine** valige „Saldo”.</span><span class="sxs-lookup"><span data-stu-id="53d7a-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="53d7a-123">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="53d7a-124">Tellimuste ühte arvesse ühendamine</span><span class="sxs-lookup"><span data-stu-id="53d7a-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="53d7a-125">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="53d7a-126">Leidke klient, kellel on mitu arvet avatud.</span><span class="sxs-lookup"><span data-stu-id="53d7a-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="53d7a-127">Saate valida mitu avatud müügitellimust kliendi kohta.</span><span class="sxs-lookup"><span data-stu-id="53d7a-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="53d7a-128">Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="53d7a-129">Laiendage jaotist **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="53d7a-130">Väljal **Kogus** valige Kõik.</span><span class="sxs-lookup"><span data-stu-id="53d7a-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="53d7a-131">Pange tähele, et ülevaate jaotises on loetletud kaks arvet.</span><span class="sxs-lookup"><span data-stu-id="53d7a-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="53d7a-132">Ühendame need nüüd ühte arvesse.</span><span class="sxs-lookup"><span data-stu-id="53d7a-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="53d7a-133">Väljal **Koondsisestamine** valige „Arve konto”.</span><span class="sxs-lookup"><span data-stu-id="53d7a-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="53d7a-134">Müügitellimuste ühte arvesse ühendamiseks klõpsake käsku **Korralda**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="53d7a-135">Kaks müügitellimust on nüüd ühte arvesse ühendatud.</span><span class="sxs-lookup"><span data-stu-id="53d7a-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="53d7a-136">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="53d7a-137">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="53d7a-138">Partii jaoks arvete sisestamine</span><span class="sxs-lookup"><span data-stu-id="53d7a-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="53d7a-139">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Arved > Partii arveldamine > Arve**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="53d7a-140">Klõpsake **Vali**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-140">Click **Select**.</span></span>
3. <span data-ttu-id="53d7a-141">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-141">Click **OK**.</span></span>
4. <span data-ttu-id="53d7a-142">Klõpsake valikut **Partii**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-142">Click **Batch**.</span></span>
5. <span data-ttu-id="53d7a-143">Valige suvandi **Pakktöötlus** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="53d7a-144">Klõpsake valikul **Korduvus**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="53d7a-145">Valige **Päevad**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-145">Select **Days**.</span></span>
8. <span data-ttu-id="53d7a-146">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-146">Click **OK**.</span></span>
9. <span data-ttu-id="53d7a-147">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-147">Click **OK**.</span></span>
10. <span data-ttu-id="53d7a-148">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="53d7a-149">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="53d7a-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]