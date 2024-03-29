---
title: Kontsernisisese müügitellimuse loomine ja arveldamine sisemiseks kasutamiseks
description: See artikkel selgitab, kuidas luua kontsernisisest müügitellimust sisemiseks kasutamiseks.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: a37b8ab1b3df10cdbd3bbb87410bc3dc70dc0ed0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873517"
---
# <a name="create-an-intercompany-sales-order-for-internal-use"></a>Kontsernisisese müügitellimuse loomine ja arveldamine sisemiseks kasutamiseks

[!include [banner](../../includes/banner.md)]

Tavaliselt luuakse kontsernisisene müügitellimus automaatselt, põhinedes kontsernisisesele ostutellimusele. Samuti saate käsitsi luua kontsernisisese müügitellimuse, mis loob seejärel kontsernisisese ostutellimuse kontsernisisese kliendi juriidilises isikus.

![Kontsernisisene müügiprotsess](media/intercompanyinternalsalesprocess.png)

## <a name="create-an-intercompany-sales-order-manually"></a>Kontsernisisese müügitellimuse käsitsi loomine

Läbige need juriidilise isiku B etapid, nagu on joonisel kujutatud.

1. Avage jaotis **Müügireskontro \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse loomiseks valige toimingupaanilt suvand **Müügitellimus**.
1. Valige lehel **Müügitellimuse loomine** kliendi konto. Veenduge, et kiirkaardil **Üldine** oleks märgitud ruut **Kontsernisisene**. See näitab, et valitud klient on kontsernisisene klient.
1. Sisestage või muutke andmed ning klõpsake nuppu **OK**, seejärel täitke tellimuse read tavapärasel viisil.

    **Tarneaadressi** väli kopeeritakse kontsernisisese müügitellimuse päisest kontsernisisese ostutellimuse päisesse. Välja **Kaubakoodi** väärtus, sealhulgas tootedimensioonid ning väljade **Tarnekuupäev** ja **Valuutakood** väärtused kopeeritakse kontsernisisese müügitellimuse ridadelt kontsernisisese ostutellimuse ridadele.

1. Seotud kontsernisisese ostutellimuse vaatamiseks valige tellimuse päises **Kontsernisisene**.
1. Kontsernisisese kaubavahetuse vaba kaubavaru kohta teabe kuvamiseks märkige tellimuse ridadel ruut **Kontsernisisene**.

> [!TIP]
> Kontsernisiseseid müügitellimusi saate vaadata lehel **Kontsernisisesed tellimused**.

> [!NOTE]
> Kui töötate kontsernisiseselt, on soovitatav tühjendada märkeruut **Kustuta tellimus pärast arveldamist** lehel **Müügireskontro parameetrid**. Vastasel juhul seotud ostutellimus kustutatakse. Me soovitame ka tühjendada märkeruut **Kustuta tellimus pärast arveldamist** lehel **Müügireskontro parameetrid**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
