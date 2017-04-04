---
title: "Müügi ja tasuvuse jõudlus Power BI sisu"
description: "Selles teemas kirjeldatakse, mida sisaldab Dynamics 365 toiminguteks - müügi ja tasuvuse tulemuslikkuse sisu pack Microsoft Power BI. Selgitab, kuidas sisu pakendis aruannetele juurde pääseda ja teave andmemudel ja üksuste, mida kasutatakse ehitada sisu pakendi."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 3e6b48768bb8e69d46f1555d9300f3b878b01ff1
ms.lasthandoff: 03/31/2017


---

# <a name="sales-and-profitability-performance-power-bi-content"></a>Müügi ja tasuvuse jõudlus Power BI sisu

Selles teemas kirjeldatakse, mida sisaldab Dynamics 365 toiminguteks - müügi ja tasuvuse tulemuslikkuse sisu pack Microsoft Power BI. Selgitab, kuidas sisu pakendis aruannetele juurde pääseda ja teave andmemudel ja üksuste, mida kasutatakse ehitada sisu pakendi.

<a name="overview"></a>Ülevaade
--------

Sisu pack loodi müügijuhid jälgida müügi võtmemõõdikute tulu, kogutulu ja kasumimarginaale. See kasutab Dynamics 365 selgituseks müügiandmetega toimingute ja pakub nii kokku ülevaate kogu ettevõtte andmed ja jaotus müügi tulemuslikkuse kliente ja tooteid. Tõstes esile muutused tulude ja kasumi kasvu ajas, aruanded saab kasutada alert juhtidega positiivsete ja negatiivsete suundumuste üksikute klientide ja toodete. Kategooria ja regiooni näidatakse läheb vaja on võrrelda tulu ja kasumlikkuse erinevate tootekategooriate ja kliendigruppide üksteisele esile delel alumises ja juhid graafikuid. Põhjaliku aruande, mis kujutab üksiku kliendi tulud versus kasumimarginaali pakkumised kliendihaldurid häälestada oma müügi- ja jõupingutusi iga kliendi vastava profiili andmed tagatud Sihtasutus. Müügi ja tasuvuse jõudlus sisu võimaldab analüüsida müügi tulemuslikkuse poolt müügijuhid:

-   Tulu, aasta kuupäevani (kaupa kliendigrupp ja üksikute klientide, müügi, ja üksikute toodete kaugemad)
-   Müügitulu muutus aastane (kliendi piirkondade ja müük kategooriate) järgi

Tasuvuse saab analüüsida:

-   Brutokasum ning – marginaal (nii klientide kui vaatlusaluse toote müük kategooriate)
-   Kogutulu muutus,-aastane
-   Kliendi kasumlikkus (müügitulu võrreldes brutomarginaalist) poolt

## <a name="accessing-the-content-pack"></a>Juurdepääsu sisu pakendi
Müügi ja tasuvuse jõudlus Power BI sisu avaldatakse rakendamist varana elutsükli teenused (LCS) ja pääseb Dynamics 365 toiminguteks. Kuidas leida ja käivitada Power BI aruanded kohta lisateabe saamiseks vaadake [Power BI sisu LCS Microsofti ja oma partnerite](power-bi-content-microsoft-partners.md).

## <a name="metrics-included-in-the-content-pack"></a>Kaasatud sisu pack mõõdikud
Sisu pack sisaldab aruande, milles on kirjeldatud parameetrid näitlikustada diagrammid, plaadid ja tabelid. Järgmises tabelis antakse ülevaade Visual sisu Pack.

