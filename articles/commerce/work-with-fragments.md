---
title: Fragmentidega töötamine
description: Selles teemas kirjeldatakse, miks, millal ja kuidas kasutada fragmente rakenduses Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
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
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f29046ded47ed9c49a2cc841aa7c1f6492b49aec
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124355"
---
# <a name="work-with-fragments"></a><span data-ttu-id="9cf8e-103">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="9cf8e-103">Work with fragments</span></span> 


[!include [banner](includes/banner.md)]

<span data-ttu-id="9cf8e-104">Selles teemas kirjeldatakse, miks, millal ja kuidas kasutada fragmente rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9cf8e-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="9cf8e-105">Overview</span></span>

<span data-ttu-id="9cf8e-106">Fragmendid tagavad tsentraliseeritud loomiskogemuse mooduli konfiguratsioonidele, mida tuleb kogu saidil uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="9cf8e-107">Näiteks päiseid, jaluseid ja ribareklaame konfigureeritakse sageli fragmentidena, kuna neid jagatakse paljude lehtede vahel.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="9cf8e-108">Mõelge fragmentidest kui miniatuursetest veebisaitidest, mida saab sisestada teie saidi teistele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="9cf8e-109">Fragmentidel on oma elutsükkel.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="9cf8e-110">Teisisõnu need luuakse, neile viidatakse, neid värskendatakse ja need kustutatakse loomistööriistade sõltumatute üksustena.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="9cf8e-111">Pärast fragmentide konfigureerimist saab neid kasutada kõikjal teie saidi struktuuris, kus saab kasutada mooduleid.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="9cf8e-112">Fragmentidele saab lehtedel, paigutustes, mallide ja teistes fragmentides viidata.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="9cf8e-113">Fragmendid võivad olla kuni seitsme taseme sügavusel teistes fragmentides.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="9cf8e-114">Näiteks kui soovite reklaamida hooajalist sündmust saidi paljudel lehtedel, võite selleks kasutada fragmenti.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="9cf8e-115">Uue fragmendi loomise esimene samm on valida mooduli tüüp, millest soovite alustada.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="9cf8e-116">Selles näites saate luua fragmendi pannoomoodulist.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="9cf8e-117">Fragmente saab luua igast mooduli tüübist.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="9cf8e-118">Seejärel saate konfigureerida pannoofragmendi konkreetse kampaaniasisuga.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="9cf8e-119">Saate seda ka vajaduse järgi lokaliseerida.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-119">You can also localize it as you require.</span></span> <span data-ttu-id="9cf8e-120">Uut eraldiseisevat pannoofragmenti saab seejärel kasutada eelkonfigureeritud moodulina kogu saidil.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="9cf8e-121">Saate seda hõlpsasti lisada mallidele, konkreetsetele lehtedele või teistele fragmentidele, mis sisaldavad pannoomooduleid.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="9cf8e-122">Kõik kohad, kuhu fragment lisatakse, on viited loodud kesksele pannoofragmendile.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="9cf8e-123">Kui avaldate fragmendi muudatused, kajastuvad need muudatused kohe kõikides kohtades üle saidi, kus fragmendile viidatakse.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="9cf8e-124">Seega pakuvad fragmendid võimsat ja tõhusat moodust mooduli konfiguratsioonide uuesti kasutamiseks ja tsentraalselt haldamiseks saidil.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="9cf8e-125">Neid tõhusalt kasutades saate muuta töö oluliselt kiiremaks ja vähendada saidi haldamisega seotud kulusid.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="9cf8e-126">Järgmisel joonisel on näha, kuidas saab fragmente kasutada jagatud mooduli konfiguratsioonide loomise tsentraliseerimiseks üle e-kaubanduse saidi.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Näide sellest, kuidas saab fragmente kasutada jagatud mooduli konfiguratsioonide loomise tsentraliseerimiseks üle e-kaubanduse saidi.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="9cf8e-128">Fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="9cf8e-128">Create a fragment</span></span>

<span data-ttu-id="9cf8e-129">Saate kas luua uue fragmendi või salvestada olemasoleva mooduli konfiguratsiooni fragmendina.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="9cf8e-130">Olemasoleva mooduli konfiguratsiooni salvestamine fragmendina</span><span class="sxs-lookup"><span data-stu-id="9cf8e-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="9cf8e-131">Varem konfigureeritud mooduli teisendamiseks korduskasutatavaks fragmendiks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-131">To convert a previously configured module to a reusable fragment, follow these steps.</span></span>

