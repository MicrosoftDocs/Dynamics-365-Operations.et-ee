---
title: Õppimise Power BI sisu
description: See artikkel kirjeldab õppe sisu Power BI.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a7aca9e47ed26dcb4ef7f4b9aee72987e2d8fdd2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273955"
---
# <a name="learning-power-bi-content"></a>Õppimise Power BI sisu

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab **õppe sisu** Microsoft Power BI.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad aruanded

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

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
