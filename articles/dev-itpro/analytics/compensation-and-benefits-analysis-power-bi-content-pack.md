---
title: "Hüvitise ja eeliste Power BI sisu"
description: "See teema kirjeldab Finance and Operationsi mooduli Hüvitis ja eelised Power BI sisu."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: cb43245afe578341251b140383a3b03ba2abd962
ms.openlocfilehash: 510064a462258b2a632eaa2a5ffd341950775b89
ms.contentlocale: et-ee
ms.lasthandoff: 12/19/2017

---

# <a name="compensation-and-benefits-power-bi-content"></a>Hüvitise ja eeliste Power BI sisu

[!include [banner](../includes/banner.md)]

See teema kirjeldab Finance and Operationsi mooduli Hüvitis ja eelised Power BI sisu. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad aruanded
Pärast sisupaketi ühendamist Dynamics 365 for Finance and Operationsi andmetega näitavad aruanded teie organisatsiooni andmeid. Kui te pole Microsoft Power BI-d varem kasutanud, saate selle kohta lisateavet jaotisest [Power BI juhendatud õpe](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sisupaketti kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                     | Sisu                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Hüvitise ja eeliste analüüs | Ettevõtte tunni- ja kuupalgalised töövõtjad, keskmine tunnitasu, keskmine kuutasu, töövõtjad töövõtutüübi järgi ja plaaniga liitumine |
| Töövõtja eelised          | Töövõtja liitumine valitud eelise järgi                                                                                               |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Hüvitise ja eeliste sisupaketi aruannete täitmiseks kasutatakse Finance and Operationsi andmeid. Järgmises tabelis on toodud sisupaketi aluseks olevad üksused.

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
| Tööjõud\_PastPositionAssignment | Määramise põhjus, alguskuupäev, lõppkuupäev ja töö                                                           | Tööjõud\_CalendarOffset Tööjõud\_Kuupäev Tööjõud\_Töö Tööjõud\_Ametikoht                                                                                                                                                                                                                                                     |
| Tööjõud\_Tulemus            | Hinnang, kirjeldus ja hinnangumudel                                                                      | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_Amet               | Osakond, TTE, ametikoht, ametikoha tüüp ja ametinimetus                                                        | Tööjõud\_CurrentPosition Tööjõud\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Tööjõud\_PositionTrend          | Ametikohad aja jooksul, TTE ja töö                                                                          | Tööjõud\_CalendarOffset Tööjõud\_Kuupäev Tööjõud\_Töö Tööjõud\_Ametikoht                                                                                                                                                                                                                                                     |
| Tööjõud\_ReportsToWorkerName    | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_Oskus                  | Oskus, oskuse tüüp ja hinnang                                                                              |                                                                                                                                                                                                                                                                                                                                  |
| Tööjõud\_TerminatedWorker       | Lõpetatud lepinguga töötajad, lepingu lõpetamise kuupäev, ametinimetus, ametikoht ja töö                                             | Tööjõud\_Ettevõte Tööjõud\_Hüvitis Tööjõud\_GeographicLocation Tööjõud\_Tulemus Tööjõud\_WorkerName Tööjõud\_ReportsToWorkerName Tööjõud\_CalendarOffset Tööjõud\_Kuupäev Tööjõud\_WorkerTitle Tööjõud\_Demograafia Tööjõud\_Tööhõive Tööjõud\_Töö Tööjõud\_Ametikoht Tööjõud\_WorkerBenefit |
| Tööjõud\_WorkerBenefit          | Jõustumiskuupäev, eelise valik, eelise plaan ja eelise tüüp                                             | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_WorkerName             | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_WorkerTitle            | Ametinimetus ja staaži kuupäev                                                                                   | Tööjõud\_CurrentWorker Tööjõud\_TerminatedWorker Tööjõud\_WorkerTrend                                                                                                                                                                                                                                                       |
| Tööjõud\_WorkerTrend             | Töötajad aja jooksul, inimeste arv, ettevõte ja ametikoht                                                        | Tööjõud\_Ettevõte Tööjõud\_Hüvitis Tööjõud\_GeographicLocation Tööjõud\_Tulemus Tööjõud\_WorkerName Tööjõud\_ReportsToWorkerName Tööjõud\_CalendarOffset Tööjõud\_Kuupäev Tööjõud\_WorkerTitle Tööjõud\_Demograafia Tööjõud\_Tööhõive Tööjõud\_Töö Tööjõud\_WorkerBenefit                     |







