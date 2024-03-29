---
title: Saadetiste konsolideerimine koorma planeerimise töölaua suvandi Lattu väljastamine abil
description: See artikkel sisaldab stsenaariumi, kus mitu tellimust vabastatakse lattu samas koormas ja seejärel konsolideeritakse automaatselt saadetisteks.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 862b4b4121effa3ed0a2134924b2152c8a982110
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428086"
---
# <a name="consolidate-shipments-by-releasing-to-warehouse-from-the-load-planning-workbench"></a>Saadetiste konsolideerimine koorma planeerimise töölaua suvandi Lattu väljastamine abil

[!include [banner](../includes/banner.md)]

See artikkel sisaldab stsenaariumi, kus mitu tellimust vabastatakse lattu samas koormas ja seejärel konsolideeritakse automaatselt saadetisteks.

## <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle artikli stsenaarium viitab väärtustele ja kirjetele, mis sisalduvad Microsofti standardsetes demoandmetes Dynamics 365 Supply Chain Management. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine

Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed. Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.

## <a name="create-the-sales-orders-for-this-scenario"></a>Müügitellimuste loomine selle stsenaariumi jaoks

Alustage müügitellimuste kogumi loomisega, millega saate töötada. Peate töötama laoga, kus on lubatud täpsema laohalduse (WMS) protsessid. Kui pole konkreetselt viidatud mõnele muule laole, tuleb kasutada sama ladu kõigi järgmiste tellimuste kogumite puhul.

Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge müügitellimuste kogum, millel on järgmistes alamjaotistes kirjeldatud sätted.

### <a name="create-order-set-1"></a>Tellimuse komplekti 1 loomine

#### <a name="sales-order-1-1"></a>Müügitellimus 1-1

1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Tarneviis:** *Airwa-Air*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

#### <a name="sales-order-1-2"></a>Müügitellimus 1-2

1. Looge järgmiste sätetega müügitellimuse rida.

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

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a>Koorma planeerimise töölaua kasutamine koormate loomiseks ja lattu vabastamiseks

Järgige neid samme koormuse loomiseks igale selle stsenaariumi jaoks loodud tellimuse komplektile ja seejärel vabastage see lattu.

1. Avage **Laohaldus \> Koormused \> Koormuse plaanimise töölaud**.
1. Otsige üles ja valige vahekaardil **Müügiread** kõik müügitellimuse read ühest selle stsenaariumi jaoks loodud tellimuse komplektist.
1. Valige tegevusepaani vahekaardil **Pakkumine ja nõudlus** suvand **Lisa \> Uuele koormusele**, et lisada valitud tellimuseread uuele koormusele.
1. Valige dialoogiboksi **Koormuse malli määramine** väljal **Koormuse malli ID** koormuse mall, näiteks *Stnd koormuse mall*.
1. Valige dialoogiboksi sulgemiseks suvand **OK**. 
1. Otsige üles ja valige äsja loodud koormus jaotises **Koormused**.
1. Valitud koormuse lattu väljastamiseks valige **Väljasta \> Lattu väljastamine**.
1. Korrake seda protseduuri selle stsenaariumi jaoks loodud ülejäänud kolme tellimuse komplekti puhul.

## <a name="verify-the-shipments"></a>Saadetiste kontrollimine

Järgmine protseduur võimaldab teil kontrollida saadetise konsolideerimise käigus loodud või värskendatud saadetisi. Kasutage seda iga selle stsenaariumi jaoks loodud tellimuse komplekti läbivaatamiseks ja vaadake üle järgnevad alamjaotised veendumaks, et saavutasite oodatud tulemused.

1. Avage **Laohaldus \> Saadetised \> Kõik saadetised**.
1. Otsige üles ja valige nõutav saadetis.
1. Kui saadetise loomise või värskendamise ajal kasutati konsolideerimispoliitikat, kasutage välja **Saadetise konsolideerimispoliitika**.

### <a name="release-order-set-1-in-one-load"></a>1. tellimuse komplekti väljastamine ühes koormuses

Kaks saadetist peaks olema loodud.

- Esimene saadetis sisaldab kolme rida ja loodi saadetise konsolideerimispoliitika *CustomerMode* abil.
- Teine saadetis, mis ei kasuta transportimisel tarneviisi *Lennutransport*, loodi saadetise konsolideerimispoliitika *CustomerOrderNo* abil.

### <a name="release-order-set-2-in-one-load"></a>2. tellimuse komplekti väljastamine ühes koormuses

Kolm saadetist peaks olema loodud.

- Esimene saadetis sisaldab *kergsüttivaid* kaupu.
- Ülejäänud kaks saadetist sisaldavad ühte rida, millel on kaup *Lõhkeaine*.

### <a name="release-order-set-3-in-one-load"></a>3. tellimuse komplekti väljastamine ühes koormuses

Kaks saadetist peaks olema loodud.

- Esimene saadetis sisaldab tellimuse ridu müügitellimuselt, kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*.
- Teine saadetis sisaldab tellimuse ridu müügitellimuselt, kus välja **Kliendi ostutellimus** väärtuseks on seatud *2*.

### <a name="release-order-set-4-in-one-load"></a>4. tellimuse komplekti väljastamine ühes koormuses

Neli saadetist peaks olema loodud.

- Kliendi konto *USA-003* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.
- Kliendi konto *USA-004* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.
- Kliendi konto *USA-007* tellimuste 4–5 ja 4–6 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.
- Kliendi konto *USA-007* tellimuste 4–7 ja 4–8 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *CrossOrder* abil.

## <a name="additional-resources"></a>Lisaressursid

- [Saadetise konsolideerimispoliitikate ülevaade](about-shipment-consolidation-policies.md)
- [Saadetise konsolideerimispoliitikate konfigureerimine](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]