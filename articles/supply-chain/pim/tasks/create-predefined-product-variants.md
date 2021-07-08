---
title: Eelmääratletud tootevariantide loomine
description: Selles protseduuris juhendatakse teid looma tooteetalonidele tootevariante, kasutades tootedimensioonide kombinatsioone.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 442a5f5b321833c170cfecc4069e62a1254605cd
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270476"
---
# <a name="predefined-product-variants"></a><span data-ttu-id="32184-103">Eelmääratletud tootevariandid</span><span class="sxs-lookup"><span data-stu-id="32184-103">Predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a><span data-ttu-id="32184-104">Näidistsenaarium: Eelmääratletud tootevariantide loomine</span><span class="sxs-lookup"><span data-stu-id="32184-104">Example scenario: Create predefined product variants</span></span>

<span data-ttu-id="32184-105">Selles näidisstenaariumis juhendatakse teid looma tooteetalonidele tootevariante, kasutades tootedimensioonide kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="32184-105">This example scenario shows how to create product variants for a product master using a combinations of product dimensions.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="32184-106">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="32184-106">Make demo data available</span></span>

<span data-ttu-id="32184-107">Selle stsenaariumi ja siinsoovitatud väärtustega töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku *USMF*.</span><span class="sxs-lookup"><span data-stu-id="32184-107">To follow this scenario using the values suggested here, you must have demo data installed, and you must select the *USMF* legal entity.</span></span>

### <a name="step-1-create-a-product-master"></a><span data-ttu-id="32184-108">Samm 1. Tooteetaloni loomine</span><span class="sxs-lookup"><span data-stu-id="32184-108">Step 1: Create a product master</span></span>

<span data-ttu-id="32184-109">Tooteetaloni loomiseks:</span><span class="sxs-lookup"><span data-stu-id="32184-109">To create a product master:</span></span>

1. <span data-ttu-id="32184-110">Avage **Tooteteabe haldus > Tooted > Tooteetalonid**.</span><span class="sxs-lookup"><span data-stu-id="32184-110">Go to **Product information management > Products > Product masters**.</span></span>
1. <span data-ttu-id="32184-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="32184-111">Select **New**.</span></span>
1. <span data-ttu-id="32184-112">Kui väljal **Tootenumber** ei ole veel numbrit, sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="32184-112">If the **Product number** field doesn't already show a number, then enter a value.</span></span> <span data-ttu-id="32184-113">See on nõutav ainult siis, kui sellele väljale pole numbrijada häälestatud.</span><span class="sxs-lookup"><span data-stu-id="32184-113">This is only required if no number sequence has been set for this field.</span></span>
1. <span data-ttu-id="32184-114">Sisestage toote nimi väljale **Toote nimi**.</span><span class="sxs-lookup"><span data-stu-id="32184-114">Enter a name in the **Product name** field.</span></span>
1. <span data-ttu-id="32184-115">Valige väljal **Tootedimensioonigrupp** tootedimensiooni grupp *SizeCol* (Suurus ja värv).</span><span class="sxs-lookup"><span data-stu-id="32184-115">In the **Product dimension group** field, select the product dimension group *SizeCol* (Size and Color).</span></span>
1. <span data-ttu-id="32184-116">Valige uue tooteemudeli loomiseks ja avamiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="32184-116">Select **OK** to create and open the new product master.</span></span>

### <a name="step-2-add-product-dimensions"></a><span data-ttu-id="32184-117">Samm 2. Tootedimensioonide lisamine</span><span class="sxs-lookup"><span data-stu-id="32184-117">Step 2: Add product dimensions</span></span>

<span data-ttu-id="32184-118">Selles näites kirjeldatakse, kuidas sisestada käsitsi tootedimensioone.</span><span class="sxs-lookup"><span data-stu-id="32184-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="32184-119">Samuti saate valida suuruse, värvi või laadi grupi, mis sisaldab tootedimensiooni väärtusi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="32184-119">You can also choose to select a size, color, or style group that includes the product dimension values you want to use.</span></span>

<span data-ttu-id="32184-120">Tootedimensioonide lisamiseks:</span><span class="sxs-lookup"><span data-stu-id="32184-120">To add product dimensions:</span></span>

