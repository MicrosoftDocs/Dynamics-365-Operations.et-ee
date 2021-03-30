---
title: Kaasa füüsiline väärtus
description: Märkeruutu Kaasa füüsiline väärtus kiirkaardil Laomudel või lehel Kauba mudeligrupid kasutatakse määramiseks, kas füüsiliselt värskendatud kandeid arvestatakse kauba jooksva keskmise omahinna arvutuses.
author: AndersGirke
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a769f9cb5b34581b9bd20b19bcd8bcd0b1c7bff8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205426"
---
# <a name="include-physical-value"></a>Kaasa füüsiline väärtus

[!include [banner](../includes/banner.md)]

Märkeruutu Kaasa füüsiline väärtus kiirkaardil Laomudel või lehel Kauba mudeligrupid kasutatakse määramiseks, kas füüsiliselt värskendatud kandeid arvestatakse kauba jooksva keskmise omahinna arvutuses.

Märkeruudul **Kaasa füüsiline väärtus** on järgmised väärtused.

| Väärtus    | Tulemus                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Valitud | Jooksva keskmise omahinna arvutamiseks kasutatakse nii füüsiliselt kui ka rahaliselt värskendatud kandeid. |
| Tühjendatud  | Jooksva keskmise omahinna arvutamiseks kasutatakse ainult rahaliselt värskendatud kandeid.                                     |

Märkeruudul on veidi erinevad mõjud, olenevalt kasutatavast laomudelist.

-   Kui märgite ruudu **Kaasa füüsiline väärtus** laomudeli FIFO (elavjärjekorra), LIFO (viimaste esmaväljastamine) või LIFO kasutamisel, korrigeerib lao sulgemine ka füüsiliselt värskendatud kandeid.
-   Kui te ei märgi laomudelite kasutamisel ruutu **Kaasa füüsiline väärtus**, teeb lao sulgemine tasakaalustusi ainult rahaliselt värskendatud kannetes.
-   Kui kasutate kaalutud keskmise või kaalutud keskmise kuupäeva laomudelit, tasakaalustab lao sulgemine vaid rahaliselt värskendatud kanded, olenemata sellest, kas märgite ruudu **Kaasa füüsiline väärtus**.

**Näide 1** Olete märkinud ruudu **Kaasa füüsiline väärtus** ja saate järgmised ostutellimused.

-   Ostutellimus kogusele 2 omahinnaga 10,00 USA dollarit, mis on saatelehega sisestatud.
-   Ostutellimus kogusele 3 omahinnaga 12,00 USA dollarit, mis on arvega sisestatud.

Sellisel juhul on jooksev keskmine omahind 11,20 USA dollarit = (2x10+3x12)/(2+3), sest omahinna arvutamiseks kasutatakse nii füüsiliselt kui ka rahaliselt värskendatud kandeid. 

**Näide 2** Te pole märkinud ruutu **Kaasa füüsiline väärtus** ja kauba seadistuse omahind on 10.00 USD. 

-   Saate ostutellimuse kogusele 20 omahinnaga 12.00 USA dollarit, mis on saatelehega sisestatud

Müügitellimuse sisestamisel sisestatakse kulusumma 10.00 USD kulusumma, sest jooksev keskmine omahind ei hõlma füüsiliselt sisestatud kandeid. 

> [!NOTE]
> Võrdluseks, kui märgite selle kauba puhul müügitellimuse sisestamisel ruudu **Kaasa füüsiline väärtus**, on sisestatav kulusumma 12,00 USA dollarit.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]