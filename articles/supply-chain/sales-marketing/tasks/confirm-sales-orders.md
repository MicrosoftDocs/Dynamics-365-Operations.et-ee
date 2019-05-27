---
title: Müügitellimuste kinnitamine
description: See protseduur näitab, kuidas kinnitada müügitellimusi.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db475cf967bebec2d442aaa864800d920cf0ab81
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563990"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="ebc12-103">Müügitellimuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="ebc12-103">Confirm sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ebc12-104">See protseduur näitab, kuidas kinnitada müügitellimusi.</span><span class="sxs-lookup"><span data-stu-id="ebc12-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="ebc12-105">Teile selgitatakse üksiku tellimuse kinnitamist ja mitme tellimuse korraga kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="ebc12-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="ebc12-106">Neid ülesandeid täidab üldjuhul müügitellimuse töötleja.</span><span class="sxs-lookup"><span data-stu-id="ebc12-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="ebc12-107">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="ebc12-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="ebc12-108">Enne alustamist veenduge, et sama kliendi jaoks oleks mitu avatud müügitellimust.</span><span class="sxs-lookup"><span data-stu-id="ebc12-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="ebc12-109">Kui kasutate USMF-i, saate kasutada klienti US-027.</span><span class="sxs-lookup"><span data-stu-id="ebc12-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="ebc12-110">Üksiku müügitellimuse kinnitamine</span><span class="sxs-lookup"><span data-stu-id="ebc12-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="ebc12-111">Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="ebc12-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="ebc12-112">Leidke ja valige loendist tellimus, mille soovite kinnitada.</span><span class="sxs-lookup"><span data-stu-id="ebc12-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="ebc12-113">Klõpsake müügitellimuse numbris linki valitud tellimuse avamiseks.</span><span class="sxs-lookup"><span data-stu-id="ebc12-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="ebc12-114">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="ebc12-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="ebc12-115">Klõpsake suvandit Müügitellimuse kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="ebc12-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="ebc12-116">Laiendage või ahendage jaotist Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ebc12-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="ebc12-117">Veenduge, et väli Sisestamine: jah oleks aktiivne.</span><span class="sxs-lookup"><span data-stu-id="ebc12-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="ebc12-118">Määrake suvandi Kinnituse printimine sätteks Jah.</span><span class="sxs-lookup"><span data-stu-id="ebc12-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="ebc12-119">Väli Krediidilimiidi kontrolli määrab kliendi järelejäänud krediidi arvutamise meetodi.</span><span class="sxs-lookup"><span data-stu-id="ebc12-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="ebc12-120">Vaikimisi kopeeritakse see lehelt Müügireskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ebc12-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="ebc12-121">Kui soovite kindla müügitellimuse kinnitamisel krediidilimiidi kontrolli vahele jätta, valige suvandi Kontrolli krediidilimiiti sätteks Puudub.</span><span class="sxs-lookup"><span data-stu-id="ebc12-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="ebc12-122">Siiski tuleb arvestada, et isegi kui selle välja sätteks on valitud Puudub, tehakse krediidilimiidi kontroll ikkagi, kui kliendi põhiandmetes on valitud suvand Kohustuslik krediidilimiit.</span><span class="sxs-lookup"><span data-stu-id="ebc12-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="ebc12-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ebc12-123">Click OK.</span></span>
9. <span data-ttu-id="ebc12-124">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="ebc12-124">Click Yes.</span></span>
10. <span data-ttu-id="ebc12-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ebc12-125">Close the page.</span></span>
11. <span data-ttu-id="ebc12-126">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="ebc12-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="ebc12-127">Klõpsake suvandit Muuda vaadet.</span><span class="sxs-lookup"><span data-stu-id="ebc12-127">Click Change view.</span></span>
13. <span data-ttu-id="ebc12-128">Klõpsake suvandit Päisevaade.</span><span class="sxs-lookup"><span data-stu-id="ebc12-128">Click Header view.</span></span>
    * <span data-ttu-id="ebc12-129">Kui tellimus on kinnitatud, määratakse suvandi Dokumendi olek sätteks Kinnitus.</span><span class="sxs-lookup"><span data-stu-id="ebc12-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="ebc12-130">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="ebc12-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="ebc12-131">Klõpsake suvandit Müügitellimuse kinnitus.</span><span class="sxs-lookup"><span data-stu-id="ebc12-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="ebc12-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ebc12-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="ebc12-133">Mitme müügitellimuse korraga kinnitamine</span><span class="sxs-lookup"><span data-stu-id="ebc12-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="ebc12-134">Avage Müük ja turundus > Müügitellimused > Tellimuse kinnitus > Müügitellimuse kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="ebc12-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="ebc12-135">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="ebc12-135">Click Select.</span></span>
3. <span data-ttu-id="ebc12-136">Leidke ja valige vahekaardil Vahemik olevast loendist kirje, mis viitab väljale Kliendikonto.</span><span class="sxs-lookup"><span data-stu-id="ebc12-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="ebc12-137">Klõpsake väljal Kriteeriumid otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ebc12-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ebc12-138">Leidke ja valige loendist kliendikonto, millel on mitu tellimust, mida soovite korraga kinnitada.</span><span class="sxs-lookup"><span data-stu-id="ebc12-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="ebc12-139">Kui kasutate USMF-i, saate valida konto US-027.</span><span class="sxs-lookup"><span data-stu-id="ebc12-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="ebc12-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ebc12-140">Click OK.</span></span>
    * <span data-ttu-id="ebc12-141">Vahekaardil Ülevaade kuvatakse loend tellimustest, mis vastavad päringukriteeriumile.</span><span class="sxs-lookup"><span data-stu-id="ebc12-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="ebc12-142">Need kaasatakse kinnitusse.</span><span class="sxs-lookup"><span data-stu-id="ebc12-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="ebc12-143">Väli Koondsisestamine määrab parameetri, mille järgi koondatakse mitu tellimust ühte kinnitusdokumenti.</span><span class="sxs-lookup"><span data-stu-id="ebc12-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="ebc12-144">Vaikimisi kopeeritakse suvand lehel Müügireskontro parameetrid sättest Koondsisestuse vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="ebc12-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="ebc12-145">Valige väljal Koondsisestamine suvand Tellimus.</span><span class="sxs-lookup"><span data-stu-id="ebc12-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="ebc12-146">Koondsisestuste loomiseks nõutavad minimaalsed parameetrid on Arvekonto ja Valuuta.</span><span class="sxs-lookup"><span data-stu-id="ebc12-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="ebc12-147">See tähendab, et erinevate arvekontode ja erinevate valuutadega koondsisestused pole lubatud.</span><span class="sxs-lookup"><span data-stu-id="ebc12-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="ebc12-148">Koondsisestuse parameetrid saab seadistada lehel Koondsisestuste parameetrid, millele pääseb juurde lehelt Müügireskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ebc12-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="ebc12-149">Klõpsake väljal Müügitellimus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ebc12-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ebc12-150">Valige loendist tellimuse number, mis peaks olema koondtellimus.</span><span class="sxs-lookup"><span data-stu-id="ebc12-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="ebc12-151">Klõpsake suvandit Korralda.</span><span class="sxs-lookup"><span data-stu-id="ebc12-151">Click Arrange.</span></span>
11. <span data-ttu-id="ebc12-152">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ebc12-152">Click OK.</span></span>
12. <span data-ttu-id="ebc12-153">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ebc12-153">Click OK.</span></span>

