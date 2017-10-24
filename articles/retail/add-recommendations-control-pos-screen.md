---
title: Soovituste juhtelemendi lisamine kassaaparaadi kannetelehele
description: See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 for Retaili kuvapaigutuse kujundajat.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4cdfcbdcafdbbbab21c398ebc8002a45742e33e6
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="f9369-103">Soovituste juhtelemendi lisamine kassaaparaadi kannetelehele</span><span class="sxs-lookup"><span data-stu-id="f9369-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="f9369-104">See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 for Retaili kuvapaigutuse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="f9369-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="f9369-105">Saate Microsoft Dynamics 365 for Retaili kasutamisel kuvada kassaaparaadis tootesoovitusi.</span><span class="sxs-lookup"><span data-stu-id="f9369-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="f9369-106">*Soovitused* on kaubad, millest teie klient võib oma ostuajaloo, oma sooviloendi kaupade ja teiste klientide võrgu- ja füüsilistest poodidest ostetud kaupade põhjal huvituda.</span><span class="sxs-lookup"><span data-stu-id="f9369-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="f9369-107">Tootesoovituste kuvamiseks peate lisama kannetekuvale juhtelemendi, kasutades kuvapaigutuse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="f9369-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="f9369-108">Paigutusekujundaja avamine</span><span class="sxs-lookup"><span data-stu-id="f9369-108">Open Layout designer</span></span>
1.  <span data-ttu-id="f9369-109">Minge jaotisse **Jaemüük** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kuvapaigutused**.</span><span class="sxs-lookup"><span data-stu-id="f9369-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="f9369-110">Leidke kiirfiltri abil kuva, kuhu soovite juhtelemendi lisada.</span><span class="sxs-lookup"><span data-stu-id="f9369-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="f9369-111">Näiteks saate filtreerida välja **Kuvapaigutuse ID** väärtuse „F2CP16:9M” järgi.</span><span class="sxs-lookup"><span data-stu-id="f9369-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="f9369-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f9369-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="f9369-113">Valige näiteks Nimi: F2CP16:9M Kuvapaigutuse ID: F2CP16:9M”.</span><span class="sxs-lookup"><span data-stu-id="f9369-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="f9369-114">Klõpsake valikut **Paigutusekujundaja**.</span><span class="sxs-lookup"><span data-stu-id="f9369-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="f9369-115">Järgige paigutusekujundaja avamiseks viipasid.</span><span class="sxs-lookup"><span data-stu-id="f9369-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="f9369-116">Kui küsitakse identimisteavet, sisestage sama identimisteave, mida kasutasite, kui paigutusekujundaja lehel **Kuvapaigutused** käivitasite.</span><span class="sxs-lookup"><span data-stu-id="f9369-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="f9369-117">Sisselogimisel avaneb alltoodule sarnane leht.</span><span class="sxs-lookup"><span data-stu-id="f9369-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="f9369-118">Paigutus erineb olenevalt teie poele tehtud kohandustest.</span><span class="sxs-lookup"><span data-stu-id="f9369-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="f9369-119">[![kuvapaigutuse-pilt-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Kuvamisvaliku tegemine</span><span class="sxs-lookup"><span data-stu-id="f9369-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="f9369-120">Saadaval on kaks konfigureerimisvalikut.</span><span class="sxs-lookup"><span data-stu-id="f9369-120">There are two configurations options available.</span></span> <span data-ttu-id="f9369-121">Tehke oma poe jaoks sobivam valik ja järgige juhtelemendi seadistamise lõpetamiseks järelejäänud juhiseid.</span><span class="sxs-lookup"><span data-stu-id="f9369-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="f9369-122">Võimalused on järgmised.</span><span class="sxs-lookup"><span data-stu-id="f9369-122">The two options are:</span></span>
-   <span data-ttu-id="f9369-123">Soovitused on alati nähtaval.</span><span class="sxs-lookup"><span data-stu-id="f9369-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="f9369-124">Kuva paremas servas olevas ruudustikus kuvatakse vahekaart **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="f9369-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="f9369-125">Soovituste alati nähtavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="f9369-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="f9369-126">Vähendage kanderidade üksikasjade ala kõrgust, nii et see oleks sama kõrge kui vasakul asuv kliendipaneel.[](./media/pic-2.png)[![kuvapaigutuse-pilt-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="f9369-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="f9369-127">Pukseerige soovituste juhtelement vasakul asuvast menüüst kanderea üksikasjade ala ja kannetekuva alaosa keskel asuva nupuruudustiku vahele.</span><span class="sxs-lookup"><span data-stu-id="f9369-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="f9369-128">Muutke juhtelemendi suurust, nii et see mahuks olemasolevasse ruumi.[](./media/pic-3.png)[![kuvapaigutuse-pilt-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="f9369-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="f9369-129">Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.</span><span class="sxs-lookup"><span data-stu-id="f9369-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="f9369-130">Dynamics 365 for Retailis minge jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.</span><span class="sxs-lookup"><span data-stu-id="f9369-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="f9369-131">Valige loendist suvand **1090, registrid**.</span><span class="sxs-lookup"><span data-stu-id="f9369-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="f9369-132">Klõpsake valikut **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="f9369-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="f9369-133">Soovituste vahekaardi lisamine kuva paremas servas olevasse nupuruudustikku</span><span class="sxs-lookup"><span data-stu-id="f9369-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="f9369-134">Paremklõpsake lehe paremas servas asuva nupuruudustiku viimase vahekaardi all olevat tühja ruumi.</span><span class="sxs-lookup"><span data-stu-id="f9369-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="f9369-135">Klõpsake valikut **Kohanda**.[![pilt-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="f9369-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="f9369-136">Klõpsake valikut **Uus vahekaart**.</span><span class="sxs-lookup"><span data-stu-id="f9369-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="f9369-137">Leidke vastlisatud uus vahekaart.</span><span class="sxs-lookup"><span data-stu-id="f9369-137">Find the new tab that you just added.</span></span> <span data-ttu-id="f9369-138">Võib-olla peate selleks allapoole kerima.</span><span class="sxs-lookup"><span data-stu-id="f9369-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="f9369-139">Valige ripploendist **Sisu** suvand **Soovitatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="f9369-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="f9369-140">[![pilt-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="f9369-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="f9369-141">Tippige väljale **Silt** soovituste vahekaardi nimi. Tippige näiteks „Soovitatud tooted”.</span><span class="sxs-lookup"><span data-stu-id="f9369-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="f9369-142">Valige väljal **Pilt** vahekaardil kuvatav pilt.</span><span class="sxs-lookup"><span data-stu-id="f9369-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="f9369-143">Klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9369-143">Click **OK**.</span></span> <span data-ttu-id="f9369-144">Uus vahekaart kuvatakse nupuruudustikus.</span><span class="sxs-lookup"><span data-stu-id="f9369-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="f9369-145">Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.</span><span class="sxs-lookup"><span data-stu-id="f9369-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="f9369-146">Dynamics 365 for Retailis minge jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.</span><span class="sxs-lookup"><span data-stu-id="f9369-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="f9369-147">Valige loendist suvand **1090, registrid**.</span><span class="sxs-lookup"><span data-stu-id="f9369-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="f9369-148">Klõpsake valikut **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="f9369-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="f9369-149">Vt ka</span><span class="sxs-lookup"><span data-stu-id="f9369-149">See also</span></span>
--------

[<span data-ttu-id="f9369-150">Isikupärastatud tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="f9369-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




