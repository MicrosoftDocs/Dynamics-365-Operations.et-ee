---
title: Kliendile kuuluvate varade hooldamise arve
description: Selles teemas selgitatakse, kuidas luua, töödelda ja esitada arve hooldustöö eest, mis tehakse varadele, mis kuuluvad teie klientidele.
author: johanhoffmann
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjProjectsListPage, ProjTable, EntAssetWorkOrderType, EntAssetWorkOrderProjectSetup, EntAssetObjectTable, EntAssetWorkOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5532f1ce14239002022f487f227286efe10abf12
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813793"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="aa683-103">Kliendile kuuluvate varade hooldamise arve</span><span class="sxs-lookup"><span data-stu-id="aa683-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa683-104">Funktsioon *Töökäsu arveldamine* võimaldab teil luua, töödelda ja esitada arve hooldustöö eest, mis tehakse teie klientidele kuuluvatele varadele.</span><span class="sxs-lookup"><span data-stu-id="aa683-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="aa683-105">See funktsioon võimaldab teil teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="aa683-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="aa683-106">Sidus kliendid neile kuuluvate varadega.</span><span class="sxs-lookup"><span data-stu-id="aa683-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="aa683-107">Töökäsku luues valida kliendi ja vaadata varasid, mida klient omab.</span><span class="sxs-lookup"><span data-stu-id="aa683-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="aa683-108">Häälestada iga kliendi jaoks ülemprojekt.</span><span class="sxs-lookup"><span data-stu-id="aa683-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="aa683-109">Registreerida töökäsu tunde, üksusi, kulusid ja tasusid ning luua seejärel hiljem kliendile arvesoovitus.</span><span class="sxs-lookup"><span data-stu-id="aa683-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="aa683-110">Lisaks omab see funktsioon järgmisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="aa683-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="aa683-111">Kliendi ülemprojekti projektileping kopeeritakse automaatselt asjaomasesse töökäsu projekti.</span><span class="sxs-lookup"><span data-stu-id="aa683-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="aa683-112">Varahaldus saab nüüd kasutada *tasuta* projekti kandetüüpi nii töökäsu prognooside kui ka töökäsu töölehtede jaoks.</span><span class="sxs-lookup"><span data-stu-id="aa683-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="aa683-113">Kliendi arveldusfunktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="aa683-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="aa683-114">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="aa683-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="aa683-115">Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="aa683-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="aa683-116">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="aa683-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="aa683-117">**Moodul:** *Projektihaldus ja raamatupidamine*</span><span class="sxs-lookup"><span data-stu-id="aa683-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="aa683-118">**Funktsiooni nimi:** *Töökäsu arveldamine*</span><span class="sxs-lookup"><span data-stu-id="aa683-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="aa683-119">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="aa683-119">Example scenario</span></span>

