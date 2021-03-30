---
title: Fragmentidega töötamine
description: Selles teemas kirjeldatakse, miks, millal ja kuidas kasutada fragmente rakenduses Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3df2d99ef10f909cedef16167fb8d5a0024683b3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210943"
---
# <a name="work-with-fragments"></a><span data-ttu-id="9b7a9-103">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="9b7a9-103">Work with fragments</span></span> 

[!include [banner](includes/banner.md)]

<span data-ttu-id="9b7a9-104">Selles teemas kirjeldatakse, miks, millal ja kuidas kasutada fragmente rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-104">This topic describes why, when, and how to use fragments in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9b7a9-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="9b7a9-105">Overview</span></span>

<span data-ttu-id="9b7a9-106">Fragmendid tagavad tsentraliseeritud loomiskogemuse mooduli konfiguratsioonidele, mida tuleb kogu saidil uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-106">Fragments allow for a centralized authoring experience for module configurations that must be reused throughout your site.</span></span> <span data-ttu-id="9b7a9-107">Näiteks päiseid, jaluseid ja ribareklaame konfigureeritakse sageli fragmentidena, kuna neid jagatakse paljude lehtede vahel.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-107">For example, headers, footers, and banners are often configured as fragments, because they are shared across many pages.</span></span> <span data-ttu-id="9b7a9-108">Mõelge fragmentidest kui miniatuursetest veebisaitidest, mida saab sisestada teie saidi teistele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-108">You can think of fragments as miniature webpages that can be inserted into other pages on your site.</span></span> <span data-ttu-id="9b7a9-109">Fragmentidel on oma elutsükkel.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-109">Fragments have their own lifecycle.</span></span> <span data-ttu-id="9b7a9-110">Teisisõnu need luuakse, neile viidatakse, neid värskendatakse ja need kustutatakse loomistööriistade sõltumatute üksustena.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-110">In other words, they are created, referenced, updated, and deleted as independent entities in the authoring tools.</span></span>

<span data-ttu-id="9b7a9-111">Pärast fragmentide konfigureerimist saab neid kasutada kõikjal teie saidi struktuuris, kus saab kasutada mooduleid.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-111">After fragments are configured, they can be used wherever modules can be used in your site structure.</span></span> <span data-ttu-id="9b7a9-112">Fragmentidele saab lehtedel, paigutustes, mallide ja teistes fragmentides viidata.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-112">Fragments can be referenced on pages, in layouts, in templates, and in other fragments.</span></span>

> [!NOTE]
> <span data-ttu-id="9b7a9-113">Fragmendid võivad olla kuni seitsme taseme sügavusel teistes fragmentides.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-113">Fragments can be nested up to seven levels deep inside other fragments.</span></span>

<span data-ttu-id="9b7a9-114">Näiteks kui soovite reklaamida hooajalist sündmust saidi paljudel lehtedel, võite selleks kasutada fragmenti.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-114">For example, if you want to promote a seasonal event cross many pages on our site, you can use a fragment.</span></span> <span data-ttu-id="9b7a9-115">Uue fragmendi loomise esimene samm on valida mooduli tüüp, millest soovite alustada.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-115">The first step in the process of creating a new fragment is to select the type of module that you want to start from.</span></span> <span data-ttu-id="9b7a9-116">Selles näites saate luua fragmendi pannoomoodulist.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-116">For this example, you can build the fragment from a hero module.</span></span>

> [!NOTE]
> <span data-ttu-id="9b7a9-117">Fragmente saab luua igast mooduli tüübist.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-117">Fragments can be built from any module type.</span></span>

<span data-ttu-id="9b7a9-118">Seejärel saate konfigureerida pannoofragmendi konkreetse kampaaniasisuga.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-118">You can then configure the hero fragment with your specific promotional content.</span></span> <span data-ttu-id="9b7a9-119">Saate seda ka vajaduse järgi lokaliseerida.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-119">You can also localize it as you require.</span></span> <span data-ttu-id="9b7a9-120">Uut eraldiseisevat pannoofragmenti saab seejärel kasutada eelkonfigureeritud moodulina kogu saidil.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-120">The new stand-alone hero fragment can then be consumed as a preconfigured module throughout your site.</span></span> <span data-ttu-id="9b7a9-121">Saate seda hõlpsasti lisada mallidele, konkreetsetele lehtedele või teistele fragmentidele, mis sisaldavad pannoomooduleid.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-121">You can easily add it to templates, to specific pages, or to other fragments that can contain hero modules.</span></span>

