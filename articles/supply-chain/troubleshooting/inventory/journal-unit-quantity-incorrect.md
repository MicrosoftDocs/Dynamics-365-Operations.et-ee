---
title: Ühik ja ühiku kogus ei tööta varude töölehel õigesti
description: Ühik ja ühiku kogus ei tööta varude töölehel õigesti
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
ms.openlocfilehash: 39f462ae325aa1104a25a8290daed70388e624ec
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476101"
---
# <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>Ühik ja ühiku kogus ei tööta varude töölehel õigesti

## <a name="symptoms"></a>Sümptomid

Varude töölehel üksuste ja kogustega töötades võite puutuda kokku ühe või mõlema probleemiga.

- Te ei näe varude töölehel ühikuid ega ühiku koguseid, kui väljastatud tootele on seadistatud teisendusühik, ja te ei saa ühikut varude töölehel muuta.
- Näete varude töölehel väljasid **Kogus** ja **Ühik**, kuid te ei näe välja **Ühiku kogus**. Kui muudate ühikut, sisestate koguse ja sisestate töölehe, kuvatakse töölehel siiski selle koguse algne mõõtühik.

## <a name="resolution"></a>Lahendus

Selle probleemi lahendamiseks tehke järgmist.

1. Kontrollige **funktsioonihalduse** tööruumis, et funktsioon *Mõõtühiku ja ühiku koguse kasutamine varude töölehtedel* oleks sisse lülitatud. See funktsioon lisab töölehele väljad **Ühik** ja **Ühiku kogus**.
1. Kui funktsioon on sisse lülitatud, kasutage välju **Kogus**, **Ühiku kogus** ja **Ühik** järgmisel viisil.

    - **Kogus** – määrake kogus, kasutades vaikeühikut, mis on vabastatud toote jaoks määratletud. Samas vaikeühikut ennast siin ei kuvata. Kui vaikeühiku ja väljal **Ühik** valitud ühiku vahel on häälestatud teisendus, uuendatakse välja **Kogus** väljade **Ühiku kogus** ja **Ühik** valikute alusel automaatselt.
    - **Ühiku kogus** – määrake kogus, kasutades ühikut, mis on valitud väljal **Ühik**.
    - **Ühik** – valige ühik, mida rakendada väljal **Ühiku kogus** määratud väärtusele.
