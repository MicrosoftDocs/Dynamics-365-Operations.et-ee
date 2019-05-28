---
title: Kasutajal on juurdepääs Core HR-ile, aga mitte rakendusele Onboard või Attract
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus kasutajal on juurdepääs rakenduse Microsoft Dynamics 365 for Talent Core HR-ile, aga mitte rakendusele Onboard ega Attract.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517818"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Kasutaja pääseb ligi Core HR-ile, aga mitte rakendusele Onboard või Attract

[!include [banner](includes/banner.md)]

**Keskkonna üksikasjad**

- Teenuse Microsoft Dynamics Lifecycle Services (LCS) juurutamise viis läbi kasutaja A.
- Kasutaja A lisas kasutaja B kasutajana rakenduse Microsoft Dynamics 365 for Talent Core HR-i.

**Väljastamine**

Kasutaja B-l on juurdepääs Core HR-ile, aga mitte rakendusele Talent: Attract või Talent: Onboard. Valiku **Kogemuse rakendused** tegemisel suunatakse kasutaja selle asemel proovikeskkonda.

**Lahendus**

Kasutajale B peavad olema määratud õigused vaadata Microsoft PowerAppsi keskkonda, mille kasutaja A ettevalmistusprotsessi ajal lõi.

Lisateavet vt jaotisest Keskkonnale juurdepääsu andmine lehel [Talenti ettevalmistamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

**Pikaajaline lahendus**

Kui Core HR-i lisatakse kasutaja, kaalub Microsoft rakendustele Onboard ja Attract asjakohaste õiguste automaatset määramist.
