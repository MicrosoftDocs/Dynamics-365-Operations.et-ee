---
title: Moodulitega töötamine
description: Selles teemas kirjeldatakse, kuidas ja millal kasutada mooduleid rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/31/2020
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
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: da430857801d8007244c04aadd325e99c0b882c5
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646011"
---
# <a name="work-with-modules"></a><span data-ttu-id="3eb1a-103">Moodulitega töötamine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-103">Work with modules</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3eb1a-104">Selles teemas kirjeldatakse, kuidas ja millal kasutada mooduleid rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3eb1a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="3eb1a-105">Overview</span></span>

<span data-ttu-id="3eb1a-106">Moodulid on loogilised koosteüksused, mis moodustavad teie lehe struktuuri, neil on mitmesuguseid eesmärke ja ulatusi.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="3eb1a-107">Mõni moodul on kõrgetasemeline konteiner ning nende ainus eesmärk on hoida ja korraldada teisi mooduleid (alammooduleid).</span><span class="sxs-lookup"><span data-stu-id="3eb1a-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="3eb1a-108">Teistel moodulitel, näiteks lihtsal pildipaigutusmoodulil, on väga konkreetne eesmärk.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="3eb1a-109">Teised moodulid, nt karussellmoodul, jäävad kusagile nende kahe kategooria vahele.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="3eb1a-110">Vaikimisi sisaldab teie Dynamics 365 Commerce’i sait alustuskomplekti mooduli teeki, mille abil saate luua kõige üldisemaid e-kaubanduse stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="3eb1a-111">Vaid neid mooduleid kasutades peaksite saama luua täieliku e-kaubanduse saidi.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="3eb1a-112">Kuid võib-olla soovite neid mooduleid kohandada või luua uusi, kohandatud mooduleid, mis vastavad konkreetsetele vajadustele.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="3eb1a-113">Kui soovite luua kohandatud mooduleid, aitab mooduli kujundustarkvara arenduskomplekt (SDK) teil luua kohandatud mooduli teegi.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="3eb1a-114">Konteineri moodulid ja pesad</span><span class="sxs-lookup"><span data-stu-id="3eb1a-114">Container modules and slots</span></span>

<span data-ttu-id="3eb1a-115">Nagu varem mainitud, on mõni moodul kavandatud sisaldama alammooduleid.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="3eb1a-116">Neid mooduleid nimetatakse *konteineriteks* ja need võimaldavad luua pesastatud moodulite hierarhiaid.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="3eb1a-117">Konteineri moodulid sisaldavad *pesasid*.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-117">Container modules include *slots*.</span></span> <span data-ttu-id="3eb1a-118">Pesasid kasutatakse konteineri alammoodulite paigutuse ja eesmärgiga tegelemiseks.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="3eb1a-119">Näiteks üldine lehe konteineri mooduli (mis tahes lehe kõrgema taseme moodul), mis määratleb mitu olulist pesa.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="3eb1a-120">Päise pesa</span><span class="sxs-lookup"><span data-stu-id="3eb1a-120">A header slot</span></span>
- <span data-ttu-id="3eb1a-121">Alampäise pesa</span><span class="sxs-lookup"><span data-stu-id="3eb1a-121">A sub-header slot</span></span>
- <span data-ttu-id="3eb1a-122">Põhipesa</span><span class="sxs-lookup"><span data-stu-id="3eb1a-122">A main slot</span></span>
- <span data-ttu-id="3eb1a-123">Jaluse pesa</span><span class="sxs-lookup"><span data-stu-id="3eb1a-123">A footer slot</span></span>
- <span data-ttu-id="3eb1a-124">Alamjaluse pesa</span><span class="sxs-lookup"><span data-stu-id="3eb1a-124">A sub-footer slot</span></span>

