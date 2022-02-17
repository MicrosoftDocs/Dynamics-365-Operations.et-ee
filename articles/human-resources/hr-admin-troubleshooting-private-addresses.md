---
title: Juurdepääs privaatsetele aadressidele turberolli järgi
description: Selles teemas selgitatakse, kuidas lahendada probleemi, kus kliendil puudub juurdepääs privaatsetele aadressidele.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 05895d58cfd108c45c3c75921cb6930b904a6482
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068380"
---
# <a name="access-to-private-addresses-by-security-role"></a>Juurdepääs privaatsetele aadressidele turberolli järgi


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Probleem**

Pärast turberolli paljundamist ja uue rollina sisselogimist ei näe klient privaatseks märgitud aadresse.

**Eraldusvõime**

Probleemi lahendamiseks peab klient toimima topeltturberolli korral järgmiselt.

1. Minge jaotisse **Organisatsiooni haldamine \> Globaalne aadressiraamat \> Globaalse aadressiraamatu parameetrid**.
2. Teisaldage vahekaardil **Privaatse asukoha turvalisus** uus turberoll loendist **Saadaolevad rollid** loendisse **Valitud rollid**.
3. Valige käsk **Salvesta**.

![Globaalse aadressiraamatu parameetrite leht.](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
