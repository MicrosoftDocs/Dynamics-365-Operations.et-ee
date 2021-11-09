---
title: Ostutellimuse kinnitamisel ilmneb tõrge „Objektiviidet pole määratud”
description: Ostutellimuse kinnitamisel ilmneb tõrge „Objektiviidet pole määratud”
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 78e5e365f7197c1a0c25bf6eb63bcd5bd0f482ed
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476141"
---
# <a name="error-object-reference-not-set-occurs-during-purchase-order-confirmation"></a>Ostutellimuse kinnitamisel ilmneb tõrge „Objektiviidet pole määratud”

## <a name="symptoms"></a>Sümptomid

Ostutellimuse kinnitamisel saate järgmise erandi:

> Objektiviidet pole seatud

## <a name="cause"></a>Põhjus

See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.

## <a name="resolution"></a>Lahendus

Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**. Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).