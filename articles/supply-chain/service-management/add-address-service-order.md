---
title: Teenusetellimusele aadressi lisamine
description: See artikkel kirjeldab, kuidas lisada teenuse tellimusele kliendi aadress.
author: sorenva
ms.date: 06/15/2020
ms.topic: article
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c485c50bab7c2e945aa0f0fc0601008dcebd3328
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015721"
---
# <a name="add-an-address-to-a-service-order"></a>Teenusetellimusele aadressi lisamine

[!include [banner](../includes/banner.md)]

See artikkel kirjeldab, kuidas lisada teenuse tellimusele kliendi aadress. Teenustellimuse loomisel edastatakse aadressiteave projektilt, millele on lisatud teenustellimus. Siiski saate valida alternatiivse asukoha klientide, hankijate, laoalade, ladude, teenusetellimuste ja projektide aadresside hulgast, mis on juba rakendusse Microsoft Dynamics AX sisestatud.

Saate ka luua uue aadressi. Vaikimisi kantakse uus aadress projekti üle. Siiski saate määrata, et uus aadress on asjakohane vaid teenuse selle eksemplari jaoks. Sel juhul ei kanta uut aadressi projekti üle.

## <a name="create-a-customer-address-for-a-service-order"></a>Kliendi aadressi loomine teenusetellimuse jaoks

Teenusetellimusele aadressi lisamiseks tehke järgmist.

1. Minge teenusehalduse **teenusetellimuste** \> **teenusetellimuste** \> **loendisse**.

1. Avage teenusetellimus, mille jaoks soovite aadressi luua.

1. Avage vahekaart **Päis**.

1. Laiendage **aadressi** kiirkaarti ja seejärel valige **kiirkaardi** tööriistaribalt Lisa aadress.

1. Dialoogiaknas **Uus** aadress sisestage aadressi kordumatu nimi ja täitke ülejäänud väljad. 

    > [!WARNING]
    > Kui sisestate olemasoleva aadressi nime, kirjutab ülejäänud väljadele sisestatud teave üle olemasoleva aadressi teabe.

1. Valige **OK**, et kopeerida uus aadress oma teenustellimusele.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Teenustellimusele muu aadressi määramine

Teenusetellimusele alternatiivse aadressi lisamiseks tehke järgmist.

1. Minge teenusehalduse **teenusetellimuste** \> **teenusetellimuste** \> **loendisse**.

1. Avage teenusetellimus, mille jaoks soovite alternatiivse aadressi sisestada.

1. Avage vahekaart **Päis**.

1. Laiendage **aadressi** kiirkaarti ja seejärel valige **kiirkaardi tööriistaribalt** Muu aadress.

1. Valige dialoogiaknas **Aadressi** valik **suvand Teenusetellimused** dialoogiakna kohal kuvatavast ripploendist.

1. Valige aadress ja seejärel valige OK **,** et kopeerida see oma teenustellimusele.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]