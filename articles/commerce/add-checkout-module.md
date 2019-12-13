---
title: Maksmise moodul
description: Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4b810441fd25d41ee0893b119b4f7d91e7435d21
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697079"
---
# <a name="checkout-module"></a>Maksmise moodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse, kuidas lisada lehele maksmise moodul ja määrata vajalikud atribuudid.

## <a name="overview"></a>Ülevaade

Maksmise moodul on spetsiaalne konteiner, mis majutab kõiki tellimuse loomiseks vajalikke mooduleid. Kassa moodul võib sisaldada mooduleid, mis töötlevad kättetoimetamise aadressi, tarne meetodeid, arveldusteavet, tellimuse kokkuvõtet ja muud kliendi tellimusega seotud teavet. See esitab samm-sammulise voo, mida klient ostu sooritamiseks kogu asjakohase teabe sisestamiseks kasutab.

Maksmise moodul renderdab andmeid ostukorvi ID põhjal. See ostukorvi ID salvestatakse brauseriküpsisena. Ostukorvi ID on nõutav, et renderdada maksmise mooduli teavet, nagu tellimuse kaubad, kogusumma ja allahindlused.

## <a name="checkout-module-properties"></a>Maksmise mooduli atribuudid

Maksmise moodul majutab endas moodulite kogumit. Laiuse atribuut võimaldab teil määrata, kas maksmise moodulis olevad kaubad peavad mahtuma selle laiusesse või täitma ekraani.

Maksmise moodulil on mitu pesa, näiteks pesa **Maksmise teave**, pesa **Tellimuse kokkuvõte** ja pesa **Tellimuse esitamine**. Iga pesa toetab moodulite kogumit, mis kuvatakse lehel kindlas paigutuses. Näiteks sisaldab pesa **Maksmise teave** kõiki mooduleid, mis on vajalikud maksmise käivitamiseks, nagu saatmise aadressi ja makseviisi moodulid. Pesa **Tellimuse kokkuvõtte** näitab tellimuse kokkuvõtet ja toetab tellimuse esitamise tegevust. Pesa **Tellimuse esitamine** toetab samuti tellimuse esitamise tegevust. Tellimuse esitamise mooduleid saab erinevatelt platvormidelt tellimuste esitamise protsessi optimeerimiseks määratleda kahes pesas.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moodulid, mida saab ostukorvi moodulis kasutada

