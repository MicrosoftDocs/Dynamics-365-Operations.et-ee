---
title: Soovituste juhtelemendi lisamine kassaseadmete kandekuvale
description: See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 for Retaili ekraanipaigutuse kujundajat.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: f17da3db6fbc19548544a0c6c090a0b6db093673
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606845"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="1360f-103">Soovituste juhtelemendi lisamine kassaseadmete kandekuvale</span><span class="sxs-lookup"><span data-stu-id="1360f-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="1360f-104">Eemaldame tootesoovitusteenuse praeguse versiooni kuniks me seda funktsiooni parema algoritmi ja uuemate jaemüügile suunatud võimalustega täiustame.</span><span class="sxs-lookup"><span data-stu-id="1360f-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="1360f-105">Lisateavet vt teemast [Eemaldatud või aegunud funktsioonid](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="1360f-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="1360f-106">See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 for Retaili ekraanipaigutuse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="1360f-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="1360f-107">Saate Microsoft Dynamics 365 for Retaili kasutamisel kuvada kassaseadmes tootesoovitusi.</span><span class="sxs-lookup"><span data-stu-id="1360f-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="1360f-108">*Soovitused* on kaubad, millest teie klient võib oma ostuajaloo, oma sooviloendi kaupade ja teiste klientide võrgu- ja füüsilistest poodidest ostetud kaupade põhjal huvituda.</span><span class="sxs-lookup"><span data-stu-id="1360f-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="1360f-109">Tootesoovituste kuvamiseks peate lisama kannetekuvale juhtelemendi, kasutades kuvapaigutuse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="1360f-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="1360f-110">Paigutusekujundaja avamine</span><span class="sxs-lookup"><span data-stu-id="1360f-110">Open Layout designer</span></span>

