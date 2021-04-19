---
title: Varude toimingute tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada varude toimingutega töötamisel tekkivaid probleeme.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832054"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="c5f25-103">Varude toimingute tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="c5f25-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5f25-104">Selles teemas kirjeldatakse, kuidas lahendada varude toimingutega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="c5f25-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="c5f25-105">Ma ei leia varude töölehel ripploendi välja „Töövoog”.</span><span class="sxs-lookup"><span data-stu-id="c5f25-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c5f25-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c5f25-106">Issue description</span></span>

<span data-ttu-id="c5f25-107">Te ei leia töölehelt ripploendi välja **Töövoog** või ei ole seotud töövoo toimingud saadaval.</span><span class="sxs-lookup"><span data-stu-id="c5f25-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="c5f25-108">See probleem võib esineda kolmel põhjusel, nagu kirjeldatud järgmistes alamjaotistes.</span><span class="sxs-lookup"><span data-stu-id="c5f25-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="c5f25-109">Probleemi lahendus 1</span><span class="sxs-lookup"><span data-stu-id="c5f25-109">Issue resolution 1</span></span>

<span data-ttu-id="c5f25-110">Kui see probleem tekib kõigil kasutajatel, võib selle põhjuseks olla, et kinnitamise töövoog pole töölehe nimele määratud.</span><span class="sxs-lookup"><span data-stu-id="c5f25-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="c5f25-111">Probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c5f25-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="c5f25-112">Avage **Varude haldus &gt; Seadistus &gt; Töölehtede nimed &gt; Varud**.</span><span class="sxs-lookup"><span data-stu-id="c5f25-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="c5f25-113">Valige sellel paanil töölehe nimi, et avada selle sätted.</span><span class="sxs-lookup"><span data-stu-id="c5f25-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="c5f25-114">Määrake kiirkaardi **Üldine** suvandi **Kinnituse töövoog** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="c5f25-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="c5f25-115">Kui teil palutakse muudatus kinnitada, klõpsake valikut **Jah**.</span><span class="sxs-lookup"><span data-stu-id="c5f25-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="c5f25-116">Väljal **Töövoog** valige töövoog, mida soovite valitud töölehe nime jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="c5f25-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="c5f25-117">Probleemi lahendus 2</span><span class="sxs-lookup"><span data-stu-id="c5f25-117">Issue resolution 2</span></span>

<span data-ttu-id="c5f25-118">Kui teie töövoog kasutab kohandatud koodi, võivad ilmneda probleemid pärast süsteemi täiendamist.</span><span class="sxs-lookup"><span data-stu-id="c5f25-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="c5f25-119">Näiteks võidakse töölehe töövoos nupp **Esita** muutuda halliks, nii et te ei saa seda esitamise kinnitamiseks valida.</span><span class="sxs-lookup"><span data-stu-id="c5f25-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="c5f25-120">Kui nupp **Esita** on hall, on võimalik, et teie töövoog on kohandatud, mis tähendab, et töövoo meetodit `canSubmitToWorkflow()` atribuudis `FormDataUtil` laiendati.</span><span class="sxs-lookup"><span data-stu-id="c5f25-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="c5f25-121">Selle probleemi lahendamiseks muutke viisi, kuidas te atribuudi `canSubmitToWorkflow()` meetodit laiendate, et kasutada järgmises näites.</span><span class="sxs-lookup"><span data-stu-id="c5f25-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="c5f25-122">Probleemi lahendus 3</span><span class="sxs-lookup"><span data-stu-id="c5f25-122">Issue resolution 3</span></span>

<span data-ttu-id="c5f25-123">Kui probleem esineb vaid teatud kindlatel kasutajatel, ei pruugi nendel kasutajatel olla turvaõigusi, mis on vajalikud varude töölehtedel töövoo toimingute käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="c5f25-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="c5f25-124">Veenduge, et igal mõjutatud kasutajal oleks turvalisuse privileeg *Varude töölehe töövoo haldamine*.</span><span class="sxs-lookup"><span data-stu-id="c5f25-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="c5f25-125">Vaikimisi määratakse see privileeg kohustusele, mis on sama nimega, ja see kohustus rakendatakse rollidele *Laotöötaja* ja *Lao juhataja*.</span><span class="sxs-lookup"><span data-stu-id="c5f25-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="c5f25-126">Minu varude tööleht jääb süsteemis lukus olekusse ja töövoo pakett-töö ei tööta.</span><span class="sxs-lookup"><span data-stu-id="c5f25-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c5f25-127">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c5f25-127">Issue description</span></span>

