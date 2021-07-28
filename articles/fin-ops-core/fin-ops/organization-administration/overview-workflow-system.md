---
title: Töövoosüsteemi ülevaade
description: Teema kirjeldab töövoosüsteemi.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc73f1bde3407c144dc1cd48283385c19713430e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349080"
---
# <a name="workflow-system-overview"></a>Töövoosüsteemi ülevaade

[!include [banner](../includes/banner.md)]

Teema kirjeldab töövoosüsteemi.

## <a name="what-is-workflow"></a>Mis on töövoog?

Mõiste *töövoo* saab määratleda kahel viisil: süsteemi ja äriprotsessi.

### <a name="workflow-is-a-system"></a>Töövoog on süsteem

Töövoog on süsteem, mis töötab rakendusobjekti serveris (AOS). Töövoo süsteemil on funktsioone, millega saate luua eraldi töövooge või äriprotsesse.

### <a name="workflow-is-a-business-process"></a>Töövoog on äriprotsess

Töövoog esindab äriprotsessi. See määratleb, kuidas dokument voogab või liigub läbi süsteemi, näidates, kes peab täitma ülesannet, otsuse või dokumendi kinnitamiseks. Alltoodud joonisel kujutatakse kuluaruannete töövoogu.

![Kasutajatele määratud elementidega töövoog.](./media/workflow_user.gif)

Selle töövoo paremaks mõistmiseks oletame, et Sam esitab kuluaruande summale 7000 USA dollarit. Selle stsenaariumi kohaselt on Ivani ülesanne Sami lähetatud sissetulekud üle vaadata. Seejärel peavad Frank ja Sue kuluaruande kinnitama. Oletame nüüd, et Sam esitab kuluaruande summas 11 000 USA dollarit. Selles stsenaariumis peab Ivan tšekid üle vaatama ning Frank, Sue ja Ann peavad kuluaruande kinnitama.

## <a name="benefits-of-using-the-workflow-system"></a> Töövoo süsteemi kasutamise eelised

Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.

- **Järjepidevad protsessid** – töövoo süsteem lubab teil määratleda, kuidas kindlaid dokumente, näiteks ostutaotlused ja kuluaruanded, töödeldakse. Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse ühtemoodi ja efektiivselt.
- **Protsessi nähtavus** – töövoo süsteem lubab teil jälgida kindlate töövoo eksemplaride olekut ja ajalugu. See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.
- **Koondatud tööde loend** – kasutajad saavad vaadata koondatud tööde loendit, et näha neile määratud töövoo ülesandeid ja kinnitusi.


## <a name="workflow-content"></a>Töövoo sisu

+ [Töövoo süsteemi arhitektuur](workflow-system-architecture.md)
+ [Töövooelemendid](workflow-elements.md)
+ [Tegevused töövoo kinnitusprotsessis](workflow-actions.md)
+ [Töövoogude loomise ülevaade](create-workflow.md)
+ [Töövooatribuutide konfigureerimine](configure-workflow-properties.md)
+ [Töövoos käsitsi ülesannete konfigureerimine](configure-manual-task-workflow.md)
+ [Töövoos automaatsete ülesannete konfigureerimine](configure-automated-task-workflow.md)
+ [Töövoo kinnitusprotsesside konfigureerimine](configure-approval-process-workflow.md)
+ [Töövoo kinnitusetappide konfigureerimine](configure-approval-step-workflow.md)
+ [Töövoos käsitsi otsuste konfigureerimine](configure-manual-decision-workflow.md)
+ [Töövoos tingimuslike otsuste konfigureerimine](configure-conditional-decision-workflow.md)
+ [Paralleeltegevuste konfigureerimine töövoos](configure-parallel-activity-workflow.md)
+ [Paralleelharude konfigureerimine töövoos](configure-parallel-branch-workflow.md)
+ [Reakauba töövoogude konfigureerimine](configure-line-item-workflow.md)
+ [Töövoo KKK](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]