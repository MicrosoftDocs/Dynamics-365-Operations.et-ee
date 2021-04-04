---
title: Elektroonilise aruandluse domeenispetsiifilise andmemudeli kujundamine
description: Selles teemas kirjeldatakse, kuidas luua uut elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab elektrooniliste maksedokumentide andmemudelit.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 284fad8b6646c35217789cc9936cbe9fe75a03d0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567805"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="d5add-103">Elektroonilise aruandluse domeenispetsiifilise andmemudeli kujundamine</span><span class="sxs-lookup"><span data-stu-id="d5add-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5add-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab andmemudelit elektrooniliste maksedokumentide jaoks.</span><span class="sxs-lookup"><span data-stu-id="d5add-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="d5add-105">Seda andmemudelit kasutatakse hiljem maksedokumentide vormingu loomisel andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="d5add-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="d5add-106">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtetel ühised.</span><span class="sxs-lookup"><span data-stu-id="d5add-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="d5add-107">Etappide lõpuleviimiseks, peate esmalt läbima teemas „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” kirjeldatudetapid.</span><span class="sxs-lookup"><span data-stu-id="d5add-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="d5add-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="d5add-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="d5add-109">Valige konfiguratsiooni pakkuja näidisettevõttele „Litware, Inc.”</span><span class="sxs-lookup"><span data-stu-id="d5add-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="d5add-110">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” esitatud juhised.</span><span class="sxs-lookup"><span data-stu-id="d5add-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="d5add-111">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="d5add-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="d5add-112">Loote konfiguratsiooni, mis sisaldab elektroonilise makse dokumentide andmemudelit.</span><span class="sxs-lookup"><span data-stu-id="d5add-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="d5add-113">Seda andmemudelit kasutatakse hiljem andmeallikana maksedokumentide vormingu loomisel.</span><span class="sxs-lookup"><span data-stu-id="d5add-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="d5add-114">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="d5add-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="d5add-115">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="d5add-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="d5add-116">Sisestage väljale Nimi suvand Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="d5add-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="d5add-117">Sisestage väljale Kirjeldus suvand Makse mudeli konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="d5add-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="d5add-118">Aktiivne konfiguratsiooni pakkuja sisestatakse siia automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d5add-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="d5add-119">See pakkuja saab seda konfiguratsiooni hallata.</span><span class="sxs-lookup"><span data-stu-id="d5add-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="d5add-120">Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.</span><span class="sxs-lookup"><span data-stu-id="d5add-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="d5add-121">Klõpsake konfiguratsiooni loomise ülesande lõpetamiseks nuppu „Loo konfiguratsioon”</span><span class="sxs-lookup"><span data-stu-id="d5add-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="d5add-122">Andmemudeli loomine</span><span class="sxs-lookup"><span data-stu-id="d5add-122">Create a data model</span></span>
<span data-ttu-id="d5add-123">Loote valitud konfiguratsioonile uut andmemudelit.</span><span class="sxs-lookup"><span data-stu-id="d5add-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="d5add-124">Selle konfiguratsiooni versiooni olekuks on Mustand.</span><span class="sxs-lookup"><span data-stu-id="d5add-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="d5add-125">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="d5add-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="d5add-126">Makseprotsessis osaleva osapoole struktuuri määratlemine</span><span class="sxs-lookup"><span data-stu-id="d5add-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="d5add-127">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="d5add-128">Väljale Nimi sisestage Osapool.</span><span class="sxs-lookup"><span data-stu-id="d5add-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="d5add-129">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-129">Click Add.</span></span>
4. <span data-ttu-id="d5add-130">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="d5add-131">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5add-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="d5add-132">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="d5add-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="d5add-133">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-133">Click Add.</span></span>
8. <span data-ttu-id="d5add-134">Väljale Otsi sisestage Osapool.</span><span class="sxs-lookup"><span data-stu-id="d5add-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="d5add-135">Klõpsake nuppu Leia eelmine.</span><span class="sxs-lookup"><span data-stu-id="d5add-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="d5add-136">Selle mudeli pangastruktuuri määratlemine</span><span class="sxs-lookup"><span data-stu-id="d5add-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="d5add-137">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="d5add-138">Sisestage väljale Nimi suvand Esindaja.</span><span class="sxs-lookup"><span data-stu-id="d5add-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="d5add-139">Valige väljalt Kaubakood suvand Kirje.</span><span class="sxs-lookup"><span data-stu-id="d5add-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="d5add-140">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-140">Click Add.</span></span>
5. <span data-ttu-id="d5add-141">Sisestage väljale Kirjeldus suvand Osapoole (deebitor/kreeditor) kontot hooldav finantsasutus (nt pank).</span><span class="sxs-lookup"><span data-stu-id="d5add-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="d5add-142">Osapoole (deebitor/kreeditor) kontot hooldav finantsasutus.</span><span class="sxs-lookup"><span data-stu-id="d5add-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="d5add-143">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="d5add-144">Sisestage väljale Nimi suvand Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5add-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="d5add-145">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="d5add-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="d5add-146">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-146">Click Add.</span></span>
10. <span data-ttu-id="d5add-147">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="d5add-148">Sisestage väljale Nimi suvand SWIFT.</span><span class="sxs-lookup"><span data-stu-id="d5add-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="d5add-149">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-149">Click Add.</span></span>
13. <span data-ttu-id="d5add-150">Väljale Kirjeldus sisestage „Panga ID-kood”.</span><span class="sxs-lookup"><span data-stu-id="d5add-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="d5add-151">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="d5add-152">Sisestage väljale Nimi suvand RoutingNumber.</span><span class="sxs-lookup"><span data-stu-id="d5add-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="d5add-153">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-153">Click Add.</span></span>
17. <span data-ttu-id="d5add-154">Väljale Kirjeldus sisestage „Registreerimisnumber”.</span><span class="sxs-lookup"><span data-stu-id="d5add-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="d5add-155">Klõpsake nuppu Leia eelmine.</span><span class="sxs-lookup"><span data-stu-id="d5add-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="d5add-156">Selle mudeli konto struktuuri määratlemine</span><span class="sxs-lookup"><span data-stu-id="d5add-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="d5add-157">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="d5add-158">Sisestage väljale Nimi suvand Konto.</span><span class="sxs-lookup"><span data-stu-id="d5add-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="d5add-159">Valige väljalt Kaubakood suvand Kirje.</span><span class="sxs-lookup"><span data-stu-id="d5add-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="d5add-160">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-160">Click Add.</span></span>
5. <span data-ttu-id="d5add-161">Väljale Kirjeldus sisestage „Osapoole konto tuvastamine finantsasutuses (näiteks pangas)”.</span><span class="sxs-lookup"><span data-stu-id="d5add-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="d5add-162">Osapoole konto tuvastamine finantsasutuses (näiteks pangas).</span><span class="sxs-lookup"><span data-stu-id="d5add-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="d5add-163">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="d5add-164">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="d5add-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="d5add-165">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="d5add-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="d5add-166">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-166">Click Add.</span></span>
10. <span data-ttu-id="d5add-167">Väljale Kirjeldus sisestage „Valuutakood”.</span><span class="sxs-lookup"><span data-stu-id="d5add-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="d5add-168">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="d5add-169">Sisestage väljale Nimi suvand Number.</span><span class="sxs-lookup"><span data-stu-id="d5add-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="d5add-170">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-170">Click Add.</span></span>
14. <span data-ttu-id="d5add-171">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="d5add-172">Sisestage väljale Nimi suvand IBAN.</span><span class="sxs-lookup"><span data-stu-id="d5add-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="d5add-173">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-173">Click Add.</span></span>
17. <span data-ttu-id="d5add-174">Väljale Kirjeldus sisestage „Rahvusvaheline pangakonto number”.</span><span class="sxs-lookup"><span data-stu-id="d5add-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="d5add-175">Kreeditiülekande maksetüübi jaoks makseteate struktuuri määratlemine</span><span class="sxs-lookup"><span data-stu-id="d5add-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="d5add-176">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="d5add-177">Väljale Uus sõlm kui sisestage „Mudeli juur”.</span><span class="sxs-lookup"><span data-stu-id="d5add-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="d5add-178">Sisestage väljale Nimi suvand CustomerCreditTransferInitiation.</span><span class="sxs-lookup"><span data-stu-id="d5add-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="d5add-179">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-179">Click Add.</span></span>
5. <span data-ttu-id="d5add-180">Väljale Otsi tippige „CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="d5add-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="d5add-181">Klõpsake nuppu Leia eelmine.</span><span class="sxs-lookup"><span data-stu-id="d5add-181">Click Find previous.</span></span>
7. <span data-ttu-id="d5add-182">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="d5add-183">Sisestage väljale Nimi suvand MessageIdentification.</span><span class="sxs-lookup"><span data-stu-id="d5add-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="d5add-184">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-184">Click Add.</span></span>
10. <span data-ttu-id="d5add-185">Väljale Kirjeldus sisestage „Juhendava osapoole määratud punkt-punktiline viide (mis saadetakse järgmisele osapoolele) teate identifitseerimiseks”.</span><span class="sxs-lookup"><span data-stu-id="d5add-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="d5add-186">Juhendava osapoole määratud punkt-punktiline viide (mis saadetakse järgmisele osapoolele) teate identifitseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d5add-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="d5add-187">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="d5add-188">Sisestage väljale Nimi suvand ProcessingDateTime.</span><span class="sxs-lookup"><span data-stu-id="d5add-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="d5add-189">Valige väljalt Kaubakood suvand DateTime.</span><span class="sxs-lookup"><span data-stu-id="d5add-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="d5add-190">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-190">Click Add.</span></span>
15. <span data-ttu-id="d5add-191">Väljale Kirjeldus sisestage „Makseteate loomise kuupäev ja kellaaeg”.</span><span class="sxs-lookup"><span data-stu-id="d5add-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="d5add-192">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="d5add-193">Määratlege selle mudeli puhul makse kande struktuur.</span><span class="sxs-lookup"><span data-stu-id="d5add-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="d5add-194">Sisestage väljale Nimi suvand Maksed.</span><span class="sxs-lookup"><span data-stu-id="d5add-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="d5add-195">Valige väljalt Kaubakood suvand Kirjete loend.</span><span class="sxs-lookup"><span data-stu-id="d5add-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="d5add-196">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-196">Click Add.</span></span>
20. <span data-ttu-id="d5add-197">Sisestage väljale Kirjeldus suvand Praeguse teate makseread.</span><span class="sxs-lookup"><span data-stu-id="d5add-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="d5add-198">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="d5add-199">Sisestage väljale Nimi suvand Saaja.</span><span class="sxs-lookup"><span data-stu-id="d5add-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="d5add-200">Valige väljalt Kaubakood suvand Kirje.</span><span class="sxs-lookup"><span data-stu-id="d5add-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="d5add-201">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-201">Click Add.</span></span>
25. <span data-ttu-id="d5add-202">Väljale Kirjeldus sisestage „Osapool, kellele tuleb rahasumma maksta”.</span><span class="sxs-lookup"><span data-stu-id="d5add-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="d5add-203">Klõpsake nuppu Vaheta kauba viidet.</span><span class="sxs-lookup"><span data-stu-id="d5add-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="d5add-204">Väljale Otsi sisestage Osapool.</span><span class="sxs-lookup"><span data-stu-id="d5add-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="d5add-205">Klõpsake nuppu Otsi järgmine.</span><span class="sxs-lookup"><span data-stu-id="d5add-205">Click Find next.</span></span>
29. <span data-ttu-id="d5add-206">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5add-206">Click OK.</span></span>
30. <span data-ttu-id="d5add-207">Väljale Otsi sisestage „Maksed”.</span><span class="sxs-lookup"><span data-stu-id="d5add-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="d5add-208">Klõpsake nuppu Otsi järgmine.</span><span class="sxs-lookup"><span data-stu-id="d5add-208">Click Find next.</span></span>
32. <span data-ttu-id="d5add-209">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="d5add-210">Sisestage väljale Nimi suvand Maksja.</span><span class="sxs-lookup"><span data-stu-id="d5add-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="d5add-211">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-211">Click Add.</span></span>
35. <span data-ttu-id="d5add-212">Väljale Kirjeldus sisestage „Osapool, kes võlgneb rahasumma (lõplikule) kreeditorile”.</span><span class="sxs-lookup"><span data-stu-id="d5add-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="d5add-213">Klõpsake nuppu Vaheta kauba viidet.</span><span class="sxs-lookup"><span data-stu-id="d5add-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="d5add-214">Väljale Otsi sisestage Osapool.</span><span class="sxs-lookup"><span data-stu-id="d5add-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="d5add-215">Klõpsake nuppu Otsi järgmine.</span><span class="sxs-lookup"><span data-stu-id="d5add-215">Click Find next.</span></span>
39. <span data-ttu-id="d5add-216">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5add-216">Click OK.</span></span>
40. <span data-ttu-id="d5add-217">Klõpsake nuppu Otsi järgmine.</span><span class="sxs-lookup"><span data-stu-id="d5add-217">Click Find next.</span></span>
41. <span data-ttu-id="d5add-218">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="d5add-219">Sisestage väljale Nimi suvand Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d5add-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="d5add-220">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="d5add-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="d5add-221">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-221">Click Add.</span></span>
45. <span data-ttu-id="d5add-222">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="d5add-223">Sisestage väljale Nimi suvand Valuuta.</span><span class="sxs-lookup"><span data-stu-id="d5add-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="d5add-224">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-224">Click Add.</span></span>
48. <span data-ttu-id="d5add-225">Väljale Kirjeldus sisestage „Valuutakood”.</span><span class="sxs-lookup"><span data-stu-id="d5add-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="d5add-226">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="d5add-227">Sisestage väljale Nimi suvand TransactionDate.</span><span class="sxs-lookup"><span data-stu-id="d5add-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="d5add-228">Valige väljalt Kaubakood suvand Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="d5add-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="d5add-229">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-229">Click Add.</span></span>
53. <span data-ttu-id="d5add-230">Väljale Kirjeldus sisestage „Kande kuupäev”.</span><span class="sxs-lookup"><span data-stu-id="d5add-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="d5add-231">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="d5add-232">Sisestage väljale Nimi suvand InstructedAmount.</span><span class="sxs-lookup"><span data-stu-id="d5add-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="d5add-233">Valige väljalt Kaubakood suvand Tegelik.</span><span class="sxs-lookup"><span data-stu-id="d5add-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="d5add-234">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-234">Click Add.</span></span>
58. <span data-ttu-id="d5add-235">Väljale Kirjeldus sisestage „Maksja ja saaja vahel enne maksude mahaarvamist liigutatav rahasumma”.</span><span class="sxs-lookup"><span data-stu-id="d5add-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="d5add-236">Summa peaks olema väljendatud algatanud osapoole tellitud valuutas.</span><span class="sxs-lookup"><span data-stu-id="d5add-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="d5add-237">Maksja ja saaja vahel enne maksude mahaarvamist liigutatav rahasumma.</span><span class="sxs-lookup"><span data-stu-id="d5add-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="d5add-238">Summa peaks olema väljendatud algatanud osapoole tellitud valuutas.</span><span class="sxs-lookup"><span data-stu-id="d5add-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="d5add-239">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5add-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="d5add-240">Sisestage väljale Nimi suvand End2EndID.</span><span class="sxs-lookup"><span data-stu-id="d5add-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="d5add-241">Valige väljalt Kaubakood suvand String.</span><span class="sxs-lookup"><span data-stu-id="d5add-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="d5add-242">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5add-242">Click Add.</span></span>
63. <span data-ttu-id="d5add-243">Väljale Kirjeldus sisestage „Algatava osapoole määratud kordumatu kood.</span><span class="sxs-lookup"><span data-stu-id="d5add-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="d5add-244">Seda ID-d edastatakse muutmata kujul kogu ahela ulatuses.</span><span class="sxs-lookup"><span data-stu-id="d5add-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="d5add-245">Sisestage väljale Nimi suvand PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="d5add-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="d5add-246">Suvandi PaymentModel nimi joondatakse maksevormide eelmääratletud liidestega.</span><span class="sxs-lookup"><span data-stu-id="d5add-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="d5add-247">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d5add-247">Click Save.</span></span>
66. <span data-ttu-id="d5add-248">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d5add-248">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]