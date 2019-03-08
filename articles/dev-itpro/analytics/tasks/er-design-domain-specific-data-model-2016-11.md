---
title: Elektroonilise aruandluse domeenispetsiifilise andmemudeli kujundamine
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab andmemudelit elektrooniliste maksedokumentide jaoks.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0debb7276c4f3e41c2e85ce6bc63b8df5bc159f8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "348407"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="0c7ed-103">Elektroonilise aruandluse domeenispetsiifilise andmemudeli kujundamine</span><span class="sxs-lookup"><span data-stu-id="0c7ed-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c7ed-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab andmemudelit elektrooniliste maksedokumentide jaoks.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="0c7ed-105">Seda andmemudelit kasutatakse hiljem maksedokumentide vormingu loomisel andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="0c7ed-106">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtetel ühised.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="0c7ed-107">Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="0c7ed-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="0c7ed-109">Valige konfiguratsiooni pakkuja näidisettevõttele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="0c7ed-110">Kui seda konfiguratsiooni pakkujat ei kuvata, peate esmalt lõpetama etapid protseduuris Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="0c7ed-111">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="0c7ed-112">Loote konfiguratsiooni, mis sisaldab elektroonilise makse dokumentide andmemudelit.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="0c7ed-113">Seda andmemudelit kasutatakse hiljem andmeallikana maksedokumentide vormingu loomisel.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="0c7ed-114">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="0c7ed-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="0c7ed-115">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="0c7ed-116">Sisestage väljale Nimi suvand Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="0c7ed-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="0c7ed-117">Maksed (lihtsustatud mudel)</span><span class="sxs-lookup"><span data-stu-id="0c7ed-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="0c7ed-118">Sisestage väljale Kirjeldus suvand Makse mudeli konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="0c7ed-119">Makse mudeli konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="0c7ed-119">Payment model configuration</span></span>  
    * <span data-ttu-id="0c7ed-120">Aktiivne konfiguratsiooni pakkuja sisestatakse siia automaatselt.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="0c7ed-121">See pakkuja saab seda konfiguratsiooni hallata.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="0c7ed-122">Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="0c7ed-123">Klõpsake konfiguratsiooni loomise ülesande lõpetamiseks nuppu Loo konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="0c7ed-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="0c7ed-124">Andmemudeli loomine</span><span class="sxs-lookup"><span data-stu-id="0c7ed-124">Create a data model</span></span>
    * <span data-ttu-id="0c7ed-125">Loote valitud konfiguratsioonile uut andmemudelit.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="0c7ed-126">Selle konfiguratsiooni versiooni olekuks on Mustand.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="0c7ed-127">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="0c7ed-128">Makseprotsessis osaleva osapoole struktuuri määratlemine</span><span class="sxs-lookup"><span data-stu-id="0c7ed-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="0c7ed-129">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0c7ed-130">Väljale Nimi sisestage Osapool.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="0c7ed-131">Osapool</span><span class="sxs-lookup"><span data-stu-id="0c7ed-131">Party</span></span>  
