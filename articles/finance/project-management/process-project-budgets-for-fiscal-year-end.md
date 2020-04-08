---
title: Projektieelarvete ülekandmine finantsaasta lõpus
description: Selles artiklis kirjeldatakse kuidas järelejäänud eelarvesummasid järgmistesse aastatesse üle kanda ja eelarveregistri üksikasju luua.
author: RadhikaRS
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 41e985825a24de2d6510938cf3d61715c35f9939
ms.sourcegitcommit: 2ea5ff784500d5be9203e9a1560eabd4fea46f4e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172326"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="89644-103">Projektieelarvete ülekandmine finantsaasta lõpus</span><span class="sxs-lookup"><span data-stu-id="89644-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89644-104">Mitmeaastase projektiga töötamisel võib teil finantsaasta lõpus tekkida eelarve ülejääk.</span><span class="sxs-lookup"><span data-stu-id="89644-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="89644-105">Saate kanda eelarve jääksummad üle valitud tulevasse aastasse ja luua seostatud pearaamatusse nende summadega eelarveregistri üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="89644-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="89644-106">Enne jääksummade ülekandmist vaadake üle ja analüüsige järelejäänud eelarve summasid.</span><span class="sxs-lookup"><span data-stu-id="89644-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="89644-107">Eelarve jääksummade ülevaatamine ja analüüsimine</span><span class="sxs-lookup"><span data-stu-id="89644-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="89644-108">Läbige järgmised etapid projektide aastalõpu eelarvesummade ülevaatamiseks, kuid mitte nende summade edasi kandmiseks.</span><span class="sxs-lookup"><span data-stu-id="89644-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="89644-109">Avage jaotis **Projektihaldus ja -arvestus** > **Perioodiline** > **Eelarved** > **Edasikantavad eelarved**.</span><span class="sxs-lookup"><span data-stu-id="89644-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="89644-110">Lehe **Projekti eelarve edasikandmisprotsess** vahekaardil **Aastalõpu suvandid** veenduge, et suvand **Projektieelarve jääksumma edasikandmine** ei oleks lubatud.</span><span class="sxs-lookup"><span data-stu-id="89644-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="89644-111">Vahekaardi **Parameetrid** väljal **Projekti eelarveaasta** valige selle finantsaasta, mille eelarve jääksummat vaadata soovite.</span><span class="sxs-lookup"><span data-stu-id="89644-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="89644-112">Väljal **Avatud finantsaasta** valige see finantsaasta, mille eelarve jääksummasid vaadata soovite.</span><span class="sxs-lookup"><span data-stu-id="89644-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="89644-113">Väljal **Prognoosimudelist** valige **Järelejäänud eelarve**.</span><span class="sxs-lookup"><span data-stu-id="89644-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="89644-114">Teie valitud kriteeriumitele vastavate projektide kaasamiseks ilma järelejääva eelarveta valige **Nulljäägi kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="89644-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="89644-115">Valige vahekaardil **Eelarvete valimine** käsk **Too kõik eelarved**, et laadida kõik eelarved, mis vastavad teie valitud kriteeriumitele ja seejärel valige **Töötle**.</span><span class="sxs-lookup"><span data-stu-id="89644-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="89644-116">Andmebaasipäringu loomiseks, mis laadib paani konkreetse eelarvete kogumi, klõpsake valikut **Too valitud eelarved**.</span><span class="sxs-lookup"><span data-stu-id="89644-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="89644-117">Paanil kindla rea kohta kohta saamiseks valige see rida ja seejärel valige **Kuva eelarve üksikasjad** või **Vaata kontosid**.</span><span class="sxs-lookup"><span data-stu-id="89644-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="89644-118">Kanna eelarve järelejäänud summad edasi</span><span class="sxs-lookup"><span data-stu-id="89644-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="89644-119">Kui töötlete eelarve jääksummasid, saate luua pearaamatusse kanded edasikantavate summade kohta.</span><span class="sxs-lookup"><span data-stu-id="89644-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="89644-120">Pearaamatu kannete loomiseks tehke järgmised toimingud jaotises [Eelarve summade edasi kandmine ja pearaamatu kannete loomine](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="89644-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="89644-121">Edasikantud eelarvesummad kantakse üle eelarvemudelisse, mis on valitud lehel **Eelarvemudelid** edasikandmise eelarvemudeliks.</span><span class="sxs-lookup"><span data-stu-id="89644-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="89644-122">Eelarvesummade edasikandmine ja pearaamatu kannete loomine</span><span class="sxs-lookup"><span data-stu-id="89644-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="89644-123">Valige **Projektihaldus ja -arvestus** > **Perioodiline** > **Eelarved** > **Edasikantavad eelarved**.</span><span class="sxs-lookup"><span data-stu-id="89644-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="89644-124">Lehel **Projekti eelarve edasikandmisprotsess** valige **Aastalõpp** ja seejärel lubage **Projekti eelarve jääksummade edasikandmine** ja **Eelarveregistri kirjete loomine pearaamatus**.</span><span class="sxs-lookup"><span data-stu-id="89644-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="89644-125">Tehke järgmised valikud vahekaardi **Parameetrid** väljagrupis **Projekti parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="89644-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="89644-126">**Projekti eelarveaasta**: valige selle finantsaasta algus, mille eelarve jääksummasid vaadata soovite.</span><span class="sxs-lookup"><span data-stu-id="89644-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="89644-127">**Kasum ja kahjum**: looge pearaamatus kasumi ja kahjumi kanded.</span><span class="sxs-lookup"><span data-stu-id="89644-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="89644-128">**WIP**: looge pearaamatus poolelioleva töö (WIP) kanded.</span><span class="sxs-lookup"><span data-stu-id="89644-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="89644-129">**Palgaarvestus**: looge pearaamatus palgaarvestuse eraldamise kanded.</span><span class="sxs-lookup"><span data-stu-id="89644-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="89644-130">Sisestage järgmine teave väljagrupis **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="89644-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="89644-131">Väljal **Avatud finantsaasta** valige see finantsaasta, millele projektide eelarve jääksummasid üle kanda soovite.</span><span class="sxs-lookup"><span data-stu-id="89644-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="89644-132">Vaikeväärtus on üks aasta pärast välja **Projekti eelarveaasta** väärtust.</span><span class="sxs-lookup"><span data-stu-id="89644-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="89644-133">Väljal **Edasikandmise periood** valige periood, milles soovite pearaamatusse eelarveregistri üksikasju luua.</span><span class="sxs-lookup"><span data-stu-id="89644-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="89644-134">See on tavaliselt avatud finantsaasta esimene periood.</span><span class="sxs-lookup"><span data-stu-id="89644-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="89644-135">Sisestage järgmine teave väljagrupis **Kopeeri üksusest/üksusesse**.</span><span class="sxs-lookup"><span data-stu-id="89644-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="89644-136">Väljal **Eelarvemudelist** valige projekti eelarvemudel, mis on seostatud eelarve jääksummadega, mida soovite projektide puhul üle kanda.</span><span class="sxs-lookup"><span data-stu-id="89644-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="89644-137">Väljal **Pearaamatu eelarvemudelisse** valige pearaamatu eelarvemudel, mis on seostatud eelarvesummadega, mida soovite pearaamatusse üle kanda.</span><span class="sxs-lookup"><span data-stu-id="89644-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="89644-138">Valige **Müügivaluuta ülekandmine** projekti müügivaluuta kasutamiseks pearaamatu kannetel, mis luuakse projektide eelarvesummade ülekandmisel.</span><span class="sxs-lookup"><span data-stu-id="89644-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="89644-139">Kui seda suvandit pole valitud, kasutavad kanded arvestusvaluutat.</span><span class="sxs-lookup"><span data-stu-id="89644-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="89644-140">Valige **Nulljäägi kuvamine**, et kaasata ilma eelarve jääksummata projektid, kuid mis vastavad muudele valitud kriteeriumitele paani allservas kuvatud projektidel.</span><span class="sxs-lookup"><span data-stu-id="89644-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="89644-141">Valige vahekaardil **Eelarvete valimine** käsk **Too kõik eelarved**, et laadida kõik eelarved, mis vastavad teie valitud kriteeriumitele.</span><span class="sxs-lookup"><span data-stu-id="89644-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="89644-142">Kui eelistate luua andmebaasipäringu, mis laadib paani konkreetse projekti eelarvete kogumi, klõpsake valikut **Too valitud eelarved**.</span><span class="sxs-lookup"><span data-stu-id="89644-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="89644-143">Iga projekti puhul, mida soovite töödelda, valige suvand vastava projekti rea alguses.</span><span class="sxs-lookup"><span data-stu-id="89644-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="89644-144">Kõigi või enamiku projektide valimiseks valige märge ülemises vasakus nurgas.</span><span class="sxs-lookup"><span data-stu-id="89644-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="89644-145">Mis tahes projekti töötlemise välistamiseks tühjendage selle projekti märge.</span><span class="sxs-lookup"><span data-stu-id="89644-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="89644-146">Selleks , et kanda valitud projektide eelarve jääksummad üle valitud finantsaastasse ja luua pearaamatusse eelarveregistri üksikasjad, valige **Töötle**.</span><span class="sxs-lookup"><span data-stu-id="89644-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="89644-147">Eelarvesummade edasikandmine ilma pearaamatu kannete loomiseta</span><span class="sxs-lookup"><span data-stu-id="89644-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="89644-148">Avage jaotis **Projektihaldus ja -arvestus** > **Perioodiline** > **Eelarved** > **Edasikantavad eelarved**.</span><span class="sxs-lookup"><span data-stu-id="89644-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="89644-149">Lehe **Projekti eelarve edasikandmisprotsess** väljal **Aastalõpu suvandid** valige **Projektieelarve jääksumma edasikandmine**.</span><span class="sxs-lookup"><span data-stu-id="89644-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="89644-150">Grupi **Parameetrid** väljal **Projekti eelarveaasta** valige selle finantsaasta, mille eelarve jääksummasid vaadata soovite.</span><span class="sxs-lookup"><span data-stu-id="89644-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="89644-151">Sisestage järgmine teave grupis **Kopeeri üksusest/üksusesse**.</span><span class="sxs-lookup"><span data-stu-id="89644-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="89644-152">Väljal **Eelarvemudelist** valige projekti eelarvemudel, mis on seostatud eelarve jääksummadega, mida soovite projektide puhul üle kanda.</span><span class="sxs-lookup"><span data-stu-id="89644-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="89644-153">Valige **Nulljäägi kuvamine** teie valitud kriteeriumitele vastavate projektide kaasamiseks ilma järelejääva eelarveta.</span><span class="sxs-lookup"><span data-stu-id="89644-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="89644-154">Valige grupis **Eelarvete valimine** käsk **Too kõik eelarved**, et laadida kõik eelarved, mis vastavad teie valitud kriteeriumitele.</span><span class="sxs-lookup"><span data-stu-id="89644-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="89644-155">Andmebaasipäringu loomiseks, mis laadib paani konkreetse projekti eelarvete kogumi, klõpsake valikut **Too valitud eelarved**.</span><span class="sxs-lookup"><span data-stu-id="89644-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="89644-156">Iga projekti puhul, mida soovite töödelda, valige suvand vastava projekti rea alguses.</span><span class="sxs-lookup"><span data-stu-id="89644-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="89644-157">Valige **Töötle**, et kanda valitud projektide eelarve jääksummad üle valitud finantsaastale.</span><span class="sxs-lookup"><span data-stu-id="89644-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>