1. <span data-ttu-id="9cf8e-132">Avage leht või mall, mis sisaldab moodulit, mida soovite teisendada fragmendiks.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="9cf8e-133">Valige vasakul liigenduspaanil mooduli nime kõrval kolmikpunkti nupp (**...**).</span><span class="sxs-lookup"><span data-stu-id="9cf8e-133">In the outline pane on the left, select the ellipsis button (**...**) next to the name of the module.</span></span> 
1. <span data-ttu-id="9cf8e-134">Valige suvand **Jaga fragmendina**.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-134">Select **Share as Fragment**.</span></span> 
1. <span data-ttu-id="9cf8e-135">Kuvatakse dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-135">A dialog box appears.</span></span> <span data-ttu-id="9cf8e-136">Sisestage fragmendi nimi ja metaandmed.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-136">Enter a name and metadata for the fragment.</span></span>
1. <span data-ttu-id="9cf8e-137">Valige nupp **OK**, et salvestada mooduli konfiguratsioon fragmendina, mida saab lisada teistele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>

<span data-ttu-id="9cf8e-138">Järgmine pilt näitab, kuidas salvestada mooduli konfiguratsiooni fragmendina.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-138">The following image shows how to save a module configuration as a fragment.</span></span>

![Mooduli konfiguratsiooni fragmendina salvestamise kuvahõive](./media/save-as-fragment.png)

### <a name="create-a-new-fragment"></a><span data-ttu-id="9cf8e-140">Uue fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="9cf8e-140">Create a new fragment</span></span>

<span data-ttu-id="9cf8e-141">Uue fragmendi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-141">To create a new fragment, follow these steps.</span></span>

1. <span data-ttu-id="9cf8e-142">Valige navigeerimispaanilt vasakult suvand **Fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-142">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9cf8e-143">Valige suvand **Uus lehe fragment**.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-143">Select **New Page Fragment**.</span></span> <span data-ttu-id="9cf8e-144">Kuvatakse dialoogiboks, kus on näha kõik saadaolevad mooduli tüübid.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-144">A dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="9cf8e-145">Nagu varem mainitud, fragmente saab luua igast mooduli tüübist.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-145">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="9cf8e-146">Valige oma fragmendi jaoks mooduli tüüp.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-146">Select a module type for your fragment.</span></span>

<span data-ttu-id="9cf8e-147">Järgmine pilt näitab, kus uus fragment luua.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-147">The following image shows where to create a new fragment.</span></span>

![Uue fragmendi loomiskoha kuvahõive](./media/fragment-nav-menu.png)

> [!TIP]
> <span data-ttu-id="9cf8e-149">Valides üldkonteineri mooduli tüübi, on teil hiljem fragmendi värskendamise ja konfigureerimise vajadusel kõige rohkem vabadust.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-149">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="9cf8e-150">Fragmentide lisamine, eemaldamine või redigeerimine lehel</span><span class="sxs-lookup"><span data-stu-id="9cf8e-150">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="9cf8e-151">Järgmistes protseduurides kirjeldatakse, kuidas fragmente lisada, eemaldada ja redigeerida.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-151">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="9cf8e-152">Fragmendi lisamine</span><span class="sxs-lookup"><span data-stu-id="9cf8e-152">Add a fragment</span></span>

<span data-ttu-id="9cf8e-153">Lehele fragmendi lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-153">To add a fragment to a page, follow these steps.</span></span>