<span data-ttu-id="9b7a9-122">Kõik kohad, kuhu fragment lisatakse, on viited loodud kesksele pannoofragmendile.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-122">All the places where the fragment is added are references to the central hero fragment that you created.</span></span> <span data-ttu-id="9b7a9-123">Kui avaldate fragmendi muudatused, kajastuvad need muudatused kohe kõikides kohtades üle saidi, kus fragmendile viidatakse.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-123">If you publish changes to the fragment, those changes are immediately reflected in all the places where the fragment is referenced across the site.</span></span> <span data-ttu-id="9b7a9-124">Seega pakuvad fragmendid võimsat ja tõhusat moodust mooduli konfiguratsioonide uuesti kasutamiseks ja tsentraalselt haldamiseks saidil.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-124">Therefore, fragments provide a powerful and efficient way to reuse and centrally manage module configurations on a site.</span></span> <span data-ttu-id="9b7a9-125">Neid tõhusalt kasutades saate muuta töö oluliselt kiiremaks ja vähendada saidi haldamisega seotud kulusid.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-125">By effectively using them, you can significantly increase agility and help reduce the cost that is associated with managing site content.</span></span>

<span data-ttu-id="9b7a9-126">Järgmisel joonisel on näha, kuidas saab fragmente kasutada jagatud mooduli konfiguratsioonide loomise tsentraliseerimiseks üle e-kaubanduse saidi.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-126">The following illustration shows how fragments can be used to centralize authoring of shared module configurations across an e-Commerce site.</span></span>

![Näide sellest, kuidas saab fragmente kasutada jagatud mooduli konfiguratsioonide loomise tsentraliseerimiseks üle e-kaubanduse saidi.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a><span data-ttu-id="9b7a9-128">Fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="9b7a9-128">Create a fragment</span></span>

<span data-ttu-id="9b7a9-129">Saate kas luua uue fragmendi või salvestada olemasoleva mooduli konfiguratsiooni fragmendina.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-129">You can either create a new fragment or save an existing module configuration as a fragment.</span></span>

### <a name="save-an-existing-module-configuration-as-a-fragment"></a><span data-ttu-id="9b7a9-130">Olemasoleva mooduli konfiguratsiooni salvestamine fragmendina</span><span class="sxs-lookup"><span data-stu-id="9b7a9-130">Save an existing module configuration as a fragment</span></span>

<span data-ttu-id="9b7a9-131">Varem konfigureeritud mooduli teisendamiseks korduskasutatavaks fragmendiks Commerce'i saidiehitajas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-131">To convert a previously configured module to a reusable fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9b7a9-132">Avage leht või mall, mis sisaldab moodulit, mida soovite teisendada fragmendiks.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-132">Open a page or template that contains the module that you want to convert to a fragment.</span></span>
1. <span data-ttu-id="9b7a9-133">Valige vasakul liigenduspaanil või otse visuaalses leheehitajas eelnevalt konfigureeritud moodul.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-133">In the outline pane on the left or directly in visual page builder, select the previously configured module.</span></span>
1. <span data-ttu-id="9b7a9-134">Valige kolmikpunkt (**...**) mooduli nime kõrval kas liigenduspaanil või visuaalses leheehitajas valitud mooduli tööriistaribal.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-134">Select the ellipsis (**...**) next to the name of the module in either the outline pane or the selected module's toolbar in visual page builder.</span></span> 
1. <span data-ttu-id="9b7a9-135">Valige **Jaga fragmendina**.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-135">Select **Share as fragment**.</span></span> 
1. <span data-ttu-id="9b7a9-136">Sisestage dialoogiboksis **Salvesta fragmendina** fragmendi nimi.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-136">In the **Save as fragment** dialog box, enter a name for the fragment.</span></span>
1. <span data-ttu-id="9b7a9-137">Valige nupp **OK**, et salvestada mooduli konfiguratsioon fragmendina, mida saab lisada teistele lehtedele.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-137">Select **OK** to save the module configuration as a fragment that can be added to other pages.</span></span>
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a><span data-ttu-id="9b7a9-138">Loo uus fragment</span><span class="sxs-lookup"><span data-stu-id="9b7a9-138">Create a new fragment</span></span>

<span data-ttu-id="9b7a9-139">Uue fragmendi loomiseks Commerce'i saidiehitajas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-139">To create a new fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9b7a9-140">Valige navigeerimispaanilt vasakult suvand **Fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-140">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9b7a9-141">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-141">Select **New**.</span></span> <span data-ttu-id="9b7a9-142">Kuvatakse dialoogiboks **Uus fragment**, kus on näha kõik saadaolevad mooduli tüübid.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-142">A **New fragment** dialog box appears that shows all the available module types.</span></span> <span data-ttu-id="9b7a9-143">Nagu varem mainitud, fragmente saab luua igast mooduli tüübist.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-143">As was mentioned earlier, fragments can be created from any module type.</span></span>
1. <span data-ttu-id="9b7a9-144">Valige oma fragmendi jaoks mooduli tüüp.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-144">Select a module type for your fragment.</span></span>

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment](./media/fragment-nav-menu.png)-->
> [!TIP]
> <span data-ttu-id="9b7a9-145">Valides üldkonteineri mooduli tüübi, on teil hiljem fragmendi värskendamise ja konfigureerimise vajadusel kõige rohkem vabadust.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-145">By selecting a generic container module type, you get the most flexibility when you need to update and configure your fragment later.</span></span>

