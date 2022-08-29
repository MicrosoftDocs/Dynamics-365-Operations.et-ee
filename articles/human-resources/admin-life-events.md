---
title: Elusündmuste administraatori õiguste korraldamine
description: See artikkel selgitab, kuidas konfigureerida Microsofti elusündmuste administraatoriõigusi Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229985"
---
# <a name="set-administrator-rights-for-life-events"></a>Elusündmuste administraatori õiguste korraldamine

[!include [banner](../includes/preview-banner.md)]

Administraatorid saavad olenevalt konfiguratsioonisätetest uuendada elusündmuse valikuid. **Inimressursside parameetrite lehel saate konfigureerida** parameetreid, mis võimaldavad administraatoritel teha plaani valikutes muudatusi. Samuti saate administraatoritel muudatuste tegemisest täielikult piirata.

**Inimressursside parameetrite lehel saate seadistada** plaani muutmise piiranguid kinnitatud plaanide ja eluea sündmuste valikute jaoks.

Kui on **valitud** suvand Kinnitatud plaanid, saab muudatusi teha ainult siis, kui registreerimisperiood on aktiivne. (Registreerimisperioodide näited hõlmavad avatud registreerimisperioode, uusi palkamise registreerimisperioode ja elusündmuste registreerimisperioode.) Kui seda valikut ei valita, saab muudatusi teha igal ajal.

Kui on **valitud valik** Elusündmuse valikud, on eluea sündmuse jooksul tehtud plaanimuudatused piiratud plaani tüübis määratletud elusündmuse valikutega. Kui seda valikut ei valita, saab plaanivalikuid muuta elusündmuse ajal.

## <a name="set-plan-change-restrictions"></a>Sea plaani muutmise piirangud

**Soodustuste halduse vahekaardi** lehel **Inimressursside** parameetrid on saadaval järgmised väljad.

| Väli | Kirjeldus |
|-------|-------------|
| Kinnitatud plaanid | Valige see suvand, kui plaani muudatused on lubatud ainult siis, kui registreerimisperiood on aktiivne. Kui seda valikut ei valita, saab muudatusi teha igal ajal. |
| Elusündmuse suvandid | Valige see suvand, kui plaani muudatused elusündmuse jooksul on piiratud plaani tüübis määratletud elusündmuste valikutega. Kui seda valikut ei valita, saab plaanivalikuid muuta elusündmuse ajal. |
