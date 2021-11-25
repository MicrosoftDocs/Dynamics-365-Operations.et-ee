---
title: Rahavoo prognoosimise lubamine
description: Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse rahavoo prognoosimise funktsioon.
author: ShivamPandey-msft
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: d968f28126cf205a487d84301aa28f1251713386
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752684"
---
# <a name="enable-cash-flow-forecasting"></a>Rahavoo prognoosimise lubamine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

See teema kirjeldab, kuidas lülitada finantside vihjetes sisse likviidsuse prognoosimise funktsioon.

> [!NOTE]
> Maksete prognoosimises rahavoo kasutamiseks peate häälestama kliendimaksete prognoosimise funktsiooni, nagu on kirjeldatud jaotises [Kliendimaksete prognoosimise lubamine](enable-cust-paymnt-prediction.md).
  
1. Avage tööruum **Funktsioonide haldus** ja järgige järgmisi etappe.

    1. Valige **Otsi värskendusi**.
    2. Vahekaardil **Kõik** otsige **likviidsuse eelarveid**. Kui te seda funktsiooni ei leia, otsige **(eelvaade) likviidsuse prognoose**. 
    3. Lülitage funktsioon sisse.

2. Avage jaotis **Sularaha ja panga haldus \> Rahavoo prognoosimise seadistus** ja lisage likviiduses kontod, mis peaksid olema prognoosi kaasatud. Saate seadistada ka vahekaartide Müügireskontro **ja** Ostureskontro **maksete** likviidsuskonto. Arvutage kindlasti likviidsuse prognoos ümber.

    > [!NOTE]
    > Kui likviidsuse kontosid ei ole seadistatud, ei saa rahavoogu luua.
    >
    > Lisateavet likviidsuse eelarvete seadistamise kohta vt [likviidsuse](../cash-bank-management/cash-flow-forecasting.md) prognoosimine.

3. Avage jaotis **Sularaha ja panga haldus \> Seadistus \> Finantsülevaated (eelversioon) \> Rahavoo prognoosid (eelversioon)** ja tehke järgmist.

    1. Valige vahekaardil **Rahavoo prognoosimine** suvand **Luba funktsioon**.
    2. Valige **Prognoosimise mudeli loomine**.

Lisainfo saamiseks rahavoo prognoosimise võimaluste kohta vt teemast [Rahavoo prognoosimine](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
