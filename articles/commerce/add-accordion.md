---
title: Akordionmoodul
description: See teema hõlmab akordionmooduleid ja selles kirjeldatakse, kuidas neid rakenduses Microsoft Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: ba973299291276fe48d82360e203ca28f02aaffb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796266"
---
# <a name="accordion-module"></a><span data-ttu-id="b007b-103">Akordionmoodul</span><span class="sxs-lookup"><span data-stu-id="b007b-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b007b-104">See teema hõlmab akordionmooduleid ja selles kirjeldatakse, kuidas neid rakenduses Microsoft Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="b007b-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b007b-105">Akordionmoodulid on konteinerilaadsed moodulid, mis pakuvad leheküljel teabe või moodulite korrastamiseks võimalust, mis sarnaneb ahendatava sahtliga.</span><span class="sxs-lookup"><span data-stu-id="b007b-105">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="b007b-106">Akordionmoodulit saab kasutada igal leheküljel.</span><span class="sxs-lookup"><span data-stu-id="b007b-106">An accordion module can be used on any page.</span></span>

<span data-ttu-id="b007b-107">Igasse akordionmoodulisse saab lisada ühe või enama akordioniüksuse mooduli.</span><span class="sxs-lookup"><span data-stu-id="b007b-107">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="b007b-108">Iga akordioniüksuse moodul tähistab ahendatavat sahtlit.</span><span class="sxs-lookup"><span data-stu-id="b007b-108">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="b007b-109">Igasse akordioniüksuse moodulisse saab lisada ühe või enama mooduli.</span><span class="sxs-lookup"><span data-stu-id="b007b-109">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="b007b-110">Akordioniüksuse moodulisse saab lisada igat tüüpi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="b007b-110">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="b007b-111">Järgmisel pildil on näide akordionmoodulist, mida kasutatakse kaupluse korduma kippuvate küsimuste (KKK) lehe teabe korrastamiseks.</span><span class="sxs-lookup"><span data-stu-id="b007b-111">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Akordionmooduli näide](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="b007b-113">Akordionmooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="b007b-113">Accordion module properties</span></span>

| <span data-ttu-id="b007b-114">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="b007b-114">Property name</span></span> | <span data-ttu-id="b007b-115">Väärtused</span><span class="sxs-lookup"><span data-stu-id="b007b-115">Values</span></span> | <span data-ttu-id="b007b-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b007b-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="b007b-117">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="b007b-117">Heading</span></span> | <span data-ttu-id="b007b-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="b007b-118">Text</span></span> | <span data-ttu-id="b007b-119">See atribuut määratleb akordionmooduli jaoks valikulise teksti pealkirja.</span><span class="sxs-lookup"><span data-stu-id="b007b-119">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="b007b-120">Laienda kõik</span><span class="sxs-lookup"><span data-stu-id="b007b-120">Expand All</span></span> | <span data-ttu-id="b007b-121">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="b007b-121">**True** or **False**</span></span> | <span data-ttu-id="b007b-122">Kui väärtuseks on seatud **Tõene**, on laiendamis-/ahendamisfunktsioon sisse lülitatud, nii et kõiki akordionmoodulis olevaid üksuseid saab laiendada ja ahendada.</span><span class="sxs-lookup"><span data-stu-id="b007b-122">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="b007b-123">Suhtlemisstiil</span><span class="sxs-lookup"><span data-stu-id="b007b-123">Interaction Style</span></span> | <span data-ttu-id="b007b-124">**Sõltumatu** või **Laienda ainult üht üksust**</span><span class="sxs-lookup"><span data-stu-id="b007b-124">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="b007b-125">See atribuut määratleb akordioniüksuste jaoks suhtlemisstiili.</span><span class="sxs-lookup"><span data-stu-id="b007b-125">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="b007b-126">Kui väärtuseks on seatud **Sõltumatu**, saab iga akordioniüksust laiendada või ahendada sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="b007b-126">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="b007b-127">Kui väärtuseks on seatud **Laienda ainult üht üksust**, saab korraga laiendada ainult üht üksust.</span><span class="sxs-lookup"><span data-stu-id="b007b-127">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="b007b-128">Üksuste laiendamisel ahendatakse enne laiendatud üksused.</span><span class="sxs-lookup"><span data-stu-id="b007b-128">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="b007b-129">Akordioniüksuse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="b007b-129">Accordion item module properties</span></span>

| <span data-ttu-id="b007b-130">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="b007b-130">Property name</span></span> | <span data-ttu-id="b007b-131">Väärtused</span><span class="sxs-lookup"><span data-stu-id="b007b-131">Values</span></span> | <span data-ttu-id="b007b-132">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b007b-132">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b007b-133">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="b007b-133">Title</span></span> | <span data-ttu-id="b007b-134">Tekst</span><span class="sxs-lookup"><span data-stu-id="b007b-134">Text</span></span> | <span data-ttu-id="b007b-135">See atribuut määratleb akordioniüksuse mooduli jaoks pealkirja teksti.</span><span class="sxs-lookup"><span data-stu-id="b007b-135">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="b007b-136">Pealkirja piirkonnale klõpsates saavad kasutajad jaotist laiendada või ahendada.</span><span class="sxs-lookup"><span data-stu-id="b007b-136">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="b007b-137">Laienda vaikimisi</span><span class="sxs-lookup"><span data-stu-id="b007b-137">Expand by default</span></span> | <span data-ttu-id="b007b-138">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="b007b-138">**True** or **False**</span></span> | <span data-ttu-id="b007b-139">Kui väärtuseks on seatud **Tõene**, laiendatakse akordioniüksus vaikimisi siis, kui leht on laaditud.</span><span class="sxs-lookup"><span data-stu-id="b007b-139">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="b007b-140">KKK lehele akordionmooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="b007b-140">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="b007b-141">KKK lehele akordionmooduli lisamiseks ja selle atribuutide seadistamiseks saidiehitajas toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b007b-141">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="b007b-142">Avage **Lehed** ja kasutage Fabrikami turundusmalli (või mis tahes piiranguteta malli) uue lehe loomiseks, mille nimi on **Kaupluse KKK**.</span><span class="sxs-lookup"><span data-stu-id="b007b-142">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="b007b-143">Valige **Vaikelehe** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b007b-143">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b007b-144">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b007b-144">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b007b-145">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b007b-145">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b007b-146">Valige dialoogiboksis **Lisa moodul** moodul **Akordion** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b007b-146">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b007b-147">Valige akordionmooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="b007b-147">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="b007b-148">Sisestage dialoogiboksis **Pealkiri** jaotises **Pealkirja tekst** tekst **Korduma kippuvad küsimused**.</span><span class="sxs-lookup"><span data-stu-id="b007b-148">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="b007b-149">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b007b-149">Then select **OK**.</span></span>
1. <span data-ttu-id="b007b-150">Valige akordionmooduli atribuutide paanil märkeruut **Kuva laiendamine** ja seejärel valige väljal **Suhtlemisstiil** suvand **Sõltumatu**.</span><span class="sxs-lookup"><span data-stu-id="b007b-150">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="b007b-151">Valige pesas **Akordion** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b007b-151">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b007b-152">Valige dialoogiboksis **Lisa moodul** moodul **Akordioniüksus** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b007b-152">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b007b-153">Sisestage akordioniüksuse mooduli atribuutide paanil jaotises **Pealkiri** pealkirja tekst (nt **Kuidas toimib tagastamine?**).</span><span class="sxs-lookup"><span data-stu-id="b007b-153">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="b007b-154">Valige pesas **Akordioniüksus** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b007b-154">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b007b-155">Valige dialoogiboksis **Lisa moodul** moodul **Tekstiplokk** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b007b-155">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b007b-156">Sisestage tekstiploki mooduli atribuutide paanil tekstilõik (nt **Tagastamiseks tuleb võtta ühendust kõnekeskusega. Tagastamiseks helistage numbrile 1-800-FABRIKAM. Toodetel on 30-päevane tagastuspoliitika. Tagastamist tuleb alustada selle ajavahemiku jooksul.**).</span><span class="sxs-lookup"><span data-stu-id="b007b-156">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="b007b-157">Lisage pesas **Akordion** veel mõni akordioniüksuse moodul.</span><span class="sxs-lookup"><span data-stu-id="b007b-157">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="b007b-158">Lisage igas akordioniüksuse moodulis sisuga tekstiploki moodul.</span><span class="sxs-lookup"><span data-stu-id="b007b-158">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="b007b-159">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="b007b-159">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="b007b-160">Lehel kuvatakse akordionmoodul, milles on teie lisatud sisu.</span><span class="sxs-lookup"><span data-stu-id="b007b-160">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="b007b-161">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="b007b-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b007b-162">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b007b-162">Additional resources</span></span>

[<span data-ttu-id="b007b-163">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="b007b-163">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b007b-164">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="b007b-164">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b007b-165">Vahekaardimoodul</span><span class="sxs-lookup"><span data-stu-id="b007b-165">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="b007b-166">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="b007b-166">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]