---
title: Ostukulutuste analüüsi Power BI sisu
description: See teema kirjeldab, mida hõlmab ostukulutuste analüüsi Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutatakse.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "313838"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Ostukulutuste analüüsi Power BI sisu

[!include [banner](../includes/banner.md)]

See teema kirjeldab, mida hõlmab **ostukulutuste analüüsi** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Ostukulutuste analüüsi** Power BI sisu on mõeldud eelarvete eest vastutavate ostujuhtide ja juhtide abistamiseks ostukulutuste jälgimisel. Juhid saavad analüüsida ostukulutusi järgmiselt.

- Aasta seniste ostude summa (hankijarühmade ja eraldi hankijate, tootekategooriate ja eraldi toodete ning hankija asukoha järgi)
- Ostmise muutumine aastate lõikes (hankijarühmade ja hankekategooriate järgi)

Sisu kasutab ostukannete andmeid ning annab koondvaate kogu ettevõtte ostunumbritest ja ostukulude jaotuse hankijate ja toodete kaupa. Aruanded tõstavad esile ostukulude muutusi aja jooksul. Seega saab neid aruandeid kasutada juhtide teavitamiseks eraldi hankijate ja toodete positiivsetest ning negatiivsetest kulutamistrendidest. Lisaks näitavad diagrammid erinevate hankekategooriate ja hankijagruppide kulusid. Seega saavad kategooria- ja piirkonnajuhid kasutada neid diagramme muutuste tuvastamiseks kulutamiskäitumises.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Ostukulutuste analüüsi** Power BI sisu kuvatakse lehel **Ostu- ja kulutusanalüüs** (**Hanked** \> **Päringud ja aruanded** \> **Ostujõudluse analüüs** \> **Ostu- ja kulutusanalüüs**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad mõõdikud
**Ostukulutuste analüüsi** Power BI sisu sisaldab mõõdikute kogumist koosnevat aruannet. Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena. Järgmises tabelis antakse ülevaade visualiseeringutest.

<table>
<thead>
<tr>
<th>Aruandeleht</th>
<th>Diagrammid</th>
<th>Paanid</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ostud hankija alusel</td>
<td><ul>
<li>10 tipphankijat ostu alusel (virntulpdiagramm)</li>
<li>Ostud kokku hankijagrupi/riigi/nime alusel (sektordiagramm)</li>
<li>Ostud hankijagrupi/riigi/nime alusel (tulpdiagramm)</li>
<li>Keskmine ost hankijagrupi/riigi/nime alusel (tulpdiagramm)</li>
</ul></td>
<td><ul>
<li>Koguost</li>
<li>YOY ostude kasv</li>
<li>Hankijate arv kokku</li>
<li>Aktiivsete hankijate arv kokku</li>
</ul></td>
</tr>
<tr>
<td>Ostud toodete alusel</td>
<td><ul>
<li>Ostud hankekategooria / toote nime alusel (tulpdiagramm)</li>
<li>Ostud hankekategooria / toote nime alusel kokku (sektordiagramm)</li>
<li>10 tipptoodet ostu alusel (virntulpdiagramm)</li>
</ul></td>
<td><ul>
<li>Toodete arv kokku</li>
<li>Aktiivsete toodete osakaal toodete arvust kokku</li>
<li>Toodete arv, mis annavad 80% ostudest</li>
</ul></td>
</tr>
<tr>
<td>Ostud perioodi alusel*</td>
<td><ul>
<li>Ostud kuu/päeva alusel (tulpdiagramm)</li>
<li>Kumulatiivsete ostude YOY hälve (kaskaaddiagramm)</li>
<li>Ostude YOY kasv kokku (tulpdiagramm)</li>
<li>Hankeväljavõte (maatriks)</li>
</ul></td>
<td><ul>
<li>YOY ostude kasv</li>
<li>YOY ostude kasvu %</li>
</ul></td>
</tr>
<tr>
<td>Ostud hankija asukoha alusel</td>
<td><ul>
<li>Ostud linna alusel</li>
<li>Ostude YOY kasvu %</li>
<li>Ostud riikide järgi</li>
</ul></td>
<td></td>
</tr>
<tr>
<td>Ostukulutuste analüüs aja alusel</td>
<td><ul>
<li>Jooksva aasta ostud kuu/päeva alusel (joondiagramm)</li>
<li>Jooksva ja eelmise aasta ostud (joon- ja tulpdiagramm)</li>
</ul></td>
<td></td>
</tr>
<tr>
<td>Ostukulutuste analüüs hankija alusel</td>
<td><ul>
<li>10 juhtiva hankija ostude % ostudest (lehter)</li>
<li>10 parimat hankijat suurema kulutuste YOY-ga</li>
<li>10 parimat hankijat väiksema kulutuste YOY-ga</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\* Selle ja eelmise aasta ostud ja kasv hankekategooriate alusel

## <a name="data-model-and-entities"></a>Andmemudel ja üksused
Aruandelehtede täitmiseks **ostukulutuste analüüsi** Power BI sisus kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md).

Selle sisu koondmõõtmised on rakenduste Microsoft Dynamics AX 2012 ja Microsoft Dynamics AX 2012 R3 ostukuubis saadaval olnud koondmõõtmiste alamkogum. Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks. Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebipostituses [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md). Järgmised peamised koondmõõtmised on saadaval otse arve ridade üksusest ja neid kasutatakse sisu alusena.

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
