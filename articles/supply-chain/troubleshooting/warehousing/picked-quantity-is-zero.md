---
title: Saadetist ei saa kinnitada, kuna kogus on null
description: Saadetist ei saa kinnitada, kuna kogus on null
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938454"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Saadetist ei saa kinnitada, kuna kogus on null

Tõrkekood: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Sümptomid

Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:

> Kauba %1 ja saadetise %2 koormarida on värskendatud nullkogusele, kuna alatarne häälestus ei luba selle kauba jaoks ükskõik millises koguses saadetisi.

Seega ei saa te koorma saadetist kinnitada.

## <a name="cause"></a>Põhjus

Süsteem hindab, kas komplekteeritud kogus jääb oodatud piiridesse, võttes aluseks komplekteeritud koguse, koormarea koguse ja alatarne protsendi. Kui süsteem leiab, et komplekteeritud kogus koormareal on 0 (null), ei saa saadetist kinnitada. Näiteks võib see probleem ilmneda, kui töö on tühistatud ja koormarea alatarne protsent on 100 protsenti.

## <a name="resolution"></a>Eraldusvõime

Kontrollige koorma ridu veendumaks, et alatarnete protsent ja kogused on joondatud komplekteeritud tööga.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab alatarne protsendi.
1. Korrigeerige välja **Alatarne** väärtust või välja **Kogus** vastavalt vajadusele.

> [!TIP]
> Kui probleem pole ikka veel lahendatud, peate lõpule viima rohkem komplekteerimistööd seotud müügitellimustes või üleviimistellimustes kuni saadav kogus on koorma või saadetisega joondatud.