## <a name="add-remove-or-edit-fragments-on-a-page"></a><span data-ttu-id="9b7a9-146">Fragmentide lisamine, eemaldamine või redigeerimine lehel</span><span class="sxs-lookup"><span data-stu-id="9b7a9-146">Add, remove, or edit fragments on a page</span></span>

<span data-ttu-id="9b7a9-147">Järgmistes protseduurides kirjeldatakse, kuidas fragmente lisada, eemaldada ja redigeerida.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-147">The following procedures describe how to add, remove, and edit fragments.</span></span>

### <a name="add-a-fragment"></a><span data-ttu-id="9b7a9-148">Fragmendi lisamine</span><span class="sxs-lookup"><span data-stu-id="9b7a9-148">Add a fragment</span></span>

<span data-ttu-id="9b7a9-149">Lehele uue fragmendi lisamiseks Commerce'i saidiehitajas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-149">To add a fragment to a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9b7a9-150">Valige vasakult liigenduspaanilt või otse visuaalsest leheehitajast konteiner või pesa, kuhu võib lisada alammoodulid.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-150">In the outline pane on the left or directly in visual page builder, select a container or slot to which child modules can be added.</span></span>
1. <span data-ttu-id="9b7a9-151">Valige kolmikpunkt (**...**) konteineri või pesa nime kõrval.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-151">Select the ellipsis (**...**) next to the name of the container or slot.</span></span>  <span data-ttu-id="9b7a9-152">Kui kasutate visuaalset leheehitajat, valige teise võimalusena pluss-sümbol (**+**).</span><span class="sxs-lookup"><span data-stu-id="9b7a9-152">Alternately, if using visual page builder, select the plus symbol (**+**).</span></span>  
1. <span data-ttu-id="9b7a9-153">Valige **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-153">Select **Add fragment**.</span></span>
    <!-- ![A screen capture of how to add an existing fragment to a slot or container](./media/add-fragment.png)-->
 
    > [!NOTE]
    > <span data-ttu-id="9b7a9-154">Kui konteiner või pesa ei toeta uusi alammooduleid, ei ole suvand **Lisa fragment** saadaval.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-154">If the container or slot doesn't support new child modules, the **Add fragment** option is unavailable.</span></span>
    
1. <span data-ttu-id="9b7a9-155">Otsige dialoogiboksist **Lisa fragment** fragmenti ja valige see lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-155">In the **Select fragment** dialog box, search for and select a fragment to add.</span></span> <span data-ttu-id="9b7a9-156">Kui ühtegi saadaolevat fragmenti loendis pole, peate kõigepealt looma fragmendi mooduli tüübist, mida valitud konteiner või pesa toetab.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-156">If no available fragments are listed, you might first have to create a fragment from a module type that the selected container or slot supports.</span></span>
1. <span data-ttu-id="9b7a9-157">Valige soovitud fragment, et lisada see oma lehel konteinerile või pesale.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-157">Select your desired fragment to add it to the container or slot on your page.</span></span>
<!--    ![A screen capture of the fragment picker modal window](./media/fragment-picker.png)-->

> [!NOTE]
> <span data-ttu-id="9b7a9-158">Konteineris või pesas lubatud moodulid on määratletud lehe malli või moodulite enda määratlustega.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-158">The modules that are allowed in a container or slot are defined by the page's template or the modules' own definitions.</span></span>

### <a name="remove-a-fragment"></a><span data-ttu-id="9b7a9-159">Fragmendi eemaldamine</span><span class="sxs-lookup"><span data-stu-id="9b7a9-159">Remove a fragment</span></span>

