---
title: Komplekteerimistööd ei looda kohe, kui väljaminev koormus vabastatakse
description: Kui töö tuleb luua kohe, kui koorem on väljastatud, tuleb teil voo mall vastavalt konfigureerida. See lehekülg juhendab teid läbi nende sammude.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: fdeb0b27f4d2c1a2cc9f8e0c4ba537cdce604bd2
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476138"
---
# <a name="picking-work-isnt-generated-immediately-when-outbound-load-is-released"></a>Komplekteerimistööd ei looda kohe, kui väljaminev koormus vabastatakse

## <a name="symptoms"></a>Sümptomid

Väljamineva koorma saate luua müügi- või üleviimistellimusega ja vabastada koorma lattu. Pange tähele, et komplekteerimise tööd pole veel loodud.

## <a name="resolution"></a>Lahendus

Kui töö tuleb luua kohe, kui koorem on väljastatud, tuleb teil voo mall vastavalt konfigureerida. Voo mallis seadke järgmised valikud väärtusele *Jah*:

- Automatiseeri voo loomine
- Töötle voogu lattu vabastamisel
- Automatiseeri voog vabastamine
