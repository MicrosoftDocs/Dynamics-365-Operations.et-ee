---
title: Laoasukoha olek
description: Selles teemas antakse ülevaade lao asukoha oleku funktsiooni kohta.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 29815abc2892aecb080a9b673f2336f5368821ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993774"
---
# <a name="warehouse-location-status"></a>Laoasukoha olek

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management sisaldab mitut asukoha välja, mis annavad teile paindlikku asukohtadega töötamisel ja nende haldamisel. Asukoha olekuid saate kaasata asukohakorralduse päringusse, et tagada lao voo parem juhtimine.

Järgmised neli välja lehel **Asukohad** jälgivad teavet asukoha praeguse oleku kohta. Need väljad võimaldavad laohalduritel saada ülevaadet lao asukohtade oleku kohta. Need võimaldavad ka täpsemat aruandlust ja filtreerimist.

- **Kaubakood** – kaup, mis on hetkel asukohas. Kui asukoht sisaldab mitut kaupa, on see väli tühi.
- **Viimase tegevuse kuupäev ja kellaaeg** – selle asukohaga tehtud viimase laokande ajatempel.
- **Ajalise jaotuse kuupäev** – kuupäev, mil selle asukoha varud toodi lattu. See väärtus arvutatakse identifitseerimisnumbri ajalise jaotuse kuupäeva alusel. See on täpne asukohtade puhul, mida jälgitakse identifitseerimisnumbri järgi, kuid ei pruugi olla täpne asukohtade puhul, mida ei jälgita identifitseerimisnumbri järgi.
- **Asukoha olek** – selle asukoha olek. Võimalikke väärtuseid on neli.

    - **Määratlemata** – asukohaprofiil ei saa jälgida olekut. Seetõttu ei ole praegune olek teada.
    - **Tühi** – asukohas pole praegu ühtegi varu.
    - **Komplekteerimine** – väljaminevad kanded on tehtud asukoha suhtes, kui see oli viimati tühi.
    - **Ladustamine** – ainult sissetulevad kanded on tehtud asukoha suhtes sellest ajast, kui see oli viimati tühi.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Funktsiooni Lao asukoha olek sisselülitamine

Enne funktsiooni *Lao asukoha olek* kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Lao asukoha olek*

## <a name="set-up-warehouse-location-status"></a>Lao asukoha oleku seadistamine

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Valmistage ette näitestsenaariumi jaoks nõutavad näidisandmed

Enne, kui alustate stsenaariumi kasutamist, peate aktiveerima näidisandmed ja seadistama selle funktsiooni käesolevas jaotistes kirjeldatu järgi. Näidisstsenaariumi lõpule viimiseks peate kasutama laorakendust või brauseripõhist emulaatorit. Siin esitatud etapid kasutavad laorakendust. Brauseripõhise emulaatori etapid on sarnased.

#### <a name="use-the-usmf-legal-entity"></a>Juriidilise isiku USMF kasutamine

Selle näidisstsenaariumi kasutamiseks siin määratud näidiskirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Enne alustamist peate valima ka juriidilise isiku **USMF**.

#### <a name="set-up-location-profiles"></a>Asukohaprofiilide häälestamine

See näidisstsenaarium nõuab kahe asukohaprofiili ettevalmistamist.

1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.
1. Lehe redigeerimisrežiimi panemiseks valige **Redigeeri**.
1. Valige profiil **HULGI-06**.
1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Luba kaup asukohas:** määrake selle suvandi väärtuseks _Jah_.
    - **Luba asukoha tegevuse kuupäev ja kellaaeg:** määrake selle suvandi väärtuseks _Jah_.
    - **Luba asukoha olek:** määrake selle suvandi väärtuseks _Jah_.

    Need suvandid juhivad seda, kas asukoha viiteväljad on aktiivsed.

1. Korrake etappe 3–4 profiili **KOMPLEKTEERIMINE-06** jaoks.

> [!NOTE]
> Kui asukohaprofiili parameetrid (**Luba kaup asukohas**, **Luba asukoha tegevus**, **Luba asukoha olek**) on seatud väärtusele *Jah*, uuendab süsteem vastavaid asukohti kohe, käivitades *lao asukoha oleku ühtsuskontrolli* töö.

### <a name="scenario"></a>Stsenaarium

1. Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.
1. Valige suvand **Uus**.
1. Valige dialoogiboksi **Ostutellimuse loomine** kiirkaardi **Hankija** väljal **Hankija konto** suvand *104*.
1. Kiirkaardi **Üldine** väljal **Ladu** valige *61*.
1. Valige nupp **OK**.
1. Teie uus ostutellimus (PO) on avatud. See lisab uue tühja rea ruudustikku **Ostutellimuse read**. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** _A0002_
    - **Kogus:** _5_

1. Valige toimingupaani vahekaardi **Ost** grupis **Tegevused** suvand **Kinnita**, et kinnitada ostutellimus.
1. Avage mobiilsel seadmel jaotis **Sissetulev \> Vastuvõetud ost**.
1. Valige väli **PONUM**, sisestage ostutellimuse number ja kinnitage.
1. Valige väli **KAUP**, sisestage ostutellimuse number *A0002* ja kinnitage.
1. Sisestage lehel **KOGUS** kogus *5* ja kinnitage.

    Saate sisestada kogust mõlemal alloleval viisil.

    - Arvulise väärtuse liitmiseks või lahutamiseks valige plussmärgi (**+**) või miinusmärgi (**–**) nupp.
    - Numbriklahvistiku avamiseks valige plussmärgi (**+**) ja miinusmärgi (**–**) vaheline tühi väli.

1. Kinnitage kaubakoodi *A0002* ja koguse *5* valik. Lehe allosas kuvatakse teade „Töö lõpule viidud”.
1. Valige paremas ülanurgas nupp Menüü (mida nimetatakse mõnikord ka hamburgeriks või hamburgeri nupuks) ja seejärel valige **Tühista** menüüst **Vastuvõetud ost** väljumiseks ja menüüsse **Sissetulev** naasmiseks.
1. Valige ostutellimuse lehel ruudustiku **Ostutellimuse read** kohal suvand **Töö üksikasjad**.
1. Pange tähele, et vahekaardil **Üldine** loodi väärtused **Töö ID** ja **Sihtidentifitseerimisnumbri ID**.
1. Pange tähele jaotise **Read** väärtusi **Asukoht** töötüüpide *Komplekteerimine* ja *Ladustamine* jaoks.
1. Avage mobiilsel seadmel jaotis **Sissetulev \> Ladustatud ost**.
1. Valige väli **ID**, sisestage töö ID ja kinnitage.
1. Kinnitage uuesti kirje *Komplekteerimine* lõpule viimiseks.
1. Valige paremast ülanurgast nupp Menüü ja seejärel valige **Valmis** töö *Komplekteerimine* lõpule viimiseks.
1. Märkige üles ladustamise asukoht ja kinnitage. Lehe allosas kuvatakse teade „Töö lõpule viidud”.
1. Valige paremas ülanurgas nupp Menüü nupp ja seejärel valige **Tühista** menüüst **Ladustatud ost** väljumiseks ja menüüsse **Sissetulev** naasmiseks.
1. Peamenüüsse naasmiseks valige **Tagasi**.
1. Avage Dynamics 365 Supply Chain Managementis jaotis **Laohaldus \> Seadistus \> Ladu \> Asukohad**.
1. Filtreerige suivandit **Asukoht** ja sisestage ladustamise asukoht ostutellimuse tööst. Teile peaks olema kuvatud järgmised tulemused.

    - Veerus **Asukoha olek** kuvatakse väärtus *Ladustamine*, kuna viimane kanne selles asukohas oli ladustamine.
    - Veerus **Kaubakood** kuvatakse väärtus *A0002*, kuna see kaup võeti vastu ja ladustati sellesse asukohta.
    - Veerus **Viimase tegevuse kuupäev ja kellaaeg** kuvatakse kuupäeva ja kellaaja ajatempel, mil töö viidi lõpule selles asukohas.

