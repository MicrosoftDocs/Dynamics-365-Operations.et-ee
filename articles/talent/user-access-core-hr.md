---
title: "Kasutajal on juurdepääs Core HR-ile, aga mitte rakendusele Onboard või Attract"
description: "Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus kasutajal on juurdepääs rakenduse Microsoft Dynamics 365 for Talent Core HR-ile, aga mitte rakendusele Onboard või Attract."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: et-ee
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Kasutajal on juurdepääs Core HR-ile, aga mitte rakendusele Onboard või Attract

[!include [banner](includes/banner.md)]

**Keskkonna üksikasjad**

- Microsoft Dynamicsi teenuse Lifecycle Services (LCS) juurutamise viis läbi kasutaja A.
- Kasutaja A lisas kasutaja B kasutajana rakenduse Microsoft Dynamics 365 for Talent Core HR-i.

**Probleem**

Kasutaja B-l on juurdepääs Core HR-ile, aga mitte rakendusele Talent: Attract või Talent: Onboard. Valiku **Kogemuse rakendused** tegemisel suunatakse kasutaja selle asemel proovikeskkonda.

**Lahendus**

Kasutajale B peavad olema määratud õigused vaadata Microsoft PowerAppsi keskkonda, mida kasutaja A ettevalmistusprotsessi ajal lõi.

Lisateavet vt jaotisest Keskkonnale juurdepääsu andmine lehel [Talenti ettevalmistamine](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

**Pikaajaline lahendus**

Kui Core HR-i lisatakse kasutaja, kaalub Microsoft rakendustele Onboard ja Attract asjakohaste õiguste automaatset määramist.

