---
title: Saadetiste konsolideerimine saadetise konsolideerimise töölaua abil
description: See artikkel sisaldab stsenaariumi, kus mitu tellimust vabastatakse lattu ja konsolideeritakse seejärel saadetisteks hiljem, kasutades saadetise konsolideerimise töölauale.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: db8dc5101b223a0033284d8e6c494721871809d8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335791"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Saadetiste konsolideerimine saadetise konsolideerimise töölaua abil

[!include [banner](../includes/banner.md)]

See artikkel sisaldab stsenaariumi, kus mitu tellimust vabastatakse lattu ja konsolideeritakse seejärel saadetisteks hiljem, kasutades saadetise konsolideerimise töölauale.

## <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle artikli stsenaarium viitab väärtustele ja kirjetele, mis sisalduvad Microsofti standardsetes demoandmetes Dynamics 365 Supply Chain Management. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine

Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed. Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.

## <a name="turn-the-manual-shipment-consolidation-feature-on-or-off"></a>Saadetise käsitsi konsolideerimise funktsiooni sisse- või väljalülitamine

Käsitsi saadetiste konsolideerimise kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul lülitatakse funktsioon vaikimisi sisse. Administraatorid saavad selle funktsiooni sisse või välja lülitada, otsides funktsioonihalduse *tööruumis* käsitsi saadetise [konsolideerimise](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funktsiooni.

Enne poliitikate *loomiseks* (tarneahela halduse versiooni 10.0.29 alusel on see funktsioon kohustuslik ja seda ei saa välja lülitada), peate ka konsolideeritud saadetise funktsiooni sisse lülitama. Lisateavet vt saadetise konsolideerimispoliitikate [konfigureerimine](configure-shipment-consolidation-policies.md).

## <a name="create-the-sales-orders-for-this-scenario"></a>Müügitellimuste loomine selle stsenaariumi jaoks

Alustage müügitellimuste kogumi loomisega, millega saate töötada. Peate töötama laoga, kus on lubatud täpsema laohalduse (WMS) protsessid. Kui pole konkreetselt viidatud mõnele muule laole, tuleb kasutada sama ladu kõigi järgmiste tellimuste kogumite puhul.

Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge müügitellimuste kogum, millel on järgmistes alamjaotistes kirjeldatud sätted.

### <a name="create-order-set-1"></a>Tellimuse komplekti 1 loomine

#### <a name="sales-orders-1-1-and-1-2"></a>Müügitellimused 1-1 ja 1-2

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-001*
    - **Tarneviis:** *Airwa-Air*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

#### <a name="sales-order-1-3"></a>Müügitellimus 1-3

1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Tarneviis:** *10*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.
1. Lisage teine järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0002* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*
    - **Tarneviis:** *Airwa-Air*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan teise tellimuserea reserveerimiseks **Reserveeri saatepartii**.

### <a name="create-order-set-2"></a>Tellimuse komplekti 2 loomine

#### <a name="sales-orders-2-1-and-2-2"></a>Müügitellimused 2-1 ja 2-2

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-002*
    - **Tarneviis:** *Airwa-Air*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *M9200* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Kergsüttiv*)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.
1. Lisage teine järgmiste sätetega tellimuserida.

    - **Kaubakood:** *M9201* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Lõhkeaine*)
    - **Kogus:** *1.00*
    - **Tarneviis:** *Airwa-Air*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan teise tellimuserea reserveerimiseks **Reserveeri saatepartii**.

### <a name="create-order-set-3"></a>Tellimuse komplekti 3 loomine

#### <a name="sales-orders-3-1-and-3-2"></a>Müügitellimused 3-1 ja 3-2

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-001*
    - **Kliendi ostutellimus:** *1*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

#### <a name="sales-orders-3-3-and-3-4"></a>Müügitellimused 3-3 ja 3-4

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-001*
    - **Kliendi ostutellimus:** *2*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

### <a name="create-order-set-4"></a>Tellimuse komplekti 4 loomine

#### <a name="sales-orders-4-1-and-4-2"></a>Müügitellimused 4-1 ja 4-2

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-003*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

#### <a name="sales-orders-4-3-and-4-4"></a>Müügitellimused 4-3 ja 4-4

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-004*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

#### <a name="sales-orders-4-5-and-4-6"></a>Müügitellimused 4-5 ja 4-6

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-007*
    - **Tegevuskoht:** *6*
    - **Ladu:** *61*
    - **Kaust:** *ShipCons*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