<span data-ttu-id="c5f25-128">Üks teie varude töölehtedest on mingi toimingu poolt lukustatud ja seda ei vabastata.</span><span class="sxs-lookup"><span data-stu-id="c5f25-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="c5f25-129">Näiteks kui sisestamisel (mis on süsteemi lukustustoiming) ilmneb tundmatu tõrge, võib tööleht jääda süsteemis lukus olekusse.</span><span class="sxs-lookup"><span data-stu-id="c5f25-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="c5f25-130">Sel juhul kuvab töövoo tööüksuse ohjur tõrke, tehes samal ajal lukustuse kinnitamise.</span><span class="sxs-lookup"><span data-stu-id="c5f25-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c5f25-131">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c5f25-131">Issue resolution</span></span>

<span data-ttu-id="c5f25-132">Logige sisse Supply Chain Managementi SQL-serveri eksemplari ja kontrollige, kas **InventJournalTable.SystemBlocked** väärtuseks on määratud *1*.</span><span class="sxs-lookup"><span data-stu-id="c5f25-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="c5f25-133">Kui on, siis veenduge, et tööleht ei oleks lukustatud olekus, ja lähtestage atribuut **inventJournalTable.SystemBlocked** väärtusele *0*.</span><span class="sxs-lookup"><span data-stu-id="c5f25-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="c5f25-134">Minu varude töölehe töövoog ei ole kunagi lõpetatud ja töölehte ei saa redigeerida ega sisestada.</span><span class="sxs-lookup"><span data-stu-id="c5f25-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c5f25-135">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c5f25-135">Issue description</span></span>

<span data-ttu-id="c5f25-136">Pärast töölehe kinnitamise töövoogu esitamist lõpetab töövoo töötlemine vastamise ja te ei saa oma töölehti redigeerida ega töödelda.</span><span class="sxs-lookup"><span data-stu-id="c5f25-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c5f25-137">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c5f25-137">Issue resolution</span></span>

<span data-ttu-id="c5f25-138">On mitu põhjust, miks töövoo töötlemine ei pruugi olla lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="c5f25-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="c5f25-139">Kontrollige järgmiste probleemide suhtes.</span><span class="sxs-lookup"><span data-stu-id="c5f25-139">Check for the following issues:</span></span>

- <span data-ttu-id="c5f25-140">Avage **Laohaldus &gt; Seadistus &gt; Varude halduse töövood** ja vaadake üle mõjutatud töövoo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="c5f25-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="c5f25-141">Lisateavet vt [Varude töölehe kinnitamise töövood](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c5f25-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="c5f25-142">Töövoos võib tekkida erand või tõrge.</span><span class="sxs-lookup"><span data-stu-id="c5f25-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="c5f25-143">Vaadake üle mõjutatud töövoo tööüksuse ajalugu, et näha, kas see sisaldab rakenduse tõrget, mis lõpetab töövoo.</span><span class="sxs-lookup"><span data-stu-id="c5f25-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="c5f25-144">Varude töölehte saab uuendada või redigeerida ainult siis, kui see on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="c5f25-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="c5f25-145">Kui tagasikutsumine on aktiivne, võite proovida töölehte tagasi kutsuda.</span><span class="sxs-lookup"><span data-stu-id="c5f25-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="c5f25-146">Töövoo pakett-töö käivitamine võib olla peatatud mitmel põhjusel.</span><span class="sxs-lookup"><span data-stu-id="c5f25-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="c5f25-147">Mõned neist põhjustest võivad olla põhjustatud töövoo raamistiku probleemist.</span><span class="sxs-lookup"><span data-stu-id="c5f25-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="c5f25-148">Varude töölehe töövoo tingimused kehtivad ainult töölehe tasemel, mitte rea tasemel</span><span class="sxs-lookup"><span data-stu-id="c5f25-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="c5f25-149">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c5f25-149">Issue description</span></span>

