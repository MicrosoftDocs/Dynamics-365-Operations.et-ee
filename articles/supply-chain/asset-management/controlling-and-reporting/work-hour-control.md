---
title: Töötundide kontroll
description: Selles teemas selgitatakse töötundide kontrolli varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 482bee9dba22763a065c8aca93745f53f06f99be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5253706"
---
# <a name="work-hour-control"></a><span data-ttu-id="08fe6-103">Töötundide kontroll</span><span class="sxs-lookup"><span data-stu-id="08fe6-103">Work hour control</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="08fe6-104">Varahalduses saate arvutada tunde, et saada ülevaade tegelikest tundidest, võrreldes eelarve tundidega varade, funktsionaalsete asukohtade või töötellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="08fe6-104">In Asset Management, you can calculate hours to get an overview of actual hours compared to budget hours on assets, functional locations, or work orders.</span></span> <span data-ttu-id="08fe6-105">Tegelikud tunnid põhinevad sisestatud kannetel.</span><span class="sxs-lookup"><span data-stu-id="08fe6-105">Actual hours are based on posted transactions.</span></span>

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="08fe6-106">Töötunni juhtelement varade, funktsionaalsete asukohtade ja töötellimuste jaoks</span><span class="sxs-lookup"><span data-stu-id="08fe6-106">Work hour control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="08fe6-107">Varade, funktsionaalsete asukohtade ja töökäskude kohta tehtud arvutused on peaaegu samasugused.</span><span class="sxs-lookup"><span data-stu-id="08fe6-107">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="08fe6-108">Ainuke erinevus on, et varade ja funktsionaalsete asukohtade puhul saate arvutusse kaasata ka alavarasid ja alaasukohti.</span><span class="sxs-lookup"><span data-stu-id="08fe6-108">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="08fe6-109">Kuupäev on kande kuupäev, mil registreering salvestati.</span><span class="sxs-lookup"><span data-stu-id="08fe6-109">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="08fe6-110">Klõpsake **Varahaldus** > **Päringud** > **Varad** > **Varatunni kontroll** või **Funktsionaalse asukoha tunnikontroll** või **Varahaldus** > **Päringud** > **Töökäsud** > **Töökäsu tunnikontroll**.</span><span class="sxs-lookup"><span data-stu-id="08fe6-110">Click **Asset management** > **Inquiries** > **Assets** > **Asset hour control** or **Functional location hour control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order hour control**.</span></span>

2. <span data-ttu-id="08fe6-111">**Vara tunnikontroll** dialoogiaknas.</span><span class="sxs-lookup"><span data-stu-id="08fe6-111">In the **Asset hour control** dialog, .</span></span>

3. <span data-ttu-id="08fe6-112">Valige dialoogiaknas **Vara tunnikontroll** / **Funktsionaalse asukoha tunnikontroll** / **Töökäsu tunnikontroll** periood, mis arvutatakse väljadel **Alates** ja **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="08fe6-112">In the **Asset hour control** / **Functional location hour control** / **Work order hour control** dialog, select a period to be calculated in the **From date** and **To date** fields.</span></span>

4. <span data-ttu-id="08fe6-113">Vajadusel kaasake arvutusse **Finantsdimensiooni komplekt**.</span><span class="sxs-lookup"><span data-stu-id="08fe6-113">If required, select a **Financial dimension set** to be included in the calculation.</span></span>

5. <span data-ttu-id="08fe6-114">Kui te ei soovi nulli tunniga tulemusi näidata, valige "Jah" lülitusnupul **Jäta null vahele**.</span><span class="sxs-lookup"><span data-stu-id="08fe6-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results containing zero hours.</span></span>

6. <span data-ttu-id="08fe6-115">Saate kasutada välja **Tase**, et näidata, kui üksikasjalikult soovite, et tunnikontrolli read oleksid seotud töö asukohtadega.</span><span class="sxs-lookup"><span data-stu-id="08fe6-115">You can use the **Level** field to indicate how detailed you want the hour control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="08fe6-116">Näiteks kui sisestate väljale numbri "1" ja teil on mitmetasandiline töö asukoha hierarhia, kuvatakse ülemisel tasemel kõik tunnikontrolli read töö asukoha kohta ja seetõttu võib rea tunnid kokku liita töö asukohtadest, mis asuvad madalamal tasemel.</span><span class="sxs-lookup"><span data-stu-id="08fe6-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all hour control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="08fe6-117">Kui sisestate numbri "0" väljale **Tase**, näete üksikasjalikku tulemust, kus kuvatakse kõik tunnikontrolli read kõigil töö asukoha tasemetel, millega need on seotud.</span><span class="sxs-lookup"><span data-stu-id="08fe6-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all hour control lines on all the functional location levels to which they are related.</span></span>