<span data-ttu-id="aa683-120">Et teada saada, kuidas see funktsioon töötab, töötage läbi järgmise näite stsenaarium.</span><span class="sxs-lookup"><span data-stu-id="aa683-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="aa683-121">Selle stsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="aa683-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="aa683-122">Enne alustamist peate valima **USMF-i** juriidilise isiku.</span><span class="sxs-lookup"><span data-stu-id="aa683-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="aa683-123">Seda stsenaariumi saate kasutada ka juhistena funktsiooni kasutamiseks, kui töötate tootmissüsteemis.</span><span class="sxs-lookup"><span data-stu-id="aa683-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="aa683-124">Kuid sellisel juhul peate asendama oma väärtused ja teil ei pruugi olla teatud tüüpi nõutavaid kirjeid, mida pakuvad standardsed demoandmed.</span><span class="sxs-lookup"><span data-stu-id="aa683-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="aa683-125">1. etapp: kliendi jaoks uue projektilepingu loomine</span><span class="sxs-lookup"><span data-stu-id="aa683-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="aa683-126">Avage **Projektihaldus ja raamatupidamine \> Projektid \> Projektilepingud**.</span><span class="sxs-lookup"><span data-stu-id="aa683-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="aa683-127">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="aa683-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="aa683-128">Dialoogiboksis **Uus projektileping** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="aa683-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="aa683-129">**Nimi:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="aa683-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="aa683-130">**Rahastamise tüüp:** *klient*</span><span class="sxs-lookup"><span data-stu-id="aa683-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="aa683-131">**Rahastamisallikas:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="aa683-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="aa683-132">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa683-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="aa683-133">2. etapp: kliendi jaoks uue ülemprojekti loomine</span><span class="sxs-lookup"><span data-stu-id="aa683-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="aa683-134">Siin loodud ülemprojekti kasutatakse kliendi töökäskude loomisel.</span><span class="sxs-lookup"><span data-stu-id="aa683-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="aa683-135">Avage **Projektihaldus ja raamatupidamine \> Projektid \> Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="aa683-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="aa683-136">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="aa683-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="aa683-137">Dialoogiboksis **Uus projekt** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="aa683-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="aa683-138">**Projekti tüüp:** *aeg ja materjal*</span><span class="sxs-lookup"><span data-stu-id="aa683-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="aa683-139">**Projekti nimi:** *Pelican Wholesalesi töökäsud*</span><span class="sxs-lookup"><span data-stu-id="aa683-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="aa683-140">**Projekti rühm:** *TM*</span><span class="sxs-lookup"><span data-stu-id="aa683-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="aa683-141">**Projektilepingu ID:** *Pelican Wholesales* (varem loodud leping)</span><span class="sxs-lookup"><span data-stu-id="aa683-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="aa683-142">**Alguskuupäev:** valige tänane kuupäev.</span><span class="sxs-lookup"><span data-stu-id="aa683-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="aa683-143">Valige **Loo projekt**.</span><span class="sxs-lookup"><span data-stu-id="aa683-143">Select **Create project**.</span></span>
1. <span data-ttu-id="aa683-144">Uus projekt avatakse.</span><span class="sxs-lookup"><span data-stu-id="aa683-144">The new project is opened.</span></span> <span data-ttu-id="aa683-145">Märkige üles suvandi **Projekti ID** väärtus.</span><span class="sxs-lookup"><span data-stu-id="aa683-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="aa683-146">Peate selle hiljem sisestama.</span><span class="sxs-lookup"><span data-stu-id="aa683-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="aa683-147">3. etapp: varahalduses uue töökäsu tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="aa683-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="aa683-148">Avage **Varahaldus \> Seadistus \> Töökäsk \> Töökäsu tüübid**.</span><span class="sxs-lookup"><span data-stu-id="aa683-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="aa683-149">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="aa683-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="aa683-150">Uus kirje lisatakse loendisse.</span><span class="sxs-lookup"><span data-stu-id="aa683-150">A new record is added to the list.</span></span> <span data-ttu-id="aa683-151">Seadke selle jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="aa683-151">Set the following values for it:</span></span>

    - <span data-ttu-id="aa683-152">**Töökäsu tüüp:** *teenus*</span><span class="sxs-lookup"><span data-stu-id="aa683-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="aa683-153">**Nimi:** *Teenuse töökäsud*</span><span class="sxs-lookup"><span data-stu-id="aa683-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="aa683-154">**Töökäsu töötsükli olek:** *standardne*</span><span class="sxs-lookup"><span data-stu-id="aa683-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="aa683-155">4. etapp: kliendikonto sidumine üleprojektiga</span><span class="sxs-lookup"><span data-stu-id="aa683-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="aa683-156">Peate nüüd varahalduses projekti seadistamises siduma kliendikonto ülemprojektiga.</span><span class="sxs-lookup"><span data-stu-id="aa683-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="aa683-157">Avage **Varahaldus \> Seadistamine \> Töökäsud \> Projekti seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="aa683-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="aa683-158">Valige vahekaardil **Ülemprojekt** suvand **Lisa**, et lisada rida.</span><span class="sxs-lookup"><span data-stu-id="aa683-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="aa683-159">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="aa683-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="aa683-160">**Kliendikonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="aa683-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="aa683-161">**Projekti ID:** sisestage projekti ID, mille olete varem üles märkinud.</span><span class="sxs-lookup"><span data-stu-id="aa683-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="aa683-162">5. etapp: projektirühma ja tüübi töökäsu projektiga sidumine</span><span class="sxs-lookup"><span data-stu-id="aa683-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="aa683-163">Peate olema endiselt lehel **Projekti seadistamine** (**Varahaldus \> Seadistamine \> Töökäsud \> Projekti häälestamine**).</span><span class="sxs-lookup"><span data-stu-id="aa683-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="aa683-164">Valige vahekaardil **Projektirühm** suvand **Lisa**, et lisada rida.</span><span class="sxs-lookup"><span data-stu-id="aa683-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="aa683-165">Määrake uuel real järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="aa683-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="aa683-166">**Töötellimuse tüüp:** *teenus* (varem loodud töökäsu tüüp)</span><span class="sxs-lookup"><span data-stu-id="aa683-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="aa683-167">**Projekti rühm:** *TM*</span><span class="sxs-lookup"><span data-stu-id="aa683-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="aa683-168">Töökäsu projekti leping päritakse alati ülemprojektilt.</span><span class="sxs-lookup"><span data-stu-id="aa683-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="aa683-169">6. etapp: siduge vara kliendi ID-ga</span><span class="sxs-lookup"><span data-stu-id="aa683-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="aa683-170">Avage **Varahaldus \> Varad \> Aktiivsed varad**.</span><span class="sxs-lookup"><span data-stu-id="aa683-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="aa683-171">Väljal **Filter** sisestage väärtus *VE-102* ja valige filtrimisaluseks **Vara**.</span><span class="sxs-lookup"><span data-stu-id="aa683-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="aa683-172">Valig selle seadistuste avamiseks vara.</span><span class="sxs-lookup"><span data-stu-id="aa683-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="aa683-173">Määrake kiirkaardi **Klient** välja **Kliendi konto** väärtuseks *US-013* (*Pelican Wholesales*).</span><span class="sxs-lookup"><span data-stu-id="aa683-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="aa683-174">Väli **Nimi** värskendatakse automaatselt väärtusele *Pelican Wholesales*.</span><span class="sxs-lookup"><span data-stu-id="aa683-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="aa683-175">7. etapp: vara uue töökäsu tüübi loomine</span><span class="sxs-lookup"><span data-stu-id="aa683-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="aa683-176">Avage **Varahaldus \> Töökäsud \> Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="aa683-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="aa683-177">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="aa683-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="aa683-178">Dialoogiboksis **Töökäsu loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="aa683-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="aa683-179">**Töökäsu tüüp:** *teenus*</span><span class="sxs-lookup"><span data-stu-id="aa683-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="aa683-180">**Kirjeldus:** *auto remontimine*</span><span class="sxs-lookup"><span data-stu-id="aa683-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="aa683-181">**Kliendikonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="aa683-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="aa683-182">**Vara:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="aa683-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="aa683-183">Otsing näitab ainult valitud kliendikontoga seotud varasid.</span><span class="sxs-lookup"><span data-stu-id="aa683-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="aa683-184">**Hooldustöö tüüp:** *remont*</span><span class="sxs-lookup"><span data-stu-id="aa683-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="aa683-185">**Valdkond:** *mehaanika*</span><span class="sxs-lookup"><span data-stu-id="aa683-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="aa683-186">**Teenuse tase:** *4*</span><span class="sxs-lookup"><span data-stu-id="aa683-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="aa683-187">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa683-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="aa683-188">8. etapp: töötellimuse läbivaatamine ja selle kallal töötamine</span><span class="sxs-lookup"><span data-stu-id="aa683-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="aa683-189">Selles jaotises töötate eelmises jaotses loodud töökäsu kallal.</span><span class="sxs-lookup"><span data-stu-id="aa683-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="aa683-190">Järgige järgmisi samme, et veenduda, kas ülemprojekt on *Pelican Wholesalesi töökäsk*.</span><span class="sxs-lookup"><span data-stu-id="aa683-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="aa683-191">Valige jaotises **Töökäsu hooldustööd** rida.</span><span class="sxs-lookup"><span data-stu-id="aa683-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="aa683-192">Kiirkaardil **Rea üksikasjad** kontrollige väärtust **Projekti ID**.</span><span class="sxs-lookup"><span data-stu-id="aa683-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="aa683-193">See peaks olema sidekriipsuga number kujul *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="aa683-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="aa683-194">See väärtus on link.</span><span class="sxs-lookup"><span data-stu-id="aa683-194">This value is a link.</span></span>
    1. <span data-ttu-id="aa683-195">Valige projekti ID link, et avada lehekülg, kus saate vaadata ülemprojekti ja projekti nimesid.</span><span class="sxs-lookup"><span data-stu-id="aa683-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="aa683-196">Tegumiriba vahekaardi **Töökäsk** rühmas **Töötsükli olek** valige **Värskenda töökäsu olekut**.</span><span class="sxs-lookup"><span data-stu-id="aa683-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="aa683-197">Dialoogiboksis **Töökäsu oleku värskendamine** veerus **Valimine** valige märkeruut rea jaoks, kus väli **Töötsükli olek** on määratud valikule *Pooleli*.</span><span class="sxs-lookup"><span data-stu-id="aa683-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="aa683-198">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa683-198">Select **OK**.</span></span>