<span data-ttu-id="c5f25-150">Teil võib tekkida selline probleem, kui proovite näiteks seadistada varude töölehe töövoo tingimust kulusummale.</span><span class="sxs-lookup"><span data-stu-id="c5f25-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="c5f25-151">Seadistate tingimuse nii, et 1. etappi käitatakse ainult siis, kui omahind on väiksem kui 100.</span><span class="sxs-lookup"><span data-stu-id="c5f25-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="c5f25-152">Seejärel seadistate teise tingimuse nii, et 2. etappi käitatakse ainult siis, kui omahind on suurem või võrdne kui 100.</span><span class="sxs-lookup"><span data-stu-id="c5f25-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="c5f25-153">Töövoo käivitamisel kuvatakse töövoo ajaloos ainult üks rida ja esimene tingimus hinnatakse alati *tõesena*, sõltumata edastatud väärtusest.</span><span class="sxs-lookup"><span data-stu-id="c5f25-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="c5f25-154">Probleemi lahendus</span><span class="sxs-lookup"><span data-stu-id="c5f25-154">Issue workaround</span></span>

<span data-ttu-id="c5f25-155">Praeguses versioonis kehtivad varude töövoo tingimused ainult töölehe tasemel, mitte rea tasemel.</span><span class="sxs-lookup"><span data-stu-id="c5f25-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="c5f25-156">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="c5f25-156">This behavior is by design.</span></span> <span data-ttu-id="c5f25-157">Soovitame seada tingimuse kriteeriumiks ainult töölehe taseme atribuudid.</span><span class="sxs-lookup"><span data-stu-id="c5f25-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="c5f25-158">Vaba kaubavaru loendilehe filtripaan ei filtreeri tulemusi nii, nagu ma eeldan.</span><span class="sxs-lookup"><span data-stu-id="c5f25-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c5f25-159">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c5f25-159">Issue description</span></span>

<span data-ttu-id="c5f25-160">**Vaba kaubavaru** loendilehe filtripaani filtrid ei filtreeri tulemusi nii, nagu te eeldate.</span><span class="sxs-lookup"><span data-stu-id="c5f25-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c5f25-161">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c5f25-161">Issue resolution</span></span>

<span data-ttu-id="c5f25-162">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="c5f25-162">This behavior is by design.</span></span>

