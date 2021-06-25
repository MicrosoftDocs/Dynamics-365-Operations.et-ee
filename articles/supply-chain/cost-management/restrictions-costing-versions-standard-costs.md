---
title: Standardkulude kuluversioonide piirangud
description: Selles teemas kirjeldatakse piiranguid, mis kehtivad standardkulude kuluversiooni puhul.
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9d828e2413a20c4e61d162a31d3c2ed2b18718b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187670"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Standardkulude kuluversioonide piirangud

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse piiranguid, mis kehtivad standardkulude kuluversiooni puhul. 

Järgmised piirangud aitavad tagada standardkulude põhimõtetest kinnipidamist.

-  Kauba kulusse tuleb kaasata tasud. Toodetud kauba tasud näitavad amortiseeritud püsikulusid koosluse ja marsruuditeabe piires. Seetõttu tuleb nad kaasata ühiku hinda. Ostetud kauba tasud kaasatakse ka selle kauba ühiku hinda.

-  Toodetud kaupade standardkulude arvutamine peab põhinema standardkulude kuluversioonis olevatel kulukirjetel. Kuluandmete alternatiivseid allikaid saab kasutada ainult planeeritud kulude kuluversiooniga, nt ostuhinna kaubanduslepped ostetud kaupade puhul. Kuluandmete alternatiivsed allikad saab määratleda koosluse kalkulatsioonigrupp.

-  Koosluse kalkulatsioone tuleb teha üksiktaseme tormilise arengu režiimiga.

Standardkulude kaubakulu andmeid saab kopeerida muusse kuluversiooni, mis sisaldab standardkulusid või planeeritud kulusid. Planeeritud kulude kaubakuluandmeid ei saa siiski kopeerida standardkulusid sisaldavasse kuluversiooni, sest varem selles teemas loetletud piiranguid ei kohaldata planeeritud kuludele.

## <a name="related-topics"></a>Seotud dokumendid

[Kuluarvutusversioonide ülevaade](costing-versions.md)

[Mittetootmiskeskkonnas standardomahindade värskendamine](update-standard-costs-non-manufacturing-environment.md)

[Toodetud kaupade standardkulude säilitamise ettevalmistus](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]