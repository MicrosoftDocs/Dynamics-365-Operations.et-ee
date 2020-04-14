---
title: Kuluhalduse töövoogude häälestamine
description: Saate seadistada töövooprotsessi, mida kasutatakse reisi- ja kuludokumentide kinnitamiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153988"
---
# <a name="set-up-workflows-for-expense-management"></a>Kuluhalduse töövoogude häälestamine

[!include [banner](../includes/banner.md)]

Saate seadistada töövooprotsessi, mida kasutatakse reisi- ja kuludokumentide kinnitamiseks. Dokumendid, millele saab määratleda töövoogusid, on kuluaruanded, reisiplaanid ja avansimaksete taotlused.

Töövoog esindab äriprotsessi. Töövoog määrab, kuidas dokument voogab läbi süsteemi, näidates, kes peab seda töötlema ja kinnitama. Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.

-   **Järjepidevad protsessid** — töövoo süsteem lubab teil määratleda kinnitusprotsessi kindlatele dokumentidele nagu näiteks ostutaotlused ja kuluaruanded. Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse järjekindlal ja tõhusal viisil.

-   Protsessi nähtavus — töövoo süsteem lubab teil jälgida kindla töövoo eksemplari olekut ja ajalugu. See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.

-   Koondatud tööde loend — kasutajad saavad vaadata koondatud tööde loendit, et näha neile määratud töövoo ülesandeid ja kinnitusi. 

**Loodavate töövoogude tüübid**

Järgmises tabelis on esitatud töövoo tüübid, mida saate luua jaotises **Kulu**.


|              <strong>Tüüp</strong>              |                   <strong>Kasutage seda tüüpi järgmiseks</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Kuluaruanne</strong>         |            Kuluaruannetele kinnitamise töövoogude loomine.             |
|  <strong>Kuluaruande automaatne sisestamine</strong>   |        Kuluaruannetele automaatse sisestamise töövoogude loomine.        |
|       <strong>Kulurea kaup</strong>        |     Kuluaruannete reaüksustele kinnitamise töövoogude loomine.      |
| <strong>Kulurea kauba automaatne sisestamine</strong> | Kuluaruannete reaüksustele automaatse sisestamise töövoogude loomine. |
|       <strong>Reisitellimus</strong>       |          Reisiplaanidele kinnitamise töövoogude loomine.           |
|      <strong>Avansimakse taotlus</strong>      |         Sularaha ettemakse taotluste kinnitustöövoogude loomine.          |
|        <strong>Käibemaksu korvamine</strong>        | Käibemaksu (KM) korvamise kinnitustöövoogude loomine.  |

