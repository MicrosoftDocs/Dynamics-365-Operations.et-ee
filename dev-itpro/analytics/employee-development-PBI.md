---
title: "Töötajate arengu Power BI sisu"
description: "Selles teemas kirjeldatakse töötajate arengu Power BI sisu. See selgitab ka seda, kuidas pääseda juurde aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks."
author: jcart1106
manager: AnnBe
ms.date: 05/24/2017
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
ms.openlocfilehash: d25f3be5821a02ea618a2356878bf2904765a6f7
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="employee-development-power-bi-content"></a>Töötajate arengu Power BI sisu

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse **töötajate arengu** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule

Kui kasutate Microsoft Dynamics 365 for Finance and Operations, Enterprise editioni 2017. aasta juuli värskendust, siis leiate **töötaja arengu** Power BI sisu sisupaketi teenuse Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegist. Lisateavet sisupaketi allalaadimise ja selle ühendamise kohta teie andmetega vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad aruanded
**Töötaja arengu** Power BI sisusse kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                        | Sisu |
|-------------------------------|----------|
| Töötaja arengu ülevaade | Teiste aruannete kokkuvõte |
| Töötaja oskuste analüüs       | Töötaja oskuste tüübid ja töötaja oskused tüübi järgi |
| Töötaja oskuste taseme analüüs | Töötaja oskuste tase osakonna järgi, töötajad oskuste taseme ja oskuste tüübi järgi ja madalaimad ning kõrgeimad tasemed oskuste järgi |
| Oskuse profiil                 | Valitud töötaja oskuse profiil |
| Oskuse analüüs                | Oskused tüübi ja hinnangu alusel |
| Jõudluse hinnangu analüüs   | Töötajad madalaima ja kõrgeima hinnangu järgi töö alusel, töötajate hinnangud osakondade järgi, töötajad hinnangu ja ametikoha tüübi järgi ning kõrgeimad ja madalaimad hinnangud ametikoha järgi  |
| Töötaja jõudluse analüüs | Töötaja hinnangud valitud hinnangu puhul juhilt |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
| Üksus                   | Sisu                                                                                                   | Seosed teiste üksustega |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalendri tasakaalustus          | Kalendri tasakaalustused aruannete tükeldamiseks                                                                          | Varasem ametikoha määramine, ametikoha trend, töötaja trend, lõpetatud lepinguga töötaja 
| Ettevõte                  | Ettevõtted, mille alusel aruandeid filtreerida                                                                             | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Praegune ametikoht         | Ametikohad tänase kuupäeva seisuga, täistööaja ekvivalent (TTE), avatud ametikohad ja täitmiseks avatud ametikohad | Töö, ametikoht |
| Praegune töötaja         | Töötajad tänase kuupäeva seisuga, vanus ja inimeste arv                                                         | Ettevõte, geograafiline asukoht, töötaja nimi, otsene juht, töötaja ametinimetus, demograafilised andmed, töö, töösuhe, ametikoht |
| Kuupäev                     | Päevad, nädalad, kuud ja aastad                                                                             | Varasem ametikoha määramine, ametikoha trend, lõpetatud lepinguga töötaja, töötaja trend |
| Demograafilised näitajad             | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis                                                   | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Tööhõive               | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                                                                  | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Geograafiline asukoht      | Linn, maakond, sihtnumber ja osariik või provints                                                           | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Töö                      | Funktsioon, tüüp ja ametinimetus                                                                                  | Praegune ametikoht, praegune töötaja |
| Varasem ametikoha määramine | Määramise põhjus, alguskuupäev, lõppkuupäev ja töö                                                           | Kalendri tasakaalustus, kuupäev, töö, ametikoht |
| Ametikoht                 | Osakond, TTE, ametikoht, ametikoha tüüp ja ametinimetus                                                        | Praegune ametikoht, praegune töötaja |
| Ametikoha trend           | Ametikohad aja jooksul, TTE ja töö                                                                          | Kalendri tasakaalustus, kuupäev, töö, ametikoht |
| Otsene juht               | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Lõpetatud lepinguga töötaja      | Lõpetatud lepinguga töötajad, lepingu lõpetamise kuupäev, ametinimetus, ametikoht ja töö                                             | Ettevõte, geograafiline asukoht, töötaja nimi, otsene juht, kalendri tasakaalustus, kuupäev, töötaja ametinimetus, demograafilised andmed, töösuhe, töö, ametikoht |
| Töövõtja nimi            | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Praegune töötaja, lõpetatud lepinguga töötaja, töötaja trend |
| Töötaja ametinimetus           | Ametinimetus ja staaži kuupäev                                                                                   | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Töötaja trend           | Töötajad aja jooksul, inimeste arv, ettevõte ja ametikoht                                                        | Ettevõte, geograafiline asukoht, töötaja nimi, otsene juht, kalendri tasakaalustus, kuupäev, töötaja ametinimetus, demograafilised andmed, töösuhe, töö |
| Töö                      | Funktsioon, tüüp ja ametinimetus                                                                                      | Praegune töötaja, praegune ametikoht, töötaja trend, töö eelistatud oskus, varasem ametikoha määramine, ametikoha trend, lõpetatud lepinguga töötaja |
| Töö eelistatud oskus      | Tähtsus, hinnang, oskus ja oskuse tase                                                                 | Töö |
| Töötaja oskuste analüüs  | Sertifitseeritud, tase, taseme kuupäev ja oskus                                                                    | Töötaja nimi, oskus |  
| Jõudlus              | Hinnang, kirjeldus ja hinnangumudel                                                                      | Praegune töötaja, praegune ametikoht, töötaja trend, töö eelistatud oskus, varasem ametikoha määramine, ametikoha trend, lõpetatud lepinguga töötaja |
|  Oskus                   | Oskus, oskuse tüüp ja hinnang                                                                              | Töötaja oskuste analüüs, töö eelistatud oskus |                                                                                                                        

Neid olemeid kasutati arvutatud meetmete loomiseks andmemudelis. Seejärel kasutatakse neid arvutatud meetmeid Power BI sisus kasutatavate tulemuslikkuse võtmenäitajate (KPI-d) ja aruannete arvutamiseks. Aruannetesse ja armatuurlauale täiendavate arvutuste lisamiseks võite laadida PBIX-faili LCS-ist alla ja seda muuta. See fail on vaikeandmemudel, mida kasutati Power BI sisu loomiseks. Kui muudatused on tehtud, saate luua organisatsiooni sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.

