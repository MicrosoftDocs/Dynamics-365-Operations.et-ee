---
title: Faviconi lisamine
description: See teema selgitab, kuidas lisada saidile faviconi.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001529"
---
# <a name="add-a-favicon"></a><span data-ttu-id="0c26a-103">Faviconi lisamine</span><span class="sxs-lookup"><span data-stu-id="0c26a-103">Add a favicon</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0c26a-104">See teema selgitab, kuidas lisada saidile faviconi.</span><span class="sxs-lookup"><span data-stu-id="0c26a-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="0c26a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="0c26a-105">Overview</span></span>

<span data-ttu-id="0c26a-106">Favicon on väike graafika fail, mis kuvatakse muu hulgas veebibrauseri vahekaardil, aadressiribal, sirvimisajaloos ja järjehoidjates või lemmikutes.</span><span class="sxs-lookup"><span data-stu-id="0c26a-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="0c26a-107">Soovitame lisada saidile faviconi, kuna see esindab ja tugevdab teie kaubamärki ja aitab eristada teie saiti teistest saitidest, mida teie kliendid külastavad.</span><span class="sxs-lookup"><span data-stu-id="0c26a-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="0c26a-108">Kuigi saate lisada oma saidile erineva suuruse ja failitüübiga favicone, näitab see teema, kuidas lisata ühte faviconi.</span><span class="sxs-lookup"><span data-stu-id="0c26a-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="0c26a-109">Samas kasutatakse sama protsessi ja asukohta rohkemate faviconide lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c26a-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="0c26a-110">Faviconi üleslaadimine saidi varade kollektsiooni</span><span class="sxs-lookup"><span data-stu-id="0c26a-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="0c26a-111">Faviconi saidi varade kollektsiooni üleslaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0c26a-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="0c26a-112">Avage **Varad \> Laadi üles \> Varade üleslaadimine**.</span><span class="sxs-lookup"><span data-stu-id="0c26a-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="0c26a-113">Leidke ja valige kohalikus failisüsteemis favicon.</span><span class="sxs-lookup"><span data-stu-id="0c26a-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="0c26a-114">Sisestage pealkiri ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c26a-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="0c26a-115">Parempoolsel atribuudipaanil kopeerige faviconi avalik URL-i.</span><span class="sxs-lookup"><span data-stu-id="0c26a-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="0c26a-116">Kui te suvandit **Avalda varad pärast üleslaadimist** ei vali, peate naasma lehele **Varad** ja avaldama faviconi hiljem käsitsi.</span><span class="sxs-lookup"><span data-stu-id="0c26a-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="0c26a-117">Faviconi HTML-i loomine</span><span class="sxs-lookup"><span data-stu-id="0c26a-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="0c26a-118">Faviconi HTML-i loomiseks kasutage järgmist HTML-i lõiku.</span><span class="sxs-lookup"><span data-stu-id="0c26a-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="0c26a-119">Atribuudi **href** jaoks asendage **"Avalik\_URL\_teie\_faviconi\_jaoks"** avaliku URL-iga, mille varem kopeerisite.</span><span class="sxs-lookup"><span data-stu-id="0c26a-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="0c26a-120">Lisage faviconi HTML oma lehtede elemendile \<head\>.</span><span class="sxs-lookup"><span data-stu-id="0c26a-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="0c26a-121">Oma saidile faviconi lisamiseks kasutage sama toimingut, mida kasutatakse mis tahes HTML-i või skripti lisamiseks saidi lehtede elemendile **\<head\>**.</span><span class="sxs-lookup"><span data-stu-id="0c26a-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c26a-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0c26a-122">Additional resources</span></span>

[<span data-ttu-id="0c26a-123">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="0c26a-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="0c26a-124">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="0c26a-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0c26a-125">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="0c26a-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0c26a-126">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="0c26a-126">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0c26a-127">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="0c26a-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0c26a-128">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="0c26a-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0c26a-129">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="0c26a-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

