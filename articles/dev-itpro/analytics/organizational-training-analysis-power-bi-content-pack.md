---
title: Organisatsiooni koolituse Power BI sisu
description: "See teema kirjeldab Dynamics 365 for Finance and Operationsi mooduli Organisatsiooni koolitus Power BI sisu. See selgitab ka seda, kuidas sisupaketile juurde pääseda, ning kirjeldab andmemudelit ja üksusi, mida sisupaketi loomiseks kasutati."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e49d9af8b8bd8d5edb977c49742861199c6964fd
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="organizational-training-power-bi-content"></a>Organisatsiooni koolituse Power BI sisu

[!include[banner](../includes/banner.md)]


See teema kirjeldab Dynamics 365 for Finance and Operationsi mooduli Organisatsiooni koolitus Power BI sisu. See selgitab ka seda, kuidas sisupaketile juurde pääseda, ning kirjeldab andmemudelit ja üksusi, mida sisupaketi loomiseks kasutati.

<a name="accessing-the-content-pack"></a>Juurdepääs sisupaketile
--------------------------

Organisatsiooni koolituse sisupaketi leiate teenuste Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegist. Lisateavet sisupaketi allalaadimise ja selle ühendamise kohta Microsoft Dynamics 365 for Finance and Operationsi andmetega vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Sisupaketti kuuluvad aruanded
Pärast sisupaketi ühendamist Dynamics 365 for Finance and Operationsi andmetega näitavad aruanded teie organisatsiooni andmeid. Kui te pole Microsoft Power BI-d varem kasutanud, saate selle kohta lisateavet jaotisest [Power BI juhendatud õpe](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Sisupaketti kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne          | Sisu                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kursuse analüüs | Registreerumine asukoha, kursusel osalejate oleku ja registreerimisloendi järgi |
| Kursuste tüübid    | Kursuse tüübid oskuse järgi                                                       |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Organisatsiooni koolituse sisupaketi aruannete täitmiseks kasutatakse Finance and Operationsi andmeid. Järgmises tabelis on toodud sisupaketi aluseks olevad üksused.

| Üksus                    | Sisu                                                         | Seosed teiste üksustega                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Koolitus\_CalendarOffset  | Kalendri tasakaalustused aruannete tükeldamiseks                                | Koolitus\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Koolitus\_Ettevõte         | Ettevõtted, mille alusel aruandeid filtreerida                                   | Koolitus\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Koolitus\_Kursus          | Kursus, kirjeldus, juhendaja nimi, asukoht, ruum ja olek | Koolitus\_CourseAgenda Training\_CourseAttendees Training\_CourseSkill                                                                                                                             |
| Koolitus\_CourseAgenda    | Päevakord, kursus ja alguse ning lõpu ajad                          | Koolitus\_Ettevõtte koolitus\_Koolituse CalendarOffset\_Koolituse kuupäev\_Kursus                                                                                                                         |
| Koolitus\_CourseAttendees | Nimi, olek, töö ja registreerimise kuupäev                         | Koolitus\_Ettevõtte koolitus\_Koolituse CalendarOffset\_Koolituse kuupäev\_Koolituse demograafilised andmed\_Töökoolitus\_Koolituskursus\_Koolituse WorkerName\_Koolituse WorkerTitle\_Töökoolitus\_Amet |
| Koolitus\_CourseSkill     | Oskus, oskuse tüüp ja tase                                     | Koolitus\_Kursus                                                                                                                                                                                   |
| Koolitus\_Kuupäev            | Päevad, nädalad, kuud ja aastad                                   | Koolitus\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Koolitus\_Demograafilised andmed    | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis         | Koolitus\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Koolitus\_Töösuhe      | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                        | Koolitus\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Koolitus\_Töö             | Funktsioon, tüüp ja ametinimetus                                        | Koolitus\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Koolitus\_Amet        | Amet, ametinimetus ja täistööajaga võrdne väärtus (FTE)                  | Koolitus\_CourseAgenda Training\_CourseAttendees                                                                                                                                                   |
| Koolitus\_WorkerName      | Eesnimi, perekonnanimi ja täielik nimi                             | Koolitus\_CourseAttendees                                                                                                                                                                          |
| Koolitus\_WorkerTitle     | Ametinimetus ja staaži kuupäev                                         | Koolitus\_CourseAttendees                                                                                                                                                                          |

Neid olemeid kasutati arvutatud meetmete loomiseks andmemudelis. Seejärel kasutatakse neid arvutatud meetmeid sisupaketis kasutatavate tulemuslikkuse võtmenäitajate (KPI-d) ja aruannete arvutamiseks. Aruannetesse ja armatuurlauale täiendavate arvutuste lisamiseks võite laadida LCS-ist alla ja muuta faili Training.pbix. See fail on vaikeandmemudel, mida kasutati sisupaketi loomiseks. Kui muudatused on tehtud, saate luua organisatsiooni sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





