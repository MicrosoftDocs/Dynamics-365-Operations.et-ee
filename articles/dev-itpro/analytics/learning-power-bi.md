---
title: "Õppimise Power BI sisu"
description: "Selles teemas kirjeldatakse õppimise Power BI sisu."
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0ee0cc2e22609d1a87e7d2b6dcd031606191f879
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="learning-power-bi-content"></a>Õppimise Power BI sisu

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse **õppimise** Microsoft Power BI sisu.

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

