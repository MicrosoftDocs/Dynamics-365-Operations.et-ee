---
title: Pane seinale – pane kauplusesse
description: Selles teemas antakse teavet funktsiooni Pane seinale – pane kauplusesse kohta. See funktsioon võimaldab teil käsitseda stsenaariume, kus peate konsolideerima toote eelpakkimise vaheasukohta konfigureeritavate kriteeriumide põhjal. See aitab vähendada komplekteerimise aega, sest see võimaldab komplekteerimist ühele sihtidentifitseerimisnumbrile ja panna rohkematesse asukohtadesse kui kogumi komplekteerimise puhul.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationType, WHSLocationProfile, WHSLocation, WHSPackProfile, WHSWaveStepCode, WHSOutboundSortTemplate, WHSPostMethod, WHSWaveTemplateTable, WHSLocDirTable, WHSWorkClass, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3f2ae63758fcb6247c5e56433645d9252576c755
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996271"
---
# <a name="put-to-wall---put-to-store"></a>Pane seinale – pane kauplusesse

[!include [banner](../includes/banner.md)]

Funktsioon *Pane seinale – pane kauplusesse* võimaldab teil käsitseda stsenaariume, kus peate konsolideerima toote eelpakkimise vaheasukohta konfigureeritavate kriteeriumide põhjal. Kuna see funktsioon võimaldab komplekteerimist ühele sihtidentifitseerimisnumbrile ja panna rohkematesse asukohtadesse kui kogumi komplekteerimise puhul, saavad lühenenud komplekteerimisajast kasu ettevõtted, mis lähetavad kauplustesse või tegelevad väikeste kaupadega.

Selle funktsiooni töövoog suunab komplekteeritud toote sortimise asukohta eri tüüpi konteineritesse jaotamiseks. Üldiselt sisaldab iga sortimise asukoht mitut sortimise paigutust. Iga sortimise asukoht määratakse vastavalt äriprotsessi seadistatud kriteeriumidele. Tavalised kriteeriumid on lõppsihtkoht, saadetis või koormus. Pärast toote saabumist jaotatakse see kõigi sortimise asukohtade vahel tellimuse, sihtkoha, saadetise või koormusega seostatud koguse põhjal. Kui konteiner on täis või lõpule viidud, teisaldatakse see sõltuvalt äriprotsessist vahekasukohta või saadetise asukohta edasiseks töötlemiseks.

Seda ladustamise funktsiooni nimetatakse ka näiteks kiireks panemiseks ja piirjoonte avamisteks.

## <a name="turn-on-the-outbound-sorting-feature"></a>Väljamineku sortimise funktsiooni sisselülitamine

Enne funktsiooni *Pane seinale – pane kauplusesse* kasutamist peab funktsioon *Väljamineku sortimine* olema teie süsteemis sisse lülitatud. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Väljamineku sortimine*

Funktsiooni *Väljamineku sortimine* saab kasutada koos funktsiooniga *Organisatsiooniülene vooetapi kood*, kui see on sisse lülitatud. Samuti peate selle funktsiooni sisse lülitama, kui kasutate eelmääratletud koode, mis seadistatakse vooetapi koodides. Tööruumis **Funktsioonihaldus** loetletakse seda funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Organisatsiooniülene vooetapi kood*

## <a name="setup"></a>Häälestus

Selle demo puhul kasutatakse standardseid Contoso andmeid ja ladu *62*. Samuti kasutatakse mõndasid hiljem esitatud täiendusi.

### <a name="location-type"></a>Asukoha tüüp

1. Avage jaotis **Laohaldus \> Seadistus \> Ladu \> Asukoha tüübid**.
1. Valige toimingupaanil **Uus**, et luua asukoha tüüp sortimiseks.
1. Määrake järgmised väärtused.

    - **Asukoha tüüp:** *SORTIMINE*
    - **Kirjeldus:** *Sortimine*

1. Valige käsk **Salvesta**.

