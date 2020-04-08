---
title: Vormingute loomisel andmemudelite määratluste valimine
description: Selle protseduuri toimingute lõpuleviimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 374c31b5ea9160fba773e82f658e8de05c67cab4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143242"
---
# <a name="select-data-model-definitions-when-you-create-formats"></a><span data-ttu-id="be321-103">Vormingute loomisel andmemudelite määratluste valimine</span><span class="sxs-lookup"><span data-stu-id="be321-103">Select data model definitions when you create formats</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be321-104">Selle protseduuri toimingute lõpuleviimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“.</span><span class="sxs-lookup"><span data-stu-id="be321-104">To complete the steps in this procedure, you must first complete the procedure, ER Create a configuration provider and mark it as active.</span></span> 

<span data-ttu-id="be321-105">Selle protseduuriga demonstreeritakse, kuidas saab käsitleda mudeli juurkaupa andmemudeli definitsioonina ER-i vormingukonfiguratsioonis, mis on kujundatud elektrooniliste dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="be321-105">This procedure shows how a model's root item can be selected as a data model definition for inserting an Electronic reporting (ER) format configuration that is designed to generate electronic documents.</span></span> <span data-ttu-id="be321-106">Selles näites lisate uue vormingukonfiguratsiooni näidisettevõttele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="be321-106">In this procedure, you will add a new ER format configuration for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="be321-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="be321-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="be321-108">Need toimingud saab lõpule viia ükskõik, millise andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="be321-108">The steps can be completed by using any dataset.</span></span>

1. <span data-ttu-id="be321-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="be321-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="be321-110">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena.</span><span class="sxs-lookup"><span data-stu-id="be321-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="be321-111">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="be321-111">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  
2. <span data-ttu-id="be321-112">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="be321-112">Click Reporting configurations.</span></span>

## <a name="add-a-new-er-data-model-configuration"></a><span data-ttu-id="be321-113">Uue elektroonilise aruandluse andmemudeli konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="be321-113">Add a new ER data model configuration</span></span>
1. <span data-ttu-id="be321-114">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="be321-114">Click Create configuration to open the drop dialog.</span></span>
    * <span data-ttu-id="be321-115">Lisame uue elektroonilise aruandluse konfiguratsiooni, mis sisaldab andmemudeleid, mida kasutatakse andmeallikatena elektroonilise aruandluse genereerimiseks.</span><span class="sxs-lookup"><span data-stu-id="be321-115">We add a new ER model configuration containing a data model that is designed to be used as data source for generation ER reports.</span></span>  
2. <span data-ttu-id="be321-116">Sisestage nimeväljale tekst „Payment model (fictitious)".</span><span class="sxs-lookup"><span data-stu-id="be321-116">In the Name field, type 'Payment model (fictitious)'.</span></span>
    * <span data-ttu-id="be321-117">Maksemudel (fiktiivne)</span><span class="sxs-lookup"><span data-stu-id="be321-117">Payment model (fictitious)</span></span>  
3. <span data-ttu-id="be321-118">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="be321-118">Click Create configuration.</span></span>
4. <span data-ttu-id="be321-119">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="be321-119">Click Designer.</span></span>
    * <span data-ttu-id="be321-120">Avage selle konfiguratsiooni andmemudeli struktuuri määramiseks elektroonilise aruandluse koostur.</span><span class="sxs-lookup"><span data-stu-id="be321-120">Open the ER designer to specify the structure of data model of this configuration.</span></span>  
    * <span data-ttu-id="be321-121">Oletame, et me loome andmemudeli maksete äridomeeni jaoks, et toetada kahte makseviisi – kreeditülekannet ja otsekorraldust.</span><span class="sxs-lookup"><span data-stu-id="be321-121">Assume that we design the data model for payments business domain to support 2 payment methods – credit transfer and direct debit ones.</span></span>  
5. <span data-ttu-id="be321-122">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="be321-122">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="be321-123">Sisestage nimeväljale tekst „Payments – credit transfer”.</span><span class="sxs-lookup"><span data-stu-id="be321-123">In the Name field, type 'Payments – credit transfer'.</span></span>
    * <span data-ttu-id="be321-124">Maksed – kreeditiülekanne</span><span class="sxs-lookup"><span data-stu-id="be321-124">Payments – credit transfer</span></span>  
