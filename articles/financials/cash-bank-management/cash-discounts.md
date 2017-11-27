---
title: Skontod
description: "Skontod seadistatakse ning neid ühiskasutatakse ostu- ja müügireskontroga.  Saadaolevat skontot saab määratleda kliendi- või hankija arve puhul ja see võetakse, kui arve tasutakse skonto kuupäeval."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9960af8c4961a42e7e829077da40bcbbf3bc71c2
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="cash-discounts"></a>Skontod

[!include[banner](../includes/banner.md)]


Skontod seadistatakse ning neid ühiskasutatakse ostu- ja müügireskontroga.  Saadaolevat skontot saab määratleda kliendi- või hankija arve puhul ja see võetakse, kui arve tasutakse skonto kuupäeval. 

<a name="cash-discounts"></a>Skontod
--------------

Lehel Skontod saab luua skontosid nii klientidele kui ka hankijatele. Saate määratleda välja Järgmine allahindluse kood abil ka eelnevate skontokuupäevade möödumisel üksteisele järgnevate skontode seeria. Lisateavet leiate selle teema osast „Näide: skontoseeriad”. Kui arve, kreeditkanne (kas makse või kreeditarve) või mõlemad sisestatakse muus valuutas kui juriidilise isiku arvestusvaluuta, arvutatakse skonto kreeditarve maksekuupäeval kehtiva vahetuskursi alusel. Kui arve ja kreeditarve sisestatakse erinevatele juriidilistele isikutele ja juriidiliste isikute arvestusvaluutad erinevad, võetakse vahetuskurss arve juriidiliselt isikult kreeditarve kuupäeva seisuga. Lisateavet leiate selle teema osast „Näide: skontode vahetuskursid”.
Skonto põhikonto vaiketegevuste järjestus
----------------------------------------------

Kui arve on allahindluse saamiseks õigel ajal tasutud, sisestatakse allahindlus automaatselt skonto jaoks määratud põhikontole järgmiste vaikeprioriteetide alusel.
1.  Põhikonto, mis on määratud kliendi lehe Avatud kannete tasakaalustamine või hankija lehe Avatud kannete tasakaalustamine väljal Alternatiivne skonto.
2.  Põhikonto määratakse arve käibemaksukoodiga määratud pearaamatu sisestamisgrupi väljal Kliendi skonto või Hankija skonto. Saate seadistada lehel Pearaamatu sisestusgrupid pearaamatu sisestusgruppe ja määrata neid käibemaksukoodidele lehel Käibemaksukoodid.
3.  Tasakaalustatud arvel oleva skonto koodi peamine sisestuskonto lehel Skontod väljal Kliendi allahindluste põhikonto või Hankija allahindluste põhikonto.
4.  Lehel Automaatsete kannete kontod määratletud skontode põhikonto.

## <a name="example-series-of-cash-discounts"></a> Näide: skontode seeriad
Seadistage kolm skontokoodi järgmiselt:
-   Kood 5D10% – allahindlus 10%, kui summa tasutakse 5 päeva jooksul.
-   Kood 10D5% – allahindlus 5%, kui summa tasutakse 10 päeva jooksul.
-   Kood 14D2% – allahindlus 2%, kui summa tasutakse 14 päeva jooksul.

Tehke väljal Järgmine allahindlus järgmist.
-   Koodi 5D10% puhul valige 10D5%.
-   Koodi 10D5% puhul valige 14D2%.
-   Koodi 14D2% puhul jätke väli Järgmine allahindluse kood tühjaks.

Kolm skontot järgnevad üksteisele, kui maksekuupäev ületab arve eelmise skonto kuupäeva. Arve maksmisel antakse ainult üks skonto, olenevalt sellest, milline skonto kuupäev skontode seerias kehtib.

## <a name="example-exchange-rates-for-cash-discounts"></a> Näide: skontode vahetuskursid
Teie juriidilise isiku arvestusvaluuta on euro ja USA dollarile on määratud järgmised vahetuskursid:
-   1. veebruar = 110
-   1. märts = 80

15. veebruaril sisestatakse arve 1000 USD skonto tingimustega 20D2%. Arve summa arvestusvaluutas on 1100 eurot. Makse summas 980 USA dollarit tasakaalustatakse arvega 1. märtsil. Skonto summa on 20 dollarit. Makse summa arvestusvaluutas on 784 eurot. Skonto summa arvestusvaluutas arvutatakse 1. märtsi vahetuskursiga: 20 \* 80 / 100 = 16 eurot.
| **Märkus**                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kui lehel Müügireskontro parameetrid või Ostureskontro parameetrid on tehtud valik Arvuta skontod osaliste maksete jaoks, kasutatakse iga osamakse kuupäeval kehtivat vahetuskurssi. |

 
=

 