1. <span data-ttu-id="32184-121">Kui uus tooteetelm on endiselt avatud, valige tegevuspaanil **tootedimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="32184-121">With your new product master still open, select **Product dimensions** on the Action Pane.</span></span>
1. <span data-ttu-id="32184-122">Avage vahekaart **Suurus** ja valige tööriistaribal **Uus**, et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="32184-122">Open the **Size** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="32184-123">Uue rea jaoks seadistage järgnev.</span><span class="sxs-lookup"><span data-stu-id="32184-123">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="32184-124">**Suurus:** valige suuruse väärtus.</span><span class="sxs-lookup"><span data-stu-id="32184-124">**Size:** Select a size value.</span></span>
    - <span data-ttu-id="32184-125">**Nimi:** sisestage suuruse nimi.</span><span class="sxs-lookup"><span data-stu-id="32184-125">**Name:** Enter a name for the size.</span></span>
1. <span data-ttu-id="32184-126">Valige tööriistaribal **Uus** ja lisage ruudustikule teine suurus, millel on uus **suurus** ja **nimi**.</span><span class="sxs-lookup"><span data-stu-id="32184-126">Select **New** on the toolbar and add a second size to the grid with a new **Size** and **Name**.</span></span>
1. <span data-ttu-id="32184-127">Avage vahekaart **Värvid** ja valige tööriistaribal **Uus**, et lisada rida ruudustikule.</span><span class="sxs-lookup"><span data-stu-id="32184-127">Open the **Colors** tab and select **New** on the toolbar to add a row to the grid.</span></span> <span data-ttu-id="32184-128">Uue rea jaoks seadistage järgnev.</span><span class="sxs-lookup"><span data-stu-id="32184-128">Make the following settings for the new row:</span></span>
    - <span data-ttu-id="32184-129">**Värv:** valige värvi väärtus.</span><span class="sxs-lookup"><span data-stu-id="32184-129">**Color:** Select a color value.</span></span>
    - <span data-ttu-id="32184-130">**Nimi:** sisestage värvi nimi.</span><span class="sxs-lookup"><span data-stu-id="32184-130">**Name:** Enter a name for the color.</span></span>
1. <span data-ttu-id="32184-131">Valige tööriistaribal **Uus** ja lisage ruudustikule teine värv, millel on uus **värv** ja **nimi**.</span><span class="sxs-lookup"><span data-stu-id="32184-131">Select **New** on the toolbar and add a second color to the grid with a new **Color** and **Name**.</span></span>
1. <span data-ttu-id="32184-132">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="32184-132">Select **Save**.</span></span>
1. <span data-ttu-id="32184-133">Uue tootekoondi juurde tagasipöördumiseks sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="32184-133">Close the page to return to your new product master.</span></span>

### <a name="step-3-generate-product-variants"></a><span data-ttu-id="32184-134">3. samm. Tootevariantide loomine</span><span class="sxs-lookup"><span data-stu-id="32184-134">Step 3: Generate product variants</span></span>

> [!NOTE]
> <span data-ttu-id="32184-135">See jaotis kirjeldab, kuidas luua tootevariantide, kui *variandisoovituste lehekülje parendusfunktsioon* ei ole lubatud.</span><span class="sxs-lookup"><span data-stu-id="32184-135">This section describes how to generate product variants when the *Variant suggestions page improvements* feature isn't enabled.</span></span> <span data-ttu-id="32184-136">Tootevariantide loomise üksikasju, kui see funktsioon on saadaval, leiate järgmisest jaotisest.</span><span class="sxs-lookup"><span data-stu-id="32184-136">See the next section for details about how to generate product variants when that feature is available.</span></span>

<span data-ttu-id="32184-137">Tootevariantide loomiseks:</span><span class="sxs-lookup"><span data-stu-id="32184-137">To generate product variants:</span></span>

