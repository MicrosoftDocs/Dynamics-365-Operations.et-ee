---
title: Saadetiste konsolideerimine, kui need väljastatakse lattu müügitellimuste automaatse väljastamise abil
description: Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust sama automaatse perioodilise lattu väljastamise protseduuri käigus.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 10c0b8b9478c8b31957cc08a1a827461c4621b8a
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574277"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a>Saadetiste konsolideerimine, kui need väljastatakse lattu müügitellimuste automaatse väljastamise abil

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust sama automaatse perioodilise lattu väljastamise protseduuri käigus. Tellimused konsolideeritakse saadetisteks automaatselt saadetiste konsolideerimispoliitikatena määratletud reeglite põhjal.

Selle stsenaariumi käigus loote müügitellimuste komplekti ja väljastate kõik komplektid lattu. Seejärel saate saadetise konsolideerimise käigus loodud või värskendatud saadetised nende konfigureeritud poliitikate põhjal üle vaadata.

## <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.

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

#### <a name="sales-order-1-2"></a>Müügitellimus 1-2

1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Tarneviis:** *Airwa-Air*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

#### <a name="sales-order-1-3"></a>Müügitellimus 1-3

1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Tarneviis:** *10*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Lisage teine järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0002* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*
    - **Tarneviis:** *Airwa-Air*

### <a name="create-order-set-2"></a>Tellimuse komplekti 2 loomine

#### <a name="sales-orders-2-1-and-2-2"></a>Müügitellimused 2-1 ja 2-2

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-002*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *M9200* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Kergsüttiv*)
    - **Kogus:** *1.00*

1. Lisage teine järgmiste sätetega tellimuserida.

    - **Kaubakood:** *M9201* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Lõhkeaine*)
    - **Kogus:** *1.00*
    - **Tarneviis:** *Airwa-Air*

### <a name="create-order-set-3"></a>Tellimuse komplekti 3 loomine

#### <a name="sales-order-3-1"></a>Müügitellimus 3-1

1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-002*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *M9200* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Kergsüttiv*)
    - **Kogus:** *1.00*

1. Lisage teine järgmiste sätetega tellimuserida.

    - **Kaubakood:** *M9201* (kaup, kus filtri **Kood 4** väärtuseks on seatud *Lõhkeaine*)
    - **Kogus:** *1.00*
    - **Tarneviis:** *Airwa-Air*

> [!NOTE]
> See tellimus on identne kahe tellimusega, mille lõite tellimuse komplekti 2 jaoks. Kuid see loetletakse eraldi tellimuse komplektina, kuna te väljastate selle hiljem antud stsenaariumi käigus.

### <a name="create-order-set-4"></a>Tellimuse komplekti 4 loomine

#### <a name="sales-order-4-1"></a>Müügitellimus 4-1

1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Kliendi ostutellimus:** *1*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

### <a name="create-order-set-5"></a>Tellimuse komplekti 5 loomine

#### <a name="sales-orders-5-1-and-5-2"></a>Müügitellimused 5-1 ja 5-2

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-001*
    - **Kliendi ostutellimus:** *2*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

#### <a name="sales-order-5-3"></a>Müügitellimus 5-3

1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Kliendi ostutellimus:** *1*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

### <a name="create-order-set-6"></a>Tellimuse komplekti 6 loomine

#### <a name="sales-orders-6-1-and-6-2"></a>Müügitellimused 6-1 ja 6-2

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-003*
    - **Kliendi ostutellimus:** *2*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Müügitellimused 6-3 ja 6-4

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-004*
    - **Kliendi ostutellimus:** *1*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Müügitellimused 6-5 ja 6-6

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-007*
    - **Tegevuskoht:** *6*
    - **Ladu:** *61*
    - **Kaust:** *ShipCons*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Müügitellimused 6-7 ja 6-8

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-007*
    - **Tegevuskoht:** *6*
    - **Ladu:** *61*
    - **Kaust:** jätke väli tühjaks.

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Müügitellimuste automaatne lattu väljastamine

