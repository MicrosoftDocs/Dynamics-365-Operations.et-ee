---
title: Retaili kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides
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
ms.openlocfilehash: 20ae19fb03acb075b6553b95808779c905bcd31b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "370534"
---
# <a name="retail-customer-invoices-and-return-sales-orders-in-eastern-european-countries"></a>Retaili kliendiarved ja tagastuse müügitellimused Ida-Euroopa riikides


[!include [banner](../../includes/banner.md)]

See teema kirjeldab, kuidas sedistada teavet kliendiarvete ja tagastatavate müügitellimuste jaoks Ida-Euroopa riikides.

Saate seadistada Retail POS-is loodud kliendiarvete ja tagastatavate müügitellimuste järgmist teavet.

- Saate tagastatavaid müügitellimusi kasutades kasutada tagastuste käitlemiseks käibemaksugruppe. Avage **Jaemüük > Haldamise seadistamine > Parameetrid > Jaemüügi parameetrid**. Avage **Sisestamine > Arve** vahekaart ning seejärel määrake **Käibemaksugruppide kasutamine tagastusteks** olekuks **Jah**. 

  * Kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige käibemaksugrupp **Kliendi** lehel **Jaemüügi** kiirkaardil **Tagastuste käibemaksugrupi** väljal. Kliendile tagastatava müügitellimuse sisestamisel värskendatakse tagastatava müügitellimuse rida koos **Kliendi** vormil määratud tagasutste käibemaksugrupiga.
  
  * Retail POS-is kliendi tehtud tagastuste jaoks käibemaksugrupi määramiseks valige **Kaupluste** lehel **Üldisel** kiirkaardil **Tagastuste käibemaksugrupi** väljal käibemaksugrupp. Tagastatava müügitellimuse sisestamisel kaupluse kliendi jaoks värskendatakse tagastatava müügitellimuse rida **Kaupluste** lehel määratud tagastuste käibemaksugrupiga.

- Kui arvel või tagastusel pole müügi vaikekuupäeva, saate arve või tagastuse müügikuupäevana kasutada jaemüügi kliendiarve või tagastatava müügiarve sisestuskuupäeva. Avage **Jaemüük > Haldamise seadistamine > Parameetrid > Jaemüügi parameetrid**. Avage **Sisestamine > Arve** vahekaart ning seejärel määrake **Sisestuskuupäeva kasutamine müügikuupäevana** olekuks **Jah**.

- Saate Läti ja Leedu kliendiarvete ja tagastatavate müügitellimuste nummerdamiseks kasutada maksuameti esitatud numbrivahemikku. 

  * Avage **Organisatsiooni haldus > Numbriseeriad > Loendurite haldamine**. Olemas peab olema kirje, kus **Moodul** = **Müük** ja **Tüüp** = **Arve**.

  * Avage **Organisatsiooni haldus > Numbriseeriad > Arvete numeratsiooni seadistamine**. Märkige **Jaemüügi** märkeruut kliendiarvete nummerdamseks kasutatava numbriseeria real.
