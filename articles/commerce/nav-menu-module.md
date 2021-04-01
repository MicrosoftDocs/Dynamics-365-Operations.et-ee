---
title: Navigeerimismenüü moodul
description: See teema hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3461993e2bd59d66be1640331e4ef315a078469
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251207"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="0c908-103">Navigeerimismenüü moodul</span><span class="sxs-lookup"><span data-stu-id="0c908-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="0c908-104">See teema hõlmab navigeerimismenüü mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="0c908-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0c908-105">Navigeerimismenüü moodulite peamine eesmärk on võimaldada saidi kasutajatel sirvida tooteid ja saite vastavalt Dynamics 365 Commerce'i peakontoris määratletud kanali navigeerimishierarhiale.</span><span class="sxs-lookup"><span data-stu-id="0c908-105">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="0c908-106">Navigeerimismenüü moodulis konfigureeritud üksused ilmuvad saidi päise navigeerimises.</span><span class="sxs-lookup"><span data-stu-id="0c908-106">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="0c908-107">Navigeerimismenüü moodulid toetavad ka staatilisi menüü-üksusi, mis lingivad e-kaubanduse saidi muudele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="0c908-107">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="0c908-108">Navigeerimismenüü mooduli saab lisada lehe päisemoodulisse.</span><span class="sxs-lookup"><span data-stu-id="0c908-108">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="0c908-109">Fabrikami kujunduse navigeerimismenüüs kuvatakse vaikimisi kaks taset.</span><span class="sxs-lookup"><span data-stu-id="0c908-109">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="0c908-110">Starteri kujunduse navigeerimismenüüs kuvatakse vaikimisi kolm taset.</span><span class="sxs-lookup"><span data-stu-id="0c908-110">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="0c908-111">Tasemete arvu muutmiseks on kujunduses nõutav vaate laiend.</span><span class="sxs-lookup"><span data-stu-id="0c908-111">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="0c908-112">Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüü näide, millel on kaks kategooriahierarhia taset ja mõned staatilised menüü-üksused.</span><span class="sxs-lookup"><span data-stu-id="0c908-112">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="0c908-113">![Navigeerimismenüü mooduli näide](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="0c908-113">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="0c908-114">Navigeerimismenüü mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="0c908-114">Navigation menu module properties</span></span>

