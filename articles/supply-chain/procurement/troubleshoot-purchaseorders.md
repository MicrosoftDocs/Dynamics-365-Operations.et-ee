---
title: Ostutellimuste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada ostutellimustega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 964f31c21faae6a947174f637624aca917881297
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841451"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="2ee1e-103">Ostutellimuste tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="2ee1e-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="2ee1e-104">Selles teemas kirjeldatakse, kuidas lahendada ostutellimustega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="2ee1e-105">Tegevuse saab lõpule viia alles pärast reanumbri täielikku ärajagamist.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="2ee1e-106">See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="2ee1e-107">Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="2ee1e-108">Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="2ee1e-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="2ee1e-109">Kui ostutellimused imporditakse andmehalduse kaudu, ei järgita ostutellimuse reanumbrite puhul süsteemiparameetrites määratletud sammu.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2ee1e-110">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2ee1e-110">Issue description</span></span>

<span data-ttu-id="2ee1e-111">Vaikimisi ei kasutata andmeüksuse *Ostutellimuse read V2* kaudu imporditud ostutellimuse ridade jaoks automaatselt loodud reanumbrite puhul süsteemiparameetrites määratud süsteemi reanumbri sammu.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="2ee1e-112">Kui loote ostutellimuse käsitsi ja lisate ridu kasutajaliidese kaudu (UI), siis on reanumbrite samm õige.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="2ee1e-113">Kuid kui kasutate andmehaldusraamistikku (DMF), ei ole nende samm õige.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="2ee1e-114">See probleem ilmneb seetõttu, et kui impordite ridu DMF-i kaudu ja reanumbrid ei ole imporditud üksuses juba määratud, kasutab süsteem nende määramiseks DMF-i meetodit.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="2ee1e-115">See meetod suurendab reanumbreid alati ühe võrra.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="2ee1e-116">Probleemi lahendus</span><span class="sxs-lookup"><span data-stu-id="2ee1e-116">Issue workaround</span></span>

<span data-ttu-id="2ee1e-117">Veenduge, et soovitud reanumbrid oleksid ostutellimuse ridade importimisel andmeüksuse reanumbrite väljades juba olemas.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="2ee1e-118">Sel juhul ei kirjuta DMF reanumbreid üle.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="2ee1e-119">Vaikemaksugruppi ja vaikeskontot ei täideta arve konto põhjal.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="2ee1e-120">Kui kasutate arve kontot, mis erineb kliendi kontost, siis ei täideta ostutellimuse loomisel arvekonto põhjal vaikemaksugruppi ja -skontot.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="2ee1e-121">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-121">This behavior is by design.</span></span> <span data-ttu-id="2ee1e-122">Maksugrupi ja skontode vaikeväärtused ning muu hinnateave põhineb kliendi kontol, mitte arve kontol.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="2ee1e-123">Ostutellimuse kinnitamise ajal kuvatakse tõrge „Objekti viide ei ole seatud” või hankija arve sisestamisel ilmneb erand „Kutsumise sihtmärgi puhul ilmnes erand”.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="2ee1e-124">See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="2ee1e-125">Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="2ee1e-126">Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="2ee1e-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="2ee1e-127">Üks või mitu arvestuse jaotust on kas üle- või alajaotatud.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2ee1e-128">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2ee1e-128">Issue description</span></span>

<span data-ttu-id="2ee1e-129">Kuvatakse järgmine tõrge: „Üks või mitu arvestuse jaotust on kas üle- või alajaotatud”.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2ee1e-130">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="2ee1e-130">Issue resolution</span></span>

<span data-ttu-id="2ee1e-131">See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="2ee1e-132">Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="2ee1e-133">Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="2ee1e-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="2ee1e-134">Kas saan kuvada ainult minu loodud ostutellimusi?</span><span class="sxs-lookup"><span data-stu-id="2ee1e-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="2ee1e-135">See funktsioon pole praegu saadaval.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="2ee1e-136">Kas ma saan reserveerida varusid ja luua kandeid ostutellimusel registreeritud varude põhjal?</span><span class="sxs-lookup"><span data-stu-id="2ee1e-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="2ee1e-137">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2ee1e-137">Issue description</span></span>

<span data-ttu-id="2ee1e-138">Isegi kui kaupade olek on ostutellimusel *Registreeritud*, saate varusid siiski reserveerida.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="2ee1e-139">Teisisõnu saate luua kandeid registreeritud varude põhjal.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="2ee1e-140">Probleemi taastekitamine</span><span class="sxs-lookup"><span data-stu-id="2ee1e-140">Reproduce the issue</span></span>

<span data-ttu-id="2ee1e-141">Järgmine protsess näitab üht viisi probleemi taastekitamiseks.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="2ee1e-142">Looge ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-142">Create a purchase order.</span></span>
2. <span data-ttu-id="2ee1e-143">Registreerige ostutellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="2ee1e-144">Pange tähele, et saate luua reserveeringuid või kandeid registreeritud varude põhjal.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2ee1e-145">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="2ee1e-145">Issue resolution</span></span>

<span data-ttu-id="2ee1e-146">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-146">This behavior is by design.</span></span> <span data-ttu-id="2ee1e-147">Eeldatakse, et registreeritud kaubad on füüsiliselt lattu või varudesse saabunud ja seetõttu on need reserveerimiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="2ee1e-148">Ostutellimustel ei kajastate juriidilise isiku keelesätteid.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2ee1e-149">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2ee1e-149">Issue description</span></span>

<span data-ttu-id="2ee1e-150">Ostutellimusel kuvatakse toote nimi süsteemikeeles, mitte keeles, mis on määratud juriidilise isiku jaoks, kus ostutellimus loodi.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="2ee1e-151">Probleemi taastekitamine</span><span class="sxs-lookup"><span data-stu-id="2ee1e-151">Reproduce the issue</span></span>

