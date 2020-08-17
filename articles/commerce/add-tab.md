---
title: Vahekaardi moodul
description: See teema hõlmab vahekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: b4187dfd704c78d506d7840b04c986687fe807a3
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621009"
---
# <a name="tab-module"></a><span data-ttu-id="b1495-103">Vahekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="b1495-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b1495-104">See teema hõlmab vahekaardi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="b1495-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b1495-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b1495-105">Overview</span></span>

<span data-ttu-id="b1495-106">Vahekaardi moodulid on konteinerilaadsed moodulid, mida kasutatakse vahekaartide abil saidi lehel teabe korrastamiseks.</span><span class="sxs-lookup"><span data-stu-id="b1495-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="b1495-107">Neid saab kasutada igal lehel, kus teave tuleb esitada vahekaartidel.</span><span class="sxs-lookup"><span data-stu-id="b1495-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="b1495-108">Igas vahekaardi moodulis saab lisada ühe või enama vahekaardi mooduli.</span><span class="sxs-lookup"><span data-stu-id="b1495-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="b1495-109">Iga vahekaardi moodul tähistab üht vahekaarti. Igas vahekaardi moodulis saab lisada ühe või enama mooduli.</span><span class="sxs-lookup"><span data-stu-id="b1495-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="b1495-110">Vahekaardi moodulisse saab lisada igat tüüpi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="b1495-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="b1495-111">Järgmisel pildil on näide vahekaardi moodulist saidi lehel.</span><span class="sxs-lookup"><span data-stu-id="b1495-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="b1495-112">Näites on valitud vahekaart **Lähetamine**.</span><span class="sxs-lookup"><span data-stu-id="b1495-112">In this example, the **Shipping** tab selected.</span></span>

![Vahekaardi mooduli näide](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="b1495-114">Vahekaardi mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="b1495-114">Tab module properties</span></span>

| <span data-ttu-id="b1495-115">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="b1495-115">Property name</span></span> | <span data-ttu-id="b1495-116">Väärtused</span><span class="sxs-lookup"><span data-stu-id="b1495-116">Values</span></span> | <span data-ttu-id="b1495-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b1495-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b1495-118">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="b1495-118">Heading</span></span> | <span data-ttu-id="b1495-119">Tekst</span><span class="sxs-lookup"><span data-stu-id="b1495-119">Text</span></span> | <span data-ttu-id="b1495-120">See atribuut määratleb vahekaardi mooduli jaoks valikulise teksti pealkirja.</span><span class="sxs-lookup"><span data-stu-id="b1495-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="b1495-121">Aktiivse vahekaardi indeks</span><span class="sxs-lookup"><span data-stu-id="b1495-121">Active Tab Index</span></span> | <span data-ttu-id="b1495-122">Number</span><span class="sxs-lookup"><span data-stu-id="b1495-122">Number</span></span> | <span data-ttu-id="b1495-123">See atribuut määratleb vahekaardi, mis peaks lehe laadimisel olema vaikimisi aktiivne.</span><span class="sxs-lookup"><span data-stu-id="b1495-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="b1495-124">Kui väärtust ei esitada, siis on vaikimisi aktiivne esimene vahekaart.</span><span class="sxs-lookup"><span data-stu-id="b1495-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="b1495-125">Vahekaardi üksuse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="b1495-125">Tab item module properties</span></span>

| <span data-ttu-id="b1495-126">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="b1495-126">Property name</span></span> | <span data-ttu-id="b1495-127">Väärtused</span><span class="sxs-lookup"><span data-stu-id="b1495-127">Values</span></span> | <span data-ttu-id="b1495-128">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b1495-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b1495-129">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="b1495-129">Title</span></span> | <span data-ttu-id="b1495-130">Tekst</span><span class="sxs-lookup"><span data-stu-id="b1495-130">Text</span></span> | <span data-ttu-id="b1495-131">See atribuut määratleb vahekaardi üksuse mooduli jaoks pealkirja teksti.</span><span class="sxs-lookup"><span data-stu-id="b1495-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="b1495-132">Lehele vahekaardi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="b1495-132">Add a tab module to a page</span></span>

<span data-ttu-id="b1495-133">Lehele vahekaardi mooduli lisamiseks ja atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b1495-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="b1495-134">Kasutage Fabrikami turundusmalli (või mis tahes piiranguteta malli) uue lehe loomiseks, mille nimi on **Kaupluse poliitikate leht**.</span><span class="sxs-lookup"><span data-stu-id="b1495-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="b1495-135">Valige **Vaikelehe** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b1495-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1495-136">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1495-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1495-137">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b1495-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1495-138">Valige dialoogiboksis **Lisa moodul** moodul **Vahekaart** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1495-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1495-139">Valige vahekaardi mooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="b1495-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="b1495-140">Sisestage dialoogiboksis **Päis** jaotisesse **Päise tekst** päise tekst (nt **Poliitikad**).</span><span class="sxs-lookup"><span data-stu-id="b1495-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="b1495-141">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1495-141">Then select **OK**.</span></span>
1. <span data-ttu-id="b1495-142">Valige pesas **Vahekaart** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b1495-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1495-143">Valige dialoogiboksis **Lisa moodul** moodul **Vahekaardi üksus** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1495-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1495-144">Sisestage vahekaardi üksuse mooduli atribuutide paanil jaotises **Pealkiri** pealkirja tekst (nt **Tarne**).</span><span class="sxs-lookup"><span data-stu-id="b1495-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="b1495-145">Valige pesas **Vahekaardi üksus** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b1495-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1495-146">Valige dialoogiboksis **Lisa moodul** moodul **Tekstiplokk** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1495-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1495-147">Lisage tekstiploki mooduli atribuutide paani väljale **Rikastekst** tekstilõik.</span><span class="sxs-lookup"><span data-stu-id="b1495-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="b1495-148">Lisage pesas **Vahekaart** veel mõned pealkirjaga vahekaardi üksuse moodulid.</span><span class="sxs-lookup"><span data-stu-id="b1495-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="b1495-149">Lisage igas vahekaardi üksuse moodulis sisuga tekstiploki moodul.</span><span class="sxs-lookup"><span data-stu-id="b1495-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="b1495-150">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="b1495-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="b1495-151">Lehel kuvatakse vahekaardi moodul, mis sisaldab teie lisatud sisuga vahekaardi üksuse mooduleid.</span><span class="sxs-lookup"><span data-stu-id="b1495-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="b1495-152">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="b1495-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1495-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b1495-153">Additional resources</span></span>

[<span data-ttu-id="b1495-154">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="b1495-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b1495-155">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="b1495-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b1495-156">Akordionmoodul</span><span class="sxs-lookup"><span data-stu-id="b1495-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="b1495-157">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="b1495-157">Text block module</span></span>](add-content-rich-block.md)
