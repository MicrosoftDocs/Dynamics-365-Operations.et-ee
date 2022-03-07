---
title: Hankija arve sisestamisel ilmneb erand
description: Hankija arve sisestamisel ilmneb erand, "Erandiks on kutsumise sihtmärk".
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
ms.openlocfilehash: ecc63cb7d0d2392105d8e4290f8e837945ae0781
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476116"
---
# <a name="an-exception-occurs-during-vendor-invoice-posting"></a>Hankija arve sisestamisel ilmneb erand


## <a name="symptoms"></a>Sümptomid

Hankija arve sisestamisel saate järgmise erandi:

> Kutsumise siht on välja kutsunud erandi

## <a name="cause"></a>Põhjus

See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.

## <a name="resolution"></a>Lahendus

Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**. Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).
