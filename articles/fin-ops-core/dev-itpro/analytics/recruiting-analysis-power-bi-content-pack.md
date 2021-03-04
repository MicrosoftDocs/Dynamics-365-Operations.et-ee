---
title: Värbamise Power BI sisu
description: Selles teemas kirjeldatakse värbamise Power BI sisu. See selgitab ka seda, kuidas pääseda juurde aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 524b1c29d204c1b013546008b1be7868cbf8db06
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680558"
---
# <a name="recruiting-power-bi-content"></a>Värbamise Power BI sisu

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse **värbamise** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Värbamise** Power BI sisu kuvatakse tööruumis **Värbamise haldus**.

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>Aruanded ja visuaalid värbamise halduse tööruumis
Tööruum **Värbamise haldus** sisaldab vahekaarti **Analüüs**. Sellel vahekaardil on manustatud Power BI sisu värbamise jaoks. Sisu koosneb ülevaate vahekaardist ja täiendavatest andmeid sisaldavatest vahekaartidest. Järgmises tabelis on kirjeldatud iga vahekaardi aruandeid.

| Aruanne               | Sisu |
|----------------------|----------|
| Värbamise ülevaade | Teeb kokkuvõtte teistest aruannetest |
| Kandidaadi analüüs   | Kandidaatide arv kokku, kandidaadid töö järgi, kandidaatide allikad, nais- ja meessoost kandidaatide suhtarv ning kandidaadid asukoha järgi |
| Kandidaadi olek     | Kandidaadid tüübi ja oleku järgi ning kandidaadi olek |
| Värbamise analüüs  | Palkamise netosuhe, palkamise keskmine päevade arv, halbade palkamiste protsent, värbamiskulud, värbamisprojektide arv, palkamiste ja kandideerimiste suhtarv ning kandidaatide arv vabade ametikohtade suhtes värbamisprojektide kaupa |

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Järgmises tabelis on toodud **värbamise** Power BI sisu aluseks olevad üksused.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]