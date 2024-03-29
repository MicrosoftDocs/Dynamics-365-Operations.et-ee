---
title: Asukohtade konfigureerimine WMS-loaga laos
description: See juhend näitab, kuidas konfigureerida asukoha seadistust uuele WMS-lubatud laole (ladu, mis kasutab laohaldusprotsesse (WMS)).
author: perlynne
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cce7ea0c06938d2ce038853a262f843ec76fe4c
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219654"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Asukohtade konfigureerimine LHS-i loaga laos

[!include [banner](../../includes/banner.md)]

See juhend näitab, kuidas konfigureerida asukoha seadistust uuele WMS-lubatud laole (ladu, mis kasutab laohaldusprotsesse (WMS)). Selle protsessiga tegeleb tavaliselt laohaldur. Saate seda juhendit käitada demoettevõtte USMF andmetega või oma andmetega. Eeltingimuseks on vähemalt üks konfigureeritud sait.


## <a name="create-a-new-warehouse"></a>Uue lao loomine
1. Avage **Navigeerimispaan > Moodulid > Varude haldus > Seadistus > Laovarude jaotamine > Laod**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Ladu**.
4. Sisestage väärtus väljale **Nimi**.
5. Väljal **Sait** valige või tippige olemasolev saidi väärtus.
6. Laiendage jaotist **Ladu**.
7. Valige suvandi **Kasuta laohaldusprotsesside valikut** sätteks Jah. See säte võimaldab teil käitada laohaldusprotsesse (WMS) laotöö ja mobiilsete seadmete abil.
8. Sulgege leht.

## <a name="define-a-location-format"></a>Asukohavormingu määratlemine
1. Avage **Navigeerimispaan >Moodulid > Laohaldus > Seadistus > Ladu > Asukohavormingud**. Asukoha vormingud on nimetamissüsteem, mida kasutatakse laos kasutatavatele kordumatutele ja järjepidevatele nimedele erinevate asukoha asukohakohtade jaoks. Asukohavormingus on kasulik kasutada eraldajaid, et hõlbustada asukoha komponentide, nagu riiulirea numbri, tuvastamist. Selles näites loome nelja komponendiga nime. Need võivad olla näiteks riiulirida, sektsioon, riiul ja koht.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Asukohavorming**.
4. Sisestage väärtus väljale **Nimi**.
5. Sisestage väärtus väljale **Segmendi kirjeldus**. See kirjeldab asukohanime esimest komponenti. See võib olla näiteks „Riiulirida”.
6. Sisestage arv väljale **Pikkus**. See määratleb, mitu tähemärki peab see asukohanime osa sisaldama. Pange tähele, et kõigi komponentide kohta kokku (koos eraldajatega) ei tohi nimi ületada 10 tärki.    
7. Sisestage väärtus väljale **Eraldaja**. See määratleb, millist märki või sümbolit kasutatakse nime esimese ja teise komponendi vahel.  
8. Klõpsake jaotises **Üksikasjad** valikut **Uus**.
9. Sisestage väärtus väljale **Segmendi kirjeldus**.
10. Sisestage arv väljale **Pikkus**.
11. Sisestage väärtus väljale **Eraldaja**.
12. Klõpsake jaotises **Üksikasjad** valikut **Uus**.
13. Sisestage väärtus väljale **Segmendi kirjeldus**.
14. Sisestage arv väljale **Pikkus**.
15. Sisestage väärtus väljale **Eraldaja**.
16. Klõpsake jaotises **Üksikasjad** valikut **Uus**.
17. Sisestage väärtus väljale **Segmendi kirjeldus**.
18. Sisestage arv väljale **Pikkus**.
19. Klõpsake valikut **Salvesta**.
20. Sulgege leht.

## <a name="define-location-types"></a>Asukohatüüpide määratlemine
1. Avage **Navigeerimispaan >Moodulid > Laohaldus > Seadistus > Ladu > Asukoha tüübid**. Asukohatüüpe saab kasutada filtreerimissuvanditena erinevate laohaldusprotsesside kontrollimiseks. Minimaalselt peate looma saadetise vahe- ja lõppasukoha tüübid laohalduse väljaminev protsessi määratlemiseks. 
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Asukoha tüüp**.
4. Sisestage väärtus väljale **Kirjeldus**.
5. Sulgege leht.

