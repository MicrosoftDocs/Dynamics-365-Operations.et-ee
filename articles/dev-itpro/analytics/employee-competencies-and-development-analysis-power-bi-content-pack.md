---
title: Töövõtja pädevuste ja arengu Power BI sisu
description: Teema kirjeldab Finance and Operationsi mooduli Töötaja pädevused ja areng Power BI sisu.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0442e795eadf28a07132c160d69ad44e9fb05eed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553273"
---
# <a name="employee-competencies-and-development-power-bi-content"></a>Töövõtja pädevuste ja arengu Power BI sisu

[!include [banner](../includes/banner.md)]

Teema kirjeldab Finance and Operationsi mooduli Töötaja pädevused ja areng Power BI sisu. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad aruanded
Pärast sisupaketi ühendamist Finance and Operationsi andmetega näitavad aruanded teie organisatsiooni andmeid. Kui te pole Microsoft Power BI-d varem kasutanud, saate selle kohta lisateavet teemast [Power BI juhendatud õpe.](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData) Sisupaketti kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                            | Sisu                                               |
|-----------------------------------|--------------------------------------------------------|
| Pädevuste ja arengu analüüs | Meeskonnaliikme oskuste tüübid ja meeskonnaliikme oskused tüübi järgi |
| Oskuse profiil                     | Valitud töötaja oskuse profiil                |
| Oskuse analüüs                    | Oskused tüübi ja hinnangu alusel                              |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Töötaja pädevuste ja arengu sisupaketi aruannete täitmiseks kasutatakse Finance and Operationsi andmeid. Järgmises tabelis on toodud sisupaketi aluseks olevad üksused.

| Üksus                            | Sisu                                                                                                   | Seosed teiste üksustega |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Tööjõud\_CalendarOffset         | Kalendri tasakaalustused aruannete tükeldamiseks                                                                          | |
| Tööjõud\_Ettevõte                | Ettevõtted, mille alusel aruandeid filtreerida                                                                             | |
| Tööjõud\_Tasu           | Tasu määr ja sagedus aja jooksul                                                                           | |
| Tööjõud\_CurrentCompensation    | Tasu määr ja sagedus tänase kuupäeva seisuga                                                              | Tööjõud\_Ettevõte, Tööjõud\_CurrentCompensation, Tööjõud\_Demograafilised andmed, Tööjõud\_Töö, Tööjõud\_Amet |
| Tööjõud\_CurrentPosition        | Ametikohad tänase kuupäeva seisuga, täistööaja ekvivalent (TTE), avatud ametikohad ja täitmiseks avatud ametikohad | Tööjõud\_Tööjõu töö\_Amet |
| Tööjõud\_CurrentWorker          | Töötajad tänase kuupäeva seisuga, vanus ja inimeste arv                                                         | Tööjõud\_Ettevõte, Tööjõud\_Tasu, Tööjõud\_GeographicLocation, Tööjõud\_Tulemus, Tööjõud\_PersonSkill, Tööjõud\_WorkerName, Tööjõud\_ReportsToWorkerName, Tööjõud\_WorkerTitle, Tööjõud\_Demograafilised andmed, Tööjõud\_Töö, Tööjõud\_Töösuhe, Tööjõud\_Amet |
| Tööjõud\_Kuupäev                   | Päevad, nädalad, kuud ja aastad                                                                             | |
| Tööjõud\_Demograafilised andmed           | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis                                                   | |
| Tööjõud\_Töösuhe             | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                                                                  | |
| Tööjõud\_GeographicLocation     | Linn, maakond, sihtnumber ja osariik või provints                                                           | |
| Tööjõud\_Töö                    | Funktsioon, tüüp ja ametinimetus                                                                                  | |
| Tööjõud\_JobPreferredSkill      | Tähtsus, hinnang, oskus ja oskuse tase                                                                 | Tööjõud\_Oskus, Tööjõud\_Töö |
| Tööjõud\_PastPositionAssignment | Määramise põhjus, alguskuupäev, lõppkuupäev ja töö                                                           | Tööjõud\_CalendarOffset, Tööjõud\_Kuupäev, Tööjõud\_Töö, Tööjõud\_Ametikoht |
| Tööjõud\_Tulemus            | Hinnang, kirjeldus ja hinnangumudel                                                                      | |
| Tööjõud\_PersonSkill            | Tase, taseme kuupäev ja oskus                                                                               | Tööjõud\_Oskus |
| Tööjõud\_PersonSkillAnalysis    | Sertifitseeritud, tase, taseme kuupäev ja oskus                                                                    | Tööjõud\_WorkerName, Tööjõud\_Oskus |
| Tööjõud\_Amet               | Osakond, TTE, ametikoht, ametikoha tüüp ja ametinimetus                                                        | |
| Tööjõud\_PositionTrend          | Ametikohad aja jooksul, TTE ja töö                                                                          | Tööjõud\_CalendarOffset, Tööjõud\_Kuupäev, Tööjõud\_Töö, Tööjõud\_Ametikoht |
| Tööjõud\_ReportsToWorkerName    | Eesnimi, perekonnanimi ja täielik nimi                                                                       | |
| Tööjõud\_Oskus                  | Oskus, oskuse tüüp ja hinnang                                                                              | |
| Tööjõud\_TerminatedWorker       | Lõpetatud lepinguga töötajad, lepingu lõpetamise kuupäev, ametinimetus, ametikoht ja töö                                             | Tööjõud\_Ettevõte, Tööjõud\_Tasu, Tööjõud\_GeographicLocation, Tööjõud\_Tulemus, Tööjõud\_WorkerName, Tööjõud\_ReportsToWorkerName, Tööjõud\_CalendarOffset, Tööjõud\_Kuupäev, Tööjõud\_WorkerTitle, Tööjõud\_Demograafia, Tööjõud\_Töösuhe, Tööjõud\_Töö, Tööjõud\_Amet |
| Tööjõud\_WorkerName             | Eesnimi, perekonnanimi ja täielik nimi                                                                       | |
| Tööjõud\_WorkerTitle            | Ametinimetus ja staaži kuupäev                                                                                   | |
| Tööjõud\_WorkerTrend             | Töötajad aja jooksul, inimeste arv, ettevõte ja ametikoht                                                        | Tööjõud\_Ettevõte, Tööjõud\_Tasu, Tööjõud\_GeographicLocation, Tööjõud\_Tulemus, Tööjõud\_WorkerName, Tööjõud\_ReportsToWorkerName, Tööjõud\_CalendarOffset, Tööjõud\_Kuupäev, Tööjõud\_WorkerTitle, Tööjõud\_Demograafilised andmed, Tööjõud\_Töösuhe, Tööjõud\_Töö |
