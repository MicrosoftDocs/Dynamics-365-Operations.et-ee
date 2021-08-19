---
title: Alustatud karantiinitellimuse kogust tellimuse jagamisel ei värskendata
description: Kui loote karantiinitellimuse ja proovite seda tükeldada, ei uuendata tellimuse kogust järelejäänud tükeldatud koguseks.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 4625570cb706199dca78f23b1864ca1d81cc66e896cf10d6d5f16cf1a9d1dc16
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713490"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Alustatud karantiinitellimuse kogust tellimuse jagamisel ei värskendata

KB number: 4613113

## <a name="symptoms"></a>Sümptomid

Kui loote karantiinitellimuse ja proovite seda tükeldada, ei uuendata tellimuse kogust pärast jagamist järelejäänud koguseks.

## <a name="resolution"></a>Eraldusvõime

Süsteem ei muuda karantiinikorralduse algset kogust, tagamaks, et saate jälgida selle vahelao orderi jaoks loodud algset kogust. Süsteem jälgib siiski karantiinitellimusest jagatud kogust. Selleks jälituse jaoks kasutab see andmebaasi välja nimega `QuantityThatHasSplitIntoOtherQuarantineOrders`. Kuid seda välja ei kuvata kasutajaliideses (UI).
