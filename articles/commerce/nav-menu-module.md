---
title: Navigeerimismenüü moodul
description: See teema hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055733"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="59ace-103">Navigeerimismenüü moodul</span><span class="sxs-lookup"><span data-stu-id="59ace-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="59ace-104">See teema hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="59ace-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="59ace-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="59ace-105">Overview</span></span>

<span data-ttu-id="59ace-106">Navigeerimismenüü moodulite peamine eesmärk on võimaldada saidi kasutajatel sirvida tooteid ja saite vastavalt Dynamics 365 Commerce'i peakontoris määratletud kanali navigeerimishierarhiale.</span><span class="sxs-lookup"><span data-stu-id="59ace-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="59ace-107">Navigeerimismenüü moodulis konfigureeritud üksused ilmuvad saidi päise navigeerimises.</span><span class="sxs-lookup"><span data-stu-id="59ace-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="59ace-108">Navigeerimismenüü moodulid toetavad ka staatilisi menüü-üksusi, mis lingivad e-kaubanduse saidi muudele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="59ace-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="59ace-109">Navigeerimismenüü mooduli saab lisada lehe päisemoodulisse.</span><span class="sxs-lookup"><span data-stu-id="59ace-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="59ace-110">Fabrikami kujunduse navigeerimismenüüs kuvatakse vaikimisi kaks taset.</span><span class="sxs-lookup"><span data-stu-id="59ace-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="59ace-111">Starteri kujunduse navigeerimismenüüs kuvatakse vaikimisi kolm taset.</span><span class="sxs-lookup"><span data-stu-id="59ace-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="59ace-112">Tasemete arvu muutmiseks on kujunduses nõutav vaate laiend.</span><span class="sxs-lookup"><span data-stu-id="59ace-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="59ace-113">Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüü näide, millel on kaks kategooriahierarhia taset ja mõned staatilised menüü-üksused.</span><span class="sxs-lookup"><span data-stu-id="59ace-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="59ace-114">![Navigeerimismenüü mooduli näide](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="59ace-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="59ace-115">Navigeerimismenüü mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="59ace-115">Navigation menu module properties</span></span>

