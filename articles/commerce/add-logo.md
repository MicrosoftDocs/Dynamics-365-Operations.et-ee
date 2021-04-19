---
title: Logo lisamine
description: Selles teemas kirjeldatakse, kuidas lisada logo rakenduses Microsoft Dynamics 365 Commerce oma saidile.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9e1cba6bd07e0c3d9ed7d741d87e10837d8021c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797595"
---
# <a name="add-a-logo"></a><span data-ttu-id="18d6e-103">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="18d6e-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="18d6e-104">Selles teemas kirjeldatakse, kuidas lisada logo rakenduses Microsoft Dynamics 365 Commerce oma saidile.</span><span class="sxs-lookup"><span data-stu-id="18d6e-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="18d6e-105">Kui te loote oma saiti, on üks esimesi asju, mida te tõenäoliselt teete, lisada oma ettevõtte või kaubamärgi logo saidi päisesse.</span><span class="sxs-lookup"><span data-stu-id="18d6e-105">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="18d6e-106">Rakenduse Dynamics 365 Commerce veebimooduliteek pakub moodulit, mis muudab selle ülesande lihtsaks.</span><span class="sxs-lookup"><span data-stu-id="18d6e-106">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="18d6e-107">Logo saate lisada otse mallile, paigutusele või lehele.</span><span class="sxs-lookup"><span data-stu-id="18d6e-107">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="18d6e-108">Sel viisil saate hõlpsasti muuta logo, mis kuvatakse kindlatel lehekülgedel või lehekülgede gruppides.</span><span class="sxs-lookup"><span data-stu-id="18d6e-108">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="18d6e-109">See teema katab siiski kõige sagedasema stsenaariumi, kuhu lisate oma logo päise fragmenti, mida saab taaskasutada teie saidi kõigi lehtede puhul.</span><span class="sxs-lookup"><span data-stu-id="18d6e-109">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="18d6e-110">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="18d6e-110">Prerequisites</span></span>

<span data-ttu-id="18d6e-111">Enne kui saate lisada logo kõigile oma saidi lehtedele, peate need ülesanded lõpetama.</span><span class="sxs-lookup"><span data-stu-id="18d6e-111">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="18d6e-112">Laadige oma logo meediateeki üles.</span><span class="sxs-lookup"><span data-stu-id="18d6e-112">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="18d6e-113">Loo päise fragment</span><span class="sxs-lookup"><span data-stu-id="18d6e-113">Create a header fragment.</span></span> <span data-ttu-id="18d6e-114">Lisateavet fragmentide loomise ja kasutamise kohta leiate teemast [töö fragmentidega](work-with-fragments.md)</span><span class="sxs-lookup"><span data-stu-id="18d6e-114">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="18d6e-115">Kaasake päise fragment malli, mida teie saidi leheküljed kasutavad paigutuse ja mooduli suvandite jaoks.</span><span class="sxs-lookup"><span data-stu-id="18d6e-115">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="18d6e-116">Vaadake lisateavet mallidega töötamise kohta jaotisest [Töö mallidega](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="18d6e-116">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="18d6e-117">Logo lisamine päise fragmenti</span><span class="sxs-lookup"><span data-stu-id="18d6e-117">Add a logo to a header fragment</span></span>

<span data-ttu-id="18d6e-118">Oma saidi päise fragmenti logo lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="18d6e-118">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="18d6e-119">Valige navigeerimispaanilt vasakult suvand **Fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="18d6e-119">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="18d6e-120">Valige varem loodud päise fragment ja seejärel valige käsk **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="18d6e-120">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="18d6e-121">Laiendage päise moodulit.</span><span class="sxs-lookup"><span data-stu-id="18d6e-121">Expand the header module.</span></span>
1. <span data-ttu-id="18d6e-122">Sisestage päise mooduli atribuudi paanile logo jaoks pilt ja link.</span><span class="sxs-lookup"><span data-stu-id="18d6e-122">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="18d6e-123">Salvestage päise fragment, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="18d6e-123">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="18d6e-124">Pärast värskendatud päise fragmenti avaldamist kuvatakse kõik saidi lehed, mis kasutavad päise fragmenti sisaldavat malli, mis näitavad teie logo.</span><span class="sxs-lookup"><span data-stu-id="18d6e-124">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="18d6e-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="18d6e-125">Additional resources</span></span>

[<span data-ttu-id="18d6e-126">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="18d6e-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="18d6e-127">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="18d6e-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="18d6e-128">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="18d6e-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="18d6e-129">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="18d6e-129">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="18d6e-130">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="18d6e-130">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="18d6e-131">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="18d6e-131">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="18d6e-132">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="18d6e-132">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
