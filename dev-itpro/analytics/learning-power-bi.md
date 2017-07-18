---
title: "Õppimise Power BI sisu"
description: "Selles teemas kirjeldatakse õppimise Power BI sisu. See selgitab ka seda, kuidas pääseda juurde aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: JCart
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a3f28d21a7e73d3ad462c5cc37198dd2b6f5f8af
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="learning-power-bi-content"></a>Õppimise Power BI sisu

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse **õppimise** Microsoft Power BI sisu. See selgitab ka seda, kuidas sisule juurde pääseda, ning kirjeldab andmemudelit ja üksusi, mida sisu loomiseks kasutati.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

Kui kasutate Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni 2017. aasta juuli värskendust, siis leiate **õppimise** Power BI sisu teenuse Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegist. Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md). Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad aruanded

**Õppimise** Power BI sisusse kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                | Sisu |
|-----------------------|----------|
| Õppimise ülevaade     | Teiste aruannete kokkuvõte |
| Kursuse analüüs       | Registreerimine asukoha alusel, osaleja oleku alusel, kursused tüübi alusel ettevõtte kohta ja kursusel osalemine tööde kaupa |
| Registreerimise analüüs | Registreerimisloend |
| Kursuste tüübid          | Kursuse tüübid oskuse järgi |
| Juhendaja analüüs   | Kursuste suhtarv juhendajate kohta, juhendajate arv, kursused juhendaja alusel, kursusi juhendaja kohta ja kursuse päevakord juhendaja alusel |
| Pakutavad kursused       | Kursuste loend |
| Kursuste ülesehitus        | Kursuse päevakord |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused

**Õppimise** Power BI sisus olevate aruannete täitmiseks kasutatakse järgmisi andmeid. Selles tabelis on toodud sisu aluseks olevad üksused.

| Üksus           | Sisu                                                         | Seosed teiste üksustega |
|------------------|------------------------------------------------------------------|-----------------------------------|
| Kalendri tasakaalustus  | Kalendri tasakaalustused aruannete tükeldamiseks                                | Kursuse päevakord, kursusel osalejad |
| Ettevõte          | Ettevõtted, mille alusel aruandeid filtreerida                                   | Kursuse päevakord, kursusel osalejad |
| Kursus           | Kursus, kirjeldus, juhendaja nimi, asukoht, ruum ja olek | Kursuse päevakord, kursusel osalejad, kursuse oskus |
| Kursuse päevakord    | Päevakord, kursus ja alguse ning lõpu ajad                          | Ettevõte, kalendri tasakaalustus, kuupäev, kursus |
| Kursusel osalejad | Nimi, olek, töö ja registreerimise kuupäev                         | Ettevõte, kalendri tasakaalustus, kuupäev, kursus, demograafilised andmed, töösuhe, kursus, töötaja nimi, töötaja ametinimetus, töö, ametikoht |
| Kursuse oskus     | Oskus, oskuse tüüp ja tase                                     | Kursus |
| Kuupäev             | Päevad, nädalad, kuud ja aastad                                   | Kursuse päevakord, kursusel osalejad |
| Demograafilised näitajad     | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis         | Kursuse päevakord, kursusel osalejad |
| Tööhõive       | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                        | Kursuse päevakord, kursusel osalejad |
| Töö              | Funktsioon, tüüp ja ametinimetus                                        | Kursuse päevakord, kursusel osalejad |
| Ametikoht         | Amet, ametinimetus ja täistööajaga võrdne väärtus (FTE)                  | Kursuse päevakord, kursusel osalejad |
| Töövõtja nimi    | Eesnimi, perekonnanimi ja täielik nimi                             | Kursusel osalejad |
| Töötaja ametinimetus   | Ametinimetus ja staaži kuupäev                                         | Kursusel osalejad |

Neid olemeid kasutati arvutatud meetmete loomiseks andmemudelis. Seejärel kasutatakse neid arvutatud meetmeid sisus kasutatavate tulemuslikkuse võtmenäitajate (KPI-de) ja aruannete arvutamiseks. Aruannetesse ja armatuurlauale täiendavate arvutuste lisamiseks võite laadida PBIX-faili LCS-ist alla ja seda muuta. See fail on vaikeandmemudel, mida kasutati sisu loomiseks. Kui muudatused on tehtud, saate luua organisatsiooni sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.