| <span data-ttu-id="59ace-116">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="59ace-116">Property name</span></span>             | <span data-ttu-id="59ace-117">Väärtus</span><span class="sxs-lookup"><span data-stu-id="59ace-117">Value</span></span>                 | <span data-ttu-id="59ace-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="59ace-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="59ace-119">Allikas</span><span class="sxs-lookup"><span data-stu-id="59ace-119">Source</span></span>                  | <span data-ttu-id="59ace-120">**Jaemüük** , **Käsitsi koostamine** , **Jaemüük ja käsitsi koostamine**</span><span class="sxs-lookup"><span data-stu-id="59ace-120">**Retail** , **Manual authoring** , **Retail and manual authoring**</span></span> | <span data-ttu-id="59ace-121">Väärtus **Jaemüük** võimaldab navigeerimismenüüs kuvada kanali navigeerimishierarhia Commerce'i peakontorist.</span><span class="sxs-lookup"><span data-stu-id="59ace-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="59ace-122">Väärtus **Käsitsi koostamine** võimaldab staatiliste menüüde üksusi kureerida.</span><span class="sxs-lookup"><span data-stu-id="59ace-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="59ace-123">Väärtus **Jaemüük ja käsitsi koostamine** võimaldab mõlemat.</span><span class="sxs-lookup"><span data-stu-id="59ace-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="59ace-124">Kategooria piltide kuvamine</span><span class="sxs-lookup"><span data-stu-id="59ace-124">Show category images</span></span> | <span data-ttu-id="59ace-125">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="59ace-125">**True** or **False**</span></span>    | <span data-ttu-id="59ace-126">Kui see on lubatud, kuvatakse navigeerimismenüüs kategooria pildid, nagu on määratletud iga kategooria kohta Commerce’i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="59ace-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="59ace-127">Lisatud Commerce'i väljalaskesse 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="59ace-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="59ace-128">Mitme tasemega navigeerimismenüü lubamine</span><span class="sxs-lookup"><span data-stu-id="59ace-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="59ace-129">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="59ace-129">**True** or **False**</span></span> | <span data-ttu-id="59ace-130">Kui see atribuut on lubatud, võib navigeerimismenüü kuvada navigeerimise hierarhia mitut taset.</span><span class="sxs-lookup"><span data-stu-id="59ace-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="59ace-131">See funktsioon on saadaval Dynamics 365 Commerce'i versioonis 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="59ace-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="59ace-132">Tasemete arv</span><span class="sxs-lookup"><span data-stu-id="59ace-132">Number of levels</span></span> | <span data-ttu-id="59ace-133">täisarv</span><span class="sxs-lookup"><span data-stu-id="59ace-133">integer</span></span> | <span data-ttu-id="59ace-134">See atribuut määratleb tasemete numbrid, mis tuleb kuvada, kui atribuudi **Luba mitmetasandiline navigeerimismenüü** väärtuseks on seatud **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="59ace-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="59ace-135">Staatiline menüü-üksus</span><span class="sxs-lookup"><span data-stu-id="59ace-135">Static menu item</span></span>| <span data-ttu-id="59ace-136">Väärtuste massiiv</span><span class="sxs-lookup"><span data-stu-id="59ace-136">Array of values</span></span>| <span data-ttu-id="59ace-137">Staatilised menüü-üksused, mis seostavad menüü-üksuse nime staatilise saidi lingiga.</span><span class="sxs-lookup"><span data-stu-id="59ace-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="59ace-138">Menüü-üksusi saate luua muude menüü-üksuste all.</span><span class="sxs-lookup"><span data-stu-id="59ace-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="59ace-139">Vaikimisi kuvatakse staatilised menüüd juuretasandil ja need lisatakse kanali navigeerimishierarhiasse, kui see on olemas.</span><span class="sxs-lookup"><span data-stu-id="59ace-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="59ace-140">Juurmenüü kuvamine</span><span class="sxs-lookup"><span data-stu-id="59ace-140">Show root menu</span></span> | <span data-ttu-id="59ace-141">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="59ace-141">**True** or **False**</span></span> | <span data-ttu-id="59ace-142">Kui see atribuut on lubatud, saab navigeerimismenüü määratleda kohandatud juure alusel (nt **Osta kohe** ).</span><span class="sxs-lookup"><span data-stu-id="59ace-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now** ).</span></span> <span data-ttu-id="59ace-143">See funktsioon on saadaval Dynamics 365 Commerce'i versioonis 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="59ace-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="59ace-144">Juurmenüü</span><span class="sxs-lookup"><span data-stu-id="59ace-144">Root menu</span></span> | <span data-ttu-id="59ace-145">string</span><span class="sxs-lookup"><span data-stu-id="59ace-145">string</span></span> | <span data-ttu-id="59ace-146">Seda atribuuti saab kasutada kohandatud juure teksti määratlemiseks, kui atribuudi **Kuva juurmenüü** väärtuseks on seatud **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="59ace-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="59ace-147">Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüüs kuvatav kategooria pilt.</span><span class="sxs-lookup"><span data-stu-id="59ace-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="59ace-148">![Kategooria piltidega navigeerimismenüü mooduli näide](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="59ace-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="59ace-149">Navigeerimismenüü mooduli lisamine päisemoodulisse</span><span class="sxs-lookup"><span data-stu-id="59ace-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="59ace-150">Üksikasjalikumat teavet selle kohta, kuidas lisada navigeerimismenüü moodulit päisemoodulisse, vt teemast [Päisemoodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="59ace-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59ace-151">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="59ace-151">Additional resources</span></span>

[<span data-ttu-id="59ace-152">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="59ace-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="59ace-153">Lingireamoodul</span><span class="sxs-lookup"><span data-stu-id="59ace-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="59ace-154">Saidi valija moodul</span><span class="sxs-lookup"><span data-stu-id="59ace-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="59ace-155">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="59ace-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="59ace-156">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="59ace-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="59ace-157">Päisemoodul</span><span class="sxs-lookup"><span data-stu-id="59ace-157">Header module</span></span>](author-header-module.md)