### <a name="warehouse-management-parameters"></a>Laohalduse parameetrid

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Sisestage vahekaardi **Üldine** kiirkaardi **Asukoha tüübid** väljale **Sortimise asukoha tüüp** väärtus *SORTIMINE*.
1. Valige käsk **Salvesta**.

### <a name="location-profile"></a>Asukohaprofiil

1. Minge asukohta **Laohaldus \> Seadistus \> Ladu \> Asukohaprofiilid**.
1. Valige toimingupaanil **Uus**, et luua asukohaprofiil sortimise asukoha jaoks.
1. Määrake päises järgmised väärtused.

    - **Asukohaprofiili ID:** *Sortimine*
    - **Nimi:** *Sortimine*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Asukoha vorming:** *PAKKIMINE*
    - **Asukoha tüüp:** *SORTIMINE*
    - **Kasuta identifitseerimisnumbri jälgimist:** *Jah*
    - **Luba segakaubad:** *Jah*
    - **Luba varude segaolekud:** *Jah*

1. Valige käsk **Salvesta**.

### <a name="locations"></a>Asukohad

1. Avage **Laohaldus \> Seadistus \> Ladu \> Asukohad**.
1. Tühjendage märkeruut **Loo kontrollnumbrid asukoha jaoks**.
1. Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.

    - **Ladu:** *62*
    - **Asukoht:** *Sortimine*
    - **Asukohaprofiili ID:** *Sortimine*

1. Valige käsk **Salvesta**.

### <a name="packing-profiles"></a>Pakkimisprofiilid

1. Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Pakkimisprofiilid**.
1. Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.

    - **Pakkimisprofiili ID:** *Sortimine*
    - **Kirjeldus:** *Sortimine*
    - **Konteineri pakkimise poliitika:** jätke see väli tühjaks.
    - **Konteineri ID-režiim:** *Automaatne*
    - **Konteineri tüüp:** *KAUBAALUS 48X48*
    - **Konteineri automaatne loomine konteineri sulgemisel:** jätke see väli tühjaks.

1. Valige käsk **Salvesta**.

### <a name="wave-step-codes"></a>Vooetapi koodid

Kui lülitasite sisse funktsiooni *Organisatsiooniülene vooetapi kood*, seadistage järgmine kood.

1. Avage jaotis **Laohaldus \> Seadistus \> Vood \> Vooetapi koodid**.
1. Valige toimingupaanil **Uus** ja seejärel seadke järgmised väärtused.

    - **Vooetapi kood:** *Sortimine*
    - **Vooetapi kirjeldus:** *Sortimine*
    - **Vooetapi tüüp:** *Sortimismall*

1. Valige käsk **Salvesta**.

### <a name="outbound-sorting-template"></a>Väljastuste sortimise mall

Sortimismall juhib seda, kas sortimise asukohad luuakse, milliseid kriteeriume kasutatakse ja muid sortimisprotsessi atribuute.

1. Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Väljamineku sortimismallid**.
1. Sortimismalli loomiseks valige toimingupaanilt suvand **Uus**.
1. Määrake uue malli päises järgmised väärtused.

    - **Väljamineku sortimismalli ID:** *Voo sortimine*
    - **Kirjeldus:** *Voo sortimine*
    - **Sortimismalli tüüp:** *Voo nõudlus*

        See väli määratleb protsessi, milleks sortimismalli kasutatakse. Saadaval on järgmised väärtused:

        - **Voo nõudlus** – sortimismalli kasutatakse protsessi *Pane seinale* puhul. Seda malli tüüpi kasutatakse pakkimisjaama vahelejätmiseks ja varude töötlemiseks otse lainest. Seda tüüpi saate kasutada ainult juhul, kui **sortimise** voo töötlemise meetod on lisatud voo malli.
        - **Konteiner** – sortimismalli kasutatakse protsessi *Kaubaaluse loomine pärast pakkimist* jaoks. Seda malli tüüpi kasutatakse nende konteinerite töötlemiseks, mis on selles pakkimisjaamas suletud ja mis tuleb kaubaalustele sortida.

    - **Ladu:** *62*
    - **Asukoht:** *Sortimine*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Sortimise kontrollimine:** *Asukoha skannimine*

        See väli määratleb sortimise käigus nõutava kinnitamise. Saadaval on järgmised väärtused:

        - None
        - Litsentsiplaadi skannimine
        - Asukoha skannimine

    - **Loo töö asukoha sulgemisel:** *Jah*

        Kui selle suvandi väärtuseks on seatud *Jah*, kui asukoht on suletud, luuakse töö varude lõppsihtkohta teisaldamiseks. Kui väärtuseks on seatud *Ei*, komplekteeritakse varud asukoha sulgemisel kohe tellimusele.

    - **Asukoha määramine:** *Käsitsi*

        See väli määratleb asukoha määramise tüübi. Saadaval on järgmised väärtused:

        - **Käsitsi** – kasutaja peab alati näitama, millisesse asukohta varud sortida tuleb.
        - **Automaatne** – süsteem juhib varud võimaluse korral automaatselt asukohta, võttes aluseks sortimismalli jaotamised.

    - **Määra sortimise asukoha kriteeriumid:** *Kasuta ainult tühja asukohta*

        See väli juhib, kas nõudluse jaoks asukoha määramisel võetakse sortimise asukohtades juba olemasolevaid varusid arvesse. Saadaval on järgmised väärtused:

        - **Kasuta ainult tühja asukohta** – arvesse võetakse asukohti, millel on juba nendega seostatud varusid
        - **Eelda tühja asukohta** – mis tahes varusid, mis on juba asukohas, eiratakse määramise käigus. Kasutatakse kõiki saadaolevaid asukohti.

    - **Vooetapi kood:** *Sortimine*

        Kui funktsioon *Organisatsiooniülene vooetapi kood* on sisse lülitatud, peab vooetapi kood *Sortimine* olema samuti seadistatud vooetapi koodides.

    - **Sortimise asukoha automaatne sulgemine:** *Jah*

        Selle suvandi väärtuseks on seatud *Jah*, suletakse sortimise asukoht automaatselt, kui kõik asukohta tulevad tööd on lõpule viidud.

    - **Sortimise asukohtade arv:** *3*

        See väli määratleb süsteemi loodavate sortimise asukohtade maksimaalse arvu.

    - **Sortimise asukoha eesliide:** *SP-*

        See väli määratleb eesliite, mille süsteem määrab enne asukoha numbrit.

    - **Sortimise asukoha automaatne pakkimine:** *Jah*

        Kui selle suvandi väärtuseks on määratud *Jah*, pakitakse sortimise asukoha varud konteinerisse, kui asukoht on suletud.

    - **Pakkimisprofiili ID:** *Sortimine*

        See väli määratsel pakkimisprofiili, mida kasutatakse, kui sortimise asukoht pakitakse konteinerisse.

1. Valige toimingupaanil **Redigeeri päringut** selle sortimismalli puhul kasutatavate kriteeriumide määramiseks.
1. Valige päringu dialoogiboksis vahekaardil **Sortimine** suvand **Uus**, et lisada rida ja määrake siis järgmised väärtused.

    - **Tabel:** *Koormuse üksikasjad*
    - **Tuletatud tabel:** *Koormuse üksikasjad*
    - **Väli:** *Saadetise ID*
    - **Otsingusuund:** *Kasvav*

1. Valige nupp **OK**.
1. Teile võidakse kuvada järgmine teade: „Grupeerimine lähtestatakse, kas soovite jätkata?” Valige **Jah**.

    Toimingupaani nupp **Väljamineku sortimismalli piirid** muutub kättesaadavaks.

1. Valige toimingupaanil **Väljamineku sortimismalli piirid**.
1. Märkige ruut **Grupeeri välja alusel**, et grupeerida saadetise ID alusel.

    Selle sättega luuakse üks sortimise asukoht saadetise kohta, milleks on voos olev konteiner.

1. Valige nupp **OK**.

### <a name="wave-process-methods"></a>Voo töötlemise meetodid

1. Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**.
1. Valige toimingupaanil suvand **Meetodite uuesti loomine**.

    **Sortimise** meetod lisatakse saadaolevate meetodite loendisse ja sellele valitakse voo malli tüüp *Lähetamine*.

