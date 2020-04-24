---
title: Vara vea analüüs
description: Selles teemas seletatakse vara vea analüüsi Varahalduses.
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
ms.openlocfilehash: 67ccbb742bb4e2283c30b4dec055d137b4a51e40
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216409"
---
# <a name="asset-fault-analysis"></a><span data-ttu-id="0605d-103">Vara vea analüüs</span><span class="sxs-lookup"><span data-stu-id="0605d-103">Asset fault analysis</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0605d-104">Varade Halduses saate analüüsida vara vea registreerimisi, et saada ülevaade kindla perioodi jooksul registreeritud vigade koguarvust.</span><span class="sxs-lookup"><span data-stu-id="0605d-104">In Asset Management, you can analyze asset fault registrations to get an overview of the total number of faults registered during a specific period.</span></span> <span data-ttu-id="0605d-105">Vea registreerimisi saab analüüsida erinevatest vaatenurkadest, näiteks keskendudes varadele, vara tüüpidele, töö asukohtadele, vigade sümptomitele või vigade tüübile.</span><span class="sxs-lookup"><span data-stu-id="0605d-105">Fault registrations can be analyzed from different perspectives, for example with focus on assets, asset types, functional locations, fault symptoms, or fault types.</span></span>

1. <span data-ttu-id="0605d-106">Klõpsake **Varahaldus** > **Päringud** > **Vara viga** > **Vara vea analüüs**.</span><span class="sxs-lookup"><span data-stu-id="0605d-106">Click **Asset management** > **Inquiries** > **Asset fault** > **Asset fault analysis**.</span></span>

2. <span data-ttu-id="0605d-107">Dialoogiaknas **Vara vea analüüsi arvutamine** saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et vara vea read oleksid seotud töö asukohtadega.</span><span class="sxs-lookup"><span data-stu-id="0605d-107">In the **Asset fault analysis calculation** dialog, you can use the **Level** field to indicate how detailed you want the asset fault lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="0605d-108">Näiteks kui sisestate väljale numbri "1" ja teil on mitmetasandiline töö asukoha struktuur, kuvatakse ülemisel tasemel kõik vara vea read töö asukoha kohta ja seetõttu võib rea tunnid kokku liita töö asukohtadest, mis asuvad madalamal tasemel.</span><span class="sxs-lookup"><span data-stu-id="0605d-108">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all asset fault lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
        
    <span data-ttu-id="0605d-109">Kui sisestate numbri "0" väljale **Tase**, näete üksikasjalikku tulemust, kus kuvatakse kõik vara vea read kõigil töö asukoha tasemetel, millega need on seotud.</span><span class="sxs-lookup"><span data-stu-id="0605d-109">If you insert the number "0" in the **Level** field, you will see a detailed result showing all asset fault lines on all the functional location level to which they are related.</span></span>

3. <span data-ttu-id="0605d-110">Kui soovite otsingut piirata, saate valida kindlad varad, vea kuupäevad, vea põhjused ja vea parandusmeetmed **Lisamiskirjed** kiirkaardi valikus.</span><span class="sxs-lookup"><span data-stu-id="0605d-110">If you want to limit the search, you can select specific assets, fault dates, fault causes, and fault remedies on the **Records to include** FastTab.</span></span>

4. <span data-ttu-id="0605d-111">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="0605d-111">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="0605d-112">Klõpsake vahekaardil **Vara vea analüüs** ühte või mitut nuppu **Grupeerimisalus**, et kuvada detailide tase, mida soovite näha.</span><span class="sxs-lookup"><span data-stu-id="0605d-112">On the **Asset fault analysis** tab, click one or more **Group by** buttons to display the detail level you want to see.</span></span> <span data-ttu-id="0605d-113">Aktiveeritud nupud on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="0605d-113">Activated buttons are highlighted.</span></span> <span data-ttu-id="0605d-114">Nuppude aktiveerimiseks või inaktiveerimiseks klõpsake neil.</span><span class="sxs-lookup"><span data-stu-id="0605d-114">Activate or deactivate buttons by clicking on them.</span></span>

6. <span data-ttu-id="0605d-115">Klõpsake **Värskenda arvutusi**, et näidata oma valikuid ekraanil.</span><span class="sxs-lookup"><span data-stu-id="0605d-115">Click **Update calculations** to show your selections on the screen.</span></span> 

