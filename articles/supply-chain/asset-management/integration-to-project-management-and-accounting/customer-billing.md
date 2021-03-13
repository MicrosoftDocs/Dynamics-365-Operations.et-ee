---
title: Kliendile kuuluvate varade hooldamise arve
description: Selles teemas selgitatakse, kuidas luua, töödelda ja esitada arve hooldustöö eest, mis tehakse varadele, mis kuuluvad teie klientidele.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131837"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="9a20d-103">Kliendile kuuluvate varade hooldamise arve</span><span class="sxs-lookup"><span data-stu-id="9a20d-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a20d-104">Funktsioon *Töökäsu arveldamine* võimaldab teil luua, töödelda ja esitada arve hooldustöö eest, mis tehakse teie klientidele kuuluvatele varadele.</span><span class="sxs-lookup"><span data-stu-id="9a20d-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="9a20d-105">See funktsioon võimaldab teil teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="9a20d-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="9a20d-106">Sidus kliendid neile kuuluvate varadega.</span><span class="sxs-lookup"><span data-stu-id="9a20d-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="9a20d-107">Töökäsku luues valida kliendi ja vaadata varasid, mida klient omab.</span><span class="sxs-lookup"><span data-stu-id="9a20d-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="9a20d-108">Häälestada iga kliendi jaoks ülemprojekt.</span><span class="sxs-lookup"><span data-stu-id="9a20d-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="9a20d-109">Registreerida töökäsu tunde, üksusi, kulusid ja tasusid ning luua seejärel hiljem kliendile arvesoovitus.</span><span class="sxs-lookup"><span data-stu-id="9a20d-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="9a20d-110">Lisaks omab see funktsioon järgmisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="9a20d-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="9a20d-111">Kliendi ülemprojekti projektileping kopeeritakse automaatselt asjaomasesse töökäsu projekti.</span><span class="sxs-lookup"><span data-stu-id="9a20d-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="9a20d-112">Varahaldus saab nüüd kasutada *tasuta* projekti kandetüüpi nii töökäsu prognooside kui ka töökäsu töölehtede jaoks.</span><span class="sxs-lookup"><span data-stu-id="9a20d-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="9a20d-113">Kliendi arveldusfunktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="9a20d-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="9a20d-114">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="9a20d-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="9a20d-115">Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="9a20d-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="9a20d-116">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="9a20d-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="9a20d-117">**Moodul:** *Projektihaldus ja raamatupidamine*</span><span class="sxs-lookup"><span data-stu-id="9a20d-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="9a20d-118">**Funktsiooni nimi:** *Töökäsu arveldamine*</span><span class="sxs-lookup"><span data-stu-id="9a20d-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="9a20d-119">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="9a20d-119">Example scenario</span></span>

