---
title: Planeerimise optimeerimise ülevaade
description: Selles teemas antakse planeerimise optimeerimise funktsioonist ülevaade.
author: ChristianRytt
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9b55a48847e9c6201e7a93a2fb5d6622b581d785
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354709"
---
# <a name="planning-optimization-overview"></a>Planeerimise optimeerimise ülevaade

[!include [banner](../../includes/banner.md)]

Rakenduse Microsoft Dynamics 365 Supply Chain Management planeerimise optimeerimise lisandmoodul võimaldab koondplaneerimise arvutuste tegemist väljaspool Dynamics 365 Supply Chain Managementi ja seotud SQL-andmebaasi. Planeerimise optimeerimise funktsiooniga seotud eelised hõlmavad paremat jõudlust ja minimaalset mõju SQL-andmebaasile koondplaneerimise käivitamiste ajal. Kiireid planeerimise käivitamisi saab teha isegi kontoris viibimise ajal, seega saavad planeerijad nõudlusele või parameetri muutustele kohe reageerida.

Planeerimise optimeerimise kasutamiseks peate installima planeerimise optimeerimise lisandmooduli oma projektist portaalis Microsoft Dynamics Lifecycle Services (LCS) ja lülitama planeerimise optimeerimise funktsiooni tarneahela halduses sisse. Lisateavet vt [Planeerimise optimeerimise kasutamise alustamine](get-started.md).

Järgmisel joonisel on näha planeerimise optimeerimise kontoris viibimise ajal käivitamise eelis.

![Planning Optimization`i tööajal käitamise eelis.](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Parem jõudlus

Planeerimise optimeerimist saab kasutada stsenaariumides, mis hõlmavad pikaajalisi koondplaane. See on spetsiaalselt loodud väga kiirete arvutuste jaoks, mis hõlmavad väga suurt hulka andmeid. Kuna see on loodud hüperskaleeritava mitme rentnikuga teenusena, saavad mitu üksust plaani arvutamiseks samaaegselt koos töötada. Lisaks eemaldab planeerimise teenus teie süsteemist koondplaneerimise koormuse ja töötab andmevooga, mis vähendab serveri koormust.

Planeerimise optimeerimine saab aidata teil saavutada järgmisi eesmärke.

- Planeerimise jõudluse parandamine lühema käitamisaja kaudu.
- Koondplaneerimise käivitamise ajal teistele protsessidele avaldatava mõju vähendamine.
- Sagedasem planeerimise käivitamiste tegemine. (Te pole piiratud igapäevaste käivitustega.)
- Saate olla kindlad, et äri kasvamine tulevikus ei koorma planeerimise süsteemi üle.

## <a name="architecture-and-data-flow"></a>Arhitektuur ja andmevoog

Kui planeerimise optimeerimise lisandmoodul on LCS-ist installitud, luuakse turvaline ühendus planeerimise optimeerimise teenusega. Teenus asub samas andmekeskuse riigis või piirkonnas kui seotud tarneahela halduse eksemplar. Pärast planeerimise optimeerimise seadistamist kui käivitatakse koondplaneerimist, saadetakse koondandmed ja kandeandmed tarneahela haldusest planeerimise optimeerimise teenusesse.

Kui planeerimise optimeerimise lisandmoodul desinstallitakse, eemaldatakse kõik planeerimise optimeerimise teenusega seotud andmed.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Kõrgetasemeline andmevoog taasloomise käivitusteks

1. Tarneahela halduse klient saadab signaali, et taotleda planeerimise optimeerimiselt planeerimise käivitust.
2. Planeerimise optimeerimine taotleb integreeritud konnektori kaudu vajalikke andmeid.
3. SQL-andmebaas saadab taotletud teabe häälestuse, koondandmete ja kandeandmete kohta konnektori kaudu planeerimise optimeerimisse. Konnektor tõlgendab teavet tarneahela halduse ja planeerimise optimeerimise teenuse vahel.
4. Planeerimise optimeerimise teenus hoiab planeerimisega seotud andmeid mälus ja teeb vajalikud arvutused.
5. Planeerimise tulemus saadetakse konnektori kaudu tarneahela halduse andmebaasile. Tulemused hõlmavad teavet, nagu plaanitud tellimused ja sidumisandmed. Planeerimise optimeerimine saadab signaali tarneahela haldusele, et näidata, et planeerimise käivitamine on lõpetatud. See saadab ka kõik asjakohased teated ja hoiatused.

Järgmine illustratsioon näitab andmevoogu.

![Andmevoog taasloomise käivitusteks.](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Seotud ressursid

[Planeerimise optimeerimise kasutamise alustamine](get-started.md)

[Planeerimise optimeerimise sobivuse analüüs](planning-optimization-fit-analysis.md)

[Plaani ajaloo ja plaanimise logide vaatamine](plan-history-logs.md)

[Plaanile filtrite rakendamine](plan-filters.md)

[Planeerimistöö tühistamine](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]