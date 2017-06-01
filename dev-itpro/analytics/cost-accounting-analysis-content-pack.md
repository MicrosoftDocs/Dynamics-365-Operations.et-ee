---
title: "Kuluarvestuse analüüsi Power BI sisu"
description: "See teema kirjeldab, mida hõlmab kuluarvestuse analüüsi Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5ce75a6145bde4a8c33ed785c7d2a60a52416676
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kuluarvestuse analüüsi Power BI sisu

[!include[banner](../includes/banner.md)]


See teema kirjeldab, mida hõlmab kuluarvestuse analüüsi Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

<a name="overview"></a>Ülevaade
--------

**Kuluarvestuse analüüsi** Microsoft Power BI sisu on mõeldud kulul kontrollijatele või organisatsioonis kulujuhtimise eest vastutavatele isikutele. See hõlmab põhimõõdikuid, nagu kulu, väärtus ja kulumäär tegeliku kulu, eelarvekulu ja paindliku eelarvekulu alusel. See kasutab kandeandmeid Microsoft Dynamics 365 for Operationsi kuluarvestusest ja annab koondvaate kogu organisatsiooni kuludest ühes aruandlusvaluutas. Haldajad saavad andmeid filtreerida kuluobjektide alusel oma organisatsiooniüksuste kulujuhtimiseks, isegi kui organisatsioonil on mitu juriidilist isikut. Kuna **kuluarvestuse analüüsi** Power BI sisu tõstab esile hälbed tegelike ja eelarvestatud kulude vahel, saab haldajaid teavitada nende tootmisüksuse positiivsetest ja negatiivsetest trendidest. Haldajatel on võimalik kuluelementide hierarhiaid või üksikuid kuluelemente sügavuti uurida, et saada põhjalik ülevaade kuluhälvete tekkimisest ja rakendada asjakohaseid meetmeid. **Kuluarvestuse analüüsi** Power BI sisu võimaldab kuluarvestajatel analüüsida kulude voogu läbi kogu organisatsiooni kuluobjektide. Lisateavet kuluarvestuse kohta vt teemast [Kuluarvestuse koduleht](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page). Määratledes juurdepääsutasemel turvalisuse kuluarvestuses ja kombineerides selle reatasemel turvalisusega Power BI-s, saate anda kõigile kuluobjektide omanikele juurdepääsu **kuluarvestuse analüüsi** Power BI sisule. Kõik andmed visualisatsioonis filtreeritakse seejärel kuluarvestuses juhitava juurdepääsutaseme alusel. Lisateavet juurdepääsutasemel turvalisuse ja reatasemel turvalisuse kohta vt teemast [Turbe seadistamine kuluarvestuse sisu jaoks Power BI puhul](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Kuluarvestuse analüüsi** Power BI sisu leiate teenuste Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegist. Lisateavet sisu allalaadimise ja selle ühendamise kohta Microsoft Dynamics 365 for Operationsi andmetega vt teemast [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md). 

> Märkus. **KB4011327** on selle Power BI sisu eeltingimus. Pärast elutsükli teenustesse sisselogimist pääsete teabebaasiartiklile juurde siin:<https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad mõõdikud
Sisu hõlmab aruandelehtede komplekti. Iga leht koosneb mõõdikute komplektist, mida visualiseeritakse diagrammide, paanide ja tabelitena. Järgmine tabel annab ülevaate **kuluarvestuse analüüsi** Power BI sisu visualiseerimistest.

| Aruandeleht                      | Diagramm                                                                                                                         | Paan                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kulujuhtimine rahandusperioodi alusel    | Tegelik kulu ja eelarvekulu kuluelemendi hierarhiataseme alusel                                                                   | Tegelik kulu vs eelarvekulu                    |
|                                  | Eelarvehälve kuluelemendi hierarhiataseme alusel                                                                               | Tegeliku kulu määr vs eelarvekulu määr          |
|                                  | 10 peamist eelarvehälvet protsentides kuluelemendi alusel                                                                          | Tegelik väärtus vs eelarveväärtus          |
| Kulujuhtimine aasta tänaseni alusel     | Tegelik kulu ja eelarvekulu kalendriaasta perioodi alusel                                                                           | Tegelik kulu vs eelarvekulu                    |
|                                  | Eelarvehälve kalendriaasta perioodi alusel                                                                                       | Tegeliku kulu määr vs eelarvekulu määr          |
|                                  | 10 peamist eelarvehälvet protsentides kuluelemendi alusel                                                                          | Tegelik väärtus vs eelarveväärtus          |
| Kulumäär finantsaasta alusel         | Tegeliku kulu määr kulukäitumise alusel                                                                                             | Tegeliku kulu määr vs eelarvekulu määr          |
|                                  | Tegeliku kulu määr, eelarve kulumäära hälve, eelarve kulumäära protsent ja eelarve kulumäär kuluelemendi hierarhiataseme alusel | Tegelik väärtus vs eelarveväärtus          |
|                                  | Eelarvehälve kuluelemendi hierarhiataseme alusel                                                                               |                                               |
|                                  | 10 peamist eelarvehälvet protsentides kuluelemendi alusel                                                                          |                                               |
| Paindlik eelarve rahandusperioodi alusel | Tegelik kulu, eelarvekulu ja paindlik eelarvekulu kuluelemendi hierarhiataseme alusel                                             | Tegelik väärtus vs eelarveväärtus          |
|                                  | Eelarvehälve ja paindlik eelarvehälve kuluelemendi hierarhiataseme alusel                                                  | Tegelik kulu vs paindlik eelarvekulu           |
|                                  | Tegelik kulu, eelarvekulu ja paindlik eelarvekulu kulukäitumise ning kuluelemendi hierarhiataseme alusel                                  | Tegeliku kulu määr vs paindliku eelarvekulu määr |
| Kuluaruanne rahandusperioodi alusel  | Tegelik kulu kuluelemendi hierarhiataseme ja kuluobjekti dimensiooniliikme nime alusel                                             |                                               |
|                                  | Tegelik kulu kuluobjekti dimensiooniliikme nime ja kuluelemendi dimensiooniliikme nime alusel                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Aruandelehtede täitmiseks **kuluarvestuse analüüsi** Power BI sisus kasutatakse Dynamics 365 for Operationsi andmeid. Need andmed esitatakse koondmõõtmistena, mis on koondatud üksuse kauplusse, mis on analüüsimiseks optimeeritud Microsoft SQL-i andmebaas. Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md). Sisu alusena kasutatakse järgmisi peamisi koondmõõtmisi.

