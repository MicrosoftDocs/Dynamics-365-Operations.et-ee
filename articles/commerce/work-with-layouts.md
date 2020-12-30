---
title: Eelmääratud paigutustega töötamine
description: Selles teemas kirjeldatakse, kuidas töötada eelmääratud paigutustega rakenduses Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f31dfa1fdbb3732610748abe4a9de851033f2b89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411692"
---
# <a name="work-with-preset-layouts"></a><span data-ttu-id="fca41-103">Eelmääratud paigutustega töötamine</span><span class="sxs-lookup"><span data-stu-id="fca41-103">Work with preset layouts</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fca41-104">Selles teemas kirjeldatakse, kuidas töötada eelmääratud paigutustega rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fca41-104">This topic describes how to work with preset layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fca41-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="fca41-105">Overview</span></span>

<span data-ttu-id="fca41-106">Enne selle teema protseduuride läbimist lugege kindlasti teemat [Eelseadistatud ja kohandatud paigutused](templates-layouts-overview.md#preset-and-custom-layouts).</span><span class="sxs-lookup"><span data-stu-id="fca41-106">Before you complete the procedures in this topic, be sure to read [Preset and custom layouts](templates-layouts-overview.md#preset-and-custom-layouts).</span></span> <span data-ttu-id="fca41-107">Üldise ülevaate saamiseks vt teemat [Mallide ja paigutuste ülevaade](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fca41-107">For a general overview, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="create-a-new-preset-layout"></a><span data-ttu-id="fca41-108">Uue eelmääratud paigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="fca41-108">Create a new preset layout</span></span>

<span data-ttu-id="fca41-109">Eelmääratud paigutuse loomiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="fca41-109">There are two methods for creating a preset layout.</span></span> <span data-ttu-id="fca41-110">Võite salvestada olemasoleva kohandatud paigutuse uue eelmääratud paigutusena või luua nullist eelmääratud paigutuse.</span><span class="sxs-lookup"><span data-stu-id="fca41-110">You can save an existing custom layout as a new preset layout, or you can create a preset layout from scratch.</span></span>

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a><span data-ttu-id="fca41-111">Eelmääratud paigutuse loomine olemasolevast kohandatud paigutusest</span><span class="sxs-lookup"><span data-stu-id="fca41-111">Create a preset layout from an existing custom layout</span></span>

<span data-ttu-id="fca41-112">Eelmääratud paigutuse loomiseks olemasolevast kohandatud paigutusest tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="fca41-112">To create a preset layout from an existing custom layout, follow these steps.</span></span>

1. <span data-ttu-id="fca41-113">Avage olemasolev leht, mis ei kasuta praegu eelmääratud paigutust ja millel on mooduli struktuur, mida soovite oma saidi teistel lehtedel uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="fca41-113">Open an existing page that doesn't currently use a preset layout, and that has a module structure that you want to reuse for other pages on your site.</span></span>
1. <span data-ttu-id="fca41-114">Lehe vaatamiseks valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="fca41-114">Select **Edit** to check out the page.</span></span>
1. <span data-ttu-id="fca41-115">Valige suvand **Salvesta uue paigutusena**.</span><span class="sxs-lookup"><span data-stu-id="fca41-115">Select **Save as new layout**.</span></span> <span data-ttu-id="fca41-116">Ilmub dialoogiboks **Salvesta uue paigutusena**.</span><span class="sxs-lookup"><span data-stu-id="fca41-116">The **Save as new layout** dialog box appears.</span></span>
1. <span data-ttu-id="fca41-117">Sisestage eelmääratud paigutuse nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="fca41-117">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="fca41-118">Sisestatud väärtused kuvatakse teistele autoritele, kui nad loovad teie paigutusest uusi lehti või lähevad sellele üle.</span><span class="sxs-lookup"><span data-stu-id="fca41-118">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="fca41-119">Seega sisestage väärtused, mis on kasulikud teistele lehe autoritele.</span><span class="sxs-lookup"><span data-stu-id="fca41-119">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="fca41-120">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="fca41-120">Select **OK**.</span></span>

<span data-ttu-id="fca41-121">Eelmääratud paigutus on nüüd saadaval, kui loote uued lehed või valite lehele samas malli hierarhias teise paigutuse.</span><span class="sxs-lookup"><span data-stu-id="fca41-121">The preset layout will now be available when you create new pages or select a different layout for a page in the same template hierarchy.</span></span>

> [!TIP]
> <span data-ttu-id="fca41-122">Selleks et kiiresti näha, kas konkreetne leht on parasjagu seotud eelmääratud paigutusega, valige lehtede loendi vaatest leht ja kontrollige paigutuse metaandmeid paremal atribuutide paanil.</span><span class="sxs-lookup"><span data-stu-id="fca41-122">To quickly see whether a specific page is currently bound to a preset layout, select the page in the pages list view, and inspect the layout metadata in the property pane on the right.</span></span>

### <a name="create-a-new-preset-layout"></a><span data-ttu-id="fca41-123">Uue eelmääratud paigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="fca41-123">Create a new preset layout</span></span>

<span data-ttu-id="fca41-124">Eelmääratud paigutuse loomiseks nullist tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="fca41-124">To create a preset layout from scratch, follow these steps.</span></span>

1. <span data-ttu-id="fca41-125">Valige navigeerimispaanilt vasakult suvand **Paigutused**.</span><span class="sxs-lookup"><span data-stu-id="fca41-125">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="fca41-126">Valige suvand **Uus paigutus**.</span><span class="sxs-lookup"><span data-stu-id="fca41-126">Select **New Layout**.</span></span> <span data-ttu-id="fca41-127">Ilmub dialoogiboks **Uus paigutus**.</span><span class="sxs-lookup"><span data-stu-id="fca41-127">The **New layout** dialog box appears.</span></span>
1. <span data-ttu-id="fca41-128">Valige eelmääratud paigutuse jaoks kasutatav mall.</span><span class="sxs-lookup"><span data-stu-id="fca41-128">Select the template to use for your preset layout.</span></span>
1. <span data-ttu-id="fca41-129">Sisestage eelmääratud paigutuse nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="fca41-129">Enter a name and description for your preset layout.</span></span> <span data-ttu-id="fca41-130">Sisestatud väärtused kuvatakse teistele autoritele, kui nad loovad teie paigutusest uusi lehti või lähevad sellele üle.</span><span class="sxs-lookup"><span data-stu-id="fca41-130">The values that you enter will be shown to other authors when they create new pages from your layout or switch to it.</span></span> <span data-ttu-id="fca41-131">Seega sisestage väärtused, mis on kasulikud teistele lehe autoritele.</span><span class="sxs-lookup"><span data-stu-id="fca41-131">Therefore, enter values that will be useful to page authors.</span></span>
1. <span data-ttu-id="fca41-132">Valige nupp **OK**, et luua uus eelmääratud paigutus ja avada paigutuse redaktor.</span><span class="sxs-lookup"><span data-stu-id="fca41-132">Select **OK** to create the new preset layout and open the layout editor.</span></span>
1. <span data-ttu-id="fca41-133">Paigutuse redaktoris lisa ja konfigureerige mooduleid, kasutades liigendpuud vasakul ja atribuutide paani paremal.</span><span class="sxs-lookup"><span data-stu-id="fca41-133">In the layout editor, add and configure modules by using the outline tree on the left and the property pane on the right.</span></span> <span data-ttu-id="fca41-134">(See protsess meenutab malli moodulite lisamist ja konfigureerimist malli redaktoris.) Moodulite asetus ja lukustatud vaikesätted muutuvad mooduli keskseks konfiguratsiooniks lehtedel, mis kasutavad seda eelmääratud paigutust.</span><span class="sxs-lookup"><span data-stu-id="fca41-134">(The process resembles the process for adding and configuring modules for a template in the template editor.) The arrangement of modules and any locked default settings become the centralized module configuration for any pages that use this preset layout.</span></span>

## <a name="modify-a-preset-layout"></a><span data-ttu-id="fca41-135">Eelmääratud paigutuse muutmine</span><span class="sxs-lookup"><span data-stu-id="fca41-135">Modify a preset layout</span></span>

<span data-ttu-id="fca41-136">Eelmääratud paigutuse muutmiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="fca41-136">To modify a preset layout, follow these steps.</span></span>

1. <span data-ttu-id="fca41-137">Valige navigeerimispaanilt vasakult suvand **Paigutused**.</span><span class="sxs-lookup"><span data-stu-id="fca41-137">In the navigation pane on the left, select **Layouts**.</span></span>
1. <span data-ttu-id="fca41-138">Valige paigutuse redaktorist vasakult liigendpuust moodul, mida soovite muuta.</span><span class="sxs-lookup"><span data-stu-id="fca41-138">In the layout editor, in the outline tree on the left, select the module to modify.</span></span> <span data-ttu-id="fca41-139">Seejärel järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="fca41-139">Then follow any of these steps:</span></span>

    - <span data-ttu-id="fca41-140">Mooduli liigutamiseks ülema sees üles või alla valige mooduli kolmikpunkti nupp (**...**) ja seejärel käsk **Nihuta üles** või **Nihuta alla**.</span><span class="sxs-lookup"><span data-stu-id="fca41-140">To move a module up or down inside its parent, select the ellipsis button (**...**) for the module, and then select **Move up** or **Move down**.</span></span>
    - <span data-ttu-id="fca41-141">Mooduli vaikesätete muutmiseks kasutage atribuutide paani, et sisestada vaikeväärtused, ja lukustage need valikuliselt kõikide järgmiste lehtede jaoks.</span><span class="sxs-lookup"><span data-stu-id="fca41-141">To change a module's default settings, use the property pane to enter default values and optionally lock them for all downstream pages.</span></span>
    - <span data-ttu-id="fca41-142">Uute moodulite või fragmentide lisamiseks konteineri moodulitesse valige kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul** või **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="fca41-142">To add new modules or fragments to container modules, select the ellipsis button, and then select **Add module** or **Add fragment**.</span></span>
    - <span data-ttu-id="fca41-143">Mooduli eemaldamiseks paigutuselt valige kolmikpunkti nupp ja seejärel valige käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="fca41-143">To remove a module from the layout, select the ellipsis button, and then select **Delete**.</span></span>

## <a name="change-a-preset-layout-theme"></a><span data-ttu-id="fca41-144">Eelmääratud paigutuse kujunduse muutmine</span><span class="sxs-lookup"><span data-stu-id="fca41-144">Change a preset layout theme</span></span>

<span data-ttu-id="fca41-145">Tavaline on seadistada kõikidele eelmääratud paigutust kasutavatele lehtedele vaikekujundus.</span><span class="sxs-lookup"><span data-stu-id="fca41-145">A typical practice is to set a default theme for all pages that use a preset layout.</span></span>

<span data-ttu-id="fca41-146">Kujunduse määramiseks või muutmiseks kõikidele alamlehtedele, mis kasutavad teie eelmääratud paigutust, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="fca41-146">To set or change the theme for all child pages that use your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="fca41-147">Valige paigutuse redaktorist vasakult liigendpuust lehe konteineri moodul.</span><span class="sxs-lookup"><span data-stu-id="fca41-147">In the layout editor, in the outline tree on the left, select the page container module.</span></span> <span data-ttu-id="fca41-148">(Tavaliselt on see moodul teine sõlm ja kannab nime **Vaikeleht**.)</span><span class="sxs-lookup"><span data-stu-id="fca41-148">(Typically, this module is the second node and is named **Default page**.)</span></span>
1. <span data-ttu-id="fca41-149">Valige kujundus paremalt atribuutide paanilt väljast **Kujundus**.</span><span class="sxs-lookup"><span data-stu-id="fca41-149">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a><span data-ttu-id="fca41-150">Eelmääratud paigutuse salvestamine, registreerimine, eelvaatamine ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="fca41-150">Save, check in, preview, and publish a preset layout</span></span>

<span data-ttu-id="fca41-151">Eelmääratud paigutuse salvestamiseks ja kontrollimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="fca41-151">To save and check in your preset layout, follow these steps.</span></span>

1. <span data-ttu-id="fca41-152">Valige paigutuse redaktorist ülevalt suvand **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fca41-152">Select **Save** at the top of the layout editor.</span></span> <span data-ttu-id="fca41-153">Salvestatud muudatused ei mõjuta järgmisi lehti, kuni need registreeritakse.</span><span class="sxs-lookup"><span data-stu-id="fca41-153">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="fca41-154">Valige **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="fca41-154">Select **Finish editing**.</span></span> <span data-ttu-id="fca41-155">Teie muudatused on nüüd leitavad järgmiste töövoogude jaoks.</span><span class="sxs-lookup"><span data-stu-id="fca41-155">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="fca41-156">Muudatuste eelvaatamiseks avage olemasolev leht, mis kasutab eelmääratud paigutust, või looge paigutusest uus leht.</span><span class="sxs-lookup"><span data-stu-id="fca41-156">To preview your changes, either open an existing page that uses the preset layout or create a new page from the layout.</span></span>

<span data-ttu-id="fca41-157">Pärast eelmääratud paigutuse muudatuste vaatamist järgige üht alltoodud etappidest paigutuse avaldamiseks reaalajas saidil.</span><span class="sxs-lookup"><span data-stu-id="fca41-157">After you've previewed the changes to your preset layout, follow one of these steps to publish the layout to your live site:</span></span>

* <span data-ttu-id="fca41-158">Valige suvand **Paigutused**, valige paigutus ja seejärel käsk **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fca41-158">Go to **Layouts**, select the layout, and then select **Publish**.</span></span>
* <span data-ttu-id="fca41-159">Valige paigutuse redaktori avamiseks paigutuse nimi ja seejärel **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fca41-159">Select the layout name to open the layout editor, and then select **Publish**.</span></span>
* <span data-ttu-id="fca41-160">Avaldage leht, mis viitab avaldamata paigutusele.</span><span class="sxs-lookup"><span data-stu-id="fca41-160">Publish a page that references the unpublished layout.</span></span> <span data-ttu-id="fca41-161">Paigutus avaldatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="fca41-161">The layout will automatically be published.</span></span>

> [!WARNING]
> <span data-ttu-id="fca41-162">Eelmääratud paigutustele saab viidata mitmelt lehelt.</span><span class="sxs-lookup"><span data-stu-id="fca41-162">Preset layouts can be referenced by multiple pages.</span></span> <span data-ttu-id="fca41-163">Kui avaldate eelmääratud paigutuse, pange tähele, et see võib mõjutada mitme lehe paigutust.</span><span class="sxs-lookup"><span data-stu-id="fca41-163">When you publish a preset layout, be aware that you might affect the layout of multiple pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fca41-164">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fca41-164">Additional resources</span></span>

[<span data-ttu-id="fca41-165">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="fca41-165">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="fca41-166">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="fca41-166">Work with templates</span></span>](work-with-templates.md)
