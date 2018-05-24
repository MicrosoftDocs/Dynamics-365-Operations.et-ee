---
title: Kuluhalduse Power BI sisu
description: "See teema kirjeldab, mida hõlmab kuluhalduse Power BI sisu."
author: YuyuScheller
manager: AnnBe
ms.date: 03/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 88bbc54721f5da94dd811ef155e8d3bcf8c2b53c
ms.openlocfilehash: b06abae184d07cd3b914caf74bdb16a7803919af
ms.contentlocale: et-ee
ms.lasthandoff: 05/09/2018

---

# <a name="cost-management-power-bi-content"></a>Kuluhalduse Power BI sisu

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

**Kuluhalduse** Microsoft Power BI sisu on mõeldud laoraamatupidajatele või organisatsioonis varude eest vastutavatele või varude olekust või lõpetamata toodangust (WIP) huvitatud üksikisikutele või neile, kes vastutavad või on huvitatud standardkulu erinevuste analüüsimisest.

> [!Note]
> Selles teemas kirjeldatud **Kuluhalduse** Power BI sisu kehtib rakenduse Dynamics 365 for Finance and Operations 8.0 puhul.
> 
> Saidil AppSource saadaval olev **Kuluhalduse** Power BI sisupakett on aegunud. Lisateavet aegumise kohta vt teemast [AppSource’is saadaval olevad Power BI sisupaketid](../migration-upgrade/deprecated-features.md#power-bi-content-packs-available-on-appsource).

See Power BI sisu pakub liigitatud vormingut, mis aitab teil jälgida varude jõudlust ja visualiseerida kulude voogu läbi nende. Pääsete juhtimisülevaadetele, nagu ringluskiirus; päevade arv, kui kaua varud on laos olnud; täpsus ja ABC-liigitus, ligi eelistatud koondtasemel (ettevõte, kaup, kaubagrupp või koht). Teavet saab kasutada ka finantsaruande üksikasjaliku lisana.

Power BI sisu on rajatud on koondmõõtmisele **CostObjectStatementCacheMonthly**, millele on põhiandmete allikatabelina liidetud **CostObjectStatementCache**. Seda tabelit hallatakse andmekogumi vahemälu raamistikuga. Vaikimisi värskendatakse tabelit iga 24 tunni järel, kuid saate värskendamissagedust muuta või lubada andmekogumi vahemälu konfiguratsioonis käsitsi värskendused. Käsitsi värskendusi saab käivitada kas tööruumis **Kuluhaldus** või **Kuluanalüüs**.

Pärast iga tabeli **CostObjectStatementCache** värskendust tuleb enne, kui andmed Power BI visualisatsioonidel värskendatakse, värskendada koondmõõtmist **CostObjectStatementCacheMonthly**.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

**Kuluhalduse** Power BI sisu kuvatakse tööruumis **Kuluhaldus** ja **Kuluanalüüs**.

Tööruum **Kuluhaldus** sisaldab järgmisi vahekaarte.

- **Ülevaade** – sellel vahekaardil kuvatakse rakenduse andmed.
- **Laoarvestuse olek** – sellel vahekaardil kuvatakse Power BI sisu.
- **Tootmise raamatupidamise olek** – sellel vahekaardil kuvatakse Power BI sisu.

Tööruum **Kuluanalüüs** sisaldab järgmisi vahekaarte.

- **Ülevaade** – sellel vahekaardil kuvatakse rakenduse andmed.
- **Laoarvestuse analüüs** – sellel vahekaardil kuvatakse Power BI sisu.
- **Tootmise raamatupidamise analüüs** – sellel vahekaardil kuvatakse Power BI sisu.
- **Standardse omahinna hälbe analüüs** – sellel vahekaardil kuvatakse Power BI sisu.

## <a name="report-pages-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad aruande lehed

**Kuluhalduse** Power BI sisu sisaldab aruandelehtede komplekti, mis koosneb mõõdikute kogumist. Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena. 

Järgmised tabelid annavad ülevaate **Kuluhalduse** Power BI sisu visualiseeringutest.

### <a name="inventory-accounting-status"></a>Laoarvestuse olek

| Aruandeleht                               | Visualiseering                                   |
|-------------------------------------------|-------------------------------------------------|
| Varude ülevaade                        | Algsaldo                               |
|                                           | Netomuutus                                      |
|                                           | Netomuutuse %                                    |
|                                           | Lõppsaldo                                  |
|                                           | Varude täpsus                              |
|                                           | Lao ringluskiirus                        |
|                                           | Vaba kaubavaru hoidmise päevad                          |
|                                           | Aktiivne toode perioodis                        |
|                                           | Aktiivsed kuluobjektid perioodis                   |
|                                           | Saldo kaubagruppide kaupa                           |
|                                           | Saldo laoala järgi                                 |
|                                           | Väljavõte kategooria alusel                           |
|                                           | Netomuutus kvartalite kaupa                           |
| Varude ülevaade laoala ja kaubagruppide kaupa | Varude täpsus laoala järgi                      |
|                                           | Lao ringluskiirus laoala järgi                |
|                                           | Varude lõppsaldo laoala järgi                |
|                                           | Varude täpsus kaubagruppide kaupa                |
|                                           | Lao ringluskiirus kaubagruppide kaupa          |
|                                           | Varude lõppsaldo laoala ja kaubagruppide kaupa |
| Inventuuriväljavõte                       | Inventuuriväljavõte                             |
| Inventuuriväljavõte laoala järgi               | Inventuuriväljavõte laoala järgi                     |
| Inventuuriväljavõte tootehierarhia alusel  | Inventuuriväljavõte                             |
| Inventuuriväljavõte tootehierarhia alusel  | Inventuuriväljavõte laoala järgi                     |

### <a name="manufacturing-accounting-status"></a>Tootmise raamatupidamise olek

| Aruandeleht                | Visualiseering                       |
|----------------------------|-------------------------------------|
| Lõpetamata toodangu ülevaade YTD-ni           | Algsaldo                   |
|                            | Netomuutus                          |
|                            | Netomuutuse %                        |
|                            | Lõppsaldo                      |
|                            | WIP-i ringluskiirus                  |
|                            | WIP-i hoidmise päevad                    |
|                            | Aktiivne kuluobjekt perioodis        |
|                            | Netomuutus ressursigrupi alusel        |
|                            | Saldo laoala järgi                     |
|                            | Väljavõte kategooria alusel               |
|                            | Netomuutus kvartalite kaupa               |
| lõpetamata toodangu aruanne              | Algsaldo                   |
|                            | Lõppsaldo                      |
|                            | WIP-aruanne kategooria alusel           |
| WIP-aruanne laoala järgi      | Algsaldo                   |
|                            | Lõppsaldo                      |
|                            | WIP-aruanne kategooria ja laoala alusel  |
| WIP-aruanne hierarhia alusel | Algsaldo                   |
|                            | Lõppsaldo                      |
|                            | WIP-aruanne kategooriahierarhia alusel |

### <a name="inventory-accounting-analysis"></a>Laoarvestuse analüüs

| Aruandeleht        | Visualiseering                                                                |
|--------------------|------------------------------------------------------------------------------|
| Kaubavaru üksikasjad  | 10 peamist ressurssi lõppsaldo alusel                                           |
|                    | 10 peamist ressurssi netomuutuse tõusu alusel                                      |
|                    | 10 peamist ressurssi netomuutuse vähenemise alusel                                      |
|                    | 10 peamist ressurssi lao ringluskiiruse alusel                                 |
|                    | Ressursid madala lao ringluskiiruse ja läve ületava lõppsaldo alusel |
|                    | 10 peamist ressurssi vähese täpsuse alusel                                             |
| ABC-liigitamine | Varude lõppsaldo                                                     |
|                    | Tarbitud materjal                                                            |
|                    | Müüdud (COGS)                                                                  |
| Varude trendid   | Varude lõppsaldo                                                     |
|                    | Varude netomuutus                                                         |
|                    | Lao ringluskiirus                                                     |
|                    | Varude täpsus                                                           |

### <a name="manufacturing-accounting-analysis"></a>Tootmise raamatupidamise analüüs

| Aruandeleht | Visualiseering      |
|-------------|--------------------|
| WIP trendid  | WIP lõppsaldo |
|             | WIP netomuutus     |
|             | WIP-i ringluskiirus |

### <a name="std-cost-variance-analysis"></a>Standardse omahinna hälbe analüüs

| Aruandeleht                             | Visualiseering                                        |
|-----------------------------------------|------------------------------------------------------|
| Ostuhinna hälve (standardhind) YTD-ni | Hangitud saldo                                     |
|                                         | Ostuhinna hälve                              |
|                                         | Ostuhinna hälbe määr                        |
|                                         | Hälve kaubagruppide kaupa                               |
|                                         | Hälve laoala järgi                                     |
|                                         | Ostuhind kvartalite kaupa                            |
|                                         | Ostuhind kvartalite ja kaubagruppide kaupa             |
|                                         | 10 peamist ressurssi ebasoodsa ostuhinna hälbe määra järgi |
|                                         | 10 peamist ressurssi soodsa ostuhinna hälbe määra järgi   |
| Tootmiskulude hälve (standardhind) YTD-ni     | Toodangu omahind                                    |
|                                         | Tootmiskulude hälve                                  |
|                                         | Tootmiskulude hälbe määr                            |
|                                         | Hälve kaubagruppide kaupa                               |
|                                         | Hälve laoala järgi                                     |
|                                         | Tootmishälve kvartalite kaupa                       |
|                                         | Tootmishälve kvartalite ja hälbe tüübi järgi     |
|                                         | 10 peamist ressurssi ebasoodsa tootmishälbe järgi  |
|                                         | 10 peamist ressurssi soodsa tootmishälbe järgi    |

### <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

Rakenduse Microsoft Dynamics 365 for Finance and Operations andmeid kasutatakse **Kuluhalduse** Power BI sisu aruande lehtede täitmiseks. Need andmed esitatakse koondmõõtmistena, mis on koondatud üksuse kauplusesse, mis on analüüsimiseks optimeeritud Microsoft SQL Serveri andmebaas. Lisateavet vt teemast [Power BI integratsioon üksuse kauplusega](power-bi-integration-entity-store.md).

Järgmiste objektide peamisi koondmõõdikuid kasutatakse Power BI sisu alusena.

| Objekt                          | Peamised koondmõõtmised | Finance and Operationsi andmeallikas | Väli               |
|---------------------------------|----------------------------|----------------------------------------|---------------------|
| CostObjectStatementCacheMonthly | Summa                     | CostObjectStatementCache               | Summa              |
| CostObjectStatementCacheMonthly | Kogus                   | CostObjectStatementCache               | Kogus                 |
| CostInventoryAccountingKPIGoal  | AnnualInventoryTurn        | CostInventoryAccountingKPIGoal         | AnnualInventoryTurn |
| CostInventoryAccountingKPIGoal  | InventoryAccuracy          | CostInventoryAccountingKPIGoal         | InventoryAccuracy   |

Järgmises tabelis on toodud peamised arvutatud mõõtmised Power BI sisus.

| Mõõt                            | Kalkulatsioon |
|------------------------------------|-------------|
| Algsaldo                  | Algsaldo = [Lõppsaldo] - [Netomuutus] |
| Koguse algsaldo             | Koguse algsaldo = [Lõppsaldo kogus] - [Netomuutuse kogus] |
| Lõppsaldo                     | Lõppsaldo = (CALCULATE(SUM([Summa]), FILTER(ALL(FiscalCalendar) ,FiscalCalendar[MONTHSTARTDATE] \<= MAX(FiscalCalendar[MONTHSTARTDATE])))) |
| Koguse lõppsaldo                | Koguse lõppsaldo = CALCULATE(SUM([QTY]), FILTER(ALL(FiscalCalendar),FiscalCalendar[MONTHSTARTDATE] \<= MAX(FiscalCalendar[MONTHSTARTDATE]))) |
| Netomuutus                         | Netomuutus = SUM([AMOUNT]) |
| Koguse netomuutuse                    | Koguse netomuutuse = SUM([QTY]) |
| Lao ringluskiirus summa järgi | Lao ringluskiirus summa järgi = if(OR([Varude keskmine saldo] \<= 0, [Müüdud või tarbitud varude väljaminekud] \>= 0), 0, ABS([Müüdud või tarbitud varude väljaminekud])/[Varude keskmine saldo]) |
| Varude keskmine saldo          | Varude keskmine saldo = (([Lõppsaldo] + [Algsaldo]) / 2) |
| Vaba kaubavaru hoidmise päevad             | Vaba kaubavaru hoidmise päevad = 365 / CostObjectStatementEntries[Lao ringluskiirus summa järgi] |
| Varude täpsus                 | Varude täpsus summa alusel = IF([Lõppsaldo] \<= 0, IF(OR([Varude loetud summa] \<\> 0, [Lõppsaldo] \< 0), 0, 1), MAX(0, ([Lõppsaldo] - ABS([Varude loetud summa]))/[Lõppsaldo])) |

Järgmisi põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate andmiseks.


|                         Üksus                          |             Atribuutide näited              |
|---------------------------------------------------------|-------------------------------------------------|
|                        Tooted                         | Tootenumber, toote nimi, ühik, kaubagrupid |
| Kategooriahierarhiad (määratud rolli Kuluhaldus) |       Kategooriahierarhia, kategooria tase        |
|                     Juriidilised isikud                      |               Juriidilise isiku nimed                |
|                    Rahandussaasta kalendrid                     |  Rahanduskalender, aasta, kvartal, periood, kuu  |
|                          Sait                           |        ID, nimi, aadress, maakond, riik        |


