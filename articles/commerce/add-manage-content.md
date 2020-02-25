---
title: Sisu lisamise viisid
description: See teema annab ülevaate ja valitud lingid, kust ja kuidas alustada sisu haldamist kasutades Microsoft Dynamics 365 Commerce'i saidiehitaja veebivalmistamise tööriistakomplekti.
author: phinneyridge
manager: annbe
ms.date: 01/31/2020
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
ms.openlocfilehash: 916e28c2628613332246d19af0fae81f258404b0
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025712"
---
# <a name="ways-to-add-content"></a><span data-ttu-id="3f0a9-103">Sisu lisamise viisid</span><span class="sxs-lookup"><span data-stu-id="3f0a9-103">Ways to add content</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3f0a9-104">See teema annab ülevaate ja valitud lingid dokumentatsiooni juurde, kuidas hallata sisu kasutades Microsoft Dynamics 365 Commerce'i saidiehitaja veebivalmistamise tööriistakomplekti.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-104">This topic provides an overview and links to documentation about how to manage content using the Microsoft Dynamics 365 Commerce site builder web authoring toolset.</span></span>

## <a name="overview"></a><span data-ttu-id="3f0a9-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="3f0a9-105">Overview</span></span>

<span data-ttu-id="3f0a9-106">Saidi välimuse, olemuse ja sisu muutmiseks on mitmeid viise.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-106">There are many ways to change the look, feel, and content of your site.</span></span> <span data-ttu-id="3f0a9-107">Sõltuvalt nõutavast kohandamise tasemest, saab paljusid neid muudatusi rakendada mitte-arendajate poolt saidiehitajaga, Dynamics 365 Commerce'iga kaasasolevas veebivalmistamise tööriistakomplektiga.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-107">Depending on the required level of customization, many of these changes can be implemented by non-developers within site builder, the web authoring toolset included with Dynamics 365 Commerce.</span></span> <span data-ttu-id="3f0a9-108">Saidiehitaja võimaldab teil luua malle, valida kujundusi ning valida ja konfigureerida moodulid ilma koodi kirjutamata.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-108">Site builder enables you to build templates, select themes, and select and configure modules without writing any code.</span></span> <span data-ttu-id="3f0a9-109">Seevastu on arendamise oskused vajalikud uue kujunduse või mooduli loomiseks, kuna kasutada tuleb e-kaubanduse tarkvara arendusekomplekti (SDK) ja Microsoft Dynamicsi teenuse Lifecycle Services (LCS) juurutamise töövoogu.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-109">By contrast, development skills are required to create a new theme or module, because the e-Commerce software development kit (SDK) and the Microsoft Dynamics Lifecycle Services (LCS) deployment workflow must be used.</span></span>

<span data-ttu-id="3f0a9-110">Järgmised teemad on heaks alguspunktiks, et alustada saidile sisu lisamist ja haldamist.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-110">The following topics are good jumping off points to start understanding how to add and manage site content.</span></span> <span data-ttu-id="3f0a9-111">Enamikud toodud teemad keskenduvad teie saidi aladele, mille jaoks arendajat ei ole vaja.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-111">Most of the topics listed focus on areas of your site that don't require a developer.</span></span> <span data-ttu-id="3f0a9-112">Mõned tegelevad põhilise sisu redigeerimisega, samas kui teised keskenduvad saidi haldustoimingutele.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-112">Some address basic content editing, while others focus on site administrator tasks.</span></span> <span data-ttu-id="3f0a9-113">Kõik need teemad tähistavad kindlaid ülesandeid, mis võivad nõuda SDK-tööd.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-113">Each of these topics will denote specific tasks might require SDK work.</span></span> <span data-ttu-id="3f0a9-114">Iga teema eeldab, et olete saidi juba ette valmistanud ja teile on antud juurdepääs oma saidi saidiehitaja tööriistakomplektile.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-114">Each topic assumes that you have already provisioned a site and been granted access to the site builder toolset for your site.</span></span>

<span data-ttu-id="3f0a9-115">Alustamiseks valige üks järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="3f0a9-115">Select one of the following topics to get started.</span></span>

- <span data-ttu-id="3f0a9-116">Saidiehitajas ja selle dokumentatsioonis kasutatava sisuhalduse terminoloogiaga tutvumiseks vaadake jaotist [Lehe mudeli sõnastik](page-elements-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a9-116">To familiarize yourself with the content management terminology used in site builder and within this documentation, see [Page model glossary](page-elements-overview.md).</span></span>
- <span data-ttu-id="3f0a9-117">Et mõista, kuidas moodulid sisuhalduse töövoogudes töötavad, vt jaotist [Töö moodulitega](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a9-117">To understand how modules work within content management workflows, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="3f0a9-118">Olemasoleva saidi lehe teksti, piltide või video muutmise kohta vaadake teemat [Moodulitega töötamine](work-with-modules.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a9-118">To change the text, images, or video on an existing site page, see [Work with modules](work-with-modules.md).</span></span>
- <span data-ttu-id="3f0a9-119">Et näha, kuidas fragmendid saavad muuta sisuhalduse tõhusamaks ja paindlikumaks muuta, vt jaotist [Töö fragmentidega](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a9-119">To see how fragments can make content management more efficient and flexible, see [Work with fragments](work-with-fragments.md).</span></span>
- <span data-ttu-id="3f0a9-120">Veebisisu autoritele eduka kaubamärgi sisu loomise kogemuse kindlustamiseks vt jaotist [Mallide ja paigutuse ülevaade](templates-layouts-overview.md) ja [Töö mallidega](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a9-120">To help ensure a successful on-brand authoring experience for web content authors, see [Templates and layouts overview](templates-layouts-overview.md) and [Work with templates](work-with-templates.md).</span></span>
- <span data-ttu-id="3f0a9-121">Saidi lehe jaotiste ümberkorraldamise kohta vaadake teemat [Paigutustega töötamine](work-with-layouts.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a9-121">To rearrange sections on a site page, see [Work with layouts](work-with-layouts.md).</span></span>
- <span data-ttu-id="3f0a9-122">Saidi lehtede fontide, värvide ja üldise välimuse muutmise kohta vt jaotist [Saidi kujunduse valimine](select-site-theme.md) või [Töö CSS'i alistamisfailidega](css-override-files.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a9-122">To change the fonts, colors, and general look of site pages, see [Select a site theme](select-site-theme.md) or [Work with CSS over-ride files](css-override-files.md).</span></span>
- <span data-ttu-id="3f0a9-123">Navigeerimisvalikute ümberkorraldamiseks või uute lisamiseks vt jaotist [Saidi navigeerimise kohandamine](customize-site-navigation.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a9-123">To rearrange or add new navigation options, see [Customize site navigation](customize-site-navigation.md).</span></span>
- <span data-ttu-id="3f0a9-124">Teavet selle kohta, kuidas korraldada, eelvaadata ja avaldada laialdasi samaaegseid veebisisu muudatusi, vt jaotisest [Töö avaldamise gruppidega](publish-groups.md).</span><span class="sxs-lookup"><span data-stu-id="3f0a9-124">To learn how to stage, preview, and publish a broad set of concurrent web content changes, see [Work with publish groups](publish-groups.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f0a9-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3f0a9-125">Additional resources</span></span>

[<span data-ttu-id="3f0a9-126">Autorluse lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="3f0a9-126">Authoring page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="3f0a9-127">Dokumendi olekud ja töötsükkel</span><span class="sxs-lookup"><span data-stu-id="3f0a9-127">Document states and lifecycle</span></span>](document-states-overview.md)
