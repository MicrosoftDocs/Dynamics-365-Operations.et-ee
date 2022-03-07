---
title: Organisatsiooni koolituse Power BI sisu
description: Selles teemas kirjeldatakse Finance and Operations - organisatsiooni koolituse Power BI sisu.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cd48c12ea3ea31904c437f678888a51e5381cfcfbeef0e1c709858b0c6cb857d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763544"
---
# <a name="organizational-training-power-bi-content"></a>Organisatsiooni koolituse Power BI sisu

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse Finance and Operations - organisatsiooni koolituse Power BI sisu.

## <a name="reports-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad aruanded
Pärast sisupaketi ühendamist andmetega näitavad aruanded teie organisatsiooni andmeid. Kui te pole Microsoft Power BI-d varem kasutanud, saate selle kohta lisateavet teemast [Juhendatud õpe Power BI](https://powerbi.microsoft.com/guided-learning/?WT.mc_id=PBIService_GetData). Sisupaketti kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne          | Sisu                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kursuse analüüs | Registreerumine asukoha, kursusel osalejate oleku ja registreerimisloendi järgi |
| Kursuste tüübid    | Kursuse tüübid oskuse järgi                                                       |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Organisatsiooni koolituse sisupaketi aruannete täitmiseks kasutatakse rakenduse andmeid. Järgmises tabelis on toodud sisupaketi aluseks olevad üksused.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]