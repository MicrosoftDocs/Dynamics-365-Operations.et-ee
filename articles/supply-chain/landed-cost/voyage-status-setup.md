---
title: Teekonna oleku seadistamine
description: See artikkel kirjeldab, kuidas luua olekuväärtusi, mida kasutajad saavad reisidele määrata.
author: Weijiesa
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMStatusTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 1cec728f2fa49175c063818ee7f188b441945647
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8907315"
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