>[!NOTE]
><span data-ttu-id="0605d-116">Iga kord, kui aktiveerite või desaktiveerite nupu **Grupeerimisalus**, ärge unustage klõpsata nuppu **Värskenda arvutusi**.</span><span class="sxs-lookup"><span data-stu-id="0605d-116">Every time you activate or deactivate a **Group by** button, remember to click the **Update calculations** button.</span></span> <span data-ttu-id="0605d-117">See on nõutav, kuna suur hulk andmeid töödeldakse, kui arvutate vea tõenäosuse ümber.</span><span class="sxs-lookup"><span data-stu-id="0605d-117">This is required because a large amount of data is processed as you are recalculating fault probability.</span></span>

## <a name="examples"></a><span data-ttu-id="0605d-118">Näited</span><span class="sxs-lookup"><span data-stu-id="0605d-118">Examples</span></span>

<span data-ttu-id="0605d-119">Vigade registreerimiste analüüsimiseks on mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="0605d-119">There are many ways to analyze fault registrations.</span></span> <span data-ttu-id="0605d-120">Selles jaotises kirjeldatakse viit näidet, kuidas erinevad andmevalikud saavad pakkuda rohkem teavet ja üksikasju, analüüsides vara vea registreerimisi.</span><span class="sxs-lookup"><span data-stu-id="0605d-120">This section has five examples of how different data selections can provide more insight and detail when analyzing asset fault registrations.</span></span>

### <a name="group-by-symptoms"></a><span data-ttu-id="0605d-121">Grupeerimine sümptomite alusel</span><span class="sxs-lookup"><span data-stu-id="0605d-121">Group by symptoms</span></span>

<span data-ttu-id="0605d-122">Alltoodud ekraanipildil on valitud ainult **Sümptomi** nupp.</span><span class="sxs-lookup"><span data-stu-id="0605d-122">In the screenshot below, only the **Symptom** button is selected.</span></span>

- <span data-ttu-id="0605d-123">Vea registreerimised on tehtud kolme vea sümptomi korral: "Õhuleke", "Läbipõlenud kaitse" ja "Seade ummistunud".</span><span class="sxs-lookup"><span data-stu-id="0605d-123">Fault registrations have been made on three fault symptoms: "Air leak", "Blown fuse", and "Equipment jammed".</span></span>  
- <span data-ttu-id="0605d-124">Veerus **Tõenäosuse %** on kõik protsendid kokku 100%.</span><span class="sxs-lookup"><span data-stu-id="0605d-124">In the **Probability %** column, all percentages add up to 100%.</span></span> <span data-ttu-id="0605d-125">Tõenäosus põhineb kõigi **Sümptom** valikute registreerimisel selles tõrke analüüsis.</span><span class="sxs-lookup"><span data-stu-id="0605d-125">Probability is based on all **Symptom** registrations in this fault analysis.</span></span>

![Joonis 1](media/06-controlling-and-reporting.png)

### <a name="group-by-symptoms-and-time-period"></a><span data-ttu-id="0605d-127">Grupeerimine sümptomite ja ajaperioodi alusel</span><span class="sxs-lookup"><span data-stu-id="0605d-127">Group by symptoms and time period</span></span>

<span data-ttu-id="0605d-128">Alloleval ekraanipildil lisatakse **Aasta** ja **Kuu**, et näidata, kuidas saate vaadata vigade registreerimisi valitud perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="0605d-128">In the screenshot below, **Year** and **Month** are added to show how you can view fault registrations during a selected period.</span></span>

- <span data-ttu-id="0605d-129">Vea sümptomid on nüüd näidatud registreerimistena aastas/kuus.</span><span class="sxs-lookup"><span data-stu-id="0605d-129">The fault symptoms are now shown as registrations per year/month.</span></span>  
- <span data-ttu-id="0605d-130">Veerus **Tõenäosuse %**, kui lisate kõik protsendid iga kuu kohta, moodustavad nad kokku 100%.</span><span class="sxs-lookup"><span data-stu-id="0605d-130">In the **Probability %** column, if you add all percentages for each month, they add up to 100%.</span></span> <span data-ttu-id="0605d-131">Tõenäosus põhineb **Sümptom** valikute registreerimisel selles vea analüüsis.</span><span class="sxs-lookup"><span data-stu-id="0605d-131">Probability is based on the **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="0605d-132">Kui teil on varal palju ridu, kuid real paistab suur protsent silma, siis on see märk vea sümptomist, mida täpsemalt uurida, et leida moodus, kuidas piirata selle vea sümptomite registreerimiste arvu.</span><span class="sxs-lookup"><span data-stu-id="0605d-132">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Joonis 2](media/07-controlling-and-reporting.png)

