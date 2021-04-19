---
title: Lao konfiguratsiooni tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega Microsoft Dynamics 365 Supply Chain Management rakenduse konfigureerimisel tekkivaid probleeme.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814388"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="c7c3d-103">Lao konfiguratsiooni tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="c7c3d-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7c3d-104">Selles teemas kirjeldatakse, kuidas lahendada müügipakkumistega Microsoft Dynamics 365 Supply Chain Management rakenduse konfigureerimisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="c7c3d-105">Kuvatakse järgmine tõrketeade: "Identifitseerimisnumber või asukoht on kehtetu."</span><span class="sxs-lookup"><span data-stu-id="c7c3d-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c7c3d-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c7c3d-106">Issue description</span></span>

<span data-ttu-id="c7c3d-107">See tõrketeade kuvatakse, kui skaneerite identifitseerimisnumbri või asukoha.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c7c3d-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c7c3d-108">Issue resolution</span></span>

<span data-ttu-id="c7c3d-109">Veenduge, et identifitseerimisnumber ei ole reserveeritud muuks.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="c7c3d-110">See probleem tekkis, kui väärtus, mida kasutaja mobiilirakenduses Warehouse Management skaneeris, oli nii kehtiv asukoht kui ka kehtiv identifitseerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-110">This issue used to occur when the value that a user scanned in the Warehouse Management mobile app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="c7c3d-111">See probleem lahendati versioonis 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="c7c3d-112">Kuvatakse järgmine tõrketeade: "Selle asukoha kohta peab määrama identifitseerimisnumbri."</span><span class="sxs-lookup"><span data-stu-id="c7c3d-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c7c3d-113">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c7c3d-113">Issue description</span></span>

<span data-ttu-id="c7c3d-114">See tõrketeade kuvatakse, kui loote üleviimistellimuse, kasutades ladu, mis on lubatud täiustatud laohalduse (WMS) jaoks, ja proovite pärast töö lõpetamist saadetist kinnitada.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c7c3d-115">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c7c3d-115">Issue resolution</span></span>

<span data-ttu-id="c7c3d-116">**Lao vastuvõtu vaikimisi asukoht** on "päritolu" lao transiidilao jaoks on tühi.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="c7c3d-117">Probleemi lahendamiseks määrake transiidilaos vaikimisi vastuvõtu asukoht.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="c7c3d-118">Veenduge, et see asukoht on identifitseerimisnumbritega kontrollitav.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="c7c3d-119">Kuvatakse järgmine tõrketeade: "Töömalli rida ei saa varude oleku muutmiseks luua, kuna töö tüüp on kehtetu.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="c7c3d-120">Valige mõni muu töö tüüp."</span><span class="sxs-lookup"><span data-stu-id="c7c3d-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c7c3d-121">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c7c3d-121">Issue description</span></span>

<span data-ttu-id="c7c3d-122">Töömalli puhul ei saa valida *Varude oleku muutust* **Töö tüübi** veerus **Töömalli detailide** jaotises.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c7c3d-123">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c7c3d-123">Issue resolution</span></span>

<span data-ttu-id="c7c3d-124">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-124">This behavior is by design.</span></span> <span data-ttu-id="c7c3d-125">*Varude oleku muutmise* töö tüüpi kasutatakse ainult süsteemi protsessidega.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="c7c3d-126">Seda ei saa konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-126">It can't be configured.</span></span> <span data-ttu-id="c7c3d-127">Kuna töö tüüpide loend on fikseeritud kui loendamine, ei saa lisakirjeid **Töö tüübi** rippmenüüst välja filtreerida.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="c7c3d-128">Kuvatakse järgmine tõrketeade: "Kogus on kehtetu kauba 1% korral."</span><span class="sxs-lookup"><span data-stu-id="c7c3d-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c7c3d-129">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c7c3d-129">Issue description</span></span>

<span data-ttu-id="c7c3d-130">Kogus ei kehti *tk* kauba kohta, kui on komplekteerimisel töö, millel on mitu identifitseerimisnumbrit ühes asukohas.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c7c3d-131">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c7c3d-131">Issue resolution</span></span>

