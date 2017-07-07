---
title: "Värbamise Power BI sisu"
description: "Selles teemas kirjeldatakse värbamise Power BI sisu. See selgitab ka seda, kuidas pääseda juurde aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks."
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 49cfd0f1ed645f1980b21b6d4f453cb7a8957a1a
ms.contentlocale: et-ee
ms.lasthandoff: 06/13/2017


---

# <a name="recruiting-power-bi-content"></a>Värbamise Power BI sisu

[!include[banner](../includes/banner.md)]

Selles teemas kirjeldatakse **värbamise** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 2017. aasta juuli värskendust, kuvatakse **värbamise** Power BI sisu aruanded tööruumis **Värbamise haldus**. 

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Aruanded ja visuaalid värbamise halduse tööruumis
**Värbamise halduse** tööruum sisaldab vahekaarti **Analüüs**. Sellel vahekaardil on manustatud Power BI sisu värbamise jaoks. Sisu koosneb ülevaate vahekaardist ja täiendavatest andmeid sisaldavatest vahekaartidest. Järgmises tabelis on kirjeldatud iga vahekaardi aruandeid.

| Aruanne               | Sisu |
|----------------------|----------|
| Värbamise ülevaade | Teeb kokkuvõtte teistest aruannetest |
| Kandidaadi analüüs   | Kandidaatide arv kokku, kandidaadid töö järgi, kandidaatide allikad, nais- ja meessoost kandidaatide suhtarv ning kandidaadid asukoha järgi |
| Kandidaadi olek     | Kandidaadid tüübi ja oleku järgi ning kandidaadi olek |
| Värbamise analüüs  | Palkamise netosuhe, palkamise keskmine päevade arv, halbade palkamiste protsent, värbamiskulud, värbamisprojektide arv, palkamiste ja kandideerimiste suhtarv ning kandidaatide arv vabade ametikohtade suhtes värbamisprojektide kaupa |

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt jaotisest [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Järgmises tabelis on näidatud üksused, millel **värbamise** Power BI sisu põhines.

| Üksus               | Sisu                                                         | Seosed teiste üksustega |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| Kandidaat            | Kandidaadid, palgatud kandidaadid, palkamise netosuhe ja kulud          | Kandidaadi nimi, ettevõte, kalendri tasakaalustus, kuupäev, geograafiline asukoht, demograafilised andmed, töö, meedia, värbamisprojekt |
| Kandidaadi nimi       | Kandidaadi eesnimi, perekonnanimi ja täielik nimi                   | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Kalendri tasakaalustus      | Kalendri tasakaalustused aruannete tükeldamiseks                                | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Ettevõte              | Ettevõtted, mille alusel aruandeid filtreerida                                   | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Kuupäev                 | Päevad, nädalad, kuud ja aastad                                   | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Demograafilised näitajad         | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis         | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Palgatud kandidaat   | Kandidaat, tulemused, alguskuupäev ja kandidaadi tüüp           | Ettevõte, kalendri tasakaalustus, kuupäev, geograafiline asukoht, kandidaadi nimi, töösuhe, tulemused, töö, meedia, värbamisprojekt |
| Tööhõive           | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                        | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Geograafiline asukoht  | Linn, maakond, sihtnumber ja osariik või provints                 | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Töö                  | Funktsioon, tüüp ja ametinimetus                                        | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Värbamisvahend                | Kandidaatide allikas                                             | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Jõudlus          | Hinnang, kirjeldus ja hinnangumudel                            | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Värbamisprojekt  | Projekti kirjeldus, projekti olek ja vabad ametikohad                | Kandidaat, palgatud kandidaat, lõpetatud kandidaat |
| Lõpetatud kandidaat | Lõpetatud kandidaadid, põhjus, tulemused ja lõpetamise kuupäev | Ettevõte, kalendri tasakaalustus, kuupäev, geograafiline asukoht, tulemused, demograafilised andmed, töösuhe, meedia, värbamisprojekt, kandidaadi nimi |

Neid üksusi kasutati arvutatud meetmete loomiseks. Seejärel kasutatakse neid arvutatud meetmeid sisus kasutatavate tulemuslikkuse võtmenäitajate (KPI-de) ja aruannete arvutamiseks. Aruannetesse ja armatuurlauale täiendavate arvutuste lisamiseks võite laadida teenusest Microsoft Dynamics Lifecycle Services (LCS) alla ja muuta faili Recruiting.pbix. See fail on vaikeandmemudel, mida kasutati sisu loomiseks. Kui muudatused on tehtud, saate luua organisatsiooni sisupaketi ja armatuurlaua, mis sisaldab teie lisatud teavet.

