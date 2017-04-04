---
title: Kulude juhtimise Power BI sisu
description: "Selles teemas kirjeldatakse, mida sisaldab kulude juhtimise Power BI sisu. See selgitab, kuidas on võimalik saada Power BI aruanded ja teave andmemudel ja üksuste, mida kasutatakse ehitada sisu."
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

# <a name="cost-management-power-bi-content"></a>Kulude juhtimise Power BI sisu

Selles teemas kirjeldatakse, mida sisaldab kulude juhtimise Power BI sisu. See selgitab, kuidas on võimalik saada Power BI aruanded ja teave andmemudel ja üksuste, mida kasutatakse ehitada sisu.

# <a name="overview"></a>Ülevaade

Selle **kulude juhtimise** Microsoft Power BI sisu on mõeldud varude raamatupidajate või organisatsioonis isikud, kes vastutavad varude. Selle **kulude juhtimise** Power BI sisu võimaldavad juhtimis varude ja töö-in-progress (WIP) varude ja kuidas kuluvoog nende kaudu kaupa ajas. Teavet saab ka üksikasjaliku finantsaruande täiendamiseks.

## <a name="key-measures"></a>Peamised meetmed

+ Algsaldo
+ Lõppsaldo
+ Netomuutus
+ Muutus %
+ Ajaline jaotus

## <a name="key-performance-indicators"></a>Juhtimismõõdikud
+ Laokäive
+ Varude täpsus

