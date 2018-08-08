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
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 7b5c7419e1f8a775ce4b5b9ba46f582c9be23ad0
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="47801-103">Müügitellimuse arvete loomine</span><span class="sxs-lookup"><span data-stu-id="47801-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47801-104">Selles tegevuse juhises kirjeldatakse müügitellimuse arveldust, sh arvete ühendamine ja pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="47801-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="47801-105">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="47801-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="47801-106">Müügitellimusest arve loomine</span><span class="sxs-lookup"><span data-stu-id="47801-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="47801-107">Avage Müügireskontro > Tellimused > Ilma arvet väljastamata lähetatud müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="47801-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="47801-108">Valige loendist müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="47801-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="47801-109">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="47801-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="47801-110">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="47801-110">Click Invoice.</span></span>
    * <span data-ttu-id="47801-111">Pange tähele, et selle müügitellimusega on seostatud mitu saatelehte.</span><span class="sxs-lookup"><span data-stu-id="47801-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="47801-112">Saatelehe numbri asemel kuvatakse ainult sõna <multiple> (mitu).</span><span class="sxs-lookup"><span data-stu-id="47801-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="47801-113">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="47801-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="47801-114">Arve sisestamiseks peab sisestamise väärtuseks olema määratud Jah.</span><span class="sxs-lookup"><span data-stu-id="47801-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="47801-115">Võite ka sisestamise välja lülitada ja arve ainult printida.</span><span class="sxs-lookup"><span data-stu-id="47801-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="47801-116">Sama tulemuse saate ka siis, kui loote arve asemel esialgse arve.</span><span class="sxs-lookup"><span data-stu-id="47801-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="47801-117">Seda suvandit kasutatakse pakett-tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="47801-117">This option is used for batch jobs.</span></span> <span data-ttu-id="47801-118">Päring käivitatakse pakett-töö käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="47801-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="47801-119">Väljal Printimine valige Pärast.</span><span class="sxs-lookup"><span data-stu-id="47801-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="47801-120">Väljal Prindi arve valige suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="47801-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="47801-121">Prindihaldus võimaldab mitme arve koopiat printida, samuti PDF‑vormingus arvet meiliga saata.</span><span class="sxs-lookup"><span data-stu-id="47801-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="47801-122">Väljal Prinditasud valige Summeerimine.</span><span class="sxs-lookup"><span data-stu-id="47801-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="47801-123">Väljal Krediidilimiidi kontrollimine valige Saldo.</span><span class="sxs-lookup"><span data-stu-id="47801-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="47801-124">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="47801-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="47801-125">Tellimuste ühte arvesse ühendamine</span><span class="sxs-lookup"><span data-stu-id="47801-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="47801-126">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="47801-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="47801-127">Leidke klient, kellel on mitu arvet avatud.</span><span class="sxs-lookup"><span data-stu-id="47801-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="47801-128">Valige avatud müügitellimus</span><span class="sxs-lookup"><span data-stu-id="47801-128">Select an open sales order.</span></span>
4. <span data-ttu-id="47801-129">Valige mõni teine sama kliendi avatud müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="47801-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="47801-130">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="47801-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="47801-131">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="47801-131">Click Invoice.</span></span>
7. <span data-ttu-id="47801-132">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="47801-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="47801-133">Valige väljal Kogus väärtus Kõik.</span><span class="sxs-lookup"><span data-stu-id="47801-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="47801-134">Pange tähele, et ülevaate jaotises on loetletud kaks arvet.</span><span class="sxs-lookup"><span data-stu-id="47801-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="47801-135">Ühendame need nüüd ühte arvesse.</span><span class="sxs-lookup"><span data-stu-id="47801-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="47801-136">Väljal Koondsisestamine valige Arve konto.</span><span class="sxs-lookup"><span data-stu-id="47801-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="47801-137">Müügitellimuste ühte arvesse ühendamiseks klõpsake käsku Korralda.</span><span class="sxs-lookup"><span data-stu-id="47801-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="47801-138">Kaks müügitellimust on nüüd ühte arvesse ühendatud.</span><span class="sxs-lookup"><span data-stu-id="47801-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="47801-139">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="47801-139">Click Cancel.</span></span>
12. <span data-ttu-id="47801-140">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="47801-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="47801-141">Partii jaoks arvete sisestamine</span><span class="sxs-lookup"><span data-stu-id="47801-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="47801-142">Avage Müügireskonto > Arved > Partii arveldamine > Arve.</span><span class="sxs-lookup"><span data-stu-id="47801-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="47801-143">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="47801-143">Click Select.</span></span>
3. <span data-ttu-id="47801-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="47801-144">Click OK.</span></span>
4. <span data-ttu-id="47801-145">Klõpsake valikut Partii.</span><span class="sxs-lookup"><span data-stu-id="47801-145">Click Batch.</span></span>
5. <span data-ttu-id="47801-146">Pakktöötluse sisse lülitamiseks klõpsake suvandit Jah.</span><span class="sxs-lookup"><span data-stu-id="47801-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="47801-147">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="47801-147">Click Recurrence.</span></span>
7. <span data-ttu-id="47801-148">Valige Päevad</span><span class="sxs-lookup"><span data-stu-id="47801-148">Select Days</span></span>
8. <span data-ttu-id="47801-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="47801-149">Click OK.</span></span>
9. <span data-ttu-id="47801-150">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="47801-150">Click OK.</span></span>
10. <span data-ttu-id="47801-151">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="47801-151">Click Cancel.</span></span>
11. <span data-ttu-id="47801-152">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="47801-152">Click Yes.</span></span>