- **Tarneaadress** – see moodul võimaldab kliendil lisada või valida tellimuse tarneaadressi. Kui klient on sisse logitud, kuvatakse aadress, mis selle kliendi jaoks eelmisel korral salvestati. Seejärel saab klient valida nende aadresside seast. Klient saab lisada ka uue aadressi. Tarneaadressi kasutatakse kõigi kaupade puhul, mis nõuavad tarnet. Seda ei saa üksikute reakaupade puhul kohandada. Tarneaadressi vormingud määratletakse iga riigi või piirkonna kohta ja sellest moodulist tulenevad riigi/piirkonna spetsiifilised reeglid. Kuigi see moodul ei paku aadressi kinnitamist, saab aadressi kinnitamist rakendada kohandamise kaudu. Kui tellimus sisaldav ainult kaupu, millele minnakse poodi järgi, siis see moodul peidetakse automaatselt.
- **Tarnevalikud** – see moodul võimaldab kliendil valida tellimuse tarnevaliku. tarnevalikud põhinevad saatmisaadressil. Kui tarneaadressi muudetakse, tuleb tarnevalikud uuesti hankida. Kui tellimus sisaldav ainult kaupu, millele minnakse poodi järgi, siis see moodul peidetakse automaatselt.
- **Maksmise jaotise konteiner** – see moodul on konteiner, kuhu saate lisada mitu moodulit, et luua jaotis maksmise voo sees. Näiteks saate panna sellesse konteinerisse kõik maksmisega seotud moodulid, et need kuvataks ühe jaotisena. See moodul mõjutab ainult voo paigutust.
- **Kinkekaart** – see moodul võimaldab kliendil tasuda tellimuse eest kinkekaardiga. See toetab ainult Microsoft Dynamics 365 Commerce’i kinkekaarte. Tellimusele saab rakendada ühe või mitu kinkekaarti. Kui kinkekaardi saldo ei kata ostukorvis olevat summat, saab kinkekaardi kombineerida muu makseviisiga. Kinkekaarte saab lunastada ainult siis, kui klient on sisse logitud.
- **Püsikliendi punktid** – see moodul võimaldab kliendil tasuda tellimuse eest püsikliendi punktidega. See esitab saadaolevate punktide ja aeguvate punktide kokkuvõtte ja võimaldab klientidel valida lunastamiseks punktide arvu. Kui klient ei ole sisse logitud või ei ole püsikliendis programmi liige või kui ostukorvi kogusumma on 0 (null), peidetakse see moodul automaatselt.
- **Krediitkaart** – see moodul võimaldab kliendil tasuda tellimuse eest krediitkaardiga. Kui püsikliendi punktid või kinkekaart katab ostukorvi kogusumma või kui see on 0 (null), peidetakse see moodul automaatselt. Krediitkaardi integratsiooni pakub Adyeni makseühendus. Lisateavet selle konnektori kasutamise kohta vaadake teemast [Adyeni makseühendus](https://).
- **Arveldusaadress** – see moodul võimaldab kliendil esitada arveldusteavet. Seda teavet töötleb koos krediitkaardi teabega Adyen. See moodul sisaldab võimalust, et kliendid kasutavad oma arveldusaadressi tarneaadressina.
- **Kontaktteave** – see moodul võimaldab kliendil lisada või muuta tellimuse kontaktandmeid (meiliaadress).
- **Tellimuse esitamine** – see moodul võimaldab kliendil esitada tellimuse.
- **Sisurikas plokk** – see moodul sisaldab mis tahes teateid, mida juhib sisuhaldussüsteem (CMS). Näiteks võib see sisaldada teadet, mis ütleb: „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-FABRIKAM”. 
- **Tellimuse Kokkuvõte** – selles moodulis kuvatakse tellimuse kulude jaotus.
- **Tellimuserea kaubad** – selles moodulis kuvatakse tellimuses sisalduvate kaupade kokkuvõte.

## <a name="retail-server-interaction"></a>Jaemüügiserveri suhtlus

Enamik maksmise teabest, näiteks tarneaadress ja tarnemeetod, salvestatakse ostukorvis ja töödeldakse tellimuse osana. Ainus erand on krediitkaardi teave. See teave töödeldakse otse Adyeni makseühenduse abil. Makse on autoriseeritakse, kuid seda ei nõuta sisse.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Uuele lehele maksmise mooduli lisamine ja vajalike atribuutide seadistamine

Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Avage **Fragment \> Uus fragment** ja andke uuele fragmendile nimi **Maksmise fragment**.
1. Lisage fragmendile maksmise moodul.
1. Lisage maksmise moodulile päis.
1. Lisage pesas **Maksmise teave** tarneaadressi, tarnevaliku, maksmise jaotise konteineri ja kontaktteabe moodulid. Nüüd peaks pesas **Maksmise teave** olema neli jaotist.
1. Lisage maksmise jaotise konteinermoodulis kinkekaardi, püsikliendi punktide ja krediitkaardi moodulid. Sel viisil saate kindlustada, et kõik maksmisviisid ilmuvad jaotises koos.
1. Lisage pesas **Tellimuse kokkuvõte** tellimuse kokkuvõtte, tellimuse esitamise ja sisurikas plokimoodul.
1. Lisage sisurikkas plokimoodulis järgmine tekst: **Tellimusega seotud küsimuste korral võtke ühendust numbril 1-800-FABRIKAM**.
1. Lisage pesas **Tellimuse esitamine** tellimuse esitamise moodul.
1. Valige käsk **Salvesta**. Osasid mooduleid ei pruugita eelvaates renderdada, kuna nendel puudub kaardi kontekst.
1. Kontrollige selles fragmenti ja avaldage see.
1. Looge mall, mis kasutab uut maksmise fragmenti.
1. Looge maksmise leht, mis kasutab uut malli.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Ostukorvi moodul](add-cart-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
