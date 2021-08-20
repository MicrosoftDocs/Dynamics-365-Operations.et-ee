---
title: Koondplaneerimise tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada koondplaneerimisega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4dc3c5c8a1597fce4cc61461d16cd11ad80426eb8841871278772fcd7b8c86b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766627"
---
# <a name="troubleshoot-master-planning"></a>Koondplaneerimise tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada koondplaneerimisega töötamisel tekkivaid probleeme.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Koosluse tükeldamine käitub erinevalt kinnitatud tootmistellimustest ja plaanitud tootmistellimustest käsitsi loodud töö jaoks.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui tootmistellimus on kinnitatud, ei tükeldata kaupu koosluse tükeldamisel. Kuid kui loote käsitsi töötellimuse ja seejärel hindate tootmistellimuse, siis kaubad tükeldatakse.

### <a name="issue-resolution"></a>Probleemi lahendamine

Süsteem töötab ootuspäraselt. Tükeldamine, mis ilmneb tootmistellimuse kinnitamisel, osutab plaanitud tellimusele, kuid ei ilmne, et plaanitud tellimus on praegu selles juhtumis kinnitatud. Kui tootmistellimus on hinnatud, käivitatakse tükeldamine vabastatud tootmistellimuselt, kus pole plaanitud tellimust.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Viivituse väärtust ei uuendata, kui plaanin plaanitud tellimust uuesti planeerida.

Plaanitud tellimuste viivituse uuendamiseks avage planeeritud tellimuse **Ümberplaneerimine** dialoogiaken. Veenduge, et FastTabil **Tükeldamine** oleks suvandi **Teosta tükeldamine pärast ümberplaneerimist** väärtuseks seatud *Jah*.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Tootmise planeerimisel ei arvestata ohutusvaru, mis on seatud kauba laovarule fikseeritud tarne puhul.

### <a name="issue-description"></a>Probleemi kirjeldus

Koondplaneerimine vaatleb ohutusvaru. Siiski eiratakse ohutusvaru plaanitud tootmistellimuste planeerimisel.

### <a name="issue-resolution"></a>Probleemi lahendamine

Marginaale arvestatakse ainult koondplaneerimise käigus, mitte käsitsi planeerimisel. Veerised on kavandatud toimima puhvrina planeerimise faasis, et anda osa "marginaali" tegeliku protsessi jaoks.

Soovitud tulemuse saamiseks saate marginaali eemaldada. Seejärel tuleb protsessi uuendada nii, et see sisaldaks soovitud kellaaega (nt ooteaeg). Nii koondplaneerimine kui ka käsitsi planeerimine peaksid seejärel esitama sama tulemuse.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Plaanitud tellimused luuakse ka siis, kui meil on laos ja tootmistellimustes kaubad juba olemas.

Võimalik, et saate selle probleemi lahendada, suurendades vastavate gruppide **Positiivsete päevade** väärtust **Laovarude grupi** lehel. See muudatus paneb süsteemi määratlema, kas vaba kaubavaru saab nõudluse jaoks kasutada. Seejärel ei looda laos olevate kaupade jaoks uut plaanitud tellimust.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Koondplaneerimise käigus ei arvestata võimsuse piiranguid ja planeeritakse rohkem kui saadaolev võimsus.

### <a name="issue-description"></a>Probleemi kirjeldus

Kui kasutate operatsiooni planeerimist, kus on piiratud võimsus ja kui protsess määrab nii ressursirühma kui ka üksikute ressursside jaoks nõuete kombinatsiooni, on väike võimalus üle broneerida, kuna algoritm kontrollib võimsuse konflikte. See ülebroneerimine võib ilmneda, kui kasutate koondplaneerimise käivitamiseks abilisi. See on kõige tõenäolisem juhul, kui on palju töid, millel on suhteliselt lühike käitusaeg.

### <a name="issue-resolution"></a>Probleemi lahendamine

Kui on oluline, et operatsiooni planeerimisel ei esineks ülebroneerimist, saate koondplaneerimise planeerimisosa muuta ühekordseks, lülitades sisse **Täpne piiratud võimsus operatsiooni planeerimiseks** valiku **Koondplaneerimise parameetrite** lehel. See valik pole vaikimisi saadaval. Peate selle lehele käsitsi lisama, kasutades isikupärastamise funktsioone. Selle suvandi kasutamisel toimub planeerimine aeglasemalt, kuna puudub paralleelne töötlemine.

## <a name="planned-orders-take-a-long-time-to-update"></a>Plaanitud tellimused võtaksid uuendamiseks kaua aega.

### <a name="issue-description"></a>Probleemi kirjeldus

Plaanitud tellimuse vajaduse koguse ja/või tarnekuupäeva uuendamisel võtab see tavaliselt aega vähemalt 30 sekundit, et värskendust salvestada.

### <a name="issue-resolution"></a>Probleemi lahendamine

See on teadaolev probleem sisseehitatud koondplaneerimise mootoriga. Selle põhjuseks on aluseks olev automaatne tükeldamine koosluse struktuuri kaudu redigeerimisel. Seda probleemi käsitletakse planeerimise optimeerimisel, kus planeerija saab vastavaid tellimusi värskendada ja kinnitada ning soovi korral käivitab planeerimise käivitamise, et värskendada aluseks oleva koosluse struktuuri jaoks plaanitud tellimusi.

Üks viis jõudluse parandamiseks sisseehitatud koondplaneerimise mootoriga on teha järgmist:

1. Avage **Koondplaneerimine \> Seadistus \> Plaanid \> Koondplaanid**.
1. Valige plaan.
1. Laiendage **Ajapiir päevades** FastTab.
1. Seadke **Tükeldamine** väärtusele *Jah* ja seadke selle sätte all oleva välja väärtuseks 0 (null).

> [!NOTE]
> See piirab selle koondplaani jaoks teostatavate tükeldamiste perioodi ühele päevale.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]