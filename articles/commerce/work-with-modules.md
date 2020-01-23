---
title: Moodulitega töötamine
description: Selles teemas kirjeldatakse, kuidas ja millal kasutada mooduleid rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914790"
---
# <a name="work-with-modules"></a><span data-ttu-id="b8844-103">Moodulitega töötamine</span><span class="sxs-lookup"><span data-stu-id="b8844-103">Work with modules</span></span>

<span data-ttu-id="b8844-104">Selles teemas kirjeldatakse, kuidas ja millal kasutada mooduleid rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b8844-104">This topic describes how and when to use modules in Microsoft Dynamics 365 Commerce.</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="b8844-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b8844-105">Overview</span></span>

<span data-ttu-id="b8844-106">Moodulid on loogilised koosteüksused, mis moodustavad teie lehe struktuuri, neil on mitmesuguseid eesmärke ja ulatusi.</span><span class="sxs-lookup"><span data-stu-id="b8844-106">Modules are logical building blocks that make up your page structure, and they have various purposes and scopes.</span></span> <span data-ttu-id="b8844-107">Mõni moodul on kõrgetasemeline konteiner ning nende ainus eesmärk on hoida ja korraldada teisi mooduleid (alammooduleid).</span><span class="sxs-lookup"><span data-stu-id="b8844-107">Some modules are high-level containers, and their only purpose is to hold and organize other modules (child modules).</span></span> <span data-ttu-id="b8844-108">Teistel moodulitel, näiteks lihtsal pildipaigutusmoodulil, on väga konkreetne eesmärk.</span><span class="sxs-lookup"><span data-stu-id="b8844-108">Other modules, such as a simple image placement module, have a very specific purpose.</span></span> <span data-ttu-id="b8844-109">Teised moodulid, nt karussellmoodul, jäävad kusagile nende kahe kategooria vahele.</span><span class="sxs-lookup"><span data-stu-id="b8844-109">Other modules, such as a carousel module, fall somewhere between those two categories.</span></span>

<span data-ttu-id="b8844-110">Vaikimisi sisaldab teie Dynamics 365 Commerce’i sait alustuskomplekti mooduli teeki, mille abil saate luua kõige üldisemaid e-kaubanduse stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="b8844-110">By default, your Dynamics 365 Commerce site includes a starter kit module library that lets you achieve most basic e-Commerce scenarios.</span></span> <span data-ttu-id="b8844-111">Vaid neid mooduleid kasutades peaksite saama luua täieliku e-kaubanduse saidi.</span><span class="sxs-lookup"><span data-stu-id="b8844-111">You should be able to construct an end-to-end e-Commerce site just by using these modules.</span></span> <span data-ttu-id="b8844-112">Kuid võib-olla soovite neid mooduleid kohandada või luua uusi, kohandatud mooduleid, mis vastavad konkreetsetele vajadustele.</span><span class="sxs-lookup"><span data-stu-id="b8844-112">However, you might also want to customize these modules or build new, custom modules for specific needs.</span></span> <span data-ttu-id="b8844-113">Kui soovite luua kohandatud mooduleid, aitab mooduli kujundustarkvara arenduskomplekt (SDK) teil luua kohandatud mooduli teegi.</span><span class="sxs-lookup"><span data-stu-id="b8844-113">If you want to build custom modules, a module design software development kit (SDK) is available to help you create a custom module library.</span></span>

## <a name="container-modules-and-slots"></a><span data-ttu-id="b8844-114">Konteineri moodulid ja pesad</span><span class="sxs-lookup"><span data-stu-id="b8844-114">Container modules and slots</span></span>

