--- 
title: "Müügitellimuse arvete loomine"
description: "Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4b72d5b283f9401d358ee68f4650c486ebb2fd7d
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="10a77-103">Müügitellimuse arvete loomine</span><span class="sxs-lookup"><span data-stu-id="10a77-103">Create sales order invoices</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10a77-104">Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="10a77-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="10a77-105">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="10a77-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="10a77-106">Müügitellimusest arve loomine</span><span class="sxs-lookup"><span data-stu-id="10a77-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="10a77-107">Avage Müügireskontro > Tellimused > Ilma arvet väljastamata lähetatud müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="10a77-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="10a77-108">Valige loendist müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="10a77-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="10a77-109">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="10a77-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="10a77-110">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="10a77-110">Click Invoice.</span></span>
    * <span data-ttu-id="10a77-111">Pange tähele, et selle müügitellimusega on seostatud mitu saatelehte.</span><span class="sxs-lookup"><span data-stu-id="10a77-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="10a77-112">Saatelehe numbri asemel kuvatakse ainult sõna <multiple> (mitu).</span><span class="sxs-lookup"><span data-stu-id="10a77-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="10a77-113">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="10a77-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="10a77-114">Arve sisestamiseks peab sisestamise väärtuseks olema määratud Jah.</span><span class="sxs-lookup"><span data-stu-id="10a77-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="10a77-115">Võite ka sisestamise välja lülitada ja arve ainult printida.</span><span class="sxs-lookup"><span data-stu-id="10a77-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="10a77-116">Sama tulemuse saate ka siis, kui loote arve asemel esialgse arve.</span><span class="sxs-lookup"><span data-stu-id="10a77-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="10a77-117">Seda suvandit kasutatakse pakett-tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="10a77-117">This option is used for batch jobs.</span></span> <span data-ttu-id="10a77-118">Päring käivitatakse pakett-töö käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="10a77-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="10a77-119">Väljal Printimine valige Pärast.</span><span class="sxs-lookup"><span data-stu-id="10a77-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="10a77-120">Väljal Prindi arve valige suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="10a77-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="10a77-121">Prindihaldus võimaldab mitme arve koopiat printida, samuti PDF‑vormingus arvet meiliga saata.</span><span class="sxs-lookup"><span data-stu-id="10a77-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="10a77-122">Väljal Prinditasud valige Summeerimine.</span><span class="sxs-lookup"><span data-stu-id="10a77-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="10a77-123">Väljal Krediidilimiidi kontrollimine valige Saldo.</span><span class="sxs-lookup"><span data-stu-id="10a77-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="10a77-124">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="10a77-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="10a77-125">Tellimuste ühte arvesse ühendamine</span><span class="sxs-lookup"><span data-stu-id="10a77-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="10a77-126">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="10a77-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="10a77-127">Leidke klient, kellel on mitu arvet avatud.</span><span class="sxs-lookup"><span data-stu-id="10a77-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="10a77-128">Valige avatud müügitellimus</span><span class="sxs-lookup"><span data-stu-id="10a77-128">Select an open sales order.</span></span>
4. <span data-ttu-id="10a77-129">Valige mõni teine sama kliendi avatud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="10a77-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="10a77-130">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="10a77-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="10a77-131">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="10a77-131">Click Invoice.</span></span>
7. <span data-ttu-id="10a77-132">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="10a77-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="10a77-133">Valige väljal Kogus väärtus Kõik.</span><span class="sxs-lookup"><span data-stu-id="10a77-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="10a77-134">Pange tähele, et ülevaate jaotises on loetletud kaks arvet.</span><span class="sxs-lookup"><span data-stu-id="10a77-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="10a77-135">Ühendame need nüüd ühte arvesse.</span><span class="sxs-lookup"><span data-stu-id="10a77-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="10a77-136">Väljal Koondsisestamine valige Arve konto.</span><span class="sxs-lookup"><span data-stu-id="10a77-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="10a77-137">Müügitellimuste ühte arvesse ühendamiseks klõpsake käsku Korralda.</span><span class="sxs-lookup"><span data-stu-id="10a77-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="10a77-138">Kaks müügitellimust on nüüd ühte arvesse ühendatud.</span><span class="sxs-lookup"><span data-stu-id="10a77-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="10a77-139">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="10a77-139">Click Cancel.</span></span>
12. <span data-ttu-id="10a77-140">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="10a77-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="10a77-141">Partii jaoks arvete sisestamine</span><span class="sxs-lookup"><span data-stu-id="10a77-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="10a77-142">Avage Müügireskonto > Arved > Partii arveldamine > Arve.</span><span class="sxs-lookup"><span data-stu-id="10a77-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="10a77-143">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="10a77-143">Click Select.</span></span>
3. <span data-ttu-id="10a77-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10a77-144">Click OK.</span></span>
4. <span data-ttu-id="10a77-145">Klõpsake valikut Partii.</span><span class="sxs-lookup"><span data-stu-id="10a77-145">Click Batch.</span></span>
5. <span data-ttu-id="10a77-146">Pakktöötluse sisse lülitamiseks klõpsake suvandit Jah.</span><span class="sxs-lookup"><span data-stu-id="10a77-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="10a77-147">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="10a77-147">Click Recurrence.</span></span>
7. <span data-ttu-id="10a77-148">Valige Päevad</span><span class="sxs-lookup"><span data-stu-id="10a77-148">Select Days</span></span>
8. <span data-ttu-id="10a77-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10a77-149">Click OK.</span></span>
9. <span data-ttu-id="10a77-150">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10a77-150">Click OK.</span></span>
10. <span data-ttu-id="10a77-151">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="10a77-151">Click Cancel.</span></span>
11. <span data-ttu-id="10a77-152">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="10a77-152">Click Yes.</span></span>


