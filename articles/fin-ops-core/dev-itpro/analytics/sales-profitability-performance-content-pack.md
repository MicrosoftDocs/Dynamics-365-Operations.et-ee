---
title: Müügi ja tulususe jõudluse Power BI sisu
description: See teema kirjeldab, mida hõlmab müügi ja tulususe jõudluse Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SalesProfitabilityPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 490a4f6d1bd9f3bdb0af09bd4e6f7f8fb2c92a1b
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984270"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>Müügi ja tulususe jõudluse Power BI sisu

[!include [banner](../includes/banner.md)]

See teema kirjeldab, mida hõlmab **müügi ja tulususe jõudluse** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="overview"></a>Ülevaade

**Müügi ja tulususe jõudluse** Power BI sisu loodi selleks, et müügijuhid saaksid jälgida peamisi müügimõõdikuid: tulu, brutokasumit ja kasumimarginaale. Selles kasutatakse müügikannete andmeid ning antakse koondvaade kogu ettevõtte müüginumbritest ja müügitulemuste jaotusest klientide ning toodete kohta.

Aruanded toovad esile tulu muutused ja kasumi kasvu aja jooksul. Seega saab neid aruandeid kasutada juhtide teavitamiseks eraldi klientide ja toodete positiivsetest ning negatiivsetest trendidest. Lisaks võrreldakse diagrammidel erinevate tootekategooriate tulu ja kasumlikkust ning kliendigruppe omavahel. Tänu sellele saavad kategooria- ja piirkonnajuhid tuvastada mahajääjaid ja liidreid. Lõpuks loob põhjalik aruanne graafiku eraldi kliendi tulu ja kasumimarginaali võrdlusega. Seega on kliendihalduritel andmetepõhine alus, mille abil oma müügi- ja turundustegevusi iga kliendi profiiliga kohandada.

**Müügi ja tulususe tulemuste sisu** võimaldab müügijuhtidel analüüsida müügitulemusi järgmisel viisil.

- Aasta senine tulu (kliendigruppide ja eraldi klientide, müügikategooriate ja eraldi toodete ning geograafiliste asukohtade järgi)
- Tulu muutus aastate lõikes (kliendipiirkondade ja müügikategooriate alusel)

Kasumlikkuse analüüsimiseks on järgmised võimalused.

- Brutokasum ja kasumimarginaal (kliendigruppide ja toote müügikategooriate alusel)
- Brutokasumi muutus aastate lõikes
- Kliendi kasumlikkus (tulu järgi võrreldes kogutuluga)

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Müügi ja tulususe jõudluse** Power BI sisu kuvatakse lehel **Müügi ja tulususe jõudlus** (**Müük ja turundus** \> **Päringud ja aruanded** \> **Müügijõudluse analüüs** \> **Müügi ja tulususe jõudlus**).

## <a name="metricsthat-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad mõõdikud
**Müügi ja tulususe jõudluse** Power BI sisu sisaldab mõõdikute kogumist koosnevat aruannet. Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena. Järgmine tabel annab ülevaate sisu visualiseerimistest.

| Aruandeleht            | Diagrammid                                     | Paanid                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Tulu kliendi alusel    | 10 parimat klienti tulu alusel                | Kogutulem                                           |
|                        | Kogutulu kliendigrupi alusel            | YOY tulu kasv                                      |
|                        | Keskmine kliendi tulu kliendigrupi alusel | Kogutulu                                            |
|                        | Tulu ja brutokasum kliendigrupi alusel   |                                                         |
| Tulu toote alusel     | Tulu ja brutokasum müügikategooria alusel   | Toodete \# kokku                                    |
|                        | 10 parimat toodet tulu alusel                 | Aktiivsete toodete arv ja osakaal koguarvust |
|                        | Kogutulu müügikategooria alusel            | Toodete arv, mis annavad 80% tulust           |
| Tulu perioodi alusel\*    | Tulu kuu alusel                           | YOY tulu kasv                                      |
|                        | Varasema tulu hälve, YOY             | YOY tulu kasvu %                                    |
|                        | Müügihälve kokku kliendipiirkonna alusel    |                                                         |
| Tulu asukoha järgi    | Müügitulu linna alusel                      |                                                         |
|                        | YOY tulu kasvu %                       |                                                         |
|                        | Müügitulu piirkonna alusel                    |                                                         |
| Kliendi kasumlikkus | Kogutulu võrreldes kliendipõhise tuluga   | Brutokasum, kogutulu, YOY tulu kasv          |
| Tulususe analüüs | Tulu ja kogutulu kuu alusel          |                                                         |
|                        | 15 parimat klienti kogutulu alusel           |                                                         |
|                        | Kogutulu kuu alusel, YOY                 |                                                         |

\* Selle ja eelmise aasta tulu ja kasv müügikategooriate alusel.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Aruandelehtede täitmiseks **müügi ja tulususe jõudluse** Power BI sisus kasutatakse järgmisi andmeid. Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised. Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet vt teemast [Power BI integratsioon üksuse kauplusega](power-bi-integration-entity-store.md).

Selle sisu koondmõõtmised on rakenduste Microsoft Dynamics AX 2012 ja Microsoft Dynamics AX 2012 R3 müügikuubis saadaval olnud koondmõõtmiste alamkogum. Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks. Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebipostituses [Power BI integratsioon üksuse kauplusega Dynamicsis](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/).

Järgmisi arve ridade üksuse peamisi koondmõõtmisi kasutatakse sisu alusena.

| Üksus        | Peamised koondmõõtmised                   | Dynamics 365 andmeallikas | Väli                                        | Kirjeldus                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| Arve read | Tulu                                      | CustInvoiceTrans             | SUM(LineAmountMST)                           | Summa arvestusvaluutas.            |
|               | Müüdud kaupade omahind                           | InventTrans                  | SUM(CostAmountPosted + CostAmountAdjustment) | Kulusumma ja korrigeerimine    |
|               | Komisjoni rea summa – arvestusvaluuta | CustInvoiceTrans             | SUM(CommissAmountMST)                        | Komisjonitasu summa arvestusvaluutas. |

Järgmine tabel näitab arve ridade üksuse peamisi koondmõõtmisi, mida kasutatakse mitme arvutatud meetme loomiseks sisu andmekogumis.

| Mõõt           | Kalkulatsioon                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Kogukasum      | SUM(Tulu – COGS – Komisjon – Käibemaks (sisaldub kliendiarve rea summas))          |
| Kogutulu      | SUM(Kogutulu / (Tulu – Käibemaks (sisaldub kliendiarve rea summas)))             |
| Eelmise aasta tulu | Eelmise aasta tulu = CALCULATE(SUM('Arve read'\[Tulu\]), SAMEPERIODLASTYEAR(Kuupäevad\[Kuupäev\])) |

Järgmises müügikuubis olevaid põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate andmiseks.

| Üksus           | Atribuutide näited                               |
|------------------|------------------------------------------------------|
| Kliendid        | Kliendigrupid, Kliendipiirkonnad, Aadress, Valdkond |
| Tooted         | Tootenumber, Toote nimi, Kaubagruppide nimi       |
| Müügikategooriad | Müügi kategooria nimed                                 |
| Juriidilised isikud   | Juriidilise isiku nimed                                   |
| Kuupäevad            | Kuupäevad                                                |

Vaikimisi näitab sisu jooksva kalendriaasta andmeid. Kuid kuupäevafiltrit saab muuta aruande filtrite jaotises. Saate muuta ka ettevõtte filtrit.