<span data-ttu-id="3eb1a-125">Mooduli arendaja määrab need pesad ning millised alammoodulid ja mitu alammoodulit saab panna otse selle sisse.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-125">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="3eb1a-126">Näiteks võib päise pesa toetada vaid üht moodulit tüübiga **Päise moodul**, samas kui keha pesa võib toetada piiramatut arvu mis tahes tüüpi mooduleid (v.a teised lehe konteineri moodulid).</span><span class="sxs-lookup"><span data-stu-id="3eb1a-126">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="3eb1a-127">Loomistööriistades ei pea autorid ette teadma, milliseid mooduleid saab või ei saa igasse pessa panna.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-127">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="3eb1a-128">Kui lehe autorid valivad pesa ja proovivad seejärel valida sellele lisamiseks mooduli, näevad nad filtreeritud vaadet mooduli tüüpidest, mida see pesa toetab.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-128">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="3eb1a-129">Sisu moodulid</span><span class="sxs-lookup"><span data-stu-id="3eb1a-129">Content modules</span></span>

<span data-ttu-id="3eb1a-130">Sisu moodulid sisaldavad sisu- ja meediaelemente, nt teksti (pealkirjad, lõigud ja lingid) või vara viiteid (nt pildid, video ja PDF-id).</span><span class="sxs-lookup"><span data-stu-id="3eb1a-130">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="3eb1a-131">Tüüpilised sisu mooduli tüübid hõlmavad sisu plokki, teksti plokki ja promo banneri mooduleid.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-131">Typical content module types include content block, text block, and promo banner modules.</span></span> <span data-ttu-id="3eb1a-132">Need kolme tüüpi moodulid võivad sisaldada teksti või meediat ja neil pole vaja alammooduleid, et midagi lehel nähtavaks muuta.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-132">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="3eb1a-133">Suurem osa tüüpilistest igapäevastest lehe ja sisu loomise tegevustest hõlmavad sisu mooduleid, peamiselt seetõttu, et need moodulid määravad tegeliku sisu, mida renderdatakse nende konteineri ülemmoodulites.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-133">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="3eb1a-134">Saadaval on palju sisu mooduleid ja need on enamasti viimased tükid, mis tuleb lisada lehe pesastatud moodulite hierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-134">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="3eb1a-135">Järgmisel joonisel on näha, kuidas moodulid on pesastatud konteineri ülemmooduli pesadesse.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-135">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Moodulite pesastamine](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="3eb1a-137">Moodulite lisamine või eemaldamine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-137">Add or remove modules</span></span>

<span data-ttu-id="3eb1a-138">Järgmistes protseduurides kirjeldatakse, kuidas mooduleid lisada lisada ja eemaldada.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-138">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="3eb1a-139">Mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-139">Add a module</span></span>

<span data-ttu-id="3eb1a-140">Mooduli lisamiseks pesasse või konteinerisse lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-140">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="3eb1a-141">Valige vasakult liigenduspaanilt või otse põhilõuendilt konteiner või pesa, kuhu võib lisada alammooduli.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-141">In the outline pane on the left or directly in the main canvas, select a container or slot to which a child module can be added.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3eb1a-142">Mooduli koostaja määrab loendi mooduli tüüpidega, mida saab konkreetsesse mooduli pesasse lisada.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-142">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="3eb1a-143">Malli autorid saavad seejärel täpsustada lubatud mooduli suvandid, et tagada järjepidev otsingumootori optimeerimine (SEO) ja loomise tõhusus kõikidel lehtedel, mis luuakse konkreetsest mallist.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-143">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages that are built from a specific template.</span></span> <span data-ttu-id="3eb1a-144">Mooduli pesasse lisamisel filtreeritakse dialoogiboks **Lisa moodul** automaatselt, nii et kuvatakse ainult moodulid, mida toetatakse valitud konteineris või pesas.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-144">When adding a module to a slot, the **Add Module** dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="3eb1a-145">See lubatud moodulite loend määratletakse lehe malli või konteineri mooduli määratlusega.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-145">This list of allowed modules is determined by the page's template or the container's module definition.</span></span>

