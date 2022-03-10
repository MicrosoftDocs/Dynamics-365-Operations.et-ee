---
title: Mitte-vedaja tarneviiside peitmine POS-i saadetise valikutest
description: Selles teemas kirjeldatakse konfiguratsioonivalikut, mis võib takistada mitte-vedaja tarneviisi kuvamist valikutele, kui saadetise tellimused luuakse kassa rakenduses (POS).
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
ms.openlocfilehash: 4d885aa7ab3b4daaebb1fa8378562d86cc153270ea166b495bf3381fae826773
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773876"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Mitte-vedaja tarneviiside peitmine POS-i tarnevalikutest


[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse konfiguratsioonivalikut, mis on saadaval kassarakenduse (POS) jaoks. See konfiguratsioonivalik muudab tarneviisi valimise käitumist, kui saadetise tellimused luuakse POS-is.

Kui kasutajad loovad kliendi saadetise tellimused POS-is, saavad nad valida saadetise tarneviisi. See funktsioon on saadaval olenemata sellest, kas kogu tellimus on saadetud või ainult valitud read.

Vaikimisi kuvatakse dialoogiboksis, kus on valitud tarneviis, kõik kehtivad tarneviisisid kanali, kauba ja tarneaadressi kombinatsiooni jaoks. Need tarneviisid on määratletud peakontori lehel **Tarneviisid** (**Müük ja turundus \> Seadistus \> Jaotus \> Tarneviisid**). Dialoogiboksis võidakse valimiseks kuvada ka "mitte-vedaja" tarneviisid, näiteks **Järeletulemine** või **Kättesaamine**.

Siiski on lisatud funktsioon, mis võimaldab teil peita mitte-vedaja tarneviisid dialoogiboksis. Selle funktsiooni sisselülitamiseks määrake vahekaardi **Klienditellimused** lehel **Kaubandusparameetrid** suvandi **Kuva tellimuste lähetamiseks ainult vedajarežiimi valikud** olekuks **Jah**. Pärast selle funktsiooni sisselülitamist ja sobivate jaotustööde käitamist teabe sünkroonimiseks kanali andmebaasiga, ei kuvata POS-is saadetise tellimuste loomisel mitte-vedaja tarneviise enam valimiseks.


[!INCLUDE[footer-include](../includes/footer-banner.md)]