7. <span data-ttu-id="08fe6-118">Märkige Jah nupul **Kaasa alavarad**, et näidata alavaradega seotud kulusid eraldi ridadena.</span><span class="sxs-lookup"><span data-stu-id="08fe6-118">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="08fe6-119">Kui soovite otsingut piirata, saate valida kindlad varad / funktsionaalsed asukohad / töökäsud **Lisamiskirjed** kiirkaardi valikus.</span><span class="sxs-lookup"><span data-stu-id="08fe6-119">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="08fe6-120">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="08fe6-120">Click **OK** to start the calculation.</span></span>

10. <span data-ttu-id="08fe6-121">Klõpsale lehe **Varatunni kontroll** jaotise **Grupeerimisalus** nuppe, et näidata arvutuse nõutavat üksikasjalikku taset.</span><span class="sxs-lookup"><span data-stu-id="08fe6-121">On the **Asset hour control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="08fe6-122">Valitud nupud **Rühmitusalus** on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="08fe6-122">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="08fe6-123">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="08fe6-123">Click on a button to activate or deactivate it.</span></span>

## <a name="example"></a><span data-ttu-id="08fe6-124">Näide</span><span class="sxs-lookup"><span data-stu-id="08fe6-124">Example</span></span>

<span data-ttu-id="08fe6-125">Alltoodud kuvatõmmisel on näidatud lehe **Varatunni kontroll** näidisarvutus.</span><span class="sxs-lookup"><span data-stu-id="08fe6-125">The screenshot below shows an example of an **Asset hour control** calculation.</span></span>

- <span data-ttu-id="08fe6-126">Väli **Algne eelarve** väli näitab eelarve tunde töökäskude prognoosist.</span><span class="sxs-lookup"><span data-stu-id="08fe6-126">The **Original budget** field shows budget hours from the work order forecast.</span></span> 
- <span data-ttu-id="08fe6-127">Väljal **Tegelikud tunnid** kuvatakse töökäskudesse sisestatud tunnid.</span><span class="sxs-lookup"><span data-stu-id="08fe6-127">The **Actual hours** field shows posted hours on work orders.</span></span> 
- <span data-ttu-id="08fe6-128">Väli **Kooskõlastatud tunnid** näitab kogutunde, millele teie ettevõte on pühendunud seoses töökäskudega.</span><span class="sxs-lookup"><span data-stu-id="08fe6-128">The **Committed hours** field shows total amount of hours that your company is committed to in relation to work orders.</span></span>

![Varatunni kontrolli näidisarvutus](media/04-controlling-and-reporting.png)

<span data-ttu-id="08fe6-130">Teine moodus tundide arvutamiseks on valida kas **Kõik varad** või **Aktiivsed varad**.</span><span class="sxs-lookup"><span data-stu-id="08fe6-130">Another way of making an hour calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="08fe6-131">Seejärel klõpsake nuppu **Tunnikontroll** kiirkaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="08fe6-131">Then you click the **Hour control** button on the **General** FastTab.</span></span> <span data-ttu-id="08fe6-132">Valitud varad sisestatakse automaatselt välja **Varad** kiirkaardil **Kaasatavad kirjed**.</span><span class="sxs-lookup"><span data-stu-id="08fe6-132">The selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="08fe6-133">Klõpsake **OK** dialoogiaknas **Varatunni kontroll** ja valitud varade arvutus kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="08fe6-133">Click **OK** in the **Asset hour control** dialog, and the calculation for the selected assets is shown.</span></span> <span data-ttu-id="08fe6-134">Sama protseduuri saab teha funktsionaalsete asukohtade puhul väljades **Kõik funktsionaalsed asukohad** või **Aktiivsed funktsionaalsed asukohad** ja ktöökäskude puhul väljades **Kõik töökäsud** või **Aktiivsed töökäsud**.</span><span class="sxs-lookup"><span data-stu-id="08fe6-134">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]