### <a name="group-by-multiple-symptoms-and-assets"></a><span data-ttu-id="0605d-134">Grupeerimine mitme sümptomi ja vara alusel</span><span class="sxs-lookup"><span data-stu-id="0605d-134">Group by multiple symptoms and assets</span></span>

<span data-ttu-id="0605d-135">Varade ja varade tüübi kombinatsiooni kasutatakse kolmes allpool olevas ekraanipildis näidatud arvutuste alusena, mis suurenevad detailsuse tasemel.</span><span class="sxs-lookup"><span data-stu-id="0605d-135">The combination of assets and an asset type is used as a basis for the calculations shown in the three screenshots below, which will increase in detail level.</span></span>  

<span data-ttu-id="0605d-136">Üldiselt, nupud **Rühmita kuupäeva järgi**, **Rühmita vara järgi**, **Rühmita töö asukoha järgi** toimingupaanide gruppides, nagu ka **Viga** nupp (Vea ID), sisaldavad perioode või vara suhted.</span><span class="sxs-lookup"><span data-stu-id="0605d-136">Generally, the buttons in the **Group by date**, **Group by asset**, **Group by functional location** action pane groups, as well as the **Fault** button (Fault ID), contain periods or asset relations.</span></span> <span data-ttu-id="0605d-137">Nupud **Sümptom**, **Ala**, **Tüüp**, **Põhjus** ja **Parandusmeede** on veahalduses kasutatavad kategooriad, et analüüsida vara vigade registreerimisi ja probleemseid alasi täpselt ära näidata.</span><span class="sxs-lookup"><span data-stu-id="0605d-137">The **Symptom**, **Area**, **Type**, **Cause**, and **Remedy** buttons are categorizations used in fault management to analyze asset fault registrations and pinpoint problem areas.</span></span>  

<span data-ttu-id="0605d-138">**Grupeerimine sümptomi, vara ja varatüübi alusel**</span><span class="sxs-lookup"><span data-stu-id="0605d-138">**Group by symptom, asset, and asset type**</span></span>

<span data-ttu-id="0605d-139">Alloleval ekraanipildil lisati **Vara** ja **Vara tüüp**, et anda üksikasjalikumat teavet vigade registreerimiste kohta.</span><span class="sxs-lookup"><span data-stu-id="0605d-139">In the screenshot below, **Asset** and **Asset type** were added to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="0605d-140">Vea sümptomid on nüüd jaotatud **Vara** / **Vara tüüp** / **Sümptom** kombinatsioonideks.</span><span class="sxs-lookup"><span data-stu-id="0605d-140">The fault symptoms are now split up in **Asset** / **Asset type** / **Symptom** combinations.</span></span>  
- <span data-ttu-id="0605d-141">Kui lisate kõik protsendid veerus **Tõenäosuse %** vastavalt **Vara** / **Vara tüüp** / **Sümptom** kombinatsioonidele, moodustavad nad kõik kokku 100%.</span><span class="sxs-lookup"><span data-stu-id="0605d-141">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** respectively, they each add up to 100%.</span></span> <span data-ttu-id="0605d-142">Tõenäosus põhineb **Sümptom** registreeringutel selles vea analüüsis.</span><span class="sxs-lookup"><span data-stu-id="0605d-142">Probability is based on **Symptom** registrations in this fault analysis.</span></span> <span data-ttu-id="0605d-143">Kui teil on varal palju ridu, kuid real paistab suur protsent silma, siis on see märk vea sümptomist, mida täpsemalt uurida, et leida moodus, kuidas piirata selle vea sümptomite registreerimiste arvu.</span><span class="sxs-lookup"><span data-stu-id="0605d-143">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault symptom to examine more closely to find a way to limit the number of registrations for that fault symptom.</span></span>

![Joonis 3](media/08-controlling-and-reporting.png)

<span data-ttu-id="0605d-145">**Grupeerimine kahe sümptomi, vara ja varatüübi alusel**</span><span class="sxs-lookup"><span data-stu-id="0605d-145">**Group by two symptoms, asset, and asset type**</span></span>

