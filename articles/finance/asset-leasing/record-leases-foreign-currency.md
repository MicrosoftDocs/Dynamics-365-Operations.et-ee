---
title: Rendi kirjendamine välisvaluutas
description: Selles teemas selgitatakse, kuidas kirjendada rendilepinguid muudes valuutades peale arvestusvaluuta või aruandlusvaluuta.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fd4d04ae7e89b8ce41ed745c643b8e736484789d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241486"
---
# <a name="record-leases-in-foreign-currencies"></a>Rendi kirjendamine välisvaluutas

[!include [banner](../includes/banner.md)]

Vara rentimise kontod rentidele, mis on muud valuutas kui arvestusvaluuta või aruandevaluuta luuakse lehel **Pearaamatu seadistamine**. Kõik rendid tuleb sisestada nende tehingu valuutas. Teisisõnu tuleb need sisestada rendilepingus määratud valuutas. Selles teemas selgitatakse, kuidas kirjendada rendilepinguid muudes valuutades peale arvestusvaluuta või aruandlusvaluuta.

Kui sisestate rendilepingu välisvaluutas, amortiseeritakse kasutamisõiguse esemeks olev vara nii arvestusvaluutas kui ka aruandevaluutas. Need valuutad konfigureeritakse lehel **Pearaamatu seadistamine**. Seda käitumist kasutatakse ka põhivarades. Kui loote rendilepingu välisvaluutas, valige tehingu valuuta väljal **Valuuta**.

Arvestusvaluuta vahetuskurss on vaikimisi välja **Arvestusvaluuta vahetuskurss** väärtus. Aruandlusvaluuta vahetuskurss on vaikimisi välja **Aruandlusvaluuta vahetuskurss** väärtus. Need vahetuskursid kehtisid rendilepingu alguskuupäeval. Väljad **Arvestusvaluuta vahetuskurss** ja **Aruandlusvaluuta vahetuskurss** asuvad kiirkaadil **Arvestus- ja aruandlusvaluuta vahetuskursi teave**, mis asub lehel **Rendi üksikasjad**.

1. Märkige märkeruut **Fikseeritud kurss**, et alistada automaatselt sisestatud vahetuskurss ja seejärel sisestage uus kurss.
2. Teistes väljades sisestage rendi jaoks nõutav teave ja seejärel valige **Loo graafikud**.
3. Valige uuel lehel **Rendi üksikasjad** suvand **Raamatud**.
4. Kinnitage lehel **Rendiraamat**, mis asub vahekaardil **Arvestus- ja aruandlusvaluuta vahetuskursi teave** väljade **Arvestusvaluuta algne kasutamisõiguse esemeks olev vara** ja **Aruandlusvaluuta algne kasutamisõiguse esemeks olev vara** väärtused. Kõik need väljad näitavad tõlgitud kasutamisõiguse esemeks oleva vara saldot vastavas valuutas. Neid välju uuendatakse iga kord, kui muudate finantsteavet. Enne maksegraafiku kinnitamist valige **Loo graafikud**.

    Algne tunnustamise töölehe kirje kirjendab kasutamisõiguse esemeks olevat vara, mis kasutab rendilepingus loetletud valuutakursse. Töölehe kirje hõlmab ka väljade **Arvestusvaluuta algne kasutamisõiguse esemeks olev vara** ja **Aruandlusvaluuta algne kasutamisõiguse esemeks olev vara** väärtusi.

## <a name="subsequent-measurement-for-foreign-currency-leases"></a>Välisvaluutas rentide järgnev mõõtmine

Kulumi graafik näitab eeldatavat kulumi kulu summasid aruandevaluutas, arvestusvaluutas ja tehingu valuutas.

Kasutamisõiguse esemeks oleva vara saldode ja kulumi summade vaatamiseks kas aruandevaluutas või arvestusvaluutas avage leht **Vara kulumi graafik** ja valige märkeruut **Kuva arvestusvaluuta summad** või **Kuva aruandevaluuta summad**.

Kui loote kulumiarvestuse kulu töölehe kanded välisvaluutas nomineeritud rendilepingule, kasutab kanne rendilepingus loetletud valuutakursse. See kasutab ka väljade **Arvestusvaluuta algne kasutamisõiguse esemeks olev vara** ja **Aruandlusvaluuta algne kasutamisõiguse esemeks olev vara** väärtusi.

Lõpliku kulumi summa saab arvutada veidi erineva vahetuskursi abil, nii et kasutamisõiguse esemeks olev vara amortiseeritakse täielikult nii arvestusvaluuta kui ka aruandevaluuta puhul.

Kui rendileping on ümberklassifitseeritud kui **Edasilükatud rent**, tühjendab süsteem automaatselt arvestus- ja aruandlusvaluutad, kui need on juba määratletud.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]