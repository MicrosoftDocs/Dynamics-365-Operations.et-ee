---
title: Mitte-vedaja tarneviiside peitmine POS-i saadetise valikutest
description: Selles teemas kirjeldatakse konfiguratsioonivalikut, mis võib takistada mitte-vedaja tarneviisi kuvamist valikutele, kui saadetise tellimused luuakse kassa rakenduses (POS).
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 09ea83b3336b208f8af0a91025c2e6c50d64c385
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/24/2019
ms.locfileid: "2659017"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Mitte-vedaja tarneviiside peitmine POS-i tarnevalikutest

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse konfiguratsioonivalikut, mis on saadaval kassarakenduse (POS) jaoks. See konfiguratsioonivalik muudab tarneviisi valimise käitumist, kui saadetise tellimused luuakse POS-is.

Kui kasutajad loovad kliendi saadetise tellimused POS-is, saavad nad valida saadetise tarneviisi. See funktsioon on saadaval olenemata sellest, kas kogu tellimus on saadetud või ainult valitud read.

Vaikimisi kuvatakse dialoogiboksis, kus on valitud tarneviis, kõik kehtivad tarneviisisid kanali, kauba ja tarneaadressi kombinatsiooni jaoks. Need tarneviisid on määratletud lehel **Tarneviisid** asukohas Retail Headquarters (**Müük ja turundus \> Seadistus \> Jaotus \> Tarneviisid**). Dialoogiboksis võidakse valimiseks kuvada ka "mitte-vedaja" tarneviisid, näiteks **Järeletulemine** või **Kättesaamine**.

Siiski on lisatud funktsioon, mis võimaldab teil peita mitte-vedaja tarneviisid dialoogiboksis. Selle funktsiooni sisselülitamiseks määrake vahekaardi **Klienditellimused** lehel **Jaemüügi parameetris** suvandi **Kuva tellimuste lähetamiseks ainult vedajarežiimi valikud** olekuks **Jah**. Pärast selle funktsiooni sisselülitamist ja sobivate jaotustööde käitamist teabe sünkroonimiseks kanali andmebaasiga, ei kuvata POS-is saadetise tellimuste loomisel mitte-vedaja tarneviise enam valimiseks.
