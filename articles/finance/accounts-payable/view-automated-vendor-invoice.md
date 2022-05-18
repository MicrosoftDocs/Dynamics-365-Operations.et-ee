---
title: Hankija arve automatiseerimise tulemuste kuvamine (eelversioon)
description: Selles teemas selgitatakse, kuidas vaadata hankija arvete olekut, mis on kaasatud töövoole edastamise automatiseeritud protsessi.
author: abruer
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1700f4c4748dc12bf000b25c0d51bc6ed069a97b
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717245"
---
# <a name="view-vendor-invoice-automation-results"></a>Hankija arve automatiseerimise tulemuste kuvamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas vaadata hankija arvete olekut, mis on kaasatud töövoole edastamise automatiseeritud protsessi. Automatiseerimisajaloo üksikasjad säilitatakse iga imporditud hankija arve kohta. Sõltuvalt teie automatiseeritud äriprotsessidest kuvatakse lehel **Ootel hankija arved** väärtused **Automatiseeritud sissetuleku vastavusseviimise olek** ja **Automatiseeritud töövoole edastamise olek**. Saate vaadata üksikasju ja teha plaani, et keskenduda arvetele, mis automatiseerimise käigus nurjusid. Seejärel saate pärast probleemi parandamist jätkata imporditud arve automatiseeritud protsessi.

Enne edastatud arve redigeerimist peate automatiseeritud töötluse peatama. Kui automaatses töövoole edastamise protsessis tuleb arve peatada, seadke välja **Kaasa automatiseeritud töötlusse** väärtuseks **Ei** lehel **Hankija arved**. Automatiseerimine ei käivitu enne, kui suvandi **Kaasa automatiseeritud töötlusse** väärtuseks seatakse **Jah**. Arve saab jääta välja täiendavast automatiseerimisest, kui see ei ole veel töövoosüsteemis ja seda ei kasutata automatiseeritud protsessis.

Kui imporditud arve puhul rakendatakse töövoole edastamise protsessi, saate vaadata selle suvandi **Automatiseerimise olek** väärtust lehel **Hankija arved**. Jälgitakse järgmisi olekuid.

- **Kaasatud** – automatiseeritud protsessid, mis on määratud lehel **Ostureskontro parameetrid**, töötavad õigesti, kuid pole veel lõpetatud.
- **Peatatud** – automatiseeritud protsessid, mis on määratud lehel **Ostureskontro parameetrid**, on käivitatud, kuid vähemalt üks etapp protsessis nurjus. Olekut **Peatatud** rakendatakse ka juhul, kui välja **Kaasa automatiseeritud töötlemisse** väärtuseks on seatud **Ei**. Nurjumisi saate kuvada, kui valite **Kuva kõige viimased tulemused**.
- **Töövoos** – imporditud arve on edastatud töövoosüsteemi kas automatiseeritud töövoole edastamise protsessi kaudu või käsitsi.
- **Töövoog lõpetatud** – töövooprotsess on imporditud arve jaoks lõpetatud.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
