---
title: Telemeetria toetamiseks saidile skriptikoodi lisamine
description: Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e035c767474cba19c3a31eafdefb08b422b564ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209199"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="c8ba1-103">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c8ba1-104">Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="c8ba1-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="c8ba1-105">Overview</span></span>

<span data-ttu-id="c8ba1-106">Veebianalüüs on oluline tööriist, kui soovite mõista, kuidas kliendid teie saidiga suhtlevad, ja teha otsuseid, mis aitavad maksimaalse teisenduse kogemust optimeerida.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="c8ba1-107">Saadaval on palju veebianalüüsi pakette, et aidata teid nende eesmärkide saavutamisel, nagu Google Analytics, Clicky, Moz Analytics ja KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="c8ba1-108">Enamik veebianalüüsi pakette nõuavad, et lisaksite oma saidi kõikidele lehtedele HTML-i elemendis **\<head\>** kliendipoolse skriptikoodi.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="c8ba1-109">Selle teema juhised rakenduvad ka teistele kohandatud kliendipoolsetele funktsioonidele, mida Microsoft Microsoft Dynamics 365 Commerce ei paku.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="c8ba1-110">Skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="c8ba1-111">Fragment võimaldab teil taaskasutada tekstisisest või välist skripti koodi saidi kõigil lehtedel, olenemata kasutatavast mallist.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="c8ba1-112">Tekstisisese skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="c8ba1-113">Saidiehitajas taaskasutatava fragmendi loomiseks tekstisisese skriptikoodi jaoks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c8ba1-114">Avage **Fragmendid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="c8ba1-115">Valige dialoogiboksis **Uus fragment** suvand **Tekstisisene skript**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="c8ba1-116">Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c8ba1-117">Valige loodud fragmendi jaotises moodul **Tekstisisene vaikeskript**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="c8ba1-118">Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="c8ba1-119">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c8ba1-120">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c8ba1-121">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="c8ba1-122">Tekstivälise skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="c8ba1-123">Saidiehitajas taaskasutatava fragmendi loomiseks tekstivälise skriptikoodi jaoks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c8ba1-124">Avage **Fragmendid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="c8ba1-125">Valige dialoogiboksis **Uus fragment** suvand **Väline skript**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="c8ba1-126">Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c8ba1-127">Valige loodud fragmendi jaotises moodul **Tekstiväline vaikeskript**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="c8ba1-128">Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="c8ba1-129">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c8ba1-130">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c8ba1-131">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="c8ba1-132">Kui sisu turbepoliitika (CSP) on teie saidi jaoks lubatud, veenduge, et kõik välised URL-id oleksid lisatud rakenduse Commerce saidiehitajas CSP direktiivi **script-src**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="c8ba1-133">Lisateavet leiate teemast [Sisu turbepoliitika (CSP) haldamine](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="c8ba1-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="c8ba1-134">Lisage fragment, mis sisaldab malli skriptikoodi</span><span class="sxs-lookup"><span data-stu-id="c8ba1-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="c8ba1-135">Saidiehitajas malli skriptikoodi sisaldava fragmendi lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c8ba1-136">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="c8ba1-137">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="c8ba1-138">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="c8ba1-139">Valige fragment, mille lõite oma skriptikoodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="c8ba1-140">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c8ba1-141">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="c8ba1-142">Tekstivälise või -sisese skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="c8ba1-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="c8ba1-143">Kui soovite sisestada tekstisisese või -välise skripti otse ühe malli juhitavasse lehtede komplekti, ei pea te esmalt fragmenti looma.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="c8ba1-144">Tekstisisese skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="c8ba1-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="c8ba1-145">Saidiehitajas tekstisisese skripti otse malli lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c8ba1-146">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="c8ba1-147">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="c8ba1-148">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c8ba1-149">Dialoogiboksis **Lisa moodul** valige **Tekstisisene skript**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="c8ba1-150">Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="c8ba1-151">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c8ba1-152">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c8ba1-153">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="c8ba1-154">Tekstvälise skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="c8ba1-154">Add an external script directly to a template</span></span>

<span data-ttu-id="c8ba1-155">Saidiehitajas tekstivälise skripti otse malli lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c8ba1-156">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="c8ba1-157">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="c8ba1-158">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c8ba1-159">Dialoogiboksis **Lisa moodul** valige **Tekstiväline skript**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="c8ba1-160">Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="c8ba1-161">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c8ba1-162">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c8ba1-163">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c8ba1-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8ba1-164">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c8ba1-164">Additional resources</span></span>

[<span data-ttu-id="c8ba1-165">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="c8ba1-166">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="c8ba1-167">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="c8ba1-168">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="c8ba1-169">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="c8ba1-170">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="c8ba1-171">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="c8ba1-171">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]