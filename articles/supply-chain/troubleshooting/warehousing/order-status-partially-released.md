---
title: Tellimuse olek jääb osaliselt väljastatud olekusse isegi pärast müügitellimuse arveldamist
description: Mõnel juhul müügitellimuse väljastamise olek jääb osaliselt väljastatud olekusse ka pärast müügitellimuse arveldamist. See lehekülg selgitab, miks ja milline on võimalik lahendus.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8bfe7ecfd4beb6e77e8dd1e23ccd896d067bdb51
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476130"
---
# <a name="order-status-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Tellimuse olek jääb osaliselt väljastatud olekusse isegi pärast müügitellimuse arveldamist

## <a name="symptoms"></a>Sümptomid

Müügitellimus on kättetoimetamise tellimus, kuid ühel või mitmel kaubal on erinev tarneviis. Pärast tellimuse arveldamist on sellel veel väljastamise olekuks *Osaliselt väljastatud*.

Näiteks on müügitellimusel kaks kaupa: üks tarnimiseks ja üks komplekteerimiseks. Nii tarne kui ka komplekteerimine on tehtud. Seetõttu on mõlemad read arveldatud. Kuid väljastamise olekuks kuvatakse endiselt *Osaliselt väljastatud*, mis on eksitav.

## <a name="workaround"></a>Vastukaal

Väljastamise olek rakendub ainult tellimuse ridadele, kus kaubad on laohalduse jaoks lubatud. Seetõttu jääb selle stsenaariumi korral väljastamise olekuks *Osaliselt väljastatud*. Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang. Väljastamise oleku värskendamiseks võib saatelehe ja arveldamise protsessi osana lisada laiendi.
