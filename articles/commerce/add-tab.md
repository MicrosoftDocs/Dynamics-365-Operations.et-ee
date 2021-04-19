---
title: Vahekaardi moodul
description: See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c865d5e055e3fadf2dda225b49f13a163974768f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797451"
---
# <a name="tab-module"></a><span data-ttu-id="e1b4d-103">Vahekaardimoodul</span><span class="sxs-lookup"><span data-stu-id="e1b4d-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1b4d-104">See teema hõlmab ostukasti mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e1b4d-105">Vahekaardi moodulid on konteinerilaadsed moodulid, mida kasutatakse vahekaartide abil saidi lehel teabe korrastamiseks.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="e1b4d-106">Neid saab kasutada igal lehel, kus teave tuleb esitada vahekaartidel.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="e1b4d-107">Igas vahekaardi moodulis saab lisada ühe või enama vahekaardi mooduli.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="e1b4d-108">Iga vahekaardi moodul tähistab üht vahekaarti. Igas vahekaardi moodulis saab lisada ühe või enama mooduli.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="e1b4d-109">Vahekaardi moodulisse saab lisada igat tüüpi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="e1b4d-110">Järgmisel pildil on näide vahekaardi moodulist saidi lehel.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="e1b4d-111">Näites on valitud vahekaart **Lähetamine**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-111">In this example, the **Shipping** tab selected.</span></span>

![Vahekaardi mooduli näide](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="e1b4d-113">Vahekaardi mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="e1b4d-113">Tab module properties</span></span>

| <span data-ttu-id="e1b4d-114">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="e1b4d-114">Property name</span></span> | <span data-ttu-id="e1b4d-115">Väärtused</span><span class="sxs-lookup"><span data-stu-id="e1b4d-115">Values</span></span> | <span data-ttu-id="e1b4d-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e1b4d-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e1b4d-117">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="e1b4d-117">Heading</span></span> | <span data-ttu-id="e1b4d-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="e1b4d-118">Text</span></span> | <span data-ttu-id="e1b4d-119">See atribuut määratleb vahekaardi mooduli jaoks valikulise teksti pealkirja.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="e1b4d-120">Aktiivse vahekaardi indeks</span><span class="sxs-lookup"><span data-stu-id="e1b4d-120">Active Tab Index</span></span> | <span data-ttu-id="e1b4d-121">Number</span><span class="sxs-lookup"><span data-stu-id="e1b4d-121">Number</span></span> | <span data-ttu-id="e1b4d-122">See atribuut määratleb vahekaardi, mis peaks lehe laadimisel olema vaikimisi aktiivne.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="e1b4d-123">Kui väärtust ei esitada, siis on vaikimisi aktiivne esimene vahekaart.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="e1b4d-124">Vahekaardi üksuse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="e1b4d-124">Tab item module properties</span></span>

| <span data-ttu-id="e1b4d-125">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="e1b4d-125">Property name</span></span> | <span data-ttu-id="e1b4d-126">Väärtused</span><span class="sxs-lookup"><span data-stu-id="e1b4d-126">Values</span></span> | <span data-ttu-id="e1b4d-127">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e1b4d-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="e1b4d-128">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="e1b4d-128">Title</span></span> | <span data-ttu-id="e1b4d-129">Tekst</span><span class="sxs-lookup"><span data-stu-id="e1b4d-129">Text</span></span> | <span data-ttu-id="e1b4d-130">See atribuut määratleb vahekaardi üksuse mooduli jaoks pealkirja teksti.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="e1b4d-131">Lehele vahekaardi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="e1b4d-131">Add a tab module to a page</span></span>

<span data-ttu-id="e1b4d-132">Lehele vahekaardi mooduli lisamiseks ja atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="e1b4d-133">Kasutage Fabrikami turundusmalli (või mis tahes piiranguteta malli) uue lehe loomiseks, mille nimi on **Kaupluse poliitikate leht**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="e1b4d-134">Valige **Vaikelehe** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e1b4d-135">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e1b4d-136">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e1b4d-137">Valige dialoogiboksis **Lisa moodul** moodul **Vahekaart** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e1b4d-138">Valige vahekaardi mooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="e1b4d-139">Sisestage dialoogiboksis **Päis** jaotisesse **Päise tekst** päise tekst (nt **Poliitikad**).</span><span class="sxs-lookup"><span data-stu-id="e1b4d-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="e1b4d-140">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-140">Then select **OK**.</span></span>
1. <span data-ttu-id="e1b4d-141">Valige pesas **Vahekaart** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e1b4d-142">Valige dialoogiboksis **Lisa moodul** moodul **Vahekaardi üksus** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e1b4d-143">Sisestage vahekaardi üksuse mooduli atribuutide paanil jaotises **Pealkiri** pealkirja tekst (nt **Tarne**).</span><span class="sxs-lookup"><span data-stu-id="e1b4d-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="e1b4d-144">Valige pesas **Vahekaardi üksus** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e1b4d-145">Valige dialoogiboksis **Lisa moodul** moodul **Tekstiplokk** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="e1b4d-146">Lisage tekstiploki mooduli atribuutide paani väljale **Rikastekst** tekstilõik.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="e1b4d-147">Lisage pesas **Vahekaart** veel mõned pealkirjaga vahekaardi üksuse moodulid.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="e1b4d-148">Lisage igas vahekaardi üksuse moodulis sisuga tekstiploki moodul.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="e1b4d-149">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="e1b4d-150">Lehel kuvatakse vahekaardi moodul, mis sisaldab teie lisatud sisuga vahekaardi üksuse mooduleid.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="e1b4d-151">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="e1b4d-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e1b4d-152">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e1b4d-152">Additional resources</span></span>

[<span data-ttu-id="e1b4d-153">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="e1b4d-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e1b4d-154">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="e1b4d-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e1b4d-155">Akordionmoodul</span><span class="sxs-lookup"><span data-stu-id="e1b4d-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="e1b4d-156">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="e1b4d-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]