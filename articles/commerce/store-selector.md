---
title: Kaupluse valija moodul
description: See teema hõlmab kaupluse valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378204"
---
# <a name="store-selector-module"></a>Kaupluse valija moodul

[!include [banner](includes/banner.md)]

See teema hõlmab kaupluse valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Kaupluse valija moodulit kasutatakse kliendistsenaariumi „osta veebis, käi poes järel” (BOPIS) korral. Seal kuvatakse kaupluste loend, kus toode on järele minemiseks saadaval ja ka iga kaupluse lahtiolekuajad ning toote varud.

Kaupluse valija moodul nõuab kaupluste otsimiseks toote konteksti ja otsingu asukohta. Otsingu asukoha puudumise korral on see vaikimisi kliendi brauseri asukoht, kui klient on selleks nõusoleku andnud. Moodulil on sisendkast, mis võimaldab kliendil sisestada läheduses asuvate kaupluste leidmiseks asukohta (sihtnumber, linn ja osariik).

Kaupluse valija moodul on integreeritud Bingi kaartide geokodeerimise rakenduse programmeerimisliidesega (API) asukoha laius- ja pikkuskraadideks teisendamiseks. Vajalik on Bingi kaartide API võti ja see tuleb lisada Commerce'i jagatud parameetrite lehele rakenduses Dynamics 365 Commerce.

Kaupluse valija moodulit saab lisada toote üksikasjade lehe (PDP) ostukasti moodulisse, et kuvada kauplusi, kus toode on järele tulemiseks saadaval. Seda saab lisada ka ostukorvi moodulisse. Ostukorvi moodulisse lisamisel kuvab kaupluse valija moodul iga ostukorvi rea kauba kohta järele minemise valikud. Lisaks saab seda moodulit kohandatud kodeerimise abil lisada teistele lehtedele või moodulitele laienduste ja kohanduste kaudu.

Selleks, et BOPIS-stsenaarium töötaks, tuleb toodete tarneviisiks konfigureerida „kliendi järele minemine”. Vastasel juhul ei kuvata moodulit vastavatel lehtedel. Lisateavet tarneviisi konfigureerimise kohta vaadake teemast [Tarneviiside häälestamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).

Järgmisel pildil on näide, kuidas kasutatakse kaupluse valija moodulit PDP-s.

![Kaupluse valija mooduli näide](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a>Kaupluse valija mooduli kasutamine e-kaubanduses

- Kaupluse valija moodulit saab kasutada toote üksikasjade lehel (PDP), et leida lähedal asuvaid kauplusi, kus toode on järele tulemiseks saadaval.
- Kaupluse valija moodulit saab kasutada ostukorvi lehel, et leida lähedal asuvaid kauplusi, kus ostukorvis olev toode on järele tulemiseks saadaval.

## <a name="store-selector-module-properties"></a>Kaupluse valija mooduli atribuudid

| Atribuudi nimi             | Väärtus                 | Kirjeldus |
|---------------------------|-----------------------|-------------|
| Otsinguraadius | Number | Määratleb kaupluste otsinguraadiuse miilides. Kui väärtust pole määratud, kasutatakse vaikimisi 50-miilist otsinguraadiust.|
|Teenusetingimused | URL    |  Bing kaartide teenuse korral on teenuse tingimuste URL nõutav. |

## <a name="add-a-store-selector-module-to-a-page"></a>Kaupluse valija mooduli lehele lisamine

Kaupluse valija moodul vajab toote konteksti, seega seda saab kasutada ainult ostukasti ja ostukorvi moodulites. Kaupluse valija moodulid ei tööta nendest moodulitest väljaspool.

- Lisateavet selle kohta, kuidas lisada kaupluse valija moodulit ostukasti moodulisse, vaadake teemast [Ostukasti moodul](add-buy-box.md). 
- Lisateavet selle kohta, kuidas lisada kaupluse valija moodulit ostukorvii moodulisse, vaadake teemast [Ostukorvi moodul](add-cart-module.md)

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvimoodul](add-cart-module.md)

[PDP lühiülevaade](quick-tour-pdp.md)

[Ostukorvi ja väljaregistreerimise lühiülevaade](quick-tour-cart-checkout.md)

[Tarneviiside häälestamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[Teie organisatsiooni Bingi kaartide haldamine](dev-itpro/manage-bing-maps.md)
