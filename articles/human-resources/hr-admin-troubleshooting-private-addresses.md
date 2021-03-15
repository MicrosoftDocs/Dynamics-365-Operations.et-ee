---
title: Juurdepääs privaatsetele aadressidele turberolli järgi
description: Selles artiklis selgitatakse, kuidas lahendada probleemi, mille käigus kliendil puudub juurdepääs privaatsetele aadressidele.
author: andreabichsel
manager: tfehr
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6598094e7877a30c35e1b03794f82c8a4ec001a7
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112197"
---
# <a name="access-to-private-addresses-by-security-role"></a>Juurdepääs privaatsetele aadressidele turberolli alusel

**Probleem**

Pärast turberolli paljundamist ja uue rollina sisselogimist ei näe klient privaatseks märgitud aadresse.

**Eraldusvõime**

Probleemi lahendamiseks peab klient toimima topeltturberolli korral järgmiselt.

1. Minge jaotisse **Organisatsiooni haldamine \> Globaalne aadressiraamat \> Globaalse aadressiraamatu parameetrid**.
2. Teisaldage vahekaardil **Privaatse asukoha turvalisus** uus turberoll loendist **Saadaolevad rollid** loendisse **Valitud rollid**.
3. Valige **Salvesta**.

![Globaalse aadressiraamatu parameetrite leht](media/GAD-parameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]