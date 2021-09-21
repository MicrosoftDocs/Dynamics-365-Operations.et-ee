---
title: Varude päeviku töövoog ei ole kunagi lõpetatud ja töövoogu ei saa töödelda
description: Pärast töölehe kinnitamise töövoogu esitamist lõpetab töövoo töötlemine vastamise ja te ei saa oma töölehti redigeerida ega töödelda.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9430068f9c2d92c894817db04143297de6c6aa6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476082"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Varude päeviku töövoog ei ole kunagi lõpetatud ja töövoogu ei saa töödelda

## <a name="symptoms"></a>Sümptomid

Pärast töölehe kinnitamise töövoogu esitamist lõpetab töövoo töötlemine vastamise ja te ei saa oma töölehti redigeerida ega töödelda.

## <a name="resolution"></a>Lahendus

On mitu põhjust, miks töövoo töötlemine ei pruugi olla lõpule viidud. Kontrollige järgmiste probleemide suhtes.

- Avage **Laohaldus &gt; Seadistus &gt; Varude halduse töövood** ja vaadake üle mõjutatud töövoo konfiguratsioon. Lisateavet vt [Varude töölehe kinnitamise töövood](/dynamics365/supply-chain/inventory/inventory-journal-workflow.md).
- Töövoos võib tekkida erand või tõrge. Vaadake üle mõjutatud töövoo tööüksuse ajalugu, et näha, kas see sisaldab rakenduse tõrget, mis lõpetab töövoo.
- Varude töölehte saab uuendada või redigeerida ainult siis, kui see on kinnitatud. Kui tagasikutsumine on aktiivne, võite proovida töölehte tagasi kutsuda. Töövoo pakett-töö käivitamine võib olla peatatud mitmel põhjusel. Mõned neist põhjustest võivad olla põhjustatud töövoo raamistiku probleemist.