| <span data-ttu-id="0c908-115">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="0c908-115">Property name</span></span>             | <span data-ttu-id="0c908-116">Väärtus</span><span class="sxs-lookup"><span data-stu-id="0c908-116">Value</span></span>                 | <span data-ttu-id="0c908-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0c908-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="0c908-118">Allikas</span><span class="sxs-lookup"><span data-stu-id="0c908-118">Source</span></span>                  | <span data-ttu-id="0c908-119">**Jaemüük**, **Käsitsi koostamine**, **Jaemüük ja käsitsi koostamine**</span><span class="sxs-lookup"><span data-stu-id="0c908-119">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="0c908-120">Väärtus **Jaemüük** võimaldab navigeerimismenüüs kuvada kanali navigeerimishierarhia Commerce'i peakontorist.</span><span class="sxs-lookup"><span data-stu-id="0c908-120">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="0c908-121">Väärtus **Käsitsi koostamine** võimaldab staatiliste menüüde üksusi kureerida.</span><span class="sxs-lookup"><span data-stu-id="0c908-121">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="0c908-122">Väärtus **Jaemüük ja käsitsi koostamine** võimaldab mõlemat.</span><span class="sxs-lookup"><span data-stu-id="0c908-122">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="0c908-123">Kategooria piltide kuvamine</span><span class="sxs-lookup"><span data-stu-id="0c908-123">Show category images</span></span> | <span data-ttu-id="0c908-124">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="0c908-124">**True** or **False**</span></span>    | <span data-ttu-id="0c908-125">Kui see on lubatud, kuvatakse navigeerimismenüüs kategooria pildid, nagu on määratletud iga kategooria kohta Commerce’i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="0c908-125">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="0c908-126">Lisatud Commerce'i väljalaskesse 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="0c908-126">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="0c908-127">Kuva kampaaniad</span><span class="sxs-lookup"><span data-stu-id="0c908-127">Show promotions</span></span> | <span data-ttu-id="0c908-128">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="0c908-128">**True** or **False**</span></span> | <span data-ttu-id="0c908-129">Kui see atribuut on lubatud, saab kampaaniaid konfigureerida piltide, linkide ja teksti abil.</span><span class="sxs-lookup"><span data-stu-id="0c908-129">When this property is enabled, promotions can be configured by using images, links, and text.</span></span> <span data-ttu-id="0c908-130">See atribuut lisati Commerce'i versiooni 10.0.17 väljalaskesse.</span><span class="sxs-lookup"><span data-stu-id="0c908-130">This property was added in the Commerce version 10.0.17 release.</span></span> |
| <span data-ttu-id="0c908-131">Kampaaniate lisamine</span><span class="sxs-lookup"><span data-stu-id="0c908-131">Add promotions</span></span> | <span data-ttu-id="0c908-132">Tekst, pilt või link</span><span class="sxs-lookup"><span data-stu-id="0c908-132">Text, image, or link</span></span> | <span data-ttu-id="0c908-133">Kui atribuut **Kuva kampaaniad** on lubatud, saate lisada navigeerimismenüüst kampaaniasisuna teksti, pildi või lingi.</span><span class="sxs-lookup"><span data-stu-id="0c908-133">When the **Show promotions** property is enabled, you can add text, an image, or a link as promotional content on the navigation menu.</span></span> |
| <span data-ttu-id="0c908-134">Mitme tasemega navigeerimismenüü lubamine</span><span class="sxs-lookup"><span data-stu-id="0c908-134">Enable multi-level navigation menu</span></span> | <span data-ttu-id="0c908-135">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="0c908-135">**True** or **False**</span></span> | <span data-ttu-id="0c908-136">Kui see atribuut on lubatud, võib navigeerimismenüü kuvada navigeerimise hierarhia mitut taset.</span><span class="sxs-lookup"><span data-stu-id="0c908-136">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="0c908-137">See funktsioon on saadaval Commerce'i versiooni 10.0.15 väljalaskes.</span><span class="sxs-lookup"><span data-stu-id="0c908-137">This feature is available in the Commerce version 10.0.15 release.</span></span> |
| <span data-ttu-id="0c908-138">Tasemete arv</span><span class="sxs-lookup"><span data-stu-id="0c908-138">Number of levels</span></span> | <span data-ttu-id="0c908-139">täisarv</span><span class="sxs-lookup"><span data-stu-id="0c908-139">integer</span></span> | <span data-ttu-id="0c908-140">See atribuut määratleb tasemete numbrid, mis tuleb kuvada, kui atribuudi **Luba mitmetasandiline navigeerimismenüü** väärtuseks on seatud **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="0c908-140">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="0c908-141">Staatiline menüü-üksus</span><span class="sxs-lookup"><span data-stu-id="0c908-141">Static menu item</span></span>| <span data-ttu-id="0c908-142">Väärtuste massiiv</span><span class="sxs-lookup"><span data-stu-id="0c908-142">Array of values</span></span>| <span data-ttu-id="0c908-143">Staatilised menüü-üksused, mis seostavad menüü-üksuse nime staatilise saidi lingiga.</span><span class="sxs-lookup"><span data-stu-id="0c908-143">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="0c908-144">Menüü-üksusi saate luua muude menüü-üksuste all.</span><span class="sxs-lookup"><span data-stu-id="0c908-144">You can create menu items below other menu items.</span></span> <span data-ttu-id="0c908-145">Vaikimisi kuvatakse staatilised menüüd juuretasandil ja need lisatakse kanali navigeerimishierarhiasse, kui see on olemas.</span><span class="sxs-lookup"><span data-stu-id="0c908-145">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="0c908-146">Juurmenüü kuvamine</span><span class="sxs-lookup"><span data-stu-id="0c908-146">Show root menu</span></span> | <span data-ttu-id="0c908-147">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="0c908-147">**True** or **False**</span></span> | <span data-ttu-id="0c908-148">Kui see atribuut on lubatud, saab navigeerimismenüü määratleda kohandatud juure alusel (nt **Osta kohe**).</span><span class="sxs-lookup"><span data-stu-id="0c908-148">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="0c908-149">See funktsioon on saadaval Dynamics 365 Commerce'i versioonis 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="0c908-149">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="0c908-150">Juurmenüü</span><span class="sxs-lookup"><span data-stu-id="0c908-150">Root menu</span></span> | <span data-ttu-id="0c908-151">string</span><span class="sxs-lookup"><span data-stu-id="0c908-151">string</span></span> | <span data-ttu-id="0c908-152">Seda atribuuti saab kasutada kohandatud juure teksti määratlemiseks, kui atribuudi **Kuva juurmenüü** väärtuseks on seatud **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="0c908-152">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="0c908-153">Järgmisel joonisel on kujutatud Fabrikami saidi navigeerimismenüüs kuvatav kategooria pilt.</span><span class="sxs-lookup"><span data-stu-id="0c908-153">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="0c908-154">![Kategooria piltidega navigeerimismenüü mooduli näide](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="0c908-154">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="0c908-155">Navigeerimismenüü mooduli lisamine päisemoodulisse</span><span class="sxs-lookup"><span data-stu-id="0c908-155">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="0c908-156">Üksikasjalikumat teavet selle kohta, kuidas lisada navigeerimismenüü moodulit päisemoodulisse, vt teemast [Päisemoodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="0c908-156">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c908-157">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0c908-157">Additional resources</span></span>

[<span data-ttu-id="0c908-158">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="0c908-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0c908-159">Lingireamoodul</span><span class="sxs-lookup"><span data-stu-id="0c908-159">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="0c908-160">Saidi valija moodul</span><span class="sxs-lookup"><span data-stu-id="0c908-160">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="0c908-161">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="0c908-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0c908-162">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="0c908-162">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="0c908-163">Päisemoodul</span><span class="sxs-lookup"><span data-stu-id="0c908-163">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]