---
title: Töö pole blokeeritud
description: Töö pole blokeeritud
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6b4361682246397732e8326b98b1b86ff878664e54c8c352296b0d7eaff6bbbd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719547"
---
# <a name="work-isnt-blocked"></a>Töö pole blokeeritud

Tõrkekood: WHSUnblockNotBlockedWorkErrorMessage

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Töö ID-ga %1 pole blokeeritud.

## <a name="cause"></a>Põhjus

**Blokeeritud voo** suvand on seatud väärtusele *Ei*. Töö blokeeringut ei saa eemaldada, kuna see pole praegu blokeeritud.

## <a name="resolution"></a>Eraldusvõime

 Ainult tööl, mille **Blokeeritud voo** suvand on seatud valikule *Jah* saab blokeeringu eemaldada.
