---
title: Telemeetria toetamiseks saidile skriptikoodi lisamine
description: Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797427"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="4626a-103">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="4626a-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4626a-104">Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.</span><span class="sxs-lookup"><span data-stu-id="4626a-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="4626a-105">Veebianalüüs on oluline tööriist, kui soovite mõista, kuidas kliendid teie saidiga suhtlevad, ja teha otsuseid, mis aitavad maksimaalse teisenduse kogemust optimeerida.</span><span class="sxs-lookup"><span data-stu-id="4626a-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="4626a-106">Saadaval on palju veebianalüüsi pakette, et aidata teid nende eesmärkide saavutamisel, nagu Google Analytics, Clicky, Moz Analytics ja KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="4626a-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="4626a-107">Enamik veebianalüüsi pakette nõuavad, et lisaksite oma saidi kõikidele lehtedele HTML-i elemendis **\<head\>** kliendipoolse skriptikoodi.</span><span class="sxs-lookup"><span data-stu-id="4626a-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="4626a-108">Selle teema juhised rakenduvad ka teistele kohandatud kliendipoolsetele funktsioonidele, mida Microsoft Microsoft Dynamics 365 Commerce ei paku.</span><span class="sxs-lookup"><span data-stu-id="4626a-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="4626a-109">Skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="4626a-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="4626a-110">Fragment võimaldab teil taaskasutada tekstisisest või välist skripti koodi saidi kõigil lehtedel, olenemata kasutatavast mallist.</span><span class="sxs-lookup"><span data-stu-id="4626a-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="4626a-111">Tekstisisese skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="4626a-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="4626a-112">Saidiehitajas taaskasutatava fragmendi loomiseks tekstisisese skriptikoodi jaoks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="4626a-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4626a-113">Avage **Fragmendid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="4626a-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="4626a-114">Valige dialoogiboksis **Uus fragment** suvand **Tekstisisene skript**.</span><span class="sxs-lookup"><span data-stu-id="4626a-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="4626a-115">Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="4626a-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="4626a-116">Valige loodud fragmendi jaotises moodul **Tekstisisene vaikeskript**.</span><span class="sxs-lookup"><span data-stu-id="4626a-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="4626a-117">Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript.</span><span class="sxs-lookup"><span data-stu-id="4626a-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="4626a-118">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="4626a-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="4626a-119">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4626a-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4626a-120">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="4626a-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="4626a-121">Tekstivälise skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="4626a-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="4626a-122">Saidiehitajas taaskasutatava fragmendi loomiseks tekstivälise skriptikoodi jaoks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="4626a-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4626a-123">Avage **Fragmendid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="4626a-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="4626a-124">Valige dialoogiboksis **Uus fragment** suvand **Väline skript**.</span><span class="sxs-lookup"><span data-stu-id="4626a-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="4626a-125">Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="4626a-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="4626a-126">Valige loodud fragmendi jaotises moodul **Tekstiväline vaikeskript**.</span><span class="sxs-lookup"><span data-stu-id="4626a-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="4626a-127">Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL.</span><span class="sxs-lookup"><span data-stu-id="4626a-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="4626a-128">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="4626a-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="4626a-129">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4626a-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4626a-130">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="4626a-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="4626a-131">Kui sisu turbepoliitika (CSP) on teie saidi jaoks lubatud, veenduge, et kõik välised URL-id oleksid lisatud rakenduse Commerce saidiehitajas CSP direktiivi **script-src**.</span><span class="sxs-lookup"><span data-stu-id="4626a-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="4626a-132">Lisateavet leiate teemast [Sisu turbepoliitika (CSP) haldamine](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="4626a-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="4626a-133">Lisage fragment, mis sisaldab malli skriptikoodi</span><span class="sxs-lookup"><span data-stu-id="4626a-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="4626a-134">Saidiehitajas malli skriptikoodi sisaldava fragmendi lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="4626a-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4626a-135">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="4626a-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="4626a-136">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="4626a-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="4626a-137">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="4626a-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="4626a-138">Valige fragment, mille lõite oma skriptikoodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="4626a-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="4626a-139">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4626a-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4626a-140">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="4626a-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="4626a-141">Tekstivälise või -sisese skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="4626a-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="4626a-142">Kui soovite sisestada tekstisisese või -välise skripti otse ühe malli juhitavasse lehtede komplekti, ei pea te esmalt fragmenti looma.</span><span class="sxs-lookup"><span data-stu-id="4626a-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="4626a-143">Tekstisisese skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="4626a-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="4626a-144">Saidiehitajas tekstisisese skripti otse malli lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="4626a-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4626a-145">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="4626a-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="4626a-146">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="4626a-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="4626a-147">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="4626a-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4626a-148">Dialoogiboksis **Lisa moodul** valige **Tekstisisene skript**.</span><span class="sxs-lookup"><span data-stu-id="4626a-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="4626a-149">Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript.</span><span class="sxs-lookup"><span data-stu-id="4626a-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="4626a-150">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="4626a-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="4626a-151">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4626a-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4626a-152">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="4626a-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="4626a-153">Tekstvälise skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="4626a-153">Add an external script directly to a template</span></span>

<span data-ttu-id="4626a-154">Saidiehitajas tekstivälise skripti otse malli lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="4626a-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="4626a-155">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="4626a-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="4626a-156">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="4626a-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="4626a-157">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="4626a-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="4626a-158">Dialoogiboksis **Lisa moodul** valige **Tekstiväline skript**.</span><span class="sxs-lookup"><span data-stu-id="4626a-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="4626a-159">Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL.</span><span class="sxs-lookup"><span data-stu-id="4626a-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="4626a-160">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="4626a-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="4626a-161">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4626a-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4626a-162">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="4626a-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4626a-163">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4626a-163">Additional resources</span></span>

[<span data-ttu-id="4626a-164">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="4626a-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="4626a-165">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="4626a-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="4626a-166">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="4626a-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="4626a-167">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="4626a-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="4626a-168">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="4626a-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="4626a-169">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="4626a-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="4626a-170">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="4626a-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