1. <span data-ttu-id="3eb1a-146">Kui kasutate liigenduspaani, valige kolmikpunkt (**...**) mooduli nime kõrval ja seejärel valige **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-146">If using the outline pane, select the ellipsis (**...**) next to the module name, and then select **Add Module**.</span></span> <span data-ttu-id="3eb1a-147">Kui kasutate juhtelemente otse lõuendi sees, valige pluss sümbol (**+**) tühjas pesas või praegu valitud mooduli kõrval ja seejärel valige **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-147">If using the controls directly within the canvas, select the plus symbol (**+**) in an empty slot or adjacent to the currently selected module, and then select **Add Module**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3eb1a-148">Kui konteiner või pesa ei toeta uusi alammooduleid, ei ole käsk **Lisa moodul** saadaval.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-148">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="3eb1a-149">Otsige ja valige lehele lisamiseks dialoogiboksist **Lisa moodul** moodul.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-149">In the **Add Module** dialog box, select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="3eb1a-150">**Sisu plokk**on hea mooduli tüüp algajatele töötamiseks.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-150">**Content block** is a good module type for beginners to work with.</span></span>

1. <span data-ttu-id="3eb1a-151">Valige nupp **OK**, et lisada valitud moodul valitud konteinerisse või pesasse oma lehel.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-151">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="3eb1a-152">Mooduli eemaldamine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-152">Remove a module</span></span>

<span data-ttu-id="3eb1a-153">Mooduli eemaldamiseks pesast või konteinerist lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-153">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="3eb1a-154">Vasakult liigenduspaanilt valige eemaldatava mooduli kõrvalt kolmikpunkti (**...**) ja seejärel valige prügikasti tähis.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-154">In the outline pane on the left, select the ellipsis (**...**) next to the name of the module to be removed, and then select the trash can symbol.</span></span> <span data-ttu-id="3eb1a-155">Alternatiivselt saate põhilõuendil valitud mooduli tööristaribal valida prügikasti tähise.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-155">Alternately, in the main canvas you can select the trash can symbol on a selected module's toolbar.</span></span>
1. <span data-ttu-id="3eb1a-156">Kui teil palutakse kinnitada, et soovite moodulit eemaldada, valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-156">When prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="move-a-module-to-a-new-position"></a><span data-ttu-id="3eb1a-157">Mooduli liigutamine uude asendisse</span><span class="sxs-lookup"><span data-stu-id="3eb1a-157">Move a module to a new position</span></span>

<span data-ttu-id="3eb1a-158">Lehel mooduli teisaldamiseks uude asukohta kasutage järgmisi meetodeid.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-158">To move a module to a new position within your page, use any of the following methods.</span></span>

### <a name="move-a-module-using-the-outline-pane"></a><span data-ttu-id="3eb1a-159">Mooduli teisaldamine liigenduspaani abil</span><span class="sxs-lookup"><span data-stu-id="3eb1a-159">Move a module using the outline pane</span></span>

<span data-ttu-id="3eb1a-160">Mooduli teisaldamiseks liigenduspaani abil toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-160">To move a module using the outline pane, follow these steps.</span></span>

1. <span data-ttu-id="3eb1a-161">Valige ja hoidke all moodulit, mida soovite teisaldada liigenduspaanil, seejärel lohistage moodul liigenduses uude asukohta.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-161">Select and hold the module you want to move in the outline pane, then drag the module to a new position in the outline.</span></span> <span data-ttu-id="3eb1a-162">Sinine rida liigenduses ja lõuendil näitab, kuhu saab mooduli paigutada.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-162">The blue line in the outline and on the canvas indicates where the module can be placed.</span></span>
1. <span data-ttu-id="3eb1a-163">Vabastage moodul, et see uude asukohta kukutada.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-163">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-directly-within-the-canvas"></a><span data-ttu-id="3eb1a-164">Mooduli teisaldamine otse lõuendil</span><span class="sxs-lookup"><span data-stu-id="3eb1a-164">Move a module directly within the canvas</span></span>

<span data-ttu-id="3eb1a-165">Mooduli teisaldamiseks otse lõuendil toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-165">To move a module directly within the canvas, follow these steps.</span></span>

