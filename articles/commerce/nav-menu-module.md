---
title: Navigeerimismenüü moodul
description: See teema hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761382"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="a1e94-103">Navigeerimismenüü moodul</span><span class="sxs-lookup"><span data-stu-id="a1e94-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="a1e94-104">See teema hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="a1e94-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a1e94-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="a1e94-105">Overview</span></span>

<span data-ttu-id="a1e94-106">Navigeerimismenüü moodulite peamine eesmärk on võimaldada saidi kasutajatel sirvida tooteid ja saite vastavalt Dynamics 365 Commerce'i peakontoris määratletud kanali navigeerimishierarhiale.</span><span class="sxs-lookup"><span data-stu-id="a1e94-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="a1e94-107">Navigeerimismenüü moodulis konfigureeritud üksused ilmuvad saidi päise navigeerimises.</span><span class="sxs-lookup"><span data-stu-id="a1e94-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="a1e94-108">Navigeerimismenüü moodulid toetavad ka staatilisi menüü-üksusi, mis lingivad e-kaubanduse saidi muudele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="a1e94-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="a1e94-109">Navigeerimismenüü mooduli saab lisada lehe päisemoodulisse.</span><span class="sxs-lookup"><span data-stu-id="a1e94-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="a1e94-110">Fabrikami kujunduse navigeerimismenüüs kuvatakse vaikimisi kaks taset.</span><span class="sxs-lookup"><span data-stu-id="a1e94-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="a1e94-111">Starteri kujunduse navigeerimismenüüs kuvatakse vaikimisi kolm taset.</span><span class="sxs-lookup"><span data-stu-id="a1e94-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="a1e94-112">Tasemete arvu muutmiseks on kujunduses nõutav vaate laiend.</span><span class="sxs-lookup"><span data-stu-id="a1e94-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="a1e94-113">Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüü näide, millel on kaks kategooriahierarhia taset ja mõned staatilised menüü-üksused.</span><span class="sxs-lookup"><span data-stu-id="a1e94-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="a1e94-114">![Navigeerimismenüü mooduli näide](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="a1e94-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="a1e94-115">Navigeerimismenüü mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="a1e94-115">Navigation menu module properties</span></span>

| <span data-ttu-id="a1e94-116">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="a1e94-116">Property name</span></span>             | <span data-ttu-id="a1e94-117">Väärtus</span><span class="sxs-lookup"><span data-stu-id="a1e94-117">Value</span></span>                 | <span data-ttu-id="a1e94-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a1e94-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="a1e94-119">Allikas</span><span class="sxs-lookup"><span data-stu-id="a1e94-119">Source</span></span>                  | <span data-ttu-id="a1e94-120">**Jaemüük**, **Käsitsi koostamine**, **Jaemüük ja käsitsi koostamine**</span><span class="sxs-lookup"><span data-stu-id="a1e94-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="a1e94-121">Väärtus **Jaemüük** võimaldab navigeerimismenüüs kuvada kanali navigeerimishierarhia Commerce'i peakontorist.</span><span class="sxs-lookup"><span data-stu-id="a1e94-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="a1e94-122">Väärtus **Käsitsi koostamine** võimaldab staatiliste menüüde üksusi kureerida.</span><span class="sxs-lookup"><span data-stu-id="a1e94-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="a1e94-123">Väärtus **Jaemüük ja käsitsi koostamine** võimaldab mõlemat.</span><span class="sxs-lookup"><span data-stu-id="a1e94-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="a1e94-124">Kategooria piltide kuvamine</span><span class="sxs-lookup"><span data-stu-id="a1e94-124">Show category images</span></span> | <span data-ttu-id="a1e94-125">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="a1e94-125">**True** or **False**</span></span>    | <span data-ttu-id="a1e94-126">Kui see on lubatud, kuvatakse navigeerimismenüüs kategooria pildid, nagu on määratletud iga kategooria kohta Commerce’i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="a1e94-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="a1e94-127">Lisatud Commerce'i väljalaskesse 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="a1e94-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="a1e94-128">Staatiline menüü-üksus</span><span class="sxs-lookup"><span data-stu-id="a1e94-128">Static menu item</span></span>| <span data-ttu-id="a1e94-129">Väärtuste massiiv</span><span class="sxs-lookup"><span data-stu-id="a1e94-129">Array of values</span></span>| <span data-ttu-id="a1e94-130">Staatilised menüü-üksused, mis seostavad menüü-üksuse nime staatilise saidi lingiga.</span><span class="sxs-lookup"><span data-stu-id="a1e94-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="a1e94-131">Menüü-üksusi saate luua muude menüü-üksuste all.</span><span class="sxs-lookup"><span data-stu-id="a1e94-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="a1e94-132">Vaikimisi kuvatakse staatilised menüüd juuretasandil ja need lisatakse kanali navigeerimishierarhiasse, kui see on olemas.</span><span class="sxs-lookup"><span data-stu-id="a1e94-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="a1e94-133">Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüüs kuvatav kategooria pilt.</span><span class="sxs-lookup"><span data-stu-id="a1e94-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="a1e94-134">![Kategooria piltidega navigeerimismenüü mooduli näide](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="a1e94-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="a1e94-135">Navigeerimismenüü mooduli lisamine päisemoodulisse</span><span class="sxs-lookup"><span data-stu-id="a1e94-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="a1e94-136">Üksikasjalikumat teavet selle kohta, kuidas lisada navigeerimismenüü moodulit päisemoodulisse, vt teemast [Päisemoodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="a1e94-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a1e94-137">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a1e94-137">Additional resources</span></span>

[<span data-ttu-id="a1e94-138">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="a1e94-138">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a1e94-139">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="a1e94-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a1e94-140">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="a1e94-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="a1e94-141">Päisemoodul</span><span class="sxs-lookup"><span data-stu-id="a1e94-141">Header module</span></span>](author-header-module.md)
