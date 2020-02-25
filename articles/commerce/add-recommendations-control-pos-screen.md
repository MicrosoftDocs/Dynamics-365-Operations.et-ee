---
title: Soovituste juhtelemendi lisamine kassaseadmete kandekuvale
description: See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 Commercei ekraanipaigutuse kujundajat.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6d6f48197a36f633e3cd63cbad4518f53946fc7f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022213"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="f5a80-103">Soovituste juhtelemendi lisamine kassaseadmete kandekuvale</span><span class="sxs-lookup"><span data-stu-id="f5a80-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="f5a80-104">See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 Commercei ekraanipaigutuse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="f5a80-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="f5a80-105">Lisateavet tootesoovituste kohta lugege teemast [Tootesoovitused kassa dokumentatsioonis](product.md).</span><span class="sxs-lookup"><span data-stu-id="f5a80-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="f5a80-106">Saate Commerce'i kasutamisel kuvada kassaseadmes tootesoovitusi.</span><span class="sxs-lookup"><span data-stu-id="f5a80-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="f5a80-107">Tootesoovituste kuvamiseks peate lisama kannetekuvale juhtelemendi, kasutades kuvapaigutuse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="f5a80-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="f5a80-108">Paigutusekujundaja avamine</span><span class="sxs-lookup"><span data-stu-id="f5a80-108">Open Layout designer</span></span>

1. <span data-ttu-id="f5a80-109">Avage **Jaemüük ja kaubandus** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kuvapaigutused**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="f5a80-110">Leidke kiirfiltri abil kuva, kuhu soovite juhtelemendi lisada.</span><span class="sxs-lookup"><span data-stu-id="f5a80-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="f5a80-111">Näiteks saate filtreerida välja **Kuvapaigutuse ID** väärtuse **F2CP16:9M** järgi.</span><span class="sxs-lookup"><span data-stu-id="f5a80-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="f5a80-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f5a80-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="f5a80-113">Valige näiteks **Nimi: F2CP16:9M Kuvapaigutuse ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="f5a80-114">Klõpsake valikut **Paigutusekujundaja**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="f5a80-115">Järgige paigutusekujundaja avamiseks viipasid.</span><span class="sxs-lookup"><span data-stu-id="f5a80-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="f5a80-116">Kui küsitakse identimisteavet, sisestage sama identimisteave, mida kasutasite, kui paigutusekujundaja lehel **Kuvapaigutused** käivitasite.</span><span class="sxs-lookup"><span data-stu-id="f5a80-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="f5a80-117">Sisselogimisel avaneb alltoodule sarnane leht.</span><span class="sxs-lookup"><span data-stu-id="f5a80-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="f5a80-118">Paigutus erineb olenevalt teie poele tehtud kohandustest.</span><span class="sxs-lookup"><span data-stu-id="f5a80-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="f5a80-119">[![Paigutusekujundaja](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="f5a80-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="f5a80-120">Valige kuvatav valik</span><span class="sxs-lookup"><span data-stu-id="f5a80-120">Choose a display option</span></span>

<span data-ttu-id="f5a80-121">Saadaval on kaks konfigureerimisvalikut.</span><span class="sxs-lookup"><span data-stu-id="f5a80-121">There are two configurations options available.</span></span> <span data-ttu-id="f5a80-122">Tehke oma poe jaoks sobivam valik ja järgige juhtelemendi seadistamise lõpetamiseks järelejäänud juhiseid.</span><span class="sxs-lookup"><span data-stu-id="f5a80-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="f5a80-123">Võimalused on järgmised.</span><span class="sxs-lookup"><span data-stu-id="f5a80-123">The two options are:</span></span>

- <span data-ttu-id="f5a80-124">Soovitused on alati nähtaval.</span><span class="sxs-lookup"><span data-stu-id="f5a80-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="f5a80-125">Kuva paremas servas olevas ruudustikus kuvatakse vahekaart **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="f5a80-126">Soovituste alati nähtavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="f5a80-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="f5a80-127">Vähendage kanderidade üksikasjade ala kõrgust, nii et see oleks sama kõrge, kui vasakul asuv kliendipaneel.</span><span class="sxs-lookup"><span data-stu-id="f5a80-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="f5a80-128">[![Kanderidade üksikasjade ala kõrgust on vähendatud](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="f5a80-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="f5a80-129">Pukseerige soovituste juhtelement vasakul asuvast menüüst kanderea üksikasjade ala ja kannetekuva alaosa keskel asuva nupuruudustiku vahele.</span><span class="sxs-lookup"><span data-stu-id="f5a80-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="f5a80-130">Muutke juhtelemendi suurust, nii et see mahuks olemasolevasse ruumi.</span><span class="sxs-lookup"><span data-stu-id="f5a80-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="f5a80-131">[![Paigutusele on lisatud soovituste juhtelement](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="f5a80-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="f5a80-132">Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="f5a80-133">Avage Commerce'is **Jaemüük ja kaubandus** &gt; **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafikud**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="f5a80-134">Valige loendist suvand **1090, registrid**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="f5a80-135">Klõpsake valikut **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="f5a80-136">Lisage soovituste vahekaart kuva paremas servas olevasse nupuruudustikku</span><span class="sxs-lookup"><span data-stu-id="f5a80-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="f5a80-137">Paremklõpsake lehe paremas servas asuva nupuruudustiku viimase vahekaardi all olevat tühja ruumi.</span><span class="sxs-lookup"><span data-stu-id="f5a80-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="f5a80-138">Klõpsake **Kohandada**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-138">Click **Customize**.</span></span>

    <span data-ttu-id="f5a80-139">[![Kohandamine – vahekaardi juhtimise dialoogiboks](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="f5a80-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="f5a80-140">Klõpsake valikut **Uus vahekaart**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-140">Click **New tab**.</span></span>
4. <span data-ttu-id="f5a80-141">Leidke vastlisatud uus vahekaart.</span><span class="sxs-lookup"><span data-stu-id="f5a80-141">Find the new tab that you just added.</span></span> <span data-ttu-id="f5a80-142">Võib-olla peate selleks allapoole kerima.</span><span class="sxs-lookup"><span data-stu-id="f5a80-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="f5a80-143">Valige ripploendist **Sisu** suvand **Soovitatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="f5a80-144">[![Soovitatud toodete valimine sisu väljast](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="f5a80-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="f5a80-145">Tippige väljale **Silt** soovituste vahekaardi nimi. Tippige näiteks „Soovitatud tooted”.</span><span class="sxs-lookup"><span data-stu-id="f5a80-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="f5a80-146">Valige väljal **Pilt** vahekaardil kuvatav pilt.</span><span class="sxs-lookup"><span data-stu-id="f5a80-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="f5a80-147">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-147">Click **OK**.</span></span> <span data-ttu-id="f5a80-148">Uus vahekaart kuvatakse nupuruudustikus.</span><span class="sxs-lookup"><span data-stu-id="f5a80-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="f5a80-149">Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="f5a80-150">Avage Commerce'is **Jaemüük ja kaubandus** &gt; **Jaemüügi ja kaubanduse IT** &gt; **Jaotusgraafikud**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="f5a80-151">Valige loendist suvand **1090, registrid**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="f5a80-152">Klõpsake valikut **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="f5a80-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5a80-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="f5a80-153">Additional resources</span></span>

[<span data-ttu-id="f5a80-154">Tootesoovitused kassas</span><span class="sxs-lookup"><span data-stu-id="f5a80-154">Product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="f5a80-155">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="f5a80-155">Product recommendations overview</span></span>](../commerce/product-recommendations.md)