## <a name="define-location-profile"></a>Asukohaprofiili määratlemine
1. Avage **Navigeerimispaan >Moodulid > Laohaldus > Seadistus > Ladu > Asukoha profiilid**. Asukohaprofiilide määratlus on väga oluline. Siin saab kontrollida grupeeritud asukohtade koormust, samuti poliitikaid, mis on seotud sellega, milliseid varusid ja kuidas hoitakse. Asukohaprofiile saab kasutada filtreerimissuvanditena erinevate laohaldusprotsesside kontrollimiseks. WmS-i lubamiseks peate esmalt looma kasutaja asukoha profiili.
2. Klõpsake valikut **Uus**.
3. Väljale **Asukohaprofiili ID** sisestage väärtus.
4. Sisestage väärtus väljale **Nimi**.
5. Klõpsake väljal **Asukohavorming** otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake väljal **Asukoha tüüp** otsingu avamiseks ripploendi nuppu.
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake loendis valitud real olevat linki.
11. Valige või tühjendage märkeruut **Luba lao segaolekud**. Lubage see suvand, kui soovite lubada varude segaoleku väärtused asukohtades, mida grupeeritakse selle asukohaprofiili järgi. 
12. Valige või tühjendage märkeruut **Tühista partiipäevade reeglid**. Lubage see suvand, kui soovite tühistada reegli, mitu päeva võivad varude partii aegumiskuupäevad erineda, et lubada seda reeglit mittejärgivate varude partiide segamist.  
13. Valige või tühjendage märkeruut **Luba tsükliline inventuur**. Lubage see suvand, kui soovite lubada tsüklilise inventuuri töötlemise kõigis asukohtades, mida grupeeritakse selle asukohaprofiili järgi. 
14. Laiendage või ahendage jaotist **Dimensioonid**. Vahekaardil Dimensioonid saate määratleda parameetrid ja meetodid, millega võimaldada koormuse võimsuse täpsed arvutused igas asukohas.  
15. Sulgege leht.

## <a name="enable-warehouse-management-parameters"></a>Laohalduse parameetrite lubamine
1. Minge **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Laohalduse parameetrid**. Laotöö töötlemiseks peate määrama kasutaja asukohaprofiili parameetrid vaheasukoha tüüp ja saadetise lõppasukoha tüüp. Niipea, kui väljaminev protsess saadetise teie määratletud tüüpi lõppasukohas lõpeb, värskendatakse seotud väljaminevad kanded olekusse „Komplekteeritud”.
2. Jaotse **Asukoha profiilid** laiendamine või ahendamine.
3. Klõpsake väljal **Kasutaja asukoht** otsingu avamiseks ripploendi nuppu.
4. Klõpsake loendis valitud real olevat linki.
5. Jaotse **Asukoha tüübid** laiendamine või ahendamine.
6. Klõpsake väljal **Vaheasukoha tüübi koondamine** otsingu avamiseks ripploendi nuppu.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake väljal **Saadetise lõppsihtkoha tüüp** otsingu avamiseks ripploendi nuppu.
9. Klõpsake loendis valitud real olevat linki.
10. Sulgege leht.

## <a name="define-warehouse-zone-groups"></a>Laotsooni gruppide määratlemine
1. Avage **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Lao tsoonigrupid**. Laotsoone saab kasutada filtreerimissuvanditena erinevate laohaldusprotsesside kontrollimiseks. Enne tsooni määratlemist peate looma tsoonigrupi.   
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Tsoonigrupi ID**.
4. Sisestage väärtus väljale **Tsoonigrupi nimi**.
5. Sulgege leht.

## <a name="define-warehouse-zones"></a>Laotsoonide määratlemine
1. Avage **Navigeerimispaan >Moodulid > Laohaldus > Seadistus > Ladu > Tsoonid**.
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Tsooni ID**.
4. Sisestage väärtus väljale **Tsooni nimi**.
5. Klõpsake väljal **Tsoonigrupi ID** otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Sulgege leht.

