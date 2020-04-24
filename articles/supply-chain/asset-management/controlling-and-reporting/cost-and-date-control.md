---
title: Kulu ja kuupäeva juhtelementi
description: Selles teemas tutvustatakse kulu ja kuupäeva juhtelementi varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dc3b4d22f5ce9a7e14b3834c299fa5a86d8d2868
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205502"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="54e84-103">Kulu ja kuupäeva juhtelementi</span><span class="sxs-lookup"><span data-stu-id="54e84-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="54e84-104">Varahalduses saate kulusid arvutada, et saada ülevaade tegelikest kuludest võrreldes varade, töö asukohtade ja töökäskude eelarvekuludega.</span><span class="sxs-lookup"><span data-stu-id="54e84-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="54e84-105">Tegelikud kulud põhinevad sisestatud kannetel.</span><span class="sxs-lookup"><span data-stu-id="54e84-105">Actual costs are based on posted transactions.</span></span> 

<span data-ttu-id="54e84-106">Samuti saate teha kuupäeva arvutuse, kui soovite võrrelda plaanitud algus- ja lõppkuupäevasid töökäskude tegelike algus- ja lõppkuupäevadega.</span><span class="sxs-lookup"><span data-stu-id="54e84-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="54e84-107">Kulu juhtelement varade, töö asukohtade ja töökäskude jaoks</span><span class="sxs-lookup"><span data-stu-id="54e84-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="54e84-108">Varade, funktsionaalsete asukohtade ja töökäskude kohta tehtud arvutused on peaaegu samasugused.</span><span class="sxs-lookup"><span data-stu-id="54e84-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="54e84-109">Ainuke erinevus on, et varade ja töö asukohtade puhul saate arvutusse kaasata ka alamvarasid ja alamasukohti.</span><span class="sxs-lookup"><span data-stu-id="54e84-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="54e84-110">Kuupäev on kande kuupäev, mil registreering salvestati.</span><span class="sxs-lookup"><span data-stu-id="54e84-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="54e84-111">Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Vara kulu juhtelement** või **Töö asukoha kulu juhtelement** või **Varahaldus** > **Päringud** > **Töökäsud** > **Töökäsu kulu juhtelement**.</span><span class="sxs-lookup"><span data-stu-id="54e84-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="54e84-112">Dialoogiboksis **Vara kulu juhtelement** / **Töö asukoha kulu juhtelement** / **Töökäsu kulu juhtelement** valige arvutatav ajavahemik.</span><span class="sxs-lookup"><span data-stu-id="54e84-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="54e84-113">Kui on nõutud, valige arvutusse kaasatav finatsdimensioonikogum.</span><span class="sxs-lookup"><span data-stu-id="54e84-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="54e84-114">Kui te ei soovi nulli kuluga tulemusi näidata, valige "Jah" lülitusnupul **Jäta null vahele**.</span><span class="sxs-lookup"><span data-stu-id="54e84-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="54e84-115">Saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et kulujuhtimise read oleksid seotud töö asukohtadega.</span><span class="sxs-lookup"><span data-stu-id="54e84-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="54e84-116">Kui sisestate väljale näiteks arvu "1" ja teil on mitmetasandiline töö asukoha hierarhia, kuvatakse ülemisel tasemel kõik töö asukoha kulu juhtelemendi read ning seetõttu võivad tunnid real olla lisatud ülespoole töö asukohtades, mis asuvad madalamal tasemel.</span><span class="sxs-lookup"><span data-stu-id="54e84-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="54e84-117">Kui sisestate väljale **Tase** arvu "0", näete üksikasjalikku tulemust, mis näitab kõiki kulu juhtelemendi ridu kõigi töö asukoha tasemete kohta, millega nad on seotud.</span><span class="sxs-lookup"><span data-stu-id="54e84-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="54e84-118">Valige "Jah" tumblernupul **Kuva avatud kooskõlastatud kulu**, kui soovite seda tulpa arvutusse kaasata.</span><span class="sxs-lookup"><span data-stu-id="54e84-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="54e84-119">Märkige Jah nupul **Kaasa alavarad**, et näidata alavaradega seotud kulusid eraldi ridadena.</span><span class="sxs-lookup"><span data-stu-id="54e84-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="54e84-120">Kui soovite otsingut piirata, saate valida kindlad varad / funktsionaalsed asukohad / töökäsud **Lisamiskirjed** kiirkaardi valikus.</span><span class="sxs-lookup"><span data-stu-id="54e84-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="54e84-121">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="54e84-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="54e84-122">Alloleval joonisel kuvatakse näidet dialoogiboksist **Vara kulu juhtelement**.</span><span class="sxs-lookup"><span data-stu-id="54e84-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Dialoogiboks Vara kulu juhtimine](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="54e84-124">Klõpsale lehe **Vara kulu juhtimine** jaotise **Grupeerimisalus** nuppe, et näidata arvutuse nõutavat üksikasjalikku taset.</span><span class="sxs-lookup"><span data-stu-id="54e84-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="54e84-125">Valitud nupud **Rühmitusalus** on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="54e84-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="54e84-126">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="54e84-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="54e84-127">Näide</span><span class="sxs-lookup"><span data-stu-id="54e84-127">Example</span></span>

