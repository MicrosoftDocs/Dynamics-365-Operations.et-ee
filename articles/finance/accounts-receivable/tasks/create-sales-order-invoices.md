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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c504ef36f61613c7aa7db5a1e5ddba6e69cd7285
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140259"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="77f0c-103">Müügitellimuse arvete loomine</span><span class="sxs-lookup"><span data-stu-id="77f0c-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="77f0c-104">Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="77f0c-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="77f0c-105">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="77f0c-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="77f0c-106">Müügitellimusest arve loomine</span><span class="sxs-lookup"><span data-stu-id="77f0c-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="77f0c-107">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Ilma arvet väljastamata lähetatud müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="77f0c-108">Valige loendist müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="77f0c-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="77f0c-109">Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="77f0c-110">Pange tähele, et selle müügitellimusega on seostatud mitu saatelehte.</span><span class="sxs-lookup"><span data-stu-id="77f0c-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="77f0c-111">Saatelehe numbri asemel kuvatakse ainult sõna <multiple> (mitu).</span><span class="sxs-lookup"><span data-stu-id="77f0c-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="77f0c-112">Laiendage jaotist **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="77f0c-113">Arve sisestamiseks peab sisestamise väärtuseks olema määratud Jah.</span><span class="sxs-lookup"><span data-stu-id="77f0c-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="77f0c-114">Võite ka sisestamise välja lülitada ja arve ainult printida.</span><span class="sxs-lookup"><span data-stu-id="77f0c-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="77f0c-115">Sama tulemuse saate ka siis, kui loote arve asemel esialgse arve.</span><span class="sxs-lookup"><span data-stu-id="77f0c-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="77f0c-116">Seda suvandit kasutatakse pakett-tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="77f0c-116">This option is used for batch jobs.</span></span> <span data-ttu-id="77f0c-117">Päring käivitatakse pakett-töö käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="77f0c-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="77f0c-118">Väljal **Printimine** valige „Pärast”.</span><span class="sxs-lookup"><span data-stu-id="77f0c-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="77f0c-119">Väljal **Prindi arve** valige suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="77f0c-120">Prindihaldus võimaldab mitme arve koopiat printida, samuti PDF‑vormingus arvet meiliga saata.</span><span class="sxs-lookup"><span data-stu-id="77f0c-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="77f0c-121">Väljal **Prinditasud** valige „Summeerimine”.</span><span class="sxs-lookup"><span data-stu-id="77f0c-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="77f0c-122">Väljal **Krediidilimiidi kontrollimine** valige „Saldo”.</span><span class="sxs-lookup"><span data-stu-id="77f0c-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="77f0c-123">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="77f0c-124">Tellimuste ühte arvesse ühendamine</span><span class="sxs-lookup"><span data-stu-id="77f0c-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="77f0c-125">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="77f0c-126">Leidke klient, kellel on mitu arvet avatud.</span><span class="sxs-lookup"><span data-stu-id="77f0c-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="77f0c-127">Saate valida mitu avatud müügitellimust kliendi kohta.</span><span class="sxs-lookup"><span data-stu-id="77f0c-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="77f0c-128">Klõpsake **Toimingupaanil** valikut **Arve > Loo > Arve**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="77f0c-129">Laiendage jaotist **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="77f0c-130">Väljal **Kogus** valige Kõik.</span><span class="sxs-lookup"><span data-stu-id="77f0c-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="77f0c-131">Pange tähele, et ülevaate jaotises on loetletud kaks arvet.</span><span class="sxs-lookup"><span data-stu-id="77f0c-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="77f0c-132">Ühendame need nüüd ühte arvesse.</span><span class="sxs-lookup"><span data-stu-id="77f0c-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="77f0c-133">Väljal **Koondsisestamine** valige „Arve konto”.</span><span class="sxs-lookup"><span data-stu-id="77f0c-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="77f0c-134">Müügitellimuste ühte arvesse ühendamiseks klõpsake käsku **Korralda**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="77f0c-135">Kaks müügitellimust on nüüd ühte arvesse ühendatud.</span><span class="sxs-lookup"><span data-stu-id="77f0c-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="77f0c-136">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="77f0c-137">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="77f0c-138">Partii jaoks arvete sisestamine</span><span class="sxs-lookup"><span data-stu-id="77f0c-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="77f0c-139">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Arved > Partii arveldamine > Arve**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="77f0c-140">Klõpsake **Vali**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-140">Click **Select**.</span></span>
3. <span data-ttu-id="77f0c-141">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-141">Click **OK**.</span></span>
4. <span data-ttu-id="77f0c-142">Klõpsake valikut **Partii**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-142">Click **Batch**.</span></span>
5. <span data-ttu-id="77f0c-143">Valige suvandi **Pakktöötlus** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="77f0c-144">Klõpsake valikul **Korduvus**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="77f0c-145">Valige **Päevad**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-145">Select **Days**.</span></span>
8. <span data-ttu-id="77f0c-146">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-146">Click **OK**.</span></span>
9. <span data-ttu-id="77f0c-147">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-147">Click **OK**.</span></span>
10. <span data-ttu-id="77f0c-148">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="77f0c-149">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="77f0c-149">Click **Yes**.</span></span>

