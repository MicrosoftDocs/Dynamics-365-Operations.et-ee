---
title: Lao vanemate partiide mobiilses seadmes kuvamise konfigureerimine
description: "Selles teemas kirjeldatakse mobiilse seadme seadistamist kuvama asukohtade loendit partiidega, mis on vanemad kui töörea praegune asukoht."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3e9386f6da7b8bdc1cbb817a78f72c225cbaa9bc
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---

# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Lao vanemate partiide mobiilses seadmes kuvamise konfigureerimine

[!include[banner](../includes/banner.md)]

Konfiguratsioon **Kuva vanemad partiid laos** võimaldab kuvada loendi asukohtadest vanemate partiidega kui töörea praegune asukoht. Kuvatav asukohtade loend sisaldab teavet asukohas olevate vanemate partiide kohta koos iga partii aegumiskuupäeva ja füüsilise varuga. Saate valida uuest asukohast komplekteerimise või jätkata komplekteerimist praegusest asukohast. 
- Komplekteerimine uuest asukohast – kui valite komplekteerimiseks uue asukoha, värskendatakse praegust töörida, et kasutada uut asukohta, ning töö jätkub tavapäraselt uue asukohaga. Selleks et uus asukoht kehtiks, peab sel olema kogu töörea ulatuses piisav saadaolev kogus. Kui nõutud kogus pole saadaval, siis töörida ei värskendata ja kuvatakse loend. 
- Komplekteerimise jätkamine praegusest asukohast – kui jätkate praeguse töörea asukohaga, komplekteeritakse töörea koguseid edasi algsest asukohast.

## <a name="where-it-applies"></a>Kus see kehtib
Laos olevate vanemate partiide kuvamine on konfigureeritud mobiilse seadme menüüelementides ja see mõjutab allpool nimetatud partii komplekteerimist.

## <a name="set-up-display-older-batches-within-warehouse"></a>Laos olevate vanemate partiide kuvamise seadistamine
Konfiguratsioon **Laos olevate vanemate partiide kuvamine** on saadaval mobiilse seadme menüüelementides, kui suvandi **Komplekteeri vanim partii** sätteks on valitud **Hoiata**.

- Valige menüüs **Laohaldus** > **Seadistus** > **Mobiilne seade** > **Mobiilse seadme menüüelemendid** suvandi **Kasuta olemasolevat tööd** sätteks menüüelemendi puhul **Jah** ja valige väljal **Komplekteeri vanim partii** säte **Hoiata**. 

