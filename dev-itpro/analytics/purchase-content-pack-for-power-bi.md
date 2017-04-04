---
title: "Ostu veeta Power BI sisu analüüs"
description: "Teema käsitleb koostist kulutada ostu analüüsi sisu pack Microsoft Power BI. Ta selgitab, kuidas on võimalik saada aruandeid, mis on kaasatud sisu pack ja andmemudel ja üksusi, mida kasutatakse ehitada sisu pakendi teave."
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

# <a name="purchase-spend-analysis-power-bi-content"></a>Ostu veeta Power BI sisu analüüs

Teema käsitleb koostist kulutada ostu analüüsi sisu pack Microsoft Power BI. Ta selgitab, kuidas on võimalik saada aruandeid, mis on kaasatud sisu pack ja andmemudel ja üksusi, mida kasutatakse ehitada sisu pakendi teave.

<a name="overview"></a>Ülevaade
--------

Ostu veeta sisu pack Microsoft Power BI loodi juhtide ja juhid, kes vastutavad eelarve analüüs. See on loodud, et aidata neil hoida silma peal ostu kulutusi. Ta kasutab ostu kandeandmete Microsoft Dynamics 365 operatsioonide ja nii kokku ülevaate kogu ettevõtte ostu arve ja ostutellimuse hankija ja toote kulutuste jaotus. Raportite ostu kulutusi aja jooksul muutustest. Seetõttu nad sobib alert juhid positiivsete ja negatiivsete kulutuste suundumustest erinevate hankijate ja tooted. Diagrammid näitavad erinevate hangete kategooriad ja hankijagruppide ostu. Kategooria ja regiooni osutuda vajalikuks selliste diagrammide abil saate tuvastada muutusi kulutuste käitumine. Sisu pack let's ostu juhtide ja juhid, kes vastutavad eelarve analüüsida ostu kulutusi järgmiselt:

-   Aasta kuupäevani ostu (hankijagrupi ja erinevate hankijate, hanke liigi ja üksikute toodete ja hankija asukoha) järgi
-   Aastane ostu muutus (hankija nimel ja hangete kategooriate kaupa)