Te viite lõpule automaatse lattu väljastamise protseduuri iga eelnevalt loodud müügitellimuste komplekti kohta. Viite kõigiga neist läbi siin esitatud [üldise lattu väljastamise protseduuri](#release-procedure).

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Üldine lattu väljastamise protseduur

Te viite lõpule kolm järgmistes alamjaotistes kirjeldatud protseduuri iga eelnevalt loodud müügitellimuste komplekti kohta.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Väljastamise ajal kasutatava voo malli värskendamine

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Määrake välja **Voo malli tüüp** väärtuseks *Lähetamine*.
1. Otsige üles ja valige voo mall, mis on seostatud laoga, mida kasutasite selle stsenaariumi jaoks loodud tellimuse komplektides. Kui kasutasite näiteks ladu *24*, valige voo mall **24 saadetise vaikemall**. Kui kasutasite ladu *61*, valige voo mall **61 saatmine**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Määrake suvandi **Töötle voogu lattu vabastamisel** väärtuseks *Ei*.

#### <a name="release-to-the-warehouse"></a>Lattu väljastamine

1. Avage jaotis **Laohaldus \> Lattu väljastamine \> Müügitellimuste automaatne väljastamine**.
1. Määrake välja **Väljastatav kogus** väärtuseks *Kõik*.
1. Päringu dialoogiboksi avamiseks valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**.
1. Valige vahekaardil **Vahemik** suvand **Lisa**, et lisada ruudustikule järgmiste sätetega rida.

    - **Tabel:** *Müügitellimus*
    - **Tuletatud tabel:** *Müügitellimus*
    - **Väli:** *Müügitellimus*
    - **Kriteeriumid:** sisestage soovitud tellimuse komplekti müügitellimuste numbrite komaeraldusega loend.

1. Päringu salvestamiseks klõpsake nuppu **OK**.
1. Protseduuri *Automaatne lattu väljastamine* käivitamiseks klõpsake nuppu **OK**.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Loodud või värskendatud saadetise ülevaatamine

1. Avage **Laohaldus \> Saadetised \> Kõik saadetised**.
1. Otsige üles ja valige nõutav saadetis.
1. Kui saadetise loomise või värskendamise ajal kasutati konsolideerimispoliitikat, kasutage välja **Saadetise konsolideerimispoliitika**.

### <a name="release-sales-orders-from-order-set-1"></a>Müügitellimuste väljastamine tellimuse komplektist 1

Müügitellimuste väljastamiseks tellimuse komplektist 1, järgige [üldist lattu väljastamise protseduuri](#release-procedure).

Kui olete lõpetanud, peaksite nägema, et loodi kaks saadetist.

- Esimene saadetis sisaldab kolme rida ja loodi saadetise konsolideerimispoliitika *CustomerMode* abil.
- Teine saadetis, mis ei kasuta transportimisel tarneviisi *Lennutransport*, loodi saadetise konsolideerimispoliitika *CustomerOrderNo* abil.

### <a name="release-sales-orders-from-order-set-2"></a>Müügitellimuste väljastamine tellimuse komplektist 2

Müügitellimuste väljastamiseks tellimuse komplektist 2, järgige [üldist lattu väljastamise protseduuri](#release-procedure).

Kui olete lõpetanud, peaksite nägema, et loodi kolm saadetist.

- Esimene saadetis sisaldab *Kergsüttivaid* kaupu.
- Ülejäänud kaks saadetist sisaldavad ühte rida, millel on kaup *Lõhkeaine*.

### <a name="release-sales-orders-from-order-set-3"></a>Müügitellimuste väljastamine tellimuse komplektist 3

Müügitellimuste väljastamiseks tellimuse komplektist 3, järgige [üldist lattu väljastamise protseduuri](#release-procedure).

Kui olete lõpetanud, peaksite nägema, et ilmnesid järgmised tegevused.

- Värskendati üks olemasolev saadetis (saadetis, mis loodi tellimuse komplekti 2 väljastamisel lattu). Lisati rida, millel on *Kergsüttiv* kaup.
- Loodi üks uus saadetis, mis sisaldab kaupa *Lõhkeaine*.

### <a name="release-sales-orders-from-order-set-4"></a>Müügitellimuste väljastamine tellimuse komplektist 4

Müügitellimuste väljastamiseks tellimuse komplektist 4, järgige [üldist lattu väljastamise protseduuri](#release-procedure).

Kui olete lõpetanud, peaksite nägema, et värskendati üks olemasolev saadetis (kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*). Sellele lisati üks uus rida.

### <a name="release-sales-orders-from-order-set-5"></a>Müügitellimuste väljastamine tellimuse komplektist 5

Müügitellimuste väljastamiseks tellimuse komplektist 5, järgige [üldist lattu väljastamise protseduuri](#release-procedure).

Kui olete lõpetanud, peaksite nägema, et ilmnesid järgmised tegevused.

- Värskendati üks olemasolev saadetis (kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*). Sellele lisati rida müügitellimusest 5-3 (kus välja **Kliendi ostutellimus** väärtuseks on seatud *1*).
- Loodi üks uus saadetis, kus müügitellimuste 5-1 ja 5-2 read grupeeritakse ühte saadetisse.

### <a name="release-sales-orders-from-order-set-6"></a>Müügitellimuste väljastamine tellimuse komplektist 6

Müügitellimuste väljastamiseks tellimuse komplektist 6, järgige [üldist lattu väljastamise protseduuri](#release-procedure).

Kui olete lõpetanud, peaksite nägema, et loodi neli saadetist.

- Kliendi *USA-003* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.
- Kliendi *USA-004* kahe tellimuse read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.
- Kliendi *USA-007* tellimuste 6-5 ja 6-6 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *Tellimuse kaust* abil.
- Kliendi *USA-007* tellimuste 6-7 ja 6-8 read grupeeriti ühte saadetisse saadetise konsolideerimispoliitika *CrossOrder* abil.

## <a name="additional-resources"></a>Lisaressursid

- [Saadetise konsolideerimispoliitikad](about-shipment-consolidation-policies.md)
- [Saadetise konsolideerimispoliitikate konfigureerimine](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]