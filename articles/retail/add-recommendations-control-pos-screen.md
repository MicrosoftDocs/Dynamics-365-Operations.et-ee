---
title: Soovituste juhtelemendi lisamine kassaaparaadi kannetelehele
description: See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 for Retaili kuvapaigutuse kujundajat.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa7d1e5392e4d3fa86bf62943cb4f5b5f4c7b383
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="7c034-103">Soovituste juhtelemendi lisamine kassaaparaadi kannetelehele</span><span class="sxs-lookup"><span data-stu-id="7c034-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!INCLUDE [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="7c034-104">Eemaldame tootesoovitusteenuse praeguse versiooni kuniks me seda funktsiooni parema algoritmi ja uuemate jaemüügile suunatud võimalustega täiustame.</span><span class="sxs-lookup"><span data-stu-id="7c034-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="7c034-105">Lisateavet vt teemast [Eemaldatud või aegunud funktsioonid](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="7c034-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="7c034-106">See teema kirjeldab, kuidas lisada soovituste juhtelement kassaaparaadi kannetekuvale, kasutades Microsoft Dynamics 365 for Retaili kuvapaigutuse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="7c034-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="7c034-107">Saate Microsoft Dynamics 365 for Retaili kasutamisel kuvada kassaaparaadis tootesoovitusi.</span><span class="sxs-lookup"><span data-stu-id="7c034-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="7c034-108">*Soovitused* on kaubad, millest teie klient võib oma ostuajaloo, oma sooviloendi kaupade ja teiste klientide võrgu- ja füüsilistest poodidest ostetud kaupade põhjal huvituda.</span><span class="sxs-lookup"><span data-stu-id="7c034-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="7c034-109">Tootesoovituste kuvamiseks peate lisama kannetekuvale juhtelemendi, kasutades kuvapaigutuse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="7c034-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="7c034-110">Paigutusekujundaja avamine</span><span class="sxs-lookup"><span data-stu-id="7c034-110">Open Layout designer</span></span>
1.  <span data-ttu-id="7c034-111">Minge jaotisse **Jaemüük** &gt; **Kanali seadistus** &gt; **Kassa seadistus** &gt; **Kassa** &gt; **Kuvapaigutused**.</span><span class="sxs-lookup"><span data-stu-id="7c034-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="7c034-112">Leidke kiirfiltri abil kuva, kuhu soovite juhtelemendi lisada.</span><span class="sxs-lookup"><span data-stu-id="7c034-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="7c034-113">Näiteks saate filtreerida välja **Kuvapaigutuse ID** väärtuse „F2CP16:9M” järgi.</span><span class="sxs-lookup"><span data-stu-id="7c034-113">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="7c034-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7c034-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="7c034-115">Valige näiteks Nimi: F2CP16:9M Kuvapaigutuse ID: F2CP16:9M”.</span><span class="sxs-lookup"><span data-stu-id="7c034-115">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="7c034-116">Klõpsake valikut **Paigutusekujundaja**.</span><span class="sxs-lookup"><span data-stu-id="7c034-116">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="7c034-117">Järgige paigutusekujundaja avamiseks viipasid.</span><span class="sxs-lookup"><span data-stu-id="7c034-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="7c034-118">Kui küsitakse identimisteavet, sisestage sama identimisteave, mida kasutasite, kui paigutusekujundaja lehel **Kuvapaigutused** käivitasite.</span><span class="sxs-lookup"><span data-stu-id="7c034-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="7c034-119">Sisselogimisel avaneb alltoodule sarnane leht.</span><span class="sxs-lookup"><span data-stu-id="7c034-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="7c034-120">Paigutus erineb olenevalt teie poele tehtud kohandustest.</span><span class="sxs-lookup"><span data-stu-id="7c034-120">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="7c034-121">[![kuvapaigutuse-pilt-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Kuvamisvaliku tegemine</span><span class="sxs-lookup"><span data-stu-id="7c034-121">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="7c034-122">Saadaval on kaks konfigureerimisvalikut.</span><span class="sxs-lookup"><span data-stu-id="7c034-122">There are two configurations options available.</span></span> <span data-ttu-id="7c034-123">Tehke oma poe jaoks sobivam valik ja järgige juhtelemendi seadistamise lõpetamiseks järelejäänud juhiseid.</span><span class="sxs-lookup"><span data-stu-id="7c034-123">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="7c034-124">Võimalused on järgmised.</span><span class="sxs-lookup"><span data-stu-id="7c034-124">The two options are:</span></span>
-   <span data-ttu-id="7c034-125">Soovitused on alati nähtaval.</span><span class="sxs-lookup"><span data-stu-id="7c034-125">Recommendations are always visible.</span></span>
-   <span data-ttu-id="7c034-126">Kuva paremas servas olevas ruudustikus kuvatakse vahekaart **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="7c034-126">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="7c034-127">Soovituste alati nähtavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="7c034-127">To make recommendations always visible</span></span>

1.  <span data-ttu-id="7c034-128">Vähendage kanderidade üksikasjade ala kõrgust, nii et see oleks sama kõrge kui vasakul asuv kliendipaneel.[](./media/pic-2.png)[![kuvapaigutuse-pilt-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="7c034-128">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="7c034-129">Pukseerige soovituste juhtelement vasakul asuvast menüüst kanderea üksikasjade ala ja kannetekuva alaosa keskel asuva nupuruudustiku vahele.</span><span class="sxs-lookup"><span data-stu-id="7c034-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="7c034-130">Muutke juhtelemendi suurust, nii et see mahuks olemasolevasse ruumi.[](./media/pic-3.png)[![kuvapaigutuse-pilt-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="7c034-130">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="7c034-131">Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.</span><span class="sxs-lookup"><span data-stu-id="7c034-131">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="7c034-132">Dynamics 365 for Retailis minge jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.</span><span class="sxs-lookup"><span data-stu-id="7c034-132">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="7c034-133">Valige loendist suvand **1090, registrid**.</span><span class="sxs-lookup"><span data-stu-id="7c034-133">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="7c034-134">Klõpsake valikut **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="7c034-134">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="7c034-135">Soovituste vahekaardi lisamine kuva paremas servas olevasse nupuruudustikku</span><span class="sxs-lookup"><span data-stu-id="7c034-135">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="7c034-136">Paremklõpsake lehe paremas servas asuva nupuruudustiku viimase vahekaardi all olevat tühja ruumi.</span><span class="sxs-lookup"><span data-stu-id="7c034-136">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="7c034-137">Klõpsake valikut **Kohanda**.[![pilt-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="7c034-137">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="7c034-138">Klõpsake valikut **Uus vahekaart**.</span><span class="sxs-lookup"><span data-stu-id="7c034-138">Click **New tab**.</span></span>
4.  <span data-ttu-id="7c034-139">Leidke vastlisatud uus vahekaart.</span><span class="sxs-lookup"><span data-stu-id="7c034-139">Find the new tab that you just added.</span></span> <span data-ttu-id="7c034-140">Võib-olla peate selleks allapoole kerima.</span><span class="sxs-lookup"><span data-stu-id="7c034-140">You may need to scroll down.</span></span>
5.  <span data-ttu-id="7c034-141">Valige ripploendist **Sisu** suvand **Soovitatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="7c034-141">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="7c034-142">[![pilt-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="7c034-142">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="7c034-143">Tippige väljale **Silt** soovituste vahekaardi nimi. Tippige näiteks „Soovitatud tooted”.</span><span class="sxs-lookup"><span data-stu-id="7c034-143">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="7c034-144">Valige väljal **Pilt** vahekaardil kuvatav pilt.</span><span class="sxs-lookup"><span data-stu-id="7c034-144">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="7c034-145">Klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c034-145">Click **OK**.</span></span> <span data-ttu-id="7c034-146">Uus vahekaart kuvatakse nupuruudustikus.</span><span class="sxs-lookup"><span data-stu-id="7c034-146">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="7c034-147">Salvestamiseks ja paigutusekujundajast väljumiseks klõpsake nuppu **X**.</span><span class="sxs-lookup"><span data-stu-id="7c034-147">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="7c034-148">Dynamics 365 for Retailis minge jaotisse **Jaemüük** &gt; **Jaemüügi IT** &gt; **Jaotusgraafikud**.</span><span class="sxs-lookup"><span data-stu-id="7c034-148">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="7c034-149">Valige loendist suvand **1090, registrid**.</span><span class="sxs-lookup"><span data-stu-id="7c034-149">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="7c034-150">Klõpsake valikut **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="7c034-150">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="7c034-151">Vt ka</span><span class="sxs-lookup"><span data-stu-id="7c034-151">See also</span></span>
--------

[<span data-ttu-id="7c034-152">Isikupärastatud tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="7c034-152">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




