---
title: Fragmentidega töötamine
description: Selles teemas kirjeldatakse, miks, millal ja kuidas kasutada fragmente rakenduses Microsoft Dynamics 365 Commerce.
author: phinneyridge
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
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b3e3299388190f03e761591a0c23164b705db9e8
ms.sourcegitcommit: f16db76c1c235dfa445b50614bcee9219782d6dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961654"
---
# <a name="work-with-fragments"></a><span data-ttu-id="9de29-103">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="9de29-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="9de29-104">Selles teemas kirjeldatakse, miks, millal ja kuidas kasutada fragmente rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9de29-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9de29-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="9de29-105">Overview</span></span>

<span data-ttu-id="9de29-106">Fragmendid tagavad tsentraliseeritud loomiskogemuse mooduli konfiguratsioonidele, mida tuleb kogu saidil uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="9de29-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="9de29-107">Näiteks päiseid, jaluseid ja ribareklaame konfigureeritakse sageli fragmentidena, kuna neid jagatakse paljude lehtede vahel.</span><span class="sxs-lookup"><span data-stu-id="9de29-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="9de29-108">Mõelge fragmentidest kui miniatuursetest veebisaitidest, mida saab sisestada teie saidi teistele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="9de29-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="9de29-109">Fragmentidel on oma elutsükkel.</span><span class="sxs-lookup"><span data-stu-id="9de29-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="9de29-110">Teisisõnu need luuakse, neile viidatakse, neid värskendatakse ja need kustutatakse loomistööriistade sõltumatute üksustena.</span><span class="sxs-lookup"><span data-stu-id="9de29-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="9de29-111">Pärast fragmentide konfigureerimist saab neid kasutada kõikjal teie saidi struktuuris, kus saab kasutada mooduleid.</span><span class="sxs-lookup"><span data-stu-id="9de29-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="9de29-112">Fragmentidele saab lehtedel, paigutustes, mallide ja teistes fragmentides viidata.</span><span class="sxs-lookup"><span data-stu-id="9de29-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="9de29-113">Fragmendid võivad olla kuni seitsme taseme sügavusel teistes fragmentides.</span><span class="sxs-lookup"><span data-stu-id="9de29-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="9de29-114">Näiteks kui soovite reklaamida hooajalist sündmust saidi paljudel lehtedel, võite selleks kasutada fragmenti.</span><span class="sxs-lookup"><span data-stu-id="9de29-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="9de29-115">Uue fragmendi loomise esimene samm on valida mooduli tüüp, millest soovite alustada.</span><span class="sxs-lookup"><span data-stu-id="9de29-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="9de29-116">Selles näites saate luua fragmendi pannoomoodulist.</span><span class="sxs-lookup"><span data-stu-id="9de29-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="9de29-117">Fragmente saab luua igast mooduli tüübist.</span><span class="sxs-lookup"><span data-stu-id="9de29-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="9de29-118">Seejärel saate konfigureerida pannoofragmendi konkreetse kampaaniasisuga.</span><span class="sxs-lookup"><span data-stu-id="9de29-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="9de29-119">Saate seda ka vajaduse järgi lokaliseerida.</span><span class="sxs-lookup"><span data-stu-id="9de29-119">You can also localize it as you require.</span></span> <span data-ttu-id="9de29-120">Uut eraldiseisevat pannoofragmenti saab seejärel kasutada eelkonfigureeritud moodulina kogu saidil.</span><span class="sxs-lookup"><span data-stu-id="9de29-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="9de29-121">Saate seda hõlpsasti lisada mallidele, konkreetsetele lehtedele või teistele fragmentidele, mis sisaldavad pannoomooduleid.</span><span class="sxs-lookup"><span data-stu-id="9de29-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="9de29-122">Kõik kohad, kuhu fragment lisatakse, on viited loodud kesksele pannoofragmendile.</span><span class="sxs-lookup"><span data-stu-id="9de29-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="9de29-123">Kui avaldate fragmendi muudatused, kajastuvad need muudatused kohe kõikides kohtades üle saidi, kus fragmendile viidatakse.</span><span class="sxs-lookup"><span data-stu-id="9de29-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="9de29-124">Seega pakuvad fragmendid võimsat ja tõhusat moodust mooduli konfiguratsioonide uuesti kasutamiseks ja tsentraalselt haldamiseks saidil.</span><span class="sxs-lookup"><span data-stu-id="9de29-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="9de29-125">Neid tõhusalt kasutades saate muuta töö oluliselt kiiremaks ja vähendada saidi haldamisega seotud kulusid.</span><span class="sxs-lookup"><span data-stu-id="9de29-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="9de29-126">Järgmisel joonisel on näha, kuidas saab fragmente kasutada jagatud mooduli konfiguratsioonide loomise tsentraliseerimiseks üle e-kaubanduse saidi.</span><span class="sxs-lookup"><span data-stu-id="9de29-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Näide sellest, kuidas saab fragmente kasutada jagatud mooduli konfiguratsioonide loomise tsentraliseerimiseks üle e-kaubanduse saidi.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="9de29-128">Fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="9de29-128">Create a fragment</span></span>