7. <span data-ttu-id="be321-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="be321-125">Click Add.</span></span>
8. <span data-ttu-id="be321-126">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="be321-126">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="be321-127">Väljale Uus sõlm kui sisestage „Mudeli juur”.</span><span class="sxs-lookup"><span data-stu-id="be321-127">In the New node as a field, enter 'Model root'.</span></span>
10. <span data-ttu-id="be321-128">Sisestage nimeväljale tekst „Payments – direct debit'.".</span><span class="sxs-lookup"><span data-stu-id="be321-128">In the Name field, type 'Payments – direct debit'.</span></span>
    * <span data-ttu-id="be321-129">Maksed – otsekorraldus</span><span class="sxs-lookup"><span data-stu-id="be321-129">Payments – direct debit</span></span>  
11. <span data-ttu-id="be321-130">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="be321-130">Click Add.</span></span>
12. <span data-ttu-id="be321-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="be321-131">Click Save.</span></span>
13. <span data-ttu-id="be321-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be321-132">Close the page.</span></span>
14. <span data-ttu-id="be321-133">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="be321-133">Click Change status.</span></span>
    * <span data-ttu-id="be321-134">Uue mudeli kättesaadavaks tegemiseks uue mudeli vastendustes ja vormingute viige lõpule mudeli mustandiversioon.</span><span class="sxs-lookup"><span data-stu-id="be321-134">Complete the draft version of the model to make it available in new model mappings and formats.</span></span>  
15. <span data-ttu-id="be321-135">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="be321-135">Click Complete.</span></span>
16. <span data-ttu-id="be321-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="be321-136">Click OK.</span></span>

## <a name="start-to-enter-a-new-er-format-configuration"></a><span data-ttu-id="be321-137">Hakake sisestama uut elektroonilise aruandluse (ER) konfiguratsiooni</span><span class="sxs-lookup"><span data-stu-id="be321-137">Start to enter a new ER format configuration</span></span>
1. <span data-ttu-id="be321-138">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="be321-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="be321-139">Sisestage väljale Uus tekst „Format based on data model Payment model (fictitious)".</span><span class="sxs-lookup"><span data-stu-id="be321-139">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="be321-140">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="be321-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="be321-141">Pange tähele, et kõik valitud andmemudeli juurkaubad on praegu saadaval andmemudeli definitsioonina valimiseks.</span><span class="sxs-lookup"><span data-stu-id="be321-141">Note that all root items of the selected data model are currently available for selection as a data model definition.</span></span> <span data-ttu-id="be321-142">Saate jätkata oma vormingu loomist, kui kasutate selleks andmemudeli nõutavaid juurkaupu.</span><span class="sxs-lookup"><span data-stu-id="be321-142">You can continue to design your format by using any of the required root items of the data model.</span></span> <span data-ttu-id="be321-143">Valitud juurkauba puuduv mudelivastendus ei takista teil jätkamast.</span><span class="sxs-lookup"><span data-stu-id="be321-143">A missing model mapping for the selected root item doesn't prevent you from continuing.</span></span>  
4. <span data-ttu-id="be321-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be321-144">Close the page.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="be321-145">Uue elektroonilise aruandluse mudelivastenduse konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="be321-145">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="be321-146">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="be321-146">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="be321-147">Sisestage väljale Uus suvand „Model Mapping based on data model Payment model (fictitious)".</span><span class="sxs-lookup"><span data-stu-id="be321-147">In the New field, enter 'Model Mapping based on data model Payment model (fictitious)'.</span></span>
3. <span data-ttu-id="be321-148">Sisestage nimeväljale tekst „Payment model mappings (fictitious)".</span><span class="sxs-lookup"><span data-stu-id="be321-148">In the Name field, type 'Payment model mappings (fictitious)'.</span></span>
    * <span data-ttu-id="be321-149">Maksemudeli vastendused (fiktiivne)</span><span class="sxs-lookup"><span data-stu-id="be321-149">Payment model mappings (fictitious)</span></span>  
