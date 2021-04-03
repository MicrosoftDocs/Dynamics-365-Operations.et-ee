---
title: Pearaamatu vaikekirjeldused
description: Vaikekirjeldusi saate kasutada kande sisestuste välja Kirjeldus uuendamiseks pearaamatusse.
author: sherry-zheng
manager: tfehr
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 47c5c9e71dba7a0cb7c798c167208faebeb5af6c
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500376"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Pearaamatu vaikekirjeldused

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Vaikekirjeldusi saate kasutada kande sisestuste välja **Kirjeldus** uuendamiseks pearaamatusse. Seda funktsiooni on täiustatud väljalaadimiskuluga töötamiseks.

Pearaamatu sisestuste vaikekirjelduste häälestamiseks valige **Organisatsiooni haldus \> Häälestamine \> Vaikekirjeldused**.

Järgmises tabelis loetletakse uued väärtused, mis on lisatud lehe **Vaikekirjeldused** väljale **Kirjeldus**, et toetada väljalaadimiskulu.

| Kirjelduse tüüp | Märkmed |
|---|---|
| Impordi kuluarvutus – kulu juurdekasv | Ostutellimuse arve sisestamisel töödeldakse kulude juurdekavu teekonna hinnanguliste kulude osas. Saate määrata vaikekirjeldused, et lisada kirjeldusele teekonna numbri. Kasutage *%4* saadetise numbri jaoks. |
| Impordi kuluarvutus – kaubad transiittellimuses | Kui kasutate transiidi töötlust, sisestatakse ostutellimuse arve ja kaubad sisestatakse transiidikonto kaupadele. Saate määrata vaikekirjeldused, et lisada kirjeldusele transiittellimuse numbri. Kasutage *%4* transiittellimuse numbri jaoks. |
| Ladu - sulgemine - korrigeerimine | Kui ostureskontro (AP) arvet töödeldakse teekonna kulu jaoks, töödeldakse varude korrigeerimist teekonna kulude prognoosimiseks. Saate määrata vaikekirjeldused, et lisada kirjeldusele teekonna numbri. Kasutage *%4* saadetise numbri jaoks. |

Lisateavet lehe **Vaikekirjeldused** kasutamise kohta vt teemat [Automaatse sisestamise vaikekirjelduste häälestamine](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
