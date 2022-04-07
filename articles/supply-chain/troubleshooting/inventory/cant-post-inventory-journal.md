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
ms.openlocfilehash: 5e8168a20a1fa4f52d28129eebb9931b31157ced
ms.sourcegitcommit: ab690bc897699ff8a4c489e749251fe0367050ca
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/26/2022
ms.locfileid: "8488963"
---
# <a name="inventory-journal-workflow-never-completes-and-the-journal-cant-be-processed"></a>Varude päeviku töövoog ei ole kunagi lõpetatud ja töövoogu ei saa töödelda

## <a name="symptoms"></a>Sümptomid

Pärast töölehe kinnitamise töövoogu esitamist lõpetab töövoo töötlemine vastamise ja te ei saa oma töölehti redigeerida ega töödelda.

## <a name="resolution"></a>Lahendus

On mitu põhjust, miks töövoo töötlemine ei pruugi olla lõpule viidud. Kontrollige järgmiste probleemide suhtes.

- Avage **Laohaldus &gt; Seadistus &gt; Varude halduse töövood** ja vaadake üle mõjutatud töövoo konfiguratsioon. Lisateavet vt [Varude töölehe kinnitamise töövood](../../inventory/inventory-journal-workflow.md).
- Töövoos võib tekkida erand või tõrge. Vaadake üle mõjutatud töövoo tööüksuse ajalugu, et näha, kas see sisaldab rakenduse tõrget, mis lõpetab töövoo.
- Varude töölehte saab uuendada või redigeerida ainult siis, kui see on kinnitatud. Kui tagasikutsumine on aktiivne, võite proovida töölehte tagasi kutsuda. Töövoo pakett-töö käivitamine võib olla peatatud mitmel põhjusel. Mõned neist põhjustest võivad olla põhjustatud töövoo raamistiku probleemist.
