---
title: Telemeetria toetamiseks saidile skriptikoodi lisamine
description: Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686810"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="fa3a5-103">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa3a5-104">Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="fa3a5-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="fa3a5-105">Overview</span></span>

<span data-ttu-id="fa3a5-106">Veebianalüüs on oluline tööriist, kui soovite mõista, kuidas kliendid teie saidiga suhtlevad, ja teha otsuseid, mis aitavad maksimaalse teisenduse kogemust optimeerida.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="fa3a5-107">Saadaval on palju veebianalüüsi pakette, et aidata teid nende eesmärkide saavutamisel, nagu Google Analytics, Clicky, Moz Analytics ja KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="fa3a5-108">Enamik veebianalüüsi pakette nõuavad, et lisaksite oma saidi kõikidele lehtedele HTML-i elemendis **\<head\>** kliendipoolse skriptikoodi.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="fa3a5-109">Selle teema juhised rakenduvad ka teistele kohandatud kliendipoolsetele funktsioonidele, mida Microsoft Dynamics 365 Commerce ei paku.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="fa3a5-110">Skriptikoodi jaoks taaskasutatava lehe loomine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="fa3a5-111">Lehe fragment võimaldab teil taaskasutada tekstisisest või välist skripti koodi saidi kõigil lehtedel, olenemata kasutatavast mallist.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="fa3a5-112">Tekstisisese skriptikoodi jaoks taaskasutatava lehe loomine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="fa3a5-113">Saidiehitajas taaskasutatava lehe fragmendi loomiseks tekstisisese skriptikoodi jaoks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fa3a5-114">Avage **Fragmendid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="fa3a5-115">Valige dialoogiboksis **Uus lehe fragment** suvand **Tekstisisene skript**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-115">In the **New page fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="fa3a5-116">Sisestage jaotises **Lehe fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-116">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="fa3a5-117">Valige loodud lehe fragmendi jaotises moodul **Tekstisisene vaikeskript**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="fa3a5-118">Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="fa3a5-119">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="fa3a5-120">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fa3a5-121">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="fa3a5-122">Tekstivälise skriptikoodi jaoks taaskasutatava lehe loomine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="fa3a5-123">Saidiehitajas taaskasutatava lehe fragmendi loomiseks tekstivälise skriptikoodi jaoks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fa3a5-124">Avage **Fragmendid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="fa3a5-125">Valige dialoogiboksis **Uus lehe fragment** suvand **Väline skript**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-125">In the **New page fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="fa3a5-126">Sisestage jaotises **Lehe fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-126">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="fa3a5-127">Valige loodud lehe fragmendi jaotises moodul **Tekstiväline vaikeskript**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="fa3a5-128">Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="fa3a5-129">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="fa3a5-130">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fa3a5-131">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="fa3a5-132">Lisage lehe fragment, mis sisaldab malli skriptikoodi</span><span class="sxs-lookup"><span data-stu-id="fa3a5-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="fa3a5-133">Saidiehitajas malli skriptikoodi sisaldava lehe fragmendi lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fa3a5-134">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="fa3a5-135">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="fa3a5-136">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa lehe fragment**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="fa3a5-137">Valige fragment, mille lõite oma skriptikoodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="fa3a5-138">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fa3a5-139">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="fa3a5-140">Tekstivälise või -sisese skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="fa3a5-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="fa3a5-141">Kui soovite sisestada tekstisisese või -välise skripti otse ühe malli juhitavasse lehtede komplekti, ei pea te esmalt lehe fragmenti looma.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="fa3a5-142">Tekstisisese skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="fa3a5-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="fa3a5-143">Saidiehitajas tekstisisese skripti otse malli lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fa3a5-144">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="fa3a5-145">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="fa3a5-146">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fa3a5-147">Dialoogiboksis **Lisa moodul** valige **Tekstisisene skript**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="fa3a5-148">Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="fa3a5-149">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="fa3a5-150">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fa3a5-151">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="fa3a5-152">Tekstvälise skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="fa3a5-152">Add an external script directly to a template</span></span>

<span data-ttu-id="fa3a5-153">Saidiehitajas tekstivälise skripti otse malli lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="fa3a5-154">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="fa3a5-155">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="fa3a5-156">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="fa3a5-157">Dialoogiboksis **Lisa moodul** valige **Tekstiväline skript**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="fa3a5-158">Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="fa3a5-159">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="fa3a5-160">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="fa3a5-161">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="fa3a5-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa3a5-162">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fa3a5-162">Additional resources</span></span>

[<span data-ttu-id="fa3a5-163">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="fa3a5-164">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="fa3a5-165">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="fa3a5-166">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="fa3a5-167">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="fa3a5-168">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="fa3a5-169">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="fa3a5-169">Add languages to your site</span></span>](add-languages-to-site.md)