<span data-ttu-id="9de29-129">Saate kas luua uue fragmendi või salvestada olemasoleva mooduli konfiguratsiooni fragmendina.</span><span class="sxs-lookup"><span data-stu-id="9de29-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="9de29-130">Olemasoleva mooduli konfiguratsiooni salvestamine fragmendina</span><span class="sxs-lookup"><span data-stu-id="9de29-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="9de29-131">Varem konfigureeritud mooduli teisendamiseks korduskasutatavaks fragmendiks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9de29-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="9de29-132">Avage leht või mall, mis sisaldab moodulit, mida soovite teisendada fragmendiks.</span><span class="sxs-lookup"><span data-stu-id="9de29-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="9de29-133">Valige vasakul liigenduspaanil või otse visuaalses leheehitajas eelnevalt konfigureeritud moodul.</span><span class="sxs-lookup"><span data-stu-id="9de29-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="9de29-134">Valige kolmikpunkt (**...**) mooduli nime kõrval kas liigenduspaanil või visuaalses leheehitajas valitud mooduli tööriistaribal.</span><span class="sxs-lookup"><span data-stu-id="9de29-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="9de29-135">Valige suvand **Jaga lehekülje fragmendina**.</span><span class="sxs-lookup"><span data-stu-id="9de29-135">Select **Share as Page Fragment**.</span></span> 
1. <span data-ttu-id="9de29-136">Dialoogiaknas **Salvesta lehe fragmendina** sisestage fragmendi nimi.</span><span class="sxs-lookup"><span data-stu-id="9de29-136">In the **Save as Page Fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="9de29-137">Valige nupp **OK**, et salvestada mooduli konfiguratsioon fragmendina, mida saab lisada teistele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="9de29-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="9de29-138">Järgmine pilt näitab, kuidas salvestada mooduli konfiguratsiooni fragmendina.</span><span class="sxs-lookup"><span data-stu-id="9de29-138">The following image shows how to save a module configuration as a fragment.</span></span>

