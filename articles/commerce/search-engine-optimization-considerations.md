---
title: Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused
description: See teema hõlmab otsingumootori optimeerimise (SEO) kaalutlusi teie saidi jaoks arengust tootmiseni.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b35d0cb606e1b17a0258ea3fcb6287988d83091c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698207"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="3e4eb-103">Saidi jaoks otsingumootori optimeerimise (SEO) kaalutlused</span><span class="sxs-lookup"><span data-stu-id="3e4eb-103">Search engine optimization (SEO) considerations for your site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3e4eb-104">See teema hõlmab otsingumootori optimeerimise (SEO) kaalutlusi teie saidi jaoks arengust tootmiseni.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="3e4eb-105">Arendatav sait</span><span class="sxs-lookup"><span data-stu-id="3e4eb-105">A site that is under development</span></span>

<span data-ttu-id="3e4eb-106">Kui saiti arendatakse, peaks kõigil saidi lehekülgedel olema metasildid **NOINDEX** ja **NOFOLLOW**, nii et otsingumootorid ei indekseeriks lehti ja kaupluse arenduse versioone oma saidi vahemälu.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="3e4eb-107">Selle konfiguratsiooni tegemiseks peate lisama vaikimisi metasildid mooduli lehe mallile.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="3e4eb-108">Vaikimisi metasiltide atribuudid on siis saadaval SEO atribuutide jaotises lehe redaktoris.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="3e4eb-109">Neid atribuute saate kasutada metasiltide haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="3e4eb-110">Saidi esialgne käivitamine</span><span class="sxs-lookup"><span data-stu-id="3e4eb-110">Soft launch of a site</span></span>

<span data-ttu-id="3e4eb-111">"Esialgse käivitamise" ajal tehakse veebisait kättesaadavaks piiratud publikule või turule enne täieliku käivitamise toimumist.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="3e4eb-112">Kui teete oma veebisaidile esialgse käivitamise, peaksite metasildid **NOINDEX** jätma oma kohale.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="3e4eb-113">Sel viisil aitate tagada, et esialgne käivitamine piirduks piiratud publikuga, kelleni soovite jõuda.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="3e4eb-114">Sait, mis on tootmises</span><span class="sxs-lookup"><span data-stu-id="3e4eb-114">A site that is in production</span></span>

<span data-ttu-id="3e4eb-115">Kui sait on tootmisse kaasatud, veenduge, et kõik saidi lehed on õigesti märgistatud.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="3e4eb-116">Microsoft Dynamics 365 Commerce kasutab lehe jaoks sisestatud teavet, et renderdada kõik SEO andmed sellel lehel.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="3e4eb-117">Järgmised moodulid pakuvad seda funktsiooni: kategooria lehekülje kokkuvõte, loendi lehekülje kokkuvõte ja toote lehekülje kokkuvõte.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="3e4eb-118">Otsingumootori indekseerimise optimeerimiseks kasutab renderdamise raamistik mõlemat teavet SEO atribuutidest, mis on konfigureeritud rakenduses Dynamics 365 Commerce ja konkreetse mooduli teabes.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="3e4eb-119">Tootmiseks kasutatava saidi puhul peaksite veenduma, et fail robots.txt võimaldab kogu saidi indekseerimist ja see sisaldab linke teie avaldatud saidi vastenduse dokumendile.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="3e4eb-120">Peaksite lülitama saidi kaardi loomise funktsioonid **Saidi sätted \> Saidi kaart on lubatud**.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="3e4eb-121">Lehekülje SEO sätted sisemise eelvaate, piiratud sihtrühmade ja kogu publiku jaoks</span><span class="sxs-lookup"><span data-stu-id="3e4eb-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="3e4eb-122">Kuna rakendus Dynamics 365 Commerce toetab "mida sa näed on see, mida sa saad" (WYSIWYG) autenditud eelvaateid, saavad autorid ette valmistada oma lehe sisu, ilma et peaks muretsema, et teave muutub saidi külastajatele nähtavaks.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="3e4eb-123">Kui leht tuleb avaldada, kuid selle säritus peab olema piiratud, peaks sellel olema metasilt **NOINDEX**, nii et otsingumootorid seda ei indekseeriks.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="3e4eb-124">Seejärel, kui leht on kõigi sihtrühmade jaoks valmis, tuleb esitada kõik põhilised SEO metaandmed, et maksimeerida otsingumootori indekseerimise efektiivsust.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="3e4eb-125">Lisaks tuleks eemaldada metasilt **NOLIMIT**.</span><span class="sxs-lookup"><span data-stu-id="3e4eb-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3e4eb-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3e4eb-126">Additional resources</span></span>

[<span data-ttu-id="3e4eb-127">E-kaubanduse kasutajate ja rollide haldamine</span><span class="sxs-lookup"><span data-stu-id="3e4eb-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="3e4eb-128">Telemeetria toetamiseks saidile skriptikoodi lisamine</span><span class="sxs-lookup"><span data-stu-id="3e4eb-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="3e4eb-129">Sisu turbepoliitika (CSP) haldamine</span><span class="sxs-lookup"><span data-stu-id="3e4eb-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
