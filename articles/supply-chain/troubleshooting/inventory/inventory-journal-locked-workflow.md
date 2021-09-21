---
title: Teie varude tööleht on lukus ja töövoo pakett-töö ei tööta
description: Üks teie varude töölehtedest on mingi toimingu poolt lukustatud ja seda ei vabastata
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476093"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Teie varude tööleht on lukus ja töövoo pakett-töö ei tööta

## <a name="symptoms"></a>Sümptomid

Üks teie varude töölehtedest on mingi toimingu poolt lukustatud ja seda ei vabastata. Näiteks kui sisestamisel (mis on süsteemi lukustustoiming) ilmneb tundmatu tõrge, võib tööleht jääda süsteemis lukus olekusse. Sel juhul kuvab töövoo tööüksuse ohjur tõrke, tehes samal ajal lukustuse kinnitamise.

## <a name="resolution"></a>Lahendus

Logige sisse Supply Chain Managementi SQL-serveri eksemplari ja kontrollige, kas **InventJournalTable.SystemBlocked** väärtuseks on määratud *1*. Kui on, siis veenduge, et tööleht ei oleks lukustatud olekus, ja lähtestage atribuut **inventJournalTable.SystemBlocked** väärtusele *0*.
