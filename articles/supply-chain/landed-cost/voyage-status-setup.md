---
title: Teekonna oleku seadistamine
description: Selles teemas kirjeldatakse, kuidas kehtestada olekuväärtusi, mida kasutajad saavad teekondadele määrata.
author: sherry-zheng
manager: tfehr
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: b7180cc9ab2d13f2260635d717adb7aab2177ab9
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500882"
---
# <a name="voyage-status-setup"></a>Teekonna oleku seadistamine

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Lehel **Teekonna olek** saate koostada komplekti olekuväärtustest, mida kasutajad saavad teekondadele määrata. Kasutajad saavad määrata teekonna olekuväärtusi teekonna kõigile tasemetele: teekond, saatmiskonteiner, foolio, ostutellimus ja kaup (osturead ja üleviimistellimuse read). Neid kasutatakse kahel otstarbel.

- Saate teavitada kasutajat teekonna, saatmiskonteineri, foolio, ostutellimuse või kauba olekust (osturead ja üleviimistellimuse read).
- Saate piirata kuluala kasutamist, tõkestades muutmise või kustutamise.

Teekonna olekute seadistamiseks avage **Väljalaadimiskulu \> Seadistamine \> Teekonna olekud**. Seal saate toimingupaani nuppude abil olekuid lisada, eemaldada ja redigeerida.

Igal kulualal on oma teekonnaolekute komplekt ja hierarhia. Seetõttu tuleb lehel **Teekonna olekud** väljal **Kuluala** esmalt valida kuluala, mida soovite vaadata või mille jaoks teekonnaolekuid luua. Seejärel määrake iga teekonna oleku jaoks vastavalt vajadusele väljad, mida kirjeldatakse järgmises tabelis. Arvestage, et teekonna olekut võivad automaatselt muuta ka süsteemisündmused, nt jälgimise juhtimiskeskuse abil kehtestatud reeglid.

| Field | Kirjeldus |
|---|---|
| Reisi olek | Sisestage teekonna oleku nimi. |
| Kirjeldus | Sisestage teekonna oleku kirjeldus. |
| Muuda | Valige see märkeruut, kui kasutajatel on lubatud selle olekuga teekondi muuta. |
| Kustutamine | Valige see märkeruut, kui kasutajatel on lubatud selle olekuga teekondi kustutada. |
| Kohustuslik | Valige see märkeruut, et muuta teekonna olek kohustuslikuks, et seda ei saaks vahele jätta. |
| Ema | Selle välja abil saate kehtestada olekuväärtuste hierarhia. Teekonna olekuid saab muuta (kas käsitsi või automaatselt) ainult hierarhias allapoole, emaolekust ühte selle tütarolekusse.

> [!NOTE]
> Seadistada tuleb ainult need konkreetsed teekonna olekud, mida teie organisatsioon kasutab. Tüüpilisteks teekonna olekuteks on *Kinnitatud*, *Transiidis olevad kaubad*, *Vastuvõetud*, *Kuluarvestuseks valmis* ja *Arvestatud kulu*. Kuid võib olla ka teisi olekuid.
