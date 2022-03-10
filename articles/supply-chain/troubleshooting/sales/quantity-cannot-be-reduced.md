---
title: Kogust ei saa müügitellimuse tühistamisel vähendada
description: Kogust ei saa müügitellimuse tühistamisel vähendada.
author: hja-ms
ms.date: 5/17/2021
ms.topic: troubleshooting
ms.search.form: SalesTable_SalesCancelOrder, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: hja
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3453c83b5e8ead4269a6054167d73a0cd12381ba374b98bc407c01edaa68a1c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752630"
---
# <a name="the-quantity-cant-be-reduced-when-a-sales-order-is-canceled"></a>Kogust ei saa müügitellimuse tühistamisel vähendada

Tõrkekood: SYS138831

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Kogust ei saa vähendada. Tellimuse laokannete arv on liiga väike, kuna kogusele või osale sellest viidatakse väljaminekuorderiga või tootmistellimusega või kui see on märgitud teiste kannete suhtes.

## <a name="cause"></a>Põhjus

Kui töö on seotud müügitellimusega, ei saa müügitellimust tühistada enne töö tühistamist. See nõue kehtib ka juhul, kui müügitellimusega seotud töö on suletud.

## <a name="resolution"></a>Lahendus

Selle probleemi lahendamiseks täitke üks järgmistest toimingutest:

1. Tühista avatud töö.
1. Kustutage koorem.
1. Vähenda komplekteeritavat kogust.

### <a name="cancel-open-work"></a>Tühista avatud töö

Avatud töö tühistamiseks tehke järgmist.

1. Minge **Laohalduse \> Perioodiliste ülesannete juurde \> Puhastamine \>Tühista töö**.
1. Väljal **Töö ID** määrake töö ID, mida soovite tühistada ja millel on **Töö oleku** väärtuseks kas *Ava*, *Pooleli*, *Tühistatud*, *Kombineeritud* või *Suletud*.
1. Valige nupp **OK**.
1. Valige **Jah**, et kinnitada, et soovite töö tühistada.

### <a name="delete-the-load"></a>Kustutage koorem

Koorma kustutamiseks tehke järgmist.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Avage asjakohane müügitellimus.
1. Kiirkaardil **Müügitellimuse read** valige **Ladu \> Töö üksikasjad**.
1. Valige **Töö** lehel vahekaardil **Töö** grupis olev üksus **Töö** ja **Töö tühistamine**.
1. Veenduge, et **töö oleku** väli oleks seatud väärtusele *Tühistatud*.
1. Sulgege leht **Töö**.
1. Müügitellimuse üksikasjade lehel **müügitellimuse ridade** kiirkaardil valige **Ladu \> Koormuse üksikasjad**.
1. Valige tegumiribal suvand **Kustuta**.
1. Valige **Jah**, et kinnitada, et soovite koorma kustutada.
1. Sulgege **Koorem** leht.

### <a name="reduce-the-picked-quantity"></a>Vähenda komplekteeritavat kogust

Kui kogu töö on tühistatud, järgige komplekteeritud koguse vähendamiseks neid samme.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Avage asjakohane müügitellimus.
1. Kiirkaardil **Müügitellimuse read** valige **Uuenda rida \> Komplekteeri** tööriistaribalt.
1. Valige **Komplekteeritud** leheküljel **Kanded** jaotises rida, kus on välja **Väljamineku olek** väärtuseks määratud *Komplekteeritud*.
1. Valige jaotises **Kanded** tööriistaribalt **komplekteerimisrea lisamine**.
1. Valige jaotises **Komplekteerimise read** tööriistaribalt **Kinnita komplekteerimine**.
1. Sulgege **Komplekteeri** leht.
1. Valige lehe Müügitellimus tegumiriba vahekaardi **Müügitellimused** grupist **Arvuta** valik **Tühista**.
1. Valige **Jah**, et kinnitada, et soovite müügitellimuse tühistada.
