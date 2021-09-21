---
title: Ostutellimuse sissetulek ei sisalda kõiki tasusid
description: Ostutellimuse sissetulek ei sisalda kõiki tasusid
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: bb567e00ef52269db0dc866148a37c73f0a9827c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476078"
---
# <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a>Ostutellimuse sissetulek ei sisalda kõiki tasusid

## <a name="symptoms"></a>Sümptomid

Ostutellimuse saamisel ei kaasata sissetulekusse kõiki tasusid.

### <a name="reproduce-the-issue"></a>Probleemi taastekitamine

Järgmine protsess näitab üht viisi probleemi taastekitamiseks.

1. Veenduge, et lehe **Hankeparameetrid** vahekaardil **Tarne** oleks suvandi **Loo toote sissetuleku kulud** väärtuseks seatud *Jah*.
1. Looge ostutellimus, mis sisaldab kulusid.
1. Kinnitage ostutellimus.
1. Võtke ostutellimus vastu.
1. Vaadake sissetuleku kogusummat ja võrrelge seda oodatud kogusummaga.
1. Pange tähele, et ostutellimuse sissetulek ei sisalda kõiki kulusid.

## <a name="resolution"></a>Lahendus

Lahendus sõltub sellest, kuidas lisakulud on seadistatud. Teavet lisakulude seadistamise kohta oma vajaduste järgi leiate ajaveebipostitusest [Lisakulude sisestamine toote sissetuleku ajal](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).
