---
title: Isiklike kontaktide sobivuse suvandite konfigureerimine
description: See teema selgitab, kuidas konfigureerida isiklike kontaktide sobivuse suvandeid rakenduses Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/24/2021
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
ms.openlocfilehash: e145acf6a6ba3333acfcc6e66dadd1f7d5deac65
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692306"
---
# <a name="configure-personal-contact-eligibility-options"></a>Isiklike kontaktide sobivuse suvandite konfigureerimine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See teema kirjeldab, kuidas konfigureerida soodustuste kasutamiseks isiklike kontaktide tüüpe rakenduses Microsoft Dynamics 365 Human Resources. Isiklikud kontaktid on need isikud, kellele teie plaanid kuuluvad (ülalpeetavad) või kes saavad teie plaanidest kasu (kasusaajad). Ülalpeetavad on tavaliselt abikaasad või lapsed. Kasusaajad võivad olla abikaasad, pered, usaldusisikud või lapsevanemad.

1. Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Isikliku kontakti sobivuse suvandid**.

2. Valige suvand **Uus**.

3. Määrake järgmiste väljade väärtused.

   | Väli | Kirjeldus |
   | --- | --- |
   | **Sobivuse suvand** | Kordumatu sobivuse suvandi nimi või kood, et tuvastada sobivuse suvandit. |
   | **Kirjeldus** | Sobivuse suvandi lühikirjeldus. |
   | **Kontakti sobivuskood** | Isikliku sobivuse suvandit kõige paremini kirjeldav süsteemikood. Saate valida järgneva seast. <ul><li>Seos</li><li>Üliõpilane</li><li>Liiga vana sõltuv</li><li>Liiga vana invaliidist sõltuv</li></ul> |
   | **Olek** | Sobivuse suvandi olek. Kui sobivuse suvandi olek on seatud passiivseks, ei saa te seda isiklike kontaktide abikõlblikkuse valikut isiklike kontaktide jaoks valida. |
   | **Seos** | Määrab seose isikliku kontakti ja töövõtja vahel. See väli on aktiivne ainult juhul, kui kontakti sobivuse kood on seatud suvandile Seos. |
   | **Vanus** | Soodustuse plaani sobiva isikliku kontakti maksimaalne vanus. See väli on aktiivne ainult siis, kui valite seose. Seda vanust võrreldakse isikliku kontakti arvutatud vanusega. Arvutatud vanus on: (katvuse kuupäev – isiklik kontakti sünnikuupäev / 365). See number on alati täisarv. |

4. Valige käsk **Salvesta**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
