---
title: Koosluse koosnevusarvutuse kooslused on seotud kinnitatud ja hinnangulised tootmistellimustega erinevalt
description: Koosluse tükeldamine käitub erinevalt kinnitatud tootmistellimustest ja plaanitud tootmistellimustest käsitsi loodud töö jaoks
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 94d4b00ea30396923a61b2748cf1aaeedc0af8af
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476117"
---
# <a name="bom-explosion-behaves-differently-for-firmed-and-estimated-production-orders"></a>Koosluse koosnevusarvutuse kooslused on seotud kinnitatud ja hinnangulised tootmistellimustega erinevalt

## <a name="symptoms"></a>Sümptomid

Kui tootmistellimus on kinnitatud, ei tükeldata kaupu koosluse tükeldamisel. Kuid kui loote käsitsi töötellimuse ja seejärel hindate tootmistellimuse, siis kaubad tükeldatakse.

### <a name="resolution"></a>Lahendus

Tükeldamine, mis ilmneb tootmistellimuse kinnitamisel, osutab plaanitud tellimusele, kuid ei ilmne, et plaanitud tellimus on praegu selles juhtumis kinnitatud. Kui tootmistellimus on hinnatud, käivitatakse tükeldamine vabastatud tootmistellimuselt, kus pole plaanitud tellimust.