1. <span data-ttu-id="3eb1a-166">Valige moodul, mida soovite teisaldada lõuendil.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-166">Select the module you want to move in the canvas.</span></span> 
1. <span data-ttu-id="3eb1a-167">Valige mooduli tööriistaribal kas üles- või allapoole osutava noole tähis ja lohistage seejärel nool uude asukohta leheküljel.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-167">Select either an upward or downward pointing arrow symbol in the module's toolbar, and then drag the arrow to a new position on the page.</span></span> <span data-ttu-id="3eb1a-168">Sinine rida lõuendil ja liigenduses näitab, kuhu saab mooduli paigutada.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-168">The blue line in the canvas and outline indicates where the module can be placed.</span></span> <span data-ttu-id="3eb1a-169">Kui moodulit ei saa üles või alla nihutada, on noole sümbol halli värvi.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-169">If a module cannot be moved up or down, that arrow symbol will be grayed out.</span></span> 
1. <span data-ttu-id="3eb1a-170">Vabastage moodul, et see uude asukohta kukutada.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-170">Release the module to drop it into the new position.</span></span>

### <a name="move-a-module-using-the-ellipsis-menu"></a><span data-ttu-id="3eb1a-171">Mooduli teisaldamine kolmikpunkti menüü abil</span><span class="sxs-lookup"><span data-stu-id="3eb1a-171">Move a module using the ellipsis menu</span></span>

<span data-ttu-id="3eb1a-172">Mooduli teisaldamiseks kolmikpunkti menüü abil toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-172">To move a module using the ellipsis menu, follow these steps.</span></span>

1. <span data-ttu-id="3eb1a-173">Valige moodul kas liigenduses või lõuendil.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-173">Select a module in either the outline or the canvas.</span></span>
1. <span data-ttu-id="3eb1a-174">Valige kolmikpunkt (**...**) mooduli nime kõrval liigenduspaanil või lõuendi mooduli tööriistaribal.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-174">Select the ellipsis (**...**) next to the module's name in the outline pane, or in the module's toolbar in the canvas.</span></span>
1. <span data-ttu-id="3eb1a-175">Kui moodulit saab konteineris või pesas üles või alla nihutada, näete suvandeid **Nihuta üles** või **Nihuta alla**.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-175">If the module can be moved up or down within the container or slot, you will see options for **Move up** or **Move down**.</span></span> <span data-ttu-id="3eb1a-176">Valige soovitud teisaldamise suvand, et liigutada moodulit oma alamosade suhtes üles või alla.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-176">Select the desired move option to move the module up or down relative to its siblings.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="3eb1a-177">Moodulite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-177">Configure modules</span></span>

<span data-ttu-id="3eb1a-178">Järgmistes protseduurides kirjeldatakse, kuidas sisu ja konteineri mooduleid konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-178">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="3eb1a-179">Sisu mooduli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-179">Configure a content module</span></span>

<span data-ttu-id="3eb1a-180">Sisu mooduli konfigureerimiseks lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-180">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="3eb1a-181">Vasakul liigenduspaanil laiendage puud ja valige mis tahes sisu moodul (nt **Sisu blokk**).</span><span class="sxs-lookup"><span data-stu-id="3eb1a-181">In the outline pane on the left, expand the tree and select any content module (for example, **Content block**).</span></span> <span data-ttu-id="3eb1a-182">Lisaks saade valida mooduli valida põhilõuendil.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-182">Alternately, you can select the module in the main canvas.</span></span>
1. <span data-ttu-id="3eb1a-183">Sisestage parempoolse mooduli atribuutide paanil kõik soovitud mooduli juhtelementide atribuudid.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-183">In the module properties pane on the right, enter properties for any desired module controls.</span></span>
1. <span data-ttu-id="3eb1a-184">Valige käsuribal suvand **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-184">On the command bar, select **Save**.</span></span> <span data-ttu-id="3eb1a-185">See värskendab ka eelvaate lõuendit.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-185">This will also refresh the preview canvas.</span></span>

### <a name="edit-module-text-properties"></a><span data-ttu-id="3eb1a-186">Mooduli tekstiomaduste muutmine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-186">Edit module text properties</span></span>

<span data-ttu-id="3eb1a-187">Mooduli tekstiatribuute, mis ei ole kirjutuskaitstud, saab redigeerida otse lõuendile.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-187">Module text properties that are not read-only can be edited directly in the canvas.</span></span>

