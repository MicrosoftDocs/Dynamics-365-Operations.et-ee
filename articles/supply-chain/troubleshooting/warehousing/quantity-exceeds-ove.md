---
title: Saadetist ei saa kinnitada, kuna kogus ületab ületarne protsendi
description: Saadetist ei saa kinnitada, kuna kogus ületab ületarne protsendi
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
ms.openlocfilehash: b25050572662afebbeaa39fa5a96e70cef618ac671dceba189fab1315480ede2
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755151"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a>Saadetist ei saa kinnitada, kuna kogus ületab ületarne protsendi

Tõrkekood: WAX1687

## <a name="symptoms"></a>Sümptomid

Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:

> Koorma saadetist %1 ei saanud kinnitada, kuna kauba kogus %2 ületab ületarne jaoks määratletud protsenti.

Seega ei saa te koorma saadetist kinnitada.

## <a name="cause"></a>Põhjus

Koorma või saadetise kogus on ainult osaliselt komplekteeritud. Praegu ületab kogus komplekteeritud kogust protsendi võrra, mis on väljaspool lubatud ületarne protsenti.

## <a name="resolution"></a>Eraldusvõime

Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

- Määrake laadimisliini kogus.
- Saate seadistada ületarne protsendi.

### <a name="set-the-load-line-quantity"></a>Määrake laadimisliini kogus

Koguse sätete määratlemiseks järgige neid samme.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab ületarne protsendi.
1. Kiirkaardil **Liini detailid** valige **Tellimus**.
1. Seadke väljal **Kogus** väärtus komplekteeritud kogusele (st **Tööga loodud kogus** väärtusele), et saadetise kinnitus saaks toimuda.

### <a name="set-the-overdelivery-percentage"></a>Saate seadistada ületarne protsendi

Alatarne protsendi määratlemiseks järgige neid samme.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige kiirkaardil **Koorma read** koorma rida kauba jaoks, mis ületab ületarne protsendi.
1. Kiirkaardil **Liini detailid** valige **Üldine**.
1. Seadke **Ületarne** väljal väärtus suuremale protsendile, mis rahuldab koorma koguse suhtes komplekteeritud kogust, nii et saadetise kinnitus on võimalik.