<span data-ttu-id="2ee1e-152">Järgmine protsess näitab üht viisi probleemi taastekitamiseks.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="2ee1e-153">Seadke süsteemikeeleks *EN-US* (USA inglise keel).</span><span class="sxs-lookup"><span data-stu-id="2ee1e-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="2ee1e-154">Veenduge, et olemas oleks toode, mille nimi on tõlgitud keeltesse *EN-US* ja *DE* (saksa).</span><span class="sxs-lookup"><span data-stu-id="2ee1e-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="2ee1e-155">Muutke juriidilise isiku keeleks *DE*.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="2ee1e-156">Looge toodet sisaldav ostutellimus juriidilises isikus, mille keeleks on määratud *DE*.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="2ee1e-157">Pange tähele, et toote nimi kuvatakse ikka USA inglise keeles (süsteemikeeles).</span><span class="sxs-lookup"><span data-stu-id="2ee1e-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2ee1e-158">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="2ee1e-158">Issue resolution</span></span>

<span data-ttu-id="2ee1e-159">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-159">This behavior is by design.</span></span> <span data-ttu-id="2ee1e-160">Ostutellimuste puhul kuvatakse toode alati süsteemikeeles.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="2ee1e-161">Ostutellimuse keelt kasutatakse kinnitustöölehe loomisel.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="2ee1e-162">Üksus „Kinnitatud hankijate loend toote põhjal” ei lase muuta jõustumiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2ee1e-163">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2ee1e-163">Issue description</span></span>

<span data-ttu-id="2ee1e-164">Tootel on kinnitatud hankija, mille jõustumiskuupäev on näiteks 11. jaanuar 2018 (*01/11/2018*) ja aegumiskuupäev *Mitte kunagi*.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="2ee1e-165">Kui proovite muuta jõustumiskuupäevaks 10. jaanuari 2018 (*01/10/2018*) või 12. jaanuari 2018 (*01/12/2018*), kuvatakse järgmine tõrge.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="2ee1e-166">Kinnitatud tarnijate loendis (PdsApproveVendorList) ei saa kirjet luua.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="2ee1e-167">Väärtus „Aegumine” peab olema suurem kui väärtus „Jõustumine” või sellega võrdne.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2ee1e-168">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="2ee1e-168">Issue resolution</span></span>

<span data-ttu-id="2ee1e-169">Saate pikendada ainult perioodi, mille jooksul on hankija kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="2ee1e-170">Kehtivad järgnevad reeglid.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-170">The following rules apply:</span></span>

- <span data-ttu-id="2ee1e-171">Jõustumiskuupäeva muutmiseks nii, et see oleks varem kui ükskõik milline kauba hankija olemasolev kirje (periood), peab uue perioodi aegumiskuupäev olema enne kõiki olemasolevate kirjete aegumiskuupäevi.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="2ee1e-172">Aegumiskuupäeva muutmiseks nii, et see oleks hiljem kui mõni olemasolev periood, peab jõustumiskuupäev olema pärast mis tahes olemasoleva kirje hilisemat aegumiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="2ee1e-173">Et vähendada tervet perioodi, mille jooksul on hankija kinnitatud, peate olemasolevad kirjed kustutama või neid muutma.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="2ee1e-174">Teise võimalusena saate kasutada importimise ajal **kärpimise** lülitit.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="2ee1e-175">See lüliti kustutab kõik tabelis „Kinnitatud hankijad kauba põhjal” olevad kirjed.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="2ee1e-176">Probleemi kirjelduses kirjeldatud näidisstsenaariumi puhul, kus kirje jõustumiskuupäev on *01/11/2018* ja aegumiskuupäev *Mitte kunagi*, saate importida uue kirje, mille jõustumiskuupäev on *01/10/2018* ja aegumiskuupäev *Mitte kunagi*.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="2ee1e-177">Kuid te ei saa perioodi vähendada nii, et jõustumiskuupäev muudetaks andmehalduse kaudu kuupäevaks *01/12/2018*.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="2ee1e-178">Selle muudatuse peate tegema kasutajaliidese kaudu.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-name-isnt-synced"></a><span data-ttu-id="2ee1e-179">Pärast tarneaadressi muutmist ostutellimuse päisel ei sünkroonita tarne nime.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="2ee1e-180">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2ee1e-180">Issue description</span></span>

<span data-ttu-id="2ee1e-181">Ostutellimuse päises olev aadress muudetakse aadressiks, mis pole tarneaadress.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="2ee1e-182">Kuigi aadressi värskendatakse ostutellimusel, ei värskendata tarne nime värskendatud aadressi alusel.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="2ee1e-183">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="2ee1e-183">Issue resolution</span></span>

<span data-ttu-id="2ee1e-184">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-184">This behavior is by design.</span></span> <span data-ttu-id="2ee1e-185">Valitud aadress tuleb märkida tarneaadressina.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="2ee1e-186">Muidu ei värskendata tarne nime valitud aadressi alusel.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="2ee1e-187">Kas ma saan otsida üles ostutellimuse tühistanud kasutaja?</span><span class="sxs-lookup"><span data-stu-id="2ee1e-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="2ee1e-188">Seda teavet jälgitakse ainult siis, kui ostutellimuse puhul kasutatakse muudatuste haldust.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="2ee1e-189">Kui kasutate muudatuste haldust, saate vaadata, kes esitas muudatuse (tühistamise) ja kes selle kinnitas.</span><span class="sxs-lookup"><span data-stu-id="2ee1e-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]