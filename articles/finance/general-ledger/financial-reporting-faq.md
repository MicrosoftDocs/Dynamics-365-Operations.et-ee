---
title: Finantsaruandluse KKK
description: Sellesse teemasse on kogutud teiste kasutajate esitatud finantsaruandlusega seotud küsimused.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3f9381f5b656d0cc0b46c8828b2ef9d024e296b0
ms.sourcegitcommit: 14785208d84b2c1efd30f140c52df35a2ccd1577
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/27/2021
ms.locfileid: "5070213"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="43d79-103">Finantsaruandluse KKK</span><span class="sxs-lookup"><span data-stu-id="43d79-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="43d79-104">Sellesse teemasse on kogutud teiste kasutajate esitatud finantsaruandlusega seotud küsimused.</span><span class="sxs-lookup"><span data-stu-id="43d79-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="43d79-105">Kuidas piirata turvapuu abil juurdepääsu aruandele?</span><span class="sxs-lookup"><span data-stu-id="43d79-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="43d79-106">Stsenaarium: USMF-i demoettevõte ei soovi, et tema bilansi aruanne oleks D365-s nähtav kõigile finantsaruandluse kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="43d79-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="43d79-107">Lahendus: turvapuu abil saate piirata juurdepääsu ühele aruandele nii, et sellele oleks juurdepääs ainult teatud kasutajatel.</span><span class="sxs-lookup"><span data-stu-id="43d79-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="43d79-108">Logige sisse finantsaruandluse aruandekoosturisse.</span><span class="sxs-lookup"><span data-stu-id="43d79-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="43d79-109">Looge uus puu definitsioon (Fail | Uus | Puu definitsioon) a.</span><span class="sxs-lookup"><span data-stu-id="43d79-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="43d79-110">Topeltklõpsake veerus **Üksuse turve** rida **Kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="43d79-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="43d79-111">i.</span><span class="sxs-lookup"><span data-stu-id="43d79-111">i.</span></span>    <span data-ttu-id="43d79-112">Klõpsake suvandit Kasutajad ja rühmad.</span><span class="sxs-lookup"><span data-stu-id="43d79-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="43d79-113">1. Valige kasutaja(d) või rühm, kellele soovite lubada juurdepääsu sellele aruandele.</span><span class="sxs-lookup"><span data-stu-id="43d79-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="43d79-114">[![kasutaja ekraan](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="43d79-115">[![turbeekraan](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="43d79-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="43d79-116">b.</span><span class="sxs-lookup"><span data-stu-id="43d79-116">b.</span></span>    <span data-ttu-id="43d79-117">Klõpsake nuppu **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="43d79-117">Click **Save**.</span></span>
  
<span data-ttu-id="43d79-118">[![salvestamisnupp](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="43d79-119">Lisage aruandedefinitsioonis uus puu definitsioon.</span><span class="sxs-lookup"><span data-stu-id="43d79-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="43d79-120">[![puu definitsiooni vorm](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="43d79-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="43d79-121">A.</span><span class="sxs-lookup"><span data-stu-id="43d79-121">A.</span></span>  <span data-ttu-id="43d79-122">Asudes puu definitsioonis klõpsake nuppu Säeadistamine ja märkige jaotises „Aruandlusüksuse valik“ ruut „Kaasa kõik üksused“.</span><span class="sxs-lookup"><span data-stu-id="43d79-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="43d79-123">[![aruandlusüksuse valiku vorm](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="43d79-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="43d79-124">**Enne:** [![enne-kuvatõmmis](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="43d79-125">**Pärast:** [![pärast-kuvatõmmis](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="43d79-126">Märkus. Ülaltoodud teate põhjuseks on, et pärast Üksuse turbe rakendamist pole minu kasutajal sellele aruandele juurdepääsu</span><span class="sxs-lookup"><span data-stu-id="43d79-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="43d79-127">Kuidas määratleda, milline konto või millised kontod pole vastavuses minu saldodega D365-s?</span><span class="sxs-lookup"><span data-stu-id="43d79-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="43d79-128">Kui teil on aruanne, mis ei vasta D365-s eeldatud olukorrale, võivad järgmised tegevused aidata teil selliseid kontosid ja hälbeid tuvastada.</span><span class="sxs-lookup"><span data-stu-id="43d79-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="43d79-129">Finantsaruandluse aruandekoosturis</span><span class="sxs-lookup"><span data-stu-id="43d79-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="43d79-130">Looge uus readefinitsioon a.</span><span class="sxs-lookup"><span data-stu-id="43d79-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="43d79-131">Klõpsake Redigeeri | Lisa read dimensioonidest i.</span><span class="sxs-lookup"><span data-stu-id="43d79-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="43d79-132">Valige MainAccount [![Valige Peaekraan_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="43d79-133">ii.</span><span class="sxs-lookup"><span data-stu-id="43d79-133">ii.</span></span> <span data-ttu-id="43d79-134">Klõpsake nuppu Ok b.</span><span class="sxs-lookup"><span data-stu-id="43d79-134">Click Ok b.</span></span>    <span data-ttu-id="43d79-135">Salvestage readefinitsioon</span><span class="sxs-lookup"><span data-stu-id="43d79-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="43d79-136">Looge uus veerudefinitsioon     [![Looge uus veerudefinitsioon](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="43d79-137">Looge uus aruandedefinitsioon a.</span><span class="sxs-lookup"><span data-stu-id="43d79-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="43d79-138">Klõpsake Sätted ja tühjendage märkeruut [![Sätetevorm](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="43d79-139">Looge aruanne.</span><span class="sxs-lookup"><span data-stu-id="43d79-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="43d79-140">Eksportige aruanne Excelisse.</span><span class="sxs-lookup"><span data-stu-id="43d79-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="43d79-141">D365-s:</span><span class="sxs-lookup"><span data-stu-id="43d79-141">In D365:</span></span> 
1.  <span data-ttu-id="43d79-142">Klõpsake Pearaamat | Päringud ja aruanded | Proovibilanss a.</span><span class="sxs-lookup"><span data-stu-id="43d79-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="43d79-143">Parameetrid i.</span><span class="sxs-lookup"><span data-stu-id="43d79-143">Parameters i.</span></span>  <span data-ttu-id="43d79-144">Alguskuupäev: rahandusaasta algus ii.</span><span class="sxs-lookup"><span data-stu-id="43d79-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="43d79-145">Kuupäevani: kuupäev, millal lõite iii. aruande</span><span class="sxs-lookup"><span data-stu-id="43d79-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="43d79-146">Finantsdimensioonikogum „Põhikonto kogum“ [![Põhikonto vorm](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="43d79-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="43d79-147">b.</span><span class="sxs-lookup"><span data-stu-id="43d79-147">b.</span></span>    <span data-ttu-id="43d79-148">Klõpsake valikut Arvuta</span><span class="sxs-lookup"><span data-stu-id="43d79-148">Click Calculate</span></span>

2.  <span data-ttu-id="43d79-149">Eksportige aruanne Excelisse</span><span class="sxs-lookup"><span data-stu-id="43d79-149">Export the report to Excel</span></span>

<span data-ttu-id="43d79-150">Nüüd saate kopeerida andmeid FR Exceli aruandest D365 proovibilansi aruandesse ja võrrelda veerge „Sulgemissaldo“.</span><span class="sxs-lookup"><span data-stu-id="43d79-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>