### <a name="wave-templates"></a>Voomallid

Redigeerige voo nõudluse sortimiseks kasutatavat voo malli.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Valige väljal **Voo malli tüüp** suvand *Lähetamine*.
1. Valige olemasolev mall **62 saadetise vaikemall**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Tehke kiirkaardil **Üldine** järgmised muudatused.

    - Määrake suvandi **Töötle voogu lattu vabastamisel** väärtuseks *Ei*.
    - Määrake suvandi **Määra avatud voogudele** väärtuseks *Jah*.

1. Seadistage kiirkaardil **Meetodid** meetod **Sortimine**.

    1. Valige ruudustikus **Ülejäänud meetodid** suvand **sortimine**.
    2. Valige meetodi **sortimine** ruudustikku **Valitud meetodid** teisaldamiseks paremnoole nupp.
    3. Valige ruudustikus **Valitud meetodid** suvand **sortimine**.
    4. Seadke välja **Vooetapi kood** väärtuseks *sortimine*.

1. Valige käsk **Salvesta**.

### <a name="mobile-device-menu-items"></a>Mobiilse seadme menüü-üksused

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake päises järgmised väärtused.

    - **Menüü-üksuse nimi:** *Sortimine*
    - **Pealkiri:** *Sortimine*
    - **Režiim:** *Kaudne*
    - **Kasuta olemasolevat tööd:** *Ei*

1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - **Tegevuse kood:** *Väljamineku sortimine*
    - **Protsessijuhendi kasutamine:** *Jah* (vaikeväärtus)
    - **Väljamineku sortimismalli ID:** *Voo sortimine*

1. Valige käsk **Salvesta**.

### <a name="mobile-device-menu"></a>Mobiilse seadme menüü

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige menüüde loendist suvand **Väljaminev**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Otsige üles ja valige ruudustikust **Saadaolevad menüüd ja menüü-üksused** äsja loodud menüü-üksus **Sortimine**.
1. Valige paremnoole nupp, et teisaldada **Sortimine** ruudustikku **Menüü struktuur**. Sedasi saate lisada menüü-üksuse menüüsse **Väljaminev**.
1. Valige käsk **Salvesta**.

### <a name="location-directives"></a>Asukohakorraldus

Pärast sortimise lõpule viimist loodud töö suunamiseks peate looma asukohakorraldused.

1. Minge jaotisse **Laohaldus \> Seadistus \> Asukohakorraldused**.
1. Valige väljal **Töökäsu tüüp** suvand *Sorditud varude komplekteerimine*.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake päises järgmised väärtused.

    - **Järjestus:** *1*
    - **Nimi:** *Pane laadimisukse juurde*

1. Määrake kiirkaardil **Asukohakorraldused** järgmised väärtused.

    - **Töö tüüp:** *Ladustamine*
    - **Tegevuskoht:** *6*
    - **Ladu:** *62*
    - **Korralduse kood:** jätke see väli tühjaks.
    - **Mitu SKU-d:** *Ei*

1. Valige **Salvesta**, et muuta kiirkaart **Read** kättesaadavaks.
1. Valige kiirkaardil **Read** suvand **Uus** ja seejärel seadke järgmised väärtused. Võtke vastu kõigi teiste väljade vaikeväärtused.

    - **Järjekorranumber:** *1*
    - **Alates kogusest:** *0*
    - **Koguseni:** *1000000*

1. Valige **Salvesta**, et muuta kiirkaart **Asukohakorralduse toimingud** kättesaadavaks.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Uus** ja seejärel seadke järgmised väärtused. Võtke vastu kõigi teiste väljade vaikeväärtused.

    - **Järjekorranumber:** *1*
    - **Nimi:** *Baydoor*