<span data-ttu-id="b8844-115">Nagu varem mainitud, on mõni moodul kavandatud sisaldama alammooduleid.</span><span class="sxs-lookup"><span data-stu-id="b8844-115">As was mentioned earlier, some modules are designed to hold child modules.</span></span> <span data-ttu-id="b8844-116">Neid mooduleid nimetatakse *konteineriteks* ja need võimaldavad luua pesastatud moodulite hierarhiaid.</span><span class="sxs-lookup"><span data-stu-id="b8844-116">These modules are known as *containers*, and they allow for hierarchies of nested modules.</span></span> <span data-ttu-id="b8844-117">Konteineri moodulid sisaldavad *pesasid*.</span><span class="sxs-lookup"><span data-stu-id="b8844-117">Container modules include *slots*.</span></span> <span data-ttu-id="b8844-118">Pesasid kasutatakse konteineri alammoodulite paigutuse ja eesmärgiga tegelemiseks.</span><span class="sxs-lookup"><span data-stu-id="b8844-118">Slots are used to handle the layout and purpose of child modules in the container.</span></span> <span data-ttu-id="b8844-119">Näiteks üldine lehe konteineri mooduli (mis tahes lehe kõrgema taseme moodul), mis määratleb mitu olulist pesa.</span><span class="sxs-lookup"><span data-stu-id="b8844-119">An example is a basic page container module (a top-level module for any page) that defines several important slots:</span></span>

- <span data-ttu-id="b8844-120">Päise pesa</span><span class="sxs-lookup"><span data-stu-id="b8844-120">A header slot</span></span>
- <span data-ttu-id="b8844-121">Sisu pesa</span><span class="sxs-lookup"><span data-stu-id="b8844-121">A body slot</span></span>
- <span data-ttu-id="b8844-122">Jaluse pesa</span><span class="sxs-lookup"><span data-stu-id="b8844-122">A footer slot</span></span>

<span data-ttu-id="b8844-123">Mooduli arendaja määrab need pesad ning millised alammoodulid ja mitu alammoodulit saab panna otse selle sisse.</span><span class="sxs-lookup"><span data-stu-id="b8844-123">The module's developer defines these slots, and determines which child modules and how many child modules can be put directly inside it.</span></span> <span data-ttu-id="b8844-124">Näiteks võib päise pesa toetada vaid üht moodulit tüübiga **Päise moodul**, samas kui keha pesa võib toetada piiramatut arvu mis tahes tüüpi mooduleid (v.a teised lehe konteineri moodulid).</span><span class="sxs-lookup"><span data-stu-id="b8844-124">For example, the header slot might support only one module of the **Header Module** type, whereas the body slot might support an unlimited number of modules of any type (except other page container modules).</span></span>

<span data-ttu-id="b8844-125">Loomistööriistades ei pea autorid ette teadma, milliseid mooduleid saab või ei saa igasse pessa panna.</span><span class="sxs-lookup"><span data-stu-id="b8844-125">In the authoring tools, page authors don't have to know in advance which modules can and can't be put in each slot.</span></span> <span data-ttu-id="b8844-126">Kui lehe autorid valivad pesa ja proovivad seejärel valida sellele lisamiseks mooduli, näevad nad filtreeritud vaadet mooduli tüüpidest, mida see pesa toetab.</span><span class="sxs-lookup"><span data-stu-id="b8844-126">When page authors select a slot and then try to select a module to add to it, they see a filtered view of module types that are supported for that slot.</span></span>

## <a name="content-modules"></a><span data-ttu-id="b8844-127">Sisu moodulid</span><span class="sxs-lookup"><span data-stu-id="b8844-127">Content modules</span></span>

<span data-ttu-id="b8844-128">Sisu moodulid sisaldavad sisu- ja meediaelemente, nt teksti (pealkirjad, lõigud ja lingid) või vara viiteid (nt pildid, video ja PDF-id).</span><span class="sxs-lookup"><span data-stu-id="b8844-128">Content modules contain content and media elements, such as text (for example, headlines, paragraphs, and links) or asset references (for example, images, video, and PDFs).</span></span> <span data-ttu-id="b8844-129">Tüüpilised sisu mooduli tüübid on näiteks **Pannoo**, **Funktsioon** ja **Ribareklaam**.</span><span class="sxs-lookup"><span data-stu-id="b8844-129">Examples of typical content module types are **Hero**, **Feature**, and **Banner**.</span></span> <span data-ttu-id="b8844-130">Need kolme tüüpi moodulid võivad sisaldada teksti või meediat ja neil pole vaja alammooduleid, et midagi lehel nähtavaks muuta.</span><span class="sxs-lookup"><span data-stu-id="b8844-130">Modules of these three types can contain text or media, and they don't require any child modules to make something visible on a page.</span></span>