1. <span data-ttu-id="aa683-199">Dialoogiboksis **Töötsükli olek: pooleli** valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa683-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="aa683-200">9. etapp: sisestage töökäsule kulunud tunnid ja looge uus arve soovitus</span><span class="sxs-lookup"><span data-stu-id="aa683-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="aa683-201">Selles jaotises jätkate töötamist töökäsuga, mille kallal eelmises jaotises töötasite.</span><span class="sxs-lookup"><span data-stu-id="aa683-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="aa683-202">Toimingupaani vahekaardi **Töökäsk** grupis **Projekt** valige suvand **Töölehed**.</span><span class="sxs-lookup"><span data-stu-id="aa683-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="aa683-203">Kuvatakse leht **Töökäsu töölehed**.</span><span class="sxs-lookup"><span data-stu-id="aa683-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="aa683-204">Siin saate registreerida töökäsule kulutatud aja.</span><span class="sxs-lookup"><span data-stu-id="aa683-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="aa683-205">Valige kiirkaardil **Tunnid** suvand **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="aa683-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="aa683-206">Uuel real seadke määrake välja **Tunnid** väärtuseks *4*.</span><span class="sxs-lookup"><span data-stu-id="aa683-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="aa683-207">Tehke toimingupaanil valik **Sisesta töölehed**.</span><span class="sxs-lookup"><span data-stu-id="aa683-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="aa683-208">Sulgege leht **Töökäsu töölehed**, et töökäsku naasta.</span><span class="sxs-lookup"><span data-stu-id="aa683-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="aa683-209">Toimingupaanil vahekaardil **Arveldamine** valige suvand **Uus arve soovitus**.</span><span class="sxs-lookup"><span data-stu-id="aa683-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="aa683-210">Dialoogiboksis **Arve soovituse loomine** jaotises **Projektitehingud** valige märkeruut **Valimine** iga rea jaoks, mille kohta arve soovite esitada.</span><span class="sxs-lookup"><span data-stu-id="aa683-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="aa683-211">Dialoogiboksi sulgemiseks ja uue arve soovituse vaatamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa683-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]