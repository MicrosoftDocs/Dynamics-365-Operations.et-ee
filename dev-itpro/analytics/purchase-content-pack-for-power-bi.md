---
title: "Ostukulutuste analüüsi Power BI sisu"
description: "See teema kirjeldab, mida hõlmab Microsoft Power BI ostukulutuste analüüsi sisupakett. See selgitab juurdepääsu sisupaketis sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisupaketi loomiseks kasutatakse."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Ostukulutuste analüüsi Power BI sisu

See teema kirjeldab, mida hõlmab Microsoft Power BI ostukulutuste analüüsi sisupakett. See selgitab juurdepääsu sisupaketis sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisupaketi loomiseks kasutatakse.

<a name="overview"></a>Ülevaade
--------

Microsoft Power BI ostukulutuste analüüsi sisupakett loodi ostujuhtide ja eelarvete eest vastutavate juhtide jaoks. Selle eesmärk on aidata neil ostukulutustel silma peal hoida. See kasutab Microsoft Dynamics 365 for Operationsi ostukannete andmeid ning annab koondvaate kogu ettevõtte ostunumbritest ja ostukulude jaotuse hankijate ja toodete kaupa. Aruanded tõstavad esile ostukulude muutusi aja jooksul. Seega saab neid kasutada juhtide teavitamiseks eraldi hankijate ja toodete positiivsetest ning negatiivsetest kulutamistrendidest. Diagrammid näitavad erinevate hankekategooriate ja hankijagruppide kulusid. Kategooria- ja piirkonnajuhtidel võib olla neist diagrammidest abi, et tuvastada muutusi kulutamiskäitumises. Sisupakett võimaldab ostujuhtidel ja eelarvete eest vastutavatel juhtidel analüüsida ostukulutusi järgmiselt.

-   Aasta seniste ostude summa (hankijarühmade ja eraldi hankijate, tootekategooriate ja eraldi toodete ning hankija asukoha järgi)
-   Ostmise muutumine aastate lõikes (hankijarühmade ja hankekategooriate järgi)

## <a name="accessing-the-content-pack"></a>Juurdepääs sisupaketile
Ostukulutuste analüüsi sisupakett on avaldatud juurutusvahendina teenuses Microsoft Dynamics Lifecycle Services (LCS) ja sellele pääseb juurde rakendusest Microsoft Dynamics 365 for Operations. Lisateavet Power BI aruannete juurde pääsemise ja nende avamise kohta vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad mõõdikud
Ostukulutuste analüüsi sisupakett sisaldab mõõdikute kogumist koosnevat aruannet. Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena. Järgmine tabel annab ülevaate sisupaketi visualiseerimistest.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Aruandeleht</th>
<th>Diagrammid</th>
<th>Paanid</th>
</tr>
</thead>
<tbody>
<tr class="odd">
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
<tr class="even">
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
<tr class="odd">
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
<tr class="even">
<td>Ostud hankija asukoha alusel</td>
<td><ul>
<li>Ostud linna alusel</li>
<li>Ostude YOY kasvu %</li>
<li>Ostud riikide järgi</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Ostukulutuste analüüs aja alusel</td>
<td><ul>
<li>Jooksva aasta ostud kuu/päeva alusel (joondiagramm)</li>
<li>Jooksva ja eelmise aasta ostud (joon- ja tulpdiagramm)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
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
Ostukulutuste analüüsi sisupaketis kasutatakse aruande jaoks Dynamics 365 for Operationsi andmeid. Need andmed esitatakse koondmõõtmistena, mis on koondatud üksuse kauplusse, mis on analüüsimiseks optimeeritud Microsoft SQL-i andmebaas. Lisateavet üksuse kaupluse kohta leiate ajaveebipostitusest [Power BI integratsioon üksuse kauplusega Dynamicsis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Selle sisupaketi koondmõõtmised on rakenduste Microsoft Dynamics AX 2012 ja Microsoft Dynamics 365 for Operations 2012 R3 ostukuubis olnud koondmõõtmiste alamkogum. Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks. Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebipostituses [Power BI integratsioon üksuse kauplusega Dynamicsis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Järgmised peamised koondmõõtmised on saadaval otse arve ridade üksusest ja neid kasutatakse sisupaketi alusena.

| Üksus        | Peamised koondmõõtmised | Dynamics 365 for Operationsi andmeallikas | Väli              | Kirjeldus                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Arve read | Ost                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa arvestusvaluutas |

Järgmises tabelis on antud peamised mõõtmised, mis arvutatakse sisupaketis arve ridade üksusest.

| Mõõt               | Kalkulatsioon                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Jooksva aasta ostud | Jooksva aasta ostud = SUM('Arve read'\[Ost\])                                            |
| Eelmise aasta ostud    | Eelmise aasta ostud = CALCULATE(SUM('Arve read'\[Ost\]), SAMEPERIODLASTYEAR(Kuupäevad\[Kuupäev\])) |
| YOY ostude kasv   | YOY ostude kasv = \[Jooksva aasta ostud\] – \[Eelmise aasta ostud\]                            |

Järgmisi sisupaketi põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate andmiseks.

| Üksus                 | Atribuutide näited                                |
|------------------------|-------------------------------------------------------|
| Hankijad                | Hankijagrupid, Hankija riik või regioonid, Hankija nimi |
| Tooted               | Tootenumber, Toote nimi, Kaubagruppide nimi        |
| Hankekategooriad | Hankekategooria, Hankekategooria nimed      |
| Juriidilised isikud         | Juriidilise isiku nimi                                     |
| Kuupäevad                  | Kuupäevad, Aasta vastaskonto                                    |

Vaikimisi näitab sisupakett jooksva kalendriaasta andmeid. Kuid kuupäevafiltrit saab muuta aruande filtrite jaotises. Saate muuta ka ettevõtte filtrit.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)



