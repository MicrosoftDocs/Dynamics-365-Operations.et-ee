---
title: Saadetist ei saa kinnitada, kuna kogus ületab alatarne protsendi
description: Saadetist ei saa kinnitada, kuna kogus ületab alatarne protsendi
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123815"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>Saadetist ei saa kinnitada, kuna kogus ületab alatarne protsendi

Tõrkekood: WAX1686

## <a name="symptoms"></a>Sümptomid

Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:

> Koorma saadetist %1 ei saanud kinnitada, kuna kauba kogus %2 ületab alatarne jaoks määratletud protsenti.

Seega ei saa te koorma saadetist kinnitada.

## <a name="cause"></a>Põhjus

Koorma või saadetise kogus on ainult osaliselt komplekteeritud. Kogus on praegu valitud kogusest väiksem protsentides, mis jääb väljapoole lubatud alatarnimise protsenti.

## <a name="resolution"></a>Eraldusvõime

Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Määrake laadimisliini kogus.
- Saate seadistada alatarne protsendi.

### <a name="set-the-load-line-quantity"></a>Määrake laadimisliini kogus

Koguse sätete määratlemiseks järgige neid samme.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab alatarne protsendi.
1. Kiirkaardil **Liini detailid** valige **Tellimus**.
1. Seadke väljal **Kogus** väärtus komplekteeritud kogusele (st **Tööga loodud kogus** väärtusele), et saadetise kinnitus saaks toimuda.

### <a name="set-the-underdelivery-percentage"></a>Saate seadistada alatarne protsendi

Alatarne protsendi määratlemiseks järgige neid samme.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab alatarne protsendi.
1. Kiirkaardil **Liini detailid** valige **Üldine**.
1. Seadke **Alatarne** väljal väärtus suuremale protsendile, mis rahuldab koorma koguse suhtes komplekteeritud kogust, nii et saadetise kinnitus on võimalik.
