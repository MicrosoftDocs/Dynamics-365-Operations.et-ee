---
title: Isiklike kontaktide sobivuse suvandite konfigureerimine
description: See artikkel selgitab, kuidas konfigureerida Microsofti isiklike kontaktide sobivuse suvandeid Dynamics 365 Human Resources.
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
ms.openlocfilehash: 251a12b0da364744f1d8c84324099708a2f816a1
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749278"
---
# <a name="configure-personal-contact-eligibility-options"></a>Isiklike kontaktide sobivuse suvandite konfigureerimine


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel selgitab, kuidas konfigureerida isiklike kontaktide tüüpe, mida saab Microsofti soodustustes kasutada Dynamics 365 Human Resources. Isiklikud kontaktid on need isikud, kellele teie plaanid kuuluvad (ülalpeetavad) või kes saavad teie plaanidest kasu (kasusaajad). Ülalpeetavad on tavaliselt abikaasad või lapsed. Kasusaajad võivad olla abikaasad, pered, usaldusisikud või lapsevanemad.

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
   | **Vanus** | Soodustusplaani jaoks sobiliku isikliku kontakti minimaalne vanus. See väli on aktiivne ainult siis, kui valite seose. Seda vanust võrreldakse isikliku kontakti arvutatud vanusega. Arvutatud vanus on: (katvuse kuupäev – isiklik kontakti sünnikuupäev / 365). See number on alati täisarv. |

4. Valige käsk **Salvesta**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