1. Valige **Salvesta**, et muuta kiirkaardi **Asukohakorralduse toimingud** nupp **Päringu redigeerimine** kättesaadavaks.
1. Valige kiirkaardil **Asukohakorralduse tegevused** suvand **Päringu redigeerimine**.
1. Otsige päringu dialoogiboksi vahekaardil **Vahemik** üles rida, kus välja **Väli** väärtuseks on seatud *Asukoht*. Määrake selle rea välja **Kriteeriumid** väärtuseks *Baydoor*.
1. Valige redigeerimise kinnitamiseks **OK**.

### <a name="work-classes"></a>Töö klassid

1. Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töö klassid**.
1. Valige toimingupaanil nupp **Uus**.
1. Määrake päises järgmised väärtused.

    - **Töö klassi ID:** *Sortimine*
    - **Kirjeldus:** *Sortimine*
    - **Töötellimuse tüüp:** *Sorditud varude komplekteerimine*

1. Valige käsk **Salvesta**.

### <a name="work-templates"></a>Töömallid

1. Avage jaotis **Laohaldus \> Töö \> Töömallid**.
1. Valige väljal **Töökäsu tüüp** suvand *Müügitellimused*.
1. Valige ruudustikus töömall **62 pakkimiseks komplekteerimine**.
1. Valige toimingupaanilt suvand **Tööpäise piirid**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Tühjendage real, kus välja **Välja nimi** väärtuseks on seatud *Saadetise ID*, märkeruut **Grupeeri selle välja alusel**.
1. Valige **Salvesta** ja seejärel sulgege dialoogiboks **Tööpäise piirid**.
1. Valige väljal **Töökäsu tüüp** suvand *Sorditud varude komplekteerimine*.
1. Valige töömalli loomiseks **Uus**.
1. Määrake jaotises **Ülevaade** järgmised väärtused. Võtke vastu kõigi teiste väljade vaikeväärtused.

    - **Töömall:** *Sorditud komplekteerimine*
    - **Töömalli kirjeldus:** *Sorditud komplekteerimine*

1. Valige **Salvesta**, et muuta jaotis **Töömalli üksikasjad** kättesaadavaks.
1. Loote kaks rida jaotises **Töömalli üksikasjad**. Valige **Uus** ja seejärel seadke järgmised väärtused 1. rea jaoks.

    - **Töö tüüp:** *Komplekteerimine*
    - **Kohustuslik:** valitud (= *Jah*)
    - **Töö klassi ID:** *Sortimine*

1. Valige **Uus** uuesti ja seejärel seadke järgmised väärtused 2. rea jaoks.

    - **Töö tüüp:** *Ladustamine*
    - **Kohustuslik:** valitud (= *Jah*)
    - **Töö klassi ID:** *Sortimine*

1. Valige käsk **Salvesta**.

## <a name="example-scenario"></a>Näidisstsenaarium

See stsenaarium simuleerib olukorda, kus ladu talletab asukohtades väikeseid kaupasid ja peab need enne lähetamist kastidesse pakkima, kuid pakkimisjaama funktsioon ei ole sobilik. Komplekteerimise kiiruse suurendamiseks komplekteerivad töötajad mitme kliendi ja erinevate aadressidega tellimusi üheaegselt. Kui komplekteerimine on lõpule viidud, saabuvad töötajad sorteerimise asukohta, kus komplekteeritud kaubad sorditakse nõutavate kriteeriumide alusel õigesse kasti. Selles näites kasutatakse saadetise ID-d õige kasti määratlemiseks, kuna igal saadetisel on erinev aadress. Kui koormuse kõik kaubad on pakitud ja sorditud saadetise järgi, teisaldatakse kastid vaheasukohta ja lõpuks laaditakse veokile.

Enne stsenaariumi käivitamist veenduge, et kõik standardsed ladustamise funktsioonid oleksid teie laos õigesti seadistatud. Sellel otstarbel kasutatakse standardset Contoso ladu *62*. Standardseid konfiguratsioone pole muudetud, peale selle, mida kirjeldatakse häälestuses.

### <a name="create-demand"></a>Nõudluse loomine

Enne selle funktsiooni demonstreerimist peate looma mõne nõudluse. Selles stsenaariumis loote kolm müügitellimust kolme erineva kliendi jaoks erinevate tarneaadresside simuleerimiseks. Sedasi loote kolm eraldi saadetist.

