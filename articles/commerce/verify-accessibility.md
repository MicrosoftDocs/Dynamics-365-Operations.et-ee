---
title: Lehe sisu juurdepääsetavuse kontrollimine
description: Selles teemas kirjeldatakse, kuidas kontrollida lehe sisu juurdepääsetavust rakenduses Microsoft Dynamics 365 Commerce.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 186044fc7a360f227cecffb39bad0e225245dd4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210967"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="51ddb-103">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="51ddb-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="51ddb-104">Selles teemas kirjeldatakse, kuidas kontrollida lehe sisu juurdepääsetavust rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="51ddb-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="51ddb-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="51ddb-105">Overview</span></span>

<span data-ttu-id="51ddb-106">Kui olete lehe muutmise lõpetanud, veenduge, et sisu oleks veebis kõigile juurdepääsetav.</span><span class="sxs-lookup"><span data-stu-id="51ddb-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="51ddb-107">Commerce’i autorluse tööriistades saate hõlpsalt kontrollida lehe sisu juurdepääsetavust, kasutades sisse-ehitatud teenust [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="51ddb-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="51ddb-108">See teenus kontrollib teie lehe sisu vastavalt uusimatele [World Wide Webi konsortsiumi (W3C) juurdepääsetavuse](https://www.w3.org/standards/webdesign/accessibility) juhistele.</span><span class="sxs-lookup"><span data-stu-id="51ddb-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="51ddb-109">Enne selle kasutamist peab teenuse [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integratsioon olema rentniku või saidi tasemel sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="51ddb-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="51ddb-110">Teenuse Microsoft Accessibility Insights sisselülitamine rentniku kõikide saitide jaoks</span><span class="sxs-lookup"><span data-stu-id="51ddb-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="51ddb-111">Teenuse [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integratsiooni sisselülitamiseks kõikide rentniku Commerce’i saitide jaoks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="51ddb-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="51ddb-112">Rentniku sätete avamiseks peate olema Commerce’i süsteemiadministraatorina sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="51ddb-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="51ddb-113">Logige Commerce’i süsteemiadministraatorina sisse.</span><span class="sxs-lookup"><span data-stu-id="51ddb-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="51ddb-114">Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).</span><span class="sxs-lookup"><span data-stu-id="51ddb-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="51ddb-115">Jaotises **Rentniku sätted** valige suvand **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="51ddb-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="51ddb-116">Seadke valik **Hõlbustuskontroll** väärtusele **Sees**.</span><span class="sxs-lookup"><span data-stu-id="51ddb-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="51ddb-117">Teenuse Microsoft Accessibility Insights sisselülitamine ühe saidi jaoks</span><span class="sxs-lookup"><span data-stu-id="51ddb-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="51ddb-118">Teenuse [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integratsiooni sisselülitamiseks Commerce’i ühe saidi jaoks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="51ddb-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="51ddb-119">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="51ddb-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="51ddb-120">Vasakpoolsel navigeerimispaanil valige suvand **Saidi sätted** selle laiendamiseks.</span><span class="sxs-lookup"><span data-stu-id="51ddb-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="51ddb-121">Jaotises **Saidi sätted** valige suvand **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="51ddb-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="51ddb-122">Seadke valik **Hõlbustuskontroll** väärtusele **Sees**.</span><span class="sxs-lookup"><span data-stu-id="51ddb-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="51ddb-123">Kodulehe sisu juurdepääsetavuse kontrollimine</span><span class="sxs-lookup"><span data-stu-id="51ddb-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="51ddb-124">Integreeritud teenuse [Microsoft Accessibility Insights](https://accessibilityinsights.io/) kasutamiseks Commerce’is oma kodulehe sisu skannimiseks ja kinnitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="51ddb-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="51ddb-125">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="51ddb-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="51ddb-126">Valige vasakpoolsel navigeerimispaanil suvand **Lehed**.</span><span class="sxs-lookup"><span data-stu-id="51ddb-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="51ddb-127">Leidke ja valige avaleht, et avada see lehe redaktoris.</span><span class="sxs-lookup"><span data-stu-id="51ddb-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="51ddb-128">Klõpsake käsuribal käsku **Kontrolli kasutushõlpsust**.</span><span class="sxs-lookup"><span data-stu-id="51ddb-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="51ddb-129">Kuvatakse leht **Kontrolli kasutushõlpsust**.</span><span class="sxs-lookup"><span data-stu-id="51ddb-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="51ddb-130">Vadake pärast skannimise lõpetamist aruande sisu üle.</span><span class="sxs-lookup"><span data-stu-id="51ddb-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="51ddb-131">Kui mõni kontroll ebaõnnestus, valige iga ebaõnnestunud kontroll, et seda laiendada, et saaksite vaadata rohkem üksikasju.</span><span class="sxs-lookup"><span data-stu-id="51ddb-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="51ddb-132">Pärast selle läbivaatamist aruande sulgemiseks kerige lehe **Kontrolli kasutushõlpsust** lõppu ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="51ddb-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="51ddb-133">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="51ddb-133">Additional resources</span></span>

[<span data-ttu-id="51ddb-134">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="51ddb-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="51ddb-135">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="51ddb-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="51ddb-136">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="51ddb-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="51ddb-137">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="51ddb-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="51ddb-138">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="51ddb-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="51ddb-139">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="51ddb-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="51ddb-140">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="51ddb-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="51ddb-141">Dünaamiliste e-kaubanduse lehtede loomine URL-parameetrite põhjal</span><span class="sxs-lookup"><span data-stu-id="51ddb-141">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]