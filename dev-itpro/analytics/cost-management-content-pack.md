---
title: Kuluhalduse Power BI sisu
description: "See teema kirjeldab, mida hõlmab kuluhalduse Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations
ms.custom: 270314
ms.assetid: 9680d977-43c8-47a7-966d-2280ba21402a
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: e4de011e6eeac58643b828b65e24b874d981d5e7
ms.lasthandoff: 03/31/2017


---

# <a name="cost-management-power-bi-content"></a>Kuluhalduse Power BI sisu

[!include[banner](../includes/banner.md)]


See teema kirjeldab, mida hõlmab kuluhalduse Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

# <a name="overview"></a>Ülevaade

**Kuluhalduse** Microsoft Power BI sisu on mõeldud laoraamatupidajatele või organisatsioonis varude eest vastutavatele üksikisikutele. **Kuluhalduse** Power BI sisu pakub juhtimisülevaadet varudest ja pooleliolevatest (WIP) varudest ning neist aja jooksul kategooriate kaupa läbivoolavast kulust. Teavet saab kasutada ka finantsaruande üksikasjaliku lisana.

## <a name="key-measures"></a>Põhimeetmed

+ Algsaldo
+ Lõppsaldo
+ Netomuutus
+ Netomuutus, %
+ Ajaline jaotus

## <a name="key-performance-indicators"></a>Juhtimismõõdikud
+ Laokäive
+ Varude täpsus