Enne müügitellimuste ja saadetiste loomist veenduge, et komplekteerimise asukohtadel oleks tellimuste kõikide kaupade jaoks piisavalt varusid. Vaadake üle asukohakorralduse seadistused, et kinnitada müügitellimuse komplekteerimiseks kasutatavad komplekteerimise asukohad. Kui peate korrigeerima varusid, saate luua käsitsi liikumisi, kasutada täiendamist või kasutada mis tahes muud voogu. Seejärel reserveerige varud.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. 1 tellimuse müügitellimuse loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Klient:** *US-001*
    - **Ladu:** *62*

1. Valige nupp **OK**.
1. Kiirkaardile **Müügitellimuse read** lisatakse uus rida. Määrake järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *5*

1. Valige **Lisa rida**, et lisada teine rida ja seadke järgmised väärtused.

    - **Kauba kood:** *A0002*
    - **Kogus:** *10*

1. Korrake järgmisi etappe iga müügirea puhul, et reserveerida selle jaoks varud.

    1. Valige ruudustiku kohal oleva menüü **Varud** kiirkaardilt **Müügitellimuse read** suvand **Reserveerimine**.
    1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.
    1. Valige käsk **Salvesta**.

1. 2 tellimuse müügitellimuse loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Klient:** *US-004*
    - **Ladu:** *62*

1. Valige nupp **OK**.
1. Kiirkaardile **Müügitellimuse read** lisatakse uus rida. Määrake järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *7*

1. Valige **Lisa rida**, et lisada teine rida ja seadke järgmised väärtused.

    - **Kauba kood:** *A0002*
    - **Kogus:** *3*

1. Korrake järgmisi etappe iga müügirea puhul, et reserveerida selle jaoks varud.

    1. Valige ruudustiku kohal oleva menüü **Varud** kiirkaardilt **Müügitellimuse read** suvand **Reserveerimine**.
    1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.
    1. Valige käsk **Salvesta**.

1. 3 tellimuse müügitellimuse loomiseks valige **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Klient:** *US-007*
    - **Ladu:** *62*

1. Valige nupp **OK**.
1. Kiirkaardile **Müügitellimuse read** lisatakse uus rida. Määrake järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *8*

1. Müügirea varude reserveerimiseks järgige neid etappe.

    1. Valige ruudustiku kohal oleva menüü **Varud** kiirkaardilt **Müügitellimuse read** suvand **Reserveerimine**.
    1. Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii** ja seejärel sulgege leht.
    1. Valige käsk **Salvesta**.

Viige lõpule järgmine protseduur, et vabastada kõik müügitellimused lattu. Luuakse kolm erinevat saadetist. Seejärel saate lisada kõik kolm saadetist ühte uude voogu.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige ruudustikus esimene enda loodud müügitellimus.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Saate teabesõnumi, mis näitab loodud voo ID-d ja saadetise ID-d.

1. Korrake eelmisi etappe, et vabastada 2. ja 3. müügitellimus lattu. Pange tähele, et saadud teabesõnum näitab, et saadetis on lisatud voogu, mis loodi 1. müügitellimuse väljastamisel.
1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Valige voo ID, mis loodi müügitellimuse väljastamisel, et avada leht **Vood**. Sellel lehel kuvatakse voo üksikasjad. Kiirkaardil **Voo read** kuvatakse loodud saadetised.

    Nüüd peate looma töö, et teisaldada kaubad komplekteerimise asukohtadest sortimise asukohta.

1. Klõpsake toimingupaanil suvandit **Töötlemine**.

    Voo töötlemisel kasutab sortimise meetod sortimismalli varude määrmiseks sortimise asukohtadesse. Kui voo töötlemine on lõpule viidud, kuvatakse teabesõnum, mis teatab, et voog on sisestatud ja töö on loodud.

