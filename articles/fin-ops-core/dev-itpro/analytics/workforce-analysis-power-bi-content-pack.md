---
title: Tööjõu mõõdikute Power BI sisu
description: See artikkel kirjeldab Tööjõu meetermõõdulise sisu Power BI.
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.form: HcmWorkforceWorkspace
ms.openlocfilehash: 9d5c156eda3559394cb2723f0492b0ab575d815d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289812"
---
# <a name="workforce-metrics-power-bi-content"></a>Tööjõu mõõdikute Power BI sisu

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab **Tööjõu meetermõõdulise sisu** Microsoft Power BI. See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.

## <a name="accessing-the-power-bi-content"></a>Juurdepääs Power BI sisule
**Tööjõu mõõdikute** Power BI sisu kuvatakse tööruumis **Personalijuhtimine**, kui kasutate üht järgmistest toodetest:

- Microsoft Dynamics 365 Finantsid
- Microsoft Dynamics 365 Human Resources

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Power BI sisusse kuuluvad mõõdikud
Järgmine tabel loetleb igas aruandes kuvatavad mõõdikud.

| Aruanne                                           | Mõõdikud |
|--------------------------------------------------|---------|
| Inimeste mõõdikud                                   | Teiste aruannete kokkuvõte |
| Headcount Analysis Company, osakond, asukoht | Töötajate arv ettevõtte, osakonna ja asukoha järgi ning töötajate koguarv. |
| Töötajate koguarvu analüüsitöö, etapp, juhataja            | Töötajate arv töökoha, etapi ja halduri järgi ning töötajate koguarv |
| Töötajate koguarvu suundumuste analüüs                         | Töötajate koguarv sellel aastal vs eelmisel aastal ettevõtte järgi ja töötajate koondarv viimase 12 kuu kohta |
| TTE analüüs                                     | Täistööaja ekvivalent kokku (TTE), määratud TTE kokku, TTE osakondade kaupa, TTE viimase 12 kuu kohta ja TTE töö kohta |
| Tööjõu demograafilised andmed                           | Töötajate arv vanuse ja soo, etnilise päritolu, veteranistaatuse ja perekonnaseisu järgi, täiskohaga õpilaste arv, keskmine ametiaeg, keskmine vanus, naissoost ja meessoost töötajate suhtarv ning keeled, mida töötajad räägivad |
| Ametikohaanalüüs                                | Avatud ametikohad osakonna järgi, täitmiseks avatud ametikohad, aktiivsed kuni mitteaktiivsed ametikohad ja ametikohad osakonna järgi |
| Kinnipidamise analüüs                               | Kinnipidamine sellel aastal vs eelmisel aastal, kinnipidamine, lahkuvad töötajad vanuse ja soo järgi, lahkuvate töötajate keskmine ametiaeg, sel kuul lahkuvad töötajad ja lahkuvad töötajad põhjuse järgi |
| Inimesed osakonniti                             | Personalinumbriga töötajad osakonna, ametikoha ja määramise algus- ja lõppkuupäevade alusel |
| Staažianalüüs                               | Keskmine ametiaeg, keskmine tööaastate arv ettevõtte järgi ja staažiloend |
| Töötaja tähtpäevad                           | Tähtpäevi sellel kuul, tähtpäevi järgmisel kuul, töötajad tööaastate järgi ja tähtpäevad, tööaastad osakonna järgi |
| Töötajate sünnipäevad                               | Sünnipäevad sellel kuul, sünnipäevad järgmisel kuul, töötajate sünnipäevad ja sünnipäevad kuu ning osakonna järgi |
| Hulgivärbamisprojektid                               | Hulgivärbamisprojekte kokku, hulgivärbamisprojektid oleku järgi, hulgivärbamisprojektid osakonna ja omaniku järgi, hulgivärbamisprojektid töö järgi ja hulgivärbamisprojektid |

Saate neil aruannetel olevaid diagramme ja paane filtreerida ning kinnitada armatuurlauale. Lisateavet Power BI-s filtreerimise ja kinnitamise kohta vt teemast [Armatuurlaua loomine ja konfigureerimine](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards).