<span data-ttu-id="3eb1a-188">Mooduli tekstiatribuutide redigeerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-188">To edit module text properties, follow these steps.</span></span>

1. <span data-ttu-id="3eb1a-189">Valige lõuendi teksti juhtelement, seejärel asetage kursor sinna, kus soovite teksti redigeerida.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-189">Select the text control in the canvas, then place your cursor where you wish to edit text.</span></span>
1. <span data-ttu-id="3eb1a-190">Sisestage soovitud teksti sisu.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-190">Enter your text content.</span></span>
1. <span data-ttu-id="3eb1a-191">Muu sisu redigeerimise jätkamiseks valige teksti sisust väljaspoole.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-191">Select anywhere outside the text content to continue editing other content.</span></span>

### <a name="inline-image-selection"></a><span data-ttu-id="3eb1a-192">Tekstisisese pildi valik</span><span class="sxs-lookup"><span data-stu-id="3eb1a-192">Inline image selection</span></span>

<span data-ttu-id="3eb1a-193">Mooduli pilte, mis ei ole kirjutuskaitstud, saab muuta otse lõuendile.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-193">Module images that are not read-only can be changed directly from the canvas.</span></span>

<span data-ttu-id="3eb1a-194">Sisu mooduli uue pildi valimiseks järgige järgmisi samme.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-194">To choose a new image for a content module, follow these steps.</span></span>

1. <span data-ttu-id="3eb1a-195">Topeltklõpsake lõuendi pildil.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-195">In the canvas, double-click the image.</span></span> <span data-ttu-id="3eb1a-196">See avab meedia valija akna.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-196">This will bring up the media picker window.</span></span>
1. <span data-ttu-id="3eb1a-197">Leidke ja valige uus pilt, mida soovite kasutada, ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-197">Find and select a new image you want to use, and then select **OK**.</span></span> <span data-ttu-id="3eb1a-198">Uus pilt on nüüd lõuendile sobitatud.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-198">The new image is now rendered in the canvas.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="3eb1a-199">Konteineri mooduli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-199">Configure a container module</span></span>

<span data-ttu-id="3eb1a-200">Konteineri mooduli konfigureerimiseks lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-200">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="3eb1a-201">Valige lehel konteineri moodul (nt karussell- või sujuva konteineri moodul).</span><span class="sxs-lookup"><span data-stu-id="3eb1a-201">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="3eb1a-202">Laiendage paremal atribuutide paanil pesastatud juhtelemente, valides päised, ja määrake juhtelementidele vajalikud väärtused.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-202">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="3eb1a-203">Vasakult liigenduspaanilt valige konteineri või konteineri sees oleva pesa nime kõrvalt kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-203">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="3eb1a-204">Seejärel lisage alammoodulid valitud konteinerile.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-204">Then, add child modules to the selected container.</span></span> <span data-ttu-id="3eb1a-205">Lisateavet vaadake jaotisest [Moodulitega töötamine](#add-a-module) selles teemas üleval.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-205">For more information, see the [Work with modules](#add-a-module) section earlier in this topic.</span></span>
1. <span data-ttu-id="3eb1a-206">Kui ülemmoodulis on mitu õdeüksusena eksisteerivat alammoodulit, saate muuta nende kuvamisjärjekorda ülemkonteineris.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-206">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="3eb1a-207">Valige mooduli kolmikpunkti nupp ja seejärel kasutage üles- ja allanoole nuppe.</span><span class="sxs-lookup"><span data-stu-id="3eb1a-207">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3eb1a-208">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3eb1a-208">Additional resources</span></span>

[<span data-ttu-id="3eb1a-209">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="3eb1a-209">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="3eb1a-210">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-210">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="3eb1a-211">Eelmääratud paigutustega töötamine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-211">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="3eb1a-212">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-212">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="3eb1a-213">Konteineri mooduli lisamine lehele</span><span class="sxs-lookup"><span data-stu-id="3eb1a-213">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="3eb1a-214">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="3eb1a-214">Work with publish groups</span></span>](publish-groups.md)

