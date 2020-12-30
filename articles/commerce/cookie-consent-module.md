---
title: Küpsistega nõustumise moodul
description: See teema hõlmab küpsistega nõustumise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 60ce530575841c22355e4a14e8b0bbec6c0e35ab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411573"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="54d7a-103">Küpsistega nõustumise moodul</span><span class="sxs-lookup"><span data-stu-id="54d7a-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="54d7a-104">See teema hõlmab küpsistega nõustumise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="54d7a-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="54d7a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="54d7a-105">Overview</span></span>

<span data-ttu-id="54d7a-106">Küpsistega nõustumise moodul palub saidi kasutajatel anda nõusolek küpsiste lubamiseks mis tahes funktsiooni või mooduli jaoks, mis jälgib brauseri küpsiseid.</span><span class="sxs-lookup"><span data-stu-id="54d7a-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="54d7a-107">Nõusolekut küsitakse saidi esmakordsel sirvimisel brauseri esimesel seansil.</span><span class="sxs-lookup"><span data-stu-id="54d7a-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="54d7a-108">Nõusoleku saamisel jälgitakse seda ja saidi kasutajalt ei küsita uuesti nõusolekut.</span><span class="sxs-lookup"><span data-stu-id="54d7a-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="54d7a-109">Lisateavet vt teemast [Küpsise vastavus](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="54d7a-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="54d7a-110">Kui saidi kasutaja küpsise nõusolekut ei anna, ei renderdata lehel ühtegi küpsise nõusolekut nõudvat funktsiooni või moodulit.</span><span class="sxs-lookup"><span data-stu-id="54d7a-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="54d7a-111">Näiteks maksmise moodul, suhtlussaidil jagamise moodul ja eelistatud kaupluse funktsioon nõuavad küpsise nõusolekut ja neid ei renderdata, kui saidi kasutaja nõusolekut ei anna.</span><span class="sxs-lookup"><span data-stu-id="54d7a-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="54d7a-112">Küpsistega nõustumise mooduli saab konfigureerida lehe päise fragmendis, et seda saaks lehe laadimisel jõustada.</span><span class="sxs-lookup"><span data-stu-id="54d7a-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="54d7a-113">Küpsistega nõustumise moodulil peaks olema selge teade, mis teavitab saidi kasutajat küpsiste kasutamisest saidil ja peaks esitama saidi privaatsuspoliitika lehele viiva lingi.</span><span class="sxs-lookup"><span data-stu-id="54d7a-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="54d7a-114">Järgmisel joonisel on toodud küpsise nõusoleku teate näide koos saidilehe päises kuvatava saidi privaatsuspoliitika lehele viiva lingiga.</span><span class="sxs-lookup"><span data-stu-id="54d7a-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="54d7a-115">![Küpsistega nõustumise mooduli näide](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="54d7a-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="54d7a-116">Küpsistega nõustumise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="54d7a-116">Cookie consent module properties</span></span>

| <span data-ttu-id="54d7a-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="54d7a-117">Property name</span></span>             | <span data-ttu-id="54d7a-118">Väärtus</span><span class="sxs-lookup"><span data-stu-id="54d7a-118">Value</span></span>                 | <span data-ttu-id="54d7a-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="54d7a-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="54d7a-120">Rikastekst</span><span class="sxs-lookup"><span data-stu-id="54d7a-120">Rich Text</span></span>                  | <span data-ttu-id="54d7a-121">Rikastekst</span><span class="sxs-lookup"><span data-stu-id="54d7a-121">Rich Text</span></span> | <span data-ttu-id="54d7a-122">Määrab saidi kasutajatele kuvatava rikasteksti teatise selle kohta, et sait kasutab brauseri küpsiseid ja et kasutajad peaksid nõustuma küpsiste kasutamisega saidi täielikult funktsioneerimiseks.</span><span class="sxs-lookup"><span data-stu-id="54d7a-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="54d7a-123">Lingid</span><span class="sxs-lookup"><span data-stu-id="54d7a-123">Links</span></span> | <span data-ttu-id="54d7a-124">URL</span><span class="sxs-lookup"><span data-stu-id="54d7a-124">URL</span></span> | <span data-ttu-id="54d7a-125">Saidi privaatsuspoliitika lehele saab lisada ühe või mitu linki, mis kirjeldavad saidil jälgitavate küpsiste tüüpe.</span><span class="sxs-lookup"><span data-stu-id="54d7a-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="54d7a-126">Küpsistega nõustumise mooduli lisamine saidi lehtedele</span><span class="sxs-lookup"><span data-stu-id="54d7a-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="54d7a-127">Küpsistega nõustumise mooduli tõhusaks lisamiseks mitmele saidi lehele saab selle lisada ühiskasutusega lehe päise fragmenti.</span><span class="sxs-lookup"><span data-stu-id="54d7a-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="54d7a-128">Pärast päise fragmendi lisamist kõigile saidi lehtedele renderdatakse küpsise nõusoleku teatis automaatselt, kui saidi kasutaja liigub esimest korda suvalisele saidi lehele.</span><span class="sxs-lookup"><span data-stu-id="54d7a-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="54d7a-129">Lisateavet päise fragmentide ja -moodulite kohta vt teemast [Päisemoodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="54d7a-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="54d7a-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="54d7a-130">Additional resources</span></span>

[<span data-ttu-id="54d7a-131">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="54d7a-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="54d7a-132">Päisemoodul</span><span class="sxs-lookup"><span data-stu-id="54d7a-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="54d7a-133">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="54d7a-133">Cookie compliance</span></span>](cookie-compliance.md)
