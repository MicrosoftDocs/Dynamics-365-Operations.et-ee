---
title: Pearaamatu töölehe tüübid
description: Selles artiklis kirjeldatakse töölehe tüüpe, mille saate finantstöölehtede jaoks seadistada.
author: kweekley
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 883c54b84ed31384a28c31c8b814c75d340d020e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901309"
---
# <a name="ledger-journal-types"></a>Pearaamatu töölehe tüübid

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse töölehe tüüpe, mille saate finantstöölehtede jaoks seadistada. Kasutage töölehe **nimede lehte** töölehtede häälestamiseks, mida saate kasutada kogu Dynamics 365 Finance'is.

| Töölehe tüüp                      | Eesmärk                       | Sisestage kanded sellel lehel                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Eraldamine                        | Looge eraldamiskandeid eraldamise töölehel. Enne kui saate luua eraldamistöölehe, peate looma eraldamisreegli lehel **Pearaamatu eraldamisreegel**.      | Protsessi eraldamise taotlus             |
| Kinnitus                          | Sisestage hankija arveid, mis on sobivate pearaamatukontode jaoks kinnitatud.  | Arve kinnitamise tööleht                                       |
| Pangatšeki pöördtehing               | Tühistage sisestatud tšekk. Selle töölehe tüübi kasutamiseks valige suvand **Kasuta maksete storneerimiseks läbivaatusprotsessi** lehel **Sularaha- ja pangahalduse parameetrid**.   | Tühistamistšekid, makse tagasivõtmine                   |
| Panga sissemaksekorralduse tühistamine    | Tühistage deposiitkviitung. Selle töölehe tüübi kasutamiseks valige suvand **Kasuta deposiitkviitungite maksete tühistamiseks läbivaatusprotsessi** lehel **Sularaha- ja pangahalduse parameetrid**.   | Maksekorralduse maksmise tühistamised            |
| Eelarve                            | Töödelge eelarve eraldamisi. Selle töölehe tüübi kasutamiseks valige suvand **Eelarve jaotamise lubamine** lehel **Pearaamatu parameetrid**. Eelarve töölehe kirjed sisaldavad teavet, mis põhineb pearaamatukontodel, mis on määratletud lehel **Sisestamisdefinitsioonid**.                                                        |                                                                |
| Kliendipoolne pangatähe aktsepteerimine  | Looge käskveksli jaoks kliendi aktsepteerimise kanded.             | Koosta pangatähe tööleht, koosta pangatähe tööleht uuesti |
| Kliendi pangaülekanne          | Looge käskveksli ülekandefail, mida saab saata teie organisatsiooni panka. Selle töölehe tüübi kasutamiseks kustutage suvand **Automaatne tasakaalustus** lehel **Müügireskontro** **parameetrid**.            | Rahaülekanne                                                     |
| Kliendi koostatud pangatäht    | Looge kliendi koostatud käskveksli kanded. Selle töölehe tüübi kasutamiseks kustutage suvand **Koostamise töölehe automaatne loomine ja sisestamine arvete sisestamisel** lehel **Makseviisid – kliendid**.   | Koosta pangatähe tööleht                                  |
| Kliendi makse                  | Looge kliendi maksekanded.                             | Maksetööleht             |
| Kliendi vaidlustatud pangatäht | Looge kliendi vaidlustatud käskveksli kanded.                    | Vaidlusta pangatähe tööleht                               |
| Kliendi uuesti koostatud pangatäht  | Looge kliendi uuesti koostatud käskveksli kanded.                     | Koosta pangatähe tööleht uuesti                                |
| Kliendi tasakaalustuse pangatäht  | Looge kliendi tasakaalustatud käskveksli kanded.                       | Tasakaalusta pangatähe tööleht                                |
| Kord päevas                             | Looge päevaraamatus igapäevased kanded.                          | Päevaraamat                                                |
| Eemaldamine                       | Looge eemaldamise töölehel eemaldamiskanded. Selle töölehe tüübi kasutamiseks valige suvandid **Kasuta finantsiliseks eemaldamisprotsessiks** ja **Finantskonsolideerimise protsessi jaoks kasutamine** lehel **Juriidilised isikud**. Enne kui saate seda töölehe tüüpi kasutada, peate looma lehel **Pearaamatu eemaldamisreegel** pearaamatu eemaldamisreegli. | Eemaldamine                                                    |
| Põhivara eelarve                | Looge põhivara eelarve registrikanded.                                                                                                                                                                                                                                                                                                                 | Põhivara eelarve                                             |
| Arveregister                  | Registreerige põhiteave hankijate arvete kohta.                                                                                                                                                                                                                                                                                                           | Arveregister                                               |
| Palga väljamaksed              | Väljastage maksed, mis põhinevad palga maksmise väljavõtetel. Sellel töölehel ei saa kandeid käsitsi sisestada. Peate looma palga väljavõtted ja esitama need seejärel maksmiseks.                                                                                                                                                              |                                                                |
| Perioodiline                          | Looge perioodilise töölehe jaoks perioodilised kanded.                                                                                                                                                                                                                                                                                                      | Perioodilised töölehed                                              |
| Sisesta põhivara                 | Sisestage põhivarakanded.                                                                                                                                                                                                                                                                                                                              | Põhivarad                                                   |
| Projekt - Kulud                | Looge projekti kulukanded.                                                                                                                                                                                                                                                                                                                        | Expense                                                        |
| Aruandlusvaluuta korrigeerimine     | Pearaamatukonto saldode aruandlusvaluuta korrigeerimine.               | Aruandlusvaluuta korrigeerimise töölehed                         |
| Statistikakanded            | Looge statistilised kanded.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Hankija pangaülekanne            | Looge võlatähe ülekandefail, mida saab saata teie organisatsiooni panka.                                                                                                                                                                                                                                                                      | Rahaülekande tööleht                                             |
| Maksed hankijale               | Looge hankija väljaminekukanne.                                                                                                                                                                                                                                                                                                                    | Maksetööleht                                                |
| Hankija koostatud võlatäht       | Koostage hankija võlatäht makseviisina. Selle töölehe tüübi kasutamiseks kustutage suvand **Koostamise töölehe automaatne loomine ja sisestamine arvete sisestamisel** lehel **Makseviisid – hankijad**.                                                                                                                                          | Koosta võlatähe tööleht                                   |
| Hankijaarvete kaust ilma sisestuseta | Looge hankija arve kanded, mida ei ole veel ajutisele saabumiskontole sisestatud.                                                                                                                                                                                                                                                             | Hankija arve kaust ilma sisestamise üksikasjadeta                  |
| Hankija arvete kaust               | Looge hankija arve kausta kanded.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Hankijaarvete kirjendamine          | Sisestage hankija arved, mis on töölehel.                                                                                                                                                                                                                                                                                                                 | Arve tööleht                                                |
| Hankija uuesti koostatud võlatäht     | Koostage uuesti võlatäht, mille teie organisatsiooni pank on eelnevalt tasunud.                                                                                                                                                                                                                                                                      | Koosta võlatähe tööleht uuesti                                 |
| Hankija tasakaalustatud võlatäht     | Looge hankija tasakaalustatud võlatähe kanded.                                                                                                                                                                                                                                                                                                          | Tasakaalusta võlatähe tööleht                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