1. Valige toimingupaani vahekaardi **Voog** grupis **Seotud teave** suvand **Töö**, et kuvada loodud tööd. Märkige üles töö ID.
1. Avage jaotis **Laohaldus \> Pakkimine ja konteinerisse määramine \> Väljamineku sortimise asukoha määramised**.
1. Vasakpoolses veerus saate kuvada iga saadetise jaoks loodud väljamineku sortimise asukohta.
1. Kiirkaardil **Sortimise asukoha kriteeriumid** saate kuvada selle asukoha saadetise ID-d.

Loodi üks töö ID, et teisaldada varud komplekteerimise asukohtadest sortimise asukohta. Töö lõpule viimiseks vajate töö ID-d, mis loodi voo töötlemisel.

### <a name="sales-order-picking-to-the-sorting-location"></a>Müügitellimuse komplekteerimine sortimise asukohta

1. Logige mobiilirakendusse lao *62* töötajana sisse.
1. Valige peamenüüs suvand **Väljaminev**.
1. Valige menüüs **Väljaminev** suvand **Müügi komplekteerimine**.
1. Valige väli **ID** ja seejärel sisestage voo töötlemisest pärineva töö ID.
1. Kinnitage kirje.

    Järgmisena palutakse teil sisestada sihtidentifitseerimisnumber (LP). Pange tähele, et 1. müügitellimuse 1. rida tuleb komplekteerida ja lisada sihtidentifitseerimisnumbrile. Kuvatakse kaubakood, kogus, kauba kirjeldus ja komplekteerimise asukoht.

1. Sisestage väljale **Siht-LP** identifitseerimisnumber.

    Peate komplekteerima kõik read, mis loodi töödeldud voost samale sihtidentifitseerimisnumbrile.

1. Kinnitage kirje.

    Mobiilirakendus esitab nüüd lehtede kogumi **Komplekteerimine**, mis suunavad teid komplekteerimise asukohta ning komplekteerimiseks vajalikule kaubale ja kogusele. Pärast komplekteeritud kauba identifitseerimisnumbrile lisamist peate kinnitama komplekteerimise töö. Viimane leht on töö komplekteeritud kaupade panemiseks sortimise asukohta.

1. Kinnitage esimene komplekteerimise töö.
1. Kuvatakse järgmine komplekteerimise töö. Kinnitage komplekteerimine.
1. Jätkake järelejäänud komplekteerimise tööde kinnitamist.
1. Viimane etapp on panemise töö lõpule viimine. Kinnitage kõrvalepanek sortimise asukohta.

    Teile kuvatakse teade „Töö lõpule viidud”.

1. Väljuge mobiilirakenduse suvandist **Müügi komplekteerimine**.

### <a name="sortingput-to-wall"></a>Sortimine/pane seinale

Kui kõik varud on pandud sortimise asukohta, tuleb need sortida õigesse sortimise paigutusse.

1. Logige mobiilirakendusse sisse.
1. Valige peamenüüs suvand **Väljaminev**.
1. Valige menüüs **Väljaminev** suvand **Sortimine**, et alustada kaupade sortimist.
1. Sisestage väljale **LP/CON** komplekteeritud müügitellimuse töö sihtidentifitseerimisnumber.
1. Kinnitage kirje.
1. Sisestage esimesena sorditava kauba kood.
1. Süsteem määratleb esimese sortimise asukoha, mida tuleks kuvada. Kinnitage sortimise asukoht.
1. Teil palutakse määrata identifitseerimisnumber sortimise asukohale. Valige väli **LP**, sisestage identifitseerimisnumbr ja kinnitage kirje.

    Kuna sortimise asukoht on seostatud saadetise ID-ga, sordite komplekteeritud kaubad väljaminevale saadetisele ja müügitellimusele omasele identifitseerimisnumbrile.

    Järgmisel lehel kuvatakse kauba ID, kogus, sortimise asukoha ID ja identifitseerimisnumbri ID-d „alates” (komplekteerimine) ja „kuni” (sortimine). Sellel lehel olev teave juhendab teid sortima määratud kauba ja kogused komplekteerimise identifitseerimisnumbrilt sortimise identifitseerimisnumbrile.

