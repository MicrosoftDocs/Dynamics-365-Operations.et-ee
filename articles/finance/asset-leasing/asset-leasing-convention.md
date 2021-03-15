---
title: Vara rentimise reeglid
description: Selles teemas kirjeldatakse renditavate varade reegleid.
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ea89d54f1ce3a1e971d41623bf44f909f7dfdf09
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131279"
---
# <a name="asset-leasing-conventions"></a>Vara rentimise reeglid

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse renditavate varade reegleid. Rentimisreegleid kasutatakse rendiraamatu alguskuupäeva määramiseks. Kui rentimisreegeli väärtuseks on määratud **Puudub**, on alguskuupäev sama, mis rendi alguskuupäev (st välja **Rendi alguskuupäev** väärtus). Kui rentimisreegliks on määratud **Terve kuu**, on alguskuupäev selle kuu esimene päev, millesse langeb rendi alguskuupäev.

Alguskuupäev määrab kohustise amortiseerimise ja vara kulumi graafikute perioodi alguskuupäeva. Intressikulud ja amortisatsioonikulud sisestatakse vastavate graafikute perioodi lõppkuupäeval. Esialgne tuvastuse ja korrigeerimise töölehekirje sisestatakse alguskuupäeval.

> [!NOTE]
> Rentimisreeglite funktsioon peab olema funktsioonihalduse kaudu sisse lülitatud. Otsige tööruumis **Funktsioonihaldus** üles funktsioon nimega **Vara rentimise rentimisreegel** ja seejärel tehke valik **Luba kohe**.

Rentimisreeglid määratakse rendivara raamatu häälestuseks.

Rentimisreegli kuvamiseks või määramiseks tehke järgmised toimingud.

1. Avage **Vara rentimine \> Seadistus \> Rendiraamatud**.
2. Valige väljal **Rentimisreegel** üks järgmistest väärtustest.

    | Rentimise reegel | Kirjeldus |
    |--------------------|-------------|
    | None               | Kohustise amortiseerimise ja vara kulumi graafikud algavad rendi alguskuupäeval, kuna alguskuupäev on võrdne rendi alguskuupäevaga. Lõppkuupäev on üks kuu hiljem. See rentimisreegel ei taga, et intress sisestatakse iga kuu viimasel päeval. |
    | Terve kuu         | Rentide puhul, mille alguskuupäev langeb kuu mis tahes päevale, hakkavad kohustise amortiseerimise ja vara kulumi graafikud kulusid koondama selle kuu esimesel päeval. See rentimisreegel tagab, et kogu kuu intress kogutakse iga kuu viimasel päeval. |

3. Valige käsk **Salvesta**.

Rendi loomisel sisestatakse iga raamatu alguskuupäev automaatselt, lähtudes sisestatud rendi alguskuupäevast ja raamatu jaoks määratud rentimisreeglist.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]