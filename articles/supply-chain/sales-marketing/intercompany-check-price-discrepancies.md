---
title: Kontrolli kontsernisisese tellimuse hinnaerinevusi
description: See artikkel selgitab, kuidas kontrollida kontsernisisese tellimuse hinnaerinevusi
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: PurchTable, PurchTablePart, PurchLineOpenOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: ca27e86545ba8179c595e55487dbbf49cd9ec528
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890679"
---
# <a name="check-intercompany-order-price-discrepancies"></a>Kontrolli kontsernisisese tellimuse hinnaerinevusi

[!include [banner](../../includes/banner.md)]

Selle toimingu abil saate kontrollida kontsernisiseste tellimuste hinnaerinevusi.

1. Minge **Soetamine ja hankimine \> Perioodiline \> Puhastus \> Kontrollige kontsernisiseste tellimuste hindade erinevusi**.
1. Seadistage vajadusel partii töö, ja seejärel valige **OK**, et kontrollida kontsernisiseste müügitellimuste ja ostutellimuste hindu ja allahindlusi. Vastasel juhul valige lehe sulgemiseks kontrolli sooritamata nuppu **Tühista**.

    > [!TIP]
    > Kui esineb sünkroonimisprobleeme või probleeme hindadega, loetletakse need kuvatavas teavitusteates. Saate teavitusteate kasutamiseks printida.

1. Teavitusteates valige sobiv rida tellimuse avamiseks praeguses juriidilises isikus. Avage tellimus seotud juriidilises isikus, valides **Kontsernisisene** ja seejärel **Kontsernisisene ostutellimus** või **Kontsernisisene müügitellimus**.

    > [!NOTE]
    > Kontsernisisese tellimuse uuendamise lubamiseks:
    >
    > 1. Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.
    > 1. Tegevuspaanil valige vahekaart **Üldine** ja seejärel valige **Kontsernisisene**.
    > 1. Valige **Kontserni** leheküljel **Ostutellimuste poliitikad** või **Müügitellimuste poliitikad**.
    > 1. Valige **Luba hinna redigeerimine** ja **Luba allahindluse redigeerimine** mõlemas alas.

1. Avage vastav kontsernisisene tellimus, kus soovite hinda säilitada.
1. Muutke kõigi tellimuseridade puhul rea välja **Ühiku hind** ja seejärel muutke need tagasi algsetele väärtustele. Muutke rea välja **Allahindlus** edasi-tagasi ja muutke ka vastavalt väljade **Ostutasud** ja **Müügitasud** väärtusi. Selline vahelduv väärtuste muutmine käivitab hindade, allahindluste ja kulude sünkroonimise kontsernisisese tellimuse rea ja viidatud kontsernisisese tellimuse rea vahel ning need joondatakse automaatselt.

    > [!NOTE]
    > See sünkroonimine kehtib ainult arveldamata kontsernisisese müügitellimuse puhul. Kui kontsernisisene müügitellimus on arveldatud ja sisestatud ning kliendiarve tööleht on loodud, peab muudatused tegema otse kontsernisisese ostutellimuse ridadel, seadistades hinnad, allahindlused ja tasud võrdseks kontsernisisese kliendiarve töölehel olevatega. Seda tegemata pole kontsernisisest ostutellimust võimalik tellimuse kogusummade mittevastavuse tõttu arvega sisestada.

1. Korrake toimingut, kuni kõik kontsernisisesed ostu- ja müügitellimused on sünkroonitud.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
