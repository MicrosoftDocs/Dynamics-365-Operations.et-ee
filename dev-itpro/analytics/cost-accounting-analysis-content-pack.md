---
title: "Kuluarvestuse analüüs Power BI sisu"
description: "Selles teemas kirjeldatakse, mis kaasatakse kuluarvestuse analüüsi Power BI sisu. Ta selgitab, kuidas on võimalik saada Power BI aruanded ja andmemudel ja üksuste sisu loomiseks kasutatud teavet."
author: YuyuScheller
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 50e7bd92ee693f59fd013226aee22bd1a54c81e2
ms.lasthandoff: 03/31/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kuluarvestuse analüüs Power BI sisu

Selles teemas kirjeldatakse, mis kaasatakse kuluarvestuse analüüsi Power BI sisu. Ta selgitab, kuidas on võimalik saada Power BI aruanded ja andmemudel ja üksuste sisu loomiseks kasutatud teavet.

<a name="overview"></a>Ülevaade
--------

Selle **kuluarvestuse analüüs** Microsoft Power BI sisu on mõeldud eest vastutav töötleja või keegi, kes on tegemise kulude kontrolli organisatsiooni. See sisaldab võtmemõõdikute kulu, ulatuse ja määra poolt tegelikud kulud, eelarvekulud ja paindliku eelarve kulud. See kasutab kuluarvestuse tehingu andmeid Microsoft Dynamics 365 toiminguteks ning kulud kokku ülevaate ette kogu organisatsiooni ühe aruandevaluutas. Juhtide saate filtreerida andmeid kuluobjektiks täida kulude kontrolli oma organisatsioonilised üksused, isegi kui organisatsioon võib olla mitu õigussubjekti. Sest on **kuluarvestuse analüüs** Power BI sisu toob esile tegelikud kulud ja planeeritud kulud, erinevused juhid saaksid teatada positiivsete ja negatiivsete suundumuste kohta nende üksuste jaoks. Juhtide saab minna süvitsi kulude element hierarhiate või kuluelementide saada detailne ülevaade kuidas kulude erinevused tekkinud, ning seejärel võtta tõhusaid meetmeid. Selle **kuluarvestuse analüüs** Power BI sisu, let's kulu raamatupidajate analüüsida, kuidas maksumus voolab läbi kogu organisatsiooni kuluobjektiks. Kuluarvestuse kohta lisateabe saamiseks vaadake [kuluarvestuse kodulehekülg](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page.md). Määratledes juurdepääsu tasemel turvalisust kuluarvestuse ja kombineerides selle rea tasandil turvalisuse Power BI, saab anda kõik kulu objekti omanikud juurdepääsu ning **kuluarvestuse analüüs** Power BI sisu. Kõigi andmete visualiseerimine siis filtreeritakse vastavalt juurdepääsu tase, mida juhitakse kuluarvestuse kohta. Juurdepääsu tase Turvalisus ja rea tasandil turvalisuse kohta lisateabe saamiseks vt [seadnud turvasätted kuluarvestuse sisu Power BI](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Power BI infosisu
Leiad selle **kuluarvestuse analüüs** Power BI sisu jagatud varade teegi in Microsoft Dynamics elutsükli teenused (LCS). Sisu alla laadida ja ühendada oma Dynamics 365 toimingute andmete kohta lisateabe saamiseks vt [Power BI sisu LCS Microsofti ja oma partnerite](power-bi-content-microsoft-partners.md). **Märkus:** KB4011327 ** ** eelduseks on **kuluarvestuse analüüs** Power BI sisu.  Kui logite elutsükli teenuseid, on teil juurdepääs KB siin: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mõõdikud, mis sisalduvad Power BI sisu
Sisu hõlmab aruanne lehtede komplektist. Iga lehekülg koosneb parameetrid, mis on näitlikustada diagrammid, plaadid ja tabelid. Järgnev tabel annab ülevaate visualiseeringuid ja selle **kuluarvestuse analüüs** Power BI sisu.

