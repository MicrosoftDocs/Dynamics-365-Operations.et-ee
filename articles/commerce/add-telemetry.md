---
title: Telemeetria toetamiseks saidile skriptikoodi lisamine
description: Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761245"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="eaf52-103">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="eaf52-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eaf52-104">Selles teemas kirjeldatakse saidi lehtedele kliendipoolse skriptikoodi lisamist, et toetada kliendipoolset telemeetriat.</span><span class="sxs-lookup"><span data-stu-id="eaf52-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="eaf52-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="eaf52-105">Overview</span></span>

<span data-ttu-id="eaf52-106">Veebianalüüs on oluline tööriist, kui soovite mõista, kuidas kliendid teie saidiga suhtlevad, ja teha otsuseid, mis aitavad maksimaalse teisenduse kogemust optimeerida.</span><span class="sxs-lookup"><span data-stu-id="eaf52-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="eaf52-107">Saadaval on palju veebianalüüsi pakette, et aidata teid nende eesmärkide saavutamisel, nagu Google Analytics, Clicky, Moz Analytics ja KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="eaf52-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="eaf52-108">Enamik veebianalüüsi pakette nõuavad, et lisaksite oma saidi kõikidele lehtedele HTML-i elemendis **\<head\>** kliendipoolse skriptikoodi.</span><span class="sxs-lookup"><span data-stu-id="eaf52-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="eaf52-109">Selle teema juhised rakenduvad ka teistele kohandatud kliendipoolsetele funktsioonidele, mida Microsoft Dynamics 365 Commerce ei paku.</span><span class="sxs-lookup"><span data-stu-id="eaf52-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="eaf52-110">Skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="eaf52-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="eaf52-111">Fragment võimaldab teil taaskasutada tekstisisest või välist skripti koodi saidi kõigil lehtedel, olenemata kasutatavast mallist.</span><span class="sxs-lookup"><span data-stu-id="eaf52-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="eaf52-112">Tekstisisese skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="eaf52-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="eaf52-113">Saidiehitajas taaskasutatava fragmendi loomiseks tekstisisese skriptikoodi jaoks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="eaf52-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eaf52-114">Avage **Fragmendid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="eaf52-115">Valige dialoogiboksis **Uus fragment** suvand **Tekstisisene skript**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="eaf52-116">Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="eaf52-117">Valige loodud fragmendi jaotises moodul **Tekstisisene vaikeskript**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="eaf52-118">Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript.</span><span class="sxs-lookup"><span data-stu-id="eaf52-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="eaf52-119">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="eaf52-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="eaf52-120">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eaf52-121">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="eaf52-122">Tekstivälise skriptikoodi jaoks taaskasutatava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="eaf52-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="eaf52-123">Saidiehitajas taaskasutatava fragmendi loomiseks tekstivälise skriptikoodi jaoks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="eaf52-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eaf52-124">Avage **Fragmendid** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="eaf52-125">Valige dialoogiboksis **Uus fragment** suvand **Väline skript**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="eaf52-126">Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="eaf52-127">Valige loodud fragmendi jaotises moodul **Tekstiväline vaikeskript**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="eaf52-128">Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL.</span><span class="sxs-lookup"><span data-stu-id="eaf52-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="eaf52-129">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="eaf52-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="eaf52-130">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eaf52-131">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-131">Select **Publish**.</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="eaf52-132">Lisage fragment, mis sisaldab malli skriptikoodi</span><span class="sxs-lookup"><span data-stu-id="eaf52-132">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="eaf52-133">Saidiehitajas malli skriptikoodi sisaldava fragmendi lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="eaf52-133">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eaf52-134">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="eaf52-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="eaf52-135">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="eaf52-136">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="eaf52-137">Valige fragment, mille lõite oma skriptikoodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="eaf52-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="eaf52-138">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eaf52-139">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="eaf52-140">Tekstivälise või -sisese skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="eaf52-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="eaf52-141">Kui soovite sisestada tekstisisese või -välise skripti otse ühe malli juhitavasse lehtede komplekti, ei pea te esmalt fragmenti looma.</span><span class="sxs-lookup"><span data-stu-id="eaf52-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="eaf52-142">Tekstisisese skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="eaf52-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="eaf52-143">Saidiehitajas tekstisisese skripti otse malli lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="eaf52-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eaf52-144">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="eaf52-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="eaf52-145">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="eaf52-146">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="eaf52-147">Dialoogiboksis **Lisa moodul** valige **Tekstisisene skript**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="eaf52-148">Sisestage parempoolsel atribuudi paanil jaotises **Tekstisisene skript** oma kliendipoolne skript.</span><span class="sxs-lookup"><span data-stu-id="eaf52-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="eaf52-149">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="eaf52-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="eaf52-150">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eaf52-151">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="eaf52-152">Tekstvälise skripti lisamine otse malli</span><span class="sxs-lookup"><span data-stu-id="eaf52-152">Add an external script directly to a template</span></span>

<span data-ttu-id="eaf52-153">Saidiehitajas tekstivälise skripti otse malli lisamiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="eaf52-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="eaf52-154">Avage **Mallid** ja avage lehtede mall, millele soovite oma skriptikoodi lisada.</span><span class="sxs-lookup"><span data-stu-id="eaf52-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="eaf52-155">Laiendage vasakpoolsel paanil malli hierarhiat, et kuvada pesa **HTML-i pea**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="eaf52-156">Valige pesa **HTML-i päis** jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="eaf52-157">Dialoogiboksis **Lisa moodul** valige **Tekstiväline skript**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="eaf52-158">Lisage parempoolsel atribuudipaani jaotises **Skripti allikas** välise skripti allika väline või suhteline URL.</span><span class="sxs-lookup"><span data-stu-id="eaf52-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="eaf52-159">Seejärel konfigureerige teised suvandid vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="eaf52-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="eaf52-160">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="eaf52-161">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="eaf52-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eaf52-162">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="eaf52-162">Additional resources</span></span>

[<span data-ttu-id="eaf52-163">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="eaf52-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="eaf52-164">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="eaf52-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="eaf52-165">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="eaf52-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="eaf52-166">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="eaf52-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="eaf52-167">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="eaf52-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="eaf52-168">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="eaf52-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="eaf52-169">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="eaf52-169">Add languages to your site</span></span>](add-languages-to-site.md)
