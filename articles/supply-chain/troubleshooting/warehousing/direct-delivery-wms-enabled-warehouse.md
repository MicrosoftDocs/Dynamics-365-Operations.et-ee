---
title: Otsetarnet ei saa WMS-lubatud lao puhul töödelda
description: Kui laol on WMS lubatud, ei toeta see otsetarnet. Et kasutada otsetarnet, peate valima mitte-WMS-i kauba ja lao.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476172"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>Otsetarnet ei saa WMS-lubatud lao puhul töödelda

## <a name="symptoms"></a>Sümptomid

Kui kaup lisatakse müügireale otsetarneks laost, mis on lubatud laohalduseks (WMS), saate müügirea uuendamisel järgmise tõrketeate:

> Otsetarnet ei saa 1% lao jaoks töödelda, kuna see on laohalduseks lubatud. Määrake mõni muu ladu, mis pole laohalduse jaoks lubatud.

## <a name="resolution"></a>Lahendus

Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang. Praegu ei toeta WMS otsetarnet. Seetõttu peate otsetarne kasutamiseks valima mitte-WMS kauba ja lao.
