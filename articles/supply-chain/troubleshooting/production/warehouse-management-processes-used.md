---
title: Warehouse management protsessid, mida praegu kasutatakse
description: Töö reserveerimisel või vabastamisel võidakse kuvada teade, et praegu kasutatakse laohaldusprotsesse. Lahendage probleem ühe nimetatud sammuga.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476072"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Tööd ei saa reserveerida ega vabastada, sest protsessid on praegu kasutusel

## <a name="symptoms"></a>Sümptomid

Diskreetse tootmisega töötamisel kuvatakse järgmine tõrge:

> Warehouse management protsessid, mida praegu kasutatakse. Kui tööread ei ole veel registreeritud, saate loodud töö ja koorma või saadetise read tühistada ning jätkata komplekteerimise või saatmise protsessiga.

## <a name="cause"></a>Põhjus

See probleem ilmneb juhul, kui proovite reserveerida või vabastada tööd rea jaoks, kuid laokande olek on *Komplekteeritud*, mis näitab, et materjal on komplekteeritud.

## <a name="resolution"></a>Lahendus

Selle probleemi lahendamiseks järgige üht järgmistest sammudest.

- Muutke tootmistellimuse olek tagasi väärtusele *Hinnanguline* või *Väljastatud*.
- Avage leht vastava tootmistellimuse üksikasjade kohta. Valige tegumiribal vahekaardil **Ladu** grupis **Peatamine** valik **Peata ja Tühista**, et tühistada kõik komplekteeritud kanded. Seejärel valige tootmistellimuse töötlemiseks **Eemalda peatus**.

Siin on *Komplekteerimise tühistamise* ja *Peatamise* funktsioonide kirjeldus:
  
- **Komplekteerimise tühistamine** – See funktsioon tühistab laokannete oleku koosluse ridade ja valemi ridade jaoks, mille olek on *Komplekteeritud* *tellimuse alusel*. Kui tooraine komplekteerimise töö on lõpetatud, seatakse ridade olekuks *Komplekteeritud*. See olek takistab tootmistellimuse lähtestamist *Loodud* olekusse. Sel juhul saate kasutada funktsiooni *Tühista komplekteerimine*, et ennistada kanded *Komplekteeritud* olekust ja seejärel lähtestada tootmistellimus olekusse *Loodud*.
- **Peata** – See funktsioon määrab tootmistellimusele **Peatatud** lipu, et vältida tellimuse oleku uuendamist. **Peatatud** lipu leiate **Lao** FastTab-is tootmistellimuse üksikasjade lehelt.

> [!NOTE]
>
> - Nupud on nähtavad ainult siis, kui tootmistellimused on loodud kaubale, mis on lao protsesside jaoks lubatud.
> - **Peata** grupp on nähtav ainult tootmistellimuse üksikasjade lehe tegumiriba **Lao** vahekaardil. See ei ole kuvatud **Lao** FastTab-is **Tootmistellimuste** loendi lehel.
