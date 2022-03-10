---
title: Laadungi ridade kaaluväljad ei vasta laadungi kaaluväljadele
description: Laadungi ridade kaaluväljad ei vasta laadungi kaaluväljadele
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSShipmentDetails_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f71ac7b2777cb77fccdf1a4c72a47c9b406bbd68b2d20c41ddc96028d2ffc348
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756699"
---
# <a name="the-weight-fields-on-load-lines-dont-match-the-weight-fields-on-the-load"></a>Laadungi ridade kaaluväljad ei vasta laadungi kaaluväljadele

Tõrkekoodid: WHSLaadungKaalRidadelEiKlapiLaadungHoiatus

## <a name="symptoms"></a>Sümptomid

Süsteem näitab järgmist tõrketeadet:

> Laadungi ridade kaaluväljad ei vasta laadungi kaaluväljadele %1. Käivitage lao laadungi kaalu ühtsuse kontroll kaaluväljade uuesti arvutamiseks.

## <a name="cause"></a>Põhjus

**Netokaal** ja **Tühikaal** väljad on laadungireal seatud väärtusele *0* (null). Kaaluväljade väärtuseks ei ole aga toote kaalu mõõtmiste puhul seatud *0*. Kui laadungireal pole kaaluvälju seatud, võivad mis tahes laadungirea koguse parandused põhjustada laadungi kaalu vale arvutust. See probleem võib ilmneda, kui toote kaalu on pärast laadungirea loomist muudetud.

## <a name="resolution"></a>Eraldusvõime

Laadungirea loomisel sisestatakse vaikimisi toote kaaluväljad. Kui kaal on null, saate selle *Lao koormuse kaalu ühtsuse kontrolli* funktsiooni abil ümber arvutada.

1. Minge **Süsteemi administreerimine \> Perioodilised ülesanded \> Andmebaas \> Ühtsuskontroll**.
1. Dialoogiboksis **Ühtsuse kontroll** seadke väli **Moodul** väärtusele *Laohaldus*.
1. Seadke välja **Kontroll/parandus** väärtuseks *Paranda tõrge*.
1. Märkeruudu nimekirjas valge **Lao koormuse kaalu ühtsuse kontroll** märkeruut ja veenduge, et ainult see rida märkeruudul on esile tõstetud.
1. Valige märkeruuduloendi ülaosas kolmikpunkti nupp (**...**) ja seejärel valige menüüst **Dialoog**.
1. Määrake dialoogiboksis **Lao koormuse kaalu ühtsuse kontroll** järgmised väljad, et määratleda kriteeriumid, mille puhul tuleks ühtsuskontrolli käitada:

    - **Laadungi ID:** Määrake laadungi ID. Jätke see tühjaks, et kontrollida kõiki laadungi ID-sid.
    - **Kaubakood:** Määrake kaubakood. Jätke see tühjaks, et kontrollida kõiki kaupu.
    - **Koormate kaalu ümberarvutamine alati** Määrake selle suvandi väärtuseks *Jah*.
    - **Luba koormaridade kaalu ülekirjutamine:** Määrake selle suvandi väärtuseks *Jah*.

1. Valige **OK**, et sulgeda **Lao koorma kaalu ühtsuse kontroll** dialoogiaken.
1. Valige kolmikpunkt nupp ja seejärel valige menüüst **Teosta**.

Kaal arvutatakse ümber teie määratud kriteeriumide alusel. Valige **Sõnumi üksikasjade** link, et vaadata ühtsuskontrolli tulemust.
