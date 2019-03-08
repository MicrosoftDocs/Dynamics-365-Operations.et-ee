---
title: Müügipakkumiste loomine ja redigeerimine
description: See protseduur näitab, kuidas koostada ja muuta müügipakkumist.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5b5618a815aaff12dd366523920ed275801b3b16
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "343623"
---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="c78c9-103">Müügipakkumiste loomine ja redigeerimine</span><span class="sxs-lookup"><span data-stu-id="c78c9-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c78c9-104">See protseduur näitab, kuidas koostada ja muuta müügipakkumist.</span><span class="sxs-lookup"><span data-stu-id="c78c9-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="c78c9-105">Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="c78c9-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="c78c9-106">Müügipakkumise loomine</span><span class="sxs-lookup"><span data-stu-id="c78c9-106">Create a sales quotation</span></span>
1. <span data-ttu-id="c78c9-107">Avage Müük ja turundus > Müügipakkumised > Kõik hinnapakkumised.</span><span class="sxs-lookup"><span data-stu-id="c78c9-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="c78c9-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c78c9-108">Click New.</span></span>
3. <span data-ttu-id="c78c9-109">Tehke väljal Konto tüüp valik Potentsiaalne klient.</span><span class="sxs-lookup"><span data-stu-id="c78c9-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="c78c9-110">Valige või sisestage väärtus väljal Potentsiaalne klient.</span><span class="sxs-lookup"><span data-stu-id="c78c9-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="c78c9-111">Laiendage jaotis Üldine.</span><span class="sxs-lookup"><span data-stu-id="c78c9-111">Expand the General section.</span></span>
    * <span data-ttu-id="c78c9-112">Kuna otsustasite koostada pakkumise müügi ja turunduse alalt, määratakse tüübiks automaatselt Müügipakkumine.</span><span class="sxs-lookup"><span data-stu-id="c78c9-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="c78c9-113">Projektipakkumise koostamiseks tuleb see avada projektijuhtimise ja raamatupidamise moodulis.</span><span class="sxs-lookup"><span data-stu-id="c78c9-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="c78c9-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c78c9-114">Click OK.</span></span>
    * <span data-ttu-id="c78c9-115">Hinnapakkumise ridade väljad ja tegevused on müügitellimuse ridade omadega väga sarnased.</span><span class="sxs-lookup"><span data-stu-id="c78c9-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="c78c9-116">Sarnaselt müügitellimustele saab hinnapakkumisi koostada konkreetsele kaubale või kui kaubakood pole teada või seda pole hinnapakkumise koostamise ajal olemas, saab hinnapakkumisi koostada müügikategooriale.</span><span class="sxs-lookup"><span data-stu-id="c78c9-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="c78c9-117">Valige või sisestage väärtus väljal Kaup.</span><span class="sxs-lookup"><span data-stu-id="c78c9-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="c78c9-118">Tippige väärtus väljale Kaup.</span><span class="sxs-lookup"><span data-stu-id="c78c9-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="c78c9-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c78c9-119">Close the page.</span></span>
10. <span data-ttu-id="c78c9-120">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="c78c9-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="c78c9-121">Kui real valitud kaubal on kehtivaid kaubandusleppeid, kopeeritakse kehtiv hind ja allahindlused automaatselt pakkumise reale.</span><span class="sxs-lookup"><span data-stu-id="c78c9-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="c78c9-122">Veenduge, et ühiku hinna väljal on väärtus, ja saate soovi korral sisestada ka allahindluse väärtusi.</span><span class="sxs-lookup"><span data-stu-id="c78c9-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="c78c9-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c78c9-123">Click Save.</span></span>
12. <span data-ttu-id="c78c9-124">Klõpsake toimingupaanil valikut Müügipakkumine.</span><span class="sxs-lookup"><span data-stu-id="c78c9-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="c78c9-125">Klõpsake valikut Kogusummad.</span><span class="sxs-lookup"><span data-stu-id="c78c9-125">Click Totals.</span></span>
14. <span data-ttu-id="c78c9-126">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c78c9-126">Click OK.</span></span>
15. <span data-ttu-id="c78c9-127">Klõpsake valikut Müügipakkumise rida.</span><span class="sxs-lookup"><span data-stu-id="c78c9-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="c78c9-128">Klõpsake valikut Hinnad.</span><span class="sxs-lookup"><span data-stu-id="c78c9-128">Click Prices.</span></span>
    * <span data-ttu-id="c78c9-129">Lehel Hinnasimulatsiooni käivitamine saate proovida korrigeerida oma hinnapakkumise eeldatavat tulu või kasumlikkust, tuginedes soovitud ühiku hinnale, allahindluse summale, allahindluse protsendile, kogusummale, marginaalile või kasumiprotsendile.</span><span class="sxs-lookup"><span data-stu-id="c78c9-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="c78c9-130">Kui olete sihtarvudega rahul, rakendage soovitus hinnapakkumise reale ja selle hinnaga seotud välju värskendatakse vastavalt.</span><span class="sxs-lookup"><span data-stu-id="c78c9-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="c78c9-131">Saate luua soovitud arvu hinnasimulatsioone.</span><span class="sxs-lookup"><span data-stu-id="c78c9-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="c78c9-132">Kui klõpsate nuppu Uus, kopeeritakse selle pakkumise rea hinnatingimused lehele.</span><span class="sxs-lookup"><span data-stu-id="c78c9-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="c78c9-133">Seejärel saate muuta hinnaga seotud väljade väärtused sihtväärtusteks.</span><span class="sxs-lookup"><span data-stu-id="c78c9-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="c78c9-134">Ühe välja muutmine käivitab kõigi teiste väljade ümberarvutamise.</span><span class="sxs-lookup"><span data-stu-id="c78c9-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="c78c9-135">Et süsteem saaks arvutada müügimarginaali ja kasumiprotsendi, peab toote ühiku omahind teada olema.</span><span class="sxs-lookup"><span data-stu-id="c78c9-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="c78c9-136">Vaadake vahekaardilt Simuleeritud hinnad algseid hindu, soovitatavaid muudatusi ja nende mõju hinnapakkumise kogusummadele.</span><span class="sxs-lookup"><span data-stu-id="c78c9-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="c78c9-137">Reeglina, kui hinnapakkumise reale rakendatakse simulatsioon, mis määrab uue summa, arvutab süsteem uue väärtuse ja sisestab selle väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="c78c9-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="c78c9-138">Kui simulatsioon põhineb uuel marginaalil või kasumiprotsendil, muudetakse ainult välja Netosumma ja Ühiku hind on tühi.</span><span class="sxs-lookup"><span data-stu-id="c78c9-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="c78c9-139">Mõlemal juhul kustutatakse kõik allahindlused, mis olid enne simulatsiooni pakkumise real.</span><span class="sxs-lookup"><span data-stu-id="c78c9-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="c78c9-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c78c9-140">Close the page.</span></span>
