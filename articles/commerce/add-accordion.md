---
title: Akordionmoodul
description: See teema hõlmab akordionmooduleid ja selles kirjeldatakse, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2bb18539f610e5af05f8d9a20a0ba9f34db5c94f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411592"
---
# <a name="accordion-module"></a><span data-ttu-id="3ea27-103">Akordionmoodul</span><span class="sxs-lookup"><span data-stu-id="3ea27-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ea27-104">See teema hõlmab akordionmooduleid ja selles kirjeldatakse, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="3ea27-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3ea27-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="3ea27-105">Overview</span></span>

<span data-ttu-id="3ea27-106">Akordionmoodulid on konteinerilaadsed moodulid, mis pakuvad leheküljel teabe või moodulite korrastamiseks võimalust, mis sarnaneb ahendatava sahtliga.</span><span class="sxs-lookup"><span data-stu-id="3ea27-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="3ea27-107">Akordionmoodulit saab kasutada igal leheküljel.</span><span class="sxs-lookup"><span data-stu-id="3ea27-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="3ea27-108">Igasse akordionmoodulisse saab lisada ühe või enama akordioniüksuse mooduli.</span><span class="sxs-lookup"><span data-stu-id="3ea27-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="3ea27-109">Iga akordioniüksuse moodul tähistab ahendatavat sahtlit.</span><span class="sxs-lookup"><span data-stu-id="3ea27-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="3ea27-110">Igasse akordioniüksuse moodulisse saab lisada ühe või enama mooduli.</span><span class="sxs-lookup"><span data-stu-id="3ea27-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="3ea27-111">Akordioniüksuse moodulisse saab lisada igat tüüpi mooduleid.</span><span class="sxs-lookup"><span data-stu-id="3ea27-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="3ea27-112">Järgmisel pildil on näide akordionmoodulist, mida kasutatakse kaupluse korduma kippuvate küsimuste (KKK) lehe teabe korrastamiseks.</span><span class="sxs-lookup"><span data-stu-id="3ea27-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Akordionmooduli näide](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="3ea27-114">Akordionmooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="3ea27-114">Accordion module properties</span></span>

| <span data-ttu-id="3ea27-115">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="3ea27-115">Property name</span></span> | <span data-ttu-id="3ea27-116">Väärtused</span><span class="sxs-lookup"><span data-stu-id="3ea27-116">Values</span></span> | <span data-ttu-id="3ea27-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3ea27-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="3ea27-118">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="3ea27-118">Heading</span></span> | <span data-ttu-id="3ea27-119">Tekst</span><span class="sxs-lookup"><span data-stu-id="3ea27-119">Text</span></span> | <span data-ttu-id="3ea27-120">See atribuut määratleb akordionmooduli jaoks valikulise teksti pealkirja.</span><span class="sxs-lookup"><span data-stu-id="3ea27-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="3ea27-121">Laienda kõik</span><span class="sxs-lookup"><span data-stu-id="3ea27-121">Expand All</span></span> | <span data-ttu-id="3ea27-122">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="3ea27-122">**True** or **False**</span></span> | <span data-ttu-id="3ea27-123">Kui väärtuseks on seatud **Tõene**, on laiendamis-/ahendamisfunktsioon sisse lülitatud, nii et kõiki akordionmoodulis olevaid üksuseid saab laiendada ja ahendada.</span><span class="sxs-lookup"><span data-stu-id="3ea27-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="3ea27-124">Suhtlemisstiil</span><span class="sxs-lookup"><span data-stu-id="3ea27-124">Interaction Style</span></span> | <span data-ttu-id="3ea27-125">**Sõltumatu** või **Laienda ainult üht üksust**</span><span class="sxs-lookup"><span data-stu-id="3ea27-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="3ea27-126">See atribuut määratleb akordioniüksuste jaoks suhtlemisstiili.</span><span class="sxs-lookup"><span data-stu-id="3ea27-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="3ea27-127">Kui väärtuseks on seatud **Sõltumatu**, saab iga akordioniüksust laiendada või ahendada sõltumatult.</span><span class="sxs-lookup"><span data-stu-id="3ea27-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="3ea27-128">Kui väärtuseks on seatud **Laienda ainult üht üksust**, saab korraga laiendada ainult üht üksust.</span><span class="sxs-lookup"><span data-stu-id="3ea27-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="3ea27-129">Üksuste laiendamisel ahendatakse enne laiendatud üksused.</span><span class="sxs-lookup"><span data-stu-id="3ea27-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="3ea27-130">Akordioniüksuse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="3ea27-130">Accordion item module properties</span></span>

