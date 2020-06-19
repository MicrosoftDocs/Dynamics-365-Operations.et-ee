---
title: Juurdepääs privaatsetele aadressidele turberolli järgi
description: Selles artiklis selgitatakse, kuidas lahendada probleemi, mille käigus kliendil puudub juurdepääs privaatsetele aadressidele.
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: fbe0e8acc1b879e4d7982b33413236432f25f630
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431034"
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
