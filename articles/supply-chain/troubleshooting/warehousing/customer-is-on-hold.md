---
title: Saadetist ei saa kinnitada, kuna klient ootab
description: Saadetist ei saa kinnitada, kuna klient ootab.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 801778fc8f04b106bf168a3dcd5a89767a837740
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344260"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Saadetist ei saa kinnitada, kuna klient ootab

Tõrkekood: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Sümptomid

Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:

> Saadetist %1 ei saa kinnitada, sest klient on üksuse %2 ootel.

Seega ei saa te koorma saadetist kinnitada.

## <a name="cause"></a>Põhjus

Koorma või saadetise kliendikonto on ootel. Seetõttu takistab kliendi olek saadetise kinnitamist.

## <a name="resolution"></a>Lahendus

Kliendi konto blokeeringu tühistamiseks kasutage järgmist protseduuri.

1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
1. Avage kliendikonto, mille saadetist ei saa kinnitada.
1. Seadke kiirkaardi **Kreedit ja sissenõuded** väli **Arveldamine ja tarne ootel** olekusse *Ei*.
1. Korrake seda toimingut kõigi blokeeritud klientide puhul.
