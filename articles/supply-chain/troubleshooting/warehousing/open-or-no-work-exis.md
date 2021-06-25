---
title: Saadetist ei saa kinnitada lõpetamata või puuduva töö tõttu
description: Saadetist ei saa kinnitada lõpetamata või puuduva töö tõttu
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: beef0909d41e69f3e7bcc1021527be35b7e6fd44
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123839"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Saadetist ei saa kinnitada lõpetamata või puuduva töö tõttu

Tõrkekood: WAX515

## <a name="symptoms"></a>Sümptomid

Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:

> Koorma %1 saadetist ei saanud kinnitada, kuna kogu koorma töö peab olema lõpetatud.

Seega ei saa te koorma saadetist kinnitada.

## <a name="cause"></a>Põhjus

Koorem või saadetis on praegu olekus, kus saadetise kinnitamine nurjub. Enne saadetise kinnitamist peab koorma jaoks olema vähemalt üks töö ja kogu selle töö olek peab olema kas *Suletud* või *Tühistatud*.

## <a name="resolution"></a>Eraldusvõime

Kontrollige koorma või saadetisega seotud müügitellimusi või üleviimistellimusi ja veenduge, et kogu seotud töö on lõpule viidud või tühistatud.

Saate töötada saadetiste ja koormatega mitmel lehel. Järgmised alamjaotised pakuvad mõnda näidet.

### <a name="all-loads-page"></a>Kõigi koormate leht

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Toimingupaani vahekaardil **Ladu** grupis **Seotud teave** valige **Töö**.
1. Kontrollige iga töö ID olekut. Jälgige kõiki töö ID-sid, mille olek ei ole *Suletud* või *Tühistatud*.
1. Kui iga töö ID olek on *Suletud* või *Tühistatud*, proovige saadetist uuesti kinnitada.

### <a name="all-shipments-page"></a>Kõigi saadetiste leht

1. Avage **Laohaldus \> Saadetised \> Kõik saadetised**.
1. Valige saadetis, mida ei saa kinnitada.
1. Valige toimingupaani vahekaardil **Saadetised** grupis **Töö** üksus **Töö üksikasjad**.
1. Kontrollige iga töö ID olekut. Jälgige kõiki töö ID-sid, mille olek ei ole *Suletud* või *Tühistatud*.
1. Kui iga töö ID olek on *Suletud* või *Tühistatud*, proovige saadetist uuesti kinnitada.

### <a name="all-work-page"></a>Kõigi tööde leht

1. Avage jaotis **Laohaldus \> Töö \> Kõik tööd**.
1. Valige töö tellimuse numbriga, mille jaoks ei saa saadetist kinnitada.
1. Paani tegumiriba vahekaardil **Tarne** grupis **tarne** valige suvand **Kinnita tarne**.
1. Kontrollige iga töö ID olekut. Jälgige kõiki töö ID-sid, mille olek ei ole *Suletud* või *Tühistatud*.
1. Kui iga töö ID olek on *Suletud* või *Tühistatud*, proovige saadetist uuesti kinnitada.