Laadige kindlasti alla **tööjõu mõõdikute** Power BI sisu, mis kehtib teie kasutatava Microsoft Dynamics 365 versiooni puhul.

> [!NOTE]
> Elutsükli teenustes saadaolevad .pbix-failid rakenduvad ainult finantside ja toimingute rakendustele.

## <a name="understanding-the-data-model-and-entities"></a>Andmemudelid ja üksused
Järgmises tabelis on toodud sisu aluseks olevad üksused.

| Üksus                   | Sisu                                                                            | Seosed teiste üksustega |
|--------------------------|-------------------------------------------------------------------------------------|-----------------------------------|
| Kalendri tasakaalustus          | Kalendri tasakaalustused aruannete tükeldamiseks                                                   | Varasem ametikoha määramine, ametikoha trend, töötaja trend, lõpetatud lepinguga töötaja |
| Ettevõte                  | Ettevõtted, mille alusel aruandeid filtreerida                                                      | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Praegune ametikoht         | Ametikohad tänase kuupäeva seisuga, TTE, avatud ametikohad ja täitmiseks avatud ametikohad | Töö, ametikoht |
| Praegune töötaja         | Töötajad tänase kuupäeva seisuga, vanus ja inimeste arv                                  | Ettevõte, geograafiline asukoht, töötaja nimi, otsene juht, töötaja ametinimetus, demograafilised andmed, töö, töösuhe, ametikoht |
| Kuupäev                     | Päevad, nädalad, kuud ja aastad                                                      | Varasem ametikoha määramine, ametikoha trend, lõpetatud lepinguga töötaja, töötaja trend |
| Demograafilised näitajad             | Sünnikuupäev, sugu, etniline päritolu ja perekonnaseis                            | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Tööhõive               | Alguskuupäev, lõppkuupäev ja ülemineku kuupäev                                           | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Geograafiline asukoht      | Linn, maakond, sihtnumber ja osariik või provints                                    | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Töö                      | Funktsioon, tüüp ja ametinimetus                                                           | Praegune ametikoht, praegune töötaja |
| Varasem ametikoha määramine | Määramise põhjus, alguskuupäev, lõppkuupäev ja töö                                    | Kalendri tasakaalustus, kuupäev, töö, ametikoht |
| Ametikoht                 | Osakond, TTE, ametikoht, ametikoha tüüp ja ametinimetus                                 | Praegune ametikoht, praegune töötaja |
| Ametikoha trend           | Ametikohad aja jooksul, TTE ja töö                                                   | Kalendri tasakaalustus, kuupäev, töö, ametikoht |
| Otsene juht               | Eesnimi, perekonnanimi ja täielik nimi                                                | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Lõpetatud lepinguga töötaja      | Lõpetatud lepinguga töötajad, lepingu lõpetamise kuupäev, ametinimetus, ametikoht ja töö                      | Ettevõte, geograafiline asukoht, töötaja nimi, otsene juht, kalendri tasakaalustus, kuupäev, töötaja ametinimetus, demograafilised andmed, töösuhe, töö, ametikoht |
| Töövõtja nimi            | Eesnimi, perekonnanimi ja täielik nimi                                                | Praegune töötaja, lõpetatud lepinguga töötaja, töötaja trend |
| Töötaja ametinimetus           | Ametinimetus ja staaži kuupäev                                                            | Praegune töötaja, lõpetatud, töötaja, töötaja trend |
| Töötaja trend           | Töötajad aja jooksul, inimeste arv, ettevõte ja ametikoht                                 | Ettevõte, geograafiline asukoht, töötaja nimi, otsene juht, kalendri tasakaalustus, kuupäev, töötaja ametinimetus, demograafilised andmed, töösuhe, töö |
| Hulgivärbamisprojekt        | Hulgivärbamisprojektide arv, projekti omanik ja projekti olek                     | Ettevõte, hulgivärbamise rida |
| Hulgivärbamise rida           | Osakond, töösuhte tüüp ja amet                                           | Kuupäev, töö, hulgivärbamisprojekt |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