Atribuudi CostAggregatedCostStatementEntryEntity peamine andmeallikas on tabel CostStatementCache. Seda tabelit hallatakse andmekogumi vahemälu raamistikuga. Vaikimisi värskendatakse tabelit iga 24 tunni järel, kuid saate lubada andmete vahemälu konfiguratsioonis käsitsi värskendused. Seejärel saate tabelit käsitsi värskendada tööruumis **Kuluhaldus** või **Kuluanalüüs**. Pärast atribuudi CostStatementCache värskendamist peate värskendama Power Bi.com’is OData ühendust, et näha värskendatud andmeid saidil. Hälbe (ostu, tootmise) meetmed selles Power BI sisus puudutavad ainult kaupu, mida hinnatakse varude standardomahinna meetodiga. Toote hälve arvutatakse erinevusena tegeliku kulu ja realiseeritud kulu vahel. Tootmishälve arvutatakse, kui tootmistellimuse olek on **Lõpetatud**. Lisateavet tootmishälvete tüüpide ja iga tüübi arvutamise kohta vt teemast [Teave lõpule viidud tootmistellimuse hälvete analüüsimise kohta](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Kuluhalduse** Power BI sisu on saadaval veebisaidil PowerBI.com. Lisateavet Microsoft Dynamics 365 for Operationsi andmete ühendamise ja laadimise kohta vt teemast [Juurdepääs Power BI sisule saidilt PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad mõõdikud
Sisu hõlmab aruandelehtede komplekti. Iga leht koosneb mõõdikute komplektist, mida visualiseeritakse diagrammide, paanide ja tabelitena. Järgmine tabel annab ülevaate **kuluhalduse** Power BI sisu visualiseerimistest.

| Aruandeleht | Diagrammid | Tiitlid |
|---|---|---|
|Varud kokku (vaikimisi praeguse perioodi järgi) |Täpsus |Varude meetmed<br>Varude lõppsaldo<br>Varude netomuutus<br>Varude netomuutuse %<br>|
| |Laokäive | |
| |Varude lõppsaldo ressursigrupi alusel | |
| |Varude netomuutus kategooria 1. ja 2. nimetaseme alusel| |
| |Ostuhälbed ressursigrupi ja kategooria 3. nimetaseme alusel | |
|Varud saidi alusel (vaikimisi praeguse perioodi järgi) |Varude lõppsaldo saidi nime ja ressursigrupi alusel | |
| |Laokäive saidi nime ja ressursigrupi alusel | |
| |Varude lõppsaldo linna ja ressursigrupi alusel | |
|Varud ressursigrupi alusel (vaikimisi praeguse perioodi järgi) |Varude meetmed | |
| |Varude täpsus summa alusel ressursigrupi järgi | |
| |Laokäive summa alusel ressursigrupi järgi | |
|Varude YOY (vaikimisi praegune aasta vs eelmine aasta) |Varude meetmed | |
| |Varude KPI-d<br>Laokäive<br>Varude täpsus | |
| |Varude lõppsaldo aasta ja ressursigrupi alusel | |
| |Ostuhälbed aasta ja kategooria 3. nimetaseme alusel | |
|Varude ajaline jaotus (vaikimisi praeguse aasta järgi) |Varude ajaline jaotus kvartali ja ressursigrupi alusel | |
| |Varude ajaline jaotus kvartali ja saidi nime alusel | |
|WIP kokku (vaikimisi praeguse perioodi järgi) |WIP netomuutus kategooria 1. ja 2. nimetaseme alusel |Poolelioleva töö (WIP) meetmed<br>WIP lõppsaldo<br>WIP netomuutus<br>WIP netomuutuse %<br> |
| |Tootmishälbed ressursigrupi ja kategooria 3. nimetaseme alusel | |
| |WIP netomuutus ressursigrupi alusel | |
|WIP saidi alusel (vaikimisi praeguse perioodi järgi) |Poolelioleva töö (WIP) meetmed | |
| |WIP netomuutus saidi nime ja kategooria 2. nimetaseme alusel | |
| |Tootmishälbed saidi nime ja kategooria 3. nimetaseme alusel | |

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Aruandelehtede täitmiseks **kuluhalduse** Power BI sisus kasutatakse Dynamics 365 for Operationsi andmeid. Need andmed esitatakse koondmõõtmistena, mis on koondatud üksuse kauplusse, mis on analüüsimiseks optimeeritud Microsoft SQL-i andmebaas. Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md). Sisu alusena kasutatakse järgmisi peamisi koondmõõtmisi.

| Üksus            | Peamine koondmõõtmine | Dynamics 365 for Operationsi andmeallikas | Väli             | Kirjeldus                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Väljavõtte kirjed | Netomuutus                | CostAggregatedCostStatementEntryEntity      | sum(\[Summa\])   | Summa arvestusvaluutas |
| Väljavõtte kirjed | Netomuutuse kogus       | CostAggregatedCostStatementEntryEntity      | sum(\[Kogus\]) |                                   |

Järgmine tabel näitab, kuidas kasutatakse peamisi koondmõõtmisi mitme arvutatud meetme loomiseks sisu andmekogumis.

| Mõõt                                 | Meetme arvutamise viis                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Algsaldo                       | \[Lõppsaldo\]-\[Netomuutus\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Algsaldo kogus              | \[Lõppsaldo kogus\]-\[Netomuutuse kogus\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Lõppsaldo                          | CALCULATE(SUM(\[Summa\]), FILTER(ALLEXCEPT('Rahandusaasta kalendrid', 'Rahandusaasta kalendrid'\[LedgerRecId\], 'üksused'\[ID\], 'üksused'\[Nimi\], 'Pearaamatud'\[Valuuta\], 'Pearaamatud'\[Kirjeldus\], 'Pearaamatud'\[Nimi\]), 'Rahandusaasta kalendrid'\[Kuupäev\] &lt;= MAX('Rahandusaasta kalendrid'\[Kuupäev\])))                                                                                                                                                                                           |
| Lõppsaldo kogus                 | CALCULATE(SUM(\[Kogus\]), FILTER(ALLEXCEPT('Rahandusaasta kalendrid', 'Rahandusaasta kalendrid'\[LedgerRecId\], 'olemid'\[ID\], 'olemid'\[Nimi\], 'Pearaamatud'\[Valuuta\], 'Pearaamatud'\[Kirjeldus\], 'Pearaamatud'\[Nimi\]), 'Rahandusaasta kalendrid'\[Kuupäev\] &lt;= MAX('Rahandusaasta kalendrid'\[Kuupäev\])))                                                                                                                                                                                         |
| Varude algsaldo             | CALCULATE(\[Algsaldo\], 'Väljavõtte kirjed'\[Väljavõtte tüüp\] = "Varud")                                                                                                                                                                                                                                                                                                                                                                                      |
| Varude lõppsaldo                | CALCULATE(\[Lõppsaldo\], 'Väljavõtte kirjed'\[Väljavõtte tüüp\] = "Varud")                                                                                                                                                                                                                                                                                                                                                                                         |
| Varude netomuutus                    | CALCULATE(\[Netomuutus\], 'Väljavõtte kirjed'\[Väljavõtte tüüp\] = "Varud")                                                                                                                                                                                                                                                                                                                                                                                             |
| Varude netomuutuse kogus           | CALCULATE(\[Netomuutus\], 'Väljavõtte kirjed'\[Väljavõtte tüüp\] = "Varud")                                                                                                                                                                                                                                                                                                                                                                                    |
| Varude netomuutuse %                  | IF(\[Varude lõppsaldo\] = 0, 0, \[Varude netomuutus\] / \[Varude lõppsaldo\])                                                                                                                                                                                                                                                                                                                                                                           |
| Laokäive summa alusel                | if(OR(\[Varude keskmine saldo\] &lt;= 0, \[Müüdud või tarbitud varude väljaminekud\] &gt;= 0), 0, ABS(\[Müüdud või tarbitud varude väljaminekud\])/\[Varude keskmine saldo\])                                                                                                                                                                                                                                                                                                  |
| Varude keskmine saldo               | (\[Varude lõppsaldo\] + \[Varude algsaldo\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Müüdud või tarbitud varude väljaminekud       | \[Müüdud varud\] + \[Tarbitud varude materjalikulu\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Tarbitud varude materjalikulu        | CALCULATE(\[Varude netomuutus\], 'Väljavõtte kirjed'\[Kategooria nimi – 2. tase\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Müüdud varud                          | CALCULATE(\[Varude netomuutus\], 'Väljavõtte kirjed'\[Kategooria nimi – 2. tase\_\] = "Müüdud")                                                                                                                                                                                                                                                                                                                                                                             |
| Varude täpsus summa alusel            | IF(\[Varude lõppsaldo\] &lt;= 0, IF(OR(\[Varude loetud summa\] &lt;&gt; 0, \[Varude lõppsaldo\] &lt; 0), 0, 1), MAX(0, (\[Varude lõppsaldo\] - ABS(\[Varude loetud summa\]))/\[Varude lõppsaldo\]))                                                                                                                                                                                                                              |
| Varude loetud summa                | CALCULATE(\[Varude netomuutus\], 'Väljavõtte kirjed'\[Kategooria nimi – 3. tase\_\] = "Loendus")                                                                                                                                                                                                                                                                                                                                                                         |
| Varude ajaline jaotus                         | if(ISBLANK(max('Rahandusaasta kalendrid'\[Kuupäev\])), blank(), MAX(0, MIN(\[Varude ajalise jaotusega sissetulekute kogus\], \[Varude ajalise jaotusega lõppsaldo kogus\] - \[Varude ajalise jaotusega sissetulekute kogus tulevikus\]))) \* \[Varude keskmine ühikukulu\]                                                                                                                                                                                                                                |
| Varude ajalise jaotusega sissetulekute kogus       | IF(\[minDate\] = \[minDateAllSelected\], CALCULATE(\[Varude netomuutuse kogus\], 'Väljavõtte kirjed'\[Kogus\] &gt; 0, FILTER(ALLEXCEPT('Rahandusaasta kalendrid', 'Rahandusaasta kalendrid'\[LedgerRecId\], 'olemid'\[ID\], 'olemid'\[Nimi\], 'Pearaamatud'\[Valuuta\], 'Pearaamatud'\[Kirjeldus\], 'Pearaamatud'\[Nimi\]), 'Rahandusaasta kalendrid'\[Kuupäev\] &lt;= MAX('Rahandusaasta kalendrid'\[Kuupäev\]))), CALCULATE(\[Varude netomuutuse kogus\], 'Väljavõtte kirjed'\[Kogus\] &gt; 0)) |
| Varude ajalise jaotusega lõppsaldo kogus | \[Varude lõppsaldo kogus\] + CALCULATE(\[Varude netomuutuse kogus\], FILTER(ALLEXCEPT('Rahandusaasta kalendrid', 'Rahandusaasta kalendrid'\[LedgerRecId\], 'olemid'\[ID\], 'olemid'\[Name\], 'Pearaamatud'\[Valuuta\], 'Pearaamatud'\[Kirjeldus\], 'Pearaamatud'\[Nimi\]), 'Rahandusaasta kalendrid'\[Kuupäev\] &gt; max('Rahandusaasta kalendrid'\[Kuupäev\]) ))                                                                                                                                 |
| Varude ajalise jaotusega sissetulekud tulevikus  | CALCULATE(\[Varude netomuutus\], 'Väljavõtte kirjed'\[Summa\] &gt; 0, FILTER(ALLEXCEPT('Rahandusaasta kalendrid', 'Rahandusaasta kalendrid'\[LedgerRecId\], 'üksused'\[ID\], 'üksused'\[Nimi\], 'Pearaamatud'\[Valuuta\], 'Pearaamatud'\[Kirjeldus\], 'Pearaamatud'\[Nimi\]), 'Rahandusaasta kalendrid'\[Kuupäev\] &gt; MAX('Rahandusaasta kalendrid'\[Kuupäev\])))                                                                                                                                             |
| Varude keskmine ühikukulu                 | CALCULATE(\[Varude lõppsaldo\] / \[Varude lõppsaldo kogus\],ALLEXCEPT('Rahandusaasta kalendrid', 'Rahandusaasta kalendrid'\[LedgerRecId\], 'üksused'\[ID\], 'üksused'\[Nimi\], 'Pearaamatud'\[Valuuta\], 'Pearaamatud'\[Kirjeldus\], 'Pearaamatud'\[Nimi\]))                                                                                                                                                                                                                 |
| Ostuhälbed                      | CALCULATE(SUM(\[Summa\]), 'Väljavõtte kirjed'\[Kategooria nimi – 2. tase\_\] = "Hangitud", 'Väljavõtte kirjed'\[Väljavõtte tüüp\] = "Hälve")                                                                                                                                                                                                                                                                                                                              |
| WIP algsaldo                   | CALCULATE(\[Algsaldo\], 'Väljavõtte kirjed'\[Väljavõtte tüüp\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                            |
| WIP lõppsaldo                      | CALCULATE(\[Lõppsaldo\], 'Väljavõtte kirjed'\[Väljavõtte tüüp\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                               |
| WIP netomuutus                          | CALCULATE(\[Netomuutus\], 'Väljavõtte kirjed'\[Väljavõtte tüüp\] = "WIP")                                                                                                                                                                                                                                                                                                                                                                                                   |
| WIP netomuutuse %                        | IF(\[WIP lõppsaldo\] = 0, 0, \[WIP netomuutus\] / \[WIP lõppsaldo\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Tootmishälbed                    | CALCULATE(SUM(\[Summa\]), 'Väljavõtte kirjed'\[Kategooria nimi – 2. tase\_\] = "ManufacturedCost", 'Väljavõtte kirjed'\[Väljavõtte tüüp\] = "Hälve")                                                                                                                                                                                                                                                                                                                      |
| Kategooria nimi – 1. tase                 | switch(\[Kategooria nimi – 1. tase\_\], "Pole", "Pole", "NetSourcing", "Netohange", "NetUsage", "Netokasutus", "NetConversionCost", "Teisenduse netokulu", "NetCostOfGoodsManufactured", "Toodetud kaupade netokulu", "BeginningBalance", "Algsaldo")                                                                                                                                                                                                         |
| Kategooria nimi – 2. tase                 | switch(\[Kategooria nimi – 2. tase\_\], "Pole", "Pole", "Hangitud", "Hangitud", "Likvideeritud", "Likvideeritud", "Ülekantud", "Üle kantud", "Müüdud", "Müüdud", "ConsumedMaterialsCost", "Tarbitud materjalikulu", "ConsumedManufacturingCost", "Tarbitud tootmiskulu", "ConsumedOutsourcingCost", "Tarbitud hankekulu", "ConsumedIndirectCost", "Tarbitud kaudne kulu", "ManufacturedCost", "Tootmiskulu", "Hälbed", "Hälbed")                            |
| Kategooria nimi – 3. tase                 | switch(\[Kategooria nimi – 3. tase\_\], "Pole", "Pole", "Loendus", "Pole", "ProductionPriceVariance", "Tootmishind", "QuantityVariance", "Kogus", "SubstitutionVariance", "Asendus", "ScrapVariance", "Praak", "LotSizeVariance", "Partii suurus", "RevaluationVariance", "Ümberhindlus", "PurchasePriceVariance", "Ostuhind", "CostChangeVariance", "Kulu muutus", "RoundingVariance", "Ümardamishälve")                                                   |

Järgmisi põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate andmiseks.

| Üksus           | Atribuutide näited                       |
|------------------|----------------------------------------------|
| Üksused         | ID, nimi                                     |
| Rahandussaasta kalendrid | Kalender, kuu, periood, kvartal, aasta       |
| KPI eesmärgid        | Varude täpsuse eesmärk, laokäibe eesmärk |
| Pearaamatud          | Valuuta, nimi, kirjeldus                  |
| Saidid            | ID, nimi, riik, linn                      |

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)





