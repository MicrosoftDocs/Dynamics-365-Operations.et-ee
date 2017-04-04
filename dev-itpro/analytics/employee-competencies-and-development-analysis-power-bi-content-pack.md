---
title: "Töötajate pädevus ja arengu Power BI sisu"
description: "Teema käsitleb Dynamics 365 toiminguteks - töötaja pädevus ja arengu Power BI sisu. Ta selgitab, kuidas on võimalik saada aruandeid, mis on kaasatud sisu pack ja andmemudel ja üksuste, ehitada sisu pakendi kasutatud teavet."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>Töötajate pädevus ja arengu Power BI sisu

Teema käsitleb Dynamics 365 toiminguteks - töötaja pädevus ja arengu Power BI sisu. Ta selgitab, kuidas on võimalik saada aruandeid, mis on kaasatud sisu pack ja andmemudel ja üksuste, ehitada sisu pakendi kasutatud teavet.

<a name="accessing-the-content-pack"></a>Juurdepääsu sisu pakendi
--------------------------

Leidmiseks töötaja pädevust ja arengu sisu pack jagatud varade teegi in Microsoft Dynamics elutsükli teenused (LCS). Lae sisu pakendi ja ühendada oma Microsoft Dynamics 365 toimingute andmete kohta lisateabe saamiseks vt [Power BI sisu LCS Microsofti ja oma partnerite](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Aruanded, mis on kaasatud sisu pack
Pärast sisu pakendi oma Dynamics 365 toimingute andmed, aruannetest nähtub teie ettevõtte andmeid. Kui te pole varem Microsoft Power BI enne, saab õppida rohkem sellest on [juhindub õppe lehekülg Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Aruanded, mis on kaasatud sisu pack on graafikuid ja tabeleid, mis sisaldavad täiendavat teavet. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                            | Sisu                                               |
|-----------------------------------|--------------------------------------------------------|
| Pädevusvaldkonna ja arengu analüüs | Meeskonna liige oskuste tüübid ja meeskonna liige oskused tüübi järgi |
| Oskuste reeglid                     | Valitud töötaja oskuste reeglid                |
| Oskuste analüüs                    | Oskuste tüüpide ja reiting                              |

Saate filtreerida diagrammid ja plaadid aruannete ja diagrammide ja plaadid armatuurlauale kinnitada. Filter ja Power BI pin kohta lisateabe saamiseks vt [loomine ja konfigureerimine armatuurlaua](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Toimingute andmed Dynamics 365 saab asustada aruanded töötajate pädevust ja arengu sisu pakendi. Järgmine tabel näitab üksuste sisu pakendi põhines.

| Üksus                            | Sisu                                                                                                   | Suhted ka teiste                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tööjõu\_CalendarOffset         | Kalendri tasakaalustab viil aruanded                                                                          |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_firma                | Ettevõtete poolt aruannete filtreerimiseks                                                                             |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_hüvitist           | Töötasu määr ja sagedus aja jooksul                                                                           |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_CurrentCompensation    | Töötasu määr ja sagedus jooksva kuupäeva seisuga                                                              | Tööjõu\_firma tööjõu\_CurrentCompensation tööjõu\_demograafia tööjõu\_töö tööjõu\_asendis                                                                                                                                                                                            |
| Tööjõu\_CurrentPosition        | Praeguse kuupäeva, täiskoha ekvivalent (taandatuna Täistööajale), avatud positsioonide ja avatud täidetud seisukohad seisukohad | Tööjõu\_töö tööjõu\_asendis                                                                                                                                                                                                                                                                      |
| Tööjõu\_CurrentWorker          | Töötajate praeguse kuupäeva, vanus ja töötajate arv                                                         | Tööjõu\_firma tööjõu\_hüvitist töötajate\_GeographicLocation tööjõu\_tulemuslikkuse tööjõu\_PersonSkill tööjõu\_WorkerName tööjõu\_ReportsToWorkerName tööjõu\_WorkerTitle tööjõu\_demograafia tööjõu\_töö tööjõu\_tööhõive tööjõu\_asendis                     |
| Tööjõu\_kuupäev                   | Päeva, nädala, kuu ja aasta                                                                             |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_demograafia           | Sünniaeg, soo, etnilise päritolu ja Perekonnaseis                                                   |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_tööhõive             | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                                                                  |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_GeographicLocation     | Linn, maakond, postiindeks kood ja maakond                                                           |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_töö                    | Funktsiooni, tüüp ja tiitel                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_JobPreferredSkill      | Tähtsust, reiting, oskusi ja oskuste tase                                                                 | Tööjõu\_oskus tööjõu\_töö                                                                                                                                                                                                                                                                         |
| Tööjõu\_PastPositionAssignment | Määramise põhjus, alguskuupäev, lõppkuupäev ja töö                                                           | Tööjõu\_ClaendarOffset tööjõu\_kuupäev tööjõu\_töö tööjõu\_asendis                                                                                                                                                                                                                            |
| Tööjõu\_täitmise            | Hinnang, kirjeldus ja hinnang mudel                                                                      |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_PersonSkill            | Oskuste taseme ja taseme kuupäev                                                                               | Tööjõu\_oskus                                                                                                                                                                                                                                                                                        |
| Tööjõu\_PersonSkillAnalysis    | Sertifitseeritud, taseme, taseme kuupäev ja oskus                                                                    | Tööjõu\_WorkerName tööjõu\_oskus                                                                                                                                                                                                                                                                  |
| Tööjõu\_asendis               | Osakond, Täistööajale, seisundit, positsiooni tüüp ja pealkiri                                                        |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_PositionTrend          | Positsiooni, Täistööajale, ja töötajate                                                                          | Tööjõu\_CalendarOffset tööjõu\_kuupäev tööjõu\_töö tööjõu\_asendis                                                                                                                                                                                                                            |
| Tööjõu\_ReportsToWorkerName    | Eesnimi, perekonnanimi ja täisnimi                                                                       |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_oskus                  | Oskus, oskused ja hinnang                                                                              |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_TerminatedWorker       | Lõpetada töötajate, lõpetamise kuupäev, nimetus, paigutus ja töö                                             | Tööjõu\_firma tööjõu\_hüvitist töötajate\_GeographicLocation tööjõu\_tulemuslikkuse tööjõu\_WorkerName tööjõu\_ReportsToWorkerName tööjõu\_CalendarOffset personali\_kuupäev tööjõu\_WorkerTitle tööjõu\_demograafia tööjõu\_tööhõive tööjõu\_töö tööjõu\_seisukoht |
| Tööjõu\_WorkerName             | Eesnimi, perekonnanimi ja täisnimi                                                                       |                                                                                                                                                                                                                                                                                                         |
| Tööjõu\_WorkerTitle            | Pealkiri ja staažist                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | Aeg, töötajate arv, ettevõtte ja asukoha üle                                                        | Tööjõu\_firma tööjõu\_hüvitist töötajate\_GeographicLocation tööjõu\_tulemuslikkuse tööjõu\_WorkerName tööjõu\_ReportsToWorkerName tööjõu\_CalendarOffset personali\_kuupäev tööjõu\_WorkerTitle tööjõu\_demograafia tööjõu\_tööhõive tööjõu\_töö                     |

Need üksused olid saab luua arvutatud mõõtmeid andmemudel. Need arvutatakse meetmed seejärel kasutatakse tulemuslikkuse võtmenäitajate (KPI) ja aruanded, mida kasutatakse sisu Pack. Kui soovite kaasata edasiste arvutuste aruanded ja armatuurlaud, saate alla laadida ja muuta LCS CompetenciesandDevelopment.pbix faili. See fail on vaikimisi andmemudel, kust luua sisu pakendi. Kui olete teinud muudatusi, saate luua organisatsiooni sisu pakendi ja armatuurlaud, mis sisaldab lisatud teavet.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