18. <span data-ttu-id="c78c9-141">Klõpsake toimingupaanil valikut Pakkumine.</span><span class="sxs-lookup"><span data-stu-id="c78c9-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="c78c9-142">Klõpsake käsku Saada pakkumine.</span><span class="sxs-lookup"><span data-stu-id="c78c9-142">Click Send quotation.</span></span>
20. <span data-ttu-id="c78c9-143">Tehke väljal Hinnapakkumise printimine valik Jah.</span><span class="sxs-lookup"><span data-stu-id="c78c9-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="c78c9-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c78c9-144">Click OK.</span></span>
    * <span data-ttu-id="c78c9-145">Aruande koostamine võib minuti aega võtta.</span><span class="sxs-lookup"><span data-stu-id="c78c9-145">The report may take a minute to generate.</span></span> <span data-ttu-id="c78c9-146">Ärge sulgege lehte enne, kui see on valmis.</span><span class="sxs-lookup"><span data-stu-id="c78c9-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="c78c9-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c78c9-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="c78c9-148">Müügipakkumise värskendamine</span><span class="sxs-lookup"><span data-stu-id="c78c9-148">Update a sales quotation</span></span>
1. <span data-ttu-id="c78c9-149">Klõpsake tegumiribal valikut Järeltegevus.</span><span class="sxs-lookup"><span data-stu-id="c78c9-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="c78c9-150">Klõpsake valikut Teisenda kliendiks.</span><span class="sxs-lookup"><span data-stu-id="c78c9-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="c78c9-151">Sisestage väärtus väljale Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="c78c9-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="c78c9-152">Klõpsake nuppu Kontrolli.</span><span class="sxs-lookup"><span data-stu-id="c78c9-152">Click Check.</span></span>
    * <span data-ttu-id="c78c9-153">Veenduge, et näete sõnumit, et sisestatud konto number on kasutamiseks vaba.</span><span class="sxs-lookup"><span data-stu-id="c78c9-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="c78c9-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c78c9-154">Click OK.</span></span>
    * <span data-ttu-id="c78c9-155">Süsteem on nüüd loonud hinnapakkumise potentsiaalsele kliendile uue kliendikonto.</span><span class="sxs-lookup"><span data-stu-id="c78c9-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="c78c9-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c78c9-156">Close the page.</span></span>
7. <span data-ttu-id="c78c9-157">Klõpsake tegumiribal valikut Järeltegevus.</span><span class="sxs-lookup"><span data-stu-id="c78c9-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="c78c9-158">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="c78c9-158">Click Confirm.</span></span>
9. <span data-ttu-id="c78c9-159">Valige või sisestage väärtus väljal Põhjus.</span><span class="sxs-lookup"><span data-stu-id="c78c9-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="c78c9-160">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c78c9-160">Click OK.</span></span>
11. <span data-ttu-id="c78c9-161">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="c78c9-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="c78c9-162">Klõpsake valikut Müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="c78c9-162">Click Sales orders.</span></span>
13. <span data-ttu-id="c78c9-163">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c78c9-163">Close the page.</span></span>

