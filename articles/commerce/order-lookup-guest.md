---
title: Tellimuse otsingu lubamine külaliste väljaregistreerimiseks
description: See artikkel kirjeldab, kuidas lubada tellimuste otsingut sisseregistreerimiseks Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 4f381f1ec0ea08f18db3cac474e8990906364504
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286887"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Tellimuse otsingu lubamine külaliste väljaregistreerimiseks

[!include [banner](includes/banner.md)]

See artikkel kirjeldab, kuidas lubada tellimuste otsingut sisseregistreerimiseks Microsoft Dynamics 365 Commerce.

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

Pärast isiklike **andmete** kaasamisväärtuse muutmisel külalise tellimuse otsinguväljal peate käitama töö 1070 (**kanali** konfiguratsioon) Commerce Headquartersis **\>, nides jaemüügi ja äri jaemüügi ja äri äri IT \> jaotuse graafikusse**.

## <a name="configure-the-order-lookup-module"></a>Tellimuse otsingumooduli konfigureerimine

Commerce module library tellimuse otsingumoodulit kasutatakse tellimuse otsimiseks kasutatava vormi renderdamiseks. Tellimuse otsingumoodul võib olla kaasatud iga lehe kehapesasse, mis ei nõua kliendi sisselogimist. Lisateavet mooduli konfigureerimise kohta vt [Tellimuse otsingumoodulist](order-lookup-module.md).

## <a name="configure-the-order-details-page"></a>Tellimuse üksikasjade lehe konfigureerimine

Enne, kui külaliskasutajad saavad vaadata oma tellimuse üksikasju, peab tellimuse üksikasjade leht teie e-äri saidil olema konfigureeritud nii, et see ei nõua sisselogimist. Tellimuse üksikasjade lehe sisselogimisnõude välja lülitamiseks avage leht Commerce’i saidikonstruktoris, **valige puuvaates vaikeleht (nõutav)** **ja** tühjendage parempoolsel paanil atribuutide allosas ruut Nõuab logimist.

## <a name="add-a-link-to-order-details-in-transactional-emails"></a>Lisa link kande meilide üksikasjade tellimiseks

Tellimusega seotud meilide puhul saate anda lingi või nupu, mis viib kliendid tellimuse üksikasjade lehele. Lingi või nupu lisamiseks looge HTML-link, mis osutab tellimuse üksikasjade leheküljele teie e-kaubanduse saidil, ning läbige tellimuse kinnituse ID ja kliendi meiliaadress URL-i parameetritena, nagu näha järgmises näites.

`<a href="https://[domain]/[orderdetailspage]?confirmationId=%orderconfirmationid%&propertyName=email&propertyValue=%customeremailaddress%" target="_blank">View my order status</a>`

## <a name="additional-resources"></a>Lisaressursid

[Tellimuse otsingu moodul](order-lookup-module.md)

[Meiliteatise profiili seadistamine](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