<span data-ttu-id="c5f25-163">Leht  **Vaba kaubavaru** loend koostatakse üksikasjalikust vaba kaubavaru tabelist, mis sisaldab kõiki saadaolevaid dimensioone.</span><span class="sxs-lookup"><span data-stu-id="c5f25-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="c5f25-164">Sellel lehel olev loend on aga vaid kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="c5f25-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="c5f25-165">Seetõttu võidakse selles kombineerida lähtetabeli ridu, koondades väärtuseid kuvatud dimensioonide järgi.</span><span class="sxs-lookup"><span data-stu-id="c5f25-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="c5f25-166">Filtripaanil häälestatud filtrid rakenduvad lähtetabelile, mitte koondatud loendile.</span><span class="sxs-lookup"><span data-stu-id="c5f25-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="c5f25-167">Selline käitumine võib mõnikord anda ootamatuid tulemusi, nagu näha [nendes näidetes](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="c5f25-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="c5f25-168">Ruudustikus  [ruudustikus esitatud filtrid](inventory-on-hand-list.md#grid-filters) *siiski* rakenduvad koondatud loendile.</span><span class="sxs-lookup"><span data-stu-id="c5f25-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="c5f25-169">Need filtrid hõlmavad nii kiirfiltrit ruudustiku ülaosas kui ka iga veerupäise filtrit.</span><span class="sxs-lookup"><span data-stu-id="c5f25-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="c5f25-170">Ühik ja ühiku kogus ei tööta varude töölehel õigesti.</span><span class="sxs-lookup"><span data-stu-id="c5f25-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c5f25-171">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c5f25-171">Issue description</span></span>

<span data-ttu-id="c5f25-172">Varude töölehel üksuste ja kogustega töötades võite puutuda kokku ühe või mõlema probleemiga.</span><span class="sxs-lookup"><span data-stu-id="c5f25-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="c5f25-173">Te ei näe varude töölehel ühikuid ega ühiku koguseid, kui väljastatud tootele on seadistatud teisendusühik, ja te ei saa ühikut varude töölehel muuta.</span><span class="sxs-lookup"><span data-stu-id="c5f25-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="c5f25-174">Näete varude töölehel väljasid **Kogus** ja **Ühik**, kuid te ei näe välja **Ühiku kogus**.</span><span class="sxs-lookup"><span data-stu-id="c5f25-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="c5f25-175">Kui muudate ühikut, sisestate koguse ja sisestate töölehe, kuvatakse töölehel siiski selle koguse algne mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="c5f25-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c5f25-176">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c5f25-176">Issue resolution</span></span>

<span data-ttu-id="c5f25-177">Selle probleemi lahendamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="c5f25-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="c5f25-178">Kontrollige **funktsioonihalduse** tööruumis, et funktsioon *Mõõtühiku ja ühiku koguse kasutamine varude töölehtedel* oleks sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="c5f25-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="c5f25-179">See funktsioon lisab töölehele väljad **Ühik** ja **Ühiku kogus**.</span><span class="sxs-lookup"><span data-stu-id="c5f25-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="c5f25-180">Kui funktsioon on sisse lülitatud, kasutage välju **Kogus**, **Ühiku kogus** ja **Ühik** järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="c5f25-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="c5f25-181">**Kogus** – määrake kogus, kasutades vaikeühikut, mis on vabastatud toote jaoks määratletud.</span><span class="sxs-lookup"><span data-stu-id="c5f25-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="c5f25-182">Samas vaikeühikut ennast siin ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="c5f25-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="c5f25-183">Kui vaikeühiku ja väljal **Ühik** valitud ühiku vahel on häälestatud teisendus, uuendatakse välja **Kogus** väljade **Ühiku kogus** ja **Ühik** valikute alusel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="c5f25-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="c5f25-184">**Ühiku kogus** – määrake kogus, kasutades ühikut, mis on valitud väljal **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="c5f25-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="c5f25-185">**Ühik** – valige ühik, mida rakendada väljal **Ühiku kogus** määratud väärtusele.</span><span class="sxs-lookup"><span data-stu-id="c5f25-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="c5f25-186">Mulle kuvatakse järgmine tõrketeade: „Varude arvestusühiku kümnendkohtade maksimumarv on 0.”</span><span class="sxs-lookup"><span data-stu-id="c5f25-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c5f25-187">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c5f25-187">Issue description</span></span>

<span data-ttu-id="c5f25-188">Kui proovite sisestada laokannet või varude reserveerimist, kuvatakse järgmine tõrketeade: „Varude arvestusühiku kümnendkohtade maksimumarv on 0.”</span><span class="sxs-lookup"><span data-stu-id="c5f25-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="c5f25-189">See probleem ilmneb, kui laokanmete kogus on määratud kümnendväärtusena, mis on allpool täpsustaset, mida väli toetab.</span><span class="sxs-lookup"><span data-stu-id="c5f25-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="c5f25-190">Näiteks on laokande jaoks määratud kogus *0,5*, kuid toetatakse ainult täisarvukoguseid.</span><span class="sxs-lookup"><span data-stu-id="c5f25-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="c5f25-191">Seetõttu peab väärtus olema *0,5* asemel *1*.</span><span class="sxs-lookup"><span data-stu-id="c5f25-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c5f25-192">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c5f25-192">Issue resolution</span></span>

1. <span data-ttu-id="c5f25-193">Käivitage oma SQL-serveri eksemplaris järgmine skript, et ümardada laokannetes kogused.</span><span class="sxs-lookup"><span data-stu-id="c5f25-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="c5f25-194">See skript parandab väärtused tabelis **inventTrans**.</span><span class="sxs-lookup"><span data-stu-id="c5f25-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="c5f25-195">Käivitage vaba kaubavaru järjepidevuse kontroll, kus valik **paranda tõrge** on sisselülitatud.</span><span class="sxs-lookup"><span data-stu-id="c5f25-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="c5f25-196">See kontroll parandab väärtused tabelis **inventSum**.</span><span class="sxs-lookup"><span data-stu-id="c5f25-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5f25-197">Soovitame tungivalt, et redigeeriksite skripti hoolikalt vastavalt oma keskkonnale, katsetaksite seda katsekeskkonnas ning seejärel kontrolliksite saadud andmeid enne skripti käivitamist tootmiskeskkonnas.</span><span class="sxs-lookup"><span data-stu-id="c5f25-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]