<span data-ttu-id="9a20d-120">Et teada saada, kuidas see funktsioon töötab, töötage läbi järgmise näite stsenaarium.</span><span class="sxs-lookup"><span data-stu-id="9a20d-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="9a20d-121">Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="9a20d-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="9a20d-122">Enne alustamist peate valima **USMF-i** juriidilise isiku.</span><span class="sxs-lookup"><span data-stu-id="9a20d-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="9a20d-123">Seda stsenaariumi saate kasutada ka juhistena funktsiooni kasutamiseks, kui töötate tootmissüsteemis.</span><span class="sxs-lookup"><span data-stu-id="9a20d-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="9a20d-124">Kuid sellisel juhul peate asendama oma väärtused ja teil ei pruugi olla teatud tüüpi nõutavaid kirjeid, mida pakuvad standardsed demoandmed.</span><span class="sxs-lookup"><span data-stu-id="9a20d-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="9a20d-125">1. etapp: kliendi jaoks uue projektilepingu loomine</span><span class="sxs-lookup"><span data-stu-id="9a20d-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="9a20d-126">Avage **Projektihaldus ja raamatupidamine \> Projektid \> Projektilepingud**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="9a20d-127">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9a20d-128">Dialoogiboksis **Uus projektileping** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9a20d-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9a20d-129">**Nimi:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="9a20d-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="9a20d-130">**Rahastamise tüüp:** *klient*</span><span class="sxs-lookup"><span data-stu-id="9a20d-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="9a20d-131">**Rahastamisallikas:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="9a20d-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="9a20d-132">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="9a20d-133">2. etapp: kliendi jaoks uue ülemprojekti loomine</span><span class="sxs-lookup"><span data-stu-id="9a20d-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="9a20d-134">Siin loodud ülemprojekti kasutatakse kliendi töökäskude loomisel.</span><span class="sxs-lookup"><span data-stu-id="9a20d-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="9a20d-135">Avage **Projektihaldus ja raamatupidamine \> Projektid \> Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="9a20d-136">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9a20d-137">Dialoogiboksis **Uus projekt** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9a20d-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9a20d-138">**Projekti tüüp:** *aeg ja materjal*</span><span class="sxs-lookup"><span data-stu-id="9a20d-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="9a20d-139">**Projekti nimi:** *Pelican Wholesalesi töökäsud*</span><span class="sxs-lookup"><span data-stu-id="9a20d-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="9a20d-140">**Projekti rühm:** *TM*</span><span class="sxs-lookup"><span data-stu-id="9a20d-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="9a20d-141">**Projektilepingu ID:** *Pelican Wholesales* (varem loodud leping)</span><span class="sxs-lookup"><span data-stu-id="9a20d-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="9a20d-142">**Alguskuupäev:** valige tänane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="9a20d-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="9a20d-143">Valige **Loo projekt**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-143">Select **Create project**.</span></span>
1. <span data-ttu-id="9a20d-144">Uus projekt avatakse.</span><span class="sxs-lookup"><span data-stu-id="9a20d-144">The new project is opened.</span></span> <span data-ttu-id="9a20d-145">Märkige üles suvandi **Projekti ID** väärtus.</span><span class="sxs-lookup"><span data-stu-id="9a20d-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="9a20d-146">Peate selle hiljem sisestama.</span><span class="sxs-lookup"><span data-stu-id="9a20d-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="9a20d-147">3. etapp: varahalduses uue töökäsu tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="9a20d-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="9a20d-148">Avage **Varahaldus \> Seadistus \> Töökäsk \> Töökäsu tüübid**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="9a20d-149">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9a20d-150">Uus kirje lisatakse loendisse.</span><span class="sxs-lookup"><span data-stu-id="9a20d-150">A new record is added to the list.</span></span> <span data-ttu-id="9a20d-151">Seadke selle jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9a20d-151">Set the following values for it:</span></span>

    - <span data-ttu-id="9a20d-152">**Töökäsu tüüp:** *teenus*</span><span class="sxs-lookup"><span data-stu-id="9a20d-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="9a20d-153">**Nimi:** *Teenuse töökäsud*</span><span class="sxs-lookup"><span data-stu-id="9a20d-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="9a20d-154">**Töökäsu töötsükli olek:** *standardne*</span><span class="sxs-lookup"><span data-stu-id="9a20d-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="9a20d-155">4. etapp: kliendikonto sidumine üleprojektiga</span><span class="sxs-lookup"><span data-stu-id="9a20d-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="9a20d-156">Peate nüüd varahalduses projekti seadistamises siduma kliendikonto ülemprojektiga.</span><span class="sxs-lookup"><span data-stu-id="9a20d-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="9a20d-157">Avage **Varahaldus \> Seadistamine \> Töökäsud \> Projekti seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="9a20d-158">Valige vahekaardil **Ülemprojekt** suvand **Lisa**, et lisada rida.</span><span class="sxs-lookup"><span data-stu-id="9a20d-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="9a20d-159">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9a20d-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9a20d-160">**Kliendikonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="9a20d-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="9a20d-161">**Projekti ID:** sisestage projekti ID, mille olete varem üles märkinud.</span><span class="sxs-lookup"><span data-stu-id="9a20d-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="9a20d-162">5. etapp: projektirühma ja tüübi töökäsu projektiga sidumine</span><span class="sxs-lookup"><span data-stu-id="9a20d-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="9a20d-163">Peate olema endiselt lehel **Projekti seadistamine** (**Varahaldus \> Seadistamine \> Töökäsud \> Projekti häälestamine**).</span><span class="sxs-lookup"><span data-stu-id="9a20d-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="9a20d-164">Valige vahekaardil **Projektirühm** suvand **Lisa**, et lisada rida.</span><span class="sxs-lookup"><span data-stu-id="9a20d-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="9a20d-165">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9a20d-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="9a20d-166">**Töötellimuse tüüp:** *teenus* (varem loodud töökäsu tüüp)</span><span class="sxs-lookup"><span data-stu-id="9a20d-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="9a20d-167">**Projekti rühm:** *TM*</span><span class="sxs-lookup"><span data-stu-id="9a20d-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="9a20d-168">Töökäsu projekti leping päritakse alati ülemprojektilt.</span><span class="sxs-lookup"><span data-stu-id="9a20d-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="9a20d-169">6. etapp: siduge vara kliendi ID-ga</span><span class="sxs-lookup"><span data-stu-id="9a20d-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="9a20d-170">Avage **Varahaldus \> Varad \> Aktiivsed varad**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="9a20d-171">Väljal **Filter** sisestage väärtus *VE-102* ja valige filtrimisaluseks **Vara**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="9a20d-172">Valig selle seadistuste avamiseks vara.</span><span class="sxs-lookup"><span data-stu-id="9a20d-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="9a20d-173">Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-013* (*Pelican Wholesales*).</span><span class="sxs-lookup"><span data-stu-id="9a20d-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="9a20d-174">Väli **Nimi** värskendatakse automaatselt väärtusele *Pelican Wholesales*.</span><span class="sxs-lookup"><span data-stu-id="9a20d-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="9a20d-175">7. etapp: vara uue töökäsu tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="9a20d-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="9a20d-176">Avage **Varahaldus \> Töökäsud \> Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="9a20d-177">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="9a20d-178">Dialoogiboksis **Töökäsu loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="9a20d-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="9a20d-179">**Töökäsu tüüp:** *teenus*</span><span class="sxs-lookup"><span data-stu-id="9a20d-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="9a20d-180">**Kirjeldus:** *auto remontimine*</span><span class="sxs-lookup"><span data-stu-id="9a20d-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="9a20d-181">**Kliendikonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="9a20d-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="9a20d-182">**Vara:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="9a20d-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="9a20d-183">Otsing näitab ainult valitud kliendikontoga seotud varasid.</span><span class="sxs-lookup"><span data-stu-id="9a20d-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="9a20d-184">**Hooldustöö tüüp:** *remont*</span><span class="sxs-lookup"><span data-stu-id="9a20d-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="9a20d-185">**Valdkond:** *mehaanika*</span><span class="sxs-lookup"><span data-stu-id="9a20d-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="9a20d-186">**Teenuse tase:** *4*</span><span class="sxs-lookup"><span data-stu-id="9a20d-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="9a20d-187">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="9a20d-188">8. etapp: töötellimuse läbivaatamine ja selle kallal töötamine</span><span class="sxs-lookup"><span data-stu-id="9a20d-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="9a20d-189">Selles jaotises töötate eelmises jaotses loodud töökäsu kallal.</span><span class="sxs-lookup"><span data-stu-id="9a20d-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="9a20d-190">Järgige järgmisi samme, et veenduda, kas ülemprojekt on *Pelican Wholesalesi töökäsk*.</span><span class="sxs-lookup"><span data-stu-id="9a20d-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="9a20d-191">Valige jaotises **Töökäsu hooldustööd** rida.</span><span class="sxs-lookup"><span data-stu-id="9a20d-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="9a20d-192">Kiirkaardil **Rea üksikasjad** kontrollige väärtust **Projekti ID**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="9a20d-193">See peaks olema sidekriipsuga number kujul *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="9a20d-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="9a20d-194">See väärtus on link.</span><span class="sxs-lookup"><span data-stu-id="9a20d-194">This value is a link.</span></span>
    1. <span data-ttu-id="9a20d-195">Valige projekti ID link, et avada lehekülg, kus saate vaadata ülemprojekti ja projekti nimesid.</span><span class="sxs-lookup"><span data-stu-id="9a20d-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="9a20d-196">Tegumiriba vahekaardi **Töökäsk** rühmas **Töötsükli olek** valige **Värskenda töökäsu olekut**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="9a20d-197">Dialoogiboksis **Töökäsu oleku värskendamine** veerus **Valimine** valige märkeruut rea jaoks, kus väli **Töötsükli olek** on määratud valikule *Pooleli*.</span><span class="sxs-lookup"><span data-stu-id="9a20d-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="9a20d-198">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-198">Select **OK**.</span></span>