![Mooduli konfiguratsiooni fragmendina salvestamise kuvahõive](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="9de29-140">Uue fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="9de29-140">Create a new fragment</span></span>

<span data-ttu-id="9de29-141">Uue fragmendi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9de29-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="9de29-142">Valige navigeerimispaanilt vasakult suvand **Fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="9de29-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9de29-143">Valige suvand **Uus lehe fragment**.</span><span class="sxs-lookup"><span data-stu-id="9de29-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="9de29-144">Kuvatakse dialoogiboks, kus on näha kõik saadaolevad mooduli tüübid.</span><span class="sxs-lookup"><span data-stu-id="9de29-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="9de29-145">Nagu varem mainitud, fragmente saab luua igast mooduli tüübist.</span><span class="sxs-lookup"><span data-stu-id="9de29-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="9de29-146">Valige oma fragmendi jaoks mooduli tüüp.</span><span class="sxs-lookup"><span data-stu-id="9de29-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="9de29-147">Järgmine pilt näitab, kus uus fragment luua.</span><span class="sxs-lookup"><span data-stu-id="9de29-147">The following image shows where to create a new fragment.</span></span>

![Uue fragmendi loomiskoha kuvahõive](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="9de29-149">Valides üldkonteineri mooduli tüübi, on teil hiljem fragmendi värskendamise ja konfigureerimise vajadusel kõige rohkem vabadust.</span><span class="sxs-lookup"><span data-stu-id="9de29-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="9de29-150">Fragmentide lisamine, eemaldamine või redigeerimine lehel</span><span class="sxs-lookup"><span data-stu-id="9de29-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="9de29-151">Järgmistes protseduurides kirjeldatakse, kuidas fragmente lisada, eemaldada ja redigeerida.</span><span class="sxs-lookup"><span data-stu-id="9de29-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="9de29-152">Fragmendi lisamine</span><span class="sxs-lookup"><span data-stu-id="9de29-152">Add a fragment</span></span>

<span data-ttu-id="9de29-153">Lehele fragmendi lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9de29-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="9de29-154">Valige vasakult liigenduspaanilt või otse visuaalsest leheehitajast konteiner või pesa, kuhu võib lisada alammoodulid.</span><span class="sxs-lookup"><span data-stu-id="9de29-154">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="9de29-155">Valige võrgupaanil kolmikpunkt (**...**) konteineri või pesa nime kõrval.</span><span class="sxs-lookup"><span data-stu-id="9de29-155">In the online pane, select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="9de29-156">Kui kasutate visuaalset leheehitajat, valige teise võimalusena pluss-sümbol (**+**).</span><span class="sxs-lookup"><span data-stu-id="9de29-156">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="9de29-157">Valige nupp **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="9de29-157">Select **Add Fragment**.</span></span>

    ![Olemasoleva fragmendi pessa või konteinerisse lisamise kuvahõive](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="9de29-159">Kui konteiner või pesa ei toeta uusi alammooduleid, ei ole käsk **Lisa fragment** saadaval.</span><span class="sxs-lookup"><span data-stu-id="9de29-159">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="9de29-160">Otsige ja valige lisamiseks dialoogiboksist **Lisa fragment** fragment.</span><span class="sxs-lookup"><span data-stu-id="9de29-160">In the **Add Fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="9de29-161">Kui ühtegi saadaolevat fragmenti loendis pole, peate kõigepealt looma fragmendi mooduli tüübist, mida valitud konteiner või pesa toetab.</span><span class="sxs-lookup"><span data-stu-id="9de29-161">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="9de29-162">Valige soovitud fragment, et lisada see oma lehel konteinerile või pesale.</span><span class="sxs-lookup"><span data-stu-id="9de29-162">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![Fragmendi valija modaalakna ekraanihõive](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="9de29-164">Konteineris või pesas lubatud moodulid on määratletud lehe malli või moodulite enda määratlustega.</span><span class="sxs-lookup"><span data-stu-id="9de29-164">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="9de29-165">Fragmendi eemaldamine</span><span class="sxs-lookup"><span data-stu-id="9de29-165">Remove a fragment</span></span>

<span data-ttu-id="9de29-166">Fragmendi eemaldamiseks pesast või konteinerist lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9de29-166">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="9de29-167">Vasakult liigenduspaanilt valige eemaldatava fragmendi kõrvalt kolmikpunkt (**...**) ja seejärel valige prügikasti tähis.</span><span class="sxs-lookup"><span data-stu-id="9de29-167">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="9de29-168">Alternatiivselt saate valida visuaalses leheehitajas fragmendi ja valida fragmendi tööriistaribal prügikasti tähise.</span><span class="sxs-lookup"><span data-stu-id="9de29-168">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="9de29-169">Kui teil palutakse kinnitada, et soovite fragmenti eemaldada, valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="9de29-169">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="9de29-170">Kui fragmendi lehelt eemaldate, eemaldate lehelt vaid viite sellele.</span><span class="sxs-lookup"><span data-stu-id="9de29-170">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="9de29-171">Te **ei** kustuta fragmenti saidilt.</span><span class="sxs-lookup"><span data-stu-id="9de29-171">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="9de29-172">Fragmentide kustutamiseks saidilt peate kasutama fragmendi kontrollija kasutajaliidest (UI).</span><span class="sxs-lookup"><span data-stu-id="9de29-172">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="9de29-173">Fragmente saate saidilt kustutada ainult siis, kui neile ei viita parasjagu ükski leht, mall või teine fragment.</span><span class="sxs-lookup"><span data-stu-id="9de29-173">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="9de29-174">Fragmendi redigeerimine</span><span class="sxs-lookup"><span data-stu-id="9de29-174">Edit a fragment</span></span>

<span data-ttu-id="9de29-175">Fragmentide redigeerimiseks peate kasutama fragmendi redaktori kasutajaliidest.</span><span class="sxs-lookup"><span data-stu-id="9de29-175">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="9de29-176">See piirang on kavandatud.</span><span class="sxs-lookup"><span data-stu-id="9de29-176">This restriction is by design.</span></span> <span data-ttu-id="9de29-177">See aitab tagada, et autorid ei ajaks segi konkreetse lehe moodulite redigeerimise protsessi paljude lehtede vahel jagatavate fragmentide redigeerimise protsessiga.</span><span class="sxs-lookup"><span data-stu-id="9de29-177">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="9de29-178">Fragmendi redigeerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9de29-178">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="9de29-179">Valige navigeerimispaanilt vasakult suvand **Fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="9de29-179">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9de29-180">Valige jaotisest **Fragmendid** redigeerimiseks fragment.</span><span class="sxs-lookup"><span data-stu-id="9de29-180">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="9de29-181">Redigeerige fragmendi mooduli atribuute ja struktuuri vajaduse järgi.</span><span class="sxs-lookup"><span data-stu-id="9de29-181">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="9de29-182">Protsess meenutab moodulite redigeerimise protsessi, mis toimub lehe redaktori vaates.</span><span class="sxs-lookup"><span data-stu-id="9de29-182">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="9de29-183">Saate fragmenti redigeerida ka nii, et valite selle lehelt, mallist või ülemfragmendist ja seejärel valite paremalt atribuutide paanilt suvandi **Fragmendi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9de29-183">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9de29-184">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9de29-184">Additional resources</span></span>

[<span data-ttu-id="9de29-185">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="9de29-185">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="9de29-186">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="9de29-186">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="9de29-187">Eelmääratud paigutustega töötamine</span><span class="sxs-lookup"><span data-stu-id="9de29-187">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="9de29-188">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="9de29-188">Work with publish groups</span></span>](publish-groups.md)
