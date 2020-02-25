---
title: Dokumendi olekud ja töötsükkel
description: Selles teemas käsitletakse rakenduse Microsoft Dynamics 365 Commerce leheelementide erinevaid dokumendi olekuid.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: b4f1c462f734b2d58843308f0f877fe18a4d9af7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002977"
---
# <a name="document-states-and-lifecycle"></a>Dokumendi olekud ja töötsükkel


[!include [banner](includes/banner.md)]

Selles teemas käsitletakse rakenduse Microsoft Dynamics 365 Commerce leheelementide erinevaid dokumendi olekuid.

## <a name="document-state-descriptions"></a>Dokumendi oleku kirjeldused

Teema [lehekülje elemendid](page-elements-overview.md) loetleb erinevate dokumentide tüübid sisu haldamise süsteemis (CMS). Nendel dokumenditüüpidel võib autorluse tööriistas olla mitu olekut. Dokumendi olekud aitavad ennetada andmekonflikte ja jõustada versiooni kontrollimist. Need määratlevad, kes saavad dokumente muuta, millal dokumente saab muuta ja millal võivad teised inimesed muudatusi näha.

Järgmises tabelis on toodud Commerce’i leheelementide võimalikud dokumentide olekud.

| Dokumendi olek | Kirjeldus |
|---|---|
| Väljaregistreeritud | Kui CMS-i üksus on teile välja registreeritud, ei saa ükski teine volitatud süsteemi kasutaja seda redigeerida. Mis tahes üksusele tehtavad muudatused on nähtavad ainult teile. |
| Sisseregistreeritud | Kui CMS-i üksus on registreeritud, on kõik muudatused teistele volitatud süsteemi kasutajatele nähtavad ja need kasutajad saavad seejärel üksuse välja registreerida ja seda redigeerida. Iga registreerimine loob üksuse ajaloos dokumendi versiooni kirje. |
| Avaldatud | Kui CMS-i üksus on avaldatud, suunatakse see teie reaalajas saidile ja see muutub mitte volitatud välistele kasutajatele internetis leitavaks. Üksuseid saab avaldada ainult siis, kui need on registreeritud. |
| Salvestatud | Väljaregistreeritud CMS-i üksusele tehtud muudatused saab salvestada CMS-i enne, kui üksus registreeritakse või avaldatakse. Need salvestatud muudatused ei ole teistele autenditud süsteemi kasutajatele nähtavad enne, kui üksus on registreeritud. Need ei ole välistele kasutajatele nähtavad enne, kuni üksus on avaldatud. |
| Loobutud väljaregistreerimine | Kui väljaregistreeritud CMS-i üksusest loobutakse, kustutatakse kõik salvestatud muudatused ja üksus naaseb versioonile, mis oli viimati registreeritud. |

## <a name="additional-resources"></a>Lisaressursid

[Sisu lisamise viisid](add-manage-content.md)

[Lehe mudeli sõnastik](page-elements-overview.md)

[Avaldamisrühmadega töötamine](publish-groups.md)

[Moodulitega töötamine](work-with-modules.md)

[Fragmentidega töötamine](work-with-fragments.md)

[Mallide ja paigutuste ülevaade](templates-layouts-overview.md)

[Saidil navigeerimise kohandamine](customize-site-navigation.md)
