---
title: Osaliste väljastuste ja osaliste saadetiste tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada osaliste väljastuste ja osaliste saadetistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645944"
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