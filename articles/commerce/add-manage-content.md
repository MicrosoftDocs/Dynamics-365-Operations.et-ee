---
title: Sisu lisamise viisid
description: See teema annab teavet selle kohta, kuidas rakenduse Microsoft Dynamics 365 Commerce saidil lisada ja hallata sisu.
author: phinneyridge
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3d91235837aee9ad06466ffe47727b435e39094f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770524"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="65d5d-103">Sisu lisamise viisid</span><span class="sxs-lookup"><span data-stu-id="65d5d-103">Ways to add content</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="65d5d-104">See teema annab teavet selle kohta, kuidas rakenduse Microsoft Dynamics 365 Commerce saidil lisada ja hallata sisu.</span><span class="sxs-lookup"><span data-stu-id="65d5d-104">This topic provides information about how to add and manage content on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="65d5d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="65d5d-105">Overview</span></span>

<span data-ttu-id="65d5d-106">Saidi välimuse, olemuse ja sisu muutmiseks on mitmeid viise.</span><span class="sxs-lookup"><span data-stu-id="65d5d-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="65d5d-107">Vajalikust kohandamise tasemest sõltuvalt saavad paljusid neid muudatusi rakendada mittearendajast kasutajad.</span><span class="sxs-lookup"><span data-stu-id="65d5d-107">Depending on the required level of customization, many of these changes can be implemented by non-developers.</span></span> <span data-ttu-id="65d5d-108">Näiteks ei ole mallide koostamiseks, teemade valimiseks ja moodulite valimiseks ning konfigureerimiseks koodi kirjutamine vajalik.</span><span class="sxs-lookup"><span data-stu-id="65d5d-108">For example, no code has to be written to build templates, select themes, and select and configure modules.</span></span> <span data-ttu-id="65d5d-109">Seevastu on arendamise oskused vajalikud uue kujunduse või mooduli loomiseks, kuna kasutada tuleb e-kaubanduse tarkvara arendusekomplekti (SDK) ja Microsoft Dynamicsi teenuse Lifecycle Services (LCS) juurutamise töövoogu.</span><span class="sxs-lookup"><span data-stu-id="65d5d-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="65d5d-110">Järgmised teemad annavad üksikasjalikku teavet selle kohta, kuidas lisada ja hallata saidi sisu.</span><span class="sxs-lookup"><span data-stu-id="65d5d-110">The following topics provide detailed information about how to add and manage site content.</span></span> <span data-ttu-id="65d5d-111">Need keskenduvad teie saidi aladele, mille jaoks arendajat ei ole vaja.</span><span class="sxs-lookup"><span data-stu-id="65d5d-111">They focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="65d5d-112">Vastavalt vajadusele viitavad need ülesannetele, mis nõuavad SDK tööd.</span><span class="sxs-lookup"><span data-stu-id="65d5d-112">As required, they point out tasks that require SDK work.</span></span>

- <span data-ttu-id="65d5d-113">Olemasoleva saidi lehe teksti, piltide või video muutmise kohta vaadake teemat [Moodulitega töötamine](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="65d5d-113">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="65d5d-114">Veebisisu autorite eksituskindla kaubamärgipõhise autorluskogemuse tagamiseks vaadake teemat [Mallidega töötamine](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="65d5d-114">To help guarantee a foolproof, on-brand authoring experience for web content authors, see [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="65d5d-115">Saidi lehe jaotiste ümberkorraldamise kohta vaadake teemat [Paigutustega töötamine](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="65d5d-115">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="65d5d-116">Saidi lehtede fontide, värvide ja üldise välimuse muutmise kohta vaadake teemat [Saidi teema valimine](select-site-theme.md).</span><span class="sxs-lookup"><span data-stu-id="65d5d-116">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65d5d-117">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="65d5d-117">Additional resources</span></span>

[<span data-ttu-id="65d5d-118">Lehemudeli sõnastik</span><span class="sxs-lookup"><span data-stu-id="65d5d-118">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="65d5d-119">Dokumendi olekud ja töötsükkel</span><span class="sxs-lookup"><span data-stu-id="65d5d-119">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="65d5d-120">Moodulitega töötamine</span><span class="sxs-lookup"><span data-stu-id="65d5d-120">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="65d5d-121">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="65d5d-121">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="65d5d-122">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="65d5d-122">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="65d5d-123">Saidil navigeerimise kohandamine</span><span class="sxs-lookup"><span data-stu-id="65d5d-123">Customize site navigation</span></span>](customize-site-navigation.md)