<span data-ttu-id="54e84-128">Alloleval kuvatõmmisel kuvatakse näidet arvutuse tulemustest dialoogiboksis **Vara kulu juhtimine**.</span><span class="sxs-lookup"><span data-stu-id="54e84-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="54e84-129">**Algne eelarve** väli näitab eelarve kulusid töökäskude prognoosist.</span><span class="sxs-lookup"><span data-stu-id="54e84-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="54e84-130">Väljal **Kooskõlastatud kulu** kuvatakse kulude kogusumma, mille juriidiline isik on võtnud kohustuseks maksta.</span><span class="sxs-lookup"><span data-stu-id="54e84-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="54e84-131">Väljal **Avatud kooskõlastatud kulu** kuvatakse kohustused maksta kaupade, tundide ja teenuste eest, mille olete tellinud või saanud, kuid mille eest pole veel maksnud.</span><span class="sxs-lookup"><span data-stu-id="54e84-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="54e84-132">Kui kõik tarbimise registreeringud on sisestatud, kuvatakse seotud kulud väljal **Tegelik kulu**.</span><span class="sxs-lookup"><span data-stu-id="54e84-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Arvutustulemuste näide lehel vara kulu juhtimine](media/02-controlling-and-reporting.png)

<span data-ttu-id="54e84-134">Teine viis kulu juhtelemendi loomiseks on teha mitmikvalik varadele suvandis **Kõik varad** või **Aktiivsed varad**.</span><span class="sxs-lookup"><span data-stu-id="54e84-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="54e84-135">Seejärel klõpsake nupule **Kulu juhtelement** vahekaardil **Üldine**. Dialoogiboksis **Vara kulu juhtelement** valitud varad sisestatakse automaatselt väljale **Vara** vahekaardil **Kaasatavad kirjed**.</span><span class="sxs-lookup"><span data-stu-id="54e84-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="54e84-136">Klõpsake **OK** ja kuvatakse kulu arvutus valitud varade kohta.</span><span class="sxs-lookup"><span data-stu-id="54e84-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="54e84-137">Sama protseduuri saab teha funktsionaalsete asukohtade puhul väljades **Kõik funktsionaalsed asukohad** või **Aktiivsed funktsionaalsed asukohad** ja ktöökäskude puhul väljades **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="54e84-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>


## <a name="work-order-date-control"></a><span data-ttu-id="54e84-138">Töökäsu kuupäevajuhtimine</span><span class="sxs-lookup"><span data-stu-id="54e84-138">Work order date control</span></span>

<span data-ttu-id="54e84-139">Kasutage seda lehte, kui soovite saata ülevaate oodatavatest algus- ja lõppkuupäevadest võrreldes töökäskude tegelike algus- ja lõppkuupäevadega.</span><span class="sxs-lookup"><span data-stu-id="54e84-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="54e84-140">Klõpsake **Varahaldus** > **Päringud** > **Töökäsud** > **Töökäsu kuupäeva juhtelement**.</span><span class="sxs-lookup"><span data-stu-id="54e84-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="54e84-141">Klõpsake valikut **Arvuta**.</span><span class="sxs-lookup"><span data-stu-id="54e84-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="54e84-142">Valige töö asukoht väljal **Töö asukoht**.</span><span class="sxs-lookup"><span data-stu-id="54e84-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="54e84-143">Sisestage vahemik, mille kohta soovite arvutust teha väljadel **Kuupäevast** ja **Kuupäevani**.</span><span class="sxs-lookup"><span data-stu-id="54e84-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="54e84-144">Kaasatakse kõik eeldatava alguskuupäevaga töökäsud vahemiku piires.</span><span class="sxs-lookup"><span data-stu-id="54e84-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="54e84-145">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="54e84-145">Click **OK**.</span></span>

6. <span data-ttu-id="54e84-146">Valige nupud **Rühmitusalus**, et vaadata arvutuse soovitud üksikasja taset.</span><span class="sxs-lookup"><span data-stu-id="54e84-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="54e84-147">Valitud nupud **Rühmitusalus** on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="54e84-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="54e84-148">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="54e84-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="54e84-149">Näide</span><span class="sxs-lookup"><span data-stu-id="54e84-149">Example</span></span>

<span data-ttu-id="54e84-150">Alloleval kuvatõmmisel kuvatakse näide arvutustulemuste kohta dialoogiboksis **Töökäsu kuupäeva juhtimine**.</span><span class="sxs-lookup"><span data-stu-id="54e84-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="54e84-151">Väljal **Keskm. alguse hilinemine** kuvatakse erinevus töökäsu plaanitud alguskuupäeva ja tegeliku alguskuupäeva vahel.</span><span class="sxs-lookup"><span data-stu-id="54e84-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="54e84-152">Näiteks kui tegelik alguskuupäev oli kaks päeva enne plaanitud alguskuupäeva, kuvatakse sellel väljal "-2".</span><span class="sxs-lookup"><span data-stu-id="54e84-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="54e84-153">Väljal **Keskm. alguse hilinemine** kuvatakse erinevus töökäsu plaanitud lõppkuupäeva ja tegeliku lõppkuupäeva vahel.</span><span class="sxs-lookup"><span data-stu-id="54e84-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="54e84-154">Näiteks kui tegelik lõppkuupäev oli kolm päeva pärast plaanitud lõppkuupäeva, kuvatakse sellel väljal "3".</span><span class="sxs-lookup"><span data-stu-id="54e84-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="54e84-155">Väljal **Esinemiskorrad** kuvatakse kõrvalekallete arv seoses töökäsu plaanitud ja tegelike alguskuupäevadega ning plaanitud ja tegelike lõppkuupäevadega.</span><span class="sxs-lookup"><span data-stu-id="54e84-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![Arvutustulemuste näide lehel Töökäsu kuupäeva juhtimine](media/03-controlling-and-reporting.png)


