---
title: Rahavoo prognoosimise lubamine
description: Selles teemas selgitatakse, kuidas lülitada finantsülevaadetes sisse rahavoo prognoosimise funktsioon.
author: ShivamPandey-msft
ms.date: 02/11/2022
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
ms.openlocfilehash: 763818f70095964d77ff82cf02178367d05eaf23
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109575"
---
# <a name="enable-cash-flow-forecasting"></a>Rahavoo prognoosimise lubamine

[!include [banner](../includes/banner.md)]

See teema kirjeldab, kuidas lülitada finantside vihjetes sisse likviidsuse prognoosimise funktsioon.

> [!NOTE]
> Maksete prognoosimises rahavoo kasutamiseks peate häälestama kliendimaksete prognoosimise funktsiooni, nagu on kirjeldatud jaotises [Kliendimaksete prognoosimise lubamine](enable-cust-paymnt-prediction.md).
  
1. Avage tööruum **Funktsioonide haldus** ja järgige järgmisi etappe.

    1. Valige **Otsi värskendusi**.
    2. **Vahekaardil Kõik** otsige likviidsuse **eelarveid**. Kui te seda funktsiooni ei leia, otsige **(eelvaade) likviidsuse prognoose**. 
    3. Lülitage funktsioon sisse.

2. Avage jaotis **Sularaha ja panga haldus \>Rahavoo prognoosimise seadistus** ja lisage likviiduses kontod, mis peaksid olema prognoosi kaasatud. Saate seadistada ka vahekaartide Müügireskontro **ja** Ostureskontro **maksete likviidsuskonto**. Arvutage kindlasti likviidsuse prognoos ümber.

    > [!NOTE]
    > Kui likviidsuse kontosid ei ole seadistatud, ei saa rahavoogu luua.
    >
    > Likviidsuse prognoosimise kohta lisateabe saamiseks vt likviidsuse [prognoosimist](../cash-bank-management/cash-flow-forecasting.md).

3. Avage jaotis **Sularaha ja panga haldus \> Seadistus \> Finantsülevaated (eelversioon) \> Rahavoo prognoosid (eelversioon)** ja tehke järgmist.

    1. Valige vahekaardil **Rahavoo prognoosimine** suvand **Luba funktsioon**.
    2. Valige **Prognoosimise mudeli loomine**.

> [!NOTE]
> Likviidsuse **prognoosimudeli** koolitus hõlmab andmeid, mille 100 või rohkem kandeid ulatuvad üle aasta. Soovitame teil vähemalt kaks aastat andmeid omada rohkem kui 1000 kandega.

Lisainfo saamiseks rahavoo prognoosimise võimaluste kohta vt teemast [Rahavoo prognoosimine](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