| Üksus                  | Peamine koondmõõtmine | Dynamics 365 for Operationsi andmeallikas | Väli     | Kirjeldus                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Kuluarvestuse sisestused | SUM(Summa)               | CAMDATAAggregatedCostEntry                  | Summa    | Summa kuluarvestuse pearaamatu valuutas |
| Statistilised kirjed     | SUM(Väärtus)            | CAMDATAAggregatedStatisctialEntry           | Väärtus |                                               |

Järgmine tabel näitab, kuidas kasutatakse peamisi koondmõõtmisi mitme arvutatud meetme loomiseks sisu andmekogumis.

| Mõõt                                       | Meetme arvutamise viis                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Tegelik kulu                                   | CALCULATE('Kuluarvestuse sisestused'\[Meede\], 'Ülekandeversioonid'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)            |
| Eelarvekulu                                   | CALCULATE('Kuluarvestuse sisestused'\[Meede\], 'Ülekandeversioonid'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)            |
| Eelarvekulu hälve                          | \[Eelarvekulu\] - \[Tegelik kulu\]                                                                                      |
| Eelarvehälbe protsent                    | IF(\[Eelarvekulu\] = 0, blank(), \[Eelarvehälve\] / \[Eelarvekulu\])                                                |
| Tegelik väärtus                              | CALCULATE('Statistilised sisestused'\[FullMagnitude\], 'Ülekandeversioonid'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 0)          |
| Eelarveväärtus                              | CALCULATE(\[FullMagnitude\], 'Ülekandeversioonid'\[ISSOURCEVERSIONBUDGET\_VALUE\] = 1)                               |
| Statistiline eelarvehälve                   | \[Eelarveväärtus\] - \[Tegelik väärtus\]                                                                            |
| Statistilise eelarvehälbe protsent        | IF(\[Eelarveväärtus\] = 0, blank(), \[Statistiline eelarvehälve\] / \[Eelarveväärtus\])                          |
| Tegelik kulumäär                              | IF(\[Tegelik väärtus\] = 0, BLANK(), \[Tegelik kulu\] / \[Tegelik väärtus\])                                          |
| Eelarve kulumäär                              | IF(\[Eelarveväärtus\] = 0, BLANK(), \[Eelarvekulu\] / \[Eelarveväärtus\])                                          |
| Eelarve kulumäära hälve                     | \[Eelarve kulumäär\] - \[Tegelik kulumäär\]                                                                            |
| Eelarve kulumäära hälbe protsent          | IF(\[Eelarvekulu\] = 0, blank(), \[Eelarve kulumäära hälve\] / \[Eelarve kulumäär\])                                 |
| Fikseeritud eelarvekulu                             | CALCULATE(\[Eelarvekulu\], 'Kuluarvestuse sisestused'\[COSTBEHAVIOR\] = 1)                                              |
| Muutuv eelarvekulu                          | CALCULATE(\[Eelarvekulu\], 'Kuluarvestuse sisestused'\[COSTBEHAVIOR\] = 2)                                              |
| Fikseeritud paindlik eelarvekulu                    | \[Fikseeritud eelarvekulu\]                                                                                                  |
| Muutuv paindlik eelarvekulu                 | IF(\[Eelarveväärtus\] = 0, BLANK(), (\[Muutuv eelarvekulu\] / \[Eelarveväärtus\]) \* \[Tegelik väärtus\])       |
| Paindlik eelarvekulu                          | \[Fikseeritud paindlik eelarvekulu\] + \[Muutuv paindlik eelarvekulu\]                                                     |
| Paindlik eelarvehälve                      | \[Paindlik eelarvehälve\] - \[Tegelik kulu\]                                                                             |
| Paindliku eelarvehälbe protsent           | IF(\[Paindlik eelarvekulu\] = 0, BLANK(), \[Paindlik eelarvehälve\] / \[Paindlik eelarvekulu\])                     |
| Paindlik eelarve kulumäär                     | IF(\[Tegelik väärtus\] = 0, BLANK(), \[Paindlik eelarvekulu\] / \[Tegelik väärtus\])                                 |
| Paindliku eelarve kulumäära hälve            | \[Paindlik eelarve kulumäär\] - \[Tegelik kulumäär\]                                                                   |
| Paindliku eelarve kulumäära hälbe protsent | IF(\[Paindlik eelarve kulumäär\] = 0, BLANK(), \[Paindliku eelarve kulumäära hälve\] / \[Paindlik eelarve kulumäär\]) |

