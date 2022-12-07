---
title: Skontod
description: Skontod seadistatakse ning neid ühiskasutatakse ostu- ja müügireskontroga.  Saadaolevat skontot saab määratleda kliendi- või hankija arve puhul ja see võetakse, kui arve tasutakse skonto kuupäeval.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: kfend
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b75637bfb38c13591223ff11be36d958b3972d4f
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804125"
---
# <a name="cash-discounts"></a>Skontod

[!include [banner](../includes/banner.md)]

Skontod seadistatakse ning neid ühiskasutatakse ostu- ja müügireskontroga. Saadaolevat skontot saab määratleda kliendi- või hankija arve puhul ja see võetakse, kui arve tasutakse skonto kuupäeval. 

## <a name="cash-discounts"></a>Skontod

Mõlema kliendi või hankija skontod saab luua skonto **leheküljel** . Järgmise allahindluskoodi välja abil saate määratleda ka **üksteisele** järgnevate skontokuupäevade aegumisjad. Lisateavet vt jaotisest "Näide: skonto seeria" (selles artiklis). Kui arve, kreeditkanne (kas makse või kreeditarve) või mõlemad sisestatakse muus valuutas kui juriidilise isiku arvestusvaluuta, arvutatakse skonto kreeditarve maksekuupäeval kehtiva vahetuskursi alusel. Kui arve ja kreeditarve sisestatakse erinevatele juriidilistele isikutele ja juriidiliste isikute arvestusvaluutad erinevad, võetakse vahetuskurss arve juriidiliselt isikult kreeditarve kuupäeva seisuga. Lisateavet vt jaotisest "Näide skonto vahetuskursside kohta" (selles artiklis).

## <a name="defaulting-order-of-cash-discount-main-account"></a>Skonto põhikonto vaiketegevuste järjestus

Kui arve on allahindluse saamiseks õigel ajal tasutud, sisestatakse allahindlus automaatselt skonto jaoks määratud põhikontole järgmiste vaikeprioriteetide alusel.
1.  Põhikonto on määratud alternatiivse **skonto konto väljal** kliendi avatud **kannete** tasakaalustamise lehel või lehel Hankija avatud **kannete tasakaalustamine** .
2.  Kliendi skonto väljal **või**  **arve** käibemaksukoodile määratud pearaamatu sisestusgrupi hankija skonto väljal määratud põhikonto. Seadistage pearaamatu sisestusgrupid pearaamatu **sisestamisgruppide** lehel ja määrake need käibemaksukoodide **lehekülje käibemaksukoodidele** .
3.  Skontolehe **·**  **·**  **põhikonto** on kas kliendi allahindluste põhikonto või tasakaalustatud arvel oleva skonto koodi puhul hankija allahindluste põhikonto.
4.  Skonto põhikonto, nagu määratud automaatsete kannete **lehel Kontode** jaoks.

## <a name="example-series-of-cash-discounts"></a> Näide: skontode seeriad
Seadistage kolm skontokoodi järgmiselt:
-   Kood 5D10% – allahindlus 10%, kui summa tasutakse 5 päeva jooksul.
-   Kood 10D5% – allahindlus 5%, kui summa tasutakse 10 päeva jooksul.
-   Kood 14D2% – allahindlus 2%, kui summa tasutakse 14 päeva jooksul.

Väljal Järgmine **allahindluskood** :
-   Koodi 5D10% puhul valige 10D5%.
-   Koodi 10D5% puhul valige 14D2%.
-   Koodi 14D2% puhul jätke väli Järgmine allahindluse kood tühjaks.

Kolm skontot järgnevad üksteisele, kui maksekuupäev ületab arve eelmise skonto kuupäeva. Arve maksmisel antakse ainult üks skonto, olenevalt sellest, milline skonto kuupäev skontode seerias kehtib.

## <a name="example-exchange-rates-for-cash-discounts"></a> Näide: skontode vahetuskursid
Teie juriidilise isiku arvestusvaluuta on euro ja USA dollarile on määratud järgmised vahetuskursid:
-   1. veebruar = 110
-   1. märts = 80

15. veebruaril sisestatakse arve 1000 USD skonto tingimustega 20D2%. Arve summa arvestusvaluutas on 1100 eurot. Makse summas 980 USA dollarit tasakaalustatakse arvega 1. märtsil. Skonto summa on 20 dollarit. Makse summa arvestusvaluutas on 784 eurot. Skonto summa arvestusvaluutas arvutatakse 1. märtsi vahetuskursiga: 20 \* 80 / 100 = 16 eurot.

> [!NOTE]
>  **Kui suvand Arvuta skontod**  **osaliste maksete jaoks on valitud müügireskontro parameetrites**  **või ostureskontro parameetrite lehtedel**, kasutatakse vahetuskurssi, mis kehtib iga osamakse kuupäeval. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
