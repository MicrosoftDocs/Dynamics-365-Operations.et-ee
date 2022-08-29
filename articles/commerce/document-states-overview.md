---
title: Dokumendi olekud ja töötsükkel
description: See artikkel hõlmab mitmesuguseid leheküljeelementide dokumendi osalisi elemendid Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: intro-internal
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 350b3236eec6ad6520025bf44b22f12366f1e266
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269912"
---
# <a name="document-states-and-lifecycle"></a>Dokumendi olekud ja töötsükkel

[!include [banner](includes/banner.md)]

See artikkel hõlmab mitmesuguseid leheküljeelementide dokumendi osalisi elemendid Microsoft Dynamics 365 Commerce.

## <a name="document-state-descriptions"></a>Dokumendi oleku kirjeldused

Lehe [elementide artiklis](page-elements-overview.md) loetletakse erinevad dokumenditüübid sisuhalduse süsteemis (CMS). Nendel dokumenditüüpidel võib autorluse tööriistas olla mitu olekut. Dokumendi olekud aitavad ennetada andmekonflikte ja jõustada versiooni kontrollimist. Need määratlevad, kes saavad dokumente muuta, millal dokumente saab muuta ja millal võivad teised inimesed muudatusi näha.

Järgmises tabelis on toodud Commerce’i leheelementide võimalikud dokumentide olekud.

| Dokumendi olek      | Saidiehitaja tegevus        | Kirjeldus                                                  |
| ------------------- | -------------------------- | ------------------------------------------------------------ |
| Väljaregistreeritud         | Valige suvand **Redigeeri**.           | Kohaldatav dokument on teile välja registreeritud. Kui dokument on selles olekus, ei saa teised autenditud süsteemi kasutajad seda muuta ja kõik dokumendis tehtud muudatused on nähtavad ainult teile. |
| Salvestatud               | Valige käsk **Salvesta**.           | Välja registreeritud dokumendis tehtud muudatused salvestatakse andmebaasi, kuid dokumenti pole veel registreeritud ega avaldatud. Salvestatud muudatused ei ole teistele autenditud süsteemi kasutajatele nähtavad enne, kui autor on teinud valiku **Lõpeta redigeerimine**. Need ei ole välistele kasutajatele nähtavad enne, kuni üksus on avaldatud. |
| Loobutud väljaregistreerimine | Valige **Hülga redigeerimine**.  | Kõik välja registreeritud dokumendis tehtud muudatused hüljatakse ja üksus taastab viimase registreeritud versiooni. |
| Sisseregistreeritud          | Valige **Lõpeta redigeerimine**. | Redigeeritud dokument on registreeritud. Kõik muudatused on teistele autenditud süsteemikasutajatele nähtavad ja need kasutajad saavad seejärel dokumenti redigeerida. Iga registreerimine loob üksuse ajaloos dokumendi versiooni kirje. |
| Avaldatud           | Valige **Avalda**.        | Dokument avaldatakse ja muudatused suunatakse teie reaalajas saidile ja need muutuvad süsteemivälistele kasutajatele leitavaks. Üksusi saab avaldada ainult juhul, kui nad on esmalt registreeritud käsu **Lõpeta redigeerimine** abil. |

## <a name="additional-resources"></a>Lisaressursid

[Sisu lisamise viisid](add-manage-content.md)

[Lehemudeli sõnastik](page-elements-overview.md)

[Avaldamisrühmadega töötamine](publish-groups.md)

[Kanaliülese ühiskasutuse lubamine ja kasutamine](cross-channel-sharing.md)

[Moodulitega töötamine](work-with-modules.md)

[Fragmentidega töötamine](work-with-fragments.md)

[Mallide ja paigutuste ülevaade](templates-layouts-overview.md)

[Saidil navigeerimise kohandamine](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
