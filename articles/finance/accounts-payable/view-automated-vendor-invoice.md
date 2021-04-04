---
title: Hankija arve automatiseerimise tulemuste kuvamine (eelversioon)
description: Selles teemas selgitatakse, kuidas vaadata hankija arvete olekut, mis on kaasatud töövoole edastamise automatiseeritud protsessi.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 3b87af4c64f8021a1b23cca5d8f38ac21c8efbd4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248084"
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