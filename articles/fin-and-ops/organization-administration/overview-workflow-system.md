---
title: Töövoo süsteem
description: Teema kirjeldab töövoosüsteemi rakenduses Microsoft Dynamics 365 for Finance and Operationsi.
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a35184a48eff9e320087cb9390a0f1eed1e7ba19
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545805"
---
# <a name="workflow-system"></a>Töövoo süsteem

[!include [banner](../includes/banner.md)]

Teema kirjeldab töövoosüsteemi rakenduses Microsoft Dynamics 365 for Finance and Operationsi.

## <a name="what-is-workflow"></a>Mis on töövoog?

Mõiste *töövoo* saab määratleda kahel viisil: süsteemi ja äriprotsessi.

### <a name="workflow-is-a-system"></a>Töövoog on süsteem

Töövoog on koos Finance and Operationsiga installitud süsteem, mis töötab rakendusobjekti serveril (AOS-il). Töövoo süsteemil on funktsioone, millega saate luua eraldi töövooge või äriprotsesse.

### <a name="workflow-is-a-business-process"></a>Töövoog on äriprotsess

Töövoog esindab äriprotsessi. See määratleb, kuidas dokument voogab või liigub läbi süsteemi, näidates, kes peab täitma ülesannet, otsuse või dokumendi kinnitamiseks. Alltoodud joonisel kujutatakse kuluaruannete töövoogu.

![Kasutajatele määratud elementidega töövoog](./media/workflow_user.gif)

Selle töövoo paremaks mõistmiseks oletame, et Sam esitab kuluaruande summale 7000 USA dollarit. Selle stsenaariumi kohaselt on Ivani ülesanne Sami lähetatud sissetulekud üle vaadata. Seejärel peavad Frank ja Sue kuluaruande kinnitama. Oletame nüüd, et Sam esitab kuluaruande summas 11 000 USA dollarit. Selles stsenaariumis peab Ivan tšekid üle vaatama ning Frank, Sue ja Ann peavad kuluaruande kinnitama.

## <a name="benefits-of-using-the-workflow-system"></a> Töövoo süsteemi kasutamise eelised

Töövoo süsteemi kasutamine teie organisatsioonis on mitmeti kasulik.

- **Järjepidevad protsessid** – töövoo süsteem lubab teil määratleda, kuidas kindlaid dokumente, näiteks ostutaotlused ja kuluaruanded, töödeldakse. Töövoo süsteemi abil tagate, et dokumente töödeldakse ja kinnitatakse ühtemoodi ja efektiivselt.
- **Protsessi nähtavus** – töövoo süsteem lubab teil jälgida kindlate töövoo eksemplaride olekut ja ajalugu. See aitab teil määratleda, kas töövoos tuleks muudatusi tõhususe parandamiseks.
- **Koondatud tööde loend** – kasutajad saavad vaadata koondatud tööde loendit, et näha neile määratud töövoo ülesandeid ja kinnitusi.


## <a name="workflow-content"></a>Töövoo sisu

+ [Töövoo arhitektuur](workflow-system-architecture.md)
+ [Töövoo elemendid](workflow-elements.md)
+ [Töövoo tegevused](workflow-actions.md)
+ [Töövoo loomine](create-workflow.md)
+ [Töövoo atribuutide konfigureerimine](configure-workflow-properties.md)
+ [Töövoos käsitsi ülesande konfigureerimine](configure-manual-task-workflow.md)
+ [Töövoos automaatse ülesande konfigureerimine](configure-automated-task-workflow.md)
+ [Töövoo kinnitusprotsessi konfigureerimine](configure-approval-process-workflow.md)
+ [Töövoo kinnitusetapi konfigureerimine](configure-approval-step-workflow.md)
+ [Töövoos käsitsi otsuse konfigureerimine](configure-manual-decision-workflow.md)
+ [Töövoos tingimusliku otsuse konfigureerimine](configure-conditional-decision-workflow.md)
+ [Töövoos paralleeltegevuse konfigureerimine](configure-parallel-activity-workflow.md)
+ [Töövoos paralleelharu konfigureerimine](configure-parallel-branch-workflow.md)
+ [Rea kauba töövoo konfigureerimine](configure-line-item-workflow.md)
+ [Töövoo KKK](workflow-FAQ.md)
