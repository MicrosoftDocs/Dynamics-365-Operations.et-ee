---
title: Dokumendi olekud ja töötsükkel
description: Selles teemas käsitletakse rakenduse Microsoft Dynamics 365 Commerce leheelementide erinevaid dokumendi olekuid.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8aad7ef8425e46182c669686710dfc178abc418f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411679"
---
# <a name="document-states-and-lifecycle"></a>Dokumendi olekud ja töötsükkel

[!include [banner](includes/banner.md)]

Selles teemas käsitletakse rakenduse Microsoft Dynamics 365 Commerce leheelementide erinevaid dokumendi olekuid.

## <a name="document-state-descriptions"></a>Dokumendi oleku kirjeldused

Teema [lehekülje elemendid](page-elements-overview.md) loetleb erinevate dokumentide tüübid sisu haldamise süsteemis (CMS). Nendel dokumenditüüpidel võib autorluse tööriistas olla mitu olekut. Dokumendi olekud aitavad ennetada andmekonflikte ja jõustada versiooni kontrollimist. Need määratlevad, kes saavad dokumente muuta, millal dokumente saab muuta ja millal võivad teised inimesed muudatusi näha.

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