---
title: Kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides
description: See teema kirjeldab, kuidas sedistada teavet kliendiarvete ja tagastatavate müügitellimuste jaoks Ida-Euroopa riikides.
author: epopov
manager: annbe
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a00a960142b0e3955c80d75f7963f4827209bf75
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407846"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a>Kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides


[!include [banner](../../includes/banner.md)]

See teema kirjeldab, kuidas sedistada teavet kliendiarvete ja tagastatavate müügitellimuste jaoks Ida-Euroopa riikides.

Saate seadistada Retail POS-is loodud kliendiarvete ja tagastatavate müügitellimuste järgmist teavet.

- Saate tagastatavaid müügitellimusi kasutades kasutada tagastuste käitlemiseks käibemaksugruppe. Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**. Avage vahekaart **Sisestamine \> Arve** ja seejärel määrake suvandi **Kasutage käibemaksugruppi tagastustele** sätteks **Jah**.

    * Kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige käibemaksugrupp **Kliendi** lehel **Kaubanduse** kiirkaardil **Tagastuste käibemaksugrupi** väljal. Kliendile tagastatava müügitellimuse sisestamisel värskendatakse tagastatava müügitellimuse rida koos **Kliendi** vormil määratud tagasutste käibemaksugrupiga.
    * Retail POS-is kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige **Kaupluste** lehel **Üldisel** kiirkaardil **Tagastuste käibemaksugrupi** väljal käibemaksugrupp. Tagastatava müügitellimuse sisestamisel kaupluse kliendi jaoks värskendatakse tagastatava müügitellimuse rida **Kaupluste** lehel määratud tagastuste käibemaksugrupiga.

- Kui arvel või tagastusel pole müügi vaikekuupäeva, saate arve või tagastuse müügikuupäevana kasutada kliendiarve või tagastatava müügitellimuse sisestuskuupäeva. Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**. Avage vahekaart **Sisestamine \> Arve** ja seejärel määrake suvandi **Kasutage sisestuskuupäeva müügikuupäevana** sätteks **Jah**.
- Saate Läti ja Leedu kliendiarvete ja tagastatavate müügitellimuste nummerdamiseks kasutada maksuameti esitatud numbrivahemikku.

    * Valige **Organisatsiooni haldus \> Numbriseeriad \> Loendurite haldamine**. Olemas peab olema kirje, kus **Moodul** = **Müük** ja **Tüüp** = **Arve**.
    * Valige **Organisatsiooni haldus \> Numbriseeriad \> Arvete numeratsiooni seadistus**. Märkige **Kaubanduse** märkeruut kliendiarvete nummerdamiseks kasutatava numbriseeria real.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]