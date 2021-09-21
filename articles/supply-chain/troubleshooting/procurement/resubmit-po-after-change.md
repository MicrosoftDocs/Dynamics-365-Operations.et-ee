---
title: Tõrge ostutellimuse töövoole pärast muutmist taasedastamisel
description: Tõrge ostutellimuse töövoole pärast muutmist taasedastamisel
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4b8465d198c440f27a4b3cc4268445e0aa450f5b
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476167"
---
# <a name="error-on-resubmitting-a-purchase-order-to-a-workflow-after-a-change"></a>Tõrge ostutellimuse töövoole pärast muutmist taasedastamisel


## <a name="symptoms"></a>Sümptomid

Järgmine tõrge ilmneb töövoos, kui ostutellimus taasedastatakse pärast muutmist.

> Peatatud (tõrge): X++ erand: ostutellimust PO0000569 saab muuta ainult olekus „Mustand”, kui muudatuste haldus on aktiveeritud siin:<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

See probleem ilmneb ainult siis, kui ostutellimuse olek oli enne muudatuste taotlemist *Kinnitatud*. Kui taotlete muudatusi, kui ostutellimuse olek on *Heaks kiidetud*, saab töövoogu edukalt töödelda.

## <a name="resolution"></a>Lahendus

See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.

Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**. Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Probleemi saab lahendada [selle Microsofti teabebaasi (KB) artikli kaudu](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).
