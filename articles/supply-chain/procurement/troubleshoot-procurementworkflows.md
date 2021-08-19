---
title: Hangete töövoogude tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada hangete töövoogudega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cda9da1a084bf3c04aef6911516ebee0facf1be61e94bfc1abab95e9dee75475
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729455"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a>Hangete töövoogude tõrkeotsing

Selles teemas kirjeldatakse, kuidas lahendada hangete töövoogudega töötamisel tekkivaid probleeme.

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a>Pärast ostutellimuse taasedastamist töövoosse pärast muudatust ilmneb tõrge: „Ostutellimust X saab muuta ainult olekus „Mustand”, kui muudatuste haldus on aktiveeritud”

See probleem ilmneb ainult siis, kui ostutellimuse olek oli enne muudatuste taotlemist *Kinnitatud*. Kui taotlete muudatusi, kui ostutellimuse olek on *Heaks kiidetud*, saab töövoogu edukalt töödelda.

### <a name="error-description"></a>Tõrke kirjeldus

Järgmine tõrge ilmneb töövoos, kui ostutellimus taasedastatakse pärast muutmist.

> Peatatud (tõrge): X++ erand: ostutellimust PO0000569 saab muuta ainult olekus „Mustand”, kui muudatuste haldus on aktiveeritud siin:<br>
SysWorkflowParticipantProvider-resolve<br>
SysWorkflowParticipantProvider-resolveParticipants<br>
SysWorkflowServiceProvider-resolveParticipant<br>
SysWorkflowQueue-resume

### <a name="issue-resolution"></a>Probleemi lahendamine

See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.

Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**. Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

Probleemi saab lahendada [selle Microsofti teabebaasi (KB) artikli kaudu](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a>Üks või mitu arvestuse jaotust on kas üle- või alajaotatud.

See probleem võib ilmneda ostutellimuse jaotuste vastuolu tõttu.

Probleemi blokeeringu tühistamiseks ja ostutellimuse lähtestamiseks olekusse *Mustand* avage **Hanked \> Perioodilised ülesanded \> Puhastamine \> Ostutellimuse jaotuse lähtestamine**. Lisateavet leiate ajaveebipostitusest [Ostutellimuse jaotustõrgete lahendamine rakenduses Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a>Kui tarnejääk tühistatakse ostutellimusel, mille puhul on muudatuste haldus sisse lülitatud, määratakse ostutellimuse olekuks „Kinnitatud”.

### <a name="issue-description"></a>Probleemi kirjeldus

Muudatuste haldust kasutava ostutellimuse puhul määratakse selle olekuks otse *Kinnitatud* ja töölehte ei looda, kui ainus taotletud muudatus on tarnejäägi tühistamine ühel või mitmel real.

### <a name="issue-resolution"></a>Probleemi lahendamine

Tarnejäägi tühistamine ei mõjuta kinnitustöölehe sisu. Seda funktsiooni tuleks kasutada siis, kui rida on osaliselt vastu võetud ja järelejäänud kogus tuleks tühistada protsessi etapis, mis toimub pärast seda, kui hankija on ostutellimuse kinnitanud.

Kui see peaks kajastuma ostutellimuse kinnitusel, tuleb kogust ostutellimuse real korrigeerida, nii et kinnitus oleks vajalik. Kui rea puhul pole midagi vastu võetud, on võimalik teise võimalusena kogus eemaldada. Sellisel juhul on vajalik taaskinnitus.

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a>Tühistatud ostutellimused kuvatakse ostutellimuse ettevalmistamise tööruumis mustandiloendis.

### <a name="issue-description"></a>Probleemi kirjeldus

Pärast olekus *Kinnitatud* ostutellimuste tühistamist kuvatakse tühistatud ostutellimused ikka tööruumis **Ostutellimuse ettevalmistamine** asuvas ostutellimuste mustandite loendis.

### <a name="issue-resolution"></a>Probleemi lahendamine

See probleem ilmneb ainult ostutellimuste puhul, mille korral kasutatakse muudatuste haldust. See ilmneb seetõttu, et tühistamist peetakse muudatuseks, mis tuleb kinnitada. Süsteem saab selle kinnitada automaatselt. Seetõttu tuleb tühistatud ostutellimus edastada kinnitamise töövoogu, et selle olekuks saaks määrata *Heaks kiidetud*. Seejärel ei kuvata ostutellimust enam tööruumis **Ostutellimuse ettevalmistamine** asuvas ostutellimuste mustandite loendis.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]