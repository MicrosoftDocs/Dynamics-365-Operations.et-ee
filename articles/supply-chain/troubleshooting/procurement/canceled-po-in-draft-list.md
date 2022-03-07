---
title: Tühistatud ostutellimused kuvatakse tööruumis mustandiloendis
description: Tühistatud ostutellimused kuvatakse ostutellimuse ettevalmistamise tööruumis mustandiloendis
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: f1dc23cd7e5b4b99cb7a9440d7d4666d8396511f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476142"
---
# <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-workspace"></a>Tühistatud ostutellimused kuvatakse tööruumis mustandiloendis

## <a name="symptoms"></a>Sümptomid

Pärast olekus *Kinnitatud* ostutellimuste tühistamist kuvatakse tühistatud ostutellimused ikka tööruumis **Ostutellimuse ettevalmistamine** asuvas ostutellimuste mustandite loendis.

## <a name="resolution"></a>Lahendus

See probleem ilmneb ainult ostutellimuste puhul, mille korral kasutatakse muudatuste haldust. See ilmneb seetõttu, et tühistamist peetakse muudatuseks, mis tuleb kinnitada. Süsteem saab selle kinnitada automaatselt. Seetõttu tuleb tühistatud ostutellimus edastada kinnitamise töövoogu, et selle olekuks saaks määrata *Heaks kiidetud*. Seejärel ei kuvata ostutellimust enam tööruumis **Ostutellimuse ettevalmistamine** asuvas ostutellimuste mustandite loendis.
