---
title: Osaliste väljastuste ja osaliste saadetiste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada osaliste väljastuste ja osaliste saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b8cb887a4acd6fc1a691614dc666bbdbe4a34b1ff874c5d80cf492f2984d299
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742556"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a>Osaliste väljastuste ja osaliste saadetiste tõrkeotsing

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lahendada osaliste väljastuste ja osaliste saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a>Müügitellimuse väljastamise olek jääb osaliselt väljastatud olekusse ka pärast müügitellimuse arveldamist.

### <a name="issue-description"></a>Probleemi kirjeldus

Müügitellimus on kättetoimetamise tellimus, kuid ühel või mitmel kaubal on erinev tarneviis. Pärast tellimuse arveldamist on sellel veel väljastamise olekuks *Osaliselt väljastatud*.

Näiteks on müügitellimusel kaks kaupa: üks tarnimiseks ja üks komplekteerimiseks. Nii tarne kui ka komplekteerimine on tehtud. Seetõttu on mõlemad read arveldatud. Kuid väljastamise olekuks kuvatakse endiselt *Osaliselt väljastatud*, mis on eksitav.

### <a name="issue-resolution"></a>Probleemi lahendamine

Väljastamise olek rakendub ainult tellimuse ridadele, kus kaubad on laohalduse jaoks lubatud. Seetõttu jääb selle stsenaariumi korral väljastamise olekuks *Osaliselt väljastatud*. Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang. Väljastamise oleku värskendamiseks võib saatelehe ja arveldamise protsessi osana lisada laiendi.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]