## <a name="create-locations-using-the-location-setup-wizard"></a>Asukohtade loomine asukoha seadistusviisardi abil
1. Avage **Navigeerimispaan > Moodulid > Laohaldus > Seadistus > Ladu > Asukoha installiviisard**.
2. Väljal **Ladu** klõpsake ripploendi nuppu, et avada otsing.
3. Otsige loendist ja valige soovitud kirje.
4. Klõpsake loendis valitud real olevat linki.
5. Klõpsake väljal **Tsooni ID** otsingu avamiseks ripploendi nuppu.
6. Otsige loendist ja valige soovitud kirje.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake väljal **Asukohaprofiili ID** otsingu avamiseks ripploendi nuppu.
9. Otsige loendist ja valige soovitud kirje.
10. Klõpsake loendis valitud real olevat linki.
11. Märkige loendis valitud rida.
12. Sisestage number väljale **Alates numbrist**. Väljad Alates numbrist ja Kuni numbrini määratlevad loodavate asukohtade arvu. Näiteks kui määrate asukohavormingu kõigi nelja rea puhul välja Alates numbrist väärtuseks 1 ja välja Kuni numbrini väärtuseks 3, luuakse 81 välja (3 × 3 × 3 × 3).   
13. Sisestage number väljale **Kuni numbrini**.
14. Otsige loendist ja valige soovitud kirje.
15. Sisestage number väljale **Alates numbrist**.
16. Sisestage number väljale **Kuni numbrini**.
17. Otsige loendist ja valige soovitud kirje.
18. Sisestage number väljale **Alates numbrist**.
19. Sisestage number väljale **Kuni numbrini**.
20. Otsige loendist ja valige soovitud kirje.
21. Sisestage number väljale **Alates numbrist**.
22. Sisestage number väljale **Kuni numbrini**.
23. Klõpsake käsku Loo.

## <a name="create-locations-manually"></a>Asukohtade käsitsi loomine
1. Avage **Laohaldus > Seadistus > Ladu > Asukohad**. Asukohtade käsitsi loomine laos on lihtne. Väärtused asukoha nimi ja asukohaprofiili ID on kohustuslikud. 
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Ladu**.
4. Tippige väärtus väljale **Asukoht**. Pange tähele, et loote siin uue asukoha, seega peate sisestama uue kordumatu nime, mitte valima olemasoleva.
5. Väljale **Asukohaprofiili ID** sisestage väärtus.
6. Sulgege leht.

## <a name="define-pack-size-categories"></a>Pakendite suuruskategooriate määratlemine
1. Avage **Laohaldus > Seadistus > Ladu > Pakendisuuruse kategooriad**. Pakendite suuruskategooriaid saab kasutada sarnaste füüsiliste pakendisuurustega kaupade grupeerimiseks. Selles näites kasutatakse pakendi suuruskategooriat võimsuse juhtimiseks komplekteerimisasukohtades lao teatud tsooni piires. Pange tähele, et pakendi suuruskategooria ID peab olema määratud väljastatud tooteüksusele, et seda kasutada osana ladustamispiirangute töötlemisest.  
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Pakendisuuruse kategooria ID**.
4. Sisestage väärtus väljale **Pakendisuuruse kategooria nimi**.
5. Sulgege leht.

## <a name="define-location-stocking-limits"></a>Asukoha ladustamispiirangute määratlemine
1. Avage **Laohaldus > Seadistus > Ladu > Asukoha ladustamise piirangud**. Asukoha ladustamispiirangud aitavad tagada, et ei loodaks tööd, mis nõuab varude panemist asukohta, milles puudub varude kandmiseks vajalik füüsiline võimsus.  
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Ladu**.
4. Väljale **Asukohaprofiili ID** sisestage väärtus.
5. Sisestage väärtus väljale **Pakendisuuruse kategooria ID**.
6. Sisestage arv väljale **Kogus**.
7. Klõpsake valikut **Salvesta**.
8. Sulgege leht.

## <a name="define-fixed-picking-locations"></a>Fikseeritud komplekteerimiskohtade määratlemine
1. Avage **Laohaldus > Seadistus > Ladu > Fikseeritud asukohad**. Saate määratleda kasutatavad asukohad toote või tootevariandi kohta. Sama toote kohta samas laos on võimalik luua mitu fikseeritud asukohta.     
2. Klõpsake valikut **Uus**.
3. Sisestage väärtus väljale **Kaubakood**.
4. Sisestage väärtus väljale **Ladu**.
5. Klõpsake väljal **Asukoht** otsingu avamiseks ripploendi nuppu.
6. Klõpsake loendis valitud real olevat linki.
7. Sulgege leht.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
