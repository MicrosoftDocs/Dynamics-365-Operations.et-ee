---
title: Müügi komisjonitasude registreerimine
description: See protseduur selgitab müügi komisjonitasude arvutamist ja registreerimist.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4c0e63923d0cb9a4a2c2bed87cfb72edfb0d2741
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833902"
---
# <a name="register-sales-commissions"></a><span data-ttu-id="553ae-103">Müügi komisjonitasude registreerimine</span><span class="sxs-lookup"><span data-stu-id="553ae-103">Register sales commissions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="553ae-104">See protseduur selgitab müügi komisjonitasude arvutamist ja registreerimist.</span><span class="sxs-lookup"><span data-stu-id="553ae-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="553ae-105">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="553ae-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="553ae-106">Enne selle juhendi avamist käivitage juhend „Müügi komisjonitasu reeglite seadistamine” veendumaks, et teil on kõik vajalikud komisjonitasu arvutused seadistatud.</span><span class="sxs-lookup"><span data-stu-id="553ae-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="553ae-107">Märkige üles komisjonitasu töötlemiseks valitud kliendi ja kauba koodid ning kasutage neid, kui teil palutakse selles juhendis luua müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="553ae-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="553ae-108">Müügiisikule komisjonitasu kvalifitseeriva müügitellimuse arveldamine</span><span class="sxs-lookup"><span data-stu-id="553ae-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="553ae-109">Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="553ae-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="553ae-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="553ae-110">Click New.</span></span>
3. <span data-ttu-id="553ae-111">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="553ae-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="553ae-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="553ae-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="553ae-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="553ae-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="553ae-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="553ae-114">Click OK.</span></span>
7. <span data-ttu-id="553ae-115">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="553ae-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="553ae-116">Klõpsake suvandit Muuda vaadet.</span><span class="sxs-lookup"><span data-stu-id="553ae-116">Click Change view.</span></span>
9. <span data-ttu-id="553ae-117">Klõpsake suvandit Päisevaade.</span><span class="sxs-lookup"><span data-stu-id="553ae-117">Click Header view.</span></span>
10. <span data-ttu-id="553ae-118">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="553ae-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="553ae-119">Väljal Müügigrupp olev väärtus tähistab gruppi koos ühe või mitme sellele määratud müügiesindajaga.</span><span class="sxs-lookup"><span data-stu-id="553ae-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="553ae-120">Grupis olevad inimesed on need, kes saavad tellimuse arveldamisel komisjonitasu eelmääratletud määrade ja jaotuse järgi.</span><span class="sxs-lookup"><span data-stu-id="553ae-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="553ae-121">Väärtus kopeeritakse kliendikaardilt, kuid seda saab soovi korral muuta.</span><span class="sxs-lookup"><span data-stu-id="553ae-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="553ae-122">Müügigrupp kopeeritakse ka müügitellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="553ae-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="553ae-123">Saate seda muuta, nii et see võib päise ja/või ridade vahel erineda.</span><span class="sxs-lookup"><span data-stu-id="553ae-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="553ae-124">Välja Komisjonitasu grupp väärtus tähistab gruppi, mille olete loonud ühe või mitme kliendi jaoks komisjonitasude jälgimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="553ae-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="553ae-125">Väärtus kopeeritakse kliendikaardilt, kuid seda saab soovi korral muuta.</span><span class="sxs-lookup"><span data-stu-id="553ae-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="553ae-126">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="553ae-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="553ae-127">Klõpsake suvandit Muuda vaadet.</span><span class="sxs-lookup"><span data-stu-id="553ae-127">Click Change view.</span></span>
13. <span data-ttu-id="553ae-128">Klõpsake suvandit Reavaade.</span><span class="sxs-lookup"><span data-stu-id="553ae-128">Click Line view.</span></span>
14. <span data-ttu-id="553ae-129">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="553ae-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="553ae-130">Valige loendist komisjonitasude jaoks seadistatud kaup.</span><span class="sxs-lookup"><span data-stu-id="553ae-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="553ae-131">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="553ae-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="553ae-132">Märkige üles rea netosumma.</span><span class="sxs-lookup"><span data-stu-id="553ae-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="553ae-133">See tähistab müügitulu, mis siintoodud näites on komisjonitasu arvutamise aluseks.</span><span class="sxs-lookup"><span data-stu-id="553ae-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="553ae-134">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="553ae-134">Click Save.</span></span>
18. <span data-ttu-id="553ae-135">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="553ae-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="553ae-136">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="553ae-136">Click Invoice.</span></span>
20. <span data-ttu-id="553ae-137">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="553ae-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="553ae-138">Valige väljal Kogus väärtus Kõik.</span><span class="sxs-lookup"><span data-stu-id="553ae-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="553ae-139">Valige väljal Sisestamine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="553ae-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="553ae-140">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="553ae-140">Click OK.</span></span>
24. <span data-ttu-id="553ae-141">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="553ae-141">Click OK.</span></span>
    * <span data-ttu-id="553ae-142">Kande sisestamiseks võib kuluda ligikaudu minut.</span><span class="sxs-lookup"><span data-stu-id="553ae-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="553ae-143">Oodake, kuni töötlemine on lõpule jõudnud, ja ärge lehte sulgege.</span><span class="sxs-lookup"><span data-stu-id="553ae-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="553ae-144">Registreeritud müügi komisjonitasude ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="553ae-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="553ae-145">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="553ae-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="553ae-146">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="553ae-146">Click Invoice.</span></span>
3. <span data-ttu-id="553ae-147">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="553ae-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="553ae-148">Klõpsake suvandit Komisjonitasu kanded.</span><span class="sxs-lookup"><span data-stu-id="553ae-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="553ae-149">Vahekaardil Ülevaade kuvatakse read, mis tähistavad arveldatud müügitellimusega seostatud müügiesindajatele makstavaid komisjonitasu summasid.</span><span class="sxs-lookup"><span data-stu-id="553ae-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="553ae-150">Vaadakem üksikasjad üle.</span><span class="sxs-lookup"><span data-stu-id="553ae-150">Let's review the details.</span></span>     
    * <span data-ttu-id="553ae-151">Kui kasutasite komisjonitasu müügigrupi seadistamiseks juhendit „Müügi komisjonitasu reeglite seadistamine”, saab müügi komisjonitasu kaks müügiisikut ja komisjonitasu jaotatakse nende vahel võrdselt.</span><span class="sxs-lookup"><span data-stu-id="553ae-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="553ae-152">Selle näite puhul arvutatakse komisjonitasu kogusumma protsendina müügitulust (tellimuserea netosummast).</span><span class="sxs-lookup"><span data-stu-id="553ae-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="553ae-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="553ae-153">Close the page.</span></span>
6. <span data-ttu-id="553ae-154">Klõpsake suvandit Kanne.</span><span class="sxs-lookup"><span data-stu-id="553ae-154">Click Voucher.</span></span>
    * <span data-ttu-id="553ae-155">Saate üle vaadata komisjonitasu summade kandeid, mis on sisestatud eelmääratletud komisjonitasu kulukontodele ja komisjonitasu ostureskontrotele.</span><span class="sxs-lookup"><span data-stu-id="553ae-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  

