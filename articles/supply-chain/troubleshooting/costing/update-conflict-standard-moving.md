---
title: Värskendage konflikti, kui varude hinna määramise meetod on kas standardne kulu või libisev keskmine
description: Uuenduse vastuolu ilmneb, kui varude hinna määramise meetod on kas standardne kulu või libisev keskmine
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 920d20d19843ce0cac678c5426c00ec99aa61c61
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476150"
---
# <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Uuenduse vastuolu ilmneb, kui varude hinna määramise meetod on kas standardne kulu või libisev keskmine

## <a name="symptoms"></a>Sümptomid

Kui sisestate dokumente, nt laotöölehti, ostutellimuse arveid või müügitellimuste arveid paralleelselt skaleeritavuse ja jõudluse huvides, võite saada tõrketeate uuenduse vastuolu kohta ja mõningaid dokumente ei pruugita sisestada. See probleem võib ilmneda, kui varude hinna määramise meetod on kas *standardne kulu* või *libisev keskmine*. Mõlemad meetodid on pideva keskmise põhimõttel tuginevad kuluarvestusmeetodid. Teisisõnu määratletakse lõplik kulu sisestamise ajal.

Kui kasutate meetodit *Liikuv keskmine*, sarnaneb veateade järgmisele näitele.

> Laoväärtust xx.xx ei oodata pärast proportsionaalse kulu arvutamist

Kui kasutate meetodit *Standardkulu*, sarnaneb veateade järgmisele näitele.

> Standardkulu ei kattu pärast uuendamist finantsilise laovaru väärtusega. Väärtus = xx,xx, kogus = yy,yy, standardkulu = zz,zz

## <a name="workaround"></a>Vastukaal

Kuni Microsoft annab probleemi lahendamiseks välja lahenduse, kaaluge järgmiste lahenduste kasutamist nende tõrgete vältimiseks või vähendamiseks.

- Postitage nurjunud dokumendid uuesti.
- Looge dokumente, millel on vähem ridu.
- Vältige standardkulus kümnendkohaga väärtusi. Proovige määratleda standardnkulu nii, et välja **Hinna kogus** väärtuseks oleks seatud *1*. Kui peate määrama **hinna koguse** väärtuseks üle *1*, proovige vähendada kümnendkohtade arvu ühiku standardkulus. (Ideaaljuhul peaks see olema alla kahe komakoha.) Näiteks vältige standardsete kulusätete, näiteks **Hind** = *10* ja **Hinna kogus** = *3*, kuna need tekitavad ühiku standardkulu 3,333333 (kus kümnendväärtus kordub).
- Vältige enamikes dokumentides mitme rea omamist, millel on sama tootekombinatsioon ja finantsiliste varude dimensioon.
- Vähendage paralleelsuse astet. (Sel juhul võib süsteem muutuda kiiremaks, sest tekib vähem uuenduse vastuolusid ja uuesti tegemist.)
