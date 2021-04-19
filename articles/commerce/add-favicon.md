---
title: Faviconi lisamine
description: See teema selgitab, kuidas lisada saidile faviconi.
author: bicyclingfool
ms.date: 08/31/2020
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
ms.openlocfilehash: 9268bc74a4131256f5a2e88df833104db271b56a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797715"
---
# <a name="add-a-favicon"></a><span data-ttu-id="82efa-103">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="82efa-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="82efa-104">See teema selgitab, kuidas lisada saidile faviconi.</span><span class="sxs-lookup"><span data-stu-id="82efa-104">This topic explains how to add a favicon to your site.</span></span>

<span data-ttu-id="82efa-105">Favicon on väike graafika fail, mis kuvatakse muu hulgas veebibrauseri vahekaardil, aadressiribal, sirvimisajaloos ja järjehoidjates või lemmikutes.</span><span class="sxs-lookup"><span data-stu-id="82efa-105">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="82efa-106">Soovitame lisada saidile faviconi, kuna see esindab ja tugevdab teie kaubamärki ja aitab eristada teie saiti teistest saitidest, mida teie kliendid külastavad.</span><span class="sxs-lookup"><span data-stu-id="82efa-106">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="82efa-107">Kuigi saate lisada oma saidile erineva suuruse ja failitüübiga favicone, näitab see teema, kuidas lisata ühte faviconi.</span><span class="sxs-lookup"><span data-stu-id="82efa-107">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="82efa-108">Samas kasutatakse sama protsessi ja asukohta rohkemate faviconide lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="82efa-108">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="82efa-109">Faviconi üleslaadimine saidi varade kollektsiooni</span><span class="sxs-lookup"><span data-stu-id="82efa-109">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="82efa-110">Faviconi saidi varade kollektsiooni üleslaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="82efa-110">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="82efa-111">Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="82efa-111">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="82efa-112">Valige tegumiriba käsk **Laadi üles \> Laadi üles meediumiüksused**.</span><span class="sxs-lookup"><span data-stu-id="82efa-112">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="82efa-113">Tuvastage File Exploreri aknas faviconi pildifail, mille soovite üles laadida, valige see ning seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="82efa-113">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="82efa-114">Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** nõutav pealkiri ja alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="82efa-114">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="82efa-115">Pildi avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.</span><span class="sxs-lookup"><span data-stu-id="82efa-115">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="82efa-116">Kui te ei märgista ruutu **Avalda meediumiüksused pärast üleslaadimist**, peate naasma lehele **Meediumiüksused** ja avaldama faviconi hiljem käsitsi.</span><span class="sxs-lookup"><span data-stu-id="82efa-116">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="82efa-117">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="82efa-117">Select **OK**.</span></span>
1. <span data-ttu-id="82efa-118">Parempoolsel atribuudipaanil kopeerige faviconi avalik URL-i.</span><span class="sxs-lookup"><span data-stu-id="82efa-118">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="82efa-119">Seda URL-i kasutate hiljem.</span><span class="sxs-lookup"><span data-stu-id="82efa-119">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="82efa-120">Faviconi jaoks HTML-i loomine</span><span class="sxs-lookup"><span data-stu-id="82efa-120">Create the HTML for your favicon</span></span>

<span data-ttu-id="82efa-121">Faviconi HTML-i loomiseks kasutage järgmist HTML-stringi.</span><span class="sxs-lookup"><span data-stu-id="82efa-121">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="82efa-122">Atribuudi **href** jaoks asendage **Avalik\_URL\_teie\_faviconi\_jaoks** avaliku URL-iga, mille varem kopeerisite.</span><span class="sxs-lookup"><span data-stu-id="82efa-122">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="82efa-123">Teie lemmikuikooni metasilti sisaldava fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="82efa-123">Create a fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="82efa-124">Teie lemmikuikooni metasilti sisaldava fragmendi loomiseks järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="82efa-124">To create a fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="82efa-125">Avage **Fragmendid** ja valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="82efa-125">Go to **Fragments**, and select **New**.</span></span>
1. <span data-ttu-id="82efa-126">Määrake dialoogiboksis **Uus fragment** mooduliks (millel põhineb fragment) **Metasildid**.</span><span class="sxs-lookup"><span data-stu-id="82efa-126">In the **New fragment** dialog box, select **Metatags** as the module that the fragment is based on.</span></span>
1. <span data-ttu-id="82efa-127">Sisestage fragmendi nimi ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="82efa-127">Enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="82efa-128">Valige fragmendihierarhiapuus tütarüksus **Vaikimisi metasildid**.</span><span class="sxs-lookup"><span data-stu-id="82efa-128">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="82efa-129">Valige parempoolsel paanil jaotises **Metasildid** suvand **Lisa** ja seejärel sisestage HTML-string, mille eelnevalt faviconi jaoks lõite.</span><span class="sxs-lookup"><span data-stu-id="82efa-129">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="82efa-130">Valige **Lõpeta redigeerimine** ja seejärel valige fragmendi avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="82efa-130">Select **Finish editing**, and then select **Publish** to publish the fragment.</span></span>

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="82efa-131">Metasildi fragmendi lisamine lehtede HTML-i päise jaotisse</span><span class="sxs-lookup"><span data-stu-id="82efa-131">Add the metatag fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="82efa-132">Metasildi fragmendi lisamiseks lehtede HTML-i **päise** jaotisse järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="82efa-132">To add the metatag fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="82efa-133">Avage **Mallid**, avage lehtede mall, mille soovite oma faviconile lisada ja valige seejärel **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="82efa-133">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="82efa-134">Valige malli hierarhiapuus ümbrisest **HTML-i päis** paremal asuv kolmikpunkti (**...**) nupp ja seejärel valige **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="82efa-134">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add fragment**.</span></span>
1. <span data-ttu-id="82efa-135">Valige dialoogiboksis **Vali fragment** varem loodud metasildi fragment ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="82efa-135">In the **Select fragment** dialog box, select the metatag fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="82efa-136">Valige **Lõpeta redigeerimine** ja seejärel valige malli avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="82efa-136">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="82efa-137">Kui teie sait kasutab rohkem kui ühte malli, peate metasiltide fragmendi lisama kõigile mallidele.</span><span class="sxs-lookup"><span data-stu-id="82efa-137">If your site uses more than one template, you must add the metatags fragment to all of them.</span></span>

<span data-ttu-id="82efa-138">Kui vaatate nende lehtede eelversiooni, mis põhinevad mallil, millele lisasite metasiltide fragmendi, peaksite nüüd nägema lemmikuikooni brauseri vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="82efa-138">When you preview pages that are based on the template that you added the metatags fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82efa-139">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="82efa-139">Additional resources</span></span>

[<span data-ttu-id="82efa-140">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="82efa-140">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="82efa-141">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="82efa-141">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="82efa-142">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="82efa-142">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="82efa-143">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="82efa-143">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="82efa-144">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="82efa-144">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="82efa-145">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="82efa-145">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="82efa-146">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="82efa-146">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