1. <span data-ttu-id="32184-138">Kui uus tooteetelm on endiselt avatud, valige tegevuspaanil **tootevariandid**.</span><span class="sxs-lookup"><span data-stu-id="32184-138">With your new product master still open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="32184-139">Valige toimingupaanil suvand **Variandisoovitused**.</span><span class="sxs-lookup"><span data-stu-id="32184-139">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="32184-140">Süsteem loob loendi kõigi võimalike tootele määratud suuruste ja värvide kombinatsioonidega.</span><span class="sxs-lookup"><span data-stu-id="32184-140">The system generates a list with all possible combinations of the sizes and colors you defined for the product.</span></span> <span data-ttu-id="32184-141">Valige **Vali kõik** tööriistaribal.</span><span class="sxs-lookup"><span data-stu-id="32184-141">Select **Select all** on the toolbar.</span></span>
    - <span data-ttu-id="32184-142">Selles näites valige kõik võimalikud variandid.</span><span class="sxs-lookup"><span data-stu-id="32184-142">In this example, select all of the possible variants.</span></span> <span data-ttu-id="32184-143">Kui soovite kasutada ainult võimalike tootedimensioonide kombinatsioonide alamkogumeid, märkige vastavalt vajadusele ainult vajalikud märkeruudud.</span><span class="sxs-lookup"><span data-stu-id="32184-143">If you only want to use a subset of the possible product dimension combinations, select only the required check boxes as needed.</span></span>  
1. <span data-ttu-id="32184-144">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="32184-144">Select **Create**.</span></span>
1. <span data-ttu-id="32184-145">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="32184-145">Select **Save**.</span></span>

## <a name="improved-variant-suggestions"></a><span data-ttu-id="32184-146">Täiustatud variandisoovitused</span><span class="sxs-lookup"><span data-stu-id="32184-146">Improved variant suggestions</span></span>

<span data-ttu-id="32184-147">*Variandisoovituste lehekülje parendusfunktsioon* parandab **variandisoovituste** lehte, et lahendada jõudluse ja kasutatavuse probleemid ettevõtete puhul, kus on suur hulk tootedimensiooni kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="32184-147">The *Variant suggestions page improvements* feature improves the **Variant suggestions** page to address performance and usability issues for companies that have a high number of product dimension combinations.</span></span> <span data-ttu-id="32184-148">Täiustatud protsess tootedimensiooni väärtuste valimiseks, mille jaoks variandisoovitusi luua, muudab asjakohase tootevariantide kogumi tuvastamise ja vabastamise kiiremaks ja lihtsamaks.</span><span class="sxs-lookup"><span data-stu-id="32184-148">The enhanced process for selecting the product dimension values for which to generate variant suggestions makes it faster and easier to identify and release the relevant set of product variants.</span></span>

<span data-ttu-id="32184-149">Selle funktsiooniga lisatakse järgmised parendused:</span><span class="sxs-lookup"><span data-stu-id="32184-149">The following improvements are added by this feature:</span></span>

- <span data-ttu-id="32184-150">**Variandisoovituste edasi lükatud loomine:** **variandisoovituste** leht ei näita enam soovitusi, kui selle esimest korda avate.</span><span class="sxs-lookup"><span data-stu-id="32184-150">**Deferred generation of variant suggestions:** The **Variant suggestions** page no longer shows suggestions when you first open it.</span></span> <span data-ttu-id="32184-151">Selle asemel peate valima selgesõnaliselt soovitud väärtused ja valima kombinatsioonide loomiseks nupu **Soovita**.</span><span class="sxs-lookup"><span data-stu-id="32184-151">Instead, you must explicitly choose which values you will need and then select the **Suggest** button to generate the combinations.</span></span> <span data-ttu-id="32184-152">See muudab protsessi nähtavamaks ja interaktiivsemaks.</span><span class="sxs-lookup"><span data-stu-id="32184-152">This makes the process more visible and interactive.</span></span>
- <span data-ttu-id="32184-153">**Dimensiooniväärtuste valik:** kui teil on palju dimensiooniväärtusi, olete tavaliselt huvitatud variantide soovituste loomisest, mis sisaldavad ainult mõnda neist (nt uute värvide või stiilide kogumi tutvustamisel).</span><span class="sxs-lookup"><span data-stu-id="32184-153">**Selection of dimensions values:** When you have many dimension values, you are typically interested in generating variant suggestions that include just a few of them (such as when introducing a new set of colors or styles).</span></span> <span data-ttu-id="32184-154">Täiustatud kujundusega saate valida dimensiooniväärtused, mille jaoks soovite tootevariandi soovitusi luua.</span><span class="sxs-lookup"><span data-stu-id="32184-154">With the improved design, you can select the dimension values for which you want to generate product variant suggestions.</span></span> <span data-ttu-id="32184-155">See suurendab oluliselt soovitatud variantide olulisust ning parandab nii süsteemi jõudlust kui ka kasutajate tööviljakust.</span><span class="sxs-lookup"><span data-stu-id="32184-155">This greatly increases the relevance of the suggested variants and improves both system performance and user productivity.</span></span>

