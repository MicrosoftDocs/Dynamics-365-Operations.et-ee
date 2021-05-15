---
title: Kviitungit pole loodud
description: See teema pakub tõrkeotsingu teavet, mis võib aidata, kui kviitung peaks loodama, aga ei looda.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947628"
---
# <a name="voucher-isnt-generated"></a>Kviitungit pole loodud

[!include [banner](../includes/banner.md)]

Kui kviitung tuleb luua, kuid **Kviitungi kande** leht ei näita ühtegi kviitungit, järgige selle probleemi tõrkeotsinguks vajalikke etappe järgmistes jaotistes.

[![Kviitungite kandeleht kus pole kviitungeid](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Kontrollige maksu kohaldatavust

1. Mine **Maks** \> **Perioodilised ülesanded** \> **Arveraamatu alamtöölehe kirjeid pole veel üle kantud**.
2. Kui päevaraamatu kirje on olemas, valige see ja seejärel valige **Kanna kohe üle**.

    [![Kanna üle nupp Arveraamatu alamtöölehe kanded ei ole veel üle kantud leht](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Avage **Kviitungi kanded** leht uuesti, et näha, kas kviitung loodi.

## <a name="determine-whether-customization-exists"></a>Kohanduse olemasolu tuvastamine

Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik. Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
