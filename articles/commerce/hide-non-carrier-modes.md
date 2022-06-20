---
title: Mitte-vedaja tarneviiside peitmine POS-i saadetise valikutest
description: See artikkel kirjeldab konfiguratsioonivalikut, mis võib takistada mitte vedaja tarneviiside kuvamist valiku puhul, kui saadetise tellimused luuakse müügikoha rakenduses (POS).
author: hhainesms
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 469e6ebb8afed26a6bf25f4c9c3ab8f7f4ac78ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897001"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Mitte-vedaja tarneviiside peitmine POS-i tarnevalikutest


[!include [banner](includes/banner.md)]

See artikkel kirjeldab konfiguratsioonivalikut, mis on saadaval müügikoha rakendusele. See konfiguratsioonivalik muudab tarneviisi valimise käitumist, kui saadetise tellimused luuakse POS-is.

Kui kasutajad loovad kliendi saadetise tellimused POS-is, saavad nad valida saadetise tarneviisi. See funktsioon on saadaval olenemata sellest, kas kogu tellimus on saadetud või ainult valitud read.

Vaikimisi kuvatakse dialoogiboksis, kus on valitud tarneviis, kõik kehtivad tarneviisisid kanali, kauba ja tarneaadressi kombinatsiooni jaoks. Need tarneviisid on määratletud peakontori lehel **Tarneviisid** (**Müük ja turundus \> Seadistus \> Jaotus \> Tarneviisid**). Dialoogiboksis võidakse valimiseks kuvada ka "mitte-vedaja" tarneviisid, näiteks **Järeletulemine** või **Kättesaamine**.

Siiski on lisatud funktsioon, mis võimaldab teil peita mitte-vedaja tarneviisid dialoogiboksis. Selle funktsiooni sisselülitamiseks määrake vahekaardi **Klienditellimused** lehel **Kaubandusparameetrid** suvandi **Kuva tellimuste lähetamiseks ainult vedajarežiimi valikud** olekuks **Jah**. Pärast selle funktsiooni sisselülitamist ja sobivate jaotustööde käitamist teabe sünkroonimiseks kanali andmebaasiga, ei kuvata POS-is saadetise tellimuste loomisel mitte-vedaja tarneviise enam valimiseks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]