---
title: Tellimuse tühistamisel ei saa reserveeringuid eemaldada
description: Kui töö on seotud müügitellimusega, ei saa müügitellimust tühistada enne töö tühistamist. Nii tegemiseks järgige kolme järgmist sammu.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: a8d947e64568246dba5eff3c21fd3920b6494b73
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476131"
---
# <a name="reservations-cannot-be-removed-when-canceling-an-order"></a>Tellimuse tühistamisel ei saa reserveeringuid eemaldada

## <a name="symptoms"></a>Sümptomid

Kui töö on seotud müügitellimusega ja te proovite seda tellimust tühistada, saate järgmise tõrketeate:

> Reserveeringuid ei saa eemaldada, kuna loodud töö põhineb reserveeringutel.

Kui töö on seotud müügitellimusega, ei saa müügitellimust tühistada enne töö tühistamist. See nõue kehtib ka juhul, kui müügitellimusega seotud töö on suletud.

## <a name="resolution"></a>Lahendus

Selle probleemi lahendamiseks tehke järgmist:

1. Tühistage töö ja pange varud tagasi soovitud asukohta. Valige müügitellimuse asjakohane koorem ja valige koorma real kas **Vähenda komplekteeritud kogust** või toimingupaanil **Tühista töö**.

    Töö olek on nüüd *Tühistatud* ning varude tagasipanemiseks asukohta, mida kirjeldati tühistamise ajal, luuakse automaatselt uus varude liikumise töö, mida ka kohe töödeldakse.

2. Kustutage koorem. Saadetis kustutatakse samuti.

3. Nüüd peaks olema teil võimalik müügitellimust tühistada.
