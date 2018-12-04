---
title: Organisatsiooni koolituse Power BI sisu
description: See teema kirjeldab Dynamics 365 for Finance and Operationsi mooduli Organisatsiooni koolitus Power BI sisu.
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
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 6c1855013dc449950877f8727a5453942aeb75de
ms.contentlocale: et-ee
ms.lasthandoff: 08/13/2018

---

# <a name="organizational-training-power-bi-content"></a>Organisatsiooni koolituse Power BI sisu

[!include [banner](../includes/banner.md)]

See teema kirjeldab Dynamics 365 for Finance and Operationsi mooduli Organisatsiooni koolitus Power BI sisu.

## <a name="reports-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad aruanded
Pärast sisupaketi ühendamist Finance and Operationsi andmetega näitavad aruanded teie organisatsiooni andmeid. Kui te pole Microsoft Power BI-d varem kasutanud, saate selle kohta lisateavet jaotisest [Power BI juhendatud õpe](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sisupaketti kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne          | Sisu                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kursuse analüüs | Registreerumine asukoha, kursusel osalejate oleku ja registreerimisloendi järgi |
| Kursuste tüübid    | Kursuse tüübid oskuse järgi                                                       |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Organisatsiooni koolituse sisupaketi aruannete täitmiseks kasutatakse Finance and Operationsi andmeid. Järgmises tabelis on toodud sisupaketi aluseks olevad üksused.

| Üksus                    | Sisu                                                         | Seosed teiste üksustega |
|---------------------------|------------------------------------------------------------------|-----------------------------------|
| Koolitus\_CalendarOffset  | Kalendri tasakaalustused aruannete tükeldamiseks                                | Koolitus\_CourseAgenda, Koolitus\_CourseAttendees |
| Koolitus\_Ettevõte         | Ettevõtted, mille alusel aruandeid filtreerida                                   | Koolitus\_CourseAgenda, Koolitus\_CourseAttendees |
| Koolitus\_Kursus          | Kursus, kirjeldus, juhendaja nimi, asukoht, ruum ja olek | Koolitus\_CourseAgenda, Koolitus\_CourseAttendees, Koolitus\_CourseSkill |
| Koolitus\_CourseAgenda    | Päevakord, kursus ja alguse ning lõpu ajad                          | Koolitus\_Ettevõte, Koolitus\_CalendarOffset, Koolitus\_Kuupäev, Koolitus\_Kursus |
| Koolitus\_CourseAttendees | Nimi, olek, töö ja registreerimise kuupäev                         | Koolitus\_Ettevõte, Koolitus\_CalendarOffset, Koolitus\_Kuupäev, Koolitus\_Demograafilised andmed, Koolitus\_Töösuhe, Koolitus\_Kursus, Koolitus\_WorkerName, Koolitus\_WorkerTitle, Koolitus\_Töö, Koolitus\_Amet |
| Koolitus\_CourseSkill     | Oskus, oskuse tüüp ja tase                                     | Koolitus\_Kursus |
| Koolitus\_Kuupäev            | Päevad, nädalad, kuud ja aastad                                   | Koolitus\_CourseAgenda, Koolitus\_CourseAttendees |
| Koolitus\_Demograafilised andmed    | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis         | Koolitus\_CourseAgenda, Koolitus\_CourseAttendees |
| Koolitus\_Töösuhe      | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                        | Koolitus\_CourseAgenda, Koolitus\_CourseAttendees |
| Koolitus\_Töö             | Funktsioon, tüüp ja ametinimetus                                        | Koolitus\_CourseAgenda, Koolitus\_CourseAttendees |
| Koolitus\_Amet        | Amet, ametinimetus ja täistööajaga võrdne väärtus (FTE)                  | Koolitus\_CourseAgenda, Koolitus\_CourseAttendees |
| Koolitus\_WorkerName      | Eesnimi, perekonnanimi ja täielik nimi                             | Koolitus\_CourseAttendees |
| Koolitus\_WorkerTitle     | Ametinimetus ja staaži kuupäev                                         | Koolitus\_CourseAttendees |

