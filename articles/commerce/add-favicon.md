---
title: Faviconi lisamine
description: See teema selgitab, kuidas lisada saidile faviconi.
author: bicyclingfool
manager: annbe
ms.date: 04/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 198927e3391bdb577ebc845ff41d49ca798251ff
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686786"
---
# <a name="add-a-favicon"></a><span data-ttu-id="17665-103">Faviconi lisamine</span><span class="sxs-lookup"><span data-stu-id="17665-103">Add a favicon</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="17665-104">See teema selgitab, kuidas lisada saidile faviconi.</span><span class="sxs-lookup"><span data-stu-id="17665-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="17665-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="17665-105">Overview</span></span>

<span data-ttu-id="17665-106">Favicon on väike graafika fail, mis kuvatakse muu hulgas veebibrauseri vahekaardil, aadressiribal, sirvimisajaloos ja järjehoidjates või lemmikutes.</span><span class="sxs-lookup"><span data-stu-id="17665-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="17665-107">Soovitame lisada saidile faviconi, kuna see esindab ja tugevdab teie kaubamärki ja aitab eristada teie saiti teistest saitidest, mida teie kliendid külastavad.</span><span class="sxs-lookup"><span data-stu-id="17665-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="17665-108">Kuigi saate lisada oma saidile erineva suuruse ja failitüübiga favicone, näitab see teema, kuidas lisata ühte faviconi.</span><span class="sxs-lookup"><span data-stu-id="17665-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="17665-109">Samas kasutatakse sama protsessi ja asukohta rohkemate faviconide lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="17665-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="17665-110">Faviconi üleslaadimine saidi varade kollektsiooni</span><span class="sxs-lookup"><span data-stu-id="17665-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="17665-111">Faviconi saidi varade kollektsiooni üleslaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="17665-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="17665-112">Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="17665-112">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="17665-113">Valige tegumiriba käsk **Laadi üles \> Laadi üles meediumiüksused**.</span><span class="sxs-lookup"><span data-stu-id="17665-113">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="17665-114">Tuvastage File Exploreri aknas faviconi pildifail, mille soovite üles laadida, valige see ning seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="17665-114">In the File Explorer window, browse to the favicon image file that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="17665-115">Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** nõutav pealkiri ja alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="17665-115">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="17665-116">Pildi avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.</span><span class="sxs-lookup"><span data-stu-id="17665-116">If you want to publish the image immediately after upload, select the **Publish media items after upload** check box.</span></span>

    > [!NOTE]
    > <span data-ttu-id="17665-117">Kui te ei märgista ruutu **Avalda meediumiüksused pärast üleslaadimist**, peate naasma lehele **Meediumiüksused** ja avaldama faviconi hiljem käsitsi.</span><span class="sxs-lookup"><span data-stu-id="17665-117">If you don't select the **Publish media items after upload** check box, you must return to **Media items** page and manually publish the favicon later.</span></span>

1. <span data-ttu-id="17665-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="17665-118">Select **OK**.</span></span>
1. <span data-ttu-id="17665-119">Parempoolsel atribuudipaanil kopeerige faviconi avalik URL-i.</span><span class="sxs-lookup"><span data-stu-id="17665-119">In the property pane on the right, copy the public URL of the favicon.</span></span> <span data-ttu-id="17665-120">Seda URL-i kasutate hiljem.</span><span class="sxs-lookup"><span data-stu-id="17665-120">You will use this URL later.</span></span>

## <a name="create-the-html-for-your-favicon"></a><span data-ttu-id="17665-121">Faviconi jaoks HTML-i loomine</span><span class="sxs-lookup"><span data-stu-id="17665-121">Create the HTML for your favicon</span></span>

<span data-ttu-id="17665-122">Faviconi HTML-i loomiseks kasutage järgmist HTML-stringi.</span><span class="sxs-lookup"><span data-stu-id="17665-122">To create the HTML for the favicon, use the following HTML string.</span></span> <span data-ttu-id="17665-123">Atribuudi **href** jaoks asendage **Avalik\_URL\_teie\_faviconi\_jaoks** avaliku URL-iga, mille varem kopeerisite.</span><span class="sxs-lookup"><span data-stu-id="17665-123">For the **href** attribute, replace **Public\_URL\_for\_your\_favicon** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-page-fragment-that-contains-a-metatag-for-your-favicon"></a><span data-ttu-id="17665-124">Looge lehefragment, mis sisaldab teie faviconi metasilti</span><span class="sxs-lookup"><span data-stu-id="17665-124">Create a page fragment that contains a metatag for your favicon</span></span>