1. Kinnitage sortimise asukoht.
1. Sortige kaubad esimeses sortimise asukohas. Kui olete lõpetanud, suunab süsteem teid järgmisse sortimise asukohta.
1. Korrake seda protsessi töökäsu kõigi komplekteeritud ridade puhul. Seda protsessi tuleks kasutada ka juhul, kui on mitu sama kaubakoodiga komplekteerimise rida.

    Kui kordate seda protsessi kõigi kaupade puhul, hindab süsteem kriteeriume järgmisest skannitud kaubast (töörida) ja määrab, millisesse sortimise asukohta see tuleks panna. Teid suunatakse automaatselt kaupa õigesse sortimise asukohta panema. Sõltuvalt kinnituse seadistusest, suunatakse teid kinnitama seda tegevust asukoha numbri ja identifitseerimisnumbri ID sisestamisega.

    > [!NOTE]
    > Kui automaatne sortimine on sisse lülitatud, ei ole käsitsi alistamine saadaval.

1. Kui olete lõpetanud, avage rakenduses Microsoft Dynamics 365 Supply Chain Management leht **Väljamineku sortimise asukoha määramised**, et vaadata üle asukohtade olek.

    - Kui asukohad suletakse automaatselt, valige **Kuva suletud** suletud asukohtade kuvamiseks.
    - Pange tähele, et kuvataksesortimise asukoha kanded. Kuvatakse asukoha kaudu töödeldud kaup ja kogus.

    Kui seadistate väljamineku sortimismalli, seadke suvandi **Sortimise asukoha automaatne sulgemine** väärtuseks *Jah*. Seega, asukoht suletakse automaatselt pärast sellele viimaste eeldatavate varude panemist. Sortimise asukohtade olek on **Suletud** ja töö on loodud, et teisaldada sorditud varud asukohta *Baydoor*.

1. Viige sorditud varude komplekteerimise töö lõpule, et teisaldada varud lähetuse asukohta. Kui varud on valmis, kinnitage need lähetuseks.

> [!NOTE]
> Sorditud varude komplekteerimise töö õigesti töötlemiseks peaks teisaldamise ja laadimise protsessis kasutama mobiilse seadme menüü-üksust, millel on tööklassi ID seal, kus välja **Töökäsu tüüp** väärtuseks on seatud *Sorditud varude komplekteerimine*.

### <a name="manually-close-a-position-optional"></a>Asukoha käsitsi sulgemine (valikuline)

Kui sortimise asukohti on vaja käsitsi sulgeda, peab väljamineku sortimismalli suvandi **Sortimise asukoha automaatne sulgemine** väärtuseks olema *Ei* ja sulgemine tuleb teha enne, kui varusid saab teisaldada laadimisukse piirkonda. Asukohti saab sulgeda mitmel viisil.

- Laorakenduse kaudu.

    - Kasutaja saab skannida ühte kaupa, mis on juba asukohas ja seejärel valida asukoha sulgemiseks **Sule**.
    - Kui kasutaja skannib konteinerit, mis on juba sorditud konteiner, kuvatakse tõrketeade. Kuid kasutaja saab siiski jätkata asukoha sulgemisega.

- Microsoft Dynamics 365 Supply Chain Managementi lehe **Väljamineku sortimise asukoha määramised** kaudu.

    - Kasutaja saab valida väljamineku sortimise asukoha kirje ja seejärel valida toimingupaanil **Sule asukoht**.

## <a name="tips"></a>Näpunäited

- Ku kaup on juba määratud ühte asukohta, ei saa seda mujale teisaldada. Süsteem hindab kogust, kui palju ühest kaubast tuleks kindlasse asukohta panna.
- Sortimismalli saab konfigureerida automaatselt konteinereid looma asukohtade sulgemisel. See lähenemine loob standardse konteineri ID struktuuri määratud pakkimise profiili põhjal.

> [!IMPORTANT]
> Kui liikumise töö on loodud sortimise asukohast, ei tohi tööd tühistada. Vastasel juhul kustutatakse asukoht ja selles olevad konteinerid süsteemist ja need pole edasiseks töötlemiseks saadaval. Samuti eemaldatakse varud.
