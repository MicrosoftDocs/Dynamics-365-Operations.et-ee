---
title: Tellimuse otsingu lubamine külaliste väljaregistreerimiseks
description: See teema kirjeldab, kuidas lubada tellimuste otsingut Microsoft Dynamics 365 Commerce sisseregistreerimiseks.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 639ee670b83198423425d03dad308306c9eed25c
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674972"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Tellimuse otsingu lubamine külaliste väljaregistreerimiseks

[!include [banner](includes/banner.md)]

See teema kirjeldab, kuidas lubada tellimuste otsingut Microsoft Dynamics 365 Commerce sisseregistreerimiseks.

Külalise väljaregistreerimise funktsiooni tellimise otsing võimaldab klientidel, kes sooritavad oste kui külaliskasutajad, otsida oma tellimusi. Tellimuse otsingu võimalus on kasulik, kui kliendid soovivad teostada tegevusi, nt kontrollida toodete täitmise olekut tellimusel, kinnitada aadressi, kuhu tellimus saadeti, toote ümberjärjekorras tellimist või kaupluse kinnitust, et tellimus peale võetaks.

Kliendid, kes registreerivad tellimusi registreeritud kasutajatena saavad näha oma tellimuse üksikasju, kui nad on sisse logitud, kuid kliendid, kes kasutavad külalise väljaregistreerimist, et tellimusi teha, ei saa seda teha. Kuid kui külalise väljaregistreerimise otsingu funktsioon on lubatud, annab see vormi, mida kliendid saavad kasutada külalisena esitatud tellimuste otsimiseks. Selles vormis sisestavad kliendid tellimuse kinnituse ID ja (valikuliselt) meiliaadressi, mille nad väljaregistreerimises määrasid.

Lisaks saab link või nupp, mis viib kliendi otse tellimuse üksikasjade leheküljele, nende tellimuse kohta, kaasata mis tahes tellimusega seotud kande e-kirjad. See link või nupp töötab tellimuste puhul, mille on paigutanud registreeritud kasutajad ja külaliskasutajad.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Commerce Headquarters`i vajalike funktsioonide sisse lülitamine

Tellimuse otsingu lubamiseks külalisregistreerimistes peate Commerce headquartersis lülitama sisse järgmised funktsioonid **Tööruumid \> Funktsioonihaldus**.

| Funktsioon | Eesmärk |
|---------|---------|
| Retaili anonüümse kasutaja otsingutellimuse üksikasjade valimise funktsioon | See funktsioon võimaldab teil lubada tellimuse otsingu API autentimata kasutajatele ja konfigureerida, kuidas isikuandmeid kuvatakse. |
| Luba tugevama kanali viite ID genereerimine | See funktsioon loob turvalisema 12-märgise kanaliviite ID (tellimuse kinnituse ID), mille saab tellimuse otsimisel päringustringis sisestada. |
| Looge kanalite üleselt ühtne kanali viite ID vorming | See funktsioon loob turvalise kanaliviite ID tellimustele, mis pannakse läbi e-äri saidi, müügikoha (POS) või kõnekeskuse. Enne selle funktsiooni sisselülitamist peab olema sisse lülitatud funktsioon **Luba kanali viite ID loomine**. |

Kui olete lülitanud sisse **Jaemüügi anonüümse kasutaja otsingutellimuse üksikasjade valiku** funktsiooni, peate lubama API, mis toetab autentimata tellimuse otsingut Commerce Headquarters`is. Valige suvandid **Jaemüük ja äri \> Peakontori seadistamine \> Parameetrid \> Klienditellimused**. Seadke **kliendi tellimuste** lehel **Tellimuse otsing** kiirkaardil **Luba autentimata tellimuse otsing** valik väärtusele **Jah** nagu on näha järgmises illustratsioonis.

## <a name="manage-the-display-of-personal-data"></a>Isikuandmete kuvamis haldamine

**Tellimuse otsing** kiirkaardil **Kliendi tellimused** lehel Commerce Headquarters`is sisaldab **isikuandmete kaasamist külalise tellimuse otsingu** väljale, mis võimaldab kontrollida, kas kliendile kuvatakse teavet. See isiklik teave hõlmab kliendi tarneaadressi ja kliendi krediitkaardinumbri nelja viimast numbrit. Vaikimisi ei kuvata klientidele isiklikku teavet, kui autentimata tellimuse otsing on lubatud. Järgmises tabelis kirjeldatakse saadaval valikuid.

| Suvand | Tulemus |
|--------|--------|
| Mitte kunagi | Vaikeväärtus. Tellimuse otsingutes isikuandmeid ei kuvata. Kui registreeritud kasutajad, kes on sisse logitud, saavad nad näha oma isiklikke andmeid. |
| Ainult külalistellimused | Isiklikke andmeid näidatakse tellimuseotsingutes tellimuste puhul, mis kliendid on loonud külalisena. Kui tellimuse lõi registreeritud kasutaja, peab see kasutaja sisse logima, et näha oma isiklikke andmeid. |
| Kõik tellimused | Tellimuse otsingutes isikuandmeid ei kuvata. |

> [!NOTE]
> Need valikud määravad, millal anonüümsetele kasutajatele kuvatakse sellised isiklikud andmed nagu kliendi aadress ja kliendi krediitkaardinumbri neli viimast numbrit. Registreeritud klientide privaatsuse kaitsmiseks on soovitatav valida **Ainult külalistellimuste** suvand. Kõige turvalisem valik on aga **Mitte kunagi**.

Pärast väärtuse muutmist **isiklike andmete kaasamisväärtuse muutmisel külalise tellimuse otsingul** väljal peate käitama Commerce Headquartersis töö1070 (**kanali konfiguratsioon**) ja minema **Jaemüügi ja äri \> Jaemüük ja äri IT \> jaotusgraafikusse**.

## <a name="configure-the-order-lookup-module"></a>Tellimuse otsingumooduli konfigureerimine

Commerce module library tellimuse otsingumoodulit kasutatakse tellimuse otsimiseks kasutatava vormi renderdamiseks. Tellimuse otsingumoodul võib olla kaasatud iga lehe kehapesasse, mis ei nõua kliendi sisselogimist. Lisateavet mooduli konfigureerimise kohta vt [Tellimuse otsingumoodulist](order-lookup-module.md).

## <a name="additional-resources"></a>Lisaressursid

[Tellimuse otsingu moodul](order-lookup-module.md)

[Meiliteatise profiili seadistamine](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