Järgmisi põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate andmiseks.

| Üksus                             | Atribuutide näited                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Kuluarvestuse pearaamatud            | Kuluarvestuse pearaamat                                                                                               |
| Kulujuhtseadmed                 | Kulujuhtseadme nimi                                                                                               |
| Kuluelemendi dimensioonid            | Kuluelementide dimensiooni nimi, kuluelemendi dimensiooniliikme nimi, kuluelemendi dimensiooniliikme kirjeldus          |
| Kuluobjekti dimensioonid             | Kuluobjektide dimensiooni nimi, kuluobjekti dimensiooniliikme nimi, kuluobjekti dimensiooniliikme kirjeldus              |
| Statistilised dimensioonid             | Statistilise dimensiooni nimi, statistilise dimensiooniliikme nimi, statistilise dimensiooniliikme kirjeldus              |
| Kuluobjektide dimensioonihierarhiad  | Kuluobjektide dimensioonihierarhia nimi, kuluobjekti dimensioonihierarhia tase, kuluobjekti dimensioonihierarhia puu    |
| Kuluelementide dimensioonihierarhiad | Kuluelementide dimensioonihierarhia nimi, kuluelemendi dimensioonihierarhia tase, kuluelemendi dimensioonihierarhia puu |
| Statistilised dimensioonihierarhiad  | Statistilise dimensioonihierarhia nimi, statistilise dimensioonihierarhia tase, statistilise dimensioonihierarhia puu    |
| Kande versioonid               | Versiooni nimi                                                                                                         |
| Rahandussaasta kalendrid                   | Kalender, kalendri kirjeldus                                                                                       |
| Finantsaastad                       | Kalendriaasta                                                                                                        |
| Rahandusperioodid                     | Kalendriaasta periood                                                                                                 |

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](..\data-entities\data-entities.md)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](configure-power-bi-integration.md)
-   [Kuluarvestuse sisu turbe seadistamine Power BI puhul](setup-security-cost-accounting-content-pack.md)




