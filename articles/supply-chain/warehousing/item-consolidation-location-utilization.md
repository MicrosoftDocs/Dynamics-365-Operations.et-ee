---
title: Kauba konsolideerimine – asukoha kasutamine
description: Selles teemas antakse teavet funktsiooni kohta, mis hõlbustab laohalduritel kuvada ja filtreerida asukohtade mahulist kasutust terves laos. Haldurid saavad valida asukohti ja luua varude liikumise tööd otse kauba konsolideerimise lehelt, et konsolideerida kaupu ja seeläbi kasutada laos olevat ruumi tõhusamalt.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 6a328b20c1cfb2fc376ab4656c64cf585a5aa015
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4426583"
---
# <a name="item-consolidation---location-utilization"></a>Kauba konsolideerimine – asukoha kasutamine

[!include [banner](../includes/banner.md)]

Selles teemas antakse teavet funktsiooni kohta, mis hõlbustab laohalduritel kuvada ja filtreerida asukohtade mahulist kasutust terves laos. Haldurid saavad valida asukohti ja luua varude liikumise tööd otse lehelt **Kauba konsolideerimine**, et konsolideerida kaupu ja seeläbi kasutada laos olevat ruumi tõhusamalt.

## <a name="turn-on-the-features"></a>Funktsioonide sisselülitamine

