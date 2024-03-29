---
title: Ostukulutuste analüüsi Power BI sisu
description: See artikkel kirjeldab, mis sisaldub ostu kulu kulutamise analüüsi sisus Power BI.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.form: PurchaseSpendAnalysisPowerBI
ms.openlocfilehash: 757b782131617104422e15f3ceec747b92d96666
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276656"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Ostukulutuste analüüsi Power BI sisu

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, mis sisaldub ostu **kulu kulutamise analüüsi sisus** Microsoft Power BI. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Ostukulutuste analüüsi** Power BI sisu on mõeldud eelarvete eest vastutavate ostujuhtide ja juhtide abistamiseks ostukulutuste jälgimisel. Juhid saavad analüüsida ostukulutusi järgmiselt.

- Aasta seniste ostude summa (hankijarühmade ja eraldi hankijate, tootekategooriate ja eraldi toodete ning hankija asukoha järgi)
- Ostmise muutumine aastate lõikes (hankijarühmade ja hankekategooriate järgi)

Sisu kasutab ostukannete andmeid ning annab koondvaate kogu ettevõtte ostunumbritest ja ostukulude jaotuse hankijate ja toodete kaupa. Aruanded tõstavad esile ostukulude muutusi aja jooksul. Seega saab neid aruandeid kasutada juhtide teavitamiseks eraldi hankijate ja toodete positiivsetest ning negatiivsetest kulutamistrendidest. Lisaks näitavad diagrammid erinevate hankekategooriate ja hankijagruppide kulusid. Seega saavad kategooria- ja piirkonnajuhid kasutada neid diagramme muutuste tuvastamiseks kulutamiskäitumises.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Ostukulutuste analüüsi** Power BI sisu kuvatakse lehel **Ostu- ja kulutusanalüüs** (**Hanked** \> **Päringud ja aruanded** \> **Ostujõudluse analüüs** \> **Ostu- ja kulutusanalüüs**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad mõõdikud
**Ostukulutuste analüüsi** Power BI sisu sisaldab mõõdikute kogumist koosnevat aruannet. Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena. 

Järgmistes jaotistes antakse ülevaade visualiseeringutest.

### <a name="purchase-by-vendor-report-page"></a>Ostmine hankija aruandelehe alusel
**Diagrammid**
- 10 tipphankijat ostu alusel (virntulpdiagramm)
- Ostud kokku hankijagrupi/riigi/nime alusel (sektordiagramm)
- Ostud hankijagrupi/riigi/nime alusel (tulpdiagramm)
- Keskmine ost hankijagrupi/riigi/nime alusel (tulpdiagramm)

**Paanid**
- Koguost
- YOY ostude kasv
- Hankijate arv kokku
- Aktiivsete hankijate arv kokku

**Näide**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Ostmine toote aruandelehe alusel

**Diagrammid**
- Ostud hankekategooria / toote nime alusel (tulpdiagramm)
- Ostud hankekategooria / toote nime alusel kokku (sektordiagramm)
- 10 tipptoodet ostu alusel (virntulpdiagramm)

**Paanid**
- Toodete arv kokku</li>
- Aktiivsete toodete osakaal toodete arvust kokku
- Toodete arv, mis annavad 80% ostudest

**Näide**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Ostmine ajaperioodi aruandelehe alusel
See leht näitab selle ja eelmise aasta oste ja kasvu hankekategooriate alusel.

**Diagrammid** 
- Ostud kuu/päeva alusel (tulpdiagramm)
- Kumulatiivsete ostude YOY hälve (kaskaaddiagramm)
- Ostude YOY kasv kokku (tulpdiagramm)
- Hankeväljavõte (maatriks)

**Paanid**
- YOY ostude kasv
- YOY ostude kasvu %

**Näide**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Ostmine hankija asukoha aruandelehe alusel

**Diagrammid**
- Ostud linna alusel
- Ostude YOY kasvu %
- Ostud riikide järgi

**Näide**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Ostukulutuste analüüs aja aruandelehe alusel

**Diagrammid** 
- Jooksva aasta ostud kuu/päeva alusel (joondiagramm)
- Jooksva ja eelmise aasta ostud (joon- ja tulpdiagramm)

**Näide**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Ostukulutuste analüüs hankija aruandelehe alusel

**Diagrammid** 
- 10 juhtiva hankija ostude % ostudest (lehter)
- 10 parimat hankijat suurema kulutuste YOY-ga
- 10 parimat hankijat väiksema kulutuste YOY-ga

**Näide** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Andmemudel ja üksused
Aruandelehtede täitmiseks **ostukulutuste analüüsi** Power BI sisus kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet vt teemast [Power BI integratsioon üksuse kauplusega](power-bi-integration-entity-store.md).

Selle sisu koondmõõtmised on rakenduste Microsoft Dynamics AX 2012 ja Microsoft Dynamics AX 2012 R3 ostukuubis saadaval olnud koondmõõtmiste alamkogum. Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks. Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebipostituses [Power BI integreerimine üksuse kauplusega](power-bi-integration-entity-store.md). Järgmised peamised koondmõõtmised on saadaval otse arve ridade üksusest ja neid kasutatakse sisu alusena.

| Üksus        | Peamised koondmõõtmised | Andmeallikas                                 | Väli              | Kirjeldus                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Arve read | Ost                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa arvestusvaluutas. |

Järgmises tabelis on antud peamised mõõtmised, mis arvutatakse sisupaketis arve ridade üksusest.

| Mõõt               | Kalkulatsioon                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Jooksva aasta ostud | Jooksva aasta ostud = SUM('Arve read'\[Ost\])                                            |
| Eelmise aasta ostud    | Eelmise aasta ostud = CALCULATE(SUM('Arve read'\[Ost\]), SAMEPERIODLASTYEAR(Kuupäevad\[Kuupäev\])) |
| YOY ostude kasv   | YOY ostude kasv = \[Jooksva aasta ostud\] – \[Eelmise aasta ostud\]                            |

Järgmisi sisu põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate saamiseks.

| Üksus                 | Atribuutide näited                                |
|------------------------|-------------------------------------------------------|
| Hankijad                | Hankijagrupid, Hankija riik või regioonid, Hankija nimi |
| Tooted               | Tootenumber, Toote nimi, Kaubagruppide nimi        |
| Hankekategooriad | Hankekategooria, Hankekategooria nimed      |
| Juriidilised isikud         | Juriidilise isiku nimi                                     |
| Kuupäevad                  | Kuupäevad, Aasta vastaskonto                                    |

Vaikimisi näitab sisu jooksva kalendriaasta andmeid. Kuid kuupäevafiltrit saab muuta aruande filtrite jaotises. Saate muuta ka ettevõtte filtrit.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