<span data-ttu-id="b8844-131">Suurem osa tüüpilistest igapäevastest lehe ja sisu loomise tegevustest hõlmavad sisu mooduleid, peamiselt seetõttu, et need moodulid määravad tegeliku sisu, mida renderdatakse nende konteineri ülemmoodulites.</span><span class="sxs-lookup"><span data-stu-id="b8844-131">The majority of typical, day-to-day page and content authoring activities involve content modules, primarily because these modules define the actual content that is rendered in their parent container modules.</span></span> <span data-ttu-id="b8844-132">Saadaval on palju sisu mooduleid ja need on enamasti viimased tükid, mis tuleb lisada lehe pesastatud moodulite hierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="b8844-132">Many content modules are available, and these modules are typically the last pieces that you will add to a page's hierarchy of nested modules.</span></span>

<span data-ttu-id="b8844-133">Järgmisel joonisel on näha, kuidas moodulid on pesastatud konteineri ülemmooduli pesadesse.</span><span class="sxs-lookup"><span data-stu-id="b8844-133">The following illustration shows how modules are nested inside parent container module slots.</span></span>

![Moodulite pesastamine](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a><span data-ttu-id="b8844-135">Moodulite lisamine või eemaldamine</span><span class="sxs-lookup"><span data-stu-id="b8844-135">Add or remove modules</span></span>

<span data-ttu-id="b8844-136">Järgmistes protseduurides kirjeldatakse, kuidas mooduleid lisada lisada ja eemaldada.</span><span class="sxs-lookup"><span data-stu-id="b8844-136">The following procedures describe how to add and remove modules.</span></span>

### <a name="add-a-module"></a><span data-ttu-id="b8844-137">Mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="b8844-137">Add a module</span></span>

<span data-ttu-id="b8844-138">Mooduli lisamiseks pesasse või konteinerisse lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b8844-138">To add a module to a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="b8844-139">Valige vasakult liigenduspaanilt konteiner või pesa, kuhu võib lisada alammooduli.</span><span class="sxs-lookup"><span data-stu-id="b8844-139">In the outline pane on the left, select a container or slot that a child module can be added to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8844-140">Mooduli koostaja määrab loendi mooduli tüüpidega, mida saab konkreetsesse mooduli pesasse lisada.</span><span class="sxs-lookup"><span data-stu-id="b8844-140">The module designer defines the list of modules types that can be added to a specific module slot.</span></span> <span data-ttu-id="b8844-141">Malli autorid saavad seejärel täpsustada lubatud mooduli suvandid, et tagada järjepidev otsingumootori optimeerimine (SEO) ja loomise tõhusus kõikidel lehtedel, mis luuakse konkreetsest mallist.</span><span class="sxs-lookup"><span data-stu-id="b8844-141">Template authors can then refine the allowed module options to help guarantee consistent search engine optimization (SEO) and authoring efficiency for all the pages pages that are built from a specific template.</span></span>

1. <span data-ttu-id="b8844-142">Valige mooduli kolmikpunkti nupp (**...**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b8844-142">Select the ellipsis button (**...**) for the module, and then select **Add Module**.</span></span> <span data-ttu-id="b8844-143">Ilmub dialoogiboks **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b8844-143">The **Add Module** dialog box appears.</span></span> <span data-ttu-id="b8844-144">See dialoogiboks filtreeritakse automaatselt, nii et kuvatakse ainult moodulid, mida toetatakse valitud konteineris või pesas.</span><span class="sxs-lookup"><span data-stu-id="b8844-144">This dialog box is automatically filtered so that it shows only modules that are supported in the selected container or slot.</span></span> <span data-ttu-id="b8844-145">Moodulite loend määratletakse lehe malli või konteineri mooduli määratlusega.</span><span class="sxs-lookup"><span data-stu-id="b8844-145">The list of modules is determined by the page's template or the container module definition.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b8844-146">Kui konteiner või pesa ei toeta uusi alammooduleid, ei ole käsk **Lisa moodul** saadaval.</span><span class="sxs-lookup"><span data-stu-id="b8844-146">If a container or slot doesn't support new child modules, the **Add Module** option is unavailable.</span></span>

1. <span data-ttu-id="b8844-147">Otsige ja valige lehele lisamiseks dialoogiboksist moodul.</span><span class="sxs-lookup"><span data-stu-id="b8844-147">In the dialog box, search for and select a module to add to your page.</span></span>

    > [!TIP]
    > <span data-ttu-id="b8844-148">**Funktsioon** ja **Pannoo** on sobivad mooduli tüübid algajatele.</span><span class="sxs-lookup"><span data-stu-id="b8844-148">**Feature** and **Hero** are good module types for beginners to work with.</span></span>

1. <span data-ttu-id="b8844-149">Valige nupp **OK**, et lisada valitud moodul valitud konteinerisse või pesasse oma lehel.</span><span class="sxs-lookup"><span data-stu-id="b8844-149">Select **OK** to add the selected module to the selected container or slot on your page.</span></span>

### <a name="remove-a-module"></a><span data-ttu-id="b8844-150">Mooduli eemaldamine</span><span class="sxs-lookup"><span data-stu-id="b8844-150">Remove a module</span></span>

<span data-ttu-id="b8844-151">Mooduli eemaldamiseks pesast või konteinerist lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b8844-151">To remove a module from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="b8844-152">Vasakult liigenduspaanilt valige eemaldatava mooduli kõrvalt kolmikpunkti nupp ja seejärel valige prügikasti nupp.</span><span class="sxs-lookup"><span data-stu-id="b8844-152">In the outline pane on the left, select the ellipsis button next to the name of the module to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="b8844-153">Kui teil palutakse kinnitada, et soovite moodulit eemaldada, valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b8844-153">When you're prompted to confirm that you want to remove the module, select **OK**.</span></span>

## <a name="configure-modules"></a><span data-ttu-id="b8844-154">Moodulite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b8844-154">Configure modules</span></span>

<span data-ttu-id="b8844-155">Järgmistes protseduurides kirjeldatakse, kuidas sisu ja konteineri mooduleid konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="b8844-155">The following procedures describe how to configure content and container modules.</span></span>

### <a name="configure-a-content-module"></a><span data-ttu-id="b8844-156">Sisu mooduli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b8844-156">Configure a content module</span></span>

<span data-ttu-id="b8844-157">Sisu mooduli konfigureerimiseks lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b8844-157">To configure a content module on a page, follow these steps.</span></span>

1. <span data-ttu-id="b8844-158">Valige vasakult liigenduspaanilt sisu mooduli tüüp (nt **Funktsioon**, **Pannoo** või **Ribareklaam**).</span><span class="sxs-lookup"><span data-stu-id="b8844-158">In the outline pane on the left, select a content module type (for example, **Feature**, **Hero**, or **Banner**).</span></span>
1. <span data-ttu-id="b8844-159">Laiendage paremal atribuutide paanil pesastatud juhtelemente, valides päised, ja määrake juhtelementidele vajalikud väärtused.</span><span class="sxs-lookup"><span data-stu-id="b8844-159">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="b8844-160">Kui atribuutide paanil on jaotis **Andmete konfigureerimine**, valige see, et seda laiendada.</span><span class="sxs-lookup"><span data-stu-id="b8844-160">If the properties pane has a **Data Configuration** section, select it to expand it.</span></span> <span data-ttu-id="b8844-161">Vastasel korral jätkake 5. etapiga.</span><span class="sxs-lookup"><span data-stu-id="b8844-161">Otherwise, go to step 5.</span></span>
1. <span data-ttu-id="b8844-162">Kui olemas on nupp **Lisa andmeallikas**, valige see ja seejärel valige lisamiseks sisuüksused.</span><span class="sxs-lookup"><span data-stu-id="b8844-162">If there is a **Add Data Source** button, select it, and then select the content items to add.</span></span>
1. <span data-ttu-id="b8844-163">Sisestage vajalike või sobivate mooduli juhtelementide sätted.</span><span class="sxs-lookup"><span data-stu-id="b8844-163">Enter settings for any required or desired module controls.</span></span>
1. <span data-ttu-id="b8844-164">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b8844-164">Select **Save**.</span></span>

### <a name="configure-a-container-module"></a><span data-ttu-id="b8844-165">Konteineri mooduli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b8844-165">Configure a container module</span></span>

<span data-ttu-id="b8844-166">Konteineri mooduli konfigureerimiseks lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b8844-166">To configure a container module on a page, follow these steps.</span></span>

1. <span data-ttu-id="b8844-167">Valige lehel konteineri moodul (nt karussell- või sujuva konteineri moodul).</span><span class="sxs-lookup"><span data-stu-id="b8844-167">Select a container module on your page (for example, a carousel or fluid container module).</span></span>
1. <span data-ttu-id="b8844-168">Laiendage paremal atribuutide paanil pesastatud juhtelemente, valides päised, ja määrake juhtelementidele vajalikud väärtused.</span><span class="sxs-lookup"><span data-stu-id="b8844-168">In the properties pane on the right, expand the nested controls by selecting the headers, and set any required control values.</span></span>
1. <span data-ttu-id="b8844-169">Vasakult liigenduspaanilt valige konteineri või konteineri sees oleva pesa nime kõrvalt kolmikpunkti nupp ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b8844-169">In the outline pane on the left, select the ellipsis button next to the name of either the container or any slots inside the container, and then select **Add Module**.</span></span> <span data-ttu-id="b8844-170">Seejärel lisage alammoodulid valitud konteinerile.</span><span class="sxs-lookup"><span data-stu-id="b8844-170">Then add child modules to the selected container.</span></span> <span data-ttu-id="b8844-171">Lisateavet vaadake protseduuri [Mooduli lisamine](#add-a-module) selles teemas üleval.</span><span class="sxs-lookup"><span data-stu-id="b8844-171">For more information, see the [Add a module](#add-a-module) procedure earlier in this topic.</span></span>
1. <span data-ttu-id="b8844-172">Kui ülemmoodulis on mitu õdeüksusena eksisteerivat alammoodulit, saate muuta nende kuvamisjärjekorda ülemkonteineris.</span><span class="sxs-lookup"><span data-stu-id="b8844-172">If multiple child modules exist as siblings in a parent container, you can change their display order in the parent container.</span></span> <span data-ttu-id="b8844-173">Valige mooduli kolmikpunkti nupp ja seejärel kasutage üles- ja allanoole nuppe.</span><span class="sxs-lookup"><span data-stu-id="b8844-173">Select the ellipsis button for a module, and then use the up arrow and down arrow buttons.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8844-174">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b8844-174">Additional resources</span></span>

[<span data-ttu-id="b8844-175">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b8844-175">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="b8844-176">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="b8844-176">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="b8844-177">Eelmääratud paigutustega töötamine</span><span class="sxs-lookup"><span data-stu-id="b8844-177">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="b8844-178">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="b8844-178">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="b8844-179">Konteineri mooduli lisamine lehele</span><span class="sxs-lookup"><span data-stu-id="b8844-179">Add a container module to a page</span></span>](add-container-module.md)

[<span data-ttu-id="b8844-180">Sisupaigutusmoodulite lisamine lehele</span><span class="sxs-lookup"><span data-stu-id="b8844-180">Add content placement modules to a page</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="b8844-181">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="b8844-181">Work with publish groups</span></span>](publish-groups.md)
