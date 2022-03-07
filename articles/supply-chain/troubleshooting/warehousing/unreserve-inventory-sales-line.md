---
title: Varude reserveerimist müügitellimuste real ei saa tühistada
description: Kui müügirea suhtes on avatud töö ja te proovite varusid realereservimata eemaldada, kuvatakse tõrketeade. Lõpetage või kustutage töö reserveerimise vabastamiseks.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476129"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Varude reserveerimist müügitellimuste real ei saa tühistada

## <a name="symptoms"></a>Sümptomid

Kui müügitellimuse rea suhtes on avatud töö ja te proovite selle rea varusid reservimata eemaldada, kuvatakse tõrketeade.

> Reserveeringuid ei saa eemaldada, kuna loodud töö põhineb reserveeringutel.

## <a name="resolution"></a>Lahendus

Uurige, kas avatud pakkimisgrupi töö on olemas, et tuua kaup pakkimisühiku teise asukohta (nt *Uks*). Vaadake üle kirjed **Töö loomise ajaloo logi** ja **Töö üksikasjade** lehtedel, et teha kindlaks, mis kaupa füüsiliselt broneerib, ja seejärel lõpetage või kustutage töö, et broneeringut vabastada.
