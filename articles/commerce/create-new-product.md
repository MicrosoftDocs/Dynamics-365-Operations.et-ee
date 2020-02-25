---
title: Uue toote loomine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus toode.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 356bf91b2a946e7c0f5d5af9e2fe0b64342b856e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001961"
---
# <a name="create-a-new-product"></a><span data-ttu-id="dfa72-103">Uue toote loomine</span><span class="sxs-lookup"><span data-stu-id="dfa72-103">Create a new product</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dfa72-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus toode.</span><span class="sxs-lookup"><span data-stu-id="dfa72-104">This topic describes how to create a new product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dfa72-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="dfa72-105">Overview</span></span>

<span data-ttu-id="dfa72-106">Toodet defineeritakse peamiselt toote numbri, nime ja kirjeldusega.</span><span class="sxs-lookup"><span data-stu-id="dfa72-106">A product is primarily defined by a product number, name, and description.</span></span> <span data-ttu-id="dfa72-107">Kuid toote või teenuse kirjeldamiseks on vaja ka muid andmeid.</span><span class="sxs-lookup"><span data-stu-id="dfa72-107">However, other data is also required in order to describe a product or service:</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="dfa72-108">Uue toote loomine</span><span class="sxs-lookup"><span data-stu-id="dfa72-108">Create a new product</span></span>

1. <span data-ttu-id="dfa72-109">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Tooted kategooriate alusel**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Products by category**.</span></span>
1. <span data-ttu-id="dfa72-110">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="dfa72-111">Valige ripploendist **Toote tüüp** kas **Kaup** või **Teenus**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-111">In the **Product type** drop-down list, select either **Item** or **Service**.</span></span>
1. <span data-ttu-id="dfa72-112">Valige ripploendist **Toote alatüüp** kas **Toode** (kui tootel pole variante) või **Tooteetalon** (kui tootel on variandid).</span><span class="sxs-lookup"><span data-stu-id="dfa72-112">In the **Product subtype** drop-down list, select either **Product** (if the product will have no variants) or **Product master** (if the product will have variants).</span></span>
1. <span data-ttu-id="dfa72-113">Sisestage väljale **Tootenumber** tootenumber, kui see ei ole juba eelnevalt täidetud.</span><span class="sxs-lookup"><span data-stu-id="dfa72-113">In the **Product number** box, enter a product number if one is not already prepopulated.</span></span>
1. <span data-ttu-id="dfa72-114">Sisestage toote nimi väljale **Toote nimi**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-114">In the **Product name** box, enter a product name.</span></span>
1. <span data-ttu-id="dfa72-115">Sisestage otsingunimi väljale **Otsingunimi**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-115">In the **Search name** box, enter a search name.</span></span>
1. <span data-ttu-id="dfa72-116">Valige ripploendist **Jaemüügi kategooria** sobiv kategooria.</span><span class="sxs-lookup"><span data-stu-id="dfa72-116">In the **Retail category** drop-down list, select an appropriate category.</span></span>
1. <span data-ttu-id="dfa72-117">Kui toode on komplekt, valige **Jah** väljale **Tootekomplekt**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-117">If the product is a kit, select **Yes** for **Product kit**.</span></span>
1. <span data-ttu-id="dfa72-118">Kui toote alatüüp on tooteetalon, seadistage **Tootedimensiooni grupp** nii, et see sisaldaks toetatud variante.</span><span class="sxs-lookup"><span data-stu-id="dfa72-118">If the product subtype is product master, set the **Product dimension group** to include the supported variants.</span></span> <span data-ttu-id="dfa72-119">Valikute hulgas on **Värv**, **Suurus**, **Stiil** ja **Konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-119">Options include **Color**, **Size**, **Style**, and **Configuration**.</span></span> <span data-ttu-id="dfa72-120">Vajadusel peate võib-olla looma täiendavaid tootedimensioonide gruppide.</span><span class="sxs-lookup"><span data-stu-id="dfa72-120">You may need to create additional product dimension groups if needed.</span></span>
1. <span data-ttu-id="dfa72-121">Valige ripploendist **Konfiguratsiooni tehnoloogia** sobiv valik.</span><span class="sxs-lookup"><span data-stu-id="dfa72-121">In the **Configuration technology** drop-down list, select an appropriate option.</span></span>
1. <span data-ttu-id="dfa72-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-122">Select **OK**.</span></span>

<span data-ttu-id="dfa72-123">Järgmine pilt näitab näidistoote lisamist.</span><span class="sxs-lookup"><span data-stu-id="dfa72-123">The following image shows an example product being added.</span></span>

![Toote loomine](media/create-new-product.png)

<span data-ttu-id="dfa72-125">Kui toode on lisatud, saab sellele seadistada täiendavaid andmeid, nagu **Toote kirjeldus**, **Variandigrupid**, **Dimensioonigrupid**, **Toote atribuudid** ja **Seotud tooted**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-125">Once a product is added, additional data can be set for it, such as **Product description**, **Variant groups**, **Dimension groups**, **Product attributes**, and **Related products**.</span></span>

<span data-ttu-id="dfa72-126">Järgmine pilt näitab toote täiendavaid üksikasju.</span><span class="sxs-lookup"><span data-stu-id="dfa72-126">The following image shows a product's additional details.</span></span>

![Toote üksikasjad](media/create-new-product-2.png)

