---
title: Saadetiste konsolideerimine, kui lehel Lattu väljastamine alistatakse saadetise konsolideerimispoliitika
description: Selles teemas kirjeldatakse stsenaariumi, kus tuleb vähemalt üks müügirida väljastada lattu käsitsi lehe Lattu väljastamine kaudu ja enne väljastamist alistada süsteemi määratletud saadetise konsolideerimispoliitika.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 4aaaa7949d988607b38dd6e38a3c3497f227b8af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963331"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden-from-the-release-to-warehouse-page"></a>Saadetiste konsolideerimine, kui lehel Lattu väljastamine alistatakse saadetise konsolideerimispoliitika

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse stsenaariumi, kus tuleb vähemalt üks müügirida väljastada lattu käsitsi lehe **Lattu väljastamine** kaudu ja enne väljastamist alistada süsteemi määratletud saadetise konsolideerimispoliitika. Saadetiste konsolideerimispoliitika alistamine võib olla nõutav, kui näiteks tellimus, mida tavaliselt ei konsolideerita avatud saadetistega, tuleb konsolideerida avatud saadetistega.

Selle stsenaariumi käigus loote müügitellimuste komplekti ja seejärel alistate vaikimisi saadetise konsolideerimispoliitika enne tellimuste lattu väljastamist.

## <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle teema stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Saadetise konsolideerimispoliitikate ja tootefiltrite seadistamine

Siin kirjeldatud stsenaarium eeldab, et olete juba funktsiooni sisse lülitanud, sooritanud [saadetise konsolideerimispoliitikate konfigureerimise](configure-shipment-consolidation-policies.md) harjutused ning loonud poliitikad ja muud seal kirjeldatud kirjed. Veenduge, et olete enne selle stsenaariumi jätkamist sooritanud need harjutused.

## <a name="create-the-sales-orders-for-this-scenario"></a>Müügitellimuste loomine selle stsenaariumi jaoks

1. Avage jaotis **Müügireskontro \> Tellimused \> Kõik müügitellimused** ja looge kolm identset müügitellimust, millel on järgmised sätted.

    - **Kliendi konto:** *US-002*

1. Lisage järgmiste sätetega tellimuserida.

    - **Kaubakood:** *A0001* (kaup, millele pole määratud filtrit **Kood 4**)
    - **Kogus:** *1.00*

1. Valige **Varud \> Reserveerimine** ja seejärel valige paanil Toimingupaan tellimuserea reserveerimiseks **Reserveeri saatepartii**.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Müügitellimuste väljastamine lehelt Lattu väljastamine

Järgige neid juhiseid saadetise konsolideerimispoliitika alistamiseks lattu väljastamise ajal.

1. Avage jaotis **Laohaldus \> Lattu väljastamine \> Lattu väljastamine**.
1. Valige ülemisel paanil esimene selle stsenaariumi jaoks loodud müügitellimus.
1. Valige **Lisa**, et lisada rida lattu väljastamisele. Pange tähele, et *Vaikimisi* saadetise konsolideerimispoliitika rakendatakse alumisel paanil.
1. Valige alumisel paanil **Uue saadetise konsolideerimispoliitika valimine**.
1. Valige poliitika, mis lubab sama poliitika teiste avatud saadetiste konsolideerimist. Valige näiteks poliitika *CustomerOrderNo*.
1. Valige **Lattu väljastamine**.
1. Valige selle stsenaariumi jaoks loodud teine ja kolmas müügitellimus.
1. Valige **Lisa**, et lisada read lattu väljastamisele. Pange tähele, et *Vaikimisi* poliitika rakendatakse alumisel paanil.
1. Valige teine rida ja seejärel valige väljal **Uue saadetise konsolideerimispoliitika valimine** poliitika *CustomerOrderNo*.
1. Valige mõlemal real **Lattu väljastamine**.

## <a name="verify-the-shipments"></a>Saadetiste kontrollimine

Kaks saadetist peaks olema loodud.

- Esimene saadetis sisaldab kahte rida ja loodi saadetise konsolideerimispoliitika *CustomerOrderNo* abil.
- Teine saadetis sisaldab ühte rida ja loodi saadetise konsolideerimispoliitika *Vaikimisi* abil.

Loodud saadetiste ülevaatamiseks järgige neid etappe.

1. Avage **Laohaldus \> Saadetised \> Kõik saadetised**.
1. Otsige üles ja valige nõutav saadetis.
1. Vaadake väljal **Saadetise konsolideerimispoliitika** üle saadetise loomisel kasutatud konsolideerimispoliitika.

## <a name="additional-resources"></a>Lisaressursid

- [Saadetise konsolideerimispoliitikad](about-shipment-consolidation-policies.md)
- [Saadetise konsolideerimispoliitikate konfigureerimine](configure-shipment-consolidation-policies.md)
