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
ms.openlocfilehash: cfcdbe76d640d1786b4622febf9157f5fb1c42f9
ms.sourcegitcommit: 133aa728b8a795eaeaef22544f76478da2bd1df9
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/13/2022
ms.locfileid: "7969133"
---
# <a name="enable-cash-flow-forecasting"></a>Rahavoo prognoosimise lubamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas sisse lülitada rahavoogude prognooside funktsioon finance insightsis.

> [!NOTE]
> Maksete prognoosimises rahavoo kasutamiseks peate häälestama kliendimaksete prognoosimise funktsiooni, nagu on kirjeldatud jaotises [Kliendimaksete prognoosimise lubamine](enable-cust-paymnt-prediction.md).
  
1. Avage tööruum **Funktsioonide haldus** ja järgige järgmisi etappe.

    1. Valige **Otsi värskendusi**.
    2. Otsige **vahekaardil** Kõik **väljalt Rahavoogude prognoosid**. Kui te seda funktsiooni ei leia, otsige **(eelvaade) rahavoogude prognoose**. 
    3. Lülitage funktsioon sisse.

2. Avage jaotis **Sularaha ja panga haldus \>Rahavoo prognoosimise seadistus** ja lisage likviiduses kontod, mis peaksid olema prognoosi kaasatud. Seadistage ka maksete likviidsuskonto **vahekaartidel Ostureskontro** ja **Ostureskontro.** Arvutage kindlasti rahavoogude prognoos ümber.

    > [!NOTE]
    > Kui likviidsuse kontosid ei ole seadistatud, ei saa rahavoogu luua.
    >
    > Rahavoogude prognooside seadistamise kohta leiate lisateavet teemast [Rahavoogude prognoosimine](../cash-bank-management/cash-flow-forecasting.md).

3. Avage jaotis **Sularaha ja panga haldus \> Seadistus \> Finantsülevaated (eelversioon) \> Rahavoo prognoosid (eelversioon)** ja tehke järgmist.

    1. Valige vahekaardil **Rahavoo prognoosimine** suvand **Luba funktsioon**.
    2. Valige **Prognoosimise mudeli loomine**.

Lisainfo saamiseks rahavoo prognoosimise võimaluste kohta vt teemast [Rahavoo prognoosimine](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
