---
title: Soodustuste Power BI sisu
description: "Selles teemas kirjeldatakse soodustuste Power BI sisu. See selgitab ka seda, kuidas sisalduvatele aruannetele juurde pääseda, ning annab teavet sisu loomiseks kasutatud andmemudeli ja üksuste kohta."
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
ms.openlocfilehash: 815d8ecfe85c1000667d2d289c05c1e98b8b8c76
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017

---

# <a name="benefits-power-bi-content"></a>Soodustuste Power BI sisu

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse **soodustuste** Microsoft Power BI sisu. See selgitab ka seda, kuidas sisalduvatele aruannetele juurde pääseda, ning annab teavet sisu loomiseks kasutatud andmemudeli ja üksuste kohta.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Soodustuste** Power BI sisu kuvatakse tööruumis **Soodustuste haldus**, kui kasutate ühte järgmistest toodetest:

- Lahenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise Editioni 2017. aasta juuli värskendus
- Microsoft Dynamics 365 for Talent

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisu hulka kuuluvad aruanded
**Soodustuste** Power BI sisusse kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                       | Sisu                                                                                       |
|------------------------------|------------------------------------------------------------------------------------------------|
| Soodustuse registreerimise ülevaade  | Kõige rohkem ja vähem registreeritud plaanid, registreerimine töötajagruppide kaupa ja valitud soodustusplaanide võimalused |
| Töövõtja eelised            | Töövõtja liitumine valitud eelise järgi                                                        |
                                                                                             
Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="extending-the-power-bi-content"></a>Power BI sisu laiendamine
Kasutades teenuses Microsoft Dynamics Lifecycle Services (LCS) olevaid sisupakette, saate pakkuda suurepäraseid analüüsivõimalusi inimestele, kes rakendusse Finance and Operations sisse ei logi. Neid sisupakette saab muuta nii, et need sisaldaksid teisi aruandeid või visuaale, ja avaldada siis sisupaketid analüüsimiseks Power BI.com-i rentnikus.

**Soodustuste** Power BI sisu leiate LCS-i ühiste vahendite teegist. Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md). Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).

>[!NOTE]
>Teenuses Lifecycle Services olevad PBIX-failid kehtivad ainult Finance and Operationsi puhul.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
**Soodustuste** Power BI sisus olevate aruannete täitmiseks kasutatakse järgmisi andmeid. Selles tabelis on toodud sisu aluseks olevad üksused.

| Üksus                   | Sisu                                                                                                   | Seosed teiste üksustega |
|--------------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Kalendri tasakaalustus          | Kalendri tasakaalustused aruannete tükeldamiseks                                                                          | Varasem ametikoha määramine, ametikoha trend, töötaja trend, lõpetatud lepinguga töötaja |
| Ettevõte                  | Ettevõtted, mille alusel aruandeid filtreerida                                                                             | Praegune tasu, praegune töötaja, lõpetatud lepinguga töötaja, töötaja trend |
| Hüvitus             | Tasu määr ja sagedus aja jooksul                                                                           | Praegune tasu, praegune töötaja, lõpetatud lepinguga töötaja, töötaja trend |
| Praegune tasu     | Tasu määr ja sagedus tänase kuupäeva seisuga                                                              | Ettevõte, tasu, demograafia, töö, ametikoht |
| Praegune ametikoht         | Ametikohad tänase kuupäeva seisuga, täistööaja ekvivalent (TTE), avatud ametikohad ja täitmiseks avatud ametikohad | Töö, ametikoht |
| Praegune töötaja         | Töötajad tänase kuupäeva seisuga, vanus ja inimeste arv                                                         | Ettevõte, tasu, geograafiline asukoht, töötaja nimi, otsene juht, töötaja ametinimetus, demograafilised andmed, töö, töösuhe, ametikoht, soodustused |
| Kuupäev                     | Päevad, nädalad, kuud ja aastad                                                                             | Varasem ametikoha määramine, ametikoha trend, lõpetatud lepinguga töötaja, töötaja trend |
| Demograafilised näitajad             | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis                                                   | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Tööhõive               | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                                                                  | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Geograafiline asukoht      | Linn, maakond, sihtnumber ja osariik või provints                                                           | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Töö                      | Funktsioon, tüüp ja ametinimetus                                                                                  | Praegune ametikoht, praegune töötaja |
| Varasem ametikoha määramine | Määramise põhjus, alguskuupäev, lõppkuupäev ja töö                                                           | Kalendri tasakaalustus, kuupäev, töö, ametikoht |
| Ametikoht                 | Osakond, TTE, ametikoht, ametikoha tüüp ja ametinimetus                                                        | Praegune ametikoht, praegune töötaja |
| Ametikoha trend           | Ametikohad aja jooksul, TTE ja töö                                                                          | Kalendri tasakaalustus, kuupäev, töö, ametikoht |
| Otsene juht               | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Praegune töötaja, lõpetatud lepinguga töötaja, töötaja trend |
| Lõpetatud lepinguga töötaja      | Lõpetatud lepinguga töötajad, lepingu lõpetamise kuupäev, ametinimetus, ametikoht ja töö                                           | Ettevõte, tasu, geograafiline asukoht, töötaja nimi, otsene juht, kalendri tasakaalustus, kuupäev, töötaja ametinimetus, demograafilised andmed, töö, ametikoht, soodustused |
| Soodustused                 | Jõustumiskuupäev, eelise valik, eelise plaan ja eelise tüüp                                             | Praegune nimi, lõpetatud lepinguga töötaja, töötaja trend |
| Töövõtja nimi            | Eesnimi, perekonnanimi ja täielik nimi                                                                       | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Töötaja ametinimetus           | Ametinimetus ja staaži kuupäev                                                                                   | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Töötaja trend           | Töötajad aja jooksul, inimeste arv, ettevõte ja ametikoht                                                        | Ettevõte, tasu, geograafiline asukoht, töötaja nimi, otsene juht, kalendri tasakaalustus, kuupäev, töötaja ametinimetus, demograafilised andmed, töö, soodustused |

Neid olemeid kasutati arvutatud meetmete loomiseks andmemudelis. Seejärel kasutatakse neid arvutatud meetmeid sisus kasutatavate tulemuslikkuse võtmenäitajate (KPI-de) ja aruannete arvutamiseks. Aruannetesse ja armatuurlauale täiendavate arvutuste lisamiseks võite laadida PBIX-faili LCS-ist alla ja seda muuta. See fail on vaikeandmemudel, mida kasutati sisu loomiseks. Kui muudatused on tehtud, saate luua organisatsiooni sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.
