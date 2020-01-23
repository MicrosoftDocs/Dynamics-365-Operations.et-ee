---
title: Logo lisamine
description: Selles teemas kirjeldatakse, kuidas lisada logo rakenduses Microsoft Dynamics 365 Commerce oma saidile.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914614"
---
# <a name="add-a-logo"></a><span data-ttu-id="9000f-103">Logo lisamine</span><span class="sxs-lookup"><span data-stu-id="9000f-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9000f-104">Selles teemas kirjeldatakse, kuidas lisada logo rakenduses Microsoft Dynamics 365 Commerce oma saidile.</span><span class="sxs-lookup"><span data-stu-id="9000f-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9000f-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="9000f-105">Overview</span></span>

<span data-ttu-id="9000f-106">Kui te loote oma saiti, on üks esimesi asju, mida te tõenäoliselt teete, lisada oma ettevõtte või kaubamärgi logo saidi päisesse.</span><span class="sxs-lookup"><span data-stu-id="9000f-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="9000f-107">Dynamics 365 Commerce Online Starter Kit pakub moodulit, mis muudab selle ülesande lihtsaks.</span><span class="sxs-lookup"><span data-stu-id="9000f-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="9000f-108">Logo saate lisada otse mallile, paigutusele või lehele.</span><span class="sxs-lookup"><span data-stu-id="9000f-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="9000f-109">Sel viisil saate hõlpsasti muuta logo, mis kuvatakse kindlatel lehekülgedel või lehekülgede gruppides.</span><span class="sxs-lookup"><span data-stu-id="9000f-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="9000f-110">See teema katab siiski kõige sagedasema stsenaariumi, kuhu lisate oma logo päise fragmenti, mida saab taaskasutada teie saidi kõigi lehtede puhul.</span><span class="sxs-lookup"><span data-stu-id="9000f-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="9000f-111">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="9000f-111">Prerequisites</span></span>

<span data-ttu-id="9000f-112">Enne kui saate lisada logo kõigile oma saidi lehtedele, peate need ülesanded lõpetama.</span><span class="sxs-lookup"><span data-stu-id="9000f-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="9000f-113">Laadige oma logo üles digitaalsete varade haldurile, millele pääsete juurde lehelt **varad**.</span><span class="sxs-lookup"><span data-stu-id="9000f-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="9000f-114">Loo päise fragment</span><span class="sxs-lookup"><span data-stu-id="9000f-114">Create a header fragment.</span></span> <span data-ttu-id="9000f-115">Lisateavet fragmentide loomise ja kasutamise kohta leiate teemast [töö fragmentidega](work-with-fragments.md)</span><span class="sxs-lookup"><span data-stu-id="9000f-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="9000f-116">Kaasake päise fragment malli, mida teie saidi leheküljed kasutavad paigutuse ja mooduli suvandite jaoks.</span><span class="sxs-lookup"><span data-stu-id="9000f-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="9000f-117">Vaadake lisateavet mallidega töötamise kohta jaotisest [Töö mallidega](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="9000f-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="9000f-118">Logo lisamine päise fragmenti</span><span class="sxs-lookup"><span data-stu-id="9000f-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="9000f-119">Oma saidi päise fragmenti logo lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9000f-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="9000f-120">Vasakpoolses navigeerimispaanil valige **fragmendid**ja seejärel valige loodud päise fragment.</span><span class="sxs-lookup"><span data-stu-id="9000f-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="9000f-121">Valige suvand **Registreeri välja**.</span><span class="sxs-lookup"><span data-stu-id="9000f-121">Select **Check out**.</span></span>
3. <span data-ttu-id="9000f-122">Laiendage **päise** pesa ja **logo** pesa.</span><span class="sxs-lookup"><span data-stu-id="9000f-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="9000f-123">Valige **logo** pesa jaoks kolmikpunkti nupp (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="9000f-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="9000f-124">Valige logo moodul.</span><span class="sxs-lookup"><span data-stu-id="9000f-124">Select the logo module.</span></span>
6. <span data-ttu-id="9000f-125">Konfigureerige paremal atribuutide paanil logo moodulit nii, et teie logo oleks näha.</span><span class="sxs-lookup"><span data-stu-id="9000f-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="9000f-126">Salvestage pease fragment, kontrollige seda ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="9000f-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="9000f-127">Pärast värskendatud päise fragmenti avaldamist kuvatakse kõik saidi lehed, mis kasutavad päise fragmenti sisaldavat malli, mis näitavad teie logo.</span><span class="sxs-lookup"><span data-stu-id="9000f-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9000f-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9000f-128">Additional resources</span></span>

[<span data-ttu-id="9000f-129">Saidi kujunduse valimine</span><span class="sxs-lookup"><span data-stu-id="9000f-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="9000f-130">CSS-i alistusfailidega töötamine</span><span class="sxs-lookup"><span data-stu-id="9000f-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="9000f-131">Leheikooni lisamine</span><span class="sxs-lookup"><span data-stu-id="9000f-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="9000f-132">Tervitussõnumi lisamine</span><span class="sxs-lookup"><span data-stu-id="9000f-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="9000f-133">Autoriõiguste teatise lisamine</span><span class="sxs-lookup"><span data-stu-id="9000f-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="9000f-134">Saidile keelte lisamine</span><span class="sxs-lookup"><span data-stu-id="9000f-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="9000f-135">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="9000f-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