## <a name="accessing-the-content-pack"></a>Juurdepääsu sisu pakendi
Ostu veeta analüüsi sisu rakendamise varana on Microsoft Dynamics elutsükli teenused (LCS) avaldatakse ja pääseb juurde Microsoft Dynamics 365 toiminguteks. Juurdepääsu ja avatud Power BI aruanded kohta lisateabe saamiseks vt [Power BI sisu LCS Microsofti ja oma partnerite](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Mõõdikud, mis on kaasatud sisu pack
Ostu veeta analüüsi sisu pack sisaldab aruande, milles on kirjeldatud parameetrid. Need mõõdikud on näitlikustada diagrammid, plaadid ja tabelid. Järgmises tabelis antakse ülevaade sisu Pack visualiseeringuid.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Aruanne lehekülg</th>
<th>Diagrammid</th>
<th>Plaadid</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Hankija osta</td>
<td><ul>
<li>Top 10 hankijate ostuga (virnlintdiagrammis)</li>
<li>Kokku osta hankija rühm / riik / nimi (sektordiagramm)</li>
<li>Ostutellimuse hankija rühm / riik / nimi (tulpdiagramm)</li>
<li>Ostutellimuse hankija Keskmine rühm / riik / nimi (tulpdiagramm)</li>
</ul></td>
<td><ul>
<li>Koguost</li>
<li>Jäädes ostu</li>
<li>Kokku # müüjad</li>
<li>Aktiivne müüjad kokku #</li>
</ul></td>
</tr>
<tr class="even">
<td>Osta toode</td>
<td><ul>
<li>Ostu hanke kategooria / toote nimetus (tulpdiagramm)</li>
<li>Kokku ostu hanke kategooria / toote nimetus (sektordiagramm)</li>
<li>Top 10 tooted ostuga (virnlintdiagrammis)</li>
</ul></td>
<td><ul>
<li>Tooteid kokku #</li>
<li>Kokku # toodete osakaal kokku aktiivsed tooted</li>
<li>Arvu tooteid, mis moodustavad 80% ostmiseks</li>
</ul></td>
</tr>
<tr class="odd">
<td>Osta perioodil *</td>
<td><ul>
<li>Osta kuu / päev (tulpdiagramm)</li>
<li>Kumulatiivne ostu aastaga erinevus (juga diagramm)</li>
<li>Ostu jäädes (tulpdiagramm)</li>
<li>Riigihanke aruanne (matrix)</li>
</ul></td>
<td><ul>
<li>Jäädes ostu</li>
<li>Aastaga ostu kasv %</li>
</ul></td>
</tr>
<tr class="even">
<td>Osta hankija asukoha järgi</td>
<td><ul>
<li>Osta linna</li>
<li>Ostu Kvartaalne kasv %</li>
<li>Osta riigi poolt</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Ostu veeta aega analüüs</td>
<td><ul>
<li>Ostu jooksva aasta kuu / päev (joondiagrammi)</li>
<li>Praeguse ja eelmise aasta (rea- ja diagramm)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Ostu veeta analüüsi hankija</td>
<td><ul>
<li>Top 10 Müük ost % ostu (lehter)</li>
<li>Top 10 hankijad, kelle suurenenud kulutuste kasv</li>
<li>Top 10 hankijad, kelle vähenenud kulutuste kasv</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Ostu sel aastal ja eelmisel aastal ja kasvu hanke kategooriate kaupa

## <a name="data-model-and-entities"></a>Andmemudel ja üksuste
Dynamics 365 toimingute andmeid kasutatakse aruande ostmiseks kulutada analüüsi sisu pakendi. Need andmed esitatakse arvuna kokku mõõtmised, mis on lavastatud olem poest, mis on Microsoft SQL andmebaasi, mis on optimeeritud analytics. Üksuse poe kohta lisateabe saamiseks vaadake selle [Power BI Integratsioon üksus poe Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogi postitus. Kogu selle sisu Pack on kokku mõõtmised, mis on saadaval Microsoft Dynamics AX 2012 ja Microsoft Dynamics 365 toimingute 2012 R3 ostu Cube osa. Lavale kuubi kokku mõõtmise üksus poes, tegema positsioonidele. Lisateabe saamiseks vt kord lavastus kogu mõõtmise üksus poe ning [Power BI Integratsioon üksus poe Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blogi postitus. Järgmisi peamisi kokku mõõtmisi käest otse arve read olemi ja sisu pakendi alusena kasutatakse.

| Üksus        | Võtme kõigi mõõtmiste | Dynamics 365 operatsioonide jaoks | Väli              | Kirjeldus                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Arve read | Ost                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Summa arvestusvaluutas |

Järgmine tabel näitab peamised mõõtmised, mis arvutatakse sisu pakendi üksusest arve read.

| Mõõt               | Kalkulatsioon                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Ostu jooksva aasta | Ostu aasta = SUM (ridade arveldamiseks\[ostmine\])                                            |
| Osta eelmisel aastal    | Ostu eelmisel aastal = Arvuta (summa (ridade arveldamiseks\[ostmine\]), SAMEPERIODLASTYEAR (kuupäevad\[alates\])) |
| Jäädes ostu   | Aastaga osta kasvu = \[osta jooksva aasta\] – \[osta eelmisel aastal\]                            |

Järgmisi peamisi näitajaid, mille sisu pakendi kasutatakse filtrite viil kokku mõõtmised, et sa oleksid granulaarsus üha sügavama analüüsi pilgu.

| Üksus                 | Näited atribuutidest                                |
|------------------------|-------------------------------------------------------|
| Hankijad                | Hankijagruppe, hankija riigi või piirkondade, hankija nimi |
| Tooted               | Toote number, toote nimi, rühma nimi        |
| Hankekategooriad | Hanke kategooria, hangete kategooria nimed      |
| Juriidilised isikud         | Juriidilise isiku nimi                                     |
| Kuupäevad                  | Kuupäevad, aasta nihe                                    |

Vaikimisi kuvatakse sisu pakendi andmed kalendriaasta. Siiski saate muuta jaotises aruande filtrid Kuupäevafilter. Saate muuta ettevõtte filter.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)