| Aruanne lehekülg                      | Diagramm                                                                                                                         | Paan                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kulude jälgimine fiskaalperioodide lõikes    | Tegelike kulude ja eelarve kulude poolt kulude element hierarhia tase                                                                   | Tegelik kulu vs eelarve kulu                    |
|                                  | Eelarve erinevus kulud element hierarhia tase                                                                               | Tegelik kulu määr vs eelarve kulukuse määr          |
|                                  | Top 10 eelarve erinevus protsentides kuluelement                                                                          | Tegelik suurus vs eelarve suurus          |
| Kulude jälgimine kuupäeva aasta võrra     | Tegelike kulude ja eelarve kulude poolt kalendriaasta jooksul                                                                           | Tegelik kulu vs eelarve kulu                    |
|                                  | Eelarve erinevus poolt kalendriaasta jooksul                                                                                       | Tegelik kulu määr vs eelarve kulukuse määr          |
|                                  | Top 10 eelarve erinevus protsentides kuluelement                                                                          | Tegelik suurus vs eelarve suurus          |
| Finantsaasta alusel kulumäär         | Tegelik kulumäär kulude käitumist                                                                                             | Tegelik kulu määr vs eelarve kulukuse määr          |
|                                  | Tegelik kulumäär eelarve kulude määra erinevus, eelarve kulude määra võrra ja eelarve määra kulu element hierarhia tase | Tegelik suurus vs eelarve suurus          |
|                                  | Eelarve erinevus kulud element hierarhia tase                                                                               |                                               |
|                                  | Top 10 eelarve erinevus protsentides kuluelement                                                                          |                                               |
| Paindliku eelarve fiskaalperioodide lõikes | Tegelikud kulud, eelarvekulud ja paindliku eelarve kulud kulude element hierarhia tase                                             | Tegelik suurus vs eelarve suurus          |
|                                  | Eelarve erinevus ja paindliku eelarve erinevus kulud element hierarhia tase                                                  | Tegelik kulu vs paindliku eelarve kulud           |
|                                  | Tegelikud kulud, eelarvekulud ja paindliku hind poolt käitumine ja kulude element hierarhia tase                                  | Tegelik määr vs paindliku eelarve kulude määra |
| Kuluaruanne fiskaalperioodide lõikes  | Tegelik kulu kulude element hierarhia tase ja hind objekti dimensioon liikme nimi                                             |                                               |
|                                  | Tegelik kulu kulud dimensiooni liige objektinimi ja kulude element dimensioon liikme nimi                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Toimingute andmed Dynamics 365 saab täita aruande lehed on **kuluarvestuse analüüs** Power BI sisu. Need andmed esitatakse arvuna kokku mõõtmised, mis on lavastatud olem poest, mis on Microsoft SQL andmebaasi, mis on optimeeritud analytics. Lisateabe saamiseks vaadake [ülevaade Power BI Integratsioon üksus poe](power-bi-integration-entity-store.md). Aluse sisu kasutatakse järgmisi peamisi kokku mõõtmisi.

| Üksus                  | Kogu hindamise | Dynamics 365 operatsioonide jaoks | Väli     | Kirjeldus                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Kuluarvestuse kanded | SUM(amount)               | CAMDATAAggregatedCostEntry                  | Summa    | Summa valuutas kuluarvestuse pearaamatu |
| Statistilised kirjed     | SUM(Magnitude)            | CAMDATAAggregatedStatisctialEntry           | Väärtus |                                               |

Järgmises tabelis on kokku peamised mõõtmised kasutamise luua mitu arvutatud mõõtmeid sisu andmekogumis.

