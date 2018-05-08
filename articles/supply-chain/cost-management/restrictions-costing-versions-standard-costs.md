---
title: Standardkulude kuluversioonide piirangud
description: Selles teemas kirjeldatakse piiranguid, mis kehtivad standardkulude kuluversiooni puhul.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e14d5d11e987d2dbc841f86c39fc7e94864144d3
ms.openlocfilehash: 658575492597eed91509561f4710f07e271c53c8
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---


#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Standardkulude kuluversioonide piirangud

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse piiranguid, mis kehtivad standardkulude kuluversiooni puhul. 

Järgmised piirangud aitavad tagada standardkulude põhimõtetest kinnipidamist.

-  Kauba kulusse tuleb kaasata tasud. Toodetud kauba tasud näitavad amortiseeritud püsikulusid koosluse ja marsruuditeabe piires. Seetõttu tuleb nad kaasata ühiku hinda. Ostetud kauba tasud kaasatakse ka selle kauba ühiku hinda.

-  Toodetud kaupade standardkulude arvutamine peab põhinema standardkulude kuluversioonis olevatel kulukirjetel. Kuluandmete alternatiivseid allikaid saab kasutada ainult planeeritud kulude kuluversiooniga, nt ostuhinna kaubanduslepped ostetud kaupade puhul. Kuluandmete alternatiivsed allikad saab määratleda koosluse kalkulatsioonigrupp.

-  Koosluse kalkulatsioone tuleb teha üksiktaseme tormilise arengu režiimiga.

Standardkulude kaubakulu andmeid saab kopeerida muusse kuluversiooni, mis sisaldab standardkulusid või planeeritud kulusid. Planeeritud kulude kaubakuluandmeid ei saa siiski kopeerida standardkulusid sisaldavasse kuluversiooni, sest varem selles teemas loetletud piiranguid ei kohaldata planeeritud kuludele.

<a name="related-topics"></a>Seotud dokumendid
--------

[Kuluversioonid](costing-versions.md)

[Mittetootmiskeskkonna standardkulude värskendamine](update-standard-costs-non-manufacturing-environment.md)

[Toodetud kaupade standardkulude säilitamise ettevalmistus](update-standard-costs-manufacturing-environment.md)