1. <span data-ttu-id="9a20d-199">Dialoogiboksis **Töötsükli olek: pooleli** valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="9a20d-200">9. etapp: sisestage töökäsule kulunud tunnid ja looge uus arve soovitus</span><span class="sxs-lookup"><span data-stu-id="9a20d-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="9a20d-201">Selles jaotises jätkate töötamist töökäsuga, mille kallal eelmises jaotises töötasite.</span><span class="sxs-lookup"><span data-stu-id="9a20d-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="9a20d-202">Toimingupaani vahekaardi **Töökäsk** grupis **Projekt** valige suvand **Töölehed**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="9a20d-203">Kuvatakse leht **Töökäsu töölehed**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="9a20d-204">Siin saate registreerida töökäsule kulutatud aja.</span><span class="sxs-lookup"><span data-stu-id="9a20d-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="9a20d-205">Valige kiirkaardil **Tunnid** suvand **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="9a20d-206">Uuel real seadke määrake välja **Tunnid** väärtuseks *4*.</span><span class="sxs-lookup"><span data-stu-id="9a20d-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="9a20d-207">Tehke toimingupaanil valik **Sisesta töölehed**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="9a20d-208">Sulgege leht **Töökäsu töölehed**, et töökäsku naasta.</span><span class="sxs-lookup"><span data-stu-id="9a20d-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="9a20d-209">Toimingupaanil vahekaardil **Arveldamine** valige suvand **Uus arve soovitus**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="9a20d-210">Dialoogiboksis **Arve soovituse loomine** jaotises **Projektitehingud** valige märkeruut **Valimine** iga rea jaoks, mille kohta arve soovite esitada.</span><span class="sxs-lookup"><span data-stu-id="9a20d-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="9a20d-211">Dialoogiboksi sulgemiseks ja uue arve soovituse vaatamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a20d-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>