Enne, kui saate kasutada selles teemas kirjeldatud funktsioone, peate need oma süsteemis sisse lülitama. Administraatorid saavad kasutada tööruumi [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et kontrollida funktsioonide olekut ja need vajadusel sisse lülitada. Lülitage sisse mõlemad järgmised funktsioonid loendis olevas järjekorras. (Mõlemad funktsioonid on mooduli **Laohaldus** jaoks.)

1. Laoasukoha olek
2. Kauba konsolideerimise asukoha kasutamine

## <a name="warehouse-location-status"></a>Laoasukoha olek

Funktsioon *Lao asukoha olek* lisab lehele **Asukohad** neli uut välja, et jälgida lisateavet asukoha praeguse oleku kohta.

- **Kaubakood** – kaup, mis on hetkel asukohas. Kui asukoht sisaldab mitut kaupa, jäetakse see väli tühjaks.
- **Viimase tegevuse kuupäev ja kellaaeg** – selle asukohaga tehtud viimase laokande ajatempel.
- **Ajalise jaotuse kuupäev** – kuupäev, mil selle asukoha varud toodi lattu. See kuupäev arvutatakse identifitseerimisnumbri aegumiskuupäeva alusel. Kuigi see kuupäev on täpne identifitseerimisnumbri järgi jälgitavate asukohtade puhul, ei pruugi see olla täpne asukohtade puhul, mida ei jälgita identifitseerimisnumbri järgi.
- **Asukoha olek** – selle asukoha olek. Saadaval on neli väärtust.

    - **Määratlemata** – asukohaprofiil ei jälgi olekut. Seetõttu ei ole praegune olek teada.
    - **Tühi** – asukohas pole praegu varusid.
    - **Komplekteerimine** – väljaminevad kanded on tehtud asukoha suhtes pärast seda, kui see oli viimati tühi.
    - **Ladustamine** – ainult sissetulevad kanded on tehtud sellest ajast, kui see oli viimati tühi.

Need väljad võimaldavad laohalduritel saada täpsemat ülevaadet lao asukohtade oleku kohta. Need võimaldavad ka palju täpsemat aruandlust ja filtreerimist.

## <a name="set-up-item-consolidation-and-location-utilization"></a>Kauba konsolideerimise ja asukoha kasutamise seadistamine

Selles jaotises kirjeldatakse, kuidas valmistada süsteemi ette kauba konsolideerimise ja asukoha kasutamise kasutamiseks. Need protseduurid kasutavad standardsete demoandmete näidisväärtusi. Kui plaanite töötada näidisstsenaariumiga, mida selles teemas hiljem käsitletakse, valige juriidiline isik **USMF** (mis sisaldab standardseid demoandmeid) ja looge kõik selles jaotises kirjeldatavad kirjed. Kui te ei plaani töötada näidisstsenaariumiga, saate siin esitatud väärtusi käsitleda sellist tüüpi seadistuste näidetena, mille peate funktsioonide kasutamiseks lõpule viima.

### <a name="released-product"></a>Väljastatud toode

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Valige väljal **Kaubakood** suvand *M9201* ja avage üksikasjade leht.
1. Valige toimingupaani vahekaardi **Varude haldamine** grupis **Ladu** suvand **Füüsilised dimensioonid**.
1. Valige toimingupaani lehel **Füüsilised dimensioonid** suvand **Uus**.

    Ruudustikku lisatakse uus rida. Väli **Kaubakood** on eelseadistatud.

1. Valige *ea* väljal **Ühik**. Rea ülejäänud väljad määratakse automaatselt.
1. Valige **Salvesta** ja sulgege leht.

### <a name="location-profile"></a>Asukohaprofiil

1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.
1. Valige asukohaprofiilide loendist suvand **KORRUS-05**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Veenduge, et kiirkaardil **Üldine** oleks mõlema järgmise suvandi väärtuseks seatud *Jah*.

    - Luba kaup asukohas
    - Luba asukoha olek

1. Valige käsk **Salvesta**.

    > [!IMPORTANT]
    > Kui suvandite **Luba kaup asukohas** ja **Luba asukoha olek** väärtuseks oli juba seatud *Jah*, jätkake etapis 10 toodud juhistega kiirkaardi **Dimensioonid** seadistamiseks. Kui suvandite väärtuseks polnud seatud *Jah*, peate käivitama ühtsuskontrolli mooduli **Laohaldus** jaoks pärast nende käsitsi määramist. Sellisel juhul jätkake järgmise etapiga.

1. Ühtsuskontrolli käivitamiseks avage jaotis **Süsteemi administreerimine \> Perioodilised ülesanded \> Andmebaas \> Ühtsuskontroll**.
1. Dialoogiboksis **Ühtsuskontroll** määrake järgmised väärtused.

    - **Moodul:** *laohaldus*
    - **Kontroll/parandus:** *Kontroll*
    - **Alates kuupäevast:** jätke väli tühjaks.
    - **Lao asukoha oleku ühtsuskontroll:** märkige see ruut.

1. Valige nupp **OK**.

    > [!TIP]
    > Teile kuvatakse teade, kui ühtsuskontroll on lõpule viidud. Teate kuvamiseks avage [Tegevuskeskus](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications). Valige üksikasjade kuvamiseks **Halda üksikasju**.
    >
    > Kui ühtsuskontroll kuvab teadet „Leiti vale asukoha oleku teave asukoha XXXX jaoks laos XX”, peate käivitama ühtsuskontrolli uuesti. Seekord seadke välja **Kontroll/parandus** väärtuseks *Paranda tõrge*. Kontrollige teateid, veendumaks, et tõrkeid ei leitud.

1. Nüüd peate asukohaprofiili seadistamise lõpetama. Naaske jaotisse **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**, valige asukohaprofiil **KORRUS-05** ja seejärel valige toimingupaanil **Redigeeri**.
1. Määrake kiirkaardil **Dimensioonid** järgmised väärtused.

    - **Mahu kasutamise protsent:** *100*
    - **Lao asukoha jaoks kasutatav mahuline meetod:** *Kasuta asukoha mahtu*
    - **Asukoha tegelik kõrgus:** *10*
    - **Asukoha tegelik laius:** *10*
    - **Asukoha tegelik sügavus:** *10*
    - **Maksimaalne kaal:** *100*

1. Valige käsk **Salvesta**.

### <a name="mobile-device-menu-items"></a>Mobiilse seadme menüü-üksused

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige toimingupaanil **Uus**, et luua menüü-üksus sortimiseks.
1. Määrake päises järgmised väärtused.

    - **Menüü-üksuse nimi:** *Korrigeeri üksuses*
    - **Pealkiri:** *Korrigeeri üksuses*
    - **Režiim:** *töö*
    - **Kasuta olemasolevat tööd:** *Ei*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Töö loomise protsess:** *Korrigeeri üksuses*
    - **Varude korrigeerimistüübid:** *Korrigeeri üksuses*

1. Valige käsk **Salvesta**.

### <a name="mobile-device-menu"></a>Mobiilse seadme menüü

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige menüüde loendist suvand **Varud**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Otsige üles ja valige loendist **Saadaolevad menüüd ja menüü-üksused** suvand **Korrigeeri üksuses**.
1. Valige paremnoole nupp, et teisaldada **Korrigeeri üksuses** loendisse **Menüü struktuur**. Sedasi saate lisada uue menüü-üksuse valitud menüüsse.
1. Valige käsk **Salvesta**.

### <a name="movement-types"></a>Teisaldamise tüübid

1. Avage jaotis **Laohaldus \> Seadistus \> Varud \> Liikumise tüübid**.
1. Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.

    - **Liikumise tüübi kood:** *KONSOLIDEERI*
    - **Kirjeldus:** *Konsolideeri asukohad*
    - **Töö klassi ID:** *InvMov*

1. Valige käsk **Salvesta**.

## <a name="example-scenario"></a>Näidisstsenaarium

Järgmine stsenaarium kasutab mobiilse seadme laorakendust, et teha varude *korrigeerimist üksusesse* lao kahes asukohas.

### <a name="add-inventory-to-locations"></a>Varude lisamine asukohtadesse

1. Logige mobiilsesse seadmesse sisse kasutajana, kes on seadistatud lao *51* jaoks.
1. Avage jaotis **Varud \> Korrigeeri üksuses**.

    Nüüd saate sisestada esimese asukoha korrigeerimise.

1. Valige ülesandes **Korrigeeri üksuses** asukoht, mille jaoks varude korrigeerimist teha. Valige väljal **LOC** suvand *LP-001*.
1. Kinnitage asukoht.
1. Looge asukohta lisatava kauba jaoks identifitseerimisnumbri ID. Sisestage väljale **LP** väärtus *LP00101*.
1. Kinnitage identifitseerimisnumber.
1. Sisestage kaup, mis lisatakse identifitseerimisnumbrile. Sisestage väljale **ITEM** väärtus *M9201*.
1. Kinnitage kaup.
1. Sisestage lisatava kauba kogus. Sisestage väljale **KOGUS** väärtus *10*.
1. Kinnitage kogus.

    Teile kuvatakse teade „Töö lõpule viidud”. Nüüd saate sisestada teise asukoha korrigeerimise.

1. Valige ülesandes **Korrigeeri üksuses** asukoht, mille jaoks varude korrigeerimist teha. Valige väljal **LOC** suvand *LP-002*.
1. Kinnitage asukoht.
1. Looge asukohta lisatava kauba jaoks identifitseerimisnumbri ID. Sisestage väljale **LP** väärtus *LP00201*.
1. Kinnitage identifitseerimisnumber.
1. Sisestage kaup, mis lisatakse identifitseerimisnumbrile. Sisestage väljale **ITEM** väärtus *M9201*.
1. Kinnitage kaup.
1. Sisestage lisatava kauba kogus. Sisestage väljale **KOGUS** väärtus *15*.
1. Kinnitage kogus.

    Teile kuvatakse teade „Töö lõpule viidud”.

1. Valige nupp Menüü (nimetatakse mõnikord hamburgeriks või hamburgeri nupuks) ja seejärel valige **Tühista**, et väljuda ülesandest **Korrigeeri üksuses**.

### <a name="consolidate-locations"></a>Asukohtade konsolideerimine

1. Avage jaotis **Laohaldus \> Perioodilised ülesanded \> Kauba konsolideerimine**.
1. Valige päises ladu, mille jaoks soovite konsolideerimist teha. Sisestage väljal **Ladu** väärtus *51*.

    Kuvatakse kirje iga asukoha kohta, kus kaup *M9201* korrigeeriti. Veerus **Kasutuse protsent** kuvatakse iga asukoha mahuline kasutamine.

1. Varude konsolideerimiseks valige kõik konsolideeritavad asukohad ja seejärel valige toimingupaanil **Konsolideeri varud**.
1. Määrake dialoogiboksis **Konsolideeri varud** asukoht ja liikumise tüüp, mida tuleks kasutada varude liikumise töö loomiseks. Määrake järgmised väärtused.

    - **Asukoht:** *LP-001*
    - **Liikumise tüübi kood:** *KONSOLIDEERI*

1. Valige nupp **OK**.
1. Saate teate, mis kuvab loodud liikumise töö. Märkige üles liikumise ID.

### <a name="view-movement-work"></a>Liikumise töö kuvamine

1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Vaadake loodud tööd. Kasutage liikumise töö ID-d varude konsolideerimisest, et filtreerida või otsida tööruudustikku.

    Selle stsenaariumi puhul kasutati varude konsolideerimise asukohana olemasolevat asukohta, millel oli varusid. Seetõttu loodi ainult üks töö ID.

    > [!NOTE]
   > Süsteem loob ühe töö ID iga liikumise kohta, mis tuleb lõpule viia. Kui määrate juba varusid sisaldava asukoha, luuakse ainult üks töö ID. Kui määrate uue asukoha, luuakse kaks töö ID-d.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]