#### <a name="sales-orders-4-7-and-4-8"></a>Müügitellimused 4-7 ja 4-8

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-007*
    - **Tegevuskoht:** *6*
    - **Ladu:** *61*
    - **Kaust:** jätke väli tühjaks.

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

## <a name="release-the-orders-to-the-warehouse"></a>Väljastage tellimused lattu

Järgige neid etappe iga selle stsenaariumi jaoks loodud müügitellimuse väljastamiseks lattu.

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused**.
1. Otsige üles ja valige väljastatav müügitellimus.
1. Tehke Toimingupaani vahekaardil **Ladu** valik **Tegevused \> Vabasta lattu**, et väljastada valitud müügitellimus.
1. Korrake seda protseduuri kõigi selle stsenaariumi jaoks loodud müügitellimuste puhul.

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>Saadetiste konsolideerimine saadetise konsolideerimise töölaua abil

1. Avage jaotis **Laohaldus \> Lattu väljastamine \> Saadetise konsoldeerimise töölaud**.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Valige päringu redaktori dialoogiboksis vahekaardil **Vahemik** suvand  **Lisa**, et lisada järgmiste sätetega rida ruudustikule.

    - **Tabel:** *Müügitellimused*
    - **Väli:** *Müügitellimus*
    - **Kriteeriumid:** sisestage iga selle stsenaariumi jaoks loodud tellimusele komaeraldusega müügitellimuse numbrite loend.

1. Oma päringu salvestamiseks ja dialoogiboksi sulgemiseks valige **OK**.
1. Valige Toimingupaanil suvand **Saadetise konsolideerimine**.
1. Valige kõik saadetised ja valige Toimingupaanil suvand **Konsolideerimine**.

## <a name="verify-the-shipments"></a>Saadetiste kontrollimine

Järgmine protseduur võimaldab teil kontrollida saadetise konsolideerimise käigus loodud või värskendatud saadetisi. Kasutage seda iga selle stsenaariumi jaoks loodud tellimuse komplekti läbivaatamiseks ja vaadake üle järgnevad alamjaotised veendumaks, et saavutasite oodatud tulemused.

1. Avage **Laohaldus \> Saadetised \> Kõik saadetised**.
1. Otsige üles ja valige nõutav saadetis.
1. Kui saadetise loomise või värskendamise ajal kasutati konsolideerimispoliitikat, kasutage välja **Saadetise konsolideerimispoliitika**.

### <a name="related-shipments-for-order-set-1"></a>Tellimuse komplektiga 1 seostatud saadetised

Kaks saadetist peaks olema loodud.

- Esimene saadetis sisaldab kolme rida ja loodi saadetise konsolideerimispoliitika *CustomerMode* abil.
- Teine saadetis, mis ei kasuta transportimisel tarneviisi *Lennutransport*, loodi saadetise konsolideerimispoliitika *CustomerOrderNo* abil.

### <a name="related-shipments-for-order-set-2"></a>Tellimuse komplektiga 2 seostatud saadetised

Kolm saadetist peaks olema loodud.

- Esimene saadetis sisaldab *Kergsüttivaid* kaupu.
- Ülejäänud kaks saadetist sisaldavad ühte rida, millel on kaup *Lõhkeaine*.

### <a name="related-shipments-for-order-set-3"></a>Tellimuse komplektiga 3 seostatud saadetised

Kaks saadetist peaks olema loodud.

- Esimene saadetis sisaldab tellimuse ridu müügitellimuselt, kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*.
- Teine saadetis sisaldab tellimuse ridu müügitellimuselt, kus välja **Kliendi ostutellimus** väärtuseks on seatud *2*.

### <a name="related-shipments-for-order-set-4"></a>Tellimuse komplektiga 4 seostatud saadetised

Neli saadetist peaks olema loodud.

- Kliendi *USA-003* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.
- Kliendi *USA-004* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.
- Kliendi *USA-007* tellimuste 4-5 ja 4-6 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.
- Kliendi *USA-007* tellimuste 4-7 ja 4-8 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *CrossOrder* abil.

## <a name="additional-resources"></a>Lisaressursid

- [Saadetise konsolideerimispoliitikad](about-shipment-consolidation-policies.md)
- [Saadetise konsolideerimispoliitikate konfigureerimine](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]