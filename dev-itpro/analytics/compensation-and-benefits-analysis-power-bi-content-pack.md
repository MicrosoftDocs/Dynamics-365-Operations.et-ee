---
title: "Hüvitist ja hüvitiste Power BI"
description: "Teema käsitleb Dynamics 365 toiminguteks - hüvitist ja hüvitiste Power BI sisu. Ta selgitab, kuidas on võimalik saada aruandeid, mis on kaasatud sisu pack ja andmemudel ja üksuste, ehitada sisu pakendi kasutatud teavet."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 557f9218032e2b1160b6ea0631ada951353d2afd
ms.lasthandoff: 03/31/2017


---

# <a name="compensation-and-benefits-power-bi-content"></a>Hüvitist ja hüvitiste Power BI

Teema käsitleb Dynamics 365 toiminguteks - hüvitist ja hüvitiste Power BI sisu. Ta selgitab, kuidas on võimalik saada aruandeid, mis on kaasatud sisu pack ja andmemudel ja üksuste, ehitada sisu pakendi kasutatud teavet.

<a name="accessing-the-content-pack"></a>Juurdepääsu sisu pakendi
--------------------------

Kompensatsioonide ja toetuste sisu pakendi leiad jagatud varade teegi in Microsoft Dynamics elutsükli teenused (LCS). Lae sisu pakendi ja ühendada oma Microsoft Dynamics 365 toimingute andmete kohta lisateabe saamiseks vt [Power BI sisu LCS Microsofti ja oma partnerite](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Aruanded, mis on kaasatud sisu pack
Pärast sisu pakendi oma Dynamics 365 toimingute andmed, aruannetest nähtub teie ettevõtte andmeid. Kui te pole varem Microsoft Power BI enne, saab õppida rohkem sellest on [juhindub õppe lehekülg Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Aruanded, mis on kaasatud sisu pack on graafikuid ja tabeleid, mis sisaldavad täiendavat teavet. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                     | Sisu                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Comp ja kasu analüüs | Ühe tunni ja palgalistel töötajad ettevõtte Keskmine tunnitasu, palgaline Keskmine palk, töötajate tööhõive tüübi järgi ja kava registreerimine |
| Hüvitised töötajatele          | Töötaja registreerimine valitud kasuga                                                                                               |

Saate filtreerida diagrammid ja plaadid aruannete ja diagrammide ja plaadid armatuurlauale kinnitada. Filter ja Power BI pin kohta lisateabe saamiseks vt [loomine ja konfigureerimine armatuurlaua](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Toimingute andmed Dynamics 365 saab asustada kompensatsioonide ja toetuste sisu Pack aruanded. Järgmine tabel näitab üksuste sisu pakendi põhines.

| Üksus                            | Sisu                                                                                                   | Suhted ka teiste                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tööjõu\_CalendarOffset         | Kalendri tasakaalustab viil aruanded                                                                          | Tööjõu\_PastPositionAssignment tööjõu\_PositionTrend Workorce\_WorkerTrend tööjõu\_TerminatedWorker                                                                                                                                                                                                                     |
| Tööjõu\_firma                | Ettevõtete poolt aruannete filtreerimiseks                                                                             | Tööjõu\_CurrentCompensation tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Tööjõu\_hüvitist           | Töötasu määr ja sagedus aja jooksul                                                                           | Tööjõu\_CurrentCompensation tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Tööjõu\_CurrentCompensation    | Töötasu määr ja sagedus jooksva kuupäeva seisuga                                                              | Tööjõu\_firma tööjõu\_hüvitist tööjõu\_demograafia tööjõu\_töö tööjõu\_asendis                                                                                                                                                                                                                            |
| Tööjõu\_CurrentPosition        | Praeguse kuupäeva, täiskoha ekvivalent (taandatuna Täistööajale), avatud positsioonide ja avatud täidetud seisukohad seisukohad | Tööjõu\_töö tööjõu\_asendis                                                                                                                                                                                                                                                                                               |
| Tööjõu\_CurrentWorker          | Töötajate praeguse kuupäeva, vanus ja töötajate arv                                                         | Tööjõu\_firma tööjõu\_hüvitist töötajate\_GeographicLocation tööjõu\_täitmise tööjõu\_WorkerName tööjõu\_ReportsToWorkerName tööjõu\_WorkerTitle tööjõu\_demograafia tööjõu\_töö tööjõu\_tööhõive tööjõu\_paigutada tööjõu\_WorkerBenefit                                            |
| Tööjõu\_kuupäev                   | Päeva, nädala, kuu ja aasta                                                                             | Tööjõu\_PastPositionAssignment tööjõu\_PositionTrend tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Tööjõu\_demograafia           | Sünniaeg, soo, etnilise päritolu ja Perekonnaseis                                                   | Tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõu\_tööhõive             | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                                                                  | Tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõu\_GeographicLocation     | Linn, maakond, postiindeks kood ja maakond                                                           | Tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõu\_töö                    | Funktsiooni, tüüp ja tiitel                                                                                  | Tööjõu\_CurrentPosition tööjõu\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Tööjõu\_PastPositionAssignment | Määramise põhjus, alguskuupäev, lõppkuupäev ja töö                                                           | Tööjõu\_CalendarOffset tööjõu\_kuupäev tööjõu\_töö tööjõu\_asendis                                                                                                                                                                                                                                                     |
| Tööjõu\_täitmise            | Hinnang, kirjeldus ja hinnang mudel                                                                      | Tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõu\_asendis               | Osakond, Täistööajale, seisundit, positsiooni tüüp ja pealkiri                                                        | Tööjõu\_CurrentPosition tööjõu\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Tööjõu\_PositionTrend          | Positsiooni, Täistööajale, ja töötajate                                                                          | Tööjõu\_CalendarOffset tööjõu\_kuupäev tööjõu\_töö tööjõu\_asendis                                                                                                                                                                                                                                                     |
| Tööjõu\_ReportsToWorkerName    | Eesnimi, perekonnanimi ja täisnimi                                                                       | Tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõu\_oskus                  | Oskus, oskused ja hinnang                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Tööjõu\_TerminatedWorker       | Lõpetada töötajate, lõpetamise kuupäev, nimetus, paigutus ja töö                                             | Tööjõu\_firma tööjõu\_hüvitist töötajate\_GeographicLocation tööjõu\_tulemuslikkuse tööjõu\_WorkerName tööjõu\_ReportsToWorkerName tööjõu\_CalendarOffset personali\_kuupäev tööjõu\_WorkerTitle tööjõu\_demograafia tööjõu\_tööhõive tööjõu\_töö tööjõu\_paigutada tööjõu\_WorkerBenefit |
| Tööjõu\_WorkerBenefit          | Jõustumise kuupäeva, kasu võimalus, plaani ja kasu tüüp                                             | Tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõu\_WorkerName             | Eesnimi, perekonnanimi ja täisnimi                                                                       | Tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõu\_WorkerTitle            | Pealkiri ja staažist                                                                                   | Tööjõu\_CurrentWorker tööjõu\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | Aeg, töötajate arv, ettevõtte ja asukoha üle                                                        | Tööjõu\_firma tööjõu\_hüvitist töötajate\_GeographicLocation tööjõu\_tulemuslikkuse tööjõu\_WorkerName tööjõu\_ReportsToWorkerName tööjõu\_CalendarOffset personali\_kuupäev tööjõu\_WorkerTitle tööjõu\_demograafia tööjõu\_tööhõive tööjõu\_töö tööjõu\_WorkerBenefit                     |

Need üksused olid saab luua arvutatud mõõtmeid andmemudel. Need arvutatakse meetmed seejärel kasutatakse tulemuslikkuse võtmenäitajate (KPI) ja aruanded, mida kasutatakse sisu Pack. Kui soovite kaasata edasiste arvutuste aruanded ja armatuurlaud, saate alla laadida ja muuta LCS CompensationandBenefits.pbix faili. See fail on vaikimisi andmemudel, kust luua sisu pakendi. Kui olete teinud muudatusi, saate luua organisatsiooni sisu pakendi ja armatuurlaud, mis sisaldab lisatud teavet.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