<span data-ttu-id="17665-125">Teie faviconi sisaldava lehefragmendi loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="17665-125">To create a page fragment that contains a metatag for your favicon, follow these steps.</span></span>

1. <span data-ttu-id="17665-126">Avage **Fragmendid** ja valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="17665-126">Go to **Fragments**, and select **New**.</span></span>
1. <span data-ttu-id="17665-127">Valige dialoogiboksis **Uus lehe fragment** lehefragmendi aluseks oleva moodulina **Metasildid**.</span><span class="sxs-lookup"><span data-stu-id="17665-127">In the **New page fragment** dialog box, select **Metatags** as the module that the page fragment is based on.</span></span>
1. <span data-ttu-id="17665-128">Sisestage lehefragmendi nimi ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="17665-128">Enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="17665-129">Valige fragmendihierarhiapuus tütarüksus**Vaikimisi metasildid**.</span><span class="sxs-lookup"><span data-stu-id="17665-129">In the fragment hierarchy tree, select the **Default metatags** child.</span></span>
1. <span data-ttu-id="17665-130">Valige parempoolsel paanil jaotises **Metasildid** suvand **Lisa** ja seejärel sisestage HTML-string, mille eelnevalt faviconi jaoks lõite.</span><span class="sxs-lookup"><span data-stu-id="17665-130">In the right pane, under **Meta Tags**, select **Add**, and then enter the HTML string that you created earlier for the favicon.</span></span> 
1. <span data-ttu-id="17665-131">Valige **Lõpeta redigeerimine** ja seejärel valige lehefragmendi avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="17665-131">Select **Finish editing**, and then select **Publish** to publish the page fragment.</span></span>

## <a name="add-the-metatag-page-fragment-to-the-html-head-section-of-your-pages"></a><span data-ttu-id="17665-132">Lisage metasildi lehefragment oma lehtede HTML-i päise jaotisesse</span><span class="sxs-lookup"><span data-stu-id="17665-132">Add the metatag page fragment to the HTML head section of your pages</span></span>

<span data-ttu-id="17665-133">Metasildi lehefragmendi lisamiseks oma lehtede HTML-i **päise** jaotisesse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="17665-133">To add the metatag page fragment to the HTML **head** section of your pages, follow these steps.</span></span>

1. <span data-ttu-id="17665-134">Avage **Mallid**, avage lehtede mall, mille soovite oma faviconile lisada ja valige seejärel **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="17665-134">Go to **Templates**, open the template for the pages that you want to add your favicon to, and then select **Edit**.</span></span>
1. <span data-ttu-id="17665-135">Vajutage mallihierarhiapuus kolmikpunkti (**...**) nupule, mis paikneb konteineri **HTML-i päis** paremal küljel, ja valige seejärel **Lisa lehefragment**.</span><span class="sxs-lookup"><span data-stu-id="17665-135">In the template hierarchy tree, select the ellipsis (**...**) button to the right of the **HTML head** container, and then select **Add page fragment**.</span></span>
1. <span data-ttu-id="17665-136">Valige dialoogiboksis**Lehe fragmendi valimine** varem loodud metasildi lehefragment ja seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="17665-136">In the **Select page fragment** dialog box, select the metatag page fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="17665-137">Valige **Lõpeta redigeerimine** ja seejärel valige malli avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="17665-137">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>

> [!NOTE]
> <span data-ttu-id="17665-138">Kui teie saidil kasutatakse enam kui üht malli, siis peate kõigile lisama metasiltide lehefragmendi.</span><span class="sxs-lookup"><span data-stu-id="17665-138">If your site uses more than one template, you must add the metatags page fragment to all of them.</span></span>

<span data-ttu-id="17665-139">Kui kuvate selliste lehtede eelvaate, mis põhinevad mallil, millele lisasite metasiltide lehefragmendi, siis peaksite nüüd nägema brauseriaknas faviconi.</span><span class="sxs-lookup"><span data-stu-id="17665-139">When you preview pages that are based on the template that you added the metatags page fragment to, you should now see the favicon on the browser tab.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17665-140">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="17665-140">Additional resources</span></span>

[<span data-ttu-id="17665-141">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="17665-141">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="17665-142">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="17665-142">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="17665-143">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="17665-143">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="17665-144">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="17665-144">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="17665-145">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="17665-145">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="17665-146">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="17665-146">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="17665-147">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="17665-147">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