### <a name="create-product-variants"></a><span data-ttu-id="dfa72-128">Tootevariantide loomine</span><span class="sxs-lookup"><span data-stu-id="dfa72-128">Create product variants</span></span>

<span data-ttu-id="dfa72-129">Kui toote alatüüp on **Tooteetalon**, tuleb luua kindlad variandid.</span><span class="sxs-lookup"><span data-stu-id="dfa72-129">If the product subtype is **Product master**, specific variants will need to be created.</span></span> 

<span data-ttu-id="dfa72-130">Toote variantide loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="dfa72-130">To create product variants, follow these steps.</span></span>

1. <span data-ttu-id="dfa72-131">Klõpsake toimingupaanil suvandit **Toote variandid**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-131">On the action pane, select **Product variants**.</span></span>
1. <span data-ttu-id="dfa72-132">Kui toimingupaanil on variandi grupid valitud, valige \**Variandi soovitused*.</span><span class="sxs-lookup"><span data-stu-id="dfa72-132">If variant groups have been selected on the action pane, select \**Variant suggestions*.</span></span>
1. <span data-ttu-id="dfa72-133">Valige variandid, mida soovite toote jaoks toetada.</span><span class="sxs-lookup"><span data-stu-id="dfa72-133">Select the variants you would like to support for the product.</span></span>
1. <span data-ttu-id="dfa72-134">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-134">Select **Create**.</span></span>

## <a name="release-a-product"></a><span data-ttu-id="dfa72-135">Toote väljastamine</span><span class="sxs-lookup"><span data-stu-id="dfa72-135">Release a product</span></span>

<span data-ttu-id="dfa72-136">Toote müümiseks tuleb see kõigepealt juriidilisele isikule väljastada.</span><span class="sxs-lookup"><span data-stu-id="dfa72-136">To sell a product it must first be released to a legal entity.</span></span>

1. <span data-ttu-id="dfa72-137">Valige toote lehel **Väljasta tooteid**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-137">From the product page, select **Release products**.</span></span>

    ![Toote väljastamine](media/create-new-product-3.png)

1. <span data-ttu-id="dfa72-139">Valige väljastatav toode ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-139">Select the product to release, and then select **Next**.</span></span>

    ![Valige väljastatav toode](media/create-new-product-4.png)

1. <span data-ttu-id="dfa72-141">Valige väljastatav toote variantide komplekt ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-141">Select the set of product variants to release, and then select **Next**.</span></span>

    ![Valige väljastatavad variandid](media/create-new-product-5.png)

1. <span data-ttu-id="dfa72-143">Valige juriidiline isik ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-143">Select the legal entity, and then select **Next**.</span></span>

    ![Valige juriidiline isik](media/create-new-product-6.png)

1. <span data-ttu-id="dfa72-145">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-145">Select **Finish**.</span></span>

    ![Toote väljastamise lõpetamine](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a><span data-ttu-id="dfa72-147">Väljastatud toote konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dfa72-147">Configure a released product</span></span>

<span data-ttu-id="dfa72-148">Kui toode on vabastatud, siis on vajab see täiendavat konfiguratsiooni, mis sisaldab tootele hinna lisamist.</span><span class="sxs-lookup"><span data-stu-id="dfa72-148">Once a product is released, it will then require further configuration that includes adding a price to the product.</span></span>

1. <span data-ttu-id="dfa72-149">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Väljastatud tooted kategooria alusel**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-149">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Released products by category**.</span></span>
1. <span data-ttu-id="dfa72-150">Valige väljastatud tootele tootekategooria sõlm ja seejärel valige tooteloendist toode.</span><span class="sxs-lookup"><span data-stu-id="dfa72-150">Select the product category node for the product that was released, and then select the product from the product list.</span></span>
1. <span data-ttu-id="dfa72-151">Valige tegevuspaanil nupp **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-151">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="dfa72-152">Konfigureerige mistahes vajalikud atribuudid jaotises **Ost**, sh **Ühik**, **Hind** ja **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-152">In the **Purchase** section, configure any required properties including **Unit**, **Price**,  and **Quantity**.</span></span>
1. <span data-ttu-id="dfa72-153">Valige toimingupaanil **Kinnita**, et veenduda, et puuduvatele väljadele ei ole esitatud tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="dfa72-153">On the action pane, select **Validate** to ensure that no errors are reported for missing fields.</span></span>
1. <span data-ttu-id="dfa72-154">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dfa72-154">On the action pane, select **Save**.</span></span>

<span data-ttu-id="dfa72-155">Järgmine pilt näitab väljastatud toote konfiguratsiooni näidet.</span><span class="sxs-lookup"><span data-stu-id="dfa72-155">The following image shows an example configuration for a released product.</span></span>

![Väljastatud toote konfigureerimine](media/create-new-product-8.png)

## <a name="additional-resources"></a><span data-ttu-id="dfa72-157">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="dfa72-157">Additional resources</span></span>

[<span data-ttu-id="dfa72-158">Juriidiliste isikute loomine</span><span class="sxs-lookup"><span data-stu-id="dfa72-158">Create legal entities</span></span>](channels-legal-entities.md)

[<span data-ttu-id="dfa72-159">Variandi grupi loomine</span><span class="sxs-lookup"><span data-stu-id="dfa72-159">Create a variant group</span></span>](create-variant-group.md) 