| <span data-ttu-id="3ea27-131">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="3ea27-131">Property name</span></span> | <span data-ttu-id="3ea27-132">Väärtused</span><span class="sxs-lookup"><span data-stu-id="3ea27-132">Values</span></span> | <span data-ttu-id="3ea27-133">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3ea27-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="3ea27-134">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="3ea27-134">Title</span></span> | <span data-ttu-id="3ea27-135">Tekst</span><span class="sxs-lookup"><span data-stu-id="3ea27-135">Text</span></span> | <span data-ttu-id="3ea27-136">See atribuut määratleb akordioniüksuse mooduli jaoks pealkirja teksti.</span><span class="sxs-lookup"><span data-stu-id="3ea27-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="3ea27-137">Pealkirja piirkonnale klõpsates saavad kasutajad jaotist laiendada või ahendada.</span><span class="sxs-lookup"><span data-stu-id="3ea27-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="3ea27-138">Laienda vaikimisi</span><span class="sxs-lookup"><span data-stu-id="3ea27-138">Expand by default</span></span> | <span data-ttu-id="3ea27-139">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="3ea27-139">**True** or **False**</span></span> | <span data-ttu-id="3ea27-140">Kui väärtuseks on seatud **Tõene**, laiendatakse akordioniüksus vaikimisi siis, kui leht on laaditud.</span><span class="sxs-lookup"><span data-stu-id="3ea27-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="3ea27-141">KKK lehele akordionmooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="3ea27-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="3ea27-142">KKK lehele akordionmooduli lisamiseks ja selle atribuutide seadistamiseks saidiehitajas toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3ea27-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="3ea27-143">Avage **Lehed** ja kasutage Fabrikami turundusmalli (või mis tahes piiranguteta malli) uue lehe loomiseks, mille nimi on **Kaupluse KKK**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="3ea27-144">Valige **Vaikelehe** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3ea27-145">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3ea27-146">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3ea27-147">Valige dialoogiboksis **Lisa moodul** moodul **Akordion** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3ea27-148">Valige akordionmooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="3ea27-149">Sisestage dialoogiboksis **Pealkiri** jaotises **Pealkirja tekst** tekst **Korduma kippuvad küsimused**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="3ea27-150">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-150">Then select **OK**.</span></span>
1. <span data-ttu-id="3ea27-151">Valige akordionmooduli atribuutide paanil märkeruut **Kuva laiendamine** ja seejärel valige väljal **Suhtlemisstiil** suvand **Sõltumatu**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="3ea27-152">Valige pesas **Akordion** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3ea27-153">Valige dialoogiboksis **Lisa moodul** moodul **Akordioniüksus** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3ea27-154">Sisestage akordioniüksuse mooduli atribuutide paanil jaotises **Pealkiri** pealkirja tekst (nt **Kuidas toimib tagastamine?**).</span><span class="sxs-lookup"><span data-stu-id="3ea27-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="3ea27-155">Valige pesas **Akordioniüksus** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3ea27-156">Valige dialoogiboksis **Lisa moodul** moodul **Tekstiplokk** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3ea27-157">Sisestage tekstiploki mooduli atribuutide paanil tekstilõik (nt **Tagastamiseks tuleb võtta ühendust kõnekeskusega. Tagastamiseks helistage numbrile 1-800-FABRIKAM. Toodetel on 30-päevane tagastuspoliitika. Tagastamist tuleb alustada selle ajavahemiku jooksul.**).</span><span class="sxs-lookup"><span data-stu-id="3ea27-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="3ea27-158">Lisage pesas **Akordion** veel mõni akordioniüksuse moodul.</span><span class="sxs-lookup"><span data-stu-id="3ea27-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="3ea27-159">Lisage igas akordioniüksuse moodulis sisuga tekstiploki moodul.</span><span class="sxs-lookup"><span data-stu-id="3ea27-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="3ea27-160">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="3ea27-161">Lehel kuvatakse akordionmoodul, milles on teie lisatud sisu.</span><span class="sxs-lookup"><span data-stu-id="3ea27-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="3ea27-162">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="3ea27-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ea27-163">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3ea27-163">Additional resources</span></span>

[<span data-ttu-id="3ea27-164">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="3ea27-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3ea27-165">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="3ea27-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3ea27-166">Vahekaardimoodul</span><span class="sxs-lookup"><span data-stu-id="3ea27-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="3ea27-167">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="3ea27-167">Text block module</span></span>](add-content-rich-block.md)
