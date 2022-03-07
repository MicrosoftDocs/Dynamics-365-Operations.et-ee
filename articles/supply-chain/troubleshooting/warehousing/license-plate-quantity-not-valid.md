---
title: Kogus on sissetulevate tellimuste registreerimisel kehtetu
description: "Kui litsentsiplaadi jaoks määratud kogus ületab koguse, mis praeguste mõõtmete jaoks tuleb veel saada, kuvatakse tõrketeade: 'Kogus ei kehti.'"
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5099b320447bf59c72f5017564ea660f19c690a5
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476160"
---
# <a name="license-plate-quantity-is-not-valid-when-registering-inbound-orders"></a>Sissetulevate tellimuste registreerimisel ei kehti numbrimärgi kogus

## <a name="symptoms"></a>Sümptomid

Kui proovite plaanitud tellimusi kindlustada, kuvatakse järgmine tõrketeade:

> Kogus on kehtetu.

Kui väli **Litsentsiplaadi grupeerimise poliitika** on seatud väärtusele *Kasutaja määratud* mobiilse seadme menüükäsule, mida kasutatakse sissetulevate tellimuste registreerimiseks, saate selle tõrketeate ja registreerimist ei saa lõpule viia.

## <a name="cause"></a>Põhjus

Kui *kasutaja määratletud* on kasutatud litsentsiplaadi grupeerimispoliitikana, tükeldab süsteem sissetulevad varud eraldi litsentsiplaatideks, nagu näitab ka ühiku seeriagrupp. Kui vastuvõetava kauba jälgimiseks kasutatakse partii- või seerianumbreid, tuleb iga partii või seerianumbri kogus registreerida registreeritud numbrimärgi kohta. Kui litsentsiplaadi jaoks määratud kogus ületab koguse, mis praeguste mõõtmete jaoks tuleb veel saada, kuvatakse tõrketeade.

## <a name="resolution"></a>Lahendus

Kui registreerite kauba mobiilse seadme menüü-üksuse abil, kus väli **Litsentsiplaadi grupeerimise poliitika** väärtuseks on seatud *Kasutaja määratud*, võib süsteem nõuda litsentsiplaadi numbrite, partii- või seerianumbrite kinnitamist või sisestamist.

Litsentsiplaadi kinnituslehel näitab süsteem praeguse litsentsiplaadi jaoks eraldatud kogust. Partii- või seeriakinnituse lehtedel näitab süsteem kogust, mis praegusel litsentsiplaadile peab veel laekuma. See hõlmab ka välja, kus saate sisestada koguse, et registreerida see litsentsiplaadi ja partii- või seerianumbri kombinatsioon. Sel juhul veenduge, et litsentsiplaadile registreeritav kogus ei ületaks vastuvõetud kogust.

Kui sissetuleva tellimuse registreerimisel luuakse liiga palju litsentsiplaate, saab välja **Litsentsiplaadi grupeerimise poliitika** väärtust muuta väärtuseks *Litsentsiplaadi grupeerimine*, määrata kaubale uus ühiku seeriagrupp või üksuse seeriagrupi suvand **litsentsiplaadi grupeerimise** inaktiveerida.
