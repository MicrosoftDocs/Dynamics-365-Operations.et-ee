---
title: Teekonna oleku seadistamine
description: Selles teemas kirjeldatakse, kuidas kehtestada olekuväärtusi, mida kasutajad saavad teekondadele määrata.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e19a54fc9de166c93fd68408ca8c8c692dc96cab
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022104"
---
# <a name="voyage-status-setup"></a>Teekonna oleku seadistamine

[!include [banner](../../includes/banner.md)]

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