CostAggregatedCostStatementEntryEntity esmane andmeallikas on CostStatementCache tabel. See tabel haldab andmete vahemälu raames. Vaikimisi on tabelis on värskendatud iga 24 tunni järel, kuid saate lubada andmete vahemälu konfiguratsiooni käsitsi värskendamine. Te saate tehke käsitsi uuendamine ning **kulude juhtimise** või **kulude analüüs** tööruumi. Pärast värskenduse CostStatementCache peate värskendama värskendatud andmed saidil näha BI.com õigus OData-ühenduses. Power BI sisu dispersiooni (ost, tootmine) meetmed puudutavad ainult üksused, mis on hinnata standardkulu seire metoodikast. Tootmise dispersiooni arvutamiseks aktiivne kulude ja realiseeritud kulusid. Tootmise dispersioon arvutatakse tootmistellimuse olek on **lõpetatud**. Tootmise hälve tüübid ja iga tüübi arvutamine kohta lisateabe saamiseks vaadake [analüüsides dispersiooniga lõpetatud tootmistellimuse kohta](https://technet.microsoft.com/en-us/library/gg242850.aspx).

## <a name="accessing-the-power-bi-content"></a>Power BI infosisu
Selle **kulude juhtimise** Power BI on saadaval PowerBI.com. Kuidas ühendada ja laadida oma Microsoft Dynamics 365 toimingute andmete kohta lisateabe saamiseks vaadake [juurdepääsu Power BI sisu: PowerBI.com](power-bi-home-page.md).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mõõdikud, mis sisalduvad Power BI sisu
Sisu hõlmab aruanne lehtede komplektist. Iga lehekülg koosneb parameetrid, mis on näitlikustada diagrammid, plaadid ja tabelid. Järgnev tabel annab ülevaate visualiseeringuid ja selle **kulude juhtimise** Power BI sisu.

| Aruanne lehekülg | Diagrammid | Tiitlid |
|---|---|---|
|Varude üldine (vaikimisi järgi praeguse perioodi) |Täpsus |Varude meetmed:<br>Varude lõppsaldo<br>Varude muutus<br>Varude muutus %<br>|
| |Laokäive | |
| |Varude lõppsaldo ressursirühma poolt | |
| |Varude muutus kategooria nimi tase 1 ja kategooria nimi tase 2| |
| |Osta dispersiooniga ressursirühma ja kategooria nimi tase 3 | |
|Varude saidi (vaikimisi järgi praeguse perioodi) |Varude lõppsaldo saidi nimi ja ressursirühma | |
| |Varude lülitada saidi nimi ja ressursirühma | |
| |Varude lõppsaldo linna ja ressursside Group | |
|Varude ressursirühma (vaikimisi järgi praeguse perioodi) |Varude meetmed | |
| |Varude täpsus poolt ressursirühma summaga | |
| |Nimekirja lülitada, ressursirühma summaga | |
|Varude kasv (vaikimisi jooksval aastal versus eelmisel aastal) |Varude meetmed | |
| |Varude KPI-d:<br>Laokäive<br>Varude täpsus | |
| |Varude lõppsaldo aasta ja ressursside Group | |
| |Osta dispersiooniga aasta ja kategooria nimi tase 3 | |
|Varude vananemine (vaikimisi poolt jooksval aastal) |Varude vananemist kvartali ja ressursside Group | |
| |Varude vananemist kvartali ja saidi nime järgi | |
|Lõpetamata toodangu üldist (vaikimisi järgi praeguse perioodi) |WIP neto muuta kategooria nimi 1 ja kategooria nimi 2 |Tööd lõpetamata toodangu meetmed:<br>Lõpetamata toodangu lõppsaldo<br>Lõpetamata toodangu muutus<br>Lõpetamata toodangu muutus %<br> |
| |Tootmise dispersiooniga ressursirühma ja kategooria nimi tase 3 | |
| |Lõpetamata toodangu muutus ressursirühma poolt | |
|Lõpetamata toodangu Site (vaikimisi järgi praeguse perioodi) |Tööd lõpetamata toodangu meetmed | |
| |WIP kokku muuta saidi nimi ja kategooria nimi tase 2 | |
| |Tootmise dispersiooniga saidi nimi ja kategooria nimi tase 3 | |

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Dynamics 365 operatsioonide andmeid kasutatakse aruande lehti asustada selle **kulude juhtimise** Power BI sisu. Need andmed esitatakse arvuna kokku mõõtmised, mis on lavastatud olem poest, mis on Microsoft SQL andmebaasi, mis on optimeeritud analytics. Lisateabe saamiseks vaadake [ülevaade Power BI Integratsioon üksus poe](power-bi-integration-entity-store.md). Aluse sisu kasutatakse järgmisi peamisi kokku mõõtmisi.

| Üksus            | Kogu hindamise | Dynamics 365 operatsioonide jaoks | Väli             | Kirjeldus                       |
|-------------------|---------------------------|---------------------------------------------|-------------------|-----------------------------------|
| Pangaväljavõtte kannete | Netomuutus                | CostAggregatedCostStatementEntryEntity      | Summa (\[summa\])   | Summa valuutas raamatupidamise |
| Pangaväljavõtte kannete | Koguse muutus       | CostAggregatedCostStatementEntryEntity      | Summa (\[kogus\]) |                                   |

Järgmises tabelis on kokku peamised mõõtmised kasutamise luua mitu arvutatud mõõtmeid sisu andmekogumis.

| Mõõt                                 | Meetme arvutamine                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Algsaldo                       | \[Lõppsaldo\]-\[käive\]                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Alguses tasakaalu kogus              | \[Lõppenud tasakaalu kogus\]-\[muutus, kogus\]                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Lõppsaldo                          | Arvuta (summa (\[summa\]), FILTER (ALLEXCEPT ("Finantskalendrid", "Finantskalendrid"\[LedgerRecId\], "üksust"\[ID\], "üksust"\[nimi\], "Arvestusraamatud"\[valuuta\], "Arvestusraamatud"\[kirjeldus\], "Arvestusraamatud"\[nimi\]), finantsaasta kalendrid\[kuupäev\]&lt;= MAX (finantsaasta kalendrid\[kuupäev\])))                                                                                                                                                                                           |
| Lõpp tasakaalu kogus                 | Arvuta (summa (\[kogus\]), FILTER (ALLEXCEPT ("Finantskalendrid", "Finantskalendrid"\[LedgerRecId\], "üksust"\[ID\], "üksust"\[nimi\], "Arvestusraamatud"\[valuuta\], "Arvestusraamatud"\[kirjeldus\], "Arvestusraamatud"\[nimi\]), finantsaasta kalendrid\[kuupäev\]&lt;= MAX (finantsaasta kalendrid\[kuupäev\])))                                                                                                                                                                                         |
| Lao algsaldo             | Arvuta (\[algsaldo\], "Pangaväljavõtte kannete"\[aruande tüübi\] = "Varu")                                                                                                                                                                                                                                                                                                                                                                                      |
| Varude lõppsaldo                | Arvuta (\[lõppsaldo\], "Pangaväljavõtte kannete"\[aruande tüübi\] = "Varu")                                                                                                                                                                                                                                                                                                                                                                                         |
| Varude muutus                    | Arvuta (\[muutus\], "Pangaväljavõtte kannete"\[aruande tüübi\] = "Varu")                                                                                                                                                                                                                                                                                                                                                                                             |
| Varude muutus kogus           | Arvuta (\[muutus, kogus\], "Pangaväljavõtte kannete"\[aruande tüübi\] = "Varu")                                                                                                                                                                                                                                                                                                                                                                                    |
| Varude muutus %                  | IF (\[varude lõppsaldo\] = 0, 0, \[varude muutus\] / \[varude lõppsaldo\])                                                                                                                                                                                                                                                                                                                                                                           |
| Nimekirja lülitada, summa                | Kui (OR (\[varude keskmine jääk\]&lt;= 0, \[inventuuri müüdud või kasutatud küsimusi\]&gt;= 0), 0, ABS (\[inventuuri müüdud või kasutatud küsimused\]) /\[varude panga\])                                                                                                                                                                                                                                                                                                  |
| Keskmist laoseisu               | (\[Varude lõppsaldo\] + \[varude alguse saldo\]) / 2                                                                                                                                                                                                                                                                                                                                                                                                       |
| Inventuuri müüdud või kasutatud küsimusi       | \[Laost müüdud\] + \[varude tarbitud materjalikulu\]                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Varude tarbitud materjalikulu        | Arvuta (\[varude muutus\], "Pangaväljavõtte kannete"\[kategooria nimi - tase 2\_\] = "ConsumedMaterialsCost")                                                                                                                                                                                                                                                                                                                                                            |
| Laost müüdud                          | Arvuta (\[varude muutus\], "Pangaväljavõtte kannete"\[kategooria nimi - tase 2\_\] = "Müüdud")                                                                                                                                                                                                                                                                                                                                                                             |
| Varude täpsus summa võrra            | IF (\[varude lõppsaldo\]&lt;= 0, kui (või (\[laoseisu loendatud kogus\]&lt;&gt; 0, \[varude lõppsaldo\]&lt; 0), 0, 1), MAX (0, (\[varude lõppsaldo\] -ABS (\[laoseisu loendatud kogus\])) /\[varude lõppsaldo\]))                                                                                                                                                                                                                              |
| Varude summa maha                | Arvuta (\[varude muutus\], "Pangaväljavõtte kannete"\[kategooria nimi - tase 3\_\] = "Inventuur")                                                                                                                                                                                                                                                                                                                                                                         |
| Varude ajaline jaotus                         | Kui (ISBLANK (max (finantsaasta kalendrid\[kuupäev\])), blank(), MAX (0, MIN (\[varude vananemist laekumise kogus\], \[varude vananemist lõpeb tasakaalu kogus\] - \[varude vananemist laekumise kogus tulevikus\]))) \*\[varude avg ühiku omahind\]                                                                                                                                                                                                                                |
| Lao sissetulekute kogus vananemist       | Kui (\[minDate\] = \[minDateAllSelected\], Arvuta (\[varude muutus kogus\], "Pangaväljavõtte kannete"\[kogus\]&gt; 0, FILTER (ALLEXCEPT (finantsaasta kalendrid, "Finantskalendrid"\[LedgerRecId\], "üksust"\[ID\], "üksust"\[nimi\], "Arvestusraamatud"\[valuuta\], "Arvestusraamatud"\[kirjeldus\], "Arvestusraamatud"\[nimi\]), finantsaasta kalendrid\[kuupäev\]&lt;= MAX (finantsaasta kalendrid\[kuupäev\]))), Arvuta (\[varude muutus kogus\], "Pangaväljavõtte kannete"\[kogus\]&gt; 0)) |
| Varude vananemist lõppenud tasakaalu kogus | \[Varude lõppenud tasakaalu kogus\] + Arvuta (\[varude muutus kogus\], FILTER (ALLEXCEPT (finantsaasta kalendrid, "Finantskalendrid"\[LedgerRecId\], "üksust"\[ID\], "üksust"\[nimi\], "Arvestusraamatud"\[valuuta\], "Arvestusraamatud"\[kirjeldus\], "Arvestusraamatud"\[nimi\]), finantsaasta kalendrid\[kuupäev\]&gt; max (finantsaasta kalendrid\[kuupäev\])))                                                                                                                                 |
| Lao vananemist sissetulekuid tulevikus  | Arvuta (\[varude muutus\], "Pangaväljavõtte kannete"\[summa\]&gt; 0, FILTER (ALLEXCEPT ("Finantskalendrid", "Finantskalendrid"\[LedgerRecId\], "üksust"\[ID\], "üksust"\[nimi\], "Arvestusraamatud"\[valuuta\], "Arvestusraamatud"\[kirjeldus\], "Arvestusraamatud"\[nimi\]), finantsaasta kalendrid\[kuupäev\]&gt; MAX (finantsaasta kalendrid\[kuupäev\])))                                                                                                                                             |
| Varude avg ühiku omahind                 | Arvuta (\[varude lõppsaldo\] / \[varude lõpeb tasakaalu kogus\], ALLEXCEPT ("Finantskalendrid", "Finantskalendrid"\[LedgerRecId\], "üksust"\[ID\], "üksust"\[nimi\], "Arvestusraamatud"\[valuuta\], "Arvestusraamatud"\[kirjeldus\], "Arvestusraamatud"\[nimi\]))                                                                                                                                                                                                                 |
| Osta dispersioonide                      | Arvuta (summa (\[summa\]), "Pangaväljavõtte kannete"\[kategooria nimi - tase 2\_\] = "Procured", "Pangaväljavõtte kannete"\[aruande tüübi\] = "Hälve")                                                                                                                                                                                                                                                                                                                              |
| Lõpetamata toodangu alguse saldo                   | Arvuta (\[algsaldo\], "Pangaväljavõtte kannete"\[aruande tüübi\] = "Lõpetamata")                                                                                                                                                                                                                                                                                                                                                                                            |
| Lõpetamata toodangu lõppsaldo                      | Arvuta (\[lõppsaldo\], "Pangaväljavõtte kannete"\[aruande tüübi\] = "Lõpetamata")                                                                                                                                                                                                                                                                                                                                                                                               |
| Lõpetamata toodangu muutus                          | Arvuta (\[muutus\], "Pangaväljavõtte kannete"\[aruande tüübi\] = "Lõpetamata")                                                                                                                                                                                                                                                                                                                                                                                                   |
| Lõpetamata toodangu muutus %                        | IF (\[lõpetamata toodangu lõppsaldo\] = 0, 0, \[lõpetamata toodangu muutus\] / \[lõpetamata toodangu lõppsaldo\])                                                                                                                                                                                                                                                                                                                                                                                             |
| Tootmise dispersioonide                    | Arvuta (summa (\[summa\]), "Pangaväljavõtte kannete"\[kategooria nimi - tase 2\_\] = "ManufacturedCost", "Pangaväljavõtte kannete"\[aruande tüübi\] = "Hälve")                                                                                                                                                                                                                                                                                                                      |
| Kategooria nimi - tase 1                 | Lüliti (\[kategooria nimi - tase 1\_\], "Ei ole", "Ei ole", "NetSourcing", "Neto hankimisel", "NetUsage", "Net kasutamine", "NetConversionCost", "Neto Konversiooni kulu", "NetCostOfGoodsManufactured", "Net kaupade maksumus", "BeginningBalance", "Algsaldo")                                                                                                                                                                                                         |
| Kategooria nimi - tase 2                 | Lüliti (\[kategooria nimi - tase 2\_\], "Ei ole", "Ei ole", "Procured", "Procured", "Disposed", "Disposed", "Üle kantud", "Üle kantud", "Müüdud", "Müüdud", "ConsumedMaterialsCost", "Tarbitud materjalikulu", "ConsumedManufacturingCost", "Tarbitud tootmiskulude", "ConsumedOutsourcingCost", "Tarbitud kulu allhanget", "ConsumedIndirectCost", "Keskmine kaudne kulu", "ManufacturedCost", "Valmistatud maksab", "Erinevused", "Dispersiooniga")                            |
| Kategooria nimi - tase 3                 | Lüliti (\[kategooria nimi - tase 3\_\], "Ei ole", "Ei ole", "Lugedes", "Ei ole", "ProductionPriceVariance", "Tootjahind", "QuantityVariance", "Kogus", "SubstitutionVariance", "Asendamine", "ScrapVariance", "Jääk", "LotSizeVariance", "Partii suurus", "RevaluationVariance", "Ümberhindamise", "PurchasePriceVariance", "Ostuhind", "CostChangeVariance", "Kulude muutus", "RoundingVariance", "Ümardamise erinevus")                                                   |

Filtritena kasutatakse järgmisi peamisi näitajaid viil kokku mõõtmistel saavutada suurem granulaarsus ja annavad põhjalikuma analüüsi ülevaate.

| Üksus           | Näited atribuutidest                       |
|------------------|----------------------------------------------|
| Üksused         | ID, nimi                                     |
| Rahandussaasta kalendrid | Kalender, kuu, kvartal, perioodi aasta       |
| KPI eesmärgid        | Varude täpsus eesmärk, varude omakorda eesmärk |
| Pearaamatud          | Valuuta, nimi, kirjeldus                  |
| Saidid            | ID, nimi, riik,                      |

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)