<span data-ttu-id="9b7a9-160">Fragmendi eemaldamiseks pesast või konteinerist Commerce'i saidiehitaja lehel, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-160">To remove a fragment from a slot or container on a page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9b7a9-161">Vasakult liigenduspaanilt valige eemaldatava fragmendi kõrvalt kolmikpunkt (**...**) ja seejärel valige prügikasti tähis.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-161">In the outline pane on the left, select the ellipsis (**...**) next to the name of the fragment to be removed, and then select the trash can symbol.</span></span>  <span data-ttu-id="9b7a9-162">Alternatiivselt saate valida visuaalses leheehitajas fragmendi ja valida fragmendi tööriistaribal prügikasti tähise.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-162">Alternately, you can select the fragment in visual page builder and select the trash can symbol in the fragment's toolbar.</span></span>
1. <span data-ttu-id="9b7a9-163">Kui teil palutakse kinnitada, et soovite fragmenti eemaldada, valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-163">When you're prompted to confirm that you want to remove the fragment, select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="9b7a9-164">Kui fragmendi lehelt eemaldate, eemaldate lehelt vaid viite sellele.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-164">When you remove a fragment from a page, you just remove the reference to it from that page.</span></span> <span data-ttu-id="9b7a9-165">Te **ei** kustuta fragmenti saidilt.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-165">You do **not** delete the fragment from your site.</span></span> <span data-ttu-id="9b7a9-166">Fragmentide kustutamiseks saidilt peate kasutama fragmendi kontrollija kasutajaliidest (UI).</span><span class="sxs-lookup"><span data-stu-id="9b7a9-166">To delete fragments from your site, you must use the fragment inspector user interface (UI).</span></span> <span data-ttu-id="9b7a9-167">Fragmente saate saidilt kustutada ainult siis, kui neile ei viita parasjagu ükski leht, mall või teine fragment.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-167">You can delete fragments from a site only if they aren't currently referenced by any pages, templates, or other fragments.</span></span>

### <a name="edit-a-fragment"></a><span data-ttu-id="9b7a9-168">Fragmendi redigeerimine</span><span class="sxs-lookup"><span data-stu-id="9b7a9-168">Edit a fragment</span></span>

<span data-ttu-id="9b7a9-169">Fragmentide redigeerimiseks peate kasutama fragmendi redaktori kasutajaliidest.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-169">To edit fragments, you must use the fragment editor UI.</span></span> <span data-ttu-id="9b7a9-170">See piirang on kavandatud.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-170">This restriction is by design.</span></span> <span data-ttu-id="9b7a9-171">See aitab tagada, et autorid ei ajaks segi konkreetse lehe moodulite redigeerimise protsessi paljude lehtede vahel jagatavate fragmentide redigeerimise protsessiga.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-171">It helps guarantee that authors don't confuse the process of editing the modules for a specific page with the process of editing fragments that might be shared across many pages.</span></span>

<span data-ttu-id="9b7a9-172">Fragmendi redigeerimiseks Commerce'i saidiehitajas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-172">To edit a fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="9b7a9-173">Valige navigeerimispaanilt vasakult suvand **Fragmendid**.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-173">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="9b7a9-174">Valige jaotisest **Fragmendid** redigeerimiseks fragment.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-174">Under **Fragments**, select the fragment to edit.</span></span>
1. <span data-ttu-id="9b7a9-175">Redigeerige fragmendi mooduli atribuute ja struktuuri vajaduse järgi.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-175">Edit the fragment's module properties and structure as you require.</span></span> <span data-ttu-id="9b7a9-176">Protsess meenutab moodulite redigeerimise protsessi, mis toimub lehe redaktori vaates.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-176">The process resembles the process for editing modules are edited in the page editor view.</span></span>

<span data-ttu-id="9b7a9-177">Saate fragmenti redigeerida ka nii, et valite selle lehelt, mallist või ülemfragmendist ja seejärel valite paremalt atribuutide paanilt suvandi **Fragmendi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="9b7a9-177">You can also edit a fragment by selecting it on a page, in a template, or in a parent fragment, and then selecting **Edit Fragment** in the properties pane on the right.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9b7a9-178">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9b7a9-178">Additional resources</span></span>

[<span data-ttu-id="9b7a9-179">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="9b7a9-179">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="9b7a9-180">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="9b7a9-180">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="9b7a9-181">Eelmääratud paigutustega töötamine</span><span class="sxs-lookup"><span data-stu-id="9b7a9-181">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="9b7a9-182">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="9b7a9-182">Work with publish groups</span></span>](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]