3. <span data-ttu-id="0c7ed-132">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-132">Click Add.</span></span>
4. <span data-ttu-id="0c7ed-133">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="0c7ed-134">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="0c7ed-135">Nimi</span><span class="sxs-lookup"><span data-stu-id="0c7ed-135">Name</span></span>  
6. <span data-ttu-id="0c7ed-136">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="0c7ed-137">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-137">Click Add.</span></span>
8. <span data-ttu-id="0c7ed-138">Väljale Otsi sisestage Osapool.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="0c7ed-139">Osapool</span><span class="sxs-lookup"><span data-stu-id="0c7ed-139">Party</span></span>  
9. <span data-ttu-id="0c7ed-140">Klõpsake nuppu Leia eelmine.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="0c7ed-141">Selle mudeli pangastruktuuri määratlemine</span><span class="sxs-lookup"><span data-stu-id="0c7ed-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="0c7ed-142">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0c7ed-143">Sisestage väljale Nimi suvand Esindaja.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="0c7ed-144">Esindaja</span><span class="sxs-lookup"><span data-stu-id="0c7ed-144">Agent</span></span>  
3. <span data-ttu-id="0c7ed-145">Valige väljalt Kaubakood suvand Kirje.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="0c7ed-146">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-146">Click Add.</span></span>
5. <span data-ttu-id="0c7ed-147">Sisestage väljale Kirjeldus suvand Osapoole (deebitor/kreeditor) kontot hooldav finantsasutus (nt pank).</span><span class="sxs-lookup"><span data-stu-id="0c7ed-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="0c7ed-148">Osapoole (deebitor/kreeditor) kontot hooldav finantsasutus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="0c7ed-149">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="0c7ed-150">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="0c7ed-151">Nimi</span><span class="sxs-lookup"><span data-stu-id="0c7ed-151">Name</span></span>  
8. <span data-ttu-id="0c7ed-152">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="0c7ed-153">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-153">Click Add.</span></span>
10. <span data-ttu-id="0c7ed-154">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="0c7ed-155">Sisestage väljale Nimi suvand SWIFT.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="0c7ed-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="0c7ed-156">SWIFT</span></span>  
12. <span data-ttu-id="0c7ed-157">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-157">Click Add.</span></span>
13. <span data-ttu-id="0c7ed-158">Väljale Kirjeldus sisestage „Panga ID-kood”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="0c7ed-159">Panga ID-kood</span><span class="sxs-lookup"><span data-stu-id="0c7ed-159">Bank identification code</span></span>  
14. <span data-ttu-id="0c7ed-160">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="0c7ed-161">Sisestage väljale Nimi suvand RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="0c7ed-162">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="0c7ed-162">RoutingNumber</span></span>  
16. <span data-ttu-id="0c7ed-163">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-163">Click Add.</span></span>
17. <span data-ttu-id="0c7ed-164">Väljale Kirjeldus sisestage „Registreerimisnumber”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="0c7ed-165">Registreerimisnumber</span><span class="sxs-lookup"><span data-stu-id="0c7ed-165">Routing number</span></span>  
18. <span data-ttu-id="0c7ed-166">Klõpsake nuppu Leia eelmine.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="0c7ed-167">Selle mudeli konto struktuuri määratlemine</span><span class="sxs-lookup"><span data-stu-id="0c7ed-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="0c7ed-168">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0c7ed-169">Sisestage väljale Nimi suvand Konto.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="0c7ed-170">Konto</span><span class="sxs-lookup"><span data-stu-id="0c7ed-170">Account</span></span>  
3. <span data-ttu-id="0c7ed-171">Valige väljalt Kaubakood suvand Kirje.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="0c7ed-172">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-172">Click Add.</span></span>
5. <span data-ttu-id="0c7ed-173">Väljale Kirjeldus sisestage „Osapoole konto tuvastamine finantsasutuses (näiteks pangas)”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="0c7ed-174">Osapoole konto tuvastamine finantsasutuses (näiteks pangas).</span><span class="sxs-lookup"><span data-stu-id="0c7ed-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="0c7ed-175">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="0c7ed-176">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="0c7ed-177">Valuuta</span><span class="sxs-lookup"><span data-stu-id="0c7ed-177">Currency</span></span>  
8. <span data-ttu-id="0c7ed-178">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="0c7ed-179">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-179">Click Add.</span></span>
10. <span data-ttu-id="0c7ed-180">Väljale Kirjeldus sisestage „Valuutakood”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="0c7ed-181">Valuutakood</span><span class="sxs-lookup"><span data-stu-id="0c7ed-181">Currency code</span></span>  
11. <span data-ttu-id="0c7ed-182">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="0c7ed-183">Sisestage väljale Nimi suvand Number.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="0c7ed-184">Kood</span><span class="sxs-lookup"><span data-stu-id="0c7ed-184">Number</span></span>  
13. <span data-ttu-id="0c7ed-185">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-185">Click Add.</span></span>
14. <span data-ttu-id="0c7ed-186">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="0c7ed-187">Sisestage väljale Nimi suvand IBAN.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="0c7ed-188">IBAN</span><span class="sxs-lookup"><span data-stu-id="0c7ed-188">IBAN</span></span>  
16. <span data-ttu-id="0c7ed-189">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-189">Click Add.</span></span>
17. <span data-ttu-id="0c7ed-190">Väljale Kirjeldus sisestage „Rahvusvaheline pangakonto number”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="0c7ed-191">Rahvusvaheline pangakonto number</span><span class="sxs-lookup"><span data-stu-id="0c7ed-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="0c7ed-192">Kreeditiülekande maksetüübi jaoks makseteate struktuuri määratlemine</span><span class="sxs-lookup"><span data-stu-id="0c7ed-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="0c7ed-193">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="0c7ed-194">Väljale Uus sõlm kui sisestage „Mudeli juur”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="0c7ed-195">Sisestage väljale Nimi suvand CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="0c7ed-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="0c7ed-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="0c7ed-197">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-197">Click Add.</span></span>
5. <span data-ttu-id="0c7ed-198">Väljale Otsi tippige „CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="0c7ed-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="0c7ed-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="0c7ed-200">Klõpsake nuppu Leia eelmine.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-200">Click Find previous.</span></span>
7. <span data-ttu-id="0c7ed-201">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="0c7ed-202">Sisestage väljale Nimi suvand MessageIdentification.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="0c7ed-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="0c7ed-203">MessageIdentification</span></span>  
9. <span data-ttu-id="0c7ed-204">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-204">Click Add.</span></span>
10. <span data-ttu-id="0c7ed-205">Väljale Kirjeldus sisestage „Juhendava osapoole määratud punkt-punktiline viide (mis saadetakse järgmisele osapoolele) teate identifitseerimiseks”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="0c7ed-206">Juhendava osapoole määratud punkt-punktiline viide (mis saadetakse järgmisele osapoolele) teate identifitseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="0c7ed-207">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="0c7ed-208">Sisestage väljale Nimi suvand ProcessingDateTime.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="0c7ed-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="0c7ed-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="0c7ed-210">Valige väljalt Kaubakood suvand DateTime.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="0c7ed-211">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-211">Click Add.</span></span>
15. <span data-ttu-id="0c7ed-212">Väljale Kirjeldus sisestage „Makseteate loomise kuupäev ja kellaaeg”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="0c7ed-213">Makseteate loomise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="0c7ed-214">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="0c7ed-215">Määratlege selle mudeli puhul makse kande struktuur.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="0c7ed-216">Sisestage väljale Nimi suvand Maksed.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="0c7ed-217">Maksed</span><span class="sxs-lookup"><span data-stu-id="0c7ed-217">Payments</span></span>  
18. <span data-ttu-id="0c7ed-218">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="0c7ed-219">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-219">Click Add.</span></span>
20. <span data-ttu-id="0c7ed-220">Sisestage väljale Kirjeldus suvand Praeguse teate makseread.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="0c7ed-221">Praeguse teate makseread</span><span class="sxs-lookup"><span data-stu-id="0c7ed-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="0c7ed-222">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="0c7ed-223">Sisestage väljale Nimi suvand Saaja.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="0c7ed-224">Saaja</span><span class="sxs-lookup"><span data-stu-id="0c7ed-224">Creditor</span></span>  
23. <span data-ttu-id="0c7ed-225">Valige väljalt Kaubakood suvand Kirje.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="0c7ed-226">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-226">Click Add.</span></span>
25. <span data-ttu-id="0c7ed-227">Väljale Kirjeldus sisestage „Osapool, kellele tuleb rahasumma maksta”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="0c7ed-228">Osapool, kellele tuleb rahasumma maksta.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="0c7ed-229">Klõpsake nuppu Vaheta kauba viidet.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="0c7ed-230">Väljale Otsi sisestage Osapool.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="0c7ed-231">Osapool</span><span class="sxs-lookup"><span data-stu-id="0c7ed-231">Party</span></span>  
28. <span data-ttu-id="0c7ed-232">Klõpsake nuppu Otsi järgmine.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-232">Click Find next.</span></span>
29. <span data-ttu-id="0c7ed-233">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-233">Click OK.</span></span>
30. <span data-ttu-id="0c7ed-234">Väljale Otsi sisestage „Maksed”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="0c7ed-235">Maksed</span><span class="sxs-lookup"><span data-stu-id="0c7ed-235">Payments</span></span>  
31. <span data-ttu-id="0c7ed-236">Klõpsake nuppu Otsi järgmine.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-236">Click Find next.</span></span>
32. <span data-ttu-id="0c7ed-237">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="0c7ed-238">Sisestage väljale Nimi suvand Maksja.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="0c7ed-239">Deebitor</span><span class="sxs-lookup"><span data-stu-id="0c7ed-239">Debtor</span></span>  
34. <span data-ttu-id="0c7ed-240">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-240">Click Add.</span></span>
35. <span data-ttu-id="0c7ed-241">Väljale Kirjeldus sisestage „Osapool, kes võlgneb rahasumma (lõplikule) kreeditorile”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="0c7ed-242">Osapool, kes võlgneb rahasumma (lõplikule) kreeditorile.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="0c7ed-243">Klõpsake nuppu Vaheta kauba viidet.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="0c7ed-244">Väljale Otsi sisestage Osapool.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="0c7ed-245">Osapool</span><span class="sxs-lookup"><span data-stu-id="0c7ed-245">Party</span></span>  
38. <span data-ttu-id="0c7ed-246">Klõpsake nuppu Otsi järgmine.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-246">Click Find next.</span></span>
39. <span data-ttu-id="0c7ed-247">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-247">Click OK.</span></span>
40. <span data-ttu-id="0c7ed-248">Klõpsake nuppu Otsi järgmine.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-248">Click Find next.</span></span>
41. <span data-ttu-id="0c7ed-249">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="0c7ed-250">Sisestage väljale Nimi suvand Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="0c7ed-251">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0c7ed-251">Description</span></span>  
43. <span data-ttu-id="0c7ed-252">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="0c7ed-253">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-253">Click Add.</span></span>
45. <span data-ttu-id="0c7ed-254">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="0c7ed-255">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="0c7ed-256">Valuuta</span><span class="sxs-lookup"><span data-stu-id="0c7ed-256">Currency</span></span>  
47. <span data-ttu-id="0c7ed-257">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-257">Click Add.</span></span>
48. <span data-ttu-id="0c7ed-258">Väljale Kirjeldus sisestage „Valuutakood”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="0c7ed-259">Valuutakood</span><span class="sxs-lookup"><span data-stu-id="0c7ed-259">Currency code</span></span>  
49. <span data-ttu-id="0c7ed-260">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="0c7ed-261">Sisestage väljale Nimi suvand TransactionDate.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="0c7ed-262">TransactionDate</span><span class="sxs-lookup"><span data-stu-id="0c7ed-262">TransactionDate</span></span>  
51. <span data-ttu-id="0c7ed-263">Valige väljalt Kaubakood suvand Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="0c7ed-264">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-264">Click Add.</span></span>
53. <span data-ttu-id="0c7ed-265">Väljale Kirjeldus sisestage „Kande kuupäev”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="0c7ed-266">Kande kuupäev</span><span class="sxs-lookup"><span data-stu-id="0c7ed-266">Transaction date</span></span>  
54. <span data-ttu-id="0c7ed-267">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="0c7ed-268">Sisestage väljale Nimi suvand InstructedAmount.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="0c7ed-269">InstructedAmount</span><span class="sxs-lookup"><span data-stu-id="0c7ed-269">InstructedAmount</span></span>  
56. <span data-ttu-id="0c7ed-270">Valige väljalt Kaubakood suvand Tegelik.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="0c7ed-271">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-271">Click Add.</span></span>
58. <span data-ttu-id="0c7ed-272">Väljale Kirjeldus sisestage „Maksja ja saaja vahel enne maksude mahaarvamist liigutatav rahasumma”.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="0c7ed-273">Summa peaks olema väljendatud algatanud osapoole tellitud valuutas.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="0c7ed-274">Maksja ja saaja vahel enne maksude mahaarvamist liigutatav rahasumma.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="0c7ed-275">Summa peaks olema väljendatud algatanud osapoole tellitud valuutas.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="0c7ed-276">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="0c7ed-277">Sisestage väljale Nimi suvand End2EndID.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="0c7ed-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="0c7ed-278">End2EndID</span></span>  
61. <span data-ttu-id="0c7ed-279">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="0c7ed-280">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-280">Click Add.</span></span>
63. <span data-ttu-id="0c7ed-281">Väljale Kirjeldus sisestage „Algatava osapoole määratud kordumatu kood.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="0c7ed-282">Seda ID-d edastatakse muutmata kujul kogu ahela ulatuses.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="0c7ed-283">Algatava osapoole määratud kordumatu kood.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="0c7ed-284">Seda ID-d edastatakse muutmata kujul kogu ahela ulatuses.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="0c7ed-285">Sisestage väljale Nimi suvand PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="0c7ed-286">Suvandi PaymentModel nimi joondatakse maksevormide eelmääratletud liidestega.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="0c7ed-287">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-287">Click Save.</span></span>
66. <span data-ttu-id="0c7ed-288">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c7ed-288">Close the page.</span></span>

