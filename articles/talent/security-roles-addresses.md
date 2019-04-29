---
title: Juurdepääs privaatsetele aadressidele turberolli alusel
description: Selles teemas selgitatakse, kuidas lahendada probleemi, mille käigus kliendil puudub juurdepääs privaatsetele aadressidele.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: f8aaa33e5fda404b48548f9a57977dd0ccd53dc1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "859478"
---
# <a name="access-to-private-addresses-by-security-role"></a>Juurdepääs privaatsetele aadressidele turberolli alusel

[!include [banner](includes/banner.md)]

**Probleem**

Pärast turberolli paljundamist ja uue rollina sisselogimist ei näe klient privaatseks märgitud aadresse.

**Eraldusvõime**

Probleemi lahendamiseks peab klient toimima topeltturberolli korral järgmiselt.

1. Minge jaotisse **Organisatsiooni haldamine \> Globaalne aadressiraamat \> Globaalse aadressiraamatu parameetrid**.
2. Teisaldage vahekaardil **Privaatse asukoha turvalisus** uus turberoll loendist **Saadaolevad rollid** loendisse **Valitud rollid**.
3. Valige **Salvesta**.

![Globaalse aadressiraamatu parameetrite leht](media/GAD-parameters.png)
