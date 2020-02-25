---
title: Logo lisamine
description: Selles teemas kirjeldatakse, kuidas lisada logo rakenduses Microsoft Dynamics 365 Commerce oma saidile.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5fc0673dcdcc8b761089be2c2d201c8488128865
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025686"
---
# <a name="add-a-logo"></a><span data-ttu-id="e4227-103">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="e4227-103">Add a logo</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e4227-104">Selles teemas kirjeldatakse, kuidas lisada logo rakenduses Microsoft Dynamics 365 Commerce oma saidile.</span><span class="sxs-lookup"><span data-stu-id="e4227-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e4227-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e4227-105">Overview</span></span>

<span data-ttu-id="e4227-106">Kui te loote oma saiti, on üks esimesi asju, mida te tõenäoliselt teete, lisada oma ettevõtte või kaubamärgi logo saidi päisesse.</span><span class="sxs-lookup"><span data-stu-id="e4227-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="e4227-107">Dynamics 365 Commerce Online Starter Kit pakub moodulit, mis muudab selle ülesande lihtsaks.</span><span class="sxs-lookup"><span data-stu-id="e4227-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="e4227-108">Logo saate lisada otse mallile, paigutusele või lehele.</span><span class="sxs-lookup"><span data-stu-id="e4227-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="e4227-109">Sel viisil saate hõlpsasti muuta logo, mis kuvatakse kindlatel lehekülgedel või lehekülgede gruppides.</span><span class="sxs-lookup"><span data-stu-id="e4227-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="e4227-110">See teema katab siiski kõige sagedasema stsenaariumi, kuhu lisate oma logo päise fragmenti, mida saab taaskasutada teie saidi kõigi lehtede puhul.</span><span class="sxs-lookup"><span data-stu-id="e4227-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e4227-111">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="e4227-111">Prerequisites</span></span>

<span data-ttu-id="e4227-112">Enne kui saate lisada logo kõigile oma saidi lehtedele, peate need ülesanded lõpetama.</span><span class="sxs-lookup"><span data-stu-id="e4227-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="e4227-113">Laadige oma logo meediateeki üles.</span><span class="sxs-lookup"><span data-stu-id="e4227-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="e4227-114">Loo päise fragment</span><span class="sxs-lookup"><span data-stu-id="e4227-114">Create a header fragment.</span></span> <span data-ttu-id="e4227-115">Lisateavet fragmentide loomise ja kasutamise kohta leiate teemast [töö fragmentidega](work-with-fragments.md)</span><span class="sxs-lookup"><span data-stu-id="e4227-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="e4227-116">Kaasake päise fragment malli, mida teie saidi leheküljed kasutavad paigutuse ja mooduli suvandite jaoks.</span><span class="sxs-lookup"><span data-stu-id="e4227-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="e4227-117">Vaadake lisateavet mallidega töötamise kohta jaotisest [Töö mallidega](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="e4227-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="e4227-118">Logo lisamine päise fragmenti</span><span class="sxs-lookup"><span data-stu-id="e4227-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="e4227-119">Oma saidi päise fragmenti logo lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e4227-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="e4227-120">Valige navigeerimispaanilt vasakult suvand **Lehe fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="e4227-120">In the navigation pane on the left, select **Page Fragments**.</span></span>
1. <span data-ttu-id="e4227-121">Valige varem loodud päise fragment ja seejärel valige käsk **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="e4227-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="e4227-122">Laiendage päise moodulit.</span><span class="sxs-lookup"><span data-stu-id="e4227-122">Expand the header module.</span></span>
1. <span data-ttu-id="e4227-123">Sisestage päise mooduli atribuudi paanile logo jaoks pilt ja link.</span><span class="sxs-lookup"><span data-stu-id="e4227-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="e4227-124">Salvestage päise fragment, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="e4227-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="e4227-125">Pärast värskendatud päise fragmenti avaldamist kuvatakse kõik saidi lehed, mis kasutavad päise fragmenti sisaldavat malli, mis näitavad teie logo.</span><span class="sxs-lookup"><span data-stu-id="e4227-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4227-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e4227-126">Additional resources</span></span>

[<span data-ttu-id="e4227-127">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="e4227-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="e4227-128">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="e4227-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="e4227-129">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="e4227-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e4227-130">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="e4227-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="e4227-131">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="e4227-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="e4227-132">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="e4227-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="e4227-133">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="e4227-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

