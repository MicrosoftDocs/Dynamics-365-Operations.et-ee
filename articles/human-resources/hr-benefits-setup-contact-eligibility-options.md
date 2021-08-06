---
title: Isikliku kontakti sobivuse suvandite konfigureerimine
description: Isiklike kontaktide sobivuse suvandite konfigureerimine rakenduses Microsoft Dynamics 365 Human Resources. Isiklikud kontaktid võivad olla kasusaajad või sõltuvad.
author: andreabichsel
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 071523e2a1e9de6f0ed2b77e4ad6802efb0073f7
ms.sourcegitcommit: 08797bc43e93ea05711c5a70dd7cdb82cada667a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6558245"
---
# <a name="configure-personal-contact-eligibility-options"></a>Isiklike kontaktide sobivuse suvandite konfigureerimine

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
