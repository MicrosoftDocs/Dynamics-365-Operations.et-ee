---
title: Juurdepääs privaatsetele aadressidele turberolli järgi
description: See artikkel selgitab, kuidas lahendada, millal kliendil ei ole juurdepääsu privaatsetele aadressidele.
author: twheeloc
ms.date: 09/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7c1db052937b03817f22b37c50b9f1b319579cb2
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/20/2022
ms.locfileid: "9702099"
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