|                        |                                            |                                                         |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| **Aruanne lehekülg**        | **Charts**                                 | **Plaadid**                                               |
| Tulud kliendi poolt    | Top 10 hotelli tuludega                | Kogutulem                                           |
|                        | Kogutulu kliendi grupi poolt            | Kvartaalne kasv                                      |
|                        | Keskmine kliendi kliendi grupi müügitulud | Kogutulu                                            |
|                        | Müügitulu ja brutokasum kliendigrupi poolt   |                                                         |
| Tulu toodete kaupa     | Müügitulu ja brutokasum müük kategooria järgi   | Kokku \#toodete                                    |
|                        | Top 10 tooted tuludega                 | Mitu kokku protsent ja aktiivsed tooted |
|                        | Kogu müügitulust müük kategooria järgi            | Arvu tooteid, mis moodustavad 80% tulu           |
| Müügitulud perioodi\*    | Tulu kuude lõikes                           | Kvartaalne kasv                                      |
|                        | Lõpus tulude erinevus, eelmise aastaga võrreldes             | Eelmise aastaga võrreldes tulude kasv %                                    |
|                        | Kogu müügi dispersiooni kliendi piirkonniti    |                                                         |
| Müügitulu asukoha järgi    | Müügitulu linn                      |                                                         |
|                        | Eelmise aastaga võrreldes tulude kasv %                       |                                                         |
|                        | Müügitulu piirkonniti                    |                                                         |
| Kliendi kasumlikkus | Brutokasumi marginaali versus tulu, kliendi poolt   | Brutokasum, kogukasum, kasv eelmise aastaga võrreldes          |
| Tulususe analüüs | Müügitulu ja brutokasum kuude kaupa          |                                                         |
|                        | Brutokasumi marginaali klientidele Top 15           |                                                         |
|                        | Brutokasum ühe kuu võrra, eelmise aastaga võrreldes                 |                                                         |

\*Tulu see ja viimane aasta ja majanduskasvu müük kategooria järgi.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Toimingute andmed Dynamics 365 saab asustada müügi ja tasuvuse tulemuslikkuse sisu pakendi aruande. See on esindatud kokku mõõtmised, mis on lavastatud olem poest, mis on optimeeritud analytics Microsoft SQL andmebaasi. Loe seda blogi [Power BI Integratsioon üksus poe Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Kogu selle sisu Pack on osa kokku mõõtmised, mis olid saadaval müügi kuubi Dynamics AX 2012 ja AX 2012 R3. Lavale kuubi kokku mõõtmise üksus poes tegema positsioonidele. Lisateabe saamiseks vaadake menetluse etapp kokku mõõtmise üksus salvestuskohta blogi [Power BI Integratsioon üksus poe Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/). Sisu pakendi alusena kasutatakse järgmisi peamisi kokku mõõtmisi arve read üksuse.

|               |                                              |                                                 |                                              |                                          |
|---------------|----------------------------------------------|-------------------------------------------------|----------------------------------------------|------------------------------------------|
| **Entity**    | **Võtme kõigi mõõtmiste**               | **Dynamics 365 operatsioonide jaoks** | **Field**                                    | **Description**                          |
| Arve read | Tulu                                      | CustInvoiceTrans                                | SUM(LineAmountMST)                           | Summa arvestusvaluutas            |
|               | Müüdud kaupade omahind                           | InventTrans                                     | SUMMA (CostAmountPosted + CostAmountAdjustment) | Omahind + korrektsioon                 |
|               | Komisjon rea summa – raamatupidamise valuuta | CustInvoiceTrans                                | SUM(CommissAmountMST)                        | Komisjonitasu summa valuutas raamatupidamise |

Järgmises tabelis on peamised kokku mõõtmised arve read üksuse, mis kasutab mitu arvutatud mõõtmeid sisu pakendi andmekogumis.

|                   |                                                                                                  |
|-------------------|--------------------------------------------------------------------------------------------------|
| **Measure**       | **Arvutatud**                                                                                |
| Kogukasum      | SUMMA (tulu-OMAHIND – komisjon – käibemaksu (sisaldub kliendi arve rea summa))          |
| Kogutulu      | SUMMA (Brutokasum / (müügitulu - käibemaksu (sisaldub kliendi arve rea summa)))             |
| Eelmise aasta tulu | Tulu eelmise aasta = Arvuta (summa (ridade arveldamiseks\[tulu\]), SAMEPERIODLASTYEAR (kuupäevad\[alates\]) |

Järgmisi olulisi mõõtmed on **müük kuubi** viil on suurem granulaarsus ja sügavama analüüsi pilgu kokku mõõtmised filtritena kasutatakse.

|                  |                                                      |
|------------------|------------------------------------------------------|
| **Entity**       | **Näited atribuutidest**                           |
| Kliendid        | Kliendirühmad, kliendi piirkonnad, aadress, tööstuse |
| Tooted         | Toote number, toote nimi, rühma nimi       |
| Müügikategooriad | Müük kategooria nimed                                 |
| Juriidilised isikud   | Juriidilise isiku nimed                                   |
| Kuupäevad            | Kuupäevad                                                |

Vaikimisi sisu pakendi kuvatakse andmed kalendriaasta, kuid saate avada aruande filtrite sektsiooni ja Kuupäevafilter. Saate muuta ettevõtte filter.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)



