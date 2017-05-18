---
title: Workforce Metrics Power BI sisu
description: "See teema kirjeldab Dynamics 365 for Operationsi – Workforce Metrics Power BI sisu. See selgitab juurdepääsu sisupaketis sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisupaketi loomiseks kasutati."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 351306857ae62496fb28e9bb55dcbb11e7c3fd00
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="workforce-metrics-power-bi-content"></a>Workforce Metrics Power BI sisu

[!include[banner](../includes/banner.md)]


See teema kirjeldab Dynamics 365 for Operationsi – Workforce Metrics Power BI sisu. See selgitab juurdepääsu sisupaketis sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisupaketi loomiseks kasutati.

<a name="accessing-the-content-pack"></a>Juurdepääs sisupaketile
--------------------------

Tööjõu mõõdikute sisupaketi leiate teenuste Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegist. Lisateavet sisupaketi allalaadimise ja selle ühendamise kohta Microsoft Dynamics 365 for Operationsi andmetega vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad aruanded
Pärast sisupaketi ühendamist Dynamics 365 for Operationsi andmetega näitavad aruanded teie organisatsiooni andmeid. Kui te pole Microsoft Power BI-d varem kasutanud, saate selle kohta lisateavet jaotisest [Power BI juhendatud õpe](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sisupaketti kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                                           | Sisu                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Headcount Analysis Company, osakond, asukoht | Töötajate arv ettevõtte, osakonna ja asukoha järgi ning töötajate koguarv.                                                                                                                           |
| Töötajate koguarvu analüüsitöö, etapp, juhataja            | Töötajate arv töökoha, etapi ja halduri järgi ning töötajate koguarv                                                                                                                                      |
| Töötajate koguarvu suundumuste analüüs                         | Töötajate koguarv sellel aastal vs eelmisel aastal ettevõtte järgi ja töötajate koondarv viimase 12 kuu kohta                                                                                                                        |
| Tööjõu demograafilised andmed                           | Töötajate arv vanuse ja soo, etnilise päritolu, veteranistaatuse ja perekonnaseisu järgi, täiskohaga õpilaste arv, keskmine ametiaeg, keskmine vanus ning naissoost ja meessoost töötajate suhe. |
| Ametikohaanalüüs                                | Avatud ametikohad osakonna järgi, täitmiseks avatud ametikohad, aktiivsed kuni mitteaktiivsed ametikohad ja ametikohad osakonna järgi                                                                                                   |
| Kinnipidamise analüüs                               | Kinnipidamine sellel aastal vs eelmisel aastal, kinnipidamine, lahkuvate inimeste keskmine ametiaeg, lahkuvate inimeste keskmine vanus ja töötajate lahkumise põhjus                                                                   |
| Inimesed osakonniti                             | Personalinumbriga töötajad osakonna, ametikoha ja määramise algus- ja lõppkuupäevade alusel                                                                                                                       |
| Staažianalüüs                               | Teenuse keskmised aastad ettevõtte ja staažiloendi alusel                                                                                                                                                              |
| Tähtpäevad ja töötamise aastad               | Töötajad tööaastate arvu ja aastapäevade alusel                                                                                                                                                                    |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Tööjõu mõõdikute sisupaketi aruannete täitmiseks kasutatakse Dynamics 365 for Operationsi andmeid. Järgmises tabelis on toodud sisupaketi aluseks olevad üksused.

| Üksus                            | Sisu                                                                                                   | Seosed teiste üksustega                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tööjõud\_CalendarOffset         | Kalendri tasakaalustused aruannete tükeldamiseks                                                                          | Tööjõud\_PastPositionAssignment Tööjõud\_PositionTrend Tööjõud\_WorkerTrend Tööjõud\_TerminatedWorker                                                                                                                                                                                                                     |
| Tööjõud\_Ettevõte                | Ettevõtted, mille alusel aruandeid filtreerida                                                                             | Tööjõud\_CurrentCompensation Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                        |
| Tööjõud\_Tasu           | Tasu määr ja sagedus aja jooksul                                                                           | Tööjõud\_CurrentCompensation Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                        |
| Tööjõud\_CurrentCompensation    | Tasu määr ja sagedus tänase kuupäeva seisuga                                                              | Tööjõud\_Ettevõte Tööjõud\_Hüvitis Tööjõud\_Demograafia Tööjõud\_Töö Tööjõud\_Ametikoht                                                                                                                                                                                                                            |
| Tööjõud\_CurrentPosition        | Ametikohad tänase kuupäeva seisuga, täistööaja ekvivalent (TTE), avatud ametikohad ja täitmiseks avatud ametikohad | Tööjõud\_Tööjõu töö\_Amet                                                                                                                                                                                                                                                                                               |
| Tööjõud\_CurrentWorker          | Töötajad tänase kuupäeva seisuga, vanus ja inimeste arv                                                         | Tööjõud\_Ettevõte Tööjõud\_Hüvitis Tööjõud\_GeographicLocation Tööjõud\_Tulemus Tööjõud\_WorkerName Tööjõud\_ReportsToWorkerName Tööjõud\_WorkerTitle Tööjõud\_Demograafia Tööjõud\_Töö Tööjõud\_Tööhõive Tööjõud\_Ametikoht Tööjõud\_WorkerBenefit                                            |
| Tööjõud\_Kuupäev                   | Päevad, nädalad, kuud ja aastad                                                                             | Tööjõud\_PastPositionAssignment Tööjõud\_PositionTrend Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                     |
| Tööjõud\_Demograafilised andmed           | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis                                                   | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_Töösuhe             | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                                                                  | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_GeographicLocation     | Linn, maakond, sihtnumber ja osariik või provints                                                           | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_Töö                    | Funktsioon, tüüp ja ametinimetus                                                                                  | Tööjõud\_CurrentPosition Tööjõud\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Tööjõud\_JobPerferredSkill      |                                                                                                            |                                                                                                                                                                                                                                                                                                                                  |
| Tööjõud\_PastPositionAssignment | Määramise põhjus, alguskuupäev, lõppkuupäev ja töö                                                           | Tööjõud\_CalendarOffset Tööjõud\_Kuupäev Tööjõud\_Töö Tööjõud\_Ametikoht                                                                                                                                                                                                                                                     |
| Tööjõud\_Tulemus            | Hinnang, kirjeldus ja hinnangumudel                                                                      | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_PersonSkill            | Tase ja oskus                                                                                            | Tööjõud\_Oskus                                                                                                                                                                                                                                                                                                                 |
| Tööjõud\_PersonSkillAnalysis    | Sertifitseeritud, tase ja oskus                                                                                | Tööjõud\_Tööjõu oskus\_WorkerName                                                                                                                                                                                                                                                                                           |
| Tööjõud\_Amet               | Osakond, TTE, ametikoht, ametikoha tüüp ja ametinimetus                                                        | Tööjõud\_CurrentPosition Tööjõud\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Tööjõud\_PositionTrend          | Ametikohad aja jooksul, TTE ja töö                                                                          | Tööjõud\_CalendarOffset Tööjõud\_Kuupäev Tööjõud\_Töö Tööjõud\_Ametikoht                                                                                                                                                                                                                                                     |
| Tööjõud\_ReportsToWorkerName    | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_Oskus                  | Oskus, oskuse tüüp ja hinnang                                                                              | Tööjõud\_PersonSkill Tööjõud\_PersonSkillAnalysis                                                                                                                                                                                                                                                                            |
| Tööjõud\_TerminatedWorker       | Lõpetatud lepinguga töötajad, lepingu lõpetamise kuupäev, ametinimetus, ametikoht ja töö                                             | Tööjõud\_Ettevõte Tööjõud\_Hüvitis Tööjõud\_GeographicLocation Tööjõud\_Tulemus Tööjõud\_WorkerName Tööjõud\_ReportsToWorkerName Tööjõud\_CalendarOffset Tööjõud\_Kuupäev Tööjõud\_WorkerTitle Tööjõud\_Demograafia Tööjõud\_Tööhõive Tööjõud\_Töö Tööjõud\_Ametikoht Tööjõud\_WorkerBenefit |
| Tööjõud\_WorkerBenefit          | Jõustumiskuupäev, eelise valik, eelise plaan ja eelise tüüp                                             | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_WorkerName             | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend Tööjõud\_PersonSkillAnalysis                                                                                                                                                                                                                        |
| Tööjõud\_WorkerTitle            | Ametinimetus ja staaži kuupäev                                                                                   | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_WorkerTrend             | Töötajad aja jooksul, inimeste arv, ettevõte ja ametikoht                                                        | Tööjõud\_Ettevõte Tööjõud\_Hüvitis Tööjõud\_GeographicLocation Tööjõud\_Tulemus Tööjõud\_WorkerName Tööjõud\_ReportsToWorkerName Tööjõud\_CalendarOffset Tööjõud\_Kuupäev Tööjõud\_WorkerTitle Tööjõud\_Demograafia Tööjõud\_Tööhõive Tööjõud\_Töö Tööjõud\_WorkerBenefit                     |

Neid olemeid kasutati arvutatud meetmete loomiseks andmemudelis. Seejärel kasutatakse neid arvutatud meetmeid sisupaketis kasutatavate tulemuslikkuse võtmenäitajate (KPI-d) ja aruannete arvutamiseks. Aruannetesse ja armatuurlauale täiendavate arvutuste lisamiseks võite laadida LCS-ist alla ja muuta faili CompensationandBenefits.pbix. See fail on vaikeandmemudel, mida kasutati sisupaketi loomiseks. Kui muudatused on tehtud, saate luua organisatsiooni sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