<span data-ttu-id="0605d-146">Alloleval ekraanipildil lisati **Ala** suvand **Sümptom**, **Vara**, ja **Vara tüüp** suvanditele, et anda üksikasjalikumat teavet vigade registreerimiste kohta.</span><span class="sxs-lookup"><span data-stu-id="0605d-146">In the screenshot below, **Area** was added to **Symptom**, **Asset**, and **Asset type** to provide more detail regarding fault registrations.</span></span>

- <span data-ttu-id="0605d-147">Veerus **Tõenäosuse %**, kui lisate varale kõik kombinatsioonide **Vara** / **Vara tüüp** / **Sümptom** protsendid, moodustavad nad kõik kokku 100%.</span><span class="sxs-lookup"><span data-stu-id="0605d-147">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="0605d-148">Tõenäosus põhineb **Sümptom** ja **Ala** kombinatsioonis siin veaanalüüsis.</span><span class="sxs-lookup"><span data-stu-id="0605d-148">Probability is based on the combination of **Symptom** and **Area** in this fault analysis.</span></span> <span data-ttu-id="0605d-149">Kui teil on varal palju ridu, kuid real paistab suur protsent silma, siis on see märk vea alast, mida täpsemalt uurida, et leida moodus, kuidas piirata selle vea ala registreerimiste arvu.</span><span class="sxs-lookup"><span data-stu-id="0605d-149">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault area to examine more closely to find a way to limit the number of registrations for that fault area.</span></span>  

![Joonis 4](media/09-controlling-and-reporting.png)

<span data-ttu-id="0605d-151">**Grupeerimine kolme sümptomi, vara ja varatüübi alusel**</span><span class="sxs-lookup"><span data-stu-id="0605d-151">**Group by three symptom, asset, and asset type**</span></span>

<span data-ttu-id="0605d-152">Alltoodud ekraanipildil lisati **Tüüp** ja on näidatud kõige üksikasjalikum arvutus selles näites.</span><span class="sxs-lookup"><span data-stu-id="0605d-152">In the screenshot below, **Type** was added, and the most detailed calculation in this example is shown.</span></span>
 
- <span data-ttu-id="0605d-153">Veerus **Tõenäosuse %**, kui lisate varale kõik kombinatsioonide **Vara** / **Vara tüüp** / **Sümptom** protsendid, moodustavad nad kõik kokku 100%.</span><span class="sxs-lookup"><span data-stu-id="0605d-153">In the **Probability %** column, if you add all percentages for the combination of **Asset** / **Asset type** / **Symptom** on an asset, they each add up to 100%.</span></span> <span data-ttu-id="0605d-154">Tõenäosus põhineb **Sümptom**, **Ala** ja **Tüüp** kombinatsioonis siin veaanalüüsis.</span><span class="sxs-lookup"><span data-stu-id="0605d-154">Probability is based on the combination of **Symptom**, **Area**, and **Type** in this fault analysis.</span></span> <span data-ttu-id="0605d-155">Kui teil on varal palju ridu, kuid real paistab suur protsent silma, siis on see märk vea tüübist, mida täpsemalt uurida, et leida moodus, kuidas piirata selle vea tüübi registreerimiste arvu.</span><span class="sxs-lookup"><span data-stu-id="0605d-155">If you have a large number of lines on an asset, but a large percentage stands out on a line, that would be an indication of a fault type to examine more closely to find a way to limit the number of registrations on that fault type.</span></span>

![Joonis 5](media/10-controlling-and-reporting.png)


>[!NOTE]
><span data-ttu-id="0605d-157">Töökäskudele ja hooldusnõuetele loodud kõigi vigade registreerimiste ülevaate jaoks klõpsake **Varahaldus** > **Päringud** > **Vara viga** > **Vara vead**.</span><span class="sxs-lookup"><span data-stu-id="0605d-157">For an overview of all fault registrations created on work orders and maintenance requests, click **Asset management** > **Inquiries** > **Asset fault** > **Asset faults**.</span></span> <span data-ttu-id="0605d-158">Lehel **Vara vead** valige vara vea registreerimine ja laiendage **Seotud teabe** paani, et näha teavet seotud töökäsu või hooldusnõude kohta.</span><span class="sxs-lookup"><span data-stu-id="0605d-158">On the **Asset faults** page, select an asset fault registration and expand the **Related information** pane to see information regarding the related work order or maintenance request.</span></span>