| Mõõt                                       | Meetme arvutamine                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Tegelik kulu                                   | Arvuta ("kuluarvestuse kanded"\[meede\], "Tehingu versiooni"\[ISSOURCEVERSIONBUDGET\_VÄÄRTUST\] = 0)            |
| Eelarvekulu                                   | Arvuta ("kuluarvestuse kanded"\[meede\], "Tehingu versiooni"\[ISSOURCEVERSIONBUDGET\_VÄÄRTUST\] = 1)            |
| Eelarve kulude erinevus                          | \[Eelarve kulu\] - \[tegelik kulu\]                                                                                      |
| Eelarve erinevuse protsent                    | IF (\[eelarve kulu\] = 0, blank(), \[eelarve dispersioon\] / \[eelarve kulu\])                                                |
| Tegelik suurus                              | Arvuta (statistilised kirjed\[FullMagnitude\], "Tehingu versiooni"\[ISSOURCEVERSIONBUDGET\_VÄÄRTUST\] = 0)          |
| Eelarve suurus                              | Arvuta (\[FullMagnitude\], "Tehingu versiooni"\[ISSOURCEVERSIONBUDGET\_VÄÄRTUST\] = 1)                               |
| Statistilise eelarve erinevus                   | \[Eelarve suuruse\] - \[tegelik suurus\]                                                                            |
| Statistilise eelarve erinevuse protsent        | IF (\[eelarve suuruse\] = 0, blank(), \[statistilise eelarve dispersioon\] / \[eelarve suuruse\])                          |
| Tegelik kulumäär                              | IF (\[tegelik ulatust\] = 0, BLANK(), \[tegelik kulu\] / \[tegelik suurus\])                                          |
| Eelarve kulumäär                              | IF (\[eelarve suuruse\] = 0, BLANK(), \[eelarve kulu\] / \[eelarve suuruse\])                                          |
| Eelarve kulude määra erinevus                     | \[Eelarve määra\] - \[tegelik kulumäär\]                                                                            |
| Eelarve kulude Määra erinevuse protsent          | IF (\[eelarve kulu\] = 0, blank(), \[eelarve maksumuse määra erinevus\] / \[eelarve määra\])                                 |
| Fikseeritud eelarve kulu                             | Arvuta (\[eelarve kulu\], "Kuluarvestuse kanded"\[COSTBEHAVIOR\] = 1)                                              |
| Muutuva eelarve kulu                          | Arvuta (\[eelarve kulu\], "Kuluarvestuse kanded"\[COSTBEHAVIOR\] = 2)                                              |
| Fikseeritud paindliku eelarve kulud                    | \[Fikseeritud eelarve kulu\]                                                                                                  |
| Muutuva paindliku eelarve kulud                 | IF (\[eelarve suuruse\] = 0, BLANK(), (\[muutuva eelarve kulu\] / \[eelarve suuruse\]) \*\[tegelik suurus\])       |
| Paindliku eelarve kulud                          | \[Fikseeritud paindliku eelarve kulud\] + \[muutuva paindliku eelarve kulud\]                                                     |
| Paindliku eelarve erinevus                      | \[Paindliku eelarve kulud\] - \[tegelik kulu\]                                                                             |
| Paindliku eelarve erinevuse protsent           | IF (\[paindliku eelarve kulud\] = 0, BLANK(), \[paindlik eelarve dispersioon\] / \[paindliku eelarve kulud\])                     |
| Paindliku eelarve kulu määr                     | IF (\[tegelik ulatust\] = 0, BLANK(), \[paindliku eelarve kulud\] / \[tegelik suurus\])                                 |
| Paindliku eelarve kulude määra erinevus            | \[Paindliku eelarve määra\] - \[tegelik kulumäär\]                                                                   |
| Paindliku eelarve kulude Määra erinevuse protsent | IF (\[Paindlik eelarve määra\] = 0, BLANK(), \[paindliku eelarve maksumuse määra erinevus\] / \[Paindlik eelarve määra\]) |

Filtritena kasutatakse järgmisi peamisi näitajaid viil kokku mõõtmistel saavutada suurem granulaarsus ja annavad põhjalikuma analüüsi ülevaate.

| Üksus                             | Näited atribuutidest                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Kuluarvestuse pearaamatud            | Kuluarvestuse pearaamat                                                                                               |
| Kulujuhtseadmed                 | Kulujuhtseadme nimi                                                                                               |
| Kuluelemendi dimensioonid            | Kulude elemendid dimensiooni nimi, kulude element dimensioon liikme nimi, kulude element dimensiooni liige kirjeldus          |
| Kuluobjekti dimensioonid             | Kulu objekt dimensiooni nimi, kulu objekti dimensioon liikme nimi, kulu objekti dimensiooni liige kirjeldus              |
| Statistilised dimensioonid             | Statistilise dimensiooni nimi, statistilise dimensioon liikme nimi, statistilise dimensiooni liige kirjeldus              |
| Kulu objekt dimensioonihierarhiate  | Kulu objekt dimensiooni hierarhia nimi, kulu objekti dimensioonide hierarhia tase, kulu objekti dimensiooni Rakendushierarhia puu    |
| Kuluelemendi dimensioonihierarhiate | Kulu element dimensiooni hierarhia nimi, kulu element dimensiooni hierarhia tase, kulude element dimensiooni Rakendushierarhia puu |
| Statistilise dimensioonihierarhiate  | Statistilise dimensiooni hierarhia nimi, statistilise dimensiooni hierarhia tase, statistilise dimensiooni Rakendushierarhia puu    |
| Kande versioonid               | Versiooni nimi                                                                                                         |
| Rahandussaasta kalendrid                   | Kalender, kalender kirjeldus                                                                                       |
| Eelarveaasta                       | Kalendriaasta                                                                                                        |
| Rahandusperioodid                     | Kalendriaasta jooksul                                                                                                 |

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)
-   [Power BI kuluarvestuse sisu turvalisuse seadistamine](setup-security-cost-accounting-content-pack.md)


