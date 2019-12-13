---
title: Ostukorvi moodul
description: See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696757"
---
# <a name="cart-module"></a>Ostukorvi moodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.

## <a name="overview"></a>Ülevaade

Ostukorvi moodul on konteiner, mida kasutatakse kõikide moodulite majutamiseks, mis on vajalikud ostukorvis olevate kaupade esitlemiseks. Näiteks sisaldab see kõiki ostukorvi lisatud kaupu, tellimuse kokkuvõtet ja sooduskoode.

Ostukorvi moodul renderdab andmeid ostukorvi ID põhjal. Ostukorvi ID on brauseri küpsis, mis on kogu saidil saadaval.

## <a name="cart-module-properties-and-slots"></a>Ostukorvi mooduli atribuudid ja pesad

Konteinerina kontrollib ostukorvi moodul osasid põhiatribuute, nagu pealkiri ja laius. Pealkiri on tavaliselt tekst, näiteks **Ostukorv**, **Teie ostukorv** või **Ostukorvis olevad kaubad**. Laiuse säte määratleb, kas konteineri sees olevad moodulid peavad mahtuma sellesse konteinerisse või kas need saavad täita ekraani.

Ostukorvi leht on jagatud mitmeks piirkonnaks: ostukorvi reakaubad, tellimuse kokkuvõte ja maksmine, ning poes otsimise funktsiooniks. Iga piirkond on vastendatud ostukorvi mooduli pesaga ja iga pesa võtab vastu eelmääratletud moodulite kogumi.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moodulid, mida saab ostukorvi moodulis kasutada

- **Ostukorvi reakaubad** – see moodul kuvab iga ostukorvi lisatud kauba kokkuvõtte. Teave hõlmab toote pealkirja, valitud mõõtmeid, hinda, kogust ja allahindlusi. See moodul toetab ka selliseid toiminguid nagu „Eemalda ostukorvist” ja „Lisa soovinimekirja”. Iga rea kauba jaoks on olemas võimalus kauba saata või sellele poodi järele minna. See valik tuleb poes kättesaamise moodulus eraldi konfigureerida.
- **Tellimuse Kokkuvõte** – see moodul näitab tellimuse kokkuvõtet. Teave hõlmab vahesummat, saatmist, makse ja allahindlust. Selle mooduli pealkirja saab konfigureerida.
- **Sooduskood** – see moodul võimaldab kliendil sooduskoode lunastada. Sooduskoodi saab rakendada või eemaldada.
- **Maksmine** – see moodul algatab maksmise tegevuse ja suunab kasutaja maksmise lehele. Selle mooduli jaoks tuleb konfigureerida kolm linki:

    - **Maksmine** – see link sunnib kliente sisse logima, kui nad pole veel sisse logitud.
    - **Külalisena maksmine** – see link võimaldab klientidel esitada tellimusi anonüümselt. See kuvatakse ainult siis, kui kliendid ei ole sisse logitud.
    - **Tagasi ostlema** – see link võimaldab klientidel naasta kodulehele või mis tahes teisele lehele, et ostlemisega jätkata.

- **Sisurikas plokk** – see moodul toetab ostukorvi mooduli kohandatud sõnumeid. Sõnumeid juhib sisuhaldussüsteem (CMS). Lisada on võimalik mis tahes sõnum, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam”.
- **Kättesaamine poest** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas. Vaikimisi kuvab see moodul poed, mis jäävad kliendi asukohast 50 miili raadiusse. Samas saab otsingu raadiust selles moodulis kohandada. Iga poe jaoks teostatakse varude kontroll, kui varude kontrolli funktsioon on sisse lülitatud, ja kuvatakse vastav laos olemas või laost otsas teade.
- **Poodide otsing Bingi kaartidel** – seda moodulit saab kasutada poes kättesaamise mooduli sees. See võimaldab klientidel otsida poode sisestades asukoha. Bingi kaartide geokodeerimise rakenduse programmeerimisliidest (API) kasutatakse kliendi sisestatud asukoha teisendamiseks laius- ja pikkuskraadideks. Kui seda moodulit ei kasutata, kuvatakse ainult kliendi praeguse asukoha lähedal asuvad poed ja klient ei saa teist asukohta otsida.

## <a name="cart-module-settings"></a>Ostukorvi mooduli sätted

Ostukorvi moodulitel saab konfigureerida kolme sätet.

- **Maksimaalne kogus** – iga kauba maksimaalne arv, mida saab ostukorvi lisada. Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.
- **Varude kontroll** – kui väärtus on satud suvandile **Tõene**, saab kauba lisada ostukorvi ainult pärast seda, kui ostukasti moodul on veendunud, et see oleks laos olemas. See varude kontroll tehakse nii stsenaariumide jaoks, kus kaup saadetakse, kui ka stsenaariumide jaoks, kus sellele tullakse poodi järele. Kui väärtuseks on seatud suvand **Väär**, siis enne kauba ostukorvi lisamist ja tellimuse esitamist varude kontrolli ei tehta.
- **Varude puhver** – varusid hallatakse reaalajas ja kui paljud kliendid esitavad tellimusi, võib täpse varude arvu säilitamine olla keeruline. Seega saab varude jaoks määrata puhvri. Kui varude kontroll on tehtud, siis kui varusid on vähem kui puhvri kogus, käsitletakse toodet kui laost otsas. Seega kui müük toimub kiiresti läbi mitme kanali, nii et varade arv pole täielikult sünkroonitud, on vähem ohtu, et müüakse kaup, mis on laost otsas.

## <a name="retail-server-interaction"></a>Jaemüügiserveri suhtlus

Ostukorvi moodul toob toote teabe jaemüügiserveri API-de abil. Brauseriküpsise ostukorvi ID-d kasutatakse jaemüügiserverist kogu tooteteabe toomiseks.

## <a name="add-a-cart-module-to-a-page"></a>Lehele ostukorvi mooduli lisamine

Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.

1. Looge fragment nimega **ostukorvi fragment** ja lisage sellele ostukorvi moodul.
1. Ostukorvi mooduli pesas **Ostukorvi reakaubad** lisage ostukorvi reakaupade moodul.
1. Lisage pesas **Tellimuse kokkuvõte** tellimuse kokkuvõtte moodul.
1. Lisage pesas **Sooduskood** sooduskoodi moodul.
1. Lisage pesas **Maksmine** maksmise moodul.
1. Lisage pesas **Otsing poes** poest kättesaamise moodul.
1. Poes kättesaamise moodulis valige pesa **Otsing poes** ja lisage poe Bingi kaartidelt otsimise moodul.
1. Kontrollige fragmenti ja avaldage see.
1. Looge mall nimega **ostukorvi mall**ja lisage sellele ostukorvi fragment, mille just lõite.
1. Salvestage mall, kontrollige seda ja avaldage see.
1. Looge leht, mis kasutab uut malli.
1. Salvestage ja kuvage lehe eelvaade.
1. Registreerige leht ja avaldage see.

## <a name="additional-resources"></a>Lisaressursid

[Alustuskomplekti ülevaade](starter-kit-overview.md)

[Konteinermoodul](add-container-module.md)

[Ostukasti moodul](add-buy-box.md)

[Väljaregistreerimise moodul](add-checkout-module.md)

[Tellimuse kinnituse moodul](order-confirmation-module.md)

[Päise moodul](author-header-module.md)

[Jaluse moodul](author-footer-module.md)