1. <span data-ttu-id="9cf8e-154">Valige vasakult liigenduspaanilt konteiner või pesa, kuhu võib lisada alammooduleid.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-154">In the outline pane on the left, select a container or slot that child modules can be added to.</span></span>
1. <span data-ttu-id="9cf8e-155">Valige konteineri või pesa nime kõrvalt kolmikpunkti nupp ja seejärel käsk **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-155">Select the ellipsis button next to the name of the container or slot, and then select **Add Fragment**.</span></span> <span data-ttu-id="9cf8e-156">Kuvatakse dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-156">A dialog box appears.</span></span>

    ![Olemasoleva fragmendi pessa või konteinerisse lisamise kuvahõive](./media/add-fragment.png)
 
    > [!NOTE]
    > <span data-ttu-id="9cf8e-158">Kui konteiner või pesa ei toeta uusi alammooduleid, ei ole käsk **Lisa fragment** saadaval.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-158">If the container or slot doesn't support new child modules, the **Add Fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="9cf8e-159">Otsige ja valige lisamiseks dialoogiboksist fragment.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-159">In the dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="9cf8e-160">Kui ühtegi saadaolevat fragmenti loendis pole, peate kõigepealt looma fragmendi mooduli tüübist, mida valitud konteiner või pesa toetab.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-160">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="9cf8e-161">Valige soovitud fragment, et lisada see oma lehel konteinerile või pesale.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-161">Select your desired fragment to add it to the container or slot on your page.</span></span>

    ![Fragmendi valija modaalakna ekraanihõive](./media/fragment-picker.png)

> [!NOTE]
> <span data-ttu-id="9cf8e-163">Konteineris või pesas lubatud moodulid on määratletud lehe malli või moodulite enda määratlustega.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-163">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="9cf8e-164">Fragmendi eemaldamine</span><span class="sxs-lookup"><span data-stu-id="9cf8e-164">Remove a fragment</span></span>

<span data-ttu-id="9cf8e-165">Fragmendi eemaldamiseks pesast või konteinerist lehel tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-165">To remove a fragment from a slot or container on a page, follow these steps.</span></span>

1. <span data-ttu-id="9cf8e-166">Vasakult liigenduspaanilt valige eemaldatava fragmendi kõrvalt kolmikpunkti nupp ja seejärel valige prügikasti nupp.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-166">In the outline pane on the left, select the ellipsis button next to the name of the fragment to remove, and then select the trash can button.</span></span>
1. <span data-ttu-id="9cf8e-167">Kui teil palutakse kinnitada, et soovite fragmenti eemaldada, valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-167">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="9cf8e-168">Kui fragmendi lehelt eemaldate, eemaldate lehelt vaid viite sellele.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-168">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="9cf8e-169">Te **ei** kustuta fragmenti saidilt.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-169">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="9cf8e-170">Fragmentide kustutamiseks saidilt peate kasutama fragmendi kontrollija kasutajaliidest (UI).</span><span class="sxs-lookup"><span data-stu-id="9cf8e-170">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="9cf8e-171">Fragmente saate saidilt kustutada ainult siis, kui neile ei viita parasjagu ükski leht, mall või teine fragment.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-171">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="9cf8e-172">Fragmendi redigeerimine</span><span class="sxs-lookup"><span data-stu-id="9cf8e-172">Edit a fragment</span></span>

<span data-ttu-id="9cf8e-173">Fragmentide redigeerimiseks peate kasutama fragmendi redaktori kasutajaliidest.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-173">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="9cf8e-174">See piirang on kavandatud.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-174">This restriction is by design.</span></span> <span data-ttu-id="9cf8e-175">See aitab tagada, et autorid ei ajaks segi konkreetse lehe moodulite redigeerimise protsessi paljude lehtede vahel jagatavate fragmentide redigeerimise protsessiga.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-175">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="9cf8e-176">Fragmendi redigeerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-176">To edit a fragment, follow these steps.</span></span>

1. <span data-ttu-id="9cf8e-177">Valige navigeerimispaanilt vasakult suvand **Fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-177">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9cf8e-178">Valige jaotisest **Fragmendid** redigeerimiseks fragment.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-178">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="9cf8e-179">Redigeerige fragmendi mooduli atribuute ja struktuuri vajaduse järgi.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-179">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="9cf8e-180">Protsess meenutab moodulite redigeerimise protsessi, mis toimub lehe redaktori vaates.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-180">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="9cf8e-181">Saate fragmenti redigeerida ka nii, et valite selle lehelt, mallist või ülemfragmendist ja seejärel valite paremalt atribuutide paanilt suvandi **Fragmendi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9cf8e-181">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9cf8e-182">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9cf8e-182">Additional resources</span></span>

[<span data-ttu-id="9cf8e-183">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="9cf8e-183">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="9cf8e-184">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="9cf8e-184">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="9cf8e-185">Eelmääratud paigutustega töötamine</span><span class="sxs-lookup"><span data-stu-id="9cf8e-185">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="9cf8e-186">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="9cf8e-186">Work with publish groups</span></span>](publish-groups.md)