1. <span data-ttu-id="1360f-111">Minge jaotisse **Jaemüük** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kuvapaigutused**.</span><span class="sxs-lookup"><span data-stu-id="1360f-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="1360f-112">Leidke kiirfiltri abil kuva, kuhu soovite juhtelemendi lisada.</span><span class="sxs-lookup"><span data-stu-id="1360f-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="1360f-113">Näiteks saate filtreerida välja **Kuvapaigutuse ID** väärtuse **F2CP16:9M** järgi.</span><span class="sxs-lookup"><span data-stu-id="1360f-113">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="1360f-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1360f-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="1360f-115">Valige näiteks **Nimi: F2CP16:9M Kuvapaigutuse ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="1360f-115">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="1360f-116">Klõpsake valikut **Paigutusekujundaja**.</span><span class="sxs-lookup"><span data-stu-id="1360f-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="1360f-117">Järgige paigutusekujundaja avamiseks viipasid.</span><span class="sxs-lookup"><span data-stu-id="1360f-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="1360f-118">Kui küsitakse identimisteavet, sisestage sama identimisteave, mida kasutasite, kui paigutusekujundaja lehel **Kuvapaigutused** käivitasite.</span><span class="sxs-lookup"><span data-stu-id="1360f-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="1360f-119">Sisselogimisel avaneb alltoodule sarnane leht.</span><span class="sxs-lookup"><span data-stu-id="1360f-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="1360f-120">Paigutus erineb olenevalt teie poele tehtud kohandustest.</span><span class="sxs-lookup"><span data-stu-id="1360f-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="1360f-121">[![Paigutusekujundaja](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="1360f-121">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="1360f-122">Valige kuvatav valik</span><span class="sxs-lookup"><span data-stu-id="1360f-122">Choose a display option</span></span>

<span data-ttu-id="1360f-123">Saadaval on kaks konfigureerimisvalikut.</span><span class="sxs-lookup"><span data-stu-id="1360f-123">There are two configurations options available.</span></span> <span data-ttu-id="1360f-124">Tehke oma poe jaoks sobivam valik ja järgige juhtelemendi seadistamise lõpetamiseks järelejäänud juhiseid.</span><span class="sxs-lookup"><span data-stu-id="1360f-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="1360f-125">Võimalused on järgmised.</span><span class="sxs-lookup"><span data-stu-id="1360f-125">The two options are:</span></span>

- <span data-ttu-id="1360f-126">Soovitused on alati nähtaval.</span><span class="sxs-lookup"><span data-stu-id="1360f-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="1360f-127">Kuva paremas servas olevas ruudustikus kuvatakse vahekaart **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="1360f-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="1360f-128">Soovituste alati nähtavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="1360f-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="1360f-129">Vähendage kanderidade üksikasjade ala kõrgust, nii et see oleks sama kõrge, kui vasakul asuv kliendipaneel.</span><span class="sxs-lookup"><span data-stu-id="1360f-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="1360f-130">[![Kanderidade üksikasjade ala kõrgust on vähendatud](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="1360f-130">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="1360f-131">Pukseerige soovituste juhtelement vasakul asuvast menüüst kanderea üksikasjade ala ja kannetekuva alaosa keskel asuva nupuruudustiku vahele.</span><span class="sxs-lookup"><span data-stu-id="1360f-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="1360f-132">Muutke juhtelemendi suurust, nii et see mahuks olemasolevasse ruumi.</span><span class="sxs-lookup"><span data-stu-id="1360f-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="1360f-133">[![Paigutusele on lisatud soovituste juhtelement](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="1360f-133">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="1360f-134">Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.</span><span class="sxs-lookup"><span data-stu-id="1360f-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="1360f-135">Minge Dynamics 365 for Retailis jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.</span><span class="sxs-lookup"><span data-stu-id="1360f-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="1360f-136">Valige loendist suvand  **1090, registrid**.</span><span class="sxs-lookup"><span data-stu-id="1360f-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="1360f-137">Klõpsake valikut **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="1360f-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="1360f-138">Lisage soovituste vahekaart kuva paremas servas olevasse nupuruudustikku</span><span class="sxs-lookup"><span data-stu-id="1360f-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="1360f-139">Paremklõpsake lehe paremas servas asuva nupuruudustiku viimase vahekaardi all olevat tühja ruumi.</span><span class="sxs-lookup"><span data-stu-id="1360f-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="1360f-140">Klõpsake **Kohandada**.</span><span class="sxs-lookup"><span data-stu-id="1360f-140">Click **Customize**.</span></span>

    <span data-ttu-id="1360f-141">[![Kohandamine – vahekaardi juhtimise dialoogiboks](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="1360f-141">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="1360f-142">Klõpsake valikut **Uus vahekaart**.</span><span class="sxs-lookup"><span data-stu-id="1360f-142">Click **New tab**.</span></span>
4. <span data-ttu-id="1360f-143">Leidke vastlisatud uus vahekaart.</span><span class="sxs-lookup"><span data-stu-id="1360f-143">Find the new tab that you just added.</span></span> <span data-ttu-id="1360f-144">Võib-olla peate selleks allapoole kerima.</span><span class="sxs-lookup"><span data-stu-id="1360f-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="1360f-145">Valige ripploendist **Sisu** suvand **Soovitatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="1360f-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="1360f-146">[![Soovitatud toodete valimine sisu väljast](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="1360f-146">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="1360f-147">Tippige väljale **Silt** soovituste vahekaardi nimi. Tippige näiteks „Soovitatud tooted”.</span><span class="sxs-lookup"><span data-stu-id="1360f-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="1360f-148">Valige väljal **Pilt** vahekaardil kuvatav pilt.</span><span class="sxs-lookup"><span data-stu-id="1360f-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="1360f-149">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="1360f-149">Click **OK**.</span></span> <span data-ttu-id="1360f-150">Uus vahekaart kuvatakse nupuruudustikus.</span><span class="sxs-lookup"><span data-stu-id="1360f-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="1360f-151">Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.</span><span class="sxs-lookup"><span data-stu-id="1360f-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="1360f-152">Minge Dynamics 365 for Retailis jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.</span><span class="sxs-lookup"><span data-stu-id="1360f-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="1360f-153">Valige loendist suvand **1090, registrid**.</span><span class="sxs-lookup"><span data-stu-id="1360f-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="1360f-154">Klõpsake valikut **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="1360f-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1360f-155">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1360f-155">Additional resources</span></span>

[<span data-ttu-id="1360f-156">Isikupärastatud tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="1360f-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)