### <a name="turn-on-the-variant-suggestions-page-improvements-feature"></a><span data-ttu-id="32184-156">Variandisoovituste lehe parendusfunktsiooni sisse lülitamine</span><span class="sxs-lookup"><span data-stu-id="32184-156">Turn on the Variant suggestions page improvements feature</span></span>

<span data-ttu-id="32184-157">Enne funktsiooni *Variandisoovituste lehe parendused* kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="32184-157">Before you can use *Variant suggestions page improvements* feature, it must be turned on in your system.</span></span> <span data-ttu-id="32184-158">Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="32184-158">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="32184-159">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="32184-159">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="32184-160">**Moodul:** *Tooteteabe haldus*</span><span class="sxs-lookup"><span data-stu-id="32184-160">**Module:** *Product information management*</span></span>
- <span data-ttu-id="32184-161">**Funktsiooni nimi:** *variandisoovituste lehe parendused*</span><span class="sxs-lookup"><span data-stu-id="32184-161">**Feature name:** *Variant suggestions page improvements*</span></span>

### <a name="work-with-the-improved-variant-suggestions"></a><span data-ttu-id="32184-162">Täiustatud variandisoovitustega töötamine</span><span class="sxs-lookup"><span data-stu-id="32184-162">Work with the improved variant suggestions</span></span>

<span data-ttu-id="32184-163">See jaotis kirjeldab, kuidas luua tootevariantide, kui *variandisoovituste lehekülje parendusfunktsioon* on lubatud.</span><span class="sxs-lookup"><span data-stu-id="32184-163">To generate product variant suggestions when the *Variant suggestions page improvements* feature is enabled:</span></span>

1. <span data-ttu-id="32184-164">Avage või looge tooteetelm ja lisage sellel nõutavad tootedimensioonid, nagu kirjeldatud eelmises jaotises.</span><span class="sxs-lookup"><span data-stu-id="32184-164">Open or create a product master and add the required product dimensions to it, as described in the previous section.</span></span>
1. <span data-ttu-id="32184-165">Kui tooteetelm on endiselt avatud, valige tegevuspaanil **tootevariandid**.</span><span class="sxs-lookup"><span data-stu-id="32184-165">With the product master open, select **Product variants** on the Action Pane.</span></span>
1. <span data-ttu-id="32184-166">Valige toimingupaanil suvand **Variandisoovitused**.</span><span class="sxs-lookup"><span data-stu-id="32184-166">Select **Variant suggestions** on the Action Pane.</span></span>
1. <span data-ttu-id="32184-167">Valige väärtused, mida tahate iga mõõtmega kasutada.</span><span class="sxs-lookup"><span data-stu-id="32184-167">Select the values that you want to use for each of the dimensions.</span></span>
1. <span data-ttu-id="32184-168">Valige ülemisel tööriistaribal käsk **Soovita**.</span><span class="sxs-lookup"><span data-stu-id="32184-168">On the top toolbar, select **Suggest**.</span></span>
1. <span data-ttu-id="32184-169">Süsteem loob loendi kõigi võimalike valitud suuruste ja värvide kombinatsioonidega.</span><span class="sxs-lookup"><span data-stu-id="32184-169">The system generates a list with all possible combinations of the sizes and colors you selected.</span></span> <span data-ttu-id="32184-170">Märkige kiirkaardil **Soovitatud variandid** ruut iga tootedimensiooni kombinatsiooni jaoks, mida soovite kasutada, või valige tööriistaribal **Vali kõik**, et neid valida.</span><span class="sxs-lookup"><span data-stu-id="32184-170">On the **Suggested variants** FastTab, select the check box for each product dimension combination that you want to use, or select **Select all** on the toolbar to select all of them.</span></span>  
1. <span data-ttu-id="32184-171">Valige **Loo**, et lisada variandid praegusele tooteetelmi põhiandmetele.</span><span class="sxs-lookup"><span data-stu-id="32184-171">Select **Create** to add the variants to the current product master.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
