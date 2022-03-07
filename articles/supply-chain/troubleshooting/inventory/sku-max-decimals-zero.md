---
title: Varude arvestusühiku kümnendkohtade maksimumarv on 0
description: Kui proovite sisestada laokannet või varude reserveerimist, kuvatakse tõrketeade "Varude arvestusühiku kümnendkohtade maksimumarv on 0”.
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 9dec198e2d77efd2253c80e14d15791cc37f88e1
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476159"
---
# <a name="maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>Varude arvestusühiku kümnendkohtade maksimumarv on 0


## <a name="symptoms"></a>Sümptomid

Kui proovite sisestada laokannet või varude reserveerimist, kuvatakse järgmine tõrketeade:

> Varude arvestusühiku kümnendkohtade maksimumarv on 0.

See probleem ilmneb, kui laokanmete kogus on määratud kümnendväärtusena, mis on allpool täpsustaset, mida väli toetab. Näiteks on laokande jaoks määratud kogus *0,5*, kuid toetatakse ainult täisarvukoguseid. Seetõttu peab väärtus olema *0,5* asemel *1*.

## <a name="resolution"></a>Lahendus

1. Käivitage oma SQL-serveri eksemplaris järgmine skript, et ümardada laokannetes kogused. See skript parandab väärtused tabelis **inventTrans**.

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. Käivitage vaba kaubavaru järjepidevuse kontroll, kus valik **paranda tõrge** on sisselülitatud. See kontroll parandab väärtused tabelis **inventSum**.

> [!IMPORTANT]
> Soovitame tungivalt, et redigeeriksite skripti hoolikalt vastavalt oma keskkonnale, katsetaksite seda katsekeskkonnas ning seejärel kontrolliksite saadud andmeid enne skripti käivitamist tootmiskeskkonnas.