1. Avage mobiilse seadme jaotis **Kvaliteet \> Liikumine**.
1. Valige väli **LOC/LP** ja sisestage eelmises etapis üles märgitud asukoht.
1. Kinnitage kuvatav teave. Märkige üles loodud identifitseerimisnumbri number.
1. Valige kuval **Sihtkoha teave** väli **LOC/LP** ja sisestage asukohaks *06A07R2S1B*, kuhu kaup teisaldada.
1. Kinnitage kuval **Sihtkoha teave** väärtus **LP** (sihtidentifitseerimisnumber ID), mis luuakse automaatselt. Lehe allosas kuvatakse teade „Töö lõpule viidud”.
1. Valige paremas ülanurgas nupp Menüü ja seejärel valige **Tühista** menüüst **Liikumine** väljumiseks ja menüüsse **Kvaiteedihaldus** naasmiseks.
1. Peamenüüsse naasmiseks valige **Tagasi**.
1. Avage Dynamics 365 Supply Chain Managementis jaotis **Laohaldus \> Seadistus \> Ladu \> Asukohad**.
1. Värskendage lehte **Asukohad** ja vaadake uuesti algset ladustamise asukohta. Pange tähele, et välja **Asukoha olek** väärtuseks on nüüd seatud *Tühi* ja veerg **Kaubakood** on tühi.
1. Vaadake asukoha *06A07R2S1B* kirjet ja pange tähele, et suvandi **Olek** väärtuseks on muudetud *Ladustamine* ning väljad **Kaubakood** ja **Viimase tegevuse kuupäev ja kellaaeg** on värskendatud.
1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige suvand **Uus**.
1. Valige dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvand *US-002*.
1. Valige väljal **Ladu** väärtus *61*.
1. Valige nupp **OK**.
1. Teie uus müügitellimus on avatud. See lisab uue tühja rea ruudustikku **Müügitellimuse read**. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** _A0002_
    - **Kogus:** _1_

1. Valige ruudustiku kohal oleva menüü **Varud** kiirkaardilt **Müügitellimuse read** suvand **Reserveerimine**.
1. Valige lehel **Reserveerimine** tellimuserea reserveerimiseks suvand **Reserveeri saatepartii**. Seejärel valige lehe sulgemiseks paremas ülanurgas olevat nuppu **Sule** (**X**).
1. Tehke tegevuspaani vahekaardil **Ladu** grupis **Tegevused** valik **Vabasta lattu**.
1. Valige menüü **Ladu** jaotisest **Müügitellimuse read** suvand **Töö üksikasjad**.
1. Kopeerige loodud väärtus **Töö ID**.
1. Avage mobiilses seadmes jaotis **Väljaminev \> Müügi komplekteerimine**.
1. Valige väli **ID**, sisestage eelnevalt kopeeritud töö ID ja kinnitage.
1. Lehel **Müügitellimused: komplekteerimine** pakub väli **LOC** komplekteerimise asukohaks eelnevalt loodud ladustamise asukohta. Märkige see asukoht üles.
1. Valige väli **LOC**, sisestage asukoht ja kinnitage.
1. Valige väli **LP**, sisestage identifitseerimisnumbri number, mille märkisite üles tegevuse Liikumine käigus ja kinnitage.
1. Valige väli **Kaup**, sisestage ostutellimuse number *A0002* ja kinnitage.
1. Sisestage lehel **KOGUS** kogus *1* ja kinnitage.

    Saate sisestada kogust mõlemal alloleval viisil.

    - Arvulise väärtuse liitmiseks või lahutamiseks valige plussmärgi (**+**) või miinusmärgi (**–**) nupp.
    - Numbriklahvistiku avamiseks valige plussmärgi (**+**) ja miinusmärgi (**–**) vaheline tühi väli.

1. Valige väli **SIHT-LP**, sisestage kasutaja määratud sihtidentifitseerimisnumbri ID ja kinnitage.
1. Kinnitage uuesti komplekteerimistöö lõpule viimiseks. Lehe allosas kuvatakse teade „Töö lõpule viidud”.
1. Valige paremas ülanurgas nupp Menüü nupp ja seejärel valige **Tühista** komplekteerimise tegevuse lõpule viimiseks ja menüüsse **Väljaminev** naasmiseks.
1. Avage Dynamics 365 Supply Chain Managementis jaotis **Laohaldus \> Seadistus \> Ladu \> Asukohad**.
1. Filtreerige suvandit **Asukoht** ja sisestage komlekteerimise asukoht müügitellimuse tööst.
1. Pange tähele, et selle asukoha välja **Asukoha olek**, kust müügitellimus komplekteeritakse, väärtuseks on nüüd seatud *Komplekteerimine* ja väli **Viimase tegevuse kuupäev ja kellaaeg** on värskendatud.

> [!NOTE]
> Asukoha välju värskendatakse ainult laokannete alusel. Kui teisaldate varusid töölehe või mõne muu mitte-WHS protsessi abil, ei värskendata välju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]