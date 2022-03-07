---
title: Hüvitise ja eeliste Power BI sisu
description: Selles teemas kirjeldatakse kompensatsiooni ja eeliste Power BI sisu.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263914
ms.assetid: 18634bb5-3341-42f2-9cc9-7b04708b506b
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 13f084ba49baa01eea99822baa6960136725140a80c9d29a4104aabc5d7d5dca
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772078"
---
# <a name="compensation-and-benefits-power-bi-content"></a>Hüvitise ja eeliste Power BI sisu

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse kompensatsiooni ja eeliste Power BI sisu. 

## <a name="reports-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad aruanded
Pärast sisupaketi ühendamist andmetega näitavad aruanded teie organisatsiooni andmeid. Kui te pole Microsoft Power BI-d varem kasutanud, saate selle kohta lisateavet teemast [Juhendatud õpe Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Sisupaketti kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                     | Sisu                                                                                                                              |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Hüvitise ja eeliste analüüs | Ettevõtte tunni- ja kuupalgalised töövõtjad, keskmine tunnitasu, keskmine kuutasu, töövõtjad töövõtutüübi järgi ja plaaniga liitumine |
| Töövõtja eelised          | Töövõtja liitumine valitud eelise järgi                                                                                               |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Kompensatsiooni ja eeliste sisupaketi aruannete täitmiseks kasutatakse rakenduse andmeid. Järgmises tabelis on toodud sisupaketi aluseks olevad üksused.

| Üksus                            | Sisu                                                                                                   | Seosed teiste üksustega |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Tööjõud\_CalendarOffset         | Kalendri tasakaalustused aruannete tükeldamiseks                                                                          | Tööjõud\_PastPositionAssignment, Tööjõud\_PositionTrend, Tööjõud\_WorkerTrend, Tööjõud\_TerminatedWorker |
| Tööjõud\_Ettevõte                | Ettevõtted, mille alusel aruandeid filtreerida                                                                             | Tööjõud\_CurrentCompensation, Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_Tasu           | Tasu määr ja sagedus aja jooksul                                                                           | Tööjõud\_CurrentCompensation, Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_CurrentCompensation    | Tasu määr ja sagedus tänase kuupäeva seisuga                                                              | Tööjõud\_Ettevõte, Tööjõud\_Hüvitis, Tööjõud\_Demograafia, Tööjõud\_Töö, Tööjõud\_Ametikoht |
| Tööjõud\_CurrentPosition        | Ametikohad tänase kuupäeva seisuga, täistööaja ekvivalent (TTE), avatud ametikohad ja täitmiseks avatud ametikohad | Tööjõud\_Tööjõu töö\_Amet |
| Tööjõud\_CurrentWorker          | Töötajad tänase kuupäeva seisuga, vanus ja inimeste arv                                                         | Tööjõud\_Ettevõte, Tööjõud\_Hüvitis, Tööjõud\_GeographicLocation, Tööjõud\_Tulemus, Tööjõud\_WorkerName, Tööjõud\_ReportsToWorkerName, Tööjõud\_WorkerTitle, Tööjõud\_Demograafia, Tööjõud\_Töö, Tööjõud\_Tööhõive, Tööjõud\_Ametikoht, Tööjõud\_WorkerBenefit |
| Tööjõud\_Kuupäev                   | Päevad, nädalad, kuud ja aastad                                                                             | Tööjõud\_PastPositionAssignment, Tööjõud\_PositionTrend, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_Demograafilised andmed           | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis                                                   | Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_Töösuhe             | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                                                                  | Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_GeographicLocation     | Linn, maakond, sihtnumber ja osariik või provints                                                           | Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_Töö                    | Funktsioon, tüüp ja ametinimetus                                                                                  | Tööjõud\_CurrentPosition, Tööjõud\_CurrentWorker |
| Tööjõud\_PastPositionAssignment | Määramise põhjus, alguskuupäev, lõppkuupäev ja töö                                                           | Tööjõud\_CalendarOffset, Tööjõud\_Kuupäev, Tööjõud\_Töö, Tööjõud\_Ametikoht |
| Tööjõud\_Tulemus            | Hinnang, kirjeldus ja hinnangumudel                                                                      | Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_Amet               | Osakond, TTE, ametikoht, ametikoha tüüp ja ametinimetus                                                        | Tööjõud\_CurrentPosition, Tööjõud\_CurrentWorker |
| Tööjõud\_PositionTrend          | Ametikohad aja jooksul, TTE ja töö                                                                          | Tööjõud\_CalendarOffset, Tööjõud\_Kuupäev, Tööjõud\_Töö, Tööjõud\_Ametikoht |
| Tööjõud\_ReportsToWorkerName    | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_Oskus                  | Oskus, oskuse tüüp ja hinnang                                                                              | |
| Tööjõud\_TerminatedWorker       | Lõpetatud lepinguga töötajad, lepingu lõpetamise kuupäev, ametinimetus, ametikoht ja töö                                             | Tööjõud\_Ettevõte, Tööjõud\_Hüvitis, Tööjõud\_GeographicLocation, Tööjõud\_Tulemus, Tööjõud\_WorkerName, Tööjõud\_ReportsToWorkerName, Tööjõud\_CalendarOffset, Tööjõud\_Kuupäev, Tööjõud\_WorkerTitle, Tööjõud\_Demograafia, Tööjõud\_Tööhõive, Tööjõud\_Töö, Tööjõud\_Ametikoht, Tööjõud\_WorkerBenefit |
| Tööjõud\_WorkerBenefit          | Jõustumiskuupäev, eelise valik, eelise plaan ja eelise tüüp                                             | Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_WorkerName             | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_WorkerTitle            | Ametinimetus ja staaži kuupäev                                                                                   | Tööjõud\_CurrentWorker, Tööjõud\_TerminatedWorker, Tööjõud\_WorkerTrend |
| Tööjõud\_WorkerTrend            | Töötajad aja jooksul, inimeste arv, ettevõte ja ametikoht                                                        | Tööjõud\_Ettevõte, Tööjõud\_Hüvitis, Tööjõud\_GeographicLocation, Tööjõud\_Tulemus, Tööjõud\_WorkerName, Tööjõud\_ReportsToWorkerName, Tööjõud\_CalendarOffset, Tööjõud\_Kuupäev, Tööjõud\_WorkerTitle, Tööjõud\_Demograafia, Tööjõud\_Tööhõive, Tööjõud\_Töö, Tööjõud\_WorkerBenefit |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]