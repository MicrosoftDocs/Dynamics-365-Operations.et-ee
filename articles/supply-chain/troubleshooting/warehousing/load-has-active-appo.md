---
title: Saadetist ei saa kinnitada kalendri probleemi tõttu
description: Saadetist ei saa kinnitada kalendri probleemi tõttu
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
ms.openlocfilehash: f1fccd10d8867252f32b37c77f9a3bad54157bdd
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938457"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Saadetist ei saa kinnitada kalendri probleemi tõttu

Tõrkekood: TRX2716

## <a name="symptoms"></a>Sümptomid

Kui proovite saadetist kinnitada, näitab süsteem järgmist tõrketeadet:

> Kalendri tüübi %1 puhul tuleb kohtumine %2 sisse ja välja registreerida.

Seega ei saa te koorma saadetist kinnitada.

## <a name="cause"></a>Põhjus

Koorma jaoks on aktiivsed kohtumised. Näiteks on olemas reegel, mis nõuab juhi sisseregistreerimist. Seetõttu on koorem praegu olekus, kus saadetise kinnitamine nurjub.

## <a name="resolution"></a>Eraldusvõime

Peate uurida ja lahendama kõik koormaga seotud aktiivsete kohtumistega seotud probleemid.

1. Avage **Laohaldus \> Koormad \> Kõik koormad**.
1. Valige koorem, mille jaoks ei saa saadetist kinnitada.
1. Valige tegevuspaanil vahekaardil **Transport** grupis **Kohtumised** suvand **Kohtumise määramine**.
1. Järgige üht neist sammudest.

    - Veenduge, et juhi sisse- ja väljaregistreerimine oleks kohtumise jaoks lõpetatud.
    - Lõpetage või tühistage kohtumine.
    - Keelake seotud kohtumise reegli jaoks suvand **juhi sisseregistreerimine nõutav**.
