---
title: Tasu Power BI sisu
description: Selles teemas kirjeldatakse tasu Power BI sisu. See selgitab ka seda, kuidas pääseda juurde aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.
author: jcart1106
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmCompensationWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 64b4f27b4a1fa3762169a18746c6b0933bddf3ca
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687177"
---
# <a name="compensation-power-bi-content"></a>Tasu Power BI sisu

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse **tasu** Microsoft Power BI sisu. See selgitab ka seda, kuidas pääseda juurde aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Tasu** Power BI sisu kuvatakse tööruumis **Tasuhaldus**, kui kasutate üht järgmistest toodetest:

- Finance and Operations rakendused
- Microsoft Dynamics 365 Human Resources

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad aruanded
**Tasu** Power BI sisusse kuuluvad aruanded sisaldavad nii lisateavet andvaid diagramme kui ka tabeleid. Järgmises tabelis on kirjeldatud aruandeid.

| Aruanne                     | Sisu |
|----------------------------|----------|
| Tasu ülevaade      | Teiste aruannete kokkuvõte |
| Tasu analüüs      | Ettevõtte tunni- ja kuupalgalised töötajad, töötajaid kokku tasuplaani alusel, mees- ja naistöötajad tasuplaani alusel ja töötajate tasu osakondade alusel |
| Ametikoha tasu analüüs      | Kõrgeim ja madalaim tunni- ja kuupalk, kõrgeima ja madalaima palgaga ametikohad ning täis- ja osalise ajaga ametikohad |
| Tasuplaani analüüs | Töövõtja liitumine valitud eelise järgi |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
**Tasu** Power BI sisus olevate aruannete täitmiseks kasutatakse järgmisi andmeid. Selles tabelis on toodud sisu aluseks olevad üksused.

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
