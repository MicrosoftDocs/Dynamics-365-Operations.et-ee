---
title: Organisatsiooni koolitus Power BI sisu
description: "Teema käsitleb Dynamics 365 toiminguteks - organisatsiooniline koolitus Power BI sisu. Ta selgitab, kuidas pääseda sisu pakendi ja kirjeldab andmemudel ja üksuste, kasutatud ehitada sisu pakendi."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organisatsiooni koolitus Power BI sisu

Teema käsitleb Dynamics 365 toiminguteks - organisatsiooniline koolitus Power BI sisu. Ta selgitab, kuidas pääseda sisu pakendi ja kirjeldab andmemudel ja üksuste, kasutatud ehitada sisu pakendi.

<a name="accessing-the-content-pack"></a>Juurdepääsu sisu pakendi
--------------------------

Leiate organisatsioonilise koolituse sisu pakendi jagatud varade teegi in Microsoft Dynamics elutsükli teenused (LCS). Lae sisu pakendi ja ühendada oma Microsoft Dynamics 365 toimingute andmete kohta lisateabe saamiseks vt [Power BI sisu LCS Microsofti ja oma partnerite](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-content-pack"></a>Aruanded, mis on kaasatud sisu pack
Pärast sisu pakendi oma Dynamics 365 toimingute andmed, aruannetest nähtub teie ettevõtte andmeid. Kui te pole varem Microsoft Power BI enne, saab õppida rohkem sellest on [juhindub õppe lehekülg Power BI](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData). Aruanded, mis on kaasatud sisu pack on graafikuid ja tabeleid, mis sisaldavad täiendavat teavet. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne          | Sisu                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| Kursuse analüüs | Asukoht, kursuse osalejate olekut ja Registreerimisnimekiri registreerimine |
| Kursuste tüübid    | Kursuse tüübid oskuse järgi                                                       |

Saate filtreerida diagrammid ja plaadid aruannete ja diagrammide ja plaadid armatuurlauale kinnitada. Filter ja Power BI pin kohta lisateabe saamiseks vt [loomine ja konfigureerimine armatuurlaua](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Toimingute andmed Dynamics 365 saab asustada organisatsioonilise koolituse sisu Pack aruanded. Järgmine tabel näitab üksuste sisu pakendi põhines.

| Üksus                    | Sisu                                                         | Suhted ka teiste                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Koolitus\_CalendarOffset  | Kalendri tasakaalustab viil aruanded                                | Koolitus\_CourseAgenda koolitus\_CourseAttendees                                                                                                                                                   |
| Koolitus\_firma         | Ettevõtete poolt aruannete filtreerimiseks                                   | Koolitus\_CourseAgenda koolitus\_CourseAttendees                                                                                                                                                   |
| Koolitus\_kursus          | Muidugi, kirjeldus, juhendaja nimi, asukoht, tuba ja staatus | Koolitus\_CourseAgenda koolitus\_CourseAttendees koolitus\_CourseSkill                                                                                                                             |
| Koolitus\_CourseAgenda    | Tegevuskava ja kursuse algus-ja lõpp                          | Koolitus\_firma koolitus\_CalendarOffset koolitus\_koolituse kuupäev\_kursus                                                                                                                         |
| Koolitus\_CourseAttendees | Nimi, staatus, töö, ja kuupäev                         | Koolitus\_firma koolituse\_CalendarOffset koolitus\_koolituse kuupäev\_demograafia koolitus\_tööturukoolitust\_muidugi koolitus\_WorkerName koolitus\_WorkerTitle koolitus\_töö koolitus\_asendis |
| Koolitus\_CourseSkill     | Oskus, oskus tüüp ja tase                                     | Koolitus\_kursus                                                                                                                                                                                   |
| Koolitus\_kuupäev            | Päeva, nädala, kuu ja aasta                                   | Koolitus\_CourseAgenda koolitus\_CourseAttendees                                                                                                                                                   |
| Koolitus\_demograafia    | Sünniaeg, soo, etnilise päritolu ja Perekonnaseis         | Koolitus\_CourseAgenda koolitus\_CourseAttendees                                                                                                                                                   |
| Koolitus\_tööhõive      | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                        | Koolitus\_CourseAgenda koolitus\_CourseAttendees                                                                                                                                                   |
| Koolitus\_töö             | Funktsiooni, tüüp ja tiitel                                        | Koolitus\_CourseAgenda koolitus\_CourseAttendees                                                                                                                                                   |
| Koolitus\_asendis        | Positsiooni, pealkiri ja täiskoha ekvivalent (taandatuna Täistööajale)                  | Koolitus\_CourseAgenda koolitus\_CourseAttendees                                                                                                                                                   |
| Koolitus\_WorkerName      | Eesnimi, perekonnanimi ja täisnimi                             | Koolitus\_CourseAttendees                                                                                                                                                                          |
| Koolitus\_WorkerTitle     | Pealkiri ja staažist                                         | Koolitus\_CourseAttendees                                                                                                                                                                          |

Need üksused olid saab luua arvutatud mõõtmeid andmemudel. Need arvutatakse meetmed seejärel kasutatakse tulemuslikkuse võtmenäitajate (KPI) ja aruanded, mida kasutatakse sisu Pack. Kui soovite kaasata edasiste arvutuste aruanded ja armatuurlaud, saate alla laadida ja muuta LCS Training.pbix faili. See fail on vaikimisi andmemudel, kust luua sisu pakendi. Kui olete teinud muudatusi, saate luua organisatsiooni sisu pakendi ja armatuurlaud, mis sisaldab lisatud teavet.

## <a name="additional-resources"></a>Lisaressursid
Siin on mõned abistavad lingid, mis on seotud üksuste ja Power BI sisu loomisega.

-   [Andmeüksused](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [Organisatsiooniliste sisupakettide loomine](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   A[Andmete modelleerimine Power BI-d kasutades](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI paanide lisamine tööruumidele](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



