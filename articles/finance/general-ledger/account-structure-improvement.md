---
title: Konto struktuuri aktiveerimise jõudlustäiustus
description: Selles artiklis selgitatakse konto struktuuri aktiveerimisprotsessi uut jõudlustäiustust.
author: RyanCCarlson2
ms.date: 10/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-10-08
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: 42f8fcebba6465261489f74a9bb1dd46c2d5fa16
ms.sourcegitcommit: c6c2486be2359bd30106f7f52bda788239147d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/22/2022
ms.locfileid: "9713995"
---
# <a name="account-structure-activation-performance-enhancement"></a>Konto struktuuri aktiveerimise jõudlustäiustus

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

See jõudlustäiustus võimaldab teil aktiveerida konto struktuure kiiremini, käivitades mitu kandevärskendust samaaegselt. Lisaks märgitakse see struktuur pärast valideerimist aktiivseks ja kande töötlemist on võimalik jätkata, kuni olemasolevaid sisestamata kandeid värskendatakse uude struktuuri. Kuna kande värskendamisteks võib kuluda aega, saate jälgida oma aktiveerimise olekut, valides lehe **Konto struktuurid** ruudustiku kohal suvandi **Kuva aktiveerimise olek**. Samuti saate vaadata oma aktiveerimise olekut, valides toimingupaneelil suvandi **Kuva** ja seejärel valides rippmenüüst suvandi **Aktiveerimise olek**.

[![Konto struktuuride leht.](./media/AccountStructure1.png)](./media/AccountStructure1.png)

Kui olete valinud suvandi **Kuva aktiveerimise olek**, kuvatakse dialoogiaken, kus näidatakse aktiveerimisprotsessi jooksul töötavaid üksikuid ülesandeid. Saate vaadata iga ülesande olekut ja pärast ülesande lõpule viimist selle lõpetamise kuupäeva ja aega.

[![Konto struktuuri aktiveerimise ajakava.](./media/AccountStructureTimeline.png)](./media/AccountStructureTimeline.png)

## <a name="account-structure-activation-tips"></a>Konto struktuuri aktiveerimise nõuanded

Konto struktuuri aktiveerimise dialoogiaknas, mis kuvatakse konto struktuuri mustandis suvandi **Aktiveeri** valimisel, on vahekaardi jaotis nimega **Värskenda sisestamata kandeid**. See jaotis sisaldab valikut **Sundvärskendamine**. Saate valida selle suvandi kõikide sisestamata kannete praegusesse struktuuri värskendamiseks. Kuid peaksite kasutama seda valikut üksnes tõrke ilmnemisel või kui Microsofti tugiteenus on soovitanud teil seda kasutada.

Siin on mõningad tegurid, mis mõjutavad aktiveerimisprotsessi jõudlust.

- Suur hulk sisestamata töölehe kirjeid.
- Suur hulk avatud lähtedokumendi kirjeid, nagu vaba tekstiga arved, hankija arved ja seotud dokumendid, mis kasutavad lähtedokumendi raamistikku ja millel on avatud arvestuse jaotus.
- Üksuse TaxUncommitted andmete hulk.
- Avatud eelarve andmete hulk.
- Töölehe andmete importimine aktiveerimisülessannete töötamise ajal.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
