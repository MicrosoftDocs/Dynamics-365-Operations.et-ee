---
title: Kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides
description: See artikkel kirjeldab, kuidas seadistada kliendiarvete teavet ja tagastada müügitellimusi Ida-Euroopa riikides.
author: EvgenyPopovMBS
ms.date: 10/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: josaw
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.search.industry: Retail
ms.openlocfilehash: 6ebf3740b9ae93cecd5592a5564574e7f49ab5b4
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286546"
---
# <a name="customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a>Kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides


[!include [banner](../../includes/banner.md)]

See artikkel kirjeldab, kuidas seadistada kliendiarvete teavet ja tagastada müügitellimusi Ida-Euroopa riikides.

Saate seadistada Retail POS-is loodud kliendiarvete ja tagastatavate müügitellimuste järgmist teavet.

- Saate tagastatavaid müügitellimusi kasutades kasutada tagastuste käitlemiseks käibemaksugruppe. Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**. Avage vahekaart **Sisestamine \> Arve** ja seejärel määrake suvandi **Kasutage käibemaksugruppi tagastustele** sätteks **Jah**.

    * Kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige käibemaksugrupp **Kliendi** lehel **Kaubanduse** kiirkaardil **Tagastuste käibemaksugrupi** väljal. Kliendile tagastatava müügitellimuse sisestamisel värskendatakse tagastatava müügitellimuse rida koos **Kliendi** vormil määratud tagasutste käibemaksugrupiga.
    * Retail POS-is kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige **Kaupluste** lehel **Üldisel** kiirkaardil **Tagastuste käibemaksugrupi** väljal käibemaksugrupp. Tagastatava müügitellimuse sisestamisel kaupluse kliendi jaoks värskendatakse tagastatava müügitellimuse rida **Kaupluste** lehel määratud tagastuste käibemaksugrupiga.

- Kui arvel või tagastusel pole müügi vaikekuupäeva, saate arve või tagastuse müügikuupäevana kasutada kliendiarve või tagastatava müügitellimuse sisestuskuupäeva. Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**. Avage vahekaart **Sisestamine \> Arve** ja seejärel määrake suvandi **Kasutage sisestuskuupäeva müügikuupäevana** sätteks **Jah**.
- Saate Läti ja Leedu kliendiarvete ja tagastatavate müügitellimuste nummerdamiseks kasutada maksuameti esitatud numbrivahemikku.

    * Valige **Organisatsiooni haldus \> Numbriseeriad \> Loendurite haldamine**. Olemas peab olema kirje, kus **Moodul** = **Müük** ja **Tüüp** = **Arve**.
    * Valige **Organisatsiooni haldus \> Numbriseeriad \> Arvete numeratsiooni seadistus**. Märkige **Kaubanduse** märkeruut kliendiarvete nummerdamiseks kasutatava numbriseeria real.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
