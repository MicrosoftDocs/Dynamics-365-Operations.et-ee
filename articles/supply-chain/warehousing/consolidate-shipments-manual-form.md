---
title: Saadetiste käsitsi konsolideerimine saadetiste konsolideerimise lehe abil
description: Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust ja seejärel konsolideeritakse saadetiste konsolideerimise lehe abil.
author: GarmMSFT
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
ms.openlocfilehash: 0da98b24b9e0ab1ae19fd353ec226b2e0ab008fe
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/29/2021
ms.locfileid: "7574205"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Saadetiste käsitsi konsolideerimine saadetiste konsolideerimise lehe abil

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse stsenaariumi, kus lattu vabastatakse mitu tellimust ja seejärel konsolideeritakse lehe **Saadetiste konsolideerimine** abil.

## <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine

Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed. Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.

## <a name="create-the-sales-orders-for-this-scenario"></a>Müügitellimuste loomine selle stsenaariumi jaoks

Alustage müügitellimuste kogumi loomisega, millega saate töötada. Peate töötama laoga, kus on lubatud täpsema laohalduse (WMS) protsessid. Kui pole konkreetselt viidatud mõnele muule laole, tuleb kasutada sama ladu kõigi järgmiste tellimuste kogumite puhul.

Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge müügitellimuste kogum, millel on järgmistes alamjaotistes kirjeldatud sätted.

### <a name="create-sales-orders-1-and-2"></a>Looge müügitellimus 1 ja 2

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-007*
    - **Kaust:** *ShipCons*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

### <a name="create-sales-orders-3-and-4"></a>Looge müügitellimus 3 ja 4

1. Looge kaks identset müügitellimust järgmiste sätetega.

    - **Kliendi konto:** *US-007*
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

## <a name="consolidate-shipments"></a>Konsolideeri saadetised

1. Avage **Laohaldus \> Saadetised \> Kõik saadetised**.
1. Otsige üles ja valige saadetis, mis loodi 1. müügitellimuse väljastamisel lattu. (Selle välja **Saadetise konsolideerimispoliitika** väärtuseks olema seatud *Tellimuse kaust* .)
1. Valige toimingupaani vahekaardil **Saadetised** suvand **Saadetised \> Saadetiste konsolideerimine**.
1. Kinnitage konsolideerimiseks soovitatud saadetised. Konsolideerimiseks peaks olema soovitatud ainult üht sama poliitikaga saadetis.
1. Sulgege leht **Saadetise konsolideerimine**.
1. Otsige üles ja valige saadetis, mis loodi 3. müügitellimuse väljastamisel lattu. (Selle välja **Saadetise konsolideerimispoliitika** väärtuseks olema seatud *Vaikimisi* .)
1. Valige toimingupaani vahekaardil **Saadetised** suvand **Saadetised \> Saadetiste konsolideerimine**.
1. Kinnitage, et konsolideerimiseks pole soovitatud saadetisi.
1. Valige **Kuva filtrid**.
1. Eemaldage paanil **Filtrid** filter **Tellimuse number** ja seejärel valige **Rakenda**.
1. Kinnitage konsolideerimiseks soovitatud saadetised. Konsolideerimiseks peaks olema soovitatud ainult üht sama poliitikaga saadetis.

## <a name="additional-resources"></a>Lisaressursid

- [Saadetise konsolideerimispoliitikad](about-shipment-consolidation-policies.md)
- [Saadetise konsolideerimispoliitikate konfigureerimine](configure-shipment-consolidation-policies.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]