4. <span data-ttu-id="be321-150">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="be321-150">In the Data model definition field, enter or select a value.</span></span>
5. <span data-ttu-id="be321-151">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="be321-151">Click Create configuration.</span></span>

## <a name="design-er-model-mappings"></a><span data-ttu-id="be321-152">Elektroonilise aruandluse (ER) mudelivastenduste loomine</span><span class="sxs-lookup"><span data-stu-id="be321-152">Design ER model mappings</span></span>
1. <span data-ttu-id="be321-153">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="be321-153">Click Designer.</span></span>
    * <span data-ttu-id="be321-154">Nõutava juurkauba mudeli vastenduste määramiseks kasutage elektroonilise aruandluse koosturit.</span><span class="sxs-lookup"><span data-stu-id="be321-154">Use the ER designer to specify the model mappings for the required root items.</span></span>  
2. <span data-ttu-id="be321-155">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="be321-155">Click Designer.</span></span>
    * <span data-ttu-id="be321-156">Saate simuleerida mudeli juurkauba valitud mudelivastenduse sätte.</span><span class="sxs-lookup"><span data-stu-id="be321-156">Simulate setting of selected model mapping for the selected model's root item.</span></span>  
3. <span data-ttu-id="be321-157">Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.</span><span class="sxs-lookup"><span data-stu-id="be321-157">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
4. <span data-ttu-id="be321-158">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="be321-158">Click Add root.</span></span>
5. <span data-ttu-id="be321-159">Sisestage nimeväljale „Ledger”.</span><span class="sxs-lookup"><span data-stu-id="be321-159">In the Name field, type 'Ledger'.</span></span>
6. <span data-ttu-id="be321-160">Sisestage väljale Tabel suvand LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="be321-160">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="be321-161">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="be321-161">LedgerJournalTrans</span></span>  
7. <span data-ttu-id="be321-162">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="be321-162">Click OK.</span></span>
8. <span data-ttu-id="be321-163">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="be321-163">Click Save.</span></span>
9. <span data-ttu-id="be321-164">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be321-164">Close the page.</span></span>
10. <span data-ttu-id="be321-165">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be321-165">Close the page.</span></span>

## <a name="start-to-enter-another-new-er-format-configuration"></a><span data-ttu-id="be321-166">Hakake sisestama veel ühte uut elektroonilise aruandluse (ER) konfiguratsiooni</span><span class="sxs-lookup"><span data-stu-id="be321-166">Start to enter another new ER format configuration</span></span>
1. <span data-ttu-id="be321-167">Tehke puul valik „'Payment model (fictitious)".</span><span class="sxs-lookup"><span data-stu-id="be321-167">In the tree, select 'Payment model (fictitious)'.</span></span>
2. <span data-ttu-id="be321-168">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="be321-168">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="be321-169">Sisestage väljale Uus tekst „Format based on data model Payment model (fictitious)".</span><span class="sxs-lookup"><span data-stu-id="be321-169">In the New field, enter 'Format based on data model Payment model (fictitious)'.</span></span>
4. <span data-ttu-id="be321-170">Sisestage või valige väärtus väljal Andmemudeli definitsioon.</span><span class="sxs-lookup"><span data-stu-id="be321-170">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="be321-171">Pange tähele, et rakenduse andmeallikasse vastendamiseks on nüüd saadaval ainult üks juurkaup.</span><span class="sxs-lookup"><span data-stu-id="be321-171">Note that now only one root item is available to map to the application data sources.</span></span> <span data-ttu-id="be321-172">Kui kasutusele on võetud vähemalt üks mudelivastendus, saab elektroonilise aruandluse vormingusse lisada ainult need mudeli juurkaubad, mis on vastendatud rakenduse andmeallikatesse.</span><span class="sxs-lookup"><span data-stu-id="be321-172">When at least one model mapping is introduced, only the model's root items that are mapped to application data sources can be selected as a model definition while the ER format is added.</span></span>   
5. <span data-ttu-id="be321-173">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be321-173">Close the page.</span></span>