<span data-ttu-id="c7c3d-132">Veenduge, et väljastatud toote või tootevariandi väljad **Toote seeria ID** ja **Ühiku teisendused** on õigesti seadistatud.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="c7c3d-133">Võtke arvesse, et tõrketeadet on parandatud versioonis 10.0.15 (vt [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="c7c3d-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="c7c3d-134">Uus veateade on: "Kogus ei ole kehtetu.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="c7c3d-135">Eeldatud %1 %2."</span><span class="sxs-lookup"><span data-stu-id="c7c3d-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="c7c3d-136">Asukoha direktiivides müügitellimuse komplekteerimistöö kohta, ei hinda mitu SKU-suvandit mitme asukoha direktiivi tegevusi.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c7c3d-137">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c7c3d-137">Issue description</span></span>

<span data-ttu-id="c7c3d-138">*Müügitellimuste* töötellimuse tüübi ja *Komplekteerimise* töötüübid ei hinda mitme asukoha direktiivi tegevust, kui on valitud **Mitu SKU-d**.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="c7c3d-139">Hinnatakse ainult esimese asukoha direktiivi tegevust.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c7c3d-140">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c7c3d-140">Issue resolution</span></span>

<span data-ttu-id="c7c3d-141">Uus funktsioon *Hinda mitme SKU-ga asukoha direktiivide kõiki tegevusi* on lisatud versiooni 10.0.15 (vt [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="c7c3d-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="c7c3d-142">Selle funktsiooniga hinnatakse kõiki mitme SKU-ga asukoha direktiivide tegevusi.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="c7c3d-143">Kui vajate seda funktsiooni, kasutage selle sisselülitamiseks [Funktsiooni haldamist](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c7c3d-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a><span data-ttu-id="c7c3d-144">Ma ei saa kasutada lao mobiilirakendust Warehouse Management osalise komplekteerimise tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-144">I can't use the Warehouse Management mobile app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c7c3d-145">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c7c3d-145">Issue description</span></span>

<span data-ttu-id="c7c3d-146">Ostu-ja üleviimistellimuste puhul ei saa kaupu vahele jätta ja teha osalist komplekteerimist.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c7c3d-147">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c7c3d-147">Issue resolution</span></span>

<span data-ttu-id="c7c3d-148">Lehel **Mobiilse seadme menüükäsud** seadistage iga müügitellimuse või üleviimistellimuse töötlemiseks seadistatud menüükäsu kohta suvand **Luba tükeldamine** FasTab-is **Üldine** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="c7c3d-149">Kuidas ma saan muuta varude olekut osalise töökoguse kohta?</span><span class="sxs-lookup"><span data-stu-id="c7c3d-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="c7c3d-150">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c7c3d-150">Issue description</span></span>

<span data-ttu-id="c7c3d-151">Soovite teha varude oleku muutust partii osaliseks koguseks.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c7c3d-152">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c7c3d-152">Issue resolution</span></span>

<span data-ttu-id="c7c3d-153">Selleks, et võimaldada töötajatel seda muudatust teha, saate luua menüü-üksuse lao mobiilirakendusele Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-153">To enable workers to make this change, you can create a menu item for the Warehouse Management mobile app.</span></span> <span data-ttu-id="c7c3d-154">**Mobiilse seadme menüü-üksused** lehel looge (või redigeerige) menüü-üksus, millel on järgnevad seaded:</span><span class="sxs-lookup"><span data-stu-id="c7c3d-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="c7c3d-155">**Režiim:** *töö*</span><span class="sxs-lookup"><span data-stu-id="c7c3d-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="c7c3d-156">**Kasuta olemasolevat tööd:** *Ei*</span><span class="sxs-lookup"><span data-stu-id="c7c3d-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="c7c3d-157">**Töö loomise protsess:** *Liigutamine*</span><span class="sxs-lookup"><span data-stu-id="c7c3d-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="c7c3d-158">**Kuva varude olek:** *Jah*</span><span class="sxs-lookup"><span data-stu-id="c7c3d-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="c7c3d-159">Vajadusel saate seadistada lehel muid välju.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="c7c3d-160">Asukohaprofiili laadimissildade halduse profiil ei takista varude tüüpide segamist.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c7c3d-161">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c7c3d-161">Issue description</span></span>

<span data-ttu-id="c7c3d-162">Kasutate *saadetise konsolideerimispoliitikaid*.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="c7c3d-163">Olete seadistanud *asukohaprofiili* jaoks *laadimissildade halduse profiili*, kuid töö loomisel segatakse varude tüübid lõppasukohas.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c7c3d-164">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="c7c3d-164">Issue resolution</span></span>

<span data-ttu-id="c7c3d-165">Laadimissildade halduse profiilid nõuavad töö eelnevat tükeldamist.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="c7c3d-166">Teisisõnu eeldab laadimissildade halduse profiil, et tööpäises pole mitut asetamise kohta.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="c7c3d-167">Selleks, et laadimissildade halduse profiil saaks varude segamist tõhusalt hallata, tuleb seadistada tööpäise piir.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="c7c3d-168">Selles näites on meie laadimissildade halduse profiil konfigureeritud nii, et **Varude tüübid, mida ei tohiks segada** on määratud olekusse *Saadetise ID*, ja me seadistame selle jaoks tööpäise piiri:</span><span class="sxs-lookup"><span data-stu-id="c7c3d-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="c7c3d-169">Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="c7c3d-170">Redigeerimiseks valige **Töökäsu tüüp** (nt *Ostutellimused*).</span><span class="sxs-lookup"><span data-stu-id="c7c3d-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="c7c3d-171">Valige redigeeritav töömall.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="c7c3d-172">Valige Toimingupaanil nupp **Päringu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="c7c3d-173">Avage vahekaart **Sortimine** ja lisage rida järgmiste sätetega.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="c7c3d-174">**Tabel** - *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="c7c3d-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="c7c3d-175">**Tuletatud tabel** - *Ajutised töökanded*</span><span class="sxs-lookup"><span data-stu-id="c7c3d-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="c7c3d-176">**Väli** - *Saadetise ID*</span><span class="sxs-lookup"><span data-stu-id="c7c3d-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="c7c3d-177">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-177">Select **OK**.</span></span>
1. <span data-ttu-id="c7c3d-178">Naasete lehele **Töömallid**.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="c7c3d-179">Valige toimingupaanilt suvand **Tööpäise piirid**.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="c7c3d-180">Valige Toimingupaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="c7c3d-181">Märkige ruut, mis on seotud **Välja nimi** *Saadetise ID-ga*.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="c7c3d-182">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c7c3d-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
